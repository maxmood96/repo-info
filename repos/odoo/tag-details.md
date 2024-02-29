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
$ docker pull odoo@sha256:0914ec78d9a1fcf504deacb109e8ea0ac3a140aca6dde76efb4f2df6eb9e1615
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
$ docker pull odoo@sha256:a15d97c45697c1243cff2bae5446c8b67303dec04e38166a82e82a3b00755e7d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.2 MB (597185191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f90e182cc9bc73605c3c9af9d031eff046962ba435489476e47b53b5d881acd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:33 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 13 Feb 2024 00:39:36 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:09:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 04:09:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 04:09:39 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 04:09:40 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 04:13:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 04:13:45 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:13:49 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 04:13:49 GMT
ENV ODOO_VERSION=16.0
# Thu, 29 Feb 2024 19:21:31 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:21:32 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Thu, 29 Feb 2024 19:24:53 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:25:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:25:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:25:12 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:25:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:25:14 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:25:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:25:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:25:15 GMT
USER odoo
# Thu, 29 Feb 2024 19:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:25:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e47bb6241f7f89a639b08014441cb2820f9f7f4509216e43e8bbd6357c7bda0`  
		Last Modified: Tue, 13 Feb 2024 04:18:30 GMT  
		Size: 228.6 MB (228600171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c9749dac12780aa7b6979dc392d78966a3978c3a71436c61a00cc276c9b3ab`  
		Last Modified: Tue, 13 Feb 2024 04:18:00 GMT  
		Size: 2.9 MB (2875930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b38c3b73d7742aebbefe4d2d4b68642d916e808d2f230032f15cc77e6bb0c9`  
		Last Modified: Tue, 13 Feb 2024 04:18:00 GMT  
		Size: 463.0 KB (462957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365e299b265fb8ef971ce882fcde51727539eedb979861d86f8934b901c6a14e`  
		Last Modified: Thu, 29 Feb 2024 19:27:57 GMT  
		Size: 329.9 MB (329945867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bbd48422d5fb943ddc976447585c93465defa3b1efddf10278d857101ab7d6`  
		Last Modified: Thu, 29 Feb 2024 19:27:12 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73741d08a66cf116481351b62b834698e2d39cd3c3801c27a8b283fc22a60dd8`  
		Last Modified: Thu, 29 Feb 2024 19:27:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22dbf67112417618f9408945e0acda21758f33e8e96e9e0f121ae2cecc2d2c0e`  
		Last Modified: Thu, 29 Feb 2024 19:27:12 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a599195f1936bf1a6dc4c93b094952af79a36ce95cfca395ece02f6e870b35d5`  
		Last Modified: Thu, 29 Feb 2024 19:27:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:0914ec78d9a1fcf504deacb109e8ea0ac3a140aca6dde76efb4f2df6eb9e1615
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
$ docker pull odoo@sha256:a15d97c45697c1243cff2bae5446c8b67303dec04e38166a82e82a3b00755e7d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.2 MB (597185191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f90e182cc9bc73605c3c9af9d031eff046962ba435489476e47b53b5d881acd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:33 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Tue, 13 Feb 2024 00:39:36 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:09:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 13 Feb 2024 04:09:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 13 Feb 2024 04:09:39 GMT
ENV LANG=C.UTF-8
# Tue, 13 Feb 2024 04:09:40 GMT
ARG TARGETARCH
# Tue, 13 Feb 2024 04:13:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 13 Feb 2024 04:13:45 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:13:49 GMT
RUN npm install -g rtlcss
# Tue, 13 Feb 2024 04:13:49 GMT
ENV ODOO_VERSION=16.0
# Thu, 29 Feb 2024 19:21:31 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:21:32 GMT
ARG ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
# Thu, 29 Feb 2024 19:24:53 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:25:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:25:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:25:12 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=4434ed85784e13fa23cb09ed7168f0a430f73fd1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:25:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:25:14 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:25:14 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:25:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:25:15 GMT
USER odoo
# Thu, 29 Feb 2024 19:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:25:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e47bb6241f7f89a639b08014441cb2820f9f7f4509216e43e8bbd6357c7bda0`  
		Last Modified: Tue, 13 Feb 2024 04:18:30 GMT  
		Size: 228.6 MB (228600171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c9749dac12780aa7b6979dc392d78966a3978c3a71436c61a00cc276c9b3ab`  
		Last Modified: Tue, 13 Feb 2024 04:18:00 GMT  
		Size: 2.9 MB (2875930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b38c3b73d7742aebbefe4d2d4b68642d916e808d2f230032f15cc77e6bb0c9`  
		Last Modified: Tue, 13 Feb 2024 04:18:00 GMT  
		Size: 463.0 KB (462957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365e299b265fb8ef971ce882fcde51727539eedb979861d86f8934b901c6a14e`  
		Last Modified: Thu, 29 Feb 2024 19:27:57 GMT  
		Size: 329.9 MB (329945867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87bbd48422d5fb943ddc976447585c93465defa3b1efddf10278d857101ab7d6`  
		Last Modified: Thu, 29 Feb 2024 19:27:12 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73741d08a66cf116481351b62b834698e2d39cd3c3801c27a8b283fc22a60dd8`  
		Last Modified: Thu, 29 Feb 2024 19:27:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22dbf67112417618f9408945e0acda21758f33e8e96e9e0f121ae2cecc2d2c0e`  
		Last Modified: Thu, 29 Feb 2024 19:27:12 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a599195f1936bf1a6dc4c93b094952af79a36ce95cfca395ece02f6e870b35d5`  
		Last Modified: Thu, 29 Feb 2024 19:27:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:7be75cd6e517879310f9dec9090a6b25345a5bc219c4ba22f7bab9c699faff7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:f065f2807c55742df979983385d59cf3d14c79b723d7d429fa505c2bb334553e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599406969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697778a8975ba915513dee14438d400acb0530fe9d081436803d284a360e678a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:23:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 02:23:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 02:23:57 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 02:23:58 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 02:25:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 02:26:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:26:12 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 02:26:12 GMT
ENV ODOO_VERSION=17.0
# Thu, 29 Feb 2024 19:25:03 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:25:03 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Thu, 29 Feb 2024 19:26:56 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:27:00 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:27:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:27:01 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:27:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:27:01 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:27:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:27:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:27:01 GMT
USER odoo
# Thu, 29 Feb 2024 19:27:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:27:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb9367916e4f1ff7e545a30dff1796f82c18802f3d1b24c43a6e928c02511ee`  
		Last Modified: Fri, 16 Feb 2024 02:29:04 GMT  
		Size: 233.7 MB (233731383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cf39849cf6ab3e832eeac1fd52f105ef9917fabeaa12f969681fe53e462652`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 2.5 MB (2529496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f7e2693b9cb165cab924bf88c5543b01a3b122e4586070fee4bb4194bf39ec`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 463.9 KB (463923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22d57e76feea15161f1175c14a0a856e03dc43dbc6da22a041da58ebc88d955`  
		Last Modified: Thu, 29 Feb 2024 19:30:59 GMT  
		Size: 332.2 MB (332229624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36b42850688489fa3442c640666220579431ab3ca5b9b6e7823849711f50410`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8959e3f4c53355556f6a26b9554fa7969df4f52095ef3ab438d857b34b21537`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542d98e71ed36e5196e8e56eb51672cee90d0245955cd3a096fe7890e25988bd`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc68b296b826c18e0e8ba7f34f7431a26f00c6771e9601ffa54b0918609e4496`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e1c63df832deecd947510d65e5621614ffc3541271abe48a49af8110bb583956
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594346613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182c2f00b9636ad33d8c21a692ded2676a4bde8e691252b5d883190024703abf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:57:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 04:57:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 04:57:36 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 04:57:37 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 04:59:46 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 04:59:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:59:58 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 04:59:58 GMT
ENV ODOO_VERSION=17.0
# Thu, 29 Feb 2024 19:43:17 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:43:17 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Thu, 29 Feb 2024 19:45:16 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:45:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:45:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:45:24 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:45:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:45:24 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:45:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:45:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:45:24 GMT
USER odoo
# Thu, 29 Feb 2024 19:45:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:45:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f43ff6848102f4c77868ee8bb9ed93933d63150bed68b75cc1f5d0dfa4eeaf`  
		Last Modified: Fri, 16 Feb 2024 05:02:30 GMT  
		Size: 231.1 MB (231118858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515bc635e5eeaa0f3fda344640112c6b0e2582f8d6aaa3dc0009fb1d681c4db2`  
		Last Modified: Fri, 16 Feb 2024 05:02:10 GMT  
		Size: 2.5 MB (2521944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e25e5d8a9ae7f74e57205f1e7763a06398e4eca35535d5738a0c15acf01f65a`  
		Last Modified: Fri, 16 Feb 2024 05:02:09 GMT  
		Size: 463.9 KB (463921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13d8a9c09a0c31b0f1b434558bb21f9b19aab8848ee2ca00ae11928e2abe880`  
		Last Modified: Thu, 29 Feb 2024 19:48:04 GMT  
		Size: 331.8 MB (331839098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2faf5b2bfcea0182fc16423c651920a4b5d478285e62c59c6483b96d38ef039`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23e5d5ddfd77ab78b728e615bac24e5d20f62cec2346e1bfd6c9fbee95b495f`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f4c5f6f6f8e35d77bb355a41e6de56e4abb34dc0b3888d06f6098532b8caef`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb9bf8ad500de9273712c13cf52dae548d7dff9f91afee8f39f334e99a5b13`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:ce6893908c634487e5626800434c6689338080bb4e82a287f3fca420e3e8a0ba
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616170059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e136b2c387d57e154e9f4a2ae521d18d0d52ae73df1409c3723caaf04ac4f331`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:13:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 03:13:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 03:13:22 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 03:13:24 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 03:18:19 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 03:18:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:18:53 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 03:18:53 GMT
ENV ODOO_VERSION=17.0
# Thu, 29 Feb 2024 19:16:50 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:16:51 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Thu, 29 Feb 2024 19:21:04 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:21:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:21:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:21:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:21:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:21:22 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:21:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:21:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:21:25 GMT
USER odoo
# Thu, 29 Feb 2024 19:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:21:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37661a9a66b2c085c3f14ffbdfd66fca377d91f4ac8e19c84b1d974df8bde58`  
		Last Modified: Fri, 16 Feb 2024 03:24:00 GMT  
		Size: 243.3 MB (243296258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b85f5c08a6ecd6bc82853f75fbba6a2a0cb997a9704c6bfa5ce3bc19fc3087`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 2.8 MB (2805389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a0feb433839259f36e7cd3c4a48a25d6f8449e6a84091134ad9af509aa7c1c`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 464.0 KB (464004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c147f01b56f517aef5569dc2b1506841c81a78033dfa7959d3a24c26d403e8`  
		Last Modified: Thu, 29 Feb 2024 19:26:59 GMT  
		Size: 334.0 MB (333973101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6114963141787810168c32632e6c3a80614e29c382ff509ef5afa13c0228a21b`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb27a1f7b02ac82bd9b532437758284eff1241f4d3560a49c229c0f84b9d7db0`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f60372d84f5bfaa48edebe504dce062d94a1036d2b3c0d965e439d1d9f5242`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec325085226e97230efc8b1236735a7b77194124b24ce3afeb4e1acea694c9d3`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:7be75cd6e517879310f9dec9090a6b25345a5bc219c4ba22f7bab9c699faff7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:f065f2807c55742df979983385d59cf3d14c79b723d7d429fa505c2bb334553e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599406969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697778a8975ba915513dee14438d400acb0530fe9d081436803d284a360e678a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:23:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 02:23:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 02:23:57 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 02:23:58 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 02:25:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 02:26:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:26:12 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 02:26:12 GMT
ENV ODOO_VERSION=17.0
# Thu, 29 Feb 2024 19:25:03 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:25:03 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Thu, 29 Feb 2024 19:26:56 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:27:00 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:27:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:27:01 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:27:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:27:01 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:27:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:27:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:27:01 GMT
USER odoo
# Thu, 29 Feb 2024 19:27:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:27:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb9367916e4f1ff7e545a30dff1796f82c18802f3d1b24c43a6e928c02511ee`  
		Last Modified: Fri, 16 Feb 2024 02:29:04 GMT  
		Size: 233.7 MB (233731383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cf39849cf6ab3e832eeac1fd52f105ef9917fabeaa12f969681fe53e462652`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 2.5 MB (2529496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f7e2693b9cb165cab924bf88c5543b01a3b122e4586070fee4bb4194bf39ec`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 463.9 KB (463923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22d57e76feea15161f1175c14a0a856e03dc43dbc6da22a041da58ebc88d955`  
		Last Modified: Thu, 29 Feb 2024 19:30:59 GMT  
		Size: 332.2 MB (332229624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36b42850688489fa3442c640666220579431ab3ca5b9b6e7823849711f50410`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8959e3f4c53355556f6a26b9554fa7969df4f52095ef3ab438d857b34b21537`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542d98e71ed36e5196e8e56eb51672cee90d0245955cd3a096fe7890e25988bd`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc68b296b826c18e0e8ba7f34f7431a26f00c6771e9601ffa54b0918609e4496`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e1c63df832deecd947510d65e5621614ffc3541271abe48a49af8110bb583956
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594346613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182c2f00b9636ad33d8c21a692ded2676a4bde8e691252b5d883190024703abf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:57:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 04:57:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 04:57:36 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 04:57:37 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 04:59:46 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 04:59:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:59:58 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 04:59:58 GMT
ENV ODOO_VERSION=17.0
# Thu, 29 Feb 2024 19:43:17 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:43:17 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Thu, 29 Feb 2024 19:45:16 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:45:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:45:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:45:24 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:45:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:45:24 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:45:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:45:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:45:24 GMT
USER odoo
# Thu, 29 Feb 2024 19:45:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:45:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f43ff6848102f4c77868ee8bb9ed93933d63150bed68b75cc1f5d0dfa4eeaf`  
		Last Modified: Fri, 16 Feb 2024 05:02:30 GMT  
		Size: 231.1 MB (231118858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515bc635e5eeaa0f3fda344640112c6b0e2582f8d6aaa3dc0009fb1d681c4db2`  
		Last Modified: Fri, 16 Feb 2024 05:02:10 GMT  
		Size: 2.5 MB (2521944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e25e5d8a9ae7f74e57205f1e7763a06398e4eca35535d5738a0c15acf01f65a`  
		Last Modified: Fri, 16 Feb 2024 05:02:09 GMT  
		Size: 463.9 KB (463921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13d8a9c09a0c31b0f1b434558bb21f9b19aab8848ee2ca00ae11928e2abe880`  
		Last Modified: Thu, 29 Feb 2024 19:48:04 GMT  
		Size: 331.8 MB (331839098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2faf5b2bfcea0182fc16423c651920a4b5d478285e62c59c6483b96d38ef039`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23e5d5ddfd77ab78b728e615bac24e5d20f62cec2346e1bfd6c9fbee95b495f`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f4c5f6f6f8e35d77bb355a41e6de56e4abb34dc0b3888d06f6098532b8caef`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb9bf8ad500de9273712c13cf52dae548d7dff9f91afee8f39f334e99a5b13`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:ce6893908c634487e5626800434c6689338080bb4e82a287f3fca420e3e8a0ba
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616170059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e136b2c387d57e154e9f4a2ae521d18d0d52ae73df1409c3723caaf04ac4f331`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:13:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 03:13:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 03:13:22 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 03:13:24 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 03:18:19 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 03:18:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:18:53 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 03:18:53 GMT
ENV ODOO_VERSION=17.0
# Thu, 29 Feb 2024 19:16:50 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:16:51 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Thu, 29 Feb 2024 19:21:04 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:21:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:21:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:21:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:21:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:21:22 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:21:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:21:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:21:25 GMT
USER odoo
# Thu, 29 Feb 2024 19:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:21:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37661a9a66b2c085c3f14ffbdfd66fca377d91f4ac8e19c84b1d974df8bde58`  
		Last Modified: Fri, 16 Feb 2024 03:24:00 GMT  
		Size: 243.3 MB (243296258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b85f5c08a6ecd6bc82853f75fbba6a2a0cb997a9704c6bfa5ce3bc19fc3087`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 2.8 MB (2805389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a0feb433839259f36e7cd3c4a48a25d6f8449e6a84091134ad9af509aa7c1c`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 464.0 KB (464004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c147f01b56f517aef5569dc2b1506841c81a78033dfa7959d3a24c26d403e8`  
		Last Modified: Thu, 29 Feb 2024 19:26:59 GMT  
		Size: 334.0 MB (333973101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6114963141787810168c32632e6c3a80614e29c382ff509ef5afa13c0228a21b`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb27a1f7b02ac82bd9b532437758284eff1241f4d3560a49c229c0f84b9d7db0`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f60372d84f5bfaa48edebe504dce062d94a1036d2b3c0d965e439d1d9f5242`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec325085226e97230efc8b1236735a7b77194124b24ce3afeb4e1acea694c9d3`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:7be75cd6e517879310f9dec9090a6b25345a5bc219c4ba22f7bab9c699faff7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:f065f2807c55742df979983385d59cf3d14c79b723d7d429fa505c2bb334553e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.4 MB (599406969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697778a8975ba915513dee14438d400acb0530fe9d081436803d284a360e678a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:23:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 02:23:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 02:23:57 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 02:23:58 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 02:25:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 02:26:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 02:26:12 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 02:26:12 GMT
ENV ODOO_VERSION=17.0
# Thu, 29 Feb 2024 19:25:03 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:25:03 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Thu, 29 Feb 2024 19:26:56 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:27:00 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:27:00 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:27:01 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:27:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:27:01 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:27:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:27:01 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:27:01 GMT
USER odoo
# Thu, 29 Feb 2024 19:27:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:27:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb9367916e4f1ff7e545a30dff1796f82c18802f3d1b24c43a6e928c02511ee`  
		Last Modified: Fri, 16 Feb 2024 02:29:04 GMT  
		Size: 233.7 MB (233731383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cf39849cf6ab3e832eeac1fd52f105ef9917fabeaa12f969681fe53e462652`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 2.5 MB (2529496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f7e2693b9cb165cab924bf88c5543b01a3b122e4586070fee4bb4194bf39ec`  
		Last Modified: Fri, 16 Feb 2024 02:28:35 GMT  
		Size: 463.9 KB (463923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22d57e76feea15161f1175c14a0a856e03dc43dbc6da22a041da58ebc88d955`  
		Last Modified: Thu, 29 Feb 2024 19:30:59 GMT  
		Size: 332.2 MB (332229624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36b42850688489fa3442c640666220579431ab3ca5b9b6e7823849711f50410`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8959e3f4c53355556f6a26b9554fa7969df4f52095ef3ab438d857b34b21537`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542d98e71ed36e5196e8e56eb51672cee90d0245955cd3a096fe7890e25988bd`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc68b296b826c18e0e8ba7f34f7431a26f00c6771e9601ffa54b0918609e4496`  
		Last Modified: Thu, 29 Feb 2024 19:30:21 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e1c63df832deecd947510d65e5621614ffc3541271abe48a49af8110bb583956
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594346613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182c2f00b9636ad33d8c21a692ded2676a4bde8e691252b5d883190024703abf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:57:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 04:57:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 04:57:36 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 04:57:37 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 04:59:46 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 04:59:56 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:59:58 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 04:59:58 GMT
ENV ODOO_VERSION=17.0
# Thu, 29 Feb 2024 19:43:17 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:43:17 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Thu, 29 Feb 2024 19:45:16 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:45:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:45:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:45:24 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:45:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:45:24 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:45:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:45:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:45:24 GMT
USER odoo
# Thu, 29 Feb 2024 19:45:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:45:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f43ff6848102f4c77868ee8bb9ed93933d63150bed68b75cc1f5d0dfa4eeaf`  
		Last Modified: Fri, 16 Feb 2024 05:02:30 GMT  
		Size: 231.1 MB (231118858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515bc635e5eeaa0f3fda344640112c6b0e2582f8d6aaa3dc0009fb1d681c4db2`  
		Last Modified: Fri, 16 Feb 2024 05:02:10 GMT  
		Size: 2.5 MB (2521944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e25e5d8a9ae7f74e57205f1e7763a06398e4eca35535d5738a0c15acf01f65a`  
		Last Modified: Fri, 16 Feb 2024 05:02:09 GMT  
		Size: 463.9 KB (463921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13d8a9c09a0c31b0f1b434558bb21f9b19aab8848ee2ca00ae11928e2abe880`  
		Last Modified: Thu, 29 Feb 2024 19:48:04 GMT  
		Size: 331.8 MB (331839098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2faf5b2bfcea0182fc16423c651920a4b5d478285e62c59c6483b96d38ef039`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23e5d5ddfd77ab78b728e615bac24e5d20f62cec2346e1bfd6c9fbee95b495f`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f4c5f6f6f8e35d77bb355a41e6de56e4abb34dc0b3888d06f6098532b8caef`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb9bf8ad500de9273712c13cf52dae548d7dff9f91afee8f39f334e99a5b13`  
		Last Modified: Thu, 29 Feb 2024 19:47:23 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:ce6893908c634487e5626800434c6689338080bb4e82a287f3fca420e3e8a0ba
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616170059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e136b2c387d57e154e9f4a2ae521d18d0d52ae73df1409c3723caaf04ac4f331`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:13:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 16 Feb 2024 03:13:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 16 Feb 2024 03:13:22 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Feb 2024 03:13:24 GMT
ARG TARGETARCH
# Fri, 16 Feb 2024 03:18:19 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 16 Feb 2024 03:18:48 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:18:53 GMT
RUN npm install -g rtlcss
# Fri, 16 Feb 2024 03:18:53 GMT
ENV ODOO_VERSION=17.0
# Thu, 29 Feb 2024 19:16:50 GMT
ARG ODOO_RELEASE=20240229
# Thu, 29 Feb 2024 19:16:51 GMT
ARG ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
# Thu, 29 Feb 2024 19:21:04 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 29 Feb 2024 19:21:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 29 Feb 2024 19:21:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 29 Feb 2024 19:21:21 GMT
# ARGS: ODOO_RELEASE=20240229 ODOO_SHA=e6baad4c22936a3913e51e4ddfd40b47c59fd9d4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 29 Feb 2024 19:21:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 29 Feb 2024 19:21:22 GMT
EXPOSE 8069 8071 8072
# Thu, 29 Feb 2024 19:21:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 29 Feb 2024 19:21:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 29 Feb 2024 19:21:25 GMT
USER odoo
# Thu, 29 Feb 2024 19:21:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 29 Feb 2024 19:21:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37661a9a66b2c085c3f14ffbdfd66fca377d91f4ac8e19c84b1d974df8bde58`  
		Last Modified: Fri, 16 Feb 2024 03:24:00 GMT  
		Size: 243.3 MB (243296258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b85f5c08a6ecd6bc82853f75fbba6a2a0cb997a9704c6bfa5ce3bc19fc3087`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 2.8 MB (2805389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a0feb433839259f36e7cd3c4a48a25d6f8449e6a84091134ad9af509aa7c1c`  
		Last Modified: Fri, 16 Feb 2024 03:23:28 GMT  
		Size: 464.0 KB (464004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c147f01b56f517aef5569dc2b1506841c81a78033dfa7959d3a24c26d403e8`  
		Last Modified: Thu, 29 Feb 2024 19:26:59 GMT  
		Size: 334.0 MB (333973101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6114963141787810168c32632e6c3a80614e29c382ff509ef5afa13c0228a21b`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb27a1f7b02ac82bd9b532437758284eff1241f4d3560a49c229c0f84b9d7db0`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f60372d84f5bfaa48edebe504dce062d94a1036d2b3c0d965e439d1d9f5242`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec325085226e97230efc8b1236735a7b77194124b24ce3afeb4e1acea694c9d3`  
		Last Modified: Thu, 29 Feb 2024 19:25:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
