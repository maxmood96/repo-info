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
