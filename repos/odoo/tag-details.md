<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:12`](#odoo12)
-	[`odoo:12.0`](#odoo120)
-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:latest`](#odoolatest)

## `odoo:12`

```console
$ docker pull odoo@sha256:1f8faed69738382fefa1362211201feffa92146f816e8f6f982234b2558ce41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:8b8adb30c2a08f1715a1558d308c1a0d08e54b4390625fa790ee1beb1bd65de8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542585631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5602746f8c5ff4d662c6d8bf2d7c2b4af9b7af24564502b6e3522c00fb78b92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:15:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:15:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:15:29 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:15:30 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 27 Mar 2021 06:17:31 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:17:45 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:17:58 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:17:58 GMT
ENV ODOO_VERSION=12.0
# Tue, 30 Mar 2021 20:34:01 GMT
ARG ODOO_RELEASE=20210329
# Tue, 30 Mar 2021 20:34:01 GMT
ARG ODOO_SHA=cd334511a519ec8b8fd3f4555171d17f94107b77
# Tue, 30 Mar 2021 20:35:09 GMT
# ARGS: ODOO_RELEASE=20210329 ODOO_SHA=cd334511a519ec8b8fd3f4555171d17f94107b77
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 Mar 2021 20:35:11 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 30 Mar 2021 20:35:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 Mar 2021 20:35:13 GMT
# ARGS: ODOO_RELEASE=20210329 ODOO_SHA=cd334511a519ec8b8fd3f4555171d17f94107b77
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 Mar 2021 20:35:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Mar 2021 20:35:13 GMT
EXPOSE 8069 8071 8072
# Tue, 30 Mar 2021 20:35:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Mar 2021 20:35:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 Mar 2021 20:35:14 GMT
USER odoo
# Tue, 30 Mar 2021 20:35:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Mar 2021 20:35:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d85905ea21b22f3cf49d1544d54fa33de25fbd3fb032724098214829848cb7e`  
		Last Modified: Sat, 27 Mar 2021 06:22:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997e5ef07b089b7d6a8a1ab2cc7851f20c4bd8eab43877b4e69f39d90aa2dacd`  
		Last Modified: Sat, 27 Mar 2021 06:22:45 GMT  
		Size: 219.7 MB (219658920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03046533a143ccada4bcf38fe3cf27238bf9807d1705bd7f63fbb7c99d17accc`  
		Last Modified: Sat, 27 Mar 2021 06:22:02 GMT  
		Size: 2.2 MB (2224133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555b0321ec586fdb7780ba6462caba21fe7328c3b6971007ffb99e4c1d83212e`  
		Last Modified: Sat, 27 Mar 2021 06:22:11 GMT  
		Size: 22.1 MB (22053347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8726deeabbc7d4caeec0124482d31ed9aead04000972f546b3ba2a2ed0d98141`  
		Last Modified: Tue, 30 Mar 2021 20:37:49 GMT  
		Size: 276.1 MB (276118163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82df7b7e976ceb1e2a79effa73ed43054a159b1ec84bb8ab2b9d9233e11e79d2`  
		Last Modified: Tue, 30 Mar 2021 20:37:19 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48c9f266166063cd37e8bd0121ed446ceea7acc2e55c2344c9a9e43f57831d2`  
		Last Modified: Tue, 30 Mar 2021 20:37:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b081bb5df92ebd7f82e224bd73ec97142ac5e03491afd7e3175a6da1ad8b2752`  
		Last Modified: Tue, 30 Mar 2021 20:37:19 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3339387309f216813fde3eb9f9b1201109db48a57606fa5577c9aa6a7624c7b`  
		Last Modified: Tue, 30 Mar 2021 20:37:19 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:1f8faed69738382fefa1362211201feffa92146f816e8f6f982234b2558ce41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:8b8adb30c2a08f1715a1558d308c1a0d08e54b4390625fa790ee1beb1bd65de8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542585631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5602746f8c5ff4d662c6d8bf2d7c2b4af9b7af24564502b6e3522c00fb78b92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:15:29 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:15:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:15:29 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:15:30 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Sat, 27 Mar 2021 06:17:31 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:17:45 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:17:58 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:17:58 GMT
ENV ODOO_VERSION=12.0
# Tue, 30 Mar 2021 20:34:01 GMT
ARG ODOO_RELEASE=20210329
# Tue, 30 Mar 2021 20:34:01 GMT
ARG ODOO_SHA=cd334511a519ec8b8fd3f4555171d17f94107b77
# Tue, 30 Mar 2021 20:35:09 GMT
# ARGS: ODOO_RELEASE=20210329 ODOO_SHA=cd334511a519ec8b8fd3f4555171d17f94107b77
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 Mar 2021 20:35:11 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 30 Mar 2021 20:35:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 Mar 2021 20:35:13 GMT
# ARGS: ODOO_RELEASE=20210329 ODOO_SHA=cd334511a519ec8b8fd3f4555171d17f94107b77
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 Mar 2021 20:35:13 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Mar 2021 20:35:13 GMT
EXPOSE 8069 8071 8072
# Tue, 30 Mar 2021 20:35:13 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Mar 2021 20:35:13 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 Mar 2021 20:35:14 GMT
USER odoo
# Tue, 30 Mar 2021 20:35:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Mar 2021 20:35:14 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d85905ea21b22f3cf49d1544d54fa33de25fbd3fb032724098214829848cb7e`  
		Last Modified: Sat, 27 Mar 2021 06:22:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997e5ef07b089b7d6a8a1ab2cc7851f20c4bd8eab43877b4e69f39d90aa2dacd`  
		Last Modified: Sat, 27 Mar 2021 06:22:45 GMT  
		Size: 219.7 MB (219658920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03046533a143ccada4bcf38fe3cf27238bf9807d1705bd7f63fbb7c99d17accc`  
		Last Modified: Sat, 27 Mar 2021 06:22:02 GMT  
		Size: 2.2 MB (2224133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555b0321ec586fdb7780ba6462caba21fe7328c3b6971007ffb99e4c1d83212e`  
		Last Modified: Sat, 27 Mar 2021 06:22:11 GMT  
		Size: 22.1 MB (22053347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8726deeabbc7d4caeec0124482d31ed9aead04000972f546b3ba2a2ed0d98141`  
		Last Modified: Tue, 30 Mar 2021 20:37:49 GMT  
		Size: 276.1 MB (276118163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82df7b7e976ceb1e2a79effa73ed43054a159b1ec84bb8ab2b9d9233e11e79d2`  
		Last Modified: Tue, 30 Mar 2021 20:37:19 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48c9f266166063cd37e8bd0121ed446ceea7acc2e55c2344c9a9e43f57831d2`  
		Last Modified: Tue, 30 Mar 2021 20:37:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b081bb5df92ebd7f82e224bd73ec97142ac5e03491afd7e3175a6da1ad8b2752`  
		Last Modified: Tue, 30 Mar 2021 20:37:19 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3339387309f216813fde3eb9f9b1201109db48a57606fa5577c9aa6a7624c7b`  
		Last Modified: Tue, 30 Mar 2021 20:37:19 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:23e32e75f7d5e61b13559f6d5579f0d31dfae1b7fbe5ee03b1816cabe3611e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:af5aac5a291bcbed8cdb9f221e1a4afb2700787ee3b28a22eb0d7121d971ab85
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.2 MB (532245602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3676292148434f9b72ec6a20588e8aaa32d03b1d424bc0ad84cc4d5bab6ae7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:08:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:08:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:08:36 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:13:16 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:13:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:13:35 GMT
RUN npm install -g rtlcss
# Sat, 27 Mar 2021 06:13:35 GMT
ENV ODOO_VERSION=13.0
# Tue, 30 Mar 2021 20:32:35 GMT
ARG ODOO_RELEASE=20210330
# Tue, 30 Mar 2021 20:32:35 GMT
ARG ODOO_SHA=0e7a35f95285b360d01f6da0e64282519d025f31
# Tue, 30 Mar 2021 20:33:51 GMT
# ARGS: ODOO_RELEASE=20210330 ODOO_SHA=0e7a35f95285b360d01f6da0e64282519d025f31
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 Mar 2021 20:33:54 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 30 Mar 2021 20:33:55 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 Mar 2021 20:33:56 GMT
# ARGS: ODOO_RELEASE=20210330 ODOO_SHA=0e7a35f95285b360d01f6da0e64282519d025f31
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 Mar 2021 20:33:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Mar 2021 20:33:56 GMT
EXPOSE 8069 8071 8072
# Tue, 30 Mar 2021 20:33:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Mar 2021 20:33:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 Mar 2021 20:33:57 GMT
USER odoo
# Tue, 30 Mar 2021 20:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Mar 2021 20:33:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526d3837c49e3c6200cfda6d26a6a95d4cfad7afa9fa844b8c35089e92dffb36`  
		Last Modified: Sat, 27 Mar 2021 06:21:34 GMT  
		Size: 207.1 MB (207120267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eaf1ef56328b5cbcbe06575a189e8eb7d8aa1e73926fe07cfb752c883eb46e`  
		Last Modified: Sat, 27 Mar 2021 06:21:02 GMT  
		Size: 2.3 MB (2345443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68a125c2a68878ed8b102fb46ce796a30f6d773f1ddb77fa7ca748d00cd94b8`  
		Last Modified: Sat, 27 Mar 2021 06:21:01 GMT  
		Size: 909.8 KB (909791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e777bbcd98b7cca403079f18b02ea7c4132755f66dcb736d288474729efd460`  
		Last Modified: Tue, 30 Mar 2021 20:37:08 GMT  
		Size: 294.8 MB (294766671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99437ac8daf6c158a5b2d704936c48e599ab990f1a0256769755e2204a0d4e3a`  
		Last Modified: Tue, 30 Mar 2021 20:36:31 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aaa8fa6aa247a63c071e8eea0cecf7bfd0e06818c7422a07ec90bfa38b554a`  
		Last Modified: Tue, 30 Mar 2021 20:36:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129cff50094f2b02701f14133726470dce8fe4bf8214dd4df36977a91cae1763`  
		Last Modified: Tue, 30 Mar 2021 20:36:31 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fb4a74d74afa55267a8e5a60f7fcc2f81a1a35f5fef75e2e12f8a20ad823d3`  
		Last Modified: Tue, 30 Mar 2021 20:36:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:23e32e75f7d5e61b13559f6d5579f0d31dfae1b7fbe5ee03b1816cabe3611e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:af5aac5a291bcbed8cdb9f221e1a4afb2700787ee3b28a22eb0d7121d971ab85
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.2 MB (532245602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3676292148434f9b72ec6a20588e8aaa32d03b1d424bc0ad84cc4d5bab6ae7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:08:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:08:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:08:36 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:13:16 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:13:29 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:13:35 GMT
RUN npm install -g rtlcss
# Sat, 27 Mar 2021 06:13:35 GMT
ENV ODOO_VERSION=13.0
# Tue, 30 Mar 2021 20:32:35 GMT
ARG ODOO_RELEASE=20210330
# Tue, 30 Mar 2021 20:32:35 GMT
ARG ODOO_SHA=0e7a35f95285b360d01f6da0e64282519d025f31
# Tue, 30 Mar 2021 20:33:51 GMT
# ARGS: ODOO_RELEASE=20210330 ODOO_SHA=0e7a35f95285b360d01f6da0e64282519d025f31
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 Mar 2021 20:33:54 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 30 Mar 2021 20:33:55 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 Mar 2021 20:33:56 GMT
# ARGS: ODOO_RELEASE=20210330 ODOO_SHA=0e7a35f95285b360d01f6da0e64282519d025f31
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 Mar 2021 20:33:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Mar 2021 20:33:56 GMT
EXPOSE 8069 8071 8072
# Tue, 30 Mar 2021 20:33:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Mar 2021 20:33:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 Mar 2021 20:33:57 GMT
USER odoo
# Tue, 30 Mar 2021 20:33:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Mar 2021 20:33:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526d3837c49e3c6200cfda6d26a6a95d4cfad7afa9fa844b8c35089e92dffb36`  
		Last Modified: Sat, 27 Mar 2021 06:21:34 GMT  
		Size: 207.1 MB (207120267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eaf1ef56328b5cbcbe06575a189e8eb7d8aa1e73926fe07cfb752c883eb46e`  
		Last Modified: Sat, 27 Mar 2021 06:21:02 GMT  
		Size: 2.3 MB (2345443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68a125c2a68878ed8b102fb46ce796a30f6d773f1ddb77fa7ca748d00cd94b8`  
		Last Modified: Sat, 27 Mar 2021 06:21:01 GMT  
		Size: 909.8 KB (909791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e777bbcd98b7cca403079f18b02ea7c4132755f66dcb736d288474729efd460`  
		Last Modified: Tue, 30 Mar 2021 20:37:08 GMT  
		Size: 294.8 MB (294766671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99437ac8daf6c158a5b2d704936c48e599ab990f1a0256769755e2204a0d4e3a`  
		Last Modified: Tue, 30 Mar 2021 20:36:31 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aaa8fa6aa247a63c071e8eea0cecf7bfd0e06818c7422a07ec90bfa38b554a`  
		Last Modified: Tue, 30 Mar 2021 20:36:31 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129cff50094f2b02701f14133726470dce8fe4bf8214dd4df36977a91cae1763`  
		Last Modified: Tue, 30 Mar 2021 20:36:31 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2fb4a74d74afa55267a8e5a60f7fcc2f81a1a35f5fef75e2e12f8a20ad823d3`  
		Last Modified: Tue, 30 Mar 2021 20:36:32 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:9709bf21e6efe94f3d1967ec760d27479cfaa2b6ef8f68a4a8b68b87b3f654af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:e875c60cdfb0e9fe64deceb15f47af81b8c65540e5da95b7b139594e9230881d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.8 MB (515761252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc7fca734f3957554da9532068db08fe17e5780cafb5cf8c87468c516640f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:08:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:08:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:08:36 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:09:55 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:10:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:10:15 GMT
RUN npm install -g rtlcss
# Sat, 27 Mar 2021 06:10:15 GMT
ENV ODOO_VERSION=14.0
# Tue, 30 Mar 2021 20:31:09 GMT
ARG ODOO_RELEASE=20210330
# Tue, 30 Mar 2021 20:31:09 GMT
ARG ODOO_SHA=0a0ebf50846a5e5131a6725795c3fc59d511262d
# Tue, 30 Mar 2021 20:32:26 GMT
# ARGS: ODOO_RELEASE=20210330 ODOO_SHA=0a0ebf50846a5e5131a6725795c3fc59d511262d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 Mar 2021 20:32:28 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 30 Mar 2021 20:32:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 Mar 2021 20:32:30 GMT
# ARGS: ODOO_RELEASE=20210330 ODOO_SHA=0a0ebf50846a5e5131a6725795c3fc59d511262d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 Mar 2021 20:32:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Mar 2021 20:32:30 GMT
EXPOSE 8069 8071 8072
# Tue, 30 Mar 2021 20:32:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Mar 2021 20:32:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 Mar 2021 20:32:31 GMT
USER odoo
# Tue, 30 Mar 2021 20:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Mar 2021 20:32:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f95e614e07c856f6c1da438d4c95c0a6e5eac30d89fcc3a5734f5135633ed4a`  
		Last Modified: Sat, 27 Mar 2021 06:20:33 GMT  
		Size: 213.2 MB (213156617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08230c79e58cbef992d03708a57cb446a37e38c4aae753a3b55270d96eccf46d`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 2.3 MB (2348523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfde40794ec1a3832504589fefca9859cb38526d3244c425e3dbcefa0cbc7356`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 910.1 KB (910061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d40543785b0ecbd9954b39352273e6e8f24711215dc28f73fdd23e70bf2692b`  
		Last Modified: Tue, 30 Mar 2021 20:36:14 GMT  
		Size: 272.2 MB (272242624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b07fddd5c4a25abf0e6c28d282e9b84cbafb4347a8cdb189b6e55f7049d542`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c6f7368ed8074690d6c222c3daee393f56e5c7388ef6146c7f76263d08813c`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25729b0270c67c2cafe5a02ed3f0ad4a81c49dadeec47c3dcbe5b7fc112d07a`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a297e06400118a4211607da5f02373a22ec80d118969f8b278f6c070216011`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:9709bf21e6efe94f3d1967ec760d27479cfaa2b6ef8f68a4a8b68b87b3f654af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:e875c60cdfb0e9fe64deceb15f47af81b8c65540e5da95b7b139594e9230881d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.8 MB (515761252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc7fca734f3957554da9532068db08fe17e5780cafb5cf8c87468c516640f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:08:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:08:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:08:36 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:09:55 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:10:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:10:15 GMT
RUN npm install -g rtlcss
# Sat, 27 Mar 2021 06:10:15 GMT
ENV ODOO_VERSION=14.0
# Tue, 30 Mar 2021 20:31:09 GMT
ARG ODOO_RELEASE=20210330
# Tue, 30 Mar 2021 20:31:09 GMT
ARG ODOO_SHA=0a0ebf50846a5e5131a6725795c3fc59d511262d
# Tue, 30 Mar 2021 20:32:26 GMT
# ARGS: ODOO_RELEASE=20210330 ODOO_SHA=0a0ebf50846a5e5131a6725795c3fc59d511262d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 Mar 2021 20:32:28 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 30 Mar 2021 20:32:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 Mar 2021 20:32:30 GMT
# ARGS: ODOO_RELEASE=20210330 ODOO_SHA=0a0ebf50846a5e5131a6725795c3fc59d511262d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 Mar 2021 20:32:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Mar 2021 20:32:30 GMT
EXPOSE 8069 8071 8072
# Tue, 30 Mar 2021 20:32:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Mar 2021 20:32:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 Mar 2021 20:32:31 GMT
USER odoo
# Tue, 30 Mar 2021 20:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Mar 2021 20:32:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f95e614e07c856f6c1da438d4c95c0a6e5eac30d89fcc3a5734f5135633ed4a`  
		Last Modified: Sat, 27 Mar 2021 06:20:33 GMT  
		Size: 213.2 MB (213156617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08230c79e58cbef992d03708a57cb446a37e38c4aae753a3b55270d96eccf46d`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 2.3 MB (2348523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfde40794ec1a3832504589fefca9859cb38526d3244c425e3dbcefa0cbc7356`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 910.1 KB (910061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d40543785b0ecbd9954b39352273e6e8f24711215dc28f73fdd23e70bf2692b`  
		Last Modified: Tue, 30 Mar 2021 20:36:14 GMT  
		Size: 272.2 MB (272242624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b07fddd5c4a25abf0e6c28d282e9b84cbafb4347a8cdb189b6e55f7049d542`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c6f7368ed8074690d6c222c3daee393f56e5c7388ef6146c7f76263d08813c`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25729b0270c67c2cafe5a02ed3f0ad4a81c49dadeec47c3dcbe5b7fc112d07a`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a297e06400118a4211607da5f02373a22ec80d118969f8b278f6c070216011`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:9709bf21e6efe94f3d1967ec760d27479cfaa2b6ef8f68a4a8b68b87b3f654af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:e875c60cdfb0e9fe64deceb15f47af81b8c65540e5da95b7b139594e9230881d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.8 MB (515761252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc7fca734f3957554da9532068db08fe17e5780cafb5cf8c87468c516640f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:08:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:08:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:08:36 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:09:55 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:10:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:10:15 GMT
RUN npm install -g rtlcss
# Sat, 27 Mar 2021 06:10:15 GMT
ENV ODOO_VERSION=14.0
# Tue, 30 Mar 2021 20:31:09 GMT
ARG ODOO_RELEASE=20210330
# Tue, 30 Mar 2021 20:31:09 GMT
ARG ODOO_SHA=0a0ebf50846a5e5131a6725795c3fc59d511262d
# Tue, 30 Mar 2021 20:32:26 GMT
# ARGS: ODOO_RELEASE=20210330 ODOO_SHA=0a0ebf50846a5e5131a6725795c3fc59d511262d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 Mar 2021 20:32:28 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 30 Mar 2021 20:32:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 Mar 2021 20:32:30 GMT
# ARGS: ODOO_RELEASE=20210330 ODOO_SHA=0a0ebf50846a5e5131a6725795c3fc59d511262d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 Mar 2021 20:32:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Mar 2021 20:32:30 GMT
EXPOSE 8069 8071 8072
# Tue, 30 Mar 2021 20:32:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Mar 2021 20:32:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 Mar 2021 20:32:31 GMT
USER odoo
# Tue, 30 Mar 2021 20:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Mar 2021 20:32:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f95e614e07c856f6c1da438d4c95c0a6e5eac30d89fcc3a5734f5135633ed4a`  
		Last Modified: Sat, 27 Mar 2021 06:20:33 GMT  
		Size: 213.2 MB (213156617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08230c79e58cbef992d03708a57cb446a37e38c4aae753a3b55270d96eccf46d`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 2.3 MB (2348523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfde40794ec1a3832504589fefca9859cb38526d3244c425e3dbcefa0cbc7356`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 910.1 KB (910061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d40543785b0ecbd9954b39352273e6e8f24711215dc28f73fdd23e70bf2692b`  
		Last Modified: Tue, 30 Mar 2021 20:36:14 GMT  
		Size: 272.2 MB (272242624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b07fddd5c4a25abf0e6c28d282e9b84cbafb4347a8cdb189b6e55f7049d542`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c6f7368ed8074690d6c222c3daee393f56e5c7388ef6146c7f76263d08813c`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25729b0270c67c2cafe5a02ed3f0ad4a81c49dadeec47c3dcbe5b7fc112d07a`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a297e06400118a4211607da5f02373a22ec80d118969f8b278f6c070216011`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
