<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.9`](#chronograf1109)
-	[`chronograf:1.10.9-alpine`](#chronograf1109-alpine)
-	[`chronograf:1.11`](#chronograf111)
-	[`chronograf:1.11-alpine`](#chronograf111-alpine)
-	[`chronograf:1.11.2`](#chronograf1112)
-	[`chronograf:1.11.2-alpine`](#chronograf1112-alpine)
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
$ docker pull chronograf@sha256:32f78cd30e83c7e07c5206facc6ea866ef62ebcf8e9bc0a80f7afdaa688ab6c5
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
$ docker pull chronograf@sha256:773ab849771a3ea9b2671b38eeb2e543c479a25eb06bd2dc4dd469dc39530d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85009366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05319deceb59314db6ad41943ea945103c92c9b6a5a24f94746283db3b571b3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:39:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:40:05 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 22 Apr 2026 01:40:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:40:05 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:40:05 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:40:05 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:40:05 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:40:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:40:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23507b4454defde85a3dee72864eeffe971471c8435caec348c7d5a2715fb013`  
		Last Modified: Wed, 22 Apr 2026 01:40:17 GMT  
		Size: 7.9 MB (7880718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a898d087dc81b45d6dc30ed0898c6ead6ccd69ed77be869beddbb7c109d020b0`  
		Last Modified: Wed, 22 Apr 2026 01:40:18 GMT  
		Size: 48.9 MB (48867922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710692e6ae5c3a5c920300fb31ac888792e3a15555b4e6cdf5250804a171cc6d`  
		Last Modified: Wed, 22 Apr 2026 01:40:17 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08db77c5dccc9fa856d27b11e3198cd553bcc1d5b56a5616cb881865eacfda4`  
		Last Modified: Wed, 22 Apr 2026 01:40:17 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f428274b7c8cc3e578ebdd330d49230c268ec328eca676e3b89ff427ce6aa48e`  
		Last Modified: Wed, 22 Apr 2026 01:40:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:e449f1e93cf4771f53d4b9dc75bb9383d3ef45c3ac0150aaa6062917d2678ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5072e20ab0b626dd167a1c42204e7e0690b46d462f6b380fae476a60daa430`

```dockerfile
```

-	Layers:
	-	`sha256:f65285c01a0b1f7131984e80c56d72bc28a611ec2d988a08b2975fab2e8eac8c`  
		Last Modified: Wed, 22 Apr 2026 01:40:17 GMT  
		Size: 2.9 MB (2855424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ba44e6ed9f6b5632849f65a9a4d50c627b7acb8d69d16ba37a23be967eb6ff`  
		Last Modified: Wed, 22 Apr 2026 01:40:17 GMT  
		Size: 15.8 KB (15779 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1f168549df54018382b902db0cd4570b99bad80714399e687d8f2e2ea41d0c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76799292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28162a23b2cbf6339b4087a60bb283f3056893dc554cf25ccbc2aaf18a5cbdbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:20:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:21:06 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 22 Apr 2026 02:21:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:21:06 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 02:21:06 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 02:21:06 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 02:21:06 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 02:21:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:21:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:21:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d3311d55816cf34cc663f098f8e93bb8dca4772ce9f25ac1e909fa7b0628d17b`  
		Last Modified: Wed, 22 Apr 2026 00:16:41 GMT  
		Size: 23.9 MB (23941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d63a4afa778c3f3b9fd8e74cd9057dca450304be906e28bd85d6f4c74a21081`  
		Last Modified: Wed, 22 Apr 2026 02:21:17 GMT  
		Size: 6.5 MB (6513263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebee01827d7681ca5a8b903b7aab846cd0a8fc2c73f058d8860ef8426b6202`  
		Last Modified: Wed, 22 Apr 2026 02:21:19 GMT  
		Size: 46.3 MB (46320150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a74aa0bc06544eaab8b30fcefb785fa447e31add9555aea2958bf314aab3d`  
		Last Modified: Wed, 22 Apr 2026 02:21:17 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f214f00928ee13cea8dafc257e876ad3b7036a9f65df9fb4e4c0ddfb4faa5f8b`  
		Last Modified: Wed, 22 Apr 2026 02:21:17 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6b01a827e9af8128c7cf888bf179a8d36341e0ed020ca1d5fb4375d8d3adbf`  
		Last Modified: Wed, 22 Apr 2026 02:21:18 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:4b234fb76b41c8785b049320cda57a0b85b76740fe3fba6fac451deb14077c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2873569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bbf79dfeee2b5f557aed2e79bb08368027d9d728e6ab617417442d165216eb`

```dockerfile
```

-	Layers:
	-	`sha256:909c00611643842f3d8124d895a7faae7e4dde6ec8c81a2215c78dba8a2cb7b3`  
		Last Modified: Wed, 22 Apr 2026 02:21:17 GMT  
		Size: 2.9 MB (2857713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5caed5f0f965aa4cc5dc9462a8e068f0480f38b80edbc975fd4600bedd670e0a`  
		Last Modified: Wed, 22 Apr 2026 02:21:17 GMT  
		Size: 15.9 KB (15856 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a75e29f0e2d4048f85dfc880fd03e40b5a1f6ae359e63f6190e0c0f86e07016a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81847551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b6cc53f39fc5f9f8d60d588875a61fa628742f6216e40fa92980a4970d984c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:43:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:43:32 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 22 Apr 2026 01:43:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:43:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:43:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:43:32 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:43:32 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:43:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:43:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304dd309a885372461eaacf7918e8afe3c338f10a09c85c5e843b655ecaac6ac`  
		Last Modified: Wed, 22 Apr 2026 01:43:44 GMT  
		Size: 7.7 MB (7698533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf02a963e9ebf8ccfa7482b22e6e1c72c2efe5dbd50d1d313d0152315133dba`  
		Last Modified: Wed, 22 Apr 2026 01:43:45 GMT  
		Size: 46.0 MB (46008439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a6b3130985847f9b6273a06d9afe6a769024671c811abd787af4f35932d439`  
		Last Modified: Wed, 22 Apr 2026 01:43:44 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1e65366bee5cc4dd5b9dc2ce4717503d04695d924295595d181fc58ef9765e`  
		Last Modified: Wed, 22 Apr 2026 01:43:44 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8963b20cfb2b6d8a40280d0426b801be029fd523b8c00bd640ef0b3646b8fa8d`  
		Last Modified: Wed, 22 Apr 2026 01:43:45 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:1107050be75ff62e16268772c4e77a2ab3aa2f485453ae69b5e983355eb1fa6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44221eefde01ec3de636a3d61d70dfd64ed839424d61f0bdbc9ff03344dde84e`

```dockerfile
```

-	Layers:
	-	`sha256:ac3a1b127b4a08a38e84fa16471a1717efc7b66950252ed2daea55b80826b709`  
		Last Modified: Wed, 22 Apr 2026 01:43:44 GMT  
		Size: 2.9 MB (2855685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eabd1808f9c79f9c3ef71f768ac24b673f58ba2e993434753bf525263575e7bd`  
		Last Modified: Wed, 22 Apr 2026 01:43:44 GMT  
		Size: 15.9 KB (15874 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:d67db795c6c64bf832d051028112e619057390648fe212e9c427393769746798
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:257404077359221b264827d685e34eff5274d993cd8d02cb410638063df477d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33281872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a15f666b3e98ed0853b3cd6db84fb4ce28ed284b973002a3e7e0745954e2d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:40 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:23:41 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Fri, 17 Apr 2026 00:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 00:23:46 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 00:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c42c4c82c5088e972f05e6e4c61e835f85d39a8aa5867459dde6d6cf0dcf9`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f386db9e6688fb72589c06bb92c9e5581bf0f12dc9e7976d1fd94aa0e0f3fb03`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 312.2 KB (312182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c09588157059f49ad2a9622892e2ae4eea22a850019e5f096129f96ffe5ef2f`  
		Last Modified: Fri, 17 Apr 2026 00:23:55 GMT  
		Size: 29.1 MB (29136768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29f2d6761a854698c8fc77adb5c5f5ec518db3475a4dff4dc463c7d8453e5be`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d89becaf0206e7f1f6029d6b6a13607ec72d9a340adcd737bec99c4e2ddbb`  
		Last Modified: Fri, 17 Apr 2026 00:23:55 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b890ebfc700be8ee259bd864396302d8201bd5d269e82ead45a226bc9eb80026`  
		Last Modified: Fri, 17 Apr 2026 00:23:55 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:d2f1dd5e80f798e00c99361d4e5ae8a4c66a9cd69fa098c1a46b99dfecf9fd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 KB (269153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364dd10613f47468bd32987446ad21e97c4a4eb16fde031d198bcf3ad4eabdad`

```dockerfile
```

-	Layers:
	-	`sha256:81a1ebf9e733fa77e5931f96097a372de666e3ddcc8e8ef5d62ce11a2c9832c8`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 251.3 KB (251342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e576ff54c0928fe47749ca45031b2f2d5985bdeb3ea51aa3b1872c70242fdd0b`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 17.8 KB (17811 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9`

```console
$ docker pull chronograf@sha256:32f78cd30e83c7e07c5206facc6ea866ef62ebcf8e9bc0a80f7afdaa688ab6c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.9` - linux; amd64

```console
$ docker pull chronograf@sha256:773ab849771a3ea9b2671b38eeb2e543c479a25eb06bd2dc4dd469dc39530d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85009366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05319deceb59314db6ad41943ea945103c92c9b6a5a24f94746283db3b571b3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:39:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:40:05 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 22 Apr 2026 01:40:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:40:05 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:40:05 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:40:05 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:40:05 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:40:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:40:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23507b4454defde85a3dee72864eeffe971471c8435caec348c7d5a2715fb013`  
		Last Modified: Wed, 22 Apr 2026 01:40:17 GMT  
		Size: 7.9 MB (7880718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a898d087dc81b45d6dc30ed0898c6ead6ccd69ed77be869beddbb7c109d020b0`  
		Last Modified: Wed, 22 Apr 2026 01:40:18 GMT  
		Size: 48.9 MB (48867922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710692e6ae5c3a5c920300fb31ac888792e3a15555b4e6cdf5250804a171cc6d`  
		Last Modified: Wed, 22 Apr 2026 01:40:17 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08db77c5dccc9fa856d27b11e3198cd553bcc1d5b56a5616cb881865eacfda4`  
		Last Modified: Wed, 22 Apr 2026 01:40:17 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f428274b7c8cc3e578ebdd330d49230c268ec328eca676e3b89ff427ce6aa48e`  
		Last Modified: Wed, 22 Apr 2026 01:40:18 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:e449f1e93cf4771f53d4b9dc75bb9383d3ef45c3ac0150aaa6062917d2678ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5072e20ab0b626dd167a1c42204e7e0690b46d462f6b380fae476a60daa430`

```dockerfile
```

-	Layers:
	-	`sha256:f65285c01a0b1f7131984e80c56d72bc28a611ec2d988a08b2975fab2e8eac8c`  
		Last Modified: Wed, 22 Apr 2026 01:40:17 GMT  
		Size: 2.9 MB (2855424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ba44e6ed9f6b5632849f65a9a4d50c627b7acb8d69d16ba37a23be967eb6ff`  
		Last Modified: Wed, 22 Apr 2026 01:40:17 GMT  
		Size: 15.8 KB (15779 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1f168549df54018382b902db0cd4570b99bad80714399e687d8f2e2ea41d0c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76799292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28162a23b2cbf6339b4087a60bb283f3056893dc554cf25ccbc2aaf18a5cbdbf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:20:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:21:06 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 22 Apr 2026 02:21:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:21:06 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 02:21:06 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 02:21:06 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 02:21:06 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 02:21:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:21:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:21:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d3311d55816cf34cc663f098f8e93bb8dca4772ce9f25ac1e909fa7b0628d17b`  
		Last Modified: Wed, 22 Apr 2026 00:16:41 GMT  
		Size: 23.9 MB (23941424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d63a4afa778c3f3b9fd8e74cd9057dca450304be906e28bd85d6f4c74a21081`  
		Last Modified: Wed, 22 Apr 2026 02:21:17 GMT  
		Size: 6.5 MB (6513263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebee01827d7681ca5a8b903b7aab846cd0a8fc2c73f058d8860ef8426b6202`  
		Last Modified: Wed, 22 Apr 2026 02:21:19 GMT  
		Size: 46.3 MB (46320150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a74aa0bc06544eaab8b30fcefb785fa447e31add9555aea2958bf314aab3d`  
		Last Modified: Wed, 22 Apr 2026 02:21:17 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f214f00928ee13cea8dafc257e876ad3b7036a9f65df9fb4e4c0ddfb4faa5f8b`  
		Last Modified: Wed, 22 Apr 2026 02:21:17 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6b01a827e9af8128c7cf888bf179a8d36341e0ed020ca1d5fb4375d8d3adbf`  
		Last Modified: Wed, 22 Apr 2026 02:21:18 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:4b234fb76b41c8785b049320cda57a0b85b76740fe3fba6fac451deb14077c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2873569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bbf79dfeee2b5f557aed2e79bb08368027d9d728e6ab617417442d165216eb`

```dockerfile
```

-	Layers:
	-	`sha256:909c00611643842f3d8124d895a7faae7e4dde6ec8c81a2215c78dba8a2cb7b3`  
		Last Modified: Wed, 22 Apr 2026 02:21:17 GMT  
		Size: 2.9 MB (2857713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5caed5f0f965aa4cc5dc9462a8e068f0480f38b80edbc975fd4600bedd670e0a`  
		Last Modified: Wed, 22 Apr 2026 02:21:17 GMT  
		Size: 15.9 KB (15856 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a75e29f0e2d4048f85dfc880fd03e40b5a1f6ae359e63f6190e0c0f86e07016a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81847551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b6cc53f39fc5f9f8d60d588875a61fa628742f6216e40fa92980a4970d984c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:43:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:43:32 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 22 Apr 2026 01:43:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:43:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:43:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:43:32 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:43:32 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:43:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:43:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304dd309a885372461eaacf7918e8afe3c338f10a09c85c5e843b655ecaac6ac`  
		Last Modified: Wed, 22 Apr 2026 01:43:44 GMT  
		Size: 7.7 MB (7698533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf02a963e9ebf8ccfa7482b22e6e1c72c2efe5dbd50d1d313d0152315133dba`  
		Last Modified: Wed, 22 Apr 2026 01:43:45 GMT  
		Size: 46.0 MB (46008439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a6b3130985847f9b6273a06d9afe6a769024671c811abd787af4f35932d439`  
		Last Modified: Wed, 22 Apr 2026 01:43:44 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1e65366bee5cc4dd5b9dc2ce4717503d04695d924295595d181fc58ef9765e`  
		Last Modified: Wed, 22 Apr 2026 01:43:44 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8963b20cfb2b6d8a40280d0426b801be029fd523b8c00bd640ef0b3646b8fa8d`  
		Last Modified: Wed, 22 Apr 2026 01:43:45 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:1107050be75ff62e16268772c4e77a2ab3aa2f485453ae69b5e983355eb1fa6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44221eefde01ec3de636a3d61d70dfd64ed839424d61f0bdbc9ff03344dde84e`

```dockerfile
```

-	Layers:
	-	`sha256:ac3a1b127b4a08a38e84fa16471a1717efc7b66950252ed2daea55b80826b709`  
		Last Modified: Wed, 22 Apr 2026 01:43:44 GMT  
		Size: 2.9 MB (2855685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eabd1808f9c79f9c3ef71f768ac24b673f58ba2e993434753bf525263575e7bd`  
		Last Modified: Wed, 22 Apr 2026 01:43:44 GMT  
		Size: 15.9 KB (15874 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.9-alpine`

```console
$ docker pull chronograf@sha256:d67db795c6c64bf832d051028112e619057390648fe212e9c427393769746798
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:257404077359221b264827d685e34eff5274d993cd8d02cb410638063df477d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33281872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a15f666b3e98ed0853b3cd6db84fb4ce28ed284b973002a3e7e0745954e2d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:40 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:23:41 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Fri, 17 Apr 2026 00:23:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 00:23:46 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 00:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c42c4c82c5088e972f05e6e4c61e835f85d39a8aa5867459dde6d6cf0dcf9`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f386db9e6688fb72589c06bb92c9e5581bf0f12dc9e7976d1fd94aa0e0f3fb03`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 312.2 KB (312182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c09588157059f49ad2a9622892e2ae4eea22a850019e5f096129f96ffe5ef2f`  
		Last Modified: Fri, 17 Apr 2026 00:23:55 GMT  
		Size: 29.1 MB (29136768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29f2d6761a854698c8fc77adb5c5f5ec518db3475a4dff4dc463c7d8453e5be`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d89becaf0206e7f1f6029d6b6a13607ec72d9a340adcd737bec99c4e2ddbb`  
		Last Modified: Fri, 17 Apr 2026 00:23:55 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b890ebfc700be8ee259bd864396302d8201bd5d269e82ead45a226bc9eb80026`  
		Last Modified: Fri, 17 Apr 2026 00:23:55 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:d2f1dd5e80f798e00c99361d4e5ae8a4c66a9cd69fa098c1a46b99dfecf9fd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 KB (269153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:364dd10613f47468bd32987446ad21e97c4a4eb16fde031d198bcf3ad4eabdad`

```dockerfile
```

-	Layers:
	-	`sha256:81a1ebf9e733fa77e5931f96097a372de666e3ddcc8e8ef5d62ce11a2c9832c8`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 251.3 KB (251342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e576ff54c0928fe47749ca45031b2f2d5985bdeb3ea51aa3b1872c70242fdd0b`  
		Last Modified: Fri, 17 Apr 2026 00:23:54 GMT  
		Size: 17.8 KB (17811 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11`

```console
$ docker pull chronograf@sha256:301c00f5faac2c5d33b05bfe4b06dc825158120e3aaedbe0a8f9f116fc7da549
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.11` - linux; amd64

```console
$ docker pull chronograf@sha256:b789cc3f234aca70cbe48a1b756ccdae8e27e5249b4254d0b40768d5fb554504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98523348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76ace0fc98017a90832ebf70bbdb13b0b5b83fb6ccf5fc8558b4dab85b58ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:39:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
ENV CHRONOGRAF_VERSION=1.11.1
# Wed, 22 Apr 2026 01:40:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:40:03 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:40:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890bcea591fcf347b2fbf1d61b2a6b1983750cd5d9049eeda31e36c124f50e82`  
		Last Modified: Wed, 22 Apr 2026 01:40:20 GMT  
		Size: 7.9 MB (7880761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e9a112a46a66d65e1f9fd68ce3b3bb69113b37aa907bb408f12f0fdd304ee8`  
		Last Modified: Wed, 22 Apr 2026 01:40:21 GMT  
		Size: 62.4 MB (62381869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8a71fdbf6fb57d2ef3a4ee7881fa229d32585df420363632d945c6360bbaa`  
		Last Modified: Wed, 22 Apr 2026 01:40:20 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d9a90b228f0f58f48584d9b66a142f7f4511640878b26c8cf83e1a8cfddeba`  
		Last Modified: Wed, 22 Apr 2026 01:40:19 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d54185746004b87475a722a316bd05ef4ef68c46df2d550d1fa851031c7b511`  
		Last Modified: Wed, 22 Apr 2026 01:40:21 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11` - unknown; unknown

```console
$ docker pull chronograf@sha256:b6de94af8207cd47c082d6404c39429ed5d2c1fd8dd8c89f1f8ce7181c3bf707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7411f7288317e0e8573591b761771a9f6586041704aca4e3a8cb098c4717b7`

```dockerfile
```

-	Layers:
	-	`sha256:aa00abfb671c2cd3e6adb2c094a43dea281dd9b55f0c7434ac77dd8fe565fa5a`  
		Last Modified: Wed, 22 Apr 2026 01:40:19 GMT  
		Size: 2.9 MB (2873700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:852da94dc4b795b75cd9dd711b2e24141e43edbb44df342a56361a3f11e96403`  
		Last Modified: Wed, 22 Apr 2026 01:40:19 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.11` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:68bafb55be081cc169b6026b419c1b5099ae8ef2e77f47aa67e3c7ff58147294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95219034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4803eb94c2953dcc9b712710b6fea86b3bd3a5e49fbde785e8382ddfa648d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:43:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
ENV CHRONOGRAF_VERSION=1.11.1
# Wed, 22 Apr 2026 01:43:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:43:35 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:43:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:43:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3890b2677d0421ab5024893da8a9b87e11e51d5f038697a769872acc46f8eb7e`  
		Last Modified: Wed, 22 Apr 2026 01:43:50 GMT  
		Size: 7.7 MB (7698505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7f6bc004ebdfde070c98dd879bd60eb2e8b2fbbf8654cc3744687bb91b130e`  
		Last Modified: Wed, 22 Apr 2026 01:43:52 GMT  
		Size: 59.4 MB (59379943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845367a4d5112966d659b3a767e8faeacdf77ea0d336f1ce3fe6f93b073136ee`  
		Last Modified: Wed, 22 Apr 2026 01:43:50 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de84aba6d85fdb6b285d5b67445704e4f6badf59ba839f689b26293863eb6114`  
		Last Modified: Wed, 22 Apr 2026 01:43:50 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba017d4f8fdb0864069f3dec705f13b4f4dc337b21b5fbb084810cebebd8e167`  
		Last Modified: Wed, 22 Apr 2026 01:43:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11` - unknown; unknown

```console
$ docker pull chronograf@sha256:c1d1173625df32d5f717779696e450af1183fae65fec15885bbbf79afd74ca5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5cf482b920081a833f634b3740f5afacd4742f2fe22e955ad0d01826ef97d2`

```dockerfile
```

-	Layers:
	-	`sha256:f5caf2dd8813129b9c4c95cdbf9475460c6671d9b69076c9e01ff6fb31a12d18`  
		Last Modified: Wed, 22 Apr 2026 01:43:50 GMT  
		Size: 2.9 MB (2872914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b2522c54541b05c9d9fe6b86bcfddd0e313001f46fd9647c6b93e4f5b2a456e`  
		Last Modified: Wed, 22 Apr 2026 01:43:49 GMT  
		Size: 16.2 KB (16191 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11-alpine`

```console
$ docker pull chronograf@sha256:41913992a072a2fc5b7f935b05e0851f1cadb84cf0ce5e3b14ce5444905127da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.11-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c090b122c302e943ac7d72fd923b48ff169e17fbda740aac60dfa831518d5121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64549785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42e0e3604110e24dd093c463181f09858be50da21ae05d5717dc445cfff5973`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 23:11:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 23:11:15 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
ENV CHRONOGRAF_VERSION=1.11.1
# Fri, 17 Apr 2026 23:11:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 23:11:21 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 23:11:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 23:11:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d762789db4e902950bb375830c4f4c99b5e4a7dd0bc04b11f6337c42a3ddd971`  
		Last Modified: Fri, 17 Apr 2026 23:11:35 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1cd6ba1ef8b8e04a45ae4016f3187f96106910e81e0c71108f7230e9580303`  
		Last Modified: Fri, 17 Apr 2026 23:11:34 GMT  
		Size: 312.2 KB (312180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5baddaa9254e37a2265eacbc7a4b1dc2a700b80fc46b81b0910cba783d39d3a6`  
		Last Modified: Fri, 17 Apr 2026 23:11:36 GMT  
		Size: 60.4 MB (60404685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a6029ead94f040b875618c5b1482280471567cc37e931256ddb5f10940fddf`  
		Last Modified: Fri, 17 Apr 2026 23:11:35 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149ba4ecbed81f5a0d71c4a36228a7358676a0318042091d57d9ebd838b22a97`  
		Last Modified: Fri, 17 Apr 2026 23:11:36 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0d4fa8934d0846ae6e80c94c8a5946666647b429e5ff0b7db401883a0118c5`  
		Last Modified: Fri, 17 Apr 2026 23:11:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:deed3830371624aecdcb39e815df4648f0de119cdc5a05bbd30f6b7a1a4c3a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 KB (287057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21e1c2c2004f0ee1912ce1eedda595a55d0f9016c982cf9dc72208e99479993`

```dockerfile
```

-	Layers:
	-	`sha256:74295d628b90e6849531142973a6c3f1574b2d682d0414e65814e291922813d0`  
		Last Modified: Fri, 17 Apr 2026 23:11:35 GMT  
		Size: 269.3 KB (269328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c80a873777e4bc9f51b18b07552f5cc2efc09a9e81f7a97d685a46014e3665c4`  
		Last Modified: Fri, 17 Apr 2026 23:11:34 GMT  
		Size: 17.7 KB (17729 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11.2`

**does not exist** (yet?)

## `chronograf:1.11.2-alpine`

**does not exist** (yet?)

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:91a11019d5082212a0e21051c3273cc6559e8b17ddcbbc9c5d4adee10a58c845
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
$ docker pull chronograf@sha256:a3d7f2e4cbdd261861262e31636a7375c420f24681e6a7a7d10eacc6ae341948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69888359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936e5344cea578f66ddbd07af0aaf66af55bf6e94ef31433fd83809b64843f6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:39:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:39:44 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 22 Apr 2026 01:39:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:39:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:39:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:39:44 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:39:44 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:39:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:39:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:39:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ed229e15ddd59304f4da8f69a26a20d051bbc252533e755f7c8500fa66d87`  
		Last Modified: Wed, 22 Apr 2026 01:39:54 GMT  
		Size: 5.2 MB (5241719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc1aa2c9df189a64b7fc801f45af0ea69c0f42a0818bddc9f18bc98b3a92514`  
		Last Modified: Wed, 22 Apr 2026 01:39:55 GMT  
		Size: 34.4 MB (34364328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dca5f17ef138d7894ffd5972c1b6cead73de0e54ccc199c3f8c2cdaef0f2b8`  
		Last Modified: Wed, 22 Apr 2026 01:39:54 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2244ac94a66246d4b67313d8b6b36b0e6ff0e57290b66dabd2c18da6e9f872`  
		Last Modified: Wed, 22 Apr 2026 01:39:54 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce38b1256d8811efd030568515d57f1552750e9ee9c2ed39af381b086440e9d4`  
		Last Modified: Wed, 22 Apr 2026 01:39:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:4c61e69c3986763520806025a1d1a896a28c91bfd9767e702a275a72a63cd948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684e99200972cfef198b556aa17b6b2175feed2c715aa0a970495767ae516b96`

```dockerfile
```

-	Layers:
	-	`sha256:e440119e93037de5afbd61a168c11e89bfcf6f42529eb293aedb2bdaa940a36e`  
		Last Modified: Wed, 22 Apr 2026 01:39:54 GMT  
		Size: 3.1 MB (3112931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ce7e528052d0d388fe8a4544b52d225e2417eb8135a28899fc8cc234818ce9b`  
		Last Modified: Wed, 22 Apr 2026 01:39:54 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ce01ede63e8165ead12ab13ed4ee69aed2081e644fea07d4c03333088720fb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62620679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071aa8c032322298d21cf8ab8968f03d754e672e8b5c5e1f2f01cd785afa5481`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:20:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:20:35 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 22 Apr 2026 02:20:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:20:35 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 02:20:35 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 02:20:35 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 02:20:35 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 02:20:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:20:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:20:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:50e0a76bf8c998cc60af8a2a79ba2b2fade75366a3cf5b118733534c51339aab`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 25.6 MB (25551211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa8a2930bdda1102c7d1b2f1ea9f4fbb6856a17c020ec571c257e61c029e322`  
		Last Modified: Wed, 22 Apr 2026 02:20:44 GMT  
		Size: 4.5 MB (4510036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0a18a10da37fddfe2242d66d5f39a26c2926d75bbada1800157bff7eb31839`  
		Last Modified: Wed, 22 Apr 2026 02:20:44 GMT  
		Size: 32.5 MB (32535045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad2357018837b248121efc203aa64fa1571f0b4d8959336d37779ad90910e21`  
		Last Modified: Wed, 22 Apr 2026 02:20:43 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2caa541522d6335390fb35b7bc5a7126cec01a59fb933e5d082936346e993fe5`  
		Last Modified: Wed, 22 Apr 2026 02:20:44 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3c80565ee67ff0b6764bd6549e2ea746519b12700b37303c627c21dcd4d320`  
		Last Modified: Wed, 22 Apr 2026 02:20:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:aaa2a03bee5e9469ce806edd3b110211321b5885591b52169474029b6f456e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0d4d40545873ec05cfcd934388e71e082549d4e26ea3f8903cfdac3a3a877`

```dockerfile
```

-	Layers:
	-	`sha256:33a9a7145ccd4638c2932c773dc8b51a527ada0ef22464cfbbe98e45a31feeba`  
		Last Modified: Wed, 22 Apr 2026 02:20:44 GMT  
		Size: 3.1 MB (3115202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:718f1bd5b9e794cc51e37f383c110f891913d807c4323d7134e7c0e21825c9bb`  
		Last Modified: Wed, 22 Apr 2026 02:20:43 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c77df7122cd6752821dc4b6b6bfdb86a97e9a4eaa169b1f8c28a3f856d096b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66426153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9bbfabb445d4b394a8cbbe82b3da4614f4c5c4d5e13175771c073c2aab8a12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:43:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 22 Apr 2026 01:43:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:43:35 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:43:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:43:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e94f7dd017c0f3ff08400fb62062a48db4770bfdd9a6afff7d45f06569c781b`  
		Last Modified: Wed, 22 Apr 2026 01:43:46 GMT  
		Size: 5.2 MB (5229759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98740fa1db7175dc557fdcb207a69cced328e231ed29756fca4a57202c2c305`  
		Last Modified: Wed, 22 Apr 2026 01:43:47 GMT  
		Size: 32.4 MB (32429482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd48a3cff27a2051e6262d4f560d0f26fea205e4b1f553cd09490fe8914de2`  
		Last Modified: Wed, 22 Apr 2026 01:43:45 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c37e91634ff23c87959b2fb68709baea219752deda8dd177345d0dddd0dfbc`  
		Last Modified: Wed, 22 Apr 2026 01:43:45 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7d0f94670518580860bbb578a6837b8a0ed9c67eb0e6b1555c974f87be8036`  
		Last Modified: Wed, 22 Apr 2026 01:43:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:91005d5ab8b5eef938da5dc6dc998eadb2a7184392a0f1885615660c632dc819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edffe9616bd9530f8a61864044d71424874647c29ba9a45d2e83097d007a6c1c`

```dockerfile
```

-	Layers:
	-	`sha256:85ec6d78149b9e98efaa33070593c894675b3f7f66d8fdedc3ff4b9bb25c7bd1`  
		Last Modified: Wed, 22 Apr 2026 01:43:46 GMT  
		Size: 3.1 MB (3113180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d96090d0f7bf79df8e30752c7b95a0c402ab64d73bf1be0422207b466b1c98e`  
		Last Modified: Wed, 22 Apr 2026 01:43:45 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:a04ddb5aa8a08101f1c16ed3a397ee4c00dcd1ed76208f0bb50c429653294520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ede13c1b68d5428c626bce6c59f200e2d2f72711e9e1b8d337bf08d17699af43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23147985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1664c3e0943c41cb0fbb18db90fb8ff72cabbfa2721d8832c2b45834ec9ce934`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:23:28 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 17 Apr 2026 00:23:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 00:23:32 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 00:23:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a582e81c7ed2cd8d0c8d79c49ea73d52bfddf13469c4d924f55b6970462df01`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 289.1 KB (289074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa13e0a8fa89698c9691e91370f5c5da3380b44b6ac29319a4e90a09eefbe8e`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 19.2 MB (19203941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782461697da8106fc90296b3ce4a6a407db932533ecd9a4da24a10753acdcf1e`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74b1d522539dce72171cebaa3d6dd0ca9ca821e4a34e4b76dc19daa0169a5c3`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f5e2ebfd8736864ace9d37094fa3ee04d93d2ae268e430ca56f87eec508a5`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:84b7bdc8d23f218c2fe980ddfdeac820e2627fc7d91f2c4202a8f26deb5e9db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 KB (244523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983e28495a7b578fd93bcd0c3b0e98c83deddb61c866fc1c2f690ba762da5922`

```dockerfile
```

-	Layers:
	-	`sha256:365c42781b673303c2c41d46ccc50ac379917ed1053135d373385311589519d1`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 227.7 KB (227654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8bfb7d23b735a7cd84710b5948163b988bb486b65c2263456936b73344a8c85`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:91a11019d5082212a0e21051c3273cc6559e8b17ddcbbc9c5d4adee10a58c845
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
$ docker pull chronograf@sha256:a3d7f2e4cbdd261861262e31636a7375c420f24681e6a7a7d10eacc6ae341948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69888359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936e5344cea578f66ddbd07af0aaf66af55bf6e94ef31433fd83809b64843f6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:39:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:39:44 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 22 Apr 2026 01:39:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:39:44 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:39:44 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:39:44 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:39:44 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:39:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:39:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:39:44 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ed229e15ddd59304f4da8f69a26a20d051bbc252533e755f7c8500fa66d87`  
		Last Modified: Wed, 22 Apr 2026 01:39:54 GMT  
		Size: 5.2 MB (5241719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc1aa2c9df189a64b7fc801f45af0ea69c0f42a0818bddc9f18bc98b3a92514`  
		Last Modified: Wed, 22 Apr 2026 01:39:55 GMT  
		Size: 34.4 MB (34364328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dca5f17ef138d7894ffd5972c1b6cead73de0e54ccc199c3f8c2cdaef0f2b8`  
		Last Modified: Wed, 22 Apr 2026 01:39:54 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2244ac94a66246d4b67313d8b6b36b0e6ff0e57290b66dabd2c18da6e9f872`  
		Last Modified: Wed, 22 Apr 2026 01:39:54 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce38b1256d8811efd030568515d57f1552750e9ee9c2ed39af381b086440e9d4`  
		Last Modified: Wed, 22 Apr 2026 01:39:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:4c61e69c3986763520806025a1d1a896a28c91bfd9767e702a275a72a63cd948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684e99200972cfef198b556aa17b6b2175feed2c715aa0a970495767ae516b96`

```dockerfile
```

-	Layers:
	-	`sha256:e440119e93037de5afbd61a168c11e89bfcf6f42529eb293aedb2bdaa940a36e`  
		Last Modified: Wed, 22 Apr 2026 01:39:54 GMT  
		Size: 3.1 MB (3112931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ce7e528052d0d388fe8a4544b52d225e2417eb8135a28899fc8cc234818ce9b`  
		Last Modified: Wed, 22 Apr 2026 01:39:54 GMT  
		Size: 15.8 KB (15774 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ce01ede63e8165ead12ab13ed4ee69aed2081e644fea07d4c03333088720fb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62620679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071aa8c032322298d21cf8ab8968f03d754e672e8b5c5e1f2f01cd785afa5481`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:20:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:20:35 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 22 Apr 2026 02:20:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:20:35 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 02:20:35 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 02:20:35 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 02:20:35 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 02:20:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:20:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:20:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:50e0a76bf8c998cc60af8a2a79ba2b2fade75366a3cf5b118733534c51339aab`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 25.6 MB (25551211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa8a2930bdda1102c7d1b2f1ea9f4fbb6856a17c020ec571c257e61c029e322`  
		Last Modified: Wed, 22 Apr 2026 02:20:44 GMT  
		Size: 4.5 MB (4510036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0a18a10da37fddfe2242d66d5f39a26c2926d75bbada1800157bff7eb31839`  
		Last Modified: Wed, 22 Apr 2026 02:20:44 GMT  
		Size: 32.5 MB (32535045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad2357018837b248121efc203aa64fa1571f0b4d8959336d37779ad90910e21`  
		Last Modified: Wed, 22 Apr 2026 02:20:43 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2caa541522d6335390fb35b7bc5a7126cec01a59fb933e5d082936346e993fe5`  
		Last Modified: Wed, 22 Apr 2026 02:20:44 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3c80565ee67ff0b6764bd6549e2ea746519b12700b37303c627c21dcd4d320`  
		Last Modified: Wed, 22 Apr 2026 02:20:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:aaa2a03bee5e9469ce806edd3b110211321b5885591b52169474029b6f456e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0d4d40545873ec05cfcd934388e71e082549d4e26ea3f8903cfdac3a3a877`

```dockerfile
```

-	Layers:
	-	`sha256:33a9a7145ccd4638c2932c773dc8b51a527ada0ef22464cfbbe98e45a31feeba`  
		Last Modified: Wed, 22 Apr 2026 02:20:44 GMT  
		Size: 3.1 MB (3115202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:718f1bd5b9e794cc51e37f383c110f891913d807c4323d7134e7c0e21825c9bb`  
		Last Modified: Wed, 22 Apr 2026 02:20:43 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c77df7122cd6752821dc4b6b6bfdb86a97e9a4eaa169b1f8c28a3f856d096b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66426153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9bbfabb445d4b394a8cbbe82b3da4614f4c5c4d5e13175771c073c2aab8a12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:43:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 22 Apr 2026 01:43:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:43:35 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:43:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:43:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e94f7dd017c0f3ff08400fb62062a48db4770bfdd9a6afff7d45f06569c781b`  
		Last Modified: Wed, 22 Apr 2026 01:43:46 GMT  
		Size: 5.2 MB (5229759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98740fa1db7175dc557fdcb207a69cced328e231ed29756fca4a57202c2c305`  
		Last Modified: Wed, 22 Apr 2026 01:43:47 GMT  
		Size: 32.4 MB (32429482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cd48a3cff27a2051e6262d4f560d0f26fea205e4b1f553cd09490fe8914de2`  
		Last Modified: Wed, 22 Apr 2026 01:43:45 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c37e91634ff23c87959b2fb68709baea219752deda8dd177345d0dddd0dfbc`  
		Last Modified: Wed, 22 Apr 2026 01:43:45 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7d0f94670518580860bbb578a6837b8a0ed9c67eb0e6b1555c974f87be8036`  
		Last Modified: Wed, 22 Apr 2026 01:43:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:91005d5ab8b5eef938da5dc6dc998eadb2a7184392a0f1885615660c632dc819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edffe9616bd9530f8a61864044d71424874647c29ba9a45d2e83097d007a6c1c`

```dockerfile
```

-	Layers:
	-	`sha256:85ec6d78149b9e98efaa33070593c894675b3f7f66d8fdedc3ff4b9bb25c7bd1`  
		Last Modified: Wed, 22 Apr 2026 01:43:46 GMT  
		Size: 3.1 MB (3113180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d96090d0f7bf79df8e30752c7b95a0c402ab64d73bf1be0422207b466b1c98e`  
		Last Modified: Wed, 22 Apr 2026 01:43:45 GMT  
		Size: 15.9 KB (15868 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:a04ddb5aa8a08101f1c16ed3a397ee4c00dcd1ed76208f0bb50c429653294520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:ede13c1b68d5428c626bce6c59f200e2d2f72711e9e1b8d337bf08d17699af43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23147985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1664c3e0943c41cb0fbb18db90fb8ff72cabbfa2721d8832c2b45834ec9ce934`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:23:28 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 17 Apr 2026 00:23:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 00:23:32 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 00:23:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a582e81c7ed2cd8d0c8d79c49ea73d52bfddf13469c4d924f55b6970462df01`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 289.1 KB (289074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa13e0a8fa89698c9691e91370f5c5da3380b44b6ac29319a4e90a09eefbe8e`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 19.2 MB (19203941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782461697da8106fc90296b3ce4a6a407db932533ecd9a4da24a10753acdcf1e`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74b1d522539dce72171cebaa3d6dd0ca9ca821e4a34e4b76dc19daa0169a5c3`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f5e2ebfd8736864ace9d37094fa3ee04d93d2ae268e430ca56f87eec508a5`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:84b7bdc8d23f218c2fe980ddfdeac820e2627fc7d91f2c4202a8f26deb5e9db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 KB (244523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983e28495a7b578fd93bcd0c3b0e98c83deddb61c866fc1c2f690ba762da5922`

```dockerfile
```

-	Layers:
	-	`sha256:365c42781b673303c2c41d46ccc50ac379917ed1053135d373385311589519d1`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 227.7 KB (227654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8bfb7d23b735a7cd84710b5948163b988bb486b65c2263456936b73344a8c85`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 16.9 KB (16869 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:9a01e197f48fd232f55a71ef4c2efc95cb95181fac48edcf9bfe7503d22e5181
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
$ docker pull chronograf@sha256:e7883279781f547151b9ab6899f27cb0d3f30d114cb66ad422ee499adef022e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223cbf7c1d0864f0383e27666b88840a5ad16dced2315809f65d61538d2fa1f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:39:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:39:52 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 22 Apr 2026 01:39:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:39:52 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:39:52 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:39:52 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:39:52 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:39:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:39:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:39:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7712c9fc4dbcc288762e569f31802909473a2d9cac8016bd5de2a68e8ee7caf2`  
		Last Modified: Wed, 22 Apr 2026 01:40:04 GMT  
		Size: 5.2 MB (5241715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfc0b4939cee4705fe3fbe62eefd20b3fa4adee14632f1efba8816be58089fd`  
		Last Modified: Wed, 22 Apr 2026 01:40:04 GMT  
		Size: 35.0 MB (35011766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345657e49288913bdc59f54dec7eec1702deb3ef1c8d37e4351af0e99dbe8898`  
		Last Modified: Wed, 22 Apr 2026 01:40:03 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f63a05072b43ba431e72a5bb3e7ccede2a845e6c06ebb114523fe92fd7a24d9`  
		Last Modified: Wed, 22 Apr 2026 01:40:03 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adebc1f54f520decdd97c51276e637e23539e62c9d992e486188b5f5a55f1af3`  
		Last Modified: Wed, 22 Apr 2026 01:40:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:b32c9bbf0ca17ebb4b4974c94072c212085eba5ae4e828c65472121be5204d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e41d82c29e919b206ad14c5bffa87e62beda7fb77cfcf10ed65e6c5f1f1a7a1`

```dockerfile
```

-	Layers:
	-	`sha256:b12fad8b62959d578cbce1e1e3b113d04b2d87ab374271431997ec0b85643416`  
		Last Modified: Wed, 22 Apr 2026 01:40:04 GMT  
		Size: 3.1 MB (3118141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c56c87818d33f32856e91ed1708940db1a1909f82e33f251172a6485bfe9fbc`  
		Last Modified: Wed, 22 Apr 2026 01:40:03 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4658cdbfa7f73214975bf7d71914787afca47fa76eb84d3d6edebf1d633c03ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63397194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37466a87b3b0ffed38b161b3e53a458ee997255b8f7acfa443f211d7cd8b6a3b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:20:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:20:40 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 22 Apr 2026 02:20:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:20:40 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 02:20:40 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 02:20:40 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 02:20:40 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 02:20:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:20:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:20:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:50e0a76bf8c998cc60af8a2a79ba2b2fade75366a3cf5b118733534c51339aab`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 25.6 MB (25551211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777ef1a84ac794a41c5b462899398fc48ffb961cd45f79d95513e9d52b400326`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 4.5 MB (4510007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0bf5c1980e3221928061b42a7466d43f4e2bdca25f3c62206d0eb430ed6118`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 33.3 MB (33311596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388f267ba748c318557009a97c93ad06a2e71111a82316854b65d3a94f7b500e`  
		Last Modified: Wed, 22 Apr 2026 02:20:49 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8919c976c1296c8e74ec1750b7bdb797a50582be93923135d960c02a27c977d`  
		Last Modified: Wed, 22 Apr 2026 02:20:49 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e75f3291c9a1e00a39e4e7a9a0080a3d6755ed676b6d1ca1d707545bbdca11`  
		Last Modified: Wed, 22 Apr 2026 02:20:51 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:9eba4deae490bcf308ed1c05711804f888bcbc8181e9550a1ad2f279afef01e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bd748d443a5216b2f015d071d2ec1245012dc19f17ace665cd35cb54a2e508`

```dockerfile
```

-	Layers:
	-	`sha256:460f702ce440244d4866a31f86f76df9711985289eb729691cb5345c424e9b6e`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 3.1 MB (3120412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62188ab638f74e5fde698696441561177c34f51d401ee91bba869a862ef3e1`  
		Last Modified: Wed, 22 Apr 2026 02:20:49 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:826389c278c41890822cf568605ab003fa967a65569f6cddccf920936809188b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67179078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6640fd5dceb79c31ca474643c58b4dfce1d957a1db1c4c491186f3b7aedb3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:43:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:43:28 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 22 Apr 2026 01:43:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:43:28 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:43:28 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:43:28 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:43:28 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:43:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:43:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:43:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a7574c30c44c159b184368466731f2fc46e2eb0af2188b5aef7e657e61e693`  
		Last Modified: Wed, 22 Apr 2026 01:43:38 GMT  
		Size: 5.2 MB (5229812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a16ea49c2e96982716ff84121af685d56c5aa5e669d4982eb5f409dbe70def4`  
		Last Modified: Wed, 22 Apr 2026 01:43:39 GMT  
		Size: 33.2 MB (33182361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1e8c48e2f6c8e713a4ec7bd30aba8659abb8d4f4358ac4a19a011e5e09e776`  
		Last Modified: Wed, 22 Apr 2026 01:43:37 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81191d1af88c4bbd74f3d02847ba7fe4f664c9c2ae89d639e24c66339b2f8c7`  
		Last Modified: Wed, 22 Apr 2026 01:43:38 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b4a169c43cd3bae89a0217cd6d3f20df75043047b7b4cb06ee1bc2bd9a8ac3`  
		Last Modified: Wed, 22 Apr 2026 01:43:39 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:74060fd831caedd68ce4d8af9034ae53fb0be2099cac6b61ac0c691cb2c00634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d742cab26b36e8e610703837debf186ee16416c4b7bdae1216d01300853351b`

```dockerfile
```

-	Layers:
	-	`sha256:c3283b0f194d25e062f37882a6183ca40f1ce25b3c665741fa3755d34663ff32`  
		Last Modified: Wed, 22 Apr 2026 01:43:38 GMT  
		Size: 3.1 MB (3118390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:632a8fd072d44696c70d0a0248b0dd3380b507d5ff4039f68d84caef1ce90cf0`  
		Last Modified: Wed, 22 Apr 2026 01:43:37 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:0f80cd3823ff72714fb0be9429588b58a6cd474733e0369bc7f9181346b1d5cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f621eed42ec67e2c0af874c13b22cf7c5eca4a2f92496e0e777e83e0d0e54a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23616085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4f080ba353421341131d427d195e080f057481b2369a3ddd4db288e7a49570`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:23:28 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 17 Apr 2026 00:23:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 00:23:32 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 00:23:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a582e81c7ed2cd8d0c8d79c49ea73d52bfddf13469c4d924f55b6970462df01`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 289.1 KB (289074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaea6127a47f8ad745d11f7e8ea7511652ab602293817f95bee9cac7032fc393`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 19.7 MB (19672041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782461697da8106fc90296b3ce4a6a407db932533ecd9a4da24a10753acdcf1e`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74b1d522539dce72171cebaa3d6dd0ca9ca821e4a34e4b76dc19daa0169a5c3`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f5e2ebfd8736864ace9d37094fa3ee04d93d2ae268e430ca56f87eec508a5`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:4be611f408b68b71f2ce6e27bd942207676513556d3d2d9ec7df73b913fb49b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 KB (249732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b7b7e44d247f14c51737c4557d3e8bdc7e3cc786d83a99199fb64c7df6355c`

```dockerfile
```

-	Layers:
	-	`sha256:6c6b091fcc28e6afcad2a5fe2faed4c1dcff63c11868d95adf1b2056b7bbcae1`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 232.9 KB (232866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d10cb23e42c41cf8502d564e4146e704991853b11b9b54a94f89af55f1264769`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 16.9 KB (16866 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:9a01e197f48fd232f55a71ef4c2efc95cb95181fac48edcf9bfe7503d22e5181
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
$ docker pull chronograf@sha256:e7883279781f547151b9ab6899f27cb0d3f30d114cb66ad422ee499adef022e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223cbf7c1d0864f0383e27666b88840a5ad16dced2315809f65d61538d2fa1f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:39:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:39:52 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 22 Apr 2026 01:39:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:39:52 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:39:52 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:39:52 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:39:52 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:39:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:39:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:39:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7712c9fc4dbcc288762e569f31802909473a2d9cac8016bd5de2a68e8ee7caf2`  
		Last Modified: Wed, 22 Apr 2026 01:40:04 GMT  
		Size: 5.2 MB (5241715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfc0b4939cee4705fe3fbe62eefd20b3fa4adee14632f1efba8816be58089fd`  
		Last Modified: Wed, 22 Apr 2026 01:40:04 GMT  
		Size: 35.0 MB (35011766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345657e49288913bdc59f54dec7eec1702deb3ef1c8d37e4351af0e99dbe8898`  
		Last Modified: Wed, 22 Apr 2026 01:40:03 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f63a05072b43ba431e72a5bb3e7ccede2a845e6c06ebb114523fe92fd7a24d9`  
		Last Modified: Wed, 22 Apr 2026 01:40:03 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adebc1f54f520decdd97c51276e637e23539e62c9d992e486188b5f5a55f1af3`  
		Last Modified: Wed, 22 Apr 2026 01:40:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:b32c9bbf0ca17ebb4b4974c94072c212085eba5ae4e828c65472121be5204d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e41d82c29e919b206ad14c5bffa87e62beda7fb77cfcf10ed65e6c5f1f1a7a1`

```dockerfile
```

-	Layers:
	-	`sha256:b12fad8b62959d578cbce1e1e3b113d04b2d87ab374271431997ec0b85643416`  
		Last Modified: Wed, 22 Apr 2026 01:40:04 GMT  
		Size: 3.1 MB (3118141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c56c87818d33f32856e91ed1708940db1a1909f82e33f251172a6485bfe9fbc`  
		Last Modified: Wed, 22 Apr 2026 01:40:03 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:4658cdbfa7f73214975bf7d71914787afca47fa76eb84d3d6edebf1d633c03ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63397194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37466a87b3b0ffed38b161b3e53a458ee997255b8f7acfa443f211d7cd8b6a3b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:20:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 02:20:40 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 22 Apr 2026 02:20:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 02:20:40 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 02:20:40 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 02:20:40 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 02:20:40 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 02:20:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:20:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:20:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:50e0a76bf8c998cc60af8a2a79ba2b2fade75366a3cf5b118733534c51339aab`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 25.6 MB (25551211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777ef1a84ac794a41c5b462899398fc48ffb961cd45f79d95513e9d52b400326`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 4.5 MB (4510007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0bf5c1980e3221928061b42a7466d43f4e2bdca25f3c62206d0eb430ed6118`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 33.3 MB (33311596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388f267ba748c318557009a97c93ad06a2e71111a82316854b65d3a94f7b500e`  
		Last Modified: Wed, 22 Apr 2026 02:20:49 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8919c976c1296c8e74ec1750b7bdb797a50582be93923135d960c02a27c977d`  
		Last Modified: Wed, 22 Apr 2026 02:20:49 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e75f3291c9a1e00a39e4e7a9a0080a3d6755ed676b6d1ca1d707545bbdca11`  
		Last Modified: Wed, 22 Apr 2026 02:20:51 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:9eba4deae490bcf308ed1c05711804f888bcbc8181e9550a1ad2f279afef01e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bd748d443a5216b2f015d071d2ec1245012dc19f17ace665cd35cb54a2e508`

```dockerfile
```

-	Layers:
	-	`sha256:460f702ce440244d4866a31f86f76df9711985289eb729691cb5345c424e9b6e`  
		Last Modified: Wed, 22 Apr 2026 02:20:50 GMT  
		Size: 3.1 MB (3120412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc62188ab638f74e5fde698696441561177c34f51d401ee91bba869a862ef3e1`  
		Last Modified: Wed, 22 Apr 2026 02:20:49 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:826389c278c41890822cf568605ab003fa967a65569f6cddccf920936809188b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67179078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6640fd5dceb79c31ca474643c58b4dfce1d957a1db1c4c491186f3b7aedb3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:43:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:43:28 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 22 Apr 2026 01:43:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:43:28 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:43:28 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:43:28 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:43:28 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:43:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:43:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:43:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a7574c30c44c159b184368466731f2fc46e2eb0af2188b5aef7e657e61e693`  
		Last Modified: Wed, 22 Apr 2026 01:43:38 GMT  
		Size: 5.2 MB (5229812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a16ea49c2e96982716ff84121af685d56c5aa5e669d4982eb5f409dbe70def4`  
		Last Modified: Wed, 22 Apr 2026 01:43:39 GMT  
		Size: 33.2 MB (33182361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1e8c48e2f6c8e713a4ec7bd30aba8659abb8d4f4358ac4a19a011e5e09e776`  
		Last Modified: Wed, 22 Apr 2026 01:43:37 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81191d1af88c4bbd74f3d02847ba7fe4f664c9c2ae89d639e24c66339b2f8c7`  
		Last Modified: Wed, 22 Apr 2026 01:43:38 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b4a169c43cd3bae89a0217cd6d3f20df75043047b7b4cb06ee1bc2bd9a8ac3`  
		Last Modified: Wed, 22 Apr 2026 01:43:39 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:74060fd831caedd68ce4d8af9034ae53fb0be2099cac6b61ac0c691cb2c00634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d742cab26b36e8e610703837debf186ee16416c4b7bdae1216d01300853351b`

```dockerfile
```

-	Layers:
	-	`sha256:c3283b0f194d25e062f37882a6183ca40f1ce25b3c665741fa3755d34663ff32`  
		Last Modified: Wed, 22 Apr 2026 01:43:38 GMT  
		Size: 3.1 MB (3118390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:632a8fd072d44696c70d0a0248b0dd3380b507d5ff4039f68d84caef1ce90cf0`  
		Last Modified: Wed, 22 Apr 2026 01:43:37 GMT  
		Size: 15.9 KB (15862 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:0f80cd3823ff72714fb0be9429588b58a6cd474733e0369bc7f9181346b1d5cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f621eed42ec67e2c0af874c13b22cf7c5eca4a2f92496e0e777e83e0d0e54a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23616085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4f080ba353421341131d427d195e080f057481b2369a3ddd4db288e7a49570`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:23:28 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 17 Apr 2026 00:23:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 00:23:32 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 00:23:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:23:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a582e81c7ed2cd8d0c8d79c49ea73d52bfddf13469c4d924f55b6970462df01`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 289.1 KB (289074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaea6127a47f8ad745d11f7e8ea7511652ab602293817f95bee9cac7032fc393`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 19.7 MB (19672041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782461697da8106fc90296b3ce4a6a407db932533ecd9a4da24a10753acdcf1e`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74b1d522539dce72171cebaa3d6dd0ca9ca821e4a34e4b76dc19daa0169a5c3`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f5e2ebfd8736864ace9d37094fa3ee04d93d2ae268e430ca56f87eec508a5`  
		Last Modified: Fri, 17 Apr 2026 00:23:40 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:4be611f408b68b71f2ce6e27bd942207676513556d3d2d9ec7df73b913fb49b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 KB (249732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b7b7e44d247f14c51737c4557d3e8bdc7e3cc786d83a99199fb64c7df6355c`

```dockerfile
```

-	Layers:
	-	`sha256:6c6b091fcc28e6afcad2a5fe2faed4c1dcff63c11868d95adf1b2056b7bbcae1`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 232.9 KB (232866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d10cb23e42c41cf8502d564e4146e704991853b11b9b54a94f89af55f1264769`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 16.9 KB (16866 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:41913992a072a2fc5b7f935b05e0851f1cadb84cf0ce5e3b14ce5444905127da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:c090b122c302e943ac7d72fd923b48ff169e17fbda740aac60dfa831518d5121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64549785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42e0e3604110e24dd093c463181f09858be50da21ae05d5717dc445cfff5973`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 23:11:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 23:11:15 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
ENV CHRONOGRAF_VERSION=1.11.1
# Fri, 17 Apr 2026 23:11:21 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
EXPOSE map[8888/tcp:{}]
# Fri, 17 Apr 2026 23:11:21 GMT
VOLUME [/var/lib/chronograf]
# Fri, 17 Apr 2026 23:11:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 23:11:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 23:11:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d762789db4e902950bb375830c4f4c99b5e4a7dd0bc04b11f6337c42a3ddd971`  
		Last Modified: Fri, 17 Apr 2026 23:11:35 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1cd6ba1ef8b8e04a45ae4016f3187f96106910e81e0c71108f7230e9580303`  
		Last Modified: Fri, 17 Apr 2026 23:11:34 GMT  
		Size: 312.2 KB (312180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5baddaa9254e37a2265eacbc7a4b1dc2a700b80fc46b81b0910cba783d39d3a6`  
		Last Modified: Fri, 17 Apr 2026 23:11:36 GMT  
		Size: 60.4 MB (60404685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a6029ead94f040b875618c5b1482280471567cc37e931256ddb5f10940fddf`  
		Last Modified: Fri, 17 Apr 2026 23:11:35 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149ba4ecbed81f5a0d71c4a36228a7358676a0318042091d57d9ebd838b22a97`  
		Last Modified: Fri, 17 Apr 2026 23:11:36 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0d4fa8934d0846ae6e80c94c8a5946666647b429e5ff0b7db401883a0118c5`  
		Last Modified: Fri, 17 Apr 2026 23:11:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:deed3830371624aecdcb39e815df4648f0de119cdc5a05bbd30f6b7a1a4c3a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 KB (287057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21e1c2c2004f0ee1912ce1eedda595a55d0f9016c982cf9dc72208e99479993`

```dockerfile
```

-	Layers:
	-	`sha256:74295d628b90e6849531142973a6c3f1574b2d682d0414e65814e291922813d0`  
		Last Modified: Fri, 17 Apr 2026 23:11:35 GMT  
		Size: 269.3 KB (269328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c80a873777e4bc9f51b18b07552f5cc2efc09a9e81f7a97d685a46014e3665c4`  
		Last Modified: Fri, 17 Apr 2026 23:11:34 GMT  
		Size: 17.7 KB (17729 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:0f07a3a3ef4e82deb075683f72a89d194d780f1805d5232622f5619854a12da9
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
$ docker pull chronograf@sha256:b789cc3f234aca70cbe48a1b756ccdae8e27e5249b4254d0b40768d5fb554504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98523348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76ace0fc98017a90832ebf70bbdb13b0b5b83fb6ccf5fc8558b4dab85b58ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:39:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
ENV CHRONOGRAF_VERSION=1.11.1
# Wed, 22 Apr 2026 01:40:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:40:03 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:40:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890bcea591fcf347b2fbf1d61b2a6b1983750cd5d9049eeda31e36c124f50e82`  
		Last Modified: Wed, 22 Apr 2026 01:40:20 GMT  
		Size: 7.9 MB (7880761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e9a112a46a66d65e1f9fd68ce3b3bb69113b37aa907bb408f12f0fdd304ee8`  
		Last Modified: Wed, 22 Apr 2026 01:40:21 GMT  
		Size: 62.4 MB (62381869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8a71fdbf6fb57d2ef3a4ee7881fa229d32585df420363632d945c6360bbaa`  
		Last Modified: Wed, 22 Apr 2026 01:40:20 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d9a90b228f0f58f48584d9b66a142f7f4511640878b26c8cf83e1a8cfddeba`  
		Last Modified: Wed, 22 Apr 2026 01:40:19 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d54185746004b87475a722a316bd05ef4ef68c46df2d550d1fa851031c7b511`  
		Last Modified: Wed, 22 Apr 2026 01:40:21 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:b6de94af8207cd47c082d6404c39429ed5d2c1fd8dd8c89f1f8ce7181c3bf707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7411f7288317e0e8573591b761771a9f6586041704aca4e3a8cb098c4717b7`

```dockerfile
```

-	Layers:
	-	`sha256:aa00abfb671c2cd3e6adb2c094a43dea281dd9b55f0c7434ac77dd8fe565fa5a`  
		Last Modified: Wed, 22 Apr 2026 01:40:19 GMT  
		Size: 2.9 MB (2873700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:852da94dc4b795b75cd9dd711b2e24141e43edbb44df342a56361a3f11e96403`  
		Last Modified: Wed, 22 Apr 2026 01:40:19 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7f6ba8a05e8752787341b7fe2a6a74810b06aa9fa70a1a0228f775cc695b037a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930d1c377ac04e3da986523b9e03970d9aff20f8036670f211d374ae5e6e562c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:04:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 07 Apr 2026 02:04:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 02:04:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 02:04:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:04:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde4224141eb326416434e57e6985960fa0299c171636ec51c978d7483ded221`  
		Last Modified: Tue, 07 Apr 2026 02:04:50 GMT  
		Size: 6.5 MB (6512130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39644797429280d1790a41b83be262964fe685b66a13098f85a2830ef136af23`  
		Last Modified: Tue, 07 Apr 2026 02:04:51 GMT  
		Size: 46.3 MB (46320009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a038716dc519bd0d53565ee9d170bb27389cee982f799ed02c5b30bb400da63b`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2857e0024941e8431e0d2e7288ff873bb60af2b99250a6c109fb700e616232c`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac7ccabd4f0e669d232e23f27536a4797faec571f1d5b385e8d37e9543ad1d4`  
		Last Modified: Tue, 07 Apr 2026 02:04:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:d033ac4c98bc3deb3c46315bff42913e431c32321890ec7914cd6b43bf0a4454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a769173f691e7dbe1bbac685b1b6d2cf8af5e40c11a7536386e603ca5e558e45`

```dockerfile
```

-	Layers:
	-	`sha256:dff92a3ce28b58e918bb8a1b393141f0d15f0a7436d538d1b53bafdf3cd2f3f0`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29723eb32c4a4046b83b01b8e97bd5b93cfc334f24c3dcc9145d178038a36230`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:68bafb55be081cc169b6026b419c1b5099ae8ef2e77f47aa67e3c7ff58147294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95219034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4803eb94c2953dcc9b712710b6fea86b3bd3a5e49fbde785e8382ddfa648d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:43:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
ENV CHRONOGRAF_VERSION=1.11.1
# Wed, 22 Apr 2026 01:43:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:43:35 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:43:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:43:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3890b2677d0421ab5024893da8a9b87e11e51d5f038697a769872acc46f8eb7e`  
		Last Modified: Wed, 22 Apr 2026 01:43:50 GMT  
		Size: 7.7 MB (7698505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7f6bc004ebdfde070c98dd879bd60eb2e8b2fbbf8654cc3744687bb91b130e`  
		Last Modified: Wed, 22 Apr 2026 01:43:52 GMT  
		Size: 59.4 MB (59379943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845367a4d5112966d659b3a767e8faeacdf77ea0d336f1ce3fe6f93b073136ee`  
		Last Modified: Wed, 22 Apr 2026 01:43:50 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de84aba6d85fdb6b285d5b67445704e4f6badf59ba839f689b26293863eb6114`  
		Last Modified: Wed, 22 Apr 2026 01:43:50 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba017d4f8fdb0864069f3dec705f13b4f4dc337b21b5fbb084810cebebd8e167`  
		Last Modified: Wed, 22 Apr 2026 01:43:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:c1d1173625df32d5f717779696e450af1183fae65fec15885bbbf79afd74ca5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5cf482b920081a833f634b3740f5afacd4742f2fe22e955ad0d01826ef97d2`

```dockerfile
```

-	Layers:
	-	`sha256:f5caf2dd8813129b9c4c95cdbf9475460c6671d9b69076c9e01ff6fb31a12d18`  
		Last Modified: Wed, 22 Apr 2026 01:43:50 GMT  
		Size: 2.9 MB (2872914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b2522c54541b05c9d9fe6b86bcfddd0e313001f46fd9647c6b93e4f5b2a456e`  
		Last Modified: Wed, 22 Apr 2026 01:43:49 GMT  
		Size: 16.2 KB (16191 bytes)  
		MIME: application/vnd.in-toto+json
