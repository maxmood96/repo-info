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
$ docker pull odoo@sha256:ad2aa1b42b0510e64b71c54c5916c99b794246f74212ec2e2a5ae8c9a76e2fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:61247da22298dcc5f34d5edfafeba97dcc6a69bac01b27acf2bb6e52acb0f7c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563850037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d239502f164f2786d37ab0d9e2781da760531fd137413afc8cc5008e8eef7e82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:18:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 11:18:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 11:18:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 11:22:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 11:22:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:22:12 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 11:22:12 GMT
ENV ODOO_VERSION=15.0
# Thu, 29 Feb 2024 19:28:51 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:28:51 GMT
ARG ODOO_SHA=f99974a7dfc4862e348ef87e15766efcd2b777e2
# Thu, 29 Feb 2024 19:30:01 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=f99974a7dfc4862e348ef87e15766efcd2b777e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:30:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:30:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:30:06 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=f99974a7dfc4862e348ef87e15766efcd2b777e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:30:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:30:06 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:30:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:30:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:30:07 GMT
USER odoo
# Thu, 29 Feb 2024 19:30:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:30:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503d586dde6058081085a71407e0daec70122616b9a175f52944fcf0f6cae634`  
		Last Modified: Tue, 13 Feb 2024 11:24:56 GMT  
		Size: 220.3 MB (220291578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fd8ca8a48200ac393e61d324250d6da85bc0dfaa29c83841e7b384b4ae90dd`  
		Last Modified: Tue, 13 Feb 2024 11:24:31 GMT  
		Size: 2.6 MB (2625899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447d81bf30e1590e8be1f898a405b5ae2775c64d0de45831fcd3fbb2241409a1`  
		Last Modified: Tue, 13 Feb 2024 11:24:32 GMT  
		Size: 462.9 KB (462933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92732e77f9c353d2125263283b9e6f3c1cbd8119804b84c7880a7f36df279e9f`  
		Last Modified: Thu, 29 Feb 2024 19:32:32 GMT  
		Size: 309.0 MB (309044737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38edb2f7c6699b1f7ccf6ac9db224ea8c52b97d3554eec802884d38ebd244645`  
		Last Modified: Thu, 29 Feb 2024 19:31:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e360fe882e9011514f9162ef156dae23e7516b6fc30405e8b598bf782f1987`  
		Last Modified: Thu, 29 Feb 2024 19:31:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed937af20aa273420b049ec1aa8829ada3c3bb4734d857bcd338c444358f7e0`  
		Last Modified: Thu, 29 Feb 2024 19:31:59 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40917497c5f96311164f77a1446ba69b0e79ad73795ac058205309034440bc63`  
		Last Modified: Thu, 29 Feb 2024 19:31:58 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:ad2aa1b42b0510e64b71c54c5916c99b794246f74212ec2e2a5ae8c9a76e2fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:61247da22298dcc5f34d5edfafeba97dcc6a69bac01b27acf2bb6e52acb0f7c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563850037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d239502f164f2786d37ab0d9e2781da760531fd137413afc8cc5008e8eef7e82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:18:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 11:18:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 11:18:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 11:22:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 11:22:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:22:12 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 11:22:12 GMT
ENV ODOO_VERSION=15.0
# Thu, 29 Feb 2024 19:28:51 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:28:51 GMT
ARG ODOO_SHA=f99974a7dfc4862e348ef87e15766efcd2b777e2
# Thu, 29 Feb 2024 19:30:01 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=f99974a7dfc4862e348ef87e15766efcd2b777e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:30:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:30:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:30:06 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=f99974a7dfc4862e348ef87e15766efcd2b777e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:30:06 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:30:06 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:30:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:30:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:30:07 GMT
USER odoo
# Thu, 29 Feb 2024 19:30:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:30:07 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503d586dde6058081085a71407e0daec70122616b9a175f52944fcf0f6cae634`  
		Last Modified: Tue, 13 Feb 2024 11:24:56 GMT  
		Size: 220.3 MB (220291578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fd8ca8a48200ac393e61d324250d6da85bc0dfaa29c83841e7b384b4ae90dd`  
		Last Modified: Tue, 13 Feb 2024 11:24:31 GMT  
		Size: 2.6 MB (2625899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447d81bf30e1590e8be1f898a405b5ae2775c64d0de45831fcd3fbb2241409a1`  
		Last Modified: Tue, 13 Feb 2024 11:24:32 GMT  
		Size: 462.9 KB (462933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92732e77f9c353d2125263283b9e6f3c1cbd8119804b84c7880a7f36df279e9f`  
		Last Modified: Thu, 29 Feb 2024 19:32:32 GMT  
		Size: 309.0 MB (309044737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38edb2f7c6699b1f7ccf6ac9db224ea8c52b97d3554eec802884d38ebd244645`  
		Last Modified: Thu, 29 Feb 2024 19:31:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e360fe882e9011514f9162ef156dae23e7516b6fc30405e8b598bf782f1987`  
		Last Modified: Thu, 29 Feb 2024 19:31:59 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed937af20aa273420b049ec1aa8829ada3c3bb4734d857bcd338c444358f7e0`  
		Last Modified: Thu, 29 Feb 2024 19:31:59 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40917497c5f96311164f77a1446ba69b0e79ad73795ac058205309034440bc63`  
		Last Modified: Thu, 29 Feb 2024 19:31:58 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:1f5170c5b1f02abd859d8a47acdcbe34ec1c95e15e4456f6159f782990449f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:1b1bebca141affea9b47cb4ca2baf23d9e4675ded8a932b074befa708abdf3c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.6 MB (582623343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583be1ac1485c8a20dac8f0ad5354e1adf645926aa1dd13af3d84b49637cc789`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:18:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 11:18:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 11:18:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 11:18:16 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 11:19:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 11:19:34 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:19:35 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 11:19:36 GMT
ENV ODOO_VERSION=16.0
# Thu, 29 Feb 2024 19:27:12 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:27:12 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Thu, 29 Feb 2024 19:28:34 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:28:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:28:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:28:39 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:28:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:28:39 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:28:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:28:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:28:39 GMT
USER odoo
# Thu, 29 Feb 2024 19:28:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:28:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9940f8764e315ffe4d9162112c693dc2de9180d54741bcc86a94a2e8dc63796`  
		Last Modified: Tue, 13 Feb 2024 11:24:08 GMT  
		Size: 219.6 MB (219603078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c251911a36e7b29cdc68e2e6ad3c227877483a27881808128a45cdf7f29cd97`  
		Last Modified: Tue, 13 Feb 2024 11:23:43 GMT  
		Size: 2.6 MB (2629960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876b94be8a611fcadb8c1bb3ac916cbf8b7c765cb563396dcb2461b5150d88e9`  
		Last Modified: Tue, 13 Feb 2024 11:23:44 GMT  
		Size: 462.9 KB (462884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cd49ff24bb4ca0361b59d7993339c8cd2eb3e852b2a49fd9659fa4bcc12a13`  
		Last Modified: Thu, 29 Feb 2024 19:31:49 GMT  
		Size: 328.5 MB (328502534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af5c6db7fe3dd835543b603c92e7d4b2c6803f8a875efcbcd5b80edee3f16e5`  
		Last Modified: Thu, 29 Feb 2024 19:31:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23d26a7a5c6335675b0181297f5482d9e08127b7bd6f18b7c30eb2b5188bc1e`  
		Last Modified: Thu, 29 Feb 2024 19:31:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768865bd5e18e0dd2ceb98bb7d05ca88d80f4fa4ff73a46b2a92bdbee86eca9e`  
		Last Modified: Thu, 29 Feb 2024 19:31:11 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495576eb070d1c531225ff0073a40667291aa5744b16ae81052b04f5e6326f51`  
		Last Modified: Thu, 29 Feb 2024 19:31:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ce34cd26b3d4d4ad2056d845d2730bd8d933d9288f8af67924a9f2483f2197da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.3 MB (578256324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a74f88a11b2185f831c7f3305b2e397feb37852536c37bf5861af9905a5d11c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:47:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 02:47:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 02:47:36 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 02:47:36 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 02:48:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 02:48:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:48:53 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 02:48:53 GMT
ENV ODOO_VERSION=16.0
# Thu, 29 Feb 2024 19:45:40 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:45:40 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Thu, 29 Feb 2024 19:46:54 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:47:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:47:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:47:02 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:47:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:47:02 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:47:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:47:02 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:47:02 GMT
USER odoo
# Thu, 29 Feb 2024 19:47:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:47:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2f618c4954544d5a1d56ef7354df8c3a0a52e4c057e074c37924915ca2fd1`  
		Last Modified: Tue, 13 Feb 2024 02:50:56 GMT  
		Size: 216.9 MB (216902917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a473596c65e4b7b8b68f3b2d5b8b44b1d170a7c2d419f7047936e9222e56adb`  
		Last Modified: Tue, 13 Feb 2024 02:50:38 GMT  
		Size: 2.6 MB (2635157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8628656e229343de1b693a2b98cf92fb4f3b3bb43b28acb4438d79491525761f`  
		Last Modified: Tue, 13 Feb 2024 02:50:38 GMT  
		Size: 462.9 KB (462916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d197d79192603486a4ebeb06da1552af5ff656ca79b67bd8cccc207c986c6c7`  
		Last Modified: Thu, 29 Feb 2024 19:48:45 GMT  
		Size: 328.2 MB (328181793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e378408b9023c0af82378853c61b55c3a2f49977dd6724ebe9568e26c12d61e`  
		Last Modified: Thu, 29 Feb 2024 19:48:15 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a305c5593b77b8717fbccb832b8729a5b0adcbeee79bd8deaf4e3fc119074`  
		Last Modified: Thu, 29 Feb 2024 19:48:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdafef35f649cacad16793455f1a8fa9c03806577ca5daf286cb155f6e7c00`  
		Last Modified: Thu, 29 Feb 2024 19:48:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ee89c975eb46900d126a067134df6782e8e747f2e3004a7fcb68a1feef714`  
		Last Modified: Thu, 29 Feb 2024 19:48:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:ac4c26796e7de62c7c37943df36da93330c52518558ff7f6348158c7ea349c40
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.2 MB (597188342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a85ccfe0b798aed5e6e88db8c5b377cdb1d61edea6d6a99b960b829a1db777`
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
# Tue, 12 Mar 2024 02:46:14 GMT
ARG ODOO_RELEASE=20240229
# Tue, 12 Mar 2024 02:46:16 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Tue, 12 Mar 2024 02:52:18 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 02:52:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 02:52:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 02:52:53 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 02:52:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 02:52:55 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 02:52:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 02:53:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 02:53:03 GMT
USER odoo
# Tue, 12 Mar 2024 02:53:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 02:53:09 GMT
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
	-	`sha256:07524d2b73109a74dd0a1f20a0010d75b2fc711c5b53922553f135bc0ef5efa9`  
		Last Modified: Tue, 12 Mar 2024 02:54:14 GMT  
		Size: 329.9 MB (329948666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cb9dd5d6bb8e8e8204736a4e78fe836d73f315949634a50468f87045d5e537`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5623aaad4280283dfcc93d0cae94a05cf79dcc89617d8c690866ac6bb5f7403f`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26758bb8f8a978e5290eda3a3fa1038fd411b3e951a21539f2e165a9d7eecb4c`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a8f884eab14d8865dc28d1fb2728caab6b0f93bc4527fd3d1eef43c413bd97`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:1f5170c5b1f02abd859d8a47acdcbe34ec1c95e15e4456f6159f782990449f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:1b1bebca141affea9b47cb4ca2baf23d9e4675ded8a932b074befa708abdf3c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.6 MB (582623343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583be1ac1485c8a20dac8f0ad5354e1adf645926aa1dd13af3d84b49637cc789`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 11:18:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 11:18:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 11:18:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 11:18:16 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 11:19:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 11:19:34 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:19:35 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 11:19:36 GMT
ENV ODOO_VERSION=16.0
# Thu, 29 Feb 2024 19:27:12 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:27:12 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Thu, 29 Feb 2024 19:28:34 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:28:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:28:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:28:39 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:28:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:28:39 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:28:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:28:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:28:39 GMT
USER odoo
# Thu, 29 Feb 2024 19:28:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:28:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9940f8764e315ffe4d9162112c693dc2de9180d54741bcc86a94a2e8dc63796`  
		Last Modified: Tue, 13 Feb 2024 11:24:08 GMT  
		Size: 219.6 MB (219603078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c251911a36e7b29cdc68e2e6ad3c227877483a27881808128a45cdf7f29cd97`  
		Last Modified: Tue, 13 Feb 2024 11:23:43 GMT  
		Size: 2.6 MB (2629960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876b94be8a611fcadb8c1bb3ac916cbf8b7c765cb563396dcb2461b5150d88e9`  
		Last Modified: Tue, 13 Feb 2024 11:23:44 GMT  
		Size: 462.9 KB (462884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cd49ff24bb4ca0361b59d7993339c8cd2eb3e852b2a49fd9659fa4bcc12a13`  
		Last Modified: Thu, 29 Feb 2024 19:31:49 GMT  
		Size: 328.5 MB (328502534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af5c6db7fe3dd835543b603c92e7d4b2c6803f8a875efcbcd5b80edee3f16e5`  
		Last Modified: Thu, 29 Feb 2024 19:31:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23d26a7a5c6335675b0181297f5482d9e08127b7bd6f18b7c30eb2b5188bc1e`  
		Last Modified: Thu, 29 Feb 2024 19:31:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768865bd5e18e0dd2ceb98bb7d05ca88d80f4fa4ff73a46b2a92bdbee86eca9e`  
		Last Modified: Thu, 29 Feb 2024 19:31:11 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495576eb070d1c531225ff0073a40667291aa5744b16ae81052b04f5e6326f51`  
		Last Modified: Thu, 29 Feb 2024 19:31:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ce34cd26b3d4d4ad2056d845d2730bd8d933d9288f8af67924a9f2483f2197da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.3 MB (578256324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a74f88a11b2185f831c7f3305b2e397feb37852536c37bf5861af9905a5d11c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:47:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 02:47:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 02:47:36 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 02:47:36 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 02:48:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 02:48:52 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:48:53 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 02:48:53 GMT
ENV ODOO_VERSION=16.0
# Thu, 29 Feb 2024 19:45:40 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:45:40 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Thu, 29 Feb 2024 19:46:54 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:47:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:47:01 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:47:02 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:47:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:47:02 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:47:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:47:02 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:47:02 GMT
USER odoo
# Thu, 29 Feb 2024 19:47:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:47:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e2f618c4954544d5a1d56ef7354df8c3a0a52e4c057e074c37924915ca2fd1`  
		Last Modified: Tue, 13 Feb 2024 02:50:56 GMT  
		Size: 216.9 MB (216902917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a473596c65e4b7b8b68f3b2d5b8b44b1d170a7c2d419f7047936e9222e56adb`  
		Last Modified: Tue, 13 Feb 2024 02:50:38 GMT  
		Size: 2.6 MB (2635157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8628656e229343de1b693a2b98cf92fb4f3b3bb43b28acb4438d79491525761f`  
		Last Modified: Tue, 13 Feb 2024 02:50:38 GMT  
		Size: 462.9 KB (462916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d197d79192603486a4ebeb06da1552af5ff656ca79b67bd8cccc207c986c6c7`  
		Last Modified: Thu, 29 Feb 2024 19:48:45 GMT  
		Size: 328.2 MB (328181793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e378408b9023c0af82378853c61b55c3a2f49977dd6724ebe9568e26c12d61e`  
		Last Modified: Thu, 29 Feb 2024 19:48:15 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a305c5593b77b8717fbccb832b8729a5b0adcbeee79bd8deaf4e3fc119074`  
		Last Modified: Thu, 29 Feb 2024 19:48:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cdafef35f649cacad16793455f1a8fa9c03806577ca5daf286cb155f6e7c00`  
		Last Modified: Thu, 29 Feb 2024 19:48:15 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6ee89c975eb46900d126a067134df6782e8e747f2e3004a7fcb68a1feef714`  
		Last Modified: Thu, 29 Feb 2024 19:48:15 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:ac4c26796e7de62c7c37943df36da93330c52518558ff7f6348158c7ea349c40
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.2 MB (597188342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a85ccfe0b798aed5e6e88db8c5b377cdb1d61edea6d6a99b960b829a1db777`
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
# Tue, 12 Mar 2024 02:46:14 GMT
ARG ODOO_RELEASE=20240229
# Tue, 12 Mar 2024 02:46:16 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Tue, 12 Mar 2024 02:52:18 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 12 Mar 2024 02:52:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 12 Mar 2024 02:52:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 12 Mar 2024 02:52:53 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 12 Mar 2024 02:52:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 12 Mar 2024 02:52:55 GMT
EXPOSE 8069 8071 8072
# Tue, 12 Mar 2024 02:52:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 12 Mar 2024 02:53:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 12 Mar 2024 02:53:03 GMT
USER odoo
# Tue, 12 Mar 2024 02:53:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Mar 2024 02:53:09 GMT
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
	-	`sha256:07524d2b73109a74dd0a1f20a0010d75b2fc711c5b53922553f135bc0ef5efa9`  
		Last Modified: Tue, 12 Mar 2024 02:54:14 GMT  
		Size: 329.9 MB (329948666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cb9dd5d6bb8e8e8204736a4e78fe836d73f315949634a50468f87045d5e537`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5623aaad4280283dfcc93d0cae94a05cf79dcc89617d8c690866ac6bb5f7403f`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26758bb8f8a978e5290eda3a3fa1038fd411b3e951a21539f2e165a9d7eecb4c`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a8f884eab14d8865dc28d1fb2728caab6b0f93bc4527fd3d1eef43c413bd97`  
		Last Modified: Tue, 12 Mar 2024 02:53:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:6d7b28da1aa2ca75e10d0efff30c342f222da78148c295490c23df78fd51049a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:4ec7d77268a6ddcfb57bf21d4d02809a3a59a73d663038f25b9492168644af41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599400521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a643a46f2e9a90bd339ce38c1a98519a43ac5ef2d3bc16b0efea5c45bc6cc1b0`
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
# Wed, 06 Mar 2024 03:10:23 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 03:10:23 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 03:12:17 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 03:12:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 03:12:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 03:12:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 03:12:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 03:12:22 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 03:12:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 03:12:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 03:12:22 GMT
USER odoo
# Wed, 06 Mar 2024 03:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 03:12:22 GMT
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
	-	`sha256:a3717329e54eff361b366c467d937defe6ca11cabe9bf154df41b26af3e0217b`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 332.2 MB (332230458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c90c8fa1dd7a41d4d9b1a2b6668dc5e4dbe08c783555baf1b06185df4edb089`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748e7b2c45b97702bee087b74a497e56f2242989fdabd4c540a6f1fbefde1c56`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b540f23430dfda96b5ace20472fe05a61c966108bec8e74f8c9d31f9ad6117b4`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109fd9f4a47e84418a08805e18fef090743b51cd587988cd3989657c34bcdb68`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2f09607cc3f69cf0da21ce0768090ae0a1b20cc03ef11fd55e58a8fd8976f4f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594344493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210e410acf6ee10dfa11e2fd0b5183010016dfac5b66d8b3cb2aba5ae4ee280`
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
# Wed, 06 Mar 2024 04:56:24 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 04:56:25 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 04:57:58 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 04:58:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 04:58:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 04:58:07 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 04:58:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 04:58:07 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 04:58:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 04:58:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 04:58:07 GMT
USER odoo
# Wed, 06 Mar 2024 04:58:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 04:58:07 GMT
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
	-	`sha256:e119923f8f85637d1291f21089fb8f8c83b60055d0ced620ee1a5f1b0c32293b`  
		Last Modified: Wed, 06 Mar 2024 04:58:57 GMT  
		Size: 331.8 MB (331830830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0752d0b20375f0106febf3111e43b12167400a8fcd198548c83579106d8bc100`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691cbfbd6a8b660d3416a8d8f0668f4ed111b94e46f259dbbb2297ddd0a50800`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5570037660ddca8846552de495143df700ef637408692c8a75c0f167225ca6f8`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28706c51a3064cf047be7d767cf6edb9c5515434fe36bdd1d797d5f416d1038d`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:c0718bc9f52ced5ac33df5a103b6f58a1442c3fccc8819959603b136e4808130
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616165906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2268108c1666954290aba8be8ac3e3870391d630b3bc7d43d9091c24e1514ada`
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
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 03:04:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 03:04:36 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 03:04:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 03:04:39 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 03:04:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 03:04:40 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 03:04:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 03:04:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 03:04:41 GMT
USER odoo
# Wed, 06 Mar 2024 03:04:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 03:04:42 GMT
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
	-	`sha256:83c7ccee6e7cf504378174dd78461a007b2920939a2291c93e66508be975ca8e`  
		Last Modified: Wed, 06 Mar 2024 03:05:44 GMT  
		Size: 334.0 MB (333973126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f53d3050250f2fb7d38db8a1ad84df42f920f9d92b08fbf889a737c5f7ff0`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b3650ff0f9b47e5b5f2a6b81e21a6bca1b569079f13c87f2d63a860dc25890`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1ee0eedbb080c2c0a7ff7b4bb9ad2ca3daf24892cca1a34be15dc0e8fbb45f`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e5da5e8c17a8a07b38d1a833e96b5aa4143ce361893536dbc5da82c440198c`  
		Last Modified: Wed, 06 Mar 2024 03:04:56 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:6d7b28da1aa2ca75e10d0efff30c342f222da78148c295490c23df78fd51049a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:4ec7d77268a6ddcfb57bf21d4d02809a3a59a73d663038f25b9492168644af41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599400521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a643a46f2e9a90bd339ce38c1a98519a43ac5ef2d3bc16b0efea5c45bc6cc1b0`
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
# Wed, 06 Mar 2024 03:10:23 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 03:10:23 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 03:12:17 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 03:12:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 03:12:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 03:12:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 03:12:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 03:12:22 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 03:12:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 03:12:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 03:12:22 GMT
USER odoo
# Wed, 06 Mar 2024 03:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 03:12:22 GMT
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
	-	`sha256:a3717329e54eff361b366c467d937defe6ca11cabe9bf154df41b26af3e0217b`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 332.2 MB (332230458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c90c8fa1dd7a41d4d9b1a2b6668dc5e4dbe08c783555baf1b06185df4edb089`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748e7b2c45b97702bee087b74a497e56f2242989fdabd4c540a6f1fbefde1c56`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b540f23430dfda96b5ace20472fe05a61c966108bec8e74f8c9d31f9ad6117b4`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109fd9f4a47e84418a08805e18fef090743b51cd587988cd3989657c34bcdb68`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2f09607cc3f69cf0da21ce0768090ae0a1b20cc03ef11fd55e58a8fd8976f4f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594344493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210e410acf6ee10dfa11e2fd0b5183010016dfac5b66d8b3cb2aba5ae4ee280`
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
# Wed, 06 Mar 2024 04:56:24 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 04:56:25 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 04:57:58 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 04:58:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 04:58:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 04:58:07 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 04:58:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 04:58:07 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 04:58:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 04:58:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 04:58:07 GMT
USER odoo
# Wed, 06 Mar 2024 04:58:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 04:58:07 GMT
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
	-	`sha256:e119923f8f85637d1291f21089fb8f8c83b60055d0ced620ee1a5f1b0c32293b`  
		Last Modified: Wed, 06 Mar 2024 04:58:57 GMT  
		Size: 331.8 MB (331830830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0752d0b20375f0106febf3111e43b12167400a8fcd198548c83579106d8bc100`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691cbfbd6a8b660d3416a8d8f0668f4ed111b94e46f259dbbb2297ddd0a50800`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5570037660ddca8846552de495143df700ef637408692c8a75c0f167225ca6f8`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28706c51a3064cf047be7d767cf6edb9c5515434fe36bdd1d797d5f416d1038d`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:c0718bc9f52ced5ac33df5a103b6f58a1442c3fccc8819959603b136e4808130
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616165906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2268108c1666954290aba8be8ac3e3870391d630b3bc7d43d9091c24e1514ada`
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
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 03:04:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 03:04:36 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 03:04:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 03:04:39 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 03:04:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 03:04:40 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 03:04:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 03:04:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 03:04:41 GMT
USER odoo
# Wed, 06 Mar 2024 03:04:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 03:04:42 GMT
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
	-	`sha256:83c7ccee6e7cf504378174dd78461a007b2920939a2291c93e66508be975ca8e`  
		Last Modified: Wed, 06 Mar 2024 03:05:44 GMT  
		Size: 334.0 MB (333973126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f53d3050250f2fb7d38db8a1ad84df42f920f9d92b08fbf889a737c5f7ff0`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b3650ff0f9b47e5b5f2a6b81e21a6bca1b569079f13c87f2d63a860dc25890`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1ee0eedbb080c2c0a7ff7b4bb9ad2ca3daf24892cca1a34be15dc0e8fbb45f`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e5da5e8c17a8a07b38d1a833e96b5aa4143ce361893536dbc5da82c440198c`  
		Last Modified: Wed, 06 Mar 2024 03:04:56 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:6d7b28da1aa2ca75e10d0efff30c342f222da78148c295490c23df78fd51049a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:4ec7d77268a6ddcfb57bf21d4d02809a3a59a73d663038f25b9492168644af41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599400521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a643a46f2e9a90bd339ce38c1a98519a43ac5ef2d3bc16b0efea5c45bc6cc1b0`
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
# Wed, 06 Mar 2024 03:10:23 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 03:10:23 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 03:12:17 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 03:12:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 03:12:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 03:12:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 03:12:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 03:12:22 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 03:12:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 03:12:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 03:12:22 GMT
USER odoo
# Wed, 06 Mar 2024 03:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 03:12:22 GMT
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
	-	`sha256:a3717329e54eff361b366c467d937defe6ca11cabe9bf154df41b26af3e0217b`  
		Last Modified: Wed, 06 Mar 2024 03:13:33 GMT  
		Size: 332.2 MB (332230458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c90c8fa1dd7a41d4d9b1a2b6668dc5e4dbe08c783555baf1b06185df4edb089`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748e7b2c45b97702bee087b74a497e56f2242989fdabd4c540a6f1fbefde1c56`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b540f23430dfda96b5ace20472fe05a61c966108bec8e74f8c9d31f9ad6117b4`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109fd9f4a47e84418a08805e18fef090743b51cd587988cd3989657c34bcdb68`  
		Last Modified: Wed, 06 Mar 2024 03:12:51 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2f09607cc3f69cf0da21ce0768090ae0a1b20cc03ef11fd55e58a8fd8976f4f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594344493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210e410acf6ee10dfa11e2fd0b5183010016dfac5b66d8b3cb2aba5ae4ee280`
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
# Wed, 06 Mar 2024 04:56:24 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 04:56:25 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 04:57:58 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 04:58:06 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 04:58:06 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 04:58:07 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 04:58:07 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 04:58:07 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 04:58:07 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 04:58:07 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 04:58:07 GMT
USER odoo
# Wed, 06 Mar 2024 04:58:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 04:58:07 GMT
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
	-	`sha256:e119923f8f85637d1291f21089fb8f8c83b60055d0ced620ee1a5f1b0c32293b`  
		Last Modified: Wed, 06 Mar 2024 04:58:57 GMT  
		Size: 331.8 MB (331830830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0752d0b20375f0106febf3111e43b12167400a8fcd198548c83579106d8bc100`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691cbfbd6a8b660d3416a8d8f0668f4ed111b94e46f259dbbb2297ddd0a50800`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5570037660ddca8846552de495143df700ef637408692c8a75c0f167225ca6f8`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28706c51a3064cf047be7d767cf6edb9c5515434fe36bdd1d797d5f416d1038d`  
		Last Modified: Wed, 06 Mar 2024 04:58:27 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:c0718bc9f52ced5ac33df5a103b6f58a1442c3fccc8819959603b136e4808130
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616165906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2268108c1666954290aba8be8ac3e3870391d630b3bc7d43d9091c24e1514ada`
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
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_RELEASE=20240229
# Wed, 06 Mar 2024 03:01:26 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Wed, 06 Mar 2024 03:04:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 06 Mar 2024 03:04:36 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 06 Mar 2024 03:04:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 06 Mar 2024 03:04:39 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 06 Mar 2024 03:04:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 06 Mar 2024 03:04:40 GMT
EXPOSE 8069 8071 8072
# Wed, 06 Mar 2024 03:04:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 06 Mar 2024 03:04:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 06 Mar 2024 03:04:41 GMT
USER odoo
# Wed, 06 Mar 2024 03:04:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 Mar 2024 03:04:42 GMT
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
	-	`sha256:83c7ccee6e7cf504378174dd78461a007b2920939a2291c93e66508be975ca8e`  
		Last Modified: Wed, 06 Mar 2024 03:05:44 GMT  
		Size: 334.0 MB (333973126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5f53d3050250f2fb7d38db8a1ad84df42f920f9d92b08fbf889a737c5f7ff0`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b3650ff0f9b47e5b5f2a6b81e21a6bca1b569079f13c87f2d63a860dc25890`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1ee0eedbb080c2c0a7ff7b4bb9ad2ca3daf24892cca1a34be15dc0e8fbb45f`  
		Last Modified: Wed, 06 Mar 2024 03:04:57 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e5da5e8c17a8a07b38d1a833e96b5aa4143ce361893536dbc5da82c440198c`  
		Last Modified: Wed, 06 Mar 2024 03:04:56 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
