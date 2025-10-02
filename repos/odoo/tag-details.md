<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250930`](#odoo170-20250930)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250930`](#odoo180-20250930)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20250930`](#odoo190-20250930)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:eceafc793146f791c491562fb80e6a39fba96729bfd268b54d2ade541c040bc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:b991ac35851e8ecc9f73a33ec1b2c603edbb2abe2db80f5acd548c5e2bdb9d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605319759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46382d66a79cfee963c1336d53e2aab8a5574194a4d4cfb5c40ead0dccfd3f0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78acfb9d02a2f5fcec9120a938926be61087297d7a53a836d03588559bc5d772`  
		Last Modified: Thu, 02 Oct 2025 07:12:30 GMT  
		Size: 233.8 MB (233818458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c57c7544a532e9165c1a37745c85217373ff1c9d9817941fde6f344ee4807`  
		Last Modified: Thu, 02 Oct 2025 05:15:57 GMT  
		Size: 2.6 MB (2594998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527a903b017a480bfb8ac2981860ff13196b7fed4f9daaa195d6483ed48f55e0`  
		Last Modified: Thu, 02 Oct 2025 05:15:58 GMT  
		Size: 480.2 KB (480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0acd193f09f985af2ad0756b64f57cc323224d27f27dbca21e215ceabf2e6ac`  
		Last Modified: Thu, 02 Oct 2025 07:12:27 GMT  
		Size: 338.9 MB (338886819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dd8bcd9548dd5db89c652a43b5d23baed1b53cea6073cd72f7098ae13adb23`  
		Last Modified: Thu, 02 Oct 2025 05:15:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b154b21c566ad76307d393ea1d740c53fbf70774a0e3d687dc740c1ef67f0c5`  
		Last Modified: Thu, 02 Oct 2025 05:15:59 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a848976a4f3872ec808603aedbebbffb2def88714aa4677755b4d95e4e2595ec`  
		Last Modified: Thu, 02 Oct 2025 05:16:00 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2093a348d73fe551a82a2df27c2cec1b86c7d8660bce9f723b45865a5df51918`  
		Last Modified: Thu, 02 Oct 2025 05:15:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:a7e8c4ad08e73335289e519a2c9e2b0ddd04ae54c28c7eb4d82d19082dc2010a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41507727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a16a62bc2b5528d370d5182b81736f54ed63fed0bcac54bd7c3bb3ac4c5f98`

```dockerfile
```

-	Layers:
	-	`sha256:8a8d4c74d94d93eacff9830ccd22161bd8004d0d10bd34c4970641b5fc7c976f`  
		Last Modified: Thu, 02 Oct 2025 07:12:20 GMT  
		Size: 41.5 MB (41480892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b08cb760eb5ff581895f1bfbd79f7f9c61b0fa976e752ae120e4261bf5a133bd`  
		Last Modified: Thu, 02 Oct 2025 07:12:22 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0c7d6449e09c1cc5b094f0db4877b342f08f502d9218b9bde28b59f17d2bccf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.1 MB (600135864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb91c31242be97b32479e49e48ff742fb577943889392ef04bff7ae3009dd222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300193dc1f3067e8189fc775798f750a08d65d952a91a3c57b9b9e87e7f23906`  
		Last Modified: Thu, 02 Oct 2025 04:13:21 GMT  
		Size: 231.2 MB (231188183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbeca8b8d3ada08f7ba0145f036b623880df3e89ebd6fcaea81a59bc0a4e3bcb`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 2.6 MB (2590480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699de0168c5dcbad014b961839eacf1352e7b89b8bb3af44a5d9a21995230db3`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 480.3 KB (480268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd99469e55203057ec1f2d1979c81a02c8035510282c35c43b4f0f4236adfdd`  
		Last Modified: Thu, 02 Oct 2025 01:31:28 GMT  
		Size: 338.5 MB (338491389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03bf4370ad47631586284107342893b8806c63d7b2802697fa23663c7615e06`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c1c8f002f5bb791c8f036293b5292d614787b56a0f47735c946dbe973674e8`  
		Last Modified: Thu, 02 Oct 2025 02:14:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf3a7ca8466df25bc37e2adda3c7e66acf80974d1fcdd415c70c6f3bddca07`  
		Last Modified: Thu, 02 Oct 2025 02:14:44 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea36c31ebd1891d8fa1e9cd399f857fdb2d6f0ddc66a571944f2cc7dda583fa`  
		Last Modified: Thu, 02 Oct 2025 02:14:52 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:08dc7b07f81b8fefb121e5d0a2a6e9739d6d9dd05ae606bf6a79ceb9c6bbddad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41514386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39ba7af616a61e2402d176eb870885ac1d2376f0c8bc9d160a375779bc708ff`

```dockerfile
```

-	Layers:
	-	`sha256:373bdf49d9d29f44523b1dc2baee58991f9871679760e2935c3edfc269b90a73`  
		Last Modified: Thu, 02 Oct 2025 04:13:09 GMT  
		Size: 41.5 MB (41487399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:599495707f89ef59c9cc38a481902dc50fa7deb94b6d37cc47007e74e18f3a83`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:eceafc793146f791c491562fb80e6a39fba96729bfd268b54d2ade541c040bc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:b991ac35851e8ecc9f73a33ec1b2c603edbb2abe2db80f5acd548c5e2bdb9d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605319759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46382d66a79cfee963c1336d53e2aab8a5574194a4d4cfb5c40ead0dccfd3f0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78acfb9d02a2f5fcec9120a938926be61087297d7a53a836d03588559bc5d772`  
		Last Modified: Thu, 02 Oct 2025 07:12:30 GMT  
		Size: 233.8 MB (233818458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c57c7544a532e9165c1a37745c85217373ff1c9d9817941fde6f344ee4807`  
		Last Modified: Thu, 02 Oct 2025 05:15:57 GMT  
		Size: 2.6 MB (2594998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527a903b017a480bfb8ac2981860ff13196b7fed4f9daaa195d6483ed48f55e0`  
		Last Modified: Thu, 02 Oct 2025 05:15:58 GMT  
		Size: 480.2 KB (480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0acd193f09f985af2ad0756b64f57cc323224d27f27dbca21e215ceabf2e6ac`  
		Last Modified: Thu, 02 Oct 2025 07:12:27 GMT  
		Size: 338.9 MB (338886819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dd8bcd9548dd5db89c652a43b5d23baed1b53cea6073cd72f7098ae13adb23`  
		Last Modified: Thu, 02 Oct 2025 05:15:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b154b21c566ad76307d393ea1d740c53fbf70774a0e3d687dc740c1ef67f0c5`  
		Last Modified: Thu, 02 Oct 2025 05:15:59 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a848976a4f3872ec808603aedbebbffb2def88714aa4677755b4d95e4e2595ec`  
		Last Modified: Thu, 02 Oct 2025 05:16:00 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2093a348d73fe551a82a2df27c2cec1b86c7d8660bce9f723b45865a5df51918`  
		Last Modified: Thu, 02 Oct 2025 05:15:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a7e8c4ad08e73335289e519a2c9e2b0ddd04ae54c28c7eb4d82d19082dc2010a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41507727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a16a62bc2b5528d370d5182b81736f54ed63fed0bcac54bd7c3bb3ac4c5f98`

```dockerfile
```

-	Layers:
	-	`sha256:8a8d4c74d94d93eacff9830ccd22161bd8004d0d10bd34c4970641b5fc7c976f`  
		Last Modified: Thu, 02 Oct 2025 07:12:20 GMT  
		Size: 41.5 MB (41480892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b08cb760eb5ff581895f1bfbd79f7f9c61b0fa976e752ae120e4261bf5a133bd`  
		Last Modified: Thu, 02 Oct 2025 07:12:22 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0c7d6449e09c1cc5b094f0db4877b342f08f502d9218b9bde28b59f17d2bccf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.1 MB (600135864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb91c31242be97b32479e49e48ff742fb577943889392ef04bff7ae3009dd222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300193dc1f3067e8189fc775798f750a08d65d952a91a3c57b9b9e87e7f23906`  
		Last Modified: Thu, 02 Oct 2025 04:13:21 GMT  
		Size: 231.2 MB (231188183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbeca8b8d3ada08f7ba0145f036b623880df3e89ebd6fcaea81a59bc0a4e3bcb`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 2.6 MB (2590480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699de0168c5dcbad014b961839eacf1352e7b89b8bb3af44a5d9a21995230db3`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 480.3 KB (480268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd99469e55203057ec1f2d1979c81a02c8035510282c35c43b4f0f4236adfdd`  
		Last Modified: Thu, 02 Oct 2025 01:31:28 GMT  
		Size: 338.5 MB (338491389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03bf4370ad47631586284107342893b8806c63d7b2802697fa23663c7615e06`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c1c8f002f5bb791c8f036293b5292d614787b56a0f47735c946dbe973674e8`  
		Last Modified: Thu, 02 Oct 2025 02:14:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf3a7ca8466df25bc37e2adda3c7e66acf80974d1fcdd415c70c6f3bddca07`  
		Last Modified: Thu, 02 Oct 2025 02:14:44 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea36c31ebd1891d8fa1e9cd399f857fdb2d6f0ddc66a571944f2cc7dda583fa`  
		Last Modified: Thu, 02 Oct 2025 02:14:52 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:08dc7b07f81b8fefb121e5d0a2a6e9739d6d9dd05ae606bf6a79ceb9c6bbddad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41514386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39ba7af616a61e2402d176eb870885ac1d2376f0c8bc9d160a375779bc708ff`

```dockerfile
```

-	Layers:
	-	`sha256:373bdf49d9d29f44523b1dc2baee58991f9871679760e2935c3edfc269b90a73`  
		Last Modified: Thu, 02 Oct 2025 04:13:09 GMT  
		Size: 41.5 MB (41487399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:599495707f89ef59c9cc38a481902dc50fa7deb94b6d37cc47007e74e18f3a83`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250930`

```console
$ docker pull odoo@sha256:eceafc793146f791c491562fb80e6a39fba96729bfd268b54d2ade541c040bc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20250930` - linux; amd64

```console
$ docker pull odoo@sha256:b991ac35851e8ecc9f73a33ec1b2c603edbb2abe2db80f5acd548c5e2bdb9d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605319759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46382d66a79cfee963c1336d53e2aab8a5574194a4d4cfb5c40ead0dccfd3f0b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78acfb9d02a2f5fcec9120a938926be61087297d7a53a836d03588559bc5d772`  
		Last Modified: Thu, 02 Oct 2025 07:12:30 GMT  
		Size: 233.8 MB (233818458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c57c7544a532e9165c1a37745c85217373ff1c9d9817941fde6f344ee4807`  
		Last Modified: Thu, 02 Oct 2025 05:15:57 GMT  
		Size: 2.6 MB (2594998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527a903b017a480bfb8ac2981860ff13196b7fed4f9daaa195d6483ed48f55e0`  
		Last Modified: Thu, 02 Oct 2025 05:15:58 GMT  
		Size: 480.2 KB (480234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0acd193f09f985af2ad0756b64f57cc323224d27f27dbca21e215ceabf2e6ac`  
		Last Modified: Thu, 02 Oct 2025 07:12:27 GMT  
		Size: 338.9 MB (338886819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dd8bcd9548dd5db89c652a43b5d23baed1b53cea6073cd72f7098ae13adb23`  
		Last Modified: Thu, 02 Oct 2025 05:15:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b154b21c566ad76307d393ea1d740c53fbf70774a0e3d687dc740c1ef67f0c5`  
		Last Modified: Thu, 02 Oct 2025 05:15:59 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a848976a4f3872ec808603aedbebbffb2def88714aa4677755b4d95e4e2595ec`  
		Last Modified: Thu, 02 Oct 2025 05:16:00 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2093a348d73fe551a82a2df27c2cec1b86c7d8660bce9f723b45865a5df51918`  
		Last Modified: Thu, 02 Oct 2025 05:15:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:a7e8c4ad08e73335289e519a2c9e2b0ddd04ae54c28c7eb4d82d19082dc2010a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41507727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a16a62bc2b5528d370d5182b81736f54ed63fed0bcac54bd7c3bb3ac4c5f98`

```dockerfile
```

-	Layers:
	-	`sha256:8a8d4c74d94d93eacff9830ccd22161bd8004d0d10bd34c4970641b5fc7c976f`  
		Last Modified: Thu, 02 Oct 2025 07:12:20 GMT  
		Size: 41.5 MB (41480892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b08cb760eb5ff581895f1bfbd79f7f9c61b0fa976e752ae120e4261bf5a133bd`  
		Last Modified: Thu, 02 Oct 2025 07:12:22 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250930` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0c7d6449e09c1cc5b094f0db4877b342f08f502d9218b9bde28b59f17d2bccf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.1 MB (600135864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb91c31242be97b32479e49e48ff742fb577943889392ef04bff7ae3009dd222`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300193dc1f3067e8189fc775798f750a08d65d952a91a3c57b9b9e87e7f23906`  
		Last Modified: Thu, 02 Oct 2025 04:13:21 GMT  
		Size: 231.2 MB (231188183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbeca8b8d3ada08f7ba0145f036b623880df3e89ebd6fcaea81a59bc0a4e3bcb`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 2.6 MB (2590480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699de0168c5dcbad014b961839eacf1352e7b89b8bb3af44a5d9a21995230db3`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 480.3 KB (480268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd99469e55203057ec1f2d1979c81a02c8035510282c35c43b4f0f4236adfdd`  
		Last Modified: Thu, 02 Oct 2025 01:31:28 GMT  
		Size: 338.5 MB (338491389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03bf4370ad47631586284107342893b8806c63d7b2802697fa23663c7615e06`  
		Last Modified: Thu, 02 Oct 2025 02:14:45 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c1c8f002f5bb791c8f036293b5292d614787b56a0f47735c946dbe973674e8`  
		Last Modified: Thu, 02 Oct 2025 02:14:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bf3a7ca8466df25bc37e2adda3c7e66acf80974d1fcdd415c70c6f3bddca07`  
		Last Modified: Thu, 02 Oct 2025 02:14:44 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea36c31ebd1891d8fa1e9cd399f857fdb2d6f0ddc66a571944f2cc7dda583fa`  
		Last Modified: Thu, 02 Oct 2025 02:14:52 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:08dc7b07f81b8fefb121e5d0a2a6e9739d6d9dd05ae606bf6a79ceb9c6bbddad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41514386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39ba7af616a61e2402d176eb870885ac1d2376f0c8bc9d160a375779bc708ff`

```dockerfile
```

-	Layers:
	-	`sha256:373bdf49d9d29f44523b1dc2baee58991f9871679760e2935c3edfc269b90a73`  
		Last Modified: Thu, 02 Oct 2025 04:13:09 GMT  
		Size: 41.5 MB (41487399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:599495707f89ef59c9cc38a481902dc50fa7deb94b6d37cc47007e74e18f3a83`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:b19b167d6c2cd15bc103761e63635025c08c6a4f4a8bb336066cc8c4125caaae
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
$ docker pull odoo@sha256:f23cf400f8caac66128bfb78dad613395195523b98ccc04c82802e9814327c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.4 MB (679371311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b28d9b277363dc886854b6b15fd3d1668167fd9e1e037338a890df051bf0b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74ade1303eb485c1ed295b3bd9e397f678c3f4172a4606f080ffae0d316d8f`  
		Last Modified: Thu, 02 Oct 2025 06:20:27 GMT  
		Size: 256.9 MB (256943828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35da4fd4e03d1fef0289b5a3761d80bd790f1c826d1a1e92602c62fc6735cf6`  
		Last Modified: Thu, 02 Oct 2025 05:16:59 GMT  
		Size: 14.3 MB (14339329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f4611b4df587836c21ff72c472b8b8dd8ffc710881db5e0b4785cccbb0c710`  
		Last Modified: Thu, 02 Oct 2025 05:16:58 GMT  
		Size: 480.0 KB (479986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee09c29c3619839eed40cb3d354ec97d3d8a759d360968d4e808c49aa2788801`  
		Last Modified: Thu, 02 Oct 2025 06:20:07 GMT  
		Size: 377.9 MB (377882721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23e80e12301c074d61599b1c06d8094d0b05416f733a67192d3baa7de6badd9`  
		Last Modified: Thu, 02 Oct 2025 05:16:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997f1553f8ff3be2aac6a4efbf4343c87972c16e755f22049510ea69851f0eb2`  
		Last Modified: Thu, 02 Oct 2025 05:16:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdecde88bf547f9148f113d396de94101ab44b350fcca237746a448772a363c2`  
		Last Modified: Thu, 02 Oct 2025 05:16:58 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db709be05ab1433caa8dca227fab279e6832e02ac4dc17289121d66f60c700d0`  
		Last Modified: Thu, 02 Oct 2025 05:16:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:13aa0c6b375ccd06f92e2542bf3195e6f26ac35fd3903490f329435cd21bec10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61088147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37798fa19b0279e5368af66b6f680cc21d5b3807934190b78399f71ff5e2394`

```dockerfile
```

-	Layers:
	-	`sha256:e7afacbc348a744623258e0a08e1e5b98af145fa0517312ec37be45c9542852b`  
		Last Modified: Thu, 02 Oct 2025 07:12:30 GMT  
		Size: 61.1 MB (61061305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb6d9d6f4622852bf59074df53654bf1326f817eb379fa413c61772b148ff50`  
		Last Modified: Thu, 02 Oct 2025 07:12:31 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0fa66f6d7b330830194b975496e69d54c59c346046d656bc25ad37d06357175e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.6 MB (675597933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8ce80de18b947e034f7d2b8b71f080fc50692513e6e6446d38181f572d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a3b4d011173c8f10be11a9ca76ac9af624f8c86c20474f6295f4072884d571`  
		Last Modified: Thu, 02 Oct 2025 04:13:17 GMT  
		Size: 254.2 MB (254201580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b841d36c3f7927cf9372c9179a26e3ad7b96e087d61987e4c3c93d130d0aba`  
		Last Modified: Thu, 02 Oct 2025 01:32:57 GMT  
		Size: 14.3 MB (14320187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a208ad74359b046bf5040462407d27aa5fdd24a831bba4020936ec64aa14aac0`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 480.0 KB (480010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797a91a39f8ea3b3282c2f51da9c659b946e404d6006df059a8388971001bc30`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 377.7 MB (377732137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e4859d7c464de422a075630e2ca4ce2be8d286ddedd847194c281a6a018bb9`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16fba96da2d114e024b8969703d742a179c5edec8a48f7633c79f79c28112f3`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c88838d06b3d99b248a7040036e7c886b100b1bd9439a2bbe2557dd3601b2ee`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47db1384a0142d3ee7911da18de5e07c1e589452f2576c819808b679e5ca736`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:78d03bf942d9e0773375e3b891c67e19dd658088925f87ecf4725b41a235fc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61095573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f074c932f41b6417b4174a6101df0e73cb23cc333da764ab353d809a1c6fe5`

```dockerfile
```

-	Layers:
	-	`sha256:a44ec6ad328ae44c0999f11d6522aa0baf6d0dd292ee91500f7d6123291374f9`  
		Last Modified: Thu, 02 Oct 2025 04:14:06 GMT  
		Size: 61.1 MB (61068580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3455ba7fc1d3e481b7f5d5b7ab6a39aaf4fe4690a1f5affc8bcfe6409bc8cfd6`  
		Last Modified: Thu, 02 Oct 2025 04:14:08 GMT  
		Size: 27.0 KB (26993 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:a031fc8224c3c0e855415c69c5e8ba29f17e34ee47ed105ab8cc3a7008098966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.8 MB (695798442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e3871ab77cf8d77d84740eac9945b539221876dc1d88d090723ba9f3c46ade`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ace7e0079a18dcf2384ec390ef90a5595128c1ea5cdcf8e5e22341a2d14dc18`  
		Last Modified: Thu, 02 Oct 2025 03:44:06 GMT  
		Size: 378.4 MB (378416838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774389e9d09b12a08960d8c8d4534f9cbc06ebc46c34de3d20f84fc33000d38`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78ee5ca7ac877067f6a36562c78acb8d9a37ee3d26f4c13b70a202af84ba047`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063a1090c9c1b8a9ed22ad3d9bbaafbe9c28dec0b18f25dea14862aba04c37a3`  
		Last Modified: Thu, 02 Oct 2025 03:43:44 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2f4baba2896d6bf766aeab8aab6f5c95c6df77bceec7e6e9fb3ecc152fc6a8`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:e037e7ecf5829f94b0c0b6181b01bf014f812b2feed85cf950a43d34309e99f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61096586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4e90c59b5760cf46a5c5f609a411697a5c883c9f3675644744e08ef76072e7`

```dockerfile
```

-	Layers:
	-	`sha256:579761d83a62501577858d8099a228f604c49d1fa1a6ef6f6afa7f58d4ccd158`  
		Last Modified: Thu, 02 Oct 2025 04:15:53 GMT  
		Size: 61.1 MB (61069688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44edf985b4203c665ee17b86f252c11b6a52dfcbd3ac84395674243f342979a5`  
		Last Modified: Thu, 02 Oct 2025 04:15:54 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:b19b167d6c2cd15bc103761e63635025c08c6a4f4a8bb336066cc8c4125caaae
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
$ docker pull odoo@sha256:f23cf400f8caac66128bfb78dad613395195523b98ccc04c82802e9814327c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.4 MB (679371311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b28d9b277363dc886854b6b15fd3d1668167fd9e1e037338a890df051bf0b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74ade1303eb485c1ed295b3bd9e397f678c3f4172a4606f080ffae0d316d8f`  
		Last Modified: Thu, 02 Oct 2025 06:20:27 GMT  
		Size: 256.9 MB (256943828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35da4fd4e03d1fef0289b5a3761d80bd790f1c826d1a1e92602c62fc6735cf6`  
		Last Modified: Thu, 02 Oct 2025 05:16:59 GMT  
		Size: 14.3 MB (14339329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f4611b4df587836c21ff72c472b8b8dd8ffc710881db5e0b4785cccbb0c710`  
		Last Modified: Thu, 02 Oct 2025 05:16:58 GMT  
		Size: 480.0 KB (479986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee09c29c3619839eed40cb3d354ec97d3d8a759d360968d4e808c49aa2788801`  
		Last Modified: Thu, 02 Oct 2025 06:20:07 GMT  
		Size: 377.9 MB (377882721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23e80e12301c074d61599b1c06d8094d0b05416f733a67192d3baa7de6badd9`  
		Last Modified: Thu, 02 Oct 2025 05:16:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997f1553f8ff3be2aac6a4efbf4343c87972c16e755f22049510ea69851f0eb2`  
		Last Modified: Thu, 02 Oct 2025 05:16:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdecde88bf547f9148f113d396de94101ab44b350fcca237746a448772a363c2`  
		Last Modified: Thu, 02 Oct 2025 05:16:58 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db709be05ab1433caa8dca227fab279e6832e02ac4dc17289121d66f60c700d0`  
		Last Modified: Thu, 02 Oct 2025 05:16:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:13aa0c6b375ccd06f92e2542bf3195e6f26ac35fd3903490f329435cd21bec10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61088147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37798fa19b0279e5368af66b6f680cc21d5b3807934190b78399f71ff5e2394`

```dockerfile
```

-	Layers:
	-	`sha256:e7afacbc348a744623258e0a08e1e5b98af145fa0517312ec37be45c9542852b`  
		Last Modified: Thu, 02 Oct 2025 07:12:30 GMT  
		Size: 61.1 MB (61061305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb6d9d6f4622852bf59074df53654bf1326f817eb379fa413c61772b148ff50`  
		Last Modified: Thu, 02 Oct 2025 07:12:31 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0fa66f6d7b330830194b975496e69d54c59c346046d656bc25ad37d06357175e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.6 MB (675597933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8ce80de18b947e034f7d2b8b71f080fc50692513e6e6446d38181f572d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a3b4d011173c8f10be11a9ca76ac9af624f8c86c20474f6295f4072884d571`  
		Last Modified: Thu, 02 Oct 2025 04:13:17 GMT  
		Size: 254.2 MB (254201580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b841d36c3f7927cf9372c9179a26e3ad7b96e087d61987e4c3c93d130d0aba`  
		Last Modified: Thu, 02 Oct 2025 01:32:57 GMT  
		Size: 14.3 MB (14320187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a208ad74359b046bf5040462407d27aa5fdd24a831bba4020936ec64aa14aac0`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 480.0 KB (480010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797a91a39f8ea3b3282c2f51da9c659b946e404d6006df059a8388971001bc30`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 377.7 MB (377732137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e4859d7c464de422a075630e2ca4ce2be8d286ddedd847194c281a6a018bb9`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16fba96da2d114e024b8969703d742a179c5edec8a48f7633c79f79c28112f3`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c88838d06b3d99b248a7040036e7c886b100b1bd9439a2bbe2557dd3601b2ee`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47db1384a0142d3ee7911da18de5e07c1e589452f2576c819808b679e5ca736`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:78d03bf942d9e0773375e3b891c67e19dd658088925f87ecf4725b41a235fc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61095573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f074c932f41b6417b4174a6101df0e73cb23cc333da764ab353d809a1c6fe5`

```dockerfile
```

-	Layers:
	-	`sha256:a44ec6ad328ae44c0999f11d6522aa0baf6d0dd292ee91500f7d6123291374f9`  
		Last Modified: Thu, 02 Oct 2025 04:14:06 GMT  
		Size: 61.1 MB (61068580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3455ba7fc1d3e481b7f5d5b7ab6a39aaf4fe4690a1f5affc8bcfe6409bc8cfd6`  
		Last Modified: Thu, 02 Oct 2025 04:14:08 GMT  
		Size: 27.0 KB (26993 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:a031fc8224c3c0e855415c69c5e8ba29f17e34ee47ed105ab8cc3a7008098966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.8 MB (695798442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e3871ab77cf8d77d84740eac9945b539221876dc1d88d090723ba9f3c46ade`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ace7e0079a18dcf2384ec390ef90a5595128c1ea5cdcf8e5e22341a2d14dc18`  
		Last Modified: Thu, 02 Oct 2025 03:44:06 GMT  
		Size: 378.4 MB (378416838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774389e9d09b12a08960d8c8d4534f9cbc06ebc46c34de3d20f84fc33000d38`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78ee5ca7ac877067f6a36562c78acb8d9a37ee3d26f4c13b70a202af84ba047`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063a1090c9c1b8a9ed22ad3d9bbaafbe9c28dec0b18f25dea14862aba04c37a3`  
		Last Modified: Thu, 02 Oct 2025 03:43:44 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2f4baba2896d6bf766aeab8aab6f5c95c6df77bceec7e6e9fb3ecc152fc6a8`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e037e7ecf5829f94b0c0b6181b01bf014f812b2feed85cf950a43d34309e99f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61096586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4e90c59b5760cf46a5c5f609a411697a5c883c9f3675644744e08ef76072e7`

```dockerfile
```

-	Layers:
	-	`sha256:579761d83a62501577858d8099a228f604c49d1fa1a6ef6f6afa7f58d4ccd158`  
		Last Modified: Thu, 02 Oct 2025 04:15:53 GMT  
		Size: 61.1 MB (61069688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44edf985b4203c665ee17b86f252c11b6a52dfcbd3ac84395674243f342979a5`  
		Last Modified: Thu, 02 Oct 2025 04:15:54 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250930`

```console
$ docker pull odoo@sha256:b19b167d6c2cd15bc103761e63635025c08c6a4f4a8bb336066cc8c4125caaae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250930` - linux; amd64

```console
$ docker pull odoo@sha256:f23cf400f8caac66128bfb78dad613395195523b98ccc04c82802e9814327c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.4 MB (679371311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b28d9b277363dc886854b6b15fd3d1668167fd9e1e037338a890df051bf0b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74ade1303eb485c1ed295b3bd9e397f678c3f4172a4606f080ffae0d316d8f`  
		Last Modified: Thu, 02 Oct 2025 06:20:27 GMT  
		Size: 256.9 MB (256943828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35da4fd4e03d1fef0289b5a3761d80bd790f1c826d1a1e92602c62fc6735cf6`  
		Last Modified: Thu, 02 Oct 2025 05:16:59 GMT  
		Size: 14.3 MB (14339329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f4611b4df587836c21ff72c472b8b8dd8ffc710881db5e0b4785cccbb0c710`  
		Last Modified: Thu, 02 Oct 2025 05:16:58 GMT  
		Size: 480.0 KB (479986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee09c29c3619839eed40cb3d354ec97d3d8a759d360968d4e808c49aa2788801`  
		Last Modified: Thu, 02 Oct 2025 06:20:07 GMT  
		Size: 377.9 MB (377882721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23e80e12301c074d61599b1c06d8094d0b05416f733a67192d3baa7de6badd9`  
		Last Modified: Thu, 02 Oct 2025 05:16:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997f1553f8ff3be2aac6a4efbf4343c87972c16e755f22049510ea69851f0eb2`  
		Last Modified: Thu, 02 Oct 2025 05:16:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdecde88bf547f9148f113d396de94101ab44b350fcca237746a448772a363c2`  
		Last Modified: Thu, 02 Oct 2025 05:16:58 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db709be05ab1433caa8dca227fab279e6832e02ac4dc17289121d66f60c700d0`  
		Last Modified: Thu, 02 Oct 2025 05:16:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:13aa0c6b375ccd06f92e2542bf3195e6f26ac35fd3903490f329435cd21bec10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61088147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37798fa19b0279e5368af66b6f680cc21d5b3807934190b78399f71ff5e2394`

```dockerfile
```

-	Layers:
	-	`sha256:e7afacbc348a744623258e0a08e1e5b98af145fa0517312ec37be45c9542852b`  
		Last Modified: Thu, 02 Oct 2025 07:12:30 GMT  
		Size: 61.1 MB (61061305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb6d9d6f4622852bf59074df53654bf1326f817eb379fa413c61772b148ff50`  
		Last Modified: Thu, 02 Oct 2025 07:12:31 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250930` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0fa66f6d7b330830194b975496e69d54c59c346046d656bc25ad37d06357175e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.6 MB (675597933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8ce80de18b947e034f7d2b8b71f080fc50692513e6e6446d38181f572d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a3b4d011173c8f10be11a9ca76ac9af624f8c86c20474f6295f4072884d571`  
		Last Modified: Thu, 02 Oct 2025 04:13:17 GMT  
		Size: 254.2 MB (254201580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b841d36c3f7927cf9372c9179a26e3ad7b96e087d61987e4c3c93d130d0aba`  
		Last Modified: Thu, 02 Oct 2025 01:32:57 GMT  
		Size: 14.3 MB (14320187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a208ad74359b046bf5040462407d27aa5fdd24a831bba4020936ec64aa14aac0`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 480.0 KB (480010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797a91a39f8ea3b3282c2f51da9c659b946e404d6006df059a8388971001bc30`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 377.7 MB (377732137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e4859d7c464de422a075630e2ca4ce2be8d286ddedd847194c281a6a018bb9`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16fba96da2d114e024b8969703d742a179c5edec8a48f7633c79f79c28112f3`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c88838d06b3d99b248a7040036e7c886b100b1bd9439a2bbe2557dd3601b2ee`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47db1384a0142d3ee7911da18de5e07c1e589452f2576c819808b679e5ca736`  
		Last Modified: Thu, 02 Oct 2025 01:32:56 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:78d03bf942d9e0773375e3b891c67e19dd658088925f87ecf4725b41a235fc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61095573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f074c932f41b6417b4174a6101df0e73cb23cc333da764ab353d809a1c6fe5`

```dockerfile
```

-	Layers:
	-	`sha256:a44ec6ad328ae44c0999f11d6522aa0baf6d0dd292ee91500f7d6123291374f9`  
		Last Modified: Thu, 02 Oct 2025 04:14:06 GMT  
		Size: 61.1 MB (61068580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3455ba7fc1d3e481b7f5d5b7ab6a39aaf4fe4690a1f5affc8bcfe6409bc8cfd6`  
		Last Modified: Thu, 02 Oct 2025 04:14:08 GMT  
		Size: 27.0 KB (26993 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250930` - linux; ppc64le

```console
$ docker pull odoo@sha256:a031fc8224c3c0e855415c69c5e8ba29f17e34ee47ed105ab8cc3a7008098966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.8 MB (695798442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e3871ab77cf8d77d84740eac9945b539221876dc1d88d090723ba9f3c46ade`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ace7e0079a18dcf2384ec390ef90a5595128c1ea5cdcf8e5e22341a2d14dc18`  
		Last Modified: Thu, 02 Oct 2025 03:44:06 GMT  
		Size: 378.4 MB (378416838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c774389e9d09b12a08960d8c8d4534f9cbc06ebc46c34de3d20f84fc33000d38`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78ee5ca7ac877067f6a36562c78acb8d9a37ee3d26f4c13b70a202af84ba047`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063a1090c9c1b8a9ed22ad3d9bbaafbe9c28dec0b18f25dea14862aba04c37a3`  
		Last Modified: Thu, 02 Oct 2025 03:43:44 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2f4baba2896d6bf766aeab8aab6f5c95c6df77bceec7e6e9fb3ecc152fc6a8`  
		Last Modified: Thu, 02 Oct 2025 03:43:43 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:e037e7ecf5829f94b0c0b6181b01bf014f812b2feed85cf950a43d34309e99f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61096586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4e90c59b5760cf46a5c5f609a411697a5c883c9f3675644744e08ef76072e7`

```dockerfile
```

-	Layers:
	-	`sha256:579761d83a62501577858d8099a228f604c49d1fa1a6ef6f6afa7f58d4ccd158`  
		Last Modified: Thu, 02 Oct 2025 04:15:53 GMT  
		Size: 61.1 MB (61069688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44edf985b4203c665ee17b86f252c11b6a52dfcbd3ac84395674243f342979a5`  
		Last Modified: Thu, 02 Oct 2025 04:15:54 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:135083d15e23dcebb2b4449fd7f81f46966b407e3baef48bb278cde5b1956575
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
$ docker pull odoo@sha256:0e9993fc218fea1e2b657c927f918833920f94998b85deb8ae3f1d5f39d5b975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.7 MB (680728203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d1d6b3bf4bbe3a926bcf46e1a4d5addbe74ce74e15fd9f8b467697b8840904`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792a20e03e622922ae56fae61e65755012d8d8860a6928c48b8609aec7d8270b`  
		Last Modified: Thu, 02 Oct 2025 07:12:50 GMT  
		Size: 256.9 MB (256944529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2b33e72d143d84f38c4c44b5b1494537d65964a2e61f9192a91ce69808ccfa`  
		Last Modified: Thu, 02 Oct 2025 05:16:59 GMT  
		Size: 14.3 MB (14339336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee0b3c3efae080dea2f9ce1633eb12237ae98f5d48af6b64c05ba5d69fb787d`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 480.0 KB (479987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e09d0e29aaf869f014b01c31949663b83106758b380453efb08801976d6874`  
		Last Modified: Thu, 02 Oct 2025 07:13:01 GMT  
		Size: 379.2 MB (379238896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5f06a722926e5f2556ec7308c2a222b77276604ddc1101ff4d36233fb58ef6`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3124340f40efcf7b29b262645aacda9a13bdcd6508d4768712f69f2af616d72f`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9930c61a9b3769784952c1d4214e4121233c4d24969bcb6416dec6d49126cd6`  
		Last Modified: Thu, 02 Oct 2025 05:16:59 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6946082237ecce066df66a208ab4649bcda4738c52a337048e221087d6d978`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:e044932fecfadab18672e93313a933c123d4647a3d7a21315df54b21bfb93bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67733547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e8da9b65c7dda8f723812399cb4bbb9ac784390b4899720e5d0cb52da2a03e`

```dockerfile
```

-	Layers:
	-	`sha256:d2c5fd509d7673607ada50ecf35534d9677e8274449b7a66e18ca4f806aec4f6`  
		Last Modified: Thu, 02 Oct 2025 07:12:40 GMT  
		Size: 67.7 MB (67706411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95014b9b7a40cb716d18b1c50158a13e02349e705804bfa16b7812a1c5e4520d`  
		Last Modified: Thu, 02 Oct 2025 07:12:42 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:161ef89df3d75ff0fdca79e2b94355414a533bf4c62188e36bc646c7eb2b7fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 MB (676943329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a7d31b3862ab8b0808b8b57a18c3b537754030473b4a15d4fe393ed50ad4e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e5d2339a6059bc3c7a4ec252d57decfde3f20a6b77c2c8c1ca609e7f3c5947`  
		Last Modified: Thu, 02 Oct 2025 02:29:42 GMT  
		Size: 254.2 MB (254200999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5a203e7a483a9058423564f960e03a3fe532b12a62e27ff8d7825cde41429a`  
		Last Modified: Thu, 02 Oct 2025 01:33:23 GMT  
		Size: 14.3 MB (14320410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d18b1f6c0ff4014074f3b23f243269a39c595fe392c33a14c5e4a90e8ae86e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 480.0 KB (480001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf9f3a7b503dfe098b051887c35aba98d19a665729c8eb69a95289a145c72a1`  
		Last Modified: Thu, 02 Oct 2025 02:29:26 GMT  
		Size: 379.1 MB (379077904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256405c69c1fc96c4dd7de63cffefbe6780d3471751c4c287595b0907825dfe`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7695771ca09b4d8fecb368b5db9e5a0527560dbcbd4c1ceb08c8445facd3547`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835258a0402b4e8e31ad4d60f996a15d9591115b874535d8d858f2462446906f`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5f792e3ee7d0096b53edab4e87067ee725d5d5f438a4dc0ffb001ca5b2145e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:00df3783cd21e5005ac760b5a30caba31833cdb80961a4955ae88dc2c6023da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67740997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ead6c1c40247a474d98f48604150ce2164a028270de61f269b24315da699414`

```dockerfile
```

-	Layers:
	-	`sha256:2701eb48c73194f1e1ff74af919c9358d718977a70b0ec2a3232dc519b98b6b4`  
		Last Modified: Thu, 02 Oct 2025 04:14:35 GMT  
		Size: 67.7 MB (67713698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4db4bcfc15543405629d87c49a4c5f9c63ab41b3978a63c54c0760ea816f39`  
		Last Modified: Thu, 02 Oct 2025 04:14:36 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:526d3afb0efcd7fd170175d06cccebbcbea9fe75fd6efc3ceb23e5f3b27aa495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697159051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d365d96782efcbadf4b83fabfc795d2c1877848af8266085364ebb504613e87d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46792139f3c25fcd8010c37c4c037fc7f55941b626ba2139006b08486259db5b`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 379.8 MB (379777442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f2d9aa482942688bf3fb37fa6a67276a69da6439c60f7d216ad7678e7665d`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9f0c67d1977eda0e36d267d5dabb868eb94902c15eef84ef83191a14e70d70`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4159ac72157fbae13b6c612dbe75b29766ee70bc3f38b2191fdf9c06f3b850`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c7eb819eae59eb5b07081ad059f0337a075f2c76f6746f59263a733b15c7c6`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:78716b9f097b4776f69f1f752584fbcb23361957947b881a707c5914d2306e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67741998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a52a5c3dba67d56befc991c4e41258c4045a3a797a06307950dd5ecc85a4fe`

```dockerfile
```

-	Layers:
	-	`sha256:babaad4a2f86d393e73d58abccbc2095e201e366890f97f7055f32f76468f4c7`  
		Last Modified: Thu, 02 Oct 2025 04:16:17 GMT  
		Size: 67.7 MB (67714800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8da8184b442e0ef106f055139b568b90d7facd537c49987639eff0a55b205b`  
		Last Modified: Thu, 02 Oct 2025 04:16:18 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:135083d15e23dcebb2b4449fd7f81f46966b407e3baef48bb278cde5b1956575
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
$ docker pull odoo@sha256:0e9993fc218fea1e2b657c927f918833920f94998b85deb8ae3f1d5f39d5b975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.7 MB (680728203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d1d6b3bf4bbe3a926bcf46e1a4d5addbe74ce74e15fd9f8b467697b8840904`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792a20e03e622922ae56fae61e65755012d8d8860a6928c48b8609aec7d8270b`  
		Last Modified: Thu, 02 Oct 2025 07:12:50 GMT  
		Size: 256.9 MB (256944529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2b33e72d143d84f38c4c44b5b1494537d65964a2e61f9192a91ce69808ccfa`  
		Last Modified: Thu, 02 Oct 2025 05:16:59 GMT  
		Size: 14.3 MB (14339336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee0b3c3efae080dea2f9ce1633eb12237ae98f5d48af6b64c05ba5d69fb787d`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 480.0 KB (479987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e09d0e29aaf869f014b01c31949663b83106758b380453efb08801976d6874`  
		Last Modified: Thu, 02 Oct 2025 07:13:01 GMT  
		Size: 379.2 MB (379238896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5f06a722926e5f2556ec7308c2a222b77276604ddc1101ff4d36233fb58ef6`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3124340f40efcf7b29b262645aacda9a13bdcd6508d4768712f69f2af616d72f`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9930c61a9b3769784952c1d4214e4121233c4d24969bcb6416dec6d49126cd6`  
		Last Modified: Thu, 02 Oct 2025 05:16:59 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6946082237ecce066df66a208ab4649bcda4738c52a337048e221087d6d978`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e044932fecfadab18672e93313a933c123d4647a3d7a21315df54b21bfb93bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67733547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e8da9b65c7dda8f723812399cb4bbb9ac784390b4899720e5d0cb52da2a03e`

```dockerfile
```

-	Layers:
	-	`sha256:d2c5fd509d7673607ada50ecf35534d9677e8274449b7a66e18ca4f806aec4f6`  
		Last Modified: Thu, 02 Oct 2025 07:12:40 GMT  
		Size: 67.7 MB (67706411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95014b9b7a40cb716d18b1c50158a13e02349e705804bfa16b7812a1c5e4520d`  
		Last Modified: Thu, 02 Oct 2025 07:12:42 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:161ef89df3d75ff0fdca79e2b94355414a533bf4c62188e36bc646c7eb2b7fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 MB (676943329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a7d31b3862ab8b0808b8b57a18c3b537754030473b4a15d4fe393ed50ad4e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e5d2339a6059bc3c7a4ec252d57decfde3f20a6b77c2c8c1ca609e7f3c5947`  
		Last Modified: Thu, 02 Oct 2025 02:29:42 GMT  
		Size: 254.2 MB (254200999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5a203e7a483a9058423564f960e03a3fe532b12a62e27ff8d7825cde41429a`  
		Last Modified: Thu, 02 Oct 2025 01:33:23 GMT  
		Size: 14.3 MB (14320410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d18b1f6c0ff4014074f3b23f243269a39c595fe392c33a14c5e4a90e8ae86e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 480.0 KB (480001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf9f3a7b503dfe098b051887c35aba98d19a665729c8eb69a95289a145c72a1`  
		Last Modified: Thu, 02 Oct 2025 02:29:26 GMT  
		Size: 379.1 MB (379077904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256405c69c1fc96c4dd7de63cffefbe6780d3471751c4c287595b0907825dfe`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7695771ca09b4d8fecb368b5db9e5a0527560dbcbd4c1ceb08c8445facd3547`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835258a0402b4e8e31ad4d60f996a15d9591115b874535d8d858f2462446906f`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5f792e3ee7d0096b53edab4e87067ee725d5d5f438a4dc0ffb001ca5b2145e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:00df3783cd21e5005ac760b5a30caba31833cdb80961a4955ae88dc2c6023da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67740997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ead6c1c40247a474d98f48604150ce2164a028270de61f269b24315da699414`

```dockerfile
```

-	Layers:
	-	`sha256:2701eb48c73194f1e1ff74af919c9358d718977a70b0ec2a3232dc519b98b6b4`  
		Last Modified: Thu, 02 Oct 2025 04:14:35 GMT  
		Size: 67.7 MB (67713698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4db4bcfc15543405629d87c49a4c5f9c63ab41b3978a63c54c0760ea816f39`  
		Last Modified: Thu, 02 Oct 2025 04:14:36 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:526d3afb0efcd7fd170175d06cccebbcbea9fe75fd6efc3ceb23e5f3b27aa495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697159051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d365d96782efcbadf4b83fabfc795d2c1877848af8266085364ebb504613e87d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46792139f3c25fcd8010c37c4c037fc7f55941b626ba2139006b08486259db5b`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 379.8 MB (379777442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f2d9aa482942688bf3fb37fa6a67276a69da6439c60f7d216ad7678e7665d`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9f0c67d1977eda0e36d267d5dabb868eb94902c15eef84ef83191a14e70d70`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4159ac72157fbae13b6c612dbe75b29766ee70bc3f38b2191fdf9c06f3b850`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c7eb819eae59eb5b07081ad059f0337a075f2c76f6746f59263a733b15c7c6`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:78716b9f097b4776f69f1f752584fbcb23361957947b881a707c5914d2306e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67741998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a52a5c3dba67d56befc991c4e41258c4045a3a797a06307950dd5ecc85a4fe`

```dockerfile
```

-	Layers:
	-	`sha256:babaad4a2f86d393e73d58abccbc2095e201e366890f97f7055f32f76468f4c7`  
		Last Modified: Thu, 02 Oct 2025 04:16:17 GMT  
		Size: 67.7 MB (67714800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8da8184b442e0ef106f055139b568b90d7facd537c49987639eff0a55b205b`  
		Last Modified: Thu, 02 Oct 2025 04:16:18 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20250930`

```console
$ docker pull odoo@sha256:135083d15e23dcebb2b4449fd7f81f46966b407e3baef48bb278cde5b1956575
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20250930` - linux; amd64

```console
$ docker pull odoo@sha256:0e9993fc218fea1e2b657c927f918833920f94998b85deb8ae3f1d5f39d5b975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.7 MB (680728203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d1d6b3bf4bbe3a926bcf46e1a4d5addbe74ce74e15fd9f8b467697b8840904`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792a20e03e622922ae56fae61e65755012d8d8860a6928c48b8609aec7d8270b`  
		Last Modified: Thu, 02 Oct 2025 07:12:50 GMT  
		Size: 256.9 MB (256944529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2b33e72d143d84f38c4c44b5b1494537d65964a2e61f9192a91ce69808ccfa`  
		Last Modified: Thu, 02 Oct 2025 05:16:59 GMT  
		Size: 14.3 MB (14339336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee0b3c3efae080dea2f9ce1633eb12237ae98f5d48af6b64c05ba5d69fb787d`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 480.0 KB (479987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e09d0e29aaf869f014b01c31949663b83106758b380453efb08801976d6874`  
		Last Modified: Thu, 02 Oct 2025 07:13:01 GMT  
		Size: 379.2 MB (379238896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5f06a722926e5f2556ec7308c2a222b77276604ddc1101ff4d36233fb58ef6`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3124340f40efcf7b29b262645aacda9a13bdcd6508d4768712f69f2af616d72f`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9930c61a9b3769784952c1d4214e4121233c4d24969bcb6416dec6d49126cd6`  
		Last Modified: Thu, 02 Oct 2025 05:16:59 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6946082237ecce066df66a208ab4649bcda4738c52a337048e221087d6d978`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:e044932fecfadab18672e93313a933c123d4647a3d7a21315df54b21bfb93bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67733547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e8da9b65c7dda8f723812399cb4bbb9ac784390b4899720e5d0cb52da2a03e`

```dockerfile
```

-	Layers:
	-	`sha256:d2c5fd509d7673607ada50ecf35534d9677e8274449b7a66e18ca4f806aec4f6`  
		Last Modified: Thu, 02 Oct 2025 07:12:40 GMT  
		Size: 67.7 MB (67706411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95014b9b7a40cb716d18b1c50158a13e02349e705804bfa16b7812a1c5e4520d`  
		Last Modified: Thu, 02 Oct 2025 07:12:42 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20250930` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:161ef89df3d75ff0fdca79e2b94355414a533bf4c62188e36bc646c7eb2b7fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 MB (676943329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a7d31b3862ab8b0808b8b57a18c3b537754030473b4a15d4fe393ed50ad4e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e5d2339a6059bc3c7a4ec252d57decfde3f20a6b77c2c8c1ca609e7f3c5947`  
		Last Modified: Thu, 02 Oct 2025 02:29:42 GMT  
		Size: 254.2 MB (254200999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5a203e7a483a9058423564f960e03a3fe532b12a62e27ff8d7825cde41429a`  
		Last Modified: Thu, 02 Oct 2025 01:33:23 GMT  
		Size: 14.3 MB (14320410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d18b1f6c0ff4014074f3b23f243269a39c595fe392c33a14c5e4a90e8ae86e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 480.0 KB (480001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf9f3a7b503dfe098b051887c35aba98d19a665729c8eb69a95289a145c72a1`  
		Last Modified: Thu, 02 Oct 2025 02:29:26 GMT  
		Size: 379.1 MB (379077904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256405c69c1fc96c4dd7de63cffefbe6780d3471751c4c287595b0907825dfe`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7695771ca09b4d8fecb368b5db9e5a0527560dbcbd4c1ceb08c8445facd3547`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835258a0402b4e8e31ad4d60f996a15d9591115b874535d8d858f2462446906f`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5f792e3ee7d0096b53edab4e87067ee725d5d5f438a4dc0ffb001ca5b2145e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:00df3783cd21e5005ac760b5a30caba31833cdb80961a4955ae88dc2c6023da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67740997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ead6c1c40247a474d98f48604150ce2164a028270de61f269b24315da699414`

```dockerfile
```

-	Layers:
	-	`sha256:2701eb48c73194f1e1ff74af919c9358d718977a70b0ec2a3232dc519b98b6b4`  
		Last Modified: Thu, 02 Oct 2025 04:14:35 GMT  
		Size: 67.7 MB (67713698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4db4bcfc15543405629d87c49a4c5f9c63ab41b3978a63c54c0760ea816f39`  
		Last Modified: Thu, 02 Oct 2025 04:14:36 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20250930` - linux; ppc64le

```console
$ docker pull odoo@sha256:526d3afb0efcd7fd170175d06cccebbcbea9fe75fd6efc3ceb23e5f3b27aa495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697159051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d365d96782efcbadf4b83fabfc795d2c1877848af8266085364ebb504613e87d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46792139f3c25fcd8010c37c4c037fc7f55941b626ba2139006b08486259db5b`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 379.8 MB (379777442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f2d9aa482942688bf3fb37fa6a67276a69da6439c60f7d216ad7678e7665d`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9f0c67d1977eda0e36d267d5dabb868eb94902c15eef84ef83191a14e70d70`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4159ac72157fbae13b6c612dbe75b29766ee70bc3f38b2191fdf9c06f3b850`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c7eb819eae59eb5b07081ad059f0337a075f2c76f6746f59263a733b15c7c6`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:78716b9f097b4776f69f1f752584fbcb23361957947b881a707c5914d2306e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67741998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a52a5c3dba67d56befc991c4e41258c4045a3a797a06307950dd5ecc85a4fe`

```dockerfile
```

-	Layers:
	-	`sha256:babaad4a2f86d393e73d58abccbc2095e201e366890f97f7055f32f76468f4c7`  
		Last Modified: Thu, 02 Oct 2025 04:16:17 GMT  
		Size: 67.7 MB (67714800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8da8184b442e0ef106f055139b568b90d7facd537c49987639eff0a55b205b`  
		Last Modified: Thu, 02 Oct 2025 04:16:18 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:135083d15e23dcebb2b4449fd7f81f46966b407e3baef48bb278cde5b1956575
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
$ docker pull odoo@sha256:0e9993fc218fea1e2b657c927f918833920f94998b85deb8ae3f1d5f39d5b975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.7 MB (680728203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d1d6b3bf4bbe3a926bcf46e1a4d5addbe74ce74e15fd9f8b467697b8840904`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792a20e03e622922ae56fae61e65755012d8d8860a6928c48b8609aec7d8270b`  
		Last Modified: Thu, 02 Oct 2025 07:12:50 GMT  
		Size: 256.9 MB (256944529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2b33e72d143d84f38c4c44b5b1494537d65964a2e61f9192a91ce69808ccfa`  
		Last Modified: Thu, 02 Oct 2025 05:16:59 GMT  
		Size: 14.3 MB (14339336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee0b3c3efae080dea2f9ce1633eb12237ae98f5d48af6b64c05ba5d69fb787d`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 480.0 KB (479987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e09d0e29aaf869f014b01c31949663b83106758b380453efb08801976d6874`  
		Last Modified: Thu, 02 Oct 2025 07:13:01 GMT  
		Size: 379.2 MB (379238896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5f06a722926e5f2556ec7308c2a222b77276604ddc1101ff4d36233fb58ef6`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3124340f40efcf7b29b262645aacda9a13bdcd6508d4768712f69f2af616d72f`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9930c61a9b3769784952c1d4214e4121233c4d24969bcb6416dec6d49126cd6`  
		Last Modified: Thu, 02 Oct 2025 05:16:59 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6946082237ecce066df66a208ab4649bcda4738c52a337048e221087d6d978`  
		Last Modified: Thu, 02 Oct 2025 05:16:56 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:e044932fecfadab18672e93313a933c123d4647a3d7a21315df54b21bfb93bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67733547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e8da9b65c7dda8f723812399cb4bbb9ac784390b4899720e5d0cb52da2a03e`

```dockerfile
```

-	Layers:
	-	`sha256:d2c5fd509d7673607ada50ecf35534d9677e8274449b7a66e18ca4f806aec4f6`  
		Last Modified: Thu, 02 Oct 2025 07:12:40 GMT  
		Size: 67.7 MB (67706411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95014b9b7a40cb716d18b1c50158a13e02349e705804bfa16b7812a1c5e4520d`  
		Last Modified: Thu, 02 Oct 2025 07:12:42 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:161ef89df3d75ff0fdca79e2b94355414a533bf4c62188e36bc646c7eb2b7fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 MB (676943329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a7d31b3862ab8b0808b8b57a18c3b537754030473b4a15d4fe393ed50ad4e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e5d2339a6059bc3c7a4ec252d57decfde3f20a6b77c2c8c1ca609e7f3c5947`  
		Last Modified: Thu, 02 Oct 2025 02:29:42 GMT  
		Size: 254.2 MB (254200999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5a203e7a483a9058423564f960e03a3fe532b12a62e27ff8d7825cde41429a`  
		Last Modified: Thu, 02 Oct 2025 01:33:23 GMT  
		Size: 14.3 MB (14320410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d18b1f6c0ff4014074f3b23f243269a39c595fe392c33a14c5e4a90e8ae86e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 480.0 KB (480001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf9f3a7b503dfe098b051887c35aba98d19a665729c8eb69a95289a145c72a1`  
		Last Modified: Thu, 02 Oct 2025 02:29:26 GMT  
		Size: 379.1 MB (379077904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256405c69c1fc96c4dd7de63cffefbe6780d3471751c4c287595b0907825dfe`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7695771ca09b4d8fecb368b5db9e5a0527560dbcbd4c1ceb08c8445facd3547`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835258a0402b4e8e31ad4d60f996a15d9591115b874535d8d858f2462446906f`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5f792e3ee7d0096b53edab4e87067ee725d5d5f438a4dc0ffb001ca5b2145e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:00df3783cd21e5005ac760b5a30caba31833cdb80961a4955ae88dc2c6023da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67740997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ead6c1c40247a474d98f48604150ce2164a028270de61f269b24315da699414`

```dockerfile
```

-	Layers:
	-	`sha256:2701eb48c73194f1e1ff74af919c9358d718977a70b0ec2a3232dc519b98b6b4`  
		Last Modified: Thu, 02 Oct 2025 04:14:35 GMT  
		Size: 67.7 MB (67713698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4db4bcfc15543405629d87c49a4c5f9c63ab41b3978a63c54c0760ea816f39`  
		Last Modified: Thu, 02 Oct 2025 04:14:36 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:526d3afb0efcd7fd170175d06cccebbcbea9fe75fd6efc3ceb23e5f3b27aa495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697159051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d365d96782efcbadf4b83fabfc795d2c1877848af8266085364ebb504613e87d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46792139f3c25fcd8010c37c4c037fc7f55941b626ba2139006b08486259db5b`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 379.8 MB (379777442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f2d9aa482942688bf3fb37fa6a67276a69da6439c60f7d216ad7678e7665d`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9f0c67d1977eda0e36d267d5dabb868eb94902c15eef84ef83191a14e70d70`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4159ac72157fbae13b6c612dbe75b29766ee70bc3f38b2191fdf9c06f3b850`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c7eb819eae59eb5b07081ad059f0337a075f2c76f6746f59263a733b15c7c6`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:78716b9f097b4776f69f1f752584fbcb23361957947b881a707c5914d2306e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67741998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a52a5c3dba67d56befc991c4e41258c4045a3a797a06307950dd5ecc85a4fe`

```dockerfile
```

-	Layers:
	-	`sha256:babaad4a2f86d393e73d58abccbc2095e201e366890f97f7055f32f76468f4c7`  
		Last Modified: Thu, 02 Oct 2025 04:16:17 GMT  
		Size: 67.7 MB (67714800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8da8184b442e0ef106f055139b568b90d7facd537c49987639eff0a55b205b`  
		Last Modified: Thu, 02 Oct 2025 04:16:18 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
