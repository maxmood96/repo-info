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
$ docker pull odoo@sha256:840d8081550b1dd8311db0329b38f9ea0bda887e355f1a20e8861fd45fac8d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:47015d34a2a8959ecce43e04b0bd5b4694cbac64ea06099b7cf5f6c467153695
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538411837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b8a1f85d40d74b3cb75e3f336304aa14930162219e56808c5624d5af1debcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:21:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:21:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:21:42 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:21:43 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 03 Sep 2021 08:23:12 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:24:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:25:00 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:25:01 GMT
ENV ODOO_VERSION=12.0
# Fri, 03 Sep 2021 08:25:01 GMT
ARG ODOO_RELEASE=20210809
# Fri, 03 Sep 2021 08:25:01 GMT
ARG ODOO_SHA=7834befe1d22ae1c30bce23e1c10ab83a2963d26
# Fri, 03 Sep 2021 08:26:33 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=7834befe1d22ae1c30bce23e1c10ab83a2963d26
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 03 Sep 2021 08:26:36 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 03 Sep 2021 08:26:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 03 Sep 2021 08:26:38 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=7834befe1d22ae1c30bce23e1c10ab83a2963d26
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 03 Sep 2021 08:26:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 03 Sep 2021 08:26:39 GMT
EXPOSE 8069 8071 8072
# Fri, 03 Sep 2021 08:26:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 03 Sep 2021 08:26:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 03 Sep 2021 08:26:40 GMT
USER odoo
# Fri, 03 Sep 2021 08:26:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 08:26:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ef1fc36ce9f3859bf889c86d8cd74979ed71ae7106adb1aad7d64adb740273`  
		Last Modified: Fri, 03 Sep 2021 08:29:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff2c6c124745ce3574461d76e169045d3084e09b9c4f9a596b17659b03b4dd2`  
		Last Modified: Fri, 03 Sep 2021 08:29:29 GMT  
		Size: 219.7 MB (219657617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dde6f436aefae775b74932ee4deb96d884f715e70db318fa94b046d3080086`  
		Last Modified: Fri, 03 Sep 2021 08:29:02 GMT  
		Size: 2.2 MB (2227388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6736d7cb64ee6e1a364dcddaedf7d1e246cbf2e7cd24b3fa9c63f244fbc1b5`  
		Last Modified: Fri, 03 Sep 2021 08:29:07 GMT  
		Size: 22.0 MB (22030059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4a01424c92b989ab4cad85602be52eedafd8ca19689cd50bdea3475c5a32f`  
		Last Modified: Fri, 03 Sep 2021 08:29:33 GMT  
		Size: 272.0 MB (271966644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f088ed21f80571bff3c2620e0e3af0d855f5dbf9467d9bd21a3236f215ec38`  
		Last Modified: Fri, 03 Sep 2021 08:28:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45562f3cb99062ce635436c16085addef79f780ef1cfa5257f364637525434b`  
		Last Modified: Fri, 03 Sep 2021 08:28:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f1d2c9d44ac68db8d332f81310c7220e4aa9f3d78469a56863a65a1e785580`  
		Last Modified: Fri, 03 Sep 2021 08:28:59 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21be224fbe1bb6fd6c5517e5bc5ab5e97f25b3922c995f6232a73e89824d81fb`  
		Last Modified: Fri, 03 Sep 2021 08:28:59 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:840d8081550b1dd8311db0329b38f9ea0bda887e355f1a20e8861fd45fac8d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:47015d34a2a8959ecce43e04b0bd5b4694cbac64ea06099b7cf5f6c467153695
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538411837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b8a1f85d40d74b3cb75e3f336304aa14930162219e56808c5624d5af1debcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:21:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:21:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:21:42 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:21:43 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 03 Sep 2021 08:23:12 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:24:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:25:00 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:25:01 GMT
ENV ODOO_VERSION=12.0
# Fri, 03 Sep 2021 08:25:01 GMT
ARG ODOO_RELEASE=20210809
# Fri, 03 Sep 2021 08:25:01 GMT
ARG ODOO_SHA=7834befe1d22ae1c30bce23e1c10ab83a2963d26
# Fri, 03 Sep 2021 08:26:33 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=7834befe1d22ae1c30bce23e1c10ab83a2963d26
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 03 Sep 2021 08:26:36 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 03 Sep 2021 08:26:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 03 Sep 2021 08:26:38 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=7834befe1d22ae1c30bce23e1c10ab83a2963d26
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 03 Sep 2021 08:26:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 03 Sep 2021 08:26:39 GMT
EXPOSE 8069 8071 8072
# Fri, 03 Sep 2021 08:26:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 03 Sep 2021 08:26:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 03 Sep 2021 08:26:40 GMT
USER odoo
# Fri, 03 Sep 2021 08:26:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 08:26:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ef1fc36ce9f3859bf889c86d8cd74979ed71ae7106adb1aad7d64adb740273`  
		Last Modified: Fri, 03 Sep 2021 08:29:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff2c6c124745ce3574461d76e169045d3084e09b9c4f9a596b17659b03b4dd2`  
		Last Modified: Fri, 03 Sep 2021 08:29:29 GMT  
		Size: 219.7 MB (219657617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dde6f436aefae775b74932ee4deb96d884f715e70db318fa94b046d3080086`  
		Last Modified: Fri, 03 Sep 2021 08:29:02 GMT  
		Size: 2.2 MB (2227388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6736d7cb64ee6e1a364dcddaedf7d1e246cbf2e7cd24b3fa9c63f244fbc1b5`  
		Last Modified: Fri, 03 Sep 2021 08:29:07 GMT  
		Size: 22.0 MB (22030059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4a01424c92b989ab4cad85602be52eedafd8ca19689cd50bdea3475c5a32f`  
		Last Modified: Fri, 03 Sep 2021 08:29:33 GMT  
		Size: 272.0 MB (271966644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f088ed21f80571bff3c2620e0e3af0d855f5dbf9467d9bd21a3236f215ec38`  
		Last Modified: Fri, 03 Sep 2021 08:28:59 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45562f3cb99062ce635436c16085addef79f780ef1cfa5257f364637525434b`  
		Last Modified: Fri, 03 Sep 2021 08:28:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f1d2c9d44ac68db8d332f81310c7220e4aa9f3d78469a56863a65a1e785580`  
		Last Modified: Fri, 03 Sep 2021 08:28:59 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21be224fbe1bb6fd6c5517e5bc5ab5e97f25b3922c995f6232a73e89824d81fb`  
		Last Modified: Fri, 03 Sep 2021 08:28:59 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:042fe948a0c352ce422b494514ec01b13273c68063068020ff1a0d2a829dd467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:2638d577cab9d6a9a557b53881e9d0da6f429ed9df5f3bc556c125a23d944540
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528411927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea105e596bcdd8d1f3fb45fab107e87a65c494ef974ad92a9af749106c47e7d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:14:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:14:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:14:49 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:19:29 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:19:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:19:47 GMT
RUN npm install -g rtlcss
# Fri, 03 Sep 2021 08:19:48 GMT
ENV ODOO_VERSION=13.0
# Fri, 03 Sep 2021 08:19:48 GMT
ARG ODOO_RELEASE=20210809
# Fri, 03 Sep 2021 08:19:48 GMT
ARG ODOO_SHA=dd7613080ed2b919e6d0b0d819b271400f29a9f9
# Fri, 03 Sep 2021 08:21:22 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=dd7613080ed2b919e6d0b0d819b271400f29a9f9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 03 Sep 2021 08:21:26 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 03 Sep 2021 08:21:26 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 03 Sep 2021 08:21:27 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=dd7613080ed2b919e6d0b0d819b271400f29a9f9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 03 Sep 2021 08:21:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 03 Sep 2021 08:21:28 GMT
EXPOSE 8069 8071 8072
# Fri, 03 Sep 2021 08:21:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 03 Sep 2021 08:21:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 03 Sep 2021 08:21:28 GMT
USER odoo
# Fri, 03 Sep 2021 08:21:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 08:21:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f62eaaa3a419466e2cd8478b7344c1acd06a6095fb959f5981431356166c72`  
		Last Modified: Fri, 03 Sep 2021 08:28:43 GMT  
		Size: 207.1 MB (207129591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564b1b987da5a51f9753c4e9903495b0b9cb9d58f79cf0e7ff747938a4237a5`  
		Last Modified: Fri, 03 Sep 2021 08:28:15 GMT  
		Size: 2.3 MB (2347919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f6c8a96ec08781ed03569e5dc126ee49838d7d7891d7606e9aa97091348ad6`  
		Last Modified: Fri, 03 Sep 2021 08:28:14 GMT  
		Size: 893.4 KB (893373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecf1c0584d64f6d93681e56331e48c39f6791e6a68431988149448b9e82bf41`  
		Last Modified: Fri, 03 Sep 2021 08:28:49 GMT  
		Size: 290.9 MB (290892737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0bde256072c38298912fdcc958313da4d2ad4132838ace36b5dbed1c1f76a4`  
		Last Modified: Fri, 03 Sep 2021 08:28:12 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb15aad6908b3606f9d6b2e1aada92ed210a17404445c21c887f0c355e78dd2`  
		Last Modified: Fri, 03 Sep 2021 08:28:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6fed59bc66503fcaacb1888af6cd4ff5a41e5de0a285aee7569b59ab3649ca`  
		Last Modified: Fri, 03 Sep 2021 08:28:12 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc4cc0475d7f5c85922330ea57f2617b264a8e4c49d1c58a917583fbe4abca0`  
		Last Modified: Fri, 03 Sep 2021 08:28:12 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:042fe948a0c352ce422b494514ec01b13273c68063068020ff1a0d2a829dd467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:2638d577cab9d6a9a557b53881e9d0da6f429ed9df5f3bc556c125a23d944540
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.4 MB (528411927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea105e596bcdd8d1f3fb45fab107e87a65c494ef974ad92a9af749106c47e7d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:14:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:14:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:14:49 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:19:29 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:19:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:19:47 GMT
RUN npm install -g rtlcss
# Fri, 03 Sep 2021 08:19:48 GMT
ENV ODOO_VERSION=13.0
# Fri, 03 Sep 2021 08:19:48 GMT
ARG ODOO_RELEASE=20210809
# Fri, 03 Sep 2021 08:19:48 GMT
ARG ODOO_SHA=dd7613080ed2b919e6d0b0d819b271400f29a9f9
# Fri, 03 Sep 2021 08:21:22 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=dd7613080ed2b919e6d0b0d819b271400f29a9f9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 03 Sep 2021 08:21:26 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 03 Sep 2021 08:21:26 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 03 Sep 2021 08:21:27 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=dd7613080ed2b919e6d0b0d819b271400f29a9f9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 03 Sep 2021 08:21:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 03 Sep 2021 08:21:28 GMT
EXPOSE 8069 8071 8072
# Fri, 03 Sep 2021 08:21:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 03 Sep 2021 08:21:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 03 Sep 2021 08:21:28 GMT
USER odoo
# Fri, 03 Sep 2021 08:21:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 08:21:29 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f62eaaa3a419466e2cd8478b7344c1acd06a6095fb959f5981431356166c72`  
		Last Modified: Fri, 03 Sep 2021 08:28:43 GMT  
		Size: 207.1 MB (207129591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564b1b987da5a51f9753c4e9903495b0b9cb9d58f79cf0e7ff747938a4237a5`  
		Last Modified: Fri, 03 Sep 2021 08:28:15 GMT  
		Size: 2.3 MB (2347919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f6c8a96ec08781ed03569e5dc126ee49838d7d7891d7606e9aa97091348ad6`  
		Last Modified: Fri, 03 Sep 2021 08:28:14 GMT  
		Size: 893.4 KB (893373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ecf1c0584d64f6d93681e56331e48c39f6791e6a68431988149448b9e82bf41`  
		Last Modified: Fri, 03 Sep 2021 08:28:49 GMT  
		Size: 290.9 MB (290892737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0bde256072c38298912fdcc958313da4d2ad4132838ace36b5dbed1c1f76a4`  
		Last Modified: Fri, 03 Sep 2021 08:28:12 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb15aad6908b3606f9d6b2e1aada92ed210a17404445c21c887f0c355e78dd2`  
		Last Modified: Fri, 03 Sep 2021 08:28:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6fed59bc66503fcaacb1888af6cd4ff5a41e5de0a285aee7569b59ab3649ca`  
		Last Modified: Fri, 03 Sep 2021 08:28:12 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc4cc0475d7f5c85922330ea57f2617b264a8e4c49d1c58a917583fbe4abca0`  
		Last Modified: Fri, 03 Sep 2021 08:28:12 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:513550f4165e5ddc36ea870059718f95bdcbe61d3e454610fe85298e4ee70119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:329167e10f2ee32a96247d63900717c6faa80a5014daf74a6a17fd29005dc853
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.8 MB (516764214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78330ed2b4159d658ca98f567ed1eaa86cb3ea13f9e9661ec89c956697be43b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:14:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:14:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:14:49 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:15:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:16:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:16:12 GMT
RUN npm install -g rtlcss
# Fri, 03 Sep 2021 08:16:13 GMT
ENV ODOO_VERSION=14.0
# Fri, 03 Sep 2021 08:16:13 GMT
ARG ODOO_RELEASE=20210809
# Fri, 03 Sep 2021 08:16:13 GMT
ARG ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
# Fri, 03 Sep 2021 08:17:46 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 03 Sep 2021 08:17:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 03 Sep 2021 08:17:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 03 Sep 2021 08:17:52 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 03 Sep 2021 08:17:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 03 Sep 2021 08:17:53 GMT
EXPOSE 8069 8071 8072
# Fri, 03 Sep 2021 08:17:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 03 Sep 2021 08:17:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 03 Sep 2021 08:17:54 GMT
USER odoo
# Fri, 03 Sep 2021 08:17:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 08:17:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747cf09456121867c9a11a2b2e1b877b80dd32b1ffe451e88685f790bd2188f6`  
		Last Modified: Fri, 03 Sep 2021 08:27:50 GMT  
		Size: 213.2 MB (213172901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51c6b9c93241bd96d38967891f77680616b4df0ad6f2255bf7b4e375736d481`  
		Last Modified: Fri, 03 Sep 2021 08:27:14 GMT  
		Size: 2.4 MB (2350482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644c7d878f88578d6d5aa3edcc8f5f864b3568da52f0cbd89f566950d57bc9c8`  
		Last Modified: Fri, 03 Sep 2021 08:27:13 GMT  
		Size: 893.3 KB (893252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f57db45a946e7b8878fca0b3d7e5a80f17acee9b9e5d39df4081220a6c4adf`  
		Last Modified: Fri, 03 Sep 2021 08:27:58 GMT  
		Size: 273.2 MB (273199275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce0de6499ec5ca3a22eb60b395fc653eadca7dde5b79dcf61f2facc57ffd3f2`  
		Last Modified: Fri, 03 Sep 2021 08:27:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c224393caa418d42e9e9787c25e44d63c28291b8cceb71b2856fadc59dae8c`  
		Last Modified: Fri, 03 Sep 2021 08:27:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2970f57318788ea6776c6b3b0333623605c081e76ffa41972b784d58ab01f7a`  
		Last Modified: Fri, 03 Sep 2021 08:27:10 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38958ecd9dfce1ad80bbf59ffd456b934e47017207e6c6dc45155fdf9c3231df`  
		Last Modified: Fri, 03 Sep 2021 08:27:10 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:513550f4165e5ddc36ea870059718f95bdcbe61d3e454610fe85298e4ee70119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:329167e10f2ee32a96247d63900717c6faa80a5014daf74a6a17fd29005dc853
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.8 MB (516764214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78330ed2b4159d658ca98f567ed1eaa86cb3ea13f9e9661ec89c956697be43b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:14:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:14:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:14:49 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:15:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:16:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:16:12 GMT
RUN npm install -g rtlcss
# Fri, 03 Sep 2021 08:16:13 GMT
ENV ODOO_VERSION=14.0
# Fri, 03 Sep 2021 08:16:13 GMT
ARG ODOO_RELEASE=20210809
# Fri, 03 Sep 2021 08:16:13 GMT
ARG ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
# Fri, 03 Sep 2021 08:17:46 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 03 Sep 2021 08:17:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 03 Sep 2021 08:17:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 03 Sep 2021 08:17:52 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 03 Sep 2021 08:17:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 03 Sep 2021 08:17:53 GMT
EXPOSE 8069 8071 8072
# Fri, 03 Sep 2021 08:17:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 03 Sep 2021 08:17:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 03 Sep 2021 08:17:54 GMT
USER odoo
# Fri, 03 Sep 2021 08:17:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 08:17:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747cf09456121867c9a11a2b2e1b877b80dd32b1ffe451e88685f790bd2188f6`  
		Last Modified: Fri, 03 Sep 2021 08:27:50 GMT  
		Size: 213.2 MB (213172901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51c6b9c93241bd96d38967891f77680616b4df0ad6f2255bf7b4e375736d481`  
		Last Modified: Fri, 03 Sep 2021 08:27:14 GMT  
		Size: 2.4 MB (2350482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644c7d878f88578d6d5aa3edcc8f5f864b3568da52f0cbd89f566950d57bc9c8`  
		Last Modified: Fri, 03 Sep 2021 08:27:13 GMT  
		Size: 893.3 KB (893252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f57db45a946e7b8878fca0b3d7e5a80f17acee9b9e5d39df4081220a6c4adf`  
		Last Modified: Fri, 03 Sep 2021 08:27:58 GMT  
		Size: 273.2 MB (273199275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce0de6499ec5ca3a22eb60b395fc653eadca7dde5b79dcf61f2facc57ffd3f2`  
		Last Modified: Fri, 03 Sep 2021 08:27:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c224393caa418d42e9e9787c25e44d63c28291b8cceb71b2856fadc59dae8c`  
		Last Modified: Fri, 03 Sep 2021 08:27:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2970f57318788ea6776c6b3b0333623605c081e76ffa41972b784d58ab01f7a`  
		Last Modified: Fri, 03 Sep 2021 08:27:10 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38958ecd9dfce1ad80bbf59ffd456b934e47017207e6c6dc45155fdf9c3231df`  
		Last Modified: Fri, 03 Sep 2021 08:27:10 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:513550f4165e5ddc36ea870059718f95bdcbe61d3e454610fe85298e4ee70119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:329167e10f2ee32a96247d63900717c6faa80a5014daf74a6a17fd29005dc853
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.8 MB (516764214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78330ed2b4159d658ca98f567ed1eaa86cb3ea13f9e9661ec89c956697be43b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 08:14:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 03 Sep 2021 08:14:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 03 Sep 2021 08:14:49 GMT
ENV LANG=C.UTF-8
# Fri, 03 Sep 2021 08:15:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 03 Sep 2021 08:16:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 08:16:12 GMT
RUN npm install -g rtlcss
# Fri, 03 Sep 2021 08:16:13 GMT
ENV ODOO_VERSION=14.0
# Fri, 03 Sep 2021 08:16:13 GMT
ARG ODOO_RELEASE=20210809
# Fri, 03 Sep 2021 08:16:13 GMT
ARG ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
# Fri, 03 Sep 2021 08:17:46 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 03 Sep 2021 08:17:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 03 Sep 2021 08:17:51 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 03 Sep 2021 08:17:52 GMT
# ARGS: ODOO_RELEASE=20210809 ODOO_SHA=d9d18498eab946032cacd23d9e8ae69bfbce046b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 03 Sep 2021 08:17:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 03 Sep 2021 08:17:53 GMT
EXPOSE 8069 8071 8072
# Fri, 03 Sep 2021 08:17:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 03 Sep 2021 08:17:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 03 Sep 2021 08:17:54 GMT
USER odoo
# Fri, 03 Sep 2021 08:17:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 08:17:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747cf09456121867c9a11a2b2e1b877b80dd32b1ffe451e88685f790bd2188f6`  
		Last Modified: Fri, 03 Sep 2021 08:27:50 GMT  
		Size: 213.2 MB (213172901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51c6b9c93241bd96d38967891f77680616b4df0ad6f2255bf7b4e375736d481`  
		Last Modified: Fri, 03 Sep 2021 08:27:14 GMT  
		Size: 2.4 MB (2350482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644c7d878f88578d6d5aa3edcc8f5f864b3568da52f0cbd89f566950d57bc9c8`  
		Last Modified: Fri, 03 Sep 2021 08:27:13 GMT  
		Size: 893.3 KB (893252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f57db45a946e7b8878fca0b3d7e5a80f17acee9b9e5d39df4081220a6c4adf`  
		Last Modified: Fri, 03 Sep 2021 08:27:58 GMT  
		Size: 273.2 MB (273199275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce0de6499ec5ca3a22eb60b395fc653eadca7dde5b79dcf61f2facc57ffd3f2`  
		Last Modified: Fri, 03 Sep 2021 08:27:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c224393caa418d42e9e9787c25e44d63c28291b8cceb71b2856fadc59dae8c`  
		Last Modified: Fri, 03 Sep 2021 08:27:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2970f57318788ea6776c6b3b0333623605c081e76ffa41972b784d58ab01f7a`  
		Last Modified: Fri, 03 Sep 2021 08:27:10 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38958ecd9dfce1ad80bbf59ffd456b934e47017207e6c6dc45155fdf9c3231df`  
		Last Modified: Fri, 03 Sep 2021 08:27:10 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
