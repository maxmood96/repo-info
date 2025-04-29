## `chronograf:latest`

```console
$ docker pull chronograf@sha256:b2da07a9765e11701c538cd612853d2bbb4e10c1838f8aa8a48bbee0d3f9545c
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
$ docker pull chronograf@sha256:7dd16daa289079744a3485a5dc1f9c4d1b42fecd1c091ac8c1d060658407316a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85361259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01bfcfdf38b10aa4664a875462af00c39c7f6e34a93c9736540134e2bc239b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d948a6e444038248d3837d2e8bb8e9f5e347ce21fe67592ddea6c9636511d6f4`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 7.9 MB (7875415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7b2f54616466e283cb5bdb7c5192c06c8a43136da9bb6c0c13ab2018dad9d9`  
		Last Modified: Mon, 28 Apr 2025 21:55:45 GMT  
		Size: 49.2 MB (49233737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ded7601090ccd78e1baae3c56e7ad4c6b68a4d47cb778c98699674602e64b2`  
		Last Modified: Mon, 28 Apr 2025 21:55:43 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf9cdfbc80b60b5c327f81fec79b30bfd2450f2f23ed002d7d5e63ed4733f33`  
		Last Modified: Mon, 28 Apr 2025 21:55:43 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c7ee215395492598d52c252485f37e9039a61a48d0d0fb41af03be3a62d516`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:ba793e2f75ea28a7dbd2d1b3b0d61d7cf41106200aa00db12355a6592706cd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00aafccdf15c39046c13083c2fff37f46e3cc03c62ecdc4dbab730297fdd6639`

```dockerfile
```

-	Layers:
	-	`sha256:f1be7e3349428f3b74e918ce10522157cd3695f6a43cecb7e501641bee8edb82`  
		Last Modified: Mon, 28 Apr 2025 21:55:43 GMT  
		Size: 2.7 MB (2704173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1d5b909ceaa65802b09fa72f781272a332d157a79826d4971e5fddf194bc4e`  
		Last Modified: Mon, 28 Apr 2025 21:55:43 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:ce1ab18d90859be8271c4a87ec74aedd6adc3b7499977a642d2dcaf548eec373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76024855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140b94103f42d77d978d56dc3578322205b407929cd0a93c07ef83ec238266fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fb76179215a5134f33d423465e52f924db51a65e77a13aaaa0906ca6ef60ab`  
		Last Modified: Wed, 16 Apr 2025 16:54:17 GMT  
		Size: 6.5 MB (6497851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47e2b558eef58fa3d69cb99cdc22bf14f33644d9edc7af213e2a11d6fbc2b5b`  
		Last Modified: Wed, 16 Apr 2025 16:54:18 GMT  
		Size: 45.6 MB (45564665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4731500f9d63cd2ccb8e808cb027be01c0ae957ef5bca4abbbba4f409f158d1`  
		Last Modified: Wed, 16 Apr 2025 16:54:16 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d736ea9195596dcff970c010401024b1fa6d08d7735d531397b7947728e07ccf`  
		Last Modified: Wed, 16 Apr 2025 16:54:16 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd5519384c2608149ded636386e5e1826dc90d168b869caae8b04aa9c84957`  
		Last Modified: Wed, 16 Apr 2025 16:54:17 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:9330eae97faf97068cb594acecae642faaa8e0f164be04f68ec622a1c3381cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541d2eda69ef8de54d6dd3c256fcf07eefbd48aea5d2545de72fb7f082ca1491`

```dockerfile
```

-	Layers:
	-	`sha256:0a29c3c77403a003235e7d3da6268c83c10bb28e0f6266517958cc8a2db5fd1d`  
		Last Modified: Wed, 16 Apr 2025 16:54:16 GMT  
		Size: 2.7 MB (2706470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ef827f9e766d02f2b907010daac35f154bedac4df75b57f2839a894d89d035`  
		Last Modified: Wed, 16 Apr 2025 16:54:16 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:cacb8d93d39eac3ef294ab0e646c4a94b5939b4c424a17b032b8d826bd22a3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82763420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca9f5c2c9498337d054221ba94aa362a6ea8c6d39a760ffd5974e24eba27f48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202be231ced71b6fd1e66eb40ae03460c636f4b29f14a93251e9a8f8a734ebfa`  
		Last Modified: Wed, 16 Apr 2025 16:54:09 GMT  
		Size: 7.7 MB (7652065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc514df859781433bb3090ee8c17f16ef7f489acbf4616322e8693c6b174b1b`  
		Last Modified: Wed, 16 Apr 2025 16:54:11 GMT  
		Size: 47.0 MB (47020557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16743ec3eac1c0644d033d155881d331826c2d658f7b5530388c10c36cbffa7e`  
		Last Modified: Wed, 16 Apr 2025 16:54:09 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a44a21ad95336a14c87b1a6fbb89115ad18c5dc227751d82f953a1f363275c8`  
		Last Modified: Wed, 16 Apr 2025 16:54:09 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18780e107bb85c41331e9aeea7142a1308dce3be47a43088c94309af6bc6a56`  
		Last Modified: Wed, 16 Apr 2025 16:54:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:1ec366d47e8e38cdbc99118e1feec40e51a649124a911d7cb0bbb8657804af1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a7d1752ece36943a37d4aab5266fe307c2d4e46bb6eb838e09ffb369dce150`

```dockerfile
```

-	Layers:
	-	`sha256:c99657385a1870146bd06ad4c086ebed5fb354d07dc99e44862f7c23a280158b`  
		Last Modified: Wed, 16 Apr 2025 16:54:09 GMT  
		Size: 2.7 MB (2704446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4776b2021bc699f92ef9dda8a5081e6cc6deee2bdaeefe9f7842236913492da`  
		Last Modified: Wed, 16 Apr 2025 16:54:09 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
