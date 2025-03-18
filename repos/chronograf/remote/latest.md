## `chronograf:latest`

```console
$ docker pull chronograf@sha256:00cc5d190f70aba10c74715878372f38cc0f79a36f0f6455284bd777c909b102
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
$ docker pull chronograf@sha256:beb82792350bc91b4298018ba676c4ea0da54774f670939bd3c3d1e318436b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83322571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15296119c26269d8f84a0188feedceed710c16e227f09e1191263d4e882bf307`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4b150170885078d0820ef08ed1490836dde71e78f4d6826be3d1414fde7e63`  
		Last Modified: Mon, 17 Mar 2025 23:14:14 GMT  
		Size: 7.9 MB (7875439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76636bdf02578fda9e9747008a4444307e0f2062a1f9500a761ba870c1710a66`  
		Last Modified: Mon, 17 Mar 2025 23:14:15 GMT  
		Size: 47.2 MB (47217796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd493e654a622a3953f6fa01234fd3f6bdafc67205f955c931b008ce47f0e2`  
		Last Modified: Mon, 17 Mar 2025 23:14:13 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931954bcbc1785fa7518a16a3683b7bb9c5812c8889dd12a2a72aa21b6ed7f97`  
		Last Modified: Mon, 17 Mar 2025 23:14:13 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd459ad2fdb45a448adc4451d0febae6827b37c745afa791d218edf92caa41f6`  
		Last Modified: Mon, 17 Mar 2025 23:14:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:a2607d5cdc896c36767428c5bc6e5732a1efcc55bc652c31cbb5a7e10dffcf14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3911abbb85006aa13ca9da7273fb4dd0a98c3a1a4875214b42fc52bf9c366cb6`

```dockerfile
```

-	Layers:
	-	`sha256:56cb695f92a00400c5fb2775ad068a3270e3e6c7a24c329d179437a446cd8781`  
		Last Modified: Mon, 17 Mar 2025 23:14:14 GMT  
		Size: 2.7 MB (2703891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dbd5befe91534de03a3526eedafc5f30f7c98be3b3d4fb21905fa42acd49aec`  
		Last Modified: Mon, 17 Mar 2025 23:14:13 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:865496a9fb5845d7309e16a8da5534c449c2d5f45a3a6927229311470ff67a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74718378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c236a8cb9c914dd61bc87be54f12f4bb2bf35eb00b2c5b1d0039bbb7f1bf86`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed579ce411082527eba1a0711949162bc8d9db83a6f8e76a14eb64a1583d6c3`  
		Last Modified: Tue, 25 Feb 2025 07:21:02 GMT  
		Size: 6.5 MB (6497894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787ec40aa0152fac3138d724d445189657085f6fb82bdd7c7042cfc874873603`  
		Last Modified: Tue, 25 Feb 2025 07:21:03 GMT  
		Size: 44.3 MB (44276278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72743ea8bdcd60e42e23bb02c6a9ba9e6f5b2ccb36a4578b1a3dee07ef4b4802`  
		Last Modified: Tue, 25 Feb 2025 07:21:01 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1c1cc7ee8b1421c1a5f04900b86a9e97447be012bc1ba4ed91334d843df2b2`  
		Last Modified: Tue, 25 Feb 2025 07:21:01 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea968afdf7cebf5ab77ac07a71cc7e64c1a88177af89e4f25a478def6a56d55`  
		Last Modified: Tue, 25 Feb 2025 07:21:02 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:2d0c7c93147c4919016a86f4c9744e7b2c80f34a06ad50c39681c88dbe4860f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e51993ad95f0b8b69afbcf72f41451d17c07b1689b3c05617d9cd7a962270b7`

```dockerfile
```

-	Layers:
	-	`sha256:a90ca73ebb36de1b65c528f3d2777ae2e7c7608fbf591a246e364da2c16a5319`  
		Last Modified: Tue, 25 Feb 2025 07:21:01 GMT  
		Size: 2.7 MB (2706176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc64f21a3ebafdbef117c65898c0f96e7ecc5503c505bbca13d828bfb830b480`  
		Last Modified: Tue, 25 Feb 2025 07:21:01 GMT  
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
