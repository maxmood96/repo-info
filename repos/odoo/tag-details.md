<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20241108`](#odoo160-20241108)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20241108`](#odoo170-20241108)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20241108`](#odoo180-20241108)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:69de6d996f925fd38c859b6bfcb989f56617e02807d72946a1054d790ccde717
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:210c13eb6feecac9b27f10674fcef2e46a1af1bdef0fc17e3bbe742d80ac9c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586793079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6820bcff8b8c5ac578478be0eb60d79ed1327dd1ba0bc9db33122e164083ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=C.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=16.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=ac6b44b70f9b52d47818aa422c7e4d02cba9b05d
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=ac6b44b70f9b52d47818aa422c7e4d02cba9b05d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=ac6b44b70f9b52d47818aa422c7e4d02cba9b05d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d44ad0991637eaad6f12eff9fe46af587830dd9312baeeda4e7918603e98b68`  
		Last Modified: Tue, 29 Oct 2024 22:00:25 GMT  
		Size: 221.9 MB (221876145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11dca93129e04182ff8b4ce6d9ba1ab70c3ef0ef27a2f135d511818d0d91a09`  
		Last Modified: Tue, 29 Oct 2024 22:00:21 GMT  
		Size: 2.5 MB (2494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bddf734ad9c59d4eafc2ed7ae1bc651eb457e2e34630e4f4c428b8a8838cb06`  
		Last Modified: Tue, 29 Oct 2024 22:00:21 GMT  
		Size: 468.9 KB (468901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8d84c66d6dfd19d763307b69ba74dc4df3ca589c2eeb015cd0d40ebf7881a8`  
		Last Modified: Tue, 29 Oct 2024 22:00:25 GMT  
		Size: 330.5 MB (330522657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4edbcb7b7b2c7ac4b5c382418744cb40b1f3f3468d53c7ffd084be1e51b2f62`  
		Last Modified: Tue, 29 Oct 2024 22:00:22 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe75c5ef91ad01292e73dbd4767b3e471768c9b83c974fdd02e76cab4dc0f171`  
		Last Modified: Tue, 29 Oct 2024 22:00:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5824370e0fcea1634e768db413aa8da903ae7e27c63602e6bd560e357363b1c0`  
		Last Modified: Tue, 29 Oct 2024 22:00:22 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6b7ce7d27326391908aa415404261423931c0ba784c48eb764d4dd17dc417e`  
		Last Modified: Tue, 29 Oct 2024 22:00:22 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:4e6afee0f4f3888cd8eb15bbf854d2d3b8639a33cdd66ee7387bdb0b289fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38881608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d7cc285717cce3921573bbe1f6f76dd479180cb8db9d01f332c146bfa4f1ef`

```dockerfile
```

-	Layers:
	-	`sha256:ed7fc54154fdbef7d6a910c059d34c0ae1a0b4f1e6c6d50ed5a78835bdcbbe68`  
		Last Modified: Tue, 29 Oct 2024 22:00:21 GMT  
		Size: 38.9 MB (38855032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc54f8baaa9e32d9e769e6ec561a31d432c2e0455c55c40818dc840f8571b46b`  
		Last Modified: Tue, 29 Oct 2024 22:00:21 GMT  
		Size: 26.6 KB (26576 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a211af80bdacd1bf204ecc6c0bb38660b6c28bd184509d898333e31435c82bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.4 MB (582354266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b73ba0cb61baf0c6f58c7baefd8a2e08f92c517c8fbf4478926b06e714ee5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=C.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=16.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=ac6b44b70f9b52d47818aa422c7e4d02cba9b05d
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=ac6b44b70f9b52d47818aa422c7e4d02cba9b05d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=ac6b44b70f9b52d47818aa422c7e4d02cba9b05d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7e121ddf74ff038782441ab906f9c4ef65eaef123c14702a397004aec7c1bf`  
		Last Modified: Tue, 29 Oct 2024 23:56:00 GMT  
		Size: 219.1 MB (219131869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fb602fa5f4452693adb41554bf65d1a713cc92fa83b051bda32893aaf85b46`  
		Last Modified: Tue, 29 Oct 2024 23:55:56 GMT  
		Size: 2.5 MB (2504212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8b97b7092ad493682a04140c385dde374718eb81cb2fe499f7236eeef30d56`  
		Last Modified: Tue, 29 Oct 2024 23:55:56 GMT  
		Size: 468.9 KB (468858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3c840f5fd1e422d88f5bd1d0a2b6584d65ad0553914a9ce7213442cef7fb37`  
		Last Modified: Tue, 29 Oct 2024 23:56:05 GMT  
		Size: 330.2 MB (330171134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e438719623eb357f302f8d9ac49bbb235fe8c836312e507ac8ab44b0306ac30`  
		Last Modified: Tue, 29 Oct 2024 23:55:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fa0ee620388ebce2084752a7a49f30ec3eb971bdce5202846dd8994835c83e`  
		Last Modified: Tue, 29 Oct 2024 23:55:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56fe4a7090b36d0d80bfc7d32f49295ce064471acc649cb848c54169cc30e4f`  
		Last Modified: Tue, 29 Oct 2024 23:55:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc292ac55968df66bd2a963fe2f9d939b53210c5c1929fb0d0c5088512144fe`  
		Last Modified: Tue, 29 Oct 2024 23:55:58 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:a24636da66658a159987e8588ed5eb5ab61a90abebafeb948960487f2e169073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38888226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648fa92d02b58b79d6f6f46318b22e7098a08ea6ade3accf267313368a59fc39`

```dockerfile
```

-	Layers:
	-	`sha256:6601eefa3333ab2c578db03e318cf03bb94c049783766e7c8e0ac2929a96368c`  
		Last Modified: Tue, 29 Oct 2024 23:55:57 GMT  
		Size: 38.9 MB (38861504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b711690704ac98a7ba2e102ad4e353544256a2656a1ae118c7d1eac14a001f76`  
		Last Modified: Tue, 29 Oct 2024 23:55:55 GMT  
		Size: 26.7 KB (26722 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:69de6d996f925fd38c859b6bfcb989f56617e02807d72946a1054d790ccde717
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:210c13eb6feecac9b27f10674fcef2e46a1af1bdef0fc17e3bbe742d80ac9c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586793079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6820bcff8b8c5ac578478be0eb60d79ed1327dd1ba0bc9db33122e164083ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=C.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=16.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=ac6b44b70f9b52d47818aa422c7e4d02cba9b05d
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=ac6b44b70f9b52d47818aa422c7e4d02cba9b05d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=ac6b44b70f9b52d47818aa422c7e4d02cba9b05d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d44ad0991637eaad6f12eff9fe46af587830dd9312baeeda4e7918603e98b68`  
		Last Modified: Tue, 29 Oct 2024 22:00:25 GMT  
		Size: 221.9 MB (221876145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11dca93129e04182ff8b4ce6d9ba1ab70c3ef0ef27a2f135d511818d0d91a09`  
		Last Modified: Tue, 29 Oct 2024 22:00:21 GMT  
		Size: 2.5 MB (2494145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bddf734ad9c59d4eafc2ed7ae1bc651eb457e2e34630e4f4c428b8a8838cb06`  
		Last Modified: Tue, 29 Oct 2024 22:00:21 GMT  
		Size: 468.9 KB (468901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8d84c66d6dfd19d763307b69ba74dc4df3ca589c2eeb015cd0d40ebf7881a8`  
		Last Modified: Tue, 29 Oct 2024 22:00:25 GMT  
		Size: 330.5 MB (330522657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4edbcb7b7b2c7ac4b5c382418744cb40b1f3f3468d53c7ffd084be1e51b2f62`  
		Last Modified: Tue, 29 Oct 2024 22:00:22 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe75c5ef91ad01292e73dbd4767b3e471768c9b83c974fdd02e76cab4dc0f171`  
		Last Modified: Tue, 29 Oct 2024 22:00:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5824370e0fcea1634e768db413aa8da903ae7e27c63602e6bd560e357363b1c0`  
		Last Modified: Tue, 29 Oct 2024 22:00:22 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6b7ce7d27326391908aa415404261423931c0ba784c48eb764d4dd17dc417e`  
		Last Modified: Tue, 29 Oct 2024 22:00:22 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4e6afee0f4f3888cd8eb15bbf854d2d3b8639a33cdd66ee7387bdb0b289fbe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38881608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d7cc285717cce3921573bbe1f6f76dd479180cb8db9d01f332c146bfa4f1ef`

```dockerfile
```

-	Layers:
	-	`sha256:ed7fc54154fdbef7d6a910c059d34c0ae1a0b4f1e6c6d50ed5a78835bdcbbe68`  
		Last Modified: Tue, 29 Oct 2024 22:00:21 GMT  
		Size: 38.9 MB (38855032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc54f8baaa9e32d9e769e6ec561a31d432c2e0455c55c40818dc840f8571b46b`  
		Last Modified: Tue, 29 Oct 2024 22:00:21 GMT  
		Size: 26.6 KB (26576 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a211af80bdacd1bf204ecc6c0bb38660b6c28bd184509d898333e31435c82bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.4 MB (582354266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b73ba0cb61baf0c6f58c7baefd8a2e08f92c517c8fbf4478926b06e714ee5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=C.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=16.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=ac6b44b70f9b52d47818aa422c7e4d02cba9b05d
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=ac6b44b70f9b52d47818aa422c7e4d02cba9b05d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=ac6b44b70f9b52d47818aa422c7e4d02cba9b05d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7e121ddf74ff038782441ab906f9c4ef65eaef123c14702a397004aec7c1bf`  
		Last Modified: Tue, 29 Oct 2024 23:56:00 GMT  
		Size: 219.1 MB (219131869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fb602fa5f4452693adb41554bf65d1a713cc92fa83b051bda32893aaf85b46`  
		Last Modified: Tue, 29 Oct 2024 23:55:56 GMT  
		Size: 2.5 MB (2504212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8b97b7092ad493682a04140c385dde374718eb81cb2fe499f7236eeef30d56`  
		Last Modified: Tue, 29 Oct 2024 23:55:56 GMT  
		Size: 468.9 KB (468858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3c840f5fd1e422d88f5bd1d0a2b6584d65ad0553914a9ce7213442cef7fb37`  
		Last Modified: Tue, 29 Oct 2024 23:56:05 GMT  
		Size: 330.2 MB (330171134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e438719623eb357f302f8d9ac49bbb235fe8c836312e507ac8ab44b0306ac30`  
		Last Modified: Tue, 29 Oct 2024 23:55:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fa0ee620388ebce2084752a7a49f30ec3eb971bdce5202846dd8994835c83e`  
		Last Modified: Tue, 29 Oct 2024 23:55:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56fe4a7090b36d0d80bfc7d32f49295ce064471acc649cb848c54169cc30e4f`  
		Last Modified: Tue, 29 Oct 2024 23:55:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc292ac55968df66bd2a963fe2f9d939b53210c5c1929fb0d0c5088512144fe`  
		Last Modified: Tue, 29 Oct 2024 23:55:58 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a24636da66658a159987e8588ed5eb5ab61a90abebafeb948960487f2e169073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38888226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648fa92d02b58b79d6f6f46318b22e7098a08ea6ade3accf267313368a59fc39`

```dockerfile
```

-	Layers:
	-	`sha256:6601eefa3333ab2c578db03e318cf03bb94c049783766e7c8e0ac2929a96368c`  
		Last Modified: Tue, 29 Oct 2024 23:55:57 GMT  
		Size: 38.9 MB (38861504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b711690704ac98a7ba2e102ad4e353544256a2656a1ae118c7d1eac14a001f76`  
		Last Modified: Tue, 29 Oct 2024 23:55:55 GMT  
		Size: 26.7 KB (26722 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20241108`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:17`

```console
$ docker pull odoo@sha256:297141fa8edc5b48fe9b0bd6ac38446e038c179f106d6fb08c930e1b60516501
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:ca55031385e4a7bef08cffd307e6d320d57c6c3ab71e810011fae008805d49aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.1 MB (598051418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32778f5a8fc88f2e90e7f4b4f51612279f0495497b403809a3e6bb622f9635a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae0db15d2587c3aa0e80b7693a96addcdb1b09edba7c829da953c6f408065fe`  
		Last Modified: Tue, 29 Oct 2024 22:00:31 GMT  
		Size: 233.8 MB (233762196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca2dcaa1564cf0c8b0c80b53f3670fb4d9820e8baede902693862d6d5af91ce`  
		Last Modified: Tue, 29 Oct 2024 22:00:28 GMT  
		Size: 2.4 MB (2405325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af2a0054d1ee3a435044dc0f151dc9719fa6e4301023102b56d8b030cb8c72a`  
		Last Modified: Tue, 29 Oct 2024 22:00:27 GMT  
		Size: 469.9 KB (469919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1123f711736fd849f6a7388eafdf2947d2b8c5925b4372c5dc92d91171b331bb`  
		Last Modified: Tue, 29 Oct 2024 22:00:32 GMT  
		Size: 331.9 MB (331875855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41694f67331e5ebe820b2d75145cb921bbdffd6fdac5f4c984245ab1b74adf98`  
		Last Modified: Tue, 29 Oct 2024 22:00:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f7c37ae27038da9d0adfda17d8a8f3e8865ca3c171717dd10b855266795798`  
		Last Modified: Tue, 29 Oct 2024 22:00:29 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0553ce2d2a0063e12c5cc7dd9fead4565be82311483554028ea5a2df22484c6`  
		Last Modified: Tue, 29 Oct 2024 22:00:29 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cded9ecd91e54731fbc1594fef6a385ddeb8d9aada58ee54637bf3ba25c50a`  
		Last Modified: Tue, 29 Oct 2024 22:00:29 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:39eac25f1b4938ae2da7f8fad9ebf02a5f23c7b893d120f2f292b21d05c8091d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39589566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec787acf9427c98517cea1915499286822fb3ab8ae0ae7634eaa5868b7483c07`

```dockerfile
```

-	Layers:
	-	`sha256:b9905710f9fee8b6fa393fcc9cad6c24f91943b6ca059775f905d343cb6ce702`  
		Last Modified: Tue, 29 Oct 2024 22:00:28 GMT  
		Size: 39.6 MB (39562731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb26e02f3246a14ba72fea45b53f54d7371831d1f4cd28a857978c5c1647c1e`  
		Last Modified: Tue, 29 Oct 2024 22:00:27 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6cc963f293ef7662321c8f1c0d5dd9d5d3255ed4c5141562213bb5fb9df5e793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.9 MB (592870770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead9731b6d76c92c407ef506008770e4a33b51c0820f7045d9a0207ff9f62482`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18211c8e329275bb29117c3d983191edbfee5050326e7bb08db03638fd2e92`  
		Last Modified: Tue, 29 Oct 2024 23:52:03 GMT  
		Size: 231.2 MB (231156543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf52d1133734edf7dea066071b312ac1709c372d8f53054a846a5068e0edfe1`  
		Last Modified: Tue, 29 Oct 2024 23:51:59 GMT  
		Size: 2.4 MB (2398275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667841aad1543152f065e7435f0a15b2920d3c511c5111019bdbb25efaf304c8`  
		Last Modified: Tue, 29 Oct 2024 23:51:58 GMT  
		Size: 469.8 KB (469824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a1f23a85c41427ac93dbf021f7abeca6d8c3be4355acfec9a7a8ca4c9c79da`  
		Last Modified: Tue, 29 Oct 2024 23:52:06 GMT  
		Size: 331.5 MB (331485355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e84ed048b917806f4d43ff8925cc352b6cefc22a5972d07293ae9fd88378f3`  
		Last Modified: Tue, 29 Oct 2024 23:51:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0f446410d78ac4e5b3f2bd4cd6f87b168c245000c106efb8ad2d5dba5c12db`  
		Last Modified: Tue, 29 Oct 2024 23:52:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a027bc41c747f4e9abdcbfda88b9865c768714c8ae0190234db53274153c11`  
		Last Modified: Tue, 29 Oct 2024 23:52:00 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4746e4e87f165271a5d479ae9d4ab1f871b5dad04ed1ee35ab2fd13b8ce95d3b`  
		Last Modified: Tue, 29 Oct 2024 23:52:01 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:0477035dee3179326e70245b1afdaeabf8b2f29ee7ab6ad97e7dd6bd1c341267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39596231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2dabaefb81b38e7a5e80d8c5e99ab89e33141cded51ab62b91bccc4c29988d`

```dockerfile
```

-	Layers:
	-	`sha256:836bc34fdcac8c1dbf64f5de43a1a59c86d917baad43a5f9642a573a1b7e0a13`  
		Last Modified: Tue, 29 Oct 2024 23:52:00 GMT  
		Size: 39.6 MB (39569244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d81194903fbb100a6d0180d6809d0eaf603f22d2544e83a64482a78cce4daf3`  
		Last Modified: Tue, 29 Oct 2024 23:51:58 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:bb94552c407405698dd7766594332b2a2f348497dfb8ff34ddc02b9d5862f6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.5 MB (614538618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c34d8b717759d285490713424729fabd8adf56650b1e95e56ba16ae9568dc55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241029 ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241029 ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b048f44b1504a3d2ecae241529c88be6b9d3c112070b0117152912c964fdb8b4`  
		Last Modified: Tue, 29 Oct 2024 22:24:05 GMT  
		Size: 243.3 MB (243298380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224de38bd45f4460c67b521677946570e68856248ce8a94b53b9258838bb9f14`  
		Last Modified: Tue, 29 Oct 2024 22:23:59 GMT  
		Size: 2.7 MB (2708587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692e239060a3900d3b2ab3579a383598dcb85132b2c8040089ea7de5047d0a6b`  
		Last Modified: Tue, 29 Oct 2024 22:23:59 GMT  
		Size: 469.8 KB (469842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9c567a3ef946dcfceb258626a039b72f27272fa71c59d1e539873a838b2675`  
		Last Modified: Tue, 29 Oct 2024 22:24:07 GMT  
		Size: 333.6 MB (333611126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8efe53fabc15a4ee3a7706d8dcd0487568ef62a0613726f8719b0b6ed8da23`  
		Last Modified: Tue, 29 Oct 2024 22:24:00 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd6064ef1237010f6ec7f1d71133c645de50c9293664879bb3d9634c998e6d3`  
		Last Modified: Tue, 29 Oct 2024 22:24:00 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c61e30a03ade7d718e39e46426f2f3c1db733ea430790136067397f0c23d442`  
		Last Modified: Tue, 29 Oct 2024 22:24:01 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022b57e72a3fd7ad29981319fa97dfe284d35a61f845a5c5578b8b3b0b2ab655`  
		Last Modified: Tue, 29 Oct 2024 22:24:01 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:e1872e0cf0540da9bca1fa4f7e90155eb3cac1b7f2cd1e018f10e2c20d53a5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39597928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6b0e350590a4e85d21cbacb38717ef6063049a4b0fd2e9f97eba9cb7a78762`

```dockerfile
```

-	Layers:
	-	`sha256:bccd93ddb1179350b9f55ded19d0fd953a9b0f1a8c7df0f3b2dbbe0abaaa1702`  
		Last Modified: Tue, 29 Oct 2024 22:24:00 GMT  
		Size: 39.6 MB (39571038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a15276718b459b494bca0900daa3cb5d1e7660a8b3ac021dea142ab1d8622f`  
		Last Modified: Tue, 29 Oct 2024 22:23:58 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:297141fa8edc5b48fe9b0bd6ac38446e038c179f106d6fb08c930e1b60516501
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:ca55031385e4a7bef08cffd307e6d320d57c6c3ab71e810011fae008805d49aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.1 MB (598051418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32778f5a8fc88f2e90e7f4b4f51612279f0495497b403809a3e6bb622f9635a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae0db15d2587c3aa0e80b7693a96addcdb1b09edba7c829da953c6f408065fe`  
		Last Modified: Tue, 29 Oct 2024 22:00:31 GMT  
		Size: 233.8 MB (233762196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca2dcaa1564cf0c8b0c80b53f3670fb4d9820e8baede902693862d6d5af91ce`  
		Last Modified: Tue, 29 Oct 2024 22:00:28 GMT  
		Size: 2.4 MB (2405325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af2a0054d1ee3a435044dc0f151dc9719fa6e4301023102b56d8b030cb8c72a`  
		Last Modified: Tue, 29 Oct 2024 22:00:27 GMT  
		Size: 469.9 KB (469919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1123f711736fd849f6a7388eafdf2947d2b8c5925b4372c5dc92d91171b331bb`  
		Last Modified: Tue, 29 Oct 2024 22:00:32 GMT  
		Size: 331.9 MB (331875855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41694f67331e5ebe820b2d75145cb921bbdffd6fdac5f4c984245ab1b74adf98`  
		Last Modified: Tue, 29 Oct 2024 22:00:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f7c37ae27038da9d0adfda17d8a8f3e8865ca3c171717dd10b855266795798`  
		Last Modified: Tue, 29 Oct 2024 22:00:29 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0553ce2d2a0063e12c5cc7dd9fead4565be82311483554028ea5a2df22484c6`  
		Last Modified: Tue, 29 Oct 2024 22:00:29 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cded9ecd91e54731fbc1594fef6a385ddeb8d9aada58ee54637bf3ba25c50a`  
		Last Modified: Tue, 29 Oct 2024 22:00:29 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:39eac25f1b4938ae2da7f8fad9ebf02a5f23c7b893d120f2f292b21d05c8091d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39589566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec787acf9427c98517cea1915499286822fb3ab8ae0ae7634eaa5868b7483c07`

```dockerfile
```

-	Layers:
	-	`sha256:b9905710f9fee8b6fa393fcc9cad6c24f91943b6ca059775f905d343cb6ce702`  
		Last Modified: Tue, 29 Oct 2024 22:00:28 GMT  
		Size: 39.6 MB (39562731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb26e02f3246a14ba72fea45b53f54d7371831d1f4cd28a857978c5c1647c1e`  
		Last Modified: Tue, 29 Oct 2024 22:00:27 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6cc963f293ef7662321c8f1c0d5dd9d5d3255ed4c5141562213bb5fb9df5e793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.9 MB (592870770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead9731b6d76c92c407ef506008770e4a33b51c0820f7045d9a0207ff9f62482`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c18211c8e329275bb29117c3d983191edbfee5050326e7bb08db03638fd2e92`  
		Last Modified: Tue, 29 Oct 2024 23:52:03 GMT  
		Size: 231.2 MB (231156543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf52d1133734edf7dea066071b312ac1709c372d8f53054a846a5068e0edfe1`  
		Last Modified: Tue, 29 Oct 2024 23:51:59 GMT  
		Size: 2.4 MB (2398275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667841aad1543152f065e7435f0a15b2920d3c511c5111019bdbb25efaf304c8`  
		Last Modified: Tue, 29 Oct 2024 23:51:58 GMT  
		Size: 469.8 KB (469824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a1f23a85c41427ac93dbf021f7abeca6d8c3be4355acfec9a7a8ca4c9c79da`  
		Last Modified: Tue, 29 Oct 2024 23:52:06 GMT  
		Size: 331.5 MB (331485355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e84ed048b917806f4d43ff8925cc352b6cefc22a5972d07293ae9fd88378f3`  
		Last Modified: Tue, 29 Oct 2024 23:51:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0f446410d78ac4e5b3f2bd4cd6f87b168c245000c106efb8ad2d5dba5c12db`  
		Last Modified: Tue, 29 Oct 2024 23:52:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a027bc41c747f4e9abdcbfda88b9865c768714c8ae0190234db53274153c11`  
		Last Modified: Tue, 29 Oct 2024 23:52:00 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4746e4e87f165271a5d479ae9d4ab1f871b5dad04ed1ee35ab2fd13b8ce95d3b`  
		Last Modified: Tue, 29 Oct 2024 23:52:01 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0477035dee3179326e70245b1afdaeabf8b2f29ee7ab6ad97e7dd6bd1c341267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39596231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2dabaefb81b38e7a5e80d8c5e99ab89e33141cded51ab62b91bccc4c29988d`

```dockerfile
```

-	Layers:
	-	`sha256:836bc34fdcac8c1dbf64f5de43a1a59c86d917baad43a5f9642a573a1b7e0a13`  
		Last Modified: Tue, 29 Oct 2024 23:52:00 GMT  
		Size: 39.6 MB (39569244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d81194903fbb100a6d0180d6809d0eaf603f22d2544e83a64482a78cce4daf3`  
		Last Modified: Tue, 29 Oct 2024 23:51:58 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:bb94552c407405698dd7766594332b2a2f348497dfb8ff34ddc02b9d5862f6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.5 MB (614538618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c34d8b717759d285490713424729fabd8adf56650b1e95e56ba16ae9568dc55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241029 ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241029 ODOO_SHA=200c2bacf48dbb794c8fd55750a1adb0b59e32e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b048f44b1504a3d2ecae241529c88be6b9d3c112070b0117152912c964fdb8b4`  
		Last Modified: Tue, 29 Oct 2024 22:24:05 GMT  
		Size: 243.3 MB (243298380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224de38bd45f4460c67b521677946570e68856248ce8a94b53b9258838bb9f14`  
		Last Modified: Tue, 29 Oct 2024 22:23:59 GMT  
		Size: 2.7 MB (2708587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692e239060a3900d3b2ab3579a383598dcb85132b2c8040089ea7de5047d0a6b`  
		Last Modified: Tue, 29 Oct 2024 22:23:59 GMT  
		Size: 469.8 KB (469842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9c567a3ef946dcfceb258626a039b72f27272fa71c59d1e539873a838b2675`  
		Last Modified: Tue, 29 Oct 2024 22:24:07 GMT  
		Size: 333.6 MB (333611126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8efe53fabc15a4ee3a7706d8dcd0487568ef62a0613726f8719b0b6ed8da23`  
		Last Modified: Tue, 29 Oct 2024 22:24:00 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd6064ef1237010f6ec7f1d71133c645de50c9293664879bb3d9634c998e6d3`  
		Last Modified: Tue, 29 Oct 2024 22:24:00 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c61e30a03ade7d718e39e46426f2f3c1db733ea430790136067397f0c23d442`  
		Last Modified: Tue, 29 Oct 2024 22:24:01 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022b57e72a3fd7ad29981319fa97dfe284d35a61f845a5c5578b8b3b0b2ab655`  
		Last Modified: Tue, 29 Oct 2024 22:24:01 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e1872e0cf0540da9bca1fa4f7e90155eb3cac1b7f2cd1e018f10e2c20d53a5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39597928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6b0e350590a4e85d21cbacb38717ef6063049a4b0fd2e9f97eba9cb7a78762`

```dockerfile
```

-	Layers:
	-	`sha256:bccd93ddb1179350b9f55ded19d0fd953a9b0f1a8c7df0f3b2dbbe0abaaa1702`  
		Last Modified: Tue, 29 Oct 2024 22:24:00 GMT  
		Size: 39.6 MB (39571038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a15276718b459b494bca0900daa3cb5d1e7660a8b3ac021dea142ab1d8622f`  
		Last Modified: Tue, 29 Oct 2024 22:23:58 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20241108`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:18`

```console
$ docker pull odoo@sha256:ee15af8e1eb992ccebb1d8345cdd8b861845cc01c04ea0f48b77b78324488673
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
$ docker pull odoo@sha256:78aabb75be977d0fbc2bdc60255f222b5a1d7dc0b3f0195a805970fb95f67b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657505774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7c05a2eb4e8f7aa3b0efaf02d37229150694a3bf8e88d6fad53d75525a6db5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=18.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63561abe36430920ae9c538575e9167c01d03e75b4ee22fad5c1a2c194e61647`  
		Last Modified: Tue, 29 Oct 2024 22:00:58 GMT  
		Size: 255.6 MB (255640718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8d3bb5f6d869319ec43b8ea55ac01f2d95484d8f9705589529275d9c0320ca`  
		Last Modified: Tue, 29 Oct 2024 22:00:55 GMT  
		Size: 14.1 MB (14142265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecb2f2b755b1e680a1663ec2195972828db4e5d0cfb32fefb628612300c7be8`  
		Last Modified: Tue, 29 Oct 2024 22:00:55 GMT  
		Size: 469.6 KB (469566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f1285f2b76a2ceab06719112c8bfca824850281b29549917c9a27beb1fb72d`  
		Last Modified: Tue, 29 Oct 2024 22:01:00 GMT  
		Size: 357.5 MB (357500423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b46636260a4b11c6d019e7fbaab1e835068772303f0443c9a54e57ca3055970`  
		Last Modified: Tue, 29 Oct 2024 22:00:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c404a0f3ae81df5de58c1387ba835bc2875c1b62a219af887c3547703c5548`  
		Last Modified: Tue, 29 Oct 2024 22:00:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ee78aec1fd70062c79a759c19d43d72bf0425cb2fa51937d6cbf00a996ed73`  
		Last Modified: Tue, 29 Oct 2024 22:00:57 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66816c6c9dcbcb05bbe8362b53d49c7414bf671bbdce7eee72b9b85a0032aec1`  
		Last Modified: Tue, 29 Oct 2024 22:00:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:eb3ba98c157ab13466e420954c0d167b829f596b36916b082d8e810cb1a0dc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56188283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed1036a494ae7bbdb4b5d136cf672a0b73cef771a78fbc0a417537a38487dc0`

```dockerfile
```

-	Layers:
	-	`sha256:7e96d7b27433cd80bbd10f3f20e7044039b5f3e7abc7519adca5b8bc3658386b`  
		Last Modified: Tue, 29 Oct 2024 22:00:55 GMT  
		Size: 56.2 MB (56161147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9cb1649bddc1b3a0d398a0ee8eed6149b98b8ec533c17c10957d9bdd9135fb`  
		Last Modified: Tue, 29 Oct 2024 22:00:55 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:432ead532f1c9ee0e3d0a066735b5965156383fd0c8eec4f2a9669b09ca82823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.8 MB (653816874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f88c36958bba8bb6aeed093dcd5efee475108f4e8fe82a468dcbf1bf59d97e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=18.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8998091eb84f1c2fe96e4515e2d7d0bbf238c7a6a3daac3087a6de76df43bb6`  
		Last Modified: Tue, 29 Oct 2024 23:45:09 GMT  
		Size: 253.0 MB (252999384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066e920339d25f98363c69fa93c29502ab5e1f88a931acbc7adb8de85dd23f91`  
		Last Modified: Tue, 29 Oct 2024 23:45:02 GMT  
		Size: 14.1 MB (14115397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d48a21447981fca012489cc357bad5ad4681c58cf2d339752c795da2385023`  
		Last Modified: Tue, 29 Oct 2024 23:45:02 GMT  
		Size: 469.7 KB (469697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c409b6d782a8f341b6d4c2cd8b162702f9b20e777b6c529221264e788f661`  
		Last Modified: Tue, 29 Oct 2024 23:45:09 GMT  
		Size: 357.3 MB (357344112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbce5115d090f76131120a94b9fb8739d567040f067e017f07ed6280c4877a4`  
		Last Modified: Tue, 29 Oct 2024 23:45:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a73e19713601faa7fb044b275cba398f3b332aed69ddb9011a9259ffb7f80b1`  
		Last Modified: Tue, 29 Oct 2024 23:45:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c4969ff32461dfabfb35f6b1936f78b5d2299905a660392d1852bdaef88ba1`  
		Last Modified: Tue, 29 Oct 2024 23:45:04 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715f0f68122a224eb586bc24d21e80b16f58e7e02f60d1493a4ff1cc87b62c8e`  
		Last Modified: Tue, 29 Oct 2024 23:45:04 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:1c5f9e2c904637c6d6839e3a427ec7070bedef6cc074c367ee925e2b79e5fa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56195741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f0237bef0bdb2c958dde4f079be484a45e3c07d1b8fad741eccd03ff7bad93`

```dockerfile
```

-	Layers:
	-	`sha256:466262b724e5bf0c636d0e2eb8cdfc941a17a50e67c27b2520554af4b2de2904`  
		Last Modified: Tue, 29 Oct 2024 23:45:03 GMT  
		Size: 56.2 MB (56168441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f44067658da6ce385ce961a5be62fb7980b6329a6d92ddd70030a4280b86cb`  
		Last Modified: Tue, 29 Oct 2024 23:45:01 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:df395f570e512d430ace4cc217760252188b834958b17c693ed3b21874cc6029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.0 MB (674013287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b764d2a5531086d62f490de7713bb271350f293eaddf952fbcf702d43f668d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=18.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2aaf46c089e715d1f81d86cc3df7c4516496efc1679739c02eda8573b510b75`  
		Last Modified: Tue, 29 Oct 2024 22:14:05 GMT  
		Size: 266.4 MB (266406087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07df2513d514cab4d4efc4141744d8556b72fe962571ffa0dc4c7c18959f1588`  
		Last Modified: Tue, 29 Oct 2024 22:13:50 GMT  
		Size: 14.7 MB (14686271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d7645b1528842fc361f95fa690e2dcfa1f7fdfaaabfe2bf3da69eab89e00d0`  
		Last Modified: Tue, 29 Oct 2024 22:13:49 GMT  
		Size: 469.6 KB (469571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef77b6067cbffcf4fec9d1fd8361053e10903a20641c3fd5d709c47f70cba22`  
		Last Modified: Tue, 29 Oct 2024 22:14:15 GMT  
		Size: 358.1 MB (358059948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9403e554ede662d23207a0eeb7b020b7a99303d5205bcf216bf8064475662642`  
		Last Modified: Tue, 29 Oct 2024 22:13:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d53424306db37ca8ca790dacfbf6fc319499f2093fcd6a5573845ab01bb41dd`  
		Last Modified: Tue, 29 Oct 2024 22:13:52 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a141d3ad04adf215c1d0ef2e908b185cb965d9eb8cec6eae7fb2ecd65c7e041d`  
		Last Modified: Tue, 29 Oct 2024 22:13:52 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5edc774a76ad91872839c754694c70a624eb9bf383ee7fe1f8683b182b0223`  
		Last Modified: Tue, 29 Oct 2024 22:13:53 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:2dd977eae714a81b2a20454e84fb20013851635645c548b32bcd38025ac2ba71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56196488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a444bbff564e9ee4caebb64649e7ce24c14ac867e7bd912939461e2e82017b8f`

```dockerfile
```

-	Layers:
	-	`sha256:81186d3a2abb2a2b5e7791a6f652ad77e30028f77ee7ed29b597e2a4976f9459`  
		Last Modified: Tue, 29 Oct 2024 22:13:52 GMT  
		Size: 56.2 MB (56169290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6813723ec5a4d5f24ecbdddbd61d181052da30d71bb599f3a38d39f1f6757c32`  
		Last Modified: Tue, 29 Oct 2024 22:13:49 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:ee15af8e1eb992ccebb1d8345cdd8b861845cc01c04ea0f48b77b78324488673
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
$ docker pull odoo@sha256:78aabb75be977d0fbc2bdc60255f222b5a1d7dc0b3f0195a805970fb95f67b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657505774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7c05a2eb4e8f7aa3b0efaf02d37229150694a3bf8e88d6fad53d75525a6db5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=18.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63561abe36430920ae9c538575e9167c01d03e75b4ee22fad5c1a2c194e61647`  
		Last Modified: Tue, 29 Oct 2024 22:00:58 GMT  
		Size: 255.6 MB (255640718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8d3bb5f6d869319ec43b8ea55ac01f2d95484d8f9705589529275d9c0320ca`  
		Last Modified: Tue, 29 Oct 2024 22:00:55 GMT  
		Size: 14.1 MB (14142265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecb2f2b755b1e680a1663ec2195972828db4e5d0cfb32fefb628612300c7be8`  
		Last Modified: Tue, 29 Oct 2024 22:00:55 GMT  
		Size: 469.6 KB (469566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f1285f2b76a2ceab06719112c8bfca824850281b29549917c9a27beb1fb72d`  
		Last Modified: Tue, 29 Oct 2024 22:01:00 GMT  
		Size: 357.5 MB (357500423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b46636260a4b11c6d019e7fbaab1e835068772303f0443c9a54e57ca3055970`  
		Last Modified: Tue, 29 Oct 2024 22:00:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c404a0f3ae81df5de58c1387ba835bc2875c1b62a219af887c3547703c5548`  
		Last Modified: Tue, 29 Oct 2024 22:00:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ee78aec1fd70062c79a759c19d43d72bf0425cb2fa51937d6cbf00a996ed73`  
		Last Modified: Tue, 29 Oct 2024 22:00:57 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66816c6c9dcbcb05bbe8362b53d49c7414bf671bbdce7eee72b9b85a0032aec1`  
		Last Modified: Tue, 29 Oct 2024 22:00:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:eb3ba98c157ab13466e420954c0d167b829f596b36916b082d8e810cb1a0dc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56188283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed1036a494ae7bbdb4b5d136cf672a0b73cef771a78fbc0a417537a38487dc0`

```dockerfile
```

-	Layers:
	-	`sha256:7e96d7b27433cd80bbd10f3f20e7044039b5f3e7abc7519adca5b8bc3658386b`  
		Last Modified: Tue, 29 Oct 2024 22:00:55 GMT  
		Size: 56.2 MB (56161147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9cb1649bddc1b3a0d398a0ee8eed6149b98b8ec533c17c10957d9bdd9135fb`  
		Last Modified: Tue, 29 Oct 2024 22:00:55 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:432ead532f1c9ee0e3d0a066735b5965156383fd0c8eec4f2a9669b09ca82823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.8 MB (653816874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f88c36958bba8bb6aeed093dcd5efee475108f4e8fe82a468dcbf1bf59d97e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=18.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8998091eb84f1c2fe96e4515e2d7d0bbf238c7a6a3daac3087a6de76df43bb6`  
		Last Modified: Tue, 29 Oct 2024 23:45:09 GMT  
		Size: 253.0 MB (252999384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066e920339d25f98363c69fa93c29502ab5e1f88a931acbc7adb8de85dd23f91`  
		Last Modified: Tue, 29 Oct 2024 23:45:02 GMT  
		Size: 14.1 MB (14115397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d48a21447981fca012489cc357bad5ad4681c58cf2d339752c795da2385023`  
		Last Modified: Tue, 29 Oct 2024 23:45:02 GMT  
		Size: 469.7 KB (469697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c409b6d782a8f341b6d4c2cd8b162702f9b20e777b6c529221264e788f661`  
		Last Modified: Tue, 29 Oct 2024 23:45:09 GMT  
		Size: 357.3 MB (357344112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbce5115d090f76131120a94b9fb8739d567040f067e017f07ed6280c4877a4`  
		Last Modified: Tue, 29 Oct 2024 23:45:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a73e19713601faa7fb044b275cba398f3b332aed69ddb9011a9259ffb7f80b1`  
		Last Modified: Tue, 29 Oct 2024 23:45:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c4969ff32461dfabfb35f6b1936f78b5d2299905a660392d1852bdaef88ba1`  
		Last Modified: Tue, 29 Oct 2024 23:45:04 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715f0f68122a224eb586bc24d21e80b16f58e7e02f60d1493a4ff1cc87b62c8e`  
		Last Modified: Tue, 29 Oct 2024 23:45:04 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1c5f9e2c904637c6d6839e3a427ec7070bedef6cc074c367ee925e2b79e5fa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56195741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f0237bef0bdb2c958dde4f079be484a45e3c07d1b8fad741eccd03ff7bad93`

```dockerfile
```

-	Layers:
	-	`sha256:466262b724e5bf0c636d0e2eb8cdfc941a17a50e67c27b2520554af4b2de2904`  
		Last Modified: Tue, 29 Oct 2024 23:45:03 GMT  
		Size: 56.2 MB (56168441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f44067658da6ce385ce961a5be62fb7980b6329a6d92ddd70030a4280b86cb`  
		Last Modified: Tue, 29 Oct 2024 23:45:01 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:df395f570e512d430ace4cc217760252188b834958b17c693ed3b21874cc6029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.0 MB (674013287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b764d2a5531086d62f490de7713bb271350f293eaddf952fbcf702d43f668d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=18.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2aaf46c089e715d1f81d86cc3df7c4516496efc1679739c02eda8573b510b75`  
		Last Modified: Tue, 29 Oct 2024 22:14:05 GMT  
		Size: 266.4 MB (266406087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07df2513d514cab4d4efc4141744d8556b72fe962571ffa0dc4c7c18959f1588`  
		Last Modified: Tue, 29 Oct 2024 22:13:50 GMT  
		Size: 14.7 MB (14686271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d7645b1528842fc361f95fa690e2dcfa1f7fdfaaabfe2bf3da69eab89e00d0`  
		Last Modified: Tue, 29 Oct 2024 22:13:49 GMT  
		Size: 469.6 KB (469571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef77b6067cbffcf4fec9d1fd8361053e10903a20641c3fd5d709c47f70cba22`  
		Last Modified: Tue, 29 Oct 2024 22:14:15 GMT  
		Size: 358.1 MB (358059948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9403e554ede662d23207a0eeb7b020b7a99303d5205bcf216bf8064475662642`  
		Last Modified: Tue, 29 Oct 2024 22:13:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d53424306db37ca8ca790dacfbf6fc319499f2093fcd6a5573845ab01bb41dd`  
		Last Modified: Tue, 29 Oct 2024 22:13:52 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a141d3ad04adf215c1d0ef2e908b185cb965d9eb8cec6eae7fb2ecd65c7e041d`  
		Last Modified: Tue, 29 Oct 2024 22:13:52 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5edc774a76ad91872839c754694c70a624eb9bf383ee7fe1f8683b182b0223`  
		Last Modified: Tue, 29 Oct 2024 22:13:53 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2dd977eae714a81b2a20454e84fb20013851635645c548b32bcd38025ac2ba71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56196488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a444bbff564e9ee4caebb64649e7ce24c14ac867e7bd912939461e2e82017b8f`

```dockerfile
```

-	Layers:
	-	`sha256:81186d3a2abb2a2b5e7791a6f652ad77e30028f77ee7ed29b597e2a4976f9459`  
		Last Modified: Tue, 29 Oct 2024 22:13:52 GMT  
		Size: 56.2 MB (56169290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6813723ec5a4d5f24ecbdddbd61d181052da30d71bb599f3a38d39f1f6757c32`  
		Last Modified: Tue, 29 Oct 2024 22:13:49 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20241108`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:latest`

```console
$ docker pull odoo@sha256:ee15af8e1eb992ccebb1d8345cdd8b861845cc01c04ea0f48b77b78324488673
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
$ docker pull odoo@sha256:78aabb75be977d0fbc2bdc60255f222b5a1d7dc0b3f0195a805970fb95f67b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657505774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7c05a2eb4e8f7aa3b0efaf02d37229150694a3bf8e88d6fad53d75525a6db5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=18.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63561abe36430920ae9c538575e9167c01d03e75b4ee22fad5c1a2c194e61647`  
		Last Modified: Tue, 29 Oct 2024 22:00:58 GMT  
		Size: 255.6 MB (255640718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8d3bb5f6d869319ec43b8ea55ac01f2d95484d8f9705589529275d9c0320ca`  
		Last Modified: Tue, 29 Oct 2024 22:00:55 GMT  
		Size: 14.1 MB (14142265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecb2f2b755b1e680a1663ec2195972828db4e5d0cfb32fefb628612300c7be8`  
		Last Modified: Tue, 29 Oct 2024 22:00:55 GMT  
		Size: 469.6 KB (469566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f1285f2b76a2ceab06719112c8bfca824850281b29549917c9a27beb1fb72d`  
		Last Modified: Tue, 29 Oct 2024 22:01:00 GMT  
		Size: 357.5 MB (357500423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b46636260a4b11c6d019e7fbaab1e835068772303f0443c9a54e57ca3055970`  
		Last Modified: Tue, 29 Oct 2024 22:00:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c404a0f3ae81df5de58c1387ba835bc2875c1b62a219af887c3547703c5548`  
		Last Modified: Tue, 29 Oct 2024 22:00:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ee78aec1fd70062c79a759c19d43d72bf0425cb2fa51937d6cbf00a996ed73`  
		Last Modified: Tue, 29 Oct 2024 22:00:57 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66816c6c9dcbcb05bbe8362b53d49c7414bf671bbdce7eee72b9b85a0032aec1`  
		Last Modified: Tue, 29 Oct 2024 22:00:57 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:eb3ba98c157ab13466e420954c0d167b829f596b36916b082d8e810cb1a0dc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56188283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed1036a494ae7bbdb4b5d136cf672a0b73cef771a78fbc0a417537a38487dc0`

```dockerfile
```

-	Layers:
	-	`sha256:7e96d7b27433cd80bbd10f3f20e7044039b5f3e7abc7519adca5b8bc3658386b`  
		Last Modified: Tue, 29 Oct 2024 22:00:55 GMT  
		Size: 56.2 MB (56161147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa9cb1649bddc1b3a0d398a0ee8eed6149b98b8ec533c17c10957d9bdd9135fb`  
		Last Modified: Tue, 29 Oct 2024 22:00:55 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:432ead532f1c9ee0e3d0a066735b5965156383fd0c8eec4f2a9669b09ca82823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.8 MB (653816874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f88c36958bba8bb6aeed093dcd5efee475108f4e8fe82a468dcbf1bf59d97e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=18.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8998091eb84f1c2fe96e4515e2d7d0bbf238c7a6a3daac3087a6de76df43bb6`  
		Last Modified: Tue, 29 Oct 2024 23:45:09 GMT  
		Size: 253.0 MB (252999384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066e920339d25f98363c69fa93c29502ab5e1f88a931acbc7adb8de85dd23f91`  
		Last Modified: Tue, 29 Oct 2024 23:45:02 GMT  
		Size: 14.1 MB (14115397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d48a21447981fca012489cc357bad5ad4681c58cf2d339752c795da2385023`  
		Last Modified: Tue, 29 Oct 2024 23:45:02 GMT  
		Size: 469.7 KB (469697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c409b6d782a8f341b6d4c2cd8b162702f9b20e777b6c529221264e788f661`  
		Last Modified: Tue, 29 Oct 2024 23:45:09 GMT  
		Size: 357.3 MB (357344112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbce5115d090f76131120a94b9fb8739d567040f067e017f07ed6280c4877a4`  
		Last Modified: Tue, 29 Oct 2024 23:45:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a73e19713601faa7fb044b275cba398f3b332aed69ddb9011a9259ffb7f80b1`  
		Last Modified: Tue, 29 Oct 2024 23:45:03 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c4969ff32461dfabfb35f6b1936f78b5d2299905a660392d1852bdaef88ba1`  
		Last Modified: Tue, 29 Oct 2024 23:45:04 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715f0f68122a224eb586bc24d21e80b16f58e7e02f60d1493a4ff1cc87b62c8e`  
		Last Modified: Tue, 29 Oct 2024 23:45:04 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:1c5f9e2c904637c6d6839e3a427ec7070bedef6cc074c367ee925e2b79e5fa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56195741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f0237bef0bdb2c958dde4f079be484a45e3c07d1b8fad741eccd03ff7bad93`

```dockerfile
```

-	Layers:
	-	`sha256:466262b724e5bf0c636d0e2eb8cdfc941a17a50e67c27b2520554af4b2de2904`  
		Last Modified: Tue, 29 Oct 2024 23:45:03 GMT  
		Size: 56.2 MB (56168441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f44067658da6ce385ce961a5be62fb7980b6329a6d92ddd70030a4280b86cb`  
		Last Modified: Tue, 29 Oct 2024 23:45:01 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:df395f570e512d430ace4cc217760252188b834958b17c693ed3b21874cc6029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.0 MB (674013287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b764d2a5531086d62f490de7713bb271350f293eaddf952fbcf702d43f668d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Tue, 29 Oct 2024 13:56:14 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Oct 2024 13:56:14 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV LANG=en_US.UTF-8
# Tue, 29 Oct 2024 13:56:14 GMT
ARG TARGETARCH
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_VERSION=18.0
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_RELEASE=20241029
# Tue, 29 Oct 2024 13:56:14 GMT
ARG ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241029 ODOO_SHA=6bb4a15aa9304ea8642940b232227b1a3e9ac266
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 29 Oct 2024 13:56:14 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 29 Oct 2024 13:56:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 29 Oct 2024 13:56:14 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 29 Oct 2024 13:56:14 GMT
USER odoo
# Tue, 29 Oct 2024 13:56:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Oct 2024 13:56:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2aaf46c089e715d1f81d86cc3df7c4516496efc1679739c02eda8573b510b75`  
		Last Modified: Tue, 29 Oct 2024 22:14:05 GMT  
		Size: 266.4 MB (266406087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07df2513d514cab4d4efc4141744d8556b72fe962571ffa0dc4c7c18959f1588`  
		Last Modified: Tue, 29 Oct 2024 22:13:50 GMT  
		Size: 14.7 MB (14686271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d7645b1528842fc361f95fa690e2dcfa1f7fdfaaabfe2bf3da69eab89e00d0`  
		Last Modified: Tue, 29 Oct 2024 22:13:49 GMT  
		Size: 469.6 KB (469571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef77b6067cbffcf4fec9d1fd8361053e10903a20641c3fd5d709c47f70cba22`  
		Last Modified: Tue, 29 Oct 2024 22:14:15 GMT  
		Size: 358.1 MB (358059948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9403e554ede662d23207a0eeb7b020b7a99303d5205bcf216bf8064475662642`  
		Last Modified: Tue, 29 Oct 2024 22:13:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d53424306db37ca8ca790dacfbf6fc319499f2093fcd6a5573845ab01bb41dd`  
		Last Modified: Tue, 29 Oct 2024 22:13:52 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a141d3ad04adf215c1d0ef2e908b185cb965d9eb8cec6eae7fb2ecd65c7e041d`  
		Last Modified: Tue, 29 Oct 2024 22:13:52 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5edc774a76ad91872839c754694c70a624eb9bf383ee7fe1f8683b182b0223`  
		Last Modified: Tue, 29 Oct 2024 22:13:53 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:2dd977eae714a81b2a20454e84fb20013851635645c548b32bcd38025ac2ba71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56196488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a444bbff564e9ee4caebb64649e7ce24c14ac867e7bd912939461e2e82017b8f`

```dockerfile
```

-	Layers:
	-	`sha256:81186d3a2abb2a2b5e7791a6f652ad77e30028f77ee7ed29b597e2a4976f9459`  
		Last Modified: Tue, 29 Oct 2024 22:13:52 GMT  
		Size: 56.2 MB (56169290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6813723ec5a4d5f24ecbdddbd61d181052da30d71bb599f3a38d39f1f6757c32`  
		Last Modified: Tue, 29 Oct 2024 22:13:49 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
