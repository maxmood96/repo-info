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
$ docker pull odoo@sha256:9be5b55535cc92b43073fdc0a2b23b6cc41df30683a22a6645ee31501c05b41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:a683456e20183c69960de251aa3bbfb91f65c83246d96946ef88221ba228314a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.2 MB (540178729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671c20e62c7037e55133304eedad3a99eeac22ad797b3981fd912648500dcab8`
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
# Thu, 23 Jun 2022 04:48:58 GMT
ARG ODOO_RELEASE=20220620
# Thu, 23 Jun 2022 04:48:58 GMT
ARG ODOO_SHA=6bfc680c42e4fd310281712c3467902d8db8cb56
# Thu, 23 Jun 2022 04:50:08 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=6bfc680c42e4fd310281712c3467902d8db8cb56
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Jun 2022 04:50:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Jun 2022 04:50:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Jun 2022 04:50:12 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=6bfc680c42e4fd310281712c3467902d8db8cb56
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Jun 2022 04:50:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jun 2022 04:50:13 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Jun 2022 04:50:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jun 2022 04:50:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Jun 2022 04:50:13 GMT
USER odoo
# Thu, 23 Jun 2022 04:50:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 04:50:13 GMT
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
	-	`sha256:5af9de05ee2f4ba592b6669873903ab16c0e05088ff14d2a6f47c45050f835bf`  
		Last Modified: Thu, 23 Jun 2022 04:52:46 GMT  
		Size: 292.0 MB (291957569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538afc37b250144ada9c85d7fa428e4125c8feb2818945e10ee385f09be3b368`  
		Last Modified: Thu, 23 Jun 2022 04:52:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb27520e33808bae8ab50f1ee0290b5bbabde9dc5962ddc0baf0d44f043c0c0`  
		Last Modified: Thu, 23 Jun 2022 04:52:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3a916a79a48af1fa15377070d7ba310e7dfa742b110e1fb3ae75ba4fc02af`  
		Last Modified: Thu, 23 Jun 2022 04:52:13 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aea00603e8b772dc47ef74f99af47b9f67fdf14d3ec10b71039cb0a71382b7`  
		Last Modified: Thu, 23 Jun 2022 04:52:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:9be5b55535cc92b43073fdc0a2b23b6cc41df30683a22a6645ee31501c05b41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:a683456e20183c69960de251aa3bbfb91f65c83246d96946ef88221ba228314a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.2 MB (540178729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671c20e62c7037e55133304eedad3a99eeac22ad797b3981fd912648500dcab8`
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
# Thu, 23 Jun 2022 04:48:58 GMT
ARG ODOO_RELEASE=20220620
# Thu, 23 Jun 2022 04:48:58 GMT
ARG ODOO_SHA=6bfc680c42e4fd310281712c3467902d8db8cb56
# Thu, 23 Jun 2022 04:50:08 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=6bfc680c42e4fd310281712c3467902d8db8cb56
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Jun 2022 04:50:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Jun 2022 04:50:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Jun 2022 04:50:12 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=6bfc680c42e4fd310281712c3467902d8db8cb56
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Jun 2022 04:50:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jun 2022 04:50:13 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Jun 2022 04:50:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jun 2022 04:50:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Jun 2022 04:50:13 GMT
USER odoo
# Thu, 23 Jun 2022 04:50:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 04:50:13 GMT
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
	-	`sha256:5af9de05ee2f4ba592b6669873903ab16c0e05088ff14d2a6f47c45050f835bf`  
		Last Modified: Thu, 23 Jun 2022 04:52:46 GMT  
		Size: 292.0 MB (291957569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538afc37b250144ada9c85d7fa428e4125c8feb2818945e10ee385f09be3b368`  
		Last Modified: Thu, 23 Jun 2022 04:52:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb27520e33808bae8ab50f1ee0290b5bbabde9dc5962ddc0baf0d44f043c0c0`  
		Last Modified: Thu, 23 Jun 2022 04:52:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d3a916a79a48af1fa15377070d7ba310e7dfa742b110e1fb3ae75ba4fc02af`  
		Last Modified: Thu, 23 Jun 2022 04:52:13 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aea00603e8b772dc47ef74f99af47b9f67fdf14d3ec10b71039cb0a71382b7`  
		Last Modified: Thu, 23 Jun 2022 04:52:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:e36f476ef09666b8e42ce9cfb7c65978d9e1f63ae04e92ff66aef7b371cbb3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:834556f95e738e30874e66514d138bdb1ac195217935215d9529d7fa9e5b0487
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.5 MB (530475297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93805de691874a310f2bb4766a7ed6a430398f8d223ed26a8340954199dbf54`
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
# Thu, 23 Jun 2022 04:46:20 GMT
ARG ODOO_RELEASE=20220620
# Thu, 23 Jun 2022 04:46:20 GMT
ARG ODOO_SHA=dc5475c3c9f9affc2f795be7922efc887d4a5d29
# Thu, 23 Jun 2022 04:47:29 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=dc5475c3c9f9affc2f795be7922efc887d4a5d29
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Jun 2022 04:47:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Jun 2022 04:47:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Jun 2022 04:47:34 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=dc5475c3c9f9affc2f795be7922efc887d4a5d29
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Jun 2022 04:47:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jun 2022 04:47:34 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Jun 2022 04:47:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jun 2022 04:47:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Jun 2022 04:47:34 GMT
USER odoo
# Thu, 23 Jun 2022 04:47:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 04:47:34 GMT
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
	-	`sha256:217a61bcbb86aa0de0301204a4d2349bba370537d659121f8c4c64f862d44c83`  
		Last Modified: Thu, 23 Jun 2022 04:52:04 GMT  
		Size: 276.2 MB (276213511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f241c240e9a6b990fb7528ec9b5fc7523e21d23159aff0325002b8ae233e462`  
		Last Modified: Thu, 23 Jun 2022 04:51:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbe6a4efcc1c24320a3dc197b6a1e218a6075f62c661e7cad2e05c6f51eb8f0`  
		Last Modified: Thu, 23 Jun 2022 04:51:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12e5fa4e1e5f8af507d7340c3864739f51f7859c597ca76f773f223727cacee`  
		Last Modified: Thu, 23 Jun 2022 04:51:30 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5456b374c95c0e500613007ed156708f5a64cbb99ad9bb74e0dfe6e02955b431`  
		Last Modified: Thu, 23 Jun 2022 04:51:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:e36f476ef09666b8e42ce9cfb7c65978d9e1f63ae04e92ff66aef7b371cbb3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:834556f95e738e30874e66514d138bdb1ac195217935215d9529d7fa9e5b0487
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.5 MB (530475297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93805de691874a310f2bb4766a7ed6a430398f8d223ed26a8340954199dbf54`
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
# Thu, 23 Jun 2022 04:46:20 GMT
ARG ODOO_RELEASE=20220620
# Thu, 23 Jun 2022 04:46:20 GMT
ARG ODOO_SHA=dc5475c3c9f9affc2f795be7922efc887d4a5d29
# Thu, 23 Jun 2022 04:47:29 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=dc5475c3c9f9affc2f795be7922efc887d4a5d29
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Jun 2022 04:47:33 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Jun 2022 04:47:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Jun 2022 04:47:34 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=dc5475c3c9f9affc2f795be7922efc887d4a5d29
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Jun 2022 04:47:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jun 2022 04:47:34 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Jun 2022 04:47:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jun 2022 04:47:34 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Jun 2022 04:47:34 GMT
USER odoo
# Thu, 23 Jun 2022 04:47:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 04:47:34 GMT
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
	-	`sha256:217a61bcbb86aa0de0301204a4d2349bba370537d659121f8c4c64f862d44c83`  
		Last Modified: Thu, 23 Jun 2022 04:52:04 GMT  
		Size: 276.2 MB (276213511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f241c240e9a6b990fb7528ec9b5fc7523e21d23159aff0325002b8ae233e462`  
		Last Modified: Thu, 23 Jun 2022 04:51:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbe6a4efcc1c24320a3dc197b6a1e218a6075f62c661e7cad2e05c6f51eb8f0`  
		Last Modified: Thu, 23 Jun 2022 04:51:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12e5fa4e1e5f8af507d7340c3864739f51f7859c597ca76f773f223727cacee`  
		Last Modified: Thu, 23 Jun 2022 04:51:30 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5456b374c95c0e500613007ed156708f5a64cbb99ad9bb74e0dfe6e02955b431`  
		Last Modified: Thu, 23 Jun 2022 04:51:30 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:6d5fe376aaffe10fc4767c7ae0314c1fe12a1a0a1d1eaf7332368a7d096639c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:40b49d7cad11ff5b765352db6572d62120ea2d007e76cb76ad9b12966f0f198e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.8 MB (555791450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade1ded6b4c8f7117a4fc1cec18cb328abfda21beb03cc4f6f10a4d3c9793d13`
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
# Thu, 23 Jun 2022 04:43:32 GMT
ARG ODOO_RELEASE=20220620
# Thu, 23 Jun 2022 04:43:32 GMT
ARG ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
# Thu, 23 Jun 2022 04:44:46 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Jun 2022 04:44:51 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Jun 2022 04:44:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Jun 2022 04:44:51 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Jun 2022 04:44:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jun 2022 04:44:51 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Jun 2022 04:44:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jun 2022 04:44:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Jun 2022 04:44:52 GMT
USER odoo
# Thu, 23 Jun 2022 04:44:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 04:44:52 GMT
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
	-	`sha256:751baecbcf48c20db8558f7861a0920b4a76d59a79c9a66ae4e22b772c2d9a4b`  
		Last Modified: Thu, 23 Jun 2022 04:51:16 GMT  
		Size: 301.1 MB (301101840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4193436c4f6f715e9d0bd7bd428433798f26a83acf905fda09ce53423beebb4c`  
		Last Modified: Thu, 23 Jun 2022 04:50:40 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613109f2283a870bb4af76357dcd67c53da01bdf775c613493f96dab1ad97c0b`  
		Last Modified: Thu, 23 Jun 2022 04:50:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9de5f7dc0a0c3b24e5bb91dcd8b8c6974e3587ba6b6cb610283e4ab4a0e4c3`  
		Last Modified: Thu, 23 Jun 2022 04:50:40 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507f47748c5de9b82a1e43a7ec6c016724a5c0bb7fe7522a42f3520e731fcbd7`  
		Last Modified: Thu, 23 Jun 2022 04:50:40 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:6d5fe376aaffe10fc4767c7ae0314c1fe12a1a0a1d1eaf7332368a7d096639c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:40b49d7cad11ff5b765352db6572d62120ea2d007e76cb76ad9b12966f0f198e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.8 MB (555791450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade1ded6b4c8f7117a4fc1cec18cb328abfda21beb03cc4f6f10a4d3c9793d13`
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
# Thu, 23 Jun 2022 04:43:32 GMT
ARG ODOO_RELEASE=20220620
# Thu, 23 Jun 2022 04:43:32 GMT
ARG ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
# Thu, 23 Jun 2022 04:44:46 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Jun 2022 04:44:51 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Jun 2022 04:44:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Jun 2022 04:44:51 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Jun 2022 04:44:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jun 2022 04:44:51 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Jun 2022 04:44:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jun 2022 04:44:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Jun 2022 04:44:52 GMT
USER odoo
# Thu, 23 Jun 2022 04:44:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 04:44:52 GMT
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
	-	`sha256:751baecbcf48c20db8558f7861a0920b4a76d59a79c9a66ae4e22b772c2d9a4b`  
		Last Modified: Thu, 23 Jun 2022 04:51:16 GMT  
		Size: 301.1 MB (301101840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4193436c4f6f715e9d0bd7bd428433798f26a83acf905fda09ce53423beebb4c`  
		Last Modified: Thu, 23 Jun 2022 04:50:40 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613109f2283a870bb4af76357dcd67c53da01bdf775c613493f96dab1ad97c0b`  
		Last Modified: Thu, 23 Jun 2022 04:50:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9de5f7dc0a0c3b24e5bb91dcd8b8c6974e3587ba6b6cb610283e4ab4a0e4c3`  
		Last Modified: Thu, 23 Jun 2022 04:50:40 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507f47748c5de9b82a1e43a7ec6c016724a5c0bb7fe7522a42f3520e731fcbd7`  
		Last Modified: Thu, 23 Jun 2022 04:50:40 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:6d5fe376aaffe10fc4767c7ae0314c1fe12a1a0a1d1eaf7332368a7d096639c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:40b49d7cad11ff5b765352db6572d62120ea2d007e76cb76ad9b12966f0f198e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.8 MB (555791450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade1ded6b4c8f7117a4fc1cec18cb328abfda21beb03cc4f6f10a4d3c9793d13`
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
# Thu, 23 Jun 2022 04:43:32 GMT
ARG ODOO_RELEASE=20220620
# Thu, 23 Jun 2022 04:43:32 GMT
ARG ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
# Thu, 23 Jun 2022 04:44:46 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Jun 2022 04:44:51 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Jun 2022 04:44:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Jun 2022 04:44:51 GMT
# ARGS: ODOO_RELEASE=20220620 ODOO_SHA=38e219e59c019757bc0662e90e2f2586faf93f5e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Jun 2022 04:44:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Jun 2022 04:44:51 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Jun 2022 04:44:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Jun 2022 04:44:52 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Jun 2022 04:44:52 GMT
USER odoo
# Thu, 23 Jun 2022 04:44:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jun 2022 04:44:52 GMT
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
	-	`sha256:751baecbcf48c20db8558f7861a0920b4a76d59a79c9a66ae4e22b772c2d9a4b`  
		Last Modified: Thu, 23 Jun 2022 04:51:16 GMT  
		Size: 301.1 MB (301101840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4193436c4f6f715e9d0bd7bd428433798f26a83acf905fda09ce53423beebb4c`  
		Last Modified: Thu, 23 Jun 2022 04:50:40 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613109f2283a870bb4af76357dcd67c53da01bdf775c613493f96dab1ad97c0b`  
		Last Modified: Thu, 23 Jun 2022 04:50:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9de5f7dc0a0c3b24e5bb91dcd8b8c6974e3587ba6b6cb610283e4ab4a0e4c3`  
		Last Modified: Thu, 23 Jun 2022 04:50:40 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507f47748c5de9b82a1e43a7ec6c016724a5c0bb7fe7522a42f3520e731fcbd7`  
		Last Modified: Thu, 23 Jun 2022 04:50:40 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
