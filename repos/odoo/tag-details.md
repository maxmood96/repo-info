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
$ docker pull odoo@sha256:ea7a1bfeb448ea7d3a2a9724b2153bb409bfa5b0085bf18531d5e928eac8efd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:88bf9ecf4a1c879a80065f5f150c69e980e21b56f65780a415cc7f67e04cf6e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.7 MB (539683550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b88800dfd775fefe7371936f5aec61b31420e908674ba397fa08e2ff32b705`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:02:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Mar 2022 19:02:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Mar 2022 19:02:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 19:06:03 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 29 Mar 2022 19:06:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:06:15 GMT
RUN npm install -g rtlcss
# Tue, 29 Mar 2022 19:06:15 GMT
ENV ODOO_VERSION=13.0
# Fri, 01 Apr 2022 19:05:30 GMT
ARG ODOO_RELEASE=20220401
# Fri, 01 Apr 2022 19:05:30 GMT
ARG ODOO_SHA=2af3333f6048663e921ea49d7dc836d4dcf31cb4
# Fri, 01 Apr 2022 19:06:51 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=2af3333f6048663e921ea49d7dc836d4dcf31cb4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 01 Apr 2022 19:06:55 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 01 Apr 2022 19:06:55 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 01 Apr 2022 19:06:56 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=2af3333f6048663e921ea49d7dc836d4dcf31cb4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 01 Apr 2022 19:06:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 01 Apr 2022 19:06:56 GMT
EXPOSE 8069 8071 8072
# Fri, 01 Apr 2022 19:06:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 01 Apr 2022 19:06:56 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 01 Apr 2022 19:06:56 GMT
USER odoo
# Fri, 01 Apr 2022 19:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Apr 2022 19:06:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a511858723517facee7b2235b79b364ee6ebcf20153dc49f3c226d6d4e39e363`  
		Last Modified: Tue, 29 Mar 2022 19:10:01 GMT  
		Size: 207.1 MB (207143257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fead8ec7541d6642b89ca7e91985366ae38f95e593cea160b9edb52516a5598`  
		Last Modified: Tue, 29 Mar 2022 19:09:38 GMT  
		Size: 13.4 MB (13438585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396d3da3445e859d637b818783f718c773ee45472a72a96f4a29bc61e2726e4e`  
		Last Modified: Tue, 29 Mar 2022 19:09:35 GMT  
		Size: 457.2 KB (457185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561ae9fb2d668586275c5aa765be3ac906e4dec8a465d6d1aa9fff2a64877a6f`  
		Last Modified: Fri, 01 Apr 2022 19:09:21 GMT  
		Size: 291.5 MB (291490091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a65540165f59f2f7bcffcb5bb84b62d1b9105fd9db47aab2dfbc41767c9abe`  
		Last Modified: Fri, 01 Apr 2022 19:08:51 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1266daadce2c573ef52af29917c63bb6a6e203f698953d64fc1f90297526692f`  
		Last Modified: Fri, 01 Apr 2022 19:08:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180dcb7c8fe0d9e4ef0aebd2d2d69859460e722483a098b6a2d081947d89eadd`  
		Last Modified: Fri, 01 Apr 2022 19:08:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1093cedb6058cdf95ae83d802cad883af7f51a70e3a5d62df6410daacf2433`  
		Last Modified: Fri, 01 Apr 2022 19:08:51 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:ea7a1bfeb448ea7d3a2a9724b2153bb409bfa5b0085bf18531d5e928eac8efd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:88bf9ecf4a1c879a80065f5f150c69e980e21b56f65780a415cc7f67e04cf6e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.7 MB (539683550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b88800dfd775fefe7371936f5aec61b31420e908674ba397fa08e2ff32b705`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:02:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Mar 2022 19:02:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Mar 2022 19:02:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 19:06:03 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 29 Mar 2022 19:06:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:06:15 GMT
RUN npm install -g rtlcss
# Tue, 29 Mar 2022 19:06:15 GMT
ENV ODOO_VERSION=13.0
# Fri, 01 Apr 2022 19:05:30 GMT
ARG ODOO_RELEASE=20220401
# Fri, 01 Apr 2022 19:05:30 GMT
ARG ODOO_SHA=2af3333f6048663e921ea49d7dc836d4dcf31cb4
# Fri, 01 Apr 2022 19:06:51 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=2af3333f6048663e921ea49d7dc836d4dcf31cb4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 01 Apr 2022 19:06:55 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 01 Apr 2022 19:06:55 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 01 Apr 2022 19:06:56 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=2af3333f6048663e921ea49d7dc836d4dcf31cb4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 01 Apr 2022 19:06:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 01 Apr 2022 19:06:56 GMT
EXPOSE 8069 8071 8072
# Fri, 01 Apr 2022 19:06:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 01 Apr 2022 19:06:56 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 01 Apr 2022 19:06:56 GMT
USER odoo
# Fri, 01 Apr 2022 19:06:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Apr 2022 19:06:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a511858723517facee7b2235b79b364ee6ebcf20153dc49f3c226d6d4e39e363`  
		Last Modified: Tue, 29 Mar 2022 19:10:01 GMT  
		Size: 207.1 MB (207143257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fead8ec7541d6642b89ca7e91985366ae38f95e593cea160b9edb52516a5598`  
		Last Modified: Tue, 29 Mar 2022 19:09:38 GMT  
		Size: 13.4 MB (13438585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396d3da3445e859d637b818783f718c773ee45472a72a96f4a29bc61e2726e4e`  
		Last Modified: Tue, 29 Mar 2022 19:09:35 GMT  
		Size: 457.2 KB (457185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561ae9fb2d668586275c5aa765be3ac906e4dec8a465d6d1aa9fff2a64877a6f`  
		Last Modified: Fri, 01 Apr 2022 19:09:21 GMT  
		Size: 291.5 MB (291490091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a65540165f59f2f7bcffcb5bb84b62d1b9105fd9db47aab2dfbc41767c9abe`  
		Last Modified: Fri, 01 Apr 2022 19:08:51 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1266daadce2c573ef52af29917c63bb6a6e203f698953d64fc1f90297526692f`  
		Last Modified: Fri, 01 Apr 2022 19:08:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180dcb7c8fe0d9e4ef0aebd2d2d69859460e722483a098b6a2d081947d89eadd`  
		Last Modified: Fri, 01 Apr 2022 19:08:51 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1093cedb6058cdf95ae83d802cad883af7f51a70e3a5d62df6410daacf2433`  
		Last Modified: Fri, 01 Apr 2022 19:08:51 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:1c1d283a54b02de19111499c66454377d6e6653c53e9a0f576ba848adc000060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:2d00ef7811e4b9dc0910e25f0d84c502bd936eb807b27a4d3d5289d85917cb05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.6 MB (529593492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e471ef753894912c634bd62bb23327bf31ae2d9c99564260a9dc97ed1073c6d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:02:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Mar 2022 19:02:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Mar 2022 19:02:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 19:03:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 29 Mar 2022 19:03:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:03:47 GMT
RUN npm install -g rtlcss
# Tue, 29 Mar 2022 19:03:47 GMT
ENV ODOO_VERSION=14.0
# Fri, 01 Apr 2022 19:04:08 GMT
ARG ODOO_RELEASE=20220401
# Fri, 01 Apr 2022 19:04:08 GMT
ARG ODOO_SHA=43eabf4f6f55cd2887dc123d955bfaf9c7f27a32
# Fri, 01 Apr 2022 19:05:19 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=43eabf4f6f55cd2887dc123d955bfaf9c7f27a32
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 01 Apr 2022 19:05:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 01 Apr 2022 19:05:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 01 Apr 2022 19:05:23 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=43eabf4f6f55cd2887dc123d955bfaf9c7f27a32
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 01 Apr 2022 19:05:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 01 Apr 2022 19:05:24 GMT
EXPOSE 8069 8071 8072
# Fri, 01 Apr 2022 19:05:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 01 Apr 2022 19:05:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 01 Apr 2022 19:05:24 GMT
USER odoo
# Fri, 01 Apr 2022 19:05:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Apr 2022 19:05:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d71810975b7f42c776c1f507c47736d2bd6904ab77b06df0c936554750b0dc`  
		Last Modified: Tue, 29 Mar 2022 19:09:15 GMT  
		Size: 213.2 MB (213182657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e598731bdf8c71ef7ba2ee42f6fc6b4a739285b74bf7d60a63db66774b1d65`  
		Last Modified: Tue, 29 Mar 2022 19:08:51 GMT  
		Size: 13.4 MB (13440807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843965b80de19e5d7d522b083ee79b394c9969e157265dfbc5fb3718943f877d`  
		Last Modified: Tue, 29 Mar 2022 19:08:48 GMT  
		Size: 457.2 KB (457156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174bf7d68abecddfd975e45ddb4d2ed6d6db3fcb1f3b60d3bc2a2e19d3ab17ef`  
		Last Modified: Fri, 01 Apr 2022 19:08:40 GMT  
		Size: 275.4 MB (275358438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28b8636141eb4c7464522ecd259267f78b4aa34642968197e0859f42330afde`  
		Last Modified: Fri, 01 Apr 2022 19:08:09 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b0e65bc32923c8901606f2df62ad266158c593b39f221b51768373ac2126a`  
		Last Modified: Fri, 01 Apr 2022 19:08:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab77d5f257d645d3f505c39f595d2a2e0fc813cb40f2409d9845ad0660f0615`  
		Last Modified: Fri, 01 Apr 2022 19:08:09 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c71f0b3a0e839c169e1864744c52ed89a2bc169e7595d976f5e66a54177eaa`  
		Last Modified: Fri, 01 Apr 2022 19:08:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:1c1d283a54b02de19111499c66454377d6e6653c53e9a0f576ba848adc000060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:2d00ef7811e4b9dc0910e25f0d84c502bd936eb807b27a4d3d5289d85917cb05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.6 MB (529593492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e471ef753894912c634bd62bb23327bf31ae2d9c99564260a9dc97ed1073c6d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 19:02:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Mar 2022 19:02:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Mar 2022 19:02:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 19:03:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 29 Mar 2022 19:03:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:03:47 GMT
RUN npm install -g rtlcss
# Tue, 29 Mar 2022 19:03:47 GMT
ENV ODOO_VERSION=14.0
# Fri, 01 Apr 2022 19:04:08 GMT
ARG ODOO_RELEASE=20220401
# Fri, 01 Apr 2022 19:04:08 GMT
ARG ODOO_SHA=43eabf4f6f55cd2887dc123d955bfaf9c7f27a32
# Fri, 01 Apr 2022 19:05:19 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=43eabf4f6f55cd2887dc123d955bfaf9c7f27a32
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 01 Apr 2022 19:05:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 01 Apr 2022 19:05:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 01 Apr 2022 19:05:23 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=43eabf4f6f55cd2887dc123d955bfaf9c7f27a32
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 01 Apr 2022 19:05:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 01 Apr 2022 19:05:24 GMT
EXPOSE 8069 8071 8072
# Fri, 01 Apr 2022 19:05:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 01 Apr 2022 19:05:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 01 Apr 2022 19:05:24 GMT
USER odoo
# Fri, 01 Apr 2022 19:05:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Apr 2022 19:05:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d71810975b7f42c776c1f507c47736d2bd6904ab77b06df0c936554750b0dc`  
		Last Modified: Tue, 29 Mar 2022 19:09:15 GMT  
		Size: 213.2 MB (213182657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e598731bdf8c71ef7ba2ee42f6fc6b4a739285b74bf7d60a63db66774b1d65`  
		Last Modified: Tue, 29 Mar 2022 19:08:51 GMT  
		Size: 13.4 MB (13440807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843965b80de19e5d7d522b083ee79b394c9969e157265dfbc5fb3718943f877d`  
		Last Modified: Tue, 29 Mar 2022 19:08:48 GMT  
		Size: 457.2 KB (457156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174bf7d68abecddfd975e45ddb4d2ed6d6db3fcb1f3b60d3bc2a2e19d3ab17ef`  
		Last Modified: Fri, 01 Apr 2022 19:08:40 GMT  
		Size: 275.4 MB (275358438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28b8636141eb4c7464522ecd259267f78b4aa34642968197e0859f42330afde`  
		Last Modified: Fri, 01 Apr 2022 19:08:09 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2b0e65bc32923c8901606f2df62ad266158c593b39f221b51768373ac2126a`  
		Last Modified: Fri, 01 Apr 2022 19:08:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab77d5f257d645d3f505c39f595d2a2e0fc813cb40f2409d9845ad0660f0615`  
		Last Modified: Fri, 01 Apr 2022 19:08:09 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c71f0b3a0e839c169e1864744c52ed89a2bc169e7595d976f5e66a54177eaa`  
		Last Modified: Fri, 01 Apr 2022 19:08:09 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:f5e0d85a89e369726c606072379e7a49e2d4cf665b1aa36e2cdfc249cfaaa99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:26958007f204a5e5123945bdf2cca8b2032ccd21658f33736d6e1a301f786c7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.7 MB (551707230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f13e89de7a15fed657718fa4cbc6b8267e054da8aeecf283fd09aeba756d05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 18:59:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Mar 2022 18:59:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Mar 2022 18:59:21 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 19:00:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 29 Mar 2022 19:00:31 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:00:32 GMT
RUN npm install -g rtlcss
# Tue, 29 Mar 2022 19:00:32 GMT
ENV ODOO_VERSION=15.0
# Fri, 01 Apr 2022 19:02:45 GMT
ARG ODOO_RELEASE=20220401
# Fri, 01 Apr 2022 19:02:45 GMT
ARG ODOO_SHA=47f9d71dcfd0c0884969b361bc1bbe5f45fb3ac5
# Fri, 01 Apr 2022 19:03:58 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=47f9d71dcfd0c0884969b361bc1bbe5f45fb3ac5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 01 Apr 2022 19:04:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 01 Apr 2022 19:04:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 01 Apr 2022 19:04:03 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=47f9d71dcfd0c0884969b361bc1bbe5f45fb3ac5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 01 Apr 2022 19:04:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 01 Apr 2022 19:04:04 GMT
EXPOSE 8069 8071 8072
# Fri, 01 Apr 2022 19:04:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 01 Apr 2022 19:04:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 01 Apr 2022 19:04:04 GMT
USER odoo
# Fri, 01 Apr 2022 19:04:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Apr 2022 19:04:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c747a1fa386d9308d1e2f9baef9efced0ce497e52e37fa9688ddc2a83779205`  
		Last Modified: Tue, 29 Mar 2022 19:08:26 GMT  
		Size: 220.3 MB (220306192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26df123c00088a4376eaafc17e8c006c7c47cc1dfa794ff5663dd160dba57157`  
		Last Modified: Tue, 29 Mar 2022 19:07:59 GMT  
		Size: 2.5 MB (2510070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff3bdf6129a4fe206bdf15ab252ebd5569b0f3efff6f8c7e2be9a0e0479b1cc`  
		Last Modified: Tue, 29 Mar 2022 19:07:58 GMT  
		Size: 450.8 KB (450767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfe5fa7a0a182726edcd58bf1f5e82ab4f19c2048f583fe90cd5bd85a57be3c`  
		Last Modified: Fri, 01 Apr 2022 19:07:56 GMT  
		Size: 297.1 MB (297059284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643079364272f6553f410593bb25c3dc731f0da56a457b6704c45d982b34afc7`  
		Last Modified: Fri, 01 Apr 2022 19:07:19 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67fe820125c705abc7cca9643a570cd7753d03d4e28fd6ee52e2f338ceae516`  
		Last Modified: Fri, 01 Apr 2022 19:07:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84abbc7e1a8cf4af164506ec614b9ac6240b7f3f4007c626667998bfe10886fe`  
		Last Modified: Fri, 01 Apr 2022 19:07:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ded43a677cb29f3eadab6d908dfd2b37de0a011534359b96ebf541c89e223a1`  
		Last Modified: Fri, 01 Apr 2022 19:07:20 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:f5e0d85a89e369726c606072379e7a49e2d4cf665b1aa36e2cdfc249cfaaa99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:26958007f204a5e5123945bdf2cca8b2032ccd21658f33736d6e1a301f786c7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.7 MB (551707230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f13e89de7a15fed657718fa4cbc6b8267e054da8aeecf283fd09aeba756d05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 18:59:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Mar 2022 18:59:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Mar 2022 18:59:21 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 19:00:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 29 Mar 2022 19:00:31 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:00:32 GMT
RUN npm install -g rtlcss
# Tue, 29 Mar 2022 19:00:32 GMT
ENV ODOO_VERSION=15.0
# Fri, 01 Apr 2022 19:02:45 GMT
ARG ODOO_RELEASE=20220401
# Fri, 01 Apr 2022 19:02:45 GMT
ARG ODOO_SHA=47f9d71dcfd0c0884969b361bc1bbe5f45fb3ac5
# Fri, 01 Apr 2022 19:03:58 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=47f9d71dcfd0c0884969b361bc1bbe5f45fb3ac5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 01 Apr 2022 19:04:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 01 Apr 2022 19:04:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 01 Apr 2022 19:04:03 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=47f9d71dcfd0c0884969b361bc1bbe5f45fb3ac5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 01 Apr 2022 19:04:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 01 Apr 2022 19:04:04 GMT
EXPOSE 8069 8071 8072
# Fri, 01 Apr 2022 19:04:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 01 Apr 2022 19:04:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 01 Apr 2022 19:04:04 GMT
USER odoo
# Fri, 01 Apr 2022 19:04:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Apr 2022 19:04:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c747a1fa386d9308d1e2f9baef9efced0ce497e52e37fa9688ddc2a83779205`  
		Last Modified: Tue, 29 Mar 2022 19:08:26 GMT  
		Size: 220.3 MB (220306192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26df123c00088a4376eaafc17e8c006c7c47cc1dfa794ff5663dd160dba57157`  
		Last Modified: Tue, 29 Mar 2022 19:07:59 GMT  
		Size: 2.5 MB (2510070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff3bdf6129a4fe206bdf15ab252ebd5569b0f3efff6f8c7e2be9a0e0479b1cc`  
		Last Modified: Tue, 29 Mar 2022 19:07:58 GMT  
		Size: 450.8 KB (450767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfe5fa7a0a182726edcd58bf1f5e82ab4f19c2048f583fe90cd5bd85a57be3c`  
		Last Modified: Fri, 01 Apr 2022 19:07:56 GMT  
		Size: 297.1 MB (297059284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643079364272f6553f410593bb25c3dc731f0da56a457b6704c45d982b34afc7`  
		Last Modified: Fri, 01 Apr 2022 19:07:19 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67fe820125c705abc7cca9643a570cd7753d03d4e28fd6ee52e2f338ceae516`  
		Last Modified: Fri, 01 Apr 2022 19:07:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84abbc7e1a8cf4af164506ec614b9ac6240b7f3f4007c626667998bfe10886fe`  
		Last Modified: Fri, 01 Apr 2022 19:07:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ded43a677cb29f3eadab6d908dfd2b37de0a011534359b96ebf541c89e223a1`  
		Last Modified: Fri, 01 Apr 2022 19:07:20 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:f5e0d85a89e369726c606072379e7a49e2d4cf665b1aa36e2cdfc249cfaaa99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:26958007f204a5e5123945bdf2cca8b2032ccd21658f33736d6e1a301f786c7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.7 MB (551707230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f13e89de7a15fed657718fa4cbc6b8267e054da8aeecf283fd09aeba756d05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 18:59:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 29 Mar 2022 18:59:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 29 Mar 2022 18:59:21 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 19:00:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 29 Mar 2022 19:00:31 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 19:00:32 GMT
RUN npm install -g rtlcss
# Tue, 29 Mar 2022 19:00:32 GMT
ENV ODOO_VERSION=15.0
# Fri, 01 Apr 2022 19:02:45 GMT
ARG ODOO_RELEASE=20220401
# Fri, 01 Apr 2022 19:02:45 GMT
ARG ODOO_SHA=47f9d71dcfd0c0884969b361bc1bbe5f45fb3ac5
# Fri, 01 Apr 2022 19:03:58 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=47f9d71dcfd0c0884969b361bc1bbe5f45fb3ac5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 01 Apr 2022 19:04:03 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 01 Apr 2022 19:04:03 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 01 Apr 2022 19:04:03 GMT
# ARGS: ODOO_RELEASE=20220401 ODOO_SHA=47f9d71dcfd0c0884969b361bc1bbe5f45fb3ac5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 01 Apr 2022 19:04:04 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 01 Apr 2022 19:04:04 GMT
EXPOSE 8069 8071 8072
# Fri, 01 Apr 2022 19:04:04 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 01 Apr 2022 19:04:04 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 01 Apr 2022 19:04:04 GMT
USER odoo
# Fri, 01 Apr 2022 19:04:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Apr 2022 19:04:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c747a1fa386d9308d1e2f9baef9efced0ce497e52e37fa9688ddc2a83779205`  
		Last Modified: Tue, 29 Mar 2022 19:08:26 GMT  
		Size: 220.3 MB (220306192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26df123c00088a4376eaafc17e8c006c7c47cc1dfa794ff5663dd160dba57157`  
		Last Modified: Tue, 29 Mar 2022 19:07:59 GMT  
		Size: 2.5 MB (2510070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff3bdf6129a4fe206bdf15ab252ebd5569b0f3efff6f8c7e2be9a0e0479b1cc`  
		Last Modified: Tue, 29 Mar 2022 19:07:58 GMT  
		Size: 450.8 KB (450767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfe5fa7a0a182726edcd58bf1f5e82ab4f19c2048f583fe90cd5bd85a57be3c`  
		Last Modified: Fri, 01 Apr 2022 19:07:56 GMT  
		Size: 297.1 MB (297059284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643079364272f6553f410593bb25c3dc731f0da56a457b6704c45d982b34afc7`  
		Last Modified: Fri, 01 Apr 2022 19:07:19 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67fe820125c705abc7cca9643a570cd7753d03d4e28fd6ee52e2f338ceae516`  
		Last Modified: Fri, 01 Apr 2022 19:07:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84abbc7e1a8cf4af164506ec614b9ac6240b7f3f4007c626667998bfe10886fe`  
		Last Modified: Fri, 01 Apr 2022 19:07:19 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ded43a677cb29f3eadab6d908dfd2b37de0a011534359b96ebf541c89e223a1`  
		Last Modified: Fri, 01 Apr 2022 19:07:20 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
