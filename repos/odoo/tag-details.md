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
$ docker pull odoo@sha256:1f872668e6eff572ae8834a1edee4ea7dc2c48f345f71887981e1f9c02b3df21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:a7616d1e0ed387855c50cd6ef7ff2227f9f3944616dbfe12871a5af32b464661
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396683714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3caeb9b2751e3ecd4386a33e6f6932cac1411459110229e76cc412c1ecf0d0a`
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
# Mon, 12 Oct 2020 22:39:24 GMT
ARG ODOO_RELEASE=20201012
# Mon, 12 Oct 2020 22:39:25 GMT
ARG ODOO_SHA=0d5aa5f1d0249863b04c06a5cb8ec8587ac522da
# Mon, 12 Oct 2020 22:40:25 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=0d5aa5f1d0249863b04c06a5cb8ec8587ac522da
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 12 Oct 2020 22:40:26 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 12 Oct 2020 22:40:26 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 12 Oct 2020 22:40:27 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=0d5aa5f1d0249863b04c06a5cb8ec8587ac522da
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 12 Oct 2020 22:40:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Oct 2020 22:40:28 GMT
EXPOSE 8069 8071 8072
# Mon, 12 Oct 2020 22:40:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Oct 2020 22:40:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 12 Oct 2020 22:40:29 GMT
USER odoo
# Mon, 12 Oct 2020 22:40:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Oct 2020 22:40:31 GMT
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
	-	`sha256:f3039b768157bba6bc99087842537910814ce879050a5f40e542e4c1ef7c9c39`  
		Last Modified: Mon, 12 Oct 2020 22:45:13 GMT  
		Size: 130.0 MB (129955072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b344f374b777434c12d43cc05e1582f0fdb13b9ca2ba4de1b4cd9091fe23ae7e`  
		Last Modified: Mon, 12 Oct 2020 22:43:50 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e672f9abac1572f9e445272c31b152853ae9144225c4873432c4c511bc95447`  
		Last Modified: Mon, 12 Oct 2020 22:43:50 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd368d45183d28fb25ad12cb8c61d72c99641448faa9e059edf9e94d1e703bf`  
		Last Modified: Mon, 12 Oct 2020 22:43:50 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debea683261d803e3c95c68b2119f734350305a72b7060a044cb08827a73638f`  
		Last Modified: Mon, 12 Oct 2020 22:43:50 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:1f872668e6eff572ae8834a1edee4ea7dc2c48f345f71887981e1f9c02b3df21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:a7616d1e0ed387855c50cd6ef7ff2227f9f3944616dbfe12871a5af32b464661
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396683714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3caeb9b2751e3ecd4386a33e6f6932cac1411459110229e76cc412c1ecf0d0a`
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
# Mon, 12 Oct 2020 22:39:24 GMT
ARG ODOO_RELEASE=20201012
# Mon, 12 Oct 2020 22:39:25 GMT
ARG ODOO_SHA=0d5aa5f1d0249863b04c06a5cb8ec8587ac522da
# Mon, 12 Oct 2020 22:40:25 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=0d5aa5f1d0249863b04c06a5cb8ec8587ac522da
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 12 Oct 2020 22:40:26 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 12 Oct 2020 22:40:26 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 12 Oct 2020 22:40:27 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=0d5aa5f1d0249863b04c06a5cb8ec8587ac522da
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 12 Oct 2020 22:40:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Oct 2020 22:40:28 GMT
EXPOSE 8069 8071 8072
# Mon, 12 Oct 2020 22:40:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Oct 2020 22:40:28 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 12 Oct 2020 22:40:29 GMT
USER odoo
# Mon, 12 Oct 2020 22:40:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Oct 2020 22:40:31 GMT
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
	-	`sha256:f3039b768157bba6bc99087842537910814ce879050a5f40e542e4c1ef7c9c39`  
		Last Modified: Mon, 12 Oct 2020 22:45:13 GMT  
		Size: 130.0 MB (129955072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b344f374b777434c12d43cc05e1582f0fdb13b9ca2ba4de1b4cd9091fe23ae7e`  
		Last Modified: Mon, 12 Oct 2020 22:43:50 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e672f9abac1572f9e445272c31b152853ae9144225c4873432c4c511bc95447`  
		Last Modified: Mon, 12 Oct 2020 22:43:50 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd368d45183d28fb25ad12cb8c61d72c99641448faa9e059edf9e94d1e703bf`  
		Last Modified: Mon, 12 Oct 2020 22:43:50 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debea683261d803e3c95c68b2119f734350305a72b7060a044cb08827a73638f`  
		Last Modified: Mon, 12 Oct 2020 22:43:50 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:666a1276a08e96282b0b8240d0ea5428de5d7b584fe6ed0212e794382868f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:c7b216ae446c242c2002ccddf553dfe941b439489e6ae5e7c54185cf5f88a52e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 MB (382802183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9366d508e0de60227a8dd401d60709ea0647c90b1a6248f6015b2a42f0a44c09`
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
# Mon, 12 Oct 2020 22:38:08 GMT
ARG ODOO_RELEASE=20201012
# Mon, 12 Oct 2020 22:38:08 GMT
ARG ODOO_SHA=30bfb107a331975c09c73faeac692993313515b4
# Mon, 12 Oct 2020 22:39:08 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=30bfb107a331975c09c73faeac692993313515b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 12 Oct 2020 22:39:10 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 12 Oct 2020 22:39:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 12 Oct 2020 22:39:11 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=30bfb107a331975c09c73faeac692993313515b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 12 Oct 2020 22:39:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Oct 2020 22:39:11 GMT
EXPOSE 8069 8071 8072
# Mon, 12 Oct 2020 22:39:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Oct 2020 22:39:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 12 Oct 2020 22:39:12 GMT
USER odoo
# Mon, 12 Oct 2020 22:39:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Oct 2020 22:39:12 GMT
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
	-	`sha256:d14f9b14e05c22b156bfd471c99ee8002e06af533415694c5dbdf959baf4613e`  
		Last Modified: Mon, 12 Oct 2020 22:43:45 GMT  
		Size: 148.2 MB (148214534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd660a050ef412ce9bcfc8a30e6b3d53abf7b557772d58a6f5e17bd6c8ceb982`  
		Last Modified: Mon, 12 Oct 2020 22:41:27 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16178e023a19e91a0960caf22bc0cf24b73400068b07b54633db62e1ff0db018`  
		Last Modified: Mon, 12 Oct 2020 22:41:27 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e24991bff5864fb09afcfba703bc5c4d5751906161e90a41a548df4391f700`  
		Last Modified: Mon, 12 Oct 2020 22:41:27 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8606db0187a600861b7b6dce05831fd7e949efb109130521a876916af5dd862c`  
		Last Modified: Mon, 12 Oct 2020 22:41:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:666a1276a08e96282b0b8240d0ea5428de5d7b584fe6ed0212e794382868f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:c7b216ae446c242c2002ccddf553dfe941b439489e6ae5e7c54185cf5f88a52e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 MB (382802183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9366d508e0de60227a8dd401d60709ea0647c90b1a6248f6015b2a42f0a44c09`
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
# Mon, 12 Oct 2020 22:38:08 GMT
ARG ODOO_RELEASE=20201012
# Mon, 12 Oct 2020 22:38:08 GMT
ARG ODOO_SHA=30bfb107a331975c09c73faeac692993313515b4
# Mon, 12 Oct 2020 22:39:08 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=30bfb107a331975c09c73faeac692993313515b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 12 Oct 2020 22:39:10 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 12 Oct 2020 22:39:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 12 Oct 2020 22:39:11 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=30bfb107a331975c09c73faeac692993313515b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 12 Oct 2020 22:39:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Oct 2020 22:39:11 GMT
EXPOSE 8069 8071 8072
# Mon, 12 Oct 2020 22:39:11 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Oct 2020 22:39:11 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 12 Oct 2020 22:39:12 GMT
USER odoo
# Mon, 12 Oct 2020 22:39:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Oct 2020 22:39:12 GMT
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
	-	`sha256:d14f9b14e05c22b156bfd471c99ee8002e06af533415694c5dbdf959baf4613e`  
		Last Modified: Mon, 12 Oct 2020 22:43:45 GMT  
		Size: 148.2 MB (148214534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd660a050ef412ce9bcfc8a30e6b3d53abf7b557772d58a6f5e17bd6c8ceb982`  
		Last Modified: Mon, 12 Oct 2020 22:41:27 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16178e023a19e91a0960caf22bc0cf24b73400068b07b54633db62e1ff0db018`  
		Last Modified: Mon, 12 Oct 2020 22:41:27 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e24991bff5864fb09afcfba703bc5c4d5751906161e90a41a548df4391f700`  
		Last Modified: Mon, 12 Oct 2020 22:41:27 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8606db0187a600861b7b6dce05831fd7e949efb109130521a876916af5dd862c`  
		Last Modified: Mon, 12 Oct 2020 22:41:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14`

```console
$ docker pull odoo@sha256:2b70ff61b306e6693895f464c4d8b0436221081d8983ebb18e4a697b1fe7b3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:cc639d769299844ae6d1899166bebf2613791aadf06e573dc18535cec4a27e85
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389747666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178220d443cb5ae74e6b54534252ca81678d29ed1cb5595dbe773f956928ca7b`
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
# Fri, 02 Oct 2020 21:39:15 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb     && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Oct 2020 21:39:24 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Oct 2020 21:39:28 GMT
RUN npm install -g rtlcss
# Fri, 02 Oct 2020 21:39:28 GMT
ENV ODOO_VERSION=14.0
# Mon, 12 Oct 2020 22:37:03 GMT
ARG ODOO_RELEASE=20201012
# Mon, 12 Oct 2020 22:37:03 GMT
ARG ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
# Mon, 12 Oct 2020 22:37:53 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 12 Oct 2020 22:37:54 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 12 Oct 2020 22:37:54 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 12 Oct 2020 22:37:55 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 12 Oct 2020 22:37:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Oct 2020 22:37:55 GMT
EXPOSE 8069 8071 8072
# Mon, 12 Oct 2020 22:37:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Oct 2020 22:37:56 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 12 Oct 2020 22:37:56 GMT
USER odoo
# Mon, 12 Oct 2020 22:37:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Oct 2020 22:37:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918cd4aaeb69f3c828531962c0a4f69cbab65f3d22c4289db77087aa80581735`  
		Last Modified: Fri, 02 Oct 2020 21:45:39 GMT  
		Size: 210.1 MB (210103756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28fcced63569e31089b82f73fbfea1199b4041d35b97dfc63c59a8d5c8e631b`  
		Last Modified: Fri, 02 Oct 2020 21:44:39 GMT  
		Size: 2.4 MB (2435828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955db14828467740f3a3a069d5a2cb95a3823644a018c5b5aa1fd49ae7fcdb7d`  
		Last Modified: Fri, 02 Oct 2020 21:44:39 GMT  
		Size: 1.1 MB (1111094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93681d141bc828dae4ade726c7c123f3e19449c8fa11a2adde2c05a96fcc3392`  
		Last Modified: Mon, 12 Oct 2020 22:41:22 GMT  
		Size: 149.0 MB (149002426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead6063a98e9d3f64e8d0de8b7650107a1c0de40aaaaa984a4166359cecad981`  
		Last Modified: Mon, 12 Oct 2020 22:40:47 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b31909a205ec55c2e519515ee964d6206e654a95fe2e6109d4ad9beaa05b0`  
		Last Modified: Mon, 12 Oct 2020 22:40:47 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f96a4f181b4e9078c2bf22b318743fd04b5f1074457f1023c0cba962b04139`  
		Last Modified: Mon, 12 Oct 2020 22:40:47 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1966e4c708d5fc76034157128321885ccb607d60bacbd2124517ae0ef791aad`  
		Last Modified: Mon, 12 Oct 2020 22:40:47 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:2b70ff61b306e6693895f464c4d8b0436221081d8983ebb18e4a697b1fe7b3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:cc639d769299844ae6d1899166bebf2613791aadf06e573dc18535cec4a27e85
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389747666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178220d443cb5ae74e6b54534252ca81678d29ed1cb5595dbe773f956928ca7b`
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
# Fri, 02 Oct 2020 21:39:15 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb     && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Oct 2020 21:39:24 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Oct 2020 21:39:28 GMT
RUN npm install -g rtlcss
# Fri, 02 Oct 2020 21:39:28 GMT
ENV ODOO_VERSION=14.0
# Mon, 12 Oct 2020 22:37:03 GMT
ARG ODOO_RELEASE=20201012
# Mon, 12 Oct 2020 22:37:03 GMT
ARG ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
# Mon, 12 Oct 2020 22:37:53 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 12 Oct 2020 22:37:54 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 12 Oct 2020 22:37:54 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 12 Oct 2020 22:37:55 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 12 Oct 2020 22:37:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Oct 2020 22:37:55 GMT
EXPOSE 8069 8071 8072
# Mon, 12 Oct 2020 22:37:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Oct 2020 22:37:56 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 12 Oct 2020 22:37:56 GMT
USER odoo
# Mon, 12 Oct 2020 22:37:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Oct 2020 22:37:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918cd4aaeb69f3c828531962c0a4f69cbab65f3d22c4289db77087aa80581735`  
		Last Modified: Fri, 02 Oct 2020 21:45:39 GMT  
		Size: 210.1 MB (210103756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28fcced63569e31089b82f73fbfea1199b4041d35b97dfc63c59a8d5c8e631b`  
		Last Modified: Fri, 02 Oct 2020 21:44:39 GMT  
		Size: 2.4 MB (2435828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955db14828467740f3a3a069d5a2cb95a3823644a018c5b5aa1fd49ae7fcdb7d`  
		Last Modified: Fri, 02 Oct 2020 21:44:39 GMT  
		Size: 1.1 MB (1111094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93681d141bc828dae4ade726c7c123f3e19449c8fa11a2adde2c05a96fcc3392`  
		Last Modified: Mon, 12 Oct 2020 22:41:22 GMT  
		Size: 149.0 MB (149002426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead6063a98e9d3f64e8d0de8b7650107a1c0de40aaaaa984a4166359cecad981`  
		Last Modified: Mon, 12 Oct 2020 22:40:47 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b31909a205ec55c2e519515ee964d6206e654a95fe2e6109d4ad9beaa05b0`  
		Last Modified: Mon, 12 Oct 2020 22:40:47 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f96a4f181b4e9078c2bf22b318743fd04b5f1074457f1023c0cba962b04139`  
		Last Modified: Mon, 12 Oct 2020 22:40:47 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1966e4c708d5fc76034157128321885ccb607d60bacbd2124517ae0ef791aad`  
		Last Modified: Mon, 12 Oct 2020 22:40:47 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:2b70ff61b306e6693895f464c4d8b0436221081d8983ebb18e4a697b1fe7b3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:cc639d769299844ae6d1899166bebf2613791aadf06e573dc18535cec4a27e85
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389747666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178220d443cb5ae74e6b54534252ca81678d29ed1cb5595dbe773f956928ca7b`
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
# Fri, 02 Oct 2020 21:39:15 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb     && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 02 Oct 2020 21:39:24 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Oct 2020 21:39:28 GMT
RUN npm install -g rtlcss
# Fri, 02 Oct 2020 21:39:28 GMT
ENV ODOO_VERSION=14.0
# Mon, 12 Oct 2020 22:37:03 GMT
ARG ODOO_RELEASE=20201012
# Mon, 12 Oct 2020 22:37:03 GMT
ARG ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
# Mon, 12 Oct 2020 22:37:53 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 12 Oct 2020 22:37:54 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 12 Oct 2020 22:37:54 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 12 Oct 2020 22:37:55 GMT
# ARGS: ODOO_RELEASE=20201012 ODOO_SHA=3d559b066ee2fd8e5a84e8f00ad510dbf2e3df63
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 12 Oct 2020 22:37:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Oct 2020 22:37:55 GMT
EXPOSE 8069 8071 8072
# Mon, 12 Oct 2020 22:37:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Oct 2020 22:37:56 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 12 Oct 2020 22:37:56 GMT
USER odoo
# Mon, 12 Oct 2020 22:37:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Oct 2020 22:37:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918cd4aaeb69f3c828531962c0a4f69cbab65f3d22c4289db77087aa80581735`  
		Last Modified: Fri, 02 Oct 2020 21:45:39 GMT  
		Size: 210.1 MB (210103756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28fcced63569e31089b82f73fbfea1199b4041d35b97dfc63c59a8d5c8e631b`  
		Last Modified: Fri, 02 Oct 2020 21:44:39 GMT  
		Size: 2.4 MB (2435828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955db14828467740f3a3a069d5a2cb95a3823644a018c5b5aa1fd49ae7fcdb7d`  
		Last Modified: Fri, 02 Oct 2020 21:44:39 GMT  
		Size: 1.1 MB (1111094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93681d141bc828dae4ade726c7c123f3e19449c8fa11a2adde2c05a96fcc3392`  
		Last Modified: Mon, 12 Oct 2020 22:41:22 GMT  
		Size: 149.0 MB (149002426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead6063a98e9d3f64e8d0de8b7650107a1c0de40aaaaa984a4166359cecad981`  
		Last Modified: Mon, 12 Oct 2020 22:40:47 GMT  
		Size: 671.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8b31909a205ec55c2e519515ee964d6206e654a95fe2e6109d4ad9beaa05b0`  
		Last Modified: Mon, 12 Oct 2020 22:40:47 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f96a4f181b4e9078c2bf22b318743fd04b5f1074457f1023c0cba962b04139`  
		Last Modified: Mon, 12 Oct 2020 22:40:47 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1966e4c708d5fc76034157128321885ccb607d60bacbd2124517ae0ef791aad`  
		Last Modified: Mon, 12 Oct 2020 22:40:47 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
