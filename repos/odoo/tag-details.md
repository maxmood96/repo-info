<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250918`](#odoo170-20250918)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250918`](#odoo180-20250918)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20250918`](#odoo190-20250918)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:673a64d7e1aaf80f8848fe5026b8c7a6b93888c9da3a9559e2ffb002156f0e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:6f128fc6ce35133df3a12438380378f4dd3f7ffbecd6a776c80f655df5e7e64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.1 MB (605117262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a786cbbef5ed00de19e89017d4d87b926886a0d1e3367a37220a57e480c40919`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=amd64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=17.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f2db8198b7c9b882a15cf6ddc365ce1fd7b0fd181db4a03885304388e3ed`  
		Last Modified: Thu, 18 Sep 2025 19:12:28 GMT  
		Size: 233.8 MB (233788154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c8775490da425b7e21f1e49fd3c343e34920291f42776ab5ab459565937411`  
		Last Modified: Thu, 18 Sep 2025 19:11:27 GMT  
		Size: 2.5 MB (2532437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ded446a145b21f5f4cdced5faeb7e24e62e804fe6d38203e1b015c9c5d9d0c0`  
		Last Modified: Thu, 18 Sep 2025 19:11:30 GMT  
		Size: 481.2 KB (481248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116ebf0b72f5eba069ca641e44b96e0e1b6bf84b8888debbfe223ad005bfd182`  
		Last Modified: Thu, 18 Sep 2025 19:11:55 GMT  
		Size: 338.8 MB (338776048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e5636e4fcebd1ca3c2e8c0fe9da19aebea2ccabbefb3cd757237c0451b981c`  
		Last Modified: Thu, 18 Sep 2025 19:11:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76b8f66d547059fc4fea9380002712ec592da8305f5d67acf790da8051c212f`  
		Last Modified: Thu, 18 Sep 2025 19:11:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daf8575a6de3f842911dfd1afa89dcdcdbc11fadbba90cfa8252f7e14a15ee3`  
		Last Modified: Thu, 18 Sep 2025 19:11:30 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2157ba1c663003be09a2a2c33a5fd146f27cbb004da01fc68b1bf20195af2e96`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:1949ce9c1ba8a6fc71c6bb04a2f598ab1e105ab3149c21ce9b1966a62b236e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41481489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c796e506bebf05ea9ab519fcb13f9797719815733ac273b0155cee06d5aaa8f`

```dockerfile
```

-	Layers:
	-	`sha256:34470f0e4f27bdf174f9f7f0507007808c2006e7f3b7230b1533f80e38ae0132`  
		Last Modified: Thu, 18 Sep 2025 19:12:30 GMT  
		Size: 41.5 MB (41454654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4ae62231af566459b488bbe949671ae2443686b0c9e47729b5e2fefe01aa188`  
		Last Modified: Thu, 18 Sep 2025 19:12:32 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:cdd33bea26fc1f4a877c560c6f22b27431729bc6e9efb42bb5b988d610a7469d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599903358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8ac1a041eadb6e3c7dff51e9d6266513ce9e5c9b63b1dc0e5fe5420c0df11e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=17.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0af3946187b52df9bb21ca2713b1b174d8c8982bbfb8efe6adb00424b46b83`  
		Last Modified: Thu, 18 Sep 2025 19:13:55 GMT  
		Size: 231.2 MB (231161126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97620292b0a4e9b1a99b6167939d6468b0d59edc2eb4f8f0dee10e7324cd7d16`  
		Last Modified: Thu, 18 Sep 2025 19:04:52 GMT  
		Size: 2.5 MB (2521508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8b0a546491dc8896852597210e73f86097733ac77891f99f709d8ec1a61ccb`  
		Last Modified: Thu, 18 Sep 2025 19:04:52 GMT  
		Size: 481.3 KB (481251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04875e21b98e3749d2b3171a5a72d6d9d14751b037aed370c26c3573ee5fbda9`  
		Last Modified: Thu, 18 Sep 2025 19:14:24 GMT  
		Size: 338.4 MB (338375564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7368013eaf0296809510e70772020221d4d9cb5ab6138690a7f2bd3e0c27bce`  
		Last Modified: Thu, 18 Sep 2025 19:04:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a61accb0ef02d1397b3d058df4a9a9f16c6879545aeca666b2f1b9ba2ad55`  
		Last Modified: Thu, 18 Sep 2025 19:04:53 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38896011bef64c25122d6f013c9893348822bb84efd8d9e5ebe2fbf773cf0cb`  
		Last Modified: Thu, 18 Sep 2025 19:04:54 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7c475a492e5ce20aadc72ac7a8ead4f540f95d957adfc94d04b4f9b0af82ac`  
		Last Modified: Thu, 18 Sep 2025 19:04:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:d3434415c361f06faf39bd4b3bd98d79d94a69182e8971cec1660bd26d47738c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41488148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f3dc0cf1612097c604ea168d2c325947f039e157115f13a309235531d2c706`

```dockerfile
```

-	Layers:
	-	`sha256:cb049bb71dd0500fd5ff2448e0e31366b24296fb582e154701dd796b6dc8e38e`  
		Last Modified: Thu, 18 Sep 2025 19:13:26 GMT  
		Size: 41.5 MB (41461161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4615c42bb02b9ea7b2c202f6775c688aebbb39c2e178fa82007ddd5769099f69`  
		Last Modified: Thu, 18 Sep 2025 19:13:27 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:673a64d7e1aaf80f8848fe5026b8c7a6b93888c9da3a9559e2ffb002156f0e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:6f128fc6ce35133df3a12438380378f4dd3f7ffbecd6a776c80f655df5e7e64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.1 MB (605117262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a786cbbef5ed00de19e89017d4d87b926886a0d1e3367a37220a57e480c40919`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=amd64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=17.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f2db8198b7c9b882a15cf6ddc365ce1fd7b0fd181db4a03885304388e3ed`  
		Last Modified: Thu, 18 Sep 2025 19:12:28 GMT  
		Size: 233.8 MB (233788154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c8775490da425b7e21f1e49fd3c343e34920291f42776ab5ab459565937411`  
		Last Modified: Thu, 18 Sep 2025 19:11:27 GMT  
		Size: 2.5 MB (2532437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ded446a145b21f5f4cdced5faeb7e24e62e804fe6d38203e1b015c9c5d9d0c0`  
		Last Modified: Thu, 18 Sep 2025 19:11:30 GMT  
		Size: 481.2 KB (481248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116ebf0b72f5eba069ca641e44b96e0e1b6bf84b8888debbfe223ad005bfd182`  
		Last Modified: Thu, 18 Sep 2025 19:11:55 GMT  
		Size: 338.8 MB (338776048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e5636e4fcebd1ca3c2e8c0fe9da19aebea2ccabbefb3cd757237c0451b981c`  
		Last Modified: Thu, 18 Sep 2025 19:11:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76b8f66d547059fc4fea9380002712ec592da8305f5d67acf790da8051c212f`  
		Last Modified: Thu, 18 Sep 2025 19:11:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daf8575a6de3f842911dfd1afa89dcdcdbc11fadbba90cfa8252f7e14a15ee3`  
		Last Modified: Thu, 18 Sep 2025 19:11:30 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2157ba1c663003be09a2a2c33a5fd146f27cbb004da01fc68b1bf20195af2e96`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1949ce9c1ba8a6fc71c6bb04a2f598ab1e105ab3149c21ce9b1966a62b236e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41481489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c796e506bebf05ea9ab519fcb13f9797719815733ac273b0155cee06d5aaa8f`

```dockerfile
```

-	Layers:
	-	`sha256:34470f0e4f27bdf174f9f7f0507007808c2006e7f3b7230b1533f80e38ae0132`  
		Last Modified: Thu, 18 Sep 2025 19:12:30 GMT  
		Size: 41.5 MB (41454654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4ae62231af566459b488bbe949671ae2443686b0c9e47729b5e2fefe01aa188`  
		Last Modified: Thu, 18 Sep 2025 19:12:32 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:cdd33bea26fc1f4a877c560c6f22b27431729bc6e9efb42bb5b988d610a7469d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599903358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8ac1a041eadb6e3c7dff51e9d6266513ce9e5c9b63b1dc0e5fe5420c0df11e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=17.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0af3946187b52df9bb21ca2713b1b174d8c8982bbfb8efe6adb00424b46b83`  
		Last Modified: Thu, 18 Sep 2025 19:13:55 GMT  
		Size: 231.2 MB (231161126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97620292b0a4e9b1a99b6167939d6468b0d59edc2eb4f8f0dee10e7324cd7d16`  
		Last Modified: Thu, 18 Sep 2025 19:04:52 GMT  
		Size: 2.5 MB (2521508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8b0a546491dc8896852597210e73f86097733ac77891f99f709d8ec1a61ccb`  
		Last Modified: Thu, 18 Sep 2025 19:04:52 GMT  
		Size: 481.3 KB (481251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04875e21b98e3749d2b3171a5a72d6d9d14751b037aed370c26c3573ee5fbda9`  
		Last Modified: Thu, 18 Sep 2025 19:14:24 GMT  
		Size: 338.4 MB (338375564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7368013eaf0296809510e70772020221d4d9cb5ab6138690a7f2bd3e0c27bce`  
		Last Modified: Thu, 18 Sep 2025 19:04:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a61accb0ef02d1397b3d058df4a9a9f16c6879545aeca666b2f1b9ba2ad55`  
		Last Modified: Thu, 18 Sep 2025 19:04:53 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38896011bef64c25122d6f013c9893348822bb84efd8d9e5ebe2fbf773cf0cb`  
		Last Modified: Thu, 18 Sep 2025 19:04:54 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7c475a492e5ce20aadc72ac7a8ead4f540f95d957adfc94d04b4f9b0af82ac`  
		Last Modified: Thu, 18 Sep 2025 19:04:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d3434415c361f06faf39bd4b3bd98d79d94a69182e8971cec1660bd26d47738c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41488148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f3dc0cf1612097c604ea168d2c325947f039e157115f13a309235531d2c706`

```dockerfile
```

-	Layers:
	-	`sha256:cb049bb71dd0500fd5ff2448e0e31366b24296fb582e154701dd796b6dc8e38e`  
		Last Modified: Thu, 18 Sep 2025 19:13:26 GMT  
		Size: 41.5 MB (41461161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4615c42bb02b9ea7b2c202f6775c688aebbb39c2e178fa82007ddd5769099f69`  
		Last Modified: Thu, 18 Sep 2025 19:13:27 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250918`

```console
$ docker pull odoo@sha256:673a64d7e1aaf80f8848fe5026b8c7a6b93888c9da3a9559e2ffb002156f0e63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20250918` - linux; amd64

```console
$ docker pull odoo@sha256:6f128fc6ce35133df3a12438380378f4dd3f7ffbecd6a776c80f655df5e7e64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.1 MB (605117262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a786cbbef5ed00de19e89017d4d87b926886a0d1e3367a37220a57e480c40919`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=amd64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=17.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f2db8198b7c9b882a15cf6ddc365ce1fd7b0fd181db4a03885304388e3ed`  
		Last Modified: Thu, 18 Sep 2025 19:12:28 GMT  
		Size: 233.8 MB (233788154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c8775490da425b7e21f1e49fd3c343e34920291f42776ab5ab459565937411`  
		Last Modified: Thu, 18 Sep 2025 19:11:27 GMT  
		Size: 2.5 MB (2532437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ded446a145b21f5f4cdced5faeb7e24e62e804fe6d38203e1b015c9c5d9d0c0`  
		Last Modified: Thu, 18 Sep 2025 19:11:30 GMT  
		Size: 481.2 KB (481248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116ebf0b72f5eba069ca641e44b96e0e1b6bf84b8888debbfe223ad005bfd182`  
		Last Modified: Thu, 18 Sep 2025 19:11:55 GMT  
		Size: 338.8 MB (338776048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e5636e4fcebd1ca3c2e8c0fe9da19aebea2ccabbefb3cd757237c0451b981c`  
		Last Modified: Thu, 18 Sep 2025 19:11:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76b8f66d547059fc4fea9380002712ec592da8305f5d67acf790da8051c212f`  
		Last Modified: Thu, 18 Sep 2025 19:11:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daf8575a6de3f842911dfd1afa89dcdcdbc11fadbba90cfa8252f7e14a15ee3`  
		Last Modified: Thu, 18 Sep 2025 19:11:30 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2157ba1c663003be09a2a2c33a5fd146f27cbb004da01fc68b1bf20195af2e96`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250918` - unknown; unknown

```console
$ docker pull odoo@sha256:1949ce9c1ba8a6fc71c6bb04a2f598ab1e105ab3149c21ce9b1966a62b236e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41481489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c796e506bebf05ea9ab519fcb13f9797719815733ac273b0155cee06d5aaa8f`

```dockerfile
```

-	Layers:
	-	`sha256:34470f0e4f27bdf174f9f7f0507007808c2006e7f3b7230b1533f80e38ae0132`  
		Last Modified: Thu, 18 Sep 2025 19:12:30 GMT  
		Size: 41.5 MB (41454654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4ae62231af566459b488bbe949671ae2443686b0c9e47729b5e2fefe01aa188`  
		Last Modified: Thu, 18 Sep 2025 19:12:32 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250918` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:cdd33bea26fc1f4a877c560c6f22b27431729bc6e9efb42bb5b988d610a7469d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.9 MB (599903358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8ac1a041eadb6e3c7dff51e9d6266513ce9e5c9b63b1dc0e5fe5420c0df11e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=17.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=476f97c93065c284b6b984266e70abce2c0c7b54
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0af3946187b52df9bb21ca2713b1b174d8c8982bbfb8efe6adb00424b46b83`  
		Last Modified: Thu, 18 Sep 2025 19:13:55 GMT  
		Size: 231.2 MB (231161126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97620292b0a4e9b1a99b6167939d6468b0d59edc2eb4f8f0dee10e7324cd7d16`  
		Last Modified: Thu, 18 Sep 2025 19:04:52 GMT  
		Size: 2.5 MB (2521508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8b0a546491dc8896852597210e73f86097733ac77891f99f709d8ec1a61ccb`  
		Last Modified: Thu, 18 Sep 2025 19:04:52 GMT  
		Size: 481.3 KB (481251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04875e21b98e3749d2b3171a5a72d6d9d14751b037aed370c26c3573ee5fbda9`  
		Last Modified: Thu, 18 Sep 2025 19:14:24 GMT  
		Size: 338.4 MB (338375564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7368013eaf0296809510e70772020221d4d9cb5ab6138690a7f2bd3e0c27bce`  
		Last Modified: Thu, 18 Sep 2025 19:04:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a61accb0ef02d1397b3d058df4a9a9f16c6879545aeca666b2f1b9ba2ad55`  
		Last Modified: Thu, 18 Sep 2025 19:04:53 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38896011bef64c25122d6f013c9893348822bb84efd8d9e5ebe2fbf773cf0cb`  
		Last Modified: Thu, 18 Sep 2025 19:04:54 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7c475a492e5ce20aadc72ac7a8ead4f540f95d957adfc94d04b4f9b0af82ac`  
		Last Modified: Thu, 18 Sep 2025 19:04:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250918` - unknown; unknown

```console
$ docker pull odoo@sha256:d3434415c361f06faf39bd4b3bd98d79d94a69182e8971cec1660bd26d47738c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41488148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f3dc0cf1612097c604ea168d2c325947f039e157115f13a309235531d2c706`

```dockerfile
```

-	Layers:
	-	`sha256:cb049bb71dd0500fd5ff2448e0e31366b24296fb582e154701dd796b6dc8e38e`  
		Last Modified: Thu, 18 Sep 2025 19:13:26 GMT  
		Size: 41.5 MB (41461161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4615c42bb02b9ea7b2c202f6775c688aebbb39c2e178fa82007ddd5769099f69`  
		Last Modified: Thu, 18 Sep 2025 19:13:27 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:9a4c6e7a11eb094976433a7cfb0ea4a7f15fd5caa3b987286584de50ad26cb82
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
$ docker pull odoo@sha256:c874155dc2963c8d797ae0f9a9f33dc2e8c081a8540fb6a76e3b721952095742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.5 MB (676526752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ced2244a138c21fb688286ae51be4d82e9bbb087a8e070e5d255753352d9151`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=amd64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=18.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4481ae80980fa48ef62c23e017433bd9cbcc726cd6c1201a19f8d8f066b89e4e`  
		Last Modified: Thu, 18 Sep 2025 19:13:03 GMT  
		Size: 254.5 MB (254530142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a0b4d5d603f3da061550d1a626287b3fe9a7771d5325c55b8268ffa0b92e7d`  
		Last Modified: Thu, 18 Sep 2025 19:05:53 GMT  
		Size: 14.3 MB (14286423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92732af09bf5a263e98877d39856b71c72711399d3e709422c8cc9bb5b71a54`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 481.0 KB (480963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f96389feaf3d07d297f092f30a1e6576b0ded0a594a87816214c7dcd880876d`  
		Last Modified: Thu, 18 Sep 2025 19:12:58 GMT  
		Size: 377.5 MB (377503336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59c0edaa9f7771c73d9451bf19f38685f0957642bc844b4d718c55dc806712`  
		Last Modified: Thu, 18 Sep 2025 19:05:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73859954b79e6fd7a208e21bf8ed9481388c7f555c70535640c838181cf32581`  
		Last Modified: Thu, 18 Sep 2025 19:05:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d0490225bc77e59a0d7f4228ead376df0c6ca832df65e7eac7dd3cbbe8e125`  
		Last Modified: Thu, 18 Sep 2025 19:05:51 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6596e0ae25321237c02702d67b6c08a653dc2fc62b04902a609851dfafdd8672`  
		Last Modified: Thu, 18 Sep 2025 19:05:51 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:c9fc87adb77bc5022a46e89ef00ad474a24ab2d5707533c2421d9acbe0e5d64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60926071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ab33e639f39967e353afa480c4996bb19d2e0fa525d13f6f4402b4cf20e6b0`

```dockerfile
```

-	Layers:
	-	`sha256:69cc370288414d0d9e9291111dba95b103082896df4da308888e5a84ba62c930`  
		Last Modified: Thu, 18 Sep 2025 19:12:46 GMT  
		Size: 60.9 MB (60899230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a6169ceeee3ae08016fc30c775178af0ef4e2e9c37653ed59c9f54433a6cc4d`  
		Last Modified: Thu, 18 Sep 2025 19:12:48 GMT  
		Size: 26.8 KB (26841 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a97e29fdc50bf6ed2738af08d5967bc3774bb312d0d2a40926e7dcc37c58eee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 MB (672859386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b1fd69299877af080877e444a708e203f04127fdd8c5fb68d01df1083e0ab9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=18.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3a6d053a570812ace1190bb458e68c3ad521f2f44fab26bcfe50a3d96d2317`  
		Last Modified: Thu, 18 Sep 2025 19:11:09 GMT  
		Size: 251.9 MB (251920107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54993715cb009df3afb88fe2e60f30258ced84577c1c4ca8dd89ee76be7237c`  
		Last Modified: Thu, 18 Sep 2025 19:05:55 GMT  
		Size: 14.3 MB (14263328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876e1f734147ae19637596f3ca841f4c9b0bda7b15f4d3f4741eeff2bd621d2`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 481.0 KB (481039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de81b36cc2f1bcf4ca7b2d423215a6204dc47bdebb50d9b2274498624200ece`  
		Last Modified: Thu, 18 Sep 2025 19:11:53 GMT  
		Size: 377.3 MB (377331160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc893b56c09bf225da1e9f352a791b2f62af4bcb1e2df93f0b28c224e96163d3`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53dc2c9338b283567f17c4f2be4a15844d34afd988286234599487e757de77c`  
		Last Modified: Thu, 18 Sep 2025 19:05:53 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5abecbfa71b32a8d400da8cb347861d198af77ab3291ddc1601f058b5c0d2b`  
		Last Modified: Thu, 18 Sep 2025 19:05:53 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ee3eb0f3e820bd55225f5124c9c08be3b6a8181f984f754f673f717b71501a`  
		Last Modified: Thu, 18 Sep 2025 19:05:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:d660cfba5b5bd98ee6e746dd3627882ade593bad347302fd86c97d15f972f080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60933499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8692fd95001884b69260379870661aded9135b3f882e87f8f8fae6b29c5a0cf5`

```dockerfile
```

-	Layers:
	-	`sha256:00ac6ea860dcfe64a791ecc214c58a4d871c28c5fa4f7d8628b0815c78c99f46`  
		Last Modified: Thu, 18 Sep 2025 19:14:27 GMT  
		Size: 60.9 MB (60906505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629f014b1b2ae240e89c895aedf98ef5c0f1d70be84853fa72fce68878103cfb`  
		Last Modified: Thu, 18 Sep 2025 19:14:28 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:1ea8e6b87e33903a37d8184b875587564401aee9b718e359e9747c401943ba23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.7 MB (692714949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c078b0b24f174f3742bebfd9ece821a18a684f3d0076a8079b8454a7ce8edf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=ppc64le
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=18.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483929c4f2f077e54a74531d873099c888fbbefefab480aec6143eeac4b0a981`  
		Last Modified: Thu, 18 Sep 2025 19:09:48 GMT  
		Size: 378.0 MB (378039171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecb6f25dd7fcf67cb4c510e5bad670fda04157e1d1ef47ade35f2280844cdcb`  
		Last Modified: Thu, 18 Sep 2025 19:06:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1524bc775fa8bf45939a39195e79414363b2a24048a25d032e0eaa8ba95212ee`  
		Last Modified: Thu, 18 Sep 2025 19:06:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fc835a5499c5fbb74cb38f2ee0da910d8d7575ce974900a3b73f329165683c`  
		Last Modified: Thu, 18 Sep 2025 19:06:55 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca70ee9eaac68f92f2ab457338e9094e216a9afc54a67120c51b93eee909b0a7`  
		Last Modified: Thu, 18 Sep 2025 19:06:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:cb88912076dcfdf8d83fe6b40c9f402114e936587ebf3a2f7215213873cff645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60934511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fec01cf8330b81cf510bb8fdee54641282eb4048f22c8515e7c8c0ee2d0415`

```dockerfile
```

-	Layers:
	-	`sha256:cc4ffb36059dafcd91edc728121c26a9581f66a5caab4dd025cc94d4726c018c`  
		Last Modified: Thu, 18 Sep 2025 19:16:17 GMT  
		Size: 60.9 MB (60907613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea0552ae0be32e8a92901e3f81f33b2442ca13218788735736cb21be301f5d6`  
		Last Modified: Thu, 18 Sep 2025 19:16:18 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:9a4c6e7a11eb094976433a7cfb0ea4a7f15fd5caa3b987286584de50ad26cb82
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
$ docker pull odoo@sha256:c874155dc2963c8d797ae0f9a9f33dc2e8c081a8540fb6a76e3b721952095742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.5 MB (676526752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ced2244a138c21fb688286ae51be4d82e9bbb087a8e070e5d255753352d9151`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=amd64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=18.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4481ae80980fa48ef62c23e017433bd9cbcc726cd6c1201a19f8d8f066b89e4e`  
		Last Modified: Thu, 18 Sep 2025 19:13:03 GMT  
		Size: 254.5 MB (254530142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a0b4d5d603f3da061550d1a626287b3fe9a7771d5325c55b8268ffa0b92e7d`  
		Last Modified: Thu, 18 Sep 2025 19:05:53 GMT  
		Size: 14.3 MB (14286423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92732af09bf5a263e98877d39856b71c72711399d3e709422c8cc9bb5b71a54`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 481.0 KB (480963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f96389feaf3d07d297f092f30a1e6576b0ded0a594a87816214c7dcd880876d`  
		Last Modified: Thu, 18 Sep 2025 19:12:58 GMT  
		Size: 377.5 MB (377503336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59c0edaa9f7771c73d9451bf19f38685f0957642bc844b4d718c55dc806712`  
		Last Modified: Thu, 18 Sep 2025 19:05:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73859954b79e6fd7a208e21bf8ed9481388c7f555c70535640c838181cf32581`  
		Last Modified: Thu, 18 Sep 2025 19:05:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d0490225bc77e59a0d7f4228ead376df0c6ca832df65e7eac7dd3cbbe8e125`  
		Last Modified: Thu, 18 Sep 2025 19:05:51 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6596e0ae25321237c02702d67b6c08a653dc2fc62b04902a609851dfafdd8672`  
		Last Modified: Thu, 18 Sep 2025 19:05:51 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c9fc87adb77bc5022a46e89ef00ad474a24ab2d5707533c2421d9acbe0e5d64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60926071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ab33e639f39967e353afa480c4996bb19d2e0fa525d13f6f4402b4cf20e6b0`

```dockerfile
```

-	Layers:
	-	`sha256:69cc370288414d0d9e9291111dba95b103082896df4da308888e5a84ba62c930`  
		Last Modified: Thu, 18 Sep 2025 19:12:46 GMT  
		Size: 60.9 MB (60899230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a6169ceeee3ae08016fc30c775178af0ef4e2e9c37653ed59c9f54433a6cc4d`  
		Last Modified: Thu, 18 Sep 2025 19:12:48 GMT  
		Size: 26.8 KB (26841 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a97e29fdc50bf6ed2738af08d5967bc3774bb312d0d2a40926e7dcc37c58eee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 MB (672859386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b1fd69299877af080877e444a708e203f04127fdd8c5fb68d01df1083e0ab9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=18.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3a6d053a570812ace1190bb458e68c3ad521f2f44fab26bcfe50a3d96d2317`  
		Last Modified: Thu, 18 Sep 2025 19:11:09 GMT  
		Size: 251.9 MB (251920107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54993715cb009df3afb88fe2e60f30258ced84577c1c4ca8dd89ee76be7237c`  
		Last Modified: Thu, 18 Sep 2025 19:05:55 GMT  
		Size: 14.3 MB (14263328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876e1f734147ae19637596f3ca841f4c9b0bda7b15f4d3f4741eeff2bd621d2`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 481.0 KB (481039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de81b36cc2f1bcf4ca7b2d423215a6204dc47bdebb50d9b2274498624200ece`  
		Last Modified: Thu, 18 Sep 2025 19:11:53 GMT  
		Size: 377.3 MB (377331160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc893b56c09bf225da1e9f352a791b2f62af4bcb1e2df93f0b28c224e96163d3`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53dc2c9338b283567f17c4f2be4a15844d34afd988286234599487e757de77c`  
		Last Modified: Thu, 18 Sep 2025 19:05:53 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5abecbfa71b32a8d400da8cb347861d198af77ab3291ddc1601f058b5c0d2b`  
		Last Modified: Thu, 18 Sep 2025 19:05:53 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ee3eb0f3e820bd55225f5124c9c08be3b6a8181f984f754f673f717b71501a`  
		Last Modified: Thu, 18 Sep 2025 19:05:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d660cfba5b5bd98ee6e746dd3627882ade593bad347302fd86c97d15f972f080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60933499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8692fd95001884b69260379870661aded9135b3f882e87f8f8fae6b29c5a0cf5`

```dockerfile
```

-	Layers:
	-	`sha256:00ac6ea860dcfe64a791ecc214c58a4d871c28c5fa4f7d8628b0815c78c99f46`  
		Last Modified: Thu, 18 Sep 2025 19:14:27 GMT  
		Size: 60.9 MB (60906505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629f014b1b2ae240e89c895aedf98ef5c0f1d70be84853fa72fce68878103cfb`  
		Last Modified: Thu, 18 Sep 2025 19:14:28 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:1ea8e6b87e33903a37d8184b875587564401aee9b718e359e9747c401943ba23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.7 MB (692714949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c078b0b24f174f3742bebfd9ece821a18a684f3d0076a8079b8454a7ce8edf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=ppc64le
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=18.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483929c4f2f077e54a74531d873099c888fbbefefab480aec6143eeac4b0a981`  
		Last Modified: Thu, 18 Sep 2025 19:09:48 GMT  
		Size: 378.0 MB (378039171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecb6f25dd7fcf67cb4c510e5bad670fda04157e1d1ef47ade35f2280844cdcb`  
		Last Modified: Thu, 18 Sep 2025 19:06:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1524bc775fa8bf45939a39195e79414363b2a24048a25d032e0eaa8ba95212ee`  
		Last Modified: Thu, 18 Sep 2025 19:06:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fc835a5499c5fbb74cb38f2ee0da910d8d7575ce974900a3b73f329165683c`  
		Last Modified: Thu, 18 Sep 2025 19:06:55 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca70ee9eaac68f92f2ab457338e9094e216a9afc54a67120c51b93eee909b0a7`  
		Last Modified: Thu, 18 Sep 2025 19:06:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cb88912076dcfdf8d83fe6b40c9f402114e936587ebf3a2f7215213873cff645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60934511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fec01cf8330b81cf510bb8fdee54641282eb4048f22c8515e7c8c0ee2d0415`

```dockerfile
```

-	Layers:
	-	`sha256:cc4ffb36059dafcd91edc728121c26a9581f66a5caab4dd025cc94d4726c018c`  
		Last Modified: Thu, 18 Sep 2025 19:16:17 GMT  
		Size: 60.9 MB (60907613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea0552ae0be32e8a92901e3f81f33b2442ca13218788735736cb21be301f5d6`  
		Last Modified: Thu, 18 Sep 2025 19:16:18 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250918`

```console
$ docker pull odoo@sha256:9a4c6e7a11eb094976433a7cfb0ea4a7f15fd5caa3b987286584de50ad26cb82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250918` - linux; amd64

```console
$ docker pull odoo@sha256:c874155dc2963c8d797ae0f9a9f33dc2e8c081a8540fb6a76e3b721952095742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.5 MB (676526752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ced2244a138c21fb688286ae51be4d82e9bbb087a8e070e5d255753352d9151`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=amd64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=18.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4481ae80980fa48ef62c23e017433bd9cbcc726cd6c1201a19f8d8f066b89e4e`  
		Last Modified: Thu, 18 Sep 2025 19:13:03 GMT  
		Size: 254.5 MB (254530142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a0b4d5d603f3da061550d1a626287b3fe9a7771d5325c55b8268ffa0b92e7d`  
		Last Modified: Thu, 18 Sep 2025 19:05:53 GMT  
		Size: 14.3 MB (14286423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92732af09bf5a263e98877d39856b71c72711399d3e709422c8cc9bb5b71a54`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 481.0 KB (480963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f96389feaf3d07d297f092f30a1e6576b0ded0a594a87816214c7dcd880876d`  
		Last Modified: Thu, 18 Sep 2025 19:12:58 GMT  
		Size: 377.5 MB (377503336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59c0edaa9f7771c73d9451bf19f38685f0957642bc844b4d718c55dc806712`  
		Last Modified: Thu, 18 Sep 2025 19:05:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73859954b79e6fd7a208e21bf8ed9481388c7f555c70535640c838181cf32581`  
		Last Modified: Thu, 18 Sep 2025 19:05:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d0490225bc77e59a0d7f4228ead376df0c6ca832df65e7eac7dd3cbbe8e125`  
		Last Modified: Thu, 18 Sep 2025 19:05:51 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6596e0ae25321237c02702d67b6c08a653dc2fc62b04902a609851dfafdd8672`  
		Last Modified: Thu, 18 Sep 2025 19:05:51 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250918` - unknown; unknown

```console
$ docker pull odoo@sha256:c9fc87adb77bc5022a46e89ef00ad474a24ab2d5707533c2421d9acbe0e5d64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60926071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ab33e639f39967e353afa480c4996bb19d2e0fa525d13f6f4402b4cf20e6b0`

```dockerfile
```

-	Layers:
	-	`sha256:69cc370288414d0d9e9291111dba95b103082896df4da308888e5a84ba62c930`  
		Last Modified: Thu, 18 Sep 2025 19:12:46 GMT  
		Size: 60.9 MB (60899230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a6169ceeee3ae08016fc30c775178af0ef4e2e9c37653ed59c9f54433a6cc4d`  
		Last Modified: Thu, 18 Sep 2025 19:12:48 GMT  
		Size: 26.8 KB (26841 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250918` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a97e29fdc50bf6ed2738af08d5967bc3774bb312d0d2a40926e7dcc37c58eee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 MB (672859386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b1fd69299877af080877e444a708e203f04127fdd8c5fb68d01df1083e0ab9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=18.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3a6d053a570812ace1190bb458e68c3ad521f2f44fab26bcfe50a3d96d2317`  
		Last Modified: Thu, 18 Sep 2025 19:11:09 GMT  
		Size: 251.9 MB (251920107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54993715cb009df3afb88fe2e60f30258ced84577c1c4ca8dd89ee76be7237c`  
		Last Modified: Thu, 18 Sep 2025 19:05:55 GMT  
		Size: 14.3 MB (14263328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a876e1f734147ae19637596f3ca841f4c9b0bda7b15f4d3f4741eeff2bd621d2`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 481.0 KB (481039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de81b36cc2f1bcf4ca7b2d423215a6204dc47bdebb50d9b2274498624200ece`  
		Last Modified: Thu, 18 Sep 2025 19:11:53 GMT  
		Size: 377.3 MB (377331160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc893b56c09bf225da1e9f352a791b2f62af4bcb1e2df93f0b28c224e96163d3`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53dc2c9338b283567f17c4f2be4a15844d34afd988286234599487e757de77c`  
		Last Modified: Thu, 18 Sep 2025 19:05:53 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5abecbfa71b32a8d400da8cb347861d198af77ab3291ddc1601f058b5c0d2b`  
		Last Modified: Thu, 18 Sep 2025 19:05:53 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ee3eb0f3e820bd55225f5124c9c08be3b6a8181f984f754f673f717b71501a`  
		Last Modified: Thu, 18 Sep 2025 19:05:54 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250918` - unknown; unknown

```console
$ docker pull odoo@sha256:d660cfba5b5bd98ee6e746dd3627882ade593bad347302fd86c97d15f972f080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60933499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8692fd95001884b69260379870661aded9135b3f882e87f8f8fae6b29c5a0cf5`

```dockerfile
```

-	Layers:
	-	`sha256:00ac6ea860dcfe64a791ecc214c58a4d871c28c5fa4f7d8628b0815c78c99f46`  
		Last Modified: Thu, 18 Sep 2025 19:14:27 GMT  
		Size: 60.9 MB (60906505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629f014b1b2ae240e89c895aedf98ef5c0f1d70be84853fa72fce68878103cfb`  
		Last Modified: Thu, 18 Sep 2025 19:14:28 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250918` - linux; ppc64le

```console
$ docker pull odoo@sha256:1ea8e6b87e33903a37d8184b875587564401aee9b718e359e9747c401943ba23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.7 MB (692714949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c078b0b24f174f3742bebfd9ece821a18a684f3d0076a8079b8454a7ce8edf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=ppc64le
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=18.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=87dee1ca919a9920f1ad1b4c08933052e47c0add
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483929c4f2f077e54a74531d873099c888fbbefefab480aec6143eeac4b0a981`  
		Last Modified: Thu, 18 Sep 2025 19:09:48 GMT  
		Size: 378.0 MB (378039171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecb6f25dd7fcf67cb4c510e5bad670fda04157e1d1ef47ade35f2280844cdcb`  
		Last Modified: Thu, 18 Sep 2025 19:06:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1524bc775fa8bf45939a39195e79414363b2a24048a25d032e0eaa8ba95212ee`  
		Last Modified: Thu, 18 Sep 2025 19:06:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fc835a5499c5fbb74cb38f2ee0da910d8d7575ce974900a3b73f329165683c`  
		Last Modified: Thu, 18 Sep 2025 19:06:55 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca70ee9eaac68f92f2ab457338e9094e216a9afc54a67120c51b93eee909b0a7`  
		Last Modified: Thu, 18 Sep 2025 19:06:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250918` - unknown; unknown

```console
$ docker pull odoo@sha256:cb88912076dcfdf8d83fe6b40c9f402114e936587ebf3a2f7215213873cff645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60934511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fec01cf8330b81cf510bb8fdee54641282eb4048f22c8515e7c8c0ee2d0415`

```dockerfile
```

-	Layers:
	-	`sha256:cc4ffb36059dafcd91edc728121c26a9581f66a5caab4dd025cc94d4726c018c`  
		Last Modified: Thu, 18 Sep 2025 19:16:17 GMT  
		Size: 60.9 MB (60907613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea0552ae0be32e8a92901e3f81f33b2442ca13218788735736cb21be301f5d6`  
		Last Modified: Thu, 18 Sep 2025 19:16:18 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:67a6c4fc312186720be9566071eb3539634925657b4e2e3d799bc5608d838851
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
$ docker pull odoo@sha256:04c3a385ae47d0838b95daa5286ad0d72089c7a1b85f97188e7974d035f457f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.1 MB (677104277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ee5d07d2946efb0ba6585064a48361514c55c365bb4306d6f42b542b111a79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=amd64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d00355c0704636cb70f98ff01b12f65450ed5e6dc31fe70e15f2ff27bb2c8a9`  
		Last Modified: Thu, 18 Sep 2025 19:13:20 GMT  
		Size: 254.5 MB (254529024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc78c74f02cfa9d2d3963124dd5d978e08b28d30a5e11f0343d2db3dde3921f`  
		Last Modified: Thu, 18 Sep 2025 19:05:57 GMT  
		Size: 14.3 MB (14286373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56feb6c70e97fc514c44672a95a22f828ed2612e2b285d5b5d4de457fb03a8dc`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 481.0 KB (480963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87b3f25613d7046f870ed5ce91c1d13974a242f633fb4488f243becb44e21c`  
		Last Modified: Thu, 18 Sep 2025 19:13:19 GMT  
		Size: 378.1 MB (378082033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b02d70d192e7d5096dfb85491069537ecc913b8ada4387cc7c3f5879d1d5cea`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a69f56c596e69044a79e013229736014f8e5010255daebd70ddaf3b224175d1`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62514748077a9159bc082dc768b58eed4537f144a0de4215b85fefb777dc0c87`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6270c89452b88c8eb784ecbeb3d97ad780327bc64f93265249a3cfe479897`  
		Last Modified: Thu, 18 Sep 2025 19:05:51 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:c9ef8855fa7792e99ebfd03f67790cf9c1f5a40371e997bfa92229d0a242032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67464009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b522bb1b6bcda8d960c82b8cad0c64cab96079d57a2f962ce75b98f71a142`

```dockerfile
```

-	Layers:
	-	`sha256:57c3bfa5117d1d92c336acb37d34d14993926ecb74c8cab9d010751841b236bc`  
		Last Modified: Thu, 18 Sep 2025 19:13:03 GMT  
		Size: 67.4 MB (67436873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c242d75a39e51ef5b0d3f186419f5e47924b7d14de0465444e72124c761b1bc8`  
		Last Modified: Thu, 18 Sep 2025 19:13:06 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ae5ecb32875a3160571979c4e065dd1532b86458eff90b1fbfcc86424d938f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.5 MB (673483666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64ac348070d41de648c01aa908579811aeb09a9be335238838254a89251a176`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2d285cc6758180abd60ae65ee5488607a2b3b1e88be78ce839d3661a36e84d`  
		Last Modified: Thu, 18 Sep 2025 21:26:36 GMT  
		Size: 251.9 MB (251920419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedfe140bb0615c2f2d7dc1ce3529ea24694b98aed59eac57a3468ace9ce3a62`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 14.3 MB (14263317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cd9e29f873040e4336fd67b8b91715755847d71b5a221864b4165aff5d7f75`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 481.0 KB (480974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca62d29a99ce64d8c11b61d11423b1be460c4d19b6db2f5fc3fdae414959a42`  
		Last Modified: Thu, 18 Sep 2025 21:26:35 GMT  
		Size: 378.0 MB (377955202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40c5cb280c93547c71712afe50b6e95280f926ac987b6ace1b5c84ca6e70394`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9d8e6b97aaf796e40dd5aac02025e7ca16897122cdc261f16919317b526f5`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7a337a5b5f069bc58952426610e0698de8d69b6e74740938d5b25c6e9e7e7e`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e8f3d32fa6ac1192e6989b8291f82c3b72a88a56aec315c6b66f49689eb0c`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:f04d38112729188faa3e13d481385728b8be36b73622146843d66b899a915bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67471460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062bf84ae4ac5c0718e649728c82689e7890f19a0594a3cb883b72bc1701bd8d`

```dockerfile
```

-	Layers:
	-	`sha256:cc88bb39d91b44864dd2b132a637f66d271ff22603d9741fa55fb1762c1cacf3`  
		Last Modified: Thu, 18 Sep 2025 22:14:22 GMT  
		Size: 67.4 MB (67444160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2389be984c83baf78cb81407b87f4a10696abc9bad6f08343496ab127c29ac`  
		Last Modified: Thu, 18 Sep 2025 22:14:23 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:18abb637f3b4996cae0a081548d8d55766c3760db8fce500ba1a2d9dd74b8d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.3 MB (693294823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6093fd44149936164be17126b632368b0efea75041d4ea49b5141ab79301ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=ppc64le
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effb9ac56d3eb46ea39f74edb8236e8ce21259ac2b8e7f09120fea4e3960b689`  
		Last Modified: Thu, 18 Sep 2025 19:00:59 GMT  
		Size: 378.6 MB (378619046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097c38dae6deeaa106205c455ca9085c12aee1638ad5ab5a25f6e30cefe08633`  
		Last Modified: Thu, 18 Sep 2025 19:00:05 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7e938c2b1965169d558082c489cdecfb364f913ed7cdd44b871e693e687ec6`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3485b1a5fa30f38c98d54e01b7de5374ea5116e859100bb9728f5367fc78a0`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f053e2f77d24d2bcdeb42a4a5fd77a38df9f9fe4442bc501793f315860bb098`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:78188af6b5e9a5131a5659180f7278da8f1e7058a2570ae23f2ec4a8d34e3b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67472460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8193190bf00d13e51270e0653a5c154fe7c2810d27a866a608dd08d3d079af74`

```dockerfile
```

-	Layers:
	-	`sha256:84754f4ef145cc0aedf2e3fd7250c42d310a5be5b43901b15f7eed7edfc82ce5`  
		Last Modified: Thu, 18 Sep 2025 19:15:22 GMT  
		Size: 67.4 MB (67445262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cb129f9b79b51b8ace46f0f558bd27e9109927be05122ab66abad19e7b279c`  
		Last Modified: Thu, 18 Sep 2025 19:15:23 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:67a6c4fc312186720be9566071eb3539634925657b4e2e3d799bc5608d838851
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
$ docker pull odoo@sha256:04c3a385ae47d0838b95daa5286ad0d72089c7a1b85f97188e7974d035f457f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.1 MB (677104277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ee5d07d2946efb0ba6585064a48361514c55c365bb4306d6f42b542b111a79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=amd64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d00355c0704636cb70f98ff01b12f65450ed5e6dc31fe70e15f2ff27bb2c8a9`  
		Last Modified: Thu, 18 Sep 2025 19:13:20 GMT  
		Size: 254.5 MB (254529024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc78c74f02cfa9d2d3963124dd5d978e08b28d30a5e11f0343d2db3dde3921f`  
		Last Modified: Thu, 18 Sep 2025 19:05:57 GMT  
		Size: 14.3 MB (14286373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56feb6c70e97fc514c44672a95a22f828ed2612e2b285d5b5d4de457fb03a8dc`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 481.0 KB (480963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87b3f25613d7046f870ed5ce91c1d13974a242f633fb4488f243becb44e21c`  
		Last Modified: Thu, 18 Sep 2025 19:13:19 GMT  
		Size: 378.1 MB (378082033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b02d70d192e7d5096dfb85491069537ecc913b8ada4387cc7c3f5879d1d5cea`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a69f56c596e69044a79e013229736014f8e5010255daebd70ddaf3b224175d1`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62514748077a9159bc082dc768b58eed4537f144a0de4215b85fefb777dc0c87`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6270c89452b88c8eb784ecbeb3d97ad780327bc64f93265249a3cfe479897`  
		Last Modified: Thu, 18 Sep 2025 19:05:51 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c9ef8855fa7792e99ebfd03f67790cf9c1f5a40371e997bfa92229d0a242032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67464009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b522bb1b6bcda8d960c82b8cad0c64cab96079d57a2f962ce75b98f71a142`

```dockerfile
```

-	Layers:
	-	`sha256:57c3bfa5117d1d92c336acb37d34d14993926ecb74c8cab9d010751841b236bc`  
		Last Modified: Thu, 18 Sep 2025 19:13:03 GMT  
		Size: 67.4 MB (67436873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c242d75a39e51ef5b0d3f186419f5e47924b7d14de0465444e72124c761b1bc8`  
		Last Modified: Thu, 18 Sep 2025 19:13:06 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ae5ecb32875a3160571979c4e065dd1532b86458eff90b1fbfcc86424d938f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.5 MB (673483666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64ac348070d41de648c01aa908579811aeb09a9be335238838254a89251a176`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2d285cc6758180abd60ae65ee5488607a2b3b1e88be78ce839d3661a36e84d`  
		Last Modified: Thu, 18 Sep 2025 21:26:36 GMT  
		Size: 251.9 MB (251920419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedfe140bb0615c2f2d7dc1ce3529ea24694b98aed59eac57a3468ace9ce3a62`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 14.3 MB (14263317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cd9e29f873040e4336fd67b8b91715755847d71b5a221864b4165aff5d7f75`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 481.0 KB (480974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca62d29a99ce64d8c11b61d11423b1be460c4d19b6db2f5fc3fdae414959a42`  
		Last Modified: Thu, 18 Sep 2025 21:26:35 GMT  
		Size: 378.0 MB (377955202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40c5cb280c93547c71712afe50b6e95280f926ac987b6ace1b5c84ca6e70394`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9d8e6b97aaf796e40dd5aac02025e7ca16897122cdc261f16919317b526f5`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7a337a5b5f069bc58952426610e0698de8d69b6e74740938d5b25c6e9e7e7e`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e8f3d32fa6ac1192e6989b8291f82c3b72a88a56aec315c6b66f49689eb0c`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f04d38112729188faa3e13d481385728b8be36b73622146843d66b899a915bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67471460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062bf84ae4ac5c0718e649728c82689e7890f19a0594a3cb883b72bc1701bd8d`

```dockerfile
```

-	Layers:
	-	`sha256:cc88bb39d91b44864dd2b132a637f66d271ff22603d9741fa55fb1762c1cacf3`  
		Last Modified: Thu, 18 Sep 2025 22:14:22 GMT  
		Size: 67.4 MB (67444160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2389be984c83baf78cb81407b87f4a10696abc9bad6f08343496ab127c29ac`  
		Last Modified: Thu, 18 Sep 2025 22:14:23 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:18abb637f3b4996cae0a081548d8d55766c3760db8fce500ba1a2d9dd74b8d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.3 MB (693294823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6093fd44149936164be17126b632368b0efea75041d4ea49b5141ab79301ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=ppc64le
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effb9ac56d3eb46ea39f74edb8236e8ce21259ac2b8e7f09120fea4e3960b689`  
		Last Modified: Thu, 18 Sep 2025 19:00:59 GMT  
		Size: 378.6 MB (378619046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097c38dae6deeaa106205c455ca9085c12aee1638ad5ab5a25f6e30cefe08633`  
		Last Modified: Thu, 18 Sep 2025 19:00:05 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7e938c2b1965169d558082c489cdecfb364f913ed7cdd44b871e693e687ec6`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3485b1a5fa30f38c98d54e01b7de5374ea5116e859100bb9728f5367fc78a0`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f053e2f77d24d2bcdeb42a4a5fd77a38df9f9fe4442bc501793f315860bb098`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:78188af6b5e9a5131a5659180f7278da8f1e7058a2570ae23f2ec4a8d34e3b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67472460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8193190bf00d13e51270e0653a5c154fe7c2810d27a866a608dd08d3d079af74`

```dockerfile
```

-	Layers:
	-	`sha256:84754f4ef145cc0aedf2e3fd7250c42d310a5be5b43901b15f7eed7edfc82ce5`  
		Last Modified: Thu, 18 Sep 2025 19:15:22 GMT  
		Size: 67.4 MB (67445262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cb129f9b79b51b8ace46f0f558bd27e9109927be05122ab66abad19e7b279c`  
		Last Modified: Thu, 18 Sep 2025 19:15:23 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20250918`

```console
$ docker pull odoo@sha256:67a6c4fc312186720be9566071eb3539634925657b4e2e3d799bc5608d838851
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20250918` - linux; amd64

```console
$ docker pull odoo@sha256:04c3a385ae47d0838b95daa5286ad0d72089c7a1b85f97188e7974d035f457f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.1 MB (677104277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ee5d07d2946efb0ba6585064a48361514c55c365bb4306d6f42b542b111a79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=amd64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d00355c0704636cb70f98ff01b12f65450ed5e6dc31fe70e15f2ff27bb2c8a9`  
		Last Modified: Thu, 18 Sep 2025 19:13:20 GMT  
		Size: 254.5 MB (254529024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc78c74f02cfa9d2d3963124dd5d978e08b28d30a5e11f0343d2db3dde3921f`  
		Last Modified: Thu, 18 Sep 2025 19:05:57 GMT  
		Size: 14.3 MB (14286373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56feb6c70e97fc514c44672a95a22f828ed2612e2b285d5b5d4de457fb03a8dc`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 481.0 KB (480963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87b3f25613d7046f870ed5ce91c1d13974a242f633fb4488f243becb44e21c`  
		Last Modified: Thu, 18 Sep 2025 19:13:19 GMT  
		Size: 378.1 MB (378082033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b02d70d192e7d5096dfb85491069537ecc913b8ada4387cc7c3f5879d1d5cea`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a69f56c596e69044a79e013229736014f8e5010255daebd70ddaf3b224175d1`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62514748077a9159bc082dc768b58eed4537f144a0de4215b85fefb777dc0c87`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6270c89452b88c8eb784ecbeb3d97ad780327bc64f93265249a3cfe479897`  
		Last Modified: Thu, 18 Sep 2025 19:05:51 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20250918` - unknown; unknown

```console
$ docker pull odoo@sha256:c9ef8855fa7792e99ebfd03f67790cf9c1f5a40371e997bfa92229d0a242032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67464009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b522bb1b6bcda8d960c82b8cad0c64cab96079d57a2f962ce75b98f71a142`

```dockerfile
```

-	Layers:
	-	`sha256:57c3bfa5117d1d92c336acb37d34d14993926ecb74c8cab9d010751841b236bc`  
		Last Modified: Thu, 18 Sep 2025 19:13:03 GMT  
		Size: 67.4 MB (67436873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c242d75a39e51ef5b0d3f186419f5e47924b7d14de0465444e72124c761b1bc8`  
		Last Modified: Thu, 18 Sep 2025 19:13:06 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20250918` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ae5ecb32875a3160571979c4e065dd1532b86458eff90b1fbfcc86424d938f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.5 MB (673483666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64ac348070d41de648c01aa908579811aeb09a9be335238838254a89251a176`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2d285cc6758180abd60ae65ee5488607a2b3b1e88be78ce839d3661a36e84d`  
		Last Modified: Thu, 18 Sep 2025 21:26:36 GMT  
		Size: 251.9 MB (251920419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedfe140bb0615c2f2d7dc1ce3529ea24694b98aed59eac57a3468ace9ce3a62`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 14.3 MB (14263317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cd9e29f873040e4336fd67b8b91715755847d71b5a221864b4165aff5d7f75`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 481.0 KB (480974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca62d29a99ce64d8c11b61d11423b1be460c4d19b6db2f5fc3fdae414959a42`  
		Last Modified: Thu, 18 Sep 2025 21:26:35 GMT  
		Size: 378.0 MB (377955202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40c5cb280c93547c71712afe50b6e95280f926ac987b6ace1b5c84ca6e70394`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9d8e6b97aaf796e40dd5aac02025e7ca16897122cdc261f16919317b526f5`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7a337a5b5f069bc58952426610e0698de8d69b6e74740938d5b25c6e9e7e7e`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e8f3d32fa6ac1192e6989b8291f82c3b72a88a56aec315c6b66f49689eb0c`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20250918` - unknown; unknown

```console
$ docker pull odoo@sha256:f04d38112729188faa3e13d481385728b8be36b73622146843d66b899a915bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67471460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062bf84ae4ac5c0718e649728c82689e7890f19a0594a3cb883b72bc1701bd8d`

```dockerfile
```

-	Layers:
	-	`sha256:cc88bb39d91b44864dd2b132a637f66d271ff22603d9741fa55fb1762c1cacf3`  
		Last Modified: Thu, 18 Sep 2025 22:14:22 GMT  
		Size: 67.4 MB (67444160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2389be984c83baf78cb81407b87f4a10696abc9bad6f08343496ab127c29ac`  
		Last Modified: Thu, 18 Sep 2025 22:14:23 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20250918` - linux; ppc64le

```console
$ docker pull odoo@sha256:18abb637f3b4996cae0a081548d8d55766c3760db8fce500ba1a2d9dd74b8d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.3 MB (693294823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6093fd44149936164be17126b632368b0efea75041d4ea49b5141ab79301ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=ppc64le
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effb9ac56d3eb46ea39f74edb8236e8ce21259ac2b8e7f09120fea4e3960b689`  
		Last Modified: Thu, 18 Sep 2025 19:00:59 GMT  
		Size: 378.6 MB (378619046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097c38dae6deeaa106205c455ca9085c12aee1638ad5ab5a25f6e30cefe08633`  
		Last Modified: Thu, 18 Sep 2025 19:00:05 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7e938c2b1965169d558082c489cdecfb364f913ed7cdd44b871e693e687ec6`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3485b1a5fa30f38c98d54e01b7de5374ea5116e859100bb9728f5367fc78a0`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f053e2f77d24d2bcdeb42a4a5fd77a38df9f9fe4442bc501793f315860bb098`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20250918` - unknown; unknown

```console
$ docker pull odoo@sha256:78188af6b5e9a5131a5659180f7278da8f1e7058a2570ae23f2ec4a8d34e3b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67472460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8193190bf00d13e51270e0653a5c154fe7c2810d27a866a608dd08d3d079af74`

```dockerfile
```

-	Layers:
	-	`sha256:84754f4ef145cc0aedf2e3fd7250c42d310a5be5b43901b15f7eed7edfc82ce5`  
		Last Modified: Thu, 18 Sep 2025 19:15:22 GMT  
		Size: 67.4 MB (67445262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cb129f9b79b51b8ace46f0f558bd27e9109927be05122ab66abad19e7b279c`  
		Last Modified: Thu, 18 Sep 2025 19:15:23 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:67a6c4fc312186720be9566071eb3539634925657b4e2e3d799bc5608d838851
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
$ docker pull odoo@sha256:04c3a385ae47d0838b95daa5286ad0d72089c7a1b85f97188e7974d035f457f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.1 MB (677104277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ee5d07d2946efb0ba6585064a48361514c55c365bb4306d6f42b542b111a79`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=amd64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d00355c0704636cb70f98ff01b12f65450ed5e6dc31fe70e15f2ff27bb2c8a9`  
		Last Modified: Thu, 18 Sep 2025 19:13:20 GMT  
		Size: 254.5 MB (254529024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc78c74f02cfa9d2d3963124dd5d978e08b28d30a5e11f0343d2db3dde3921f`  
		Last Modified: Thu, 18 Sep 2025 19:05:57 GMT  
		Size: 14.3 MB (14286373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56feb6c70e97fc514c44672a95a22f828ed2612e2b285d5b5d4de457fb03a8dc`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 481.0 KB (480963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac87b3f25613d7046f870ed5ce91c1d13974a242f633fb4488f243becb44e21c`  
		Last Modified: Thu, 18 Sep 2025 19:13:19 GMT  
		Size: 378.1 MB (378082033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b02d70d192e7d5096dfb85491069537ecc913b8ada4387cc7c3f5879d1d5cea`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a69f56c596e69044a79e013229736014f8e5010255daebd70ddaf3b224175d1`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62514748077a9159bc082dc768b58eed4537f144a0de4215b85fefb777dc0c87`  
		Last Modified: Thu, 18 Sep 2025 19:05:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6270c89452b88c8eb784ecbeb3d97ad780327bc64f93265249a3cfe479897`  
		Last Modified: Thu, 18 Sep 2025 19:05:51 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c9ef8855fa7792e99ebfd03f67790cf9c1f5a40371e997bfa92229d0a242032f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67464009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b522bb1b6bcda8d960c82b8cad0c64cab96079d57a2f962ce75b98f71a142`

```dockerfile
```

-	Layers:
	-	`sha256:57c3bfa5117d1d92c336acb37d34d14993926ecb74c8cab9d010751841b236bc`  
		Last Modified: Thu, 18 Sep 2025 19:13:03 GMT  
		Size: 67.4 MB (67436873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c242d75a39e51ef5b0d3f186419f5e47924b7d14de0465444e72124c761b1bc8`  
		Last Modified: Thu, 18 Sep 2025 19:13:06 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ae5ecb32875a3160571979c4e065dd1532b86458eff90b1fbfcc86424d938f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.5 MB (673483666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64ac348070d41de648c01aa908579811aeb09a9be335238838254a89251a176`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=arm64
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2d285cc6758180abd60ae65ee5488607a2b3b1e88be78ce839d3661a36e84d`  
		Last Modified: Thu, 18 Sep 2025 21:26:36 GMT  
		Size: 251.9 MB (251920419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedfe140bb0615c2f2d7dc1ce3529ea24694b98aed59eac57a3468ace9ce3a62`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 14.3 MB (14263317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cd9e29f873040e4336fd67b8b91715755847d71b5a221864b4165aff5d7f75`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 481.0 KB (480974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca62d29a99ce64d8c11b61d11423b1be460c4d19b6db2f5fc3fdae414959a42`  
		Last Modified: Thu, 18 Sep 2025 21:26:35 GMT  
		Size: 378.0 MB (377955202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40c5cb280c93547c71712afe50b6e95280f926ac987b6ace1b5c84ca6e70394`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9d8e6b97aaf796e40dd5aac02025e7ca16897122cdc261f16919317b526f5`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7a337a5b5f069bc58952426610e0698de8d69b6e74740938d5b25c6e9e7e7e`  
		Last Modified: Thu, 18 Sep 2025 19:14:49 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e8f3d32fa6ac1192e6989b8291f82c3b72a88a56aec315c6b66f49689eb0c`  
		Last Modified: Thu, 18 Sep 2025 19:14:48 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f04d38112729188faa3e13d481385728b8be36b73622146843d66b899a915bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67471460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062bf84ae4ac5c0718e649728c82689e7890f19a0594a3cb883b72bc1701bd8d`

```dockerfile
```

-	Layers:
	-	`sha256:cc88bb39d91b44864dd2b132a637f66d271ff22603d9741fa55fb1762c1cacf3`  
		Last Modified: Thu, 18 Sep 2025 22:14:22 GMT  
		Size: 67.4 MB (67444160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2389be984c83baf78cb81407b87f4a10696abc9bad6f08343496ab127c29ac`  
		Last Modified: Thu, 18 Sep 2025 22:14:23 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:18abb637f3b4996cae0a081548d8d55766c3760db8fce500ba1a2d9dd74b8d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.3 MB (693294823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6093fd44149936164be17126b632368b0efea75041d4ea49b5141ab79301ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 09:07:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 18 Sep 2025 09:07:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 09:07:36 GMT
ARG TARGETARCH=ppc64le
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_VERSION=19.0
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_RELEASE=20250918
# Thu, 18 Sep 2025 09:07:36 GMT
ARG ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250918 ODOO_SHA=3b7db7702c236b9060d5668a39a5ac61944b1153
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 18 Sep 2025 09:07:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 18 Sep 2025 09:07:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 18 Sep 2025 09:07:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 18 Sep 2025 09:07:36 GMT
USER odoo
# Thu, 18 Sep 2025 09:07:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Sep 2025 09:07:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd53700fdf8f481c3ddfd6386b24ae80849ec7e5659bd53026a593bcfcdf9d2`  
		Last Modified: Tue, 16 Sep 2025 00:13:10 GMT  
		Size: 265.1 MB (265076067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3aebcb236853ea5cc45af6c54ce777915694fa449e161c36f03b9a68b3f13f`  
		Last Modified: Tue, 16 Sep 2025 00:12:44 GMT  
		Size: 14.8 MB (14813140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383a81e95032a2f4480f2c597480a1f28b16ea256a1ee758e514dbf62e9c373`  
		Last Modified: Mon, 15 Sep 2025 23:52:49 GMT  
		Size: 481.0 KB (481005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effb9ac56d3eb46ea39f74edb8236e8ce21259ac2b8e7f09120fea4e3960b689`  
		Last Modified: Thu, 18 Sep 2025 19:00:59 GMT  
		Size: 378.6 MB (378619046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097c38dae6deeaa106205c455ca9085c12aee1638ad5ab5a25f6e30cefe08633`  
		Last Modified: Thu, 18 Sep 2025 19:00:05 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7e938c2b1965169d558082c489cdecfb364f913ed7cdd44b871e693e687ec6`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3485b1a5fa30f38c98d54e01b7de5374ea5116e859100bb9728f5367fc78a0`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f053e2f77d24d2bcdeb42a4a5fd77a38df9f9fe4442bc501793f315860bb098`  
		Last Modified: Thu, 18 Sep 2025 19:00:03 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:78188af6b5e9a5131a5659180f7278da8f1e7058a2570ae23f2ec4a8d34e3b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67472460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8193190bf00d13e51270e0653a5c154fe7c2810d27a866a608dd08d3d079af74`

```dockerfile
```

-	Layers:
	-	`sha256:84754f4ef145cc0aedf2e3fd7250c42d310a5be5b43901b15f7eed7edfc82ce5`  
		Last Modified: Thu, 18 Sep 2025 19:15:22 GMT  
		Size: 67.4 MB (67445262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cb129f9b79b51b8ace46f0f558bd27e9109927be05122ab66abad19e7b279c`  
		Last Modified: Thu, 18 Sep 2025 19:15:23 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
