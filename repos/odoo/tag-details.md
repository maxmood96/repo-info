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
$ docker pull odoo@sha256:975d59cc187a317cdf65327f1bfe2bfaa64259b9e596597e799e96eb31b1bfb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:e77303610e6ab41e9f887d146b1f19de09955f6bd4ed9df85e075069fdf2bc8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.7 MB (539674589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30d8a003aa3d5a0769f99e4dd1cdd7ff577b7a4557020aceec27a8b1c124f52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:43:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 18 Mar 2022 08:43:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 18 Mar 2022 08:43:33 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 08:47:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 18 Mar 2022 08:48:20 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:48:23 GMT
RUN npm install -g rtlcss
# Fri, 18 Mar 2022 08:48:23 GMT
ENV ODOO_VERSION=13.0
# Fri, 25 Mar 2022 19:22:36 GMT
ARG ODOO_RELEASE=20220325
# Fri, 25 Mar 2022 19:22:36 GMT
ARG ODOO_SHA=93b53403ec8f09103d6c2cb70dc4901756bc58d2
# Fri, 25 Mar 2022 19:24:27 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=93b53403ec8f09103d6c2cb70dc4901756bc58d2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Mar 2022 19:24:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Mar 2022 19:24:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Mar 2022 19:24:31 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=93b53403ec8f09103d6c2cb70dc4901756bc58d2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Mar 2022 19:24:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Mar 2022 19:24:31 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Mar 2022 19:24:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Mar 2022 19:24:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Mar 2022 19:24:31 GMT
USER odoo
# Fri, 25 Mar 2022 19:24:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 19:24:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af34b027e523073c7675ff12f9ad5be8103e416da025f5404332e3cf0db43f35`  
		Last Modified: Fri, 18 Mar 2022 08:52:07 GMT  
		Size: 207.1 MB (207134258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13e5ae8a871168ea464816a7e582d1a276372a2c52ad4800bac7bd56a6fb924`  
		Last Modified: Fri, 18 Mar 2022 08:51:45 GMT  
		Size: 13.4 MB (13438629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74509aad15ce51f9c500e5e3c2954a378c94d498decc206e5111c2639add3dcf`  
		Last Modified: Fri, 18 Mar 2022 08:51:42 GMT  
		Size: 457.3 KB (457251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fa74bb8e30588e7f25775549360c9bf65de8ded8b580b8ec824ca6c93efbcd`  
		Last Modified: Fri, 25 Mar 2022 19:26:55 GMT  
		Size: 291.5 MB (291488158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dc7e77f104a10db6bd8fe51bc1c7c841425dbce30fdb75d799e4d5b4c7ed64`  
		Last Modified: Fri, 25 Mar 2022 19:26:25 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fce0281b4a0da0fd11979cb608828beb5ae07906ab4a26f61d26a6cf4d3e881`  
		Last Modified: Fri, 25 Mar 2022 19:26:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9862400509c699d7f9df58942ce784bfc94632ae71a00eccb2373144e783111`  
		Last Modified: Fri, 25 Mar 2022 19:26:25 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a256f33020db619cb12ebe452243715ddc3f54fe55960c0a0d37db7eb2b1867d`  
		Last Modified: Fri, 25 Mar 2022 19:26:25 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:975d59cc187a317cdf65327f1bfe2bfaa64259b9e596597e799e96eb31b1bfb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:e77303610e6ab41e9f887d146b1f19de09955f6bd4ed9df85e075069fdf2bc8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.7 MB (539674589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30d8a003aa3d5a0769f99e4dd1cdd7ff577b7a4557020aceec27a8b1c124f52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:43:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 18 Mar 2022 08:43:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 18 Mar 2022 08:43:33 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 08:47:38 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 18 Mar 2022 08:48:20 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:48:23 GMT
RUN npm install -g rtlcss
# Fri, 18 Mar 2022 08:48:23 GMT
ENV ODOO_VERSION=13.0
# Fri, 25 Mar 2022 19:22:36 GMT
ARG ODOO_RELEASE=20220325
# Fri, 25 Mar 2022 19:22:36 GMT
ARG ODOO_SHA=93b53403ec8f09103d6c2cb70dc4901756bc58d2
# Fri, 25 Mar 2022 19:24:27 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=93b53403ec8f09103d6c2cb70dc4901756bc58d2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Mar 2022 19:24:30 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Mar 2022 19:24:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Mar 2022 19:24:31 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=93b53403ec8f09103d6c2cb70dc4901756bc58d2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Mar 2022 19:24:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Mar 2022 19:24:31 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Mar 2022 19:24:31 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Mar 2022 19:24:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Mar 2022 19:24:31 GMT
USER odoo
# Fri, 25 Mar 2022 19:24:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 19:24:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af34b027e523073c7675ff12f9ad5be8103e416da025f5404332e3cf0db43f35`  
		Last Modified: Fri, 18 Mar 2022 08:52:07 GMT  
		Size: 207.1 MB (207134258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13e5ae8a871168ea464816a7e582d1a276372a2c52ad4800bac7bd56a6fb924`  
		Last Modified: Fri, 18 Mar 2022 08:51:45 GMT  
		Size: 13.4 MB (13438629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74509aad15ce51f9c500e5e3c2954a378c94d498decc206e5111c2639add3dcf`  
		Last Modified: Fri, 18 Mar 2022 08:51:42 GMT  
		Size: 457.3 KB (457251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fa74bb8e30588e7f25775549360c9bf65de8ded8b580b8ec824ca6c93efbcd`  
		Last Modified: Fri, 25 Mar 2022 19:26:55 GMT  
		Size: 291.5 MB (291488158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dc7e77f104a10db6bd8fe51bc1c7c841425dbce30fdb75d799e4d5b4c7ed64`  
		Last Modified: Fri, 25 Mar 2022 19:26:25 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fce0281b4a0da0fd11979cb608828beb5ae07906ab4a26f61d26a6cf4d3e881`  
		Last Modified: Fri, 25 Mar 2022 19:26:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9862400509c699d7f9df58942ce784bfc94632ae71a00eccb2373144e783111`  
		Last Modified: Fri, 25 Mar 2022 19:26:25 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a256f33020db619cb12ebe452243715ddc3f54fe55960c0a0d37db7eb2b1867d`  
		Last Modified: Fri, 25 Mar 2022 19:26:25 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:c2affa716a0971fad7a52578064abb5b0c401d4be2046848dead1336f447d553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:01015d4fa84fa9e0e0895b794f19b419de49fbc92dd2e943e0cc07e2d514f312
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529535129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd88ded5be371063be3537852c8fe2dc38cdc83854c6b65ef7a1e43f2e60b578`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:43:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 18 Mar 2022 08:43:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 18 Mar 2022 08:43:33 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 08:44:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 18 Mar 2022 08:45:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:45:09 GMT
RUN npm install -g rtlcss
# Fri, 18 Mar 2022 08:45:09 GMT
ENV ODOO_VERSION=14.0
# Fri, 25 Mar 2022 19:21:13 GMT
ARG ODOO_RELEASE=20220325
# Fri, 25 Mar 2022 19:21:13 GMT
ARG ODOO_SHA=eabfcf757b772782f11db1ea484e9319be58c3c5
# Fri, 25 Mar 2022 19:22:23 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=eabfcf757b772782f11db1ea484e9319be58c3c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Mar 2022 19:22:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Mar 2022 19:22:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Mar 2022 19:22:28 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=eabfcf757b772782f11db1ea484e9319be58c3c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Mar 2022 19:22:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Mar 2022 19:22:28 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Mar 2022 19:22:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Mar 2022 19:22:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Mar 2022 19:22:28 GMT
USER odoo
# Fri, 25 Mar 2022 19:22:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 19:22:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0faaa559017c2d6ff94384d09ad315a52f26cb01e5870bf721605cc8546508`  
		Last Modified: Fri, 18 Mar 2022 08:51:23 GMT  
		Size: 213.2 MB (213174285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ead5a3160839dfe6d7a3807c708dee7ce4bbdcc2a8d84878c88da20dee986d`  
		Last Modified: Fri, 18 Mar 2022 08:50:59 GMT  
		Size: 13.4 MB (13440836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38508374ad87df6acc92d697d514235f01e68121874d684a3662d65aed523024`  
		Last Modified: Fri, 18 Mar 2022 08:50:56 GMT  
		Size: 457.3 KB (457280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f9c12cfbb21b6f8b34b8c7db8af1814c2637c804fc4de1b5a547908078ed06`  
		Last Modified: Fri, 25 Mar 2022 19:26:14 GMT  
		Size: 275.3 MB (275306433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc69ee0a195aba02aa08726d644b354ee959b38f150de0a7abc44d115a47ff1`  
		Last Modified: Fri, 25 Mar 2022 19:25:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123b473fbea82268cb8fbeb1eda23e7a2c07a71383385c6f497e990b3e95fd55`  
		Last Modified: Fri, 25 Mar 2022 19:25:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed4b2e695736b50a76023d6c8fd628b17f16f944a181015caf2a6d01820cd80`  
		Last Modified: Fri, 25 Mar 2022 19:25:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7ef55e63fe440e1c1e2d9a0d6aa8b5d4e3a8e88a986661059a70cac6c2622c`  
		Last Modified: Fri, 25 Mar 2022 19:25:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:c2affa716a0971fad7a52578064abb5b0c401d4be2046848dead1336f447d553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:01015d4fa84fa9e0e0895b794f19b419de49fbc92dd2e943e0cc07e2d514f312
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529535129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd88ded5be371063be3537852c8fe2dc38cdc83854c6b65ef7a1e43f2e60b578`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:43:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 18 Mar 2022 08:43:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 18 Mar 2022 08:43:33 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 08:44:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 18 Mar 2022 08:45:05 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:45:09 GMT
RUN npm install -g rtlcss
# Fri, 18 Mar 2022 08:45:09 GMT
ENV ODOO_VERSION=14.0
# Fri, 25 Mar 2022 19:21:13 GMT
ARG ODOO_RELEASE=20220325
# Fri, 25 Mar 2022 19:21:13 GMT
ARG ODOO_SHA=eabfcf757b772782f11db1ea484e9319be58c3c5
# Fri, 25 Mar 2022 19:22:23 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=eabfcf757b772782f11db1ea484e9319be58c3c5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Mar 2022 19:22:27 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Mar 2022 19:22:27 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Mar 2022 19:22:28 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=eabfcf757b772782f11db1ea484e9319be58c3c5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Mar 2022 19:22:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Mar 2022 19:22:28 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Mar 2022 19:22:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Mar 2022 19:22:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Mar 2022 19:22:28 GMT
USER odoo
# Fri, 25 Mar 2022 19:22:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 19:22:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0faaa559017c2d6ff94384d09ad315a52f26cb01e5870bf721605cc8546508`  
		Last Modified: Fri, 18 Mar 2022 08:51:23 GMT  
		Size: 213.2 MB (213174285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ead5a3160839dfe6d7a3807c708dee7ce4bbdcc2a8d84878c88da20dee986d`  
		Last Modified: Fri, 18 Mar 2022 08:50:59 GMT  
		Size: 13.4 MB (13440836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38508374ad87df6acc92d697d514235f01e68121874d684a3662d65aed523024`  
		Last Modified: Fri, 18 Mar 2022 08:50:56 GMT  
		Size: 457.3 KB (457280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f9c12cfbb21b6f8b34b8c7db8af1814c2637c804fc4de1b5a547908078ed06`  
		Last Modified: Fri, 25 Mar 2022 19:26:14 GMT  
		Size: 275.3 MB (275306433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc69ee0a195aba02aa08726d644b354ee959b38f150de0a7abc44d115a47ff1`  
		Last Modified: Fri, 25 Mar 2022 19:25:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123b473fbea82268cb8fbeb1eda23e7a2c07a71383385c6f497e990b3e95fd55`  
		Last Modified: Fri, 25 Mar 2022 19:25:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed4b2e695736b50a76023d6c8fd628b17f16f944a181015caf2a6d01820cd80`  
		Last Modified: Fri, 25 Mar 2022 19:25:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7ef55e63fe440e1c1e2d9a0d6aa8b5d4e3a8e88a986661059a70cac6c2622c`  
		Last Modified: Fri, 25 Mar 2022 19:25:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:bf08efd58d03868f7488cac6e7a4b35bd72950ea3fea57edd6f3c8190fb6c584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:7a3cf9f366c5fbbb05e594f83d70b887096c1d1b96363fea2bb72e95e168a2e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.5 MB (551533241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f16d800a8ab1dcf0c983f4e06ca15da9b9cfef0479830781a326c330fba0f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:59 GMT
ADD file:36919ae6bb25e3269eff949443129a01a8a43fb967fe6563939ebe1e1e9b8228 in / 
# Thu, 17 Mar 2022 04:03:59 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:40:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 18 Mar 2022 08:40:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 18 Mar 2022 08:40:10 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 08:41:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 18 Mar 2022 08:41:58 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:42:00 GMT
RUN npm install -g rtlcss
# Fri, 18 Mar 2022 08:42:00 GMT
ENV ODOO_VERSION=15.0
# Fri, 25 Mar 2022 19:19:51 GMT
ARG ODOO_RELEASE=20220325
# Fri, 25 Mar 2022 19:19:51 GMT
ARG ODOO_SHA=3d498c38022150b5e3907f2d72346cefe3e16809
# Fri, 25 Mar 2022 19:21:05 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=3d498c38022150b5e3907f2d72346cefe3e16809
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Mar 2022 19:21:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Mar 2022 19:21:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Mar 2022 19:21:10 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=3d498c38022150b5e3907f2d72346cefe3e16809
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Mar 2022 19:21:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Mar 2022 19:21:10 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Mar 2022 19:21:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Mar 2022 19:21:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Mar 2022 19:21:10 GMT
USER odoo
# Fri, 25 Mar 2022 19:21:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 19:21:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ae13dd57832654086618a81dbc128846aa092489260c326ee95429b63c3cf213`  
		Last Modified: Thu, 17 Mar 2022 04:10:05 GMT  
		Size: 31.4 MB (31376572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b017bd0f3af794ea97d29bea01710b0112b2dd1193ae49ba1f535e87d7bf27`  
		Last Modified: Fri, 18 Mar 2022 08:50:35 GMT  
		Size: 220.3 MB (220298052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f81dd0cadac34bb3b184c1c920982bd6981304e625e5ad01b9dce5f2bc784d6`  
		Last Modified: Fri, 18 Mar 2022 08:50:04 GMT  
		Size: 2.5 MB (2509910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fc845e3739ad670483a172d5d1497e8da58b94a3d5c68a7f2d7eb5f7baab7c`  
		Last Modified: Fri, 18 Mar 2022 08:50:03 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e10bbd7e1f2e042a50d54fb4e4990cb2cf911a4646cbdeb680ec4c441c6764f`  
		Last Modified: Fri, 25 Mar 2022 19:25:29 GMT  
		Size: 296.9 MB (296895408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d27d86466ff424c9060bc9c659ee58b9e8c26ea0a4bfd51cbcbedb0c3abe65`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f76a21b5ca0aa40986bb150430365500a9fc271de676721b3f23e51b8a58f2`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e17ff53ea3bb2b9014ffc104a772b7830b08b5746e20575a255ccdc1478184`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5c53c2b940544b2b5dd99beff42022a67f771e964254348845e2d64b754c4e`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:bf08efd58d03868f7488cac6e7a4b35bd72950ea3fea57edd6f3c8190fb6c584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:7a3cf9f366c5fbbb05e594f83d70b887096c1d1b96363fea2bb72e95e168a2e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.5 MB (551533241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f16d800a8ab1dcf0c983f4e06ca15da9b9cfef0479830781a326c330fba0f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:59 GMT
ADD file:36919ae6bb25e3269eff949443129a01a8a43fb967fe6563939ebe1e1e9b8228 in / 
# Thu, 17 Mar 2022 04:03:59 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:40:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 18 Mar 2022 08:40:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 18 Mar 2022 08:40:10 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 08:41:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 18 Mar 2022 08:41:58 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:42:00 GMT
RUN npm install -g rtlcss
# Fri, 18 Mar 2022 08:42:00 GMT
ENV ODOO_VERSION=15.0
# Fri, 25 Mar 2022 19:19:51 GMT
ARG ODOO_RELEASE=20220325
# Fri, 25 Mar 2022 19:19:51 GMT
ARG ODOO_SHA=3d498c38022150b5e3907f2d72346cefe3e16809
# Fri, 25 Mar 2022 19:21:05 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=3d498c38022150b5e3907f2d72346cefe3e16809
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Mar 2022 19:21:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Mar 2022 19:21:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Mar 2022 19:21:10 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=3d498c38022150b5e3907f2d72346cefe3e16809
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Mar 2022 19:21:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Mar 2022 19:21:10 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Mar 2022 19:21:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Mar 2022 19:21:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Mar 2022 19:21:10 GMT
USER odoo
# Fri, 25 Mar 2022 19:21:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 19:21:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ae13dd57832654086618a81dbc128846aa092489260c326ee95429b63c3cf213`  
		Last Modified: Thu, 17 Mar 2022 04:10:05 GMT  
		Size: 31.4 MB (31376572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b017bd0f3af794ea97d29bea01710b0112b2dd1193ae49ba1f535e87d7bf27`  
		Last Modified: Fri, 18 Mar 2022 08:50:35 GMT  
		Size: 220.3 MB (220298052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f81dd0cadac34bb3b184c1c920982bd6981304e625e5ad01b9dce5f2bc784d6`  
		Last Modified: Fri, 18 Mar 2022 08:50:04 GMT  
		Size: 2.5 MB (2509910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fc845e3739ad670483a172d5d1497e8da58b94a3d5c68a7f2d7eb5f7baab7c`  
		Last Modified: Fri, 18 Mar 2022 08:50:03 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e10bbd7e1f2e042a50d54fb4e4990cb2cf911a4646cbdeb680ec4c441c6764f`  
		Last Modified: Fri, 25 Mar 2022 19:25:29 GMT  
		Size: 296.9 MB (296895408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d27d86466ff424c9060bc9c659ee58b9e8c26ea0a4bfd51cbcbedb0c3abe65`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f76a21b5ca0aa40986bb150430365500a9fc271de676721b3f23e51b8a58f2`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e17ff53ea3bb2b9014ffc104a772b7830b08b5746e20575a255ccdc1478184`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5c53c2b940544b2b5dd99beff42022a67f771e964254348845e2d64b754c4e`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:bf08efd58d03868f7488cac6e7a4b35bd72950ea3fea57edd6f3c8190fb6c584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:7a3cf9f366c5fbbb05e594f83d70b887096c1d1b96363fea2bb72e95e168a2e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.5 MB (551533241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f16d800a8ab1dcf0c983f4e06ca15da9b9cfef0479830781a326c330fba0f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:59 GMT
ADD file:36919ae6bb25e3269eff949443129a01a8a43fb967fe6563939ebe1e1e9b8228 in / 
# Thu, 17 Mar 2022 04:03:59 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:40:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 18 Mar 2022 08:40:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 18 Mar 2022 08:40:10 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 08:41:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 18 Mar 2022 08:41:58 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:42:00 GMT
RUN npm install -g rtlcss
# Fri, 18 Mar 2022 08:42:00 GMT
ENV ODOO_VERSION=15.0
# Fri, 25 Mar 2022 19:19:51 GMT
ARG ODOO_RELEASE=20220325
# Fri, 25 Mar 2022 19:19:51 GMT
ARG ODOO_SHA=3d498c38022150b5e3907f2d72346cefe3e16809
# Fri, 25 Mar 2022 19:21:05 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=3d498c38022150b5e3907f2d72346cefe3e16809
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Mar 2022 19:21:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Mar 2022 19:21:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Mar 2022 19:21:10 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=3d498c38022150b5e3907f2d72346cefe3e16809
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Mar 2022 19:21:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Mar 2022 19:21:10 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Mar 2022 19:21:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Mar 2022 19:21:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Mar 2022 19:21:10 GMT
USER odoo
# Fri, 25 Mar 2022 19:21:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 19:21:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ae13dd57832654086618a81dbc128846aa092489260c326ee95429b63c3cf213`  
		Last Modified: Thu, 17 Mar 2022 04:10:05 GMT  
		Size: 31.4 MB (31376572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b017bd0f3af794ea97d29bea01710b0112b2dd1193ae49ba1f535e87d7bf27`  
		Last Modified: Fri, 18 Mar 2022 08:50:35 GMT  
		Size: 220.3 MB (220298052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f81dd0cadac34bb3b184c1c920982bd6981304e625e5ad01b9dce5f2bc784d6`  
		Last Modified: Fri, 18 Mar 2022 08:50:04 GMT  
		Size: 2.5 MB (2509910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fc845e3739ad670483a172d5d1497e8da58b94a3d5c68a7f2d7eb5f7baab7c`  
		Last Modified: Fri, 18 Mar 2022 08:50:03 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e10bbd7e1f2e042a50d54fb4e4990cb2cf911a4646cbdeb680ec4c441c6764f`  
		Last Modified: Fri, 25 Mar 2022 19:25:29 GMT  
		Size: 296.9 MB (296895408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d27d86466ff424c9060bc9c659ee58b9e8c26ea0a4bfd51cbcbedb0c3abe65`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f76a21b5ca0aa40986bb150430365500a9fc271de676721b3f23e51b8a58f2`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e17ff53ea3bb2b9014ffc104a772b7830b08b5746e20575a255ccdc1478184`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5c53c2b940544b2b5dd99beff42022a67f771e964254348845e2d64b754c4e`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
