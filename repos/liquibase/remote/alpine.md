## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:d8d955818809fb91c2085dcfea78b033673bc37c7505e0e43ff12fb650f3b0b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:fbfebab6b53ebbec5f81fdfd4cbfaf586dd409ba823bd6a43a11697c6c6a3c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228895340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f0c74c1b66f84f0fc6211dce3c9400b67cc842a8fa8952f92cdeacd86a2147`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 13 Sep 2024 07:37:36 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
WORKDIR /liquibase
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LIQUIBASE_VERSION=4.29.2
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LB_SHA256=1d017a206a95ab3076a52f660679c2d80b9f2174942cb0715e35d53931e20ee9
# Fri, 13 Sep 2024 07:37:36 GMT
# ARGS: LIQUIBASE_VERSION=4.29.2 LB_SHA256=1d017a206a95ab3076a52f660679c2d80b9f2174942cb0715e35d53931e20ee9
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LPM_VERSION=0.2.8
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 13 Sep 2024 07:37:36 GMT
# ARGS: LIQUIBASE_VERSION=4.29.2 LB_SHA256=1d017a206a95ab3076a52f660679c2d80b9f2174942cb0715e35d53931e20ee9 LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 13 Sep 2024 07:37:36 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
USER liquibase:liquibase
# Fri, 13 Sep 2024 07:37:36 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 13 Sep 2024 07:37:36 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5968dad0c5cd11a1dee26f10ff16e5b41d50d6f3d9f206ef6f6cad5d30d1e44a`  
		Last Modified: Sat, 19 Oct 2024 01:00:16 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41864b028bfc744d8c900562c033aba6ab8bc1159e3c20e5b8308843096c44e4`  
		Last Modified: Sat, 19 Oct 2024 01:00:17 GMT  
		Size: 62.6 MB (62569517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03669f15c7771ef019bf7c4adad4e61009471faa0896dc92ee695c518eae4c71`  
		Last Modified: Sat, 19 Oct 2024 01:00:18 GMT  
		Size: 159.5 MB (159459672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547696384ce3bb9b391a1773f5050f6f77273f6a26cdd20fd63963cac5eac930`  
		Last Modified: Sat, 19 Oct 2024 01:00:16 GMT  
		Size: 3.2 MB (3240676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b07e40482a3e324ae7dcf0ff483dce5337b0179fd2d18bdb75d18ab92ef11a3`  
		Last Modified: Sat, 19 Oct 2024 01:00:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e6d3b220e0ede1553c4aff874c35c91bce9cd15fc58f1fb0e5de0b8530a185`  
		Last Modified: Sat, 19 Oct 2024 01:00:17 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:cf4a97ff56096437023cd86d5266aa8b45d7cbf098c0e24c8d67d3f8b598d9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.3 KB (398270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b10bc2c76a6f66d4fb806b977fb05df61858d51c2e9305032685c38a712d8ff`

```dockerfile
```

-	Layers:
	-	`sha256:d0a96d1d867d8f3ec45647ab8f6be33de323cac9247495e2bb3bf5aa83245f05`  
		Last Modified: Sat, 19 Oct 2024 01:00:16 GMT  
		Size: 377.3 KB (377297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556cc695717e6c5fc4fa965e1fbca86a74506567416ef8a836ea49e2f42a67d5`  
		Last Modified: Sat, 19 Oct 2024 01:00:16 GMT  
		Size: 21.0 KB (20973 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:b72dec730ff3d22b2435e22c5b08b58d52a1ba2fce991a4443cbed5d39b8f6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228817009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace713e637d0a0f1e7754192f04a40174ada546c190142d1789d995ebba80945`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 13 Sep 2024 07:37:36 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
WORKDIR /liquibase
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LIQUIBASE_VERSION=4.29.2
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LB_SHA256=1d017a206a95ab3076a52f660679c2d80b9f2174942cb0715e35d53931e20ee9
# Fri, 13 Sep 2024 07:37:36 GMT
# ARGS: LIQUIBASE_VERSION=4.29.2 LB_SHA256=1d017a206a95ab3076a52f660679c2d80b9f2174942cb0715e35d53931e20ee9
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LPM_VERSION=0.2.8
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Fri, 13 Sep 2024 07:37:36 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Fri, 13 Sep 2024 07:37:36 GMT
# ARGS: LIQUIBASE_VERSION=4.29.2 LB_SHA256=1d017a206a95ab3076a52f660679c2d80b9f2174942cb0715e35d53931e20ee9 LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
ENV LIQUIBASE_HOME=/liquibase
# Fri, 13 Sep 2024 07:37:36 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
COPY liquibase.docker.properties ./ # buildkit
# Fri, 13 Sep 2024 07:37:36 GMT
USER liquibase:liquibase
# Fri, 13 Sep 2024 07:37:36 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Fri, 13 Sep 2024 07:37:36 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a8694a6259b1e7ea95fe314fe1083207604eaafcbc0195a76799abb955d3a`  
		Last Modified: Sat, 19 Oct 2024 01:22:44 GMT  
		Size: 984.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428d94fa3adc6b7af74f52a20ed221b195f85b39e0364194e3dbfc93363021cf`  
		Last Modified: Sat, 19 Oct 2024 01:22:46 GMT  
		Size: 62.3 MB (62276294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddfef378d47d17e337043503df96d76c36d8037ed55782a5ab79874bcadaab9`  
		Last Modified: Sat, 19 Oct 2024 01:22:48 GMT  
		Size: 159.5 MB (159459631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f9e6916136a890596d86156f31468fe4c36b7abe5adc576e06b6f13541c53c`  
		Last Modified: Sat, 19 Oct 2024 01:22:44 GMT  
		Size: 3.0 MB (2991772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1906879160e6aa32e0519667cd0d2a0f168164fda6e44e7d90d4460e2f465f7`  
		Last Modified: Sat, 19 Oct 2024 01:22:45 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3239dca5a5a5d6b8df97c3ebec1eb5f179f99c54b4604a45c9236df408fd9e`  
		Last Modified: Sat, 19 Oct 2024 01:22:46 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:046dfc612f5ceb2ff8f8da08d646e12db00f0344fc6271067680cc111a434624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.6 KB (397647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58032b38f14f009ffb8491632ef91215e6fd018e9b38e22216566fd8aa0b4bec`

```dockerfile
```

-	Layers:
	-	`sha256:df4e1f185da8b654b5ca8a66796c2e898eca65619374febafa008df77b013964`  
		Last Modified: Sat, 19 Oct 2024 01:22:44 GMT  
		Size: 376.5 KB (376543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f14ce01c09ce94be140592c2f4c8bba745f91a1970241cc253c1019a197f8d`  
		Last Modified: Sat, 19 Oct 2024 01:22:44 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json
