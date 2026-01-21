<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.8`](#emqx588)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:7585e570c1bb9414b1e1042e22bf1b06bce00d9b99d9536a6889502a017bea4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:a9650edd9fdc4f15992013004c5229dbd026b726cb0a9a40a0410a3c22fb0f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108397408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17dff756ef1aff958f60d012a427c89c054769d755bed31154b763974c4cf47`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:16:39 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 13 Jan 2026 01:16:39 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 13 Jan 2026 01:16:39 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 13 Jan 2026 01:16:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:16:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:16:39 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:16:39 GMT
USER emqx
# Tue, 13 Jan 2026 01:16:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:16:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:16:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:16:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:16:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dceb230e83bb8bc743aa37e81f7cd505511e5beec0659ede59e7c2cb0671b7`  
		Last Modified: Tue, 13 Jan 2026 01:17:05 GMT  
		Size: 78.6 MB (78622661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39349b182205263062f734efc0588aafd46c8024e185c9e1d0b3fb6e410a6da2`  
		Last Modified: Tue, 13 Jan 2026 01:16:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:bafd51acc6e7a6440aa026fc9b4f85128335f3da6f197c7ce2cad0d8aeb2f72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62178f4891b9e72e7c61c360b5f01de02699e0d16a5ec8b20c3d0018d400f72`

```dockerfile
```

-	Layers:
	-	`sha256:2a0e0fcede93b90310f54e6130b0f3268db3e8c1c2664496d39ca6ca9d4d8073`  
		Last Modified: Tue, 13 Jan 2026 01:16:53 GMT  
		Size: 2.4 MB (2403463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2075dae3331b14a99bdc6144a436c04085530d0f903372d45287a41060d1ea0`  
		Last Modified: Tue, 13 Jan 2026 06:29:08 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2afc009a32aad6b0353480873027ef2d0b093bc18824d3cd5c1bdf57b2ae9bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106665479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab77492e6236c24f45b95cce628ae014e396f0145ae841a5217865ef6a9b6edd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:27 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 13 Jan 2026 01:17:27 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 13 Jan 2026 01:17:27 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 13 Jan 2026 01:17:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:28 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae82769fae53b576f967b5aaba216c788f7e834bb01daa6b9ec3353811e3c30b`  
		Last Modified: Tue, 13 Jan 2026 01:17:57 GMT  
		Size: 76.5 MB (76530374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95d537084054513975c6621d3f551d5c25fd778faaa9e88e6b1c9e5c501600d`  
		Last Modified: Tue, 13 Jan 2026 01:17:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:18acb9d20698d0fa54c2b5098b6cbe60da3bd7e0f9e4a6f7bb54e2e29dce093a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2867c9f7e497ac4ba35cd80100699ce16be85ea61ce383bea338e29500982e`

```dockerfile
```

-	Layers:
	-	`sha256:83bbe8e83cc379af23032e5d9e0bfaabb2eda78d0e6664fb5bf2619e0044ee2f`  
		Last Modified: Tue, 13 Jan 2026 01:17:41 GMT  
		Size: 2.4 MB (2403752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41188b6e930ba00d90dd4040a070af16891f6c9b8cd375e13e82853587235e83`  
		Last Modified: Tue, 13 Jan 2026 01:17:41 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:dcc5bbed8b6ebb5ec378ff16d217d11e7330557f1ceebf7e38c00e74a4ef75db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:935956b35ec8bc1cbfe09d43ab8512f34927b13172e7de5d06cc4bceb42816ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055b821f359c707981abd89414422f6f61de51db4fe98a126f6ffd1ad315678a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:17:20 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 13 Jan 2026 01:17:20 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 13 Jan 2026 01:17:20 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 13 Jan 2026 01:17:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:20 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:20 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:20 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:20 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab74449a03a22b66830e443f3b0ed5a0306aeb75e47cac051e2701170924a744`  
		Last Modified: Tue, 13 Jan 2026 01:17:36 GMT  
		Size: 97.2 MB (97155190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03b7bdaa94708eeb34de76b4623e5c21cc7083645a9f98dd74170b2f1b64733`  
		Last Modified: Tue, 13 Jan 2026 03:13:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:fcf7d0ad88e470b0cc17bc66ee48cd051a1a2c84849b89fad5ec736803ea89d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181e2811ec82261c190c03be0676af888de41aafe28f41491f1f30f0e2970452`

```dockerfile
```

-	Layers:
	-	`sha256:2ee44092a589ef431269ec51582af421b9d6920b5c48cd2afa56886f004714eb`  
		Last Modified: Tue, 13 Jan 2026 06:29:14 GMT  
		Size: 2.8 MB (2751398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddbdd23b4d37a0ccb0ab10fe7fa80c8ca96471a257de578fb52f274086e4906a`  
		Last Modified: Tue, 13 Jan 2026 06:29:14 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:38879dd3f65d644b282b35f7a75905548c1d41deb3a8ad687ef6e0138a780723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121825284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712c291c7949a90bf628a0565e9e020f9773ece818e6836f7737ac7e6806318c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:17:27 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 13 Jan 2026 01:17:27 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 13 Jan 2026 01:17:27 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 13 Jan 2026 01:17:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:27 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:27 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:27 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:27 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:27 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:27 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899d84c99c6e08fef0acbfe90da1407373d98ff31c4d0fbaeef0e33ba8c533e9`  
		Last Modified: Tue, 13 Jan 2026 01:17:57 GMT  
		Size: 93.7 MB (93716331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5bea8798303aa2d61b52b47f2b48c318068d7e46c3c24e3ae614d2a5019f73`  
		Last Modified: Tue, 13 Jan 2026 01:17:48 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:71b2128e5182c03e7eb6db846f0dfa5c7d10a7fab755ead3b2f526e1147f0e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19dbec7c55d8b5f04b7aec9d0709d1cd662e2dc8e0837f9fbf3e68294fdaeb9`

```dockerfile
```

-	Layers:
	-	`sha256:dc855847bb841400f02ae4a30c97505baa06284c736e16eadfc46e7e23097e50`  
		Last Modified: Tue, 13 Jan 2026 03:28:52 GMT  
		Size: 2.8 MB (2751654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45b92534341307f98e5afeedb6ed59f040c60f5ac76a841ba5affe92c39fcdb`  
		Last Modified: Tue, 13 Jan 2026 01:17:42 GMT  
		Size: 12.0 KB (11987 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:dcc5bbed8b6ebb5ec378ff16d217d11e7330557f1ceebf7e38c00e74a4ef75db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:935956b35ec8bc1cbfe09d43ab8512f34927b13172e7de5d06cc4bceb42816ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055b821f359c707981abd89414422f6f61de51db4fe98a126f6ffd1ad315678a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:17:20 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 13 Jan 2026 01:17:20 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 13 Jan 2026 01:17:20 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 13 Jan 2026 01:17:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:20 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:20 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:20 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:20 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab74449a03a22b66830e443f3b0ed5a0306aeb75e47cac051e2701170924a744`  
		Last Modified: Tue, 13 Jan 2026 01:17:36 GMT  
		Size: 97.2 MB (97155190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03b7bdaa94708eeb34de76b4623e5c21cc7083645a9f98dd74170b2f1b64733`  
		Last Modified: Tue, 13 Jan 2026 03:13:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:fcf7d0ad88e470b0cc17bc66ee48cd051a1a2c84849b89fad5ec736803ea89d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181e2811ec82261c190c03be0676af888de41aafe28f41491f1f30f0e2970452`

```dockerfile
```

-	Layers:
	-	`sha256:2ee44092a589ef431269ec51582af421b9d6920b5c48cd2afa56886f004714eb`  
		Last Modified: Tue, 13 Jan 2026 06:29:14 GMT  
		Size: 2.8 MB (2751398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddbdd23b4d37a0ccb0ab10fe7fa80c8ca96471a257de578fb52f274086e4906a`  
		Last Modified: Tue, 13 Jan 2026 06:29:14 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:38879dd3f65d644b282b35f7a75905548c1d41deb3a8ad687ef6e0138a780723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121825284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712c291c7949a90bf628a0565e9e020f9773ece818e6836f7737ac7e6806318c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:17:27 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 13 Jan 2026 01:17:27 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 13 Jan 2026 01:17:27 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 13 Jan 2026 01:17:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:27 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:27 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:27 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:27 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:27 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:27 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899d84c99c6e08fef0acbfe90da1407373d98ff31c4d0fbaeef0e33ba8c533e9`  
		Last Modified: Tue, 13 Jan 2026 01:17:57 GMT  
		Size: 93.7 MB (93716331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5bea8798303aa2d61b52b47f2b48c318068d7e46c3c24e3ae614d2a5019f73`  
		Last Modified: Tue, 13 Jan 2026 01:17:48 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:71b2128e5182c03e7eb6db846f0dfa5c7d10a7fab755ead3b2f526e1147f0e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19dbec7c55d8b5f04b7aec9d0709d1cd662e2dc8e0837f9fbf3e68294fdaeb9`

```dockerfile
```

-	Layers:
	-	`sha256:dc855847bb841400f02ae4a30c97505baa06284c736e16eadfc46e7e23097e50`  
		Last Modified: Tue, 13 Jan 2026 03:28:52 GMT  
		Size: 2.8 MB (2751654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e45b92534341307f98e5afeedb6ed59f040c60f5ac76a841ba5affe92c39fcdb`  
		Last Modified: Tue, 13 Jan 2026 01:17:42 GMT  
		Size: 12.0 KB (11987 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:7585e570c1bb9414b1e1042e22bf1b06bce00d9b99d9536a6889502a017bea4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:a9650edd9fdc4f15992013004c5229dbd026b726cb0a9a40a0410a3c22fb0f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108397408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17dff756ef1aff958f60d012a427c89c054769d755bed31154b763974c4cf47`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:16:39 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 13 Jan 2026 01:16:39 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 13 Jan 2026 01:16:39 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 13 Jan 2026 01:16:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:16:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:16:39 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:16:39 GMT
USER emqx
# Tue, 13 Jan 2026 01:16:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:16:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:16:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:16:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:16:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dceb230e83bb8bc743aa37e81f7cd505511e5beec0659ede59e7c2cb0671b7`  
		Last Modified: Tue, 13 Jan 2026 01:17:05 GMT  
		Size: 78.6 MB (78622661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39349b182205263062f734efc0588aafd46c8024e185c9e1d0b3fb6e410a6da2`  
		Last Modified: Tue, 13 Jan 2026 01:16:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:bafd51acc6e7a6440aa026fc9b4f85128335f3da6f197c7ce2cad0d8aeb2f72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62178f4891b9e72e7c61c360b5f01de02699e0d16a5ec8b20c3d0018d400f72`

```dockerfile
```

-	Layers:
	-	`sha256:2a0e0fcede93b90310f54e6130b0f3268db3e8c1c2664496d39ca6ca9d4d8073`  
		Last Modified: Tue, 13 Jan 2026 01:16:53 GMT  
		Size: 2.4 MB (2403463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2075dae3331b14a99bdc6144a436c04085530d0f903372d45287a41060d1ea0`  
		Last Modified: Tue, 13 Jan 2026 06:29:08 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2afc009a32aad6b0353480873027ef2d0b093bc18824d3cd5c1bdf57b2ae9bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106665479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab77492e6236c24f45b95cce628ae014e396f0145ae841a5217865ef6a9b6edd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:27 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 13 Jan 2026 01:17:27 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 13 Jan 2026 01:17:27 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 13 Jan 2026 01:17:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:28 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae82769fae53b576f967b5aaba216c788f7e834bb01daa6b9ec3353811e3c30b`  
		Last Modified: Tue, 13 Jan 2026 01:17:57 GMT  
		Size: 76.5 MB (76530374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95d537084054513975c6621d3f551d5c25fd778faaa9e88e6b1c9e5c501600d`  
		Last Modified: Tue, 13 Jan 2026 01:17:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:18acb9d20698d0fa54c2b5098b6cbe60da3bd7e0f9e4a6f7bb54e2e29dce093a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2867c9f7e497ac4ba35cd80100699ce16be85ea61ce383bea338e29500982e`

```dockerfile
```

-	Layers:
	-	`sha256:83bbe8e83cc379af23032e5d9e0bfaabb2eda78d0e6664fb5bf2619e0044ee2f`  
		Last Modified: Tue, 13 Jan 2026 01:17:41 GMT  
		Size: 2.4 MB (2403752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41188b6e930ba00d90dd4040a070af16891f6c9b8cd375e13e82853587235e83`  
		Last Modified: Tue, 13 Jan 2026 01:17:41 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:7585e570c1bb9414b1e1042e22bf1b06bce00d9b99d9536a6889502a017bea4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.8` - linux; amd64

```console
$ docker pull emqx@sha256:a9650edd9fdc4f15992013004c5229dbd026b726cb0a9a40a0410a3c22fb0f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108397408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17dff756ef1aff958f60d012a427c89c054769d755bed31154b763974c4cf47`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:16:39 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 13 Jan 2026 01:16:39 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 13 Jan 2026 01:16:39 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 13 Jan 2026 01:16:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:16:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:16:39 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:16:39 GMT
USER emqx
# Tue, 13 Jan 2026 01:16:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:16:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:16:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:16:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:16:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dceb230e83bb8bc743aa37e81f7cd505511e5beec0659ede59e7c2cb0671b7`  
		Last Modified: Tue, 13 Jan 2026 01:17:05 GMT  
		Size: 78.6 MB (78622661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39349b182205263062f734efc0588aafd46c8024e185c9e1d0b3fb6e410a6da2`  
		Last Modified: Tue, 13 Jan 2026 01:16:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:bafd51acc6e7a6440aa026fc9b4f85128335f3da6f197c7ce2cad0d8aeb2f72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62178f4891b9e72e7c61c360b5f01de02699e0d16a5ec8b20c3d0018d400f72`

```dockerfile
```

-	Layers:
	-	`sha256:2a0e0fcede93b90310f54e6130b0f3268db3e8c1c2664496d39ca6ca9d4d8073`  
		Last Modified: Tue, 13 Jan 2026 01:16:53 GMT  
		Size: 2.4 MB (2403463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2075dae3331b14a99bdc6144a436c04085530d0f903372d45287a41060d1ea0`  
		Last Modified: Tue, 13 Jan 2026 06:29:08 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2afc009a32aad6b0353480873027ef2d0b093bc18824d3cd5c1bdf57b2ae9bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106665479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab77492e6236c24f45b95cce628ae014e396f0145ae841a5217865ef6a9b6edd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:27 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 13 Jan 2026 01:17:27 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 13 Jan 2026 01:17:27 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 13 Jan 2026 01:17:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:28 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae82769fae53b576f967b5aaba216c788f7e834bb01daa6b9ec3353811e3c30b`  
		Last Modified: Tue, 13 Jan 2026 01:17:57 GMT  
		Size: 76.5 MB (76530374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95d537084054513975c6621d3f551d5c25fd778faaa9e88e6b1c9e5c501600d`  
		Last Modified: Tue, 13 Jan 2026 01:17:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:18acb9d20698d0fa54c2b5098b6cbe60da3bd7e0f9e4a6f7bb54e2e29dce093a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2867c9f7e497ac4ba35cd80100699ce16be85ea61ce383bea338e29500982e`

```dockerfile
```

-	Layers:
	-	`sha256:83bbe8e83cc379af23032e5d9e0bfaabb2eda78d0e6664fb5bf2619e0044ee2f`  
		Last Modified: Tue, 13 Jan 2026 01:17:41 GMT  
		Size: 2.4 MB (2403752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41188b6e930ba00d90dd4040a070af16891f6c9b8cd375e13e82853587235e83`  
		Last Modified: Tue, 13 Jan 2026 01:17:41 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:7585e570c1bb9414b1e1042e22bf1b06bce00d9b99d9536a6889502a017bea4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:a9650edd9fdc4f15992013004c5229dbd026b726cb0a9a40a0410a3c22fb0f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108397408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17dff756ef1aff958f60d012a427c89c054769d755bed31154b763974c4cf47`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:16:39 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 13 Jan 2026 01:16:39 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 13 Jan 2026 01:16:39 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 13 Jan 2026 01:16:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:16:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:16:39 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:16:39 GMT
USER emqx
# Tue, 13 Jan 2026 01:16:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:16:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:16:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:16:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:16:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dceb230e83bb8bc743aa37e81f7cd505511e5beec0659ede59e7c2cb0671b7`  
		Last Modified: Tue, 13 Jan 2026 01:17:05 GMT  
		Size: 78.6 MB (78622661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39349b182205263062f734efc0588aafd46c8024e185c9e1d0b3fb6e410a6da2`  
		Last Modified: Tue, 13 Jan 2026 01:16:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:bafd51acc6e7a6440aa026fc9b4f85128335f3da6f197c7ce2cad0d8aeb2f72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62178f4891b9e72e7c61c360b5f01de02699e0d16a5ec8b20c3d0018d400f72`

```dockerfile
```

-	Layers:
	-	`sha256:2a0e0fcede93b90310f54e6130b0f3268db3e8c1c2664496d39ca6ca9d4d8073`  
		Last Modified: Tue, 13 Jan 2026 01:16:53 GMT  
		Size: 2.4 MB (2403463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2075dae3331b14a99bdc6144a436c04085530d0f903372d45287a41060d1ea0`  
		Last Modified: Tue, 13 Jan 2026 06:29:08 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2afc009a32aad6b0353480873027ef2d0b093bc18824d3cd5c1bdf57b2ae9bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106665479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab77492e6236c24f45b95cce628ae014e396f0145ae841a5217865ef6a9b6edd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:17:27 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 13 Jan 2026 01:17:27 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 13 Jan 2026 01:17:27 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 13 Jan 2026 01:17:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Jan 2026 01:17:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
WORKDIR /opt/emqx
# Tue, 13 Jan 2026 01:17:28 GMT
USER emqx
# Tue, 13 Jan 2026 01:17:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Jan 2026 01:17:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 13 Jan 2026 01:17:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 13 Jan 2026 01:17:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:17:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae82769fae53b576f967b5aaba216c788f7e834bb01daa6b9ec3353811e3c30b`  
		Last Modified: Tue, 13 Jan 2026 01:17:57 GMT  
		Size: 76.5 MB (76530374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95d537084054513975c6621d3f551d5c25fd778faaa9e88e6b1c9e5c501600d`  
		Last Modified: Tue, 13 Jan 2026 01:17:48 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:18acb9d20698d0fa54c2b5098b6cbe60da3bd7e0f9e4a6f7bb54e2e29dce093a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2867c9f7e497ac4ba35cd80100699ce16be85ea61ce383bea338e29500982e`

```dockerfile
```

-	Layers:
	-	`sha256:83bbe8e83cc379af23032e5d9e0bfaabb2eda78d0e6664fb5bf2619e0044ee2f`  
		Last Modified: Tue, 13 Jan 2026 01:17:41 GMT  
		Size: 2.4 MB (2403752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41188b6e930ba00d90dd4040a070af16891f6c9b8cd375e13e82853587235e83`  
		Last Modified: Tue, 13 Jan 2026 01:17:41 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json
