## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:8be1035a39d9743ca23ec4f94a22c31db46fbe2fd94a7bcffb2239af4588827b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `liquibase:alpine` - linux; amd64

```console
$ docker pull liquibase@sha256:194f67b46611cc879ca26bd7528bb4671a90fd0bdd8a93f36d5ef7c3e9ddf64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229944668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b98e68a0a8e93ee6c5a9f18fe870e521d7f75d1e718f65bb8f37b6d93b539b`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
WORKDIR /liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LIQUIBASE_VERSION=4.30.0
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_VERSION=0.2.8
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 07 Nov 2024 14:28:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
USER liquibase:liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b03a6387a3ba379fbb55ac9c5567650d7d4264450e893a69f91d6284e2f1a`  
		Last Modified: Tue, 12 Nov 2024 02:14:17 GMT  
		Size: 986.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f18cf4ba1ae771f468d2871c87428349e06f60948ae13a9c1942888a6a6fb7`  
		Last Modified: Tue, 12 Nov 2024 02:14:18 GMT  
		Size: 62.6 MB (62619305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a76506919288088e48db967883ef03476eeb82d0dbaf48aa3d4ba59f172c8f8`  
		Last Modified: Tue, 12 Nov 2024 02:14:19 GMT  
		Size: 160.5 MB (160459050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8c5fd7554ccbbd0fbdb844b2a966a004ff8517d44dde1d8a0a9cc20cdfd7f5`  
		Last Modified: Tue, 12 Nov 2024 02:14:17 GMT  
		Size: 3.2 MB (3240740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35084c1c8c5123543705a5006bd8953075abdbd3cf508c0e409fef87b45cd53f`  
		Last Modified: Tue, 12 Nov 2024 02:14:17 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46e13aa3bae53748deb18d69d402405d2bae29eda8bf427774dab867a5d323b`  
		Last Modified: Tue, 12 Nov 2024 02:14:18 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:49a757763f040466b12fdcb8e226a8877f51a314b0e3a0528dfe1a288aeb9cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.5 KB (399518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb55911363c3764ba079c17c2b0e30a797f8130c3e8314f35e6ba46fbff71f78`

```dockerfile
```

-	Layers:
	-	`sha256:d8c5cb662d83822ad36be08504ef455be3e6b0a56ac833531607a3245e148932`  
		Last Modified: Tue, 12 Nov 2024 02:14:17 GMT  
		Size: 378.3 KB (378254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a6b7a0b216bb037cdf4c9f4b9e159cb402077f7fef94c0758ebf8024328fa60`  
		Last Modified: Tue, 12 Nov 2024 02:14:17 GMT  
		Size: 21.3 KB (21264 bytes)  
		MIME: application/vnd.in-toto+json

### `liquibase:alpine` - linux; arm64 variant v8

```console
$ docker pull liquibase@sha256:270ec5290acf31e89e16c6fb27cc1958b0daf17a700b8a37592bd73f4a1d0698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229859775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e84fa4d09e44048b50989485c4df918c5e7819d81320f53a7b3261f9b8d571c`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
RUN addgroup --gid 1001 liquibase &&     adduser --disabled-password --uid 1001 --ingroup liquibase liquibase &&     mkdir /liquibase && chown liquibase /liquibase # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
RUN apk add --no-cache openjdk17-jre-headless bash # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
WORKDIR /liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LIQUIBASE_VERSION=4.30.0
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d
RUN set -x &&     apk add --no-cache --virtual .fetch-deps wget &&     wget -q -O liquibase-${LIQUIBASE_VERSION}.tar.gz "https://github.com/liquibase/liquibase/releases/download/v${LIQUIBASE_VERSION}/liquibase-${LIQUIBASE_VERSION}.tar.gz" &&     echo "$LB_SHA256 *liquibase-${LIQUIBASE_VERSION}.tar.gz" | sha256sum -c - &&     tar -xzf liquibase-${LIQUIBASE_VERSION}.tar.gz &&     rm liquibase-${LIQUIBASE_VERSION}.tar.gz &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/liquibase /usr/local/bin/liquibase &&     ln -s /liquibase/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh &&     liquibase --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_VERSION=0.2.8
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200
# Thu, 07 Nov 2024 14:28:00 GMT
ARG LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
# Thu, 07 Nov 2024 14:28:00 GMT
# ARGS: LIQUIBASE_VERSION=4.30.0 LB_SHA256=184ffd609518091da42d6cd75e883b4f6ff1763cce8883e95fc99f7f05ca262d LPM_VERSION=0.2.8 LPM_SHA256=ad46e7f0ca67e39ddbf1435c0bd2879be8a43340c7b627a2da45c07787574200 LPM_SHA256_ARM=2a2e46f2260f46ccd39f487dca161b4e04d97664160925c5e415bd9b54a23e1a
RUN mkdir /liquibase/bin &&     apk add --no-cache --virtual .fetch-deps wget unzip &&     arch="$(apk --print-arch)" &&     case "$arch" in       x86_64)   DOWNLOAD_ARCH=""  ;;       aarch64)  DOWNLOAD_ARCH="-arm64" && LPM_SHA256=$LPM_SHA256_ARM  ;;       *) echo >&2 "error: unsupported architecture '$arch'" && exit 1 ;;     esac && wget -q -O lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip "https://github.com/liquibase/liquibase-package-manager/releases/download/v${LPM_VERSION}/lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" &&     echo "$LPM_SHA256 *lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip" | sha256sum -c - &&     unzip lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip -d bin/ &&     rm lpm-${LPM_VERSION}-linux${DOWNLOAD_ARCH}.zip &&     apk del --no-network .fetch-deps &&     ln -s /liquibase/bin/lpm /usr/local/bin/lpm &&     lpm --version # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
ENV LIQUIBASE_HOME=/liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENV DOCKER_LIQUIBASE=true
# Thu, 07 Nov 2024 14:28:00 GMT
COPY docker-entrypoint.sh ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
COPY liquibase.docker.properties ./ # buildkit
# Thu, 07 Nov 2024 14:28:00 GMT
USER liquibase:liquibase
# Thu, 07 Nov 2024 14:28:00 GMT
ENTRYPOINT ["/liquibase/docker-entrypoint.sh"]
# Thu, 07 Nov 2024 14:28:00 GMT
CMD ["--help"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e6ac71992bf291867c2507881911c4061b04c54a93f7e2beaec48bea06f829`  
		Last Modified: Thu, 07 Nov 2024 17:59:01 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1499c3188073e498b692507679e7a5cab359218af5fd77b2241df66e4ab44f5`  
		Last Modified: Thu, 07 Nov 2024 17:59:04 GMT  
		Size: 62.3 MB (62319669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bf49cf4b1f4fe1d7c997ad35fb720f6288671f6bc545711bba1a32de9ccde2`  
		Last Modified: Thu, 07 Nov 2024 17:59:06 GMT  
		Size: 160.5 MB (160458979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818c1f922cd3d04a175abb3a69638c70aab74fe2c66c0e42c0900206e63ea0bd`  
		Last Modified: Thu, 07 Nov 2024 17:59:02 GMT  
		Size: 3.0 MB (2991813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660abfac3b136d4c9e15ff7338387bc7b642288b30e632988a4d43c6c4f15ac6`  
		Last Modified: Thu, 07 Nov 2024 17:59:02 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d329f5d539eaede4ab7921e3931739a26a88ace1c9aa8e2ad3078179d2bf26`  
		Last Modified: Thu, 07 Nov 2024 17:59:03 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:17bbf4e21a4672aed94dec05405f0ea98d08b0f524dc29bcb50172d2b5ecc33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 KB (398720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36a72c74fce5f785ba0eb5310a8889dfe0f1166b25413b35c73460a88183297`

```dockerfile
```

-	Layers:
	-	`sha256:5bdc276e1c686d0511f1fc13b6bfbe2a72a1bff61a1b0b47e6de1e680a5a06db`  
		Last Modified: Thu, 07 Nov 2024 17:59:02 GMT  
		Size: 377.5 KB (377500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bc74e2eed68cb1aed11378697ffd08b7ba27bd914e5d89955d6b66e45c2c21`  
		Last Modified: Thu, 07 Nov 2024 17:59:01 GMT  
		Size: 21.2 KB (21220 bytes)  
		MIME: application/vnd.in-toto+json
