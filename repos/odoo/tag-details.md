<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20251121`](#odoo170-20251121)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20251121`](#odoo180-20251121)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20251121`](#odoo190-20251121)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:1e34182546c20b9179a48d88d55628d4c39295f5a43532fa507e126051af5446
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:3d891c81867322e5141c2b76d0c3d0076b40bdbce6ad0e0de64772718ece401c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605578741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cee2a953e916feb29d310842db36e02c4a5597ce91011e5e1d3b3c4acd0b87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:33:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:33:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:33:04 GMT
ARG TARGETARCH=amd64
# Thu, 13 Nov 2025 23:33:04 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:33:11 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:33:12 GMT
ENV ODOO_VERSION=17.0
# Thu, 13 Nov 2025 23:33:12 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:33:12 GMT
ARG ODOO_SHA=605d3adeaa4ae339dd4741d0da148d219aee8419
# Thu, 13 Nov 2025 23:34:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=605d3adeaa4ae339dd4741d0da148d219aee8419
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:12 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=605d3adeaa4ae339dd4741d0da148d219aee8419
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:12 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdeb24695cd03dd18ad7aaf50095c5c5b14475fba595eb5dcd8a0227e4109605`  
		Last Modified: Fri, 14 Nov 2025 02:13:34 GMT  
		Size: 233.8 MB (233819980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce55fe7f59000514330d17ec1e7b7959adf73f54114eeaac049fc5feec986bc`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 2.6 MB (2597228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e57dd0f991f06732561b4247493d66c9e33c7184e5f992b53170151ab817d9`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 480.3 KB (480299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd772a79bff09ffa3f0d38b1caaf45530ed4da6dacbd555fb1ce7d3441bbd3b`  
		Last Modified: Fri, 14 Nov 2025 02:12:47 GMT  
		Size: 339.1 MB (339141998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8225fb20d7b2e7e3e369bc5b1bed7be84a976f9e084967f502f0ee375c40d7`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1456e5be9283a3dff1e8e7f46fa46677f5090afdb78c89165f27d2d6645f9cc5`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811eb4273026e16669b2ef9c2ee11b1f8b3c3ea9f5214c2f738d52da34afcd1f`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c333002799d73bac09956ee2d484d78f7418d185d5878d93e3204f006e6e2b43`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:cd2fdcd99a17305a2d598d3e03a3212650efd0b185a765574b7fb7a0286d1c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41848332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5cc902daa99d833660299b59cf6357fd90da4c4512999490cf8163978372a0`

```dockerfile
```

-	Layers:
	-	`sha256:7915d55ec1a935fcfaec6c7d9322c954976970a205c72d96042783d10c89576b`  
		Last Modified: Fri, 14 Nov 2025 02:12:41 GMT  
		Size: 41.8 MB (41821540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f97a1aff71faab740fbd9e82839c5b438567c2121e44f220b935b7d75730d6d5`  
		Last Modified: Fri, 14 Nov 2025 02:12:43 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e0ad51712f932d4279e397652035fea9d5fdd8700e3e4204e19cbeb3f180237b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.4 MB (600399846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551ba80fbedde46f92ce628dd14092a0a631d957e4a0e197e7fa80b68cffe1ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:32:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:32:49 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:32:49 GMT
ARG TARGETARCH=arm64
# Thu, 13 Nov 2025 23:32:49 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:32:56 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
ENV ODOO_VERSION=17.0
# Thu, 13 Nov 2025 23:32:57 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:32:57 GMT
ARG ODOO_SHA=605d3adeaa4ae339dd4741d0da148d219aee8419
# Thu, 13 Nov 2025 23:34:00 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=605d3adeaa4ae339dd4741d0da148d219aee8419
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:00 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:00 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:00 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=605d3adeaa4ae339dd4741d0da148d219aee8419
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:00 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:00 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:00 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:00 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91548d792b045a3f7a7a018ca2414ac09522d36d8c4deeb047d53abd6ebb615c`  
		Last Modified: Fri, 14 Nov 2025 02:13:51 GMT  
		Size: 231.2 MB (231197746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9ddb0e37e72c05accf0713b594991e7fb6712f8ee9a3907da240bbff85a4f9`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 2.6 MB (2592517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1beb9a594518e4ec1bbf465011e9b9b16048db592279f622a68e2878ef1f987`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 480.3 KB (480259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddaa8f567d488afc5ae1e119e161c384c9d5156027fcca42f7489717e8a8822`  
		Last Modified: Fri, 14 Nov 2025 02:13:43 GMT  
		Size: 338.7 MB (338743013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fee3555bcb57939e376c16317f6cf05e462bef127dd0cae64f5f82e8c16271`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c0ffbeb2533836634e767a43d103e569f2c6d070e59968f0f30c92434f8246`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d02d372d72b02198e2a27688222b007c6456ced45cbf9a79c6b00cc717a6f4`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c43284a82819725ed60e8d359de403a527696b0a1940d33ed98ed7217530f4`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:878126123ec99d939f4d4acb79934fa39c59dc503aadde69318749b856350c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41854991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8798f380416d9bafdff3cd233bd73fa7ee1354a4acfe917a36673ef39e7b29`

```dockerfile
```

-	Layers:
	-	`sha256:807fcea63337d40ddd1d2dd0d3e3dbc425f791ae5c5e86b6676dad99518cf840`  
		Last Modified: Fri, 14 Nov 2025 02:13:39 GMT  
		Size: 41.8 MB (41828047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba7bdf978df34ab4384e7d2d3d287126e9b52bb7da201fdb77e9d02736889b7`  
		Last Modified: Fri, 14 Nov 2025 02:13:40 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:1e34182546c20b9179a48d88d55628d4c39295f5a43532fa507e126051af5446
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:3d891c81867322e5141c2b76d0c3d0076b40bdbce6ad0e0de64772718ece401c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605578741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00cee2a953e916feb29d310842db36e02c4a5597ce91011e5e1d3b3c4acd0b87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:33:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:33:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:33:04 GMT
ARG TARGETARCH=amd64
# Thu, 13 Nov 2025 23:33:04 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:33:11 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:33:12 GMT
ENV ODOO_VERSION=17.0
# Thu, 13 Nov 2025 23:33:12 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:33:12 GMT
ARG ODOO_SHA=605d3adeaa4ae339dd4741d0da148d219aee8419
# Thu, 13 Nov 2025 23:34:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=605d3adeaa4ae339dd4741d0da148d219aee8419
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:12 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=605d3adeaa4ae339dd4741d0da148d219aee8419
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:12 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdeb24695cd03dd18ad7aaf50095c5c5b14475fba595eb5dcd8a0227e4109605`  
		Last Modified: Fri, 14 Nov 2025 02:13:34 GMT  
		Size: 233.8 MB (233819980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce55fe7f59000514330d17ec1e7b7959adf73f54114eeaac049fc5feec986bc`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 2.6 MB (2597228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e57dd0f991f06732561b4247493d66c9e33c7184e5f992b53170151ab817d9`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 480.3 KB (480299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd772a79bff09ffa3f0d38b1caaf45530ed4da6dacbd555fb1ce7d3441bbd3b`  
		Last Modified: Fri, 14 Nov 2025 02:12:47 GMT  
		Size: 339.1 MB (339141998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8225fb20d7b2e7e3e369bc5b1bed7be84a976f9e084967f502f0ee375c40d7`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1456e5be9283a3dff1e8e7f46fa46677f5090afdb78c89165f27d2d6645f9cc5`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811eb4273026e16669b2ef9c2ee11b1f8b3c3ea9f5214c2f738d52da34afcd1f`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c333002799d73bac09956ee2d484d78f7418d185d5878d93e3204f006e6e2b43`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cd2fdcd99a17305a2d598d3e03a3212650efd0b185a765574b7fb7a0286d1c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41848332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5cc902daa99d833660299b59cf6357fd90da4c4512999490cf8163978372a0`

```dockerfile
```

-	Layers:
	-	`sha256:7915d55ec1a935fcfaec6c7d9322c954976970a205c72d96042783d10c89576b`  
		Last Modified: Fri, 14 Nov 2025 02:12:41 GMT  
		Size: 41.8 MB (41821540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f97a1aff71faab740fbd9e82839c5b438567c2121e44f220b935b7d75730d6d5`  
		Last Modified: Fri, 14 Nov 2025 02:12:43 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e0ad51712f932d4279e397652035fea9d5fdd8700e3e4204e19cbeb3f180237b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.4 MB (600399846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551ba80fbedde46f92ce628dd14092a0a631d957e4a0e197e7fa80b68cffe1ca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:32:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:32:49 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:32:49 GMT
ARG TARGETARCH=arm64
# Thu, 13 Nov 2025 23:32:49 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:32:56 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:32:57 GMT
ENV ODOO_VERSION=17.0
# Thu, 13 Nov 2025 23:32:57 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:32:57 GMT
ARG ODOO_SHA=605d3adeaa4ae339dd4741d0da148d219aee8419
# Thu, 13 Nov 2025 23:34:00 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=605d3adeaa4ae339dd4741d0da148d219aee8419
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:00 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:00 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:00 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=605d3adeaa4ae339dd4741d0da148d219aee8419
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:00 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:00 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:00 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:00 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91548d792b045a3f7a7a018ca2414ac09522d36d8c4deeb047d53abd6ebb615c`  
		Last Modified: Fri, 14 Nov 2025 02:13:51 GMT  
		Size: 231.2 MB (231197746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9ddb0e37e72c05accf0713b594991e7fb6712f8ee9a3907da240bbff85a4f9`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 2.6 MB (2592517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1beb9a594518e4ec1bbf465011e9b9b16048db592279f622a68e2878ef1f987`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 480.3 KB (480259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddaa8f567d488afc5ae1e119e161c384c9d5156027fcca42f7489717e8a8822`  
		Last Modified: Fri, 14 Nov 2025 02:13:43 GMT  
		Size: 338.7 MB (338743013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fee3555bcb57939e376c16317f6cf05e462bef127dd0cae64f5f82e8c16271`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c0ffbeb2533836634e767a43d103e569f2c6d070e59968f0f30c92434f8246`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d02d372d72b02198e2a27688222b007c6456ced45cbf9a79c6b00cc717a6f4`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c43284a82819725ed60e8d359de403a527696b0a1940d33ed98ed7217530f4`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:878126123ec99d939f4d4acb79934fa39c59dc503aadde69318749b856350c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41854991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8798f380416d9bafdff3cd233bd73fa7ee1354a4acfe917a36673ef39e7b29`

```dockerfile
```

-	Layers:
	-	`sha256:807fcea63337d40ddd1d2dd0d3e3dbc425f791ae5c5e86b6676dad99518cf840`  
		Last Modified: Fri, 14 Nov 2025 02:13:39 GMT  
		Size: 41.8 MB (41828047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba7bdf978df34ab4384e7d2d3d287126e9b52bb7da201fdb77e9d02736889b7`  
		Last Modified: Fri, 14 Nov 2025 02:13:40 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20251121`

**does not exist** (yet?)

## `odoo:18`

```console
$ docker pull odoo@sha256:2b0546c8a98b1cd8add8bb8c3556fb03cf4205bdd0c0c57cf14aff3b207576d7
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
$ docker pull odoo@sha256:28e7fffde9a52b09a96cd25e64ab56f61cc1a538096409ef76deb958d65fba32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.0 MB (677965843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b7ab3e52402b8a60783de857347dc39d30f8d431da6f74b31cf695198096a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:33:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:33:31 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:33:31 GMT
ARG TARGETARCH=amd64
# Thu, 13 Nov 2025 23:33:31 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:33:39 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:40 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:33:40 GMT
ENV ODOO_VERSION=18.0
# Thu, 13 Nov 2025 23:33:40 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:33:40 GMT
ARG ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
# Thu, 13 Nov 2025 23:34:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de470010db47f89eb953924c14648c0d25f77c4bfbd24e42f51208c722da3346`  
		Last Modified: Fri, 14 Nov 2025 02:13:18 GMT  
		Size: 254.6 MB (254557394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09eca9b09a41e0af63400ff190eff63a0ed641ff4fc98a457237e9642040d50`  
		Last Modified: Thu, 13 Nov 2025 23:36:44 GMT  
		Size: 14.4 MB (14356518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b47d38821ec7fdf66d12ef8b2fc7e013272da58af3957532e3687c5d206d779`  
		Last Modified: Thu, 13 Nov 2025 23:36:42 GMT  
		Size: 480.1 KB (480127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ccfb8fa441c622f45c57cdc73fb8a846bae91401b732b39aac87966d41d8db`  
		Last Modified: Fri, 14 Nov 2025 02:13:45 GMT  
		Size: 378.8 MB (378844674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8225fb20d7b2e7e3e369bc5b1bed7be84a976f9e084967f502f0ee375c40d7`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf744e718209ef458f75cf4bb7e3aa1c9909c5a31798c51746a65907c7f5121`  
		Last Modified: Thu, 13 Nov 2025 23:36:42 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57c75706e38c8d262fe0916604c02c36d6a62a9897c66b48d2191b112b1a318`  
		Last Modified: Thu, 13 Nov 2025 23:36:43 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde45db02ec909399f6e302ecdc35c8f97f532fe85359628969fdf38e591ae45`  
		Last Modified: Thu, 13 Nov 2025 23:36:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:de43788bfa66d2d3ee16680c1940fb52c640e5c7fd174f0198a4b4bac2c185d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61332063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e463acf31430f0078d1c38b6279efd4ba5bf133ceedda53ada860772b7549f4`

```dockerfile
```

-	Layers:
	-	`sha256:496180d9ca5102a019d9f1204e571ac8e4a7788d7ef5467bfde324bae9f6f292`  
		Last Modified: Fri, 14 Nov 2025 02:13:05 GMT  
		Size: 61.3 MB (61305265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b25d68ee92ad43f6e22903b908e627191d52b40d47c4a45952a385e9da770b`  
		Last Modified: Fri, 14 Nov 2025 02:13:07 GMT  
		Size: 26.8 KB (26798 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:678a5bcd335db878cb5c2d0436bfb72f2a0e22001bd50dc5e2639d5d60071dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.3 MB (674332287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6445010874557d0eabe37fcbb28fd2cb290e01618c57d958bc0a599f2fc37e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:33:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:33:08 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:33:08 GMT
ARG TARGETARCH=arm64
# Thu, 13 Nov 2025 23:33:08 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:33:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:33:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 13 Nov 2025 23:33:18 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:33:18 GMT
ARG ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
# Thu, 13 Nov 2025 23:34:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:17 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9937126e3f6ac81e36f557eeddaddc7547301ed0727dcd23d7d11c926c816b1`  
		Last Modified: Fri, 14 Nov 2025 02:14:41 GMT  
		Size: 252.0 MB (251959626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566eca85793ac942cb1a78b933d3cd9a62c03e5244b1ca257d385fce03cbefc4`  
		Last Modified: Thu, 13 Nov 2025 23:36:37 GMT  
		Size: 14.3 MB (14334128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b90640a695fc75bd088183dc35d22dcc57b292342e772c131435d36ddc012db`  
		Last Modified: Thu, 13 Nov 2025 23:36:36 GMT  
		Size: 480.0 KB (479994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a4309f9383538e7e1a03f3bd15e05609e2efe5c634860781be0ff24ec4dc6`  
		Last Modified: Fri, 14 Nov 2025 02:14:02 GMT  
		Size: 378.7 MB (378694142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fee3555bcb57939e376c16317f6cf05e462bef127dd0cae64f5f82e8c16271`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d32c4f7a4676d61e4039b63cfd63d37639da5fdda8f3592be77e338a809e89`  
		Last Modified: Thu, 13 Nov 2025 23:36:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6a28977649fa0d0a4f880bdf174308fd7a781742e5233b0e79e5945733d52e`  
		Last Modified: Thu, 13 Nov 2025 23:36:36 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4becc4b798ce279ccb8267d09ebb69cb88a914ca23745ad264b6d6a34d64ded4`  
		Last Modified: Thu, 13 Nov 2025 23:36:36 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:aebf7f75f2269386e25a983f7956dc6257e99f170c9b7bc6cd6d753bbcfbc453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61339490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3408f9c11ea86958d8a7f6f5df2269dabaf0efa43104c420f918684f10ea1553`

```dockerfile
```

-	Layers:
	-	`sha256:afc4dc8f429f31d146b7eaf1f79a3ab5e9ebfed127cc3214211af9fde54bceaa`  
		Last Modified: Fri, 14 Nov 2025 02:14:25 GMT  
		Size: 61.3 MB (61312540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08797b0ceb043a11a44c5f8a198a216aebc1c3438bc9a088cac19aaae87f04ad`  
		Last Modified: Fri, 14 Nov 2025 02:14:27 GMT  
		Size: 26.9 KB (26950 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:66fcc915142f8589cc9015452e209b279111cba5bd498cbcd7285759480ea771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.1 MB (694123747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7428ce25a928c18ba5ee38049d3d74a028cfaf2d4e448204f0047f2611e862c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:28:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 14 Nov 2025 00:28:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 14 Nov 2025 00:28:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 14 Nov 2025 00:28:25 GMT
ARG TARGETARCH=ppc64le
# Fri, 14 Nov 2025 00:28:25 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 14 Nov 2025 00:28:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:38 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 14 Nov 2025 00:28:38 GMT
ENV ODOO_VERSION=18.0
# Fri, 14 Nov 2025 00:28:38 GMT
ARG ODOO_RELEASE=20251106
# Fri, 14 Nov 2025 00:28:38 GMT
ARG ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
# Fri, 14 Nov 2025 00:38:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251106 ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 14 Nov 2025 00:38:12 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 14 Nov 2025 00:38:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 14 Nov 2025 00:38:13 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251106 ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 14 Nov 2025 00:38:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 14 Nov 2025 00:38:13 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 14 Nov 2025 00:38:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 14 Nov 2025 00:38:13 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 14 Nov 2025 00:38:13 GMT
USER odoo
# Fri, 14 Nov 2025 00:38:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:38:13 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1386ae14fff90d81cccfc5474fdcab37698d1e0bc604c5eda4d2c6f9713962e`  
		Last Modified: Fri, 14 Nov 2025 10:07:37 GMT  
		Size: 265.1 MB (265078619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5a39579f85839744ff5cc25707893660aabc041a13987c1333ddd1707556c0`  
		Last Modified: Fri, 14 Nov 2025 00:36:38 GMT  
		Size: 14.9 MB (14885234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6109077a9dc3b98d12dd880fc8974cdea8fc7a3183ec21a440177c7c8d75fe`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 480.1 KB (480095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e3a0c3829ee11bf884c74396357cc913718d6a35b1bd66c0988addd992ed99`  
		Last Modified: Tue, 18 Nov 2025 13:24:04 GMT  
		Size: 379.4 MB (379372937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9da6cf45a41b2659eadb7f132fe7fc40eba992aaf4d71dac84ae4d9bd27b90`  
		Last Modified: Fri, 14 Nov 2025 00:43:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254a9e9716a44f851198b162ac7be1d506a79e96ebd883d3bd04354afba956`  
		Last Modified: Fri, 14 Nov 2025 00:43:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6fa5e2b386230a1049c4fd43e42d7ce4ef6c34ca1a81254f633c8e3301f35e`  
		Last Modified: Fri, 14 Nov 2025 00:43:27 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0711bd0dd5e02a583721bdb0aa6907768394b17743ceb1d3f3c65e2fc076023`  
		Last Modified: Fri, 14 Nov 2025 00:43:26 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:96f89af281f2e2d1448795d62a4d7653556661ccab69765f61fae80b687dbf93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61340503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bac6c5252f5e92d4cde52fe0911f6caf3990b8f240fe3441390bfcf24eb66f9`

```dockerfile
```

-	Layers:
	-	`sha256:f0f1c8a293c03323c5d22bd4af13d0b47b4dbd66f0b8cb9d8c423cf470bdc74e`  
		Last Modified: Fri, 14 Nov 2025 02:15:42 GMT  
		Size: 61.3 MB (61313648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bcc3d6678c8337bfd9bb5af3023022f63b768e7f90d4f550a03eb2ff4004558`  
		Last Modified: Fri, 14 Nov 2025 02:15:43 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:2b0546c8a98b1cd8add8bb8c3556fb03cf4205bdd0c0c57cf14aff3b207576d7
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
$ docker pull odoo@sha256:28e7fffde9a52b09a96cd25e64ab56f61cc1a538096409ef76deb958d65fba32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.0 MB (677965843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b7ab3e52402b8a60783de857347dc39d30f8d431da6f74b31cf695198096a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:31 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:33:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:33:31 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:33:31 GMT
ARG TARGETARCH=amd64
# Thu, 13 Nov 2025 23:33:31 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:33:39 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:40 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:33:40 GMT
ENV ODOO_VERSION=18.0
# Thu, 13 Nov 2025 23:33:40 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:33:40 GMT
ARG ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
# Thu, 13 Nov 2025 23:34:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:36 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de470010db47f89eb953924c14648c0d25f77c4bfbd24e42f51208c722da3346`  
		Last Modified: Fri, 14 Nov 2025 02:13:18 GMT  
		Size: 254.6 MB (254557394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09eca9b09a41e0af63400ff190eff63a0ed641ff4fc98a457237e9642040d50`  
		Last Modified: Thu, 13 Nov 2025 23:36:44 GMT  
		Size: 14.4 MB (14356518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b47d38821ec7fdf66d12ef8b2fc7e013272da58af3957532e3687c5d206d779`  
		Last Modified: Thu, 13 Nov 2025 23:36:42 GMT  
		Size: 480.1 KB (480127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ccfb8fa441c622f45c57cdc73fb8a846bae91401b732b39aac87966d41d8db`  
		Last Modified: Fri, 14 Nov 2025 02:13:45 GMT  
		Size: 378.8 MB (378844674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8225fb20d7b2e7e3e369bc5b1bed7be84a976f9e084967f502f0ee375c40d7`  
		Last Modified: Thu, 13 Nov 2025 23:35:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf744e718209ef458f75cf4bb7e3aa1c9909c5a31798c51746a65907c7f5121`  
		Last Modified: Thu, 13 Nov 2025 23:36:42 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57c75706e38c8d262fe0916604c02c36d6a62a9897c66b48d2191b112b1a318`  
		Last Modified: Thu, 13 Nov 2025 23:36:43 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde45db02ec909399f6e302ecdc35c8f97f532fe85359628969fdf38e591ae45`  
		Last Modified: Thu, 13 Nov 2025 23:36:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:de43788bfa66d2d3ee16680c1940fb52c640e5c7fd174f0198a4b4bac2c185d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61332063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e463acf31430f0078d1c38b6279efd4ba5bf133ceedda53ada860772b7549f4`

```dockerfile
```

-	Layers:
	-	`sha256:496180d9ca5102a019d9f1204e571ac8e4a7788d7ef5467bfde324bae9f6f292`  
		Last Modified: Fri, 14 Nov 2025 02:13:05 GMT  
		Size: 61.3 MB (61305265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b25d68ee92ad43f6e22903b908e627191d52b40d47c4a45952a385e9da770b`  
		Last Modified: Fri, 14 Nov 2025 02:13:07 GMT  
		Size: 26.8 KB (26798 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:678a5bcd335db878cb5c2d0436bfb72f2a0e22001bd50dc5e2639d5d60071dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.3 MB (674332287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6445010874557d0eabe37fcbb28fd2cb290e01618c57d958bc0a599f2fc37e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:33:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:33:08 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:33:08 GMT
ARG TARGETARCH=arm64
# Thu, 13 Nov 2025 23:33:08 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:33:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:33:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 13 Nov 2025 23:33:18 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:33:18 GMT
ARG ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
# Thu, 13 Nov 2025 23:34:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:17 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:17 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:17 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:17 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:17 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:17 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:17 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9937126e3f6ac81e36f557eeddaddc7547301ed0727dcd23d7d11c926c816b1`  
		Last Modified: Fri, 14 Nov 2025 02:14:41 GMT  
		Size: 252.0 MB (251959626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566eca85793ac942cb1a78b933d3cd9a62c03e5244b1ca257d385fce03cbefc4`  
		Last Modified: Thu, 13 Nov 2025 23:36:37 GMT  
		Size: 14.3 MB (14334128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b90640a695fc75bd088183dc35d22dcc57b292342e772c131435d36ddc012db`  
		Last Modified: Thu, 13 Nov 2025 23:36:36 GMT  
		Size: 480.0 KB (479994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a4309f9383538e7e1a03f3bd15e05609e2efe5c634860781be0ff24ec4dc6`  
		Last Modified: Fri, 14 Nov 2025 02:14:02 GMT  
		Size: 378.7 MB (378694142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fee3555bcb57939e376c16317f6cf05e462bef127dd0cae64f5f82e8c16271`  
		Last Modified: Thu, 13 Nov 2025 23:35:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d32c4f7a4676d61e4039b63cfd63d37639da5fdda8f3592be77e338a809e89`  
		Last Modified: Thu, 13 Nov 2025 23:36:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6a28977649fa0d0a4f880bdf174308fd7a781742e5233b0e79e5945733d52e`  
		Last Modified: Thu, 13 Nov 2025 23:36:36 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4becc4b798ce279ccb8267d09ebb69cb88a914ca23745ad264b6d6a34d64ded4`  
		Last Modified: Thu, 13 Nov 2025 23:36:36 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:aebf7f75f2269386e25a983f7956dc6257e99f170c9b7bc6cd6d753bbcfbc453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61339490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3408f9c11ea86958d8a7f6f5df2269dabaf0efa43104c420f918684f10ea1553`

```dockerfile
```

-	Layers:
	-	`sha256:afc4dc8f429f31d146b7eaf1f79a3ab5e9ebfed127cc3214211af9fde54bceaa`  
		Last Modified: Fri, 14 Nov 2025 02:14:25 GMT  
		Size: 61.3 MB (61312540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08797b0ceb043a11a44c5f8a198a216aebc1c3438bc9a088cac19aaae87f04ad`  
		Last Modified: Fri, 14 Nov 2025 02:14:27 GMT  
		Size: 26.9 KB (26950 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:66fcc915142f8589cc9015452e209b279111cba5bd498cbcd7285759480ea771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **694.1 MB (694123747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7428ce25a928c18ba5ee38049d3d74a028cfaf2d4e448204f0047f2611e862c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:28:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 14 Nov 2025 00:28:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 14 Nov 2025 00:28:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 14 Nov 2025 00:28:25 GMT
ARG TARGETARCH=ppc64le
# Fri, 14 Nov 2025 00:28:25 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 14 Nov 2025 00:28:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:38 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 14 Nov 2025 00:28:38 GMT
ENV ODOO_VERSION=18.0
# Fri, 14 Nov 2025 00:28:38 GMT
ARG ODOO_RELEASE=20251106
# Fri, 14 Nov 2025 00:28:38 GMT
ARG ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
# Fri, 14 Nov 2025 00:38:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251106 ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 14 Nov 2025 00:38:12 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 14 Nov 2025 00:38:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 14 Nov 2025 00:38:13 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251106 ODOO_SHA=8f777f0d4eeb67786ae78e5330ccd5d6931c604b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 14 Nov 2025 00:38:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 14 Nov 2025 00:38:13 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 14 Nov 2025 00:38:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 14 Nov 2025 00:38:13 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 14 Nov 2025 00:38:13 GMT
USER odoo
# Fri, 14 Nov 2025 00:38:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:38:13 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1386ae14fff90d81cccfc5474fdcab37698d1e0bc604c5eda4d2c6f9713962e`  
		Last Modified: Fri, 14 Nov 2025 10:07:37 GMT  
		Size: 265.1 MB (265078619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5a39579f85839744ff5cc25707893660aabc041a13987c1333ddd1707556c0`  
		Last Modified: Fri, 14 Nov 2025 00:36:38 GMT  
		Size: 14.9 MB (14885234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6109077a9dc3b98d12dd880fc8974cdea8fc7a3183ec21a440177c7c8d75fe`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 480.1 KB (480095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e3a0c3829ee11bf884c74396357cc913718d6a35b1bd66c0988addd992ed99`  
		Last Modified: Tue, 18 Nov 2025 13:24:04 GMT  
		Size: 379.4 MB (379372937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9da6cf45a41b2659eadb7f132fe7fc40eba992aaf4d71dac84ae4d9bd27b90`  
		Last Modified: Fri, 14 Nov 2025 00:43:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1254a9e9716a44f851198b162ac7be1d506a79e96ebd883d3bd04354afba956`  
		Last Modified: Fri, 14 Nov 2025 00:43:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6fa5e2b386230a1049c4fd43e42d7ce4ef6c34ca1a81254f633c8e3301f35e`  
		Last Modified: Fri, 14 Nov 2025 00:43:27 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0711bd0dd5e02a583721bdb0aa6907768394b17743ceb1d3f3c65e2fc076023`  
		Last Modified: Fri, 14 Nov 2025 00:43:26 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:96f89af281f2e2d1448795d62a4d7653556661ccab69765f61fae80b687dbf93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61340503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bac6c5252f5e92d4cde52fe0911f6caf3990b8f240fe3441390bfcf24eb66f9`

```dockerfile
```

-	Layers:
	-	`sha256:f0f1c8a293c03323c5d22bd4af13d0b47b4dbd66f0b8cb9d8c423cf470bdc74e`  
		Last Modified: Fri, 14 Nov 2025 02:15:42 GMT  
		Size: 61.3 MB (61313648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bcc3d6678c8337bfd9bb5af3023022f63b768e7f90d4f550a03eb2ff4004558`  
		Last Modified: Fri, 14 Nov 2025 02:15:43 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20251121`

**does not exist** (yet?)

## `odoo:19`

```console
$ docker pull odoo@sha256:14c77d72303158553838d0f1e27f664b27bf79991eb9927fea98098cd011e20b
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
$ docker pull odoo@sha256:7be8bc0848b8262756c2f98f28e51b14a0dffa6bdf10e1e06f3be91d7523ddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.0 MB (683963714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b37773787acb7b23614bd1e609b2c478e6bf648a5b1e8cce7c76d017bbbd926`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:33:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:33:22 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:33:22 GMT
ARG TARGETARCH=amd64
# Thu, 13 Nov 2025 23:33:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:33:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:33 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:33:33 GMT
ENV ODOO_VERSION=19.0
# Thu, 13 Nov 2025 23:33:33 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:33:33 GMT
ARG ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
# Thu, 13 Nov 2025 23:34:33 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24009147c1cbd6d0d21fd1b7c7c37e081c9ddc5e9870ead7b748887308f10fd`  
		Last Modified: Fri, 14 Nov 2025 02:13:46 GMT  
		Size: 254.6 MB (254557661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2b8339c51d8ab46574e40282dcbf56651122dc46b32b8651e55868953237db`  
		Last Modified: Thu, 13 Nov 2025 23:37:08 GMT  
		Size: 14.4 MB (14356385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0860a92b500a903fc7b91e12f39ce9f5782448dc7bdf0fad2852a50406416224`  
		Last Modified: Thu, 13 Nov 2025 23:37:06 GMT  
		Size: 480.0 KB (480011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d061a8bde8cc2f2bb7aa900581e4f94061df0893135318af7d480cfd725159`  
		Last Modified: Fri, 14 Nov 2025 02:13:33 GMT  
		Size: 384.8 MB (384842527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4aa3e4892ae8baf47faca1b3b49850142626000d8c2bdc866bb52aa5adc29b`  
		Last Modified: Thu, 13 Nov 2025 23:37:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207572c0300c25832de297438cb0f761856c311f247cb3590ea2f3a3cf0dae3c`  
		Last Modified: Thu, 13 Nov 2025 23:37:07 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f29023e0b8c930ba6904bc48e5af1b05883492a8f3f4cb0cb53913752b21fd`  
		Last Modified: Thu, 13 Nov 2025 23:37:07 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33193717c1297a9a3fa6b9bc76c88fbfc93ff823d8b42d5e45d82f76df1ba05e`  
		Last Modified: Thu, 13 Nov 2025 23:37:07 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:2ab726738dedf2e47a8b0bb2874e943fb23d4dae6c8876181ae713470b7c9b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68304703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5cbd68ec7b2b8ca7531ece87c3280ed41a2d0cad7393f87c96434f2b2206a4`

```dockerfile
```

-	Layers:
	-	`sha256:ace57b77c21c6f2cc3b576b01f7d80065a466791ad23b3cb012c24b7f474238e`  
		Last Modified: Fri, 14 Nov 2025 02:13:23 GMT  
		Size: 68.3 MB (68277612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e699c5b607c7fc968b2c67c44891446ec3d447ec7363677410afe20183f92651`  
		Last Modified: Fri, 14 Nov 2025 02:13:25 GMT  
		Size: 27.1 KB (27091 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:60afd19d7c442faf1b24c2873699a9868535c83812f2c0912983c9f4f5d3db54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.3 MB (680340897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0fe162942360371e815dae77353abc05b032df7b346d97ef8af1fb175ca39a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:33:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:33:06 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:33:06 GMT
ARG TARGETARCH=arm64
# Thu, 13 Nov 2025 23:33:06 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:33:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:33:18 GMT
ENV ODOO_VERSION=19.0
# Thu, 13 Nov 2025 23:33:18 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:33:18 GMT
ARG ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
# Thu, 13 Nov 2025 23:34:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d238c6a96f37cee79ca3e2ae3d5cbe43b1c647819c6a26b2208bc08f2996069`  
		Last Modified: Fri, 14 Nov 2025 01:03:20 GMT  
		Size: 252.0 MB (251959556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1400a36a1261083b8ab5015b869df457ea68b6c75b9f8da871bf734ecf7e678`  
		Last Modified: Thu, 13 Nov 2025 23:37:14 GMT  
		Size: 14.3 MB (14334215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68aa7644d7551e99bb27c57e33f0956e8c50bf292ef55674836e3c2bfd8ee08`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 480.0 KB (480025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2acf7c74d31a27fd98b109896cf7976bb1d71ac38abfdbffec633cc1a7e4cbd`  
		Last Modified: Fri, 14 Nov 2025 01:03:38 GMT  
		Size: 384.7 MB (384702706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a912872f3debec2928a054009759f170d62ec371a43a65128f82b8d5f1f354`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383cf84e668294faa8fce72334ad3c62cbea4f28b581f551fcdec9dda626e195`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc4145391dc9b0e0b1ea481a1565b16893faa8f4702e8b822a0d27931836185`  
		Last Modified: Thu, 13 Nov 2025 23:37:12 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631ac0e35fcb4ac90a14f8829d23c12a34f9d8c541d5de802dcc9354765b3fa2`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:35b9b892734d61b9f41b7019049c88adbfd87b939fdfbead366fca904f759491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68312156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce32e7db07b9fbfaae85edb07dbc85610f461d93f85f4447bf1f6d6facd5524c`

```dockerfile
```

-	Layers:
	-	`sha256:72ab400622ab246361b50c5cb3a093eb99f88046833523058e1f6010a7b98854`  
		Last Modified: Fri, 14 Nov 2025 02:15:14 GMT  
		Size: 68.3 MB (68284899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48febac04520c8cb7974d8b5cd5a4f3b0399c0b9e70e032694b0f18c0af23d4`  
		Last Modified: Fri, 14 Nov 2025 02:15:15 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:d0a39ed9b8361580bae4b7fe43e774efbf31a3c28c0bfd11ce90c5b91b3c550e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.1 MB (700130728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e6d3c268454f5e5789c1f9f6541459fe6283b12347805c11b2b045494c1450`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:28:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 14 Nov 2025 00:28:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 14 Nov 2025 00:28:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 14 Nov 2025 00:28:25 GMT
ARG TARGETARCH=ppc64le
# Fri, 14 Nov 2025 00:28:25 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 14 Nov 2025 00:28:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:38 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 14 Nov 2025 00:28:38 GMT
ENV ODOO_VERSION=19.0
# Fri, 14 Nov 2025 00:28:38 GMT
ARG ODOO_RELEASE=20251106
# Fri, 14 Nov 2025 00:28:38 GMT
ARG ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
# Fri, 14 Nov 2025 00:30:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 14 Nov 2025 00:30:56 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 14 Nov 2025 00:30:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 14 Nov 2025 00:30:57 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 14 Nov 2025 00:30:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 14 Nov 2025 00:30:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 14 Nov 2025 00:30:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 14 Nov 2025 00:30:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 14 Nov 2025 00:30:58 GMT
USER odoo
# Fri, 14 Nov 2025 00:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:30:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1386ae14fff90d81cccfc5474fdcab37698d1e0bc604c5eda4d2c6f9713962e`  
		Last Modified: Fri, 14 Nov 2025 10:07:37 GMT  
		Size: 265.1 MB (265078619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5a39579f85839744ff5cc25707893660aabc041a13987c1333ddd1707556c0`  
		Last Modified: Fri, 14 Nov 2025 00:36:38 GMT  
		Size: 14.9 MB (14885234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6109077a9dc3b98d12dd880fc8974cdea8fc7a3183ec21a440177c7c8d75fe`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 480.1 KB (480095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e39ebf97dd2cae910a19abff51594a5f3b2106b2c7b97816578e062b55da1ce`  
		Last Modified: Fri, 14 Nov 2025 10:07:36 GMT  
		Size: 385.4 MB (385379916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41636e92a5e03207ac5d94055a446e51c779d613895cb4ef4e634d154f96a76b`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe68139ae3124f7d6b61f97426450a2a0b73414ad20bbb3123ef48aadeffff7`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b944262bd2ac79bcf191ee5ac254e3c932baefd2c827c25ee8a67ad1baf3e4`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4cf37cdfa125e0585f00bf04c6e7e1f8f77a463a4c8220d56717de6c34f52a`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:7a421cf0a1272f139431b933a0569456fca97a56c433fa1f1d74c0815428fb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68313155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dae45424d2842d01ef8f121a5c35950f1de549d6e34ae298e52508c593f088`

```dockerfile
```

-	Layers:
	-	`sha256:8ab77e105a226122cf91b8b988f17e5de3653d7e73c21dcb67c206aa293e97ea`  
		Last Modified: Fri, 14 Nov 2025 02:17:02 GMT  
		Size: 68.3 MB (68286001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee25463109997f7638380e71262259d52fe9ad5616563d06e4149e0671ca7d2`  
		Last Modified: Fri, 14 Nov 2025 02:17:04 GMT  
		Size: 27.2 KB (27154 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:14c77d72303158553838d0f1e27f664b27bf79991eb9927fea98098cd011e20b
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
$ docker pull odoo@sha256:7be8bc0848b8262756c2f98f28e51b14a0dffa6bdf10e1e06f3be91d7523ddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.0 MB (683963714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b37773787acb7b23614bd1e609b2c478e6bf648a5b1e8cce7c76d017bbbd926`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:33:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:33:22 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:33:22 GMT
ARG TARGETARCH=amd64
# Thu, 13 Nov 2025 23:33:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:33:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:33 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:33:33 GMT
ENV ODOO_VERSION=19.0
# Thu, 13 Nov 2025 23:33:33 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:33:33 GMT
ARG ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
# Thu, 13 Nov 2025 23:34:33 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24009147c1cbd6d0d21fd1b7c7c37e081c9ddc5e9870ead7b748887308f10fd`  
		Last Modified: Fri, 14 Nov 2025 02:13:46 GMT  
		Size: 254.6 MB (254557661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2b8339c51d8ab46574e40282dcbf56651122dc46b32b8651e55868953237db`  
		Last Modified: Thu, 13 Nov 2025 23:37:08 GMT  
		Size: 14.4 MB (14356385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0860a92b500a903fc7b91e12f39ce9f5782448dc7bdf0fad2852a50406416224`  
		Last Modified: Thu, 13 Nov 2025 23:37:06 GMT  
		Size: 480.0 KB (480011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d061a8bde8cc2f2bb7aa900581e4f94061df0893135318af7d480cfd725159`  
		Last Modified: Fri, 14 Nov 2025 02:13:33 GMT  
		Size: 384.8 MB (384842527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4aa3e4892ae8baf47faca1b3b49850142626000d8c2bdc866bb52aa5adc29b`  
		Last Modified: Thu, 13 Nov 2025 23:37:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207572c0300c25832de297438cb0f761856c311f247cb3590ea2f3a3cf0dae3c`  
		Last Modified: Thu, 13 Nov 2025 23:37:07 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f29023e0b8c930ba6904bc48e5af1b05883492a8f3f4cb0cb53913752b21fd`  
		Last Modified: Thu, 13 Nov 2025 23:37:07 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33193717c1297a9a3fa6b9bc76c88fbfc93ff823d8b42d5e45d82f76df1ba05e`  
		Last Modified: Thu, 13 Nov 2025 23:37:07 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2ab726738dedf2e47a8b0bb2874e943fb23d4dae6c8876181ae713470b7c9b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68304703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5cbd68ec7b2b8ca7531ece87c3280ed41a2d0cad7393f87c96434f2b2206a4`

```dockerfile
```

-	Layers:
	-	`sha256:ace57b77c21c6f2cc3b576b01f7d80065a466791ad23b3cb012c24b7f474238e`  
		Last Modified: Fri, 14 Nov 2025 02:13:23 GMT  
		Size: 68.3 MB (68277612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e699c5b607c7fc968b2c67c44891446ec3d447ec7363677410afe20183f92651`  
		Last Modified: Fri, 14 Nov 2025 02:13:25 GMT  
		Size: 27.1 KB (27091 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:60afd19d7c442faf1b24c2873699a9868535c83812f2c0912983c9f4f5d3db54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.3 MB (680340897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0fe162942360371e815dae77353abc05b032df7b346d97ef8af1fb175ca39a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:33:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:33:06 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:33:06 GMT
ARG TARGETARCH=arm64
# Thu, 13 Nov 2025 23:33:06 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:33:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:33:18 GMT
ENV ODOO_VERSION=19.0
# Thu, 13 Nov 2025 23:33:18 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:33:18 GMT
ARG ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
# Thu, 13 Nov 2025 23:34:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d238c6a96f37cee79ca3e2ae3d5cbe43b1c647819c6a26b2208bc08f2996069`  
		Last Modified: Fri, 14 Nov 2025 01:03:20 GMT  
		Size: 252.0 MB (251959556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1400a36a1261083b8ab5015b869df457ea68b6c75b9f8da871bf734ecf7e678`  
		Last Modified: Thu, 13 Nov 2025 23:37:14 GMT  
		Size: 14.3 MB (14334215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68aa7644d7551e99bb27c57e33f0956e8c50bf292ef55674836e3c2bfd8ee08`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 480.0 KB (480025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2acf7c74d31a27fd98b109896cf7976bb1d71ac38abfdbffec633cc1a7e4cbd`  
		Last Modified: Fri, 14 Nov 2025 01:03:38 GMT  
		Size: 384.7 MB (384702706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a912872f3debec2928a054009759f170d62ec371a43a65128f82b8d5f1f354`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383cf84e668294faa8fce72334ad3c62cbea4f28b581f551fcdec9dda626e195`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc4145391dc9b0e0b1ea481a1565b16893faa8f4702e8b822a0d27931836185`  
		Last Modified: Thu, 13 Nov 2025 23:37:12 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631ac0e35fcb4ac90a14f8829d23c12a34f9d8c541d5de802dcc9354765b3fa2`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:35b9b892734d61b9f41b7019049c88adbfd87b939fdfbead366fca904f759491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68312156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce32e7db07b9fbfaae85edb07dbc85610f461d93f85f4447bf1f6d6facd5524c`

```dockerfile
```

-	Layers:
	-	`sha256:72ab400622ab246361b50c5cb3a093eb99f88046833523058e1f6010a7b98854`  
		Last Modified: Fri, 14 Nov 2025 02:15:14 GMT  
		Size: 68.3 MB (68284899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48febac04520c8cb7974d8b5cd5a4f3b0399c0b9e70e032694b0f18c0af23d4`  
		Last Modified: Fri, 14 Nov 2025 02:15:15 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:d0a39ed9b8361580bae4b7fe43e774efbf31a3c28c0bfd11ce90c5b91b3c550e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.1 MB (700130728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e6d3c268454f5e5789c1f9f6541459fe6283b12347805c11b2b045494c1450`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:28:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 14 Nov 2025 00:28:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 14 Nov 2025 00:28:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 14 Nov 2025 00:28:25 GMT
ARG TARGETARCH=ppc64le
# Fri, 14 Nov 2025 00:28:25 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 14 Nov 2025 00:28:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:38 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 14 Nov 2025 00:28:38 GMT
ENV ODOO_VERSION=19.0
# Fri, 14 Nov 2025 00:28:38 GMT
ARG ODOO_RELEASE=20251106
# Fri, 14 Nov 2025 00:28:38 GMT
ARG ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
# Fri, 14 Nov 2025 00:30:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 14 Nov 2025 00:30:56 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 14 Nov 2025 00:30:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 14 Nov 2025 00:30:57 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 14 Nov 2025 00:30:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 14 Nov 2025 00:30:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 14 Nov 2025 00:30:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 14 Nov 2025 00:30:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 14 Nov 2025 00:30:58 GMT
USER odoo
# Fri, 14 Nov 2025 00:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:30:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1386ae14fff90d81cccfc5474fdcab37698d1e0bc604c5eda4d2c6f9713962e`  
		Last Modified: Fri, 14 Nov 2025 10:07:37 GMT  
		Size: 265.1 MB (265078619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5a39579f85839744ff5cc25707893660aabc041a13987c1333ddd1707556c0`  
		Last Modified: Fri, 14 Nov 2025 00:36:38 GMT  
		Size: 14.9 MB (14885234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6109077a9dc3b98d12dd880fc8974cdea8fc7a3183ec21a440177c7c8d75fe`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 480.1 KB (480095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e39ebf97dd2cae910a19abff51594a5f3b2106b2c7b97816578e062b55da1ce`  
		Last Modified: Fri, 14 Nov 2025 10:07:36 GMT  
		Size: 385.4 MB (385379916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41636e92a5e03207ac5d94055a446e51c779d613895cb4ef4e634d154f96a76b`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe68139ae3124f7d6b61f97426450a2a0b73414ad20bbb3123ef48aadeffff7`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b944262bd2ac79bcf191ee5ac254e3c932baefd2c827c25ee8a67ad1baf3e4`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4cf37cdfa125e0585f00bf04c6e7e1f8f77a463a4c8220d56717de6c34f52a`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7a421cf0a1272f139431b933a0569456fca97a56c433fa1f1d74c0815428fb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68313155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dae45424d2842d01ef8f121a5c35950f1de549d6e34ae298e52508c593f088`

```dockerfile
```

-	Layers:
	-	`sha256:8ab77e105a226122cf91b8b988f17e5de3653d7e73c21dcb67c206aa293e97ea`  
		Last Modified: Fri, 14 Nov 2025 02:17:02 GMT  
		Size: 68.3 MB (68286001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee25463109997f7638380e71262259d52fe9ad5616563d06e4149e0671ca7d2`  
		Last Modified: Fri, 14 Nov 2025 02:17:04 GMT  
		Size: 27.2 KB (27154 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20251121`

**does not exist** (yet?)

## `odoo:latest`

```console
$ docker pull odoo@sha256:14c77d72303158553838d0f1e27f664b27bf79991eb9927fea98098cd011e20b
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
$ docker pull odoo@sha256:7be8bc0848b8262756c2f98f28e51b14a0dffa6bdf10e1e06f3be91d7523ddf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.0 MB (683963714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b37773787acb7b23614bd1e609b2c478e6bf648a5b1e8cce7c76d017bbbd926`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:33:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:33:22 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:33:22 GMT
ARG TARGETARCH=amd64
# Thu, 13 Nov 2025 23:33:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:33:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:33 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:33:33 GMT
ENV ODOO_VERSION=19.0
# Thu, 13 Nov 2025 23:33:33 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:33:33 GMT
ARG ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
# Thu, 13 Nov 2025 23:34:33 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:34 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24009147c1cbd6d0d21fd1b7c7c37e081c9ddc5e9870ead7b748887308f10fd`  
		Last Modified: Fri, 14 Nov 2025 02:13:46 GMT  
		Size: 254.6 MB (254557661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2b8339c51d8ab46574e40282dcbf56651122dc46b32b8651e55868953237db`  
		Last Modified: Thu, 13 Nov 2025 23:37:08 GMT  
		Size: 14.4 MB (14356385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0860a92b500a903fc7b91e12f39ce9f5782448dc7bdf0fad2852a50406416224`  
		Last Modified: Thu, 13 Nov 2025 23:37:06 GMT  
		Size: 480.0 KB (480011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d061a8bde8cc2f2bb7aa900581e4f94061df0893135318af7d480cfd725159`  
		Last Modified: Fri, 14 Nov 2025 02:13:33 GMT  
		Size: 384.8 MB (384842527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4aa3e4892ae8baf47faca1b3b49850142626000d8c2bdc866bb52aa5adc29b`  
		Last Modified: Thu, 13 Nov 2025 23:37:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207572c0300c25832de297438cb0f761856c311f247cb3590ea2f3a3cf0dae3c`  
		Last Modified: Thu, 13 Nov 2025 23:37:07 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f29023e0b8c930ba6904bc48e5af1b05883492a8f3f4cb0cb53913752b21fd`  
		Last Modified: Thu, 13 Nov 2025 23:37:07 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33193717c1297a9a3fa6b9bc76c88fbfc93ff823d8b42d5e45d82f76df1ba05e`  
		Last Modified: Thu, 13 Nov 2025 23:37:07 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:2ab726738dedf2e47a8b0bb2874e943fb23d4dae6c8876181ae713470b7c9b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68304703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5cbd68ec7b2b8ca7531ece87c3280ed41a2d0cad7393f87c96434f2b2206a4`

```dockerfile
```

-	Layers:
	-	`sha256:ace57b77c21c6f2cc3b576b01f7d80065a466791ad23b3cb012c24b7f474238e`  
		Last Modified: Fri, 14 Nov 2025 02:13:23 GMT  
		Size: 68.3 MB (68277612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e699c5b607c7fc968b2c67c44891446ec3d447ec7363677410afe20183f92651`  
		Last Modified: Fri, 14 Nov 2025 02:13:25 GMT  
		Size: 27.1 KB (27091 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:60afd19d7c442faf1b24c2873699a9868535c83812f2c0912983c9f4f5d3db54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.3 MB (680340897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0fe162942360371e815dae77353abc05b032df7b346d97ef8af1fb175ca39a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:33:06 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 13 Nov 2025 23:33:06 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 13 Nov 2025 23:33:06 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:33:06 GMT
ARG TARGETARCH=arm64
# Thu, 13 Nov 2025 23:33:06 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 13 Nov 2025 23:33:17 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:33:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 13 Nov 2025 23:33:18 GMT
ENV ODOO_VERSION=19.0
# Thu, 13 Nov 2025 23:33:18 GMT
ARG ODOO_RELEASE=20251106
# Thu, 13 Nov 2025 23:33:18 GMT
ARG ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
# Thu, 13 Nov 2025 23:34:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 13 Nov 2025 23:34:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 13 Nov 2025 23:34:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 13 Nov 2025 23:34:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 13 Nov 2025 23:34:26 GMT
USER odoo
# Thu, 13 Nov 2025 23:34:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 13 Nov 2025 23:34:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d238c6a96f37cee79ca3e2ae3d5cbe43b1c647819c6a26b2208bc08f2996069`  
		Last Modified: Fri, 14 Nov 2025 01:03:20 GMT  
		Size: 252.0 MB (251959556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1400a36a1261083b8ab5015b869df457ea68b6c75b9f8da871bf734ecf7e678`  
		Last Modified: Thu, 13 Nov 2025 23:37:14 GMT  
		Size: 14.3 MB (14334215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68aa7644d7551e99bb27c57e33f0956e8c50bf292ef55674836e3c2bfd8ee08`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 480.0 KB (480025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2acf7c74d31a27fd98b109896cf7976bb1d71ac38abfdbffec633cc1a7e4cbd`  
		Last Modified: Fri, 14 Nov 2025 01:03:38 GMT  
		Size: 384.7 MB (384702706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a912872f3debec2928a054009759f170d62ec371a43a65128f82b8d5f1f354`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383cf84e668294faa8fce72334ad3c62cbea4f28b581f551fcdec9dda626e195`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc4145391dc9b0e0b1ea481a1565b16893faa8f4702e8b822a0d27931836185`  
		Last Modified: Thu, 13 Nov 2025 23:37:12 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631ac0e35fcb4ac90a14f8829d23c12a34f9d8c541d5de802dcc9354765b3fa2`  
		Last Modified: Thu, 13 Nov 2025 23:37:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:35b9b892734d61b9f41b7019049c88adbfd87b939fdfbead366fca904f759491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68312156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce32e7db07b9fbfaae85edb07dbc85610f461d93f85f4447bf1f6d6facd5524c`

```dockerfile
```

-	Layers:
	-	`sha256:72ab400622ab246361b50c5cb3a093eb99f88046833523058e1f6010a7b98854`  
		Last Modified: Fri, 14 Nov 2025 02:15:14 GMT  
		Size: 68.3 MB (68284899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48febac04520c8cb7974d8b5cd5a4f3b0399c0b9e70e032694b0f18c0af23d4`  
		Last Modified: Fri, 14 Nov 2025 02:15:15 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:d0a39ed9b8361580bae4b7fe43e774efbf31a3c28c0bfd11ce90c5b91b3c550e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.1 MB (700130728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e6d3c268454f5e5789c1f9f6541459fe6283b12347805c11b2b045494c1450`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:28:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 14 Nov 2025 00:28:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 14 Nov 2025 00:28:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 14 Nov 2025 00:28:25 GMT
ARG TARGETARCH=ppc64le
# Fri, 14 Nov 2025 00:28:25 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 14 Nov 2025 00:28:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 00:28:38 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 14 Nov 2025 00:28:38 GMT
ENV ODOO_VERSION=19.0
# Fri, 14 Nov 2025 00:28:38 GMT
ARG ODOO_RELEASE=20251106
# Fri, 14 Nov 2025 00:28:38 GMT
ARG ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
# Fri, 14 Nov 2025 00:30:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 14 Nov 2025 00:30:56 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 14 Nov 2025 00:30:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 14 Nov 2025 00:30:57 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251106 ODOO_SHA=1773144d840cb0549968aee1edaa9dfbb6df8208
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 14 Nov 2025 00:30:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 14 Nov 2025 00:30:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 14 Nov 2025 00:30:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 14 Nov 2025 00:30:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 14 Nov 2025 00:30:58 GMT
USER odoo
# Fri, 14 Nov 2025 00:30:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 14 Nov 2025 00:30:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1386ae14fff90d81cccfc5474fdcab37698d1e0bc604c5eda4d2c6f9713962e`  
		Last Modified: Fri, 14 Nov 2025 10:07:37 GMT  
		Size: 265.1 MB (265078619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5a39579f85839744ff5cc25707893660aabc041a13987c1333ddd1707556c0`  
		Last Modified: Fri, 14 Nov 2025 00:36:38 GMT  
		Size: 14.9 MB (14885234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6109077a9dc3b98d12dd880fc8974cdea8fc7a3183ec21a440177c7c8d75fe`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 480.1 KB (480095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e39ebf97dd2cae910a19abff51594a5f3b2106b2c7b97816578e062b55da1ce`  
		Last Modified: Fri, 14 Nov 2025 10:07:36 GMT  
		Size: 385.4 MB (385379916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41636e92a5e03207ac5d94055a446e51c779d613895cb4ef4e634d154f96a76b`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe68139ae3124f7d6b61f97426450a2a0b73414ad20bbb3123ef48aadeffff7`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b944262bd2ac79bcf191ee5ac254e3c932baefd2c827c25ee8a67ad1baf3e4`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4cf37cdfa125e0585f00bf04c6e7e1f8f77a463a4c8220d56717de6c34f52a`  
		Last Modified: Fri, 14 Nov 2025 00:36:35 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7a421cf0a1272f139431b933a0569456fca97a56c433fa1f1d74c0815428fb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68313155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dae45424d2842d01ef8f121a5c35950f1de549d6e34ae298e52508c593f088`

```dockerfile
```

-	Layers:
	-	`sha256:8ab77e105a226122cf91b8b988f17e5de3653d7e73c21dcb67c206aa293e97ea`  
		Last Modified: Fri, 14 Nov 2025 02:17:02 GMT  
		Size: 68.3 MB (68286001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee25463109997f7638380e71262259d52fe9ad5616563d06e4149e0671ca7d2`  
		Last Modified: Fri, 14 Nov 2025 02:17:04 GMT  
		Size: 27.2 KB (27154 bytes)  
		MIME: application/vnd.in-toto+json
