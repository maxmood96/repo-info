<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:11`](#odoo11)
-	[`odoo:11.0`](#odoo110)
-	[`odoo:12`](#odoo12)
-	[`odoo:12.0`](#odoo120)
-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:latest`](#odoolatest)

## `odoo:11`

```console
$ docker pull odoo@sha256:a7a305fdc36ae08761dc95ac28989e4905552c63369cac77c808d05d0af77ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11` - linux; amd64

```console
$ docker pull odoo@sha256:039eb8bbe7efd8617aac56f068cc7840e229719c90d50a4b6ae92be860b6f34b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.1 MB (386126494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d690c2f314c2fbae78ba600272d743b7d37d4a357614e30177e9dada6c9ef1bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:22:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 15 May 2020 20:22:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 15 May 2020 20:22:28 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2020 20:22:29 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 15 May 2020 20:25:04 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 15 May 2020 20:25:18 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:26:46 GMT
ENV ODOO_VERSION=11.0
# Fri, 15 May 2020 20:26:46 GMT
ARG ODOO_RELEASE=20200417
# Fri, 15 May 2020 20:26:46 GMT
ARG ODOO_SHA=e21c34a263785eea09babd7a0d876ba05c841935
# Fri, 15 May 2020 20:27:34 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=e21c34a263785eea09babd7a0d876ba05c841935
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb        && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 May 2020 20:27:36 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Fri, 15 May 2020 20:27:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 May 2020 20:27:38 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=e21c34a263785eea09babd7a0d876ba05c841935
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 May 2020 20:27:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 May 2020 20:27:39 GMT
EXPOSE 8069 8071 8072
# Fri, 15 May 2020 20:27:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 May 2020 20:27:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 May 2020 20:27:40 GMT
USER odoo
# Fri, 15 May 2020 20:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2020 20:27:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e67f7e4d45bb21629cfbd034b9fc0f1a3d4679fafac097ad6ade3b1efd058d3`  
		Last Modified: Fri, 15 May 2020 20:29:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8967fb63366cbc7477fe73d03a1f04d0bd7e21dfe5379f2701a73cd735f02447`  
		Last Modified: Fri, 15 May 2020 20:30:14 GMT  
		Size: 219.7 MB (219651331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7c30e01795bb25acf17e4f5a6f53cba0d976dbb4b32221fa5ec0581b7b280c`  
		Last Modified: Fri, 15 May 2020 20:29:31 GMT  
		Size: 2.3 MB (2336586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5d7d5d7ca7e5c86f7f05b432a6b34a03c03d8c4c2f3286d4825a19733d5666`  
		Last Modified: Fri, 15 May 2020 20:30:52 GMT  
		Size: 141.6 MB (141616055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62c5d5fc43112dc9bd6bf47fbd2f15abedf85d545e9c33c9bacdacd470c7c4a`  
		Last Modified: Fri, 15 May 2020 20:30:19 GMT  
		Size: 674.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb21b3adb2f3e2c1a7e4b146abc864bd63381f7abd3f04acf88b9e4a2ea97034`  
		Last Modified: Fri, 15 May 2020 20:30:19 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d4001b297a0570fd5e6d6dbfc00b0bb4bc193f13cb41e7bcaafd306b075ae9`  
		Last Modified: Fri, 15 May 2020 20:30:19 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7501d85e568a14862f263d417f5f4290d314492287f90368e83d5f8f1470f3e4`  
		Last Modified: Fri, 15 May 2020 20:30:19 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:11.0`

```console
$ docker pull odoo@sha256:a7a305fdc36ae08761dc95ac28989e4905552c63369cac77c808d05d0af77ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11.0` - linux; amd64

```console
$ docker pull odoo@sha256:039eb8bbe7efd8617aac56f068cc7840e229719c90d50a4b6ae92be860b6f34b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.1 MB (386126494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d690c2f314c2fbae78ba600272d743b7d37d4a357614e30177e9dada6c9ef1bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:22:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 15 May 2020 20:22:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 15 May 2020 20:22:28 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2020 20:22:29 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 15 May 2020 20:25:04 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 15 May 2020 20:25:18 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:26:46 GMT
ENV ODOO_VERSION=11.0
# Fri, 15 May 2020 20:26:46 GMT
ARG ODOO_RELEASE=20200417
# Fri, 15 May 2020 20:26:46 GMT
ARG ODOO_SHA=e21c34a263785eea09babd7a0d876ba05c841935
# Fri, 15 May 2020 20:27:34 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=e21c34a263785eea09babd7a0d876ba05c841935
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb        && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 May 2020 20:27:36 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Fri, 15 May 2020 20:27:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 May 2020 20:27:38 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=e21c34a263785eea09babd7a0d876ba05c841935
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 May 2020 20:27:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 May 2020 20:27:39 GMT
EXPOSE 8069 8071 8072
# Fri, 15 May 2020 20:27:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 May 2020 20:27:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 May 2020 20:27:40 GMT
USER odoo
# Fri, 15 May 2020 20:27:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2020 20:27:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e67f7e4d45bb21629cfbd034b9fc0f1a3d4679fafac097ad6ade3b1efd058d3`  
		Last Modified: Fri, 15 May 2020 20:29:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8967fb63366cbc7477fe73d03a1f04d0bd7e21dfe5379f2701a73cd735f02447`  
		Last Modified: Fri, 15 May 2020 20:30:14 GMT  
		Size: 219.7 MB (219651331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7c30e01795bb25acf17e4f5a6f53cba0d976dbb4b32221fa5ec0581b7b280c`  
		Last Modified: Fri, 15 May 2020 20:29:31 GMT  
		Size: 2.3 MB (2336586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5d7d5d7ca7e5c86f7f05b432a6b34a03c03d8c4c2f3286d4825a19733d5666`  
		Last Modified: Fri, 15 May 2020 20:30:52 GMT  
		Size: 141.6 MB (141616055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62c5d5fc43112dc9bd6bf47fbd2f15abedf85d545e9c33c9bacdacd470c7c4a`  
		Last Modified: Fri, 15 May 2020 20:30:19 GMT  
		Size: 674.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb21b3adb2f3e2c1a7e4b146abc864bd63381f7abd3f04acf88b9e4a2ea97034`  
		Last Modified: Fri, 15 May 2020 20:30:19 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d4001b297a0570fd5e6d6dbfc00b0bb4bc193f13cb41e7bcaafd306b075ae9`  
		Last Modified: Fri, 15 May 2020 20:30:19 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7501d85e568a14862f263d417f5f4290d314492287f90368e83d5f8f1470f3e4`  
		Last Modified: Fri, 15 May 2020 20:30:19 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12`

```console
$ docker pull odoo@sha256:7cefb2c3472033c23ab52e09c8d4cb9e0e7a9c4c57422e63f1f44393e3d80682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:aee6d78d22e832926709f05a6df8cd9a2769a72dbe4983cd46fed672d43f3e37
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 MB (395852034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e324bc2d8cdac3af3495080d94f35226bc67ef87fa88011ad2b98d71b45a17fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:22:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 15 May 2020 20:22:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 15 May 2020 20:22:28 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2020 20:22:29 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 15 May 2020 20:25:04 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 15 May 2020 20:25:18 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:25:36 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:25:36 GMT
ENV ODOO_VERSION=12.0
# Fri, 15 May 2020 20:25:36 GMT
ARG ODOO_RELEASE=20200417
# Fri, 15 May 2020 20:25:37 GMT
ARG ODOO_SHA=ca4a7485b0b75850ffe1458a8f3266839400a501
# Fri, 15 May 2020 20:26:24 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=ca4a7485b0b75850ffe1458a8f3266839400a501
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 May 2020 20:26:25 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 15 May 2020 20:26:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 May 2020 20:26:26 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=ca4a7485b0b75850ffe1458a8f3266839400a501
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 May 2020 20:26:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 May 2020 20:26:26 GMT
EXPOSE 8069 8071 8072
# Fri, 15 May 2020 20:26:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 May 2020 20:26:27 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 May 2020 20:26:27 GMT
USER odoo
# Fri, 15 May 2020 20:26:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2020 20:26:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e67f7e4d45bb21629cfbd034b9fc0f1a3d4679fafac097ad6ade3b1efd058d3`  
		Last Modified: Fri, 15 May 2020 20:29:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8967fb63366cbc7477fe73d03a1f04d0bd7e21dfe5379f2701a73cd735f02447`  
		Last Modified: Fri, 15 May 2020 20:30:14 GMT  
		Size: 219.7 MB (219651331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7c30e01795bb25acf17e4f5a6f53cba0d976dbb4b32221fa5ec0581b7b280c`  
		Last Modified: Fri, 15 May 2020 20:29:31 GMT  
		Size: 2.3 MB (2336586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dca58ef1986255a774cdc2ea06689a3cc67362c467c929fe5a9329f636cb468`  
		Last Modified: Fri, 15 May 2020 20:29:38 GMT  
		Size: 22.2 MB (22231831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58f0fa2f5093fda576267fb0ba54a74e3d56b3ffce9fa47be46ca007c6a2d5e`  
		Last Modified: Fri, 15 May 2020 20:30:14 GMT  
		Size: 129.1 MB (129109767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695747e8082c1000975f6c19828a9b234a6806e093b08027184702b16025102`  
		Last Modified: Fri, 15 May 2020 20:29:30 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499703a9c93ff843637f6bd5ec521044abf2a725f481e6e0feb6c763cdecca30`  
		Last Modified: Fri, 15 May 2020 20:29:30 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0530a288e4b7756171139cad9034f181f2f0dbfabb74ce902b3eba3d60d633eb`  
		Last Modified: Fri, 15 May 2020 20:29:30 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b60cf6bb087687bd81737855ba4195a01685a769d46ddcb863938930c59fd0e`  
		Last Modified: Fri, 15 May 2020 20:29:30 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:7cefb2c3472033c23ab52e09c8d4cb9e0e7a9c4c57422e63f1f44393e3d80682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:aee6d78d22e832926709f05a6df8cd9a2769a72dbe4983cd46fed672d43f3e37
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.9 MB (395852034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e324bc2d8cdac3af3495080d94f35226bc67ef87fa88011ad2b98d71b45a17fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:22:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 15 May 2020 20:22:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 15 May 2020 20:22:28 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2020 20:22:29 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Fri, 15 May 2020 20:25:04 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 15 May 2020 20:25:18 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:25:36 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:25:36 GMT
ENV ODOO_VERSION=12.0
# Fri, 15 May 2020 20:25:36 GMT
ARG ODOO_RELEASE=20200417
# Fri, 15 May 2020 20:25:37 GMT
ARG ODOO_SHA=ca4a7485b0b75850ffe1458a8f3266839400a501
# Fri, 15 May 2020 20:26:24 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=ca4a7485b0b75850ffe1458a8f3266839400a501
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 May 2020 20:26:25 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 15 May 2020 20:26:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 May 2020 20:26:26 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=ca4a7485b0b75850ffe1458a8f3266839400a501
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 May 2020 20:26:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 May 2020 20:26:26 GMT
EXPOSE 8069 8071 8072
# Fri, 15 May 2020 20:26:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 May 2020 20:26:27 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 May 2020 20:26:27 GMT
USER odoo
# Fri, 15 May 2020 20:26:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2020 20:26:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e67f7e4d45bb21629cfbd034b9fc0f1a3d4679fafac097ad6ade3b1efd058d3`  
		Last Modified: Fri, 15 May 2020 20:29:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8967fb63366cbc7477fe73d03a1f04d0bd7e21dfe5379f2701a73cd735f02447`  
		Last Modified: Fri, 15 May 2020 20:30:14 GMT  
		Size: 219.7 MB (219651331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7c30e01795bb25acf17e4f5a6f53cba0d976dbb4b32221fa5ec0581b7b280c`  
		Last Modified: Fri, 15 May 2020 20:29:31 GMT  
		Size: 2.3 MB (2336586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dca58ef1986255a774cdc2ea06689a3cc67362c467c929fe5a9329f636cb468`  
		Last Modified: Fri, 15 May 2020 20:29:38 GMT  
		Size: 22.2 MB (22231831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58f0fa2f5093fda576267fb0ba54a74e3d56b3ffce9fa47be46ca007c6a2d5e`  
		Last Modified: Fri, 15 May 2020 20:30:14 GMT  
		Size: 129.1 MB (129109767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695747e8082c1000975f6c19828a9b234a6806e093b08027184702b16025102`  
		Last Modified: Fri, 15 May 2020 20:29:30 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499703a9c93ff843637f6bd5ec521044abf2a725f481e6e0feb6c763cdecca30`  
		Last Modified: Fri, 15 May 2020 20:29:30 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0530a288e4b7756171139cad9034f181f2f0dbfabb74ce902b3eba3d60d633eb`  
		Last Modified: Fri, 15 May 2020 20:29:30 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b60cf6bb087687bd81737855ba4195a01685a769d46ddcb863938930c59fd0e`  
		Last Modified: Fri, 15 May 2020 20:29:30 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:9f8fd5de111c58735ea31c8d1f0e201a26cf6eb4cbf821d337bab9ff188966ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:94e15b7fa5777a129cae0bb1bf827d6c65bb18ffa618174f11ba41a54a7c6afa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.2 MB (378199721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409ae902066139831a8551310b2b7f6553e3b65a61dcffc6abd9ebe740cd02da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:19:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 15 May 2020 20:19:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 15 May 2020 20:19:26 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2020 20:20:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 15 May 2020 20:20:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:21:01 GMT
RUN npm install -g rtlcss
# Fri, 15 May 2020 20:21:01 GMT
ENV ODOO_VERSION=13.0
# Fri, 15 May 2020 20:21:02 GMT
ARG ODOO_RELEASE=20200417
# Fri, 15 May 2020 20:21:02 GMT
ARG ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
# Fri, 15 May 2020 20:22:17 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 May 2020 20:22:19 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 15 May 2020 20:22:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 May 2020 20:22:21 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 May 2020 20:22:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 May 2020 20:22:21 GMT
EXPOSE 8069 8071 8072
# Fri, 15 May 2020 20:22:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 May 2020 20:22:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 May 2020 20:22:22 GMT
USER odoo
# Fri, 15 May 2020 20:22:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2020 20:22:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52d64be975861953e3df408f6d5cdbb4dd1f35ca71ec1caa1c24f09f4c53539`  
		Last Modified: Fri, 15 May 2020 20:29:04 GMT  
		Size: 204.1 MB (204071234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00e3d4596d01b1640988262076b866c1f9986b4d04d43739404a9292ff39aca`  
		Last Modified: Fri, 15 May 2020 20:28:06 GMT  
		Size: 2.3 MB (2335364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edee5ebccdc5dafffcd58f9769c354aef5a3d264d4e2dd907c9d6556a5071fc`  
		Last Modified: Fri, 15 May 2020 20:28:06 GMT  
		Size: 1.1 MB (1094675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd33e1aab81e0590635a9f659f342e489cb74e1786dc0c7e6d4c8296e9f06575`  
		Last Modified: Fri, 15 May 2020 20:29:24 GMT  
		Size: 143.6 MB (143597287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44a49b61f65cb22cd0903df49505070078d5951d27340ed25fbdbe88165bf4a`  
		Last Modified: Fri, 15 May 2020 20:28:04 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2abae9e35fd9e877f8cd76409f87d2187144c2c56aab656d00b4951c59c609`  
		Last Modified: Fri, 15 May 2020 20:28:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e481d9423ad02973698607d85859b7118ad155dec2fe5dc97bba50c72ba55a77`  
		Last Modified: Fri, 15 May 2020 20:28:04 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73988fb7f4af2e77f9f3586d36895c311ea3a5e3f650635d72d953e997787c86`  
		Last Modified: Fri, 15 May 2020 20:28:04 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:9f8fd5de111c58735ea31c8d1f0e201a26cf6eb4cbf821d337bab9ff188966ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:94e15b7fa5777a129cae0bb1bf827d6c65bb18ffa618174f11ba41a54a7c6afa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.2 MB (378199721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409ae902066139831a8551310b2b7f6553e3b65a61dcffc6abd9ebe740cd02da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:19:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 15 May 2020 20:19:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 15 May 2020 20:19:26 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2020 20:20:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 15 May 2020 20:20:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:21:01 GMT
RUN npm install -g rtlcss
# Fri, 15 May 2020 20:21:01 GMT
ENV ODOO_VERSION=13.0
# Fri, 15 May 2020 20:21:02 GMT
ARG ODOO_RELEASE=20200417
# Fri, 15 May 2020 20:21:02 GMT
ARG ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
# Fri, 15 May 2020 20:22:17 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 May 2020 20:22:19 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 15 May 2020 20:22:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 May 2020 20:22:21 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 May 2020 20:22:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 May 2020 20:22:21 GMT
EXPOSE 8069 8071 8072
# Fri, 15 May 2020 20:22:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 May 2020 20:22:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 May 2020 20:22:22 GMT
USER odoo
# Fri, 15 May 2020 20:22:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2020 20:22:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52d64be975861953e3df408f6d5cdbb4dd1f35ca71ec1caa1c24f09f4c53539`  
		Last Modified: Fri, 15 May 2020 20:29:04 GMT  
		Size: 204.1 MB (204071234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00e3d4596d01b1640988262076b866c1f9986b4d04d43739404a9292ff39aca`  
		Last Modified: Fri, 15 May 2020 20:28:06 GMT  
		Size: 2.3 MB (2335364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edee5ebccdc5dafffcd58f9769c354aef5a3d264d4e2dd907c9d6556a5071fc`  
		Last Modified: Fri, 15 May 2020 20:28:06 GMT  
		Size: 1.1 MB (1094675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd33e1aab81e0590635a9f659f342e489cb74e1786dc0c7e6d4c8296e9f06575`  
		Last Modified: Fri, 15 May 2020 20:29:24 GMT  
		Size: 143.6 MB (143597287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44a49b61f65cb22cd0903df49505070078d5951d27340ed25fbdbe88165bf4a`  
		Last Modified: Fri, 15 May 2020 20:28:04 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2abae9e35fd9e877f8cd76409f87d2187144c2c56aab656d00b4951c59c609`  
		Last Modified: Fri, 15 May 2020 20:28:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e481d9423ad02973698607d85859b7118ad155dec2fe5dc97bba50c72ba55a77`  
		Last Modified: Fri, 15 May 2020 20:28:04 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73988fb7f4af2e77f9f3586d36895c311ea3a5e3f650635d72d953e997787c86`  
		Last Modified: Fri, 15 May 2020 20:28:04 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:9f8fd5de111c58735ea31c8d1f0e201a26cf6eb4cbf821d337bab9ff188966ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:94e15b7fa5777a129cae0bb1bf827d6c65bb18ffa618174f11ba41a54a7c6afa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.2 MB (378199721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409ae902066139831a8551310b2b7f6553e3b65a61dcffc6abd9ebe740cd02da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:19:25 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 15 May 2020 20:19:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 15 May 2020 20:19:26 GMT
ENV LANG=C.UTF-8
# Fri, 15 May 2020 20:20:47 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 15 May 2020 20:20:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:21:01 GMT
RUN npm install -g rtlcss
# Fri, 15 May 2020 20:21:01 GMT
ENV ODOO_VERSION=13.0
# Fri, 15 May 2020 20:21:02 GMT
ARG ODOO_RELEASE=20200417
# Fri, 15 May 2020 20:21:02 GMT
ARG ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
# Fri, 15 May 2020 20:22:17 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 15 May 2020 20:22:19 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Fri, 15 May 2020 20:22:19 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 15 May 2020 20:22:21 GMT
# ARGS: ODOO_RELEASE=20200417 ODOO_SHA=db29fbcebf63f9f656e9445f462190ac775ee533
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 15 May 2020 20:22:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 15 May 2020 20:22:21 GMT
EXPOSE 8069 8071 8072
# Fri, 15 May 2020 20:22:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 15 May 2020 20:22:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 15 May 2020 20:22:22 GMT
USER odoo
# Fri, 15 May 2020 20:22:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2020 20:22:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52d64be975861953e3df408f6d5cdbb4dd1f35ca71ec1caa1c24f09f4c53539`  
		Last Modified: Fri, 15 May 2020 20:29:04 GMT  
		Size: 204.1 MB (204071234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00e3d4596d01b1640988262076b866c1f9986b4d04d43739404a9292ff39aca`  
		Last Modified: Fri, 15 May 2020 20:28:06 GMT  
		Size: 2.3 MB (2335364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6edee5ebccdc5dafffcd58f9769c354aef5a3d264d4e2dd907c9d6556a5071fc`  
		Last Modified: Fri, 15 May 2020 20:28:06 GMT  
		Size: 1.1 MB (1094675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd33e1aab81e0590635a9f659f342e489cb74e1786dc0c7e6d4c8296e9f06575`  
		Last Modified: Fri, 15 May 2020 20:29:24 GMT  
		Size: 143.6 MB (143597287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44a49b61f65cb22cd0903df49505070078d5951d27340ed25fbdbe88165bf4a`  
		Last Modified: Fri, 15 May 2020 20:28:04 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2abae9e35fd9e877f8cd76409f87d2187144c2c56aab656d00b4951c59c609`  
		Last Modified: Fri, 15 May 2020 20:28:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e481d9423ad02973698607d85859b7118ad155dec2fe5dc97bba50c72ba55a77`  
		Last Modified: Fri, 15 May 2020 20:28:04 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73988fb7f4af2e77f9f3586d36895c311ea3a5e3f650635d72d953e997787c86`  
		Last Modified: Fri, 15 May 2020 20:28:04 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
