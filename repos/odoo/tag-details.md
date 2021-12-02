<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:latest`](#odoolatest)

## `odoo:13`

```console
$ docker pull odoo@sha256:1efd5a007091ac1f9abffa727af7de7de50e5bbe4eb11a2a35c75ea3e82a0bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:56b91d95b6548de22e3547c61faef0239eb6c86439f455c058d420fee90b98d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.3 MB (539329779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689e17aa57d6e8340674a4c1b10156fe54060e7b9bc7b00ab440ce9f86b10736`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:24:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:24:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:24:45 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:29:05 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:29:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:29:34 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:29:34 GMT
ENV ODOO_VERSION=13.0
# Thu, 02 Dec 2021 03:29:34 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 03:29:35 GMT
ARG ODOO_SHA=c16094e8ea981346e6de1171ddec9541905b254f
# Thu, 02 Dec 2021 03:31:09 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=c16094e8ea981346e6de1171ddec9541905b254f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 03:31:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 03:31:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 03:31:14 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=c16094e8ea981346e6de1171ddec9541905b254f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 03:31:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 03:31:15 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 03:31:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 03:31:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 03:31:16 GMT
USER odoo
# Thu, 02 Dec 2021 03:31:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:31:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8988f86f949d08f5ea393c3cb9d4016acd45699f4fb9c3b6a78c8b107d9be55`  
		Last Modified: Thu, 02 Dec 2021 03:34:31 GMT  
		Size: 207.1 MB (207130653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78dd91afcfb205b31d583947328c09101f9c1a292ee4ab5357b9cc5c12a691c`  
		Last Modified: Thu, 02 Dec 2021 03:33:57 GMT  
		Size: 13.4 MB (13434259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875e5005d33be86db39c7b664080d0b957d3d88521bd5d30b592382eddeea0e`  
		Last Modified: Thu, 02 Dec 2021 03:33:52 GMT  
		Size: 425.0 KB (424962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051749ba4a0a2fca19fee484df0fe59a5a509dd9f5bda5b8b796f87d34ac2694`  
		Last Modified: Thu, 02 Dec 2021 03:34:41 GMT  
		Size: 291.2 MB (291183710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4a388e1e51490af1b3280fd37bf7f2df879170740471eac78b16ca5a91e91d`  
		Last Modified: Thu, 02 Dec 2021 03:33:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43526e31befb3d7084d3b95620f7721bd56c0a02a4d829d22d632d89f2b307f6`  
		Last Modified: Thu, 02 Dec 2021 03:33:50 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015cb73e8c22163d9233a882e0bbe59a3ebc52a16fe42f2215122e141ef5c312`  
		Last Modified: Thu, 02 Dec 2021 03:33:50 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2820560b330d605e19cd80a8eacb012cef91b54c13397971e6c39847046233c4`  
		Last Modified: Thu, 02 Dec 2021 03:33:50 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:1efd5a007091ac1f9abffa727af7de7de50e5bbe4eb11a2a35c75ea3e82a0bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:56b91d95b6548de22e3547c61faef0239eb6c86439f455c058d420fee90b98d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.3 MB (539329779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689e17aa57d6e8340674a4c1b10156fe54060e7b9bc7b00ab440ce9f86b10736`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:24:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:24:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:24:45 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:29:05 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:29:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:29:34 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:29:34 GMT
ENV ODOO_VERSION=13.0
# Thu, 02 Dec 2021 03:29:34 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 03:29:35 GMT
ARG ODOO_SHA=c16094e8ea981346e6de1171ddec9541905b254f
# Thu, 02 Dec 2021 03:31:09 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=c16094e8ea981346e6de1171ddec9541905b254f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 03:31:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 03:31:13 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 03:31:14 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=c16094e8ea981346e6de1171ddec9541905b254f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 03:31:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 03:31:15 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 03:31:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 03:31:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 03:31:16 GMT
USER odoo
# Thu, 02 Dec 2021 03:31:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:31:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8988f86f949d08f5ea393c3cb9d4016acd45699f4fb9c3b6a78c8b107d9be55`  
		Last Modified: Thu, 02 Dec 2021 03:34:31 GMT  
		Size: 207.1 MB (207130653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78dd91afcfb205b31d583947328c09101f9c1a292ee4ab5357b9cc5c12a691c`  
		Last Modified: Thu, 02 Dec 2021 03:33:57 GMT  
		Size: 13.4 MB (13434259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c875e5005d33be86db39c7b664080d0b957d3d88521bd5d30b592382eddeea0e`  
		Last Modified: Thu, 02 Dec 2021 03:33:52 GMT  
		Size: 425.0 KB (424962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051749ba4a0a2fca19fee484df0fe59a5a509dd9f5bda5b8b796f87d34ac2694`  
		Last Modified: Thu, 02 Dec 2021 03:34:41 GMT  
		Size: 291.2 MB (291183710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4a388e1e51490af1b3280fd37bf7f2df879170740471eac78b16ca5a91e91d`  
		Last Modified: Thu, 02 Dec 2021 03:33:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43526e31befb3d7084d3b95620f7721bd56c0a02a4d829d22d632d89f2b307f6`  
		Last Modified: Thu, 02 Dec 2021 03:33:50 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015cb73e8c22163d9233a882e0bbe59a3ebc52a16fe42f2215122e141ef5c312`  
		Last Modified: Thu, 02 Dec 2021 03:33:50 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2820560b330d605e19cd80a8eacb012cef91b54c13397971e6c39847046233c4`  
		Last Modified: Thu, 02 Dec 2021 03:33:50 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:f55c0d01769dfb0636da3f243ce0571536245efa0d01e0135230040e71c112d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:2e8d2db393a661bebe15c0c8ea546c9d3775fae85dc143f664c2edfa3f292353
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.0 MB (528965178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65fc2798d848eeb7e77222748efc46173393384af3b8714e1a5d3c95e36d6219`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:24:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:24:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:24:45 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:26:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:26:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:26:27 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:26:27 GMT
ENV ODOO_VERSION=14.0
# Thu, 02 Dec 2021 03:26:27 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 03:26:28 GMT
ARG ODOO_SHA=01d16e4ce92fd341438f1a95984b505c9d62cc14
# Thu, 02 Dec 2021 03:27:42 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=01d16e4ce92fd341438f1a95984b505c9d62cc14
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 03:27:46 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 03:27:47 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 03:27:48 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=01d16e4ce92fd341438f1a95984b505c9d62cc14
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 03:27:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 03:27:48 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 03:27:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 03:27:48 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 03:27:49 GMT
USER odoo
# Thu, 02 Dec 2021 03:27:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:27:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc20adace522abb201c7423e22fd72bcb79776eea50c16f27d7304e0ef69a17`  
		Last Modified: Thu, 02 Dec 2021 03:33:31 GMT  
		Size: 213.2 MB (213172687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1864e4021f806774779a9ca1a51ef676584c0ebfe979b016930caa5019dbebe2`  
		Last Modified: Thu, 02 Dec 2021 03:32:56 GMT  
		Size: 13.4 MB (13436533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c504b4f0face0abb0105469a79f865565c73340c11e0eb38cf2f615bd7f3ff60`  
		Last Modified: Thu, 02 Dec 2021 03:32:52 GMT  
		Size: 424.9 KB (424854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6e899c036c434637a4d9de3412f503463241b1f6f0ac7309a6f9a129701de1`  
		Last Modified: Thu, 02 Dec 2021 03:33:40 GMT  
		Size: 274.8 MB (274774912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a20013c499ef1e409b936c0abbfa3a3bc5f1d17730b2f97ef34a646db5c80e`  
		Last Modified: Thu, 02 Dec 2021 03:32:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7b9e60fbdc17efe5f444cf5b9c4f4c6eab08155b72f43e62656e17a4ed73f9`  
		Last Modified: Thu, 02 Dec 2021 03:32:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea7783dbc45974651d125cfc39ff29486796a36a5140f01bb656ee8fae5f3cb`  
		Last Modified: Thu, 02 Dec 2021 03:32:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb6dfd3234b6c1ebf112ee2ccd7a2619cc8d13703ec4b91bdfdac2c60e6d133`  
		Last Modified: Thu, 02 Dec 2021 03:32:49 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:f55c0d01769dfb0636da3f243ce0571536245efa0d01e0135230040e71c112d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:2e8d2db393a661bebe15c0c8ea546c9d3775fae85dc143f664c2edfa3f292353
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.0 MB (528965178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65fc2798d848eeb7e77222748efc46173393384af3b8714e1a5d3c95e36d6219`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:24:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:24:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:24:45 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:26:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:26:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:26:27 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:26:27 GMT
ENV ODOO_VERSION=14.0
# Thu, 02 Dec 2021 03:26:27 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 03:26:28 GMT
ARG ODOO_SHA=01d16e4ce92fd341438f1a95984b505c9d62cc14
# Thu, 02 Dec 2021 03:27:42 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=01d16e4ce92fd341438f1a95984b505c9d62cc14
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 03:27:46 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 03:27:47 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 03:27:48 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=01d16e4ce92fd341438f1a95984b505c9d62cc14
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 03:27:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 03:27:48 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 03:27:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 03:27:48 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 03:27:49 GMT
USER odoo
# Thu, 02 Dec 2021 03:27:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:27:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc20adace522abb201c7423e22fd72bcb79776eea50c16f27d7304e0ef69a17`  
		Last Modified: Thu, 02 Dec 2021 03:33:31 GMT  
		Size: 213.2 MB (213172687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1864e4021f806774779a9ca1a51ef676584c0ebfe979b016930caa5019dbebe2`  
		Last Modified: Thu, 02 Dec 2021 03:32:56 GMT  
		Size: 13.4 MB (13436533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c504b4f0face0abb0105469a79f865565c73340c11e0eb38cf2f615bd7f3ff60`  
		Last Modified: Thu, 02 Dec 2021 03:32:52 GMT  
		Size: 424.9 KB (424854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6e899c036c434637a4d9de3412f503463241b1f6f0ac7309a6f9a129701de1`  
		Last Modified: Thu, 02 Dec 2021 03:33:40 GMT  
		Size: 274.8 MB (274774912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a20013c499ef1e409b936c0abbfa3a3bc5f1d17730b2f97ef34a646db5c80e`  
		Last Modified: Thu, 02 Dec 2021 03:32:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7b9e60fbdc17efe5f444cf5b9c4f4c6eab08155b72f43e62656e17a4ed73f9`  
		Last Modified: Thu, 02 Dec 2021 03:32:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea7783dbc45974651d125cfc39ff29486796a36a5140f01bb656ee8fae5f3cb`  
		Last Modified: Thu, 02 Dec 2021 03:32:49 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb6dfd3234b6c1ebf112ee2ccd7a2619cc8d13703ec4b91bdfdac2c60e6d133`  
		Last Modified: Thu, 02 Dec 2021 03:32:49 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:434913aa1359d95215af4c7a197e5a3cd81f1500424b78a55eb0677cb6a31ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:2659e367f3fd08670f6b1ed6513f84200e73c86dfb4817ba1520d683ba948172
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.0 MB (546015468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461590b9586ab5dd87d7b5a5e5593df52a52082e462b038f484d75a2936d60de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:21:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:21:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:21:37 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:22:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:23:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:23:04 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:23:04 GMT
ENV ODOO_VERSION=15.0
# Thu, 02 Dec 2021 03:23:04 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 03:23:04 GMT
ARG ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
# Thu, 02 Dec 2021 03:24:26 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 03:24:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 03:24:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 03:24:31 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 03:24:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 03:24:32 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 03:24:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 03:24:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 03:24:33 GMT
USER odoo
# Thu, 02 Dec 2021 03:24:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:24:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8928362baaf188d2d35b07907f7df5a83838f416511d7c90d1001f0f69b22d`  
		Last Modified: Thu, 02 Dec 2021 03:32:31 GMT  
		Size: 220.3 MB (220290298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1196c36b7759c2bc3f823f01785a679ef74915d5281b24e23220cfac4fb643c`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 2.5 MB (2506050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014833e3ecaf723c362d63385e2ff1ece9d0f33f6818690c2ffb8acbbc320186`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 417.8 KB (417795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dfe0c686c4990ade7f8ca86b4df6cfd4bf1742daed87dbd5e60af37da42e1a`  
		Last Modified: Thu, 02 Dec 2021 03:32:35 GMT  
		Size: 291.4 MB (291428645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6663917fdb44e180c376d78b44d466c7e12ec7e23100d70e41cabe4dcbf33357`  
		Last Modified: Thu, 02 Dec 2021 03:31:42 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee159f4631832129f790f7673c1ca3216c6d64310c7ef6f070f898911df9b988`  
		Last Modified: Thu, 02 Dec 2021 03:31:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26679a639358f4eb3f6c499428d55f1f10ca56dd95284bf47c9bdb7c297f1f55`  
		Last Modified: Thu, 02 Dec 2021 03:31:42 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebec24bf7d19b223b07fec2ab41e29b523f7753ce20ca7976e7e3a5ab3b00cc7`  
		Last Modified: Thu, 02 Dec 2021 03:31:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:434913aa1359d95215af4c7a197e5a3cd81f1500424b78a55eb0677cb6a31ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:2659e367f3fd08670f6b1ed6513f84200e73c86dfb4817ba1520d683ba948172
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.0 MB (546015468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461590b9586ab5dd87d7b5a5e5593df52a52082e462b038f484d75a2936d60de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:21:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:21:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:21:37 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:22:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:23:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:23:04 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:23:04 GMT
ENV ODOO_VERSION=15.0
# Thu, 02 Dec 2021 03:23:04 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 03:23:04 GMT
ARG ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
# Thu, 02 Dec 2021 03:24:26 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 03:24:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 03:24:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 03:24:31 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 03:24:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 03:24:32 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 03:24:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 03:24:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 03:24:33 GMT
USER odoo
# Thu, 02 Dec 2021 03:24:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:24:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8928362baaf188d2d35b07907f7df5a83838f416511d7c90d1001f0f69b22d`  
		Last Modified: Thu, 02 Dec 2021 03:32:31 GMT  
		Size: 220.3 MB (220290298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1196c36b7759c2bc3f823f01785a679ef74915d5281b24e23220cfac4fb643c`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 2.5 MB (2506050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014833e3ecaf723c362d63385e2ff1ece9d0f33f6818690c2ffb8acbbc320186`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 417.8 KB (417795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dfe0c686c4990ade7f8ca86b4df6cfd4bf1742daed87dbd5e60af37da42e1a`  
		Last Modified: Thu, 02 Dec 2021 03:32:35 GMT  
		Size: 291.4 MB (291428645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6663917fdb44e180c376d78b44d466c7e12ec7e23100d70e41cabe4dcbf33357`  
		Last Modified: Thu, 02 Dec 2021 03:31:42 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee159f4631832129f790f7673c1ca3216c6d64310c7ef6f070f898911df9b988`  
		Last Modified: Thu, 02 Dec 2021 03:31:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26679a639358f4eb3f6c499428d55f1f10ca56dd95284bf47c9bdb7c297f1f55`  
		Last Modified: Thu, 02 Dec 2021 03:31:42 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebec24bf7d19b223b07fec2ab41e29b523f7753ce20ca7976e7e3a5ab3b00cc7`  
		Last Modified: Thu, 02 Dec 2021 03:31:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:434913aa1359d95215af4c7a197e5a3cd81f1500424b78a55eb0677cb6a31ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:2659e367f3fd08670f6b1ed6513f84200e73c86dfb4817ba1520d683ba948172
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.0 MB (546015468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461590b9586ab5dd87d7b5a5e5593df52a52082e462b038f484d75a2936d60de`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:21:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 Dec 2021 03:21:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 Dec 2021 03:21:37 GMT
ENV LANG=C.UTF-8
# Thu, 02 Dec 2021 03:22:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 Dec 2021 03:23:01 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:23:04 GMT
RUN npm install -g rtlcss
# Thu, 02 Dec 2021 03:23:04 GMT
ENV ODOO_VERSION=15.0
# Thu, 02 Dec 2021 03:23:04 GMT
ARG ODOO_RELEASE=20211201
# Thu, 02 Dec 2021 03:23:04 GMT
ARG ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
# Thu, 02 Dec 2021 03:24:26 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 02 Dec 2021 03:24:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 02 Dec 2021 03:24:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 02 Dec 2021 03:24:31 GMT
# ARGS: ODOO_RELEASE=20211201 ODOO_SHA=8ab8486e502eb7b092ff2fc87037bd0e7a740f52
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 02 Dec 2021 03:24:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 02 Dec 2021 03:24:32 GMT
EXPOSE 8069 8071 8072
# Thu, 02 Dec 2021 03:24:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 02 Dec 2021 03:24:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 02 Dec 2021 03:24:33 GMT
USER odoo
# Thu, 02 Dec 2021 03:24:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:24:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8928362baaf188d2d35b07907f7df5a83838f416511d7c90d1001f0f69b22d`  
		Last Modified: Thu, 02 Dec 2021 03:32:31 GMT  
		Size: 220.3 MB (220290298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1196c36b7759c2bc3f823f01785a679ef74915d5281b24e23220cfac4fb643c`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 2.5 MB (2506050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014833e3ecaf723c362d63385e2ff1ece9d0f33f6818690c2ffb8acbbc320186`  
		Last Modified: Thu, 02 Dec 2021 03:31:45 GMT  
		Size: 417.8 KB (417795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dfe0c686c4990ade7f8ca86b4df6cfd4bf1742daed87dbd5e60af37da42e1a`  
		Last Modified: Thu, 02 Dec 2021 03:32:35 GMT  
		Size: 291.4 MB (291428645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6663917fdb44e180c376d78b44d466c7e12ec7e23100d70e41cabe4dcbf33357`  
		Last Modified: Thu, 02 Dec 2021 03:31:42 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee159f4631832129f790f7673c1ca3216c6d64310c7ef6f070f898911df9b988`  
		Last Modified: Thu, 02 Dec 2021 03:31:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26679a639358f4eb3f6c499428d55f1f10ca56dd95284bf47c9bdb7c297f1f55`  
		Last Modified: Thu, 02 Dec 2021 03:31:42 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebec24bf7d19b223b07fec2ab41e29b523f7753ce20ca7976e7e3a5ab3b00cc7`  
		Last Modified: Thu, 02 Dec 2021 03:31:42 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
