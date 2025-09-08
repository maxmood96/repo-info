<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250819`](#odoo160-20250819)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250819`](#odoo170-20250819)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250819`](#odoo180-20250819)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:d0974bb71fb3400b41f68147e13b41e4d707aabb24f7edbdc56412e18db51d30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:fc7318d37f57558e6aa9012a72e72388c2e59a761cb4f2cf14dbde40e0d30500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585313580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6a7fa0099633e705f4517a746c772716364a011b966fb9abcc29c632cf4a30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=16.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f14d9fb891c2a81614a962da2d601643717596e35f4d698273fa3c2cbe5e0b6`  
		Last Modified: Mon, 08 Sep 2025 22:13:05 GMT  
		Size: 219.6 MB (219626132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf71d0926305f514c85327c18045ebd6cba9ffa01c7021584ad0467dcef8e67`  
		Last Modified: Mon, 08 Sep 2025 21:51:12 GMT  
		Size: 2.6 MB (2632395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049ad3cbefbb2acd6e9a79af24d47f51985a7f50b9df969202f2adf29c20b3ee`  
		Last Modified: Mon, 08 Sep 2025 21:51:19 GMT  
		Size: 479.3 KB (479323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d853d3825eedf5bf96cdb3517b05fdb7c22bc7552640aac837391a9cc9be3be2`  
		Last Modified: Mon, 08 Sep 2025 22:12:54 GMT  
		Size: 332.3 MB (332317231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb8c03e97795e1140c0ef48ad0a3194f6896b695f0eb9cb07152a28db465641`  
		Last Modified: Mon, 08 Sep 2025 21:51:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c40979febbdd48028f2670260883e8299e047a7f71d4a4cd04c65ace100d1fc`  
		Last Modified: Mon, 08 Sep 2025 21:51:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f205b985ef20835189d8cafac414698216a439132e738c34bb53d4e92df6bf64`  
		Last Modified: Mon, 08 Sep 2025 21:51:30 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e9aaa177b18d594e8e743c5bc91a895f43fdd5745e0a1ef04594e4ee0c628`  
		Last Modified: Mon, 08 Sep 2025 21:51:34 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:58064e483d937f812df18b16276424107849e6a7812735880a383c55b6280218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39558660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0cb8fd1afd8640422c2e2c134b72619eece1de7f60fc0f8079a5cab9c518275`

```dockerfile
```

-	Layers:
	-	`sha256:6281c62a5a63ea405542fb7e8be49682fc031ffdbb3be525561e83c56ecb9295`  
		Last Modified: Mon, 08 Sep 2025 22:13:00 GMT  
		Size: 39.5 MB (39531942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d67e49c196a1826096b3d24522fb7859bf7687f3c52d3e7c37ac20523092cd`  
		Last Modified: Mon, 08 Sep 2025 22:13:02 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6abea8ea968dd3adcf453239973a9133aadb3fac3516c902eeead800614f9b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580764653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4588cbd6476166c10a5c508511e505e424bcfefbba04b5c194c92a72287ff05d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=16.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b48dc98c569b8c48d8a2d9b437ed0f3383809dd033be4ba66a0c4a18b74f22`  
		Last Modified: Mon, 08 Sep 2025 22:16:10 GMT  
		Size: 216.9 MB (216919414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7d4cd7dfb470ebe0d43e50fce96b50e890aaed966fcf1dff67e3687a9ba128`  
		Last Modified: Mon, 08 Sep 2025 22:15:28 GMT  
		Size: 2.6 MB (2639071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2672d2139662f0dbe81cf08640a10431662d0a035e646f94f911237ec2fbbf5f`  
		Last Modified: Mon, 08 Sep 2025 22:15:29 GMT  
		Size: 479.4 KB (479371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629c0afe33062008f01fbc66abf81218d46d6ebf4bea4c031da4f4c8f28a526f`  
		Last Modified: Mon, 08 Sep 2025 22:16:28 GMT  
		Size: 332.0 MB (331973907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a80667653102374b64ef84ecf168551837039892ce8bcf4ef62a1c56ba7d6e6`  
		Last Modified: Mon, 08 Sep 2025 22:15:30 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa4a2662d87ce5be4ea2c6d5a6af14a3a4849bdb5ba7f75f267e2eafd2c1ece`  
		Last Modified: Mon, 08 Sep 2025 22:15:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6513405b1a497c11d1ab27bd660a2864bc10f63d944e2512cf5f0cc15103515`  
		Last Modified: Mon, 08 Sep 2025 22:15:32 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8940c471a5d06a96c658fb80a3c995fed864f14a1b4677b8f4a6519b17a40005`  
		Last Modified: Mon, 08 Sep 2025 22:15:32 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:6a05da00f00d6cc88509f6f7c81e6c877e2326a7ff2685324ce812df59175e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39565278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10e16b20ef01b744b351a6353b0b2c6fe4d48feeab69c90cc4bc8b3bf82e669`

```dockerfile
```

-	Layers:
	-	`sha256:4202a61c683102c30f99caf33012976143dfbec708f89d24efeb7fff8015990d`  
		Last Modified: Mon, 08 Sep 2025 22:13:44 GMT  
		Size: 39.5 MB (39538408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0e4fb6299f3c3e54347b352309bc11b910d2e272c4eb942ae53ee3d5063e16`  
		Last Modified: Mon, 08 Sep 2025 22:13:46 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:d0974bb71fb3400b41f68147e13b41e4d707aabb24f7edbdc56412e18db51d30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:fc7318d37f57558e6aa9012a72e72388c2e59a761cb4f2cf14dbde40e0d30500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585313580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6a7fa0099633e705f4517a746c772716364a011b966fb9abcc29c632cf4a30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=16.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f14d9fb891c2a81614a962da2d601643717596e35f4d698273fa3c2cbe5e0b6`  
		Last Modified: Mon, 08 Sep 2025 22:13:05 GMT  
		Size: 219.6 MB (219626132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf71d0926305f514c85327c18045ebd6cba9ffa01c7021584ad0467dcef8e67`  
		Last Modified: Mon, 08 Sep 2025 21:51:12 GMT  
		Size: 2.6 MB (2632395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049ad3cbefbb2acd6e9a79af24d47f51985a7f50b9df969202f2adf29c20b3ee`  
		Last Modified: Mon, 08 Sep 2025 21:51:19 GMT  
		Size: 479.3 KB (479323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d853d3825eedf5bf96cdb3517b05fdb7c22bc7552640aac837391a9cc9be3be2`  
		Last Modified: Mon, 08 Sep 2025 22:12:54 GMT  
		Size: 332.3 MB (332317231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb8c03e97795e1140c0ef48ad0a3194f6896b695f0eb9cb07152a28db465641`  
		Last Modified: Mon, 08 Sep 2025 21:51:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c40979febbdd48028f2670260883e8299e047a7f71d4a4cd04c65ace100d1fc`  
		Last Modified: Mon, 08 Sep 2025 21:51:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f205b985ef20835189d8cafac414698216a439132e738c34bb53d4e92df6bf64`  
		Last Modified: Mon, 08 Sep 2025 21:51:30 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e9aaa177b18d594e8e743c5bc91a895f43fdd5745e0a1ef04594e4ee0c628`  
		Last Modified: Mon, 08 Sep 2025 21:51:34 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:58064e483d937f812df18b16276424107849e6a7812735880a383c55b6280218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39558660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0cb8fd1afd8640422c2e2c134b72619eece1de7f60fc0f8079a5cab9c518275`

```dockerfile
```

-	Layers:
	-	`sha256:6281c62a5a63ea405542fb7e8be49682fc031ffdbb3be525561e83c56ecb9295`  
		Last Modified: Mon, 08 Sep 2025 22:13:00 GMT  
		Size: 39.5 MB (39531942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d67e49c196a1826096b3d24522fb7859bf7687f3c52d3e7c37ac20523092cd`  
		Last Modified: Mon, 08 Sep 2025 22:13:02 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6abea8ea968dd3adcf453239973a9133aadb3fac3516c902eeead800614f9b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580764653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4588cbd6476166c10a5c508511e505e424bcfefbba04b5c194c92a72287ff05d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=16.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b48dc98c569b8c48d8a2d9b437ed0f3383809dd033be4ba66a0c4a18b74f22`  
		Last Modified: Mon, 08 Sep 2025 22:16:10 GMT  
		Size: 216.9 MB (216919414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7d4cd7dfb470ebe0d43e50fce96b50e890aaed966fcf1dff67e3687a9ba128`  
		Last Modified: Mon, 08 Sep 2025 22:15:28 GMT  
		Size: 2.6 MB (2639071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2672d2139662f0dbe81cf08640a10431662d0a035e646f94f911237ec2fbbf5f`  
		Last Modified: Mon, 08 Sep 2025 22:15:29 GMT  
		Size: 479.4 KB (479371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629c0afe33062008f01fbc66abf81218d46d6ebf4bea4c031da4f4c8f28a526f`  
		Last Modified: Mon, 08 Sep 2025 22:16:28 GMT  
		Size: 332.0 MB (331973907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a80667653102374b64ef84ecf168551837039892ce8bcf4ef62a1c56ba7d6e6`  
		Last Modified: Mon, 08 Sep 2025 22:15:30 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa4a2662d87ce5be4ea2c6d5a6af14a3a4849bdb5ba7f75f267e2eafd2c1ece`  
		Last Modified: Mon, 08 Sep 2025 22:15:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6513405b1a497c11d1ab27bd660a2864bc10f63d944e2512cf5f0cc15103515`  
		Last Modified: Mon, 08 Sep 2025 22:15:32 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8940c471a5d06a96c658fb80a3c995fed864f14a1b4677b8f4a6519b17a40005`  
		Last Modified: Mon, 08 Sep 2025 22:15:32 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6a05da00f00d6cc88509f6f7c81e6c877e2326a7ff2685324ce812df59175e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39565278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10e16b20ef01b744b351a6353b0b2c6fe4d48feeab69c90cc4bc8b3bf82e669`

```dockerfile
```

-	Layers:
	-	`sha256:4202a61c683102c30f99caf33012976143dfbec708f89d24efeb7fff8015990d`  
		Last Modified: Mon, 08 Sep 2025 22:13:44 GMT  
		Size: 39.5 MB (39538408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0e4fb6299f3c3e54347b352309bc11b910d2e272c4eb942ae53ee3d5063e16`  
		Last Modified: Mon, 08 Sep 2025 22:13:46 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250819`

```console
$ docker pull odoo@sha256:d0974bb71fb3400b41f68147e13b41e4d707aabb24f7edbdc56412e18db51d30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250819` - linux; amd64

```console
$ docker pull odoo@sha256:fc7318d37f57558e6aa9012a72e72388c2e59a761cb4f2cf14dbde40e0d30500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585313580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6a7fa0099633e705f4517a746c772716364a011b966fb9abcc29c632cf4a30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=16.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f14d9fb891c2a81614a962da2d601643717596e35f4d698273fa3c2cbe5e0b6`  
		Last Modified: Mon, 08 Sep 2025 22:13:05 GMT  
		Size: 219.6 MB (219626132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf71d0926305f514c85327c18045ebd6cba9ffa01c7021584ad0467dcef8e67`  
		Last Modified: Mon, 08 Sep 2025 21:51:12 GMT  
		Size: 2.6 MB (2632395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049ad3cbefbb2acd6e9a79af24d47f51985a7f50b9df969202f2adf29c20b3ee`  
		Last Modified: Mon, 08 Sep 2025 21:51:19 GMT  
		Size: 479.3 KB (479323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d853d3825eedf5bf96cdb3517b05fdb7c22bc7552640aac837391a9cc9be3be2`  
		Last Modified: Mon, 08 Sep 2025 22:12:54 GMT  
		Size: 332.3 MB (332317231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb8c03e97795e1140c0ef48ad0a3194f6896b695f0eb9cb07152a28db465641`  
		Last Modified: Mon, 08 Sep 2025 21:51:24 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c40979febbdd48028f2670260883e8299e047a7f71d4a4cd04c65ace100d1fc`  
		Last Modified: Mon, 08 Sep 2025 21:51:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f205b985ef20835189d8cafac414698216a439132e738c34bb53d4e92df6bf64`  
		Last Modified: Mon, 08 Sep 2025 21:51:30 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e9aaa177b18d594e8e743c5bc91a895f43fdd5745e0a1ef04594e4ee0c628`  
		Last Modified: Mon, 08 Sep 2025 21:51:34 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:58064e483d937f812df18b16276424107849e6a7812735880a383c55b6280218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39558660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0cb8fd1afd8640422c2e2c134b72619eece1de7f60fc0f8079a5cab9c518275`

```dockerfile
```

-	Layers:
	-	`sha256:6281c62a5a63ea405542fb7e8be49682fc031ffdbb3be525561e83c56ecb9295`  
		Last Modified: Mon, 08 Sep 2025 22:13:00 GMT  
		Size: 39.5 MB (39531942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d67e49c196a1826096b3d24522fb7859bf7687f3c52d3e7c37ac20523092cd`  
		Last Modified: Mon, 08 Sep 2025 22:13:02 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250819` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6abea8ea968dd3adcf453239973a9133aadb3fac3516c902eeead800614f9b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580764653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4588cbd6476166c10a5c508511e505e424bcfefbba04b5c194c92a72287ff05d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=16.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=6e4d8446d4a6af7c147f84a5b3d824a7ddaec5c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b48dc98c569b8c48d8a2d9b437ed0f3383809dd033be4ba66a0c4a18b74f22`  
		Last Modified: Mon, 08 Sep 2025 22:16:10 GMT  
		Size: 216.9 MB (216919414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7d4cd7dfb470ebe0d43e50fce96b50e890aaed966fcf1dff67e3687a9ba128`  
		Last Modified: Mon, 08 Sep 2025 22:15:28 GMT  
		Size: 2.6 MB (2639071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2672d2139662f0dbe81cf08640a10431662d0a035e646f94f911237ec2fbbf5f`  
		Last Modified: Mon, 08 Sep 2025 22:15:29 GMT  
		Size: 479.4 KB (479371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629c0afe33062008f01fbc66abf81218d46d6ebf4bea4c031da4f4c8f28a526f`  
		Last Modified: Mon, 08 Sep 2025 22:16:28 GMT  
		Size: 332.0 MB (331973907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a80667653102374b64ef84ecf168551837039892ce8bcf4ef62a1c56ba7d6e6`  
		Last Modified: Mon, 08 Sep 2025 22:15:30 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa4a2662d87ce5be4ea2c6d5a6af14a3a4849bdb5ba7f75f267e2eafd2c1ece`  
		Last Modified: Mon, 08 Sep 2025 22:15:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6513405b1a497c11d1ab27bd660a2864bc10f63d944e2512cf5f0cc15103515`  
		Last Modified: Mon, 08 Sep 2025 22:15:32 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8940c471a5d06a96c658fb80a3c995fed864f14a1b4677b8f4a6519b17a40005`  
		Last Modified: Mon, 08 Sep 2025 22:15:32 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:6a05da00f00d6cc88509f6f7c81e6c877e2326a7ff2685324ce812df59175e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39565278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10e16b20ef01b744b351a6353b0b2c6fe4d48feeab69c90cc4bc8b3bf82e669`

```dockerfile
```

-	Layers:
	-	`sha256:4202a61c683102c30f99caf33012976143dfbec708f89d24efeb7fff8015990d`  
		Last Modified: Mon, 08 Sep 2025 22:13:44 GMT  
		Size: 39.5 MB (39538408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0e4fb6299f3c3e54347b352309bc11b910d2e272c4eb942ae53ee3d5063e16`  
		Last Modified: Mon, 08 Sep 2025 22:13:46 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:d4a4c3139c39f38727e007c2f5b55f1b4bce657bf31cda4b60b6e60045f05bb2
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
$ docker pull odoo@sha256:188797ff244039822fa8b23afc7a712347106e058d49c3cc1139f243b42ae0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.9 MB (604928939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aae58107d7bd779b1cba60365ea50840ac6393de3f951b1592a76e73f784617`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2761949271b7cc720b8b1dee2bf9131f725f57919e6240396bcd6eaa5f709be`  
		Last Modified: Fri, 05 Sep 2025 17:31:02 GMT  
		Size: 233.8 MB (233788244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9874887a4e60ffc8a94255be7ac9b34500e99141ae56942338db44762c4479`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 2.5 MB (2532181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062a54876f93766336e9890bb1827df0b2cd120c7f310a3c874d08838dcd6ec3`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 480.4 KB (480384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b591079c40252cd3bda4dc58861d93c2d9224b3eb24aecbf0e0740a65871ee2`  
		Last Modified: Fri, 05 Sep 2025 17:31:22 GMT  
		Size: 338.6 MB (338588760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5965bb41a7b3eab9203f47b372b3d5437be1874397fcdc55cc2e21c3b2488f2b`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbbceb55da4ace5d878a494ce163cf7398eaafb8758e76b3ce5e3133c6ab8ae`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19764a4a2d7a9d4f7d2835e7c14d306cf703dc6ab5c9ffa83322e147a6686b57`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d535a23da2eaebd9e448c47fdb8a61daa8d38e99a07ee7c67b8d6000ef7991e4`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:980ef3a70755d9671e213a066e61993b990cb72f9ce7c215cd13a322da175e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41417380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f817875152a85037f734201b4a0e954c93cc648870932700e17aa23003ce4d5`

```dockerfile
```

-	Layers:
	-	`sha256:c2dfa823db46892b8708b58459b040de237541d6652a10dc97ae7eaf3f3864bc`  
		Last Modified: Fri, 05 Sep 2025 19:12:35 GMT  
		Size: 41.4 MB (41390545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c2133639a0b05a63f4bd3b60fa9bf6fd556f6544e7f6d246bd6debbccb4411`  
		Last Modified: Fri, 05 Sep 2025 19:12:38 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:63f9feb1611819534dbefe71140d1b1f19ee41e6572343f7f348ee9397ccf35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.7 MB (599719464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8285bdc5f288edd8586f6484f88ca4d4c49e3a8e8006d135fa23b8b8e58d4fb8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164d8839fbc223fc2412beb744758b2147cf5441da2074f606b077b9360c659a`  
		Last Modified: Fri, 05 Sep 2025 17:31:27 GMT  
		Size: 231.2 MB (231159233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436981ed639700be10a706aae1abf08200e7e222c810f85bdfdd374070936db`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 2.5 MB (2521524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f174da2152b927ebb1ded2b02763c1e4b7cd6c03dfd4595aa22991a6ecd29a99`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 480.4 KB (480418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6216952b51c8d1187774c551f118c462a6772a38954956d10e11d528b29fc52c`  
		Last Modified: Fri, 05 Sep 2025 17:31:45 GMT  
		Size: 338.2 MB (338194383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01aee41996f9461371cce0123d47037add3055ea1edbd5ae6cbbdf6ef63b1dc`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac431bee166124822ce2b511df26d493ed0dd0440d99595daa0a03389fb66f0`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859954e3e11c4d548546bbc830bbf1cc92ed6f16a7151c2cb4860931a29d05d5`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7473461e9bf7a77d61eacfd05db6313ac7451318e4a6998b06098e2b5a6202`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c60725221239ab9029314a5398a5af7d93775487bcc1d54e0664bcf339acff21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41424039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88780652742237544d0692fc970975ff7b77d58777f46b0d23e2f9cdc9504c6`

```dockerfile
```

-	Layers:
	-	`sha256:205bccd1d13bbba491d93f7c806de4da9b7ee5d69b282fa1e4826060f3ed5428`  
		Last Modified: Fri, 05 Sep 2025 19:13:19 GMT  
		Size: 41.4 MB (41397052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675e9619b2f48c742fd9b559c884412ac29c4ef7b94050ff8fe364e55a124425`  
		Last Modified: Fri, 05 Sep 2025 19:13:20 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:97a65b161526ca3d8f4a78515e69a8df79770ce7b8be2c48f60ebac7ad9a3bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.4 MB (621359257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9301bc89615a89cccaac889bfca99d5e42dab2160afb4433452fe2c7f6d3051c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0244576ff338cb147bce56c2933253a7a9b13693e7a2a4fab239f787971b79e`  
		Last Modified: Fri, 05 Sep 2025 16:46:24 GMT  
		Size: 243.3 MB (243255703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8560b7193b511593404db1da58c5c82ec824298a9b689a2b09266a88226fd23e`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 2.8 MB (2849712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e332f93026970e0b3ca80b7bc515ce4e41367ed2492efb6ead672fb111fd4e5`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 480.5 KB (480460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96e1a92411eaab6a5d06bc873045ac8d0b4391fd7bb199882136f9697861c72`  
		Last Modified: Fri, 05 Sep 2025 16:47:46 GMT  
		Size: 340.3 MB (340327720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bf7ab4effd807deaf0b6a2193fad550fb8fe6b6927c7612adb3d152d9879d5`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f26e7a1ba77bfd4cdfbaabeac133dd0c0541b8329207c17b27f9f3f0e6eb9f`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a7db06565a42de028eb713238a8954f36b5ca8cc304e5fdaa19d7934135b8d`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd8bd5333593996461856e7d4017b1cf1eec68528955180f0b3503e93c0451f`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:cf302fb653a310fc0439716bce30b9e2600a4ef578a893f06f185a48c850bb09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41426043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c662ecd74c6239b337413acf740911dade48126079798d2e42055edf7290a1`

```dockerfile
```

-	Layers:
	-	`sha256:24a9b1809ace54623cecdbf33ea6ae144ecfc590f46f79ddc5c3518741538e73`  
		Last Modified: Fri, 05 Sep 2025 16:13:42 GMT  
		Size: 41.4 MB (41399152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acad5770b4691effe12194bbf9c50dde9a9e8a9a30a72683e6054eb18dfa6778`  
		Last Modified: Fri, 05 Sep 2025 16:13:43 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:d4a4c3139c39f38727e007c2f5b55f1b4bce657bf31cda4b60b6e60045f05bb2
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
$ docker pull odoo@sha256:188797ff244039822fa8b23afc7a712347106e058d49c3cc1139f243b42ae0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.9 MB (604928939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aae58107d7bd779b1cba60365ea50840ac6393de3f951b1592a76e73f784617`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2761949271b7cc720b8b1dee2bf9131f725f57919e6240396bcd6eaa5f709be`  
		Last Modified: Fri, 05 Sep 2025 17:31:02 GMT  
		Size: 233.8 MB (233788244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9874887a4e60ffc8a94255be7ac9b34500e99141ae56942338db44762c4479`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 2.5 MB (2532181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062a54876f93766336e9890bb1827df0b2cd120c7f310a3c874d08838dcd6ec3`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 480.4 KB (480384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b591079c40252cd3bda4dc58861d93c2d9224b3eb24aecbf0e0740a65871ee2`  
		Last Modified: Fri, 05 Sep 2025 17:31:22 GMT  
		Size: 338.6 MB (338588760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5965bb41a7b3eab9203f47b372b3d5437be1874397fcdc55cc2e21c3b2488f2b`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbbceb55da4ace5d878a494ce163cf7398eaafb8758e76b3ce5e3133c6ab8ae`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19764a4a2d7a9d4f7d2835e7c14d306cf703dc6ab5c9ffa83322e147a6686b57`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d535a23da2eaebd9e448c47fdb8a61daa8d38e99a07ee7c67b8d6000ef7991e4`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:980ef3a70755d9671e213a066e61993b990cb72f9ce7c215cd13a322da175e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41417380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f817875152a85037f734201b4a0e954c93cc648870932700e17aa23003ce4d5`

```dockerfile
```

-	Layers:
	-	`sha256:c2dfa823db46892b8708b58459b040de237541d6652a10dc97ae7eaf3f3864bc`  
		Last Modified: Fri, 05 Sep 2025 19:12:35 GMT  
		Size: 41.4 MB (41390545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c2133639a0b05a63f4bd3b60fa9bf6fd556f6544e7f6d246bd6debbccb4411`  
		Last Modified: Fri, 05 Sep 2025 19:12:38 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:63f9feb1611819534dbefe71140d1b1f19ee41e6572343f7f348ee9397ccf35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.7 MB (599719464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8285bdc5f288edd8586f6484f88ca4d4c49e3a8e8006d135fa23b8b8e58d4fb8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164d8839fbc223fc2412beb744758b2147cf5441da2074f606b077b9360c659a`  
		Last Modified: Fri, 05 Sep 2025 17:31:27 GMT  
		Size: 231.2 MB (231159233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436981ed639700be10a706aae1abf08200e7e222c810f85bdfdd374070936db`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 2.5 MB (2521524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f174da2152b927ebb1ded2b02763c1e4b7cd6c03dfd4595aa22991a6ecd29a99`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 480.4 KB (480418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6216952b51c8d1187774c551f118c462a6772a38954956d10e11d528b29fc52c`  
		Last Modified: Fri, 05 Sep 2025 17:31:45 GMT  
		Size: 338.2 MB (338194383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01aee41996f9461371cce0123d47037add3055ea1edbd5ae6cbbdf6ef63b1dc`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac431bee166124822ce2b511df26d493ed0dd0440d99595daa0a03389fb66f0`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859954e3e11c4d548546bbc830bbf1cc92ed6f16a7151c2cb4860931a29d05d5`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7473461e9bf7a77d61eacfd05db6313ac7451318e4a6998b06098e2b5a6202`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c60725221239ab9029314a5398a5af7d93775487bcc1d54e0664bcf339acff21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41424039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88780652742237544d0692fc970975ff7b77d58777f46b0d23e2f9cdc9504c6`

```dockerfile
```

-	Layers:
	-	`sha256:205bccd1d13bbba491d93f7c806de4da9b7ee5d69b282fa1e4826060f3ed5428`  
		Last Modified: Fri, 05 Sep 2025 19:13:19 GMT  
		Size: 41.4 MB (41397052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675e9619b2f48c742fd9b559c884412ac29c4ef7b94050ff8fe364e55a124425`  
		Last Modified: Fri, 05 Sep 2025 19:13:20 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:97a65b161526ca3d8f4a78515e69a8df79770ce7b8be2c48f60ebac7ad9a3bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.4 MB (621359257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9301bc89615a89cccaac889bfca99d5e42dab2160afb4433452fe2c7f6d3051c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0244576ff338cb147bce56c2933253a7a9b13693e7a2a4fab239f787971b79e`  
		Last Modified: Fri, 05 Sep 2025 16:46:24 GMT  
		Size: 243.3 MB (243255703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8560b7193b511593404db1da58c5c82ec824298a9b689a2b09266a88226fd23e`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 2.8 MB (2849712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e332f93026970e0b3ca80b7bc515ce4e41367ed2492efb6ead672fb111fd4e5`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 480.5 KB (480460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96e1a92411eaab6a5d06bc873045ac8d0b4391fd7bb199882136f9697861c72`  
		Last Modified: Fri, 05 Sep 2025 16:47:46 GMT  
		Size: 340.3 MB (340327720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bf7ab4effd807deaf0b6a2193fad550fb8fe6b6927c7612adb3d152d9879d5`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f26e7a1ba77bfd4cdfbaabeac133dd0c0541b8329207c17b27f9f3f0e6eb9f`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a7db06565a42de028eb713238a8954f36b5ca8cc304e5fdaa19d7934135b8d`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd8bd5333593996461856e7d4017b1cf1eec68528955180f0b3503e93c0451f`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cf302fb653a310fc0439716bce30b9e2600a4ef578a893f06f185a48c850bb09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41426043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c662ecd74c6239b337413acf740911dade48126079798d2e42055edf7290a1`

```dockerfile
```

-	Layers:
	-	`sha256:24a9b1809ace54623cecdbf33ea6ae144ecfc590f46f79ddc5c3518741538e73`  
		Last Modified: Fri, 05 Sep 2025 16:13:42 GMT  
		Size: 41.4 MB (41399152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acad5770b4691effe12194bbf9c50dde9a9e8a9a30a72683e6054eb18dfa6778`  
		Last Modified: Fri, 05 Sep 2025 16:13:43 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250819`

```console
$ docker pull odoo@sha256:d4a4c3139c39f38727e007c2f5b55f1b4bce657bf31cda4b60b6e60045f05bb2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250819` - linux; amd64

```console
$ docker pull odoo@sha256:188797ff244039822fa8b23afc7a712347106e058d49c3cc1139f243b42ae0dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.9 MB (604928939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aae58107d7bd779b1cba60365ea50840ac6393de3f951b1592a76e73f784617`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2761949271b7cc720b8b1dee2bf9131f725f57919e6240396bcd6eaa5f709be`  
		Last Modified: Fri, 05 Sep 2025 17:31:02 GMT  
		Size: 233.8 MB (233788244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9874887a4e60ffc8a94255be7ac9b34500e99141ae56942338db44762c4479`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 2.5 MB (2532181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062a54876f93766336e9890bb1827df0b2cd120c7f310a3c874d08838dcd6ec3`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 480.4 KB (480384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b591079c40252cd3bda4dc58861d93c2d9224b3eb24aecbf0e0740a65871ee2`  
		Last Modified: Fri, 05 Sep 2025 17:31:22 GMT  
		Size: 338.6 MB (338588760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5965bb41a7b3eab9203f47b372b3d5437be1874397fcdc55cc2e21c3b2488f2b`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbbceb55da4ace5d878a494ce163cf7398eaafb8758e76b3ce5e3133c6ab8ae`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19764a4a2d7a9d4f7d2835e7c14d306cf703dc6ab5c9ffa83322e147a6686b57`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d535a23da2eaebd9e448c47fdb8a61daa8d38e99a07ee7c67b8d6000ef7991e4`  
		Last Modified: Fri, 05 Sep 2025 16:11:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:980ef3a70755d9671e213a066e61993b990cb72f9ce7c215cd13a322da175e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41417380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f817875152a85037f734201b4a0e954c93cc648870932700e17aa23003ce4d5`

```dockerfile
```

-	Layers:
	-	`sha256:c2dfa823db46892b8708b58459b040de237541d6652a10dc97ae7eaf3f3864bc`  
		Last Modified: Fri, 05 Sep 2025 19:12:35 GMT  
		Size: 41.4 MB (41390545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c2133639a0b05a63f4bd3b60fa9bf6fd556f6544e7f6d246bd6debbccb4411`  
		Last Modified: Fri, 05 Sep 2025 19:12:38 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250819` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:63f9feb1611819534dbefe71140d1b1f19ee41e6572343f7f348ee9397ccf35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.7 MB (599719464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8285bdc5f288edd8586f6484f88ca4d4c49e3a8e8006d135fa23b8b8e58d4fb8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164d8839fbc223fc2412beb744758b2147cf5441da2074f606b077b9360c659a`  
		Last Modified: Fri, 05 Sep 2025 17:31:27 GMT  
		Size: 231.2 MB (231159233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436981ed639700be10a706aae1abf08200e7e222c810f85bdfdd374070936db`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 2.5 MB (2521524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f174da2152b927ebb1ded2b02763c1e4b7cd6c03dfd4595aa22991a6ecd29a99`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 480.4 KB (480418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6216952b51c8d1187774c551f118c462a6772a38954956d10e11d528b29fc52c`  
		Last Modified: Fri, 05 Sep 2025 17:31:45 GMT  
		Size: 338.2 MB (338194383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01aee41996f9461371cce0123d47037add3055ea1edbd5ae6cbbdf6ef63b1dc`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac431bee166124822ce2b511df26d493ed0dd0440d99595daa0a03389fb66f0`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859954e3e11c4d548546bbc830bbf1cc92ed6f16a7151c2cb4860931a29d05d5`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7473461e9bf7a77d61eacfd05db6313ac7451318e4a6998b06098e2b5a6202`  
		Last Modified: Fri, 05 Sep 2025 16:14:14 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:c60725221239ab9029314a5398a5af7d93775487bcc1d54e0664bcf339acff21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41424039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88780652742237544d0692fc970975ff7b77d58777f46b0d23e2f9cdc9504c6`

```dockerfile
```

-	Layers:
	-	`sha256:205bccd1d13bbba491d93f7c806de4da9b7ee5d69b282fa1e4826060f3ed5428`  
		Last Modified: Fri, 05 Sep 2025 19:13:19 GMT  
		Size: 41.4 MB (41397052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675e9619b2f48c742fd9b559c884412ac29c4ef7b94050ff8fe364e55a124425`  
		Last Modified: Fri, 05 Sep 2025 19:13:20 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250819` - linux; ppc64le

```console
$ docker pull odoo@sha256:97a65b161526ca3d8f4a78515e69a8df79770ce7b8be2c48f60ebac7ad9a3bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.4 MB (621359257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9301bc89615a89cccaac889bfca99d5e42dab2160afb4433452fe2c7f6d3051c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=17.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=f342ea8c4ac7944ecee4b7f023903fd528f988e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0244576ff338cb147bce56c2933253a7a9b13693e7a2a4fab239f787971b79e`  
		Last Modified: Fri, 05 Sep 2025 16:46:24 GMT  
		Size: 243.3 MB (243255703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8560b7193b511593404db1da58c5c82ec824298a9b689a2b09266a88226fd23e`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 2.8 MB (2849712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e332f93026970e0b3ca80b7bc515ce4e41367ed2492efb6ead672fb111fd4e5`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 480.5 KB (480460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96e1a92411eaab6a5d06bc873045ac8d0b4391fd7bb199882136f9697861c72`  
		Last Modified: Fri, 05 Sep 2025 16:47:46 GMT  
		Size: 340.3 MB (340327720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bf7ab4effd807deaf0b6a2193fad550fb8fe6b6927c7612adb3d152d9879d5`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f26e7a1ba77bfd4cdfbaabeac133dd0c0541b8329207c17b27f9f3f0e6eb9f`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a7db06565a42de028eb713238a8954f36b5ca8cc304e5fdaa19d7934135b8d`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd8bd5333593996461856e7d4017b1cf1eec68528955180f0b3503e93c0451f`  
		Last Modified: Fri, 05 Sep 2025 16:06:11 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:cf302fb653a310fc0439716bce30b9e2600a4ef578a893f06f185a48c850bb09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41426043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c662ecd74c6239b337413acf740911dade48126079798d2e42055edf7290a1`

```dockerfile
```

-	Layers:
	-	`sha256:24a9b1809ace54623cecdbf33ea6ae144ecfc590f46f79ddc5c3518741538e73`  
		Last Modified: Fri, 05 Sep 2025 16:13:42 GMT  
		Size: 41.4 MB (41399152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acad5770b4691effe12194bbf9c50dde9a9e8a9a30a72683e6054eb18dfa6778`  
		Last Modified: Fri, 05 Sep 2025 16:13:43 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:39cd0a27a3268bc6423033ca198a22bb9c9c5799ff11b575bef969bc7767d808
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
$ docker pull odoo@sha256:b073cc503b2f21e7dbfcab8403164eaac9efba954c51d5e2aba031d64910a483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.5 MB (675547210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df37f1393e31a8e867854cf89989f53121f0c173775c14b95bd88961254631e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fcd4df6f886befc8d3e8d666b864679ecc8e0a9b01defc44e246500d0b9273`  
		Last Modified: Tue, 02 Sep 2025 00:27:19 GMT  
		Size: 254.5 MB (254529673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc8c3d7a5271f0510d576add7e5a83036345f1d97a8226c4fd28bc0bf3207dd`  
		Last Modified: Mon, 01 Sep 2025 23:15:05 GMT  
		Size: 14.3 MB (14286074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceda477f4d890a48353af295a57e9bbedb2b274a5ad50825b9c8b38109d5d86c`  
		Last Modified: Mon, 01 Sep 2025 23:15:04 GMT  
		Size: 480.2 KB (480220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa65d101bca742bba346513c3ca555ea10a21aa4a2fb851c16b75a2121ca406f`  
		Last Modified: Tue, 02 Sep 2025 00:28:00 GMT  
		Size: 376.5 MB (376525737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51f0002894eeb73a07c078c643b31827cc879777e0f2969d87dcc9bc188eeb1`  
		Last Modified: Mon, 01 Sep 2025 23:15:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0360f983c4e282d61ba1ac1bb5cb9041e22cf542bfa01473a08e3e43693c03`  
		Last Modified: Mon, 01 Sep 2025 23:15:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d9f900a6be1ca04b120585ca934dae2cad569e9f5ec0d8468977c8b0ae0d25`  
		Last Modified: Mon, 01 Sep 2025 23:15:04 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8ff8b6a30b079fc3491144bb59765234ebd44e0316cfdeac0b21f66f0eae3`  
		Last Modified: Mon, 01 Sep 2025 23:15:05 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:2a3d8b5f8f54d1a0bb20536428d47fcf5e0f9125a10485567e30abc1b01ab18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60789926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9e8919e56202981783d760e741e87b841210d389986254d4250a3376008520`

```dockerfile
```

-	Layers:
	-	`sha256:212a8e2bad0491f3fdf5e6ef8c6f27ba648ba48f98d82b940c4ab1caf1e8e48f`  
		Last Modified: Tue, 02 Sep 2025 01:12:33 GMT  
		Size: 60.8 MB (60762790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506d6d9f1c7dd5fb6dc3ed1fbb0bb2b8613ab0a48e5cc81cbb646acb160de5ec`  
		Last Modified: Tue, 02 Sep 2025 01:12:35 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9b02aca00245a63f5c19863e924d69fef1bec9ba8f5089110a091aac8beb8784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.9 MB (671899129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd98fe8bcb78b76fb0acbdc90223f962da727547c28f94694274d51f0a2755a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b95baac204027846db77cc3fdd5cd2dc84e518caa1fb5bc50542cc77876817`  
		Last Modified: Tue, 02 Sep 2025 03:24:37 GMT  
		Size: 251.9 MB (251920241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fee90181433f263c39cea7c81928effc97e646cfff118b37e155e283097401`  
		Last Modified: Tue, 02 Sep 2025 02:39:10 GMT  
		Size: 14.3 MB (14263266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a3bdcac34f21f9e0b4ed90f9e5878066889e2ce3b02b8f4ebfa1826e5e1ae2`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 480.2 KB (480185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82b5089c227f87c228f943e0dc0992885aec9334474a458d75d96cd6aa91d16`  
		Last Modified: Tue, 02 Sep 2025 03:25:23 GMT  
		Size: 376.4 MB (376372758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a0839a5420a43c9e86b2c5b4ae5e0fc454b40694f7473f79e1bc3639ed4b3c`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0fe04fff8e824e96a68edede3fb958327ce0511ce5c3f864a19a90fadde595`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c357e9175b24893a2c34188f4de53b7727a9ce964a5b60928496fe04d2d81d9`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b59b12c983dc4d911998299f2bb1e74cb2bacb8476eb40002d2628b808c1c5e`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:01592e01c2ae6ed66db15ed03d8b7699c7f5e9370a87ca1b0d4d8bc2b6cb134c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60797377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caec2f7463347e23b9b37cbd478fc6c01a6687a2c15c6503e603ea763cd2a8d9`

```dockerfile
```

-	Layers:
	-	`sha256:67c4f00ac0f6a05e5ab30520478eec7bb40c0c14550f967ab389014567695e7f`  
		Last Modified: Tue, 02 Sep 2025 04:13:54 GMT  
		Size: 60.8 MB (60770077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc11134458b74304faf78df86ba707860ec4014038970185b8cfcf3bc31d1bb2`  
		Last Modified: Tue, 02 Sep 2025 04:13:54 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:1536fc02fc8b231f90aeae5fc3463be8c5733e3f2728097c51b4ee48776f7df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.8 MB (691764001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dbfac7c096f43505fffb144e3bcce9eb431aca7aa028ada853dfc9c7b49112`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375fb8aac140fb3840d6c865952e08cb5549f35764b88abd233265875869792b`  
		Last Modified: Tue, 02 Sep 2025 02:15:27 GMT  
		Size: 265.1 MB (265076170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebb0c70656da24d45ef3fb11536054b0097162a5c9ae16cf30f5ae7ab64d097`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 14.8 MB (14813151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23737bb6e9c110b40255471148f5eb2f8681ab274947230b14040194860ea15`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 480.2 KB (480242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f3346b368f3b3c96163d47dbbc307172421cd5099e1db4397e769f859f9d6`  
		Last Modified: Tue, 02 Sep 2025 02:15:53 GMT  
		Size: 377.1 MB (377062461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c77e9306fdba620ee6f786236cb82018cd27a7c9bf7670dcf83ae5d6798cf83`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe578be03e34113206b6a3aab4d4be3b36c967eeb7a6ebcb4fdb62d6adedea41`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bf419626b86c6bcf56e91c10c3e6bd5088ff9f544de43a2275184d9e65d417`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87bdd722836755a9d624817b1f14a038ca39cf635a18d480c8b17588404e5d5`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:b8379d1246876337777fab503d42643e6282d1d81cf55be22eed3e157a04a3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60798377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245cd8892feaca4dcddc3fbb350eb417595372967e581a61805ed98477460ea8`

```dockerfile
```

-	Layers:
	-	`sha256:ac55fec4857b813594d3be62fdee6792280fbc69d981f38f510b521f83eb1a37`  
		Last Modified: Tue, 02 Sep 2025 04:15:17 GMT  
		Size: 60.8 MB (60771179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ac2e6ec49bb35bdbd4f3ee35dd659025a57b0dbc363eec5e76f2d5b138b8142`  
		Last Modified: Tue, 02 Sep 2025 04:15:18 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:39cd0a27a3268bc6423033ca198a22bb9c9c5799ff11b575bef969bc7767d808
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
$ docker pull odoo@sha256:b073cc503b2f21e7dbfcab8403164eaac9efba954c51d5e2aba031d64910a483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.5 MB (675547210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df37f1393e31a8e867854cf89989f53121f0c173775c14b95bd88961254631e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fcd4df6f886befc8d3e8d666b864679ecc8e0a9b01defc44e246500d0b9273`  
		Last Modified: Tue, 02 Sep 2025 00:27:19 GMT  
		Size: 254.5 MB (254529673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc8c3d7a5271f0510d576add7e5a83036345f1d97a8226c4fd28bc0bf3207dd`  
		Last Modified: Mon, 01 Sep 2025 23:15:05 GMT  
		Size: 14.3 MB (14286074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceda477f4d890a48353af295a57e9bbedb2b274a5ad50825b9c8b38109d5d86c`  
		Last Modified: Mon, 01 Sep 2025 23:15:04 GMT  
		Size: 480.2 KB (480220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa65d101bca742bba346513c3ca555ea10a21aa4a2fb851c16b75a2121ca406f`  
		Last Modified: Tue, 02 Sep 2025 00:28:00 GMT  
		Size: 376.5 MB (376525737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51f0002894eeb73a07c078c643b31827cc879777e0f2969d87dcc9bc188eeb1`  
		Last Modified: Mon, 01 Sep 2025 23:15:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0360f983c4e282d61ba1ac1bb5cb9041e22cf542bfa01473a08e3e43693c03`  
		Last Modified: Mon, 01 Sep 2025 23:15:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d9f900a6be1ca04b120585ca934dae2cad569e9f5ec0d8468977c8b0ae0d25`  
		Last Modified: Mon, 01 Sep 2025 23:15:04 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8ff8b6a30b079fc3491144bb59765234ebd44e0316cfdeac0b21f66f0eae3`  
		Last Modified: Mon, 01 Sep 2025 23:15:05 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2a3d8b5f8f54d1a0bb20536428d47fcf5e0f9125a10485567e30abc1b01ab18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60789926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9e8919e56202981783d760e741e87b841210d389986254d4250a3376008520`

```dockerfile
```

-	Layers:
	-	`sha256:212a8e2bad0491f3fdf5e6ef8c6f27ba648ba48f98d82b940c4ab1caf1e8e48f`  
		Last Modified: Tue, 02 Sep 2025 01:12:33 GMT  
		Size: 60.8 MB (60762790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506d6d9f1c7dd5fb6dc3ed1fbb0bb2b8613ab0a48e5cc81cbb646acb160de5ec`  
		Last Modified: Tue, 02 Sep 2025 01:12:35 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9b02aca00245a63f5c19863e924d69fef1bec9ba8f5089110a091aac8beb8784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.9 MB (671899129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd98fe8bcb78b76fb0acbdc90223f962da727547c28f94694274d51f0a2755a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b95baac204027846db77cc3fdd5cd2dc84e518caa1fb5bc50542cc77876817`  
		Last Modified: Tue, 02 Sep 2025 03:24:37 GMT  
		Size: 251.9 MB (251920241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fee90181433f263c39cea7c81928effc97e646cfff118b37e155e283097401`  
		Last Modified: Tue, 02 Sep 2025 02:39:10 GMT  
		Size: 14.3 MB (14263266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a3bdcac34f21f9e0b4ed90f9e5878066889e2ce3b02b8f4ebfa1826e5e1ae2`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 480.2 KB (480185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82b5089c227f87c228f943e0dc0992885aec9334474a458d75d96cd6aa91d16`  
		Last Modified: Tue, 02 Sep 2025 03:25:23 GMT  
		Size: 376.4 MB (376372758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a0839a5420a43c9e86b2c5b4ae5e0fc454b40694f7473f79e1bc3639ed4b3c`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0fe04fff8e824e96a68edede3fb958327ce0511ce5c3f864a19a90fadde595`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c357e9175b24893a2c34188f4de53b7727a9ce964a5b60928496fe04d2d81d9`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b59b12c983dc4d911998299f2bb1e74cb2bacb8476eb40002d2628b808c1c5e`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:01592e01c2ae6ed66db15ed03d8b7699c7f5e9370a87ca1b0d4d8bc2b6cb134c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60797377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caec2f7463347e23b9b37cbd478fc6c01a6687a2c15c6503e603ea763cd2a8d9`

```dockerfile
```

-	Layers:
	-	`sha256:67c4f00ac0f6a05e5ab30520478eec7bb40c0c14550f967ab389014567695e7f`  
		Last Modified: Tue, 02 Sep 2025 04:13:54 GMT  
		Size: 60.8 MB (60770077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc11134458b74304faf78df86ba707860ec4014038970185b8cfcf3bc31d1bb2`  
		Last Modified: Tue, 02 Sep 2025 04:13:54 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:1536fc02fc8b231f90aeae5fc3463be8c5733e3f2728097c51b4ee48776f7df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.8 MB (691764001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dbfac7c096f43505fffb144e3bcce9eb431aca7aa028ada853dfc9c7b49112`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375fb8aac140fb3840d6c865952e08cb5549f35764b88abd233265875869792b`  
		Last Modified: Tue, 02 Sep 2025 02:15:27 GMT  
		Size: 265.1 MB (265076170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebb0c70656da24d45ef3fb11536054b0097162a5c9ae16cf30f5ae7ab64d097`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 14.8 MB (14813151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23737bb6e9c110b40255471148f5eb2f8681ab274947230b14040194860ea15`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 480.2 KB (480242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f3346b368f3b3c96163d47dbbc307172421cd5099e1db4397e769f859f9d6`  
		Last Modified: Tue, 02 Sep 2025 02:15:53 GMT  
		Size: 377.1 MB (377062461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c77e9306fdba620ee6f786236cb82018cd27a7c9bf7670dcf83ae5d6798cf83`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe578be03e34113206b6a3aab4d4be3b36c967eeb7a6ebcb4fdb62d6adedea41`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bf419626b86c6bcf56e91c10c3e6bd5088ff9f544de43a2275184d9e65d417`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87bdd722836755a9d624817b1f14a038ca39cf635a18d480c8b17588404e5d5`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b8379d1246876337777fab503d42643e6282d1d81cf55be22eed3e157a04a3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60798377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245cd8892feaca4dcddc3fbb350eb417595372967e581a61805ed98477460ea8`

```dockerfile
```

-	Layers:
	-	`sha256:ac55fec4857b813594d3be62fdee6792280fbc69d981f38f510b521f83eb1a37`  
		Last Modified: Tue, 02 Sep 2025 04:15:17 GMT  
		Size: 60.8 MB (60771179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ac2e6ec49bb35bdbd4f3ee35dd659025a57b0dbc363eec5e76f2d5b138b8142`  
		Last Modified: Tue, 02 Sep 2025 04:15:18 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250819`

```console
$ docker pull odoo@sha256:39cd0a27a3268bc6423033ca198a22bb9c9c5799ff11b575bef969bc7767d808
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250819` - linux; amd64

```console
$ docker pull odoo@sha256:b073cc503b2f21e7dbfcab8403164eaac9efba954c51d5e2aba031d64910a483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.5 MB (675547210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df37f1393e31a8e867854cf89989f53121f0c173775c14b95bd88961254631e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fcd4df6f886befc8d3e8d666b864679ecc8e0a9b01defc44e246500d0b9273`  
		Last Modified: Tue, 02 Sep 2025 00:27:19 GMT  
		Size: 254.5 MB (254529673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc8c3d7a5271f0510d576add7e5a83036345f1d97a8226c4fd28bc0bf3207dd`  
		Last Modified: Mon, 01 Sep 2025 23:15:05 GMT  
		Size: 14.3 MB (14286074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceda477f4d890a48353af295a57e9bbedb2b274a5ad50825b9c8b38109d5d86c`  
		Last Modified: Mon, 01 Sep 2025 23:15:04 GMT  
		Size: 480.2 KB (480220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa65d101bca742bba346513c3ca555ea10a21aa4a2fb851c16b75a2121ca406f`  
		Last Modified: Tue, 02 Sep 2025 00:28:00 GMT  
		Size: 376.5 MB (376525737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51f0002894eeb73a07c078c643b31827cc879777e0f2969d87dcc9bc188eeb1`  
		Last Modified: Mon, 01 Sep 2025 23:15:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0360f983c4e282d61ba1ac1bb5cb9041e22cf542bfa01473a08e3e43693c03`  
		Last Modified: Mon, 01 Sep 2025 23:15:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d9f900a6be1ca04b120585ca934dae2cad569e9f5ec0d8468977c8b0ae0d25`  
		Last Modified: Mon, 01 Sep 2025 23:15:04 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8ff8b6a30b079fc3491144bb59765234ebd44e0316cfdeac0b21f66f0eae3`  
		Last Modified: Mon, 01 Sep 2025 23:15:05 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:2a3d8b5f8f54d1a0bb20536428d47fcf5e0f9125a10485567e30abc1b01ab18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60789926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9e8919e56202981783d760e741e87b841210d389986254d4250a3376008520`

```dockerfile
```

-	Layers:
	-	`sha256:212a8e2bad0491f3fdf5e6ef8c6f27ba648ba48f98d82b940c4ab1caf1e8e48f`  
		Last Modified: Tue, 02 Sep 2025 01:12:33 GMT  
		Size: 60.8 MB (60762790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506d6d9f1c7dd5fb6dc3ed1fbb0bb2b8613ab0a48e5cc81cbb646acb160de5ec`  
		Last Modified: Tue, 02 Sep 2025 01:12:35 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250819` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9b02aca00245a63f5c19863e924d69fef1bec9ba8f5089110a091aac8beb8784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.9 MB (671899129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd98fe8bcb78b76fb0acbdc90223f962da727547c28f94694274d51f0a2755a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b95baac204027846db77cc3fdd5cd2dc84e518caa1fb5bc50542cc77876817`  
		Last Modified: Tue, 02 Sep 2025 03:24:37 GMT  
		Size: 251.9 MB (251920241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fee90181433f263c39cea7c81928effc97e646cfff118b37e155e283097401`  
		Last Modified: Tue, 02 Sep 2025 02:39:10 GMT  
		Size: 14.3 MB (14263266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a3bdcac34f21f9e0b4ed90f9e5878066889e2ce3b02b8f4ebfa1826e5e1ae2`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 480.2 KB (480185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82b5089c227f87c228f943e0dc0992885aec9334474a458d75d96cd6aa91d16`  
		Last Modified: Tue, 02 Sep 2025 03:25:23 GMT  
		Size: 376.4 MB (376372758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a0839a5420a43c9e86b2c5b4ae5e0fc454b40694f7473f79e1bc3639ed4b3c`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0fe04fff8e824e96a68edede3fb958327ce0511ce5c3f864a19a90fadde595`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c357e9175b24893a2c34188f4de53b7727a9ce964a5b60928496fe04d2d81d9`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b59b12c983dc4d911998299f2bb1e74cb2bacb8476eb40002d2628b808c1c5e`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:01592e01c2ae6ed66db15ed03d8b7699c7f5e9370a87ca1b0d4d8bc2b6cb134c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60797377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caec2f7463347e23b9b37cbd478fc6c01a6687a2c15c6503e603ea763cd2a8d9`

```dockerfile
```

-	Layers:
	-	`sha256:67c4f00ac0f6a05e5ab30520478eec7bb40c0c14550f967ab389014567695e7f`  
		Last Modified: Tue, 02 Sep 2025 04:13:54 GMT  
		Size: 60.8 MB (60770077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc11134458b74304faf78df86ba707860ec4014038970185b8cfcf3bc31d1bb2`  
		Last Modified: Tue, 02 Sep 2025 04:13:54 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250819` - linux; ppc64le

```console
$ docker pull odoo@sha256:1536fc02fc8b231f90aeae5fc3463be8c5733e3f2728097c51b4ee48776f7df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.8 MB (691764001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dbfac7c096f43505fffb144e3bcce9eb431aca7aa028ada853dfc9c7b49112`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375fb8aac140fb3840d6c865952e08cb5549f35764b88abd233265875869792b`  
		Last Modified: Tue, 02 Sep 2025 02:15:27 GMT  
		Size: 265.1 MB (265076170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebb0c70656da24d45ef3fb11536054b0097162a5c9ae16cf30f5ae7ab64d097`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 14.8 MB (14813151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23737bb6e9c110b40255471148f5eb2f8681ab274947230b14040194860ea15`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 480.2 KB (480242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f3346b368f3b3c96163d47dbbc307172421cd5099e1db4397e769f859f9d6`  
		Last Modified: Tue, 02 Sep 2025 02:15:53 GMT  
		Size: 377.1 MB (377062461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c77e9306fdba620ee6f786236cb82018cd27a7c9bf7670dcf83ae5d6798cf83`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe578be03e34113206b6a3aab4d4be3b36c967eeb7a6ebcb4fdb62d6adedea41`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bf419626b86c6bcf56e91c10c3e6bd5088ff9f544de43a2275184d9e65d417`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87bdd722836755a9d624817b1f14a038ca39cf635a18d480c8b17588404e5d5`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250819` - unknown; unknown

```console
$ docker pull odoo@sha256:b8379d1246876337777fab503d42643e6282d1d81cf55be22eed3e157a04a3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60798377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245cd8892feaca4dcddc3fbb350eb417595372967e581a61805ed98477460ea8`

```dockerfile
```

-	Layers:
	-	`sha256:ac55fec4857b813594d3be62fdee6792280fbc69d981f38f510b521f83eb1a37`  
		Last Modified: Tue, 02 Sep 2025 04:15:17 GMT  
		Size: 60.8 MB (60771179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ac2e6ec49bb35bdbd4f3ee35dd659025a57b0dbc363eec5e76f2d5b138b8142`  
		Last Modified: Tue, 02 Sep 2025 04:15:18 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:39cd0a27a3268bc6423033ca198a22bb9c9c5799ff11b575bef969bc7767d808
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
$ docker pull odoo@sha256:b073cc503b2f21e7dbfcab8403164eaac9efba954c51d5e2aba031d64910a483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.5 MB (675547210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df37f1393e31a8e867854cf89989f53121f0c173775c14b95bd88961254631e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=amd64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fcd4df6f886befc8d3e8d666b864679ecc8e0a9b01defc44e246500d0b9273`  
		Last Modified: Tue, 02 Sep 2025 00:27:19 GMT  
		Size: 254.5 MB (254529673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc8c3d7a5271f0510d576add7e5a83036345f1d97a8226c4fd28bc0bf3207dd`  
		Last Modified: Mon, 01 Sep 2025 23:15:05 GMT  
		Size: 14.3 MB (14286074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceda477f4d890a48353af295a57e9bbedb2b274a5ad50825b9c8b38109d5d86c`  
		Last Modified: Mon, 01 Sep 2025 23:15:04 GMT  
		Size: 480.2 KB (480220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa65d101bca742bba346513c3ca555ea10a21aa4a2fb851c16b75a2121ca406f`  
		Last Modified: Tue, 02 Sep 2025 00:28:00 GMT  
		Size: 376.5 MB (376525737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51f0002894eeb73a07c078c643b31827cc879777e0f2969d87dcc9bc188eeb1`  
		Last Modified: Mon, 01 Sep 2025 23:15:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0360f983c4e282d61ba1ac1bb5cb9041e22cf542bfa01473a08e3e43693c03`  
		Last Modified: Mon, 01 Sep 2025 23:15:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d9f900a6be1ca04b120585ca934dae2cad569e9f5ec0d8468977c8b0ae0d25`  
		Last Modified: Mon, 01 Sep 2025 23:15:04 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8ff8b6a30b079fc3491144bb59765234ebd44e0316cfdeac0b21f66f0eae3`  
		Last Modified: Mon, 01 Sep 2025 23:15:05 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:2a3d8b5f8f54d1a0bb20536428d47fcf5e0f9125a10485567e30abc1b01ab18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60789926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9e8919e56202981783d760e741e87b841210d389986254d4250a3376008520`

```dockerfile
```

-	Layers:
	-	`sha256:212a8e2bad0491f3fdf5e6ef8c6f27ba648ba48f98d82b940c4ab1caf1e8e48f`  
		Last Modified: Tue, 02 Sep 2025 01:12:33 GMT  
		Size: 60.8 MB (60762790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506d6d9f1c7dd5fb6dc3ed1fbb0bb2b8613ab0a48e5cc81cbb646acb160de5ec`  
		Last Modified: Tue, 02 Sep 2025 01:12:35 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:9b02aca00245a63f5c19863e924d69fef1bec9ba8f5089110a091aac8beb8784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.9 MB (671899129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd98fe8bcb78b76fb0acbdc90223f962da727547c28f94694274d51f0a2755a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=arm64
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b95baac204027846db77cc3fdd5cd2dc84e518caa1fb5bc50542cc77876817`  
		Last Modified: Tue, 02 Sep 2025 03:24:37 GMT  
		Size: 251.9 MB (251920241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fee90181433f263c39cea7c81928effc97e646cfff118b37e155e283097401`  
		Last Modified: Tue, 02 Sep 2025 02:39:10 GMT  
		Size: 14.3 MB (14263266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a3bdcac34f21f9e0b4ed90f9e5878066889e2ce3b02b8f4ebfa1826e5e1ae2`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 480.2 KB (480185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82b5089c227f87c228f943e0dc0992885aec9334474a458d75d96cd6aa91d16`  
		Last Modified: Tue, 02 Sep 2025 03:25:23 GMT  
		Size: 376.4 MB (376372758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a0839a5420a43c9e86b2c5b4ae5e0fc454b40694f7473f79e1bc3639ed4b3c`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0fe04fff8e824e96a68edede3fb958327ce0511ce5c3f864a19a90fadde595`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c357e9175b24893a2c34188f4de53b7727a9ce964a5b60928496fe04d2d81d9`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b59b12c983dc4d911998299f2bb1e74cb2bacb8476eb40002d2628b808c1c5e`  
		Last Modified: Tue, 02 Sep 2025 02:39:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:01592e01c2ae6ed66db15ed03d8b7699c7f5e9370a87ca1b0d4d8bc2b6cb134c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60797377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caec2f7463347e23b9b37cbd478fc6c01a6687a2c15c6503e603ea763cd2a8d9`

```dockerfile
```

-	Layers:
	-	`sha256:67c4f00ac0f6a05e5ab30520478eec7bb40c0c14550f967ab389014567695e7f`  
		Last Modified: Tue, 02 Sep 2025 04:13:54 GMT  
		Size: 60.8 MB (60770077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc11134458b74304faf78df86ba707860ec4014038970185b8cfcf3bc31d1bb2`  
		Last Modified: Tue, 02 Sep 2025 04:13:54 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:1536fc02fc8b231f90aeae5fc3463be8c5733e3f2728097c51b4ee48776f7df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.8 MB (691764001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dbfac7c096f43505fffb144e3bcce9eb431aca7aa028ada853dfc9c7b49112`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 08:02:42 GMT
ARG RELEASE
# Tue, 19 Aug 2025 08:02:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 08:02:42 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 08:02:42 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Aug 2025 08:02:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 19 Aug 2025 08:02:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 19 Aug 2025 08:02:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_VERSION=18.0
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_RELEASE=20250819
# Tue, 19 Aug 2025 08:02:42 GMT
ARG ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250819 ODOO_SHA=25daea677dc7b60cc25ec1eebd16d1c8e3f77a8a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 19 Aug 2025 08:02:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 19 Aug 2025 08:02:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 19 Aug 2025 08:02:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 19 Aug 2025 08:02:42 GMT
USER odoo
# Tue, 19 Aug 2025 08:02:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 08:02:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375fb8aac140fb3840d6c865952e08cb5549f35764b88abd233265875869792b`  
		Last Modified: Tue, 02 Sep 2025 02:15:27 GMT  
		Size: 265.1 MB (265076170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebb0c70656da24d45ef3fb11536054b0097162a5c9ae16cf30f5ae7ab64d097`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 14.8 MB (14813151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23737bb6e9c110b40255471148f5eb2f8681ab274947230b14040194860ea15`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 480.2 KB (480242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f3346b368f3b3c96163d47dbbc307172421cd5099e1db4397e769f859f9d6`  
		Last Modified: Tue, 02 Sep 2025 02:15:53 GMT  
		Size: 377.1 MB (377062461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c77e9306fdba620ee6f786236cb82018cd27a7c9bf7670dcf83ae5d6798cf83`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe578be03e34113206b6a3aab4d4be3b36c967eeb7a6ebcb4fdb62d6adedea41`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bf419626b86c6bcf56e91c10c3e6bd5088ff9f544de43a2275184d9e65d417`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87bdd722836755a9d624817b1f14a038ca39cf635a18d480c8b17588404e5d5`  
		Last Modified: Tue, 02 Sep 2025 01:28:55 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:b8379d1246876337777fab503d42643e6282d1d81cf55be22eed3e157a04a3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60798377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245cd8892feaca4dcddc3fbb350eb417595372967e581a61805ed98477460ea8`

```dockerfile
```

-	Layers:
	-	`sha256:ac55fec4857b813594d3be62fdee6792280fbc69d981f38f510b521f83eb1a37`  
		Last Modified: Tue, 02 Sep 2025 04:15:17 GMT  
		Size: 60.8 MB (60771179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ac2e6ec49bb35bdbd4f3ee35dd659025a57b0dbc363eec5e76f2d5b138b8142`  
		Last Modified: Tue, 02 Sep 2025 04:15:18 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
