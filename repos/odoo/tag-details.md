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
$ docker pull odoo@sha256:ad8107e8496ce568a14c46926784b826421441146ed788fe66a1eacd420879fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:6b00c152d849a149ed43651dfae2e20ebe60e97c4d5899d2cbe7ff439c27a808
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.2 MB (540225556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191aea8caced7a1313516e4dfd06467fc0276a95f7540bb2bddca9c247b984cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:44:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:44:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:44:57 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:48:46 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:48:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:48:58 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:48:58 GMT
ENV ODOO_VERSION=13.0
# Wed, 29 Jun 2022 18:30:30 GMT
ARG ODOO_RELEASE=20220629
# Wed, 29 Jun 2022 18:30:30 GMT
ARG ODOO_SHA=e6873c12adae0dc8f8258d0e3b3d20f1f6408e4f
# Wed, 29 Jun 2022 18:34:59 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=e6873c12adae0dc8f8258d0e3b3d20f1f6408e4f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Jun 2022 18:35:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Jun 2022 18:35:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Jun 2022 18:35:03 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=e6873c12adae0dc8f8258d0e3b3d20f1f6408e4f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Jun 2022 18:35:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Jun 2022 18:35:03 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Jun 2022 18:35:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Jun 2022 18:35:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Jun 2022 18:35:04 GMT
USER odoo
# Wed, 29 Jun 2022 18:35:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jun 2022 18:35:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83eee462c654020a3586541aea3d6bc53550868ea56856a558c32a009ecc61f`  
		Last Modified: Thu, 23 Jun 2022 04:52:40 GMT  
		Size: 207.1 MB (207143564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccc6ace4d9383ea46d39569a7f843ffb7881fbc9c7cdab672d5e562cda66b37`  
		Last Modified: Thu, 23 Jun 2022 04:52:19 GMT  
		Size: 13.4 MB (13443244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc66057e559306ecef1d2f9dce87fdc3c8e709d9cf592428301154122ecc292`  
		Last Modified: Thu, 23 Jun 2022 04:52:16 GMT  
		Size: 491.8 KB (491847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763556f875f33f36aae362841ec52076bf33653136ca03daa07df9778aa1ecf8`  
		Last Modified: Wed, 29 Jun 2022 18:37:22 GMT  
		Size: 292.0 MB (292004398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ccebef846d885f1009ffbe53d973937cf5ef78ac23f0e3e1ba337d37a52823`  
		Last Modified: Wed, 29 Jun 2022 18:36:51 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc317b9128b5ff97c807b2b1beae1ff9d6be12d1fd9d8cde1660c56219dc842`  
		Last Modified: Wed, 29 Jun 2022 18:36:51 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb20f1c6c28397c00b95992ed5293facf65382ac55d26061b97f8898eb360145`  
		Last Modified: Wed, 29 Jun 2022 18:36:51 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d5e832db25195bfec4fa067ace100ba132d17730af0f3a0e3c0dd074ad94c3`  
		Last Modified: Wed, 29 Jun 2022 18:36:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:ad8107e8496ce568a14c46926784b826421441146ed788fe66a1eacd420879fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:6b00c152d849a149ed43651dfae2e20ebe60e97c4d5899d2cbe7ff439c27a808
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.2 MB (540225556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191aea8caced7a1313516e4dfd06467fc0276a95f7540bb2bddca9c247b984cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:44:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:44:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:44:57 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:48:46 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:48:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:48:58 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:48:58 GMT
ENV ODOO_VERSION=13.0
# Wed, 29 Jun 2022 18:30:30 GMT
ARG ODOO_RELEASE=20220629
# Wed, 29 Jun 2022 18:30:30 GMT
ARG ODOO_SHA=e6873c12adae0dc8f8258d0e3b3d20f1f6408e4f
# Wed, 29 Jun 2022 18:34:59 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=e6873c12adae0dc8f8258d0e3b3d20f1f6408e4f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Jun 2022 18:35:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Jun 2022 18:35:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Jun 2022 18:35:03 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=e6873c12adae0dc8f8258d0e3b3d20f1f6408e4f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Jun 2022 18:35:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Jun 2022 18:35:03 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Jun 2022 18:35:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Jun 2022 18:35:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Jun 2022 18:35:04 GMT
USER odoo
# Wed, 29 Jun 2022 18:35:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jun 2022 18:35:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83eee462c654020a3586541aea3d6bc53550868ea56856a558c32a009ecc61f`  
		Last Modified: Thu, 23 Jun 2022 04:52:40 GMT  
		Size: 207.1 MB (207143564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccc6ace4d9383ea46d39569a7f843ffb7881fbc9c7cdab672d5e562cda66b37`  
		Last Modified: Thu, 23 Jun 2022 04:52:19 GMT  
		Size: 13.4 MB (13443244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc66057e559306ecef1d2f9dce87fdc3c8e709d9cf592428301154122ecc292`  
		Last Modified: Thu, 23 Jun 2022 04:52:16 GMT  
		Size: 491.8 KB (491847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763556f875f33f36aae362841ec52076bf33653136ca03daa07df9778aa1ecf8`  
		Last Modified: Wed, 29 Jun 2022 18:37:22 GMT  
		Size: 292.0 MB (292004398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ccebef846d885f1009ffbe53d973937cf5ef78ac23f0e3e1ba337d37a52823`  
		Last Modified: Wed, 29 Jun 2022 18:36:51 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc317b9128b5ff97c807b2b1beae1ff9d6be12d1fd9d8cde1660c56219dc842`  
		Last Modified: Wed, 29 Jun 2022 18:36:51 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb20f1c6c28397c00b95992ed5293facf65382ac55d26061b97f8898eb360145`  
		Last Modified: Wed, 29 Jun 2022 18:36:51 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d5e832db25195bfec4fa067ace100ba132d17730af0f3a0e3c0dd074ad94c3`  
		Last Modified: Wed, 29 Jun 2022 18:36:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:f9e6480cc41ec440bf11e525bde857b5c3f9e77e98a0baab12f5462057ad1b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:0f022d7f0df834c1d5d34d541f264d6c8e6a4868406359ba0cdd7fa35fb51f1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.5 MB (530530810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6582bba7c6a492f75c42b99d79f4fbafdbc98edee658ce2c421adcb00cb126bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:44:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:44:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:44:57 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:46:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:46:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:46:20 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:46:20 GMT
ENV ODOO_VERSION=14.0
# Wed, 29 Jun 2022 18:28:52 GMT
ARG ODOO_RELEASE=20220629
# Wed, 29 Jun 2022 18:28:52 GMT
ARG ODOO_SHA=ecd7c70bcc58d29d1d43b78a0785d9926fc569b0
# Wed, 29 Jun 2022 18:30:15 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=ecd7c70bcc58d29d1d43b78a0785d9926fc569b0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Jun 2022 18:30:19 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Jun 2022 18:30:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Jun 2022 18:30:20 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=ecd7c70bcc58d29d1d43b78a0785d9926fc569b0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Jun 2022 18:30:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Jun 2022 18:30:20 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Jun 2022 18:30:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Jun 2022 18:30:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Jun 2022 18:30:20 GMT
USER odoo
# Wed, 29 Jun 2022 18:30:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jun 2022 18:30:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfddafe5e99a0c369c5c2c9011265c2b875f1b14e75d44339afebb8c4a79938`  
		Last Modified: Thu, 23 Jun 2022 04:51:57 GMT  
		Size: 213.2 MB (213182993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d794ef76c633a0fd19d5aae7fa2845374d7c5a01d812c71edd98a04287e5b02c`  
		Last Modified: Thu, 23 Jun 2022 04:51:35 GMT  
		Size: 13.4 MB (13444456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1652e870c7471ca1e119944afe2e23f91b602def7422b29d3f254074c4667ee0`  
		Last Modified: Thu, 23 Jun 2022 04:51:32 GMT  
		Size: 491.8 KB (491827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4fea0d4dab28832a576ee60e00b812d6809277378b42e84edde0e2f184be6`  
		Last Modified: Wed, 29 Jun 2022 18:36:40 GMT  
		Size: 276.3 MB (276269026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976806b6df1a298b4a0c164744aeaa61048792a8d32fa2b38a4d33d7ecfb8a63`  
		Last Modified: Wed, 29 Jun 2022 18:36:07 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad8f6d0b28e8d5d8c23b065fef5774c2dc75d1c9e13eb0f3ac9bc6ce82bb69e`  
		Last Modified: Wed, 29 Jun 2022 18:36:07 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f9d8e1293709eb6a2641c2bacdca0f01d2035c7aef236c49121479e19a1c91`  
		Last Modified: Wed, 29 Jun 2022 18:36:08 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e2e7433f86231e8fdea2b588803fd2fc68de734aa166fec758c5f2643e69cd`  
		Last Modified: Wed, 29 Jun 2022 18:36:07 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:f9e6480cc41ec440bf11e525bde857b5c3f9e77e98a0baab12f5462057ad1b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:0f022d7f0df834c1d5d34d541f264d6c8e6a4868406359ba0cdd7fa35fb51f1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.5 MB (530530810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6582bba7c6a492f75c42b99d79f4fbafdbc98edee658ce2c421adcb00cb126bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:44:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:44:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:44:57 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:46:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:46:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:46:20 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:46:20 GMT
ENV ODOO_VERSION=14.0
# Wed, 29 Jun 2022 18:28:52 GMT
ARG ODOO_RELEASE=20220629
# Wed, 29 Jun 2022 18:28:52 GMT
ARG ODOO_SHA=ecd7c70bcc58d29d1d43b78a0785d9926fc569b0
# Wed, 29 Jun 2022 18:30:15 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=ecd7c70bcc58d29d1d43b78a0785d9926fc569b0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Jun 2022 18:30:19 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Jun 2022 18:30:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Jun 2022 18:30:20 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=ecd7c70bcc58d29d1d43b78a0785d9926fc569b0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Jun 2022 18:30:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Jun 2022 18:30:20 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Jun 2022 18:30:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Jun 2022 18:30:20 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Jun 2022 18:30:20 GMT
USER odoo
# Wed, 29 Jun 2022 18:30:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jun 2022 18:30:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfddafe5e99a0c369c5c2c9011265c2b875f1b14e75d44339afebb8c4a79938`  
		Last Modified: Thu, 23 Jun 2022 04:51:57 GMT  
		Size: 213.2 MB (213182993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d794ef76c633a0fd19d5aae7fa2845374d7c5a01d812c71edd98a04287e5b02c`  
		Last Modified: Thu, 23 Jun 2022 04:51:35 GMT  
		Size: 13.4 MB (13444456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1652e870c7471ca1e119944afe2e23f91b602def7422b29d3f254074c4667ee0`  
		Last Modified: Thu, 23 Jun 2022 04:51:32 GMT  
		Size: 491.8 KB (491827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e4fea0d4dab28832a576ee60e00b812d6809277378b42e84edde0e2f184be6`  
		Last Modified: Wed, 29 Jun 2022 18:36:40 GMT  
		Size: 276.3 MB (276269026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976806b6df1a298b4a0c164744aeaa61048792a8d32fa2b38a4d33d7ecfb8a63`  
		Last Modified: Wed, 29 Jun 2022 18:36:07 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad8f6d0b28e8d5d8c23b065fef5774c2dc75d1c9e13eb0f3ac9bc6ce82bb69e`  
		Last Modified: Wed, 29 Jun 2022 18:36:07 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f9d8e1293709eb6a2641c2bacdca0f01d2035c7aef236c49121479e19a1c91`  
		Last Modified: Wed, 29 Jun 2022 18:36:08 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e2e7433f86231e8fdea2b588803fd2fc68de734aa166fec758c5f2643e69cd`  
		Last Modified: Wed, 29 Jun 2022 18:36:07 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:fc3800cd42ed2df51fb054811d3f0c6bb9849bfa33b12df5d24d8aa67edf4598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:f0fefc7811bdcc887d091a5aac2123f9ddee1ba607dda9c7cd6adc8bc1477a0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.9 MB (555885464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3695662499df289da7ba7f8bbf1cf276b63b22ff457873742987c9a94ed1dbd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:42:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:42:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:43:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:43:30 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:43:32 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:43:32 GMT
ENV ODOO_VERSION=15.0
# Wed, 29 Jun 2022 18:24:44 GMT
ARG ODOO_RELEASE=20220629
# Wed, 29 Jun 2022 18:24:44 GMT
ARG ODOO_SHA=412a8b14730e958db607a5287c6f93112b8c4f50
# Wed, 29 Jun 2022 18:28:34 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=412a8b14730e958db607a5287c6f93112b8c4f50
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Jun 2022 18:28:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Jun 2022 18:28:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Jun 2022 18:28:39 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=412a8b14730e958db607a5287c6f93112b8c4f50
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Jun 2022 18:28:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Jun 2022 18:28:39 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Jun 2022 18:28:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Jun 2022 18:28:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Jun 2022 18:28:39 GMT
USER odoo
# Wed, 29 Jun 2022 18:28:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jun 2022 18:28:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985d8d4799be91199129b639a86c297d32603e21afe9cfc8841d93193da8a300`  
		Last Modified: Thu, 23 Jun 2022 04:51:09 GMT  
		Size: 220.3 MB (220309145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eb12b3f19b77eb7d077051fb56941bf1917065af5536fbbf03ed8d6892da38`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 2.5 MB (2513193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce450078d93ef4e1ee2bc96f4c29e6fc5b4776fa5ec4d69a370bddf5466f47d`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 485.4 KB (485399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e246646288cb7be5d96429badaeafe67321bdbe3d8f6aee6ee02307e48bdad`  
		Last Modified: Wed, 29 Jun 2022 18:35:54 GMT  
		Size: 301.2 MB (301195858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f10a362cc8dcf4070a6c11fa66b49f41cfb24fc659bdc3518e1db5b4cba5cc`  
		Last Modified: Wed, 29 Jun 2022 18:35:19 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87510bcf33716d5d8abd237679866b916560c0c164258940ac5584c2bea407b`  
		Last Modified: Wed, 29 Jun 2022 18:35:19 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650fcab76410b27e2355a211416beec018b1325430a6319f9bb1a35ccffffb4`  
		Last Modified: Wed, 29 Jun 2022 18:35:19 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0861404bcfe86a62894c86b964656feab81fcbc5dbe208cdb5341e06004f2745`  
		Last Modified: Wed, 29 Jun 2022 18:35:19 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:fc3800cd42ed2df51fb054811d3f0c6bb9849bfa33b12df5d24d8aa67edf4598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:f0fefc7811bdcc887d091a5aac2123f9ddee1ba607dda9c7cd6adc8bc1477a0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.9 MB (555885464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3695662499df289da7ba7f8bbf1cf276b63b22ff457873742987c9a94ed1dbd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:42:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:42:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:43:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:43:30 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:43:32 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:43:32 GMT
ENV ODOO_VERSION=15.0
# Wed, 29 Jun 2022 18:24:44 GMT
ARG ODOO_RELEASE=20220629
# Wed, 29 Jun 2022 18:24:44 GMT
ARG ODOO_SHA=412a8b14730e958db607a5287c6f93112b8c4f50
# Wed, 29 Jun 2022 18:28:34 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=412a8b14730e958db607a5287c6f93112b8c4f50
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Jun 2022 18:28:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Jun 2022 18:28:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Jun 2022 18:28:39 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=412a8b14730e958db607a5287c6f93112b8c4f50
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Jun 2022 18:28:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Jun 2022 18:28:39 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Jun 2022 18:28:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Jun 2022 18:28:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Jun 2022 18:28:39 GMT
USER odoo
# Wed, 29 Jun 2022 18:28:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jun 2022 18:28:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985d8d4799be91199129b639a86c297d32603e21afe9cfc8841d93193da8a300`  
		Last Modified: Thu, 23 Jun 2022 04:51:09 GMT  
		Size: 220.3 MB (220309145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eb12b3f19b77eb7d077051fb56941bf1917065af5536fbbf03ed8d6892da38`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 2.5 MB (2513193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce450078d93ef4e1ee2bc96f4c29e6fc5b4776fa5ec4d69a370bddf5466f47d`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 485.4 KB (485399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e246646288cb7be5d96429badaeafe67321bdbe3d8f6aee6ee02307e48bdad`  
		Last Modified: Wed, 29 Jun 2022 18:35:54 GMT  
		Size: 301.2 MB (301195858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f10a362cc8dcf4070a6c11fa66b49f41cfb24fc659bdc3518e1db5b4cba5cc`  
		Last Modified: Wed, 29 Jun 2022 18:35:19 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87510bcf33716d5d8abd237679866b916560c0c164258940ac5584c2bea407b`  
		Last Modified: Wed, 29 Jun 2022 18:35:19 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650fcab76410b27e2355a211416beec018b1325430a6319f9bb1a35ccffffb4`  
		Last Modified: Wed, 29 Jun 2022 18:35:19 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0861404bcfe86a62894c86b964656feab81fcbc5dbe208cdb5341e06004f2745`  
		Last Modified: Wed, 29 Jun 2022 18:35:19 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:fc3800cd42ed2df51fb054811d3f0c6bb9849bfa33b12df5d24d8aa67edf4598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:f0fefc7811bdcc887d091a5aac2123f9ddee1ba607dda9c7cd6adc8bc1477a0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.9 MB (555885464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3695662499df289da7ba7f8bbf1cf276b63b22ff457873742987c9a94ed1dbd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:42:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:42:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:43:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:43:30 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:43:32 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:43:32 GMT
ENV ODOO_VERSION=15.0
# Wed, 29 Jun 2022 18:24:44 GMT
ARG ODOO_RELEASE=20220629
# Wed, 29 Jun 2022 18:24:44 GMT
ARG ODOO_SHA=412a8b14730e958db607a5287c6f93112b8c4f50
# Wed, 29 Jun 2022 18:28:34 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=412a8b14730e958db607a5287c6f93112b8c4f50
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 29 Jun 2022 18:28:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 29 Jun 2022 18:28:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 29 Jun 2022 18:28:39 GMT
# ARGS: ODOO_RELEASE=20220629 ODOO_SHA=412a8b14730e958db607a5287c6f93112b8c4f50
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 29 Jun 2022 18:28:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 29 Jun 2022 18:28:39 GMT
EXPOSE 8069 8071 8072
# Wed, 29 Jun 2022 18:28:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 29 Jun 2022 18:28:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 29 Jun 2022 18:28:39 GMT
USER odoo
# Wed, 29 Jun 2022 18:28:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Jun 2022 18:28:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985d8d4799be91199129b639a86c297d32603e21afe9cfc8841d93193da8a300`  
		Last Modified: Thu, 23 Jun 2022 04:51:09 GMT  
		Size: 220.3 MB (220309145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eb12b3f19b77eb7d077051fb56941bf1917065af5536fbbf03ed8d6892da38`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 2.5 MB (2513193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce450078d93ef4e1ee2bc96f4c29e6fc5b4776fa5ec4d69a370bddf5466f47d`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 485.4 KB (485399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e246646288cb7be5d96429badaeafe67321bdbe3d8f6aee6ee02307e48bdad`  
		Last Modified: Wed, 29 Jun 2022 18:35:54 GMT  
		Size: 301.2 MB (301195858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f10a362cc8dcf4070a6c11fa66b49f41cfb24fc659bdc3518e1db5b4cba5cc`  
		Last Modified: Wed, 29 Jun 2022 18:35:19 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87510bcf33716d5d8abd237679866b916560c0c164258940ac5584c2bea407b`  
		Last Modified: Wed, 29 Jun 2022 18:35:19 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2650fcab76410b27e2355a211416beec018b1325430a6319f9bb1a35ccffffb4`  
		Last Modified: Wed, 29 Jun 2022 18:35:19 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0861404bcfe86a62894c86b964656feab81fcbc5dbe208cdb5341e06004f2745`  
		Last Modified: Wed, 29 Jun 2022 18:35:19 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
