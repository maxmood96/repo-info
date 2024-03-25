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
$ docker pull odoo@sha256:e7a8f51be2cc271bc7d08fea2f04ba8d4825d4204cdba61a511b1022a0e1927b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:2ef4ec666209e6c0b3c70e64428664bf468819dba88e877daf3c99ebafff076c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (564015752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249baf3a8084b70f09ae671c3f39f7f9033a3f4857517b6881fc448520168ce4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 10:04:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 10:04:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 10:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 10:08:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 10:08:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:08:17 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 10:08:17 GMT
ENV ODOO_VERSION=15.0
# Mon, 25 Mar 2024 20:17:23 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 20:17:23 GMT
ARG ODOO_SHA=9a4e3ff382fef0e15308aa124a42952fc0f8d254
# Mon, 25 Mar 2024 20:18:34 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=9a4e3ff382fef0e15308aa124a42952fc0f8d254
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 20:18:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 20:18:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 20:18:38 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=9a4e3ff382fef0e15308aa124a42952fc0f8d254
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 20:18:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 20:18:39 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 20:18:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 20:18:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 20:18:39 GMT
USER odoo
# Mon, 25 Mar 2024 20:18:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:18:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f755211239ff95827bdf02a4263220ef29f30514bfb45e9719405f61b7eb1fe`  
		Last Modified: Tue, 12 Mar 2024 10:11:05 GMT  
		Size: 220.3 MB (220291492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e350755bf81273bed12fdf2a9b0164c28be00db54322cbca54eb5c183aa61798`  
		Last Modified: Tue, 12 Mar 2024 10:10:40 GMT  
		Size: 2.6 MB (2625910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1465eacd304d72395092a950bf1096c7504f0a76ef0820999e0bda4a3e4068ea`  
		Last Modified: Tue, 12 Mar 2024 10:10:40 GMT  
		Size: 462.5 KB (462463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6388baf94582edc26151abbb0d0bbfb40b9f3886786c33343aa8c0bba7f08123`  
		Last Modified: Mon, 25 Mar 2024 20:21:06 GMT  
		Size: 309.2 MB (309210938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a23c575a16fb1147073414d54c3b7edb597a086a1fede2f190971a2a982a8c4`  
		Last Modified: Mon, 25 Mar 2024 20:20:33 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0911b165ff4a806e472a6bccbaf2b5dc23d830cd820b83c424abe305875784`  
		Last Modified: Mon, 25 Mar 2024 20:20:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4077ad4bb02ed77ee25b0b7028768d28f8f5acda50d7c9b2c6d48fa311124721`  
		Last Modified: Mon, 25 Mar 2024 20:20:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566afe25af9ff7e94ff9c69a89f7f2e3d1ae963ff13fe0f619480c228f61263f`  
		Last Modified: Mon, 25 Mar 2024 20:20:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:e7a8f51be2cc271bc7d08fea2f04ba8d4825d4204cdba61a511b1022a0e1927b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:2ef4ec666209e6c0b3c70e64428664bf468819dba88e877daf3c99ebafff076c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (564015752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249baf3a8084b70f09ae671c3f39f7f9033a3f4857517b6881fc448520168ce4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 10:04:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 10:04:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 10:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 10:08:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 10:08:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:08:17 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 10:08:17 GMT
ENV ODOO_VERSION=15.0
# Mon, 25 Mar 2024 20:17:23 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 20:17:23 GMT
ARG ODOO_SHA=9a4e3ff382fef0e15308aa124a42952fc0f8d254
# Mon, 25 Mar 2024 20:18:34 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=9a4e3ff382fef0e15308aa124a42952fc0f8d254
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 20:18:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 20:18:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 20:18:38 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=9a4e3ff382fef0e15308aa124a42952fc0f8d254
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 20:18:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 20:18:39 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 20:18:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 20:18:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 20:18:39 GMT
USER odoo
# Mon, 25 Mar 2024 20:18:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:18:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f755211239ff95827bdf02a4263220ef29f30514bfb45e9719405f61b7eb1fe`  
		Last Modified: Tue, 12 Mar 2024 10:11:05 GMT  
		Size: 220.3 MB (220291492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e350755bf81273bed12fdf2a9b0164c28be00db54322cbca54eb5c183aa61798`  
		Last Modified: Tue, 12 Mar 2024 10:10:40 GMT  
		Size: 2.6 MB (2625910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1465eacd304d72395092a950bf1096c7504f0a76ef0820999e0bda4a3e4068ea`  
		Last Modified: Tue, 12 Mar 2024 10:10:40 GMT  
		Size: 462.5 KB (462463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6388baf94582edc26151abbb0d0bbfb40b9f3886786c33343aa8c0bba7f08123`  
		Last Modified: Mon, 25 Mar 2024 20:21:06 GMT  
		Size: 309.2 MB (309210938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a23c575a16fb1147073414d54c3b7edb597a086a1fede2f190971a2a982a8c4`  
		Last Modified: Mon, 25 Mar 2024 20:20:33 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0911b165ff4a806e472a6bccbaf2b5dc23d830cd820b83c424abe305875784`  
		Last Modified: Mon, 25 Mar 2024 20:20:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4077ad4bb02ed77ee25b0b7028768d28f8f5acda50d7c9b2c6d48fa311124721`  
		Last Modified: Mon, 25 Mar 2024 20:20:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566afe25af9ff7e94ff9c69a89f7f2e3d1ae963ff13fe0f619480c228f61263f`  
		Last Modified: Mon, 25 Mar 2024 20:20:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:3f918d6a670648954d5afbc204ccebdc2ec6ab1af1fd87dccd37e84dde5f70b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:e72dc6cfbbdece0e9351c90d35556113447133822c4999112f5bc245fc5feeb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.9 MB (582947372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cea8320b2ed870091910aa4e4bd2fc267436dd4697ff752216c86cf87c9f257`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 10:04:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 10:04:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 10:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 10:04:23 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 10:05:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 10:05:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:05:44 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 10:05:44 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Mar 2024 20:15:44 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 20:15:44 GMT
ARG ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
# Mon, 25 Mar 2024 20:17:01 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 20:17:05 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 20:17:05 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 20:17:05 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 20:17:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 20:17:05 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 20:17:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 20:17:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 20:17:06 GMT
USER odoo
# Mon, 25 Mar 2024 20:17:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:17:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b6792aa9ce6832f860c6e1be9f969760839af537e4898318aa4f6bfb1c028b`  
		Last Modified: Tue, 12 Mar 2024 10:10:15 GMT  
		Size: 219.6 MB (219603015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2315d87d3b1baf540e35d3ecccceacc3315ff5069bf3f9bfa9cfb289aeba9`  
		Last Modified: Tue, 12 Mar 2024 10:09:51 GMT  
		Size: 2.6 MB (2630018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075dda5b3fd48c7f6681e64745ee86cffaf18fee97aeba54f00d6ee06b5ba526`  
		Last Modified: Tue, 12 Mar 2024 10:09:50 GMT  
		Size: 462.5 KB (462467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6d096ce3e4770dc95ee2ad02a89924aab0d7d3a9a994ff6eeba7ba9e056a67`  
		Last Modified: Mon, 25 Mar 2024 20:20:25 GMT  
		Size: 328.8 MB (328826920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ac257d759350608ecaec6ab4b5c8a13bb9b794e427608461106e85db07d790`  
		Last Modified: Mon, 25 Mar 2024 20:19:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d48b0db2a5bd0ec3b9cea387ec67e2d456a3e2aa8bbfafa0f830ce87bdca6a2`  
		Last Modified: Mon, 25 Mar 2024 20:19:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23271f3da294315d71af76c1f42bd38d7b57306c4820de63c471631d0b663907`  
		Last Modified: Mon, 25 Mar 2024 20:19:45 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c347909c0ba300025339f578c639a70286daeb64d3c91c3668136f1e110849b`  
		Last Modified: Mon, 25 Mar 2024 20:19:45 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c0148af49e02249cf864a22a63fb3c830b258b4b8581a575d106954b3746687d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578565774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b8151d056dd8785a4cba69cbb80cba797bfc95b7d035be94dd126d757a6083`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:09:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 07:09:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 07:09:25 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 07:09:25 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 07:10:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 07:10:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:10:43 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 07:10:44 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Mar 2024 20:19:05 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 20:19:05 GMT
ARG ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
# Mon, 25 Mar 2024 20:20:23 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 20:20:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 20:20:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 20:20:30 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 20:20:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 20:20:30 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 20:20:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 20:20:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 20:20:30 GMT
USER odoo
# Mon, 25 Mar 2024 20:20:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:20:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550bf50c1c5bb03f8258887877b215242f2faaca6547d16135a1e15bf67c37da`  
		Last Modified: Tue, 12 Mar 2024 07:12:44 GMT  
		Size: 216.9 MB (216903519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba8867a1af5f453861e2f8e8ef6fff1ed5ff0485d4380aeb1760a3ee61ddfa`  
		Last Modified: Tue, 12 Mar 2024 07:12:27 GMT  
		Size: 2.6 MB (2635199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd44908863b6493f4ab93ee84278d19411f9365e54dc4f97fd93f6e872c6df`  
		Last Modified: Tue, 12 Mar 2024 07:12:26 GMT  
		Size: 462.5 KB (462480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3bc679128af4496ae94fd8728d85861c88a65a93cce2c76b03cbad55afffcc`  
		Last Modified: Mon, 25 Mar 2024 20:22:01 GMT  
		Size: 328.5 MB (328490998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1213e45211f33bac6457166f503d5d2018a424c88e66150e895384e654bd47dc`  
		Last Modified: Mon, 25 Mar 2024 20:21:31 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3bcf715d36fa5acc81301aa99ec9712c1e7d66b7e90704aaf80e621b23e529`  
		Last Modified: Mon, 25 Mar 2024 20:21:31 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f4f44e63d94183aceda9dc250f82eda07e604195a7c27149c954b1f13f73c2`  
		Last Modified: Mon, 25 Mar 2024 20:21:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d1e3db3ba11fbe9b29f4067cdea78170c4d9097c85277c3d1bf9d07aac7126`  
		Last Modified: Mon, 25 Mar 2024 20:21:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:c343ae22cc923f78006322686aea8578b7b414dc030e4c3aeecadbee7b5e2afb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.5 MB (597508154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8868b66c5f794fcac99fb0d108cbd92b35efd94d23561e2f5553aeeac0e18ab3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 00:31:08 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Tue, 12 Mar 2024 00:31:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:38:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 02:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 02:38:45 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 02:38:47 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 02:45:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 02:46:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:46:11 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 02:46:12 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Mar 2024 19:37:28 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 19:37:28 GMT
ARG ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
# Mon, 25 Mar 2024 19:39:42 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 19:39:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 19:39:57 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 19:39:58 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 19:39:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 19:40:00 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 19:40:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 19:40:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 19:40:02 GMT
USER odoo
# Mon, 25 Mar 2024 19:40:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 19:40:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1a32c556380680a1795889bca44d0f0a883f42b50860b84f480546468a7a03`  
		Last Modified: Tue, 12 Mar 2024 02:54:00 GMT  
		Size: 228.6 MB (228600421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c60f6a8d0d4afdc1ff134aae19e82a3c10cbeb5816bcab9c7cdac58ff961e6`  
		Last Modified: Tue, 12 Mar 2024 02:53:31 GMT  
		Size: 2.9 MB (2876315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec00e5fbd9079a262ec1e1c1ae57ae88ae27282c49b89f9952917db58b01f6b`  
		Last Modified: Tue, 12 Mar 2024 02:53:30 GMT  
		Size: 462.5 KB (462469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a8110aa0caf3590392d392457e96856bc288493008e91cd2a2ad10b2d91696`  
		Last Modified: Mon, 25 Mar 2024 19:42:01 GMT  
		Size: 330.3 MB (330268474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f955229a39f68e08918a5097386b68ff9db0780d49df27478beb4462fc6c871`  
		Last Modified: Mon, 25 Mar 2024 19:41:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cb2ed5ca155ad6d6461467775c1c5b579a62f75154e07c92941fa807666eeb`  
		Last Modified: Mon, 25 Mar 2024 19:41:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d26eca125207290f42da3eb6d86af08007e8381f45c413e3b401d22a9b7873`  
		Last Modified: Mon, 25 Mar 2024 19:41:13 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a41c4ad8a1755fb5f596f9cc73f0eb14a33c59aedb043a234c38be04457880`  
		Last Modified: Mon, 25 Mar 2024 19:41:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:3f918d6a670648954d5afbc204ccebdc2ec6ab1af1fd87dccd37e84dde5f70b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:e72dc6cfbbdece0e9351c90d35556113447133822c4999112f5bc245fc5feeb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.9 MB (582947372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cea8320b2ed870091910aa4e4bd2fc267436dd4697ff752216c86cf87c9f257`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 10:04:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 10:04:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 10:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 10:04:23 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 10:05:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 10:05:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:05:44 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 10:05:44 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Mar 2024 20:15:44 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 20:15:44 GMT
ARG ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
# Mon, 25 Mar 2024 20:17:01 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 20:17:05 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 20:17:05 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 20:17:05 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 20:17:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 20:17:05 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 20:17:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 20:17:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 20:17:06 GMT
USER odoo
# Mon, 25 Mar 2024 20:17:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:17:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b6792aa9ce6832f860c6e1be9f969760839af537e4898318aa4f6bfb1c028b`  
		Last Modified: Tue, 12 Mar 2024 10:10:15 GMT  
		Size: 219.6 MB (219603015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2315d87d3b1baf540e35d3ecccceacc3315ff5069bf3f9bfa9cfb289aeba9`  
		Last Modified: Tue, 12 Mar 2024 10:09:51 GMT  
		Size: 2.6 MB (2630018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075dda5b3fd48c7f6681e64745ee86cffaf18fee97aeba54f00d6ee06b5ba526`  
		Last Modified: Tue, 12 Mar 2024 10:09:50 GMT  
		Size: 462.5 KB (462467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6d096ce3e4770dc95ee2ad02a89924aab0d7d3a9a994ff6eeba7ba9e056a67`  
		Last Modified: Mon, 25 Mar 2024 20:20:25 GMT  
		Size: 328.8 MB (328826920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ac257d759350608ecaec6ab4b5c8a13bb9b794e427608461106e85db07d790`  
		Last Modified: Mon, 25 Mar 2024 20:19:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d48b0db2a5bd0ec3b9cea387ec67e2d456a3e2aa8bbfafa0f830ce87bdca6a2`  
		Last Modified: Mon, 25 Mar 2024 20:19:45 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23271f3da294315d71af76c1f42bd38d7b57306c4820de63c471631d0b663907`  
		Last Modified: Mon, 25 Mar 2024 20:19:45 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c347909c0ba300025339f578c639a70286daeb64d3c91c3668136f1e110849b`  
		Last Modified: Mon, 25 Mar 2024 20:19:45 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c0148af49e02249cf864a22a63fb3c830b258b4b8581a575d106954b3746687d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578565774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b8151d056dd8785a4cba69cbb80cba797bfc95b7d035be94dd126d757a6083`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:09:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 07:09:25 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 07:09:25 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 07:09:25 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 07:10:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 07:10:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:10:43 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 07:10:44 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Mar 2024 20:19:05 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 20:19:05 GMT
ARG ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
# Mon, 25 Mar 2024 20:20:23 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 20:20:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 20:20:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 20:20:30 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 20:20:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 20:20:30 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 20:20:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 20:20:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 20:20:30 GMT
USER odoo
# Mon, 25 Mar 2024 20:20:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:20:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550bf50c1c5bb03f8258887877b215242f2faaca6547d16135a1e15bf67c37da`  
		Last Modified: Tue, 12 Mar 2024 07:12:44 GMT  
		Size: 216.9 MB (216903519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ba8867a1af5f453861e2f8e8ef6fff1ed5ff0485d4380aeb1760a3ee61ddfa`  
		Last Modified: Tue, 12 Mar 2024 07:12:27 GMT  
		Size: 2.6 MB (2635199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fd44908863b6493f4ab93ee84278d19411f9365e54dc4f97fd93f6e872c6df`  
		Last Modified: Tue, 12 Mar 2024 07:12:26 GMT  
		Size: 462.5 KB (462480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3bc679128af4496ae94fd8728d85861c88a65a93cce2c76b03cbad55afffcc`  
		Last Modified: Mon, 25 Mar 2024 20:22:01 GMT  
		Size: 328.5 MB (328490998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1213e45211f33bac6457166f503d5d2018a424c88e66150e895384e654bd47dc`  
		Last Modified: Mon, 25 Mar 2024 20:21:31 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3bcf715d36fa5acc81301aa99ec9712c1e7d66b7e90704aaf80e621b23e529`  
		Last Modified: Mon, 25 Mar 2024 20:21:31 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f4f44e63d94183aceda9dc250f82eda07e604195a7c27149c954b1f13f73c2`  
		Last Modified: Mon, 25 Mar 2024 20:21:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d1e3db3ba11fbe9b29f4067cdea78170c4d9097c85277c3d1bf9d07aac7126`  
		Last Modified: Mon, 25 Mar 2024 20:21:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:c343ae22cc923f78006322686aea8578b7b414dc030e4c3aeecadbee7b5e2afb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.5 MB (597508154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8868b66c5f794fcac99fb0d108cbd92b35efd94d23561e2f5553aeeac0e18ab3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 00:31:08 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Tue, 12 Mar 2024 00:31:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:38:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 02:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 02:38:45 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 02:38:47 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 02:45:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 02:46:07 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:46:11 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 02:46:12 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Mar 2024 19:37:28 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 19:37:28 GMT
ARG ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
# Mon, 25 Mar 2024 19:39:42 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 19:39:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 19:39:57 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 19:39:58 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=88872b9636eae21266c72c95c96d1fc20a9fa9c8
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 19:39:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 19:40:00 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 19:40:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 19:40:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 19:40:02 GMT
USER odoo
# Mon, 25 Mar 2024 19:40:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 19:40:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1a32c556380680a1795889bca44d0f0a883f42b50860b84f480546468a7a03`  
		Last Modified: Tue, 12 Mar 2024 02:54:00 GMT  
		Size: 228.6 MB (228600421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c60f6a8d0d4afdc1ff134aae19e82a3c10cbeb5816bcab9c7cdac58ff961e6`  
		Last Modified: Tue, 12 Mar 2024 02:53:31 GMT  
		Size: 2.9 MB (2876315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec00e5fbd9079a262ec1e1c1ae57ae88ae27282c49b89f9952917db58b01f6b`  
		Last Modified: Tue, 12 Mar 2024 02:53:30 GMT  
		Size: 462.5 KB (462469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a8110aa0caf3590392d392457e96856bc288493008e91cd2a2ad10b2d91696`  
		Last Modified: Mon, 25 Mar 2024 19:42:01 GMT  
		Size: 330.3 MB (330268474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f955229a39f68e08918a5097386b68ff9db0780d49df27478beb4462fc6c871`  
		Last Modified: Mon, 25 Mar 2024 19:41:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cb2ed5ca155ad6d6461467775c1c5b579a62f75154e07c92941fa807666eeb`  
		Last Modified: Mon, 25 Mar 2024 19:41:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d26eca125207290f42da3eb6d86af08007e8381f45c413e3b401d22a9b7873`  
		Last Modified: Mon, 25 Mar 2024 19:41:13 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a41c4ad8a1755fb5f596f9cc73f0eb14a33c59aedb043a234c38be04457880`  
		Last Modified: Mon, 25 Mar 2024 19:41:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:4e748f0b002012da711a9ff21ebe6d4bdb784205016bd04ac7c4830026bc07ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:f247de51bf0bd27033eddb3aa76158d2c645d2cf61c864389cbc8436e97dc946
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.2 MB (601198776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e45d7945bd144b41261f9fda39f2b6b1225374f44bf20a2aba766ce058e6a73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:08:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 03:08:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 03:08:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 03:08:00 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:10:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:10:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:10:22 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:10:23 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Mar 2024 20:13:50 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 20:13:50 GMT
ARG ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
# Mon, 25 Mar 2024 20:15:27 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 20:15:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 20:15:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 20:15:33 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 20:15:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 20:15:33 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 20:15:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 20:15:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 20:15:33 GMT
USER odoo
# Mon, 25 Mar 2024 20:15:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:15:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e6c177fc20fa6387e63fd095d01292bafefb3d6e2ff9cb3e6e8b245a08381`  
		Last Modified: Wed, 06 Mar 2024 03:13:23 GMT  
		Size: 233.7 MB (233723335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3cefe2377c5eb4d88fbf2940f0a9dc339567dfe0c5c28fbc4d821dfa2ecb88`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 2.5 MB (2529426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f541a6d153b3dc5b1c957cef96a47ae608073cb3e26838fa2b35b8ce1455d`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 463.5 KB (463535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8af06cc4793bb719ec879b5341adaf15a265ab59f7b1dcfdaf0b765ad688351`  
		Last Modified: Mon, 25 Mar 2024 20:19:33 GMT  
		Size: 334.0 MB (334028714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ea0e32bd1422ccc747f0bca5a5ede791c8bb751e49db07752f0c733a2384f`  
		Last Modified: Mon, 25 Mar 2024 20:18:55 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8085f62d18ad15f5745dc2c4315ec3c6a05a2acdde8165c37105e65c1172b38d`  
		Last Modified: Mon, 25 Mar 2024 20:18:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068834d6e97533438f89c2da813f4874ac424066326774976b4d9c9995a0dc15`  
		Last Modified: Mon, 25 Mar 2024 20:18:55 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a244eff3b4db5e4f40e8521c00d6593a1a7f6a39fd0c788298773ec4cccdbc9`  
		Last Modified: Mon, 25 Mar 2024 20:18:56 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c8eba87d747dcf5da5e17bef7eed0d69e03e2dd21d5844b47ae54fbb5da739a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.1 MB (596145046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4972616593fbe72a656634bd46cc62262500cee871c767e310b187f8faf6292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:54:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 04:54:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 04:54:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 04:54:11 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 04:56:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 04:56:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:56:24 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 04:56:24 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Mar 2024 20:16:27 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 20:16:27 GMT
ARG ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
# Mon, 25 Mar 2024 20:18:42 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 20:18:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 20:18:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 20:18:50 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 20:18:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 20:18:50 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 20:18:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 20:18:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 20:18:50 GMT
USER odoo
# Mon, 25 Mar 2024 20:18:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:18:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d9a54b231a5bc1f0a4e20302873f08d395effbeb7c781ed9a3c37af48db7c`  
		Last Modified: Wed, 06 Mar 2024 04:58:49 GMT  
		Size: 231.1 MB (231124838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128cac8b0310aa37c8527357da2df9e5a839ae8ad5078e27613f0d48022f8884`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 2.5 MB (2522173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e922dc5e5f1800b74b668a923fa6fc5ff7f1729d5fd4cec6aa1f172c787096e`  
		Last Modified: Wed, 06 Mar 2024 04:58:29 GMT  
		Size: 463.5 KB (463546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366961ad535530ea1eb7009e0e5fc762d153b47985f073800b6390a4f1671ae5`  
		Last Modified: Mon, 25 Mar 2024 20:21:20 GMT  
		Size: 333.6 MB (333631383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffef111ee6ebca522b316f6b2f7243ada7870555008c644234b1089c0eaf499b`  
		Last Modified: Mon, 25 Mar 2024 20:20:50 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0f66a2bde2f26c06758bb129559279f2f80d5b8eab858865035aeffa31635f`  
		Last Modified: Mon, 25 Mar 2024 20:20:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35c02533a41b7c214a2569afb79170e0ad2cec6d84b560196a2f0ac43e324f`  
		Last Modified: Mon, 25 Mar 2024 20:20:50 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3fd697c209f540ab9d2fef92a9bc28b1e7137d371a151d9a33a58365b9fc65`  
		Last Modified: Mon, 25 Mar 2024 20:20:50 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:41f5fc35ff4c82e7fc149da8629fda122ebd49b2737cb4cfb91cdd3487b4bc46
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.0 MB (617972223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0a11f2a651874831565d54afda840ce339ed06d60318784a12bb64caddad3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:56:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 02:56:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 02:56:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 02:56:53 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:00:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:01:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:01:25 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:01:26 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Mar 2024 19:33:49 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 19:33:49 GMT
ARG ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
# Mon, 25 Mar 2024 19:36:52 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 19:37:05 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 19:37:05 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 19:37:07 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 19:37:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 19:37:08 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 19:37:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 19:37:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 19:37:10 GMT
USER odoo
# Mon, 25 Mar 2024 19:37:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 19:37:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61460e6b4239c04ae02c8b5157a7b6f189f09c73682147f3af518f0dfaa9ef2`  
		Last Modified: Wed, 06 Mar 2024 03:05:32 GMT  
		Size: 243.3 MB (243298759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ae19a2941303126a97448f3501dcc7c1751322804bf811317b9d3391718773`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 2.8 MB (2805258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12901bfadfb439f3d17c6ce880d8353bd0636598d317d2f3e4625f1ce68d290`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 463.6 KB (463555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d44c933de6a2a4801a52b166e822fa56550b69007ae7b159ab76b24e45b38e9`  
		Last Modified: Mon, 25 Mar 2024 19:41:01 GMT  
		Size: 335.8 MB (335779444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6ad50b2a9452bbe455256df986f63033fb60a561ce550de4312da2043e8b5d`  
		Last Modified: Mon, 25 Mar 2024 19:40:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514a1b09ea7dc25305e95e67169f08f64dde45d735e098622529812556f18718`  
		Last Modified: Mon, 25 Mar 2024 19:40:15 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5881699184a1c0c3fa6b9a0a06a08e154c2ae51e3a0f25238626b2f2fe2d756`  
		Last Modified: Mon, 25 Mar 2024 19:40:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cb5fe91b9baf374b5bd1552ede136a2724299a8efa916ff873efcf25dea837`  
		Last Modified: Mon, 25 Mar 2024 19:40:15 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:4e748f0b002012da711a9ff21ebe6d4bdb784205016bd04ac7c4830026bc07ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:f247de51bf0bd27033eddb3aa76158d2c645d2cf61c864389cbc8436e97dc946
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.2 MB (601198776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e45d7945bd144b41261f9fda39f2b6b1225374f44bf20a2aba766ce058e6a73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:08:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 03:08:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 03:08:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 03:08:00 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:10:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:10:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:10:22 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:10:23 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Mar 2024 20:13:50 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 20:13:50 GMT
ARG ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
# Mon, 25 Mar 2024 20:15:27 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 20:15:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 20:15:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 20:15:33 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 20:15:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 20:15:33 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 20:15:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 20:15:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 20:15:33 GMT
USER odoo
# Mon, 25 Mar 2024 20:15:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:15:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e6c177fc20fa6387e63fd095d01292bafefb3d6e2ff9cb3e6e8b245a08381`  
		Last Modified: Wed, 06 Mar 2024 03:13:23 GMT  
		Size: 233.7 MB (233723335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3cefe2377c5eb4d88fbf2940f0a9dc339567dfe0c5c28fbc4d821dfa2ecb88`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 2.5 MB (2529426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f541a6d153b3dc5b1c957cef96a47ae608073cb3e26838fa2b35b8ce1455d`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 463.5 KB (463535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8af06cc4793bb719ec879b5341adaf15a265ab59f7b1dcfdaf0b765ad688351`  
		Last Modified: Mon, 25 Mar 2024 20:19:33 GMT  
		Size: 334.0 MB (334028714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ea0e32bd1422ccc747f0bca5a5ede791c8bb751e49db07752f0c733a2384f`  
		Last Modified: Mon, 25 Mar 2024 20:18:55 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8085f62d18ad15f5745dc2c4315ec3c6a05a2acdde8165c37105e65c1172b38d`  
		Last Modified: Mon, 25 Mar 2024 20:18:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068834d6e97533438f89c2da813f4874ac424066326774976b4d9c9995a0dc15`  
		Last Modified: Mon, 25 Mar 2024 20:18:55 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a244eff3b4db5e4f40e8521c00d6593a1a7f6a39fd0c788298773ec4cccdbc9`  
		Last Modified: Mon, 25 Mar 2024 20:18:56 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c8eba87d747dcf5da5e17bef7eed0d69e03e2dd21d5844b47ae54fbb5da739a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.1 MB (596145046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4972616593fbe72a656634bd46cc62262500cee871c767e310b187f8faf6292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:54:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 04:54:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 04:54:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 04:54:11 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 04:56:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 04:56:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:56:24 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 04:56:24 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Mar 2024 20:16:27 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 20:16:27 GMT
ARG ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
# Mon, 25 Mar 2024 20:18:42 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 20:18:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 20:18:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 20:18:50 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 20:18:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 20:18:50 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 20:18:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 20:18:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 20:18:50 GMT
USER odoo
# Mon, 25 Mar 2024 20:18:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:18:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d9a54b231a5bc1f0a4e20302873f08d395effbeb7c781ed9a3c37af48db7c`  
		Last Modified: Wed, 06 Mar 2024 04:58:49 GMT  
		Size: 231.1 MB (231124838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128cac8b0310aa37c8527357da2df9e5a839ae8ad5078e27613f0d48022f8884`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 2.5 MB (2522173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e922dc5e5f1800b74b668a923fa6fc5ff7f1729d5fd4cec6aa1f172c787096e`  
		Last Modified: Wed, 06 Mar 2024 04:58:29 GMT  
		Size: 463.5 KB (463546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366961ad535530ea1eb7009e0e5fc762d153b47985f073800b6390a4f1671ae5`  
		Last Modified: Mon, 25 Mar 2024 20:21:20 GMT  
		Size: 333.6 MB (333631383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffef111ee6ebca522b316f6b2f7243ada7870555008c644234b1089c0eaf499b`  
		Last Modified: Mon, 25 Mar 2024 20:20:50 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0f66a2bde2f26c06758bb129559279f2f80d5b8eab858865035aeffa31635f`  
		Last Modified: Mon, 25 Mar 2024 20:20:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35c02533a41b7c214a2569afb79170e0ad2cec6d84b560196a2f0ac43e324f`  
		Last Modified: Mon, 25 Mar 2024 20:20:50 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3fd697c209f540ab9d2fef92a9bc28b1e7137d371a151d9a33a58365b9fc65`  
		Last Modified: Mon, 25 Mar 2024 20:20:50 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:41f5fc35ff4c82e7fc149da8629fda122ebd49b2737cb4cfb91cdd3487b4bc46
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.0 MB (617972223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0a11f2a651874831565d54afda840ce339ed06d60318784a12bb64caddad3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:56:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 02:56:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 02:56:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 02:56:53 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:00:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:01:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:01:25 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:01:26 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Mar 2024 19:33:49 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 19:33:49 GMT
ARG ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
# Mon, 25 Mar 2024 19:36:52 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 19:37:05 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 19:37:05 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 19:37:07 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 19:37:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 19:37:08 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 19:37:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 19:37:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 19:37:10 GMT
USER odoo
# Mon, 25 Mar 2024 19:37:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 19:37:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61460e6b4239c04ae02c8b5157a7b6f189f09c73682147f3af518f0dfaa9ef2`  
		Last Modified: Wed, 06 Mar 2024 03:05:32 GMT  
		Size: 243.3 MB (243298759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ae19a2941303126a97448f3501dcc7c1751322804bf811317b9d3391718773`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 2.8 MB (2805258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12901bfadfb439f3d17c6ce880d8353bd0636598d317d2f3e4625f1ce68d290`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 463.6 KB (463555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d44c933de6a2a4801a52b166e822fa56550b69007ae7b159ab76b24e45b38e9`  
		Last Modified: Mon, 25 Mar 2024 19:41:01 GMT  
		Size: 335.8 MB (335779444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6ad50b2a9452bbe455256df986f63033fb60a561ce550de4312da2043e8b5d`  
		Last Modified: Mon, 25 Mar 2024 19:40:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514a1b09ea7dc25305e95e67169f08f64dde45d735e098622529812556f18718`  
		Last Modified: Mon, 25 Mar 2024 19:40:15 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5881699184a1c0c3fa6b9a0a06a08e154c2ae51e3a0f25238626b2f2fe2d756`  
		Last Modified: Mon, 25 Mar 2024 19:40:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cb5fe91b9baf374b5bd1552ede136a2724299a8efa916ff873efcf25dea837`  
		Last Modified: Mon, 25 Mar 2024 19:40:15 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:4e748f0b002012da711a9ff21ebe6d4bdb784205016bd04ac7c4830026bc07ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:f247de51bf0bd27033eddb3aa76158d2c645d2cf61c864389cbc8436e97dc946
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.2 MB (601198776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e45d7945bd144b41261f9fda39f2b6b1225374f44bf20a2aba766ce058e6a73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:08:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 03:08:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 03:08:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 03:08:00 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:10:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:10:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:10:22 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:10:23 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Mar 2024 20:13:50 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 20:13:50 GMT
ARG ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
# Mon, 25 Mar 2024 20:15:27 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 20:15:32 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 20:15:32 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 20:15:33 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 20:15:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 20:15:33 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 20:15:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 20:15:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 20:15:33 GMT
USER odoo
# Mon, 25 Mar 2024 20:15:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:15:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e6c177fc20fa6387e63fd095d01292bafefb3d6e2ff9cb3e6e8b245a08381`  
		Last Modified: Wed, 06 Mar 2024 03:13:23 GMT  
		Size: 233.7 MB (233723335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3cefe2377c5eb4d88fbf2940f0a9dc339567dfe0c5c28fbc4d821dfa2ecb88`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 2.5 MB (2529426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f541a6d153b3dc5b1c957cef96a47ae608073cb3e26838fa2b35b8ce1455d`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 463.5 KB (463535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8af06cc4793bb719ec879b5341adaf15a265ab59f7b1dcfdaf0b765ad688351`  
		Last Modified: Mon, 25 Mar 2024 20:19:33 GMT  
		Size: 334.0 MB (334028714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ea0e32bd1422ccc747f0bca5a5ede791c8bb751e49db07752f0c733a2384f`  
		Last Modified: Mon, 25 Mar 2024 20:18:55 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8085f62d18ad15f5745dc2c4315ec3c6a05a2acdde8165c37105e65c1172b38d`  
		Last Modified: Mon, 25 Mar 2024 20:18:55 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068834d6e97533438f89c2da813f4874ac424066326774976b4d9c9995a0dc15`  
		Last Modified: Mon, 25 Mar 2024 20:18:55 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a244eff3b4db5e4f40e8521c00d6593a1a7f6a39fd0c788298773ec4cccdbc9`  
		Last Modified: Mon, 25 Mar 2024 20:18:56 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c8eba87d747dcf5da5e17bef7eed0d69e03e2dd21d5844b47ae54fbb5da739a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.1 MB (596145046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4972616593fbe72a656634bd46cc62262500cee871c767e310b187f8faf6292`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:54:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 04:54:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 04:54:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 04:54:11 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 04:56:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 04:56:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:56:24 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 04:56:24 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Mar 2024 20:16:27 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 20:16:27 GMT
ARG ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
# Mon, 25 Mar 2024 20:18:42 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 20:18:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 20:18:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 20:18:50 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 20:18:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 20:18:50 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 20:18:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 20:18:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 20:18:50 GMT
USER odoo
# Mon, 25 Mar 2024 20:18:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 20:18:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d9a54b231a5bc1f0a4e20302873f08d395effbeb7c781ed9a3c37af48db7c`  
		Last Modified: Wed, 06 Mar 2024 04:58:49 GMT  
		Size: 231.1 MB (231124838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128cac8b0310aa37c8527357da2df9e5a839ae8ad5078e27613f0d48022f8884`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 2.5 MB (2522173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e922dc5e5f1800b74b668a923fa6fc5ff7f1729d5fd4cec6aa1f172c787096e`  
		Last Modified: Wed, 06 Mar 2024 04:58:29 GMT  
		Size: 463.5 KB (463546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366961ad535530ea1eb7009e0e5fc762d153b47985f073800b6390a4f1671ae5`  
		Last Modified: Mon, 25 Mar 2024 20:21:20 GMT  
		Size: 333.6 MB (333631383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffef111ee6ebca522b316f6b2f7243ada7870555008c644234b1089c0eaf499b`  
		Last Modified: Mon, 25 Mar 2024 20:20:50 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0f66a2bde2f26c06758bb129559279f2f80d5b8eab858865035aeffa31635f`  
		Last Modified: Mon, 25 Mar 2024 20:20:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc35c02533a41b7c214a2569afb79170e0ad2cec6d84b560196a2f0ac43e324f`  
		Last Modified: Mon, 25 Mar 2024 20:20:50 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3fd697c209f540ab9d2fef92a9bc28b1e7137d371a151d9a33a58365b9fc65`  
		Last Modified: Mon, 25 Mar 2024 20:20:50 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:41f5fc35ff4c82e7fc149da8629fda122ebd49b2737cb4cfb91cdd3487b4bc46
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.0 MB (617972223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0a11f2a651874831565d54afda840ce339ed06d60318784a12bb64caddad3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:56:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 02:56:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 02:56:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 02:56:53 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:00:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:01:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:01:25 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:01:26 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Mar 2024 19:33:49 GMT
ARG ODOO_RELEASE=20240325
# Mon, 25 Mar 2024 19:33:49 GMT
ARG ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
# Mon, 25 Mar 2024 19:36:52 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Mar 2024 19:37:05 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Mar 2024 19:37:05 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Mar 2024 19:37:07 GMT
# ARGS: ODOO_RELEASE=20240325 ODOO_SHA=d137d4e0c5df0bee241a6078aa3ce0bf6953289e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Mar 2024 19:37:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Mar 2024 19:37:08 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Mar 2024 19:37:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Mar 2024 19:37:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Mar 2024 19:37:10 GMT
USER odoo
# Mon, 25 Mar 2024 19:37:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Mar 2024 19:37:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61460e6b4239c04ae02c8b5157a7b6f189f09c73682147f3af518f0dfaa9ef2`  
		Last Modified: Wed, 06 Mar 2024 03:05:32 GMT  
		Size: 243.3 MB (243298759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ae19a2941303126a97448f3501dcc7c1751322804bf811317b9d3391718773`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 2.8 MB (2805258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12901bfadfb439f3d17c6ce880d8353bd0636598d317d2f3e4625f1ce68d290`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 463.6 KB (463555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d44c933de6a2a4801a52b166e822fa56550b69007ae7b159ab76b24e45b38e9`  
		Last Modified: Mon, 25 Mar 2024 19:41:01 GMT  
		Size: 335.8 MB (335779444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6ad50b2a9452bbe455256df986f63033fb60a561ce550de4312da2043e8b5d`  
		Last Modified: Mon, 25 Mar 2024 19:40:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514a1b09ea7dc25305e95e67169f08f64dde45d735e098622529812556f18718`  
		Last Modified: Mon, 25 Mar 2024 19:40:15 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5881699184a1c0c3fa6b9a0a06a08e154c2ae51e3a0f25238626b2f2fe2d756`  
		Last Modified: Mon, 25 Mar 2024 19:40:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cb5fe91b9baf374b5bd1552ede136a2724299a8efa916ff873efcf25dea837`  
		Last Modified: Mon, 25 Mar 2024 19:40:15 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
