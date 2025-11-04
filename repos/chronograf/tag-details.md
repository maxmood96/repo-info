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
$ docker pull chronograf@sha256:8952c2a46185337082b6d88ee50ce168a6a7a183a7c6ecdc916d124dd705567f
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
$ docker pull chronograf@sha256:3e15fa77498d4b818b90a5994800e69f96529443ffed92a8f7c2cb4b4dd59200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3ce7300403c65c4b1e86422daebb73997c5c296c52251b72af6e32d992f469`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 04 Nov 2025 00:28:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:28:41 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:28:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed73089ebb3295175b105a893325db8b1f74db21ed868ff7e0fa080fae5b82c3`  
		Last Modified: Tue, 04 Nov 2025 00:28:59 GMT  
		Size: 7.9 MB (7878726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54c4f5cf93b1af5a7738b010f1a6a387946e1899973195b3f9760d455c13683`  
		Last Modified: Tue, 04 Nov 2025 00:29:04 GMT  
		Size: 49.3 MB (49276586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33928fff17d35ab8b07bb2938c602b5b243e900e2803cdba382e49bd9dec3e2`  
		Last Modified: Tue, 04 Nov 2025 00:28:59 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0e94b53f4943e061ca85cce8309b535f35f192db64ae3d8cf4b9fc884629c3`  
		Last Modified: Tue, 04 Nov 2025 00:28:59 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa8b959a19273bcc5d337452af8736eabbb36810d62038b88625bc2ae39b5ff`  
		Last Modified: Tue, 04 Nov 2025 00:28:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:3b7a84e83406126586039673c4c2c19ce0b5a7b31811fcf9a4be078ed0c9d6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59599068fca04d4ef9255a25af2a9e2d59d40d310ba4ecd628827090402786a`

```dockerfile
```

-	Layers:
	-	`sha256:279d5adbc3510522d190cf3b9440a094990afb38f8c30b9754fc0f7bed35d33e`  
		Last Modified: Tue, 04 Nov 2025 10:38:27 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42d216008927e758e45450bde8d106e54acf3244feb021dfe1a3154dcbab9aba`  
		Last Modified: Tue, 04 Nov 2025 10:38:27 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d1ca2a60d34c0e3fb74aa85c14f8538a09d87cb9910644649f52270922fe6275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d1c8795fbaca4ddd76b57a435bdda497671dc838643469701cd199bb1045fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:41:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 04 Nov 2025 00:41:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:41:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:41:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:41:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea58372cbc1e2233482831a509b9a309c4183ac0bd32fca8b29224745a3b4a38`  
		Last Modified: Tue, 04 Nov 2025 00:41:29 GMT  
		Size: 6.5 MB (6508150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01d64c10b637f7f78e240bf5c26f6195a21885625c5413dbb27ee82807875ea`  
		Last Modified: Tue, 04 Nov 2025 00:41:35 GMT  
		Size: 45.6 MB (45621823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea7e911dc89a8ef5464737bf0d16d1d17d52006a69bb2df4b8d8a1654acac1f`  
		Last Modified: Tue, 04 Nov 2025 00:41:28 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742fd2d1edb94445b05649b50e9327a910ece29230a020981b51d5e9445968c6`  
		Last Modified: Tue, 04 Nov 2025 00:41:28 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d929c27d5213b702e7e8c679440d000c068d6d85566011c7d6469680a1f6dbc5`  
		Last Modified: Tue, 04 Nov 2025 00:41:28 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:f5c4c6747fffadf6ec6e8fceb39f5fac9ab178ad3fe02c06aa319917353e4ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67c163c09c73fc886bebfd4b3b0592e57073cebabb316497c31a94401ae2543`

```dockerfile
```

-	Layers:
	-	`sha256:9b1bbb5579dda3559a9ac105d6f53642f89f68d498ee4f6f9248cd6146031266`  
		Last Modified: Tue, 04 Nov 2025 10:38:31 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52d2e71775c655e2048ade8e325ef7ea260038230e7914ca079785bee9d2985f`  
		Last Modified: Tue, 04 Nov 2025 10:38:32 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:40791fbfbab907848dcddc3d42f76951b86d7373531e57c6222a38133fbe8c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c29a15584be0079e5c539feddbfa2ec71d1c2eccafdc75dac480715eaf252fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 04 Nov 2025 00:30:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:30:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:30:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:30:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41428d9a237511f0a4e48bd146ce6ed1087542a1518962e37a2c4e4cbe3a87fb`  
		Last Modified: Tue, 04 Nov 2025 00:30:56 GMT  
		Size: 7.7 MB (7691888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98d94554815c13464c2ba8ba9d816f241b8445c2b7b0e7bbd271ed5aabc6f9f`  
		Last Modified: Tue, 04 Nov 2025 00:31:03 GMT  
		Size: 47.1 MB (47066760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adfc1cee5921690552291343756ebe367c85ba43eaa585fcf648e87a4ba80b1`  
		Last Modified: Tue, 04 Nov 2025 00:30:56 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2108f3d0938214ddda0f9f88b3d198ac68519ee14ac34c0182a9aa7367f7ed8c`  
		Last Modified: Tue, 04 Nov 2025 00:30:57 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d31b7618f2b06e266e622f1c654257c5c58b9060d1adffe85cceb7bab55bc1`  
		Last Modified: Tue, 04 Nov 2025 00:30:57 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:02354048681fba16160db315177123e01ac67a67b8bd095f1ee1e4837d8e58cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c04f60cc35a41ef691114472792c84caa3fe9b4cb188e54543bb87874322f73`

```dockerfile
```

-	Layers:
	-	`sha256:7a9a41af9332653c56373fb96883cad8706ba896080437020a5c17fdc60b6c1c`  
		Last Modified: Tue, 04 Nov 2025 10:38:35 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd7c3793902f9b0d3eb23d8d6e2cb4fb5949362275d3697e280d4ae4a4de627`  
		Last Modified: Tue, 04 Nov 2025 10:38:36 GMT  
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
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
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
		Last Modified: Thu, 09 Oct 2025 00:38:17 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Thu, 09 Oct 2025 00:38:18 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.8`

```console
$ docker pull chronograf@sha256:8952c2a46185337082b6d88ee50ce168a6a7a183a7c6ecdc916d124dd705567f
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
$ docker pull chronograf@sha256:3e15fa77498d4b818b90a5994800e69f96529443ffed92a8f7c2cb4b4dd59200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3ce7300403c65c4b1e86422daebb73997c5c296c52251b72af6e32d992f469`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 04 Nov 2025 00:28:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:28:41 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:28:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed73089ebb3295175b105a893325db8b1f74db21ed868ff7e0fa080fae5b82c3`  
		Last Modified: Tue, 04 Nov 2025 00:28:59 GMT  
		Size: 7.9 MB (7878726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54c4f5cf93b1af5a7738b010f1a6a387946e1899973195b3f9760d455c13683`  
		Last Modified: Tue, 04 Nov 2025 00:29:04 GMT  
		Size: 49.3 MB (49276586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33928fff17d35ab8b07bb2938c602b5b243e900e2803cdba382e49bd9dec3e2`  
		Last Modified: Tue, 04 Nov 2025 00:28:59 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0e94b53f4943e061ca85cce8309b535f35f192db64ae3d8cf4b9fc884629c3`  
		Last Modified: Tue, 04 Nov 2025 00:28:59 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa8b959a19273bcc5d337452af8736eabbb36810d62038b88625bc2ae39b5ff`  
		Last Modified: Tue, 04 Nov 2025 00:28:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:3b7a84e83406126586039673c4c2c19ce0b5a7b31811fcf9a4be078ed0c9d6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59599068fca04d4ef9255a25af2a9e2d59d40d310ba4ecd628827090402786a`

```dockerfile
```

-	Layers:
	-	`sha256:279d5adbc3510522d190cf3b9440a094990afb38f8c30b9754fc0f7bed35d33e`  
		Last Modified: Tue, 04 Nov 2025 10:38:27 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42d216008927e758e45450bde8d106e54acf3244feb021dfe1a3154dcbab9aba`  
		Last Modified: Tue, 04 Nov 2025 10:38:27 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d1ca2a60d34c0e3fb74aa85c14f8538a09d87cb9910644649f52270922fe6275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d1c8795fbaca4ddd76b57a435bdda497671dc838643469701cd199bb1045fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:41:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 04 Nov 2025 00:41:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:41:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:41:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:41:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea58372cbc1e2233482831a509b9a309c4183ac0bd32fca8b29224745a3b4a38`  
		Last Modified: Tue, 04 Nov 2025 00:41:29 GMT  
		Size: 6.5 MB (6508150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01d64c10b637f7f78e240bf5c26f6195a21885625c5413dbb27ee82807875ea`  
		Last Modified: Tue, 04 Nov 2025 00:41:35 GMT  
		Size: 45.6 MB (45621823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea7e911dc89a8ef5464737bf0d16d1d17d52006a69bb2df4b8d8a1654acac1f`  
		Last Modified: Tue, 04 Nov 2025 00:41:28 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742fd2d1edb94445b05649b50e9327a910ece29230a020981b51d5e9445968c6`  
		Last Modified: Tue, 04 Nov 2025 00:41:28 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d929c27d5213b702e7e8c679440d000c068d6d85566011c7d6469680a1f6dbc5`  
		Last Modified: Tue, 04 Nov 2025 00:41:28 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:f5c4c6747fffadf6ec6e8fceb39f5fac9ab178ad3fe02c06aa319917353e4ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67c163c09c73fc886bebfd4b3b0592e57073cebabb316497c31a94401ae2543`

```dockerfile
```

-	Layers:
	-	`sha256:9b1bbb5579dda3559a9ac105d6f53642f89f68d498ee4f6f9248cd6146031266`  
		Last Modified: Tue, 04 Nov 2025 10:38:31 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52d2e71775c655e2048ade8e325ef7ea260038230e7914ca079785bee9d2985f`  
		Last Modified: Tue, 04 Nov 2025 10:38:32 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:40791fbfbab907848dcddc3d42f76951b86d7373531e57c6222a38133fbe8c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c29a15584be0079e5c539feddbfa2ec71d1c2eccafdc75dac480715eaf252fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 04 Nov 2025 00:30:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:30:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:30:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:30:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41428d9a237511f0a4e48bd146ce6ed1087542a1518962e37a2c4e4cbe3a87fb`  
		Last Modified: Tue, 04 Nov 2025 00:30:56 GMT  
		Size: 7.7 MB (7691888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98d94554815c13464c2ba8ba9d816f241b8445c2b7b0e7bbd271ed5aabc6f9f`  
		Last Modified: Tue, 04 Nov 2025 00:31:03 GMT  
		Size: 47.1 MB (47066760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adfc1cee5921690552291343756ebe367c85ba43eaa585fcf648e87a4ba80b1`  
		Last Modified: Tue, 04 Nov 2025 00:30:56 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2108f3d0938214ddda0f9f88b3d198ac68519ee14ac34c0182a9aa7367f7ed8c`  
		Last Modified: Tue, 04 Nov 2025 00:30:57 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d31b7618f2b06e266e622f1c654257c5c58b9060d1adffe85cceb7bab55bc1`  
		Last Modified: Tue, 04 Nov 2025 00:30:57 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:02354048681fba16160db315177123e01ac67a67b8bd095f1ee1e4837d8e58cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c04f60cc35a41ef691114472792c84caa3fe9b4cb188e54543bb87874322f73`

```dockerfile
```

-	Layers:
	-	`sha256:7a9a41af9332653c56373fb96883cad8706ba896080437020a5c17fdc60b6c1c`  
		Last Modified: Tue, 04 Nov 2025 10:38:35 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd7c3793902f9b0d3eb23d8d6e2cb4fb5949362275d3697e280d4ae4a4de627`  
		Last Modified: Tue, 04 Nov 2025 10:38:36 GMT  
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
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
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
		Last Modified: Thu, 09 Oct 2025 00:38:17 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Thu, 09 Oct 2025 00:38:18 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:7b7edaeff058f5318a9efe258125df7ae2aedeb6b25b63558c99d9f88a1e0928
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
$ docker pull chronograf@sha256:79e0e9b2091ec19547f00102866f8d9cacbabedd4235cc760908c0de600e0fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c9bedad71af104b14727de1ba14af627adea4afc721fd8b1cede8cc7f044bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:28:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:28:19 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Nov 2025 00:28:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:28:19 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:28:19 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:28:19 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:28:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:28:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:28:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c172387ca69fbc10fde5f55f0010ba7888e5daa170cb1b2700117c755a683b7c`  
		Last Modified: Tue, 04 Nov 2025 00:28:35 GMT  
		Size: 4.2 MB (4209371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cfcfe3a8a5afab1bcb06df17b629564e444db5d38e3a1a3857ad413d5d53cd`  
		Last Modified: Tue, 04 Nov 2025 00:28:37 GMT  
		Size: 34.7 MB (34738628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75f9565e1e68f36342c3fae7b81481385c50b5f3bbd160f0399ec13d6682cd5`  
		Last Modified: Tue, 04 Nov 2025 00:28:35 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b56394cf836ceb1a1d9d06ed1b2831e9b0f3139c140d2f21a95c907b54c1040`  
		Last Modified: Tue, 04 Nov 2025 00:28:35 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7514ca2ca63742957942fca58b9f761ac8f5472f8c91a65b529d392fc299282`  
		Last Modified: Tue, 04 Nov 2025 00:28:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:54fa1828ec43685539cbedaed235906180c0f4966c174c271a467f788ab1a0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c830988a651765173eebe92a797a4586a3486184820bc4ae0af6f4c22bbf63`

```dockerfile
```

-	Layers:
	-	`sha256:8e90faa645b4eedcb2f38e5f89e8be29fa31726fad4e79bb62ed492e375e27d1`  
		Last Modified: Tue, 04 Nov 2025 10:38:39 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa8a94a11b5215372fdff516165e2dd2aa8cafcc4aa419a0f1065aa8f425b87`  
		Last Modified: Tue, 04 Nov 2025 10:38:40 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:9d406b0662ef3799bb5b27ccbbcc9889daae0585a570e638c6734b4c353506df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7361929bc4bc9a8239dc378d3f1b5f4faf0d940d8247a6504aebeb25d3b82d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:39:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:40:06 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Nov 2025 00:40:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:40:06 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:40:06 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:40:06 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:40:06 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:40:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:40:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:40:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5add2125bf9631befcab62d5e04ad41781bbc4aa838aed7e164e81e0929dd346`  
		Last Modified: Tue, 04 Nov 2025 00:13:15 GMT  
		Size: 25.5 MB (25546326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a70cdbe3d26c97224e20ddc0f06d2b85e854daf47c193948d0e157c3799d1bf`  
		Last Modified: Tue, 04 Nov 2025 00:40:27 GMT  
		Size: 3.5 MB (3511634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae062a58c16c9f5e129f590025e26b573ed52ed7aa85a9540df7b8b355fa128`  
		Last Modified: Tue, 04 Nov 2025 00:40:30 GMT  
		Size: 33.1 MB (33097570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46447b25e982172f37f258a8b75a36baf60265d9968fdd136745add23f3f00c5`  
		Last Modified: Tue, 04 Nov 2025 00:40:26 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad24fd3933e97dcdcefe49dd017b7ec9f56d7b507589882feaae025af87264b`  
		Last Modified: Tue, 04 Nov 2025 00:40:26 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ac8c9f1ed6faea6ef3be74484d6a11652f9e6f5cdbe8ca8af1aa845fe31a13`  
		Last Modified: Tue, 04 Nov 2025 00:40:26 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:307926e4410ab61ffa7bda4dbc1dbc031e962751833c503875aa6ce97537a323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ee4a03c65edd2832e86161a4fa220c8425fd660cb8ae3ce77ff43964d29909`

```dockerfile
```

-	Layers:
	-	`sha256:89537ab92dfe8869fced5da7035705b23b02c930f972993ed3b0657d5f1a539c`  
		Last Modified: Tue, 04 Nov 2025 10:38:44 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dcb941ab017c349a070fcd93e071f12174f5602cf1e63489ef0fdb96c174cd5`  
		Last Modified: Tue, 04 Nov 2025 10:38:44 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:79397cbdd8e74b69af227cfaf5b5a383bbdbfc218d65258e2a4fc9de1c154e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f233963757d28c2646279181a229b499bcbcdc1d7415b59d65e0f84c2e0886b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:54:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:54:15 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Nov 2025 00:54:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:54:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:54:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:54:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:54:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:54:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:54:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:54:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ff144fadd3f6a9f788139a677d004ee848c87e4e142cebb6b989a23a5bcce3`  
		Last Modified: Tue, 04 Nov 2025 00:54:36 GMT  
		Size: 4.2 MB (4210650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca690a126392b34138bf9dc35c1a42498b71fc3147305c2509b3ddfe05d684f`  
		Last Modified: Tue, 04 Nov 2025 00:54:40 GMT  
		Size: 33.2 MB (33238156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdff373de3db0f99d1392ac9affc52f03e50feb7603aaceb1bc30be574e30f8`  
		Last Modified: Tue, 04 Nov 2025 00:54:37 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b3cf98778b53cd032dfd264a34c0ac3125b789777fb951554f74f8d99dea5f`  
		Last Modified: Tue, 04 Nov 2025 00:54:37 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc595091f514617caa88a8fdb3c64c0e37153cfc535f36239e67802fd4d6bc3`  
		Last Modified: Tue, 04 Nov 2025 00:54:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:b0f1648b86fb615b4c5f3242a8e732c96be82c41376abec3cc0e96df9f038d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbb1301a2895e12e5055f193b9acb81863d1d6bcaa74142688a2a27a915b16b`

```dockerfile
```

-	Layers:
	-	`sha256:e0b2da8433310123ca6ae6a5f8430916cb938939873218ffd77f4bb29abf5552`  
		Last Modified: Tue, 04 Nov 2025 10:38:48 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88d6b87844a68520e6ee2732011c114353cae0f4e67bd7c66b261fb98ce2abcb`  
		Last Modified: Tue, 04 Nov 2025 10:38:49 GMT  
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
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053646d1ede74b4422e0751427c045b128d56b4d9c7521a34d9a3e2fd81f2fa6`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 290.8 KB (290771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fddb95d664d6dacdb2318596d88bdbacf9e5bde5abe2b7e4335d05288276ea`  
		Last Modified: Wed, 08 Oct 2025 23:01:21 GMT  
		Size: 19.6 MB (19556558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f367635d83aeb5f5f554e62a06a02ad833c17339cf302d30013629399527c0`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f90ee1715c3ce00ef0c8e4958732cd35aeb06708db0a00e83afbe1f17da89`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166e539db1f38a4aa1b578555a8c92c86979cbc08b8098fba9661f87ffe6167`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
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
		Last Modified: Thu, 09 Oct 2025 00:38:28 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87486fae9bd6ba27ac7806fc6b1c5c571f4d3de5fc46fd1b292df95f203bc24e`  
		Last Modified: Thu, 09 Oct 2025 00:38:28 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:7b7edaeff058f5318a9efe258125df7ae2aedeb6b25b63558c99d9f88a1e0928
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
$ docker pull chronograf@sha256:79e0e9b2091ec19547f00102866f8d9cacbabedd4235cc760908c0de600e0fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69230990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c9bedad71af104b14727de1ba14af627adea4afc721fd8b1cede8cc7f044bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:28:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:28:19 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Nov 2025 00:28:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:28:19 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:28:19 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:28:19 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:28:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:28:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:28:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c172387ca69fbc10fde5f55f0010ba7888e5daa170cb1b2700117c755a683b7c`  
		Last Modified: Tue, 04 Nov 2025 00:28:35 GMT  
		Size: 4.2 MB (4209371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cfcfe3a8a5afab1bcb06df17b629564e444db5d38e3a1a3857ad413d5d53cd`  
		Last Modified: Tue, 04 Nov 2025 00:28:37 GMT  
		Size: 34.7 MB (34738628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75f9565e1e68f36342c3fae7b81481385c50b5f3bbd160f0399ec13d6682cd5`  
		Last Modified: Tue, 04 Nov 2025 00:28:35 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b56394cf836ceb1a1d9d06ed1b2831e9b0f3139c140d2f21a95c907b54c1040`  
		Last Modified: Tue, 04 Nov 2025 00:28:35 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7514ca2ca63742957942fca58b9f761ac8f5472f8c91a65b529d392fc299282`  
		Last Modified: Tue, 04 Nov 2025 00:28:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:54fa1828ec43685539cbedaed235906180c0f4966c174c271a467f788ab1a0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c830988a651765173eebe92a797a4586a3486184820bc4ae0af6f4c22bbf63`

```dockerfile
```

-	Layers:
	-	`sha256:8e90faa645b4eedcb2f38e5f89e8be29fa31726fad4e79bb62ed492e375e27d1`  
		Last Modified: Tue, 04 Nov 2025 10:38:39 GMT  
		Size: 3.0 MB (3048873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa8a94a11b5215372fdff516165e2dd2aa8cafcc4aa419a0f1065aa8f425b87`  
		Last Modified: Tue, 04 Nov 2025 10:38:40 GMT  
		Size: 15.7 KB (15734 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:9d406b0662ef3799bb5b27ccbbcc9889daae0585a570e638c6734b4c353506df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62179925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7361929bc4bc9a8239dc378d3f1b5f4faf0d940d8247a6504aebeb25d3b82d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:39:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:40:06 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Nov 2025 00:40:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:40:06 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:40:06 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:40:06 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:40:06 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:40:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:40:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:40:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5add2125bf9631befcab62d5e04ad41781bbc4aa838aed7e164e81e0929dd346`  
		Last Modified: Tue, 04 Nov 2025 00:13:15 GMT  
		Size: 25.5 MB (25546326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a70cdbe3d26c97224e20ddc0f06d2b85e854daf47c193948d0e157c3799d1bf`  
		Last Modified: Tue, 04 Nov 2025 00:40:27 GMT  
		Size: 3.5 MB (3511634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae062a58c16c9f5e129f590025e26b573ed52ed7aa85a9540df7b8b355fa128`  
		Last Modified: Tue, 04 Nov 2025 00:40:30 GMT  
		Size: 33.1 MB (33097570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46447b25e982172f37f258a8b75a36baf60265d9968fdd136745add23f3f00c5`  
		Last Modified: Tue, 04 Nov 2025 00:40:26 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad24fd3933e97dcdcefe49dd017b7ec9f56d7b507589882feaae025af87264b`  
		Last Modified: Tue, 04 Nov 2025 00:40:26 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ac8c9f1ed6faea6ef3be74484d6a11652f9e6f5cdbe8ca8af1aa845fe31a13`  
		Last Modified: Tue, 04 Nov 2025 00:40:26 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:307926e4410ab61ffa7bda4dbc1dbc031e962751833c503875aa6ce97537a323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ee4a03c65edd2832e86161a4fa220c8425fd660cb8ae3ce77ff43964d29909`

```dockerfile
```

-	Layers:
	-	`sha256:89537ab92dfe8869fced5da7035705b23b02c930f972993ed3b0657d5f1a539c`  
		Last Modified: Tue, 04 Nov 2025 10:38:44 GMT  
		Size: 3.1 MB (3051144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dcb941ab017c349a070fcd93e071f12174f5602cf1e63489ef0fdb96c174cd5`  
		Last Modified: Tue, 04 Nov 2025 10:38:44 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:79397cbdd8e74b69af227cfaf5b5a383bbdbfc218d65258e2a4fc9de1c154e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66221759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f233963757d28c2646279181a229b499bcbcdc1d7415b59d65e0f84c2e0886b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:54:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:54:15 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 04 Nov 2025 00:54:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:54:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:54:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:54:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:54:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:54:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:54:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:54:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ff144fadd3f6a9f788139a677d004ee848c87e4e142cebb6b989a23a5bcce3`  
		Last Modified: Tue, 04 Nov 2025 00:54:36 GMT  
		Size: 4.2 MB (4210650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca690a126392b34138bf9dc35c1a42498b71fc3147305c2509b3ddfe05d684f`  
		Last Modified: Tue, 04 Nov 2025 00:54:40 GMT  
		Size: 33.2 MB (33238156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdff373de3db0f99d1392ac9affc52f03e50feb7603aaceb1bc30be574e30f8`  
		Last Modified: Tue, 04 Nov 2025 00:54:37 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b3cf98778b53cd032dfd264a34c0ac3125b789777fb951554f74f8d99dea5f`  
		Last Modified: Tue, 04 Nov 2025 00:54:37 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc595091f514617caa88a8fdb3c64c0e37153cfc535f36239e67802fd4d6bc3`  
		Last Modified: Tue, 04 Nov 2025 00:54:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:b0f1648b86fb615b4c5f3242a8e732c96be82c41376abec3cc0e96df9f038d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3064951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbb1301a2895e12e5055f193b9acb81863d1d6bcaa74142688a2a27a915b16b`

```dockerfile
```

-	Layers:
	-	`sha256:e0b2da8433310123ca6ae6a5f8430916cb938939873218ffd77f4bb29abf5552`  
		Last Modified: Tue, 04 Nov 2025 10:38:48 GMT  
		Size: 3.0 MB (3049122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88d6b87844a68520e6ee2732011c114353cae0f4e67bd7c66b261fb98ce2abcb`  
		Last Modified: Tue, 04 Nov 2025 10:38:49 GMT  
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
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053646d1ede74b4422e0751427c045b128d56b4d9c7521a34d9a3e2fd81f2fa6`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 290.8 KB (290771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fddb95d664d6dacdb2318596d88bdbacf9e5bde5abe2b7e4335d05288276ea`  
		Last Modified: Wed, 08 Oct 2025 23:01:21 GMT  
		Size: 19.6 MB (19556558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f367635d83aeb5f5f554e62a06a02ad833c17339cf302d30013629399527c0`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07f90ee1715c3ce00ef0c8e4958732cd35aeb06708db0a00e83afbe1f17da89`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 11.9 KB (11891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9166e539db1f38a4aa1b578555a8c92c86979cbc08b8098fba9661f87ffe6167`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
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
		Last Modified: Thu, 09 Oct 2025 00:38:28 GMT  
		Size: 171.8 KB (171832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87486fae9bd6ba27ac7806fc6b1c5c571f4d3de5fc46fd1b292df95f203bc24e`  
		Last Modified: Thu, 09 Oct 2025 00:38:28 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:f7944397f0946ac95ed58282e39ac475a725b6433239bde9b1b2c3f4c75411af
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
$ docker pull chronograf@sha256:657b4964663b02fcc879b446fb62eae6e4d9214378f7357b8acf4923d671639d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26969d19760b04a9beb0faac6da0a56cb849f8ad81a5d0cca1a4403672da314d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:28:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:28:29 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 04 Nov 2025 00:28:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:28:29 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:28:29 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:28:29 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:28:29 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:28:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:28:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b5f653eeed4d4a0853ec7a606e2d39d00ee31b784c9e0b133b9644d29f0ce5`  
		Last Modified: Tue, 04 Nov 2025 00:28:45 GMT  
		Size: 5.2 MB (5224241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe4a299ed02c78ed89a11ac05d41a3b9a9c33d21e5a9457ff1c95781eb658a0`  
		Last Modified: Tue, 04 Nov 2025 00:28:47 GMT  
		Size: 34.4 MB (34364297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd5a370d5d6381d87ecb3784e8e2976ef110ac325728533d4baa67316e58a6a`  
		Last Modified: Tue, 04 Nov 2025 00:28:45 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c37c384330ca8a62b263abcd201520a434eea8c41b18e421f9e9179873b74`  
		Last Modified: Tue, 04 Nov 2025 00:28:45 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9c164131844ac59263c45720f9c2f4733f1d5fe942e26dd86ed357490ace96`  
		Last Modified: Tue, 04 Nov 2025 00:28:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:efb036dc2d4f5f3214e23f499b85ec2ba5023da48576565887d72ed87dea2608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e2b5f2a0a98918150205467b19bf0b490d20be0e0bea45c89dbeb35b0a8b52`

```dockerfile
```

-	Layers:
	-	`sha256:85682614bbdcaaee1ecbc14943243829ad836b13f74d59710f8cc187963ea0fa`  
		Last Modified: Tue, 04 Nov 2025 10:38:55 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dac1bcc5ba94cec62f0adf4e241c922c220213814e9eecc9578ff581d5af86d`  
		Last Modified: Tue, 04 Nov 2025 10:38:55 GMT  
		Size: 15.8 KB (15773 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e99c1aea01b8baee82ef780b8b1477a377f75403df3405de3bc06a84510c2478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e844cb4eaed41145279ca0d823ba86ed2ceecb6321ea2d7d53cfa20b57fb705d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:40:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:40:32 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 04 Nov 2025 00:40:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:40:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:40:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:40:32 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:40:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:40:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:40:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:40:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5add2125bf9631befcab62d5e04ad41781bbc4aa838aed7e164e81e0929dd346`  
		Last Modified: Tue, 04 Nov 2025 00:13:15 GMT  
		Size: 25.5 MB (25546326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38a5da14533b1b57201c80b1db24de3e0c776d69668c33c2492607eb08a7282`  
		Last Modified: Tue, 04 Nov 2025 00:40:48 GMT  
		Size: 4.5 MB (4490242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f21100c6e7de28ba7e23ce371b22afe0c9c39a0f7f1fecfde3868fa9457f8e`  
		Last Modified: Tue, 04 Nov 2025 00:40:52 GMT  
		Size: 32.5 MB (32534888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e102eb9d31cf5ec21abb4e1867ccf671cfc748fc3d3c881e88d7c234e8274b9`  
		Last Modified: Tue, 04 Nov 2025 00:40:48 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d424ebdc64fd684324a6d66cd65275ad74e5926c51da1f2473db5d77c782693c`  
		Last Modified: Tue, 04 Nov 2025 00:40:48 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f55fab5f348fae2378a9c8df57a120d4c983dfdbaa7753605144a3efb91e0b`  
		Last Modified: Tue, 04 Nov 2025 00:40:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:da76b8e51722ca18a0ce990f791a5113bc755b7ed61d61d0a51a800f2b737d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1d08bd73a4053573627c635cc9e1c6c36d0c8cdddcb8e02381498efcdac945`

```dockerfile
```

-	Layers:
	-	`sha256:f1808a9a611c2784698e53d95cc24b77960455fe41996710fb30e6ddbc379c05`  
		Last Modified: Tue, 04 Nov 2025 10:38:59 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb1b0a58017398c88b5357218d4e89e90c24ddcb67d1894aed8c27f3a033fae`  
		Last Modified: Tue, 04 Nov 2025 10:39:00 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:1c41c25afdb55e663d8bc2a3c1d9bb25e427b3cb6a43bfaf501f04fff6f51590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db43410dd60f364ad43a7ecf1f7a53d42c99a00b5ed0e34d750f1e7933892be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:30:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:30:21 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 04 Nov 2025 00:30:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:30:21 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:30:21 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:30:21 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:30:21 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:30:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:30:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:30:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67763994a5daf1853fdd023b74cb0abe690911f8ca76168c24ba11620f0a62dc`  
		Last Modified: Tue, 04 Nov 2025 00:30:38 GMT  
		Size: 5.2 MB (5208133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3591a7059872aa2ff11db9cb79f235b2aeeec38c489796fcd4b92bf4c78cc3a`  
		Last Modified: Tue, 04 Nov 2025 00:30:43 GMT  
		Size: 32.4 MB (32429488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f94ffbf44ff238d67d48f143feac3cdfd3fd8e6c8d3f0bcf88852f2f546fa13`  
		Last Modified: Tue, 04 Nov 2025 00:30:37 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f4cf88a39e252ef538055e1eeae1abbb60280dd245a143ce17dc80917a9d2a`  
		Last Modified: Tue, 04 Nov 2025 00:30:37 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c89ce351a1637c16cfbfd03fe8857ceafc719f0612aa0d7961b4c44c8cc395`  
		Last Modified: Tue, 04 Nov 2025 00:30:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:3710110a30a56c66b99622a5584fc2773f26f634cc34a10cec8920db11d76d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4aba388464584ecd51227fc7e2cfc1d69ef6c53130dd8f4cd645e6276f9194`

```dockerfile
```

-	Layers:
	-	`sha256:a1628f528a4e51f432262376092c4d6e9a4e57bcacc117ab86f09ffc8203af12`  
		Last Modified: Tue, 04 Nov 2025 10:39:04 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be3239aa29d6ab1c4fb3187d229792784e97856d2912d00da5f541cdcb4ce510`  
		Last Modified: Tue, 04 Nov 2025 10:39:04 GMT  
		Size: 15.9 KB (15869 bytes)  
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
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaabc96984af774b48937345c7cc275e3315d3a9a42aeb994f6946de24556be`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff81f10ae11b38f809feee3b7a44d508880916016658ca83647ff9d1c294aba`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cf4bd3a04c4941275f4aa1db1887c01bcdadeb973d9c95d34bc905b974dce`  
		Last Modified: Wed, 08 Oct 2025 23:01:11 GMT  
		Size: 19.2 MB (19204014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4732a865d574eb12cd7075d139d6bbd7d47fea3c367baf1a1f56ff51506906fb`  
		Last Modified: Wed, 08 Oct 2025 23:01:08 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0733dea6fe6d3cf04ef8c52dec6540501fbf0e79664e84fd00853fab32410e15`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58005a9627e476ca3528af5a14e30f0d4549afa8e314dcde58ee7ec5fd6671`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
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
		Last Modified: Thu, 09 Oct 2025 00:38:34 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61687d781240db246500ccffe6dc5608d9be7a5e7c809173a2694ffec485f7c3`  
		Last Modified: Thu, 09 Oct 2025 00:38:35 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:f7944397f0946ac95ed58282e39ac475a725b6433239bde9b1b2c3f4c75411af
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
$ docker pull chronograf@sha256:657b4964663b02fcc879b446fb62eae6e4d9214378f7357b8acf4923d671639d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69871533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26969d19760b04a9beb0faac6da0a56cb849f8ad81a5d0cca1a4403672da314d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:28:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:28:29 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 04 Nov 2025 00:28:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:28:29 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:28:29 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:28:29 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:28:29 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:28:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:28:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b5f653eeed4d4a0853ec7a606e2d39d00ee31b784c9e0b133b9644d29f0ce5`  
		Last Modified: Tue, 04 Nov 2025 00:28:45 GMT  
		Size: 5.2 MB (5224241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe4a299ed02c78ed89a11ac05d41a3b9a9c33d21e5a9457ff1c95781eb658a0`  
		Last Modified: Tue, 04 Nov 2025 00:28:47 GMT  
		Size: 34.4 MB (34364297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd5a370d5d6381d87ecb3784e8e2976ef110ac325728533d4baa67316e58a6a`  
		Last Modified: Tue, 04 Nov 2025 00:28:45 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c37c384330ca8a62b263abcd201520a434eea8c41b18e421f9e9179873b74`  
		Last Modified: Tue, 04 Nov 2025 00:28:45 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9c164131844ac59263c45720f9c2f4733f1d5fe942e26dd86ed357490ace96`  
		Last Modified: Tue, 04 Nov 2025 00:28:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:efb036dc2d4f5f3214e23f499b85ec2ba5023da48576565887d72ed87dea2608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e2b5f2a0a98918150205467b19bf0b490d20be0e0bea45c89dbeb35b0a8b52`

```dockerfile
```

-	Layers:
	-	`sha256:85682614bbdcaaee1ecbc14943243829ad836b13f74d59710f8cc187963ea0fa`  
		Last Modified: Tue, 04 Nov 2025 10:38:55 GMT  
		Size: 3.1 MB (3104511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dac1bcc5ba94cec62f0adf4e241c922c220213814e9eecc9578ff581d5af86d`  
		Last Modified: Tue, 04 Nov 2025 10:38:55 GMT  
		Size: 15.8 KB (15773 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e99c1aea01b8baee82ef780b8b1477a377f75403df3405de3bc06a84510c2478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e844cb4eaed41145279ca0d823ba86ed2ceecb6321ea2d7d53cfa20b57fb705d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:40:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:40:32 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 04 Nov 2025 00:40:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:40:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:40:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:40:32 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:40:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:40:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:40:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:40:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5add2125bf9631befcab62d5e04ad41781bbc4aa838aed7e164e81e0929dd346`  
		Last Modified: Tue, 04 Nov 2025 00:13:15 GMT  
		Size: 25.5 MB (25546326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38a5da14533b1b57201c80b1db24de3e0c776d69668c33c2492607eb08a7282`  
		Last Modified: Tue, 04 Nov 2025 00:40:48 GMT  
		Size: 4.5 MB (4490242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f21100c6e7de28ba7e23ce371b22afe0c9c39a0f7f1fecfde3868fa9457f8e`  
		Last Modified: Tue, 04 Nov 2025 00:40:52 GMT  
		Size: 32.5 MB (32534888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e102eb9d31cf5ec21abb4e1867ccf671cfc748fc3d3c881e88d7c234e8274b9`  
		Last Modified: Tue, 04 Nov 2025 00:40:48 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d424ebdc64fd684324a6d66cd65275ad74e5926c51da1f2473db5d77c782693c`  
		Last Modified: Tue, 04 Nov 2025 00:40:48 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f55fab5f348fae2378a9c8df57a120d4c983dfdbaa7753605144a3efb91e0b`  
		Last Modified: Tue, 04 Nov 2025 00:40:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:da76b8e51722ca18a0ce990f791a5113bc755b7ed61d61d0a51a800f2b737d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1d08bd73a4053573627c635cc9e1c6c36d0c8cdddcb8e02381498efcdac945`

```dockerfile
```

-	Layers:
	-	`sha256:f1808a9a611c2784698e53d95cc24b77960455fe41996710fb30e6ddbc379c05`  
		Last Modified: Tue, 04 Nov 2025 10:38:59 GMT  
		Size: 3.1 MB (3106782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb1b0a58017398c88b5357218d4e89e90c24ddcb67d1894aed8c27f3a033fae`  
		Last Modified: Tue, 04 Nov 2025 10:39:00 GMT  
		Size: 15.9 KB (15851 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:1c41c25afdb55e663d8bc2a3c1d9bb25e427b3cb6a43bfaf501f04fff6f51590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66410572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db43410dd60f364ad43a7ecf1f7a53d42c99a00b5ed0e34d750f1e7933892be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:30:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:30:21 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 04 Nov 2025 00:30:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:30:21 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:30:21 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:30:21 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:30:21 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:30:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:30:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:30:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67763994a5daf1853fdd023b74cb0abe690911f8ca76168c24ba11620f0a62dc`  
		Last Modified: Tue, 04 Nov 2025 00:30:38 GMT  
		Size: 5.2 MB (5208133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3591a7059872aa2ff11db9cb79f235b2aeeec38c489796fcd4b92bf4c78cc3a`  
		Last Modified: Tue, 04 Nov 2025 00:30:43 GMT  
		Size: 32.4 MB (32429488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f94ffbf44ff238d67d48f143feac3cdfd3fd8e6c8d3f0bcf88852f2f546fa13`  
		Last Modified: Tue, 04 Nov 2025 00:30:37 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f4cf88a39e252ef538055e1eeae1abbb60280dd245a143ce17dc80917a9d2a`  
		Last Modified: Tue, 04 Nov 2025 00:30:37 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c89ce351a1637c16cfbfd03fe8857ceafc719f0612aa0d7961b4c44c8cc395`  
		Last Modified: Tue, 04 Nov 2025 00:30:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:3710110a30a56c66b99622a5584fc2773f26f634cc34a10cec8920db11d76d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3120629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4aba388464584ecd51227fc7e2cfc1d69ef6c53130dd8f4cd645e6276f9194`

```dockerfile
```

-	Layers:
	-	`sha256:a1628f528a4e51f432262376092c4d6e9a4e57bcacc117ab86f09ffc8203af12`  
		Last Modified: Tue, 04 Nov 2025 10:39:04 GMT  
		Size: 3.1 MB (3104760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be3239aa29d6ab1c4fb3187d229792784e97856d2912d00da5f541cdcb4ce510`  
		Last Modified: Tue, 04 Nov 2025 10:39:04 GMT  
		Size: 15.9 KB (15869 bytes)  
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
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaabc96984af774b48937345c7cc275e3315d3a9a42aeb994f6946de24556be`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff81f10ae11b38f809feee3b7a44d508880916016658ca83647ff9d1c294aba`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8cf4bd3a04c4941275f4aa1db1887c01bcdadeb973d9c95d34bc905b974dce`  
		Last Modified: Wed, 08 Oct 2025 23:01:11 GMT  
		Size: 19.2 MB (19204014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4732a865d574eb12cd7075d139d6bbd7d47fea3c367baf1a1f56ff51506906fb`  
		Last Modified: Wed, 08 Oct 2025 23:01:08 GMT  
		Size: 12.2 KB (12240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0733dea6fe6d3cf04ef8c52dec6540501fbf0e79664e84fd00853fab32410e15`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe58005a9627e476ca3528af5a14e30f0d4549afa8e314dcde58ee7ec5fd6671`  
		Last Modified: Wed, 08 Oct 2025 23:01:09 GMT  
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
		Last Modified: Thu, 09 Oct 2025 00:38:34 GMT  
		Size: 228.3 KB (228341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61687d781240db246500ccffe6dc5608d9be7a5e7c809173a2694ffec485f7c3`  
		Last Modified: Thu, 09 Oct 2025 00:38:35 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:6f17133b22c16dc6994e0eb0ed1b7ce2f72e84a824892521bf955d133dc6b2fa
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
$ docker pull chronograf@sha256:077dd34d946f01132b6512fabd222a9c26232cf3b53b80e3e20e5f8a3fb662e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829661d13b9fa7a486f673b8af4d7570073533ea25f7500afe3d88ed4f2944f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:28:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:28:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 04 Nov 2025 00:28:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:28:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:28:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:28:32 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:28:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:28:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:28:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4216daa5cdce14841aa960bd2a7d4d0b3b5953a340c8f813b87364bbdeee736d`  
		Last Modified: Tue, 04 Nov 2025 00:28:49 GMT  
		Size: 5.2 MB (5224238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7db819d7a20525956ebd70c7c34bb787cbede9d51ff1134ef27470ab581b3fc`  
		Last Modified: Tue, 04 Nov 2025 00:28:57 GMT  
		Size: 35.0 MB (35011734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211b00ff3117c1d6b1dcd86c958ecdb0e69d3b97536577f3d9c9d713ce6ff096`  
		Last Modified: Tue, 04 Nov 2025 00:28:49 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ff21e9967b211573965f2fb31389154bc08541cf9e023fa345ce7c13abe23d`  
		Last Modified: Tue, 04 Nov 2025 00:28:49 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0de6b9ef1e04bfa376e5576923ff6e470d09ebc08122bcc55136adc8456d3d`  
		Last Modified: Tue, 04 Nov 2025 00:28:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:16e01e665b1e15b0bedba10e6c6e59c61b76941900e54f35963baf7a1291f95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598fa26bc8c1d9f0b6e1463cd0bb79d30f789bdbfb9d11dc3e2d33f3adf7ac4c`

```dockerfile
```

-	Layers:
	-	`sha256:53ca736d198b913c878043ba7e02ef6f1a7d0a2abce8c76041b7cae04583680b`  
		Last Modified: Tue, 04 Nov 2025 00:28:42 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c107812ecb4b52b85c965a77d28f4f0bbed9eb2eed800990d2ec36607550a6dc`  
		Last Modified: Tue, 04 Nov 2025 00:28:42 GMT  
		Size: 15.8 KB (15766 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:018b368cf3bdffff71a3e6d162c7eab9cd1658030f6bc037c1480c16f8e67d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63372465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7b85449e1db256e84d5666150bcadf2fbad5f482fe1ffb59fb889ca832d035`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:40:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:40:39 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 04 Nov 2025 00:40:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:40:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:40:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:40:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:40:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:40:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:40:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:40:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5add2125bf9631befcab62d5e04ad41781bbc4aa838aed7e164e81e0929dd346`  
		Last Modified: Tue, 04 Nov 2025 00:13:15 GMT  
		Size: 25.5 MB (25546326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337683d6ad101fcc47eb528cd3480173b95535f70977fc30ab4315de3b2aa419`  
		Last Modified: Tue, 04 Nov 2025 00:40:55 GMT  
		Size: 4.5 MB (4490200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1af45b2224c1110434d940207b9d4ac53ef6ec76ca490324d75b3289ea96b32`  
		Last Modified: Tue, 04 Nov 2025 00:40:58 GMT  
		Size: 33.3 MB (33311551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9683de7083206f56a832ecc4dcaaee231a99da68b674870c39906a7136b3a7`  
		Last Modified: Tue, 04 Nov 2025 00:40:54 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06a9922b2263f1bb455f81713878b770bff9030e1ba0193138e24c30120a984`  
		Last Modified: Tue, 04 Nov 2025 00:40:54 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f259250f3465fc622725a20ab81c1d1be92e83a2c1e8fe2d99aa98a9daddde`  
		Last Modified: Tue, 04 Nov 2025 00:40:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:9d7f9f329a9e3c5b1aac13167c3a197bdb879d6027d558d8bc7e1aca2aaa28ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c5db6e619b33a4976a8d3a4d35c868f4908b55ebc8466c544406b8e70514c1`

```dockerfile
```

-	Layers:
	-	`sha256:980e6cb68f91d5d78f7800109e915f67f9570aaf9a4f7c0dfd9bc40d36b31d31`  
		Last Modified: Tue, 04 Nov 2025 00:40:49 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9480b1227a6dbe5a6f26d675b04e53bbe60cd5d3fc499de238b146cc4d640c81`  
		Last Modified: Tue, 04 Nov 2025 00:40:49 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c505aa074c0f6e7723cea3d607a0fa442b1350d929691fe1d4c505eac2cbc70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a451c8ff622525536cb96d7dbe3bfc283030fa2848ae645b38a42cae790be1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:30:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:30:40 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 04 Nov 2025 00:30:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:30:40 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:30:40 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:30:40 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:30:40 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:30:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:30:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:30:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0440c36bb5a54890a9bbf4fff4c98a9f9080b1ba28abcd3f0effcdaa7d222488`  
		Last Modified: Tue, 04 Nov 2025 00:30:58 GMT  
		Size: 5.2 MB (5208142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a590f3a0ceb534a5d65afcf7365312f0143a9dfc69010badd2c2c3ab281fe86`  
		Last Modified: Tue, 04 Nov 2025 00:31:01 GMT  
		Size: 33.2 MB (33182178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb292e382027b612d6aed4f232be361eb5cfa860128130f4d0b2669c8d3e183`  
		Last Modified: Tue, 04 Nov 2025 00:30:57 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea997ae791ac278eb3e9c160acfdc75620569eb66f14153d7153311ed75da28`  
		Last Modified: Tue, 04 Nov 2025 00:30:57 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb71fea19370598b93c39cf055f4045ae1ee43f70766903506c678f1faada1df`  
		Last Modified: Tue, 04 Nov 2025 00:30:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:4bfda4fe572d49679e55e43be3010c0d864e73f3f17f079260b71116147920e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c830e7737916106ba0f462e3ecd1a01d58e02300faf37e63ffcb8d41d5cbc9`

```dockerfile
```

-	Layers:
	-	`sha256:9dc02c5417588311273725f0123bdb9b111cbecef4df67a1ae6df8e16c9534fe`  
		Last Modified: Tue, 04 Nov 2025 00:30:50 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee6bac7acd3ebe554acbb87c6cd84097b1393861b481adb8b6125a1db71f8d1`  
		Last Modified: Tue, 04 Nov 2025 00:30:49 GMT  
		Size: 15.9 KB (15861 bytes)  
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
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6c508c6ab14eb797ff6524630894eea223ff1b5a3f02be3595aff5713c5112`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43383a0cdbbe70773cd822a7089d90f254cc6923262bc86a209c0c182a190472`  
		Last Modified: Wed, 08 Oct 2025 23:01:26 GMT  
		Size: 19.7 MB (19672095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11524f4d626f224d1faadbb2537a398d423351e2a0d854a4a43b4692fab631c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811766d26cc20ed9c9dee509c4ef17aa945fbbf00be418890deec226cbeae620`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90296708765453bd34d3b31917ee366ec4e86d0d341504ddd046c032d6f85842`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
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
		Last Modified: Thu, 09 Oct 2025 00:38:42 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586220b931721e2b29f86f48af9fa3579d18c357b0351f043fc2e76a05ebc52`  
		Last Modified: Thu, 09 Oct 2025 00:38:42 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:6f17133b22c16dc6994e0eb0ed1b7ce2f72e84a824892521bf955d133dc6b2fa
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
$ docker pull chronograf@sha256:077dd34d946f01132b6512fabd222a9c26232cf3b53b80e3e20e5f8a3fb662e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829661d13b9fa7a486f673b8af4d7570073533ea25f7500afe3d88ed4f2944f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:28:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:28:32 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 04 Nov 2025 00:28:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:28:32 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:28:32 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:28:32 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:28:32 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:28:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:28:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4216daa5cdce14841aa960bd2a7d4d0b3b5953a340c8f813b87364bbdeee736d`  
		Last Modified: Tue, 04 Nov 2025 00:28:49 GMT  
		Size: 5.2 MB (5224238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7db819d7a20525956ebd70c7c34bb787cbede9d51ff1134ef27470ab581b3fc`  
		Last Modified: Tue, 04 Nov 2025 00:28:57 GMT  
		Size: 35.0 MB (35011734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211b00ff3117c1d6b1dcd86c958ecdb0e69d3b97536577f3d9c9d713ce6ff096`  
		Last Modified: Tue, 04 Nov 2025 00:28:49 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ff21e9967b211573965f2fb31389154bc08541cf9e023fa345ce7c13abe23d`  
		Last Modified: Tue, 04 Nov 2025 00:28:49 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0de6b9ef1e04bfa376e5576923ff6e470d09ebc08122bcc55136adc8456d3d`  
		Last Modified: Tue, 04 Nov 2025 00:28:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:16e01e665b1e15b0bedba10e6c6e59c61b76941900e54f35963baf7a1291f95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598fa26bc8c1d9f0b6e1463cd0bb79d30f789bdbfb9d11dc3e2d33f3adf7ac4c`

```dockerfile
```

-	Layers:
	-	`sha256:53ca736d198b913c878043ba7e02ef6f1a7d0a2abce8c76041b7cae04583680b`  
		Last Modified: Tue, 04 Nov 2025 00:28:42 GMT  
		Size: 3.1 MB (3109721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c107812ecb4b52b85c965a77d28f4f0bbed9eb2eed800990d2ec36607550a6dc`  
		Last Modified: Tue, 04 Nov 2025 00:28:42 GMT  
		Size: 15.8 KB (15766 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:018b368cf3bdffff71a3e6d162c7eab9cd1658030f6bc037c1480c16f8e67d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63372465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7b85449e1db256e84d5666150bcadf2fbad5f482fe1ffb59fb889ca832d035`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:40:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:40:39 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 04 Nov 2025 00:40:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:40:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:40:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:40:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:40:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:40:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:40:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:40:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:5add2125bf9631befcab62d5e04ad41781bbc4aa838aed7e164e81e0929dd346`  
		Last Modified: Tue, 04 Nov 2025 00:13:15 GMT  
		Size: 25.5 MB (25546326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337683d6ad101fcc47eb528cd3480173b95535f70977fc30ab4315de3b2aa419`  
		Last Modified: Tue, 04 Nov 2025 00:40:55 GMT  
		Size: 4.5 MB (4490200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1af45b2224c1110434d940207b9d4ac53ef6ec76ca490324d75b3289ea96b32`  
		Last Modified: Tue, 04 Nov 2025 00:40:58 GMT  
		Size: 33.3 MB (33311551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9683de7083206f56a832ecc4dcaaee231a99da68b674870c39906a7136b3a7`  
		Last Modified: Tue, 04 Nov 2025 00:40:54 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06a9922b2263f1bb455f81713878b770bff9030e1ba0193138e24c30120a984`  
		Last Modified: Tue, 04 Nov 2025 00:40:54 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f259250f3465fc622725a20ab81c1d1be92e83a2c1e8fe2d99aa98a9daddde`  
		Last Modified: Tue, 04 Nov 2025 00:40:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:9d7f9f329a9e3c5b1aac13167c3a197bdb879d6027d558d8bc7e1aca2aaa28ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3127836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c5db6e619b33a4976a8d3a4d35c868f4908b55ebc8466c544406b8e70514c1`

```dockerfile
```

-	Layers:
	-	`sha256:980e6cb68f91d5d78f7800109e915f67f9570aaf9a4f7c0dfd9bc40d36b31d31`  
		Last Modified: Tue, 04 Nov 2025 00:40:49 GMT  
		Size: 3.1 MB (3111992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9480b1227a6dbe5a6f26d675b04e53bbe60cd5d3fc499de238b146cc4d640c81`  
		Last Modified: Tue, 04 Nov 2025 00:40:49 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:c505aa074c0f6e7723cea3d607a0fa442b1350d929691fe1d4c505eac2cbc70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67163275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a451c8ff622525536cb96d7dbe3bfc283030fa2848ae645b38a42cae790be1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:30:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:30:40 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 04 Nov 2025 00:30:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:30:40 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:30:40 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:30:40 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:30:40 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:30:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:30:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:30:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0440c36bb5a54890a9bbf4fff4c98a9f9080b1ba28abcd3f0effcdaa7d222488`  
		Last Modified: Tue, 04 Nov 2025 00:30:58 GMT  
		Size: 5.2 MB (5208142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a590f3a0ceb534a5d65afcf7365312f0143a9dfc69010badd2c2c3ab281fe86`  
		Last Modified: Tue, 04 Nov 2025 00:31:01 GMT  
		Size: 33.2 MB (33182178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb292e382027b612d6aed4f232be361eb5cfa860128130f4d0b2669c8d3e183`  
		Last Modified: Tue, 04 Nov 2025 00:30:57 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea997ae791ac278eb3e9c160acfdc75620569eb66f14153d7153311ed75da28`  
		Last Modified: Tue, 04 Nov 2025 00:30:57 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb71fea19370598b93c39cf055f4045ae1ee43f70766903506c678f1faada1df`  
		Last Modified: Tue, 04 Nov 2025 00:30:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:4bfda4fe572d49679e55e43be3010c0d864e73f3f17f079260b71116147920e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3125831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c830e7737916106ba0f462e3ecd1a01d58e02300faf37e63ffcb8d41d5cbc9`

```dockerfile
```

-	Layers:
	-	`sha256:9dc02c5417588311273725f0123bdb9b111cbecef4df67a1ae6df8e16c9534fe`  
		Last Modified: Tue, 04 Nov 2025 00:30:50 GMT  
		Size: 3.1 MB (3109970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee6bac7acd3ebe554acbb87c6cd84097b1393861b481adb8b6125a1db71f8d1`  
		Last Modified: Tue, 04 Nov 2025 00:30:49 GMT  
		Size: 15.9 KB (15861 bytes)  
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
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70c842384492021fdcd617e3e57dbc08546ebeb0a55cf5f01aa575170280c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6c508c6ab14eb797ff6524630894eea223ff1b5a3f02be3595aff5713c5112`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 290.8 KB (290774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43383a0cdbbe70773cd822a7089d90f254cc6923262bc86a209c0c182a190472`  
		Last Modified: Wed, 08 Oct 2025 23:01:26 GMT  
		Size: 19.7 MB (19672095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11524f4d626f224d1faadbb2537a398d423351e2a0d854a4a43b4692fab631c6`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 12.2 KB (12232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811766d26cc20ed9c9dee509c4ef17aa945fbbf00be418890deec226cbeae620`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
		Size: 11.9 KB (11888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90296708765453bd34d3b31917ee366ec4e86d0d341504ddd046c032d6f85842`  
		Last Modified: Wed, 08 Oct 2025 23:01:25 GMT  
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
		Last Modified: Thu, 09 Oct 2025 00:38:42 GMT  
		Size: 233.6 KB (233553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586220b931721e2b29f86f48af9fa3579d18c357b0351f043fc2e76a05ebc52`  
		Last Modified: Thu, 09 Oct 2025 00:38:42 GMT  
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
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cd1461c07b6d2b803ff1e365582cea280da85884cb0fe20c1b539046e9c0f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642952c8832a913bc8124d8c1f9800b4c40ed32aa2d21f4bbd9c85e32729fdf2`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 314.6 KB (314639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff188fbd44ef51d6c15c61b590915a7d108294cea3cebd1224f569cf88dbfbd2`  
		Last Modified: Wed, 08 Oct 2025 23:01:31 GMT  
		Size: 28.6 MB (28558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada6ea712a91804f080e3ac3a6fec72f1bf330d8affb0a76902b1f0b78a5046`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 12.2 KB (12237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d214c5daa6878e468360de897da9cd0cad1be05283f5529b5e2ce07c9e72f`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f9d62a6d73ab836332ca97429aec6104967dc35d5ab6aaa103f374c1539bd`  
		Last Modified: Wed, 08 Oct 2025 23:01:28 GMT  
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
		Last Modified: Thu, 09 Oct 2025 00:38:17 GMT  
		Size: 250.4 KB (250383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7ffc31e817e3fff1eade663dcae6dc3da5bb4370e43abaf921eebc9dd7f0a1`  
		Last Modified: Thu, 09 Oct 2025 00:38:18 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:8952c2a46185337082b6d88ee50ce168a6a7a183a7c6ecdc916d124dd705567f
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
$ docker pull chronograf@sha256:3e15fa77498d4b818b90a5994800e69f96529443ffed92a8f7c2cb4b4dd59200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85408341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3ce7300403c65c4b1e86422daebb73997c5c296c52251b72af6e32d992f469`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:28:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 04 Nov 2025 00:28:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:28:41 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:28:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:28:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed73089ebb3295175b105a893325db8b1f74db21ed868ff7e0fa080fae5b82c3`  
		Last Modified: Tue, 04 Nov 2025 00:28:59 GMT  
		Size: 7.9 MB (7878726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54c4f5cf93b1af5a7738b010f1a6a387946e1899973195b3f9760d455c13683`  
		Last Modified: Tue, 04 Nov 2025 00:29:04 GMT  
		Size: 49.3 MB (49276586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33928fff17d35ab8b07bb2938c602b5b243e900e2803cdba382e49bd9dec3e2`  
		Last Modified: Tue, 04 Nov 2025 00:28:59 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0e94b53f4943e061ca85cce8309b535f35f192db64ae3d8cf4b9fc884629c3`  
		Last Modified: Tue, 04 Nov 2025 00:28:59 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa8b959a19273bcc5d337452af8736eabbb36810d62038b88625bc2ae39b5ff`  
		Last Modified: Tue, 04 Nov 2025 00:28:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:3b7a84e83406126586039673c4c2c19ce0b5a7b31811fcf9a4be078ed0c9d6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59599068fca04d4ef9255a25af2a9e2d59d40d310ba4ecd628827090402786a`

```dockerfile
```

-	Layers:
	-	`sha256:279d5adbc3510522d190cf3b9440a094990afb38f8c30b9754fc0f7bed35d33e`  
		Last Modified: Tue, 04 Nov 2025 10:38:27 GMT  
		Size: 2.9 MB (2854074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42d216008927e758e45450bde8d106e54acf3244feb021dfe1a3154dcbab9aba`  
		Last Modified: Tue, 04 Nov 2025 10:38:27 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d1ca2a60d34c0e3fb74aa85c14f8538a09d87cb9910644649f52270922fe6275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76088570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d1c8795fbaca4ddd76b57a435bdda497671dc838643469701cd199bb1045fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:41:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 04 Nov 2025 00:41:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:41:11 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:41:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:41:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:41:11 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea58372cbc1e2233482831a509b9a309c4183ac0bd32fca8b29224745a3b4a38`  
		Last Modified: Tue, 04 Nov 2025 00:41:29 GMT  
		Size: 6.5 MB (6508150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01d64c10b637f7f78e240bf5c26f6195a21885625c5413dbb27ee82807875ea`  
		Last Modified: Tue, 04 Nov 2025 00:41:35 GMT  
		Size: 45.6 MB (45621823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea7e911dc89a8ef5464737bf0d16d1d17d52006a69bb2df4b8d8a1654acac1f`  
		Last Modified: Tue, 04 Nov 2025 00:41:28 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742fd2d1edb94445b05649b50e9327a910ece29230a020981b51d5e9445968c6`  
		Last Modified: Tue, 04 Nov 2025 00:41:28 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d929c27d5213b702e7e8c679440d000c068d6d85566011c7d6469680a1f6dbc5`  
		Last Modified: Tue, 04 Nov 2025 00:41:28 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:f5c4c6747fffadf6ec6e8fceb39f5fac9ab178ad3fe02c06aa319917353e4ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67c163c09c73fc886bebfd4b3b0592e57073cebabb316497c31a94401ae2543`

```dockerfile
```

-	Layers:
	-	`sha256:9b1bbb5579dda3559a9ac105d6f53642f89f68d498ee4f6f9248cd6146031266`  
		Last Modified: Tue, 04 Nov 2025 10:38:31 GMT  
		Size: 2.9 MB (2856371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52d2e71775c655e2048ade8e325ef7ea260038230e7914ca079785bee9d2985f`  
		Last Modified: Tue, 04 Nov 2025 10:38:32 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:40791fbfbab907848dcddc3d42f76951b86d7373531e57c6222a38133fbe8c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82885502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c29a15584be0079e5c539feddbfa2ec71d1c2eccafdc75dac480715eaf252fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:34 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
ENV CHRONOGRAF_VERSION=1.10.8
# Tue, 04 Nov 2025 00:30:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 04 Nov 2025 00:30:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 04 Nov 2025 00:30:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 04 Nov 2025 00:30:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 04 Nov 2025 00:30:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41428d9a237511f0a4e48bd146ce6ed1087542a1518962e37a2c4e4cbe3a87fb`  
		Last Modified: Tue, 04 Nov 2025 00:30:56 GMT  
		Size: 7.7 MB (7691888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98d94554815c13464c2ba8ba9d816f241b8445c2b7b0e7bbd271ed5aabc6f9f`  
		Last Modified: Tue, 04 Nov 2025 00:31:03 GMT  
		Size: 47.1 MB (47066760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adfc1cee5921690552291343756ebe367c85ba43eaa585fcf648e87a4ba80b1`  
		Last Modified: Tue, 04 Nov 2025 00:30:56 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2108f3d0938214ddda0f9f88b3d198ac68519ee14ac34c0182a9aa7367f7ed8c`  
		Last Modified: Tue, 04 Nov 2025 00:30:57 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d31b7618f2b06e266e622f1c654257c5c58b9060d1adffe85cceb7bab55bc1`  
		Last Modified: Tue, 04 Nov 2025 00:30:57 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:02354048681fba16160db315177123e01ac67a67b8bd095f1ee1e4837d8e58cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c04f60cc35a41ef691114472792c84caa3fe9b4cb188e54543bb87874322f73`

```dockerfile
```

-	Layers:
	-	`sha256:7a9a41af9332653c56373fb96883cad8706ba896080437020a5c17fdc60b6c1c`  
		Last Modified: Tue, 04 Nov 2025 10:38:35 GMT  
		Size: 2.9 MB (2854347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd7c3793902f9b0d3eb23d8d6e2cb4fb5949362275d3697e280d4ae4a4de627`  
		Last Modified: Tue, 04 Nov 2025 10:38:36 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json
