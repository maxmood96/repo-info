<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:752dda2f524064d63e1774559cad8c8c27cd43178f2024190d761c2a532e80f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:f0a1e6779210433d3746a2ea2e631c672e20c7ae30b8cbfee9d5c866b5a411b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.0 MB (563010263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f977e6e47ee455e9c7f94aa5af57f0e8b4d4115d5af30a70c809ebd4aaf66637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 01 Nov 2023 12:03:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 01 Nov 2023 12:04:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 12:04:04 GMT
RUN npm install -g rtlcss
# Wed, 01 Nov 2023 12:04:04 GMT
ENV ODOO_VERSION=15.0
# Tue, 14 Nov 2023 01:46:55 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 01:46:55 GMT
ARG ODOO_SHA=13ab7feaaa6f94269bfe4ff8922363ee7aac617c
# Tue, 14 Nov 2023 01:48:04 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=13ab7feaaa6f94269bfe4ff8922363ee7aac617c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 01:48:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 01:48:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 01:48:09 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=13ab7feaaa6f94269bfe4ff8922363ee7aac617c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 01:48:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 01:48:09 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 01:48:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 01:48:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 01:48:09 GMT
USER odoo
# Tue, 14 Nov 2023 01:48:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 01:48:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae4769061fca067a25d337753a857c225301a3391d70dc9c355ec401a1666f9`  
		Last Modified: Wed, 01 Nov 2023 12:09:44 GMT  
		Size: 220.3 MB (220298628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f037b076bdf88bd13eb93037e412a84af9179318c033537325a2abb0e21f3437`  
		Last Modified: Wed, 01 Nov 2023 12:09:20 GMT  
		Size: 2.6 MB (2624848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09c8bae1e450f33859e0454685d8e83ce199230cdf0487f7b3bca45bccd8a66`  
		Last Modified: Wed, 01 Nov 2023 12:09:20 GMT  
		Size: 457.9 KB (457875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44abe15dd5abf247216eac32ac636ec8ef1858645b3aad95f4f284fb11e7f3a2`  
		Last Modified: Tue, 14 Nov 2023 01:50:32 GMT  
		Size: 308.2 MB (308208530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af37afb87b4bdd17c0ff464def181f27aab0549c484db39b314eeac64620973`  
		Last Modified: Tue, 14 Nov 2023 01:49:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f24486a161af39390a88ced24fa696ca234f71aac53c692c3462306e68edf5a`  
		Last Modified: Tue, 14 Nov 2023 01:49:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c69e40b5b0d1e8903fabc9fc4457a738e7ae7dae82c976dd1669155ef6cd68e`  
		Last Modified: Tue, 14 Nov 2023 01:49:59 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185491d96ed1c10608eb5a60e53e89bac442dd92f63886876b883b003e6a96cf`  
		Last Modified: Tue, 14 Nov 2023 01:49:59 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:752dda2f524064d63e1774559cad8c8c27cd43178f2024190d761c2a532e80f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:f0a1e6779210433d3746a2ea2e631c672e20c7ae30b8cbfee9d5c866b5a411b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.0 MB (563010263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f977e6e47ee455e9c7f94aa5af57f0e8b4d4115d5af30a70c809ebd4aaf66637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 01 Nov 2023 12:03:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 01 Nov 2023 12:04:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 12:04:04 GMT
RUN npm install -g rtlcss
# Wed, 01 Nov 2023 12:04:04 GMT
ENV ODOO_VERSION=15.0
# Tue, 14 Nov 2023 01:46:55 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 01:46:55 GMT
ARG ODOO_SHA=13ab7feaaa6f94269bfe4ff8922363ee7aac617c
# Tue, 14 Nov 2023 01:48:04 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=13ab7feaaa6f94269bfe4ff8922363ee7aac617c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 01:48:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 01:48:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 01:48:09 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=13ab7feaaa6f94269bfe4ff8922363ee7aac617c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 01:48:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 01:48:09 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 01:48:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 01:48:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 01:48:09 GMT
USER odoo
# Tue, 14 Nov 2023 01:48:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 01:48:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae4769061fca067a25d337753a857c225301a3391d70dc9c355ec401a1666f9`  
		Last Modified: Wed, 01 Nov 2023 12:09:44 GMT  
		Size: 220.3 MB (220298628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f037b076bdf88bd13eb93037e412a84af9179318c033537325a2abb0e21f3437`  
		Last Modified: Wed, 01 Nov 2023 12:09:20 GMT  
		Size: 2.6 MB (2624848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09c8bae1e450f33859e0454685d8e83ce199230cdf0487f7b3bca45bccd8a66`  
		Last Modified: Wed, 01 Nov 2023 12:09:20 GMT  
		Size: 457.9 KB (457875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44abe15dd5abf247216eac32ac636ec8ef1858645b3aad95f4f284fb11e7f3a2`  
		Last Modified: Tue, 14 Nov 2023 01:50:32 GMT  
		Size: 308.2 MB (308208530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af37afb87b4bdd17c0ff464def181f27aab0549c484db39b314eeac64620973`  
		Last Modified: Tue, 14 Nov 2023 01:49:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f24486a161af39390a88ced24fa696ca234f71aac53c692c3462306e68edf5a`  
		Last Modified: Tue, 14 Nov 2023 01:49:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c69e40b5b0d1e8903fabc9fc4457a738e7ae7dae82c976dd1669155ef6cd68e`  
		Last Modified: Tue, 14 Nov 2023 01:49:59 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185491d96ed1c10608eb5a60e53e89bac442dd92f63886876b883b003e6a96cf`  
		Last Modified: Tue, 14 Nov 2023 01:49:59 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:8c4feb44dd6581b9d41ecd87e0a6345f6277a7c391a7b824c340ff9c90ee488a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:224afec587448938f248e5f7cce715e573e27020a840b3268b497d06aaa60c46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.2 MB (577199471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14fbcf2831eb734c4a01194f91413cfe3771b36c58b4c8c1ac6f946534eb97d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:38:54 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:40:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:40:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:40:19 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:40:19 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 Nov 2023 01:45:16 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 01:45:16 GMT
ARG ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
# Tue, 14 Nov 2023 01:46:36 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 01:46:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 01:46:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 01:46:39 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 01:46:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 01:46:39 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 01:46:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 01:46:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 01:46:39 GMT
USER odoo
# Tue, 14 Nov 2023 01:46:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 01:46:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3abf7b1c0fb11700caf26b92dbcf9281f5ee88bb7be113dd51e1237f1c4b8`  
		Last Modified: Wed, 08 Nov 2023 00:45:23 GMT  
		Size: 219.6 MB (219607112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e024eac15856bbec7f25f475d3c1810249d92b2608024fd861df2de7af7dd`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 2.6 MB (2628109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eee1f11dc9d1c4617dcf3d9bf6d5368df3304931f6c41b3318eb2bf05ef1605`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 459.5 KB (459516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5664216242bf54355d10ca6a7af8c24bee982070f72045ce26f3586c6d132aa2`  
		Last Modified: Tue, 14 Nov 2023 01:49:50 GMT  
		Size: 323.1 MB (323084359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d30b6bafd07d0ecfc8a000350839fa8548719d7bd0bad80cc09e2c63be2e20`  
		Last Modified: Tue, 14 Nov 2023 01:49:15 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f2134e2f2e688e162c83ea1d57370fc3e6496326c64cdcd4ca55d2a7ea80c9`  
		Last Modified: Tue, 14 Nov 2023 01:49:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651d62d043b824d6d7c2d2d543d5ff41faa190b3fa4497d694685b326e80619`  
		Last Modified: Tue, 14 Nov 2023 01:49:15 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333775c4dea98d4bbdf6c0090a73f927322cfd5ecc132c716dfaa9bb5c44c2d3`  
		Last Modified: Tue, 14 Nov 2023 01:49:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:26c2150d81e20760d93ea2ef38be3c2823814e2ae83382173d68de066426d911
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572792791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015469bef4a58eaa7b4390f7619903866e1a48f66afe18a8b2f3f56aca54fc96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Tue, 07 Nov 2023 23:48:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Nov 2023 23:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Nov 2023 23:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Nov 2023 23:48:30 GMT
ARG TARGETARCH
# Tue, 07 Nov 2023 23:49:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 07 Nov 2023 23:49:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Nov 2023 23:49:48 GMT
RUN npm install -g rtlcss
# Tue, 07 Nov 2023 23:49:48 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 Nov 2023 00:56:03 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 00:56:03 GMT
ARG ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
# Tue, 14 Nov 2023 00:57:15 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 00:57:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 00:57:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 00:57:22 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 00:57:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 00:57:22 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 00:57:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 00:57:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 00:57:22 GMT
USER odoo
# Tue, 14 Nov 2023 00:57:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 00:57:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5812a002d612ea362d56834609da19cbf53fb331e9f92b0b4b8d1cdd3b8aa9`  
		Last Modified: Tue, 07 Nov 2023 23:51:50 GMT  
		Size: 216.9 MB (216907690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59eaf6b2e981344b7a4bf54a869a293a9e69d429da23202eed603c8f1f41835`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 2.6 MB (2634000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd2aeeb4414cf9678f9200a368d1873d1290880b10ec32b5a9264ae836d479b`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 459.4 KB (459450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdf05cdc5b9b591787678961a1ec1aec071c1057eed23c306d8c0040718da8e`  
		Last Modified: Tue, 14 Nov 2023 00:58:44 GMT  
		Size: 322.7 MB (322725284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b14bf046a1e125c9aac7baff7af0f75345f5268208d4912f510efa3bf78ca1`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0bf7919c61b58c943d6cc0bc1f5767a8b57ababbc7ec2a289f96df06fdcfef`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fef3fc627836546c092799bf908950736a43620096addd06b21433525e99e3`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c64b7c90c1c37cb6c8832b41e9dab9a67a8fb0252dc2e633be3cee0fba0493`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:beaee16012141c50a842c5c41b9b007212c0e2c106b8de30289362d7fc1d45b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591736649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6b62f6bd23ec3806041c7b27fd34d9bbc00fbdcfaa3720daef56d4a5e0eb29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:09 GMT
ADD file:a935b2993c62bfb1ade6ba0ffcf1f955422f6f76c63a723877d4bca5bb2aff7b in / 
# Wed, 01 Nov 2023 00:22:11 GMT
CMD ["bash"]
# Wed, 08 Nov 2023 00:35:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Nov 2023 00:35:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Nov 2023 00:35:12 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:35:13 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:37:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:38:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:38:10 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:38:10 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 Nov 2023 01:25:27 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 01:25:27 GMT
ARG ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
# Tue, 14 Nov 2023 01:27:43 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 01:27:55 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 01:27:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 01:27:57 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 01:27:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 01:27:59 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 01:27:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 01:28:00 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 01:28:00 GMT
USER odoo
# Tue, 14 Nov 2023 01:28:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 01:28:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c4a0eee30f72e7c0e9938500fbc7f30b5eb02d04d49bfe7f18a17af1a6d82f81`  
		Last Modified: Wed, 01 Nov 2023 00:26:59 GMT  
		Size: 35.3 MB (35293810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbf24c6962f4383105fa75766afb1694587cd6eee6991d84986cc06060d14b0`  
		Last Modified: Wed, 08 Nov 2023 00:41:30 GMT  
		Size: 228.6 MB (228597689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2525c03537826015f6883a915c56344809b0b4d609d0331aa7496a6133c9a0d4`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 2.9 MB (2874169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f399970742679afbe633c65177cfcac0bc40ea17093cf32acf0175b1c765b8a`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 459.5 KB (459462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae85ed78ced3e415d1336bdd6594b66fe0422c5c7467c0384056baaa544cb07`  
		Last Modified: Tue, 14 Nov 2023 01:30:01 GMT  
		Size: 324.5 MB (324509058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ae9d3419ee6cee380d568782b0db7fea2880e7e8253d9725ee9ecfe6d452d0`  
		Last Modified: Tue, 14 Nov 2023 01:29:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44071f01c77e9d2235c326911cfb2415b910818fb3538c8eba60056fe1c3f499`  
		Last Modified: Tue, 14 Nov 2023 01:29:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ed20f9c194f510c0d83ef5a68ce95632c80b7cf957950c1f2221629914a231`  
		Last Modified: Tue, 14 Nov 2023 01:29:17 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afcc8c4c16f78cde13fdefc998fe1b3448c091d11e7e8b637096dff16923d29`  
		Last Modified: Tue, 14 Nov 2023 01:29:17 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:8c4feb44dd6581b9d41ecd87e0a6345f6277a7c391a7b824c340ff9c90ee488a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:224afec587448938f248e5f7cce715e573e27020a840b3268b497d06aaa60c46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.2 MB (577199471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14fbcf2831eb734c4a01194f91413cfe3771b36c58b4c8c1ac6f946534eb97d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 11:59:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Nov 2023 11:59:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Nov 2023 11:59:56 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:38:54 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:40:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:40:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:40:19 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:40:19 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 Nov 2023 01:45:16 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 01:45:16 GMT
ARG ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
# Tue, 14 Nov 2023 01:46:36 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 01:46:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 01:46:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 01:46:39 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 01:46:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 01:46:39 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 01:46:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 01:46:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 01:46:39 GMT
USER odoo
# Tue, 14 Nov 2023 01:46:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 01:46:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3abf7b1c0fb11700caf26b92dbcf9281f5ee88bb7be113dd51e1237f1c4b8`  
		Last Modified: Wed, 08 Nov 2023 00:45:23 GMT  
		Size: 219.6 MB (219607112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2e024eac15856bbec7f25f475d3c1810249d92b2608024fd861df2de7af7dd`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 2.6 MB (2628109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eee1f11dc9d1c4617dcf3d9bf6d5368df3304931f6c41b3318eb2bf05ef1605`  
		Last Modified: Wed, 08 Nov 2023 00:44:59 GMT  
		Size: 459.5 KB (459516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5664216242bf54355d10ca6a7af8c24bee982070f72045ce26f3586c6d132aa2`  
		Last Modified: Tue, 14 Nov 2023 01:49:50 GMT  
		Size: 323.1 MB (323084359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d30b6bafd07d0ecfc8a000350839fa8548719d7bd0bad80cc09e2c63be2e20`  
		Last Modified: Tue, 14 Nov 2023 01:49:15 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f2134e2f2e688e162c83ea1d57370fc3e6496326c64cdcd4ca55d2a7ea80c9`  
		Last Modified: Tue, 14 Nov 2023 01:49:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6651d62d043b824d6d7c2d2d543d5ff41faa190b3fa4497d694685b326e80619`  
		Last Modified: Tue, 14 Nov 2023 01:49:15 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333775c4dea98d4bbdf6c0090a73f927322cfd5ecc132c716dfaa9bb5c44c2d3`  
		Last Modified: Tue, 14 Nov 2023 01:49:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:26c2150d81e20760d93ea2ef38be3c2823814e2ae83382173d68de066426d911
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572792791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015469bef4a58eaa7b4390f7619903866e1a48f66afe18a8b2f3f56aca54fc96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:55 GMT
ADD file:99dc83e8bb8c67d9179a265fb750c76f73fa660e13e938b6cd613be653cd077e in / 
# Wed, 01 Nov 2023 00:39:56 GMT
CMD ["bash"]
# Tue, 07 Nov 2023 23:48:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 07 Nov 2023 23:48:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 07 Nov 2023 23:48:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Nov 2023 23:48:30 GMT
ARG TARGETARCH
# Tue, 07 Nov 2023 23:49:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 07 Nov 2023 23:49:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Nov 2023 23:49:48 GMT
RUN npm install -g rtlcss
# Tue, 07 Nov 2023 23:49:48 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 Nov 2023 00:56:03 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 00:56:03 GMT
ARG ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
# Tue, 14 Nov 2023 00:57:15 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 00:57:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 00:57:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 00:57:22 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 00:57:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 00:57:22 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 00:57:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 00:57:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 00:57:22 GMT
USER odoo
# Tue, 14 Nov 2023 00:57:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 00:57:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6e498137f0ed1053c364a5c8a688616b4abee72496a0b97cc71ea5e603565070`  
		Last Modified: Wed, 01 Nov 2023 00:43:46 GMT  
		Size: 30.1 MB (30063905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5812a002d612ea362d56834609da19cbf53fb331e9f92b0b4b8d1cdd3b8aa9`  
		Last Modified: Tue, 07 Nov 2023 23:51:50 GMT  
		Size: 216.9 MB (216907690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59eaf6b2e981344b7a4bf54a869a293a9e69d429da23202eed603c8f1f41835`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 2.6 MB (2634000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd2aeeb4414cf9678f9200a368d1873d1290880b10ec32b5a9264ae836d479b`  
		Last Modified: Tue, 07 Nov 2023 23:51:32 GMT  
		Size: 459.4 KB (459450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdf05cdc5b9b591787678961a1ec1aec071c1057eed23c306d8c0040718da8e`  
		Last Modified: Tue, 14 Nov 2023 00:58:44 GMT  
		Size: 322.7 MB (322725284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b14bf046a1e125c9aac7baff7af0f75345f5268208d4912f510efa3bf78ca1`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0bf7919c61b58c943d6cc0bc1f5767a8b57ababbc7ec2a289f96df06fdcfef`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fef3fc627836546c092799bf908950736a43620096addd06b21433525e99e3`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c64b7c90c1c37cb6c8832b41e9dab9a67a8fb0252dc2e633be3cee0fba0493`  
		Last Modified: Tue, 14 Nov 2023 00:58:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:beaee16012141c50a842c5c41b9b007212c0e2c106b8de30289362d7fc1d45b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.7 MB (591736649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6b62f6bd23ec3806041c7b27fd34d9bbc00fbdcfaa3720daef56d4a5e0eb29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Nov 2023 00:22:09 GMT
ADD file:a935b2993c62bfb1ade6ba0ffcf1f955422f6f76c63a723877d4bca5bb2aff7b in / 
# Wed, 01 Nov 2023 00:22:11 GMT
CMD ["bash"]
# Wed, 08 Nov 2023 00:35:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Nov 2023 00:35:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Nov 2023 00:35:12 GMT
ENV LANG=C.UTF-8
# Wed, 08 Nov 2023 00:35:13 GMT
ARG TARGETARCH
# Wed, 08 Nov 2023 00:37:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 08 Nov 2023 00:38:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 08 Nov 2023 00:38:10 GMT
RUN npm install -g rtlcss
# Wed, 08 Nov 2023 00:38:10 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 Nov 2023 01:25:27 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 01:25:27 GMT
ARG ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
# Tue, 14 Nov 2023 01:27:43 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 01:27:55 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 01:27:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 01:27:57 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=32bcde397225f27f01874218e43d55e70bd61814
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 01:27:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 01:27:59 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 01:27:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 01:28:00 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 01:28:00 GMT
USER odoo
# Tue, 14 Nov 2023 01:28:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 01:28:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c4a0eee30f72e7c0e9938500fbc7f30b5eb02d04d49bfe7f18a17af1a6d82f81`  
		Last Modified: Wed, 01 Nov 2023 00:26:59 GMT  
		Size: 35.3 MB (35293810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbf24c6962f4383105fa75766afb1694587cd6eee6991d84986cc06060d14b0`  
		Last Modified: Wed, 08 Nov 2023 00:41:30 GMT  
		Size: 228.6 MB (228597689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2525c03537826015f6883a915c56344809b0b4d609d0331aa7496a6133c9a0d4`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 2.9 MB (2874169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f399970742679afbe633c65177cfcac0bc40ea17093cf32acf0175b1c765b8a`  
		Last Modified: Wed, 08 Nov 2023 00:41:01 GMT  
		Size: 459.5 KB (459462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae85ed78ced3e415d1336bdd6594b66fe0422c5c7467c0384056baaa544cb07`  
		Last Modified: Tue, 14 Nov 2023 01:30:01 GMT  
		Size: 324.5 MB (324509058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ae9d3419ee6cee380d568782b0db7fea2880e7e8253d9725ee9ecfe6d452d0`  
		Last Modified: Tue, 14 Nov 2023 01:29:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44071f01c77e9d2235c326911cfb2415b910818fb3538c8eba60056fe1c3f499`  
		Last Modified: Tue, 14 Nov 2023 01:29:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ed20f9c194f510c0d83ef5a68ce95632c80b7cf957950c1f2221629914a231`  
		Last Modified: Tue, 14 Nov 2023 01:29:17 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afcc8c4c16f78cde13fdefc998fe1b3448c091d11e7e8b637096dff16923d29`  
		Last Modified: Tue, 14 Nov 2023 01:29:17 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:92bb6095ddcc2a6ab16645d988dfb4b2e61444a6371a20706d32f6b27904192b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:a7f60b1963ab43824ea42c1af5b42b4c52db8d65ec7af41a4f9e69a646b6ba62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.6 MB (592612047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7170d39c241047d94ec39e68cea318800116523bcfa6077f5524a0c8a3180eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:38:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:38:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:38:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:38:22 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:40:32 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:43:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:43:14 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:43:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 14 Nov 2023 01:43:14 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 01:43:14 GMT
ARG ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
# Tue, 14 Nov 2023 01:45:02 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 01:45:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 01:45:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 01:45:05 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 01:45:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 01:45:05 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 01:45:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 01:45:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 01:45:05 GMT
USER odoo
# Tue, 14 Nov 2023 01:45:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 01:45:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb3c31d88935a4bd21fe72cde4d10cf70f938ed370d1589f5afe78de8e9d5ef`  
		Last Modified: Tue, 14 Nov 2023 01:48:55 GMT  
		Size: 236.0 MB (236000929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1635e6cd9216147592a4196f3bd6dbd96074a19264c7ec0d1ebca064d6810ba5`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 2.5 MB (2526404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ce7265beed021294fe7c29a3a1bc47a0ccdcda030d1d53cbc088171441d3a8`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 460.6 KB (460559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491ed2407f72c50f82b88a57800e72be5c1af72ca4e45cc484dfae6634cd0030`  
		Last Modified: Tue, 14 Nov 2023 01:49:03 GMT  
		Size: 323.2 MB (323182579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543221c1238d6ee3186b24846b8c7e021f8bd44f3958d7454dfa4999d7cdea95`  
		Last Modified: Tue, 14 Nov 2023 01:48:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d25bfe6e40b514a7fd70cade9dc301affe022bde8ef3eaa213a722bc9129f1`  
		Last Modified: Tue, 14 Nov 2023 01:48:26 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338da5921028da41ae6a32bd5b0c01eac9bbef08954048427d0557332acab111`  
		Last Modified: Tue, 14 Nov 2023 01:48:26 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9683ec1a4254f4c829b1dd646c10b6d49dd3945a537dfad7f990c292207feb90`  
		Last Modified: Tue, 14 Nov 2023 01:48:26 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ace6418846e2418f335ebb344cde203804b3c7d7805b2725dcfc9a9add4ca940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.4 MB (587401328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7106e5398bb060deb25fbf804f531529370f2516531f15ff023a807a809a6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 00:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 00:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 00:50:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 00:50:56 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 00:53:29 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 00:53:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 00:53:44 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 00:53:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 14 Nov 2023 00:53:44 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 00:53:44 GMT
ARG ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
# Tue, 14 Nov 2023 00:55:41 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 00:55:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 00:55:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 00:55:48 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 00:55:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 00:55:49 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 00:55:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 00:55:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 00:55:49 GMT
USER odoo
# Tue, 14 Nov 2023 00:55:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 00:55:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab1126a28686b8ed5fe7ce9c231b2feaf2464bfdd4c69292a490627f6d3e9e`  
		Last Modified: Tue, 14 Nov 2023 00:57:54 GMT  
		Size: 233.2 MB (233245340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac61d67d73d062d91830915181a68ab467f4aec863686610d5655f2baa622d55`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 2.5 MB (2520327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50a0b71d2c501c8759efe323740bae5ad9e3440515f38b9963427218127ac5b`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 460.5 KB (460530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cce5f2a0c53a04404cd97f574d6ca67a2a85cbd2e66097307815e57487c0a4`  
		Last Modified: Tue, 14 Nov 2023 00:58:02 GMT  
		Size: 322.8 MB (322780729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524cd683dc13eb9d4acc94b4f4f7f8fe90f1ffd93bf20cb717305ed27c3d7309`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94974e1c2b8342a72e8fb852853aa86d67311a9249009ac2d4b3bf9fc8299a24`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1aee512583463453d60c93a2f72efbd2848ae464cea90e3242a994c9bc594a`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb06a82b5f82620d2831d2e5586afc5df36e67401451e0e71b07578a531b270`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:3002afaed2d6e2c48a73d012ae1cd5b1b3cc0dd05fd85cd5e47e3664f31d2dfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.8 MB (609798496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55da3a17b8f221b13a8e17342e69551856e7e72d89a47fea7206b50303cc296c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:16:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:16:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:16:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:16:49 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:21:28 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:21:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:21:53 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:21:54 GMT
ENV ODOO_VERSION=17.0
# Tue, 14 Nov 2023 01:21:54 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 01:21:55 GMT
ARG ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
# Tue, 14 Nov 2023 01:24:57 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 01:25:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 01:25:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 01:25:19 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 01:25:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 01:25:20 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 01:25:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 01:25:21 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 01:25:21 GMT
USER odoo
# Tue, 14 Nov 2023 01:25:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 01:25:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff961ccf5729ac1f3c5d8b7806dd42fa9a9fbc4083f43b7d5bc3b9bbc166edbd`  
		Last Modified: Tue, 14 Nov 2023 01:28:59 GMT  
		Size: 245.9 MB (245927069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6d3d2526a589659b9a531e4540bfd3bd343c49e9845f1409f5d7b12f7cca3`  
		Last Modified: Tue, 14 Nov 2023 01:28:17 GMT  
		Size: 2.8 MB (2803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bc659a5b58234fbb32ee9ced616e815875a88f93489359a4f37bacad64bf54`  
		Last Modified: Tue, 14 Nov 2023 01:28:16 GMT  
		Size: 460.5 KB (460495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699253e3275c43b2824531f8a6ec7d964dd806c9689e08950fc87e2f55d75d2c`  
		Last Modified: Tue, 14 Nov 2023 01:29:02 GMT  
		Size: 324.9 MB (324922432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f52d71a90a9d08bebf746f36ced6f7187a3d3f34b6f59205d84f4efacbd2759`  
		Last Modified: Tue, 14 Nov 2023 01:28:14 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496783b8a9da9a483affa25433c2d462cde89298429b70e4a5feba70a6d13cb8`  
		Last Modified: Tue, 14 Nov 2023 01:28:14 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb06de6182b184d9b59712ae21dff73450c84fc93987eec27c5e1b6e1d5d0c`  
		Last Modified: Tue, 14 Nov 2023 01:28:14 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a891f6e50ffcdda3d9390c1c535ab37e48e760cb2f0d69f698009e82493c054b`  
		Last Modified: Tue, 14 Nov 2023 01:28:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:92bb6095ddcc2a6ab16645d988dfb4b2e61444a6371a20706d32f6b27904192b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:a7f60b1963ab43824ea42c1af5b42b4c52db8d65ec7af41a4f9e69a646b6ba62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.6 MB (592612047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7170d39c241047d94ec39e68cea318800116523bcfa6077f5524a0c8a3180eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:38:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:38:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:38:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:38:22 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:40:32 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:43:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:43:14 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:43:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 14 Nov 2023 01:43:14 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 01:43:14 GMT
ARG ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
# Tue, 14 Nov 2023 01:45:02 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 01:45:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 01:45:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 01:45:05 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 01:45:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 01:45:05 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 01:45:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 01:45:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 01:45:05 GMT
USER odoo
# Tue, 14 Nov 2023 01:45:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 01:45:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb3c31d88935a4bd21fe72cde4d10cf70f938ed370d1589f5afe78de8e9d5ef`  
		Last Modified: Tue, 14 Nov 2023 01:48:55 GMT  
		Size: 236.0 MB (236000929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1635e6cd9216147592a4196f3bd6dbd96074a19264c7ec0d1ebca064d6810ba5`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 2.5 MB (2526404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ce7265beed021294fe7c29a3a1bc47a0ccdcda030d1d53cbc088171441d3a8`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 460.6 KB (460559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491ed2407f72c50f82b88a57800e72be5c1af72ca4e45cc484dfae6634cd0030`  
		Last Modified: Tue, 14 Nov 2023 01:49:03 GMT  
		Size: 323.2 MB (323182579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543221c1238d6ee3186b24846b8c7e021f8bd44f3958d7454dfa4999d7cdea95`  
		Last Modified: Tue, 14 Nov 2023 01:48:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d25bfe6e40b514a7fd70cade9dc301affe022bde8ef3eaa213a722bc9129f1`  
		Last Modified: Tue, 14 Nov 2023 01:48:26 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338da5921028da41ae6a32bd5b0c01eac9bbef08954048427d0557332acab111`  
		Last Modified: Tue, 14 Nov 2023 01:48:26 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9683ec1a4254f4c829b1dd646c10b6d49dd3945a537dfad7f990c292207feb90`  
		Last Modified: Tue, 14 Nov 2023 01:48:26 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ace6418846e2418f335ebb344cde203804b3c7d7805b2725dcfc9a9add4ca940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.4 MB (587401328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7106e5398bb060deb25fbf804f531529370f2516531f15ff023a807a809a6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 00:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 00:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 00:50:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 00:50:56 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 00:53:29 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 00:53:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 00:53:44 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 00:53:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 14 Nov 2023 00:53:44 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 00:53:44 GMT
ARG ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
# Tue, 14 Nov 2023 00:55:41 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 00:55:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 00:55:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 00:55:48 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 00:55:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 00:55:49 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 00:55:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 00:55:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 00:55:49 GMT
USER odoo
# Tue, 14 Nov 2023 00:55:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 00:55:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab1126a28686b8ed5fe7ce9c231b2feaf2464bfdd4c69292a490627f6d3e9e`  
		Last Modified: Tue, 14 Nov 2023 00:57:54 GMT  
		Size: 233.2 MB (233245340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac61d67d73d062d91830915181a68ab467f4aec863686610d5655f2baa622d55`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 2.5 MB (2520327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50a0b71d2c501c8759efe323740bae5ad9e3440515f38b9963427218127ac5b`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 460.5 KB (460530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cce5f2a0c53a04404cd97f574d6ca67a2a85cbd2e66097307815e57487c0a4`  
		Last Modified: Tue, 14 Nov 2023 00:58:02 GMT  
		Size: 322.8 MB (322780729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524cd683dc13eb9d4acc94b4f4f7f8fe90f1ffd93bf20cb717305ed27c3d7309`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94974e1c2b8342a72e8fb852853aa86d67311a9249009ac2d4b3bf9fc8299a24`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1aee512583463453d60c93a2f72efbd2848ae464cea90e3242a994c9bc594a`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb06a82b5f82620d2831d2e5586afc5df36e67401451e0e71b07578a531b270`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:3002afaed2d6e2c48a73d012ae1cd5b1b3cc0dd05fd85cd5e47e3664f31d2dfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.8 MB (609798496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55da3a17b8f221b13a8e17342e69551856e7e72d89a47fea7206b50303cc296c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:16:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:16:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:16:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:16:49 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:21:28 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:21:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:21:53 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:21:54 GMT
ENV ODOO_VERSION=17.0
# Tue, 14 Nov 2023 01:21:54 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 01:21:55 GMT
ARG ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
# Tue, 14 Nov 2023 01:24:57 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 01:25:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 01:25:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 01:25:19 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 01:25:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 01:25:20 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 01:25:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 01:25:21 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 01:25:21 GMT
USER odoo
# Tue, 14 Nov 2023 01:25:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 01:25:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff961ccf5729ac1f3c5d8b7806dd42fa9a9fbc4083f43b7d5bc3b9bbc166edbd`  
		Last Modified: Tue, 14 Nov 2023 01:28:59 GMT  
		Size: 245.9 MB (245927069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6d3d2526a589659b9a531e4540bfd3bd343c49e9845f1409f5d7b12f7cca3`  
		Last Modified: Tue, 14 Nov 2023 01:28:17 GMT  
		Size: 2.8 MB (2803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bc659a5b58234fbb32ee9ced616e815875a88f93489359a4f37bacad64bf54`  
		Last Modified: Tue, 14 Nov 2023 01:28:16 GMT  
		Size: 460.5 KB (460495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699253e3275c43b2824531f8a6ec7d964dd806c9689e08950fc87e2f55d75d2c`  
		Last Modified: Tue, 14 Nov 2023 01:29:02 GMT  
		Size: 324.9 MB (324922432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f52d71a90a9d08bebf746f36ced6f7187a3d3f34b6f59205d84f4efacbd2759`  
		Last Modified: Tue, 14 Nov 2023 01:28:14 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496783b8a9da9a483affa25433c2d462cde89298429b70e4a5feba70a6d13cb8`  
		Last Modified: Tue, 14 Nov 2023 01:28:14 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb06de6182b184d9b59712ae21dff73450c84fc93987eec27c5e1b6e1d5d0c`  
		Last Modified: Tue, 14 Nov 2023 01:28:14 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a891f6e50ffcdda3d9390c1c535ab37e48e760cb2f0d69f698009e82493c054b`  
		Last Modified: Tue, 14 Nov 2023 01:28:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:92bb6095ddcc2a6ab16645d988dfb4b2e61444a6371a20706d32f6b27904192b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:a7f60b1963ab43824ea42c1af5b42b4c52db8d65ec7af41a4f9e69a646b6ba62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.6 MB (592612047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7170d39c241047d94ec39e68cea318800116523bcfa6077f5524a0c8a3180eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:33:30 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:33:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:33:30 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:33:32 GMT
ADD file:63d5ab3ef0aab308c0e71cb67292c5467f60deafa9b0418cbb220affcd078444 in / 
# Thu, 05 Oct 2023 07:33:32 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:38:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:38:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:38:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:38:22 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:40:32 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:43:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:43:14 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:43:14 GMT
ENV ODOO_VERSION=17.0
# Tue, 14 Nov 2023 01:43:14 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 01:43:14 GMT
ARG ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
# Tue, 14 Nov 2023 01:45:02 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 01:45:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 01:45:04 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 01:45:05 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 01:45:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 01:45:05 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 01:45:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 01:45:05 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 01:45:05 GMT
USER odoo
# Tue, 14 Nov 2023 01:45:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 01:45:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:43f89b94cd7df92a2f7e565b8fb1b7f502eff2cd225508cbd7ea2d36a9a3a601`  
		Last Modified: Thu, 05 Oct 2023 08:42:10 GMT  
		Size: 30.4 MB (30439111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb3c31d88935a4bd21fe72cde4d10cf70f938ed370d1589f5afe78de8e9d5ef`  
		Last Modified: Tue, 14 Nov 2023 01:48:55 GMT  
		Size: 236.0 MB (236000929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1635e6cd9216147592a4196f3bd6dbd96074a19264c7ec0d1ebca064d6810ba5`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 2.5 MB (2526404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ce7265beed021294fe7c29a3a1bc47a0ccdcda030d1d53cbc088171441d3a8`  
		Last Modified: Tue, 14 Nov 2023 01:48:28 GMT  
		Size: 460.6 KB (460559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491ed2407f72c50f82b88a57800e72be5c1af72ca4e45cc484dfae6634cd0030`  
		Last Modified: Tue, 14 Nov 2023 01:49:03 GMT  
		Size: 323.2 MB (323182579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543221c1238d6ee3186b24846b8c7e021f8bd44f3958d7454dfa4999d7cdea95`  
		Last Modified: Tue, 14 Nov 2023 01:48:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d25bfe6e40b514a7fd70cade9dc301affe022bde8ef3eaa213a722bc9129f1`  
		Last Modified: Tue, 14 Nov 2023 01:48:26 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338da5921028da41ae6a32bd5b0c01eac9bbef08954048427d0557332acab111`  
		Last Modified: Tue, 14 Nov 2023 01:48:26 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9683ec1a4254f4c829b1dd646c10b6d49dd3945a537dfad7f990c292207feb90`  
		Last Modified: Tue, 14 Nov 2023 01:48:26 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ace6418846e2418f335ebb344cde203804b3c7d7805b2725dcfc9a9add4ca940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.4 MB (587401328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7106e5398bb060deb25fbf804f531529370f2516531f15ff023a807a809a6a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 00:50:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 00:50:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 00:50:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 00:50:56 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 00:53:29 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 00:53:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 00:53:44 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 00:53:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 14 Nov 2023 00:53:44 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 00:53:44 GMT
ARG ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
# Tue, 14 Nov 2023 00:55:41 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 00:55:48 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 00:55:48 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 00:55:48 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 00:55:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 00:55:49 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 00:55:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 00:55:49 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 00:55:49 GMT
USER odoo
# Tue, 14 Nov 2023 00:55:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 00:55:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab1126a28686b8ed5fe7ce9c231b2feaf2464bfdd4c69292a490627f6d3e9e`  
		Last Modified: Tue, 14 Nov 2023 00:57:54 GMT  
		Size: 233.2 MB (233245340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac61d67d73d062d91830915181a68ab467f4aec863686610d5655f2baa622d55`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 2.5 MB (2520327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50a0b71d2c501c8759efe323740bae5ad9e3440515f38b9963427218127ac5b`  
		Last Modified: Tue, 14 Nov 2023 00:57:35 GMT  
		Size: 460.5 KB (460530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cce5f2a0c53a04404cd97f574d6ca67a2a85cbd2e66097307815e57487c0a4`  
		Last Modified: Tue, 14 Nov 2023 00:58:02 GMT  
		Size: 322.8 MB (322780729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524cd683dc13eb9d4acc94b4f4f7f8fe90f1ffd93bf20cb717305ed27c3d7309`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94974e1c2b8342a72e8fb852853aa86d67311a9249009ac2d4b3bf9fc8299a24`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1aee512583463453d60c93a2f72efbd2848ae464cea90e3242a994c9bc594a`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb06a82b5f82620d2831d2e5586afc5df36e67401451e0e71b07578a531b270`  
		Last Modified: Tue, 14 Nov 2023 00:57:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:3002afaed2d6e2c48a73d012ae1cd5b1b3cc0dd05fd85cd5e47e3664f31d2dfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.8 MB (609798496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55da3a17b8f221b13a8e17342e69551856e7e72d89a47fea7206b50303cc296c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 01:16:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 Nov 2023 01:16:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 Nov 2023 01:16:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 14 Nov 2023 01:16:49 GMT
ARG TARGETARCH
# Tue, 14 Nov 2023 01:21:28 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 Nov 2023 01:21:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 Nov 2023 01:21:53 GMT
RUN npm install -g rtlcss
# Tue, 14 Nov 2023 01:21:54 GMT
ENV ODOO_VERSION=17.0
# Tue, 14 Nov 2023 01:21:54 GMT
ARG ODOO_RELEASE=20231113
# Tue, 14 Nov 2023 01:21:55 GMT
ARG ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
# Tue, 14 Nov 2023 01:24:57 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 Nov 2023 01:25:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 Nov 2023 01:25:18 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 Nov 2023 01:25:19 GMT
# ARGS: ODOO_RELEASE=20231113 ODOO_SHA=b72a32e3356084adb637334b45b110cdedc8ab0c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 Nov 2023 01:25:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 Nov 2023 01:25:20 GMT
EXPOSE 8069 8071 8072
# Tue, 14 Nov 2023 01:25:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 Nov 2023 01:25:21 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 Nov 2023 01:25:21 GMT
USER odoo
# Tue, 14 Nov 2023 01:25:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Nov 2023 01:25:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff961ccf5729ac1f3c5d8b7806dd42fa9a9fbc4083f43b7d5bc3b9bbc166edbd`  
		Last Modified: Tue, 14 Nov 2023 01:28:59 GMT  
		Size: 245.9 MB (245927069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6d3d2526a589659b9a531e4540bfd3bd343c49e9845f1409f5d7b12f7cca3`  
		Last Modified: Tue, 14 Nov 2023 01:28:17 GMT  
		Size: 2.8 MB (2803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bc659a5b58234fbb32ee9ced616e815875a88f93489359a4f37bacad64bf54`  
		Last Modified: Tue, 14 Nov 2023 01:28:16 GMT  
		Size: 460.5 KB (460495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699253e3275c43b2824531f8a6ec7d964dd806c9689e08950fc87e2f55d75d2c`  
		Last Modified: Tue, 14 Nov 2023 01:29:02 GMT  
		Size: 324.9 MB (324922432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f52d71a90a9d08bebf746f36ced6f7187a3d3f34b6f59205d84f4efacbd2759`  
		Last Modified: Tue, 14 Nov 2023 01:28:14 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496783b8a9da9a483affa25433c2d462cde89298429b70e4a5feba70a6d13cb8`  
		Last Modified: Tue, 14 Nov 2023 01:28:14 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb06de6182b184d9b59712ae21dff73450c84fc93987eec27c5e1b6e1d5d0c`  
		Last Modified: Tue, 14 Nov 2023 01:28:14 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a891f6e50ffcdda3d9390c1c535ab37e48e760cb2f0d69f698009e82493c054b`  
		Last Modified: Tue, 14 Nov 2023 01:28:14 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
