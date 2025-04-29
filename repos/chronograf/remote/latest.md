## `chronograf:latest`

```console
$ docker pull chronograf@sha256:f6ef7852b2257d0e7756589757627a50d2bb6ce74c4abf3c7e4297483f52b7f8
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
$ docker pull chronograf@sha256:d992d8064ea3aad5c61f05876d3d5f9b27f9caf4853f85c70115ff5b4cc7ae47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76025160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da52e8ccf76be4f48112c327593ba48cc696024c71fad43e6ae8b1126d10724c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97cc1bc73cdd53d1fb65b54eb2237cb2d74423ba085e2b4becb0d0fec7905be`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 6.5 MB (6497913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44517418a9729926f5d635549a4bd6176f13585afd47adb69f7c8b08e74c693a`  
		Last Modified: Tue, 29 Apr 2025 03:42:02 GMT  
		Size: 45.6 MB (45564703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5462df3243fd46d86ee7086f625bec52780ef4a05deaa42a8e4083e43f8907bf`  
		Last Modified: Tue, 29 Apr 2025 03:42:00 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d817a3e3afb21bf13b393479698fe8c14f39f2e3b20100e747706b51f9ccd6e`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103414f6d083444387facc3936ec4c26348ad1954d8a891d00fa696bf2469258`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:c424dca1169ea1980d8fe4891c7075b2692db626aa001bc8823714a7922df094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab36315c728813f16e98f9c535baaad3f4a8addd707f1171e03623d893f4dafd`

```dockerfile
```

-	Layers:
	-	`sha256:76c614e1be50a565a7207409c707c416355ea43389084da3c9088bc6b51a6bae`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 2.7 MB (2706470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eafd7093a3f3afb7cf09e97668195e911eb6927ef0f6699fe685e894611f0791`  
		Last Modified: Tue, 29 Apr 2025 03:42:01 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:45bd113eb85e7c27fedf83a7a9313e66d29cdc60dc9604f04b8da0e89567a04a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82763754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf23023139d2a5bba31fefbde296786407516e54bd44429fe5e3517c7627f3da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687d6d5f2d0622b294a8ce4c8f55da85356ba61e9a9ddecaa09b12c45f5dc71b`  
		Last Modified: Tue, 29 Apr 2025 01:50:04 GMT  
		Size: 7.7 MB (7652116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d52f1039bbb6fba3a0e7fc09bf372afbfc17d60d1bcd56c4659f0045214bbcf`  
		Last Modified: Tue, 29 Apr 2025 01:50:05 GMT  
		Size: 47.0 MB (47020557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9028c3e134f78f6ced2c1fc90dfc47fdb06ef46ccb86f256ce6507c93d0dacc`  
		Last Modified: Tue, 29 Apr 2025 01:50:03 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb7f61774f9814fa36e7925e9db6154efe72e897177610f87539565ae136d52`  
		Last Modified: Tue, 29 Apr 2025 01:50:03 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98fc839e4715c63a63e686672b0df5d47e4674fffc5f611891d705038ce7b65`  
		Last Modified: Tue, 29 Apr 2025 01:50:04 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:2b906c51825ebb95a9dc2c20a92a02cd282237452e5dd08e795b8fed5cb95a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a4bb964b36817b761823beb95bd7a1cf2d7be749bc8ac3013b70003e81696a`

```dockerfile
```

-	Layers:
	-	`sha256:aa39a818f83b457c77e9ed04b7dcdee0288b378f1c5bdaf38944c955f3dcb32b`  
		Last Modified: Tue, 29 Apr 2025 01:50:04 GMT  
		Size: 2.7 MB (2704446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b99ea6e4585f33d2ac9e33b0ef61919a71762bf46928bc59fb30ae003b16e0`  
		Last Modified: Tue, 29 Apr 2025 01:50:03 GMT  
		Size: 16.2 KB (16234 bytes)  
		MIME: application/vnd.in-toto+json
