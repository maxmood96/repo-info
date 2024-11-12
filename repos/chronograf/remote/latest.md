## `chronograf:latest`

```console
$ docker pull chronograf@sha256:18200f03814c9cb448ed2604d3593447dda4056c967b2f12bcac3d1e22222d33
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
$ docker pull chronograf@sha256:cbb2398ca1e9c1e79905f76a6f508c0b84e124ed19d8bd1ef329113df6bd0554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84245436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef430dd9bd942ea971170a9ad41a7b86bf2b0bd54963f64e172414e8bbf7b6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1224e7e2d3fcfa467dc4f217326c057f4f2dd7300e13ef8f9e857ce39d3b4a1a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 7.9 MB (7875383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156341f7966c50570025c0aa511f08d25d6323a659a42aed5dbf0d667f59476a`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 47.2 MB (47217593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc833227a91630f06fdbd4aa78c70728725f847e7108c30819c0dd7b1bcc2f1`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942d7292f5707350b55e75b6962c10f687a2f79cd6897f52184d0d756f3640af`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59b128af6ad42b6a2e4237a81330a24126fa56928cb1282247f5a0b2e934cce`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:d283d9166d23e08f8f2ecab79a9506abca9aca59180582cf53a41af1716e8570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dff9e10e6a0907fdc037209f268bd74095409b257480933f04b1cad3729d68f`

```dockerfile
```

-	Layers:
	-	`sha256:3e81168bed413e125218f95a0a4120c7164a7f95a704ffc312fa47035416659c`  
		Last Modified: Tue, 12 Nov 2024 02:38:20 GMT  
		Size: 2.7 MB (2706777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da14de2590a125267c353c750cc1c061c345a17e9a5da32b3651a9e5dc1c2ec`  
		Last Modified: Tue, 12 Nov 2024 02:38:19 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:45f678c553711d2db70d58535b9794b3ad28d4d84f59d79a55f54f272827789b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75517507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902c66527b2d96a1b1c3a0c88cbe54876f2dbd2a511a4c5fcb504a5a7838819d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
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
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6550685acd063dc6cce640c6f10c1dfac73cc458f5b8b19ec449579a08ab1401`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 6.5 MB (6497842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d9638c811aa475e3ef3dd738ebb9839a72c09623ca60283c170c2babda7f6`  
		Last Modified: Tue, 12 Nov 2024 16:06:27 GMT  
		Size: 44.3 MB (44276286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a1e4b1ee7537b61421076ee24fd717c335f249c42420356c0539a1f6899b9`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f869afcceefe33812d97f686e429f4d846795d1cd930495accf77f409f2506`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3c728782b2eeb8dd6001ebe7610861c011ebe762fcafbd576160449ed7bcb0`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:b310981b0390adbddba27b5ffa275d03002a50389474dc02ab36dd4e8c5b9ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621bb400573b68da87ad02e9d81f7ae8827c3ae22bd31fdb1d8e42dd93d4bd88`

```dockerfile
```

-	Layers:
	-	`sha256:a7b6c982a3a1c70e9c895470939fb5317eb615837e1c7b10cdac4960efaf1f79`  
		Last Modified: Tue, 12 Nov 2024 16:06:26 GMT  
		Size: 2.7 MB (2709073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bda2b8c1e48a2737a6f3b881aea6e27ed53014051c50ff50e1613800ad657f8`  
		Last Modified: Tue, 12 Nov 2024 16:06:25 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:55b50dea2f2137ce54f443d25b2abfeae47947ee823b2f08388d6eda47d37d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81804433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22992893a7f71a7317d6d6a37c09a42bd342530c32f54b834b877cf5e2c5ab0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["bash"]
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5311845117483a02d47c2a837750ed149b17f6ad45451557d3edf3b2361b65d1`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 7.7 MB (7652059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f1f751938fc31cf6a008145a362d6ef94697cef76dd2dcd3a8bb9c969ba5f5`  
		Last Modified: Tue, 12 Nov 2024 11:20:19 GMT  
		Size: 45.0 MB (44970549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa6316747afbf579f3ace66f98703019df3b8b3d7083660d7e299b89205fc7b`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ad95dbffe5e0b91bcdb9f70a444a19e3b49b1f65366caee2370468e451a8ff`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522a008c121d0b587cccc212b8a01b87d0893dd790681b545ce2777b6031c31f`  
		Last Modified: Tue, 12 Nov 2024 11:20:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:8005aae06ed87a042209bcd22fd86c390c027dfefd1ab385657eb9c4ff90b1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57bfeb1040a95763cafa6296c548fbc9a7c9d83b29c2a572fdd51e3e6aa28ce`

```dockerfile
```

-	Layers:
	-	`sha256:519a1a88095896e326f6589cb0448391ad985d186bae96a9b24df79476d03244`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 2.7 MB (2707049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e694a5a62286326bdb76d6c68673eb2b6e170f2c7e26eb255c0224ddbc61be`  
		Last Modified: Tue, 12 Nov 2024 11:20:18 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
