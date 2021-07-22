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
$ docker pull odoo@sha256:a978d590fd370a584bf49ea256bd254ed745ade1aa48b0c801ad1ca39ddca6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:b0449dc8b6ab0a8b77ef7168a630cf180625cf4e141ebf344969a2b1c8d59126
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538386181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d805d9efba65fb5597e199ebeb6f3d4eb3510213585caff361e91ae92f2f7425`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:17 GMT
ADD file:55a25b93e8f2940a796f3cbf1e78bddf5f49c46b1b89b63b9b5673cbed9483ca in / 
# Thu, 22 Jul 2021 00:47:17 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:18:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 22 Jul 2021 14:18:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 22 Jul 2021 14:18:32 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:18:33 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 22 Jul 2021 14:19:56 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 22 Jul 2021 14:20:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:20:32 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:20:32 GMT
ENV ODOO_VERSION=12.0
# Thu, 22 Jul 2021 14:20:33 GMT
ARG ODOO_RELEASE=20210720
# Thu, 22 Jul 2021 14:20:33 GMT
ARG ODOO_SHA=a0f73c6f7dc916286fad189bc8f7f1cb814f8004
# Thu, 22 Jul 2021 14:21:39 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=a0f73c6f7dc916286fad189bc8f7f1cb814f8004
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 22 Jul 2021 14:21:40 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 22 Jul 2021 14:21:41 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 22 Jul 2021 14:21:41 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=a0f73c6f7dc916286fad189bc8f7f1cb814f8004
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 22 Jul 2021 14:21:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 22 Jul 2021 14:21:42 GMT
EXPOSE 8069 8071 8072
# Thu, 22 Jul 2021 14:21:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 22 Jul 2021 14:21:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 22 Jul 2021 14:21:43 GMT
USER odoo
# Thu, 22 Jul 2021 14:21:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jul 2021 14:21:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:778066204fb734c2fb80cb8127cb35d67d742806a4eaf1aba0b5393c4ae6f2a4`  
		Last Modified: Thu, 22 Jul 2021 00:53:22 GMT  
		Size: 22.5 MB (22527428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b204c7c8cc64bad523e886289c004fd49d89dca323966ac1b4e5988913eb92d`  
		Last Modified: Thu, 22 Jul 2021 14:23:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a9d0cb1723e7198eb716a0778314c493ea467b36143cbbe4b40c67b5d24ef9`  
		Last Modified: Thu, 22 Jul 2021 14:24:37 GMT  
		Size: 219.7 MB (219659230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624c7e60f85c5692a09efe6c44024a23d733d0bd828c8dfeb35b2dfd358e8826`  
		Last Modified: Thu, 22 Jul 2021 14:23:56 GMT  
		Size: 2.2 MB (2224668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfabe6def0f67df43daa7647f45a0a3ebf687d388c5beff7b0027c3e45d3e87d`  
		Last Modified: Thu, 22 Jul 2021 14:24:04 GMT  
		Size: 22.0 MB (22027409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7776ba46ce5b0370aea755176bdd0b1c8e41c54c556c6a94803f220ff712890`  
		Last Modified: Thu, 22 Jul 2021 14:24:42 GMT  
		Size: 271.9 MB (271944790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743a1544773cfa1d2d50a8633ec2eca41145dd58f40f0eaaa57416581e41712d`  
		Last Modified: Thu, 22 Jul 2021 14:23:53 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf90749a5ada8352a2420bbfe47a532699adf8630107d99ee66aa20f8e13944`  
		Last Modified: Thu, 22 Jul 2021 14:23:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96dfded1613a1aacfa6180fc2b6733d96fc46cf46c4c206fe6239a6ec4a00fa6`  
		Last Modified: Thu, 22 Jul 2021 14:23:53 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491b7829636da5c28b03bac3af152b45fde73893ec620dd7e18f560be7e221e7`  
		Last Modified: Thu, 22 Jul 2021 14:23:53 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:a978d590fd370a584bf49ea256bd254ed745ade1aa48b0c801ad1ca39ddca6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:b0449dc8b6ab0a8b77ef7168a630cf180625cf4e141ebf344969a2b1c8d59126
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.4 MB (538386181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d805d9efba65fb5597e199ebeb6f3d4eb3510213585caff361e91ae92f2f7425`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:17 GMT
ADD file:55a25b93e8f2940a796f3cbf1e78bddf5f49c46b1b89b63b9b5673cbed9483ca in / 
# Thu, 22 Jul 2021 00:47:17 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:18:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 22 Jul 2021 14:18:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 22 Jul 2021 14:18:32 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:18:33 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 22 Jul 2021 14:19:56 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 22 Jul 2021 14:20:12 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:20:32 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:20:32 GMT
ENV ODOO_VERSION=12.0
# Thu, 22 Jul 2021 14:20:33 GMT
ARG ODOO_RELEASE=20210720
# Thu, 22 Jul 2021 14:20:33 GMT
ARG ODOO_SHA=a0f73c6f7dc916286fad189bc8f7f1cb814f8004
# Thu, 22 Jul 2021 14:21:39 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=a0f73c6f7dc916286fad189bc8f7f1cb814f8004
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 22 Jul 2021 14:21:40 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 22 Jul 2021 14:21:41 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 22 Jul 2021 14:21:41 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=a0f73c6f7dc916286fad189bc8f7f1cb814f8004
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 22 Jul 2021 14:21:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 22 Jul 2021 14:21:42 GMT
EXPOSE 8069 8071 8072
# Thu, 22 Jul 2021 14:21:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 22 Jul 2021 14:21:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 22 Jul 2021 14:21:43 GMT
USER odoo
# Thu, 22 Jul 2021 14:21:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jul 2021 14:21:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:778066204fb734c2fb80cb8127cb35d67d742806a4eaf1aba0b5393c4ae6f2a4`  
		Last Modified: Thu, 22 Jul 2021 00:53:22 GMT  
		Size: 22.5 MB (22527428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b204c7c8cc64bad523e886289c004fd49d89dca323966ac1b4e5988913eb92d`  
		Last Modified: Thu, 22 Jul 2021 14:23:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a9d0cb1723e7198eb716a0778314c493ea467b36143cbbe4b40c67b5d24ef9`  
		Last Modified: Thu, 22 Jul 2021 14:24:37 GMT  
		Size: 219.7 MB (219659230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624c7e60f85c5692a09efe6c44024a23d733d0bd828c8dfeb35b2dfd358e8826`  
		Last Modified: Thu, 22 Jul 2021 14:23:56 GMT  
		Size: 2.2 MB (2224668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfabe6def0f67df43daa7647f45a0a3ebf687d388c5beff7b0027c3e45d3e87d`  
		Last Modified: Thu, 22 Jul 2021 14:24:04 GMT  
		Size: 22.0 MB (22027409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7776ba46ce5b0370aea755176bdd0b1c8e41c54c556c6a94803f220ff712890`  
		Last Modified: Thu, 22 Jul 2021 14:24:42 GMT  
		Size: 271.9 MB (271944790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743a1544773cfa1d2d50a8633ec2eca41145dd58f40f0eaaa57416581e41712d`  
		Last Modified: Thu, 22 Jul 2021 14:23:53 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf90749a5ada8352a2420bbfe47a532699adf8630107d99ee66aa20f8e13944`  
		Last Modified: Thu, 22 Jul 2021 14:23:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96dfded1613a1aacfa6180fc2b6733d96fc46cf46c4c206fe6239a6ec4a00fa6`  
		Last Modified: Thu, 22 Jul 2021 14:23:53 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491b7829636da5c28b03bac3af152b45fde73893ec620dd7e18f560be7e221e7`  
		Last Modified: Thu, 22 Jul 2021 14:23:53 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:5668bbce904386068ec5f75c5d78884a6234ed6711155925599c1d13754138d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:2799ded84ce458095d3f4265615f594e96a6ec860f951fc9be81d43e57ae4178
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.3 MB (528312857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a300e0d44d10ebc58d77bc94e9d28dae29ff7b4c9204ca0cfe40b5e5a1386a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:12:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 22 Jul 2021 14:12:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 22 Jul 2021 14:12:41 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:16:50 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 22 Jul 2021 14:16:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:17:00 GMT
RUN npm install -g rtlcss
# Thu, 22 Jul 2021 14:17:00 GMT
ENV ODOO_VERSION=13.0
# Thu, 22 Jul 2021 14:17:00 GMT
ARG ODOO_RELEASE=20210720
# Thu, 22 Jul 2021 14:17:01 GMT
ARG ODOO_SHA=745f9d176fbe0a5f91459b8c89788ffde3bef476
# Thu, 22 Jul 2021 14:18:11 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=745f9d176fbe0a5f91459b8c89788ffde3bef476
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 22 Jul 2021 14:18:15 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 22 Jul 2021 14:18:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 22 Jul 2021 14:18:16 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=745f9d176fbe0a5f91459b8c89788ffde3bef476
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 22 Jul 2021 14:18:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 22 Jul 2021 14:18:16 GMT
EXPOSE 8069 8071 8072
# Thu, 22 Jul 2021 14:18:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 22 Jul 2021 14:18:17 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 22 Jul 2021 14:18:17 GMT
USER odoo
# Thu, 22 Jul 2021 14:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jul 2021 14:18:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8f3448dc635b32fd797faa7bd97abefb346d7a902095935c8e04f0f812bc8f`  
		Last Modified: Thu, 22 Jul 2021 14:23:34 GMT  
		Size: 207.1 MB (207125538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0bd24a54815ae14a888a2249982adc5e9d299f05ed362a896126ee25260548`  
		Last Modified: Thu, 22 Jul 2021 14:23:04 GMT  
		Size: 2.3 MB (2346808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a989fd222f0a84e1300dabf83f0d7f45734b16639a552c9d6849bcb0a84dd8c5`  
		Last Modified: Thu, 22 Jul 2021 14:23:04 GMT  
		Size: 889.1 KB (889054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730811cd8fd11e5786fa8ea74a9910a6b0ba10d9a2a47f5427b002bc8ca3d70e`  
		Last Modified: Thu, 22 Jul 2021 14:23:41 GMT  
		Size: 290.8 MB (290803234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c54bc016cf1b2bfc7e440f77affa95fbcdc61846f1ee3ffc846ad4a26c10393`  
		Last Modified: Thu, 22 Jul 2021 14:23:01 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634bb541e8f82b649345836f70f65c2886d6e1db09af8ff20f11472ef8c5d52f`  
		Last Modified: Thu, 22 Jul 2021 14:23:01 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8017f40ee96cb725496dd8e457a3900e9d5ca0ff3ec25264e9b6af049b41fc`  
		Last Modified: Thu, 22 Jul 2021 14:23:01 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612fd7549f3fd9109f8912f598119086822b38224bbce9d5d4afeaa62ad7f777`  
		Last Modified: Thu, 22 Jul 2021 14:23:01 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:5668bbce904386068ec5f75c5d78884a6234ed6711155925599c1d13754138d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:2799ded84ce458095d3f4265615f594e96a6ec860f951fc9be81d43e57ae4178
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.3 MB (528312857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a300e0d44d10ebc58d77bc94e9d28dae29ff7b4c9204ca0cfe40b5e5a1386a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:12:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 22 Jul 2021 14:12:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 22 Jul 2021 14:12:41 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:16:50 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb         && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 22 Jul 2021 14:16:57 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:17:00 GMT
RUN npm install -g rtlcss
# Thu, 22 Jul 2021 14:17:00 GMT
ENV ODOO_VERSION=13.0
# Thu, 22 Jul 2021 14:17:00 GMT
ARG ODOO_RELEASE=20210720
# Thu, 22 Jul 2021 14:17:01 GMT
ARG ODOO_SHA=745f9d176fbe0a5f91459b8c89788ffde3bef476
# Thu, 22 Jul 2021 14:18:11 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=745f9d176fbe0a5f91459b8c89788ffde3bef476
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 22 Jul 2021 14:18:15 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 22 Jul 2021 14:18:15 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 22 Jul 2021 14:18:16 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=745f9d176fbe0a5f91459b8c89788ffde3bef476
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 22 Jul 2021 14:18:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 22 Jul 2021 14:18:16 GMT
EXPOSE 8069 8071 8072
# Thu, 22 Jul 2021 14:18:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 22 Jul 2021 14:18:17 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 22 Jul 2021 14:18:17 GMT
USER odoo
# Thu, 22 Jul 2021 14:18:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jul 2021 14:18:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8f3448dc635b32fd797faa7bd97abefb346d7a902095935c8e04f0f812bc8f`  
		Last Modified: Thu, 22 Jul 2021 14:23:34 GMT  
		Size: 207.1 MB (207125538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0bd24a54815ae14a888a2249982adc5e9d299f05ed362a896126ee25260548`  
		Last Modified: Thu, 22 Jul 2021 14:23:04 GMT  
		Size: 2.3 MB (2346808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a989fd222f0a84e1300dabf83f0d7f45734b16639a552c9d6849bcb0a84dd8c5`  
		Last Modified: Thu, 22 Jul 2021 14:23:04 GMT  
		Size: 889.1 KB (889054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730811cd8fd11e5786fa8ea74a9910a6b0ba10d9a2a47f5427b002bc8ca3d70e`  
		Last Modified: Thu, 22 Jul 2021 14:23:41 GMT  
		Size: 290.8 MB (290803234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c54bc016cf1b2bfc7e440f77affa95fbcdc61846f1ee3ffc846ad4a26c10393`  
		Last Modified: Thu, 22 Jul 2021 14:23:01 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634bb541e8f82b649345836f70f65c2886d6e1db09af8ff20f11472ef8c5d52f`  
		Last Modified: Thu, 22 Jul 2021 14:23:01 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8017f40ee96cb725496dd8e457a3900e9d5ca0ff3ec25264e9b6af049b41fc`  
		Last Modified: Thu, 22 Jul 2021 14:23:01 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612fd7549f3fd9109f8912f598119086822b38224bbce9d5d4afeaa62ad7f777`  
		Last Modified: Thu, 22 Jul 2021 14:23:01 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:a27c258e2d0b73f8af3460a0d056bea1874679eb733ee1ad48b80312e1f7a77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:14eb922dfd65ba13c5ee6206d35de63b1c37390de420a7f1c75b5839925b0e7d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.6 MB (516571876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a622ba09ca0ec67573cdb892210033c6aa3f7e522d3b9ed543b13c866c8bf77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:12:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 22 Jul 2021 14:12:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 22 Jul 2021 14:12:41 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:14:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 22 Jul 2021 14:14:14 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:14:17 GMT
RUN npm install -g rtlcss
# Thu, 22 Jul 2021 14:14:18 GMT
ENV ODOO_VERSION=14.0
# Thu, 22 Jul 2021 14:14:18 GMT
ARG ODOO_RELEASE=20210720
# Thu, 22 Jul 2021 14:14:18 GMT
ARG ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
# Thu, 22 Jul 2021 14:15:29 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 22 Jul 2021 14:15:33 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 22 Jul 2021 14:15:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 22 Jul 2021 14:15:34 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 22 Jul 2021 14:15:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 22 Jul 2021 14:15:35 GMT
EXPOSE 8069 8071 8072
# Thu, 22 Jul 2021 14:15:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 22 Jul 2021 14:15:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 22 Jul 2021 14:15:35 GMT
USER odoo
# Thu, 22 Jul 2021 14:15:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jul 2021 14:15:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5502f02c83eb9a5d2610c8d0caea8b6d8645db289895c5071886b9231f40ac51`  
		Last Modified: Thu, 22 Jul 2021 14:22:40 GMT  
		Size: 213.2 MB (213172386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a9b423102589afe08dee7c8ee26abe30dce0b452950ca9eb03c425cf098c16`  
		Last Modified: Thu, 22 Jul 2021 14:22:17 GMT  
		Size: 2.3 MB (2349817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62bb0f68ae1402800683d9694dc8f338be4ac729f14a2e24d738f4aa12ea7e6`  
		Last Modified: Thu, 22 Jul 2021 14:22:14 GMT  
		Size: 889.3 KB (889257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb65718bd5e3f1c1bb871ad5f4994122924ff3662d74be1bd6a9e0176649b4e`  
		Last Modified: Thu, 22 Jul 2021 14:22:46 GMT  
		Size: 273.0 MB (273012190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df0c12a812f7f3caa325f459babefa4a34dd1a29b907194054b305f39b58d98`  
		Last Modified: Thu, 22 Jul 2021 14:22:11 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1f4840656a5ed310db0ab8e60a5637a9771dd6ef956d5c382b8cfb49334ec3`  
		Last Modified: Thu, 22 Jul 2021 14:22:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e650314c3551743b9acbc4c940b89521b3573e7017020ec65afbba385794a5c`  
		Last Modified: Thu, 22 Jul 2021 14:22:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cfe4eb055bc4a9b2089a0366ba845f02939106030911d8500b4d08e8f234c1`  
		Last Modified: Thu, 22 Jul 2021 14:22:10 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:a27c258e2d0b73f8af3460a0d056bea1874679eb733ee1ad48b80312e1f7a77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:14eb922dfd65ba13c5ee6206d35de63b1c37390de420a7f1c75b5839925b0e7d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.6 MB (516571876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a622ba09ca0ec67573cdb892210033c6aa3f7e522d3b9ed543b13c866c8bf77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:12:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 22 Jul 2021 14:12:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 22 Jul 2021 14:12:41 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:14:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 22 Jul 2021 14:14:14 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:14:17 GMT
RUN npm install -g rtlcss
# Thu, 22 Jul 2021 14:14:18 GMT
ENV ODOO_VERSION=14.0
# Thu, 22 Jul 2021 14:14:18 GMT
ARG ODOO_RELEASE=20210720
# Thu, 22 Jul 2021 14:14:18 GMT
ARG ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
# Thu, 22 Jul 2021 14:15:29 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 22 Jul 2021 14:15:33 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 22 Jul 2021 14:15:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 22 Jul 2021 14:15:34 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 22 Jul 2021 14:15:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 22 Jul 2021 14:15:35 GMT
EXPOSE 8069 8071 8072
# Thu, 22 Jul 2021 14:15:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 22 Jul 2021 14:15:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 22 Jul 2021 14:15:35 GMT
USER odoo
# Thu, 22 Jul 2021 14:15:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jul 2021 14:15:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5502f02c83eb9a5d2610c8d0caea8b6d8645db289895c5071886b9231f40ac51`  
		Last Modified: Thu, 22 Jul 2021 14:22:40 GMT  
		Size: 213.2 MB (213172386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a9b423102589afe08dee7c8ee26abe30dce0b452950ca9eb03c425cf098c16`  
		Last Modified: Thu, 22 Jul 2021 14:22:17 GMT  
		Size: 2.3 MB (2349817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62bb0f68ae1402800683d9694dc8f338be4ac729f14a2e24d738f4aa12ea7e6`  
		Last Modified: Thu, 22 Jul 2021 14:22:14 GMT  
		Size: 889.3 KB (889257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb65718bd5e3f1c1bb871ad5f4994122924ff3662d74be1bd6a9e0176649b4e`  
		Last Modified: Thu, 22 Jul 2021 14:22:46 GMT  
		Size: 273.0 MB (273012190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df0c12a812f7f3caa325f459babefa4a34dd1a29b907194054b305f39b58d98`  
		Last Modified: Thu, 22 Jul 2021 14:22:11 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1f4840656a5ed310db0ab8e60a5637a9771dd6ef956d5c382b8cfb49334ec3`  
		Last Modified: Thu, 22 Jul 2021 14:22:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e650314c3551743b9acbc4c940b89521b3573e7017020ec65afbba385794a5c`  
		Last Modified: Thu, 22 Jul 2021 14:22:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cfe4eb055bc4a9b2089a0366ba845f02939106030911d8500b4d08e8f234c1`  
		Last Modified: Thu, 22 Jul 2021 14:22:10 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:a27c258e2d0b73f8af3460a0d056bea1874679eb733ee1ad48b80312e1f7a77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:14eb922dfd65ba13c5ee6206d35de63b1c37390de420a7f1c75b5839925b0e7d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.6 MB (516571876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a622ba09ca0ec67573cdb892210033c6aa3f7e522d3b9ed543b13c866c8bf77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:12:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 22 Jul 2021 14:12:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 22 Jul 2021 14:12:41 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:14:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 22 Jul 2021 14:14:14 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:14:17 GMT
RUN npm install -g rtlcss
# Thu, 22 Jul 2021 14:14:18 GMT
ENV ODOO_VERSION=14.0
# Thu, 22 Jul 2021 14:14:18 GMT
ARG ODOO_RELEASE=20210720
# Thu, 22 Jul 2021 14:14:18 GMT
ARG ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
# Thu, 22 Jul 2021 14:15:29 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 22 Jul 2021 14:15:33 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 22 Jul 2021 14:15:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 22 Jul 2021 14:15:34 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 22 Jul 2021 14:15:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 22 Jul 2021 14:15:35 GMT
EXPOSE 8069 8071 8072
# Thu, 22 Jul 2021 14:15:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 22 Jul 2021 14:15:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 22 Jul 2021 14:15:35 GMT
USER odoo
# Thu, 22 Jul 2021 14:15:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jul 2021 14:15:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5502f02c83eb9a5d2610c8d0caea8b6d8645db289895c5071886b9231f40ac51`  
		Last Modified: Thu, 22 Jul 2021 14:22:40 GMT  
		Size: 213.2 MB (213172386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a9b423102589afe08dee7c8ee26abe30dce0b452950ca9eb03c425cf098c16`  
		Last Modified: Thu, 22 Jul 2021 14:22:17 GMT  
		Size: 2.3 MB (2349817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62bb0f68ae1402800683d9694dc8f338be4ac729f14a2e24d738f4aa12ea7e6`  
		Last Modified: Thu, 22 Jul 2021 14:22:14 GMT  
		Size: 889.3 KB (889257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb65718bd5e3f1c1bb871ad5f4994122924ff3662d74be1bd6a9e0176649b4e`  
		Last Modified: Thu, 22 Jul 2021 14:22:46 GMT  
		Size: 273.0 MB (273012190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df0c12a812f7f3caa325f459babefa4a34dd1a29b907194054b305f39b58d98`  
		Last Modified: Thu, 22 Jul 2021 14:22:11 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1f4840656a5ed310db0ab8e60a5637a9771dd6ef956d5c382b8cfb49334ec3`  
		Last Modified: Thu, 22 Jul 2021 14:22:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e650314c3551743b9acbc4c940b89521b3573e7017020ec65afbba385794a5c`  
		Last Modified: Thu, 22 Jul 2021 14:22:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cfe4eb055bc4a9b2089a0366ba845f02939106030911d8500b4d08e8f234c1`  
		Last Modified: Thu, 22 Jul 2021 14:22:10 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
