## `chronograf:latest`

```console
$ docker pull chronograf@sha256:d5746c708d06fe73e16df492741fd33c671682414bf57fbf203a15f23ef2ee6e
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
$ docker pull chronograf@sha256:a758a48b485dc6da1f4f6d36dd094f10397d3f3bff8939abc67fba9ebc5eec8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85366465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e559e3373078577bf4dc35d628a05ddd412394acc207d6b83ff53c8d3f0fb1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198ec8ec6518903e7d9a626735c9cb03e20fde751af60582b21a9d3eb70038a7`  
		Last Modified: Tue, 01 Jul 2025 02:26:08 GMT  
		Size: 7.9 MB (7878155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351e7ee6b54eff7b83faf43b8e504271a78d394c00bdce817ee7617c940da705`  
		Last Modified: Tue, 01 Jul 2025 06:09:38 GMT  
		Size: 49.2 MB (49233700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1435ca05117cf534df06299ca7280b03e3664dbbdb697c2c17d9b5b1a0903de`  
		Last Modified: Tue, 01 Jul 2025 02:26:00 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a6d5038a74c5e386557c6d1c2ca85626da0477aa4469155576156ddd7bcbe2`  
		Last Modified: Tue, 01 Jul 2025 02:25:54 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc0cdd94276467241fae2c2a069c058de49ff5211c42a6c7d45bb7659b1a68d`  
		Last Modified: Tue, 01 Jul 2025 02:25:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:88016d7baacd27f683d41bf900c3fd65d682f20b1d4966162317e1b174c58c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f114d5875241d6444b1eae0650dd4cd6f473621f4d3dc980c67910cb65899b60`

```dockerfile
```

-	Layers:
	-	`sha256:4c046e61f0c3f30dc7c4de0f1a809be40820a3073b607fa5f873cf2e6e30ac34`  
		Last Modified: Tue, 01 Jul 2025 06:38:19 GMT  
		Size: 2.9 MB (2851833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e36b371fcfdde5b2f8aa47c84c5f1d95e7b1b4f9be6ea7a5656d8e59aabca55`  
		Last Modified: Tue, 01 Jul 2025 06:38:20 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:e42b4289f36d7b4085a075323a59bb531859e40350527fd237a8d9e801f9488c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76033792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42fe14f21c54e0ba3e624a591fcdc6cfed61c1def4b0e28d87bb55d300088ba5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dfc0a8a409bd51a4b4334be5151c5410537b3b6148cd687158e6d65169d0dc`  
		Last Modified: Tue, 01 Jul 2025 09:02:26 GMT  
		Size: 6.5 MB (6505837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0ed00c0141d5bfd93cc1c5beecc92e07518b2b5eb214c9889f5b86ca7d594c`  
		Last Modified: Tue, 01 Jul 2025 09:02:30 GMT  
		Size: 45.6 MB (45564733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01639c4b639968328780bb744f17b46006ac04cfd461c6540ea182a45dc267b0`  
		Last Modified: Tue, 01 Jul 2025 09:02:25 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8878d5e70b8c4d9d51f673f1d922e99b11ba002ecf5901b2c601e5024b4ebce`  
		Last Modified: Tue, 01 Jul 2025 09:02:25 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc86dc6ef11723e6556a48c8b61f53891b77a42f444976643071bba9042527e`  
		Last Modified: Tue, 01 Jul 2025 09:02:25 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:670c394cec33f207d719ec0ddba217e445a275947e891ccb40c8ea61e60fd3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fcfab9af5342b3afcac9275a13d3355e35a3e0830573db3a2fc11f23d4ef45`

```dockerfile
```

-	Layers:
	-	`sha256:fcebcf866dea6d54ca649207888298edb9e910e161336347b6d109073a42baca`  
		Last Modified: Tue, 01 Jul 2025 09:38:24 GMT  
		Size: 2.9 MB (2854130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31def213389075d6cd0c19aeec66b20bd8838da5e98f73ab8a291e59f8fef29`  
		Last Modified: Tue, 01 Jul 2025 09:38:25 GMT  
		Size: 16.2 KB (16208 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:17bf5ea90ec8c8c11f1ef4f8f32803539be1869fda98ec0df79b7a65e8fac0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82784125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6addffc23a73f6bae699f9b2368aed9f9577492f33efc436f026ee7c51f07d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cd88ad45b66a6263ad455de1551bbd545eb3ba0afaebe431ddf692605642dc`  
		Last Modified: Tue, 01 Jul 2025 06:55:24 GMT  
		Size: 7.7 MB (7661432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90875276557fd3b3bc1c3ac9d9258a29144368ca4f313832bcb5d97c040b1b6`  
		Last Modified: Tue, 01 Jul 2025 09:42:52 GMT  
		Size: 47.0 MB (47020563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbe56a4ace0d419126047816df0b716bd230357ae9a5bf407e3c3dba7b4f6c2`  
		Last Modified: Tue, 01 Jul 2025 06:55:15 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eabb67396eb88c393d497b8d084ea1b763d78d36679c08970cc3eb60de0da10`  
		Last Modified: Tue, 01 Jul 2025 06:55:14 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5d2d1fd6b7244086b69c12049b6f2de1f8f6c0e15ca04c289c7e3d33241705`  
		Last Modified: Tue, 01 Jul 2025 06:55:15 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:95631d310b9515566de8138e4c3f15295705336ca0d7836d1158edc9c197717e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2868340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9188661a47419049e353669d42885745ac474fb04d936e11fd6fba33672ff66c`

```dockerfile
```

-	Layers:
	-	`sha256:2477cc5d110f35cc783c73fea3a2bf7463a5613b218251f473c1c4206aeb10f2`  
		Last Modified: Tue, 01 Jul 2025 09:38:29 GMT  
		Size: 2.9 MB (2852106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70ebd3847c83f6fd97a90ba965756fb747d7ce424f77f2ac97cf550dd2903aeb`  
		Last Modified: Tue, 01 Jul 2025 09:38:30 GMT  
		Size: 16.2 KB (16234 bytes)  
		MIME: application/vnd.in-toto+json
