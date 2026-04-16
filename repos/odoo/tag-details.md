<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260409`](#odoo170-20260409)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260409`](#odoo180-20260409)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260409`](#odoo190-20260409)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:0c14e0288c6dc35e214a482f19b563094a8a034d07aeeb12a6708477fa3df1b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:37454b83fe5427e495351da3a0f670c3bc8fb3f8df00bd5c2207b70336b3fd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.0 MB (609979042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b46d6ef4dd0b09fec7b42a67f6512c19aa9fb7fa3e6d8471d65be3f0511ff96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:47:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:47:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:47:51 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:47:51 GMT
ARG TARGETARCH=amd64
# Wed, 15 Apr 2026 20:47:51 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:47:59 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:47:59 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:47:59 GMT
ENV ODOO_VERSION=17.0
# Wed, 15 Apr 2026 20:47:59 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:47:59 GMT
ARG ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
# Wed, 15 Apr 2026 20:49:00 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:01 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:01 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b792cf214513b806f1921fe1615ca32e2595106076dbd6fdc42b4597a56cdb`  
		Last Modified: Wed, 15 Apr 2026 20:50:18 GMT  
		Size: 233.8 MB (233832228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28322a3a623eb93531ab3e7cf86b079fdf5b8cfab536702eae4bfece05943cb`  
		Last Modified: Wed, 15 Apr 2026 20:50:09 GMT  
		Size: 2.6 MB (2603690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae72417b33283cf7564b7a1537ed852849de2fe317487fade38b94d613d711`  
		Last Modified: Wed, 15 Apr 2026 20:50:09 GMT  
		Size: 481.6 KB (481560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4bb5d39ddc007d47f2d9e85c169e26006b03a18e154d16d975f7ccc65dc1cc`  
		Last Modified: Wed, 15 Apr 2026 20:50:21 GMT  
		Size: 343.3 MB (343322633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097fa12a5ad6cddf45ad0cfc5205c2daca15fbd92f9548f09912bc3c4ad713b5`  
		Last Modified: Wed, 15 Apr 2026 20:50:10 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974267a9fc815990c9eb23766363d2bf1e0c8abc0588787c0e5a8743a467123d`  
		Last Modified: Wed, 15 Apr 2026 20:50:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518d47d2d9e00b5d9421d1fc7f14055b2d7e40713bbe844f2d88a9fb5d6a44d3`  
		Last Modified: Wed, 15 Apr 2026 20:50:12 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1159e37cdb2b79b4463c5230edd923eb2d81ff4fbe06e7d857e1a53ce3da50`  
		Last Modified: Wed, 15 Apr 2026 20:50:12 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:00881c0ef375441a91dc30f1e007cc935f5153dff27fcd6835b36af355c55d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42900171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c74b68181f5654a29704488b6e9f9dd9f7c929ec8645b060c3bde2658a8295`

```dockerfile
```

-	Layers:
	-	`sha256:39d5902285c2c0cae77a4f47ba86389144d0fbed54d47a985a1fa4ac4c597226`  
		Last Modified: Wed, 15 Apr 2026 20:50:12 GMT  
		Size: 42.9 MB (42873380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c67f625f471ac77f19e966ef298a0cdea3b1b35c63e97d805703bf54c975c6`  
		Last Modified: Wed, 15 Apr 2026 20:50:09 GMT  
		Size: 26.8 KB (26791 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6989d5c3753132dec96948dd6661340edb5f60e6a464a3e9110c01dd106dd7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.8 MB (604845623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90aec3c793f98497fde42fa53ce77f7cc638243ffbcc27804a54c607cc018b77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:47:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:47:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:47:58 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:47:58 GMT
ARG TARGETARCH=arm64
# Wed, 15 Apr 2026 20:47:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:06 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:07 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:07 GMT
ENV ODOO_VERSION=17.0
# Wed, 15 Apr 2026 20:48:07 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:07 GMT
ARG ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
# Wed, 15 Apr 2026 20:49:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:14 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b4b2cb6300c46351523b916b9745ef3880937fbb2541e09d3745f114d0316a`  
		Last Modified: Wed, 15 Apr 2026 20:50:45 GMT  
		Size: 231.2 MB (231203323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83768cdac59134061edd2cae53ee80da03cc7706a892b5c698ee4d8b86e18738`  
		Last Modified: Wed, 15 Apr 2026 20:50:37 GMT  
		Size: 2.6 MB (2598114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1753b8f99757a45895a0aabd5e1639ff3925f5120a31cbf2c1c9f05f8726e916`  
		Last Modified: Wed, 15 Apr 2026 20:50:37 GMT  
		Size: 481.6 KB (481610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36918b6e085496f8143e1a1e8be1612e163cc6706f534869a8fbd5d07ab15cb7`  
		Last Modified: Wed, 15 Apr 2026 20:50:47 GMT  
		Size: 343.0 MB (342953593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142df133284adbf5f883aeb4d99d5a09dbf2052cfdcd52dff79fea83a9427ce2`  
		Last Modified: Wed, 15 Apr 2026 20:50:38 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b61c0fbaaff2aa8e0ddf3b85c6eddbb22195bc6dc763b70a2d0d4f92b8ae236`  
		Last Modified: Wed, 15 Apr 2026 20:50:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c81e3858a3cf4342de427e1e2b807877f3fbca71f46a9eaffcf2a9e4e75ddd`  
		Last Modified: Wed, 15 Apr 2026 20:50:39 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a83506ccbc728b6eff01bc8f34e3497d8d8cbcc5995549fbac356719e04da0`  
		Last Modified: Wed, 15 Apr 2026 20:50:40 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c3989242efe607c236c1c70adfd45aef85e9c4a6ea48bde174d3612932904796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42906831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef42ed1d69960d6d5cc4a12ddd7a12b74be4e1d613a36e7a8b8adc6cb03a9c6`

```dockerfile
```

-	Layers:
	-	`sha256:b115290eaf75491eacf3a47bdc11cd5dd973e24aa355cad13f00446662a12da2`  
		Last Modified: Wed, 15 Apr 2026 20:50:39 GMT  
		Size: 42.9 MB (42879887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e0cc904c876f694f70f1883347a3516c563bcf9836abb56406b8f44d240ede`  
		Last Modified: Wed, 15 Apr 2026 20:50:36 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:0c14e0288c6dc35e214a482f19b563094a8a034d07aeeb12a6708477fa3df1b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:37454b83fe5427e495351da3a0f670c3bc8fb3f8df00bd5c2207b70336b3fd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.0 MB (609979042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b46d6ef4dd0b09fec7b42a67f6512c19aa9fb7fa3e6d8471d65be3f0511ff96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:47:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:47:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:47:51 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:47:51 GMT
ARG TARGETARCH=amd64
# Wed, 15 Apr 2026 20:47:51 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:47:59 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:47:59 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:47:59 GMT
ENV ODOO_VERSION=17.0
# Wed, 15 Apr 2026 20:47:59 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:47:59 GMT
ARG ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
# Wed, 15 Apr 2026 20:49:00 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:01 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:01 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b792cf214513b806f1921fe1615ca32e2595106076dbd6fdc42b4597a56cdb`  
		Last Modified: Wed, 15 Apr 2026 20:50:18 GMT  
		Size: 233.8 MB (233832228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28322a3a623eb93531ab3e7cf86b079fdf5b8cfab536702eae4bfece05943cb`  
		Last Modified: Wed, 15 Apr 2026 20:50:09 GMT  
		Size: 2.6 MB (2603690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae72417b33283cf7564b7a1537ed852849de2fe317487fade38b94d613d711`  
		Last Modified: Wed, 15 Apr 2026 20:50:09 GMT  
		Size: 481.6 KB (481560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4bb5d39ddc007d47f2d9e85c169e26006b03a18e154d16d975f7ccc65dc1cc`  
		Last Modified: Wed, 15 Apr 2026 20:50:21 GMT  
		Size: 343.3 MB (343322633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097fa12a5ad6cddf45ad0cfc5205c2daca15fbd92f9548f09912bc3c4ad713b5`  
		Last Modified: Wed, 15 Apr 2026 20:50:10 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974267a9fc815990c9eb23766363d2bf1e0c8abc0588787c0e5a8743a467123d`  
		Last Modified: Wed, 15 Apr 2026 20:50:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518d47d2d9e00b5d9421d1fc7f14055b2d7e40713bbe844f2d88a9fb5d6a44d3`  
		Last Modified: Wed, 15 Apr 2026 20:50:12 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1159e37cdb2b79b4463c5230edd923eb2d81ff4fbe06e7d857e1a53ce3da50`  
		Last Modified: Wed, 15 Apr 2026 20:50:12 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:00881c0ef375441a91dc30f1e007cc935f5153dff27fcd6835b36af355c55d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42900171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c74b68181f5654a29704488b6e9f9dd9f7c929ec8645b060c3bde2658a8295`

```dockerfile
```

-	Layers:
	-	`sha256:39d5902285c2c0cae77a4f47ba86389144d0fbed54d47a985a1fa4ac4c597226`  
		Last Modified: Wed, 15 Apr 2026 20:50:12 GMT  
		Size: 42.9 MB (42873380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c67f625f471ac77f19e966ef298a0cdea3b1b35c63e97d805703bf54c975c6`  
		Last Modified: Wed, 15 Apr 2026 20:50:09 GMT  
		Size: 26.8 KB (26791 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6989d5c3753132dec96948dd6661340edb5f60e6a464a3e9110c01dd106dd7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.8 MB (604845623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90aec3c793f98497fde42fa53ce77f7cc638243ffbcc27804a54c607cc018b77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:47:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:47:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:47:58 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:47:58 GMT
ARG TARGETARCH=arm64
# Wed, 15 Apr 2026 20:47:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:06 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:07 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:07 GMT
ENV ODOO_VERSION=17.0
# Wed, 15 Apr 2026 20:48:07 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:07 GMT
ARG ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
# Wed, 15 Apr 2026 20:49:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:14 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b4b2cb6300c46351523b916b9745ef3880937fbb2541e09d3745f114d0316a`  
		Last Modified: Wed, 15 Apr 2026 20:50:45 GMT  
		Size: 231.2 MB (231203323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83768cdac59134061edd2cae53ee80da03cc7706a892b5c698ee4d8b86e18738`  
		Last Modified: Wed, 15 Apr 2026 20:50:37 GMT  
		Size: 2.6 MB (2598114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1753b8f99757a45895a0aabd5e1639ff3925f5120a31cbf2c1c9f05f8726e916`  
		Last Modified: Wed, 15 Apr 2026 20:50:37 GMT  
		Size: 481.6 KB (481610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36918b6e085496f8143e1a1e8be1612e163cc6706f534869a8fbd5d07ab15cb7`  
		Last Modified: Wed, 15 Apr 2026 20:50:47 GMT  
		Size: 343.0 MB (342953593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142df133284adbf5f883aeb4d99d5a09dbf2052cfdcd52dff79fea83a9427ce2`  
		Last Modified: Wed, 15 Apr 2026 20:50:38 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b61c0fbaaff2aa8e0ddf3b85c6eddbb22195bc6dc763b70a2d0d4f92b8ae236`  
		Last Modified: Wed, 15 Apr 2026 20:50:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c81e3858a3cf4342de427e1e2b807877f3fbca71f46a9eaffcf2a9e4e75ddd`  
		Last Modified: Wed, 15 Apr 2026 20:50:39 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a83506ccbc728b6eff01bc8f34e3497d8d8cbcc5995549fbac356719e04da0`  
		Last Modified: Wed, 15 Apr 2026 20:50:40 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c3989242efe607c236c1c70adfd45aef85e9c4a6ea48bde174d3612932904796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42906831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef42ed1d69960d6d5cc4a12ddd7a12b74be4e1d613a36e7a8b8adc6cb03a9c6`

```dockerfile
```

-	Layers:
	-	`sha256:b115290eaf75491eacf3a47bdc11cd5dd973e24aa355cad13f00446662a12da2`  
		Last Modified: Wed, 15 Apr 2026 20:50:39 GMT  
		Size: 42.9 MB (42879887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e0cc904c876f694f70f1883347a3516c563bcf9836abb56406b8f44d240ede`  
		Last Modified: Wed, 15 Apr 2026 20:50:36 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260409`

```console
$ docker pull odoo@sha256:0c14e0288c6dc35e214a482f19b563094a8a034d07aeeb12a6708477fa3df1b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260409` - linux; amd64

```console
$ docker pull odoo@sha256:37454b83fe5427e495351da3a0f670c3bc8fb3f8df00bd5c2207b70336b3fd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.0 MB (609979042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b46d6ef4dd0b09fec7b42a67f6512c19aa9fb7fa3e6d8471d65be3f0511ff96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:47:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:47:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:47:51 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:47:51 GMT
ARG TARGETARCH=amd64
# Wed, 15 Apr 2026 20:47:51 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:47:59 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:47:59 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:47:59 GMT
ENV ODOO_VERSION=17.0
# Wed, 15 Apr 2026 20:47:59 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:47:59 GMT
ARG ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
# Wed, 15 Apr 2026 20:49:00 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:01 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:01 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:01 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b792cf214513b806f1921fe1615ca32e2595106076dbd6fdc42b4597a56cdb`  
		Last Modified: Wed, 15 Apr 2026 20:50:18 GMT  
		Size: 233.8 MB (233832228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28322a3a623eb93531ab3e7cf86b079fdf5b8cfab536702eae4bfece05943cb`  
		Last Modified: Wed, 15 Apr 2026 20:50:09 GMT  
		Size: 2.6 MB (2603690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae72417b33283cf7564b7a1537ed852849de2fe317487fade38b94d613d711`  
		Last Modified: Wed, 15 Apr 2026 20:50:09 GMT  
		Size: 481.6 KB (481560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4bb5d39ddc007d47f2d9e85c169e26006b03a18e154d16d975f7ccc65dc1cc`  
		Last Modified: Wed, 15 Apr 2026 20:50:21 GMT  
		Size: 343.3 MB (343322633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097fa12a5ad6cddf45ad0cfc5205c2daca15fbd92f9548f09912bc3c4ad713b5`  
		Last Modified: Wed, 15 Apr 2026 20:50:10 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974267a9fc815990c9eb23766363d2bf1e0c8abc0588787c0e5a8743a467123d`  
		Last Modified: Wed, 15 Apr 2026 20:50:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518d47d2d9e00b5d9421d1fc7f14055b2d7e40713bbe844f2d88a9fb5d6a44d3`  
		Last Modified: Wed, 15 Apr 2026 20:50:12 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1159e37cdb2b79b4463c5230edd923eb2d81ff4fbe06e7d857e1a53ce3da50`  
		Last Modified: Wed, 15 Apr 2026 20:50:12 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:00881c0ef375441a91dc30f1e007cc935f5153dff27fcd6835b36af355c55d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42900171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c74b68181f5654a29704488b6e9f9dd9f7c929ec8645b060c3bde2658a8295`

```dockerfile
```

-	Layers:
	-	`sha256:39d5902285c2c0cae77a4f47ba86389144d0fbed54d47a985a1fa4ac4c597226`  
		Last Modified: Wed, 15 Apr 2026 20:50:12 GMT  
		Size: 42.9 MB (42873380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c67f625f471ac77f19e966ef298a0cdea3b1b35c63e97d805703bf54c975c6`  
		Last Modified: Wed, 15 Apr 2026 20:50:09 GMT  
		Size: 26.8 KB (26791 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20260409` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6989d5c3753132dec96948dd6661340edb5f60e6a464a3e9110c01dd106dd7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.8 MB (604845623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90aec3c793f98497fde42fa53ce77f7cc638243ffbcc27804a54c607cc018b77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:47:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:47:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:47:58 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:47:58 GMT
ARG TARGETARCH=arm64
# Wed, 15 Apr 2026 20:47:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:06 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:07 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:07 GMT
ENV ODOO_VERSION=17.0
# Wed, 15 Apr 2026 20:48:07 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:07 GMT
ARG ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
# Wed, 15 Apr 2026 20:49:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:14 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=04837830d6d0cea14c5107eff7b13da5a784253e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b4b2cb6300c46351523b916b9745ef3880937fbb2541e09d3745f114d0316a`  
		Last Modified: Wed, 15 Apr 2026 20:50:45 GMT  
		Size: 231.2 MB (231203323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83768cdac59134061edd2cae53ee80da03cc7706a892b5c698ee4d8b86e18738`  
		Last Modified: Wed, 15 Apr 2026 20:50:37 GMT  
		Size: 2.6 MB (2598114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1753b8f99757a45895a0aabd5e1639ff3925f5120a31cbf2c1c9f05f8726e916`  
		Last Modified: Wed, 15 Apr 2026 20:50:37 GMT  
		Size: 481.6 KB (481610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36918b6e085496f8143e1a1e8be1612e163cc6706f534869a8fbd5d07ab15cb7`  
		Last Modified: Wed, 15 Apr 2026 20:50:47 GMT  
		Size: 343.0 MB (342953593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142df133284adbf5f883aeb4d99d5a09dbf2052cfdcd52dff79fea83a9427ce2`  
		Last Modified: Wed, 15 Apr 2026 20:50:38 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b61c0fbaaff2aa8e0ddf3b85c6eddbb22195bc6dc763b70a2d0d4f92b8ae236`  
		Last Modified: Wed, 15 Apr 2026 20:50:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c81e3858a3cf4342de427e1e2b807877f3fbca71f46a9eaffcf2a9e4e75ddd`  
		Last Modified: Wed, 15 Apr 2026 20:50:39 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a83506ccbc728b6eff01bc8f34e3497d8d8cbcc5995549fbac356719e04da0`  
		Last Modified: Wed, 15 Apr 2026 20:50:40 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:c3989242efe607c236c1c70adfd45aef85e9c4a6ea48bde174d3612932904796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42906831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef42ed1d69960d6d5cc4a12ddd7a12b74be4e1d613a36e7a8b8adc6cb03a9c6`

```dockerfile
```

-	Layers:
	-	`sha256:b115290eaf75491eacf3a47bdc11cd5dd973e24aa355cad13f00446662a12da2`  
		Last Modified: Wed, 15 Apr 2026 20:50:39 GMT  
		Size: 42.9 MB (42879887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e0cc904c876f694f70f1883347a3516c563bcf9836abb56406b8f44d240ede`  
		Last Modified: Wed, 15 Apr 2026 20:50:36 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:43675152ed7d66d5e3ecd5fad34be8abaae8cf6adff62a36c082a5415ae1f2a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18` - linux; amd64

```console
$ docker pull odoo@sha256:af9f7518d0d71ec7de760dfc01735ff6d5548b41e8446f22109bee8d1786ab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.1 MB (684059037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ffafa5613ca788c78f6d33d84a8de409db61f2e6d35695885eeefc53381929`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:07 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:07 GMT
ARG TARGETARCH=amd64
# Wed, 15 Apr 2026 20:48:07 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:18 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:18 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Apr 2026 20:48:18 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:18 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Wed, 15 Apr 2026 20:49:10 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:11 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:11 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67e2f7d9bca55a5e17cd8bc25863d516c43c0dde7d1173068c439a9c9485941`  
		Last Modified: Wed, 15 Apr 2026 20:51:09 GMT  
		Size: 254.6 MB (254568824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e7eb436fb2f549e50903c889ece83502800a145165981d646160e97853c0bf`  
		Last Modified: Wed, 15 Apr 2026 20:50:59 GMT  
		Size: 14.4 MB (14360130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb3c0120626de8654275517e018dcd4f30184e33f08133cef6250eecf0fea78`  
		Last Modified: Wed, 15 Apr 2026 20:50:58 GMT  
		Size: 481.3 KB (481290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8edb97f27bc30b8412991058bdb24549a16e7a0166f26ca193d9fb33504923f`  
		Last Modified: Wed, 15 Apr 2026 20:51:11 GMT  
		Size: 384.9 MB (384913373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e488f18479279bc1b8b39c095281eaf37bce3aff6db5f65ba2e2f089dce51424`  
		Last Modified: Wed, 15 Apr 2026 20:50:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43878adbbe4d1dc4412054ef2958af5e7d183d089ddfab5a3ca72832692dd618`  
		Last Modified: Wed, 15 Apr 2026 20:51:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5bb1142d67830057c6a69cddcff93d588e18dc528fedd105920f8f955429da`  
		Last Modified: Wed, 15 Apr 2026 20:51:01 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579a088889cc826560103493c7a7ea32f7e82847a2ac7114e8a1f59110565273`  
		Last Modified: Wed, 15 Apr 2026 20:51:02 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:b6d710a53dc1ff2bff559885603e807f938e16429d2ca5731213ce3918945f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62223462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b899882f2366a75d40172474d499703c2eeac79acf7c176cd8f4a49bd16c92`

```dockerfile
```

-	Layers:
	-	`sha256:a60f70728dfee271ec859f03321713d7cd47c557d0514bc6033088637c9d8c83`  
		Last Modified: Wed, 15 Apr 2026 20:51:02 GMT  
		Size: 62.2 MB (62196663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53990467cab251cac71a3ad9b512ac7e52bc844a6c845939adf1ac2db9c06f65`  
		Last Modified: Wed, 15 Apr 2026 20:50:58 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:13ca02934348d2fa958c0ecd190e229a768134db0ce0fd2098316d01dca2668f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.5 MB (680457454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76097ee3d95e055029e2497d7203a5e7bcff05c848dc720d2d39d94a5db74d40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:18 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:18 GMT
ARG TARGETARCH=arm64
# Wed, 15 Apr 2026 20:48:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:29 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:30 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:30 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Apr 2026 20:48:30 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:30 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Wed, 15 Apr 2026 20:49:30 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:30 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:30 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf06e77a25e7606f8b682f4eb4f23f3b90f40dffdbfb542e7779b00ff3e0493`  
		Last Modified: Wed, 15 Apr 2026 20:51:46 GMT  
		Size: 252.0 MB (251997273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accde5792ce1cd85da550bc31ecdeb12623ef2f1992ac0d7e0fc96823c9cc455`  
		Last Modified: Wed, 15 Apr 2026 20:51:38 GMT  
		Size: 14.3 MB (14340802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e45b534072d377412795812e52788348729469ac5ee6fe42a1602af19587cad`  
		Last Modified: Wed, 15 Apr 2026 20:51:36 GMT  
		Size: 481.3 KB (481318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa146647dd4e702644ca46cc3cf86b0c5d7ccf535f15bee7efa5b9486d0b9c5`  
		Last Modified: Wed, 15 Apr 2026 20:51:51 GMT  
		Size: 384.8 MB (384759834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64eb2e7c100ab28585b92f3dcfb612c91779e1d3f1c6e82d695b65ca1d53c92`  
		Last Modified: Wed, 15 Apr 2026 20:51:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc14bfd820f988d1d9f9ce4eac947f6a610a7794df82e4243038856d90cf1a92`  
		Last Modified: Wed, 15 Apr 2026 20:51:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc9bda10ad2645411c9718068f1925a5c4068d683304c4a3905090c87ccee10`  
		Last Modified: Wed, 15 Apr 2026 20:51:39 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd4a5f7095f02d822c4a89de0eb187bb7fc411e15a8eb72f6caca10956a2c6`  
		Last Modified: Wed, 15 Apr 2026 20:51:40 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:03b84fc9fb59203698f4faa54bea1a0699189cdd69b94087c027fea56fb2c617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62230889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5301bba5642fd6af2b0c8ba37c4fb9763343f0615d1ab054d69edabe98e1b60`

```dockerfile
```

-	Layers:
	-	`sha256:8f3da85234cb6dd299c427feca0695d23202f23c5d2bbadd4bb6c086e3ef4d44`  
		Last Modified: Wed, 15 Apr 2026 20:51:40 GMT  
		Size: 62.2 MB (62203938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6c3dd5a2452526ca9c268b696b6e27c4bb02cc32fabdddddf287275f7850c9`  
		Last Modified: Wed, 15 Apr 2026 20:51:36 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:b879003ac1a1b90a1f94532e70968aecc697faceb0f27a1b740f02463ff76bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.3 MB (700257597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7712c8f26d693c0c6b90b3e48ed5b2cf286bac2bc5aa14a182fafe5cf351431a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Wed, 15 Apr 2026 22:19:45 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 22:19:46 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:19:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 22:19:47 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 22:19:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 22:19:47 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 22:19:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 22:19:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 22:19:48 GMT
USER odoo
# Wed, 15 Apr 2026 22:19:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 22:19:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fad54d30afadb15107df92c55c9dcfb9952b2ce7d69b3ebef74c8aed2d77eb2`  
		Last Modified: Wed, 15 Apr 2026 22:24:37 GMT  
		Size: 385.5 MB (385455387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479a087b7e03118482b78769ae2019a9b6edffbddf9c6f17e72a7335c7268737`  
		Last Modified: Wed, 15 Apr 2026 22:24:27 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c26e316ef0dec4200f99d26b90995608d7a054b52b7bc2b590345c213fc58a0`  
		Last Modified: Wed, 15 Apr 2026 22:24:27 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5deb47e42e239853a03b72a325df5e10db947d9ce03eef4d119ddc7fc0c23a`  
		Last Modified: Wed, 15 Apr 2026 22:24:27 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c383fc2126cf51f0fc6ba16f8e7c7087229a039a6c6f21bcde9a3b0dad3123f1`  
		Last Modified: Wed, 15 Apr 2026 22:24:28 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:85efaf73ed27fcc5ce6eed1835c330399df2bcbe77ba2a4ef61cd5a6a04efc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62231901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247299bddf72e3c7d0dee336cc1350acc1d9b8b20eea1df3a67ecd14c634b17b`

```dockerfile
```

-	Layers:
	-	`sha256:5bb0925a7160a23f80837c4cffd4562a70e2b23998881357b83df5d0b2590b15`  
		Last Modified: Wed, 15 Apr 2026 22:24:30 GMT  
		Size: 62.2 MB (62205046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df5e9c96e9d4e5f59c83bb847bf1df2d17e11bb9546326b5274c57673661c668`  
		Last Modified: Wed, 15 Apr 2026 22:24:27 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:43675152ed7d66d5e3ecd5fad34be8abaae8cf6adff62a36c082a5415ae1f2a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0` - linux; amd64

```console
$ docker pull odoo@sha256:af9f7518d0d71ec7de760dfc01735ff6d5548b41e8446f22109bee8d1786ab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.1 MB (684059037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ffafa5613ca788c78f6d33d84a8de409db61f2e6d35695885eeefc53381929`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:07 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:07 GMT
ARG TARGETARCH=amd64
# Wed, 15 Apr 2026 20:48:07 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:18 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:18 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Apr 2026 20:48:18 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:18 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Wed, 15 Apr 2026 20:49:10 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:11 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:11 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67e2f7d9bca55a5e17cd8bc25863d516c43c0dde7d1173068c439a9c9485941`  
		Last Modified: Wed, 15 Apr 2026 20:51:09 GMT  
		Size: 254.6 MB (254568824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e7eb436fb2f549e50903c889ece83502800a145165981d646160e97853c0bf`  
		Last Modified: Wed, 15 Apr 2026 20:50:59 GMT  
		Size: 14.4 MB (14360130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb3c0120626de8654275517e018dcd4f30184e33f08133cef6250eecf0fea78`  
		Last Modified: Wed, 15 Apr 2026 20:50:58 GMT  
		Size: 481.3 KB (481290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8edb97f27bc30b8412991058bdb24549a16e7a0166f26ca193d9fb33504923f`  
		Last Modified: Wed, 15 Apr 2026 20:51:11 GMT  
		Size: 384.9 MB (384913373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e488f18479279bc1b8b39c095281eaf37bce3aff6db5f65ba2e2f089dce51424`  
		Last Modified: Wed, 15 Apr 2026 20:50:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43878adbbe4d1dc4412054ef2958af5e7d183d089ddfab5a3ca72832692dd618`  
		Last Modified: Wed, 15 Apr 2026 20:51:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5bb1142d67830057c6a69cddcff93d588e18dc528fedd105920f8f955429da`  
		Last Modified: Wed, 15 Apr 2026 20:51:01 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579a088889cc826560103493c7a7ea32f7e82847a2ac7114e8a1f59110565273`  
		Last Modified: Wed, 15 Apr 2026 20:51:02 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b6d710a53dc1ff2bff559885603e807f938e16429d2ca5731213ce3918945f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62223462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b899882f2366a75d40172474d499703c2eeac79acf7c176cd8f4a49bd16c92`

```dockerfile
```

-	Layers:
	-	`sha256:a60f70728dfee271ec859f03321713d7cd47c557d0514bc6033088637c9d8c83`  
		Last Modified: Wed, 15 Apr 2026 20:51:02 GMT  
		Size: 62.2 MB (62196663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53990467cab251cac71a3ad9b512ac7e52bc844a6c845939adf1ac2db9c06f65`  
		Last Modified: Wed, 15 Apr 2026 20:50:58 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:13ca02934348d2fa958c0ecd190e229a768134db0ce0fd2098316d01dca2668f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.5 MB (680457454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76097ee3d95e055029e2497d7203a5e7bcff05c848dc720d2d39d94a5db74d40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:18 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:18 GMT
ARG TARGETARCH=arm64
# Wed, 15 Apr 2026 20:48:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:29 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:30 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:30 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Apr 2026 20:48:30 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:30 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Wed, 15 Apr 2026 20:49:30 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:30 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:30 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf06e77a25e7606f8b682f4eb4f23f3b90f40dffdbfb542e7779b00ff3e0493`  
		Last Modified: Wed, 15 Apr 2026 20:51:46 GMT  
		Size: 252.0 MB (251997273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accde5792ce1cd85da550bc31ecdeb12623ef2f1992ac0d7e0fc96823c9cc455`  
		Last Modified: Wed, 15 Apr 2026 20:51:38 GMT  
		Size: 14.3 MB (14340802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e45b534072d377412795812e52788348729469ac5ee6fe42a1602af19587cad`  
		Last Modified: Wed, 15 Apr 2026 20:51:36 GMT  
		Size: 481.3 KB (481318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa146647dd4e702644ca46cc3cf86b0c5d7ccf535f15bee7efa5b9486d0b9c5`  
		Last Modified: Wed, 15 Apr 2026 20:51:51 GMT  
		Size: 384.8 MB (384759834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64eb2e7c100ab28585b92f3dcfb612c91779e1d3f1c6e82d695b65ca1d53c92`  
		Last Modified: Wed, 15 Apr 2026 20:51:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc14bfd820f988d1d9f9ce4eac947f6a610a7794df82e4243038856d90cf1a92`  
		Last Modified: Wed, 15 Apr 2026 20:51:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc9bda10ad2645411c9718068f1925a5c4068d683304c4a3905090c87ccee10`  
		Last Modified: Wed, 15 Apr 2026 20:51:39 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd4a5f7095f02d822c4a89de0eb187bb7fc411e15a8eb72f6caca10956a2c6`  
		Last Modified: Wed, 15 Apr 2026 20:51:40 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:03b84fc9fb59203698f4faa54bea1a0699189cdd69b94087c027fea56fb2c617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62230889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5301bba5642fd6af2b0c8ba37c4fb9763343f0615d1ab054d69edabe98e1b60`

```dockerfile
```

-	Layers:
	-	`sha256:8f3da85234cb6dd299c427feca0695d23202f23c5d2bbadd4bb6c086e3ef4d44`  
		Last Modified: Wed, 15 Apr 2026 20:51:40 GMT  
		Size: 62.2 MB (62203938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6c3dd5a2452526ca9c268b696b6e27c4bb02cc32fabdddddf287275f7850c9`  
		Last Modified: Wed, 15 Apr 2026 20:51:36 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b879003ac1a1b90a1f94532e70968aecc697faceb0f27a1b740f02463ff76bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.3 MB (700257597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7712c8f26d693c0c6b90b3e48ed5b2cf286bac2bc5aa14a182fafe5cf351431a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Wed, 15 Apr 2026 22:19:45 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 22:19:46 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:19:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 22:19:47 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 22:19:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 22:19:47 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 22:19:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 22:19:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 22:19:48 GMT
USER odoo
# Wed, 15 Apr 2026 22:19:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 22:19:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fad54d30afadb15107df92c55c9dcfb9952b2ce7d69b3ebef74c8aed2d77eb2`  
		Last Modified: Wed, 15 Apr 2026 22:24:37 GMT  
		Size: 385.5 MB (385455387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479a087b7e03118482b78769ae2019a9b6edffbddf9c6f17e72a7335c7268737`  
		Last Modified: Wed, 15 Apr 2026 22:24:27 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c26e316ef0dec4200f99d26b90995608d7a054b52b7bc2b590345c213fc58a0`  
		Last Modified: Wed, 15 Apr 2026 22:24:27 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5deb47e42e239853a03b72a325df5e10db947d9ce03eef4d119ddc7fc0c23a`  
		Last Modified: Wed, 15 Apr 2026 22:24:27 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c383fc2126cf51f0fc6ba16f8e7c7087229a039a6c6f21bcde9a3b0dad3123f1`  
		Last Modified: Wed, 15 Apr 2026 22:24:28 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:85efaf73ed27fcc5ce6eed1835c330399df2bcbe77ba2a4ef61cd5a6a04efc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62231901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247299bddf72e3c7d0dee336cc1350acc1d9b8b20eea1df3a67ecd14c634b17b`

```dockerfile
```

-	Layers:
	-	`sha256:5bb0925a7160a23f80837c4cffd4562a70e2b23998881357b83df5d0b2590b15`  
		Last Modified: Wed, 15 Apr 2026 22:24:30 GMT  
		Size: 62.2 MB (62205046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df5e9c96e9d4e5f59c83bb847bf1df2d17e11bb9546326b5274c57673661c668`  
		Last Modified: Wed, 15 Apr 2026 22:24:27 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260409`

```console
$ docker pull odoo@sha256:43675152ed7d66d5e3ecd5fad34be8abaae8cf6adff62a36c082a5415ae1f2a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260409` - linux; amd64

```console
$ docker pull odoo@sha256:af9f7518d0d71ec7de760dfc01735ff6d5548b41e8446f22109bee8d1786ab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.1 MB (684059037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ffafa5613ca788c78f6d33d84a8de409db61f2e6d35695885eeefc53381929`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:07 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:07 GMT
ARG TARGETARCH=amd64
# Wed, 15 Apr 2026 20:48:07 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:18 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:18 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Apr 2026 20:48:18 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:18 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Wed, 15 Apr 2026 20:49:10 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:11 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:11 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:11 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67e2f7d9bca55a5e17cd8bc25863d516c43c0dde7d1173068c439a9c9485941`  
		Last Modified: Wed, 15 Apr 2026 20:51:09 GMT  
		Size: 254.6 MB (254568824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e7eb436fb2f549e50903c889ece83502800a145165981d646160e97853c0bf`  
		Last Modified: Wed, 15 Apr 2026 20:50:59 GMT  
		Size: 14.4 MB (14360130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb3c0120626de8654275517e018dcd4f30184e33f08133cef6250eecf0fea78`  
		Last Modified: Wed, 15 Apr 2026 20:50:58 GMT  
		Size: 481.3 KB (481290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8edb97f27bc30b8412991058bdb24549a16e7a0166f26ca193d9fb33504923f`  
		Last Modified: Wed, 15 Apr 2026 20:51:11 GMT  
		Size: 384.9 MB (384913373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e488f18479279bc1b8b39c095281eaf37bce3aff6db5f65ba2e2f089dce51424`  
		Last Modified: Wed, 15 Apr 2026 20:50:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43878adbbe4d1dc4412054ef2958af5e7d183d089ddfab5a3ca72832692dd618`  
		Last Modified: Wed, 15 Apr 2026 20:51:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5bb1142d67830057c6a69cddcff93d588e18dc528fedd105920f8f955429da`  
		Last Modified: Wed, 15 Apr 2026 20:51:01 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579a088889cc826560103493c7a7ea32f7e82847a2ac7114e8a1f59110565273`  
		Last Modified: Wed, 15 Apr 2026 20:51:02 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:b6d710a53dc1ff2bff559885603e807f938e16429d2ca5731213ce3918945f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62223462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b899882f2366a75d40172474d499703c2eeac79acf7c176cd8f4a49bd16c92`

```dockerfile
```

-	Layers:
	-	`sha256:a60f70728dfee271ec859f03321713d7cd47c557d0514bc6033088637c9d8c83`  
		Last Modified: Wed, 15 Apr 2026 20:51:02 GMT  
		Size: 62.2 MB (62196663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53990467cab251cac71a3ad9b512ac7e52bc844a6c845939adf1ac2db9c06f65`  
		Last Modified: Wed, 15 Apr 2026 20:50:58 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260409` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:13ca02934348d2fa958c0ecd190e229a768134db0ce0fd2098316d01dca2668f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.5 MB (680457454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76097ee3d95e055029e2497d7203a5e7bcff05c848dc720d2d39d94a5db74d40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:18 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:18 GMT
ARG TARGETARCH=arm64
# Wed, 15 Apr 2026 20:48:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:29 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:30 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:30 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Apr 2026 20:48:30 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:30 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Wed, 15 Apr 2026 20:49:30 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:30 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:30 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:30 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf06e77a25e7606f8b682f4eb4f23f3b90f40dffdbfb542e7779b00ff3e0493`  
		Last Modified: Wed, 15 Apr 2026 20:51:46 GMT  
		Size: 252.0 MB (251997273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accde5792ce1cd85da550bc31ecdeb12623ef2f1992ac0d7e0fc96823c9cc455`  
		Last Modified: Wed, 15 Apr 2026 20:51:38 GMT  
		Size: 14.3 MB (14340802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e45b534072d377412795812e52788348729469ac5ee6fe42a1602af19587cad`  
		Last Modified: Wed, 15 Apr 2026 20:51:36 GMT  
		Size: 481.3 KB (481318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa146647dd4e702644ca46cc3cf86b0c5d7ccf535f15bee7efa5b9486d0b9c5`  
		Last Modified: Wed, 15 Apr 2026 20:51:51 GMT  
		Size: 384.8 MB (384759834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64eb2e7c100ab28585b92f3dcfb612c91779e1d3f1c6e82d695b65ca1d53c92`  
		Last Modified: Wed, 15 Apr 2026 20:51:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc14bfd820f988d1d9f9ce4eac947f6a610a7794df82e4243038856d90cf1a92`  
		Last Modified: Wed, 15 Apr 2026 20:51:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc9bda10ad2645411c9718068f1925a5c4068d683304c4a3905090c87ccee10`  
		Last Modified: Wed, 15 Apr 2026 20:51:39 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd4a5f7095f02d822c4a89de0eb187bb7fc411e15a8eb72f6caca10956a2c6`  
		Last Modified: Wed, 15 Apr 2026 20:51:40 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:03b84fc9fb59203698f4faa54bea1a0699189cdd69b94087c027fea56fb2c617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62230889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5301bba5642fd6af2b0c8ba37c4fb9763343f0615d1ab054d69edabe98e1b60`

```dockerfile
```

-	Layers:
	-	`sha256:8f3da85234cb6dd299c427feca0695d23202f23c5d2bbadd4bb6c086e3ef4d44`  
		Last Modified: Wed, 15 Apr 2026 20:51:40 GMT  
		Size: 62.2 MB (62203938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6c3dd5a2452526ca9c268b696b6e27c4bb02cc32fabdddddf287275f7850c9`  
		Last Modified: Wed, 15 Apr 2026 20:51:36 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260409` - linux; ppc64le

```console
$ docker pull odoo@sha256:b879003ac1a1b90a1f94532e70968aecc697faceb0f27a1b740f02463ff76bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.3 MB (700257597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7712c8f26d693c0c6b90b3e48ed5b2cf286bac2bc5aa14a182fafe5cf351431a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
# Wed, 15 Apr 2026 22:19:45 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 22:19:46 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:19:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 22:19:47 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=a345108601f88b97a5732514887c071cffb24879
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 22:19:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 22:19:47 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 22:19:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 22:19:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 22:19:48 GMT
USER odoo
# Wed, 15 Apr 2026 22:19:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 22:19:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fad54d30afadb15107df92c55c9dcfb9952b2ce7d69b3ebef74c8aed2d77eb2`  
		Last Modified: Wed, 15 Apr 2026 22:24:37 GMT  
		Size: 385.5 MB (385455387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479a087b7e03118482b78769ae2019a9b6edffbddf9c6f17e72a7335c7268737`  
		Last Modified: Wed, 15 Apr 2026 22:24:27 GMT  
		Size: 702.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c26e316ef0dec4200f99d26b90995608d7a054b52b7bc2b590345c213fc58a0`  
		Last Modified: Wed, 15 Apr 2026 22:24:27 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5deb47e42e239853a03b72a325df5e10db947d9ce03eef4d119ddc7fc0c23a`  
		Last Modified: Wed, 15 Apr 2026 22:24:27 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c383fc2126cf51f0fc6ba16f8e7c7087229a039a6c6f21bcde9a3b0dad3123f1`  
		Last Modified: Wed, 15 Apr 2026 22:24:28 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:85efaf73ed27fcc5ce6eed1835c330399df2bcbe77ba2a4ef61cd5a6a04efc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62231901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247299bddf72e3c7d0dee336cc1350acc1d9b8b20eea1df3a67ecd14c634b17b`

```dockerfile
```

-	Layers:
	-	`sha256:5bb0925a7160a23f80837c4cffd4562a70e2b23998881357b83df5d0b2590b15`  
		Last Modified: Wed, 15 Apr 2026 22:24:30 GMT  
		Size: 62.2 MB (62205046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df5e9c96e9d4e5f59c83bb847bf1df2d17e11bb9546326b5274c57673661c668`  
		Last Modified: Wed, 15 Apr 2026 22:24:27 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:b1309b954d5ae10482a76aa1af95bcf00050f9393e54828ca156721b9dd29e50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19` - linux; amd64

```console
$ docker pull odoo@sha256:203fd4b933c18268c117b5c2e671d89de5cb8676290595034f346c7f04b25346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702858293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855474d437af8645d32a6834473afb08559cbed87fccf8d2f6b5dd9407ac5d13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:00 GMT
ARG TARGETARCH=amd64
# Wed, 15 Apr 2026 20:48:00 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:09 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:10 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:10 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 20:48:10 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:10 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 20:49:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fa6831676b190d2d5c94bebb83e2d7cd548fca345b58005e187b8c00173ba4`  
		Last Modified: Wed, 15 Apr 2026 20:51:36 GMT  
		Size: 254.6 MB (254568981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982dac0b7116a77d0eb99ee64e15b332d2cf2f96cebe15d2aa5bcb2d9204d756`  
		Last Modified: Wed, 15 Apr 2026 20:51:27 GMT  
		Size: 14.4 MB (14360003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f028cd970fe13e97149da5e7f82e1c550bc50f2418dd6011df4619970e969f6`  
		Last Modified: Wed, 15 Apr 2026 20:51:25 GMT  
		Size: 481.4 KB (481366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228ff53452d59ba35b1bd4b37ff467f6bb3880f5cce747216fdba4dbdf132e80`  
		Last Modified: Wed, 15 Apr 2026 20:51:42 GMT  
		Size: 403.7 MB (403712522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73630db1a964b498227c4f86424955d1c411538db2a20435744280eb1f9717ff`  
		Last Modified: Wed, 15 Apr 2026 20:51:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d081f790e2cfe3abfa8c77cee76a77914248582f099ace5a1e20e9047fc4bb5`  
		Last Modified: Wed, 15 Apr 2026 20:51:28 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca4cc5f93bd32323f0de1f58dd576ef83f84a1bc6eccc844b24d3ef14f207c3`  
		Last Modified: Wed, 15 Apr 2026 20:51:29 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea73638335432cdad3c918408fcfded01b1405664cff7ac8506b290783c9d5`  
		Last Modified: Wed, 15 Apr 2026 20:51:30 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:91c3684489350a201530f634f1552067930cc2bf64b4734ac48e222f5dc2e697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70013973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6892742651b994073abb1090a7e90ea8f972ed048f2756647081f920b1cd78a`

```dockerfile
```

-	Layers:
	-	`sha256:32480b99579928e5f58c073257cddce4d5ee82d9845e9dff3f1c239edb083e1c`  
		Last Modified: Wed, 15 Apr 2026 20:51:30 GMT  
		Size: 70.0 MB (69986881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d88a36028d6640f54fbca3cb33a441005382e1cb6d9b075c9010c7d730e8c16c`  
		Last Modified: Wed, 15 Apr 2026 20:51:26 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b03cc2fef19b099c21728ff00dd9adf63c1a284970b68757f4cafa777416dd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.2 MB (699214693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8b22aa944d037587c91ba8ac8bf9784a173ee9c51279ca326ad4cf337ac12a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:17 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:17 GMT
ARG TARGETARCH=arm64
# Wed, 15 Apr 2026 20:48:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:33 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:33 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 20:48:33 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:33 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 20:49:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f3e489f476902259b1bc1a369e63e4809cc22574b7c0c9d7b9fb0a1ca5124`  
		Last Modified: Wed, 15 Apr 2026 20:52:28 GMT  
		Size: 252.0 MB (251996977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd763d85262711f9837b628e3300d4935048ad99b8de3992a4fb29fa9f25c`  
		Last Modified: Wed, 15 Apr 2026 20:52:18 GMT  
		Size: 14.3 MB (14340843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8355eee5c2271a157cd610a9d3d833d13f83cc5f93349ad0e991202f0d5d5`  
		Last Modified: Wed, 15 Apr 2026 20:52:17 GMT  
		Size: 481.3 KB (481292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3373fccc9b39bc95f6c8fe75ab832c594126aa9f0b97ef7c45eba05b36c20a8f`  
		Last Modified: Wed, 15 Apr 2026 20:52:31 GMT  
		Size: 403.5 MB (403517357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b3bec6120f3993e425e937df871efe1fe55cb9b3b215456296b98b7a55b3b5`  
		Last Modified: Wed, 15 Apr 2026 20:52:18 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140fc9b0365e2b42fc087bbfb151f1acc84a2a98ae3a4d81bddf5c593bbc59d0`  
		Last Modified: Wed, 15 Apr 2026 20:52:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25abd3207920dd469e960eae98e11e44f77c87c176b6fa71043c41cde68642e5`  
		Last Modified: Wed, 15 Apr 2026 20:52:20 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baea3afe04b0d7a9325fce3ea62ed44eac45e665c4dd7bfda8ad6b0f66af848f`  
		Last Modified: Wed, 15 Apr 2026 20:52:21 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:308a050c74211c7285f0b974d3a33d31b10c41a1b7ae69a98dc43ed381c580d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70021424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261935b51308992317a71304703ebbb4364ea334cfabdaecf74b8e417c41c103`

```dockerfile
```

-	Layers:
	-	`sha256:0ca8ad645980fc26d92ab6c47b5dd33a2f9486fa53cf3fe1790b21371bdce16c`  
		Last Modified: Wed, 15 Apr 2026 20:52:23 GMT  
		Size: 70.0 MB (69994168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02593a4bab326b36fbb467b3dff444e7294144d4ceb74598f1e995d53793306d`  
		Last Modified: Wed, 15 Apr 2026 20:52:17 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:087480bffa7e68cc5dddd001504af53923ee4aa1f4b665eef5108bf77aab2087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.0 MB (719013665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139ed7eccbe507c9454de569ec64657032216848e6b617d055a7c2c6ee104a99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 22:11:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 22:11:49 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 22:11:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 22:11:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 22:11:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
USER odoo
# Wed, 15 Apr 2026 22:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388d300d3e84719cea202904a8e5ca0786e9fea0d6d4d6858f3da33405553073`  
		Last Modified: Wed, 15 Apr 2026 22:17:52 GMT  
		Size: 404.2 MB (404211454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432b5a45562f2f4c3b31e2fedd997d7635ebdcc7c279dbddd2662476a35911b`  
		Last Modified: Wed, 15 Apr 2026 22:17:39 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ba7b9ff260f0c5bde6d56479d191cc96520d4657d9f1ac5bb5b3d593ff58f8`  
		Last Modified: Wed, 15 Apr 2026 22:17:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f381381dd7596b8eddbd9df8b74602e34d0e8453863a22ab0dc1cb37833dce`  
		Last Modified: Wed, 15 Apr 2026 22:17:40 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871085cd3fd32e086680453022914a22a3391e0851d133c92366e39c5d6216c2`  
		Last Modified: Wed, 15 Apr 2026 22:17:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:3c23d345179d740cb0f19de9c2a0c8e48b04716294860f54fa9214d82099b7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70022425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d3e0665e4db8d1045fd4a44596ba2894e685052865fc8e4368f58424085d54`

```dockerfile
```

-	Layers:
	-	`sha256:b3b85b8c5e943bccb0dd3d10303ba0969576284ba049b5787b3882d4cb760575`  
		Last Modified: Wed, 15 Apr 2026 22:17:42 GMT  
		Size: 70.0 MB (69995270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b50952403bf0f989c877184390e524e43cd625037b5be1d156be2dd0be0db43`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:b1309b954d5ae10482a76aa1af95bcf00050f9393e54828ca156721b9dd29e50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0` - linux; amd64

```console
$ docker pull odoo@sha256:203fd4b933c18268c117b5c2e671d89de5cb8676290595034f346c7f04b25346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702858293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855474d437af8645d32a6834473afb08559cbed87fccf8d2f6b5dd9407ac5d13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:00 GMT
ARG TARGETARCH=amd64
# Wed, 15 Apr 2026 20:48:00 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:09 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:10 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:10 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 20:48:10 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:10 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 20:49:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fa6831676b190d2d5c94bebb83e2d7cd548fca345b58005e187b8c00173ba4`  
		Last Modified: Wed, 15 Apr 2026 20:51:36 GMT  
		Size: 254.6 MB (254568981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982dac0b7116a77d0eb99ee64e15b332d2cf2f96cebe15d2aa5bcb2d9204d756`  
		Last Modified: Wed, 15 Apr 2026 20:51:27 GMT  
		Size: 14.4 MB (14360003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f028cd970fe13e97149da5e7f82e1c550bc50f2418dd6011df4619970e969f6`  
		Last Modified: Wed, 15 Apr 2026 20:51:25 GMT  
		Size: 481.4 KB (481366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228ff53452d59ba35b1bd4b37ff467f6bb3880f5cce747216fdba4dbdf132e80`  
		Last Modified: Wed, 15 Apr 2026 20:51:42 GMT  
		Size: 403.7 MB (403712522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73630db1a964b498227c4f86424955d1c411538db2a20435744280eb1f9717ff`  
		Last Modified: Wed, 15 Apr 2026 20:51:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d081f790e2cfe3abfa8c77cee76a77914248582f099ace5a1e20e9047fc4bb5`  
		Last Modified: Wed, 15 Apr 2026 20:51:28 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca4cc5f93bd32323f0de1f58dd576ef83f84a1bc6eccc844b24d3ef14f207c3`  
		Last Modified: Wed, 15 Apr 2026 20:51:29 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea73638335432cdad3c918408fcfded01b1405664cff7ac8506b290783c9d5`  
		Last Modified: Wed, 15 Apr 2026 20:51:30 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:91c3684489350a201530f634f1552067930cc2bf64b4734ac48e222f5dc2e697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70013973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6892742651b994073abb1090a7e90ea8f972ed048f2756647081f920b1cd78a`

```dockerfile
```

-	Layers:
	-	`sha256:32480b99579928e5f58c073257cddce4d5ee82d9845e9dff3f1c239edb083e1c`  
		Last Modified: Wed, 15 Apr 2026 20:51:30 GMT  
		Size: 70.0 MB (69986881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d88a36028d6640f54fbca3cb33a441005382e1cb6d9b075c9010c7d730e8c16c`  
		Last Modified: Wed, 15 Apr 2026 20:51:26 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b03cc2fef19b099c21728ff00dd9adf63c1a284970b68757f4cafa777416dd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.2 MB (699214693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8b22aa944d037587c91ba8ac8bf9784a173ee9c51279ca326ad4cf337ac12a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:17 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:17 GMT
ARG TARGETARCH=arm64
# Wed, 15 Apr 2026 20:48:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:33 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:33 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 20:48:33 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:33 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 20:49:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f3e489f476902259b1bc1a369e63e4809cc22574b7c0c9d7b9fb0a1ca5124`  
		Last Modified: Wed, 15 Apr 2026 20:52:28 GMT  
		Size: 252.0 MB (251996977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd763d85262711f9837b628e3300d4935048ad99b8de3992a4fb29fa9f25c`  
		Last Modified: Wed, 15 Apr 2026 20:52:18 GMT  
		Size: 14.3 MB (14340843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8355eee5c2271a157cd610a9d3d833d13f83cc5f93349ad0e991202f0d5d5`  
		Last Modified: Wed, 15 Apr 2026 20:52:17 GMT  
		Size: 481.3 KB (481292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3373fccc9b39bc95f6c8fe75ab832c594126aa9f0b97ef7c45eba05b36c20a8f`  
		Last Modified: Wed, 15 Apr 2026 20:52:31 GMT  
		Size: 403.5 MB (403517357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b3bec6120f3993e425e937df871efe1fe55cb9b3b215456296b98b7a55b3b5`  
		Last Modified: Wed, 15 Apr 2026 20:52:18 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140fc9b0365e2b42fc087bbfb151f1acc84a2a98ae3a4d81bddf5c593bbc59d0`  
		Last Modified: Wed, 15 Apr 2026 20:52:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25abd3207920dd469e960eae98e11e44f77c87c176b6fa71043c41cde68642e5`  
		Last Modified: Wed, 15 Apr 2026 20:52:20 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baea3afe04b0d7a9325fce3ea62ed44eac45e665c4dd7bfda8ad6b0f66af848f`  
		Last Modified: Wed, 15 Apr 2026 20:52:21 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:308a050c74211c7285f0b974d3a33d31b10c41a1b7ae69a98dc43ed381c580d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70021424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261935b51308992317a71304703ebbb4364ea334cfabdaecf74b8e417c41c103`

```dockerfile
```

-	Layers:
	-	`sha256:0ca8ad645980fc26d92ab6c47b5dd33a2f9486fa53cf3fe1790b21371bdce16c`  
		Last Modified: Wed, 15 Apr 2026 20:52:23 GMT  
		Size: 70.0 MB (69994168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02593a4bab326b36fbb467b3dff444e7294144d4ceb74598f1e995d53793306d`  
		Last Modified: Wed, 15 Apr 2026 20:52:17 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:087480bffa7e68cc5dddd001504af53923ee4aa1f4b665eef5108bf77aab2087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.0 MB (719013665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139ed7eccbe507c9454de569ec64657032216848e6b617d055a7c2c6ee104a99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 22:11:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 22:11:49 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 22:11:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 22:11:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 22:11:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
USER odoo
# Wed, 15 Apr 2026 22:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388d300d3e84719cea202904a8e5ca0786e9fea0d6d4d6858f3da33405553073`  
		Last Modified: Wed, 15 Apr 2026 22:17:52 GMT  
		Size: 404.2 MB (404211454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432b5a45562f2f4c3b31e2fedd997d7635ebdcc7c279dbddd2662476a35911b`  
		Last Modified: Wed, 15 Apr 2026 22:17:39 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ba7b9ff260f0c5bde6d56479d191cc96520d4657d9f1ac5bb5b3d593ff58f8`  
		Last Modified: Wed, 15 Apr 2026 22:17:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f381381dd7596b8eddbd9df8b74602e34d0e8453863a22ab0dc1cb37833dce`  
		Last Modified: Wed, 15 Apr 2026 22:17:40 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871085cd3fd32e086680453022914a22a3391e0851d133c92366e39c5d6216c2`  
		Last Modified: Wed, 15 Apr 2026 22:17:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:3c23d345179d740cb0f19de9c2a0c8e48b04716294860f54fa9214d82099b7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70022425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d3e0665e4db8d1045fd4a44596ba2894e685052865fc8e4368f58424085d54`

```dockerfile
```

-	Layers:
	-	`sha256:b3b85b8c5e943bccb0dd3d10303ba0969576284ba049b5787b3882d4cb760575`  
		Last Modified: Wed, 15 Apr 2026 22:17:42 GMT  
		Size: 70.0 MB (69995270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b50952403bf0f989c877184390e524e43cd625037b5be1d156be2dd0be0db43`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260409`

```console
$ docker pull odoo@sha256:b1309b954d5ae10482a76aa1af95bcf00050f9393e54828ca156721b9dd29e50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20260409` - linux; amd64

```console
$ docker pull odoo@sha256:203fd4b933c18268c117b5c2e671d89de5cb8676290595034f346c7f04b25346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702858293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855474d437af8645d32a6834473afb08559cbed87fccf8d2f6b5dd9407ac5d13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:00 GMT
ARG TARGETARCH=amd64
# Wed, 15 Apr 2026 20:48:00 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:09 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:10 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:10 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 20:48:10 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:10 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 20:49:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fa6831676b190d2d5c94bebb83e2d7cd548fca345b58005e187b8c00173ba4`  
		Last Modified: Wed, 15 Apr 2026 20:51:36 GMT  
		Size: 254.6 MB (254568981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982dac0b7116a77d0eb99ee64e15b332d2cf2f96cebe15d2aa5bcb2d9204d756`  
		Last Modified: Wed, 15 Apr 2026 20:51:27 GMT  
		Size: 14.4 MB (14360003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f028cd970fe13e97149da5e7f82e1c550bc50f2418dd6011df4619970e969f6`  
		Last Modified: Wed, 15 Apr 2026 20:51:25 GMT  
		Size: 481.4 KB (481366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228ff53452d59ba35b1bd4b37ff467f6bb3880f5cce747216fdba4dbdf132e80`  
		Last Modified: Wed, 15 Apr 2026 20:51:42 GMT  
		Size: 403.7 MB (403712522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73630db1a964b498227c4f86424955d1c411538db2a20435744280eb1f9717ff`  
		Last Modified: Wed, 15 Apr 2026 20:51:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d081f790e2cfe3abfa8c77cee76a77914248582f099ace5a1e20e9047fc4bb5`  
		Last Modified: Wed, 15 Apr 2026 20:51:28 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca4cc5f93bd32323f0de1f58dd576ef83f84a1bc6eccc844b24d3ef14f207c3`  
		Last Modified: Wed, 15 Apr 2026 20:51:29 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea73638335432cdad3c918408fcfded01b1405664cff7ac8506b290783c9d5`  
		Last Modified: Wed, 15 Apr 2026 20:51:30 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:91c3684489350a201530f634f1552067930cc2bf64b4734ac48e222f5dc2e697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70013973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6892742651b994073abb1090a7e90ea8f972ed048f2756647081f920b1cd78a`

```dockerfile
```

-	Layers:
	-	`sha256:32480b99579928e5f58c073257cddce4d5ee82d9845e9dff3f1c239edb083e1c`  
		Last Modified: Wed, 15 Apr 2026 20:51:30 GMT  
		Size: 70.0 MB (69986881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d88a36028d6640f54fbca3cb33a441005382e1cb6d9b075c9010c7d730e8c16c`  
		Last Modified: Wed, 15 Apr 2026 20:51:26 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260409` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b03cc2fef19b099c21728ff00dd9adf63c1a284970b68757f4cafa777416dd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.2 MB (699214693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8b22aa944d037587c91ba8ac8bf9784a173ee9c51279ca326ad4cf337ac12a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:17 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:17 GMT
ARG TARGETARCH=arm64
# Wed, 15 Apr 2026 20:48:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:33 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:33 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 20:48:33 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:33 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 20:49:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f3e489f476902259b1bc1a369e63e4809cc22574b7c0c9d7b9fb0a1ca5124`  
		Last Modified: Wed, 15 Apr 2026 20:52:28 GMT  
		Size: 252.0 MB (251996977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd763d85262711f9837b628e3300d4935048ad99b8de3992a4fb29fa9f25c`  
		Last Modified: Wed, 15 Apr 2026 20:52:18 GMT  
		Size: 14.3 MB (14340843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8355eee5c2271a157cd610a9d3d833d13f83cc5f93349ad0e991202f0d5d5`  
		Last Modified: Wed, 15 Apr 2026 20:52:17 GMT  
		Size: 481.3 KB (481292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3373fccc9b39bc95f6c8fe75ab832c594126aa9f0b97ef7c45eba05b36c20a8f`  
		Last Modified: Wed, 15 Apr 2026 20:52:31 GMT  
		Size: 403.5 MB (403517357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b3bec6120f3993e425e937df871efe1fe55cb9b3b215456296b98b7a55b3b5`  
		Last Modified: Wed, 15 Apr 2026 20:52:18 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140fc9b0365e2b42fc087bbfb151f1acc84a2a98ae3a4d81bddf5c593bbc59d0`  
		Last Modified: Wed, 15 Apr 2026 20:52:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25abd3207920dd469e960eae98e11e44f77c87c176b6fa71043c41cde68642e5`  
		Last Modified: Wed, 15 Apr 2026 20:52:20 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baea3afe04b0d7a9325fce3ea62ed44eac45e665c4dd7bfda8ad6b0f66af848f`  
		Last Modified: Wed, 15 Apr 2026 20:52:21 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:308a050c74211c7285f0b974d3a33d31b10c41a1b7ae69a98dc43ed381c580d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70021424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261935b51308992317a71304703ebbb4364ea334cfabdaecf74b8e417c41c103`

```dockerfile
```

-	Layers:
	-	`sha256:0ca8ad645980fc26d92ab6c47b5dd33a2f9486fa53cf3fe1790b21371bdce16c`  
		Last Modified: Wed, 15 Apr 2026 20:52:23 GMT  
		Size: 70.0 MB (69994168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02593a4bab326b36fbb467b3dff444e7294144d4ceb74598f1e995d53793306d`  
		Last Modified: Wed, 15 Apr 2026 20:52:17 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260409` - linux; ppc64le

```console
$ docker pull odoo@sha256:087480bffa7e68cc5dddd001504af53923ee4aa1f4b665eef5108bf77aab2087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.0 MB (719013665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139ed7eccbe507c9454de569ec64657032216848e6b617d055a7c2c6ee104a99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 22:11:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 22:11:49 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 22:11:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 22:11:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 22:11:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
USER odoo
# Wed, 15 Apr 2026 22:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388d300d3e84719cea202904a8e5ca0786e9fea0d6d4d6858f3da33405553073`  
		Last Modified: Wed, 15 Apr 2026 22:17:52 GMT  
		Size: 404.2 MB (404211454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432b5a45562f2f4c3b31e2fedd997d7635ebdcc7c279dbddd2662476a35911b`  
		Last Modified: Wed, 15 Apr 2026 22:17:39 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ba7b9ff260f0c5bde6d56479d191cc96520d4657d9f1ac5bb5b3d593ff58f8`  
		Last Modified: Wed, 15 Apr 2026 22:17:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f381381dd7596b8eddbd9df8b74602e34d0e8453863a22ab0dc1cb37833dce`  
		Last Modified: Wed, 15 Apr 2026 22:17:40 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871085cd3fd32e086680453022914a22a3391e0851d133c92366e39c5d6216c2`  
		Last Modified: Wed, 15 Apr 2026 22:17:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260409` - unknown; unknown

```console
$ docker pull odoo@sha256:3c23d345179d740cb0f19de9c2a0c8e48b04716294860f54fa9214d82099b7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70022425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d3e0665e4db8d1045fd4a44596ba2894e685052865fc8e4368f58424085d54`

```dockerfile
```

-	Layers:
	-	`sha256:b3b85b8c5e943bccb0dd3d10303ba0969576284ba049b5787b3882d4cb760575`  
		Last Modified: Wed, 15 Apr 2026 22:17:42 GMT  
		Size: 70.0 MB (69995270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b50952403bf0f989c877184390e524e43cd625037b5be1d156be2dd0be0db43`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:b1309b954d5ae10482a76aa1af95bcf00050f9393e54828ca156721b9dd29e50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:203fd4b933c18268c117b5c2e671d89de5cb8676290595034f346c7f04b25346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702858293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855474d437af8645d32a6834473afb08559cbed87fccf8d2f6b5dd9407ac5d13`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:00 GMT
ARG TARGETARCH=amd64
# Wed, 15 Apr 2026 20:48:00 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:09 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:10 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:10 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 20:48:10 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:10 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 20:49:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:15 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:16 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fa6831676b190d2d5c94bebb83e2d7cd548fca345b58005e187b8c00173ba4`  
		Last Modified: Wed, 15 Apr 2026 20:51:36 GMT  
		Size: 254.6 MB (254568981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982dac0b7116a77d0eb99ee64e15b332d2cf2f96cebe15d2aa5bcb2d9204d756`  
		Last Modified: Wed, 15 Apr 2026 20:51:27 GMT  
		Size: 14.4 MB (14360003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f028cd970fe13e97149da5e7f82e1c550bc50f2418dd6011df4619970e969f6`  
		Last Modified: Wed, 15 Apr 2026 20:51:25 GMT  
		Size: 481.4 KB (481366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228ff53452d59ba35b1bd4b37ff467f6bb3880f5cce747216fdba4dbdf132e80`  
		Last Modified: Wed, 15 Apr 2026 20:51:42 GMT  
		Size: 403.7 MB (403712522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73630db1a964b498227c4f86424955d1c411538db2a20435744280eb1f9717ff`  
		Last Modified: Wed, 15 Apr 2026 20:51:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d081f790e2cfe3abfa8c77cee76a77914248582f099ace5a1e20e9047fc4bb5`  
		Last Modified: Wed, 15 Apr 2026 20:51:28 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca4cc5f93bd32323f0de1f58dd576ef83f84a1bc6eccc844b24d3ef14f207c3`  
		Last Modified: Wed, 15 Apr 2026 20:51:29 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebea73638335432cdad3c918408fcfded01b1405664cff7ac8506b290783c9d5`  
		Last Modified: Wed, 15 Apr 2026 20:51:30 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:91c3684489350a201530f634f1552067930cc2bf64b4734ac48e222f5dc2e697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70013973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6892742651b994073abb1090a7e90ea8f972ed048f2756647081f920b1cd78a`

```dockerfile
```

-	Layers:
	-	`sha256:32480b99579928e5f58c073257cddce4d5ee82d9845e9dff3f1c239edb083e1c`  
		Last Modified: Wed, 15 Apr 2026 20:51:30 GMT  
		Size: 70.0 MB (69986881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d88a36028d6640f54fbca3cb33a441005382e1cb6d9b075c9010c7d730e8c16c`  
		Last Modified: Wed, 15 Apr 2026 20:51:26 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b03cc2fef19b099c21728ff00dd9adf63c1a284970b68757f4cafa777416dd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.2 MB (699214693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8b22aa944d037587c91ba8ac8bf9784a173ee9c51279ca326ad4cf337ac12a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:48:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 20:48:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 20:48:17 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:48:17 GMT
ARG TARGETARCH=arm64
# Wed, 15 Apr 2026 20:48:17 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 20:48:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:48:33 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 20:48:33 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 20:48:33 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 20:48:33 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 20:49:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 20:49:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 20:49:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 20:49:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 20:49:37 GMT
USER odoo
# Wed, 15 Apr 2026 20:49:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 20:49:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f3e489f476902259b1bc1a369e63e4809cc22574b7c0c9d7b9fb0a1ca5124`  
		Last Modified: Wed, 15 Apr 2026 20:52:28 GMT  
		Size: 252.0 MB (251996977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd763d85262711f9837b628e3300d4935048ad99b8de3992a4fb29fa9f25c`  
		Last Modified: Wed, 15 Apr 2026 20:52:18 GMT  
		Size: 14.3 MB (14340843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8355eee5c2271a157cd610a9d3d833d13f83cc5f93349ad0e991202f0d5d5`  
		Last Modified: Wed, 15 Apr 2026 20:52:17 GMT  
		Size: 481.3 KB (481292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3373fccc9b39bc95f6c8fe75ab832c594126aa9f0b97ef7c45eba05b36c20a8f`  
		Last Modified: Wed, 15 Apr 2026 20:52:31 GMT  
		Size: 403.5 MB (403517357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b3bec6120f3993e425e937df871efe1fe55cb9b3b215456296b98b7a55b3b5`  
		Last Modified: Wed, 15 Apr 2026 20:52:18 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140fc9b0365e2b42fc087bbfb151f1acc84a2a98ae3a4d81bddf5c593bbc59d0`  
		Last Modified: Wed, 15 Apr 2026 20:52:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25abd3207920dd469e960eae98e11e44f77c87c176b6fa71043c41cde68642e5`  
		Last Modified: Wed, 15 Apr 2026 20:52:20 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baea3afe04b0d7a9325fce3ea62ed44eac45e665c4dd7bfda8ad6b0f66af848f`  
		Last Modified: Wed, 15 Apr 2026 20:52:21 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:308a050c74211c7285f0b974d3a33d31b10c41a1b7ae69a98dc43ed381c580d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70021424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261935b51308992317a71304703ebbb4364ea334cfabdaecf74b8e417c41c103`

```dockerfile
```

-	Layers:
	-	`sha256:0ca8ad645980fc26d92ab6c47b5dd33a2f9486fa53cf3fe1790b21371bdce16c`  
		Last Modified: Wed, 15 Apr 2026 20:52:23 GMT  
		Size: 70.0 MB (69994168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02593a4bab326b36fbb467b3dff444e7294144d4ceb74598f1e995d53793306d`  
		Last Modified: Wed, 15 Apr 2026 20:52:17 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:087480bffa7e68cc5dddd001504af53923ee4aa1f4b665eef5108bf77aab2087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.0 MB (719013665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139ed7eccbe507c9454de569ec64657032216848e6b617d055a7c2c6ee104a99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260409
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
# Wed, 15 Apr 2026 22:11:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Apr 2026 22:11:49 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260409 ODOO_SHA=1b856fbdb3e1f62e695d53e0642ba4bbf03859b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Apr 2026 22:11:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Apr 2026 22:11:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Apr 2026 22:11:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Apr 2026 22:11:50 GMT
USER odoo
# Wed, 15 Apr 2026 22:11:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Apr 2026 22:11:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388d300d3e84719cea202904a8e5ca0786e9fea0d6d4d6858f3da33405553073`  
		Last Modified: Wed, 15 Apr 2026 22:17:52 GMT  
		Size: 404.2 MB (404211454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7432b5a45562f2f4c3b31e2fedd997d7635ebdcc7c279dbddd2662476a35911b`  
		Last Modified: Wed, 15 Apr 2026 22:17:39 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ba7b9ff260f0c5bde6d56479d191cc96520d4657d9f1ac5bb5b3d593ff58f8`  
		Last Modified: Wed, 15 Apr 2026 22:17:40 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f381381dd7596b8eddbd9df8b74602e34d0e8453863a22ab0dc1cb37833dce`  
		Last Modified: Wed, 15 Apr 2026 22:17:40 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871085cd3fd32e086680453022914a22a3391e0851d133c92366e39c5d6216c2`  
		Last Modified: Wed, 15 Apr 2026 22:17:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:3c23d345179d740cb0f19de9c2a0c8e48b04716294860f54fa9214d82099b7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70022425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d3e0665e4db8d1045fd4a44596ba2894e685052865fc8e4368f58424085d54`

```dockerfile
```

-	Layers:
	-	`sha256:b3b85b8c5e943bccb0dd3d10303ba0969576284ba049b5787b3882d4cb760575`  
		Last Modified: Wed, 15 Apr 2026 22:17:42 GMT  
		Size: 70.0 MB (69995270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b50952403bf0f989c877184390e524e43cd625037b5be1d156be2dd0be0db43`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json
