## `liquibase:alpine`

```console
$ docker pull liquibase@sha256:01eeb8ce80cd94993e938240c3da6d167cbbf49a6b2e499401e52b8c7a8c817b
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
$ docker pull liquibase@sha256:428692f03e6712cc9528796a13eb788f75c4ce3edb3372338f9e830ec3dda49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229859839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a788d956019b026dcc3aab1ee7f06b9d41bcaf0f4544b1e3c2a58bba9c9a9ce4`
-	Entrypoint: `["\/liquibase\/docker-entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9240be39543c27c00ea4a3ef48f30a4ecef8372b630188f1975e90ff11fc6c5`  
		Last Modified: Tue, 12 Nov 2024 13:18:15 GMT  
		Size: 985.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90442792f200d10c62146680e56dd13ff998509e0bf75b5d2be27edc06cf7d9b`  
		Last Modified: Tue, 12 Nov 2024 13:18:17 GMT  
		Size: 62.3 MB (62319674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a6d839668bf2a174e0cd0f32f9549041117d20411d261ec2b7b7223e8710d9`  
		Last Modified: Tue, 12 Nov 2024 13:18:19 GMT  
		Size: 160.5 MB (160458970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb82ea186cd12f5ce86ffecde70a339ccb7bd2cee27b8fd3de533b927bec8e4`  
		Last Modified: Tue, 12 Nov 2024 13:18:15 GMT  
		Size: 3.0 MB (2991805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecee69a5ac21bb17cb1134fbe5c528eaf37c4b09a92682315db35e233ebd37a`  
		Last Modified: Tue, 12 Nov 2024 13:18:16 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2303085d51c094315add257fde6833a4af782af02d2b894c46e3accff2e58af`  
		Last Modified: Tue, 12 Nov 2024 13:18:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `liquibase:alpine` - unknown; unknown

```console
$ docker pull liquibase@sha256:16b71a7f2bcd22198564998bef125bcc4035e4b08a0392d95e175286c9055eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.9 KB (398901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563eb8db5b3054d8e905a5b4c1fdebaca3317bfae55b924ee0a5276b46443874`

```dockerfile
```

-	Layers:
	-	`sha256:76b09bd22679784511899ca58ff5f6c10ebe517028888b95789f983bf4ead389`  
		Last Modified: Tue, 12 Nov 2024 13:18:15 GMT  
		Size: 377.5 KB (377500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f59fe77b340b91adc033de18f868d6e384a2aceb3567164f465e6b7b2f4bd8e`  
		Last Modified: Tue, 12 Nov 2024 13:18:15 GMT  
		Size: 21.4 KB (21401 bytes)  
		MIME: application/vnd.in-toto+json
