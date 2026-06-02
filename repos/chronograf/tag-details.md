<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.9`](#chronograf1109)
-	[`chronograf:1.10.9-alpine`](#chronograf1109-alpine)
-	[`chronograf:1.11`](#chronograf111)
-	[`chronograf:1.11-alpine`](#chronograf111-alpine)
-	[`chronograf:1.11.3`](#chronograf1113)
-	[`chronograf:1.11.3-alpine`](#chronograf1113-alpine)
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
$ docker pull chronograf@sha256:4212bfe106df50084c6d16d332a0ae1f2fa4afb9bfb70532925204943c712494
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
$ docker pull chronograf@sha256:3589d92826eec8a6de865ab37b92695dd9d37934b3128545bf83d8011a3a9475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85008703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604747b8fa456af2ca3106968c70dddf935f988ae9dc99c289d1cd11efdbb2e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 May 2026 23:23:31 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 19 May 2026 23:23:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 19 May 2026 23:23:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 19 May 2026 23:23:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 19 May 2026 23:23:31 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 19 May 2026 23:23:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 May 2026 23:23:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:23:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:23:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66498cb6d1a3ae9feb8c0aad57ad24ae695279adfbd3a253809b10e917d34eb`  
		Last Modified: Tue, 19 May 2026 23:23:43 GMT  
		Size: 7.9 MB (7882832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95130d01082a5882ce2fe8335539d8e3950c526b8ec6441758d46a8c4737b6ff`  
		Last Modified: Tue, 19 May 2026 23:23:44 GMT  
		Size: 48.9 MB (48867855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf079df6290fb24745fe217ba48acc58ac7988005c2b46cb6976111ab774ed1`  
		Last Modified: Tue, 19 May 2026 23:23:42 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1218cd92899e2f632f0e7043d185af04ee9dcc0c6799e824cb68657e2f2edfb`  
		Last Modified: Tue, 19 May 2026 23:23:42 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8726232d78b1da893f671d669df79e2cf80400e6d0124e222992f168a12895`  
		Last Modified: Tue, 19 May 2026 23:23:44 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:4255b483c688d3a5cb9eaeb2174f98519dd21ac08baee939d11503fa31c478b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36089e2054012c6186c081804c109a63930e1fae63ba060bca1e5e42ae6ef23d`

```dockerfile
```

-	Layers:
	-	`sha256:04b5f9312f723daf90732de4945f91be43bbd6c292e30b3a46f4c427ef9385ee`  
		Last Modified: Tue, 19 May 2026 23:23:43 GMT  
		Size: 2.9 MB (2855442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11893cc52075ca76b00e3f4accfbacbdedb79a9ac36fedc1689e349f22b69d26`  
		Last Modified: Tue, 19 May 2026 23:23:43 GMT  
		Size: 15.8 KB (15779 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d572bad6f25c8b4b2716e657d6571ac19080114cd80d9c999a811d1018b6fd89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76800272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef274ea93a7c75ca3cd904eede68aa1bb4d7d6f5f85344d7eae4137a6da3d8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:06:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:06:12 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 20 May 2026 00:06:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 00:06:12 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 20 May 2026 00:06:12 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 20 May 2026 00:06:12 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 20 May 2026 00:06:12 GMT
VOLUME [/var/lib/chronograf]
# Wed, 20 May 2026 00:06:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:06:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49040f7a58eb3b2b9d394a653fb6defd94862c674a9b16991f001ef2d62665ca`  
		Last Modified: Wed, 20 May 2026 00:06:24 GMT  
		Size: 6.5 MB (6514151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bae880cb0dd3f1cffb9715eaa6d071c131f871b75dd64f95ae32fb173efc578`  
		Last Modified: Wed, 20 May 2026 00:06:25 GMT  
		Size: 46.3 MB (46320011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f417a18c766238d4fae80eb50406bbed212c3ab7e3cb0d24041cf3198ec63845`  
		Last Modified: Wed, 20 May 2026 00:06:23 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94b2978a4d915d53eef7aad8618c1a563aabac65a8c4b617d3d7a1e37bb5618`  
		Last Modified: Wed, 20 May 2026 00:06:23 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ad025808c3e7c27e94f307bf8849e3898e49ff86df84e460e76e2beb5a7ba3`  
		Last Modified: Wed, 20 May 2026 00:06:25 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:f2a58330bcf76071622a64ecc408e780116e37a79b2b016652a555d08f1ba617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2873587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b582b72f2bfe9545615d1604b26d377a6f33d16f495a4252543a754f701518a7`

```dockerfile
```

-	Layers:
	-	`sha256:8b23f716d37303e545491ab56d5e155f369ea3fe44a24bee2c382344919c0f7c`  
		Last Modified: Wed, 20 May 2026 00:06:23 GMT  
		Size: 2.9 MB (2857731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e99ec7dbd7216313957a1ec818bab3b6f3e47f3e00b6f29d78b7331dcca445e9`  
		Last Modified: Wed, 20 May 2026 00:06:23 GMT  
		Size: 15.9 KB (15856 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e507bf128bcedf148cddda021cd81049eddb38018f87cb252bc74c91944349dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81847856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504451837a1f4fd32a6af8809f4dc636fa78a8bab534d3307e7577cf34a2c5c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 May 2026 23:27:13 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 19 May 2026 23:27:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 19 May 2026 23:27:13 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 19 May 2026 23:27:13 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 19 May 2026 23:27:13 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 19 May 2026 23:27:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 May 2026 23:27:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:27:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:27:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79453e0e3f10b3b54e5f917a6a5190e91a70ed58e0ea5e67719b742b199a7d6d`  
		Last Modified: Tue, 19 May 2026 23:27:26 GMT  
		Size: 7.7 MB (7699455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34fe634144a1399cb25010722e6018324b0443aa307c6c0e13e5a64ffa5021d`  
		Last Modified: Tue, 19 May 2026 23:27:27 GMT  
		Size: 46.0 MB (46008883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94864be51423af3562dd29f3081fa36ccf634ec7d4c01511a730365cf04b0108`  
		Last Modified: Tue, 19 May 2026 23:27:25 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624ae7adb4dedc20fd1ca4765cb02e64c751245a96fac0379eaa29e1e4cb0e05`  
		Last Modified: Tue, 19 May 2026 23:27:25 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b318403294f11892a65bb2a78da204df41f27115d4f0f80a8b4d4a9eb7260603`  
		Last Modified: Tue, 19 May 2026 23:27:26 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:15be158243c79c3f3a1f5839d0105167b660f05925cfdb832cd2d512ffe810c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fac263a4f7a59f0be21961d69ee80e3b12e1e58e6700a682d5ef34e9b4aeb5`

```dockerfile
```

-	Layers:
	-	`sha256:bc924b263e906ecd583b04a6d730646fbc0d04ce1ce4461cd564d001419c345f`  
		Last Modified: Tue, 19 May 2026 23:27:25 GMT  
		Size: 2.9 MB (2855703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8ed34f5fb8ac221217679effebfb06373b90e593ba3666dd6c5cd4a65b2d5e8`  
		Last Modified: Tue, 19 May 2026 23:27:25 GMT  
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
$ docker pull chronograf@sha256:4212bfe106df50084c6d16d332a0ae1f2fa4afb9bfb70532925204943c712494
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
$ docker pull chronograf@sha256:3589d92826eec8a6de865ab37b92695dd9d37934b3128545bf83d8011a3a9475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85008703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604747b8fa456af2ca3106968c70dddf935f988ae9dc99c289d1cd11efdbb2e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 May 2026 23:23:31 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 19 May 2026 23:23:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 19 May 2026 23:23:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 19 May 2026 23:23:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 19 May 2026 23:23:31 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 19 May 2026 23:23:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 May 2026 23:23:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:23:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:23:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66498cb6d1a3ae9feb8c0aad57ad24ae695279adfbd3a253809b10e917d34eb`  
		Last Modified: Tue, 19 May 2026 23:23:43 GMT  
		Size: 7.9 MB (7882832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95130d01082a5882ce2fe8335539d8e3950c526b8ec6441758d46a8c4737b6ff`  
		Last Modified: Tue, 19 May 2026 23:23:44 GMT  
		Size: 48.9 MB (48867855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf079df6290fb24745fe217ba48acc58ac7988005c2b46cb6976111ab774ed1`  
		Last Modified: Tue, 19 May 2026 23:23:42 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1218cd92899e2f632f0e7043d185af04ee9dcc0c6799e824cb68657e2f2edfb`  
		Last Modified: Tue, 19 May 2026 23:23:42 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8726232d78b1da893f671d669df79e2cf80400e6d0124e222992f168a12895`  
		Last Modified: Tue, 19 May 2026 23:23:44 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:4255b483c688d3a5cb9eaeb2174f98519dd21ac08baee939d11503fa31c478b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36089e2054012c6186c081804c109a63930e1fae63ba060bca1e5e42ae6ef23d`

```dockerfile
```

-	Layers:
	-	`sha256:04b5f9312f723daf90732de4945f91be43bbd6c292e30b3a46f4c427ef9385ee`  
		Last Modified: Tue, 19 May 2026 23:23:43 GMT  
		Size: 2.9 MB (2855442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11893cc52075ca76b00e3f4accfbacbdedb79a9ac36fedc1689e349f22b69d26`  
		Last Modified: Tue, 19 May 2026 23:23:43 GMT  
		Size: 15.8 KB (15779 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d572bad6f25c8b4b2716e657d6571ac19080114cd80d9c999a811d1018b6fd89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76800272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef274ea93a7c75ca3cd904eede68aa1bb4d7d6f5f85344d7eae4137a6da3d8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:06:06 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:06:12 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Wed, 20 May 2026 00:06:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 00:06:12 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 20 May 2026 00:06:12 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 20 May 2026 00:06:12 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 20 May 2026 00:06:12 GMT
VOLUME [/var/lib/chronograf]
# Wed, 20 May 2026 00:06:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:06:12 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49040f7a58eb3b2b9d394a653fb6defd94862c674a9b16991f001ef2d62665ca`  
		Last Modified: Wed, 20 May 2026 00:06:24 GMT  
		Size: 6.5 MB (6514151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bae880cb0dd3f1cffb9715eaa6d071c131f871b75dd64f95ae32fb173efc578`  
		Last Modified: Wed, 20 May 2026 00:06:25 GMT  
		Size: 46.3 MB (46320011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f417a18c766238d4fae80eb50406bbed212c3ab7e3cb0d24041cf3198ec63845`  
		Last Modified: Wed, 20 May 2026 00:06:23 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94b2978a4d915d53eef7aad8618c1a563aabac65a8c4b617d3d7a1e37bb5618`  
		Last Modified: Wed, 20 May 2026 00:06:23 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ad025808c3e7c27e94f307bf8849e3898e49ff86df84e460e76e2beb5a7ba3`  
		Last Modified: Wed, 20 May 2026 00:06:25 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:f2a58330bcf76071622a64ecc408e780116e37a79b2b016652a555d08f1ba617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2873587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b582b72f2bfe9545615d1604b26d377a6f33d16f495a4252543a754f701518a7`

```dockerfile
```

-	Layers:
	-	`sha256:8b23f716d37303e545491ab56d5e155f369ea3fe44a24bee2c382344919c0f7c`  
		Last Modified: Wed, 20 May 2026 00:06:23 GMT  
		Size: 2.9 MB (2857731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e99ec7dbd7216313957a1ec818bab3b6f3e47f3e00b6f29d78b7331dcca445e9`  
		Last Modified: Wed, 20 May 2026 00:06:23 GMT  
		Size: 15.9 KB (15856 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:e507bf128bcedf148cddda021cd81049eddb38018f87cb252bc74c91944349dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81847856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504451837a1f4fd32a6af8809f4dc636fa78a8bab534d3307e7577cf34a2c5c4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:27:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 May 2026 23:27:13 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 19 May 2026 23:27:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 19 May 2026 23:27:13 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 19 May 2026 23:27:13 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 19 May 2026 23:27:13 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 19 May 2026 23:27:13 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 May 2026 23:27:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:27:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:27:13 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79453e0e3f10b3b54e5f917a6a5190e91a70ed58e0ea5e67719b742b199a7d6d`  
		Last Modified: Tue, 19 May 2026 23:27:26 GMT  
		Size: 7.7 MB (7699455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34fe634144a1399cb25010722e6018324b0443aa307c6c0e13e5a64ffa5021d`  
		Last Modified: Tue, 19 May 2026 23:27:27 GMT  
		Size: 46.0 MB (46008883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94864be51423af3562dd29f3081fa36ccf634ec7d4c01511a730365cf04b0108`  
		Last Modified: Tue, 19 May 2026 23:27:25 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624ae7adb4dedc20fd1ca4765cb02e64c751245a96fac0379eaa29e1e4cb0e05`  
		Last Modified: Tue, 19 May 2026 23:27:25 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b318403294f11892a65bb2a78da204df41f27115d4f0f80a8b4d4a9eb7260603`  
		Last Modified: Tue, 19 May 2026 23:27:26 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:15be158243c79c3f3a1f5839d0105167b660f05925cfdb832cd2d512ffe810c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2871577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fac263a4f7a59f0be21961d69ee80e3b12e1e58e6700a682d5ef34e9b4aeb5`

```dockerfile
```

-	Layers:
	-	`sha256:bc924b263e906ecd583b04a6d730646fbc0d04ce1ce4461cd564d001419c345f`  
		Last Modified: Tue, 19 May 2026 23:27:25 GMT  
		Size: 2.9 MB (2855703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8ed34f5fb8ac221217679effebfb06373b90e593ba3666dd6c5cd4a65b2d5e8`  
		Last Modified: Tue, 19 May 2026 23:27:25 GMT  
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
$ docker pull chronograf@sha256:eb70ca38ed0435787c9ffe469c3ad502d05f221e3c697015b070d69087c9edd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.11` - linux; amd64

```console
$ docker pull chronograf@sha256:5f287d828526a3622cbb0ada9c8cafa02a7dff6751aface86c3fd39474326595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96338084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb4e2824168d6fefce1709e3513a724bbc8f18c102506c7b82a24fac91ba249`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 02 Jun 2026 19:04:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Tue, 02 Jun 2026 19:04:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 02 Jun 2026 19:04:50 GMT
VOLUME [/var/lib/chronograf]
# Tue, 02 Jun 2026 19:04:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc8ae8cd182811c8f1025ccc205da723f8e17214b0182b8576738541b681448`  
		Last Modified: Tue, 02 Jun 2026 19:05:05 GMT  
		Size: 7.9 MB (7882781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913f912f9931a55a6888069207af19b462bf030aa63a495e5266f7efe98ac3f`  
		Last Modified: Tue, 02 Jun 2026 19:05:06 GMT  
		Size: 60.2 MB (60197283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455675abf40c5ac87a7da8c8aaf4b1a46d53d41dad64299e2d42d1035a375721`  
		Last Modified: Tue, 02 Jun 2026 19:05:04 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5205e18c12565276f1a0b9049b861f144429a336825095df5ff2aaa7a2c226`  
		Last Modified: Tue, 02 Jun 2026 19:05:04 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c0b12cf3395c8e678dbf286cb994771b3547e2f2757d93108e967f27b1ecdc`  
		Last Modified: Tue, 02 Jun 2026 19:05:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11` - unknown; unknown

```console
$ docker pull chronograf@sha256:af34f5ab4ae131481d91533abd74f94aa75d7e549f02e2b0a757181585dc64e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c161f28bf70196401d96e82464c8216b69ea8e746e0de247b5fbfef0e5778b`

```dockerfile
```

-	Layers:
	-	`sha256:0877e14103aeb5913a8a7572fe12a697f3043d31d0656e1926307268b90f695c`  
		Last Modified: Tue, 02 Jun 2026 19:05:05 GMT  
		Size: 2.9 MB (2873720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3ed46836e66c33c1fb0da4f7c7cf7ec972deb61a77f97cb98b882ee7dd5d69`  
		Last Modified: Tue, 02 Jun 2026 19:05:04 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.11` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8f60556f88893bb34a9117ad8eb3041bda2d557ede818fbf4e1e9b2c707b7ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93047811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64ae9ca865476dfd34d335223a68573df98b89f5ca2b40ea97b644ff6a7e074`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 02 Jun 2026 19:04:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Tue, 02 Jun 2026 19:04:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 02 Jun 2026 19:04:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 02 Jun 2026 19:04:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe123d17146413325d255a21d4c2f8984fd6e08d3c8460a232b1dfcf8e48566`  
		Last Modified: Tue, 02 Jun 2026 19:05:10 GMT  
		Size: 7.7 MB (7699448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef03fe0fdbc1bb5177bf111c153aafacab7551ce6d1ea2cd0a29379a492fb30`  
		Last Modified: Tue, 02 Jun 2026 19:05:11 GMT  
		Size: 57.2 MB (57208859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587cdfa30ae0c1bcfaa6cc739d142c925859efa2b8c3e7b31b6bd6337a8066da`  
		Last Modified: Tue, 02 Jun 2026 19:05:09 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f02a0b9affa9f7ef18cf4bcab1866d09d0aa22a353ad2e82b7397b2ebcb17f`  
		Last Modified: Tue, 02 Jun 2026 19:05:09 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5914993df547519c55aa65a3a21bff47e93930a0e306ea322e108d3cac587d4e`  
		Last Modified: Tue, 02 Jun 2026 19:05:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11` - unknown; unknown

```console
$ docker pull chronograf@sha256:ae95547b414d7af79db70d299dcfd82664b4fe7e7ea19a8bf248358d7afafc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fa41b0f97732b2535d5863d58f9147ba421671b1962e1642bdf584b15faeab`

```dockerfile
```

-	Layers:
	-	`sha256:8c426d19ed3b0c675a4a4d5da70287cbf62376981b5f5fa11006452e00a63c7f`  
		Last Modified: Tue, 02 Jun 2026 19:05:09 GMT  
		Size: 2.9 MB (2872934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec92e58f6d130d0dbbd936941c699acc570f0eeda6bfe15e0824363ed091ed4`  
		Last Modified: Tue, 02 Jun 2026 19:05:09 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11-alpine`

```console
$ docker pull chronograf@sha256:6a13c94781499351f6019fa26d02dc287e361d973bb5e97e58e0a25bba2579d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.11-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:a9f3b74a26e54cae5a6c7fb7b5e4abf40daa069403992677e6c5dc0753c9bb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62307276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4ba0108a1b6fbb590dc2b7e493f9b3d520846ff0b6a0875264a036e18e7a90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 02 Jun 2026 19:04:41 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Tue, 02 Jun 2026 19:04:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/usr/bin/* &&     cp -a /usr/src/chronograf-*/usr/bin/* /usr/bin &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 02 Jun 2026 19:04:46 GMT
VOLUME [/var/lib/chronograf]
# Tue, 02 Jun 2026 19:04:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287062304c09ba75dc0e215866a324ed37b156260de2f4620bb8f91128ab548e`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f12ca20af43c42fcda6630eb29e46ed6428b3442e1c5a3a7058c666c91f74`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 312.2 KB (312201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae5737a7f7c4257e5f9e07b9d767ac92f8fa0cc21a23e84f3353d9c012a0692`  
		Last Modified: Tue, 02 Jun 2026 19:04:59 GMT  
		Size: 58.2 MB (58162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f1d07db993877635002f6bf86983ac5552cb29152ca78b3ed8dba4b0f74a8d`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf29867af4e0e03fc4f2fe6a37ef5ce2e757d32aeacc686721a470943fde4ec`  
		Last Modified: Tue, 02 Jun 2026 19:04:59 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1777423041239cd1143016601133645e295a3bd49e139f0337486cafa72133`  
		Last Modified: Tue, 02 Jun 2026 19:04:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:08db9de38b0153583acd24af21133c549def40c9dec94d56e28a1b7025bab203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 KB (287078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3e7acde3366a74927292f173102513f05008301d3188d9dc8e16fd66e5a60f`

```dockerfile
```

-	Layers:
	-	`sha256:efd1fcc3b8aed71cbabb698176ad48290ef7f148a172fec85141612648087af0`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 269.3 KB (269314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845aece1bc937a99c1da8fb155a6937175ad801820bf47a5256b3c43596afc12`  
		Last Modified: Tue, 02 Jun 2026 19:04:57 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11.3`

```console
$ docker pull chronograf@sha256:eb70ca38ed0435787c9ffe469c3ad502d05f221e3c697015b070d69087c9edd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.11.3` - linux; amd64

```console
$ docker pull chronograf@sha256:5f287d828526a3622cbb0ada9c8cafa02a7dff6751aface86c3fd39474326595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96338084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb4e2824168d6fefce1709e3513a724bbc8f18c102506c7b82a24fac91ba249`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 02 Jun 2026 19:04:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Tue, 02 Jun 2026 19:04:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 02 Jun 2026 19:04:50 GMT
VOLUME [/var/lib/chronograf]
# Tue, 02 Jun 2026 19:04:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc8ae8cd182811c8f1025ccc205da723f8e17214b0182b8576738541b681448`  
		Last Modified: Tue, 02 Jun 2026 19:05:05 GMT  
		Size: 7.9 MB (7882781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913f912f9931a55a6888069207af19b462bf030aa63a495e5266f7efe98ac3f`  
		Last Modified: Tue, 02 Jun 2026 19:05:06 GMT  
		Size: 60.2 MB (60197283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455675abf40c5ac87a7da8c8aaf4b1a46d53d41dad64299e2d42d1035a375721`  
		Last Modified: Tue, 02 Jun 2026 19:05:04 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5205e18c12565276f1a0b9049b861f144429a336825095df5ff2aaa7a2c226`  
		Last Modified: Tue, 02 Jun 2026 19:05:04 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c0b12cf3395c8e678dbf286cb994771b3547e2f2757d93108e967f27b1ecdc`  
		Last Modified: Tue, 02 Jun 2026 19:05:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11.3` - unknown; unknown

```console
$ docker pull chronograf@sha256:af34f5ab4ae131481d91533abd74f94aa75d7e549f02e2b0a757181585dc64e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c161f28bf70196401d96e82464c8216b69ea8e746e0de247b5fbfef0e5778b`

```dockerfile
```

-	Layers:
	-	`sha256:0877e14103aeb5913a8a7572fe12a697f3043d31d0656e1926307268b90f695c`  
		Last Modified: Tue, 02 Jun 2026 19:05:05 GMT  
		Size: 2.9 MB (2873720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3ed46836e66c33c1fb0da4f7c7cf7ec972deb61a77f97cb98b882ee7dd5d69`  
		Last Modified: Tue, 02 Jun 2026 19:05:04 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.11.3` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8f60556f88893bb34a9117ad8eb3041bda2d557ede818fbf4e1e9b2c707b7ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93047811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64ae9ca865476dfd34d335223a68573df98b89f5ca2b40ea97b644ff6a7e074`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 02 Jun 2026 19:04:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Tue, 02 Jun 2026 19:04:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 02 Jun 2026 19:04:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 02 Jun 2026 19:04:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe123d17146413325d255a21d4c2f8984fd6e08d3c8460a232b1dfcf8e48566`  
		Last Modified: Tue, 02 Jun 2026 19:05:10 GMT  
		Size: 7.7 MB (7699448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef03fe0fdbc1bb5177bf111c153aafacab7551ce6d1ea2cd0a29379a492fb30`  
		Last Modified: Tue, 02 Jun 2026 19:05:11 GMT  
		Size: 57.2 MB (57208859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587cdfa30ae0c1bcfaa6cc739d142c925859efa2b8c3e7b31b6bd6337a8066da`  
		Last Modified: Tue, 02 Jun 2026 19:05:09 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f02a0b9affa9f7ef18cf4bcab1866d09d0aa22a353ad2e82b7397b2ebcb17f`  
		Last Modified: Tue, 02 Jun 2026 19:05:09 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5914993df547519c55aa65a3a21bff47e93930a0e306ea322e108d3cac587d4e`  
		Last Modified: Tue, 02 Jun 2026 19:05:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11.3` - unknown; unknown

```console
$ docker pull chronograf@sha256:ae95547b414d7af79db70d299dcfd82664b4fe7e7ea19a8bf248358d7afafc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fa41b0f97732b2535d5863d58f9147ba421671b1962e1642bdf584b15faeab`

```dockerfile
```

-	Layers:
	-	`sha256:8c426d19ed3b0c675a4a4d5da70287cbf62376981b5f5fa11006452e00a63c7f`  
		Last Modified: Tue, 02 Jun 2026 19:05:09 GMT  
		Size: 2.9 MB (2872934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec92e58f6d130d0dbbd936941c699acc570f0eeda6bfe15e0824363ed091ed4`  
		Last Modified: Tue, 02 Jun 2026 19:05:09 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.11.3-alpine`

```console
$ docker pull chronograf@sha256:6a13c94781499351f6019fa26d02dc287e361d973bb5e97e58e0a25bba2579d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.11.3-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:a9f3b74a26e54cae5a6c7fb7b5e4abf40daa069403992677e6c5dc0753c9bb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62307276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4ba0108a1b6fbb590dc2b7e493f9b3d520846ff0b6a0875264a036e18e7a90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 02 Jun 2026 19:04:41 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Tue, 02 Jun 2026 19:04:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/usr/bin/* &&     cp -a /usr/src/chronograf-*/usr/bin/* /usr/bin &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 02 Jun 2026 19:04:46 GMT
VOLUME [/var/lib/chronograf]
# Tue, 02 Jun 2026 19:04:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287062304c09ba75dc0e215866a324ed37b156260de2f4620bb8f91128ab548e`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f12ca20af43c42fcda6630eb29e46ed6428b3442e1c5a3a7058c666c91f74`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 312.2 KB (312201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae5737a7f7c4257e5f9e07b9d767ac92f8fa0cc21a23e84f3353d9c012a0692`  
		Last Modified: Tue, 02 Jun 2026 19:04:59 GMT  
		Size: 58.2 MB (58162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f1d07db993877635002f6bf86983ac5552cb29152ca78b3ed8dba4b0f74a8d`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf29867af4e0e03fc4f2fe6a37ef5ce2e757d32aeacc686721a470943fde4ec`  
		Last Modified: Tue, 02 Jun 2026 19:04:59 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1777423041239cd1143016601133645e295a3bd49e139f0337486cafa72133`  
		Last Modified: Tue, 02 Jun 2026 19:04:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.11.3-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:08db9de38b0153583acd24af21133c549def40c9dec94d56e28a1b7025bab203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 KB (287078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3e7acde3366a74927292f173102513f05008301d3188d9dc8e16fd66e5a60f`

```dockerfile
```

-	Layers:
	-	`sha256:efd1fcc3b8aed71cbabb698176ad48290ef7f148a172fec85141612648087af0`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 269.3 KB (269314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845aece1bc937a99c1da8fb155a6937175ad801820bf47a5256b3c43596afc12`  
		Last Modified: Tue, 02 Jun 2026 19:04:57 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:fe4d9f2ae3b6a09dc69ea71974475500dd52e79dd881c8662c37f7b01f5f5258
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
$ docker pull chronograf@sha256:3ce14e8e3ef057e8689c7b21a6c9fae9488fea85047bb2eb58601a0e6ba6d213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69888068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f1b296a3d067237fb3f8323a78ce95e532a82796dca991a449a07a5a099ad6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 May 2026 23:23:19 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 19 May 2026 23:23:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 19 May 2026 23:23:19 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 19 May 2026 23:23:19 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 19 May 2026 23:23:19 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 19 May 2026 23:23:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 May 2026 23:23:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:23:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:23:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd47ef9b74d5b9f70bc68a79b0edcf41385564f44e247900320181e997b4f84`  
		Last Modified: Tue, 19 May 2026 23:23:29 GMT  
		Size: 5.2 MB (5241766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d71a82bd9cb298f71881e9dc0155e13c0bdff03a97392675d5f5269e7f8c0fb`  
		Last Modified: Tue, 19 May 2026 23:23:30 GMT  
		Size: 34.4 MB (34364305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff50585cec69c6cb7ce980560fc5e06b2b55f8fabc82b89b19bb38f0d3e2a58a`  
		Last Modified: Tue, 19 May 2026 23:23:28 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ce9a334f1d9d4fae927f2b4f0137e4457ea67a7666e5883347a1254d54734a`  
		Last Modified: Tue, 19 May 2026 23:23:29 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20db34cd8c32f7a152a24a6ce37a679f0ea6dd7e703de6bfa074822539deb67`  
		Last Modified: Tue, 19 May 2026 23:23:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:2fa98b37820ff7f20a5124ff1eb8ab4ea3698843eeeb929ffdf7f5d5a39631e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75be21ade554897078f12b84eb859a0cc0ce845a1c55261cfbde8d163cec37ee`

```dockerfile
```

-	Layers:
	-	`sha256:34e19855353fb80d988498018b45fae45c212d4af3c0c4959b229b5c3a5c6f25`  
		Last Modified: Tue, 19 May 2026 23:23:29 GMT  
		Size: 3.1 MB (3112931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95df131077c2be5b2e91e124f6aa391e6006f9eef7806f4353955c18df15f2d0`  
		Last Modified: Tue, 19 May 2026 23:23:28 GMT  
		Size: 15.8 KB (15773 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:38a1958ed0719d64f2d6147bd16e734fbfc388b177311dacbbe8a701a2d2efc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62620301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02291411102f81214a68b1e2e3d1eb6f3340249eeb87e09057257e9b6c192fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:04:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:04:34 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 20 May 2026 00:04:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 00:04:34 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 20 May 2026 00:04:34 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 20 May 2026 00:04:34 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 20 May 2026 00:04:34 GMT
VOLUME [/var/lib/chronograf]
# Wed, 20 May 2026 00:04:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:04:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:04:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:03d011f22c8996d930f4cd66e165f41f901636aacd59f9f3a74c6b0df7ffa952`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 25.6 MB (25550938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4777cab77fff94a104d92682077343aa60bde9c868783b361395250f0610307d`  
		Last Modified: Wed, 20 May 2026 00:04:43 GMT  
		Size: 4.5 MB (4510016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce8ee99d356e0ac46d0f4e67829c14e5257c6540f1503f4677423b774eb2b02`  
		Last Modified: Wed, 20 May 2026 00:04:44 GMT  
		Size: 32.5 MB (32534951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0023ab81954adfcdb601282ce3a21324874aeddfb0635b92e81907b73a21c730`  
		Last Modified: Wed, 20 May 2026 00:04:43 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b6f7a6817279dc742f9675de4722208a91f3883571ca48ccbf2a713ad2adc1`  
		Last Modified: Wed, 20 May 2026 00:04:43 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ef440aa78a6dfb143383d621079524494448c6b921c92331bd54501eb47dc3`  
		Last Modified: Wed, 20 May 2026 00:04:44 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:8ba4023a53df840bd7f0963525eebc7b8fce5a524d9d6ceff5c23fa1189ab489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db197973a09672f3ae1aed19adafb2887eab8ceb345e92db1d3556dfca368582`

```dockerfile
```

-	Layers:
	-	`sha256:44961c2b532483f5dbc6336feb739de7dcde651642eeee3f86aa640d39ffeabb`  
		Last Modified: Wed, 20 May 2026 00:04:43 GMT  
		Size: 3.1 MB (3115202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d3d303359f4ecc4743c76f117faef685b1e2d55ca632a35c8c8b9feb146243`  
		Last Modified: Wed, 20 May 2026 00:04:43 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:47b48689adb33449bd0dec5b53ad8378bf19edcb6ae052995d6754b20930876a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66426616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2742ee4753ad6a478f9cf8010d2edef31e9468c860af5e093df68fbc5ab8e090`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 May 2026 23:27:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 19 May 2026 23:27:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 19 May 2026 23:27:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 19 May 2026 23:27:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 19 May 2026 23:27:02 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 19 May 2026 23:27:02 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 May 2026 23:27:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:27:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:27:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4b499936aab6f50c71c2cb39731e0abad7efa25e68e1477b44cd080d764d8b`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 5.2 MB (5229760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f5f0ae72a9e9c7b0d9eacb84c03213d17ec9ee0b471cafc3c8db46b4d39cf`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 32.4 MB (32429494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fd552a24a08d202acb77f37e251dfa15050a88a43fd57c4a5b07c5d0bfe092`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c78b9c4a92054282b0b121ed9ab07137e5d415991e03804a257019f831f50b`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ef04445b3b32eb28b7fcf04fc75823dc4b21533a8ec8565bebebf4baf01c31`  
		Last Modified: Tue, 19 May 2026 23:27:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:23445bfb3ecef270c0a4cd481269346e9fb8503ff632f89910a1149e392f3f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5777b5f69cc8718c19d80cd218c075997e9a9bc56d09c6ddd501fec434b3f1d`

```dockerfile
```

-	Layers:
	-	`sha256:df568fbbd9f5ea36eedc98db2fd14bb834ce4327da0b922885341b8765080c19`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 3.1 MB (3113180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4268e90440e046f6e29bb1cf4fd46dbc114f9195bfd71fa254f48de11dd7a033`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 15.9 KB (15869 bytes)  
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
$ docker pull chronograf@sha256:fe4d9f2ae3b6a09dc69ea71974475500dd52e79dd881c8662c37f7b01f5f5258
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
$ docker pull chronograf@sha256:3ce14e8e3ef057e8689c7b21a6c9fae9488fea85047bb2eb58601a0e6ba6d213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69888068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f1b296a3d067237fb3f8323a78ce95e532a82796dca991a449a07a5a099ad6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:23:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 May 2026 23:23:19 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 19 May 2026 23:23:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 19 May 2026 23:23:19 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 19 May 2026 23:23:19 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 19 May 2026 23:23:19 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 19 May 2026 23:23:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 May 2026 23:23:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:23:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:23:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd47ef9b74d5b9f70bc68a79b0edcf41385564f44e247900320181e997b4f84`  
		Last Modified: Tue, 19 May 2026 23:23:29 GMT  
		Size: 5.2 MB (5241766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d71a82bd9cb298f71881e9dc0155e13c0bdff03a97392675d5f5269e7f8c0fb`  
		Last Modified: Tue, 19 May 2026 23:23:30 GMT  
		Size: 34.4 MB (34364305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff50585cec69c6cb7ce980560fc5e06b2b55f8fabc82b89b19bb38f0d3e2a58a`  
		Last Modified: Tue, 19 May 2026 23:23:28 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ce9a334f1d9d4fae927f2b4f0137e4457ea67a7666e5883347a1254d54734a`  
		Last Modified: Tue, 19 May 2026 23:23:29 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20db34cd8c32f7a152a24a6ce37a679f0ea6dd7e703de6bfa074822539deb67`  
		Last Modified: Tue, 19 May 2026 23:23:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:2fa98b37820ff7f20a5124ff1eb8ab4ea3698843eeeb929ffdf7f5d5a39631e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3128704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75be21ade554897078f12b84eb859a0cc0ce845a1c55261cfbde8d163cec37ee`

```dockerfile
```

-	Layers:
	-	`sha256:34e19855353fb80d988498018b45fae45c212d4af3c0c4959b229b5c3a5c6f25`  
		Last Modified: Tue, 19 May 2026 23:23:29 GMT  
		Size: 3.1 MB (3112931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95df131077c2be5b2e91e124f6aa391e6006f9eef7806f4353955c18df15f2d0`  
		Last Modified: Tue, 19 May 2026 23:23:28 GMT  
		Size: 15.8 KB (15773 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:38a1958ed0719d64f2d6147bd16e734fbfc388b177311dacbbe8a701a2d2efc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62620301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02291411102f81214a68b1e2e3d1eb6f3340249eeb87e09057257e9b6c192fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:04:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:04:34 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Wed, 20 May 2026 00:04:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 00:04:34 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 20 May 2026 00:04:34 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 20 May 2026 00:04:34 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 20 May 2026 00:04:34 GMT
VOLUME [/var/lib/chronograf]
# Wed, 20 May 2026 00:04:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:04:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:04:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:03d011f22c8996d930f4cd66e165f41f901636aacd59f9f3a74c6b0df7ffa952`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 25.6 MB (25550938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4777cab77fff94a104d92682077343aa60bde9c868783b361395250f0610307d`  
		Last Modified: Wed, 20 May 2026 00:04:43 GMT  
		Size: 4.5 MB (4510016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce8ee99d356e0ac46d0f4e67829c14e5257c6540f1503f4677423b774eb2b02`  
		Last Modified: Wed, 20 May 2026 00:04:44 GMT  
		Size: 32.5 MB (32534951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0023ab81954adfcdb601282ce3a21324874aeddfb0635b92e81907b73a21c730`  
		Last Modified: Wed, 20 May 2026 00:04:43 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b6f7a6817279dc742f9675de4722208a91f3883571ca48ccbf2a713ad2adc1`  
		Last Modified: Wed, 20 May 2026 00:04:43 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ef440aa78a6dfb143383d621079524494448c6b921c92331bd54501eb47dc3`  
		Last Modified: Wed, 20 May 2026 00:04:44 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:8ba4023a53df840bd7f0963525eebc7b8fce5a524d9d6ceff5c23fa1189ab489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3131053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db197973a09672f3ae1aed19adafb2887eab8ceb345e92db1d3556dfca368582`

```dockerfile
```

-	Layers:
	-	`sha256:44961c2b532483f5dbc6336feb739de7dcde651642eeee3f86aa640d39ffeabb`  
		Last Modified: Wed, 20 May 2026 00:04:43 GMT  
		Size: 3.1 MB (3115202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d3d303359f4ecc4743c76f117faef685b1e2d55ca632a35c8c8b9feb146243`  
		Last Modified: Wed, 20 May 2026 00:04:43 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:47b48689adb33449bd0dec5b53ad8378bf19edcb6ae052995d6754b20930876a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66426616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2742ee4753ad6a478f9cf8010d2edef31e9468c860af5e093df68fbc5ab8e090`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 May 2026 23:27:02 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 19 May 2026 23:27:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 19 May 2026 23:27:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 19 May 2026 23:27:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 19 May 2026 23:27:02 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 19 May 2026 23:27:02 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 May 2026 23:27:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:27:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:27:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4b499936aab6f50c71c2cb39731e0abad7efa25e68e1477b44cd080d764d8b`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 5.2 MB (5229760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f5f0ae72a9e9c7b0d9eacb84c03213d17ec9ee0b471cafc3c8db46b4d39cf`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 32.4 MB (32429494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fd552a24a08d202acb77f37e251dfa15050a88a43fd57c4a5b07c5d0bfe092`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c78b9c4a92054282b0b121ed9ab07137e5d415991e03804a257019f831f50b`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ef04445b3b32eb28b7fcf04fc75823dc4b21533a8ec8565bebebf4baf01c31`  
		Last Modified: Tue, 19 May 2026 23:27:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:23445bfb3ecef270c0a4cd481269346e9fb8503ff632f89910a1149e392f3f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5777b5f69cc8718c19d80cd218c075997e9a9bc56d09c6ddd501fec434b3f1d`

```dockerfile
```

-	Layers:
	-	`sha256:df568fbbd9f5ea36eedc98db2fd14bb834ce4327da0b922885341b8765080c19`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 3.1 MB (3113180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4268e90440e046f6e29bb1cf4fd46dbc114f9195bfd71fa254f48de11dd7a033`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 15.9 KB (15869 bytes)  
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
$ docker pull chronograf@sha256:f1bfd505a98f466902469148348ac1c1e114c0e426a1178e39526b56acea1f38
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
$ docker pull chronograf@sha256:ab7acf4355026f4cf20b5436580e38120a84be51b44890c01e4cf4174b653231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e645d495b8b6025799dd4b602fe2e33e32e3b31a98b7f1ed5eb6fe7493f8d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:23:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 May 2026 23:23:20 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 19 May 2026 23:23:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 19 May 2026 23:23:20 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 19 May 2026 23:23:20 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 19 May 2026 23:23:20 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 19 May 2026 23:23:20 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 May 2026 23:23:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:23:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:23:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f941a58e8026d8c6ae51ab01d411a1bf8a0cda32bcbd0524149dac09b165bc1`  
		Last Modified: Tue, 19 May 2026 23:23:31 GMT  
		Size: 5.2 MB (5241778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d0c3ca85734642435fab97ffaa93a47c191fd272151973115e105946f22c63`  
		Last Modified: Tue, 19 May 2026 23:23:32 GMT  
		Size: 35.0 MB (35011759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e683562c7678968fb71f20e64185b80293bf935f46e39981097d3e8aa2c2763`  
		Last Modified: Tue, 19 May 2026 23:23:31 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ceec946fd6a85c9cdaa4f6f24f05f984617dca6a6b2fb9cb6478952c0618f0`  
		Last Modified: Tue, 19 May 2026 23:23:31 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20db34cd8c32f7a152a24a6ce37a679f0ea6dd7e703de6bfa074822539deb67`  
		Last Modified: Tue, 19 May 2026 23:23:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:2dd688968e0d31d4500fbcd00364a2b49def0069b5af217014ba9f81eb448246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583693476e9f7a0b855aee1e0671dd7eac91224b1094dee7d3e941106ad5e68c`

```dockerfile
```

-	Layers:
	-	`sha256:ede8b31e19bafffcea5ae46391ac29ed162849c729b2db5f1536240dd3142b7c`  
		Last Modified: Tue, 19 May 2026 23:23:31 GMT  
		Size: 3.1 MB (3118141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8048441f464d9bba4ef2c0536e3cd02678e3225abc92f628ef3a499e97f27180`  
		Last Modified: Tue, 19 May 2026 23:23:31 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ae88b0ebf2e35d02ddd7d0ac89e814b6780f0e19a382e5df723f20887a0a4541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63396974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6885387feb42afc2939dd1c5eaeb1c631e503f2193ec2e0e15705bb6f322b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:05:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:05:42 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 20 May 2026 00:05:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 00:05:42 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 20 May 2026 00:05:42 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 20 May 2026 00:05:42 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 20 May 2026 00:05:42 GMT
VOLUME [/var/lib/chronograf]
# Wed, 20 May 2026 00:05:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:05:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:05:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:03d011f22c8996d930f4cd66e165f41f901636aacd59f9f3a74c6b0df7ffa952`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 25.6 MB (25550938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b8a8fe6903e1062e8dffc81471bff58f1b0657a5f9eaf11beab9d3143e32ae`  
		Last Modified: Wed, 20 May 2026 00:05:52 GMT  
		Size: 4.5 MB (4510027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdadcc47ec7331886582069b303bdbdaa43c27e286aaf962abdc56cd230e0ad`  
		Last Modified: Wed, 20 May 2026 00:05:53 GMT  
		Size: 33.3 MB (33311609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b638b1431acda3c3083701107491ac33a25bddc5b9c64bde59b0ed8be3b3fe`  
		Last Modified: Wed, 20 May 2026 00:05:51 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc300e732b16380c456f1a67059f60aceba2c0ad083ef86d240122dc3303b5c0`  
		Last Modified: Wed, 20 May 2026 00:05:51 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8a0b42db29b31479500d0f752e68009ddc7592939a9ba319eb8e25ccedee05`  
		Last Modified: Wed, 20 May 2026 00:05:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:2f0d91d21411d981b0d926f9a60d9cebbd9626febf5ff64b62914b77b78b417a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325fc5d4f53e5fe86b2fd76476303614c42e87d5e0c6a117d19bd8e3b848f86f`

```dockerfile
```

-	Layers:
	-	`sha256:a5698c48bd2434414dd5c0035b3107223aef7a54fdb693c6fa891d148821fac1`  
		Last Modified: Wed, 20 May 2026 00:05:52 GMT  
		Size: 3.1 MB (3120412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45db9dbc8a5c37a2bbe513defcafb12835a89b1526f52b0d1387132714d43e7`  
		Last Modified: Wed, 20 May 2026 00:05:51 GMT  
		Size: 15.8 KB (15843 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:783f97ee14f1f46bef43813e7ded9c1c542814ff739dcfff7fdf9ba54835899a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67179617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac70d616e2964b2f938fd9479ec5753ea8c94d5881422c3a100aff0ba6473342`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 May 2026 23:27:03 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 19 May 2026 23:27:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 19 May 2026 23:27:03 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 19 May 2026 23:27:03 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 19 May 2026 23:27:03 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 19 May 2026 23:27:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 May 2026 23:27:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:27:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f934f8ede6798258d1784f19bd95453fa0428c4b7a845bbfd0e636726e2593`  
		Last Modified: Tue, 19 May 2026 23:27:13 GMT  
		Size: 5.2 MB (5229809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b07919869a9fc727360a9742fc744f18ec2f7aad4234a0a934a337759d3927`  
		Last Modified: Tue, 19 May 2026 23:27:14 GMT  
		Size: 33.2 MB (33182446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c9fb9315de50ebf4ad8233de31c2c3ac25a61fb3d34f90579b342d3cd1adeb`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa972b5d5d0f0359603f7c0637b6d0fe9dc5b185ce2ade891285caad07790a3a`  
		Last Modified: Tue, 19 May 2026 23:27:13 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9263cf0792581e37e12e557cf86a9a412aadde702900aab1747d230492d7b84`  
		Last Modified: Tue, 19 May 2026 23:27:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:c6f82cdaa299a8296cf09bc548c7a907dbd6c18bd8d393210b4ce4f7e705c93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15688edef07d1c2562ea49351b20a4f7ce59e70fca767a7aa05562ec17a838d9`

```dockerfile
```

-	Layers:
	-	`sha256:0d2693a5748b29e28dd8b0fd1d596aa34761f807a36f70d00d63e73aa437c440`  
		Last Modified: Tue, 19 May 2026 23:27:13 GMT  
		Size: 3.1 MB (3118390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aae9218184d292f4927bb6447c6ada34fee2736e295ef8c33a00c7cfbcfdb391`  
		Last Modified: Tue, 19 May 2026 23:27:13 GMT  
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
$ docker pull chronograf@sha256:f1bfd505a98f466902469148348ac1c1e114c0e426a1178e39526b56acea1f38
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
$ docker pull chronograf@sha256:ab7acf4355026f4cf20b5436580e38120a84be51b44890c01e4cf4174b653231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e645d495b8b6025799dd4b602fe2e33e32e3b31a98b7f1ed5eb6fe7493f8d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:23:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 May 2026 23:23:20 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 19 May 2026 23:23:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 19 May 2026 23:23:20 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 19 May 2026 23:23:20 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 19 May 2026 23:23:20 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 19 May 2026 23:23:20 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 May 2026 23:23:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:23:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:23:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f941a58e8026d8c6ae51ab01d411a1bf8a0cda32bcbd0524149dac09b165bc1`  
		Last Modified: Tue, 19 May 2026 23:23:31 GMT  
		Size: 5.2 MB (5241778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d0c3ca85734642435fab97ffaa93a47c191fd272151973115e105946f22c63`  
		Last Modified: Tue, 19 May 2026 23:23:32 GMT  
		Size: 35.0 MB (35011759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e683562c7678968fb71f20e64185b80293bf935f46e39981097d3e8aa2c2763`  
		Last Modified: Tue, 19 May 2026 23:23:31 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ceec946fd6a85c9cdaa4f6f24f05f984617dca6a6b2fb9cb6478952c0618f0`  
		Last Modified: Tue, 19 May 2026 23:23:31 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20db34cd8c32f7a152a24a6ce37a679f0ea6dd7e703de6bfa074822539deb67`  
		Last Modified: Tue, 19 May 2026 23:23:30 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:2dd688968e0d31d4500fbcd00364a2b49def0069b5af217014ba9f81eb448246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583693476e9f7a0b855aee1e0671dd7eac91224b1094dee7d3e941106ad5e68c`

```dockerfile
```

-	Layers:
	-	`sha256:ede8b31e19bafffcea5ae46391ac29ed162849c729b2db5f1536240dd3142b7c`  
		Last Modified: Tue, 19 May 2026 23:23:31 GMT  
		Size: 3.1 MB (3118141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8048441f464d9bba4ef2c0536e3cd02678e3225abc92f628ef3a499e97f27180`  
		Last Modified: Tue, 19 May 2026 23:23:31 GMT  
		Size: 15.8 KB (15767 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ae88b0ebf2e35d02ddd7d0ac89e814b6780f0e19a382e5df723f20887a0a4541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63396974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e6885387feb42afc2939dd1c5eaeb1c631e503f2193ec2e0e15705bb6f322b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:05:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:05:42 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Wed, 20 May 2026 00:05:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 20 May 2026 00:05:42 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 20 May 2026 00:05:42 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 20 May 2026 00:05:42 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 20 May 2026 00:05:42 GMT
VOLUME [/var/lib/chronograf]
# Wed, 20 May 2026 00:05:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:05:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:05:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:03d011f22c8996d930f4cd66e165f41f901636aacd59f9f3a74c6b0df7ffa952`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 25.6 MB (25550938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b8a8fe6903e1062e8dffc81471bff58f1b0657a5f9eaf11beab9d3143e32ae`  
		Last Modified: Wed, 20 May 2026 00:05:52 GMT  
		Size: 4.5 MB (4510027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdadcc47ec7331886582069b303bdbdaa43c27e286aaf962abdc56cd230e0ad`  
		Last Modified: Wed, 20 May 2026 00:05:53 GMT  
		Size: 33.3 MB (33311609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b638b1431acda3c3083701107491ac33a25bddc5b9c64bde59b0ed8be3b3fe`  
		Last Modified: Wed, 20 May 2026 00:05:51 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc300e732b16380c456f1a67059f60aceba2c0ad083ef86d240122dc3303b5c0`  
		Last Modified: Wed, 20 May 2026 00:05:51 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8a0b42db29b31479500d0f752e68009ddc7592939a9ba319eb8e25ccedee05`  
		Last Modified: Wed, 20 May 2026 00:05:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:2f0d91d21411d981b0d926f9a60d9cebbd9626febf5ff64b62914b77b78b417a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325fc5d4f53e5fe86b2fd76476303614c42e87d5e0c6a117d19bd8e3b848f86f`

```dockerfile
```

-	Layers:
	-	`sha256:a5698c48bd2434414dd5c0035b3107223aef7a54fdb693c6fa891d148821fac1`  
		Last Modified: Wed, 20 May 2026 00:05:52 GMT  
		Size: 3.1 MB (3120412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45db9dbc8a5c37a2bbe513defcafb12835a89b1526f52b0d1387132714d43e7`  
		Last Modified: Wed, 20 May 2026 00:05:51 GMT  
		Size: 15.8 KB (15843 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:783f97ee14f1f46bef43813e7ded9c1c542814ff739dcfff7fdf9ba54835899a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67179617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac70d616e2964b2f938fd9479ec5753ea8c94d5881422c3a100aff0ba6473342`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 19 May 2026 23:27:03 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 19 May 2026 23:27:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 19 May 2026 23:27:03 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 19 May 2026 23:27:03 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 19 May 2026 23:27:03 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 19 May 2026 23:27:03 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 May 2026 23:27:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:27:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f934f8ede6798258d1784f19bd95453fa0428c4b7a845bbfd0e636726e2593`  
		Last Modified: Tue, 19 May 2026 23:27:13 GMT  
		Size: 5.2 MB (5229809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b07919869a9fc727360a9742fc744f18ec2f7aad4234a0a934a337759d3927`  
		Last Modified: Tue, 19 May 2026 23:27:14 GMT  
		Size: 33.2 MB (33182446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c9fb9315de50ebf4ad8233de31c2c3ac25a61fb3d34f90579b342d3cd1adeb`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa972b5d5d0f0359603f7c0637b6d0fe9dc5b185ce2ade891285caad07790a3a`  
		Last Modified: Tue, 19 May 2026 23:27:13 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9263cf0792581e37e12e557cf86a9a412aadde702900aab1747d230492d7b84`  
		Last Modified: Tue, 19 May 2026 23:27:14 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:c6f82cdaa299a8296cf09bc548c7a907dbd6c18bd8d393210b4ce4f7e705c93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3134252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15688edef07d1c2562ea49351b20a4f7ce59e70fca767a7aa05562ec17a838d9`

```dockerfile
```

-	Layers:
	-	`sha256:0d2693a5748b29e28dd8b0fd1d596aa34761f807a36f70d00d63e73aa437c440`  
		Last Modified: Tue, 19 May 2026 23:27:13 GMT  
		Size: 3.1 MB (3118390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aae9218184d292f4927bb6447c6ada34fee2736e295ef8c33a00c7cfbcfdb391`  
		Last Modified: Tue, 19 May 2026 23:27:13 GMT  
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
$ docker pull chronograf@sha256:6a13c94781499351f6019fa26d02dc287e361d973bb5e97e58e0a25bba2579d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:a9f3b74a26e54cae5a6c7fb7b5e4abf40daa069403992677e6c5dc0753c9bb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62307276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4ba0108a1b6fbb590dc2b7e493f9b3d520846ff0b6a0875264a036e18e7a90`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 19:04:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 02 Jun 2026 19:04:41 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Tue, 02 Jun 2026 19:04:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/usr/bin/* &&     cp -a /usr/src/chronograf-*/usr/bin/* /usr/bin &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 02 Jun 2026 19:04:46 GMT
VOLUME [/var/lib/chronograf]
# Tue, 02 Jun 2026 19:04:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 19:04:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287062304c09ba75dc0e215866a324ed37b156260de2f4620bb8f91128ab548e`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f12ca20af43c42fcda6630eb29e46ed6428b3442e1c5a3a7058c666c91f74`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 312.2 KB (312201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae5737a7f7c4257e5f9e07b9d767ac92f8fa0cc21a23e84f3353d9c012a0692`  
		Last Modified: Tue, 02 Jun 2026 19:04:59 GMT  
		Size: 58.2 MB (58162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f1d07db993877635002f6bf86983ac5552cb29152ca78b3ed8dba4b0f74a8d`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 12.2 KB (12239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf29867af4e0e03fc4f2fe6a37ef5ce2e757d32aeacc686721a470943fde4ec`  
		Last Modified: Tue, 02 Jun 2026 19:04:59 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1777423041239cd1143016601133645e295a3bd49e139f0337486cafa72133`  
		Last Modified: Tue, 02 Jun 2026 19:04:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:08db9de38b0153583acd24af21133c549def40c9dec94d56e28a1b7025bab203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 KB (287078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3e7acde3366a74927292f173102513f05008301d3188d9dc8e16fd66e5a60f`

```dockerfile
```

-	Layers:
	-	`sha256:efd1fcc3b8aed71cbabb698176ad48290ef7f148a172fec85141612648087af0`  
		Last Modified: Tue, 02 Jun 2026 19:04:58 GMT  
		Size: 269.3 KB (269314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845aece1bc937a99c1da8fb155a6937175ad801820bf47a5256b3c43596afc12`  
		Last Modified: Tue, 02 Jun 2026 19:04:57 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:d40aa30936e76a9d77532e9a00382b998eb937370fbe440c274ed20fe158d9aa
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
$ docker pull chronograf@sha256:5f287d828526a3622cbb0ada9c8cafa02a7dff6751aface86c3fd39474326595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96338084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb4e2824168d6fefce1709e3513a724bbc8f18c102506c7b82a24fac91ba249`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 02 Jun 2026 19:04:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Tue, 02 Jun 2026 19:04:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 02 Jun 2026 19:04:50 GMT
VOLUME [/var/lib/chronograf]
# Tue, 02 Jun 2026 19:04:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 19:04:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc8ae8cd182811c8f1025ccc205da723f8e17214b0182b8576738541b681448`  
		Last Modified: Tue, 02 Jun 2026 19:05:05 GMT  
		Size: 7.9 MB (7882781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913f912f9931a55a6888069207af19b462bf030aa63a495e5266f7efe98ac3f`  
		Last Modified: Tue, 02 Jun 2026 19:05:06 GMT  
		Size: 60.2 MB (60197283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455675abf40c5ac87a7da8c8aaf4b1a46d53d41dad64299e2d42d1035a375721`  
		Last Modified: Tue, 02 Jun 2026 19:05:04 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5205e18c12565276f1a0b9049b861f144429a336825095df5ff2aaa7a2c226`  
		Last Modified: Tue, 02 Jun 2026 19:05:04 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c0b12cf3395c8e678dbf286cb994771b3547e2f2757d93108e967f27b1ecdc`  
		Last Modified: Tue, 02 Jun 2026 19:05:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:af34f5ab4ae131481d91533abd74f94aa75d7e549f02e2b0a757181585dc64e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c161f28bf70196401d96e82464c8216b69ea8e746e0de247b5fbfef0e5778b`

```dockerfile
```

-	Layers:
	-	`sha256:0877e14103aeb5913a8a7572fe12a697f3043d31d0656e1926307268b90f695c`  
		Last Modified: Tue, 02 Jun 2026 19:05:05 GMT  
		Size: 2.9 MB (2873720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3ed46836e66c33c1fb0da4f7c7cf7ec972deb61a77f97cb98b882ee7dd5d69`  
		Last Modified: Tue, 02 Jun 2026 19:05:04 GMT  
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
$ docker pull chronograf@sha256:8f60556f88893bb34a9117ad8eb3041bda2d557ede818fbf4e1e9b2c707b7ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93047811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64ae9ca865476dfd34d335223a68573df98b89f5ca2b40ea97b644ff6a7e074`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 02 Jun 2026 19:04:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Tue, 02 Jun 2026 19:04:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 02 Jun 2026 19:04:55 GMT
VOLUME [/var/lib/chronograf]
# Tue, 02 Jun 2026 19:04:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 02 Jun 2026 19:04:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 19:04:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe123d17146413325d255a21d4c2f8984fd6e08d3c8460a232b1dfcf8e48566`  
		Last Modified: Tue, 02 Jun 2026 19:05:10 GMT  
		Size: 7.7 MB (7699448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef03fe0fdbc1bb5177bf111c153aafacab7551ce6d1ea2cd0a29379a492fb30`  
		Last Modified: Tue, 02 Jun 2026 19:05:11 GMT  
		Size: 57.2 MB (57208859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587cdfa30ae0c1bcfaa6cc739d142c925859efa2b8c3e7b31b6bd6337a8066da`  
		Last Modified: Tue, 02 Jun 2026 19:05:09 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f02a0b9affa9f7ef18cf4bcab1866d09d0aa22a353ad2e82b7397b2ebcb17f`  
		Last Modified: Tue, 02 Jun 2026 19:05:09 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5914993df547519c55aa65a3a21bff47e93930a0e306ea322e108d3cac587d4e`  
		Last Modified: Tue, 02 Jun 2026 19:05:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:ae95547b414d7af79db70d299dcfd82664b4fe7e7ea19a8bf248358d7afafc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fa41b0f97732b2535d5863d58f9147ba421671b1962e1642bdf584b15faeab`

```dockerfile
```

-	Layers:
	-	`sha256:8c426d19ed3b0c675a4a4d5da70287cbf62376981b5f5fa11006452e00a63c7f`  
		Last Modified: Tue, 02 Jun 2026 19:05:09 GMT  
		Size: 2.9 MB (2872934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec92e58f6d130d0dbbd936941c699acc570f0eeda6bfe15e0824363ed091ed4`  
		Last Modified: Tue, 02 Jun 2026 19:05:09 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json
