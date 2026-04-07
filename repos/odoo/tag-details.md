<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260324`](#odoo170-20260324)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260324`](#odoo180-20260324)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260324`](#odoo190-20260324)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:2e33d9fcc8126c43d3a442abf5951e5b3255c53eac0733321c163ae8cc1a1294
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:06dd22ba616593a8398339da0251c35756ff26e85b371ddf50276c0592154c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.8 MB (609794736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5beea56738f9883deea562e15476e1261f43cb0ecaef76028176f6dfbbe55a4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:16:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Apr 2026 20:16:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Apr 2026 20:16:26 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:16:26 GMT
ARG TARGETARCH=amd64
# Wed, 01 Apr 2026 20:16:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 01 Apr 2026 20:16:33 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 01 Apr 2026 20:16:34 GMT
ENV ODOO_VERSION=17.0
# Wed, 01 Apr 2026 20:16:34 GMT
ARG ODOO_RELEASE=20260324
# Wed, 01 Apr 2026 20:16:34 GMT
ARG ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
# Wed, 01 Apr 2026 20:17:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 01 Apr 2026 20:17:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 01 Apr 2026 20:17:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 01 Apr 2026 20:17:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
USER odoo
# Wed, 01 Apr 2026 20:17:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2026 20:17:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab4ceaf43cf0a716caf425346f2a03a5244cd2f9adf1883cee6761fde78af1a`  
		Last Modified: Wed, 01 Apr 2026 20:18:59 GMT  
		Size: 233.8 MB (233831518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd5f8cd21db4a19ba6b1ed6b0b4dd4c08cf3ac783dacff8f000f811819ee137`  
		Last Modified: Wed, 01 Apr 2026 20:18:48 GMT  
		Size: 2.6 MB (2603667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96534bdb6ac6f744bb3fb07115390162e9740e286941d3b7beafcf2f98915105`  
		Last Modified: Wed, 01 Apr 2026 20:18:48 GMT  
		Size: 479.9 KB (479888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70b56cd7b46c15a5dfa3f2a14e5f93776744e6c0b4d2a6176d12da6c7c3416d`  
		Last Modified: Wed, 01 Apr 2026 20:19:02 GMT  
		Size: 343.1 MB (343140818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566d6cbf768f1bad4be7e8e6ce7088f5358e91e44477c63b9d8957fa0cd9d2c4`  
		Last Modified: Wed, 01 Apr 2026 20:18:49 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c824d7f36d4fc2ca6108d77b6901e9f845da44e43a67b726ba4912d9d3b092d6`  
		Last Modified: Wed, 01 Apr 2026 20:18:50 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2176fd2955393365ba94f1b31b13cd34a80bfb65b9d3b15bef1908f74de40fb`  
		Last Modified: Wed, 01 Apr 2026 20:18:51 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e47fb9c423e0eef51d97d2e342b9c4dbf3bd54502468976de59ecaf9cf3a5c7`  
		Last Modified: Wed, 01 Apr 2026 20:18:51 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:0a0a44bc9bdd3ca0b8920bd9ffd3c22bcc3e5fa08db0a4a71754e79d235720c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42890764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b3c4a31c0c351487d859eee94e84ca7e6aedaf3b22a9996ac8fd179937086`

```dockerfile
```

-	Layers:
	-	`sha256:8ada0a370c20b8d0b249d2306abbf6442f9f86d608f9279ce3101f6cfa329292`  
		Last Modified: Wed, 01 Apr 2026 20:18:51 GMT  
		Size: 42.9 MB (42863972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e1f69a0561df9d0734123f423414b2d3ab966068457a5fd039dc183732f8571`  
		Last Modified: Wed, 01 Apr 2026 20:18:48 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:746bed8138e7ff086caa1ff77469cca2a7ad4638a068904a9788bb2d4275e592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.6 MB (604638632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9a3c4c23ab8472c6e8a872027e15fed942df74aa0dd161e6390a82fbb2e012`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Apr 2026 20:15:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Apr 2026 20:15:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:15:36 GMT
ARG TARGETARCH=arm64
# Wed, 01 Apr 2026 20:15:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 01 Apr 2026 20:15:46 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:47 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 01 Apr 2026 20:15:47 GMT
ENV ODOO_VERSION=17.0
# Wed, 01 Apr 2026 20:15:47 GMT
ARG ODOO_RELEASE=20260324
# Wed, 01 Apr 2026 20:15:47 GMT
ARG ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
# Wed, 01 Apr 2026 20:16:52 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 01 Apr 2026 20:16:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 01 Apr 2026 20:16:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 01 Apr 2026 20:16:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
USER odoo
# Wed, 01 Apr 2026 20:16:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2026 20:16:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5323468b9fe47c33becf64e7fad967864d90448930dba5325635b63d8a340da`  
		Last Modified: Wed, 01 Apr 2026 20:18:22 GMT  
		Size: 231.2 MB (231200599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84decb908631e91de1dcf1db3c6bd153acbd75f44acd54e7a35535b3b9c9cdc`  
		Last Modified: Wed, 01 Apr 2026 20:18:12 GMT  
		Size: 2.6 MB (2598125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e96684d941b9dc5ecd2eccb0245d3480cd23c4dc36721cdc14ea87a6db171c0`  
		Last Modified: Wed, 01 Apr 2026 20:18:12 GMT  
		Size: 479.9 KB (479901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614309f8522eae6de5a5d49713ad8460060b60648a2dc1226149e0e0f45d8455`  
		Last Modified: Wed, 01 Apr 2026 20:18:26 GMT  
		Size: 342.8 MB (342750625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3545a499a034a1acf14181a50eb7de9146414abe94156be352002aec6cf3322`  
		Last Modified: Wed, 01 Apr 2026 20:18:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343de7b6834a06c372f3bf7e9262b708d0527a4515957038536f26991e45eab0`  
		Last Modified: Wed, 01 Apr 2026 20:18:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70782239ad45283b6c54afae450012ccd14767e1d34ea374790b2466ace06d1d`  
		Last Modified: Wed, 01 Apr 2026 20:18:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dbab03aaf251d189008ed918003cfb0fe3c86db8fc9533f2618a161b306251`  
		Last Modified: Wed, 01 Apr 2026 20:18:16 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:511ee1ee70b3b92329be6f83c502daef62496529faf1f50ae303e895aa928cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42897423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d2e1b0a50e1048e2d3583a0ebf72f34b6e1555a7897033875995321eea61cf`

```dockerfile
```

-	Layers:
	-	`sha256:38ac381f267a95c8af67543f0090394b25ece8a037bac450bf73efc9ce8a7480`  
		Last Modified: Wed, 01 Apr 2026 20:18:15 GMT  
		Size: 42.9 MB (42870479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd06bff75614412c7820216ed1e9e7258a8617e038f219cf821e0bfa0c364cbd`  
		Last Modified: Wed, 01 Apr 2026 20:18:12 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:2e33d9fcc8126c43d3a442abf5951e5b3255c53eac0733321c163ae8cc1a1294
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:06dd22ba616593a8398339da0251c35756ff26e85b371ddf50276c0592154c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.8 MB (609794736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5beea56738f9883deea562e15476e1261f43cb0ecaef76028176f6dfbbe55a4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:16:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Apr 2026 20:16:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Apr 2026 20:16:26 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:16:26 GMT
ARG TARGETARCH=amd64
# Wed, 01 Apr 2026 20:16:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 01 Apr 2026 20:16:33 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 01 Apr 2026 20:16:34 GMT
ENV ODOO_VERSION=17.0
# Wed, 01 Apr 2026 20:16:34 GMT
ARG ODOO_RELEASE=20260324
# Wed, 01 Apr 2026 20:16:34 GMT
ARG ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
# Wed, 01 Apr 2026 20:17:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 01 Apr 2026 20:17:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 01 Apr 2026 20:17:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 01 Apr 2026 20:17:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
USER odoo
# Wed, 01 Apr 2026 20:17:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2026 20:17:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab4ceaf43cf0a716caf425346f2a03a5244cd2f9adf1883cee6761fde78af1a`  
		Last Modified: Wed, 01 Apr 2026 20:18:59 GMT  
		Size: 233.8 MB (233831518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd5f8cd21db4a19ba6b1ed6b0b4dd4c08cf3ac783dacff8f000f811819ee137`  
		Last Modified: Wed, 01 Apr 2026 20:18:48 GMT  
		Size: 2.6 MB (2603667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96534bdb6ac6f744bb3fb07115390162e9740e286941d3b7beafcf2f98915105`  
		Last Modified: Wed, 01 Apr 2026 20:18:48 GMT  
		Size: 479.9 KB (479888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70b56cd7b46c15a5dfa3f2a14e5f93776744e6c0b4d2a6176d12da6c7c3416d`  
		Last Modified: Wed, 01 Apr 2026 20:19:02 GMT  
		Size: 343.1 MB (343140818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566d6cbf768f1bad4be7e8e6ce7088f5358e91e44477c63b9d8957fa0cd9d2c4`  
		Last Modified: Wed, 01 Apr 2026 20:18:49 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c824d7f36d4fc2ca6108d77b6901e9f845da44e43a67b726ba4912d9d3b092d6`  
		Last Modified: Wed, 01 Apr 2026 20:18:50 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2176fd2955393365ba94f1b31b13cd34a80bfb65b9d3b15bef1908f74de40fb`  
		Last Modified: Wed, 01 Apr 2026 20:18:51 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e47fb9c423e0eef51d97d2e342b9c4dbf3bd54502468976de59ecaf9cf3a5c7`  
		Last Modified: Wed, 01 Apr 2026 20:18:51 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0a0a44bc9bdd3ca0b8920bd9ffd3c22bcc3e5fa08db0a4a71754e79d235720c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42890764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b3c4a31c0c351487d859eee94e84ca7e6aedaf3b22a9996ac8fd179937086`

```dockerfile
```

-	Layers:
	-	`sha256:8ada0a370c20b8d0b249d2306abbf6442f9f86d608f9279ce3101f6cfa329292`  
		Last Modified: Wed, 01 Apr 2026 20:18:51 GMT  
		Size: 42.9 MB (42863972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e1f69a0561df9d0734123f423414b2d3ab966068457a5fd039dc183732f8571`  
		Last Modified: Wed, 01 Apr 2026 20:18:48 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:746bed8138e7ff086caa1ff77469cca2a7ad4638a068904a9788bb2d4275e592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.6 MB (604638632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9a3c4c23ab8472c6e8a872027e15fed942df74aa0dd161e6390a82fbb2e012`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Apr 2026 20:15:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Apr 2026 20:15:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:15:36 GMT
ARG TARGETARCH=arm64
# Wed, 01 Apr 2026 20:15:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 01 Apr 2026 20:15:46 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:47 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 01 Apr 2026 20:15:47 GMT
ENV ODOO_VERSION=17.0
# Wed, 01 Apr 2026 20:15:47 GMT
ARG ODOO_RELEASE=20260324
# Wed, 01 Apr 2026 20:15:47 GMT
ARG ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
# Wed, 01 Apr 2026 20:16:52 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 01 Apr 2026 20:16:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 01 Apr 2026 20:16:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 01 Apr 2026 20:16:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
USER odoo
# Wed, 01 Apr 2026 20:16:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2026 20:16:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5323468b9fe47c33becf64e7fad967864d90448930dba5325635b63d8a340da`  
		Last Modified: Wed, 01 Apr 2026 20:18:22 GMT  
		Size: 231.2 MB (231200599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84decb908631e91de1dcf1db3c6bd153acbd75f44acd54e7a35535b3b9c9cdc`  
		Last Modified: Wed, 01 Apr 2026 20:18:12 GMT  
		Size: 2.6 MB (2598125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e96684d941b9dc5ecd2eccb0245d3480cd23c4dc36721cdc14ea87a6db171c0`  
		Last Modified: Wed, 01 Apr 2026 20:18:12 GMT  
		Size: 479.9 KB (479901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614309f8522eae6de5a5d49713ad8460060b60648a2dc1226149e0e0f45d8455`  
		Last Modified: Wed, 01 Apr 2026 20:18:26 GMT  
		Size: 342.8 MB (342750625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3545a499a034a1acf14181a50eb7de9146414abe94156be352002aec6cf3322`  
		Last Modified: Wed, 01 Apr 2026 20:18:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343de7b6834a06c372f3bf7e9262b708d0527a4515957038536f26991e45eab0`  
		Last Modified: Wed, 01 Apr 2026 20:18:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70782239ad45283b6c54afae450012ccd14767e1d34ea374790b2466ace06d1d`  
		Last Modified: Wed, 01 Apr 2026 20:18:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dbab03aaf251d189008ed918003cfb0fe3c86db8fc9533f2618a161b306251`  
		Last Modified: Wed, 01 Apr 2026 20:18:16 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:511ee1ee70b3b92329be6f83c502daef62496529faf1f50ae303e895aa928cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42897423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d2e1b0a50e1048e2d3583a0ebf72f34b6e1555a7897033875995321eea61cf`

```dockerfile
```

-	Layers:
	-	`sha256:38ac381f267a95c8af67543f0090394b25ece8a037bac450bf73efc9ce8a7480`  
		Last Modified: Wed, 01 Apr 2026 20:18:15 GMT  
		Size: 42.9 MB (42870479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd06bff75614412c7820216ed1e9e7258a8617e038f219cf821e0bfa0c364cbd`  
		Last Modified: Wed, 01 Apr 2026 20:18:12 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260324`

```console
$ docker pull odoo@sha256:2e33d9fcc8126c43d3a442abf5951e5b3255c53eac0733321c163ae8cc1a1294
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260324` - linux; amd64

```console
$ docker pull odoo@sha256:06dd22ba616593a8398339da0251c35756ff26e85b371ddf50276c0592154c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.8 MB (609794736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5beea56738f9883deea562e15476e1261f43cb0ecaef76028176f6dfbbe55a4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:16:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Apr 2026 20:16:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Apr 2026 20:16:26 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:16:26 GMT
ARG TARGETARCH=amd64
# Wed, 01 Apr 2026 20:16:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 01 Apr 2026 20:16:33 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 01 Apr 2026 20:16:34 GMT
ENV ODOO_VERSION=17.0
# Wed, 01 Apr 2026 20:16:34 GMT
ARG ODOO_RELEASE=20260324
# Wed, 01 Apr 2026 20:16:34 GMT
ARG ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
# Wed, 01 Apr 2026 20:17:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 01 Apr 2026 20:17:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 01 Apr 2026 20:17:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 01 Apr 2026 20:17:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 01 Apr 2026 20:17:34 GMT
USER odoo
# Wed, 01 Apr 2026 20:17:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2026 20:17:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab4ceaf43cf0a716caf425346f2a03a5244cd2f9adf1883cee6761fde78af1a`  
		Last Modified: Wed, 01 Apr 2026 20:18:59 GMT  
		Size: 233.8 MB (233831518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd5f8cd21db4a19ba6b1ed6b0b4dd4c08cf3ac783dacff8f000f811819ee137`  
		Last Modified: Wed, 01 Apr 2026 20:18:48 GMT  
		Size: 2.6 MB (2603667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96534bdb6ac6f744bb3fb07115390162e9740e286941d3b7beafcf2f98915105`  
		Last Modified: Wed, 01 Apr 2026 20:18:48 GMT  
		Size: 479.9 KB (479888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70b56cd7b46c15a5dfa3f2a14e5f93776744e6c0b4d2a6176d12da6c7c3416d`  
		Last Modified: Wed, 01 Apr 2026 20:19:02 GMT  
		Size: 343.1 MB (343140818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566d6cbf768f1bad4be7e8e6ce7088f5358e91e44477c63b9d8957fa0cd9d2c4`  
		Last Modified: Wed, 01 Apr 2026 20:18:49 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c824d7f36d4fc2ca6108d77b6901e9f845da44e43a67b726ba4912d9d3b092d6`  
		Last Modified: Wed, 01 Apr 2026 20:18:50 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2176fd2955393365ba94f1b31b13cd34a80bfb65b9d3b15bef1908f74de40fb`  
		Last Modified: Wed, 01 Apr 2026 20:18:51 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e47fb9c423e0eef51d97d2e342b9c4dbf3bd54502468976de59ecaf9cf3a5c7`  
		Last Modified: Wed, 01 Apr 2026 20:18:51 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:0a0a44bc9bdd3ca0b8920bd9ffd3c22bcc3e5fa08db0a4a71754e79d235720c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42890764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b3c4a31c0c351487d859eee94e84ca7e6aedaf3b22a9996ac8fd179937086`

```dockerfile
```

-	Layers:
	-	`sha256:8ada0a370c20b8d0b249d2306abbf6442f9f86d608f9279ce3101f6cfa329292`  
		Last Modified: Wed, 01 Apr 2026 20:18:51 GMT  
		Size: 42.9 MB (42863972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e1f69a0561df9d0734123f423414b2d3ab966068457a5fd039dc183732f8571`  
		Last Modified: Wed, 01 Apr 2026 20:18:48 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20260324` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:746bed8138e7ff086caa1ff77469cca2a7ad4638a068904a9788bb2d4275e592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.6 MB (604638632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9a3c4c23ab8472c6e8a872027e15fed942df74aa0dd161e6390a82fbb2e012`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:15:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Apr 2026 20:15:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Apr 2026 20:15:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:15:36 GMT
ARG TARGETARCH=arm64
# Wed, 01 Apr 2026 20:15:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 01 Apr 2026 20:15:46 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:15:47 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 01 Apr 2026 20:15:47 GMT
ENV ODOO_VERSION=17.0
# Wed, 01 Apr 2026 20:15:47 GMT
ARG ODOO_RELEASE=20260324
# Wed, 01 Apr 2026 20:15:47 GMT
ARG ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
# Wed, 01 Apr 2026 20:16:52 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 01 Apr 2026 20:16:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 01 Apr 2026 20:16:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 01 Apr 2026 20:16:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 01 Apr 2026 20:16:53 GMT
USER odoo
# Wed, 01 Apr 2026 20:16:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Apr 2026 20:16:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5323468b9fe47c33becf64e7fad967864d90448930dba5325635b63d8a340da`  
		Last Modified: Wed, 01 Apr 2026 20:18:22 GMT  
		Size: 231.2 MB (231200599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84decb908631e91de1dcf1db3c6bd153acbd75f44acd54e7a35535b3b9c9cdc`  
		Last Modified: Wed, 01 Apr 2026 20:18:12 GMT  
		Size: 2.6 MB (2598125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e96684d941b9dc5ecd2eccb0245d3480cd23c4dc36721cdc14ea87a6db171c0`  
		Last Modified: Wed, 01 Apr 2026 20:18:12 GMT  
		Size: 479.9 KB (479901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614309f8522eae6de5a5d49713ad8460060b60648a2dc1226149e0e0f45d8455`  
		Last Modified: Wed, 01 Apr 2026 20:18:26 GMT  
		Size: 342.8 MB (342750625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3545a499a034a1acf14181a50eb7de9146414abe94156be352002aec6cf3322`  
		Last Modified: Wed, 01 Apr 2026 20:18:13 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343de7b6834a06c372f3bf7e9262b708d0527a4515957038536f26991e45eab0`  
		Last Modified: Wed, 01 Apr 2026 20:18:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70782239ad45283b6c54afae450012ccd14767e1d34ea374790b2466ace06d1d`  
		Last Modified: Wed, 01 Apr 2026 20:18:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dbab03aaf251d189008ed918003cfb0fe3c86db8fc9533f2618a161b306251`  
		Last Modified: Wed, 01 Apr 2026 20:18:16 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:511ee1ee70b3b92329be6f83c502daef62496529faf1f50ae303e895aa928cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42897423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d2e1b0a50e1048e2d3583a0ebf72f34b6e1555a7897033875995321eea61cf`

```dockerfile
```

-	Layers:
	-	`sha256:38ac381f267a95c8af67543f0090394b25ece8a037bac450bf73efc9ce8a7480`  
		Last Modified: Wed, 01 Apr 2026 20:18:15 GMT  
		Size: 42.9 MB (42870479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd06bff75614412c7820216ed1e9e7258a8617e038f219cf821e0bfa0c364cbd`  
		Last Modified: Wed, 01 Apr 2026 20:18:12 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:8a6ab76c7b01b40ee5bf1f8394af1356fcfc8093786178a907f5d4638264143c
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
$ docker pull odoo@sha256:83d03052db3b2a2e74a08b85623d1fa2442eea26fe30a4b6ea55c23c2d2acdc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.6 MB (683613199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87384d344c420fe1b87ff2a3c341854a0ce2e961d03a9db342c427def5eb2a28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:03:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:03:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:03:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:03:58 GMT
ARG TARGETARCH=amd64
# Tue, 07 Apr 2026 02:03:58 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:04:07 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:08 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:04:08 GMT
ENV ODOO_VERSION=18.0
# Tue, 07 Apr 2026 02:04:08 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:04:08 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 07 Apr 2026 02:04:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:04:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:04:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:04:59 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
USER odoo
# Tue, 07 Apr 2026 02:04:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:04:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6716c5b9cda8609965fcf2568c1c52fb4953b833e786b2652fd5eb942ec9dd`  
		Last Modified: Tue, 07 Apr 2026 02:06:57 GMT  
		Size: 254.6 MB (254568959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e37d92a6f1ecb968efdba2a1649431d0bf457fbe004f0b2848b6428099ad1ba`  
		Last Modified: Tue, 07 Apr 2026 02:06:47 GMT  
		Size: 14.4 MB (14360241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49bdb204a16257063929c34dfcf7110c3f02154f51a92ddae73a8d1eedd38f9`  
		Last Modified: Tue, 07 Apr 2026 02:06:45 GMT  
		Size: 479.7 KB (479652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212da6216a42b0c5ad59eeb216eab7ca71afee300476465f17fa172e8f75b1b`  
		Last Modified: Tue, 07 Apr 2026 02:06:59 GMT  
		Size: 384.5 MB (384468450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4693965853a32be01a599fd5f1f96491a31f8aa581a7ad164aa8ccae6f4c874`  
		Last Modified: Tue, 07 Apr 2026 02:06:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b77bc73f26f48771b1c053c9d95e561422b6dd55d999db9d5edb1a89ac3e3fd`  
		Last Modified: Tue, 07 Apr 2026 02:06:48 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f817274f69cec7232c26b038a98ecf703aa109682ef3f7c7f6ee56b2b3ccb4e`  
		Last Modified: Tue, 07 Apr 2026 02:06:48 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59959f1c9d707a2edd36384ad5f711a36f7d5be165ea4e4ca5b07937a0570084`  
		Last Modified: Tue, 07 Apr 2026 02:06:50 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:372f9c4eef0073200a21d27602d487ac09dae4a2307b553a1d88327094cbb3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62159366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711d069c8e165318bc08f42ad87640c05de277b7739879887a8e01733f6b5974`

```dockerfile
```

-	Layers:
	-	`sha256:f97155036b6dc2b04f9ca25c5c46a3c842915df1ab30b1ca1f0a6cf5a851d457`  
		Last Modified: Tue, 07 Apr 2026 02:06:50 GMT  
		Size: 62.1 MB (62132567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:212ca401bd97ff5011e13ae119ac05163012310a653e74591ab4043425d99f53`  
		Last Modified: Tue, 07 Apr 2026 02:06:46 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3110ee913bead95a4c23706f5915ccf4c8bab6da0dec151961e11b3e916ba66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.0 MB (680006136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fea6ecc224dd57c1735c141772456cfe8eb4a9959ddadceaddb74a03ce949f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:43:05 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:43:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:43:05 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:43:05 GMT
ARG TARGETARCH=arm64
# Tue, 07 Apr 2026 02:43:05 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:43:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:43:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:43:17 GMT
ENV ODOO_VERSION=18.0
# Tue, 07 Apr 2026 02:43:17 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:43:17 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 07 Apr 2026 02:44:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:44:23 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:44:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:44:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
USER odoo
# Tue, 07 Apr 2026 02:44:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:44:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84695fcff934393663b30f066216ec7f48081aefba9da49828d4d8db0f7b6d3`  
		Last Modified: Tue, 07 Apr 2026 02:46:47 GMT  
		Size: 252.0 MB (251996001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35472ccd661285bbf9e35acc9bd9b31d86da5e212926fff1e8b040c5cf38bfd`  
		Last Modified: Tue, 07 Apr 2026 02:46:39 GMT  
		Size: 14.3 MB (14340887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df846acc75ae1d7cbe75474082e770764fa4777b552b451d8fd2c8455fda66f`  
		Last Modified: Tue, 07 Apr 2026 02:46:37 GMT  
		Size: 479.7 KB (479671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373a2f386b1b99f8bfd222705dfa3d8adf76d31011511a00111e4171524f4428`  
		Last Modified: Tue, 07 Apr 2026 02:46:50 GMT  
		Size: 384.3 MB (384313063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1923eef19fa0e483bb8164f1f04ba152bb0d40a13bd12a477d94b32df97bc`  
		Last Modified: Tue, 07 Apr 2026 02:46:39 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3888b18a3ef8ad70ef55d1b735f79e3d9275b551057e43ffcaf8d45af068041`  
		Last Modified: Tue, 07 Apr 2026 02:46:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0e4bfad9129439d642fdaac60a313c9b245b952a55988fe67f280bf35a20cd`  
		Last Modified: Tue, 07 Apr 2026 02:46:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a12db641e02f4bb4132d486d9c51b1f53a11367bc8e5aea166030e2720b2d4c`  
		Last Modified: Tue, 07 Apr 2026 02:46:41 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:e4e1f2d330e0ecd057bdf8c121336bdf76d7e84d171c74045acabe92a175e739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62166793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3919dbcd571fdab9fc3b77277bfa3db69bf7757fa45a21fdb79980d4be0d9bc`

```dockerfile
```

-	Layers:
	-	`sha256:eb3672c333b4d8d61a2b39a858c42bee5471c4c30b4264325ec0fa343c72cca3`  
		Last Modified: Tue, 07 Apr 2026 02:46:41 GMT  
		Size: 62.1 MB (62139842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e699527c2e974be6e8acc26293673fb5cc219a391e9bcf2434d2884cbb6c96d7`  
		Last Modified: Tue, 07 Apr 2026 02:46:37 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:a9163feaac6f9aa545f4d23404bb296ddda21c69e7db51326245be29024d2007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.8 MB (699797001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c596237736b65e38d215b0cd2c0d04deed0312d06dc50590c27538aae67493`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 05:16:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 05:16:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 05:16:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 05:16:49 GMT
ARG TARGETARCH=ppc64le
# Tue, 07 Apr 2026 05:16:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 05:17:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
ENV ODOO_VERSION=18.0
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 07 Apr 2026 05:19:33 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 05:19:34 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 05:19:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 05:19:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 05:19:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 05:19:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 05:19:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 05:19:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 05:19:35 GMT
USER odoo
# Tue, 07 Apr 2026 05:19:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 05:19:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74487ed95f50675350fffef58826e35fc796b98c0e021234a16f225ffda4c6a`  
		Last Modified: Tue, 07 Apr 2026 05:24:13 GMT  
		Size: 265.1 MB (265109939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94274f5bc4aef8440fa4da1c54ad73af3dca9728f356c0bd034e73c27c360cd`  
		Last Modified: Tue, 07 Apr 2026 05:24:03 GMT  
		Size: 14.9 MB (14893935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba0cc6d20592598467e8e83a903cf7cf6db59a24e397ca7116cbb9e31a40e3`  
		Last Modified: Tue, 07 Apr 2026 05:24:02 GMT  
		Size: 479.7 KB (479745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8b63a445df3f4df0dacbd0bb79dfeec7ce2e947ff2a0697039a93cfd54def1`  
		Last Modified: Tue, 07 Apr 2026 05:24:15 GMT  
		Size: 385.0 MB (384997612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc3ac51180595f4a3e1b99b1345f7e413b840842092bf96751975749ee1861b`  
		Last Modified: Tue, 07 Apr 2026 05:24:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faed336efd8d8ce0c079ab133291e95b5ac02b9997e12f8244264cfa18f0a77c`  
		Last Modified: Tue, 07 Apr 2026 05:24:04 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45d8339723d140616d252e349b9faa6640c5dca20f481ddbc6f6c6a438a846`  
		Last Modified: Tue, 07 Apr 2026 05:24:04 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e51fde825458322566fcbb94fcac9f090a29be89ebf41ac800966cdc6794ce`  
		Last Modified: Tue, 07 Apr 2026 05:24:06 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:c722145640b5c0d20c08db3dfb4c42a197c870f6cbf86e74b35053598dd5f09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62167805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bf0510c5888891f2e2a11d4f1c66ef827f80176ebf77dfc4ef3c389e60b55e`

```dockerfile
```

-	Layers:
	-	`sha256:f0e6a279a187c024fe2b1a2e466c0be193efd4cb615f0752bcc12886cb9e61c9`  
		Last Modified: Tue, 07 Apr 2026 05:24:07 GMT  
		Size: 62.1 MB (62140950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbb0c7f3085370190924e6e64934c8966448962d876f4333c427c396bb57aa9`  
		Last Modified: Tue, 07 Apr 2026 05:24:01 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:8a6ab76c7b01b40ee5bf1f8394af1356fcfc8093786178a907f5d4638264143c
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
$ docker pull odoo@sha256:83d03052db3b2a2e74a08b85623d1fa2442eea26fe30a4b6ea55c23c2d2acdc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.6 MB (683613199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87384d344c420fe1b87ff2a3c341854a0ce2e961d03a9db342c427def5eb2a28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:03:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:03:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:03:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:03:58 GMT
ARG TARGETARCH=amd64
# Tue, 07 Apr 2026 02:03:58 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:04:07 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:08 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:04:08 GMT
ENV ODOO_VERSION=18.0
# Tue, 07 Apr 2026 02:04:08 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:04:08 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 07 Apr 2026 02:04:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:04:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:04:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:04:59 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
USER odoo
# Tue, 07 Apr 2026 02:04:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:04:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6716c5b9cda8609965fcf2568c1c52fb4953b833e786b2652fd5eb942ec9dd`  
		Last Modified: Tue, 07 Apr 2026 02:06:57 GMT  
		Size: 254.6 MB (254568959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e37d92a6f1ecb968efdba2a1649431d0bf457fbe004f0b2848b6428099ad1ba`  
		Last Modified: Tue, 07 Apr 2026 02:06:47 GMT  
		Size: 14.4 MB (14360241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49bdb204a16257063929c34dfcf7110c3f02154f51a92ddae73a8d1eedd38f9`  
		Last Modified: Tue, 07 Apr 2026 02:06:45 GMT  
		Size: 479.7 KB (479652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212da6216a42b0c5ad59eeb216eab7ca71afee300476465f17fa172e8f75b1b`  
		Last Modified: Tue, 07 Apr 2026 02:06:59 GMT  
		Size: 384.5 MB (384468450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4693965853a32be01a599fd5f1f96491a31f8aa581a7ad164aa8ccae6f4c874`  
		Last Modified: Tue, 07 Apr 2026 02:06:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b77bc73f26f48771b1c053c9d95e561422b6dd55d999db9d5edb1a89ac3e3fd`  
		Last Modified: Tue, 07 Apr 2026 02:06:48 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f817274f69cec7232c26b038a98ecf703aa109682ef3f7c7f6ee56b2b3ccb4e`  
		Last Modified: Tue, 07 Apr 2026 02:06:48 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59959f1c9d707a2edd36384ad5f711a36f7d5be165ea4e4ca5b07937a0570084`  
		Last Modified: Tue, 07 Apr 2026 02:06:50 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:372f9c4eef0073200a21d27602d487ac09dae4a2307b553a1d88327094cbb3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62159366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711d069c8e165318bc08f42ad87640c05de277b7739879887a8e01733f6b5974`

```dockerfile
```

-	Layers:
	-	`sha256:f97155036b6dc2b04f9ca25c5c46a3c842915df1ab30b1ca1f0a6cf5a851d457`  
		Last Modified: Tue, 07 Apr 2026 02:06:50 GMT  
		Size: 62.1 MB (62132567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:212ca401bd97ff5011e13ae119ac05163012310a653e74591ab4043425d99f53`  
		Last Modified: Tue, 07 Apr 2026 02:06:46 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3110ee913bead95a4c23706f5915ccf4c8bab6da0dec151961e11b3e916ba66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.0 MB (680006136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fea6ecc224dd57c1735c141772456cfe8eb4a9959ddadceaddb74a03ce949f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:43:05 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:43:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:43:05 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:43:05 GMT
ARG TARGETARCH=arm64
# Tue, 07 Apr 2026 02:43:05 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:43:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:43:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:43:17 GMT
ENV ODOO_VERSION=18.0
# Tue, 07 Apr 2026 02:43:17 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:43:17 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 07 Apr 2026 02:44:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:44:23 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:44:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:44:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
USER odoo
# Tue, 07 Apr 2026 02:44:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:44:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84695fcff934393663b30f066216ec7f48081aefba9da49828d4d8db0f7b6d3`  
		Last Modified: Tue, 07 Apr 2026 02:46:47 GMT  
		Size: 252.0 MB (251996001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35472ccd661285bbf9e35acc9bd9b31d86da5e212926fff1e8b040c5cf38bfd`  
		Last Modified: Tue, 07 Apr 2026 02:46:39 GMT  
		Size: 14.3 MB (14340887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df846acc75ae1d7cbe75474082e770764fa4777b552b451d8fd2c8455fda66f`  
		Last Modified: Tue, 07 Apr 2026 02:46:37 GMT  
		Size: 479.7 KB (479671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373a2f386b1b99f8bfd222705dfa3d8adf76d31011511a00111e4171524f4428`  
		Last Modified: Tue, 07 Apr 2026 02:46:50 GMT  
		Size: 384.3 MB (384313063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1923eef19fa0e483bb8164f1f04ba152bb0d40a13bd12a477d94b32df97bc`  
		Last Modified: Tue, 07 Apr 2026 02:46:39 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3888b18a3ef8ad70ef55d1b735f79e3d9275b551057e43ffcaf8d45af068041`  
		Last Modified: Tue, 07 Apr 2026 02:46:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0e4bfad9129439d642fdaac60a313c9b245b952a55988fe67f280bf35a20cd`  
		Last Modified: Tue, 07 Apr 2026 02:46:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a12db641e02f4bb4132d486d9c51b1f53a11367bc8e5aea166030e2720b2d4c`  
		Last Modified: Tue, 07 Apr 2026 02:46:41 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e4e1f2d330e0ecd057bdf8c121336bdf76d7e84d171c74045acabe92a175e739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62166793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3919dbcd571fdab9fc3b77277bfa3db69bf7757fa45a21fdb79980d4be0d9bc`

```dockerfile
```

-	Layers:
	-	`sha256:eb3672c333b4d8d61a2b39a858c42bee5471c4c30b4264325ec0fa343c72cca3`  
		Last Modified: Tue, 07 Apr 2026 02:46:41 GMT  
		Size: 62.1 MB (62139842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e699527c2e974be6e8acc26293673fb5cc219a391e9bcf2434d2884cbb6c96d7`  
		Last Modified: Tue, 07 Apr 2026 02:46:37 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:a9163feaac6f9aa545f4d23404bb296ddda21c69e7db51326245be29024d2007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.8 MB (699797001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c596237736b65e38d215b0cd2c0d04deed0312d06dc50590c27538aae67493`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 05:16:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 05:16:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 05:16:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 05:16:49 GMT
ARG TARGETARCH=ppc64le
# Tue, 07 Apr 2026 05:16:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 05:17:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
ENV ODOO_VERSION=18.0
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 07 Apr 2026 05:19:33 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 05:19:34 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 05:19:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 05:19:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 05:19:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 05:19:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 05:19:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 05:19:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 05:19:35 GMT
USER odoo
# Tue, 07 Apr 2026 05:19:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 05:19:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74487ed95f50675350fffef58826e35fc796b98c0e021234a16f225ffda4c6a`  
		Last Modified: Tue, 07 Apr 2026 05:24:13 GMT  
		Size: 265.1 MB (265109939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94274f5bc4aef8440fa4da1c54ad73af3dca9728f356c0bd034e73c27c360cd`  
		Last Modified: Tue, 07 Apr 2026 05:24:03 GMT  
		Size: 14.9 MB (14893935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba0cc6d20592598467e8e83a903cf7cf6db59a24e397ca7116cbb9e31a40e3`  
		Last Modified: Tue, 07 Apr 2026 05:24:02 GMT  
		Size: 479.7 KB (479745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8b63a445df3f4df0dacbd0bb79dfeec7ce2e947ff2a0697039a93cfd54def1`  
		Last Modified: Tue, 07 Apr 2026 05:24:15 GMT  
		Size: 385.0 MB (384997612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc3ac51180595f4a3e1b99b1345f7e413b840842092bf96751975749ee1861b`  
		Last Modified: Tue, 07 Apr 2026 05:24:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faed336efd8d8ce0c079ab133291e95b5ac02b9997e12f8244264cfa18f0a77c`  
		Last Modified: Tue, 07 Apr 2026 05:24:04 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45d8339723d140616d252e349b9faa6640c5dca20f481ddbc6f6c6a438a846`  
		Last Modified: Tue, 07 Apr 2026 05:24:04 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e51fde825458322566fcbb94fcac9f090a29be89ebf41ac800966cdc6794ce`  
		Last Modified: Tue, 07 Apr 2026 05:24:06 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c722145640b5c0d20c08db3dfb4c42a197c870f6cbf86e74b35053598dd5f09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62167805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bf0510c5888891f2e2a11d4f1c66ef827f80176ebf77dfc4ef3c389e60b55e`

```dockerfile
```

-	Layers:
	-	`sha256:f0e6a279a187c024fe2b1a2e466c0be193efd4cb615f0752bcc12886cb9e61c9`  
		Last Modified: Tue, 07 Apr 2026 05:24:07 GMT  
		Size: 62.1 MB (62140950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbb0c7f3085370190924e6e64934c8966448962d876f4333c427c396bb57aa9`  
		Last Modified: Tue, 07 Apr 2026 05:24:01 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260324`

```console
$ docker pull odoo@sha256:8a6ab76c7b01b40ee5bf1f8394af1356fcfc8093786178a907f5d4638264143c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260324` - linux; amd64

```console
$ docker pull odoo@sha256:83d03052db3b2a2e74a08b85623d1fa2442eea26fe30a4b6ea55c23c2d2acdc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.6 MB (683613199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87384d344c420fe1b87ff2a3c341854a0ce2e961d03a9db342c427def5eb2a28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:03:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:03:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:03:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:03:58 GMT
ARG TARGETARCH=amd64
# Tue, 07 Apr 2026 02:03:58 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:04:07 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:08 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:04:08 GMT
ENV ODOO_VERSION=18.0
# Tue, 07 Apr 2026 02:04:08 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:04:08 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 07 Apr 2026 02:04:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:04:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:04:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:04:59 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:04:59 GMT
USER odoo
# Tue, 07 Apr 2026 02:04:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:04:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6716c5b9cda8609965fcf2568c1c52fb4953b833e786b2652fd5eb942ec9dd`  
		Last Modified: Tue, 07 Apr 2026 02:06:57 GMT  
		Size: 254.6 MB (254568959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e37d92a6f1ecb968efdba2a1649431d0bf457fbe004f0b2848b6428099ad1ba`  
		Last Modified: Tue, 07 Apr 2026 02:06:47 GMT  
		Size: 14.4 MB (14360241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49bdb204a16257063929c34dfcf7110c3f02154f51a92ddae73a8d1eedd38f9`  
		Last Modified: Tue, 07 Apr 2026 02:06:45 GMT  
		Size: 479.7 KB (479652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212da6216a42b0c5ad59eeb216eab7ca71afee300476465f17fa172e8f75b1b`  
		Last Modified: Tue, 07 Apr 2026 02:06:59 GMT  
		Size: 384.5 MB (384468450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4693965853a32be01a599fd5f1f96491a31f8aa581a7ad164aa8ccae6f4c874`  
		Last Modified: Tue, 07 Apr 2026 02:06:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b77bc73f26f48771b1c053c9d95e561422b6dd55d999db9d5edb1a89ac3e3fd`  
		Last Modified: Tue, 07 Apr 2026 02:06:48 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f817274f69cec7232c26b038a98ecf703aa109682ef3f7c7f6ee56b2b3ccb4e`  
		Last Modified: Tue, 07 Apr 2026 02:06:48 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59959f1c9d707a2edd36384ad5f711a36f7d5be165ea4e4ca5b07937a0570084`  
		Last Modified: Tue, 07 Apr 2026 02:06:50 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:372f9c4eef0073200a21d27602d487ac09dae4a2307b553a1d88327094cbb3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62159366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711d069c8e165318bc08f42ad87640c05de277b7739879887a8e01733f6b5974`

```dockerfile
```

-	Layers:
	-	`sha256:f97155036b6dc2b04f9ca25c5c46a3c842915df1ab30b1ca1f0a6cf5a851d457`  
		Last Modified: Tue, 07 Apr 2026 02:06:50 GMT  
		Size: 62.1 MB (62132567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:212ca401bd97ff5011e13ae119ac05163012310a653e74591ab4043425d99f53`  
		Last Modified: Tue, 07 Apr 2026 02:06:46 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260324` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3110ee913bead95a4c23706f5915ccf4c8bab6da0dec151961e11b3e916ba66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.0 MB (680006136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fea6ecc224dd57c1735c141772456cfe8eb4a9959ddadceaddb74a03ce949f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:43:05 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:43:05 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:43:05 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:43:05 GMT
ARG TARGETARCH=arm64
# Tue, 07 Apr 2026 02:43:05 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:43:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:43:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:43:17 GMT
ENV ODOO_VERSION=18.0
# Tue, 07 Apr 2026 02:43:17 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:43:17 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 07 Apr 2026 02:44:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:44:23 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:44:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:44:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:44:23 GMT
USER odoo
# Tue, 07 Apr 2026 02:44:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:44:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84695fcff934393663b30f066216ec7f48081aefba9da49828d4d8db0f7b6d3`  
		Last Modified: Tue, 07 Apr 2026 02:46:47 GMT  
		Size: 252.0 MB (251996001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35472ccd661285bbf9e35acc9bd9b31d86da5e212926fff1e8b040c5cf38bfd`  
		Last Modified: Tue, 07 Apr 2026 02:46:39 GMT  
		Size: 14.3 MB (14340887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df846acc75ae1d7cbe75474082e770764fa4777b552b451d8fd2c8455fda66f`  
		Last Modified: Tue, 07 Apr 2026 02:46:37 GMT  
		Size: 479.7 KB (479671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373a2f386b1b99f8bfd222705dfa3d8adf76d31011511a00111e4171524f4428`  
		Last Modified: Tue, 07 Apr 2026 02:46:50 GMT  
		Size: 384.3 MB (384313063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1923eef19fa0e483bb8164f1f04ba152bb0d40a13bd12a477d94b32df97bc`  
		Last Modified: Tue, 07 Apr 2026 02:46:39 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3888b18a3ef8ad70ef55d1b735f79e3d9275b551057e43ffcaf8d45af068041`  
		Last Modified: Tue, 07 Apr 2026 02:46:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0e4bfad9129439d642fdaac60a313c9b245b952a55988fe67f280bf35a20cd`  
		Last Modified: Tue, 07 Apr 2026 02:46:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a12db641e02f4bb4132d486d9c51b1f53a11367bc8e5aea166030e2720b2d4c`  
		Last Modified: Tue, 07 Apr 2026 02:46:41 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:e4e1f2d330e0ecd057bdf8c121336bdf76d7e84d171c74045acabe92a175e739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62166793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3919dbcd571fdab9fc3b77277bfa3db69bf7757fa45a21fdb79980d4be0d9bc`

```dockerfile
```

-	Layers:
	-	`sha256:eb3672c333b4d8d61a2b39a858c42bee5471c4c30b4264325ec0fa343c72cca3`  
		Last Modified: Tue, 07 Apr 2026 02:46:41 GMT  
		Size: 62.1 MB (62139842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e699527c2e974be6e8acc26293673fb5cc219a391e9bcf2434d2884cbb6c96d7`  
		Last Modified: Tue, 07 Apr 2026 02:46:37 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260324` - linux; ppc64le

```console
$ docker pull odoo@sha256:a9163feaac6f9aa545f4d23404bb296ddda21c69e7db51326245be29024d2007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.8 MB (699797001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c596237736b65e38d215b0cd2c0d04deed0312d06dc50590c27538aae67493`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 05:16:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 05:16:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 05:16:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 05:16:49 GMT
ARG TARGETARCH=ppc64le
# Tue, 07 Apr 2026 05:16:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 05:17:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
ENV ODOO_VERSION=18.0
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 07 Apr 2026 05:19:33 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 05:19:34 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 05:19:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 05:19:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 05:19:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 05:19:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 05:19:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 05:19:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 05:19:35 GMT
USER odoo
# Tue, 07 Apr 2026 05:19:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 05:19:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74487ed95f50675350fffef58826e35fc796b98c0e021234a16f225ffda4c6a`  
		Last Modified: Tue, 07 Apr 2026 05:24:13 GMT  
		Size: 265.1 MB (265109939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94274f5bc4aef8440fa4da1c54ad73af3dca9728f356c0bd034e73c27c360cd`  
		Last Modified: Tue, 07 Apr 2026 05:24:03 GMT  
		Size: 14.9 MB (14893935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba0cc6d20592598467e8e83a903cf7cf6db59a24e397ca7116cbb9e31a40e3`  
		Last Modified: Tue, 07 Apr 2026 05:24:02 GMT  
		Size: 479.7 KB (479745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8b63a445df3f4df0dacbd0bb79dfeec7ce2e947ff2a0697039a93cfd54def1`  
		Last Modified: Tue, 07 Apr 2026 05:24:15 GMT  
		Size: 385.0 MB (384997612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc3ac51180595f4a3e1b99b1345f7e413b840842092bf96751975749ee1861b`  
		Last Modified: Tue, 07 Apr 2026 05:24:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faed336efd8d8ce0c079ab133291e95b5ac02b9997e12f8244264cfa18f0a77c`  
		Last Modified: Tue, 07 Apr 2026 05:24:04 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45d8339723d140616d252e349b9faa6640c5dca20f481ddbc6f6c6a438a846`  
		Last Modified: Tue, 07 Apr 2026 05:24:04 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e51fde825458322566fcbb94fcac9f090a29be89ebf41ac800966cdc6794ce`  
		Last Modified: Tue, 07 Apr 2026 05:24:06 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:c722145640b5c0d20c08db3dfb4c42a197c870f6cbf86e74b35053598dd5f09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62167805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30bf0510c5888891f2e2a11d4f1c66ef827f80176ebf77dfc4ef3c389e60b55e`

```dockerfile
```

-	Layers:
	-	`sha256:f0e6a279a187c024fe2b1a2e466c0be193efd4cb615f0752bcc12886cb9e61c9`  
		Last Modified: Tue, 07 Apr 2026 05:24:07 GMT  
		Size: 62.1 MB (62140950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cbb0c7f3085370190924e6e64934c8966448962d876f4333c427c396bb57aa9`  
		Last Modified: Tue, 07 Apr 2026 05:24:01 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:27d2bc34eab94f3a33fbb8e465798bf918f47cffae47a2bb232877cea280564f
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
$ docker pull odoo@sha256:f169a5b2d7f1de01c8a8a5f49f46906077b12ff455e82248c533cfeac745f07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.2 MB (702225779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d5411c05fd1c91a8bb3439dee468a462c4f7378738fcabeb67567c569b93fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:03:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:03:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:03:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:03:52 GMT
ARG TARGETARCH=amd64
# Tue, 07 Apr 2026 02:03:52 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:04:00 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
ENV ODOO_VERSION=19.0
# Tue, 07 Apr 2026 02:04:01 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:04:01 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 07 Apr 2026 02:04:57 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:04:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:04:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:04:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
USER odoo
# Tue, 07 Apr 2026 02:04:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:04:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46fb4a60fa7da69e69900a53a02aa9736f3afe7ab4083f2ed52ecd438c8af`  
		Last Modified: Tue, 07 Apr 2026 02:07:10 GMT  
		Size: 254.6 MB (254568604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf79a1170e431a1068de3b2a07f6cd874b705c0079c8d15d6218392036a3984`  
		Last Modified: Tue, 07 Apr 2026 02:07:02 GMT  
		Size: 14.4 MB (14360155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b1f3e7f7868ca2df175f4c1be1d451ba5d05479fb79df052b686c7be8aea12`  
		Last Modified: Tue, 07 Apr 2026 02:07:01 GMT  
		Size: 479.6 KB (479637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be401d21c6d4e9e7bf659cec723b9df0168fa69757504641b0380ce8c1c1edfc`  
		Last Modified: Tue, 07 Apr 2026 02:07:14 GMT  
		Size: 403.1 MB (403081482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21363cbc1d41c31000f38ab41525d2bcae0125f8cb3f613bf2ba52ba53f0e438`  
		Last Modified: Tue, 07 Apr 2026 02:07:02 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be863de1b9b5e9a0d3abfe4547df338f2c0f96de53da1ad746763398503fcc43`  
		Last Modified: Tue, 07 Apr 2026 02:07:04 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33259f123491017637387a31ffb1e42ccc525b8aeb106fab163777199ff9665`  
		Last Modified: Tue, 07 Apr 2026 02:07:04 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fef0480687385879ca2a05cd42098f80d8c4cfa4b2c99876812d7525f028ea5`  
		Last Modified: Tue, 07 Apr 2026 02:07:05 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:7f088cd013aaf2ad02a9885efa43fb83205f34164cc5d60787420e9e319091ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69981970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb25217f7105e4c291e0d45d78fd27d39de0052cc983673f89c75cb66a980fb`

```dockerfile
```

-	Layers:
	-	`sha256:3dcb9b65b3eac5ec4fbd80f66723299a5816e7f869c5c7c37bb11479b50064cd`  
		Last Modified: Tue, 07 Apr 2026 02:07:05 GMT  
		Size: 70.0 MB (69954878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b64d4192b9155a3fb70600f669df30f3b433e79d64719ddeaa695b20de14bd`  
		Last Modified: Tue, 07 Apr 2026 02:07:01 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7f1af7a3217c2d29e1878ada6018a4b24a238f5a59819c13acc6975615ed2e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.6 MB (698598877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538777fa63e6bd5a226970e46fe40bfacd6d138bf8fa92b442ef2e446bc654e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:06:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:06:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:06:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:06:48 GMT
ARG TARGETARCH=arm64
# Tue, 07 Apr 2026 02:06:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:06:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:07:00 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:07:00 GMT
ENV ODOO_VERSION=19.0
# Tue, 07 Apr 2026 02:07:00 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:07:00 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 07 Apr 2026 02:08:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:08:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:08:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:08:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
USER odoo
# Tue, 07 Apr 2026 02:08:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:08:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec15becc93e6336f80719d5758bc17111abb704c002c6de5a46c4eeda2361cae`  
		Last Modified: Tue, 07 Apr 2026 02:11:21 GMT  
		Size: 252.0 MB (251995802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac36de30c8b41dea9700b404381833a4fbd58762b8ade11c2a50191e3fbb55`  
		Last Modified: Tue, 07 Apr 2026 02:11:12 GMT  
		Size: 14.3 MB (14340809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac85eb49fae3caab5077de14370f0f0134a1a727bb75de99f7eac54c996c5b1`  
		Last Modified: Tue, 07 Apr 2026 02:11:10 GMT  
		Size: 479.6 KB (479650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9243bd71240017b4f7defcc7e9aa8bc02628df04bf27c6ebdb7f71cc31cca4`  
		Last Modified: Tue, 07 Apr 2026 02:11:23 GMT  
		Size: 402.9 MB (402906100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b443187f168dac252b55484ab1abc91d29a5803d14c175155ee3a40b4e20fe`  
		Last Modified: Tue, 07 Apr 2026 02:11:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f791705bd9cf2a0d4379bffdf902b6f9b1ebbeb43c8b0516a5579585bf68575`  
		Last Modified: Tue, 07 Apr 2026 02:11:13 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1d4c260dff1e8301be4d1d59486b8e6c95152e2507949bd71a596970fc0fd7`  
		Last Modified: Tue, 07 Apr 2026 02:11:13 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f0c3678a6a1552e281b2c68f6ac39d9000f6e42c8dca513e9966aae442f187`  
		Last Modified: Tue, 07 Apr 2026 02:11:15 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:025477f97be9c9c7d01decf43d5b4d3ccf7fa968e8c05ec9777af18428edea30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69989422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48b9471f30a54f776e5e9a8350bfff105879a3cd14f1323b62f4235fde7e299`

```dockerfile
```

-	Layers:
	-	`sha256:a7d829d07694a270b8e853f977661fe1e8fc692c4d336b46d968f0f8d7269114`  
		Last Modified: Tue, 07 Apr 2026 02:11:14 GMT  
		Size: 70.0 MB (69962165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af13ba25b91258437ca604af16d35302e49c7d9a1aa3784434219fa14d843c9d`  
		Last Modified: Tue, 07 Apr 2026 02:11:10 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:259ab2ccb9edddbf78dbf5ffef16c0ad1c657e58b9bc96bfe0388838177bc539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.4 MB (718426003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839b6744b98e7d504041ad780b27b51ffe40ed16750a1108143bb30e0616530b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 05:16:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 05:16:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 05:16:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 05:16:49 GMT
ARG TARGETARCH=ppc64le
# Tue, 07 Apr 2026 05:16:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 05:17:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
ENV ODOO_VERSION=19.0
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 07 Apr 2026 05:19:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 05:19:49 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 05:19:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 05:19:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 05:19:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
USER odoo
# Tue, 07 Apr 2026 05:19:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 05:19:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74487ed95f50675350fffef58826e35fc796b98c0e021234a16f225ffda4c6a`  
		Last Modified: Tue, 07 Apr 2026 05:24:13 GMT  
		Size: 265.1 MB (265109939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94274f5bc4aef8440fa4da1c54ad73af3dca9728f356c0bd034e73c27c360cd`  
		Last Modified: Tue, 07 Apr 2026 05:24:03 GMT  
		Size: 14.9 MB (14893935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba0cc6d20592598467e8e83a903cf7cf6db59a24e397ca7116cbb9e31a40e3`  
		Last Modified: Tue, 07 Apr 2026 05:24:02 GMT  
		Size: 479.7 KB (479745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef3127f47bfdafd8d4c61abf95b5e994408291ae20d1838460386685bcb73da`  
		Last Modified: Tue, 07 Apr 2026 05:25:47 GMT  
		Size: 403.6 MB (403626612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f63486aa373edb0a8a1153fad38b866e1f50d012df023d9865a89816646473`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6bf564a0e919d5cdbba0ed022cefcd2828ae667706c8520a31535139ade052`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50d4d0954fcaf95023601d717209272c79f5a33148c81f09d99f0870608d09b`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08531756f5b2bacaca67dc2de1e4f0f75d014c8a3c87d2f74cb1e1bb5e48922a`  
		Last Modified: Tue, 07 Apr 2026 05:25:39 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:25e6ad4ec979ff4fce96fbd8fb68714c43ef592864d10db292eaea18682ca9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69990422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3b6cfbdfff59683bc8dfb1e64a1a06f45118652fc0005cb36024d70325492e`

```dockerfile
```

-	Layers:
	-	`sha256:ce7d1c375d4e05404d72d0451f3101603059fcc361953cd3e0414fcf6f086152`  
		Last Modified: Tue, 07 Apr 2026 05:25:41 GMT  
		Size: 70.0 MB (69963267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6931d40bc95b7854ac13665aaf1c88b5e999ec9d20f914825c2f0cef7c92b9fe`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:27d2bc34eab94f3a33fbb8e465798bf918f47cffae47a2bb232877cea280564f
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
$ docker pull odoo@sha256:f169a5b2d7f1de01c8a8a5f49f46906077b12ff455e82248c533cfeac745f07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.2 MB (702225779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d5411c05fd1c91a8bb3439dee468a462c4f7378738fcabeb67567c569b93fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:03:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:03:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:03:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:03:52 GMT
ARG TARGETARCH=amd64
# Tue, 07 Apr 2026 02:03:52 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:04:00 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
ENV ODOO_VERSION=19.0
# Tue, 07 Apr 2026 02:04:01 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:04:01 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 07 Apr 2026 02:04:57 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:04:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:04:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:04:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
USER odoo
# Tue, 07 Apr 2026 02:04:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:04:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46fb4a60fa7da69e69900a53a02aa9736f3afe7ab4083f2ed52ecd438c8af`  
		Last Modified: Tue, 07 Apr 2026 02:07:10 GMT  
		Size: 254.6 MB (254568604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf79a1170e431a1068de3b2a07f6cd874b705c0079c8d15d6218392036a3984`  
		Last Modified: Tue, 07 Apr 2026 02:07:02 GMT  
		Size: 14.4 MB (14360155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b1f3e7f7868ca2df175f4c1be1d451ba5d05479fb79df052b686c7be8aea12`  
		Last Modified: Tue, 07 Apr 2026 02:07:01 GMT  
		Size: 479.6 KB (479637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be401d21c6d4e9e7bf659cec723b9df0168fa69757504641b0380ce8c1c1edfc`  
		Last Modified: Tue, 07 Apr 2026 02:07:14 GMT  
		Size: 403.1 MB (403081482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21363cbc1d41c31000f38ab41525d2bcae0125f8cb3f613bf2ba52ba53f0e438`  
		Last Modified: Tue, 07 Apr 2026 02:07:02 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be863de1b9b5e9a0d3abfe4547df338f2c0f96de53da1ad746763398503fcc43`  
		Last Modified: Tue, 07 Apr 2026 02:07:04 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33259f123491017637387a31ffb1e42ccc525b8aeb106fab163777199ff9665`  
		Last Modified: Tue, 07 Apr 2026 02:07:04 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fef0480687385879ca2a05cd42098f80d8c4cfa4b2c99876812d7525f028ea5`  
		Last Modified: Tue, 07 Apr 2026 02:07:05 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7f088cd013aaf2ad02a9885efa43fb83205f34164cc5d60787420e9e319091ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69981970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb25217f7105e4c291e0d45d78fd27d39de0052cc983673f89c75cb66a980fb`

```dockerfile
```

-	Layers:
	-	`sha256:3dcb9b65b3eac5ec4fbd80f66723299a5816e7f869c5c7c37bb11479b50064cd`  
		Last Modified: Tue, 07 Apr 2026 02:07:05 GMT  
		Size: 70.0 MB (69954878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b64d4192b9155a3fb70600f669df30f3b433e79d64719ddeaa695b20de14bd`  
		Last Modified: Tue, 07 Apr 2026 02:07:01 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7f1af7a3217c2d29e1878ada6018a4b24a238f5a59819c13acc6975615ed2e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.6 MB (698598877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538777fa63e6bd5a226970e46fe40bfacd6d138bf8fa92b442ef2e446bc654e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:06:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:06:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:06:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:06:48 GMT
ARG TARGETARCH=arm64
# Tue, 07 Apr 2026 02:06:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:06:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:07:00 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:07:00 GMT
ENV ODOO_VERSION=19.0
# Tue, 07 Apr 2026 02:07:00 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:07:00 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 07 Apr 2026 02:08:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:08:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:08:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:08:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
USER odoo
# Tue, 07 Apr 2026 02:08:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:08:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec15becc93e6336f80719d5758bc17111abb704c002c6de5a46c4eeda2361cae`  
		Last Modified: Tue, 07 Apr 2026 02:11:21 GMT  
		Size: 252.0 MB (251995802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac36de30c8b41dea9700b404381833a4fbd58762b8ade11c2a50191e3fbb55`  
		Last Modified: Tue, 07 Apr 2026 02:11:12 GMT  
		Size: 14.3 MB (14340809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac85eb49fae3caab5077de14370f0f0134a1a727bb75de99f7eac54c996c5b1`  
		Last Modified: Tue, 07 Apr 2026 02:11:10 GMT  
		Size: 479.6 KB (479650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9243bd71240017b4f7defcc7e9aa8bc02628df04bf27c6ebdb7f71cc31cca4`  
		Last Modified: Tue, 07 Apr 2026 02:11:23 GMT  
		Size: 402.9 MB (402906100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b443187f168dac252b55484ab1abc91d29a5803d14c175155ee3a40b4e20fe`  
		Last Modified: Tue, 07 Apr 2026 02:11:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f791705bd9cf2a0d4379bffdf902b6f9b1ebbeb43c8b0516a5579585bf68575`  
		Last Modified: Tue, 07 Apr 2026 02:11:13 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1d4c260dff1e8301be4d1d59486b8e6c95152e2507949bd71a596970fc0fd7`  
		Last Modified: Tue, 07 Apr 2026 02:11:13 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f0c3678a6a1552e281b2c68f6ac39d9000f6e42c8dca513e9966aae442f187`  
		Last Modified: Tue, 07 Apr 2026 02:11:15 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:025477f97be9c9c7d01decf43d5b4d3ccf7fa968e8c05ec9777af18428edea30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69989422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48b9471f30a54f776e5e9a8350bfff105879a3cd14f1323b62f4235fde7e299`

```dockerfile
```

-	Layers:
	-	`sha256:a7d829d07694a270b8e853f977661fe1e8fc692c4d336b46d968f0f8d7269114`  
		Last Modified: Tue, 07 Apr 2026 02:11:14 GMT  
		Size: 70.0 MB (69962165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af13ba25b91258437ca604af16d35302e49c7d9a1aa3784434219fa14d843c9d`  
		Last Modified: Tue, 07 Apr 2026 02:11:10 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:259ab2ccb9edddbf78dbf5ffef16c0ad1c657e58b9bc96bfe0388838177bc539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.4 MB (718426003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839b6744b98e7d504041ad780b27b51ffe40ed16750a1108143bb30e0616530b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 05:16:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 05:16:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 05:16:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 05:16:49 GMT
ARG TARGETARCH=ppc64le
# Tue, 07 Apr 2026 05:16:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 05:17:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
ENV ODOO_VERSION=19.0
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 07 Apr 2026 05:19:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 05:19:49 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 05:19:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 05:19:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 05:19:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
USER odoo
# Tue, 07 Apr 2026 05:19:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 05:19:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74487ed95f50675350fffef58826e35fc796b98c0e021234a16f225ffda4c6a`  
		Last Modified: Tue, 07 Apr 2026 05:24:13 GMT  
		Size: 265.1 MB (265109939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94274f5bc4aef8440fa4da1c54ad73af3dca9728f356c0bd034e73c27c360cd`  
		Last Modified: Tue, 07 Apr 2026 05:24:03 GMT  
		Size: 14.9 MB (14893935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba0cc6d20592598467e8e83a903cf7cf6db59a24e397ca7116cbb9e31a40e3`  
		Last Modified: Tue, 07 Apr 2026 05:24:02 GMT  
		Size: 479.7 KB (479745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef3127f47bfdafd8d4c61abf95b5e994408291ae20d1838460386685bcb73da`  
		Last Modified: Tue, 07 Apr 2026 05:25:47 GMT  
		Size: 403.6 MB (403626612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f63486aa373edb0a8a1153fad38b866e1f50d012df023d9865a89816646473`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6bf564a0e919d5cdbba0ed022cefcd2828ae667706c8520a31535139ade052`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50d4d0954fcaf95023601d717209272c79f5a33148c81f09d99f0870608d09b`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08531756f5b2bacaca67dc2de1e4f0f75d014c8a3c87d2f74cb1e1bb5e48922a`  
		Last Modified: Tue, 07 Apr 2026 05:25:39 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:25e6ad4ec979ff4fce96fbd8fb68714c43ef592864d10db292eaea18682ca9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69990422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3b6cfbdfff59683bc8dfb1e64a1a06f45118652fc0005cb36024d70325492e`

```dockerfile
```

-	Layers:
	-	`sha256:ce7d1c375d4e05404d72d0451f3101603059fcc361953cd3e0414fcf6f086152`  
		Last Modified: Tue, 07 Apr 2026 05:25:41 GMT  
		Size: 70.0 MB (69963267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6931d40bc95b7854ac13665aaf1c88b5e999ec9d20f914825c2f0cef7c92b9fe`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260324`

```console
$ docker pull odoo@sha256:27d2bc34eab94f3a33fbb8e465798bf918f47cffae47a2bb232877cea280564f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20260324` - linux; amd64

```console
$ docker pull odoo@sha256:f169a5b2d7f1de01c8a8a5f49f46906077b12ff455e82248c533cfeac745f07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.2 MB (702225779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d5411c05fd1c91a8bb3439dee468a462c4f7378738fcabeb67567c569b93fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:03:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:03:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:03:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:03:52 GMT
ARG TARGETARCH=amd64
# Tue, 07 Apr 2026 02:03:52 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:04:00 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
ENV ODOO_VERSION=19.0
# Tue, 07 Apr 2026 02:04:01 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:04:01 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 07 Apr 2026 02:04:57 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:04:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:04:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:04:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
USER odoo
# Tue, 07 Apr 2026 02:04:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:04:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46fb4a60fa7da69e69900a53a02aa9736f3afe7ab4083f2ed52ecd438c8af`  
		Last Modified: Tue, 07 Apr 2026 02:07:10 GMT  
		Size: 254.6 MB (254568604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf79a1170e431a1068de3b2a07f6cd874b705c0079c8d15d6218392036a3984`  
		Last Modified: Tue, 07 Apr 2026 02:07:02 GMT  
		Size: 14.4 MB (14360155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b1f3e7f7868ca2df175f4c1be1d451ba5d05479fb79df052b686c7be8aea12`  
		Last Modified: Tue, 07 Apr 2026 02:07:01 GMT  
		Size: 479.6 KB (479637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be401d21c6d4e9e7bf659cec723b9df0168fa69757504641b0380ce8c1c1edfc`  
		Last Modified: Tue, 07 Apr 2026 02:07:14 GMT  
		Size: 403.1 MB (403081482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21363cbc1d41c31000f38ab41525d2bcae0125f8cb3f613bf2ba52ba53f0e438`  
		Last Modified: Tue, 07 Apr 2026 02:07:02 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be863de1b9b5e9a0d3abfe4547df338f2c0f96de53da1ad746763398503fcc43`  
		Last Modified: Tue, 07 Apr 2026 02:07:04 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33259f123491017637387a31ffb1e42ccc525b8aeb106fab163777199ff9665`  
		Last Modified: Tue, 07 Apr 2026 02:07:04 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fef0480687385879ca2a05cd42098f80d8c4cfa4b2c99876812d7525f028ea5`  
		Last Modified: Tue, 07 Apr 2026 02:07:05 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:7f088cd013aaf2ad02a9885efa43fb83205f34164cc5d60787420e9e319091ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69981970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb25217f7105e4c291e0d45d78fd27d39de0052cc983673f89c75cb66a980fb`

```dockerfile
```

-	Layers:
	-	`sha256:3dcb9b65b3eac5ec4fbd80f66723299a5816e7f869c5c7c37bb11479b50064cd`  
		Last Modified: Tue, 07 Apr 2026 02:07:05 GMT  
		Size: 70.0 MB (69954878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b64d4192b9155a3fb70600f669df30f3b433e79d64719ddeaa695b20de14bd`  
		Last Modified: Tue, 07 Apr 2026 02:07:01 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260324` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7f1af7a3217c2d29e1878ada6018a4b24a238f5a59819c13acc6975615ed2e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.6 MB (698598877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538777fa63e6bd5a226970e46fe40bfacd6d138bf8fa92b442ef2e446bc654e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:06:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:06:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:06:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:06:48 GMT
ARG TARGETARCH=arm64
# Tue, 07 Apr 2026 02:06:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:06:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:07:00 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:07:00 GMT
ENV ODOO_VERSION=19.0
# Tue, 07 Apr 2026 02:07:00 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:07:00 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 07 Apr 2026 02:08:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:08:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:08:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:08:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
USER odoo
# Tue, 07 Apr 2026 02:08:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:08:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec15becc93e6336f80719d5758bc17111abb704c002c6de5a46c4eeda2361cae`  
		Last Modified: Tue, 07 Apr 2026 02:11:21 GMT  
		Size: 252.0 MB (251995802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac36de30c8b41dea9700b404381833a4fbd58762b8ade11c2a50191e3fbb55`  
		Last Modified: Tue, 07 Apr 2026 02:11:12 GMT  
		Size: 14.3 MB (14340809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac85eb49fae3caab5077de14370f0f0134a1a727bb75de99f7eac54c996c5b1`  
		Last Modified: Tue, 07 Apr 2026 02:11:10 GMT  
		Size: 479.6 KB (479650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9243bd71240017b4f7defcc7e9aa8bc02628df04bf27c6ebdb7f71cc31cca4`  
		Last Modified: Tue, 07 Apr 2026 02:11:23 GMT  
		Size: 402.9 MB (402906100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b443187f168dac252b55484ab1abc91d29a5803d14c175155ee3a40b4e20fe`  
		Last Modified: Tue, 07 Apr 2026 02:11:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f791705bd9cf2a0d4379bffdf902b6f9b1ebbeb43c8b0516a5579585bf68575`  
		Last Modified: Tue, 07 Apr 2026 02:11:13 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1d4c260dff1e8301be4d1d59486b8e6c95152e2507949bd71a596970fc0fd7`  
		Last Modified: Tue, 07 Apr 2026 02:11:13 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f0c3678a6a1552e281b2c68f6ac39d9000f6e42c8dca513e9966aae442f187`  
		Last Modified: Tue, 07 Apr 2026 02:11:15 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:025477f97be9c9c7d01decf43d5b4d3ccf7fa968e8c05ec9777af18428edea30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69989422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48b9471f30a54f776e5e9a8350bfff105879a3cd14f1323b62f4235fde7e299`

```dockerfile
```

-	Layers:
	-	`sha256:a7d829d07694a270b8e853f977661fe1e8fc692c4d336b46d968f0f8d7269114`  
		Last Modified: Tue, 07 Apr 2026 02:11:14 GMT  
		Size: 70.0 MB (69962165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af13ba25b91258437ca604af16d35302e49c7d9a1aa3784434219fa14d843c9d`  
		Last Modified: Tue, 07 Apr 2026 02:11:10 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260324` - linux; ppc64le

```console
$ docker pull odoo@sha256:259ab2ccb9edddbf78dbf5ffef16c0ad1c657e58b9bc96bfe0388838177bc539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.4 MB (718426003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839b6744b98e7d504041ad780b27b51ffe40ed16750a1108143bb30e0616530b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 05:16:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 05:16:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 05:16:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 05:16:49 GMT
ARG TARGETARCH=ppc64le
# Tue, 07 Apr 2026 05:16:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 05:17:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
ENV ODOO_VERSION=19.0
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 07 Apr 2026 05:19:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 05:19:49 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 05:19:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 05:19:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 05:19:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
USER odoo
# Tue, 07 Apr 2026 05:19:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 05:19:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74487ed95f50675350fffef58826e35fc796b98c0e021234a16f225ffda4c6a`  
		Last Modified: Tue, 07 Apr 2026 05:24:13 GMT  
		Size: 265.1 MB (265109939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94274f5bc4aef8440fa4da1c54ad73af3dca9728f356c0bd034e73c27c360cd`  
		Last Modified: Tue, 07 Apr 2026 05:24:03 GMT  
		Size: 14.9 MB (14893935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba0cc6d20592598467e8e83a903cf7cf6db59a24e397ca7116cbb9e31a40e3`  
		Last Modified: Tue, 07 Apr 2026 05:24:02 GMT  
		Size: 479.7 KB (479745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef3127f47bfdafd8d4c61abf95b5e994408291ae20d1838460386685bcb73da`  
		Last Modified: Tue, 07 Apr 2026 05:25:47 GMT  
		Size: 403.6 MB (403626612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f63486aa373edb0a8a1153fad38b866e1f50d012df023d9865a89816646473`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6bf564a0e919d5cdbba0ed022cefcd2828ae667706c8520a31535139ade052`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50d4d0954fcaf95023601d717209272c79f5a33148c81f09d99f0870608d09b`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08531756f5b2bacaca67dc2de1e4f0f75d014c8a3c87d2f74cb1e1bb5e48922a`  
		Last Modified: Tue, 07 Apr 2026 05:25:39 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:25e6ad4ec979ff4fce96fbd8fb68714c43ef592864d10db292eaea18682ca9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69990422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3b6cfbdfff59683bc8dfb1e64a1a06f45118652fc0005cb36024d70325492e`

```dockerfile
```

-	Layers:
	-	`sha256:ce7d1c375d4e05404d72d0451f3101603059fcc361953cd3e0414fcf6f086152`  
		Last Modified: Tue, 07 Apr 2026 05:25:41 GMT  
		Size: 70.0 MB (69963267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6931d40bc95b7854ac13665aaf1c88b5e999ec9d20f914825c2f0cef7c92b9fe`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:27d2bc34eab94f3a33fbb8e465798bf918f47cffae47a2bb232877cea280564f
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
$ docker pull odoo@sha256:f169a5b2d7f1de01c8a8a5f49f46906077b12ff455e82248c533cfeac745f07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.2 MB (702225779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d5411c05fd1c91a8bb3439dee468a462c4f7378738fcabeb67567c569b93fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:03:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:03:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:03:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:03:52 GMT
ARG TARGETARCH=amd64
# Tue, 07 Apr 2026 02:03:52 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:04:00 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:04:01 GMT
ENV ODOO_VERSION=19.0
# Tue, 07 Apr 2026 02:04:01 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:04:01 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 07 Apr 2026 02:04:57 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:04:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:04:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:04:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:04:58 GMT
USER odoo
# Tue, 07 Apr 2026 02:04:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:04:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a46fb4a60fa7da69e69900a53a02aa9736f3afe7ab4083f2ed52ecd438c8af`  
		Last Modified: Tue, 07 Apr 2026 02:07:10 GMT  
		Size: 254.6 MB (254568604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf79a1170e431a1068de3b2a07f6cd874b705c0079c8d15d6218392036a3984`  
		Last Modified: Tue, 07 Apr 2026 02:07:02 GMT  
		Size: 14.4 MB (14360155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b1f3e7f7868ca2df175f4c1be1d451ba5d05479fb79df052b686c7be8aea12`  
		Last Modified: Tue, 07 Apr 2026 02:07:01 GMT  
		Size: 479.6 KB (479637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be401d21c6d4e9e7bf659cec723b9df0168fa69757504641b0380ce8c1c1edfc`  
		Last Modified: Tue, 07 Apr 2026 02:07:14 GMT  
		Size: 403.1 MB (403081482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21363cbc1d41c31000f38ab41525d2bcae0125f8cb3f613bf2ba52ba53f0e438`  
		Last Modified: Tue, 07 Apr 2026 02:07:02 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be863de1b9b5e9a0d3abfe4547df338f2c0f96de53da1ad746763398503fcc43`  
		Last Modified: Tue, 07 Apr 2026 02:07:04 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33259f123491017637387a31ffb1e42ccc525b8aeb106fab163777199ff9665`  
		Last Modified: Tue, 07 Apr 2026 02:07:04 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fef0480687385879ca2a05cd42098f80d8c4cfa4b2c99876812d7525f028ea5`  
		Last Modified: Tue, 07 Apr 2026 02:07:05 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7f088cd013aaf2ad02a9885efa43fb83205f34164cc5d60787420e9e319091ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69981970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb25217f7105e4c291e0d45d78fd27d39de0052cc983673f89c75cb66a980fb`

```dockerfile
```

-	Layers:
	-	`sha256:3dcb9b65b3eac5ec4fbd80f66723299a5816e7f869c5c7c37bb11479b50064cd`  
		Last Modified: Tue, 07 Apr 2026 02:07:05 GMT  
		Size: 70.0 MB (69954878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b64d4192b9155a3fb70600f669df30f3b433e79d64719ddeaa695b20de14bd`  
		Last Modified: Tue, 07 Apr 2026 02:07:01 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7f1af7a3217c2d29e1878ada6018a4b24a238f5a59819c13acc6975615ed2e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.6 MB (698598877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538777fa63e6bd5a226970e46fe40bfacd6d138bf8fa92b442ef2e446bc654e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:06:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 02:06:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 02:06:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 02:06:48 GMT
ARG TARGETARCH=arm64
# Tue, 07 Apr 2026 02:06:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 02:06:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:07:00 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 02:07:00 GMT
ENV ODOO_VERSION=19.0
# Tue, 07 Apr 2026 02:07:00 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 02:07:00 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 07 Apr 2026 02:08:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 02:08:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 02:08:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 02:08:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
USER odoo
# Tue, 07 Apr 2026 02:08:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:08:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec15becc93e6336f80719d5758bc17111abb704c002c6de5a46c4eeda2361cae`  
		Last Modified: Tue, 07 Apr 2026 02:11:21 GMT  
		Size: 252.0 MB (251995802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac36de30c8b41dea9700b404381833a4fbd58762b8ade11c2a50191e3fbb55`  
		Last Modified: Tue, 07 Apr 2026 02:11:12 GMT  
		Size: 14.3 MB (14340809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac85eb49fae3caab5077de14370f0f0134a1a727bb75de99f7eac54c996c5b1`  
		Last Modified: Tue, 07 Apr 2026 02:11:10 GMT  
		Size: 479.6 KB (479650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9243bd71240017b4f7defcc7e9aa8bc02628df04bf27c6ebdb7f71cc31cca4`  
		Last Modified: Tue, 07 Apr 2026 02:11:23 GMT  
		Size: 402.9 MB (402906100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b443187f168dac252b55484ab1abc91d29a5803d14c175155ee3a40b4e20fe`  
		Last Modified: Tue, 07 Apr 2026 02:11:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f791705bd9cf2a0d4379bffdf902b6f9b1ebbeb43c8b0516a5579585bf68575`  
		Last Modified: Tue, 07 Apr 2026 02:11:13 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1d4c260dff1e8301be4d1d59486b8e6c95152e2507949bd71a596970fc0fd7`  
		Last Modified: Tue, 07 Apr 2026 02:11:13 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f0c3678a6a1552e281b2c68f6ac39d9000f6e42c8dca513e9966aae442f187`  
		Last Modified: Tue, 07 Apr 2026 02:11:15 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:025477f97be9c9c7d01decf43d5b4d3ccf7fa968e8c05ec9777af18428edea30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69989422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48b9471f30a54f776e5e9a8350bfff105879a3cd14f1323b62f4235fde7e299`

```dockerfile
```

-	Layers:
	-	`sha256:a7d829d07694a270b8e853f977661fe1e8fc692c4d336b46d968f0f8d7269114`  
		Last Modified: Tue, 07 Apr 2026 02:11:14 GMT  
		Size: 70.0 MB (69962165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af13ba25b91258437ca604af16d35302e49c7d9a1aa3784434219fa14d843c9d`  
		Last Modified: Tue, 07 Apr 2026 02:11:10 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:259ab2ccb9edddbf78dbf5ffef16c0ad1c657e58b9bc96bfe0388838177bc539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.4 MB (718426003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839b6744b98e7d504041ad780b27b51ffe40ed16750a1108143bb30e0616530b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 05:16:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Apr 2026 05:16:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Apr 2026 05:16:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 07 Apr 2026 05:16:49 GMT
ARG TARGETARCH=ppc64le
# Tue, 07 Apr 2026 05:16:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 07 Apr 2026 05:17:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 07 Apr 2026 05:17:05 GMT
ENV ODOO_VERSION=19.0
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_RELEASE=20260324
# Tue, 07 Apr 2026 05:17:05 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 07 Apr 2026 05:19:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 07 Apr 2026 05:19:49 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 07 Apr 2026 05:19:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 07 Apr 2026 05:19:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 07 Apr 2026 05:19:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 07 Apr 2026 05:19:50 GMT
USER odoo
# Tue, 07 Apr 2026 05:19:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 05:19:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74487ed95f50675350fffef58826e35fc796b98c0e021234a16f225ffda4c6a`  
		Last Modified: Tue, 07 Apr 2026 05:24:13 GMT  
		Size: 265.1 MB (265109939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94274f5bc4aef8440fa4da1c54ad73af3dca9728f356c0bd034e73c27c360cd`  
		Last Modified: Tue, 07 Apr 2026 05:24:03 GMT  
		Size: 14.9 MB (14893935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba0cc6d20592598467e8e83a903cf7cf6db59a24e397ca7116cbb9e31a40e3`  
		Last Modified: Tue, 07 Apr 2026 05:24:02 GMT  
		Size: 479.7 KB (479745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef3127f47bfdafd8d4c61abf95b5e994408291ae20d1838460386685bcb73da`  
		Last Modified: Tue, 07 Apr 2026 05:25:47 GMT  
		Size: 403.6 MB (403626612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f63486aa373edb0a8a1153fad38b866e1f50d012df023d9865a89816646473`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6bf564a0e919d5cdbba0ed022cefcd2828ae667706c8520a31535139ade052`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50d4d0954fcaf95023601d717209272c79f5a33148c81f09d99f0870608d09b`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08531756f5b2bacaca67dc2de1e4f0f75d014c8a3c87d2f74cb1e1bb5e48922a`  
		Last Modified: Tue, 07 Apr 2026 05:25:39 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:25e6ad4ec979ff4fce96fbd8fb68714c43ef592864d10db292eaea18682ca9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69990422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3b6cfbdfff59683bc8dfb1e64a1a06f45118652fc0005cb36024d70325492e`

```dockerfile
```

-	Layers:
	-	`sha256:ce7d1c375d4e05404d72d0451f3101603059fcc361953cd3e0414fcf6f086152`  
		Last Modified: Tue, 07 Apr 2026 05:25:41 GMT  
		Size: 70.0 MB (69963267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6931d40bc95b7854ac13665aaf1c88b5e999ec9d20f914825c2f0cef7c92b9fe`  
		Last Modified: Tue, 07 Apr 2026 05:25:37 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json
