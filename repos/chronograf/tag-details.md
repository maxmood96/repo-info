<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.8`](#chronograf1108)
-	[`chronograf:1.10.8-alpine`](#chronograf1108-alpine)
-	[`chronograf:1.7`](#chronograf17)
-	[`chronograf:1.7-alpine`](#chronograf17-alpine)
-	[`chronograf:1.7.17`](#chronograf1717)
-	[`chronograf:1.7.17-alpine`](#chronograf1717-alpine)
-	[`chronograf:1.8`](#chronograf18)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:1.8.10`](#chronograf1810)
-	[`chronograf:1.8.10-alpine`](#chronograf1810-alpine)
-	[`chronograf:1.9`](#chronograf19)
-	[`chronograf:1.9-alpine`](#chronograf19-alpine)
-	[`chronograf:1.9.4`](#chronograf194)
-	[`chronograf:1.9.4-alpine`](#chronograf194-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.10`

```console
$ docker pull chronograf@sha256:42e7b310399e57126053f3ff8eb551290b942ebbd8fd08186af03cfce512bbff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:1cc1ed9e94b3ad2e494e692082e3b43563ea6ec705fea568e9f206a3fb354ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920250cb93c814717f4751bbba4fb577f76a26a1f64057d21886264b4e1caf02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Mon, 29 Dec 2025 23:49:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:49:11 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:49:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:49:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7057b2c1916424b64a310962c344f1e3d9fa16300cda4db1d26fdc7439e56756`  
		Last Modified: Mon, 29 Dec 2025 23:49:29 GMT  
		Size: 7.9 MB (7878772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a516a78eb77c9789463954352a6bd5993aa13becbccde9d2d8215e201f2eea`  
		Last Modified: Mon, 29 Dec 2025 23:49:39 GMT  
		Size: 49.3 MB (49276671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f97085fb5a443724217d349b2d8b1884db62fc9ca7e8303b30814d215940e23`  
		Last Modified: Mon, 29 Dec 2025 23:49:29 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d46904c5a259d0e15ed3faf2c27ec708db13309dadfaf70406d685205230ec`  
		Last Modified: Mon, 29 Dec 2025 23:49:28 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607c0a53eaa400fcaf77a159c0ebe3ccd2af3acfb7ae6b7c0c91e52b7306ce73`  
		Last Modified: Mon, 29 Dec 2025 23:49:28 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:29e7891012d3d0014535dcc6e053da44fa1e928261e29856dd7dc9cf4cd02ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb6fc9e83e9b63386e39544eb7ba045eb9aa039d838a1af3a819db267063a0d`

```dockerfile
```

-	Layers:
	-	`sha256:bf9598b24cf90f9798d49be52d65a67303a38bc6a241873acd661b01dd6b39b7`  
		Last Modified: Tue, 30 Dec 2025 01:39:14 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c11679793b892f0d7a511fc980ffd1b3163f784bd5ecad1e8bbc77fb4e3fa2ed`  
		Last Modified: Tue, 30 Dec 2025 01:39:15 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:5614c0bce8750e0a6ea25194574cb8ef466e43f179f2169908d577fccbd53182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d435c6fe46ecb356e0a2b8f6e048091c0724a76c5900eb599b4058fd507bd66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 30 Dec 2025 00:38:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 30 Dec 2025 00:38:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 30 Dec 2025 00:38:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 00:38:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e76d25710d4436332b21775b55108e030e850f8146d1ca815f54043af8e4a0`  
		Last Modified: Tue, 30 Dec 2025 00:39:02 GMT  
		Size: 6.5 MB (6508147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a393dca982eab829dea2ecfdb75f004718b35ae36a9e097b5e7fa5c59c942adf`  
		Last Modified: Tue, 30 Dec 2025 00:39:06 GMT  
		Size: 45.6 MB (45621877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11fc5525ed12fc13ffc16e5beff72a153f027c5425ca12e6cbdda700d5596f`  
		Last Modified: Tue, 30 Dec 2025 00:39:01 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013ca9dd2d86195b2b731de9e069dcc979e87f76bbca8fa403669645258cdb8f`  
		Last Modified: Tue, 30 Dec 2025 00:39:01 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3301abba1bc74163e7254fd94c820ffe4dfa27122f5fa0cab1d9e5d959258b`  
		Last Modified: Tue, 30 Dec 2025 00:39:01 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:5088632808249678c5bb72c45655c939eb2596980edd61e6303628c03d26f121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a120d74c8961bde2438b31b6d73d722b88bf37ac013d7b37f2c9a511c2e1f7`

```dockerfile
```

-	Layers:
	-	`sha256:c18b311f1a79bbfcef122eddccc948baccbc699398d7f8ff36e5a2059ea0bf57`  
		Last Modified: Tue, 30 Dec 2025 04:38:51 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19a85c5833ea81731c8d12a73fd9344d8c9e3fbe2146d5ef676068662d4741f`  
		Last Modified: Tue, 30 Dec 2025 04:39:32 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ab396a4c9adf88108e26c794d4ab01dd533db1444dd50649bf676883e7465120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4b5034cdadd1d2b5a2c88cf8ee5e0ec580e11efe42ae592260e693e255a784`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Mon, 29 Dec 2025 23:49:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:49:32 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:49:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:49:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcd6af1d78457dbf8666584d3e8efb337b6ee4b89cf5915ce792d94ded22f03`  
		Last Modified: Mon, 29 Dec 2025 23:49:48 GMT  
		Size: 7.7 MB (7691849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c987fc54d10a70e2e7b896f43d6350cf278bb493022a35b39852562ef07b0ee4`  
		Last Modified: Mon, 29 Dec 2025 23:49:50 GMT  
		Size: 47.1 MB (47066825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08a9a785a4af6a10bb264b846f4c33616d2190d1ed19bff9ece4bbf6c9a286`  
		Last Modified: Mon, 29 Dec 2025 23:49:47 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e0c003b8e1c41407fd527be5262eb0c6c4c105d182f3d085a269f9a9f01a13`  
		Last Modified: Mon, 29 Dec 2025 23:49:47 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74ffbe7104d2b8a27b2491cdef1680e1cdf61636f9fec7405161b6695ca737a`  
		Last Modified: Mon, 29 Dec 2025 23:49:47 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:fd1aae3c0fbe962e4d2745c2a7c54b2ce1237044bb08423ce6953c280f21ca51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b195f0729c60f9e35a9810b73191018a373e8b4bf85657709707eaa03849f5`

```dockerfile
```

-	Layers:
	-	`sha256:8b0d9859a1a3b8dd2bd74f53ca6375ab8d51b7a8b726a9104c0c2357525207cf`  
		Last Modified: Tue, 30 Dec 2025 04:39:39 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc22d9db6ba372c2eefdc390892c1f7fbaec3094e945d01556fee201a37a5ca`  
		Last Modified: Tue, 30 Dec 2025 04:39:40 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:efc72c285cae492b0fb820a7794f2da69a70ef77caa8d28282e0df6f79856029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:08463b31a0a2617a51e230161f997b525214640155e291a423ae53004330c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32700225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af178eb7af41f52d85b69957fc583d381f6a24a9e604b40818766ecf3004a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Mon, 08 Dec 2025 02:53:47 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Mon, 08 Dec 2025 02:53:50 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Mon, 08 Dec 2025 02:53:49 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd3236bd7a2263357f0c7258a9a36c7fef283fd9f58f17f5fc2cbfa8330df313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 KB (268238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808a56c94ce865ff68fe325760f90b15b31758031ea028455935f57e4d2afe56`

```dockerfile
```

-	Layers:
	-	`sha256:d62aac69b78bc656cc8510a0566537353a4cda897cdaf124ca24ad68c0fa7fb1`  
		Last Modified: Mon, 08 Dec 2025 03:44:43 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Mon, 08 Dec 2025 03:44:44 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.8`

```console
$ docker pull chronograf@sha256:42e7b310399e57126053f3ff8eb551290b942ebbd8fd08186af03cfce512bbff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.8` - linux; amd64

```console
$ docker pull chronograf@sha256:1cc1ed9e94b3ad2e494e692082e3b43563ea6ec705fea568e9f206a3fb354ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920250cb93c814717f4751bbba4fb577f76a26a1f64057d21886264b4e1caf02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Mon, 29 Dec 2025 23:49:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:49:11 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:49:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:49:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7057b2c1916424b64a310962c344f1e3d9fa16300cda4db1d26fdc7439e56756`  
		Last Modified: Mon, 29 Dec 2025 23:49:29 GMT  
		Size: 7.9 MB (7878772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a516a78eb77c9789463954352a6bd5993aa13becbccde9d2d8215e201f2eea`  
		Last Modified: Mon, 29 Dec 2025 23:49:39 GMT  
		Size: 49.3 MB (49276671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f97085fb5a443724217d349b2d8b1884db62fc9ca7e8303b30814d215940e23`  
		Last Modified: Mon, 29 Dec 2025 23:49:29 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d46904c5a259d0e15ed3faf2c27ec708db13309dadfaf70406d685205230ec`  
		Last Modified: Mon, 29 Dec 2025 23:49:28 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607c0a53eaa400fcaf77a159c0ebe3ccd2af3acfb7ae6b7c0c91e52b7306ce73`  
		Last Modified: Mon, 29 Dec 2025 23:49:28 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:29e7891012d3d0014535dcc6e053da44fa1e928261e29856dd7dc9cf4cd02ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb6fc9e83e9b63386e39544eb7ba045eb9aa039d838a1af3a819db267063a0d`

```dockerfile
```

-	Layers:
	-	`sha256:bf9598b24cf90f9798d49be52d65a67303a38bc6a241873acd661b01dd6b39b7`  
		Last Modified: Tue, 30 Dec 2025 01:39:14 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c11679793b892f0d7a511fc980ffd1b3163f784bd5ecad1e8bbc77fb4e3fa2ed`  
		Last Modified: Tue, 30 Dec 2025 01:39:15 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:5614c0bce8750e0a6ea25194574cb8ef466e43f179f2169908d577fccbd53182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d435c6fe46ecb356e0a2b8f6e048091c0724a76c5900eb599b4058fd507bd66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 30 Dec 2025 00:38:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 30 Dec 2025 00:38:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 30 Dec 2025 00:38:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 00:38:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e76d25710d4436332b21775b55108e030e850f8146d1ca815f54043af8e4a0`  
		Last Modified: Tue, 30 Dec 2025 00:39:02 GMT  
		Size: 6.5 MB (6508147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a393dca982eab829dea2ecfdb75f004718b35ae36a9e097b5e7fa5c59c942adf`  
		Last Modified: Tue, 30 Dec 2025 00:39:06 GMT  
		Size: 45.6 MB (45621877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11fc5525ed12fc13ffc16e5beff72a153f027c5425ca12e6cbdda700d5596f`  
		Last Modified: Tue, 30 Dec 2025 00:39:01 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013ca9dd2d86195b2b731de9e069dcc979e87f76bbca8fa403669645258cdb8f`  
		Last Modified: Tue, 30 Dec 2025 00:39:01 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3301abba1bc74163e7254fd94c820ffe4dfa27122f5fa0cab1d9e5d959258b`  
		Last Modified: Tue, 30 Dec 2025 00:39:01 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:5088632808249678c5bb72c45655c939eb2596980edd61e6303628c03d26f121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a120d74c8961bde2438b31b6d73d722b88bf37ac013d7b37f2c9a511c2e1f7`

```dockerfile
```

-	Layers:
	-	`sha256:c18b311f1a79bbfcef122eddccc948baccbc699398d7f8ff36e5a2059ea0bf57`  
		Last Modified: Tue, 30 Dec 2025 04:38:51 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19a85c5833ea81731c8d12a73fd9344d8c9e3fbe2146d5ef676068662d4741f`  
		Last Modified: Tue, 30 Dec 2025 04:39:32 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ab396a4c9adf88108e26c794d4ab01dd533db1444dd50649bf676883e7465120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4b5034cdadd1d2b5a2c88cf8ee5e0ec580e11efe42ae592260e693e255a784`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Mon, 29 Dec 2025 23:49:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:49:32 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:49:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:49:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcd6af1d78457dbf8666584d3e8efb337b6ee4b89cf5915ce792d94ded22f03`  
		Last Modified: Mon, 29 Dec 2025 23:49:48 GMT  
		Size: 7.7 MB (7691849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c987fc54d10a70e2e7b896f43d6350cf278bb493022a35b39852562ef07b0ee4`  
		Last Modified: Mon, 29 Dec 2025 23:49:50 GMT  
		Size: 47.1 MB (47066825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08a9a785a4af6a10bb264b846f4c33616d2190d1ed19bff9ece4bbf6c9a286`  
		Last Modified: Mon, 29 Dec 2025 23:49:47 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e0c003b8e1c41407fd527be5262eb0c6c4c105d182f3d085a269f9a9f01a13`  
		Last Modified: Mon, 29 Dec 2025 23:49:47 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74ffbe7104d2b8a27b2491cdef1680e1cdf61636f9fec7405161b6695ca737a`  
		Last Modified: Mon, 29 Dec 2025 23:49:47 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:fd1aae3c0fbe962e4d2745c2a7c54b2ce1237044bb08423ce6953c280f21ca51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b195f0729c60f9e35a9810b73191018a373e8b4bf85657709707eaa03849f5`

```dockerfile
```

-	Layers:
	-	`sha256:8b0d9859a1a3b8dd2bd74f53ca6375ab8d51b7a8b726a9104c0c2357525207cf`  
		Last Modified: Tue, 30 Dec 2025 04:39:39 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc22d9db6ba372c2eefdc390892c1f7fbaec3094e945d01556fee201a37a5ca`  
		Last Modified: Tue, 30 Dec 2025 04:39:40 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.8-alpine`

```console
$ docker pull chronograf@sha256:efc72c285cae492b0fb820a7794f2da69a70ef77caa8d28282e0df6f79856029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:08463b31a0a2617a51e230161f997b525214640155e291a423ae53004330c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32700225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af178eb7af41f52d85b69957fc583d381f6a24a9e604b40818766ecf3004a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Mon, 08 Dec 2025 02:53:47 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Mon, 08 Dec 2025 02:53:50 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Mon, 08 Dec 2025 02:53:49 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd3236bd7a2263357f0c7258a9a36c7fef283fd9f58f17f5fc2cbfa8330df313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 KB (268238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808a56c94ce865ff68fe325760f90b15b31758031ea028455935f57e4d2afe56`

```dockerfile
```

-	Layers:
	-	`sha256:d62aac69b78bc656cc8510a0566537353a4cda897cdaf124ca24ad68c0fa7fb1`  
		Last Modified: Mon, 08 Dec 2025 03:44:43 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Mon, 08 Dec 2025 03:44:44 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:d6b4545a12b3b3e0c6a66075b5334ef6378874f5b1e946decbe6a79d6aeabcfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:f023e5accd6bc184fa4acaed238eeff659b9378833c389b4b56332ffe4d34fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4519cca69cfc55177f7c0d65e581c9ed844c6af4aaff64e4ef2ad00f35ad3a4e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:47:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:47:41 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 29 Dec 2025 23:47:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:47:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:47:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:47:41 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:47:41 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:47:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:47:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:47:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064513d2c2559da08b5da5dcf14107ab62cbd0d19c4106087580815458b34a9a`  
		Last Modified: Mon, 29 Dec 2025 23:48:00 GMT  
		Size: 4.2 MB (4209335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365150f2805dced07724af3eaa2f09c3f87470e1b88db6d5856e6814ead1d1cd`  
		Last Modified: Mon, 29 Dec 2025 23:48:03 GMT  
		Size: 34.7 MB (34738524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1b48a464e3a35b9301e3ed5e174bcdffe015dd980b38df7429b5760d86ad45`  
		Last Modified: Mon, 29 Dec 2025 23:47:59 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0319c2180698a4d3957e9641e563c7e1b807596ca8dad52ba0b2e07dbac46fb`  
		Last Modified: Mon, 29 Dec 2025 23:47:59 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063a9c05359855b0415c83e46ac304bdad0e4e96da8475ff145c331ffecbe324`  
		Last Modified: Mon, 29 Dec 2025 23:47:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:034909ab7ef33b987ce7e3632451fcf4a0c55dca9ee9c0ec95dcdbb65ecba9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc423ccdad4567b4af781cfcbfbc0d1acdfe18690b0995ac6a65f24f02a460a4`

```dockerfile
```

-	Layers:
	-	`sha256:6c1c8dc05cb40a6abcb4caea8bc2fb74f9259e5a51fb77455d486d649b15da68`  
		Last Modified: Tue, 30 Dec 2025 01:39:20 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba434287c3d6d2566c3b428048d223d5e94edc2134b6895b1921e36bac39668f`  
		Last Modified: Tue, 30 Dec 2025 01:39:21 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1b5fb8bcd53d41f671605c0b614a4a3ee4c3a96fd88bee41fdbefd2e54a4ea5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563befa5f66cea768d10af17eb3ad355453d33dc7b181b84410941b68b1f70d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:36:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 00:36:45 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 30 Dec 2025 00:36:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:36:45 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 30 Dec 2025 00:36:45 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 30 Dec 2025 00:36:45 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 30 Dec 2025 00:36:45 GMT
VOLUME [/var/lib/chronograf]
# Tue, 30 Dec 2025 00:36:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 00:36:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 00:36:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:157cb1ae1e97b073d55fa44e5e4ce17ccecf29dcfee2e34ca09a7de19793cf95`  
		Last Modified: Mon, 29 Dec 2025 22:25:27 GMT  
		Size: 25.5 MB (25546225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48eddb67d65ed3d24a2061ae344596c3fef7c057283b41725178552120cc4d6`  
		Last Modified: Tue, 30 Dec 2025 00:37:02 GMT  
		Size: 3.5 MB (3511645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3cbce731a109c472cb50aaab701124c79652295ebed6b95513b2073d107e8f`  
		Last Modified: Tue, 30 Dec 2025 00:37:05 GMT  
		Size: 33.1 MB (33097539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709517d2fe4ddcb259f53247e8f810380b563c563043d27d5dc977276af38756`  
		Last Modified: Tue, 30 Dec 2025 00:37:01 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10f1651b910fa97325d31a306d0c92c4098f3024752aed4a9cd8a53b453a5d5`  
		Last Modified: Tue, 30 Dec 2025 00:37:01 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6ca5d5b9a94cf2bbbd2d74c7e1c33cf2b014ae4d50a6b907c63b73ecb674fe`  
		Last Modified: Tue, 30 Dec 2025 00:37:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:5c4b8222514ace7104f9d6b93ad95c9107d1d1d01a6b222b36e1b3be4048e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e54c41d35117f2d5edcd1c55faf614244453871ec553041f5f0fce3051ec4eb`

```dockerfile
```

-	Layers:
	-	`sha256:af97c08722344f2d1dfa1a4801c53ec0fdea9a0ae7e9c9026f3a30c1a8a6d9e0`  
		Last Modified: Tue, 30 Dec 2025 04:39:01 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1465e803b9906db62c913cf74fdd692de2e29ae2bc98f34f7c695ddd91c38fd1`  
		Last Modified: Tue, 30 Dec 2025 04:39:02 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:4cdbe66669088a48d61cbb04ab4bf069d1ec2da4e356911d8200ff46f462b5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dff1181076e8efd4ba2aaa4db3760d5de5a370709dc02e60ff269e38afc545`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:48:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:48:22 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 29 Dec 2025 23:48:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:48:22 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:48:22 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:48:22 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:48:22 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:48:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:48:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:48:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055389dbea5d90c8d7b2e8742e34b3709a5f15e2020d1bfcf55ffdeae43e314a`  
		Last Modified: Mon, 29 Dec 2025 23:48:38 GMT  
		Size: 4.2 MB (4210630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c413d1e36f313b3dd7eac3e6f2a7be0198fcfb4f95b481e95c55e0bb16e90454`  
		Last Modified: Mon, 29 Dec 2025 23:48:40 GMT  
		Size: 33.2 MB (33238194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b398904e1318126b6efa0d26191ffc19f16f8e45ac283b1c73193fcf8dffe`  
		Last Modified: Mon, 29 Dec 2025 23:48:37 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7c00cdc86ac391bcf00452e9b451d516fa52b5b9633d3f1bc347deb9f4e86d`  
		Last Modified: Mon, 29 Dec 2025 23:48:37 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3cf4aeee9e6f07427d16db9187aed460afc2cc81d1b3e2811e04cda3c2289`  
		Last Modified: Mon, 29 Dec 2025 23:48:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:b958d24d8d0ad1a4f3f62b72a11e09dc4b36460d12b3631382f3d5ec58e553a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26044030e2df872bd8881b5131b3250748f54ae5e322ff66f96e4f9b287ee2fe`

```dockerfile
```

-	Layers:
	-	`sha256:1b367fc9911c25aa85683e654ee6853079f291c9479adef11400c6e793cd3e8a`  
		Last Modified: Tue, 30 Dec 2025 04:39:05 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f144f8c8c0ae3ab7b4711de5428c2639b8ee4a98ba094cc182da5d8d5487b3`  
		Last Modified: Tue, 30 Dec 2025 04:39:06 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:f9bf8a3a9499f5324ca9b5f428e7ecbf8a4714d366e8a7920a8d06292f7d0511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0e68a8f6a33cec3ad19c936e80df9706efc6f4a6651f78b3373920f503a90deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5704e6698a8163ec6cf9a9f4d2fc39455f7394b4b089fd3fe4fbbfcd3c84f5fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Tue, 09 Dec 2025 23:02:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053646d1ede74b4422e0751427c045b128d56b4d9c7521a34d9a3e2fd81f2fa6`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 290.8 KB (290771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fddb95d664d6dacdb2318596d88bdbacf9e5bde5abe2b7e4335d05288276ea`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 19.6 MB (19556558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f367635d83aeb5f5f554e62a06a02ad833c17339cf302d30013629399527c0`  
		Last Modified: Tue, 09 Dec 2025 23:02:45 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f90ee1715c3ce00ef0c8e4958732cd35aeb06708db0a00e83afbe1f17da89`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166e539db1f38a4aa1b578555a8c92c86979cbc08b8098fba9661f87ffe6167`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:bcbb31392ab3215af685b41ca6842da95b2e263604620ad5d7a30c80609bc543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862b2564bbbfa2013c4f206e9af5027911bf83448426df87b517b51fb5f596e0`

```dockerfile
```

-	Layers:
	-	`sha256:7d486241e7d5fad65401d86ed4cecac735dc744dd18c05a5530b79d0bc9ae6ac`  
		Last Modified: Thu, 25 Dec 2025 14:19:24 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87486fae9bd6ba27ac7806fc6b1c5c571f4d3de5fc46fd1b292df95f203bc24e`  
		Last Modified: Thu, 25 Dec 2025 14:19:24 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:d6b4545a12b3b3e0c6a66075b5334ef6378874f5b1e946decbe6a79d6aeabcfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:f023e5accd6bc184fa4acaed238eeff659b9378833c389b4b56332ffe4d34fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4519cca69cfc55177f7c0d65e581c9ed844c6af4aaff64e4ef2ad00f35ad3a4e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:47:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:47:41 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 29 Dec 2025 23:47:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:47:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:47:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:47:41 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:47:41 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:47:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:47:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:47:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064513d2c2559da08b5da5dcf14107ab62cbd0d19c4106087580815458b34a9a`  
		Last Modified: Mon, 29 Dec 2025 23:48:00 GMT  
		Size: 4.2 MB (4209335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365150f2805dced07724af3eaa2f09c3f87470e1b88db6d5856e6814ead1d1cd`  
		Last Modified: Mon, 29 Dec 2025 23:48:03 GMT  
		Size: 34.7 MB (34738524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1b48a464e3a35b9301e3ed5e174bcdffe015dd980b38df7429b5760d86ad45`  
		Last Modified: Mon, 29 Dec 2025 23:47:59 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0319c2180698a4d3957e9641e563c7e1b807596ca8dad52ba0b2e07dbac46fb`  
		Last Modified: Mon, 29 Dec 2025 23:47:59 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063a9c05359855b0415c83e46ac304bdad0e4e96da8475ff145c331ffecbe324`  
		Last Modified: Mon, 29 Dec 2025 23:47:59 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:034909ab7ef33b987ce7e3632451fcf4a0c55dca9ee9c0ec95dcdbb65ecba9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc423ccdad4567b4af781cfcbfbc0d1acdfe18690b0995ac6a65f24f02a460a4`

```dockerfile
```

-	Layers:
	-	`sha256:6c1c8dc05cb40a6abcb4caea8bc2fb74f9259e5a51fb77455d486d649b15da68`  
		Last Modified: Tue, 30 Dec 2025 01:39:20 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba434287c3d6d2566c3b428048d223d5e94edc2134b6895b1921e36bac39668f`  
		Last Modified: Tue, 30 Dec 2025 01:39:21 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1b5fb8bcd53d41f671605c0b614a4a3ee4c3a96fd88bee41fdbefd2e54a4ea5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563befa5f66cea768d10af17eb3ad355453d33dc7b181b84410941b68b1f70d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:36:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 00:36:45 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 30 Dec 2025 00:36:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:36:45 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 30 Dec 2025 00:36:45 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 30 Dec 2025 00:36:45 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 30 Dec 2025 00:36:45 GMT
VOLUME [/var/lib/chronograf]
# Tue, 30 Dec 2025 00:36:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 00:36:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 00:36:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:157cb1ae1e97b073d55fa44e5e4ce17ccecf29dcfee2e34ca09a7de19793cf95`  
		Last Modified: Mon, 29 Dec 2025 22:25:27 GMT  
		Size: 25.5 MB (25546225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48eddb67d65ed3d24a2061ae344596c3fef7c057283b41725178552120cc4d6`  
		Last Modified: Tue, 30 Dec 2025 00:37:02 GMT  
		Size: 3.5 MB (3511645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3cbce731a109c472cb50aaab701124c79652295ebed6b95513b2073d107e8f`  
		Last Modified: Tue, 30 Dec 2025 00:37:05 GMT  
		Size: 33.1 MB (33097539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709517d2fe4ddcb259f53247e8f810380b563c563043d27d5dc977276af38756`  
		Last Modified: Tue, 30 Dec 2025 00:37:01 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10f1651b910fa97325d31a306d0c92c4098f3024752aed4a9cd8a53b453a5d5`  
		Last Modified: Tue, 30 Dec 2025 00:37:01 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6ca5d5b9a94cf2bbbd2d74c7e1c33cf2b014ae4d50a6b907c63b73ecb674fe`  
		Last Modified: Tue, 30 Dec 2025 00:37:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:5c4b8222514ace7104f9d6b93ad95c9107d1d1d01a6b222b36e1b3be4048e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e54c41d35117f2d5edcd1c55faf614244453871ec553041f5f0fce3051ec4eb`

```dockerfile
```

-	Layers:
	-	`sha256:af97c08722344f2d1dfa1a4801c53ec0fdea9a0ae7e9c9026f3a30c1a8a6d9e0`  
		Last Modified: Tue, 30 Dec 2025 04:39:01 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1465e803b9906db62c913cf74fdd692de2e29ae2bc98f34f7c695ddd91c38fd1`  
		Last Modified: Tue, 30 Dec 2025 04:39:02 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:4cdbe66669088a48d61cbb04ab4bf069d1ec2da4e356911d8200ff46f462b5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dff1181076e8efd4ba2aaa4db3760d5de5a370709dc02e60ff269e38afc545`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:48:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:48:22 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 29 Dec 2025 23:48:22 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:48:22 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:48:22 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:48:22 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:48:22 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:48:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:48:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:48:22 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055389dbea5d90c8d7b2e8742e34b3709a5f15e2020d1bfcf55ffdeae43e314a`  
		Last Modified: Mon, 29 Dec 2025 23:48:38 GMT  
		Size: 4.2 MB (4210630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c413d1e36f313b3dd7eac3e6f2a7be0198fcfb4f95b481e95c55e0bb16e90454`  
		Last Modified: Mon, 29 Dec 2025 23:48:40 GMT  
		Size: 33.2 MB (33238194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b398904e1318126b6efa0d26191ffc19f16f8e45ac283b1c73193fcf8dffe`  
		Last Modified: Mon, 29 Dec 2025 23:48:37 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7c00cdc86ac391bcf00452e9b451d516fa52b5b9633d3f1bc347deb9f4e86d`  
		Last Modified: Mon, 29 Dec 2025 23:48:37 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3cf4aeee9e6f07427d16db9187aed460afc2cc81d1b3e2811e04cda3c2289`  
		Last Modified: Mon, 29 Dec 2025 23:48:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:b958d24d8d0ad1a4f3f62b72a11e09dc4b36460d12b3631382f3d5ec58e553a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26044030e2df872bd8881b5131b3250748f54ae5e322ff66f96e4f9b287ee2fe`

```dockerfile
```

-	Layers:
	-	`sha256:1b367fc9911c25aa85683e654ee6853079f291c9479adef11400c6e793cd3e8a`  
		Last Modified: Tue, 30 Dec 2025 04:39:05 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f144f8c8c0ae3ab7b4711de5428c2639b8ee4a98ba094cc182da5d8d5487b3`  
		Last Modified: Tue, 30 Dec 2025 04:39:06 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:f9bf8a3a9499f5324ca9b5f428e7ecbf8a4714d366e8a7920a8d06292f7d0511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:0e68a8f6a33cec3ad19c936e80df9706efc6f4a6651f78b3373920f503a90deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23499028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5704e6698a8163ec6cf9a9f4d2fc39455f7394b4b089fd3fe4fbbfcd3c84f5fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Tue, 09 Dec 2025 23:02:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053646d1ede74b4422e0751427c045b128d56b4d9c7521a34d9a3e2fd81f2fa6`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 290.8 KB (290771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fddb95d664d6dacdb2318596d88bdbacf9e5bde5abe2b7e4335d05288276ea`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 19.6 MB (19556558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f367635d83aeb5f5f554e62a06a02ad833c17339cf302d30013629399527c0`  
		Last Modified: Tue, 09 Dec 2025 23:02:45 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f90ee1715c3ce00ef0c8e4958732cd35aeb06708db0a00e83afbe1f17da89`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166e539db1f38a4aa1b578555a8c92c86979cbc08b8098fba9661f87ffe6167`  
		Last Modified: Tue, 09 Dec 2025 23:02:46 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:bcbb31392ab3215af685b41ca6842da95b2e263604620ad5d7a30c80609bc543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 KB (188744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862b2564bbbfa2013c4f206e9af5027911bf83448426df87b517b51fb5f596e0`

```dockerfile
```

-	Layers:
	-	`sha256:7d486241e7d5fad65401d86ed4cecac735dc744dd18c05a5530b79d0bc9ae6ac`  
		Last Modified: Thu, 25 Dec 2025 14:19:24 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87486fae9bd6ba27ac7806fc6b1c5c571f4d3de5fc46fd1b292df95f203bc24e`  
		Last Modified: Thu, 25 Dec 2025 14:19:24 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:7e6f1c387b56a6d3f4d84a34075dcd5ecd79043ade028772afeb7faf3717914a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:7ec714dbb260bbbf0e3cb33a7f2b08c0576207ed99d00564b4e74457f790a5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1deb0a8e8111e24e69cc9f6a154bc8db8fa6bdf93ea211fc463d04b6fcee2d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:48:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:48:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 29 Dec 2025 23:48:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:48:24 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:48:24 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:48:24 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:48:24 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:48:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:48:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:48:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc381980374846e1564cf8052774633d78a5087dede9f8a5859d44f4f97f091`  
		Last Modified: Mon, 29 Dec 2025 23:48:42 GMT  
		Size: 5.2 MB (5224232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73fc60ae02bea5aa460487efd2e51c7a509ab2757b5d4f85f82f542b0a248b9`  
		Last Modified: Mon, 29 Dec 2025 23:48:46 GMT  
		Size: 34.4 MB (34364312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b335230c7e26c20d732622b63555d3b35964dae8aa3e88b8162a1718ee35366`  
		Last Modified: Mon, 29 Dec 2025 23:48:40 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f78cf4d1a0f4dd5e720d86655f522c5e055ec0baa6469d548f9e59b500a832`  
		Last Modified: Mon, 29 Dec 2025 23:48:40 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3cf4aeee9e6f07427d16db9187aed460afc2cc81d1b3e2811e04cda3c2289`  
		Last Modified: Mon, 29 Dec 2025 23:48:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:a407f3becd233b5ddba29f412bc1de55ffb935c48c4fdcef91ac65801a1a92ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c552a566d34529614b2a7bba4d011558bad433c96f04859866f563c60d18c996`

```dockerfile
```

-	Layers:
	-	`sha256:e729864db236b541e4ece444bacb39bfd698417de7ba937db8178067fbd821e4`  
		Last Modified: Tue, 30 Dec 2025 01:39:28 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaa686a1093f195f0e5775e7d89030e3951c51b2cf35e892a3eab3265daafd23`  
		Last Modified: Tue, 30 Dec 2025 01:39:29 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d2e4f9cda047e68ac61ed5ef8f922a3ece3a8a48943ea85773c48f186756e14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679b044a552842dc10b545f6a66bc0b77c0c5ce76de12122d727728b749d49d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:36:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 00:36:59 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 30 Dec 2025 00:36:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:36:59 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 30 Dec 2025 00:36:59 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 30 Dec 2025 00:36:59 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 30 Dec 2025 00:36:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 30 Dec 2025 00:36:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 00:36:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 00:36:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:157cb1ae1e97b073d55fa44e5e4ce17ccecf29dcfee2e34ca09a7de19793cf95`  
		Last Modified: Mon, 29 Dec 2025 22:25:27 GMT  
		Size: 25.5 MB (25546225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e783097c4448088ae803a874dd8dbb6690afbc9252e7bcae21c86c0533b404`  
		Last Modified: Tue, 30 Dec 2025 00:37:16 GMT  
		Size: 4.5 MB (4490237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7fdbc11f18d41085686af9ea8a1adf173bd634f586ae7611293db8e1bbfd7a`  
		Last Modified: Tue, 30 Dec 2025 00:37:20 GMT  
		Size: 32.5 MB (32534928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba2db22fcdf7a2690de4f5800f0562f78332d9811bb308fefc8bac7dbf51ab7`  
		Last Modified: Tue, 30 Dec 2025 00:37:15 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1bbdac9d0e497ddb23df6677c7b1b578170aa11ee2f9a652291909329451c4`  
		Last Modified: Tue, 30 Dec 2025 00:37:15 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37812ba544717332da030a103174b03e488ccebdd25a4e0a308960cd8063fe28`  
		Last Modified: Tue, 30 Dec 2025 00:37:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:1cf8e9d9138744b68218c787fcbac694ba491d794687c696cd62ff77855e9e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c39c0926bc7cac0b186ad75bedde2f7ffcaefad9c635d7c795d3c2893d3a0a3`

```dockerfile
```

-	Layers:
	-	`sha256:8edd7c843a1819304942de0c3467a55562aa90b171eff38b2441d744b9713275`  
		Last Modified: Tue, 30 Dec 2025 04:39:13 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e31ca8d6d8a110040ea8d24b2209a8cfb4191308ca353c8928268320978ebea`  
		Last Modified: Tue, 30 Dec 2025 04:39:13 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9423c8280cf7c69da396753e3c48f64006b96922780b0a29bbaa5e492d52a103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fdedf8612218b249341309b4432d9be3e4cf5e2fc51bd0975b4f8531e5d8e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:48:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:48:42 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 29 Dec 2025 23:48:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:48:42 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:48:42 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:48:42 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:48:42 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:48:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:48:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:48:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7958a3e1061e0fa5e50b42b6eb97cb617ab31544b631a44383dc0a12b61e867a`  
		Last Modified: Mon, 29 Dec 2025 23:48:58 GMT  
		Size: 5.2 MB (5208160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54b303d3201682971e7df52d7907c8927f86f30e66556e2e05d5f15ef16ce24`  
		Last Modified: Mon, 29 Dec 2025 23:49:00 GMT  
		Size: 32.4 MB (32429494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc4699c9c926cfddab87e624399bf4bbe7167a64a38ab46da585275a60b342b`  
		Last Modified: Mon, 29 Dec 2025 23:48:58 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8f5b9dd518f5d5167d0adbb8b60a056f21947e6ecefb0142577cf605179ca1`  
		Last Modified: Mon, 29 Dec 2025 23:48:57 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb63949f91b01d8dcdf4f0dc6079da770bb10fd3dab52a30a3faea006b1ef0ba`  
		Last Modified: Mon, 29 Dec 2025 23:48:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:527e9ccd38be93db8832602864c76be3e5a90d5ee84143f8e35f705bfad554e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3aa2e7db17b6009960b0c3677db4154d6f086b02dd92641aac3a8376d88858d`

```dockerfile
```

-	Layers:
	-	`sha256:10a1915487b95f99d8a3bb459c4537835deccfa613ec4679f265a284cc3ed6cd`  
		Last Modified: Tue, 30 Dec 2025 04:39:17 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f89c5d0b2857218c647d2ac1756b187924601e5bff17e91c899b5f711cddaab`  
		Last Modified: Tue, 30 Dec 2025 04:39:17 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:8f246b11bed20824de500e732e0e0c1a9df2e2adcf60340444da2c4d2e7d83bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fae84330ab9094200744d44140ff3695efc2a2085251cd4066103541bffbe5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23146498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6035189b6fd6fc001306a038b9c5678123af0b1f907f2a31efe3e96b3b689b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaabc96984af774b48937345c7cc275e3315d3a9a42aeb994f6946de24556be`  
		Last Modified: Mon, 08 Dec 2025 07:57:14 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff81f10ae11b38f809feee3b7a44d508880916016658ca83647ff9d1c294aba`  
		Last Modified: Mon, 08 Dec 2025 07:57:14 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cf4bd3a04c4941275f4aa1db1887c01bcdadeb973d9c95d34bc905b974dce`  
		Last Modified: Mon, 08 Dec 2025 07:57:15 GMT  
		Size: 19.2 MB (19204014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4732a865d574eb12cd7075d139d6bbd7d47fea3c367baf1a1f56ff51506906fb`  
		Last Modified: Mon, 08 Dec 2025 07:57:22 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0733dea6fe6d3cf04ef8c52dec6540501fbf0e79664e84fd00853fab32410e15`  
		Last Modified: Mon, 08 Dec 2025 07:57:25 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58005a9627e476ca3528af5a14e30f0d4549afa8e314dcde58ee7ec5fd6671`  
		Last Modified: Mon, 08 Dec 2025 07:57:47 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:07f09e7f03af9efcf88f89d7ad0f207d0e5ab57b9423663591e3c7aa0b3bc6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 KB (245253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779ee449137493a2aca535f4363cae748d5a6c40f2c306362a97daf2d51bf6b`

```dockerfile
```

-	Layers:
	-	`sha256:4376140096bd52be7b1473ee7e7d625fff88ab2e731a2d509ed5b7861eab79fe`  
		Last Modified: Tue, 09 Dec 2025 03:48:01 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61687d781240db246500ccffe6dc5608d9be7a5e7c809173a2694ffec485f7c3`  
		Last Modified: Tue, 09 Dec 2025 03:48:01 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:7e6f1c387b56a6d3f4d84a34075dcd5ecd79043ade028772afeb7faf3717914a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:7ec714dbb260bbbf0e3cb33a7f2b08c0576207ed99d00564b4e74457f790a5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1deb0a8e8111e24e69cc9f6a154bc8db8fa6bdf93ea211fc463d04b6fcee2d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:48:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:48:24 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 29 Dec 2025 23:48:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:48:24 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:48:24 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:48:24 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:48:24 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:48:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:48:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:48:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc381980374846e1564cf8052774633d78a5087dede9f8a5859d44f4f97f091`  
		Last Modified: Mon, 29 Dec 2025 23:48:42 GMT  
		Size: 5.2 MB (5224232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73fc60ae02bea5aa460487efd2e51c7a509ab2757b5d4f85f82f542b0a248b9`  
		Last Modified: Mon, 29 Dec 2025 23:48:46 GMT  
		Size: 34.4 MB (34364312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b335230c7e26c20d732622b63555d3b35964dae8aa3e88b8162a1718ee35366`  
		Last Modified: Mon, 29 Dec 2025 23:48:40 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f78cf4d1a0f4dd5e720d86655f522c5e055ec0baa6469d548f9e59b500a832`  
		Last Modified: Mon, 29 Dec 2025 23:48:40 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3cf4aeee9e6f07427d16db9187aed460afc2cc81d1b3e2811e04cda3c2289`  
		Last Modified: Mon, 29 Dec 2025 23:48:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:a407f3becd233b5ddba29f412bc1de55ffb935c48c4fdcef91ac65801a1a92ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c552a566d34529614b2a7bba4d011558bad433c96f04859866f563c60d18c996`

```dockerfile
```

-	Layers:
	-	`sha256:e729864db236b541e4ece444bacb39bfd698417de7ba937db8178067fbd821e4`  
		Last Modified: Tue, 30 Dec 2025 01:39:28 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaa686a1093f195f0e5775e7d89030e3951c51b2cf35e892a3eab3265daafd23`  
		Last Modified: Tue, 30 Dec 2025 01:39:29 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d2e4f9cda047e68ac61ed5ef8f922a3ece3a8a48943ea85773c48f186756e14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679b044a552842dc10b545f6a66bc0b77c0c5ce76de12122d727728b749d49d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:36:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 00:36:59 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 30 Dec 2025 00:36:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:36:59 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 30 Dec 2025 00:36:59 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 30 Dec 2025 00:36:59 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 30 Dec 2025 00:36:59 GMT
VOLUME [/var/lib/chronograf]
# Tue, 30 Dec 2025 00:36:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 00:36:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 00:36:59 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:157cb1ae1e97b073d55fa44e5e4ce17ccecf29dcfee2e34ca09a7de19793cf95`  
		Last Modified: Mon, 29 Dec 2025 22:25:27 GMT  
		Size: 25.5 MB (25546225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e783097c4448088ae803a874dd8dbb6690afbc9252e7bcae21c86c0533b404`  
		Last Modified: Tue, 30 Dec 2025 00:37:16 GMT  
		Size: 4.5 MB (4490237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7fdbc11f18d41085686af9ea8a1adf173bd634f586ae7611293db8e1bbfd7a`  
		Last Modified: Tue, 30 Dec 2025 00:37:20 GMT  
		Size: 32.5 MB (32534928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba2db22fcdf7a2690de4f5800f0562f78332d9811bb308fefc8bac7dbf51ab7`  
		Last Modified: Tue, 30 Dec 2025 00:37:15 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1bbdac9d0e497ddb23df6677c7b1b578170aa11ee2f9a652291909329451c4`  
		Last Modified: Tue, 30 Dec 2025 00:37:15 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37812ba544717332da030a103174b03e488ccebdd25a4e0a308960cd8063fe28`  
		Last Modified: Tue, 30 Dec 2025 00:37:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:1cf8e9d9138744b68218c787fcbac694ba491d794687c696cd62ff77855e9e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c39c0926bc7cac0b186ad75bedde2f7ffcaefad9c635d7c795d3c2893d3a0a3`

```dockerfile
```

-	Layers:
	-	`sha256:8edd7c843a1819304942de0c3467a55562aa90b171eff38b2441d744b9713275`  
		Last Modified: Tue, 30 Dec 2025 04:39:13 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e31ca8d6d8a110040ea8d24b2209a8cfb4191308ca353c8928268320978ebea`  
		Last Modified: Tue, 30 Dec 2025 04:39:13 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9423c8280cf7c69da396753e3c48f64006b96922780b0a29bbaa5e492d52a103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fdedf8612218b249341309b4432d9be3e4cf5e2fc51bd0975b4f8531e5d8e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:48:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:48:42 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 29 Dec 2025 23:48:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:48:42 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:48:42 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:48:42 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:48:42 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:48:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:48:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:48:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7958a3e1061e0fa5e50b42b6eb97cb617ab31544b631a44383dc0a12b61e867a`  
		Last Modified: Mon, 29 Dec 2025 23:48:58 GMT  
		Size: 5.2 MB (5208160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54b303d3201682971e7df52d7907c8927f86f30e66556e2e05d5f15ef16ce24`  
		Last Modified: Mon, 29 Dec 2025 23:49:00 GMT  
		Size: 32.4 MB (32429494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc4699c9c926cfddab87e624399bf4bbe7167a64a38ab46da585275a60b342b`  
		Last Modified: Mon, 29 Dec 2025 23:48:58 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8f5b9dd518f5d5167d0adbb8b60a056f21947e6ecefb0142577cf605179ca1`  
		Last Modified: Mon, 29 Dec 2025 23:48:57 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb63949f91b01d8dcdf4f0dc6079da770bb10fd3dab52a30a3faea006b1ef0ba`  
		Last Modified: Mon, 29 Dec 2025 23:48:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:527e9ccd38be93db8832602864c76be3e5a90d5ee84143f8e35f705bfad554e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3aa2e7db17b6009960b0c3677db4154d6f086b02dd92641aac3a8376d88858d`

```dockerfile
```

-	Layers:
	-	`sha256:10a1915487b95f99d8a3bb459c4537835deccfa613ec4679f265a284cc3ed6cd`  
		Last Modified: Tue, 30 Dec 2025 04:39:17 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f89c5d0b2857218c647d2ac1756b187924601e5bff17e91c899b5f711cddaab`  
		Last Modified: Tue, 30 Dec 2025 04:39:17 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:8f246b11bed20824de500e732e0e0c1a9df2e2adcf60340444da2c4d2e7d83bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4fae84330ab9094200744d44140ff3695efc2a2085251cd4066103541bffbe5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23146498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6035189b6fd6fc001306a038b9c5678123af0b1f907f2a31efe3e96b3b689b22`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaabc96984af774b48937345c7cc275e3315d3a9a42aeb994f6946de24556be`  
		Last Modified: Mon, 08 Dec 2025 07:57:14 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff81f10ae11b38f809feee3b7a44d508880916016658ca83647ff9d1c294aba`  
		Last Modified: Mon, 08 Dec 2025 07:57:14 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cf4bd3a04c4941275f4aa1db1887c01bcdadeb973d9c95d34bc905b974dce`  
		Last Modified: Mon, 08 Dec 2025 07:57:15 GMT  
		Size: 19.2 MB (19204014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4732a865d574eb12cd7075d139d6bbd7d47fea3c367baf1a1f56ff51506906fb`  
		Last Modified: Mon, 08 Dec 2025 07:57:22 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0733dea6fe6d3cf04ef8c52dec6540501fbf0e79664e84fd00853fab32410e15`  
		Last Modified: Mon, 08 Dec 2025 07:57:25 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58005a9627e476ca3528af5a14e30f0d4549afa8e314dcde58ee7ec5fd6671`  
		Last Modified: Mon, 08 Dec 2025 07:57:47 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:07f09e7f03af9efcf88f89d7ad0f207d0e5ab57b9423663591e3c7aa0b3bc6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 KB (245253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2779ee449137493a2aca535f4363cae748d5a6c40f2c306362a97daf2d51bf6b`

```dockerfile
```

-	Layers:
	-	`sha256:4376140096bd52be7b1473ee7e7d625fff88ab2e731a2d509ed5b7861eab79fe`  
		Last Modified: Tue, 09 Dec 2025 03:48:01 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61687d781240db246500ccffe6dc5608d9be7a5e7c809173a2694ffec485f7c3`  
		Last Modified: Tue, 09 Dec 2025 03:48:01 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:74c29cf8bf7edbe8051bbcdd9d3daa71004092586701a98f7c29b01e24f8403b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:94df7a2fb47d6bcc39993da805ae29c56e303d3d61fb7f3e037d6195cf679279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf985f45197d744628cb5becbe28f8ebcf90b97ca153267746fb244d47c3221a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:48:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 29 Dec 2025 23:48:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:48:45 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:48:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:48:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56d924d25ddac886ed470bb0d62cfb191daef95b0d7d93b1728308a81f46fcb`  
		Last Modified: Mon, 29 Dec 2025 23:49:02 GMT  
		Size: 5.2 MB (5224253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799855feeb25840546efadee67de230da978fc1c69af182efbaebfd36cd49541`  
		Last Modified: Mon, 29 Dec 2025 23:49:03 GMT  
		Size: 35.0 MB (35011762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb6df38879de45f68b6ba2491d885a341b4913616902313896d13a0533e6763`  
		Last Modified: Mon, 29 Dec 2025 23:49:01 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8bd2dc79a66497ad11e69549cf2bdffea275c9ce9f1deb062c7a74e288fa13`  
		Last Modified: Mon, 29 Dec 2025 23:49:01 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21001b42941a7b780388b475b81c1e68e8d207c643db93e5f885ecd42dde3f42`  
		Last Modified: Mon, 29 Dec 2025 23:49:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:6442fae5968c170d8e9d988cf0231bd37be3345d2b98f584b4a0cc8b5903e5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6ba1675bb4e259e4bf6627b11d0f5c04ef623063aaf41ed2a70ceda5180cd3`

```dockerfile
```

-	Layers:
	-	`sha256:acecf42330dd72dd200a29723663538d66aed82be6554cbe4c6a9d1fdb684e8c`  
		Last Modified: Tue, 30 Dec 2025 01:39:39 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dfd16857d570e53bedafa12b4103161242b2b4902842995d962a2e9f25e26c7`  
		Last Modified: Tue, 30 Dec 2025 01:39:40 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c405545fbbf3db3cba8e4b0dcb564acfc9027bf0c7f665abf0d60c9bc2f7ea2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63372453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890fa135877089f106c5811183d4b53cbd025bbb9b31337f898e4c695af99753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:37:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 00:37:48 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 30 Dec 2025 00:37:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:37:48 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 30 Dec 2025 00:37:48 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 30 Dec 2025 00:37:48 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 30 Dec 2025 00:37:48 GMT
VOLUME [/var/lib/chronograf]
# Tue, 30 Dec 2025 00:37:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 00:37:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 00:37:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:157cb1ae1e97b073d55fa44e5e4ce17ccecf29dcfee2e34ca09a7de19793cf95`  
		Last Modified: Mon, 29 Dec 2025 22:25:27 GMT  
		Size: 25.5 MB (25546225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ccbf3a543831b632d98a5d27857cd287815894c0f4a4ac7ce49a8071787683`  
		Last Modified: Tue, 30 Dec 2025 00:38:08 GMT  
		Size: 4.5 MB (4490256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ec9c480db3fba43c640aafc97620317f46141682baa44c567901039caada60`  
		Last Modified: Tue, 30 Dec 2025 00:38:07 GMT  
		Size: 33.3 MB (33311584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a0660c160f9018742703d506f717dd94c55a6da09f01ca3e50777b5d48fe78`  
		Last Modified: Tue, 30 Dec 2025 00:38:03 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683491cecd499de5da1311d36fd7ea08457857ac4e3b8c813bde83ff7a716efc`  
		Last Modified: Tue, 30 Dec 2025 00:38:03 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774fd74b784719d25e130d33ec59158c40356933a0b4495c4249bce548d6a25a`  
		Last Modified: Tue, 30 Dec 2025 00:38:03 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:7f1aeb74f0ec36621039423a2426acd2a2ad12943fff4293cb9ced76dabc59ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44467ea11e6c0c28241b2dd2f5312fc8ae38b63854d106d94d12a14dcf1b01c`

```dockerfile
```

-	Layers:
	-	`sha256:80710d97a8cddd5c67650214dbe2a9e17f257874dc62e4824e54fa6c0dd673b0`  
		Last Modified: Tue, 30 Dec 2025 04:39:22 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3890d04dcbfc418c9ffbd7cfe125e50c551170bca722e697bc5ea16b40c1808`  
		Last Modified: Tue, 30 Dec 2025 04:39:23 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:1b43f7e055222e416e04939c240e3f292284f853ea4b5cf255c1b1cff7e31c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32be819cb55e3afb81f44fb00b5a9aa37a1cc82c117295643b3fd748194318ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:49:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:49:07 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 29 Dec 2025 23:49:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:49:07 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:49:07 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:49:07 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:49:07 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:49:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:49:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:49:07 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336bab96f6794789ad052c5e41cfe827e262ebda89fc1742be9210d21b535422`  
		Last Modified: Mon, 29 Dec 2025 23:49:23 GMT  
		Size: 5.2 MB (5208218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f78184cf0fc41cc5cf61ff3852de07e855ab070387b67dcd8d984ea5e1f726`  
		Last Modified: Mon, 29 Dec 2025 23:49:26 GMT  
		Size: 33.2 MB (33182231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa019c1bf34c920de80bfb2aa03f5e7249bd52d1b0213ae64b97a1651f962d89`  
		Last Modified: Mon, 29 Dec 2025 23:49:23 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b48fef41cb962d6b35cc972591c3ef12668adc0f50b49c0596d2ebfe0ce32f5`  
		Last Modified: Mon, 29 Dec 2025 23:49:23 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a8321c32c1dcca2328abc1308e9858500674cfd9f2cda7820ea642528c741a`  
		Last Modified: Mon, 29 Dec 2025 23:49:23 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:9f0661e764a490254f54befda3afbf44fbc9a81c0408c8b04648a9794663e596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44161e70d7dc965e7c9c41e8124b02c44e95ecbbae8b5be7d6123a97c4353936`

```dockerfile
```

-	Layers:
	-	`sha256:d064614132c6784a51657a62ab475395c5b5d52f1a03f634f1d76bb5033d5d6c`  
		Last Modified: Tue, 30 Dec 2025 01:39:47 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf355493f47040f40f39496fd1d5e9ad8b4c64188f9c3f826f82b219cd500c6`  
		Last Modified: Tue, 30 Dec 2025 01:39:48 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:b3fee5aad5c22c71cb04bbd41eea4af839aeb7d359a82d9b4233795d4cee5130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2d4252cb73b369cd488e239afeef5f7a6b44a46a01cfe8ab7d068d6397d5311d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23614563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9964a18d639210346c0ff7c26e65b91960ad4afbf36654d3a88e1c03026a1437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Mon, 08 Dec 2025 00:01:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6c508c6ab14eb797ff6524630894eea223ff1b5a3f02be3595aff5713c5112`  
		Last Modified: Thu, 11 Dec 2025 13:23:53 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43383a0cdbbe70773cd822a7089d90f254cc6923262bc86a209c0c182a190472`  
		Last Modified: Thu, 11 Dec 2025 06:17:57 GMT  
		Size: 19.7 MB (19672095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11524f4d626f224d1faadbb2537a398d423351e2a0d854a4a43b4692fab631c6`  
		Last Modified: Thu, 11 Dec 2025 06:17:54 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811766d26cc20ed9c9dee509c4ef17aa945fbbf00be418890deec226cbeae620`  
		Last Modified: Thu, 11 Dec 2025 13:23:54 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90296708765453bd34d3b31917ee366ec4e86d0d341504ddd046c032d6f85842`  
		Last Modified: Thu, 11 Dec 2025 13:23:54 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c5e372192d09b31155c48fb1472089780f956a2cdeba37b4eda3358869e38aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 KB (250462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad16fab4bfdaa94339daa5b35ee736124878a90af7d436293dd5657f43ac1f79`

```dockerfile
```

-	Layers:
	-	`sha256:6ed1879bf7ef8eb915186029d90ae2f6c3d14aa17bd74c3708035ff07dfcc75e`  
		Last Modified: Thu, 25 Dec 2025 14:21:32 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586220b931721e2b29f86f48af9fa3579d18c357b0351f043fc2e76a05ebc52`  
		Last Modified: Thu, 25 Dec 2025 14:21:32 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:74c29cf8bf7edbe8051bbcdd9d3daa71004092586701a98f7c29b01e24f8403b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:94df7a2fb47d6bcc39993da805ae29c56e303d3d61fb7f3e037d6195cf679279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf985f45197d744628cb5becbe28f8ebcf90b97ca153267746fb244d47c3221a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:48:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 29 Dec 2025 23:48:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:48:45 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:48:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:48:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:48:45 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56d924d25ddac886ed470bb0d62cfb191daef95b0d7d93b1728308a81f46fcb`  
		Last Modified: Mon, 29 Dec 2025 23:49:02 GMT  
		Size: 5.2 MB (5224253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799855feeb25840546efadee67de230da978fc1c69af182efbaebfd36cd49541`  
		Last Modified: Mon, 29 Dec 2025 23:49:03 GMT  
		Size: 35.0 MB (35011762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb6df38879de45f68b6ba2491d885a341b4913616902313896d13a0533e6763`  
		Last Modified: Mon, 29 Dec 2025 23:49:01 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8bd2dc79a66497ad11e69549cf2bdffea275c9ce9f1deb062c7a74e288fa13`  
		Last Modified: Mon, 29 Dec 2025 23:49:01 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21001b42941a7b780388b475b81c1e68e8d207c643db93e5f885ecd42dde3f42`  
		Last Modified: Mon, 29 Dec 2025 23:49:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:6442fae5968c170d8e9d988cf0231bd37be3345d2b98f584b4a0cc8b5903e5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6ba1675bb4e259e4bf6627b11d0f5c04ef623063aaf41ed2a70ceda5180cd3`

```dockerfile
```

-	Layers:
	-	`sha256:acecf42330dd72dd200a29723663538d66aed82be6554cbe4c6a9d1fdb684e8c`  
		Last Modified: Tue, 30 Dec 2025 01:39:39 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dfd16857d570e53bedafa12b4103161242b2b4902842995d962a2e9f25e26c7`  
		Last Modified: Tue, 30 Dec 2025 01:39:40 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:c405545fbbf3db3cba8e4b0dcb564acfc9027bf0c7f665abf0d60c9bc2f7ea2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63372453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890fa135877089f106c5811183d4b53cbd025bbb9b31337f898e4c695af99753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:37:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 00:37:48 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 30 Dec 2025 00:37:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:37:48 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 30 Dec 2025 00:37:48 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 30 Dec 2025 00:37:48 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 30 Dec 2025 00:37:48 GMT
VOLUME [/var/lib/chronograf]
# Tue, 30 Dec 2025 00:37:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 00:37:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 00:37:48 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:157cb1ae1e97b073d55fa44e5e4ce17ccecf29dcfee2e34ca09a7de19793cf95`  
		Last Modified: Mon, 29 Dec 2025 22:25:27 GMT  
		Size: 25.5 MB (25546225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ccbf3a543831b632d98a5d27857cd287815894c0f4a4ac7ce49a8071787683`  
		Last Modified: Tue, 30 Dec 2025 00:38:08 GMT  
		Size: 4.5 MB (4490256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ec9c480db3fba43c640aafc97620317f46141682baa44c567901039caada60`  
		Last Modified: Tue, 30 Dec 2025 00:38:07 GMT  
		Size: 33.3 MB (33311584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a0660c160f9018742703d506f717dd94c55a6da09f01ca3e50777b5d48fe78`  
		Last Modified: Tue, 30 Dec 2025 00:38:03 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683491cecd499de5da1311d36fd7ea08457857ac4e3b8c813bde83ff7a716efc`  
		Last Modified: Tue, 30 Dec 2025 00:38:03 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774fd74b784719d25e130d33ec59158c40356933a0b4495c4249bce548d6a25a`  
		Last Modified: Tue, 30 Dec 2025 00:38:03 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:7f1aeb74f0ec36621039423a2426acd2a2ad12943fff4293cb9ced76dabc59ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44467ea11e6c0c28241b2dd2f5312fc8ae38b63854d106d94d12a14dcf1b01c`

```dockerfile
```

-	Layers:
	-	`sha256:80710d97a8cddd5c67650214dbe2a9e17f257874dc62e4824e54fa6c0dd673b0`  
		Last Modified: Tue, 30 Dec 2025 04:39:22 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3890d04dcbfc418c9ffbd7cfe125e50c551170bca722e697bc5ea16b40c1808`  
		Last Modified: Tue, 30 Dec 2025 04:39:23 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:1b43f7e055222e416e04939c240e3f292284f853ea4b5cf255c1b1cff7e31c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32be819cb55e3afb81f44fb00b5a9aa37a1cc82c117295643b3fd748194318ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:49:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:49:07 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 29 Dec 2025 23:49:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:49:07 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:49:07 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:49:07 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:49:07 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:49:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:49:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:49:07 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336bab96f6794789ad052c5e41cfe827e262ebda89fc1742be9210d21b535422`  
		Last Modified: Mon, 29 Dec 2025 23:49:23 GMT  
		Size: 5.2 MB (5208218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f78184cf0fc41cc5cf61ff3852de07e855ab070387b67dcd8d984ea5e1f726`  
		Last Modified: Mon, 29 Dec 2025 23:49:26 GMT  
		Size: 33.2 MB (33182231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa019c1bf34c920de80bfb2aa03f5e7249bd52d1b0213ae64b97a1651f962d89`  
		Last Modified: Mon, 29 Dec 2025 23:49:23 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b48fef41cb962d6b35cc972591c3ef12668adc0f50b49c0596d2ebfe0ce32f5`  
		Last Modified: Mon, 29 Dec 2025 23:49:23 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a8321c32c1dcca2328abc1308e9858500674cfd9f2cda7820ea642528c741a`  
		Last Modified: Mon, 29 Dec 2025 23:49:23 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:9f0661e764a490254f54befda3afbf44fbc9a81c0408c8b04648a9794663e596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44161e70d7dc965e7c9c41e8124b02c44e95ecbbae8b5be7d6123a97c4353936`

```dockerfile
```

-	Layers:
	-	`sha256:d064614132c6784a51657a62ab475395c5b5d52f1a03f634f1d76bb5033d5d6c`  
		Last Modified: Tue, 30 Dec 2025 01:39:47 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf355493f47040f40f39496fd1d5e9ad8b4c64188f9c3f826f82b219cd500c6`  
		Last Modified: Tue, 30 Dec 2025 01:39:48 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:b3fee5aad5c22c71cb04bbd41eea4af839aeb7d359a82d9b4233795d4cee5130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:2d4252cb73b369cd488e239afeef5f7a6b44a46a01cfe8ab7d068d6397d5311d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23614563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9964a18d639210346c0ff7c26e65b91960ad4afbf36654d3a88e1c03026a1437`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Mon, 08 Dec 2025 00:01:59 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6c508c6ab14eb797ff6524630894eea223ff1b5a3f02be3595aff5713c5112`  
		Last Modified: Thu, 11 Dec 2025 13:23:53 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43383a0cdbbe70773cd822a7089d90f254cc6923262bc86a209c0c182a190472`  
		Last Modified: Thu, 11 Dec 2025 06:17:57 GMT  
		Size: 19.7 MB (19672095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11524f4d626f224d1faadbb2537a398d423351e2a0d854a4a43b4692fab631c6`  
		Last Modified: Thu, 11 Dec 2025 06:17:54 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811766d26cc20ed9c9dee509c4ef17aa945fbbf00be418890deec226cbeae620`  
		Last Modified: Thu, 11 Dec 2025 13:23:54 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90296708765453bd34d3b31917ee366ec4e86d0d341504ddd046c032d6f85842`  
		Last Modified: Thu, 11 Dec 2025 13:23:54 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:c5e372192d09b31155c48fb1472089780f956a2cdeba37b4eda3358869e38aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 KB (250462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad16fab4bfdaa94339daa5b35ee736124878a90af7d436293dd5657f43ac1f79`

```dockerfile
```

-	Layers:
	-	`sha256:6ed1879bf7ef8eb915186029d90ae2f6c3d14aa17bd74c3708035ff07dfcc75e`  
		Last Modified: Thu, 25 Dec 2025 14:21:32 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586220b931721e2b29f86f48af9fa3579d18c357b0351f043fc2e76a05ebc52`  
		Last Modified: Thu, 25 Dec 2025 14:21:32 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:efc72c285cae492b0fb820a7794f2da69a70ef77caa8d28282e0df6f79856029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:08463b31a0a2617a51e230161f997b525214640155e291a423ae53004330c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32700225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af178eb7af41f52d85b69957fc583d381f6a24a9e604b40818766ecf3004a1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 15 Aug 2025 14:37:23 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Fri, 15 Aug 2025 14:37:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 15 Aug 2025 14:37:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 15 Aug 2025 14:37:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 Aug 2025 14:37:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 Aug 2025 14:37:23 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Mon, 08 Dec 2025 02:53:47 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Mon, 08 Dec 2025 02:53:50 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Mon, 08 Dec 2025 02:53:48 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Mon, 08 Dec 2025 02:53:49 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:dd3236bd7a2263357f0c7258a9a36c7fef283fd9f58f17f5fc2cbfa8330df313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 KB (268238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808a56c94ce865ff68fe325760f90b15b31758031ea028455935f57e4d2afe56`

```dockerfile
```

-	Layers:
	-	`sha256:d62aac69b78bc656cc8510a0566537353a4cda897cdaf124ca24ad68c0fa7fb1`  
		Last Modified: Mon, 08 Dec 2025 03:44:43 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Mon, 08 Dec 2025 03:44:44 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:42e7b310399e57126053f3ff8eb551290b942ebbd8fd08186af03cfce512bbff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:1cc1ed9e94b3ad2e494e692082e3b43563ea6ec705fea568e9f206a3fb354ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920250cb93c814717f4751bbba4fb577f76a26a1f64057d21886264b4e1caf02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Mon, 29 Dec 2025 23:49:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:49:11 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:49:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:49:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:49:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7057b2c1916424b64a310962c344f1e3d9fa16300cda4db1d26fdc7439e56756`  
		Last Modified: Mon, 29 Dec 2025 23:49:29 GMT  
		Size: 7.9 MB (7878772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a516a78eb77c9789463954352a6bd5993aa13becbccde9d2d8215e201f2eea`  
		Last Modified: Mon, 29 Dec 2025 23:49:39 GMT  
		Size: 49.3 MB (49276671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f97085fb5a443724217d349b2d8b1884db62fc9ca7e8303b30814d215940e23`  
		Last Modified: Mon, 29 Dec 2025 23:49:29 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d46904c5a259d0e15ed3faf2c27ec708db13309dadfaf70406d685205230ec`  
		Last Modified: Mon, 29 Dec 2025 23:49:28 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607c0a53eaa400fcaf77a159c0ebe3ccd2af3acfb7ae6b7c0c91e52b7306ce73`  
		Last Modified: Mon, 29 Dec 2025 23:49:28 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:29e7891012d3d0014535dcc6e053da44fa1e928261e29856dd7dc9cf4cd02ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb6fc9e83e9b63386e39544eb7ba045eb9aa039d838a1af3a819db267063a0d`

```dockerfile
```

-	Layers:
	-	`sha256:bf9598b24cf90f9798d49be52d65a67303a38bc6a241873acd661b01dd6b39b7`  
		Last Modified: Tue, 30 Dec 2025 01:39:14 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c11679793b892f0d7a511fc980ffd1b3163f784bd5ecad1e8bbc77fb4e3fa2ed`  
		Last Modified: Tue, 30 Dec 2025 01:39:15 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:5614c0bce8750e0a6ea25194574cb8ef466e43f179f2169908d577fccbd53182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d435c6fe46ecb356e0a2b8f6e048091c0724a76c5900eb599b4058fd507bd66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:38:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 30 Dec 2025 00:38:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 30 Dec 2025 00:38:44 GMT
VOLUME [/var/lib/chronograf]
# Tue, 30 Dec 2025 00:38:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Dec 2025 00:38:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Dec 2025 00:38:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e76d25710d4436332b21775b55108e030e850f8146d1ca815f54043af8e4a0`  
		Last Modified: Tue, 30 Dec 2025 00:39:02 GMT  
		Size: 6.5 MB (6508147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a393dca982eab829dea2ecfdb75f004718b35ae36a9e097b5e7fa5c59c942adf`  
		Last Modified: Tue, 30 Dec 2025 00:39:06 GMT  
		Size: 45.6 MB (45621877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11fc5525ed12fc13ffc16e5beff72a153f027c5425ca12e6cbdda700d5596f`  
		Last Modified: Tue, 30 Dec 2025 00:39:01 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013ca9dd2d86195b2b731de9e069dcc979e87f76bbca8fa403669645258cdb8f`  
		Last Modified: Tue, 30 Dec 2025 00:39:01 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3301abba1bc74163e7254fd94c820ffe4dfa27122f5fa0cab1d9e5d959258b`  
		Last Modified: Tue, 30 Dec 2025 00:39:01 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:5088632808249678c5bb72c45655c939eb2596980edd61e6303628c03d26f121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a120d74c8961bde2438b31b6d73d722b88bf37ac013d7b37f2c9a511c2e1f7`

```dockerfile
```

-	Layers:
	-	`sha256:c18b311f1a79bbfcef122eddccc948baccbc699398d7f8ff36e5a2059ea0bf57`  
		Last Modified: Tue, 30 Dec 2025 04:38:51 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19a85c5833ea81731c8d12a73fd9344d8c9e3fbe2146d5ef676068662d4741f`  
		Last Modified: Tue, 30 Dec 2025 04:39:32 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ab396a4c9adf88108e26c794d4ab01dd533db1444dd50649bf676883e7465120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4b5034cdadd1d2b5a2c88cf8ee5e0ec580e11efe42ae592260e693e255a784`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:49:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Mon, 29 Dec 2025 23:49:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 29 Dec 2025 23:49:32 GMT
VOLUME [/var/lib/chronograf]
# Mon, 29 Dec 2025 23:49:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Dec 2025 23:49:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Dec 2025 23:49:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcd6af1d78457dbf8666584d3e8efb337b6ee4b89cf5915ce792d94ded22f03`  
		Last Modified: Mon, 29 Dec 2025 23:49:48 GMT  
		Size: 7.7 MB (7691849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c987fc54d10a70e2e7b896f43d6350cf278bb493022a35b39852562ef07b0ee4`  
		Last Modified: Mon, 29 Dec 2025 23:49:50 GMT  
		Size: 47.1 MB (47066825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08a9a785a4af6a10bb264b846f4c33616d2190d1ed19bff9ece4bbf6c9a286`  
		Last Modified: Mon, 29 Dec 2025 23:49:47 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e0c003b8e1c41407fd527be5262eb0c6c4c105d182f3d085a269f9a9f01a13`  
		Last Modified: Mon, 29 Dec 2025 23:49:47 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74ffbe7104d2b8a27b2491cdef1680e1cdf61636f9fec7405161b6695ca737a`  
		Last Modified: Mon, 29 Dec 2025 23:49:47 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:fd1aae3c0fbe962e4d2745c2a7c54b2ce1237044bb08423ce6953c280f21ca51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b195f0729c60f9e35a9810b73191018a373e8b4bf85657709707eaa03849f5`

```dockerfile
```

-	Layers:
	-	`sha256:8b0d9859a1a3b8dd2bd74f53ca6375ab8d51b7a8b726a9104c0c2357525207cf`  
		Last Modified: Tue, 30 Dec 2025 04:39:39 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc22d9db6ba372c2eefdc390892c1f7fbaec3094e945d01556fee201a37a5ca`  
		Last Modified: Tue, 30 Dec 2025 04:39:40 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json
