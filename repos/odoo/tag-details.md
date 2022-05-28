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
$ docker pull odoo@sha256:72deb7e839ac2ebfe998aa3530ade03b4a56247852ff8fc4638ffcbd1cd35a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:21a0f9b444617dbb5e0586614934a27a65ecd5596381faa7b15fb7076b0866db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (540026111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6769365d70d6e8d76d77358869a5272c725ea045248214f2531c0a84ac2c526d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 12:01:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 12:01:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 12:01:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:05:39 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:05:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:05:50 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:05:51 GMT
ENV ODOO_VERSION=13.0
# Sat, 28 May 2022 12:05:51 GMT
ARG ODOO_RELEASE=20220520
# Sat, 28 May 2022 12:05:51 GMT
ARG ODOO_SHA=33fd70bdad094c91ccf445753be2043c9b059b33
# Sat, 28 May 2022 12:07:01 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=33fd70bdad094c91ccf445753be2043c9b059b33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 May 2022 12:07:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 28 May 2022 12:07:05 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 May 2022 12:07:05 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=33fd70bdad094c91ccf445753be2043c9b059b33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 28 May 2022 12:07:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 May 2022 12:07:05 GMT
EXPOSE 8069 8071 8072
# Sat, 28 May 2022 12:07:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 May 2022 12:07:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 May 2022 12:07:06 GMT
USER odoo
# Sat, 28 May 2022 12:07:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 12:07:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c79567322b70756577efd1f8dcfa0263c984e263011e9803a7cda6aba5173a5`  
		Last Modified: Sat, 28 May 2022 12:09:33 GMT  
		Size: 207.1 MB (207143382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a85e75296e74df756190aea4b584b8e8697311966131e1f25a32ab750c6a6c`  
		Last Modified: Sat, 28 May 2022 12:09:11 GMT  
		Size: 13.4 MB (13442815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3489e5884bd67ef88e775a66acb08289f084239dc3fc159caa11154b5f40f2`  
		Last Modified: Sat, 28 May 2022 12:09:08 GMT  
		Size: 480.5 KB (480504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132613a237433458a384340719269709400da9055c9499fc5530c7218d1ce1d5`  
		Last Modified: Sat, 28 May 2022 12:09:39 GMT  
		Size: 291.8 MB (291816803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ef1acfde92a768de3c7d66c88e6b0ac574722602b795d77fc8cf24f8bd4137`  
		Last Modified: Sat, 28 May 2022 12:09:06 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa2108da64b736f3117224c68f9630cbd2ac0b5bfb8f38f744c69a0beed3f3d`  
		Last Modified: Sat, 28 May 2022 12:09:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78d9b0304e28270a2bedc0b82ccaf78d7cc07718ddb21014174ac2122f7db54`  
		Last Modified: Sat, 28 May 2022 12:09:06 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe87d3a84bbad78227baa52dec64a8dc6943e37bbb4f07e02a5c6abf086ced43`  
		Last Modified: Sat, 28 May 2022 12:09:06 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:72deb7e839ac2ebfe998aa3530ade03b4a56247852ff8fc4638ffcbd1cd35a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:21a0f9b444617dbb5e0586614934a27a65ecd5596381faa7b15fb7076b0866db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (540026111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6769365d70d6e8d76d77358869a5272c725ea045248214f2531c0a84ac2c526d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 12:01:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 12:01:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 12:01:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:05:39 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:05:47 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:05:50 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:05:51 GMT
ENV ODOO_VERSION=13.0
# Sat, 28 May 2022 12:05:51 GMT
ARG ODOO_RELEASE=20220520
# Sat, 28 May 2022 12:05:51 GMT
ARG ODOO_SHA=33fd70bdad094c91ccf445753be2043c9b059b33
# Sat, 28 May 2022 12:07:01 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=33fd70bdad094c91ccf445753be2043c9b059b33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 May 2022 12:07:04 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 28 May 2022 12:07:05 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 May 2022 12:07:05 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=33fd70bdad094c91ccf445753be2043c9b059b33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 28 May 2022 12:07:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 May 2022 12:07:05 GMT
EXPOSE 8069 8071 8072
# Sat, 28 May 2022 12:07:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 May 2022 12:07:06 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 May 2022 12:07:06 GMT
USER odoo
# Sat, 28 May 2022 12:07:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 12:07:06 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c79567322b70756577efd1f8dcfa0263c984e263011e9803a7cda6aba5173a5`  
		Last Modified: Sat, 28 May 2022 12:09:33 GMT  
		Size: 207.1 MB (207143382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a85e75296e74df756190aea4b584b8e8697311966131e1f25a32ab750c6a6c`  
		Last Modified: Sat, 28 May 2022 12:09:11 GMT  
		Size: 13.4 MB (13442815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3489e5884bd67ef88e775a66acb08289f084239dc3fc159caa11154b5f40f2`  
		Last Modified: Sat, 28 May 2022 12:09:08 GMT  
		Size: 480.5 KB (480504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132613a237433458a384340719269709400da9055c9499fc5530c7218d1ce1d5`  
		Last Modified: Sat, 28 May 2022 12:09:39 GMT  
		Size: 291.8 MB (291816803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ef1acfde92a768de3c7d66c88e6b0ac574722602b795d77fc8cf24f8bd4137`  
		Last Modified: Sat, 28 May 2022 12:09:06 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa2108da64b736f3117224c68f9630cbd2ac0b5bfb8f38f744c69a0beed3f3d`  
		Last Modified: Sat, 28 May 2022 12:09:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78d9b0304e28270a2bedc0b82ccaf78d7cc07718ddb21014174ac2122f7db54`  
		Last Modified: Sat, 28 May 2022 12:09:06 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe87d3a84bbad78227baa52dec64a8dc6943e37bbb4f07e02a5c6abf086ced43`  
		Last Modified: Sat, 28 May 2022 12:09:06 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:1a3a02f469dd3c9369cf372aa7d3e5abd975391bfad714173b24a024ffba2592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:0c3d1d3349c20c28649473af46cc9869d4b76227c224046550cce03bc5128bc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.1 MB (530136205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63c4d4db5057459f61927eb4377064524ceda1802846348dbb5677b47e2772f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 12:01:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 12:01:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 12:01:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:02:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:03:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:03:12 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:03:12 GMT
ENV ODOO_VERSION=14.0
# Sat, 28 May 2022 12:03:12 GMT
ARG ODOO_RELEASE=20220520
# Sat, 28 May 2022 12:03:12 GMT
ARG ODOO_SHA=f666f4a72c7ace2fa13eea01970012011c7d4828
# Sat, 28 May 2022 12:04:22 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=f666f4a72c7ace2fa13eea01970012011c7d4828
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 May 2022 12:04:26 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 28 May 2022 12:04:26 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 May 2022 12:04:27 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=f666f4a72c7ace2fa13eea01970012011c7d4828
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 28 May 2022 12:04:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 May 2022 12:04:27 GMT
EXPOSE 8069 8071 8072
# Sat, 28 May 2022 12:04:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 May 2022 12:04:27 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 May 2022 12:04:28 GMT
USER odoo
# Sat, 28 May 2022 12:04:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 12:04:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608dd6a1d283847f2f81e849d0bc623071e8222593eee6db00992e4b10b89700`  
		Last Modified: Sat, 28 May 2022 12:08:49 GMT  
		Size: 213.2 MB (213182131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca95c4836277ec91a64f63d069fe261f1155cd52d36b779818dc11814d993346`  
		Last Modified: Sat, 28 May 2022 12:08:27 GMT  
		Size: 13.4 MB (13445276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee21d359e137fb4b2d1a88d7964e3d51382ec95d462e59aea10e50328972a92`  
		Last Modified: Sat, 28 May 2022 12:08:24 GMT  
		Size: 480.4 KB (480424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59845ca7759293974a1090b5c4c2e3c70c531e99d130d62971cf7e6194e22d6`  
		Last Modified: Sat, 28 May 2022 12:08:56 GMT  
		Size: 275.9 MB (275885764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70851319c6ddb137c7433e956e224b732aa87079d0834e7af678b016293b91c1`  
		Last Modified: Sat, 28 May 2022 12:08:22 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7e78473edf92963809b358db3163aa7b80f9f28953e084a8e29751b0556e52`  
		Last Modified: Sat, 28 May 2022 12:08:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1abc9323fd2f5b9950da443a290f6a96f249fb0c85e3486ca6eac70a1f6db3`  
		Last Modified: Sat, 28 May 2022 12:08:22 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5421ac6a726bef372bed0c6fbcede7cc119009c2faee3fd192ef1d4aef9a6e`  
		Last Modified: Sat, 28 May 2022 12:08:22 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:1a3a02f469dd3c9369cf372aa7d3e5abd975391bfad714173b24a024ffba2592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:0c3d1d3349c20c28649473af46cc9869d4b76227c224046550cce03bc5128bc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.1 MB (530136205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63c4d4db5057459f61927eb4377064524ceda1802846348dbb5677b47e2772f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 12:01:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 12:01:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 12:01:50 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:02:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:03:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:03:12 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:03:12 GMT
ENV ODOO_VERSION=14.0
# Sat, 28 May 2022 12:03:12 GMT
ARG ODOO_RELEASE=20220520
# Sat, 28 May 2022 12:03:12 GMT
ARG ODOO_SHA=f666f4a72c7ace2fa13eea01970012011c7d4828
# Sat, 28 May 2022 12:04:22 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=f666f4a72c7ace2fa13eea01970012011c7d4828
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 May 2022 12:04:26 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 28 May 2022 12:04:26 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 May 2022 12:04:27 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=f666f4a72c7ace2fa13eea01970012011c7d4828
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 28 May 2022 12:04:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 May 2022 12:04:27 GMT
EXPOSE 8069 8071 8072
# Sat, 28 May 2022 12:04:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 May 2022 12:04:27 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 May 2022 12:04:28 GMT
USER odoo
# Sat, 28 May 2022 12:04:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 12:04:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608dd6a1d283847f2f81e849d0bc623071e8222593eee6db00992e4b10b89700`  
		Last Modified: Sat, 28 May 2022 12:08:49 GMT  
		Size: 213.2 MB (213182131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca95c4836277ec91a64f63d069fe261f1155cd52d36b779818dc11814d993346`  
		Last Modified: Sat, 28 May 2022 12:08:27 GMT  
		Size: 13.4 MB (13445276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee21d359e137fb4b2d1a88d7964e3d51382ec95d462e59aea10e50328972a92`  
		Last Modified: Sat, 28 May 2022 12:08:24 GMT  
		Size: 480.4 KB (480424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a59845ca7759293974a1090b5c4c2e3c70c531e99d130d62971cf7e6194e22d6`  
		Last Modified: Sat, 28 May 2022 12:08:56 GMT  
		Size: 275.9 MB (275885764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70851319c6ddb137c7433e956e224b732aa87079d0834e7af678b016293b91c1`  
		Last Modified: Sat, 28 May 2022 12:08:22 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7e78473edf92963809b358db3163aa7b80f9f28953e084a8e29751b0556e52`  
		Last Modified: Sat, 28 May 2022 12:08:22 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1abc9323fd2f5b9950da443a290f6a96f249fb0c85e3486ca6eac70a1f6db3`  
		Last Modified: Sat, 28 May 2022 12:08:22 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5421ac6a726bef372bed0c6fbcede7cc119009c2faee3fd192ef1d4aef9a6e`  
		Last Modified: Sat, 28 May 2022 12:08:22 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:2ac35f9beffd680e04256f90531da95418f2720f67e4d253c2500e784078241e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:ae5ea94a0436a54fb6ecb36cbc51ba57633b9608a237c860bdce51d0a0fd8879
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.2 MB (555172445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fc661e09c0757910a0c900ae1c5547e6b81554d2ef11a3a94fd56dffa3ac53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:59:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 11:59:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 11:59:12 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:00:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:00:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:00:19 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:00:19 GMT
ENV ODOO_VERSION=15.0
# Sat, 28 May 2022 12:00:19 GMT
ARG ODOO_RELEASE=20220520
# Sat, 28 May 2022 12:00:19 GMT
ARG ODOO_SHA=0663b11f4c05c66aadfe74fbd27b14beaa9e0f07
# Sat, 28 May 2022 12:01:33 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=0663b11f4c05c66aadfe74fbd27b14beaa9e0f07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 May 2022 12:01:37 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 28 May 2022 12:01:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 May 2022 12:01:38 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=0663b11f4c05c66aadfe74fbd27b14beaa9e0f07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 28 May 2022 12:01:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 May 2022 12:01:38 GMT
EXPOSE 8069 8071 8072
# Sat, 28 May 2022 12:01:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 May 2022 12:01:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 May 2022 12:01:38 GMT
USER odoo
# Sat, 28 May 2022 12:01:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 12:01:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e37b27d59935c5c50839381767950da6d3c54f7f411b13929df686c7c2c5cfa`  
		Last Modified: Sat, 28 May 2022 12:08:02 GMT  
		Size: 220.3 MB (220308203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08260db36e74a0f8d1b16ff325980f49c34374c59f07e4005643462652b1e9a0`  
		Last Modified: Sat, 28 May 2022 12:07:36 GMT  
		Size: 2.5 MB (2513560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77ac3bfba98847aec3a79edd77e2cd7a14ff2ce72e6b8e145c8bc738b2fbcd`  
		Last Modified: Sat, 28 May 2022 12:07:35 GMT  
		Size: 474.1 KB (474093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1180581127f4862a28c59949f32288c499c81906d7016f52a297e2525fa79a`  
		Last Modified: Sat, 28 May 2022 12:08:09 GMT  
		Size: 300.5 MB (300494856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f54ebbf91ac79d05e13d47409d9e9c775c4b7145b6a1a480a64d85eb7fb2c04`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4c788902fed312029bbeed01552b28a4c0c4d9b205ba5095ca43ed2b73a6eb`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004cff4966af458e562bb73e22849b1124a61d4fc8d049bec69f0b357cd3c686`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff000d5cface257df463692de7dfade9590c927751e80f82d6d61dd06865edc1`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:2ac35f9beffd680e04256f90531da95418f2720f67e4d253c2500e784078241e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:ae5ea94a0436a54fb6ecb36cbc51ba57633b9608a237c860bdce51d0a0fd8879
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.2 MB (555172445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fc661e09c0757910a0c900ae1c5547e6b81554d2ef11a3a94fd56dffa3ac53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:59:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 11:59:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 11:59:12 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:00:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:00:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:00:19 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:00:19 GMT
ENV ODOO_VERSION=15.0
# Sat, 28 May 2022 12:00:19 GMT
ARG ODOO_RELEASE=20220520
# Sat, 28 May 2022 12:00:19 GMT
ARG ODOO_SHA=0663b11f4c05c66aadfe74fbd27b14beaa9e0f07
# Sat, 28 May 2022 12:01:33 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=0663b11f4c05c66aadfe74fbd27b14beaa9e0f07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 May 2022 12:01:37 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 28 May 2022 12:01:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 May 2022 12:01:38 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=0663b11f4c05c66aadfe74fbd27b14beaa9e0f07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 28 May 2022 12:01:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 May 2022 12:01:38 GMT
EXPOSE 8069 8071 8072
# Sat, 28 May 2022 12:01:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 May 2022 12:01:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 May 2022 12:01:38 GMT
USER odoo
# Sat, 28 May 2022 12:01:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 12:01:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e37b27d59935c5c50839381767950da6d3c54f7f411b13929df686c7c2c5cfa`  
		Last Modified: Sat, 28 May 2022 12:08:02 GMT  
		Size: 220.3 MB (220308203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08260db36e74a0f8d1b16ff325980f49c34374c59f07e4005643462652b1e9a0`  
		Last Modified: Sat, 28 May 2022 12:07:36 GMT  
		Size: 2.5 MB (2513560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77ac3bfba98847aec3a79edd77e2cd7a14ff2ce72e6b8e145c8bc738b2fbcd`  
		Last Modified: Sat, 28 May 2022 12:07:35 GMT  
		Size: 474.1 KB (474093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1180581127f4862a28c59949f32288c499c81906d7016f52a297e2525fa79a`  
		Last Modified: Sat, 28 May 2022 12:08:09 GMT  
		Size: 300.5 MB (300494856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f54ebbf91ac79d05e13d47409d9e9c775c4b7145b6a1a480a64d85eb7fb2c04`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4c788902fed312029bbeed01552b28a4c0c4d9b205ba5095ca43ed2b73a6eb`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004cff4966af458e562bb73e22849b1124a61d4fc8d049bec69f0b357cd3c686`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff000d5cface257df463692de7dfade9590c927751e80f82d6d61dd06865edc1`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:2ac35f9beffd680e04256f90531da95418f2720f67e4d253c2500e784078241e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:ae5ea94a0436a54fb6ecb36cbc51ba57633b9608a237c860bdce51d0a0fd8879
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.2 MB (555172445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fc661e09c0757910a0c900ae1c5547e6b81554d2ef11a3a94fd56dffa3ac53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:59:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 11:59:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 11:59:12 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:00:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:00:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:00:19 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:00:19 GMT
ENV ODOO_VERSION=15.0
# Sat, 28 May 2022 12:00:19 GMT
ARG ODOO_RELEASE=20220520
# Sat, 28 May 2022 12:00:19 GMT
ARG ODOO_SHA=0663b11f4c05c66aadfe74fbd27b14beaa9e0f07
# Sat, 28 May 2022 12:01:33 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=0663b11f4c05c66aadfe74fbd27b14beaa9e0f07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 May 2022 12:01:37 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 28 May 2022 12:01:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 May 2022 12:01:38 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=0663b11f4c05c66aadfe74fbd27b14beaa9e0f07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 28 May 2022 12:01:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 May 2022 12:01:38 GMT
EXPOSE 8069 8071 8072
# Sat, 28 May 2022 12:01:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 May 2022 12:01:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 May 2022 12:01:38 GMT
USER odoo
# Sat, 28 May 2022 12:01:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 12:01:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e37b27d59935c5c50839381767950da6d3c54f7f411b13929df686c7c2c5cfa`  
		Last Modified: Sat, 28 May 2022 12:08:02 GMT  
		Size: 220.3 MB (220308203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08260db36e74a0f8d1b16ff325980f49c34374c59f07e4005643462652b1e9a0`  
		Last Modified: Sat, 28 May 2022 12:07:36 GMT  
		Size: 2.5 MB (2513560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77ac3bfba98847aec3a79edd77e2cd7a14ff2ce72e6b8e145c8bc738b2fbcd`  
		Last Modified: Sat, 28 May 2022 12:07:35 GMT  
		Size: 474.1 KB (474093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1180581127f4862a28c59949f32288c499c81906d7016f52a297e2525fa79a`  
		Last Modified: Sat, 28 May 2022 12:08:09 GMT  
		Size: 300.5 MB (300494856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f54ebbf91ac79d05e13d47409d9e9c775c4b7145b6a1a480a64d85eb7fb2c04`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4c788902fed312029bbeed01552b28a4c0c4d9b205ba5095ca43ed2b73a6eb`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004cff4966af458e562bb73e22849b1124a61d4fc8d049bec69f0b357cd3c686`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff000d5cface257df463692de7dfade9590c927751e80f82d6d61dd06865edc1`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
