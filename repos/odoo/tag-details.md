<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260217`](#odoo170-20260217)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260217`](#odoo180-20260217)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260217`](#odoo190-20260217)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:794b0b37ec542d8913f520b131ce28468b02c1b6226f4b4cb44005442805ad26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:3eee30600db1d86dadeafe0d5aef9a7dd6609e27f65b5c694884ca26c1157d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.2 MB (611186884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d04d61161c909099ed662bec758d445a1b4b5783f63cf1de724d10b415382a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:56:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:56:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:56:03 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:56:03 GMT
ARG TARGETARCH=amd64
# Mon, 09 Feb 2026 19:56:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:56:10 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:56:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:56:11 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Feb 2026 19:56:11 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:56:11 GMT
ARG ODOO_SHA=85d9a4cee5bb0b500a9c8ea440ad731132deef36
# Mon, 09 Feb 2026 19:57:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=85d9a4cee5bb0b500a9c8ea440ad731132deef36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:57:11 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:57:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:57:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=85d9a4cee5bb0b500a9c8ea440ad731132deef36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:57:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:57:11 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:57:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:57:11 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:57:11 GMT
USER odoo
# Mon, 09 Feb 2026 19:57:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:57:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74673ada0a426239c35b369d058ef07586e47faf632ba1501e16d1e20d04747`  
		Last Modified: Mon, 09 Feb 2026 19:58:28 GMT  
		Size: 236.1 MB (236101165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e808234b1498e9d32d17e0e56fdc190de28ed89870baea81f0e0b11f9ff0484`  
		Last Modified: Mon, 09 Feb 2026 19:58:19 GMT  
		Size: 2.6 MB (2597377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cddc83afc298e1222ef9416879b8226802dea19271643c108c97c3f295117ef`  
		Last Modified: Mon, 09 Feb 2026 19:58:19 GMT  
		Size: 480.3 KB (480316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4842a4d3465714f53f704d31d6563b2bd3d77e9846315eb91f06ac0b51c0d792`  
		Last Modified: Mon, 09 Feb 2026 19:58:29 GMT  
		Size: 342.5 MB (342468920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488c86bde99ac15f4ebfc2ec5e9034b5005cadec0facf165384750847d2fd9ce`  
		Last Modified: Mon, 09 Feb 2026 19:58:20 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f35dafb4cd4158cc6f8e6c2f2c7ab5579690c6d111ce5bbd59ba5f448dcd6a1`  
		Last Modified: Mon, 09 Feb 2026 19:58:21 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318405d9dcaf104575b0775862709abf0d1d92ca8929776016aa310ce27335a8`  
		Last Modified: Mon, 09 Feb 2026 19:58:21 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b5dcc310287f7d0ca4390c9f735b43ef600cc7acdc224cffdf896396655ad`  
		Last Modified: Mon, 09 Feb 2026 19:58:22 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:d28b9b7f8d0253fceed533059179d54ab7ee6076edf4eb187c35f40cd40f82eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41990643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cc8eb043d08f47e0de09f0d6573de0aadaf0429c419a551c8fd1959e9ab2f2`

```dockerfile
```

-	Layers:
	-	`sha256:38ad442b2eb0e482bd9dcf2915d3fa7e5300494a2dc4d478a3479ddb9ad549db`  
		Last Modified: Mon, 09 Feb 2026 19:58:21 GMT  
		Size: 42.0 MB (41963851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d92b5a096b0d22a8d8b772fb3d2f49a2dd5982228092e6c9b97d85910c85f72a`  
		Last Modified: Mon, 09 Feb 2026 19:58:19 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:032bae1e4f003688c346f664fcecd033689bfe30744cb6b1a3aaac878fc87245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.9 MB (605889904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7746b7d7ad5b744d9f7961b09a8a87fc86d626a27e7ac7ab4a5f787bb1489989`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:55:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:55:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:55:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:55:43 GMT
ARG TARGETARCH=arm64
# Mon, 09 Feb 2026 19:55:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:55:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:55:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:55:51 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Feb 2026 19:55:51 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:55:51 GMT
ARG ODOO_SHA=85d9a4cee5bb0b500a9c8ea440ad731132deef36
# Mon, 09 Feb 2026 19:56:53 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=85d9a4cee5bb0b500a9c8ea440ad731132deef36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:56:53 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:56:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:56:53 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=85d9a4cee5bb0b500a9c8ea440ad731132deef36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:56:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:56:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:56:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:56:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:56:53 GMT
USER odoo
# Mon, 09 Feb 2026 19:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:56:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0cc8b89293c1dd30213c28e4dac09778d1e993082527ffdc5686b9d46f266e`  
		Last Modified: Mon, 09 Feb 2026 19:58:23 GMT  
		Size: 233.3 MB (233341303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28940497bf3d465fd6fcbf29bd55cf5c6ab17ef7ca5fafc96889ba09eede35ab`  
		Last Modified: Mon, 09 Feb 2026 19:58:10 GMT  
		Size: 2.6 MB (2592561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9156a05280718d11fe02486bddb831d0137b99b936ae88f0d07258d76ac842e5`  
		Last Modified: Mon, 09 Feb 2026 19:58:10 GMT  
		Size: 480.2 KB (480250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf9fa5cda61c53af067ebe2c323c622bd15f6bff1946b2d50e640353f0ab3ad`  
		Last Modified: Mon, 09 Feb 2026 19:58:20 GMT  
		Size: 342.1 MB (342089855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11a4843caaf61bb0a59fd0030c2e1f12c88851c5d3acd12218b387a73535de3`  
		Last Modified: Mon, 09 Feb 2026 19:58:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4345a726bdfd9d20a77bd8058d3dd6d59a8f3104c9253ebddde51853bcf6cf29`  
		Last Modified: Mon, 09 Feb 2026 19:58:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563ddf84e6e779db1507725723e5c0220e94a39db136a4c38d827476a7fd675a`  
		Last Modified: Mon, 09 Feb 2026 19:58:12 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32f26e32c1da72a587ec486e9d65672311b9470d96a6d9e91b3cccaea71c179`  
		Last Modified: Mon, 09 Feb 2026 19:58:12 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:4bdb6654c8a177e46ae3267241c94c86ea1e4c81345d792c7061e1834498ddfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41997301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00949fd695dfab22b4e65dc4aab52e88bafeaedb0a90640d6f91550df4818a0f`

```dockerfile
```

-	Layers:
	-	`sha256:124921ce1ad7a4ac581bcf15a2b93c04879242bc6ea8e52651e02dc9325d359d`  
		Last Modified: Mon, 09 Feb 2026 19:58:12 GMT  
		Size: 42.0 MB (41970358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3de16b58e4b5a46aa3028d2c7e38de26a5136a1ef00f02b157c6170cd2ddbd5e`  
		Last Modified: Mon, 09 Feb 2026 19:58:09 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:794b0b37ec542d8913f520b131ce28468b02c1b6226f4b4cb44005442805ad26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:3eee30600db1d86dadeafe0d5aef9a7dd6609e27f65b5c694884ca26c1157d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.2 MB (611186884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d04d61161c909099ed662bec758d445a1b4b5783f63cf1de724d10b415382a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:56:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:56:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:56:03 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:56:03 GMT
ARG TARGETARCH=amd64
# Mon, 09 Feb 2026 19:56:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:56:10 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:56:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:56:11 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Feb 2026 19:56:11 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:56:11 GMT
ARG ODOO_SHA=85d9a4cee5bb0b500a9c8ea440ad731132deef36
# Mon, 09 Feb 2026 19:57:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=85d9a4cee5bb0b500a9c8ea440ad731132deef36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:57:11 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:57:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:57:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=85d9a4cee5bb0b500a9c8ea440ad731132deef36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:57:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:57:11 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:57:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:57:11 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:57:11 GMT
USER odoo
# Mon, 09 Feb 2026 19:57:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:57:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74673ada0a426239c35b369d058ef07586e47faf632ba1501e16d1e20d04747`  
		Last Modified: Mon, 09 Feb 2026 19:58:28 GMT  
		Size: 236.1 MB (236101165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e808234b1498e9d32d17e0e56fdc190de28ed89870baea81f0e0b11f9ff0484`  
		Last Modified: Mon, 09 Feb 2026 19:58:19 GMT  
		Size: 2.6 MB (2597377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cddc83afc298e1222ef9416879b8226802dea19271643c108c97c3f295117ef`  
		Last Modified: Mon, 09 Feb 2026 19:58:19 GMT  
		Size: 480.3 KB (480316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4842a4d3465714f53f704d31d6563b2bd3d77e9846315eb91f06ac0b51c0d792`  
		Last Modified: Mon, 09 Feb 2026 19:58:29 GMT  
		Size: 342.5 MB (342468920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488c86bde99ac15f4ebfc2ec5e9034b5005cadec0facf165384750847d2fd9ce`  
		Last Modified: Mon, 09 Feb 2026 19:58:20 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f35dafb4cd4158cc6f8e6c2f2c7ab5579690c6d111ce5bbd59ba5f448dcd6a1`  
		Last Modified: Mon, 09 Feb 2026 19:58:21 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318405d9dcaf104575b0775862709abf0d1d92ca8929776016aa310ce27335a8`  
		Last Modified: Mon, 09 Feb 2026 19:58:21 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b5dcc310287f7d0ca4390c9f735b43ef600cc7acdc224cffdf896396655ad`  
		Last Modified: Mon, 09 Feb 2026 19:58:22 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d28b9b7f8d0253fceed533059179d54ab7ee6076edf4eb187c35f40cd40f82eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41990643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cc8eb043d08f47e0de09f0d6573de0aadaf0429c419a551c8fd1959e9ab2f2`

```dockerfile
```

-	Layers:
	-	`sha256:38ad442b2eb0e482bd9dcf2915d3fa7e5300494a2dc4d478a3479ddb9ad549db`  
		Last Modified: Mon, 09 Feb 2026 19:58:21 GMT  
		Size: 42.0 MB (41963851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d92b5a096b0d22a8d8b772fb3d2f49a2dd5982228092e6c9b97d85910c85f72a`  
		Last Modified: Mon, 09 Feb 2026 19:58:19 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:032bae1e4f003688c346f664fcecd033689bfe30744cb6b1a3aaac878fc87245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.9 MB (605889904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7746b7d7ad5b744d9f7961b09a8a87fc86d626a27e7ac7ab4a5f787bb1489989`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:55:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:55:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:55:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:55:43 GMT
ARG TARGETARCH=arm64
# Mon, 09 Feb 2026 19:55:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:55:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:55:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:55:51 GMT
ENV ODOO_VERSION=17.0
# Mon, 09 Feb 2026 19:55:51 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:55:51 GMT
ARG ODOO_SHA=85d9a4cee5bb0b500a9c8ea440ad731132deef36
# Mon, 09 Feb 2026 19:56:53 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=85d9a4cee5bb0b500a9c8ea440ad731132deef36
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:56:53 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:56:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:56:53 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=85d9a4cee5bb0b500a9c8ea440ad731132deef36
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:56:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:56:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:56:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:56:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:56:53 GMT
USER odoo
# Mon, 09 Feb 2026 19:56:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:56:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0cc8b89293c1dd30213c28e4dac09778d1e993082527ffdc5686b9d46f266e`  
		Last Modified: Mon, 09 Feb 2026 19:58:23 GMT  
		Size: 233.3 MB (233341303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28940497bf3d465fd6fcbf29bd55cf5c6ab17ef7ca5fafc96889ba09eede35ab`  
		Last Modified: Mon, 09 Feb 2026 19:58:10 GMT  
		Size: 2.6 MB (2592561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9156a05280718d11fe02486bddb831d0137b99b936ae88f0d07258d76ac842e5`  
		Last Modified: Mon, 09 Feb 2026 19:58:10 GMT  
		Size: 480.2 KB (480250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf9fa5cda61c53af067ebe2c323c622bd15f6bff1946b2d50e640353f0ab3ad`  
		Last Modified: Mon, 09 Feb 2026 19:58:20 GMT  
		Size: 342.1 MB (342089855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11a4843caaf61bb0a59fd0030c2e1f12c88851c5d3acd12218b387a73535de3`  
		Last Modified: Mon, 09 Feb 2026 19:58:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4345a726bdfd9d20a77bd8058d3dd6d59a8f3104c9253ebddde51853bcf6cf29`  
		Last Modified: Mon, 09 Feb 2026 19:58:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563ddf84e6e779db1507725723e5c0220e94a39db136a4c38d827476a7fd675a`  
		Last Modified: Mon, 09 Feb 2026 19:58:12 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32f26e32c1da72a587ec486e9d65672311b9470d96a6d9e91b3cccaea71c179`  
		Last Modified: Mon, 09 Feb 2026 19:58:12 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4bdb6654c8a177e46ae3267241c94c86ea1e4c81345d792c7061e1834498ddfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41997301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00949fd695dfab22b4e65dc4aab52e88bafeaedb0a90640d6f91550df4818a0f`

```dockerfile
```

-	Layers:
	-	`sha256:124921ce1ad7a4ac581bcf15a2b93c04879242bc6ea8e52651e02dc9325d359d`  
		Last Modified: Mon, 09 Feb 2026 19:58:12 GMT  
		Size: 42.0 MB (41970358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3de16b58e4b5a46aa3028d2c7e38de26a5136a1ef00f02b157c6170cd2ddbd5e`  
		Last Modified: Mon, 09 Feb 2026 19:58:09 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260217`

**does not exist** (yet?)

## `odoo:18`

```console
$ docker pull odoo@sha256:78dde7ea7ce3aa87f4dc8133c5da2b6c1b9994a43c49a7a2857a56c66406a8b9
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
$ docker pull odoo@sha256:1139a5a5f07531a00dd6b7dbaac81bb6232a279afda1ef010a13cc00c84dca9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.7 MB (684743144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34341223607b1e77e5e37e6837c482c13a99eeb255f411fd24a702aec96a401f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:56:59 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:56:59 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:56:59 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:56:59 GMT
ARG TARGETARCH=amd64
# Mon, 09 Feb 2026 19:56:59 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Feb 2026 19:57:09 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:57:09 GMT
ARG ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
# Mon, 09 Feb 2026 19:58:05 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:58:06 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:58:06 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:58:06 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:58:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:58:06 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:58:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:58:06 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:58:06 GMT
USER odoo
# Mon, 09 Feb 2026 19:58:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:58:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb3eb599c6f15838ba29d7f6e71276428cfd1b82ab490751569bf845437dd08`  
		Last Modified: Mon, 09 Feb 2026 20:00:01 GMT  
		Size: 257.0 MB (256965635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b7fe2a52458c7a932244e72f75b79ea2fb4fb612855415762f963e339647e9`  
		Last Modified: Mon, 09 Feb 2026 19:59:53 GMT  
		Size: 14.4 MB (14356805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a191b5dc5c35dc44caba690ab95d5e2e7b4c2363e4da481fbb1cf8ed1f224e`  
		Last Modified: Mon, 09 Feb 2026 19:59:52 GMT  
		Size: 480.0 KB (480009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ba8b956f47c0af5c836d937772c2542b593db49b37643068809c1edcdff130`  
		Last Modified: Mon, 09 Feb 2026 20:00:04 GMT  
		Size: 383.2 MB (383212242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345daf9a4d3921d73ee80687be69e573c246cddf82714d9fb0e2b6332747fe53`  
		Last Modified: Mon, 09 Feb 2026 19:59:53 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aeafb0f9dd3bfe7f27c84e782ae334549a93c2e0b1251913f332bebbe902e8`  
		Last Modified: Mon, 09 Feb 2026 19:59:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f726aafa079b7233e2c25f3fc7097261979307441e71f511d0c4128b3499158f`  
		Last Modified: Mon, 09 Feb 2026 19:59:55 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d4d05d36ca428368ac5895b44c4767c0c78a51340c7f32f18842d3c2a795ca`  
		Last Modified: Mon, 09 Feb 2026 19:59:56 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:5ea3bd2e68befb695d1b07c7b0c1e14411bdad65db7367dc7615e5b523be1931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61636642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f3769d4b08de557b8472560a676389ee12e92561808b709bd98ac9bb20b42c`

```dockerfile
```

-	Layers:
	-	`sha256:b060391de139fea765bd51a7680d332d561fff9d671ba52a03a5d9d4ad6f1ecf`  
		Last Modified: Mon, 09 Feb 2026 19:59:56 GMT  
		Size: 61.6 MB (61609843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8086b6bb3617cf3b1db65819d715be2a69b60d2ee42268f4ab2a4bc8ff69f83`  
		Last Modified: Mon, 09 Feb 2026 19:59:52 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:32ef0e228acc5ae27234ad27cc5a843fc950292fb7872fef43caf93681679072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.9 MB (680908467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8a2318db3332a21f3d573ed783ff72709e3bf72d934e0a836e90de9b77b223`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:56:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:56:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:56:01 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:56:01 GMT
ARG TARGETARCH=arm64
# Mon, 09 Feb 2026 19:56:01 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:56:10 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:56:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:56:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Feb 2026 19:56:12 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:56:12 GMT
ARG ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
# Mon, 09 Feb 2026 19:57:09 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:57:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:57:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:57:09 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
USER odoo
# Mon, 09 Feb 2026 19:57:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:57:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ec8fd0ceb3ed748781ccce161e63153534458f91aa49e7a56fc172912b2c60`  
		Last Modified: Mon, 09 Feb 2026 19:59:35 GMT  
		Size: 254.2 MB (254183436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9068f4fec96aa4ac307e3cbd59f0a59cbe2608fc46cc6a3f07de16c5ce13d69`  
		Last Modified: Mon, 09 Feb 2026 19:59:13 GMT  
		Size: 14.3 MB (14334533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0ca558957cf6e23cc505a96ec3af01b980393fa3b8529a8ee72b3fe06a37ea`  
		Last Modified: Mon, 09 Feb 2026 19:59:12 GMT  
		Size: 480.0 KB (480027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd446edf299d41cf55563a6bb13da0e34f94fc11e0bd7f1930d399482bcc13d`  
		Last Modified: Mon, 09 Feb 2026 19:59:42 GMT  
		Size: 383.0 MB (383044210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e98ae45d01f2522fc5fa1a2b1ea23a4e6859b8e6273aace01b4379ec4415e66`  
		Last Modified: Mon, 09 Feb 2026 19:59:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e6872f008300d327e6f61e9d746b97c240d672cd5d5182a330872c4454025f`  
		Last Modified: Mon, 09 Feb 2026 19:59:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7afcc22e5650cae1b0b66ad38113f7b461f2138e033f259db0b926af75e522`  
		Last Modified: Mon, 09 Feb 2026 19:59:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4438259077244979e9f740e1966a652040596526d12cb51b4fcd8a907dba9130`  
		Last Modified: Mon, 09 Feb 2026 19:59:16 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:ec5c534306f314d165cbf06f365507d116f9e013c3a4dc54ba6419b14582db82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61644069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d945a40f4f4880239f0534e873e171d6ce1972438f1df62fab2199de58f451f`

```dockerfile
```

-	Layers:
	-	`sha256:3e939d667be6841c88a51729b4bf662db0886af292761daad6ff6c6defe821a1`  
		Last Modified: Mon, 09 Feb 2026 19:59:16 GMT  
		Size: 61.6 MB (61617118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d38ef89e6a4213d196f4e36553ed88d8f2c4023690700f6a455806998fd6e9f`  
		Last Modified: Mon, 09 Feb 2026 19:59:12 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:a5febb23dd00d4bcbd62657f4a186ac1a32a0c5e72c50cbe0c708843729692c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.2 MB (701173747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc8d8e7e8891c3e65ec92590e1c0b7fd6ff4e8e0204991eed4063c8b36e36f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:09:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 20:09:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 20:09:16 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 20:09:16 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Feb 2026 20:09:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 20:09:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:09:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 20:09:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Feb 2026 20:09:35 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 20:09:35 GMT
ARG ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
# Mon, 09 Feb 2026 20:12:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260209 ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 20:12:18 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 20:12:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 20:12:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260209 ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 20:12:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 20:12:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 20:12:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 20:12:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 20:12:22 GMT
USER odoo
# Mon, 09 Feb 2026 20:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 20:12:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309753fe35993f50ae1ca136b51196727dd6fcc555b07a7cce2890c409b6ae88`  
		Last Modified: Mon, 09 Feb 2026 20:17:29 GMT  
		Size: 267.8 MB (267750703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8869d3600823a629f0763702a58282df312db9e67edefe76e118d263414a5c94`  
		Last Modified: Mon, 09 Feb 2026 20:17:17 GMT  
		Size: 14.9 MB (14885554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad87469235b6d4e4b157fd9a560a908d19fcbdb06e2aa5155949240ce865092c`  
		Last Modified: Mon, 09 Feb 2026 20:17:16 GMT  
		Size: 480.1 KB (480103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82707fedee9ccbf556f79a7f6c2ee6a8d5b68d55d9fb578fd97ea4a936711285`  
		Last Modified: Mon, 09 Feb 2026 20:17:31 GMT  
		Size: 383.7 MB (383748785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c3aca6d5e3c75ba8af6e816af621bb97767798d06c73163b08b7bb0316e0bd`  
		Last Modified: Mon, 09 Feb 2026 20:17:17 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040da135e0552413460beebab24f37da90042050ca4c8043d76c98efe7086431`  
		Last Modified: Mon, 09 Feb 2026 20:17:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3bc19ffc2349474d1aa043da9a2f56ecc66558922057ed569f4cf4ffced8e9`  
		Last Modified: Mon, 09 Feb 2026 20:17:19 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26433b511614aefc78cbd5aa8c2e3e1bd63fcaa0bd255cf2ec20f19c813f1470`  
		Last Modified: Mon, 09 Feb 2026 20:17:20 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:c9df68c1929fde54b3f6215cf152fc8160b737e5c6bf3734b663a553eb4942b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61645081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cff085d9da8b80470c5eb45cf2b55cef5a9782adf2a4550a87e5cce19c54c16`

```dockerfile
```

-	Layers:
	-	`sha256:ccd8d7af11caa2420d01cb718b9865868de98f6a72edd38aa5afba797833ee00`  
		Last Modified: Mon, 09 Feb 2026 20:17:21 GMT  
		Size: 61.6 MB (61618226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8a4b04e8bea8e327ce33e8091917d503105238e0afbc5ce95ab08423be73a0`  
		Last Modified: Mon, 09 Feb 2026 20:17:16 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:78dde7ea7ce3aa87f4dc8133c5da2b6c1b9994a43c49a7a2857a56c66406a8b9
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
$ docker pull odoo@sha256:1139a5a5f07531a00dd6b7dbaac81bb6232a279afda1ef010a13cc00c84dca9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.7 MB (684743144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34341223607b1e77e5e37e6837c482c13a99eeb255f411fd24a702aec96a401f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:56:59 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:56:59 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:56:59 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:56:59 GMT
ARG TARGETARCH=amd64
# Mon, 09 Feb 2026 19:56:59 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Feb 2026 19:57:09 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:57:09 GMT
ARG ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
# Mon, 09 Feb 2026 19:58:05 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:58:06 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:58:06 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:58:06 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:58:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:58:06 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:58:06 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:58:06 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:58:06 GMT
USER odoo
# Mon, 09 Feb 2026 19:58:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:58:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb3eb599c6f15838ba29d7f6e71276428cfd1b82ab490751569bf845437dd08`  
		Last Modified: Mon, 09 Feb 2026 20:00:01 GMT  
		Size: 257.0 MB (256965635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b7fe2a52458c7a932244e72f75b79ea2fb4fb612855415762f963e339647e9`  
		Last Modified: Mon, 09 Feb 2026 19:59:53 GMT  
		Size: 14.4 MB (14356805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a191b5dc5c35dc44caba690ab95d5e2e7b4c2363e4da481fbb1cf8ed1f224e`  
		Last Modified: Mon, 09 Feb 2026 19:59:52 GMT  
		Size: 480.0 KB (480009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ba8b956f47c0af5c836d937772c2542b593db49b37643068809c1edcdff130`  
		Last Modified: Mon, 09 Feb 2026 20:00:04 GMT  
		Size: 383.2 MB (383212242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345daf9a4d3921d73ee80687be69e573c246cddf82714d9fb0e2b6332747fe53`  
		Last Modified: Mon, 09 Feb 2026 19:59:53 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aeafb0f9dd3bfe7f27c84e782ae334549a93c2e0b1251913f332bebbe902e8`  
		Last Modified: Mon, 09 Feb 2026 19:59:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f726aafa079b7233e2c25f3fc7097261979307441e71f511d0c4128b3499158f`  
		Last Modified: Mon, 09 Feb 2026 19:59:55 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d4d05d36ca428368ac5895b44c4767c0c78a51340c7f32f18842d3c2a795ca`  
		Last Modified: Mon, 09 Feb 2026 19:59:56 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:5ea3bd2e68befb695d1b07c7b0c1e14411bdad65db7367dc7615e5b523be1931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61636642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f3769d4b08de557b8472560a676389ee12e92561808b709bd98ac9bb20b42c`

```dockerfile
```

-	Layers:
	-	`sha256:b060391de139fea765bd51a7680d332d561fff9d671ba52a03a5d9d4ad6f1ecf`  
		Last Modified: Mon, 09 Feb 2026 19:59:56 GMT  
		Size: 61.6 MB (61609843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8086b6bb3617cf3b1db65819d715be2a69b60d2ee42268f4ab2a4bc8ff69f83`  
		Last Modified: Mon, 09 Feb 2026 19:59:52 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:32ef0e228acc5ae27234ad27cc5a843fc950292fb7872fef43caf93681679072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.9 MB (680908467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8a2318db3332a21f3d573ed783ff72709e3bf72d934e0a836e90de9b77b223`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:56:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:56:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:56:01 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:56:01 GMT
ARG TARGETARCH=arm64
# Mon, 09 Feb 2026 19:56:01 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:56:10 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:56:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:56:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Feb 2026 19:56:12 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:56:12 GMT
ARG ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
# Mon, 09 Feb 2026 19:57:09 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:57:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:57:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:57:09 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:57:09 GMT
USER odoo
# Mon, 09 Feb 2026 19:57:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:57:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ec8fd0ceb3ed748781ccce161e63153534458f91aa49e7a56fc172912b2c60`  
		Last Modified: Mon, 09 Feb 2026 19:59:35 GMT  
		Size: 254.2 MB (254183436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9068f4fec96aa4ac307e3cbd59f0a59cbe2608fc46cc6a3f07de16c5ce13d69`  
		Last Modified: Mon, 09 Feb 2026 19:59:13 GMT  
		Size: 14.3 MB (14334533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0ca558957cf6e23cc505a96ec3af01b980393fa3b8529a8ee72b3fe06a37ea`  
		Last Modified: Mon, 09 Feb 2026 19:59:12 GMT  
		Size: 480.0 KB (480027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd446edf299d41cf55563a6bb13da0e34f94fc11e0bd7f1930d399482bcc13d`  
		Last Modified: Mon, 09 Feb 2026 19:59:42 GMT  
		Size: 383.0 MB (383044210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e98ae45d01f2522fc5fa1a2b1ea23a4e6859b8e6273aace01b4379ec4415e66`  
		Last Modified: Mon, 09 Feb 2026 19:59:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e6872f008300d327e6f61e9d746b97c240d672cd5d5182a330872c4454025f`  
		Last Modified: Mon, 09 Feb 2026 19:59:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7afcc22e5650cae1b0b66ad38113f7b461f2138e033f259db0b926af75e522`  
		Last Modified: Mon, 09 Feb 2026 19:59:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4438259077244979e9f740e1966a652040596526d12cb51b4fcd8a907dba9130`  
		Last Modified: Mon, 09 Feb 2026 19:59:16 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:ec5c534306f314d165cbf06f365507d116f9e013c3a4dc54ba6419b14582db82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61644069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d945a40f4f4880239f0534e873e171d6ce1972438f1df62fab2199de58f451f`

```dockerfile
```

-	Layers:
	-	`sha256:3e939d667be6841c88a51729b4bf662db0886af292761daad6ff6c6defe821a1`  
		Last Modified: Mon, 09 Feb 2026 19:59:16 GMT  
		Size: 61.6 MB (61617118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d38ef89e6a4213d196f4e36553ed88d8f2c4023690700f6a455806998fd6e9f`  
		Last Modified: Mon, 09 Feb 2026 19:59:12 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:a5febb23dd00d4bcbd62657f4a186ac1a32a0c5e72c50cbe0c708843729692c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.2 MB (701173747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc8d8e7e8891c3e65ec92590e1c0b7fd6ff4e8e0204991eed4063c8b36e36f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:09:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 20:09:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 20:09:16 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 20:09:16 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Feb 2026 20:09:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 20:09:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:09:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 20:09:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 09 Feb 2026 20:09:35 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 20:09:35 GMT
ARG ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
# Mon, 09 Feb 2026 20:12:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260209 ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 20:12:18 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 20:12:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 20:12:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260209 ODOO_SHA=791ed4bab149a07c756b5188f69f600b40cefd46
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 20:12:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 20:12:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 20:12:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 20:12:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 20:12:22 GMT
USER odoo
# Mon, 09 Feb 2026 20:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 20:12:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309753fe35993f50ae1ca136b51196727dd6fcc555b07a7cce2890c409b6ae88`  
		Last Modified: Mon, 09 Feb 2026 20:17:29 GMT  
		Size: 267.8 MB (267750703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8869d3600823a629f0763702a58282df312db9e67edefe76e118d263414a5c94`  
		Last Modified: Mon, 09 Feb 2026 20:17:17 GMT  
		Size: 14.9 MB (14885554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad87469235b6d4e4b157fd9a560a908d19fcbdb06e2aa5155949240ce865092c`  
		Last Modified: Mon, 09 Feb 2026 20:17:16 GMT  
		Size: 480.1 KB (480103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82707fedee9ccbf556f79a7f6c2ee6a8d5b68d55d9fb578fd97ea4a936711285`  
		Last Modified: Mon, 09 Feb 2026 20:17:31 GMT  
		Size: 383.7 MB (383748785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c3aca6d5e3c75ba8af6e816af621bb97767798d06c73163b08b7bb0316e0bd`  
		Last Modified: Mon, 09 Feb 2026 20:17:17 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040da135e0552413460beebab24f37da90042050ca4c8043d76c98efe7086431`  
		Last Modified: Mon, 09 Feb 2026 20:17:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3bc19ffc2349474d1aa043da9a2f56ecc66558922057ed569f4cf4ffced8e9`  
		Last Modified: Mon, 09 Feb 2026 20:17:19 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26433b511614aefc78cbd5aa8c2e3e1bd63fcaa0bd255cf2ec20f19c813f1470`  
		Last Modified: Mon, 09 Feb 2026 20:17:20 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c9df68c1929fde54b3f6215cf152fc8160b737e5c6bf3734b663a553eb4942b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61645081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cff085d9da8b80470c5eb45cf2b55cef5a9782adf2a4550a87e5cce19c54c16`

```dockerfile
```

-	Layers:
	-	`sha256:ccd8d7af11caa2420d01cb718b9865868de98f6a72edd38aa5afba797833ee00`  
		Last Modified: Mon, 09 Feb 2026 20:17:21 GMT  
		Size: 61.6 MB (61618226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8a4b04e8bea8e327ce33e8091917d503105238e0afbc5ce95ab08423be73a0`  
		Last Modified: Mon, 09 Feb 2026 20:17:16 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260217`

**does not exist** (yet?)

## `odoo:19`

```console
$ docker pull odoo@sha256:bcf73ede5625b473024862e055247e2172701b70553e9c0725101f7b12546af3
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
$ docker pull odoo@sha256:f7d987696b508501fdc3d381a0ccf0c52444a2e6e556474d2c17eab73789630a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.3 MB (700293836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3393af1bc362d71d1d7680ccfaf9d6c289a411cbe788e55f6ef13464eaf5b634`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:56:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:56:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:56:55 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:56:55 GMT
ARG TARGETARCH=amd64
# Mon, 09 Feb 2026 19:56:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:57:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:57:05 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:57:05 GMT
ENV ODOO_VERSION=19.0
# Mon, 09 Feb 2026 19:57:05 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:57:05 GMT
ARG ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
# Mon, 09 Feb 2026 19:58:08 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:58:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:58:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:58:09 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
USER odoo
# Mon, 09 Feb 2026 19:58:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:58:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec7d2f393023c8d47fc7fc8dfbb08513f89551d289f7b4a785d69cdd7a12562`  
		Last Modified: Mon, 09 Feb 2026 20:00:28 GMT  
		Size: 257.0 MB (256965528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2836245bd2f95f29af22c2e06ab84fe3458b4403fec2e9720657e3c411b02aa7`  
		Last Modified: Mon, 09 Feb 2026 20:00:19 GMT  
		Size: 14.4 MB (14356868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22260229f8546eeed152c530b0cc61b5addd22637914fe5e75872d329adb6b11`  
		Last Modified: Mon, 09 Feb 2026 20:00:20 GMT  
		Size: 480.0 KB (480018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e37bcfab968f994d1585aa3324712c5b7d8afcd705ac75f5106a7bb8d2f6b9`  
		Last Modified: Mon, 09 Feb 2026 20:00:31 GMT  
		Size: 398.8 MB (398762970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345daf9a4d3921d73ee80687be69e573c246cddf82714d9fb0e2b6332747fe53`  
		Last Modified: Mon, 09 Feb 2026 19:59:53 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917ba9419a22df211490f683e76f115fdccdbcf84fb5832c31154192533090a4`  
		Last Modified: Mon, 09 Feb 2026 20:00:25 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a88d0100f22822999d96b572e093222869f3f6a30e5ab43b55aecd6b0789a75`  
		Last Modified: Mon, 09 Feb 2026 20:00:23 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8926765bd0fe3659e76bb30bef41068700ae06e0b62e2e911bdfdb44145c0405`  
		Last Modified: Mon, 09 Feb 2026 20:00:25 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:fffa1db1bb40e8e29aaba9d5779b56a31d420011bf857a498d015768faade245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69645340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987c6e9ddebf1097835adce06f6d8d20006e88a9584e01897373066fe81fc557`

```dockerfile
```

-	Layers:
	-	`sha256:05979d955e2dfac59d07ecb8ae00a300160c0dfe0ac77c4608658fad7cec371e`  
		Last Modified: Mon, 09 Feb 2026 20:00:23 GMT  
		Size: 69.6 MB (69618247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5939f6c0882d38cce3539cedca5930a96a06a64813e2f33e0bef88ae77367e44`  
		Last Modified: Mon, 09 Feb 2026 20:00:19 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b339dae8d638cd34570947c8e1aab5202dc86008766631b4acf4c2ea2f5bcd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.5 MB (696459479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad49ed2e141f820bb565f0f38a1584b3672f732f990067a131476300dff526f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:55:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:55:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:55:58 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:55:58 GMT
ARG TARGETARCH=arm64
# Mon, 09 Feb 2026 19:55:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:56:09 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:56:10 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:56:10 GMT
ENV ODOO_VERSION=19.0
# Mon, 09 Feb 2026 19:56:10 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:56:10 GMT
ARG ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
# Mon, 09 Feb 2026 19:57:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:57:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:57:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:57:15 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:57:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:57:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:57:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:57:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:57:15 GMT
USER odoo
# Mon, 09 Feb 2026 19:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:57:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f5d6664d6a5c9795c9d514cf35fc214711e2152f8ba79a763890c5708fc95e`  
		Last Modified: Mon, 09 Feb 2026 20:00:08 GMT  
		Size: 254.2 MB (254183363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e7ce57e304c1337a29b440be387ac917c5af7767a356c2fff7067ffcac9ec7`  
		Last Modified: Mon, 09 Feb 2026 19:59:59 GMT  
		Size: 14.3 MB (14334632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfbfb903b36e2dfa1a14a11d1ff9fa952f3c3cfb54484fe0319ad78bb46344c`  
		Last Modified: Mon, 09 Feb 2026 19:59:58 GMT  
		Size: 480.1 KB (480082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b588d32cfe5a2cf2979215040091176629fbc4c0f94bae1313e299cb1901cab7`  
		Last Modified: Mon, 09 Feb 2026 20:00:17 GMT  
		Size: 398.6 MB (398595138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e98ae45d01f2522fc5fa1a2b1ea23a4e6859b8e6273aace01b4379ec4415e66`  
		Last Modified: Mon, 09 Feb 2026 19:59:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f185c9023ed275cb5c9c0e9abda5b77359a4d51f76b72612646d298361a57731`  
		Last Modified: Mon, 09 Feb 2026 19:59:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6434875651c3bbf667e88e105eb388c2188f0c53f32b08f94dc581351744d3`  
		Last Modified: Mon, 09 Feb 2026 20:00:00 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a48cfc7b5eff2436b4800acb5929fc36a508ad65fdb519041c8b1c40925d8`  
		Last Modified: Mon, 09 Feb 2026 20:00:01 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:151964dd22130ac1f674898d1aec91ce471dd4c86fe531962f2d5a1d0fb4c31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69652791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a087f300e7dbf259adba1d18102b1f776f261dcca172b1afd53cbbb46d26629`

```dockerfile
```

-	Layers:
	-	`sha256:ad9e422fcb0894199e21880589b22e93031eb9409cb161a74e5992b288220509`  
		Last Modified: Mon, 09 Feb 2026 20:00:02 GMT  
		Size: 69.6 MB (69625534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac00cc5dcd5b61e0fb23cb18bd515973d75ab6b1ee26ac429e1c927596f18df`  
		Last Modified: Mon, 09 Feb 2026 19:59:58 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:a06b77e4eaae8fadd5ad325b240edd04608e2772250ec377923f2c8e13ccc584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.7 MB (716723921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca41bc48a0bb6906927fa2c06c013ceab7fa63dc42af6a5af13a060ad9fe082b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:09:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 20:09:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 20:09:16 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 20:09:16 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Feb 2026 20:09:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 20:09:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:09:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 20:09:35 GMT
ENV ODOO_VERSION=19.0
# Mon, 09 Feb 2026 20:09:35 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 20:09:35 GMT
ARG ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
# Mon, 09 Feb 2026 20:12:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 20:12:33 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 20:12:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 20:12:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 20:12:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 20:12:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 20:12:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 20:12:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 20:12:35 GMT
USER odoo
# Mon, 09 Feb 2026 20:12:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 20:12:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309753fe35993f50ae1ca136b51196727dd6fcc555b07a7cce2890c409b6ae88`  
		Last Modified: Mon, 09 Feb 2026 20:17:29 GMT  
		Size: 267.8 MB (267750703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8869d3600823a629f0763702a58282df312db9e67edefe76e118d263414a5c94`  
		Last Modified: Mon, 09 Feb 2026 20:17:17 GMT  
		Size: 14.9 MB (14885554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad87469235b6d4e4b157fd9a560a908d19fcbdb06e2aa5155949240ce865092c`  
		Last Modified: Mon, 09 Feb 2026 20:17:16 GMT  
		Size: 480.1 KB (480103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d6965fad4243e1d0d1fd16cfda43e2c23bba8a381b683d1f29b495662425b0`  
		Last Modified: Mon, 09 Feb 2026 20:18:29 GMT  
		Size: 399.3 MB (399298959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee30b2d5391ff181c8a27c7f3c5bbb9f0a79307c3ab969db71c27a5fd79b4e3`  
		Last Modified: Mon, 09 Feb 2026 20:18:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f29fdf668be2b48e9c4cb90520f36f91712c4e4f72be206bb7e55a44323b198`  
		Last Modified: Mon, 09 Feb 2026 20:18:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75e8305e6f23ada7331d88275cfeb6480e09a16ba2f51c51ac08a0e128164f6`  
		Last Modified: Mon, 09 Feb 2026 20:18:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabb02435d4df7e808d5632945c192f86c1f6e2c40dcfa180f8cf1738c5108f5`  
		Last Modified: Mon, 09 Feb 2026 20:18:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:6238ed118864936ddc1e637fc0f888eab0cac2c13a173bacda4e34bee4c469a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69653790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8679970335bfaa0631e1718580ba05c743d8e70850c08aea21ad14db1e688ba4`

```dockerfile
```

-	Layers:
	-	`sha256:f942faca544cdb80df541d522b2d5af8dcaaf6a8e73f0c68b07788287338934a`  
		Last Modified: Mon, 09 Feb 2026 20:18:17 GMT  
		Size: 69.6 MB (69626636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4a48020ffd60cf6897d1454239403639b199d3e2d075e841a4d330ffb6ddedc`  
		Last Modified: Mon, 09 Feb 2026 20:18:14 GMT  
		Size: 27.2 KB (27154 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:bcf73ede5625b473024862e055247e2172701b70553e9c0725101f7b12546af3
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
$ docker pull odoo@sha256:f7d987696b508501fdc3d381a0ccf0c52444a2e6e556474d2c17eab73789630a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.3 MB (700293836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3393af1bc362d71d1d7680ccfaf9d6c289a411cbe788e55f6ef13464eaf5b634`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:56:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:56:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:56:55 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:56:55 GMT
ARG TARGETARCH=amd64
# Mon, 09 Feb 2026 19:56:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:57:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:57:05 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:57:05 GMT
ENV ODOO_VERSION=19.0
# Mon, 09 Feb 2026 19:57:05 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:57:05 GMT
ARG ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
# Mon, 09 Feb 2026 19:58:08 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:58:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:58:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:58:09 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
USER odoo
# Mon, 09 Feb 2026 19:58:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:58:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec7d2f393023c8d47fc7fc8dfbb08513f89551d289f7b4a785d69cdd7a12562`  
		Last Modified: Mon, 09 Feb 2026 20:00:28 GMT  
		Size: 257.0 MB (256965528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2836245bd2f95f29af22c2e06ab84fe3458b4403fec2e9720657e3c411b02aa7`  
		Last Modified: Mon, 09 Feb 2026 20:00:19 GMT  
		Size: 14.4 MB (14356868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22260229f8546eeed152c530b0cc61b5addd22637914fe5e75872d329adb6b11`  
		Last Modified: Mon, 09 Feb 2026 20:00:20 GMT  
		Size: 480.0 KB (480018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e37bcfab968f994d1585aa3324712c5b7d8afcd705ac75f5106a7bb8d2f6b9`  
		Last Modified: Mon, 09 Feb 2026 20:00:31 GMT  
		Size: 398.8 MB (398762970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345daf9a4d3921d73ee80687be69e573c246cddf82714d9fb0e2b6332747fe53`  
		Last Modified: Mon, 09 Feb 2026 19:59:53 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917ba9419a22df211490f683e76f115fdccdbcf84fb5832c31154192533090a4`  
		Last Modified: Mon, 09 Feb 2026 20:00:25 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a88d0100f22822999d96b572e093222869f3f6a30e5ab43b55aecd6b0789a75`  
		Last Modified: Mon, 09 Feb 2026 20:00:23 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8926765bd0fe3659e76bb30bef41068700ae06e0b62e2e911bdfdb44145c0405`  
		Last Modified: Mon, 09 Feb 2026 20:00:25 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:fffa1db1bb40e8e29aaba9d5779b56a31d420011bf857a498d015768faade245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69645340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987c6e9ddebf1097835adce06f6d8d20006e88a9584e01897373066fe81fc557`

```dockerfile
```

-	Layers:
	-	`sha256:05979d955e2dfac59d07ecb8ae00a300160c0dfe0ac77c4608658fad7cec371e`  
		Last Modified: Mon, 09 Feb 2026 20:00:23 GMT  
		Size: 69.6 MB (69618247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5939f6c0882d38cce3539cedca5930a96a06a64813e2f33e0bef88ae77367e44`  
		Last Modified: Mon, 09 Feb 2026 20:00:19 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b339dae8d638cd34570947c8e1aab5202dc86008766631b4acf4c2ea2f5bcd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.5 MB (696459479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad49ed2e141f820bb565f0f38a1584b3672f732f990067a131476300dff526f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:55:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:55:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:55:58 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:55:58 GMT
ARG TARGETARCH=arm64
# Mon, 09 Feb 2026 19:55:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:56:09 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:56:10 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:56:10 GMT
ENV ODOO_VERSION=19.0
# Mon, 09 Feb 2026 19:56:10 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:56:10 GMT
ARG ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
# Mon, 09 Feb 2026 19:57:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:57:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:57:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:57:15 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:57:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:57:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:57:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:57:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:57:15 GMT
USER odoo
# Mon, 09 Feb 2026 19:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:57:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f5d6664d6a5c9795c9d514cf35fc214711e2152f8ba79a763890c5708fc95e`  
		Last Modified: Mon, 09 Feb 2026 20:00:08 GMT  
		Size: 254.2 MB (254183363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e7ce57e304c1337a29b440be387ac917c5af7767a356c2fff7067ffcac9ec7`  
		Last Modified: Mon, 09 Feb 2026 19:59:59 GMT  
		Size: 14.3 MB (14334632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfbfb903b36e2dfa1a14a11d1ff9fa952f3c3cfb54484fe0319ad78bb46344c`  
		Last Modified: Mon, 09 Feb 2026 19:59:58 GMT  
		Size: 480.1 KB (480082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b588d32cfe5a2cf2979215040091176629fbc4c0f94bae1313e299cb1901cab7`  
		Last Modified: Mon, 09 Feb 2026 20:00:17 GMT  
		Size: 398.6 MB (398595138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e98ae45d01f2522fc5fa1a2b1ea23a4e6859b8e6273aace01b4379ec4415e66`  
		Last Modified: Mon, 09 Feb 2026 19:59:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f185c9023ed275cb5c9c0e9abda5b77359a4d51f76b72612646d298361a57731`  
		Last Modified: Mon, 09 Feb 2026 19:59:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6434875651c3bbf667e88e105eb388c2188f0c53f32b08f94dc581351744d3`  
		Last Modified: Mon, 09 Feb 2026 20:00:00 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a48cfc7b5eff2436b4800acb5929fc36a508ad65fdb519041c8b1c40925d8`  
		Last Modified: Mon, 09 Feb 2026 20:00:01 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:151964dd22130ac1f674898d1aec91ce471dd4c86fe531962f2d5a1d0fb4c31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69652791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a087f300e7dbf259adba1d18102b1f776f261dcca172b1afd53cbbb46d26629`

```dockerfile
```

-	Layers:
	-	`sha256:ad9e422fcb0894199e21880589b22e93031eb9409cb161a74e5992b288220509`  
		Last Modified: Mon, 09 Feb 2026 20:00:02 GMT  
		Size: 69.6 MB (69625534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac00cc5dcd5b61e0fb23cb18bd515973d75ab6b1ee26ac429e1c927596f18df`  
		Last Modified: Mon, 09 Feb 2026 19:59:58 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:a06b77e4eaae8fadd5ad325b240edd04608e2772250ec377923f2c8e13ccc584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.7 MB (716723921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca41bc48a0bb6906927fa2c06c013ceab7fa63dc42af6a5af13a060ad9fe082b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:09:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 20:09:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 20:09:16 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 20:09:16 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Feb 2026 20:09:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 20:09:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:09:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 20:09:35 GMT
ENV ODOO_VERSION=19.0
# Mon, 09 Feb 2026 20:09:35 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 20:09:35 GMT
ARG ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
# Mon, 09 Feb 2026 20:12:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 20:12:33 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 20:12:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 20:12:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 20:12:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 20:12:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 20:12:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 20:12:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 20:12:35 GMT
USER odoo
# Mon, 09 Feb 2026 20:12:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 20:12:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309753fe35993f50ae1ca136b51196727dd6fcc555b07a7cce2890c409b6ae88`  
		Last Modified: Mon, 09 Feb 2026 20:17:29 GMT  
		Size: 267.8 MB (267750703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8869d3600823a629f0763702a58282df312db9e67edefe76e118d263414a5c94`  
		Last Modified: Mon, 09 Feb 2026 20:17:17 GMT  
		Size: 14.9 MB (14885554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad87469235b6d4e4b157fd9a560a908d19fcbdb06e2aa5155949240ce865092c`  
		Last Modified: Mon, 09 Feb 2026 20:17:16 GMT  
		Size: 480.1 KB (480103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d6965fad4243e1d0d1fd16cfda43e2c23bba8a381b683d1f29b495662425b0`  
		Last Modified: Mon, 09 Feb 2026 20:18:29 GMT  
		Size: 399.3 MB (399298959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee30b2d5391ff181c8a27c7f3c5bbb9f0a79307c3ab969db71c27a5fd79b4e3`  
		Last Modified: Mon, 09 Feb 2026 20:18:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f29fdf668be2b48e9c4cb90520f36f91712c4e4f72be206bb7e55a44323b198`  
		Last Modified: Mon, 09 Feb 2026 20:18:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75e8305e6f23ada7331d88275cfeb6480e09a16ba2f51c51ac08a0e128164f6`  
		Last Modified: Mon, 09 Feb 2026 20:18:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabb02435d4df7e808d5632945c192f86c1f6e2c40dcfa180f8cf1738c5108f5`  
		Last Modified: Mon, 09 Feb 2026 20:18:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6238ed118864936ddc1e637fc0f888eab0cac2c13a173bacda4e34bee4c469a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69653790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8679970335bfaa0631e1718580ba05c743d8e70850c08aea21ad14db1e688ba4`

```dockerfile
```

-	Layers:
	-	`sha256:f942faca544cdb80df541d522b2d5af8dcaaf6a8e73f0c68b07788287338934a`  
		Last Modified: Mon, 09 Feb 2026 20:18:17 GMT  
		Size: 69.6 MB (69626636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4a48020ffd60cf6897d1454239403639b199d3e2d075e841a4d330ffb6ddedc`  
		Last Modified: Mon, 09 Feb 2026 20:18:14 GMT  
		Size: 27.2 KB (27154 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260217`

**does not exist** (yet?)

## `odoo:latest`

```console
$ docker pull odoo@sha256:bcf73ede5625b473024862e055247e2172701b70553e9c0725101f7b12546af3
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
$ docker pull odoo@sha256:f7d987696b508501fdc3d381a0ccf0c52444a2e6e556474d2c17eab73789630a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.3 MB (700293836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3393af1bc362d71d1d7680ccfaf9d6c289a411cbe788e55f6ef13464eaf5b634`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:56:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:56:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:56:55 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:56:55 GMT
ARG TARGETARCH=amd64
# Mon, 09 Feb 2026 19:56:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:57:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:57:05 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:57:05 GMT
ENV ODOO_VERSION=19.0
# Mon, 09 Feb 2026 19:57:05 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:57:05 GMT
ARG ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
# Mon, 09 Feb 2026 19:58:08 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:58:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:58:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:58:09 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:58:09 GMT
USER odoo
# Mon, 09 Feb 2026 19:58:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:58:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec7d2f393023c8d47fc7fc8dfbb08513f89551d289f7b4a785d69cdd7a12562`  
		Last Modified: Mon, 09 Feb 2026 20:00:28 GMT  
		Size: 257.0 MB (256965528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2836245bd2f95f29af22c2e06ab84fe3458b4403fec2e9720657e3c411b02aa7`  
		Last Modified: Mon, 09 Feb 2026 20:00:19 GMT  
		Size: 14.4 MB (14356868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22260229f8546eeed152c530b0cc61b5addd22637914fe5e75872d329adb6b11`  
		Last Modified: Mon, 09 Feb 2026 20:00:20 GMT  
		Size: 480.0 KB (480018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e37bcfab968f994d1585aa3324712c5b7d8afcd705ac75f5106a7bb8d2f6b9`  
		Last Modified: Mon, 09 Feb 2026 20:00:31 GMT  
		Size: 398.8 MB (398762970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345daf9a4d3921d73ee80687be69e573c246cddf82714d9fb0e2b6332747fe53`  
		Last Modified: Mon, 09 Feb 2026 19:59:53 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917ba9419a22df211490f683e76f115fdccdbcf84fb5832c31154192533090a4`  
		Last Modified: Mon, 09 Feb 2026 20:00:25 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a88d0100f22822999d96b572e093222869f3f6a30e5ab43b55aecd6b0789a75`  
		Last Modified: Mon, 09 Feb 2026 20:00:23 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8926765bd0fe3659e76bb30bef41068700ae06e0b62e2e911bdfdb44145c0405`  
		Last Modified: Mon, 09 Feb 2026 20:00:25 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:fffa1db1bb40e8e29aaba9d5779b56a31d420011bf857a498d015768faade245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69645340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987c6e9ddebf1097835adce06f6d8d20006e88a9584e01897373066fe81fc557`

```dockerfile
```

-	Layers:
	-	`sha256:05979d955e2dfac59d07ecb8ae00a300160c0dfe0ac77c4608658fad7cec371e`  
		Last Modified: Mon, 09 Feb 2026 20:00:23 GMT  
		Size: 69.6 MB (69618247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5939f6c0882d38cce3539cedca5930a96a06a64813e2f33e0bef88ae77367e44`  
		Last Modified: Mon, 09 Feb 2026 20:00:19 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b339dae8d638cd34570947c8e1aab5202dc86008766631b4acf4c2ea2f5bcd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.5 MB (696459479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad49ed2e141f820bb565f0f38a1584b3672f732f990067a131476300dff526f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:55:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 19:55:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 19:55:58 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:55:58 GMT
ARG TARGETARCH=arm64
# Mon, 09 Feb 2026 19:55:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 19:56:09 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 19:56:10 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 19:56:10 GMT
ENV ODOO_VERSION=19.0
# Mon, 09 Feb 2026 19:56:10 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 19:56:10 GMT
ARG ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
# Mon, 09 Feb 2026 19:57:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 19:57:14 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 19:57:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 19:57:15 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 19:57:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 19:57:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 19:57:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 19:57:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 19:57:15 GMT
USER odoo
# Mon, 09 Feb 2026 19:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 19:57:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f5d6664d6a5c9795c9d514cf35fc214711e2152f8ba79a763890c5708fc95e`  
		Last Modified: Mon, 09 Feb 2026 20:00:08 GMT  
		Size: 254.2 MB (254183363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e7ce57e304c1337a29b440be387ac917c5af7767a356c2fff7067ffcac9ec7`  
		Last Modified: Mon, 09 Feb 2026 19:59:59 GMT  
		Size: 14.3 MB (14334632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfbfb903b36e2dfa1a14a11d1ff9fa952f3c3cfb54484fe0319ad78bb46344c`  
		Last Modified: Mon, 09 Feb 2026 19:59:58 GMT  
		Size: 480.1 KB (480082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b588d32cfe5a2cf2979215040091176629fbc4c0f94bae1313e299cb1901cab7`  
		Last Modified: Mon, 09 Feb 2026 20:00:17 GMT  
		Size: 398.6 MB (398595138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e98ae45d01f2522fc5fa1a2b1ea23a4e6859b8e6273aace01b4379ec4415e66`  
		Last Modified: Mon, 09 Feb 2026 19:59:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f185c9023ed275cb5c9c0e9abda5b77359a4d51f76b72612646d298361a57731`  
		Last Modified: Mon, 09 Feb 2026 19:59:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6434875651c3bbf667e88e105eb388c2188f0c53f32b08f94dc581351744d3`  
		Last Modified: Mon, 09 Feb 2026 20:00:00 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2a48cfc7b5eff2436b4800acb5929fc36a508ad65fdb519041c8b1c40925d8`  
		Last Modified: Mon, 09 Feb 2026 20:00:01 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:151964dd22130ac1f674898d1aec91ce471dd4c86fe531962f2d5a1d0fb4c31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69652791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a087f300e7dbf259adba1d18102b1f776f261dcca172b1afd53cbbb46d26629`

```dockerfile
```

-	Layers:
	-	`sha256:ad9e422fcb0894199e21880589b22e93031eb9409cb161a74e5992b288220509`  
		Last Modified: Mon, 09 Feb 2026 20:00:02 GMT  
		Size: 69.6 MB (69625534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac00cc5dcd5b61e0fb23cb18bd515973d75ab6b1ee26ac429e1c927596f18df`  
		Last Modified: Mon, 09 Feb 2026 19:59:58 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:a06b77e4eaae8fadd5ad325b240edd04608e2772250ec377923f2c8e13ccc584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.7 MB (716723921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca41bc48a0bb6906927fa2c06c013ceab7fa63dc42af6a5af13a060ad9fe082b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 20:09:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 09 Feb 2026 20:09:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 09 Feb 2026 20:09:16 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 20:09:16 GMT
ARG TARGETARCH=ppc64le
# Mon, 09 Feb 2026 20:09:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 09 Feb 2026 20:09:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Feb 2026 20:09:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 09 Feb 2026 20:09:35 GMT
ENV ODOO_VERSION=19.0
# Mon, 09 Feb 2026 20:09:35 GMT
ARG ODOO_RELEASE=20260209
# Mon, 09 Feb 2026 20:09:35 GMT
ARG ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
# Mon, 09 Feb 2026 20:12:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 09 Feb 2026 20:12:33 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 09 Feb 2026 20:12:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 09 Feb 2026 20:12:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260209 ODOO_SHA=593907b836bf5c4c075bb7345277707c448d4bd5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 09 Feb 2026 20:12:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Feb 2026 20:12:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 09 Feb 2026 20:12:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Feb 2026 20:12:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 09 Feb 2026 20:12:35 GMT
USER odoo
# Mon, 09 Feb 2026 20:12:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Feb 2026 20:12:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309753fe35993f50ae1ca136b51196727dd6fcc555b07a7cce2890c409b6ae88`  
		Last Modified: Mon, 09 Feb 2026 20:17:29 GMT  
		Size: 267.8 MB (267750703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8869d3600823a629f0763702a58282df312db9e67edefe76e118d263414a5c94`  
		Last Modified: Mon, 09 Feb 2026 20:17:17 GMT  
		Size: 14.9 MB (14885554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad87469235b6d4e4b157fd9a560a908d19fcbdb06e2aa5155949240ce865092c`  
		Last Modified: Mon, 09 Feb 2026 20:17:16 GMT  
		Size: 480.1 KB (480103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d6965fad4243e1d0d1fd16cfda43e2c23bba8a381b683d1f29b495662425b0`  
		Last Modified: Mon, 09 Feb 2026 20:18:29 GMT  
		Size: 399.3 MB (399298959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee30b2d5391ff181c8a27c7f3c5bbb9f0a79307c3ab969db71c27a5fd79b4e3`  
		Last Modified: Mon, 09 Feb 2026 20:18:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f29fdf668be2b48e9c4cb90520f36f91712c4e4f72be206bb7e55a44323b198`  
		Last Modified: Mon, 09 Feb 2026 20:18:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75e8305e6f23ada7331d88275cfeb6480e09a16ba2f51c51ac08a0e128164f6`  
		Last Modified: Mon, 09 Feb 2026 20:18:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabb02435d4df7e808d5632945c192f86c1f6e2c40dcfa180f8cf1738c5108f5`  
		Last Modified: Mon, 09 Feb 2026 20:18:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:6238ed118864936ddc1e637fc0f888eab0cac2c13a173bacda4e34bee4c469a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69653790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8679970335bfaa0631e1718580ba05c743d8e70850c08aea21ad14db1e688ba4`

```dockerfile
```

-	Layers:
	-	`sha256:f942faca544cdb80df541d522b2d5af8dcaaf6a8e73f0c68b07788287338934a`  
		Last Modified: Mon, 09 Feb 2026 20:18:17 GMT  
		Size: 69.6 MB (69626636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4a48020ffd60cf6897d1454239403639b199d3e2d075e841a4d330ffb6ddedc`  
		Last Modified: Mon, 09 Feb 2026 20:18:14 GMT  
		Size: 27.2 KB (27154 bytes)  
		MIME: application/vnd.in-toto+json
