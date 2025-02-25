<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.5`](#chronograf1105)
-	[`chronograf:1.10.5-alpine`](#chronograf1105-alpine)
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
$ docker pull chronograf@sha256:906f96320927a2cc1e18f2b13a25eec484635517485b2efc6074f564bd4602cb
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
$ docker pull chronograf@sha256:d8da46c45bbf4bd0233862e4e6c5ea3fe1e44b269bfc3adc4c9835515a2d68a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83336809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4b93152730951fc0a9dbbe459d10f98e2540e8d32411fc007e110349445c99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf4cc51ed963533bf134fc8a749b38d22fa512655c12a1ffa334511f7855bc2`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 7.9 MB (7875453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ec1ace7271a4d2e30062b834eeec24c82e5c1ad8e654d66f84b2ed5e3f1da5`  
		Last Modified: Tue, 25 Feb 2025 03:21:51 GMT  
		Size: 47.2 MB (47217579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c9a5ec5e92cece3ed0b6e36df99d0db435a77b0073273b2abb5c8ee2b9467`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f7aece400805a0b9f01aeff8371e20e5e94e6defb3b7bafaeb6ce70e9a40b3`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35f3ceb3a7710dabc099b27d711340f1973547771283dd8c59056a015f90c9c`  
		Last Modified: Tue, 25 Feb 2025 03:21:51 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:95c623a5c5d8b1b37515b7f948b2c08e827dc3cda6e27df34e780cb9d7c36d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a93a4b45f3e8c1f66c5fdafa7012770dfe37d4cdf8b00d0c70112adb99a789`

```dockerfile
```

-	Layers:
	-	`sha256:8ec4c32fbc96aaccb9a4ee61fa383f6667e3a2cab094516480ab751b286fdc17`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 2.7 MB (2703879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ce4bc83763ddf12872e270840e11bc59de9ea05777a529690dfa6b194a9a2b5`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:88720ca505bfb08c74f4ceb1bb1aba6cde492fdcac7046603b2f011a84107c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fc2fb831a0ea15181cc5095ac14d0b7f24ca9b9e780b114b6efdf3c79bccf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cc7c361314024427e46f49ca0282aad7c7e1c19e195d10077e345573507b56`  
		Last Modified: Tue, 04 Feb 2025 10:48:05 GMT  
		Size: 6.5 MB (6497872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6cf5468b4e77edddf9b77021e98d83564ca5e44d38fffb2aba4f385562d0c6`  
		Last Modified: Tue, 04 Feb 2025 10:48:06 GMT  
		Size: 44.3 MB (44276279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df4d3bd9618dd31da4448a675205925bb539ddd136533f180d0c85668fdf11f`  
		Last Modified: Tue, 04 Feb 2025 10:48:04 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08d3e3c8ed5226ce823000b1a5b22cc1043c1bf6cc8fb121e2d64f591e402e5`  
		Last Modified: Tue, 04 Feb 2025 10:48:05 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c93a0a6d68e759d05627b419cdbadd5c4c1f378ae68e2b3a1d70e4f1974b8`  
		Last Modified: Tue, 04 Feb 2025 10:48:05 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:062394e35a9237b5417145333219d7ca7d1b7140d82c1d6fd206202542ef59a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1153fa859ac40437c90717b2a11c8f758035eaaa7616057249db83fa8aefd24d`

```dockerfile
```

-	Layers:
	-	`sha256:06e80d01af57e5254ba8cac2ef064e8e41c67d40c82c76ae26ba6a4009ee6e63`  
		Last Modified: Tue, 04 Feb 2025 10:48:05 GMT  
		Size: 2.7 MB (2706158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba3bd0b60d93272f7e1bc61a85ba78c258b47fdcb5a8b570810fec9a060215b`  
		Last Modified: Tue, 04 Feb 2025 10:48:04 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:19624f2cf9bcadf070e04067581b2af0c9012d68168282a4e15a3a81f9efcbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80695516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f134edb6d33471cc442b9981a8f8cc87aef85c728f3463faf79898dfe273a7e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9c56777cdffdd5ca319eb018920d2e1c639be4e586bbe214e9067e145ec574`  
		Last Modified: Tue, 25 Feb 2025 05:45:10 GMT  
		Size: 7.7 MB (7652099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829f59d2de5ebc9eb3ba9a1162eca3708b86788efcf9f772038cbaedc1a3c5b0`  
		Last Modified: Tue, 25 Feb 2025 05:45:11 GMT  
		Size: 45.0 MB (44970527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b362ab190fa4d97f9a102ebab0beb5f09fce46ef41f48ce0d5862d78ae6cb4`  
		Last Modified: Tue, 25 Feb 2025 05:45:09 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4de6a654ea82d86a37134ae7ac84b946086660bd8feeed721e495f52095079`  
		Last Modified: Tue, 25 Feb 2025 05:45:09 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ce86954af7d4055352afb5a5534ef502a134de846887d85197fe6c77753b8`  
		Last Modified: Tue, 25 Feb 2025 05:45:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:0292b8508bd7b9503dc7cfb82b3e675a1a97bbf02222db05b28d7135d7b8d2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0adf99ae95e8ce3215b16017d6aa59dafc602c28b94ea91d0fd6fa50fb225c2`

```dockerfile
```

-	Layers:
	-	`sha256:a3b44361dd57918558a21ffd78a86337eb65ff10432211e762f92135915acf8a`  
		Last Modified: Tue, 25 Feb 2025 05:45:10 GMT  
		Size: 2.7 MB (2704152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b2bbb5f880bd581294211f5b785fbbae45eb64c20a23d03209835e00950dec`  
		Last Modified: Tue, 25 Feb 2025 05:45:09 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:d87e9a66df76dc2810442c6e52641e1f2df44d01d89f0c0c8ace7ee6de51dbbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:af46818df7f83a2ca358b3eb5f9317d68f8fb62299552df033d19ffb496ae0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31815096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9abcd8a6e187c12d41c913290917fed4516e1d543d9dcc2369ec95a2bbd73c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a49d50f1fe51a05325ae98d8bf9a879090b6be2b3527e6d11e59f960bdc93b7`  
		Last Modified: Fri, 14 Feb 2025 19:25:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361c594e3185bd08a55bb1bd9df81da69ae214a31a898c88bbfe9c942cb898a0`  
		Last Modified: Fri, 14 Feb 2025 19:25:04 GMT  
		Size: 296.5 KB (296499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f24eb5e953df43a31ec34d2b56d21a2c8cbbd486fcf0c69bf4c62ba2cf88cbb`  
		Last Modified: Fri, 14 Feb 2025 19:25:05 GMT  
		Size: 27.9 MB (27866993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf04d6dc2c59aa8ba5db19eae81f35471a84ac4f3294c76637f9a487fe496d47`  
		Last Modified: Fri, 14 Feb 2025 19:25:03 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d6b0cde41f5740d49b8b7c41868028d6382d2751fe1a8057d0eb8b1122b0e0`  
		Last Modified: Fri, 14 Feb 2025 19:25:04 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652ea0b93c690d604c1f573af1ecb8451a18b6e8e825f678e4c2555df428f549`  
		Last Modified: Fri, 14 Feb 2025 19:25:04 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:f7de0febfd6ddaf2ae32475727aa5806ff9254e253dc394f13a1e7d3965d90b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 KB (259450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0309720039e98d687cd49690b5b488d6e559d3736b87e0574422f03edd646db1`

```dockerfile
```

-	Layers:
	-	`sha256:27346ddfdfe4f4c0fc322b5de26cd7a216d974e4b609edbddd1dcaa51912afb6`  
		Last Modified: Fri, 14 Feb 2025 19:25:03 GMT  
		Size: 241.6 KB (241595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df79c104cbf58b736286d9972f51bb0074cc375c0bc55a4502f790fe4004478`  
		Last Modified: Fri, 14 Feb 2025 19:25:03 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5`

```console
$ docker pull chronograf@sha256:906f96320927a2cc1e18f2b13a25eec484635517485b2efc6074f564bd4602cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:1.10.5` - linux; amd64

```console
$ docker pull chronograf@sha256:d8da46c45bbf4bd0233862e4e6c5ea3fe1e44b269bfc3adc4c9835515a2d68a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83336809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4b93152730951fc0a9dbbe459d10f98e2540e8d32411fc007e110349445c99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf4cc51ed963533bf134fc8a749b38d22fa512655c12a1ffa334511f7855bc2`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 7.9 MB (7875453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ec1ace7271a4d2e30062b834eeec24c82e5c1ad8e654d66f84b2ed5e3f1da5`  
		Last Modified: Tue, 25 Feb 2025 03:21:51 GMT  
		Size: 47.2 MB (47217579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c9a5ec5e92cece3ed0b6e36df99d0db435a77b0073273b2abb5c8ee2b9467`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f7aece400805a0b9f01aeff8371e20e5e94e6defb3b7bafaeb6ce70e9a40b3`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35f3ceb3a7710dabc099b27d711340f1973547771283dd8c59056a015f90c9c`  
		Last Modified: Tue, 25 Feb 2025 03:21:51 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:95c623a5c5d8b1b37515b7f948b2c08e827dc3cda6e27df34e780cb9d7c36d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a93a4b45f3e8c1f66c5fdafa7012770dfe37d4cdf8b00d0c70112adb99a789`

```dockerfile
```

-	Layers:
	-	`sha256:8ec4c32fbc96aaccb9a4ee61fa383f6667e3a2cab094516480ab751b286fdc17`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 2.7 MB (2703879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ce4bc83763ddf12872e270840e11bc59de9ea05777a529690dfa6b194a9a2b5`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:88720ca505bfb08c74f4ceb1bb1aba6cde492fdcac7046603b2f011a84107c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fc2fb831a0ea15181cc5095ac14d0b7f24ca9b9e780b114b6efdf3c79bccf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cc7c361314024427e46f49ca0282aad7c7e1c19e195d10077e345573507b56`  
		Last Modified: Tue, 04 Feb 2025 10:48:05 GMT  
		Size: 6.5 MB (6497872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6cf5468b4e77edddf9b77021e98d83564ca5e44d38fffb2aba4f385562d0c6`  
		Last Modified: Tue, 04 Feb 2025 10:48:06 GMT  
		Size: 44.3 MB (44276279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df4d3bd9618dd31da4448a675205925bb539ddd136533f180d0c85668fdf11f`  
		Last Modified: Tue, 04 Feb 2025 10:48:04 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08d3e3c8ed5226ce823000b1a5b22cc1043c1bf6cc8fb121e2d64f591e402e5`  
		Last Modified: Tue, 04 Feb 2025 10:48:05 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c93a0a6d68e759d05627b419cdbadd5c4c1f378ae68e2b3a1d70e4f1974b8`  
		Last Modified: Tue, 04 Feb 2025 10:48:05 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:062394e35a9237b5417145333219d7ca7d1b7140d82c1d6fd206202542ef59a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1153fa859ac40437c90717b2a11c8f758035eaaa7616057249db83fa8aefd24d`

```dockerfile
```

-	Layers:
	-	`sha256:06e80d01af57e5254ba8cac2ef064e8e41c67d40c82c76ae26ba6a4009ee6e63`  
		Last Modified: Tue, 04 Feb 2025 10:48:05 GMT  
		Size: 2.7 MB (2706158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba3bd0b60d93272f7e1bc61a85ba78c258b47fdcb5a8b570810fec9a060215b`  
		Last Modified: Tue, 04 Feb 2025 10:48:04 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.10.5` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:19624f2cf9bcadf070e04067581b2af0c9012d68168282a4e15a3a81f9efcbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80695516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f134edb6d33471cc442b9981a8f8cc87aef85c728f3463faf79898dfe273a7e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9c56777cdffdd5ca319eb018920d2e1c639be4e586bbe214e9067e145ec574`  
		Last Modified: Tue, 25 Feb 2025 05:45:10 GMT  
		Size: 7.7 MB (7652099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829f59d2de5ebc9eb3ba9a1162eca3708b86788efcf9f772038cbaedc1a3c5b0`  
		Last Modified: Tue, 25 Feb 2025 05:45:11 GMT  
		Size: 45.0 MB (44970527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b362ab190fa4d97f9a102ebab0beb5f09fce46ef41f48ce0d5862d78ae6cb4`  
		Last Modified: Tue, 25 Feb 2025 05:45:09 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4de6a654ea82d86a37134ae7ac84b946086660bd8feeed721e495f52095079`  
		Last Modified: Tue, 25 Feb 2025 05:45:09 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ce86954af7d4055352afb5a5534ef502a134de846887d85197fe6c77753b8`  
		Last Modified: Tue, 25 Feb 2025 05:45:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5` - unknown; unknown

```console
$ docker pull chronograf@sha256:0292b8508bd7b9503dc7cfb82b3e675a1a97bbf02222db05b28d7135d7b8d2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0adf99ae95e8ce3215b16017d6aa59dafc602c28b94ea91d0fd6fa50fb225c2`

```dockerfile
```

-	Layers:
	-	`sha256:a3b44361dd57918558a21ffd78a86337eb65ff10432211e762f92135915acf8a`  
		Last Modified: Tue, 25 Feb 2025 05:45:10 GMT  
		Size: 2.7 MB (2704152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b2bbb5f880bd581294211f5b785fbbae45eb64c20a23d03209835e00950dec`  
		Last Modified: Tue, 25 Feb 2025 05:45:09 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.10.5-alpine`

```console
$ docker pull chronograf@sha256:d87e9a66df76dc2810442c6e52641e1f2df44d01d89f0c0c8ace7ee6de51dbbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.10.5-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:af46818df7f83a2ca358b3eb5f9317d68f8fb62299552df033d19ffb496ae0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31815096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9abcd8a6e187c12d41c913290917fed4516e1d543d9dcc2369ec95a2bbd73c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a49d50f1fe51a05325ae98d8bf9a879090b6be2b3527e6d11e59f960bdc93b7`  
		Last Modified: Fri, 14 Feb 2025 19:25:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361c594e3185bd08a55bb1bd9df81da69ae214a31a898c88bbfe9c942cb898a0`  
		Last Modified: Fri, 14 Feb 2025 19:25:04 GMT  
		Size: 296.5 KB (296499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f24eb5e953df43a31ec34d2b56d21a2c8cbbd486fcf0c69bf4c62ba2cf88cbb`  
		Last Modified: Fri, 14 Feb 2025 19:25:05 GMT  
		Size: 27.9 MB (27866993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf04d6dc2c59aa8ba5db19eae81f35471a84ac4f3294c76637f9a487fe496d47`  
		Last Modified: Fri, 14 Feb 2025 19:25:03 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d6b0cde41f5740d49b8b7c41868028d6382d2751fe1a8057d0eb8b1122b0e0`  
		Last Modified: Fri, 14 Feb 2025 19:25:04 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652ea0b93c690d604c1f573af1ecb8451a18b6e8e825f678e4c2555df428f549`  
		Last Modified: Fri, 14 Feb 2025 19:25:04 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.10.5-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:f7de0febfd6ddaf2ae32475727aa5806ff9254e253dc394f13a1e7d3965d90b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 KB (259450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0309720039e98d687cd49690b5b488d6e559d3736b87e0574422f03edd646db1`

```dockerfile
```

-	Layers:
	-	`sha256:27346ddfdfe4f4c0fc322b5de26cd7a216d974e4b609edbddd1dcaa51912afb6`  
		Last Modified: Fri, 14 Feb 2025 19:25:03 GMT  
		Size: 241.6 KB (241595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df79c104cbf58b736286d9972f51bb0074cc375c0bc55a4502f790fe4004478`  
		Last Modified: Fri, 14 Feb 2025 19:25:03 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:1ec553af5a2744430eb40cc203a5b32c6f03d2812f3ffa9d69201a5995391c80
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
$ docker pull chronograf@sha256:d09f789debcc44d20104a8972c7c562b01b18ff81be7d86453e17928c20bf6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69021129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c667ecd3b2963b148313e829ee7abc26efe20079c490858e3a23317f4c6868ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75174ce50b93cf107d0e67de190a980ec836881d33a112b0447e8cee1b6a58a`  
		Last Modified: Tue, 25 Feb 2025 02:12:53 GMT  
		Size: 4.2 MB (4209282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1158d625c0212688288ace2e57c46678e3f927ac98bf620f7576517542127e3d`  
		Last Modified: Tue, 25 Feb 2025 02:12:55 GMT  
		Size: 34.5 MB (34533521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa44d648c0ed20533fae37d2f26929ae165317fcd76213fe27099b8975265a`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695dc819cd75f7161a8d37a53e3ddb550100e51a93f48e0588ca0d7a3fc6f1b9`  
		Last Modified: Tue, 25 Feb 2025 02:12:53 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8997a471b6a9778e93f641986f6b53d9fb2a5093dca24155f2e8a6f3c9263913`  
		Last Modified: Tue, 25 Feb 2025 02:12:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:27ac7071edd9452e7140b2b59f3901227749cb67e2305082790369a8924e0b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6045ba66d6fd8eb85c183b72a3d9653ec2ac8ac45b8f03aa283478532b3223aa`

```dockerfile
```

-	Layers:
	-	`sha256:125f780e0cedb8c803a86011153dc123a720d8db77f541846be07ef50570f7c3`  
		Last Modified: Tue, 25 Feb 2025 02:12:53 GMT  
		Size: 2.9 MB (2905389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c60203c4ef60665dbafa234bcfa3e54db12bc0ee00fd8017931940471cd6f7d`  
		Last Modified: Tue, 25 Feb 2025 02:12:53 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:0b45b19e8d02ab828b08e779f6315cb4149387e917f84deec06f7a28290f8fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61962650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441789c2a55c36d830348f3df2826f53539f1c9eca5a9d6b843522e01ffaa47e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 01:38:07 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41935545bae39c8c212d5ff0711444db6a0798a1bd65ba52ef41dd95e4e73ed3`  
		Last Modified: Tue, 04 Feb 2025 10:46:06 GMT  
		Size: 3.5 MB (3511679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48d3819738a3457ded3bf596abb8918b543b2a6a221f6784323c10203e7f6b3`  
		Last Modified: Tue, 04 Feb 2025 10:46:07 GMT  
		Size: 32.9 MB (32892696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c028a40db260499e155c03fbe9b80e9f77ad1893d5e0c81390c0f06dc07efa`  
		Last Modified: Tue, 04 Feb 2025 10:46:06 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d77fa4be478920b2ff7036e7c07d7b43d88262062b593367ecbba63c4ac175`  
		Last Modified: Tue, 04 Feb 2025 10:46:06 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c3930e9b80f6f02c1b6527f9438724a64cbd0415dcc8055ffbc5465477a2ab`  
		Last Modified: Tue, 04 Feb 2025 10:46:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:2b519b26d5c3097ec62e53629e2376a2e47fdc000ffc1e5bce958962e389ab30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cc453835c19ac06a006dfc6429dc834c1f95aab4446cb476da94b28c8382e9`

```dockerfile
```

-	Layers:
	-	`sha256:87747bfde3d5e030ab0ec311511a7d35508bafc23af047e0f7456f502f0af63b`  
		Last Modified: Tue, 04 Feb 2025 10:46:06 GMT  
		Size: 2.9 MB (2907660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b975d9e6ce093870b553e4416993c0ae918f62d489d68702456c090c8f51d681`  
		Last Modified: Tue, 04 Feb 2025 10:46:06 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:145c0e534623fc66dc37e7be15ca27d19f8c533413531c75773a654b65043d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66014114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760773ebcb6c47d5fd2f544cf0dda2e4c7c758f25989dfa14e10d982d8d04fc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f39025597fcb3ad5cedb88b7ca00af183766d5a1bf9dd8dea7a4076dae436c9`  
		Last Modified: Tue, 25 Feb 2025 05:43:46 GMT  
		Size: 4.2 MB (4210655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879903329569c29ab60aeea07ac4ee5fd407a97f28ff68ae8f4660242d5ad05e`  
		Last Modified: Tue, 25 Feb 2025 05:43:47 GMT  
		Size: 33.0 MB (33033084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb4e4df48e99b83ae105bca9e8df9139296648d117829424f25d95608a736e`  
		Last Modified: Tue, 25 Feb 2025 05:43:45 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a169ec2e611ac7dcb33da272c0e5b9ca88f90728be34e4e7a7987650bc9fff`  
		Last Modified: Tue, 25 Feb 2025 05:43:46 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d112dc69c0a2c3c2b1f2e761c0aa9f4ac6addc5e9bc6da6d6edf0b9f83a828e`  
		Last Modified: Tue, 25 Feb 2025 05:43:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7` - unknown; unknown

```console
$ docker pull chronograf@sha256:0247bbd45c48c1627eb956c4ec6553851b9f25aaa26d71fec90dd918d3bf54ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74647f82b44a3d10f18607bffeb58db84d4bc2e6908d9f4ca1edf0ef52c13766`

```dockerfile
```

-	Layers:
	-	`sha256:b4a5b09978c4243dd3fc01c716df1191250c3ff5c5a049232cf536d27a302021`  
		Last Modified: Tue, 25 Feb 2025 05:43:46 GMT  
		Size: 2.9 MB (2905638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d14959f65c15cce0fa5352a761c4eecdbb0bca33b78efa930277de1b72531790`  
		Last Modified: Tue, 25 Feb 2025 05:43:45 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:df924b85652b1a3cf6ee401da68f4ef42a31256cd06244016ae21cec9f8952d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f033d37b112e959a0534de672abf91b9c3aa43535d685738ea85e838e904e8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23502749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137abfa83685c0597819295c4b3ef856c9395a461bd9bd70ff91ec3a4cd5921a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8ae06deb09ed334ed8eba44b6e425cced470152dbdd9c0e3c6125578263f57`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c71c1a03f44724b1796ddc3866d8fe5c4a5af8862448eabb7b2ebdc7a47748`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 19.6 MB (19556823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:0c38d57135acbd91b733dbd02beff4e0339d76bf9f15f687bd8c4f5a2f887e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 KB (189257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471658777992e65c6b6d0f2da3225f4e41179e9be460d18106df6b906e69e00b`

```dockerfile
```

-	Layers:
	-	`sha256:6592097eed7dd5f5abfbbe36bb576489b44efd68487a9d4d946f1dc3e7aeac87`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 172.3 KB (172345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af6f071245b63b559b430cac0c4aba0ef1cc49a72e9b52d3edae3f8b2d6ad95`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:1ec553af5a2744430eb40cc203a5b32c6f03d2812f3ffa9d69201a5995391c80
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
$ docker pull chronograf@sha256:d09f789debcc44d20104a8972c7c562b01b18ff81be7d86453e17928c20bf6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69021129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c667ecd3b2963b148313e829ee7abc26efe20079c490858e3a23317f4c6868ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75174ce50b93cf107d0e67de190a980ec836881d33a112b0447e8cee1b6a58a`  
		Last Modified: Tue, 25 Feb 2025 02:12:53 GMT  
		Size: 4.2 MB (4209282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1158d625c0212688288ace2e57c46678e3f927ac98bf620f7576517542127e3d`  
		Last Modified: Tue, 25 Feb 2025 02:12:55 GMT  
		Size: 34.5 MB (34533521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa44d648c0ed20533fae37d2f26929ae165317fcd76213fe27099b8975265a`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695dc819cd75f7161a8d37a53e3ddb550100e51a93f48e0588ca0d7a3fc6f1b9`  
		Last Modified: Tue, 25 Feb 2025 02:12:53 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8997a471b6a9778e93f641986f6b53d9fb2a5093dca24155f2e8a6f3c9263913`  
		Last Modified: Tue, 25 Feb 2025 02:12:54 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:27ac7071edd9452e7140b2b59f3901227749cb67e2305082790369a8924e0b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6045ba66d6fd8eb85c183b72a3d9653ec2ac8ac45b8f03aa283478532b3223aa`

```dockerfile
```

-	Layers:
	-	`sha256:125f780e0cedb8c803a86011153dc123a720d8db77f541846be07ef50570f7c3`  
		Last Modified: Tue, 25 Feb 2025 02:12:53 GMT  
		Size: 2.9 MB (2905389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c60203c4ef60665dbafa234bcfa3e54db12bc0ee00fd8017931940471cd6f7d`  
		Last Modified: Tue, 25 Feb 2025 02:12:53 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:0b45b19e8d02ab828b08e779f6315cb4149387e917f84deec06f7a28290f8fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61962650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441789c2a55c36d830348f3df2826f53539f1c9eca5a9d6b843522e01ffaa47e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 01:38:07 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41935545bae39c8c212d5ff0711444db6a0798a1bd65ba52ef41dd95e4e73ed3`  
		Last Modified: Tue, 04 Feb 2025 10:46:06 GMT  
		Size: 3.5 MB (3511679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48d3819738a3457ded3bf596abb8918b543b2a6a221f6784323c10203e7f6b3`  
		Last Modified: Tue, 04 Feb 2025 10:46:07 GMT  
		Size: 32.9 MB (32892696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c028a40db260499e155c03fbe9b80e9f77ad1893d5e0c81390c0f06dc07efa`  
		Last Modified: Tue, 04 Feb 2025 10:46:06 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d77fa4be478920b2ff7036e7c07d7b43d88262062b593367ecbba63c4ac175`  
		Last Modified: Tue, 04 Feb 2025 10:46:06 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c3930e9b80f6f02c1b6527f9438724a64cbd0415dcc8055ffbc5465477a2ab`  
		Last Modified: Tue, 04 Feb 2025 10:46:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:2b519b26d5c3097ec62e53629e2376a2e47fdc000ffc1e5bce958962e389ab30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cc453835c19ac06a006dfc6429dc834c1f95aab4446cb476da94b28c8382e9`

```dockerfile
```

-	Layers:
	-	`sha256:87747bfde3d5e030ab0ec311511a7d35508bafc23af047e0f7456f502f0af63b`  
		Last Modified: Tue, 04 Feb 2025 10:46:06 GMT  
		Size: 2.9 MB (2907660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b975d9e6ce093870b553e4416993c0ae918f62d489d68702456c090c8f51d681`  
		Last Modified: Tue, 04 Feb 2025 10:46:06 GMT  
		Size: 15.8 KB (15850 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:145c0e534623fc66dc37e7be15ca27d19f8c533413531c75773a654b65043d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66014114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760773ebcb6c47d5fd2f544cf0dda2e4c7c758f25989dfa14e10d982d8d04fc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f39025597fcb3ad5cedb88b7ca00af183766d5a1bf9dd8dea7a4076dae436c9`  
		Last Modified: Tue, 25 Feb 2025 05:43:46 GMT  
		Size: 4.2 MB (4210655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879903329569c29ab60aeea07ac4ee5fd407a97f28ff68ae8f4660242d5ad05e`  
		Last Modified: Tue, 25 Feb 2025 05:43:47 GMT  
		Size: 33.0 MB (33033084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bb4e4df48e99b83ae105bca9e8df9139296648d117829424f25d95608a736e`  
		Last Modified: Tue, 25 Feb 2025 05:43:45 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a169ec2e611ac7dcb33da272c0e5b9ca88f90728be34e4e7a7987650bc9fff`  
		Last Modified: Tue, 25 Feb 2025 05:43:46 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d112dc69c0a2c3c2b1f2e761c0aa9f4ac6addc5e9bc6da6d6edf0b9f83a828e`  
		Last Modified: Tue, 25 Feb 2025 05:43:46 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17` - unknown; unknown

```console
$ docker pull chronograf@sha256:0247bbd45c48c1627eb956c4ec6553851b9f25aaa26d71fec90dd918d3bf54ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2921510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74647f82b44a3d10f18607bffeb58db84d4bc2e6908d9f4ca1edf0ef52c13766`

```dockerfile
```

-	Layers:
	-	`sha256:b4a5b09978c4243dd3fc01c716df1191250c3ff5c5a049232cf536d27a302021`  
		Last Modified: Tue, 25 Feb 2025 05:43:46 GMT  
		Size: 2.9 MB (2905638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d14959f65c15cce0fa5352a761c4eecdbb0bca33b78efa930277de1b72531790`  
		Last Modified: Tue, 25 Feb 2025 05:43:45 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:df924b85652b1a3cf6ee401da68f4ef42a31256cd06244016ae21cec9f8952d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f033d37b112e959a0534de672abf91b9c3aa43535d685738ea85e838e904e8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23502749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137abfa83685c0597819295c4b3ef856c9395a461bd9bd70ff91ec3a4cd5921a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8ae06deb09ed334ed8eba44b6e425cced470152dbdd9c0e3c6125578263f57`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c71c1a03f44724b1796ddc3866d8fe5c4a5af8862448eabb7b2ebdc7a47748`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 19.6 MB (19556823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.7.17-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:0c38d57135acbd91b733dbd02beff4e0339d76bf9f15f687bd8c4f5a2f887e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 KB (189257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471658777992e65c6b6d0f2da3225f4e41179e9be460d18106df6b906e69e00b`

```dockerfile
```

-	Layers:
	-	`sha256:6592097eed7dd5f5abfbbe36bb576489b44efd68487a9d4d946f1dc3e7aeac87`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 172.3 KB (172345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af6f071245b63b559b430cac0c4aba0ef1cc49a72e9b52d3edae3f8b2d6ad95`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:eeb0bebead600f40240994ac745c283bc988d016e1716c9a5a35acb47e6bbaa2
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
$ docker pull chronograf@sha256:21b2b2b00e46932b45a4c8e9ce25b6d49c1d9e235bb4e7eaedabeb8d9fd11518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69662843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aa9448439ba648c132218c42951265b56aa8463881d8e31994492fa6878d91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d89f38058a1222576e243f9f2306447da4bbc11b0f11c25a69ac881374013`  
		Last Modified: Tue, 25 Feb 2025 02:13:08 GMT  
		Size: 5.0 MB (5020292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2e0a9cb53dc07668dd7a98ad67e01e0aec94d7ac7999246a01a83afdff9321`  
		Last Modified: Tue, 25 Feb 2025 02:13:08 GMT  
		Size: 34.4 MB (34364239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8dfc70ae99f41b36540e57ee090b72467dfb4e9acb681109f986ce33586727`  
		Last Modified: Tue, 25 Feb 2025 02:13:07 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b44e855431f0cfb8ccc7317c7ababd64bf5dc9a97251d63efb0de5456e28b1`  
		Last Modified: Tue, 25 Feb 2025 02:13:07 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679a74dc4701476354ea76978aceb95213a22bac76ab3b1e7ada196ccaf3e5c6`  
		Last Modified: Tue, 25 Feb 2025 02:13:08 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:808999355a46c7221a48f97155e22894b35c23ec5eb0a34f38a1867387f2f174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2977894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c387b4f49232a868136a62e4e45440a3189f69f82e7bfdc1642e3895375a49e`

```dockerfile
```

-	Layers:
	-	`sha256:cec6932aec7bcdc0671083ab0e803a7059d25d7970837dc2cd2615fe034c301d`  
		Last Modified: Tue, 25 Feb 2025 02:13:07 GMT  
		Size: 3.0 MB (2962077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:001cccfa7ee24e3fd3186b5bbe45baf150ab9ef259bdb1140fe47fc0d2920b57`  
		Last Modified: Tue, 25 Feb 2025 02:13:07 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:39d49e29c7f59ba36b36d3a708f567c4944b0ba2f515e0ce53f0181ec160e7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62378375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c9cf891a9e3ea1926020f7bc99bb704700fd2c016db112f2b0cb3248290a74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 01:38:07 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716ff6c04df2c3723828c67081c4bbf0570e39aca6d5eb80459e5fd5a996f422`  
		Last Modified: Tue, 04 Feb 2025 10:46:46 GMT  
		Size: 4.3 MB (4285199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e7909d8dd08b10c026da80a81f232836a694a7978e551d25e4308111881c4f`  
		Last Modified: Tue, 04 Feb 2025 10:46:47 GMT  
		Size: 32.5 MB (32534890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cabed5f34b24afbe841df1873058d593d6c85755465888873cb005c2825347`  
		Last Modified: Tue, 04 Feb 2025 10:46:46 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187a456276d746bff1d9c767e237174c505b2e9edfeedf4e3152fe4df2fda10b`  
		Last Modified: Tue, 04 Feb 2025 10:46:46 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6cd268cd13c3c0b449237086f7ce943300a9aa0324fff435ba498e120c9f98`  
		Last Modified: Tue, 04 Feb 2025 10:46:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:2d1be4bf816e07c936180ba09213ffa3060f95882ab7cff98befe417f24766b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2980238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2553ae8485363ca77b8194692ad67de2dc4ccd0259aa870f7b53a9bd559bc93`

```dockerfile
```

-	Layers:
	-	`sha256:189790983a81a75d958b903b70338e44294f26a12e87bd57616579175c108881`  
		Last Modified: Tue, 04 Feb 2025 10:46:46 GMT  
		Size: 3.0 MB (2964348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10276c740618024fddbe41e7de3daab94c370aeb989f4ee9dced7789e1de90a2`  
		Last Modified: Tue, 04 Feb 2025 10:46:46 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ac7ac31544364ff8415fe786f2a320070b777db11ad0b884e82c072c883e1960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66203547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57ade9a4191885173fd8604a95ad677fd406cd4446307a9f3f07988325bfdf5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b213a54c0de411b51596f071e4cee5f7cc900b5279db406dabb728224a4517de`  
		Last Modified: Tue, 25 Feb 2025 05:44:14 GMT  
		Size: 5.0 MB (5003609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81d6613706cf072f84eb50f2db4ad251f64f79ec55f27e9b81df2ab910d6269`  
		Last Modified: Tue, 25 Feb 2025 05:44:15 GMT  
		Size: 32.4 MB (32429551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1992cb5ccda6fbf96f52eed5abb45eaed60102b2f77f29c60e40c6638cfcd902`  
		Last Modified: Tue, 25 Feb 2025 05:44:14 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2827295707fe28a02483b35d82aeba0b0db2dbd99e46718a9f066dba628d2cf`  
		Last Modified: Tue, 25 Feb 2025 05:44:14 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ec792855beb8c1bc66162f9d1624f8508129707f437a2301697c8766b27d2b`  
		Last Modified: Tue, 25 Feb 2025 05:44:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8` - unknown; unknown

```console
$ docker pull chronograf@sha256:529cf32bc7b49634300f0574e923402f23937e1e974ed6b98c54245ea32b54cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2978238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74fc0de989669a6bb352899c06b55750312e3a7b27c15f20011504e328cda2a`

```dockerfile
```

-	Layers:
	-	`sha256:0bfad6453bcce52a9624e2783c4025bdd56fa0916b81b4d293b1a87ee6425a1a`  
		Last Modified: Tue, 25 Feb 2025 05:44:15 GMT  
		Size: 3.0 MB (2962326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77e09de9d8395a8c4159ff072ee0487532ca616f0af657db0fd5c4b1d503117`  
		Last Modified: Tue, 25 Feb 2025 05:44:14 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:830cefde62b7fa5d1e719c9cdbd90e36b6111165338d6a63589967af3b425932
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1bc656b7ebda40ceb3556472bac3163ab7b63970a38964aba666e23cab083110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23150080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1f3cf9f33249acb43998ce431a893a6196e54c6623a39388c922e747600326`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c39259f86321f91341426ea2b7c8164eb8c8a538841604f969c31abd195acba`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf003f24079392a7a29452383a6db1f26978c48f54533c79153b28b82b7257`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 294.4 KB (294385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb15ecadba26a5095f16beac190b0f35fa020ee3fff220c3243ebb39f58712a`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 19.2 MB (19204154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402cd540f74e77bd8181c883cf26fa3525fd15513ad005bc58b5bed6ddb9d248`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c299e5fdf7b7064f6b152ef78a715eefeff0a18c48c95e7a2b74b34bc318c7f5`  
		Last Modified: Fri, 14 Feb 2025 19:24:45 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ff2dde7922e46ced41d599cff59f593b600debe56130e43867bb3be500e704`  
		Last Modified: Fri, 14 Feb 2025 19:24:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:cdd0db3358b43541330dbf7e54517d4cbd7e2c4dfcdf798c5197cdc28507a544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 KB (246816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4af8a7ead9ebe09b9d15f6a3a39569c97af7c6664e752144193917be3f3928e`

```dockerfile
```

-	Layers:
	-	`sha256:41a2c152911589c4db3aec41c07d7ba26ba8320255380bc8e9f5dad25980a11b`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 229.9 KB (229904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ad8d123c697deeb31e83f6f288bbb9095d82109f9902675e157e8b88f35c2b`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:eeb0bebead600f40240994ac745c283bc988d016e1716c9a5a35acb47e6bbaa2
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
$ docker pull chronograf@sha256:21b2b2b00e46932b45a4c8e9ce25b6d49c1d9e235bb4e7eaedabeb8d9fd11518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69662843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61aa9448439ba648c132218c42951265b56aa8463881d8e31994492fa6878d91`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7d89f38058a1222576e243f9f2306447da4bbc11b0f11c25a69ac881374013`  
		Last Modified: Tue, 25 Feb 2025 02:13:08 GMT  
		Size: 5.0 MB (5020292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2e0a9cb53dc07668dd7a98ad67e01e0aec94d7ac7999246a01a83afdff9321`  
		Last Modified: Tue, 25 Feb 2025 02:13:08 GMT  
		Size: 34.4 MB (34364239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8dfc70ae99f41b36540e57ee090b72467dfb4e9acb681109f986ce33586727`  
		Last Modified: Tue, 25 Feb 2025 02:13:07 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b44e855431f0cfb8ccc7317c7ababd64bf5dc9a97251d63efb0de5456e28b1`  
		Last Modified: Tue, 25 Feb 2025 02:13:07 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679a74dc4701476354ea76978aceb95213a22bac76ab3b1e7ada196ccaf3e5c6`  
		Last Modified: Tue, 25 Feb 2025 02:13:08 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:808999355a46c7221a48f97155e22894b35c23ec5eb0a34f38a1867387f2f174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2977894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c387b4f49232a868136a62e4e45440a3189f69f82e7bfdc1642e3895375a49e`

```dockerfile
```

-	Layers:
	-	`sha256:cec6932aec7bcdc0671083ab0e803a7059d25d7970837dc2cd2615fe034c301d`  
		Last Modified: Tue, 25 Feb 2025 02:13:07 GMT  
		Size: 3.0 MB (2962077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:001cccfa7ee24e3fd3186b5bbe45baf150ab9ef259bdb1140fe47fc0d2920b57`  
		Last Modified: Tue, 25 Feb 2025 02:13:07 GMT  
		Size: 15.8 KB (15817 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:39d49e29c7f59ba36b36d3a708f567c4944b0ba2f515e0ce53f0181ec160e7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62378375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c9cf891a9e3ea1926020f7bc99bb704700fd2c016db112f2b0cb3248290a74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 01:38:07 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716ff6c04df2c3723828c67081c4bbf0570e39aca6d5eb80459e5fd5a996f422`  
		Last Modified: Tue, 04 Feb 2025 10:46:46 GMT  
		Size: 4.3 MB (4285199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e7909d8dd08b10c026da80a81f232836a694a7978e551d25e4308111881c4f`  
		Last Modified: Tue, 04 Feb 2025 10:46:47 GMT  
		Size: 32.5 MB (32534890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cabed5f34b24afbe841df1873058d593d6c85755465888873cb005c2825347`  
		Last Modified: Tue, 04 Feb 2025 10:46:46 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187a456276d746bff1d9c767e237174c505b2e9edfeedf4e3152fe4df2fda10b`  
		Last Modified: Tue, 04 Feb 2025 10:46:46 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6cd268cd13c3c0b449237086f7ce943300a9aa0324fff435ba498e120c9f98`  
		Last Modified: Tue, 04 Feb 2025 10:46:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:2d1be4bf816e07c936180ba09213ffa3060f95882ab7cff98befe417f24766b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2980238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2553ae8485363ca77b8194692ad67de2dc4ccd0259aa870f7b53a9bd559bc93`

```dockerfile
```

-	Layers:
	-	`sha256:189790983a81a75d958b903b70338e44294f26a12e87bd57616579175c108881`  
		Last Modified: Tue, 04 Feb 2025 10:46:46 GMT  
		Size: 3.0 MB (2964348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10276c740618024fddbe41e7de3daab94c370aeb989f4ee9dced7789e1de90a2`  
		Last Modified: Tue, 04 Feb 2025 10:46:46 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:ac7ac31544364ff8415fe786f2a320070b777db11ad0b884e82c072c883e1960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66203547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57ade9a4191885173fd8604a95ad677fd406cd4446307a9f3f07988325bfdf5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b213a54c0de411b51596f071e4cee5f7cc900b5279db406dabb728224a4517de`  
		Last Modified: Tue, 25 Feb 2025 05:44:14 GMT  
		Size: 5.0 MB (5003609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81d6613706cf072f84eb50f2db4ad251f64f79ec55f27e9b81df2ab910d6269`  
		Last Modified: Tue, 25 Feb 2025 05:44:15 GMT  
		Size: 32.4 MB (32429551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1992cb5ccda6fbf96f52eed5abb45eaed60102b2f77f29c60e40c6638cfcd902`  
		Last Modified: Tue, 25 Feb 2025 05:44:14 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2827295707fe28a02483b35d82aeba0b0db2dbd99e46718a9f066dba628d2cf`  
		Last Modified: Tue, 25 Feb 2025 05:44:14 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ec792855beb8c1bc66162f9d1624f8508129707f437a2301697c8766b27d2b`  
		Last Modified: Tue, 25 Feb 2025 05:44:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10` - unknown; unknown

```console
$ docker pull chronograf@sha256:529cf32bc7b49634300f0574e923402f23937e1e974ed6b98c54245ea32b54cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2978238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74fc0de989669a6bb352899c06b55750312e3a7b27c15f20011504e328cda2a`

```dockerfile
```

-	Layers:
	-	`sha256:0bfad6453bcce52a9624e2783c4025bdd56fa0916b81b4d293b1a87ee6425a1a`  
		Last Modified: Tue, 25 Feb 2025 05:44:15 GMT  
		Size: 3.0 MB (2962326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77e09de9d8395a8c4159ff072ee0487532ca616f0af657db0fd5c4b1d503117`  
		Last Modified: Tue, 25 Feb 2025 05:44:14 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:830cefde62b7fa5d1e719c9cdbd90e36b6111165338d6a63589967af3b425932
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:1bc656b7ebda40ceb3556472bac3163ab7b63970a38964aba666e23cab083110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23150080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1f3cf9f33249acb43998ce431a893a6196e54c6623a39388c922e747600326`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c39259f86321f91341426ea2b7c8164eb8c8a538841604f969c31abd195acba`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf003f24079392a7a29452383a6db1f26978c48f54533c79153b28b82b7257`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 294.4 KB (294385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb15ecadba26a5095f16beac190b0f35fa020ee3fff220c3243ebb39f58712a`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 19.2 MB (19204154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402cd540f74e77bd8181c883cf26fa3525fd15513ad005bc58b5bed6ddb9d248`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c299e5fdf7b7064f6b152ef78a715eefeff0a18c48c95e7a2b74b34bc318c7f5`  
		Last Modified: Fri, 14 Feb 2025 19:24:45 GMT  
		Size: 11.9 KB (11892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ff2dde7922e46ced41d599cff59f593b600debe56130e43867bb3be500e704`  
		Last Modified: Fri, 14 Feb 2025 19:24:45 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.8.10-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:cdd0db3358b43541330dbf7e54517d4cbd7e2c4dfcdf798c5197cdc28507a544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 KB (246816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4af8a7ead9ebe09b9d15f6a3a39569c97af7c6664e752144193917be3f3928e`

```dockerfile
```

-	Layers:
	-	`sha256:41a2c152911589c4db3aec41c07d7ba26ba8320255380bc8e9f5dad25980a11b`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 229.9 KB (229904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ad8d123c697deeb31e83f6f288bbb9095d82109f9902675e157e8b88f35c2b`  
		Last Modified: Fri, 14 Feb 2025 19:24:44 GMT  
		Size: 16.9 KB (16912 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:109e3aed0d61fa205fc5eb8f53e50aa270577abef804a98965cbf8afa874b08a
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
$ docker pull chronograf@sha256:617d9503c70be02e795cb3ccafcb2150920aae6239f6ed7b2795b083bff9a8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70310309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f83e8d47021fb2375c1e8f3d24713cfeab89073f353058b88fc8cdfc6441330`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b406cc6d2e25959a0a725a34016007dd01c0f9c76d128274e61c79d29206ed`  
		Last Modified: Tue, 25 Feb 2025 02:13:14 GMT  
		Size: 5.0 MB (5020286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ba41bff9cf5708961497b8f9e9755097d8267b2f3d69c543874f16df720d5c`  
		Last Modified: Tue, 25 Feb 2025 02:13:15 GMT  
		Size: 35.0 MB (35011702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686e4f2f872eabf07c6be6524bb22287dca00136419fef5be495892748a70ec9`  
		Last Modified: Tue, 25 Feb 2025 02:13:14 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31404322ae01d19891fcef6407116b611b531d819508474f6dc581bd3de57fe`  
		Last Modified: Tue, 25 Feb 2025 02:13:14 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40939a332735fcad390bd8c02fdec0f70d2eb246d09ac287762b1dc0699d83e7`  
		Last Modified: Tue, 25 Feb 2025 02:13:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:a5e6bf99cbcdba7470340ea4915125ac91668ace9c9aa10afe752c310e8b5cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bfb5c65fc63493694d7af204715ba441dd0e656ee7dd9070b3252b64b1c688`

```dockerfile
```

-	Layers:
	-	`sha256:de1c5ebeecb3bb76792b803ccb48410ce703aec1694228a12fe8b17114b11efd`  
		Last Modified: Tue, 25 Feb 2025 02:13:14 GMT  
		Size: 3.0 MB (2967287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ae625ade286031ab5e8c3ce1dac3bd84c9bddbfb622c51397221e2a588f4be`  
		Last Modified: Tue, 25 Feb 2025 02:13:14 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:623a388b86af575e572dcaea1cf7e10503f40da7241238ce1ba5222c125b05db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63154950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f17d7ff535ffc889b35f7efae3d30a3a0fe75bb1e016dcf8e78412ad5e0f65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 01:38:07 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716ff6c04df2c3723828c67081c4bbf0570e39aca6d5eb80459e5fd5a996f422`  
		Last Modified: Tue, 04 Feb 2025 10:46:46 GMT  
		Size: 4.3 MB (4285199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc730fd5f4030312463162690d082807b8a22f462a1c38d94d8df644fffcafdd`  
		Last Modified: Tue, 04 Feb 2025 10:47:18 GMT  
		Size: 33.3 MB (33311482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878932625049c91c7dc3844c4268464198176f0f3ae21c9a84f6f74af85eb65d`  
		Last Modified: Tue, 04 Feb 2025 10:47:17 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4319be39dc7ebacff2ab587515294234dde1e23cfa6f03bda53f561c3aea8ee1`  
		Last Modified: Tue, 04 Feb 2025 10:47:17 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6a903d6602d8d228eadaca3a4cdb08e5bd2ca84fbde8e3f0f0d219033036e2`  
		Last Modified: Tue, 04 Feb 2025 10:47:17 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:6c52e8676523b1021ef37cf7fe43b0423540305cc6c44fce95732e470cd0c456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37f2a14d35181feab28e8b7f96ba494c9f1d5c39a2c76a6c1cc7e7b3f5d4eaf`

```dockerfile
```

-	Layers:
	-	`sha256:e89a3a0497951ac87abad9e96ee6eb404049a8dbe5edc164efc2ae08e9b4f86f`  
		Last Modified: Tue, 04 Feb 2025 10:47:17 GMT  
		Size: 3.0 MB (2969558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aabfbf29b756831fe0c6c7f2c41201dfcfa7a696650314e0e319109f9bf77f5`  
		Last Modified: Tue, 04 Feb 2025 10:47:17 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:35751734683bf49e13fce055e037dbb3441e87a16a5a504c2398935704fc4918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66955653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b08ddc03a133487c53ff4eb0379457cda5630d826298fdcbd88ed5a805d8024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b213a54c0de411b51596f071e4cee5f7cc900b5279db406dabb728224a4517de`  
		Last Modified: Tue, 25 Feb 2025 05:44:14 GMT  
		Size: 5.0 MB (5003609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f2da43a92106770abecfb38b7d4fd1f80b6171c0a906f4bcc2e1a635156c58`  
		Last Modified: Tue, 25 Feb 2025 05:44:39 GMT  
		Size: 33.2 MB (33181654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f403fd914668d28fd6b0561de518e3552868bc85144358055d48b7af2f6e89ad`  
		Last Modified: Tue, 25 Feb 2025 05:44:37 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d135116bb3c403934e1a77a5aee96cdbb79eb6c290118ae5e34a0f4cdc923251`  
		Last Modified: Tue, 25 Feb 2025 05:44:38 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841e4404ce1ccd7cbbd7b96e2e5a93726bcc002ad915571e6c719b6dd24cd22c`  
		Last Modified: Tue, 25 Feb 2025 05:44:38 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9` - unknown; unknown

```console
$ docker pull chronograf@sha256:0b6ce0276581bb48cd44fcc25ad910656a6e7542fe6d59f12944b12ecd9374a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b328775e071f40fcb13d5670568550081aa3debf67382ec9e1308a87e7278a`

```dockerfile
```

-	Layers:
	-	`sha256:d39889195a5350a1944cc12e22cc68aa93a9c8cf79946c913fecfddfbc9482b6`  
		Last Modified: Tue, 25 Feb 2025 05:44:38 GMT  
		Size: 3.0 MB (2967536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1511d717c17c06bc1949db68604962ee4d1b855c701cab795ad6a1ecb2b244e3`  
		Last Modified: Tue, 25 Feb 2025 05:44:38 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:540ce018515beb499f291d9455b2a9d1c289f8fae572d53fd54246fd7e7146d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:a4dfb7641118d30a6585c108ec369459880e88c6faf92790e05d3593e3353a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23617935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c262c4b7eed1867c635b60b6ffc799536825070ed1596c83b1c42ad21c4105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de662ab890de5cb0e03103817de459544467d4b3f0784c60d26b56b9057ad500`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc476e87cc64ce09a8be67509b3baee59f88525efcf0dbb7aa18f0aeeb0823b`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 19.7 MB (19672009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:50d32d3aaaf4e53754ad80987dede42204c13fb95cb686e2c2513f3385048a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 KB (252025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0aafa46d648297defb395a6fbfbb62467880874da481dd27cd19da3182e2433`

```dockerfile
```

-	Layers:
	-	`sha256:4486aa18fc3114703709ddebe3fb35b7b024a9c27bc87effa33b6909ae7fe370`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 235.1 KB (235116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b34d12538bfcd1dd3e2b34c8aa09be9693afe86e4462d7341bee3cf95202f0`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:109e3aed0d61fa205fc5eb8f53e50aa270577abef804a98965cbf8afa874b08a
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
$ docker pull chronograf@sha256:617d9503c70be02e795cb3ccafcb2150920aae6239f6ed7b2795b083bff9a8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70310309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f83e8d47021fb2375c1e8f3d24713cfeab89073f353058b88fc8cdfc6441330`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b406cc6d2e25959a0a725a34016007dd01c0f9c76d128274e61c79d29206ed`  
		Last Modified: Tue, 25 Feb 2025 02:13:14 GMT  
		Size: 5.0 MB (5020286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ba41bff9cf5708961497b8f9e9755097d8267b2f3d69c543874f16df720d5c`  
		Last Modified: Tue, 25 Feb 2025 02:13:15 GMT  
		Size: 35.0 MB (35011702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686e4f2f872eabf07c6be6524bb22287dca00136419fef5be495892748a70ec9`  
		Last Modified: Tue, 25 Feb 2025 02:13:14 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31404322ae01d19891fcef6407116b611b531d819508474f6dc581bd3de57fe`  
		Last Modified: Tue, 25 Feb 2025 02:13:14 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40939a332735fcad390bd8c02fdec0f70d2eb246d09ac287762b1dc0699d83e7`  
		Last Modified: Tue, 25 Feb 2025 02:13:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:a5e6bf99cbcdba7470340ea4915125ac91668ace9c9aa10afe752c310e8b5cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bfb5c65fc63493694d7af204715ba441dd0e656ee7dd9070b3252b64b1c688`

```dockerfile
```

-	Layers:
	-	`sha256:de1c5ebeecb3bb76792b803ccb48410ce703aec1694228a12fe8b17114b11efd`  
		Last Modified: Tue, 25 Feb 2025 02:13:14 GMT  
		Size: 3.0 MB (2967287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ae625ade286031ab5e8c3ce1dac3bd84c9bddbfb622c51397221e2a588f4be`  
		Last Modified: Tue, 25 Feb 2025 02:13:14 GMT  
		Size: 15.8 KB (15810 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:623a388b86af575e572dcaea1cf7e10503f40da7241238ce1ba5222c125b05db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63154950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f17d7ff535ffc889b35f7efae3d30a3a0fe75bb1e016dcf8e78412ad5e0f65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 01:38:07 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716ff6c04df2c3723828c67081c4bbf0570e39aca6d5eb80459e5fd5a996f422`  
		Last Modified: Tue, 04 Feb 2025 10:46:46 GMT  
		Size: 4.3 MB (4285199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc730fd5f4030312463162690d082807b8a22f462a1c38d94d8df644fffcafdd`  
		Last Modified: Tue, 04 Feb 2025 10:47:18 GMT  
		Size: 33.3 MB (33311482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878932625049c91c7dc3844c4268464198176f0f3ae21c9a84f6f74af85eb65d`  
		Last Modified: Tue, 04 Feb 2025 10:47:17 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4319be39dc7ebacff2ab587515294234dde1e23cfa6f03bda53f561c3aea8ee1`  
		Last Modified: Tue, 04 Feb 2025 10:47:17 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6a903d6602d8d228eadaca3a4cdb08e5bd2ca84fbde8e3f0f0d219033036e2`  
		Last Modified: Tue, 04 Feb 2025 10:47:17 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:6c52e8676523b1021ef37cf7fe43b0423540305cc6c44fce95732e470cd0c456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37f2a14d35181feab28e8b7f96ba494c9f1d5c39a2c76a6c1cc7e7b3f5d4eaf`

```dockerfile
```

-	Layers:
	-	`sha256:e89a3a0497951ac87abad9e96ee6eb404049a8dbe5edc164efc2ae08e9b4f86f`  
		Last Modified: Tue, 04 Feb 2025 10:47:17 GMT  
		Size: 3.0 MB (2969558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aabfbf29b756831fe0c6c7f2c41201dfcfa7a696650314e0e319109f9bf77f5`  
		Last Modified: Tue, 04 Feb 2025 10:47:17 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:35751734683bf49e13fce055e037dbb3441e87a16a5a504c2398935704fc4918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66955653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b08ddc03a133487c53ff4eb0379457cda5630d826298fdcbd88ed5a805d8024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b213a54c0de411b51596f071e4cee5f7cc900b5279db406dabb728224a4517de`  
		Last Modified: Tue, 25 Feb 2025 05:44:14 GMT  
		Size: 5.0 MB (5003609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f2da43a92106770abecfb38b7d4fd1f80b6171c0a906f4bcc2e1a635156c58`  
		Last Modified: Tue, 25 Feb 2025 05:44:39 GMT  
		Size: 33.2 MB (33181654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f403fd914668d28fd6b0561de518e3552868bc85144358055d48b7af2f6e89ad`  
		Last Modified: Tue, 25 Feb 2025 05:44:37 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d135116bb3c403934e1a77a5aee96cdbb79eb6c290118ae5e34a0f4cdc923251`  
		Last Modified: Tue, 25 Feb 2025 05:44:38 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841e4404ce1ccd7cbbd7b96e2e5a93726bcc002ad915571e6c719b6dd24cd22c`  
		Last Modified: Tue, 25 Feb 2025 05:44:38 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4` - unknown; unknown

```console
$ docker pull chronograf@sha256:0b6ce0276581bb48cd44fcc25ad910656a6e7542fe6d59f12944b12ecd9374a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b328775e071f40fcb13d5670568550081aa3debf67382ec9e1308a87e7278a`

```dockerfile
```

-	Layers:
	-	`sha256:d39889195a5350a1944cc12e22cc68aa93a9c8cf79946c913fecfddfbc9482b6`  
		Last Modified: Tue, 25 Feb 2025 05:44:38 GMT  
		Size: 3.0 MB (2967536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1511d717c17c06bc1949db68604962ee4d1b855c701cab795ad6a1ecb2b244e3`  
		Last Modified: Tue, 25 Feb 2025 05:44:38 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:540ce018515beb499f291d9455b2a9d1c289f8fae572d53fd54246fd7e7146d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:a4dfb7641118d30a6585c108ec369459880e88c6faf92790e05d3593e3353a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23617935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c262c4b7eed1867c635b60b6ffc799536825070ed1596c83b1c42ad21c4105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de662ab890de5cb0e03103817de459544467d4b3f0784c60d26b56b9057ad500`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69641bcb67c77b895509abb75bf637ce2b76f0acdd981fd282b113d82c04c619`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 294.4 KB (294383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc476e87cc64ce09a8be67509b3baee59f88525efcf0dbb7aa18f0aeeb0823b`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 19.7 MB (19672009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29450f6d74de26216b10dc587e69dd4443992a6aea3c7b424c7aaad08ceef29`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 12.2 KB (12235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e84d9f6956c08b6776f1b3db99e0226246d044677f2e4cf470051da809c34e`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 11.9 KB (11893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030349c6370852b4bfb957d5c0dc77ca8ab49cfd26485c0b053651d825d6caf9`  
		Last Modified: Fri, 14 Feb 2025 19:24:49 GMT  
		Size: 238.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:1.9.4-alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:50d32d3aaaf4e53754ad80987dede42204c13fb95cb686e2c2513f3385048a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 KB (252025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0aafa46d648297defb395a6fbfbb62467880874da481dd27cd19da3182e2433`

```dockerfile
```

-	Layers:
	-	`sha256:4486aa18fc3114703709ddebe3fb35b7b024a9c27bc87effa33b6909ae7fe370`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 235.1 KB (235116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b34d12538bfcd1dd3e2b34c8aa09be9693afe86e4462d7341bee3cf95202f0`  
		Last Modified: Fri, 14 Feb 2025 19:24:48 GMT  
		Size: 16.9 KB (16909 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:d87e9a66df76dc2810442c6e52641e1f2df44d01d89f0c0c8ace7ee6de51dbbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:af46818df7f83a2ca358b3eb5f9317d68f8fb62299552df033d19ffb496ae0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31815096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9abcd8a6e187c12d41c913290917fed4516e1d543d9dcc2369ec95a2bbd73c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S chronograf &&     adduser -S chronograf -G chronograf &&     mkdir -m 0750 -p /var/lib/chronograf &&     chown chronograf:chronograf /var/lib/chronograf # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a49d50f1fe51a05325ae98d8bf9a879090b6be2b3527e6d11e59f960bdc93b7`  
		Last Modified: Fri, 14 Feb 2025 19:25:03 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361c594e3185bd08a55bb1bd9df81da69ae214a31a898c88bbfe9c942cb898a0`  
		Last Modified: Fri, 14 Feb 2025 19:25:04 GMT  
		Size: 296.5 KB (296499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f24eb5e953df43a31ec34d2b56d21a2c8cbbd486fcf0c69bf4c62ba2cf88cbb`  
		Last Modified: Fri, 14 Feb 2025 19:25:05 GMT  
		Size: 27.9 MB (27866993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf04d6dc2c59aa8ba5db19eae81f35471a84ac4f3294c76637f9a487fe496d47`  
		Last Modified: Fri, 14 Feb 2025 19:25:03 GMT  
		Size: 12.2 KB (12238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d6b0cde41f5740d49b8b7c41868028d6382d2751fe1a8057d0eb8b1122b0e0`  
		Last Modified: Fri, 14 Feb 2025 19:25:04 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652ea0b93c690d604c1f573af1ecb8451a18b6e8e825f678e4c2555df428f549`  
		Last Modified: Fri, 14 Feb 2025 19:25:04 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:alpine` - unknown; unknown

```console
$ docker pull chronograf@sha256:f7de0febfd6ddaf2ae32475727aa5806ff9254e253dc394f13a1e7d3965d90b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 KB (259450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0309720039e98d687cd49690b5b488d6e559d3736b87e0574422f03edd646db1`

```dockerfile
```

-	Layers:
	-	`sha256:27346ddfdfe4f4c0fc322b5de26cd7a216d974e4b609edbddd1dcaa51912afb6`  
		Last Modified: Fri, 14 Feb 2025 19:25:03 GMT  
		Size: 241.6 KB (241595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df79c104cbf58b736286d9972f51bb0074cc375c0bc55a4502f790fe4004478`  
		Last Modified: Fri, 14 Feb 2025 19:25:03 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:906f96320927a2cc1e18f2b13a25eec484635517485b2efc6074f564bd4602cb
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
$ docker pull chronograf@sha256:d8da46c45bbf4bd0233862e4e6c5ea3fe1e44b269bfc3adc4c9835515a2d68a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83336809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4b93152730951fc0a9dbbe459d10f98e2540e8d32411fc007e110349445c99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf4cc51ed963533bf134fc8a749b38d22fa512655c12a1ffa334511f7855bc2`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 7.9 MB (7875453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ec1ace7271a4d2e30062b834eeec24c82e5c1ad8e654d66f84b2ed5e3f1da5`  
		Last Modified: Tue, 25 Feb 2025 03:21:51 GMT  
		Size: 47.2 MB (47217579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c9a5ec5e92cece3ed0b6e36df99d0db435a77b0073273b2abb5c8ee2b9467`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f7aece400805a0b9f01aeff8371e20e5e94e6defb3b7bafaeb6ce70e9a40b3`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35f3ceb3a7710dabc099b27d711340f1973547771283dd8c59056a015f90c9c`  
		Last Modified: Tue, 25 Feb 2025 03:21:51 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:95c623a5c5d8b1b37515b7f948b2c08e827dc3cda6e27df34e780cb9d7c36d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a93a4b45f3e8c1f66c5fdafa7012770dfe37d4cdf8b00d0c70112adb99a789`

```dockerfile
```

-	Layers:
	-	`sha256:8ec4c32fbc96aaccb9a4ee61fa383f6667e3a2cab094516480ab751b286fdc17`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 2.7 MB (2703879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ce4bc83763ddf12872e270840e11bc59de9ea05777a529690dfa6b194a9a2b5`  
		Last Modified: Tue, 25 Feb 2025 03:21:50 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:88720ca505bfb08c74f4ceb1bb1aba6cde492fdcac7046603b2f011a84107c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fc2fb831a0ea15181cc5095ac14d0b7f24ca9b9e780b114b6efdf3c79bccf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cc7c361314024427e46f49ca0282aad7c7e1c19e195d10077e345573507b56`  
		Last Modified: Tue, 04 Feb 2025 10:48:05 GMT  
		Size: 6.5 MB (6497872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6cf5468b4e77edddf9b77021e98d83564ca5e44d38fffb2aba4f385562d0c6`  
		Last Modified: Tue, 04 Feb 2025 10:48:06 GMT  
		Size: 44.3 MB (44276279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df4d3bd9618dd31da4448a675205925bb539ddd136533f180d0c85668fdf11f`  
		Last Modified: Tue, 04 Feb 2025 10:48:04 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08d3e3c8ed5226ce823000b1a5b22cc1043c1bf6cc8fb121e2d64f591e402e5`  
		Last Modified: Tue, 04 Feb 2025 10:48:05 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082c93a0a6d68e759d05627b419cdbadd5c4c1f378ae68e2b3a1d70e4f1974b8`  
		Last Modified: Tue, 04 Feb 2025 10:48:05 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:062394e35a9237b5417145333219d7ca7d1b7140d82c1d6fd206202542ef59a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1153fa859ac40437c90717b2a11c8f758035eaaa7616057249db83fa8aefd24d`

```dockerfile
```

-	Layers:
	-	`sha256:06e80d01af57e5254ba8cac2ef064e8e41c67d40c82c76ae26ba6a4009ee6e63`  
		Last Modified: Tue, 04 Feb 2025 10:48:05 GMT  
		Size: 2.7 MB (2706158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba3bd0b60d93272f7e1bc61a85ba78c258b47fdcb5a8b570810fec9a060215b`  
		Last Modified: Tue, 04 Feb 2025 10:48:04 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:19624f2cf9bcadf070e04067581b2af0c9012d68168282a4e15a3a81f9efcbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80695516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f134edb6d33471cc442b9981a8f8cc87aef85c728f3463faf79898dfe273a7e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9c56777cdffdd5ca319eb018920d2e1c639be4e586bbe214e9067e145ec574`  
		Last Modified: Tue, 25 Feb 2025 05:45:10 GMT  
		Size: 7.7 MB (7652099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829f59d2de5ebc9eb3ba9a1162eca3708b86788efcf9f772038cbaedc1a3c5b0`  
		Last Modified: Tue, 25 Feb 2025 05:45:11 GMT  
		Size: 45.0 MB (44970527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b362ab190fa4d97f9a102ebab0beb5f09fce46ef41f48ce0d5862d78ae6cb4`  
		Last Modified: Tue, 25 Feb 2025 05:45:09 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4de6a654ea82d86a37134ae7ac84b946086660bd8feeed721e495f52095079`  
		Last Modified: Tue, 25 Feb 2025 05:45:09 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ce86954af7d4055352afb5a5534ef502a134de846887d85197fe6c77753b8`  
		Last Modified: Tue, 25 Feb 2025 05:45:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:0292b8508bd7b9503dc7cfb82b3e675a1a97bbf02222db05b28d7135d7b8d2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0adf99ae95e8ce3215b16017d6aa59dafc602c28b94ea91d0fd6fa50fb225c2`

```dockerfile
```

-	Layers:
	-	`sha256:a3b44361dd57918558a21ffd78a86337eb65ff10432211e762f92135915acf8a`  
		Last Modified: Tue, 25 Feb 2025 05:45:10 GMT  
		Size: 2.7 MB (2704152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b2bbb5f880bd581294211f5b785fbbae45eb64c20a23d03209835e00950dec`  
		Last Modified: Tue, 25 Feb 2025 05:45:09 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
