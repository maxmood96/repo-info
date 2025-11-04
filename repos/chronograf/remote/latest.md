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
