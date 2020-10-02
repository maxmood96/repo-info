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
$ docker pull odoo@sha256:5e27025af98b6d52ff2c02a25d8032b9ae9152dceaa06510b284ef7dadf74dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:c5f2c0ee85fbf02a0396de8273ea688fdee749f6d8cae8adc878bc110a05494a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.4 MB (396427542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43d7abd4e5152a09de7430f16b8bcf6026c029af0797ad920b11071d392fef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:52:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Sep 2020 12:52:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Sep 2020 12:52:34 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 12:52:36 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 10 Sep 2020 12:54:27 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 10 Sep 2020 12:54:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:54:50 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:54:51 GMT
ENV ODOO_VERSION=12.0
# Thu, 10 Sep 2020 12:54:51 GMT
ARG ODOO_RELEASE=20200826
# Thu, 10 Sep 2020 12:54:51 GMT
ARG ODOO_SHA=3acc73ce5dfbe550d6ad617a4078b0a5d160f9db
# Thu, 10 Sep 2020 12:55:35 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=3acc73ce5dfbe550d6ad617a4078b0a5d160f9db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 10 Sep 2020 12:55:36 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 10 Sep 2020 12:55:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 10 Sep 2020 12:55:37 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=3acc73ce5dfbe550d6ad617a4078b0a5d160f9db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 10 Sep 2020 12:55:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Sep 2020 12:55:38 GMT
EXPOSE 8069 8071 8072
# Thu, 10 Sep 2020 12:55:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Sep 2020 12:55:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 10 Sep 2020 12:55:38 GMT
USER odoo
# Thu, 10 Sep 2020 12:55:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 12:55:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56086b9aed3618fa49ce55fed84ad357d06f45b40509bd912a7952de116fa05b`  
		Last Modified: Thu, 10 Sep 2020 12:57:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460ce2e8a64c8ca25c6101e91b65de99f96d69bd737b6595c8f0ff7029bcdb54`  
		Last Modified: Thu, 10 Sep 2020 12:58:47 GMT  
		Size: 219.6 MB (219609382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0257fe8743d13038cee80f5a656715c65086b5b0ce8e2a87f75f4293cd01b3`  
		Last Modified: Thu, 10 Sep 2020 12:57:58 GMT  
		Size: 2.3 MB (2337725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4793f99106c9a03175078660d27f4a87519096c2bdf5b4158f02ca27111b5c4`  
		Last Modified: Thu, 10 Sep 2020 12:58:16 GMT  
		Size: 22.3 MB (22256625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bbaa5b0e4fc3f8c6fee19e30a6850cd2dddcac0bd01da16fd69d355bfce44d`  
		Last Modified: Thu, 10 Sep 2020 12:58:47 GMT  
		Size: 129.7 MB (129698898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180a1e9c90eb438e3ce6e35bb366f204c1888fe1c41059d1473cb826b1dd650b`  
		Last Modified: Thu, 10 Sep 2020 12:57:56 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726299d487e15d80befb41eb2676bafd2f611196e68a181433c7a0e7a660977`  
		Last Modified: Thu, 10 Sep 2020 12:57:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e939bc69e02ccc399b985687a6ea7cb3b084aa227bc8264e615520f2bebaff64`  
		Last Modified: Thu, 10 Sep 2020 12:57:56 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c06d597c09920bcedcbe6546a2970412f32eb87c8cf8d77b88cd3a0f9cfbd7`  
		Last Modified: Thu, 10 Sep 2020 12:57:56 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:5e27025af98b6d52ff2c02a25d8032b9ae9152dceaa06510b284ef7dadf74dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:c5f2c0ee85fbf02a0396de8273ea688fdee749f6d8cae8adc878bc110a05494a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.4 MB (396427542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43d7abd4e5152a09de7430f16b8bcf6026c029af0797ad920b11071d392fef9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:52:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Sep 2020 12:52:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Sep 2020 12:52:34 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 12:52:36 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 10 Sep 2020 12:54:27 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 10 Sep 2020 12:54:37 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:54:50 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:54:51 GMT
ENV ODOO_VERSION=12.0
# Thu, 10 Sep 2020 12:54:51 GMT
ARG ODOO_RELEASE=20200826
# Thu, 10 Sep 2020 12:54:51 GMT
ARG ODOO_SHA=3acc73ce5dfbe550d6ad617a4078b0a5d160f9db
# Thu, 10 Sep 2020 12:55:35 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=3acc73ce5dfbe550d6ad617a4078b0a5d160f9db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 10 Sep 2020 12:55:36 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 10 Sep 2020 12:55:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 10 Sep 2020 12:55:37 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=3acc73ce5dfbe550d6ad617a4078b0a5d160f9db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 10 Sep 2020 12:55:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Sep 2020 12:55:38 GMT
EXPOSE 8069 8071 8072
# Thu, 10 Sep 2020 12:55:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Sep 2020 12:55:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 10 Sep 2020 12:55:38 GMT
USER odoo
# Thu, 10 Sep 2020 12:55:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 12:55:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56086b9aed3618fa49ce55fed84ad357d06f45b40509bd912a7952de116fa05b`  
		Last Modified: Thu, 10 Sep 2020 12:57:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460ce2e8a64c8ca25c6101e91b65de99f96d69bd737b6595c8f0ff7029bcdb54`  
		Last Modified: Thu, 10 Sep 2020 12:58:47 GMT  
		Size: 219.6 MB (219609382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0257fe8743d13038cee80f5a656715c65086b5b0ce8e2a87f75f4293cd01b3`  
		Last Modified: Thu, 10 Sep 2020 12:57:58 GMT  
		Size: 2.3 MB (2337725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4793f99106c9a03175078660d27f4a87519096c2bdf5b4158f02ca27111b5c4`  
		Last Modified: Thu, 10 Sep 2020 12:58:16 GMT  
		Size: 22.3 MB (22256625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bbaa5b0e4fc3f8c6fee19e30a6850cd2dddcac0bd01da16fd69d355bfce44d`  
		Last Modified: Thu, 10 Sep 2020 12:58:47 GMT  
		Size: 129.7 MB (129698898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180a1e9c90eb438e3ce6e35bb366f204c1888fe1c41059d1473cb826b1dd650b`  
		Last Modified: Thu, 10 Sep 2020 12:57:56 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4726299d487e15d80befb41eb2676bafd2f611196e68a181433c7a0e7a660977`  
		Last Modified: Thu, 10 Sep 2020 12:57:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e939bc69e02ccc399b985687a6ea7cb3b084aa227bc8264e615520f2bebaff64`  
		Last Modified: Thu, 10 Sep 2020 12:57:56 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c06d597c09920bcedcbe6546a2970412f32eb87c8cf8d77b88cd3a0f9cfbd7`  
		Last Modified: Thu, 10 Sep 2020 12:57:56 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:6c91d4789a2dbc71829f6e0e90e7f3745fd43ec5bb14b8eb4f09fea80890d641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:1fbf52736a4d69f1616342b9c111be96f0d0bc3bb47f1e6980143945ec5f4ddd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.3 MB (382302737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f018911ebd84885cf5c5b70a8b0392f7d9229e326197818034fc46065fdb4dac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:49:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Sep 2020 12:49:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Sep 2020 12:49:31 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 12:50:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 10 Sep 2020 12:50:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:50:59 GMT
RUN npm install -g rtlcss
# Thu, 10 Sep 2020 12:50:59 GMT
ENV ODOO_VERSION=13.0
# Thu, 10 Sep 2020 12:50:59 GMT
ARG ODOO_RELEASE=20200826
# Thu, 10 Sep 2020 12:50:59 GMT
ARG ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
# Thu, 10 Sep 2020 12:52:16 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 10 Sep 2020 12:52:18 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 10 Sep 2020 12:52:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 10 Sep 2020 12:52:21 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 10 Sep 2020 12:52:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Sep 2020 12:52:21 GMT
EXPOSE 8069 8071 8072
# Thu, 10 Sep 2020 12:52:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Sep 2020 12:52:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 10 Sep 2020 12:52:23 GMT
USER odoo
# Thu, 10 Sep 2020 12:52:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 12:52:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c2c464f6195f22f9d5287694068d70f208f664cebd88823a71779448bcbfa9`  
		Last Modified: Thu, 10 Sep 2020 12:57:41 GMT  
		Size: 204.1 MB (204054893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaa85eb54a1a8603e92f874b58a604507cbfe1eab02040736f9c4ff171bfe82`  
		Last Modified: Thu, 10 Sep 2020 12:57:03 GMT  
		Size: 2.3 MB (2337739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe33153083cfe1763194a3e50a1d17c86450dd6cd294c5138327a733ded54a`  
		Last Modified: Thu, 10 Sep 2020 12:57:03 GMT  
		Size: 1.1 MB (1100454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf4f7107f7f34081752b4d5beacabbd943dac880b48c519b6e7c8d9aaa2ec12`  
		Last Modified: Thu, 10 Sep 2020 12:57:52 GMT  
		Size: 147.7 MB (147715085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81359091210b3ef6220ab0c621daaf11e9d24c10fdeaf31cdd73b162f4ff9ed8`  
		Last Modified: Thu, 10 Sep 2020 12:57:01 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97901ea432daad25187c703dd676aa8f042058e197797e114e6b88bcd53ef715`  
		Last Modified: Thu, 10 Sep 2020 12:57:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac981b568469f70e139ee3b94e08ad2ebaa9df64e44502da74e467186ca9499c`  
		Last Modified: Thu, 10 Sep 2020 12:57:01 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce985a91ce2039fc4dddf5dedae0da2c18ce145cb5e0db831508ff2324e62a10`  
		Last Modified: Thu, 10 Sep 2020 12:57:01 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:6c91d4789a2dbc71829f6e0e90e7f3745fd43ec5bb14b8eb4f09fea80890d641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:1fbf52736a4d69f1616342b9c111be96f0d0bc3bb47f1e6980143945ec5f4ddd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.3 MB (382302737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f018911ebd84885cf5c5b70a8b0392f7d9229e326197818034fc46065fdb4dac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:49:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Sep 2020 12:49:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Sep 2020 12:49:31 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 12:50:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 10 Sep 2020 12:50:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:50:59 GMT
RUN npm install -g rtlcss
# Thu, 10 Sep 2020 12:50:59 GMT
ENV ODOO_VERSION=13.0
# Thu, 10 Sep 2020 12:50:59 GMT
ARG ODOO_RELEASE=20200826
# Thu, 10 Sep 2020 12:50:59 GMT
ARG ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
# Thu, 10 Sep 2020 12:52:16 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 10 Sep 2020 12:52:18 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 10 Sep 2020 12:52:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 10 Sep 2020 12:52:21 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 10 Sep 2020 12:52:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Sep 2020 12:52:21 GMT
EXPOSE 8069 8071 8072
# Thu, 10 Sep 2020 12:52:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Sep 2020 12:52:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 10 Sep 2020 12:52:23 GMT
USER odoo
# Thu, 10 Sep 2020 12:52:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 12:52:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c2c464f6195f22f9d5287694068d70f208f664cebd88823a71779448bcbfa9`  
		Last Modified: Thu, 10 Sep 2020 12:57:41 GMT  
		Size: 204.1 MB (204054893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaa85eb54a1a8603e92f874b58a604507cbfe1eab02040736f9c4ff171bfe82`  
		Last Modified: Thu, 10 Sep 2020 12:57:03 GMT  
		Size: 2.3 MB (2337739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe33153083cfe1763194a3e50a1d17c86450dd6cd294c5138327a733ded54a`  
		Last Modified: Thu, 10 Sep 2020 12:57:03 GMT  
		Size: 1.1 MB (1100454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf4f7107f7f34081752b4d5beacabbd943dac880b48c519b6e7c8d9aaa2ec12`  
		Last Modified: Thu, 10 Sep 2020 12:57:52 GMT  
		Size: 147.7 MB (147715085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81359091210b3ef6220ab0c621daaf11e9d24c10fdeaf31cdd73b162f4ff9ed8`  
		Last Modified: Thu, 10 Sep 2020 12:57:01 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97901ea432daad25187c703dd676aa8f042058e197797e114e6b88bcd53ef715`  
		Last Modified: Thu, 10 Sep 2020 12:57:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac981b568469f70e139ee3b94e08ad2ebaa9df64e44502da74e467186ca9499c`  
		Last Modified: Thu, 10 Sep 2020 12:57:01 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce985a91ce2039fc4dddf5dedae0da2c18ce145cb5e0db831508ff2324e62a10`  
		Last Modified: Thu, 10 Sep 2020 12:57:01 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

**does not exist** (yet?)

## `odoo:14.0`

**does not exist** (yet?)

## `odoo:latest`

```console
$ docker pull odoo@sha256:6c91d4789a2dbc71829f6e0e90e7f3745fd43ec5bb14b8eb4f09fea80890d641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:1fbf52736a4d69f1616342b9c111be96f0d0bc3bb47f1e6980143945ec5f4ddd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.3 MB (382302737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f018911ebd84885cf5c5b70a8b0392f7d9229e326197818034fc46065fdb4dac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 12:49:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 10 Sep 2020 12:49:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 10 Sep 2020 12:49:31 GMT
ENV LANG=C.UTF-8
# Thu, 10 Sep 2020 12:50:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 10 Sep 2020 12:50:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 12:50:59 GMT
RUN npm install -g rtlcss
# Thu, 10 Sep 2020 12:50:59 GMT
ENV ODOO_VERSION=13.0
# Thu, 10 Sep 2020 12:50:59 GMT
ARG ODOO_RELEASE=20200826
# Thu, 10 Sep 2020 12:50:59 GMT
ARG ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
# Thu, 10 Sep 2020 12:52:16 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 10 Sep 2020 12:52:18 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 10 Sep 2020 12:52:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 10 Sep 2020 12:52:21 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 10 Sep 2020 12:52:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 10 Sep 2020 12:52:21 GMT
EXPOSE 8069 8071 8072
# Thu, 10 Sep 2020 12:52:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 10 Sep 2020 12:52:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 10 Sep 2020 12:52:23 GMT
USER odoo
# Thu, 10 Sep 2020 12:52:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 10 Sep 2020 12:52:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c2c464f6195f22f9d5287694068d70f208f664cebd88823a71779448bcbfa9`  
		Last Modified: Thu, 10 Sep 2020 12:57:41 GMT  
		Size: 204.1 MB (204054893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaa85eb54a1a8603e92f874b58a604507cbfe1eab02040736f9c4ff171bfe82`  
		Last Modified: Thu, 10 Sep 2020 12:57:03 GMT  
		Size: 2.3 MB (2337739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe33153083cfe1763194a3e50a1d17c86450dd6cd294c5138327a733ded54a`  
		Last Modified: Thu, 10 Sep 2020 12:57:03 GMT  
		Size: 1.1 MB (1100454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf4f7107f7f34081752b4d5beacabbd943dac880b48c519b6e7c8d9aaa2ec12`  
		Last Modified: Thu, 10 Sep 2020 12:57:52 GMT  
		Size: 147.7 MB (147715085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81359091210b3ef6220ab0c621daaf11e9d24c10fdeaf31cdd73b162f4ff9ed8`  
		Last Modified: Thu, 10 Sep 2020 12:57:01 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97901ea432daad25187c703dd676aa8f042058e197797e114e6b88bcd53ef715`  
		Last Modified: Thu, 10 Sep 2020 12:57:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac981b568469f70e139ee3b94e08ad2ebaa9df64e44502da74e467186ca9499c`  
		Last Modified: Thu, 10 Sep 2020 12:57:01 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce985a91ce2039fc4dddf5dedae0da2c18ce145cb5e0db831508ff2324e62a10`  
		Last Modified: Thu, 10 Sep 2020 12:57:01 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
