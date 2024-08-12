<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:15.0-20240812`](#odoo150-20240812)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20240812`](#odoo160-20240812)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20240812`](#odoo170-20240812)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:26e703eff34028d1482f54d3c81c5f87f7b5692d606d44105ae21c38dd85cc3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:8ecabdcea90195a3ebecaac64a9ba6127524f87d7d77ecee10d2393fa9c3f72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563993404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b830eb9ce929d064338ab867802fc24bef9fedcb814858fc3c4837f875ca1149`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=15.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: ODOO_RELEASE=20240812 ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: ODOO_RELEASE=20240812 ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025e01fa3710f6774b6eeac504f3b194083a72090484a40313e406d50fa63e8a`  
		Last Modified: Mon, 12 Aug 2024 16:58:30 GMT  
		Size: 220.3 MB (220282207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0ed1241c3538331bb3c51d20626b921da81bd911cf529087014c512c0b5ff3`  
		Last Modified: Mon, 12 Aug 2024 16:58:27 GMT  
		Size: 2.4 MB (2387738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f4e2657406381a48f441042947ac491a745749873dd15a912fd0451952f914`  
		Last Modified: Mon, 12 Aug 2024 16:58:27 GMT  
		Size: 463.8 KB (463808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b287d809f0865c9ea7ce75aebcf39e8d1ff3f18bfd8d0bf4b64eb9ece241aa3`  
		Last Modified: Mon, 12 Aug 2024 16:58:31 GMT  
		Size: 309.4 MB (309428886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76c54b095ac960507068f82e2f35910f6f4f0bafca431ab238b629783580a12`  
		Last Modified: Mon, 12 Aug 2024 16:58:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba7343fe5a15e88dd9ce8168c01293fe0b7715cbc1cf5c1dc7b6fbed47536c`  
		Last Modified: Mon, 12 Aug 2024 16:58:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85482987ef6aea510ad9ae884d1f4184ef4d8cde7f75206bb3c0b478536e4d07`  
		Last Modified: Mon, 12 Aug 2024 16:58:29 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6d6e4a4ea30ccdc88956c06483702d597b267181fe974006e1606f06a114c9`  
		Last Modified: Mon, 12 Aug 2024 16:58:29 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15` - unknown; unknown

```console
$ docker pull odoo@sha256:80c86d76772ca0b8b2d8bddfdb8577e49b04fda720c1732001bf6c110fcee8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cedaae3cc843c2365c0f105945e0e37434a6e89af97e4df78e974c8d4c190b4`

```dockerfile
```

-	Layers:
	-	`sha256:f55306717e1856428554d76caf3bfa347a85febcf8ac14fcb94c6f98ce76e997`  
		Last Modified: Mon, 12 Aug 2024 16:58:28 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b64d109379f701fe52f634dc16b98e6c79c26f768a12a2d9d3e5b5b81bc831b`  
		Last Modified: Mon, 12 Aug 2024 16:58:27 GMT  
		Size: 24.6 KB (24630 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0`

```console
$ docker pull odoo@sha256:26e703eff34028d1482f54d3c81c5f87f7b5692d606d44105ae21c38dd85cc3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:8ecabdcea90195a3ebecaac64a9ba6127524f87d7d77ecee10d2393fa9c3f72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563993404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b830eb9ce929d064338ab867802fc24bef9fedcb814858fc3c4837f875ca1149`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=15.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: ODOO_RELEASE=20240812 ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: ODOO_RELEASE=20240812 ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025e01fa3710f6774b6eeac504f3b194083a72090484a40313e406d50fa63e8a`  
		Last Modified: Mon, 12 Aug 2024 16:58:30 GMT  
		Size: 220.3 MB (220282207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0ed1241c3538331bb3c51d20626b921da81bd911cf529087014c512c0b5ff3`  
		Last Modified: Mon, 12 Aug 2024 16:58:27 GMT  
		Size: 2.4 MB (2387738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f4e2657406381a48f441042947ac491a745749873dd15a912fd0451952f914`  
		Last Modified: Mon, 12 Aug 2024 16:58:27 GMT  
		Size: 463.8 KB (463808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b287d809f0865c9ea7ce75aebcf39e8d1ff3f18bfd8d0bf4b64eb9ece241aa3`  
		Last Modified: Mon, 12 Aug 2024 16:58:31 GMT  
		Size: 309.4 MB (309428886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76c54b095ac960507068f82e2f35910f6f4f0bafca431ab238b629783580a12`  
		Last Modified: Mon, 12 Aug 2024 16:58:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba7343fe5a15e88dd9ce8168c01293fe0b7715cbc1cf5c1dc7b6fbed47536c`  
		Last Modified: Mon, 12 Aug 2024 16:58:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85482987ef6aea510ad9ae884d1f4184ef4d8cde7f75206bb3c0b478536e4d07`  
		Last Modified: Mon, 12 Aug 2024 16:58:29 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6d6e4a4ea30ccdc88956c06483702d597b267181fe974006e1606f06a114c9`  
		Last Modified: Mon, 12 Aug 2024 16:58:29 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0` - unknown; unknown

```console
$ docker pull odoo@sha256:80c86d76772ca0b8b2d8bddfdb8577e49b04fda720c1732001bf6c110fcee8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cedaae3cc843c2365c0f105945e0e37434a6e89af97e4df78e974c8d4c190b4`

```dockerfile
```

-	Layers:
	-	`sha256:f55306717e1856428554d76caf3bfa347a85febcf8ac14fcb94c6f98ce76e997`  
		Last Modified: Mon, 12 Aug 2024 16:58:28 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b64d109379f701fe52f634dc16b98e6c79c26f768a12a2d9d3e5b5b81bc831b`  
		Last Modified: Mon, 12 Aug 2024 16:58:27 GMT  
		Size: 24.6 KB (24630 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0-20240812`

```console
$ docker pull odoo@sha256:26e703eff34028d1482f54d3c81c5f87f7b5692d606d44105ae21c38dd85cc3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0-20240812` - linux; amd64

```console
$ docker pull odoo@sha256:8ecabdcea90195a3ebecaac64a9ba6127524f87d7d77ecee10d2393fa9c3f72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563993404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b830eb9ce929d064338ab867802fc24bef9fedcb814858fc3c4837f875ca1149`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=15.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: ODOO_RELEASE=20240812 ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: ODOO_RELEASE=20240812 ODOO_SHA=e7a94dd172521969648670f3995d7c8c3f32941c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025e01fa3710f6774b6eeac504f3b194083a72090484a40313e406d50fa63e8a`  
		Last Modified: Mon, 12 Aug 2024 16:58:30 GMT  
		Size: 220.3 MB (220282207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0ed1241c3538331bb3c51d20626b921da81bd911cf529087014c512c0b5ff3`  
		Last Modified: Mon, 12 Aug 2024 16:58:27 GMT  
		Size: 2.4 MB (2387738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f4e2657406381a48f441042947ac491a745749873dd15a912fd0451952f914`  
		Last Modified: Mon, 12 Aug 2024 16:58:27 GMT  
		Size: 463.8 KB (463808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b287d809f0865c9ea7ce75aebcf39e8d1ff3f18bfd8d0bf4b64eb9ece241aa3`  
		Last Modified: Mon, 12 Aug 2024 16:58:31 GMT  
		Size: 309.4 MB (309428886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76c54b095ac960507068f82e2f35910f6f4f0bafca431ab238b629783580a12`  
		Last Modified: Mon, 12 Aug 2024 16:58:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba7343fe5a15e88dd9ce8168c01293fe0b7715cbc1cf5c1dc7b6fbed47536c`  
		Last Modified: Mon, 12 Aug 2024 16:58:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85482987ef6aea510ad9ae884d1f4184ef4d8cde7f75206bb3c0b478536e4d07`  
		Last Modified: Mon, 12 Aug 2024 16:58:29 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6d6e4a4ea30ccdc88956c06483702d597b267181fe974006e1606f06a114c9`  
		Last Modified: Mon, 12 Aug 2024 16:58:29 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:80c86d76772ca0b8b2d8bddfdb8577e49b04fda720c1732001bf6c110fcee8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cedaae3cc843c2365c0f105945e0e37434a6e89af97e4df78e974c8d4c190b4`

```dockerfile
```

-	Layers:
	-	`sha256:f55306717e1856428554d76caf3bfa347a85febcf8ac14fcb94c6f98ce76e997`  
		Last Modified: Mon, 12 Aug 2024 16:58:28 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b64d109379f701fe52f634dc16b98e6c79c26f768a12a2d9d3e5b5b81bc831b`  
		Last Modified: Mon, 12 Aug 2024 16:58:27 GMT  
		Size: 24.6 KB (24630 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16`

```console
$ docker pull odoo@sha256:2a5ba61b80b7403d3fd7656e19595eef694cf3dc8d3c557b3b32507465d142d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:33e61a1e11e071e69531663ac4e1e78317efa1ef53528b92f122add74b8fd466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.5 MB (583509601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e3c50b9e99bf188fed899027a0164fd59815d20e6185c3b1152bd81fad2a07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca357620fc4ee9efe1be02e27ed18bff52907ab6db961d4156a0668612b6941`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 219.6 MB (219593698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a22472d982cdce2034dba879f758aaeae796f03248c4b148c323545ed8510c`  
		Last Modified: Mon, 12 Aug 2024 16:58:39 GMT  
		Size: 2.4 MB (2391464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e679074020c930187631b59fe1094b780d0b0b37e110f534ecc0d57dae3ab927`  
		Last Modified: Mon, 12 Aug 2024 16:58:39 GMT  
		Size: 463.9 KB (463853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937820541925c2b9c430100564bea219da8bdd5b9552cece35b1f17fffe3f416`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 329.6 MB (329629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85859a35a5c106187d9bfe388ae343296d00b26c2c758446970be8be95a5835c`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b1ae99f7e8b08e95bb12117b18b673d12ade021b80be0cea7840a6856b28b6`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a85992445f016e9f7cf342c0c3b0a299de6db5270cf2a04411167e20922b5`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1185937d3ac21b8dcba05ff0fd56cbb95628fe04602b082a2bb300b70c91ce9`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:cd02e4526765d348934546c446c92d6f881abdfab37fbbdc72959428a6dd67fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38754393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1ed5cb21aaff988cc37197bab918a7a371e1083c6a66791f433ad6c5432b41`

```dockerfile
```

-	Layers:
	-	`sha256:352f59bbd67507020482b8967b5d38a79b6ecd743e38be4c7c182cc32584ce0c`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 38.7 MB (38727851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2af099b1b2a1356f0dfdf6781c488dc8ba30e1e984e87e70198e4183690e251`  
		Last Modified: Mon, 12 Aug 2024 16:58:39 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:39829fe101b310b2355c07452afe48e4832456e0acaf03d44a1c84da8edac8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.1 MB (579096139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772198331c6e99793da122481fbc3a2d62da3eae0e359f3cfd29ec348e05055d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a12cd8726a6409f57fd7f79ecb26568b04fdcc5ec5fdc6c708cf2793c5930c`  
		Last Modified: Tue, 30 Jul 2024 19:08:21 GMT  
		Size: 216.9 MB (216901989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3d3b8eaeb1bcf30cb087ad2ef1105c8d5bfd734b1447c406aeefb5afb9e013`  
		Last Modified: Tue, 30 Jul 2024 19:08:13 GMT  
		Size: 2.4 MB (2393352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da722306c752cdb08871af4dbcb3bdc1de5cb9f790d9950310132c609095a06`  
		Last Modified: Tue, 30 Jul 2024 19:08:13 GMT  
		Size: 463.3 KB (463257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494a7ac79d49a03d08236d740de4714a08ac810c25ccf291ba35fabcb1514790`  
		Last Modified: Mon, 12 Aug 2024 17:19:30 GMT  
		Size: 329.3 MB (329259028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cfebd51932a9e5096d6c51c41a340321d0fc9037c272d36cd8813f23c3720a`  
		Last Modified: Mon, 12 Aug 2024 17:19:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84325406ba8b4f486ce0ac24d71b9f0f909f698d50d97e8bbed0d8dacb36b84`  
		Last Modified: Mon, 12 Aug 2024 17:19:23 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3f60044e59523de51a2ea6ef32265b72e8bb8dcdb3a665ecc08898a8a727d1`  
		Last Modified: Mon, 12 Aug 2024 17:19:23 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a999ae7ee099234b94108f5fedd3f49f8bf7e366cf17f04608527ee24bcf78de`  
		Last Modified: Mon, 12 Aug 2024 17:19:24 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:7ae7d4e702b59ccbc17c6ae3a698de2175e4c733c41e548be432c8e8b5fbfdd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38761162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5355146940fa36da575c6a7888bff29a1db8e0eeeef25d76b59ddd4d996d3072`

```dockerfile
```

-	Layers:
	-	`sha256:10edb76f6cd3d6ce58eadcf267192289046c1e15ec888ff243a9470cf6cc5813`  
		Last Modified: Mon, 12 Aug 2024 17:19:24 GMT  
		Size: 38.7 MB (38734323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd7e7722458c755f3fc433d161245984cca9c9cdf11e5ebcb0a8fcef25f2a8e`  
		Last Modified: Mon, 12 Aug 2024 17:19:23 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:f292c39c86300a13e1a5665d76606775b05ec091af2633be8f4ac7f93bf23743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.0 MB (598010806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083ac4d746331cffadf73c7fdfa857b4adccbe0cd4b594aa7e436506a56c6d71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c266932a4d6b84529e3eb327c7420cde34ae26d911eb1a686f975943e89b5e8d`  
		Last Modified: Tue, 30 Jul 2024 19:17:21 GMT  
		Size: 228.6 MB (228590208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4365e28984131a5dbb84eacd55d304baece6c277ecf937553dfe914ffd9ba9`  
		Last Modified: Tue, 30 Jul 2024 19:17:03 GMT  
		Size: 2.6 MB (2634171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf25b94d104973c28b6d9bb5b61bd21d44000aae9c5e6f455278e1b5510906e5`  
		Last Modified: Tue, 30 Jul 2024 19:17:03 GMT  
		Size: 463.3 KB (463299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8990509b07e0a3e07f44771f69ba914558eab486ec5709ca1c60eb7003e5bb`  
		Last Modified: Mon, 12 Aug 2024 17:31:25 GMT  
		Size: 331.0 MB (331015488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4886c83b7daec08a0c11ea86deab9db8365cde43b8a4ecb8d7ac218e9029ce7`  
		Last Modified: Mon, 12 Aug 2024 17:31:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd66d8469ac0a6303fc8377e9a4026054cbe45e7dd2b709cfcd0ec056fb7690`  
		Last Modified: Mon, 12 Aug 2024 17:31:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27df1e4eeb1dbeb05065ab9a4ae855e1fc6952c09bc997eba3eaa2b906741e13`  
		Last Modified: Mon, 12 Aug 2024 17:31:06 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389b3408bf9b5d769298c6039e2812d3cd25f79a867eb226b4237fe52fc20720`  
		Last Modified: Mon, 12 Aug 2024 17:31:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:96e0bd57bc817d24593055deb647692126975ed8796dca6c6817171d16e533b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38762575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b694711669aea8ca480c86e3fc4f6708b7118d3f73818fc7643a468661f82eab`

```dockerfile
```

-	Layers:
	-	`sha256:dcfd95e05e9fd771bed6b26aadfcfca62f58d4e95fbac878cdac5f6bbb6e5339`  
		Last Modified: Mon, 12 Aug 2024 17:31:08 GMT  
		Size: 38.7 MB (38735983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a71eeb610509b2544655766c0ac9b3c8b86a0f08518e9a87ae5dae4fbf3ed4`  
		Last Modified: Mon, 12 Aug 2024 17:31:06 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:2a5ba61b80b7403d3fd7656e19595eef694cf3dc8d3c557b3b32507465d142d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:33e61a1e11e071e69531663ac4e1e78317efa1ef53528b92f122add74b8fd466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.5 MB (583509601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e3c50b9e99bf188fed899027a0164fd59815d20e6185c3b1152bd81fad2a07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca357620fc4ee9efe1be02e27ed18bff52907ab6db961d4156a0668612b6941`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 219.6 MB (219593698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a22472d982cdce2034dba879f758aaeae796f03248c4b148c323545ed8510c`  
		Last Modified: Mon, 12 Aug 2024 16:58:39 GMT  
		Size: 2.4 MB (2391464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e679074020c930187631b59fe1094b780d0b0b37e110f534ecc0d57dae3ab927`  
		Last Modified: Mon, 12 Aug 2024 16:58:39 GMT  
		Size: 463.9 KB (463853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937820541925c2b9c430100564bea219da8bdd5b9552cece35b1f17fffe3f416`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 329.6 MB (329629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85859a35a5c106187d9bfe388ae343296d00b26c2c758446970be8be95a5835c`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b1ae99f7e8b08e95bb12117b18b673d12ade021b80be0cea7840a6856b28b6`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a85992445f016e9f7cf342c0c3b0a299de6db5270cf2a04411167e20922b5`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1185937d3ac21b8dcba05ff0fd56cbb95628fe04602b082a2bb300b70c91ce9`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cd02e4526765d348934546c446c92d6f881abdfab37fbbdc72959428a6dd67fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38754393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1ed5cb21aaff988cc37197bab918a7a371e1083c6a66791f433ad6c5432b41`

```dockerfile
```

-	Layers:
	-	`sha256:352f59bbd67507020482b8967b5d38a79b6ecd743e38be4c7c182cc32584ce0c`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 38.7 MB (38727851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2af099b1b2a1356f0dfdf6781c488dc8ba30e1e984e87e70198e4183690e251`  
		Last Modified: Mon, 12 Aug 2024 16:58:39 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:39829fe101b310b2355c07452afe48e4832456e0acaf03d44a1c84da8edac8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.1 MB (579096139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772198331c6e99793da122481fbc3a2d62da3eae0e359f3cfd29ec348e05055d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a12cd8726a6409f57fd7f79ecb26568b04fdcc5ec5fdc6c708cf2793c5930c`  
		Last Modified: Tue, 30 Jul 2024 19:08:21 GMT  
		Size: 216.9 MB (216901989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3d3b8eaeb1bcf30cb087ad2ef1105c8d5bfd734b1447c406aeefb5afb9e013`  
		Last Modified: Tue, 30 Jul 2024 19:08:13 GMT  
		Size: 2.4 MB (2393352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da722306c752cdb08871af4dbcb3bdc1de5cb9f790d9950310132c609095a06`  
		Last Modified: Tue, 30 Jul 2024 19:08:13 GMT  
		Size: 463.3 KB (463257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494a7ac79d49a03d08236d740de4714a08ac810c25ccf291ba35fabcb1514790`  
		Last Modified: Mon, 12 Aug 2024 17:19:30 GMT  
		Size: 329.3 MB (329259028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cfebd51932a9e5096d6c51c41a340321d0fc9037c272d36cd8813f23c3720a`  
		Last Modified: Mon, 12 Aug 2024 17:19:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84325406ba8b4f486ce0ac24d71b9f0f909f698d50d97e8bbed0d8dacb36b84`  
		Last Modified: Mon, 12 Aug 2024 17:19:23 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3f60044e59523de51a2ea6ef32265b72e8bb8dcdb3a665ecc08898a8a727d1`  
		Last Modified: Mon, 12 Aug 2024 17:19:23 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a999ae7ee099234b94108f5fedd3f49f8bf7e366cf17f04608527ee24bcf78de`  
		Last Modified: Mon, 12 Aug 2024 17:19:24 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7ae7d4e702b59ccbc17c6ae3a698de2175e4c733c41e548be432c8e8b5fbfdd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38761162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5355146940fa36da575c6a7888bff29a1db8e0eeeef25d76b59ddd4d996d3072`

```dockerfile
```

-	Layers:
	-	`sha256:10edb76f6cd3d6ce58eadcf267192289046c1e15ec888ff243a9470cf6cc5813`  
		Last Modified: Mon, 12 Aug 2024 17:19:24 GMT  
		Size: 38.7 MB (38734323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd7e7722458c755f3fc433d161245984cca9c9cdf11e5ebcb0a8fcef25f2a8e`  
		Last Modified: Mon, 12 Aug 2024 17:19:23 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:f292c39c86300a13e1a5665d76606775b05ec091af2633be8f4ac7f93bf23743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.0 MB (598010806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083ac4d746331cffadf73c7fdfa857b4adccbe0cd4b594aa7e436506a56c6d71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c266932a4d6b84529e3eb327c7420cde34ae26d911eb1a686f975943e89b5e8d`  
		Last Modified: Tue, 30 Jul 2024 19:17:21 GMT  
		Size: 228.6 MB (228590208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4365e28984131a5dbb84eacd55d304baece6c277ecf937553dfe914ffd9ba9`  
		Last Modified: Tue, 30 Jul 2024 19:17:03 GMT  
		Size: 2.6 MB (2634171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf25b94d104973c28b6d9bb5b61bd21d44000aae9c5e6f455278e1b5510906e5`  
		Last Modified: Tue, 30 Jul 2024 19:17:03 GMT  
		Size: 463.3 KB (463299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8990509b07e0a3e07f44771f69ba914558eab486ec5709ca1c60eb7003e5bb`  
		Last Modified: Mon, 12 Aug 2024 17:31:25 GMT  
		Size: 331.0 MB (331015488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4886c83b7daec08a0c11ea86deab9db8365cde43b8a4ecb8d7ac218e9029ce7`  
		Last Modified: Mon, 12 Aug 2024 17:31:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd66d8469ac0a6303fc8377e9a4026054cbe45e7dd2b709cfcd0ec056fb7690`  
		Last Modified: Mon, 12 Aug 2024 17:31:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27df1e4eeb1dbeb05065ab9a4ae855e1fc6952c09bc997eba3eaa2b906741e13`  
		Last Modified: Mon, 12 Aug 2024 17:31:06 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389b3408bf9b5d769298c6039e2812d3cd25f79a867eb226b4237fe52fc20720`  
		Last Modified: Mon, 12 Aug 2024 17:31:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:96e0bd57bc817d24593055deb647692126975ed8796dca6c6817171d16e533b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38762575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b694711669aea8ca480c86e3fc4f6708b7118d3f73818fc7643a468661f82eab`

```dockerfile
```

-	Layers:
	-	`sha256:dcfd95e05e9fd771bed6b26aadfcfca62f58d4e95fbac878cdac5f6bbb6e5339`  
		Last Modified: Mon, 12 Aug 2024 17:31:08 GMT  
		Size: 38.7 MB (38735983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a71eeb610509b2544655766c0ac9b3c8b86a0f08518e9a87ae5dae4fbf3ed4`  
		Last Modified: Mon, 12 Aug 2024 17:31:06 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20240812`

```console
$ docker pull odoo@sha256:2a5ba61b80b7403d3fd7656e19595eef694cf3dc8d3c557b3b32507465d142d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0-20240812` - linux; amd64

```console
$ docker pull odoo@sha256:33e61a1e11e071e69531663ac4e1e78317efa1ef53528b92f122add74b8fd466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.5 MB (583509601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e3c50b9e99bf188fed899027a0164fd59815d20e6185c3b1152bd81fad2a07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca357620fc4ee9efe1be02e27ed18bff52907ab6db961d4156a0668612b6941`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 219.6 MB (219593698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a22472d982cdce2034dba879f758aaeae796f03248c4b148c323545ed8510c`  
		Last Modified: Mon, 12 Aug 2024 16:58:39 GMT  
		Size: 2.4 MB (2391464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e679074020c930187631b59fe1094b780d0b0b37e110f534ecc0d57dae3ab927`  
		Last Modified: Mon, 12 Aug 2024 16:58:39 GMT  
		Size: 463.9 KB (463853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937820541925c2b9c430100564bea219da8bdd5b9552cece35b1f17fffe3f416`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 329.6 MB (329629827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85859a35a5c106187d9bfe388ae343296d00b26c2c758446970be8be95a5835c`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b1ae99f7e8b08e95bb12117b18b673d12ade021b80be0cea7840a6856b28b6`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a85992445f016e9f7cf342c0c3b0a299de6db5270cf2a04411167e20922b5`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1185937d3ac21b8dcba05ff0fd56cbb95628fe04602b082a2bb300b70c91ce9`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:cd02e4526765d348934546c446c92d6f881abdfab37fbbdc72959428a6dd67fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38754393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1ed5cb21aaff988cc37197bab918a7a371e1083c6a66791f433ad6c5432b41`

```dockerfile
```

-	Layers:
	-	`sha256:352f59bbd67507020482b8967b5d38a79b6ecd743e38be4c7c182cc32584ce0c`  
		Last Modified: Mon, 12 Aug 2024 16:58:40 GMT  
		Size: 38.7 MB (38727851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2af099b1b2a1356f0dfdf6781c488dc8ba30e1e984e87e70198e4183690e251`  
		Last Modified: Mon, 12 Aug 2024 16:58:39 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240812` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:39829fe101b310b2355c07452afe48e4832456e0acaf03d44a1c84da8edac8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.1 MB (579096139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772198331c6e99793da122481fbc3a2d62da3eae0e359f3cfd29ec348e05055d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a12cd8726a6409f57fd7f79ecb26568b04fdcc5ec5fdc6c708cf2793c5930c`  
		Last Modified: Tue, 30 Jul 2024 19:08:21 GMT  
		Size: 216.9 MB (216901989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3d3b8eaeb1bcf30cb087ad2ef1105c8d5bfd734b1447c406aeefb5afb9e013`  
		Last Modified: Tue, 30 Jul 2024 19:08:13 GMT  
		Size: 2.4 MB (2393352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da722306c752cdb08871af4dbcb3bdc1de5cb9f790d9950310132c609095a06`  
		Last Modified: Tue, 30 Jul 2024 19:08:13 GMT  
		Size: 463.3 KB (463257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494a7ac79d49a03d08236d740de4714a08ac810c25ccf291ba35fabcb1514790`  
		Last Modified: Mon, 12 Aug 2024 17:19:30 GMT  
		Size: 329.3 MB (329259028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cfebd51932a9e5096d6c51c41a340321d0fc9037c272d36cd8813f23c3720a`  
		Last Modified: Mon, 12 Aug 2024 17:19:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84325406ba8b4f486ce0ac24d71b9f0f909f698d50d97e8bbed0d8dacb36b84`  
		Last Modified: Mon, 12 Aug 2024 17:19:23 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3f60044e59523de51a2ea6ef32265b72e8bb8dcdb3a665ecc08898a8a727d1`  
		Last Modified: Mon, 12 Aug 2024 17:19:23 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a999ae7ee099234b94108f5fedd3f49f8bf7e366cf17f04608527ee24bcf78de`  
		Last Modified: Mon, 12 Aug 2024 17:19:24 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:7ae7d4e702b59ccbc17c6ae3a698de2175e4c733c41e548be432c8e8b5fbfdd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38761162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5355146940fa36da575c6a7888bff29a1db8e0eeeef25d76b59ddd4d996d3072`

```dockerfile
```

-	Layers:
	-	`sha256:10edb76f6cd3d6ce58eadcf267192289046c1e15ec888ff243a9470cf6cc5813`  
		Last Modified: Mon, 12 Aug 2024 17:19:24 GMT  
		Size: 38.7 MB (38734323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd7e7722458c755f3fc433d161245984cca9c9cdf11e5ebcb0a8fcef25f2a8e`  
		Last Modified: Mon, 12 Aug 2024 17:19:23 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240812` - linux; ppc64le

```console
$ docker pull odoo@sha256:f292c39c86300a13e1a5665d76606775b05ec091af2633be8f4ac7f93bf23743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.0 MB (598010806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083ac4d746331cffadf73c7fdfa857b4adccbe0cd4b594aa7e436506a56c6d71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=C.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=16.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=4dd27a13b50e32011048d75444bc31a022c67618
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c266932a4d6b84529e3eb327c7420cde34ae26d911eb1a686f975943e89b5e8d`  
		Last Modified: Tue, 30 Jul 2024 19:17:21 GMT  
		Size: 228.6 MB (228590208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4365e28984131a5dbb84eacd55d304baece6c277ecf937553dfe914ffd9ba9`  
		Last Modified: Tue, 30 Jul 2024 19:17:03 GMT  
		Size: 2.6 MB (2634171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf25b94d104973c28b6d9bb5b61bd21d44000aae9c5e6f455278e1b5510906e5`  
		Last Modified: Tue, 30 Jul 2024 19:17:03 GMT  
		Size: 463.3 KB (463299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8990509b07e0a3e07f44771f69ba914558eab486ec5709ca1c60eb7003e5bb`  
		Last Modified: Mon, 12 Aug 2024 17:31:25 GMT  
		Size: 331.0 MB (331015488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4886c83b7daec08a0c11ea86deab9db8365cde43b8a4ecb8d7ac218e9029ce7`  
		Last Modified: Mon, 12 Aug 2024 17:31:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd66d8469ac0a6303fc8377e9a4026054cbe45e7dd2b709cfcd0ec056fb7690`  
		Last Modified: Mon, 12 Aug 2024 17:31:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27df1e4eeb1dbeb05065ab9a4ae855e1fc6952c09bc997eba3eaa2b906741e13`  
		Last Modified: Mon, 12 Aug 2024 17:31:06 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389b3408bf9b5d769298c6039e2812d3cd25f79a867eb226b4237fe52fc20720`  
		Last Modified: Mon, 12 Aug 2024 17:31:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:96e0bd57bc817d24593055deb647692126975ed8796dca6c6817171d16e533b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38762575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b694711669aea8ca480c86e3fc4f6708b7118d3f73818fc7643a468661f82eab`

```dockerfile
```

-	Layers:
	-	`sha256:dcfd95e05e9fd771bed6b26aadfcfca62f58d4e95fbac878cdac5f6bbb6e5339`  
		Last Modified: Mon, 12 Aug 2024 17:31:08 GMT  
		Size: 38.7 MB (38735983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a71eeb610509b2544655766c0ac9b3c8b86a0f08518e9a87ae5dae4fbf3ed4`  
		Last Modified: Mon, 12 Aug 2024 17:31:06 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:12c8f9d782059814e1f190727dcc72d8831e2a8ac9f7786cf45cd39fb629400a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:1cdb1d7aca1b98368e71b0049f28ce27fd91cf33298decaa9b9ecbba07eb2b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597670298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c2ee66381b89397e9b67169cf3fe939ebd61981bfaadd1b5a3b2eb7b2e21b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b97d817b6db27c1928f6a42c844f3269e50bcf47aa9a9667fbd3db11e4ea23`  
		Last Modified: Mon, 12 Aug 2024 16:58:46 GMT  
		Size: 236.0 MB (236023122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109966a444a61189e1008ec7f78e5a63a5c678477da9969e443cfa1b9f7a3e65`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 2.3 MB (2315818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca1ceaafe360e7c2eb48ea21c069b10da0004f15050e6d6bf3513e239ba92b9`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 464.9 KB (464945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad698162b1a00c222756334da2c09ed0521109d7f1d19682b24687a5cc2ccd9`  
		Last Modified: Mon, 12 Aug 2024 16:58:47 GMT  
		Size: 329.3 MB (329329915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3e9b3139a88f6f6196e298706d83488100045f0ad3d5b18eb461bf62016b80`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddffb8bab1cd6ec722d86b9d61ecb558070b9659aae04a696ecfb59fa5a98f`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a2220e858c2c55c070c7afa3c1ca37ae8e4de6c241c2dfd57be53a8ce55eb5`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfad5f8642fd09b5f672ed93047124ce16e7e75fa69faaab3aea896c1d15d3e4`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:f43accb3034516aaa7809b520f38f958e699343058c681b0842d5d4e75cfbca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38983060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843b187fb50f3ae2b98e2c0bffd2c4fa63ce03a19d3eb58a113cce9ada645c`

```dockerfile
```

-	Layers:
	-	`sha256:a686aa91b4c474c1be0d35c6b1b4628413bf45e032bbcd2b331c9bce613a0882`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 39.0 MB (38956185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c053693c0db30b810560bc8d138c0481d82878a099c26767164165a09985b254`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b5317e9266ab45927033437194845e0b71122406dc2fb45a467b92086f22b4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590178176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6b827f072ab1c262a98d2377909bc48f2e05b6817b5d883395464a5475e9cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169fa3f48783fbeec78b2a931ddac75d618c1edb2d6ea4e2c6fe5f9730ab868`  
		Last Modified: Tue, 30 Jul 2024 19:04:26 GMT  
		Size: 231.1 MB (231116218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04b57c1d87d80886aaedd13d353dde577429e740cfb574935ba1669b44b69aa`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 2.3 MB (2306415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bcca78310f41f21f044796b20832ee3156e7de28ba2bbbe8e3a8fe835e409f`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 464.4 KB (464370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6f99caa43ea3b02cbb493d6eb8c3bc046f48220f7dd7264469b61a2cd5c5f4`  
		Last Modified: Mon, 12 Aug 2024 17:16:33 GMT  
		Size: 328.9 MB (328928708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f010333b1805242d7529c01feb8a9aba0260f3c759a82c848d47bc772c8b4`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb432b6d7099111ed941c5c26b5739ef0dcd2ff5758b15e3b1411dc2362996f`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d34c60c8d489331ab49bfc09f33ff4df4670b450fe7f1e9815a09f7926545d`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21a88d1c2047be4f9994e244b2880671cca9763c8705129630c8aedc1183e7`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:e77a5779b9910b208e131a70809823777f388a2ea9224652c27d3cf72ca4b86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38989885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1664144f6b6039e92dbfb6853a2243c9cfc821d4508af5ad7ed346a85adbab4a`

```dockerfile
```

-	Layers:
	-	`sha256:b63132ba239d961c4e39ea18df18b773cc787e3fde3e0bd6d7b98b80b115d195`  
		Last Modified: Mon, 12 Aug 2024 17:16:27 GMT  
		Size: 39.0 MB (38962710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2673e89d66bff4e99defe322064a148f7e8ca1a0599ae43edbbacbda91e9b844`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 27.2 KB (27175 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:5be0825b87874e8b2d2cc99f1f36c6cbedbcfa07ed894945a17e6c2f7fe588d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611853700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f061e48975be4deb1f6a4d2faca3663c7aa095e97fddd112fc5c6e0e7efd110f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750728ff278f8ee72bd1d43a21ffcd830b8460c31825944ca547211e693fea90`  
		Last Modified: Tue, 30 Jul 2024 19:08:40 GMT  
		Size: 243.3 MB (243278728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0144d2aa49c93b6e019b8c471462c462b926da64cb5e2cc1d18d711c14a5888`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 2.6 MB (2590475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332f9f2f0f52ab9fd31f25e668515d8ab8c4b568e8b8cc5f7cdc1a48d588d970`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 464.4 KB (464386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb27bfc9b48029d4ceee6fab8a8e952d84d859997351145e8faaa24cc3c8a06`  
		Last Modified: Mon, 12 Aug 2024 17:26:16 GMT  
		Size: 331.1 MB (331056587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69716c727479aca316bd1a3e19c41a9f6f5c921713b82889ff07b43ab2d17bab`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7d627f697b99ab9e266e4621c3d310eca7a08c8bf25a7b11b1b27bc0d0d75`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070a6b546c1f54a69f751106ae9ef1a5e2e2e1556976047dc7269bb75ebf7a8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fce6a52eed5cae88b9bcad4c2c97a8d8563c8b9c54e5ea94535b78d9efb10`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:186b7720403b4368c19b9eceeec6a2480b6a0c8974c78a89b0fa313fdadce49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38991429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4549de6f82227ccff2a41867fee8cd7459b4f1557b0b7a6a5f85eba75d8e66c`

```dockerfile
```

-	Layers:
	-	`sha256:052ecf79d8179ed602f4df5a85299720c81ebaab4c01973ea83c30cc4b8b655f`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 39.0 MB (38964498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99ce8bca182db4e4c6e543540f55fc4ac999622058c0c37d7d0320a4185ddf8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:12c8f9d782059814e1f190727dcc72d8831e2a8ac9f7786cf45cd39fb629400a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:1cdb1d7aca1b98368e71b0049f28ce27fd91cf33298decaa9b9ecbba07eb2b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597670298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c2ee66381b89397e9b67169cf3fe939ebd61981bfaadd1b5a3b2eb7b2e21b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b97d817b6db27c1928f6a42c844f3269e50bcf47aa9a9667fbd3db11e4ea23`  
		Last Modified: Mon, 12 Aug 2024 16:58:46 GMT  
		Size: 236.0 MB (236023122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109966a444a61189e1008ec7f78e5a63a5c678477da9969e443cfa1b9f7a3e65`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 2.3 MB (2315818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca1ceaafe360e7c2eb48ea21c069b10da0004f15050e6d6bf3513e239ba92b9`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 464.9 KB (464945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad698162b1a00c222756334da2c09ed0521109d7f1d19682b24687a5cc2ccd9`  
		Last Modified: Mon, 12 Aug 2024 16:58:47 GMT  
		Size: 329.3 MB (329329915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3e9b3139a88f6f6196e298706d83488100045f0ad3d5b18eb461bf62016b80`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddffb8bab1cd6ec722d86b9d61ecb558070b9659aae04a696ecfb59fa5a98f`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a2220e858c2c55c070c7afa3c1ca37ae8e4de6c241c2dfd57be53a8ce55eb5`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfad5f8642fd09b5f672ed93047124ce16e7e75fa69faaab3aea896c1d15d3e4`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f43accb3034516aaa7809b520f38f958e699343058c681b0842d5d4e75cfbca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38983060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843b187fb50f3ae2b98e2c0bffd2c4fa63ce03a19d3eb58a113cce9ada645c`

```dockerfile
```

-	Layers:
	-	`sha256:a686aa91b4c474c1be0d35c6b1b4628413bf45e032bbcd2b331c9bce613a0882`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 39.0 MB (38956185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c053693c0db30b810560bc8d138c0481d82878a099c26767164165a09985b254`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b5317e9266ab45927033437194845e0b71122406dc2fb45a467b92086f22b4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590178176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6b827f072ab1c262a98d2377909bc48f2e05b6817b5d883395464a5475e9cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169fa3f48783fbeec78b2a931ddac75d618c1edb2d6ea4e2c6fe5f9730ab868`  
		Last Modified: Tue, 30 Jul 2024 19:04:26 GMT  
		Size: 231.1 MB (231116218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04b57c1d87d80886aaedd13d353dde577429e740cfb574935ba1669b44b69aa`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 2.3 MB (2306415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bcca78310f41f21f044796b20832ee3156e7de28ba2bbbe8e3a8fe835e409f`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 464.4 KB (464370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6f99caa43ea3b02cbb493d6eb8c3bc046f48220f7dd7264469b61a2cd5c5f4`  
		Last Modified: Mon, 12 Aug 2024 17:16:33 GMT  
		Size: 328.9 MB (328928708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f010333b1805242d7529c01feb8a9aba0260f3c759a82c848d47bc772c8b4`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb432b6d7099111ed941c5c26b5739ef0dcd2ff5758b15e3b1411dc2362996f`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d34c60c8d489331ab49bfc09f33ff4df4670b450fe7f1e9815a09f7926545d`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21a88d1c2047be4f9994e244b2880671cca9763c8705129630c8aedc1183e7`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e77a5779b9910b208e131a70809823777f388a2ea9224652c27d3cf72ca4b86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38989885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1664144f6b6039e92dbfb6853a2243c9cfc821d4508af5ad7ed346a85adbab4a`

```dockerfile
```

-	Layers:
	-	`sha256:b63132ba239d961c4e39ea18df18b773cc787e3fde3e0bd6d7b98b80b115d195`  
		Last Modified: Mon, 12 Aug 2024 17:16:27 GMT  
		Size: 39.0 MB (38962710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2673e89d66bff4e99defe322064a148f7e8ca1a0599ae43edbbacbda91e9b844`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 27.2 KB (27175 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:5be0825b87874e8b2d2cc99f1f36c6cbedbcfa07ed894945a17e6c2f7fe588d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611853700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f061e48975be4deb1f6a4d2faca3663c7aa095e97fddd112fc5c6e0e7efd110f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750728ff278f8ee72bd1d43a21ffcd830b8460c31825944ca547211e693fea90`  
		Last Modified: Tue, 30 Jul 2024 19:08:40 GMT  
		Size: 243.3 MB (243278728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0144d2aa49c93b6e019b8c471462c462b926da64cb5e2cc1d18d711c14a5888`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 2.6 MB (2590475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332f9f2f0f52ab9fd31f25e668515d8ab8c4b568e8b8cc5f7cdc1a48d588d970`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 464.4 KB (464386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb27bfc9b48029d4ceee6fab8a8e952d84d859997351145e8faaa24cc3c8a06`  
		Last Modified: Mon, 12 Aug 2024 17:26:16 GMT  
		Size: 331.1 MB (331056587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69716c727479aca316bd1a3e19c41a9f6f5c921713b82889ff07b43ab2d17bab`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7d627f697b99ab9e266e4621c3d310eca7a08c8bf25a7b11b1b27bc0d0d75`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070a6b546c1f54a69f751106ae9ef1a5e2e2e1556976047dc7269bb75ebf7a8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fce6a52eed5cae88b9bcad4c2c97a8d8563c8b9c54e5ea94535b78d9efb10`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:186b7720403b4368c19b9eceeec6a2480b6a0c8974c78a89b0fa313fdadce49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38991429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4549de6f82227ccff2a41867fee8cd7459b4f1557b0b7a6a5f85eba75d8e66c`

```dockerfile
```

-	Layers:
	-	`sha256:052ecf79d8179ed602f4df5a85299720c81ebaab4c01973ea83c30cc4b8b655f`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 39.0 MB (38964498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99ce8bca182db4e4c6e543540f55fc4ac999622058c0c37d7d0320a4185ddf8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240812`

```console
$ docker pull odoo@sha256:12c8f9d782059814e1f190727dcc72d8831e2a8ac9f7786cf45cd39fb629400a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20240812` - linux; amd64

```console
$ docker pull odoo@sha256:1cdb1d7aca1b98368e71b0049f28ce27fd91cf33298decaa9b9ecbba07eb2b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597670298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c2ee66381b89397e9b67169cf3fe939ebd61981bfaadd1b5a3b2eb7b2e21b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b97d817b6db27c1928f6a42c844f3269e50bcf47aa9a9667fbd3db11e4ea23`  
		Last Modified: Mon, 12 Aug 2024 16:58:46 GMT  
		Size: 236.0 MB (236023122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109966a444a61189e1008ec7f78e5a63a5c678477da9969e443cfa1b9f7a3e65`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 2.3 MB (2315818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca1ceaafe360e7c2eb48ea21c069b10da0004f15050e6d6bf3513e239ba92b9`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 464.9 KB (464945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad698162b1a00c222756334da2c09ed0521109d7f1d19682b24687a5cc2ccd9`  
		Last Modified: Mon, 12 Aug 2024 16:58:47 GMT  
		Size: 329.3 MB (329329915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3e9b3139a88f6f6196e298706d83488100045f0ad3d5b18eb461bf62016b80`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddffb8bab1cd6ec722d86b9d61ecb558070b9659aae04a696ecfb59fa5a98f`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a2220e858c2c55c070c7afa3c1ca37ae8e4de6c241c2dfd57be53a8ce55eb5`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfad5f8642fd09b5f672ed93047124ce16e7e75fa69faaab3aea896c1d15d3e4`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:f43accb3034516aaa7809b520f38f958e699343058c681b0842d5d4e75cfbca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38983060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843b187fb50f3ae2b98e2c0bffd2c4fa63ce03a19d3eb58a113cce9ada645c`

```dockerfile
```

-	Layers:
	-	`sha256:a686aa91b4c474c1be0d35c6b1b4628413bf45e032bbcd2b331c9bce613a0882`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 39.0 MB (38956185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c053693c0db30b810560bc8d138c0481d82878a099c26767164165a09985b254`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240812` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b5317e9266ab45927033437194845e0b71122406dc2fb45a467b92086f22b4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590178176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6b827f072ab1c262a98d2377909bc48f2e05b6817b5d883395464a5475e9cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169fa3f48783fbeec78b2a931ddac75d618c1edb2d6ea4e2c6fe5f9730ab868`  
		Last Modified: Tue, 30 Jul 2024 19:04:26 GMT  
		Size: 231.1 MB (231116218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04b57c1d87d80886aaedd13d353dde577429e740cfb574935ba1669b44b69aa`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 2.3 MB (2306415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bcca78310f41f21f044796b20832ee3156e7de28ba2bbbe8e3a8fe835e409f`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 464.4 KB (464370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6f99caa43ea3b02cbb493d6eb8c3bc046f48220f7dd7264469b61a2cd5c5f4`  
		Last Modified: Mon, 12 Aug 2024 17:16:33 GMT  
		Size: 328.9 MB (328928708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f010333b1805242d7529c01feb8a9aba0260f3c759a82c848d47bc772c8b4`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb432b6d7099111ed941c5c26b5739ef0dcd2ff5758b15e3b1411dc2362996f`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d34c60c8d489331ab49bfc09f33ff4df4670b450fe7f1e9815a09f7926545d`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21a88d1c2047be4f9994e244b2880671cca9763c8705129630c8aedc1183e7`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:e77a5779b9910b208e131a70809823777f388a2ea9224652c27d3cf72ca4b86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38989885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1664144f6b6039e92dbfb6853a2243c9cfc821d4508af5ad7ed346a85adbab4a`

```dockerfile
```

-	Layers:
	-	`sha256:b63132ba239d961c4e39ea18df18b773cc787e3fde3e0bd6d7b98b80b115d195`  
		Last Modified: Mon, 12 Aug 2024 17:16:27 GMT  
		Size: 39.0 MB (38962710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2673e89d66bff4e99defe322064a148f7e8ca1a0599ae43edbbacbda91e9b844`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 27.2 KB (27175 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240812` - linux; ppc64le

```console
$ docker pull odoo@sha256:5be0825b87874e8b2d2cc99f1f36c6cbedbcfa07ed894945a17e6c2f7fe588d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611853700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f061e48975be4deb1f6a4d2faca3663c7aa095e97fddd112fc5c6e0e7efd110f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750728ff278f8ee72bd1d43a21ffcd830b8460c31825944ca547211e693fea90`  
		Last Modified: Tue, 30 Jul 2024 19:08:40 GMT  
		Size: 243.3 MB (243278728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0144d2aa49c93b6e019b8c471462c462b926da64cb5e2cc1d18d711c14a5888`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 2.6 MB (2590475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332f9f2f0f52ab9fd31f25e668515d8ab8c4b568e8b8cc5f7cdc1a48d588d970`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 464.4 KB (464386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb27bfc9b48029d4ceee6fab8a8e952d84d859997351145e8faaa24cc3c8a06`  
		Last Modified: Mon, 12 Aug 2024 17:26:16 GMT  
		Size: 331.1 MB (331056587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69716c727479aca316bd1a3e19c41a9f6f5c921713b82889ff07b43ab2d17bab`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7d627f697b99ab9e266e4621c3d310eca7a08c8bf25a7b11b1b27bc0d0d75`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070a6b546c1f54a69f751106ae9ef1a5e2e2e1556976047dc7269bb75ebf7a8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fce6a52eed5cae88b9bcad4c2c97a8d8563c8b9c54e5ea94535b78d9efb10`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240812` - unknown; unknown

```console
$ docker pull odoo@sha256:186b7720403b4368c19b9eceeec6a2480b6a0c8974c78a89b0fa313fdadce49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38991429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4549de6f82227ccff2a41867fee8cd7459b4f1557b0b7a6a5f85eba75d8e66c`

```dockerfile
```

-	Layers:
	-	`sha256:052ecf79d8179ed602f4df5a85299720c81ebaab4c01973ea83c30cc4b8b655f`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 39.0 MB (38964498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99ce8bca182db4e4c6e543540f55fc4ac999622058c0c37d7d0320a4185ddf8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:12c8f9d782059814e1f190727dcc72d8831e2a8ac9f7786cf45cd39fb629400a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:1cdb1d7aca1b98368e71b0049f28ce27fd91cf33298decaa9b9ecbba07eb2b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597670298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c2ee66381b89397e9b67169cf3fe939ebd61981bfaadd1b5a3b2eb7b2e21b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=amd64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b97d817b6db27c1928f6a42c844f3269e50bcf47aa9a9667fbd3db11e4ea23`  
		Last Modified: Mon, 12 Aug 2024 16:58:46 GMT  
		Size: 236.0 MB (236023122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109966a444a61189e1008ec7f78e5a63a5c678477da9969e443cfa1b9f7a3e65`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 2.3 MB (2315818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca1ceaafe360e7c2eb48ea21c069b10da0004f15050e6d6bf3513e239ba92b9`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 464.9 KB (464945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad698162b1a00c222756334da2c09ed0521109d7f1d19682b24687a5cc2ccd9`  
		Last Modified: Mon, 12 Aug 2024 16:58:47 GMT  
		Size: 329.3 MB (329329915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3e9b3139a88f6f6196e298706d83488100045f0ad3d5b18eb461bf62016b80`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddffb8bab1cd6ec722d86b9d61ecb558070b9659aae04a696ecfb59fa5a98f`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a2220e858c2c55c070c7afa3c1ca37ae8e4de6c241c2dfd57be53a8ce55eb5`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfad5f8642fd09b5f672ed93047124ce16e7e75fa69faaab3aea896c1d15d3e4`  
		Last Modified: Mon, 12 Aug 2024 16:58:44 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f43accb3034516aaa7809b520f38f958e699343058c681b0842d5d4e75cfbca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38983060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61843b187fb50f3ae2b98e2c0bffd2c4fa63ce03a19d3eb58a113cce9ada645c`

```dockerfile
```

-	Layers:
	-	`sha256:a686aa91b4c474c1be0d35c6b1b4628413bf45e032bbcd2b331c9bce613a0882`  
		Last Modified: Mon, 12 Aug 2024 16:58:43 GMT  
		Size: 39.0 MB (38956185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c053693c0db30b810560bc8d138c0481d82878a099c26767164165a09985b254`  
		Last Modified: Mon, 12 Aug 2024 16:58:42 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b5317e9266ab45927033437194845e0b71122406dc2fb45a467b92086f22b4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.2 MB (590178176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6b827f072ab1c262a98d2377909bc48f2e05b6817b5d883395464a5475e9cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=arm64
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c169fa3f48783fbeec78b2a931ddac75d618c1edb2d6ea4e2c6fe5f9730ab868`  
		Last Modified: Tue, 30 Jul 2024 19:04:26 GMT  
		Size: 231.1 MB (231116218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04b57c1d87d80886aaedd13d353dde577429e740cfb574935ba1669b44b69aa`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 2.3 MB (2306415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bcca78310f41f21f044796b20832ee3156e7de28ba2bbbe8e3a8fe835e409f`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 464.4 KB (464370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6f99caa43ea3b02cbb493d6eb8c3bc046f48220f7dd7264469b61a2cd5c5f4`  
		Last Modified: Mon, 12 Aug 2024 17:16:33 GMT  
		Size: 328.9 MB (328928708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f010333b1805242d7529c01feb8a9aba0260f3c759a82c848d47bc772c8b4`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb432b6d7099111ed941c5c26b5739ef0dcd2ff5758b15e3b1411dc2362996f`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d34c60c8d489331ab49bfc09f33ff4df4670b450fe7f1e9815a09f7926545d`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c21a88d1c2047be4f9994e244b2880671cca9763c8705129630c8aedc1183e7`  
		Last Modified: Mon, 12 Aug 2024 17:16:26 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:e77a5779b9910b208e131a70809823777f388a2ea9224652c27d3cf72ca4b86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38989885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1664144f6b6039e92dbfb6853a2243c9cfc821d4508af5ad7ed346a85adbab4a`

```dockerfile
```

-	Layers:
	-	`sha256:b63132ba239d961c4e39ea18df18b773cc787e3fde3e0bd6d7b98b80b115d195`  
		Last Modified: Mon, 12 Aug 2024 17:16:27 GMT  
		Size: 39.0 MB (38962710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2673e89d66bff4e99defe322064a148f7e8ca1a0599ae43edbbacbda91e9b844`  
		Last Modified: Mon, 12 Aug 2024 17:16:25 GMT  
		Size: 27.2 KB (27175 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:5be0825b87874e8b2d2cc99f1f36c6cbedbcfa07ed894945a17e6c2f7fe588d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 MB (611853700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f061e48975be4deb1f6a4d2faca3663c7aa095e97fddd112fc5c6e0e7efd110f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 12 Aug 2024 11:24:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 12 Aug 2024 11:24:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Aug 2024 11:24:22 GMT
ARG TARGETARCH=ppc64le
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_VERSION=17.0
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_RELEASE=20240812
# Mon, 12 Aug 2024 11:24:22 GMT
ARG ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240812 ODOO_SHA=f42fe6e80daa50d3198987e9d76373cfa6e4396c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 12 Aug 2024 11:24:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 12 Aug 2024 11:24:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 12 Aug 2024 11:24:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 12 Aug 2024 11:24:22 GMT
USER odoo
# Mon, 12 Aug 2024 11:24:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Aug 2024 11:24:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750728ff278f8ee72bd1d43a21ffcd830b8460c31825944ca547211e693fea90`  
		Last Modified: Tue, 30 Jul 2024 19:08:40 GMT  
		Size: 243.3 MB (243278728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0144d2aa49c93b6e019b8c471462c462b926da64cb5e2cc1d18d711c14a5888`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 2.6 MB (2590475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332f9f2f0f52ab9fd31f25e668515d8ab8c4b568e8b8cc5f7cdc1a48d588d970`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 464.4 KB (464386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb27bfc9b48029d4ceee6fab8a8e952d84d859997351145e8faaa24cc3c8a06`  
		Last Modified: Mon, 12 Aug 2024 17:26:16 GMT  
		Size: 331.1 MB (331056587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69716c727479aca316bd1a3e19c41a9f6f5c921713b82889ff07b43ab2d17bab`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d7d627f697b99ab9e266e4621c3d310eca7a08c8bf25a7b11b1b27bc0d0d75`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c070a6b546c1f54a69f751106ae9ef1a5e2e2e1556976047dc7269bb75ebf7a8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0fce6a52eed5cae88b9bcad4c2c97a8d8563c8b9c54e5ea94535b78d9efb10`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:186b7720403b4368c19b9eceeec6a2480b6a0c8974c78a89b0fa313fdadce49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38991429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4549de6f82227ccff2a41867fee8cd7459b4f1557b0b7a6a5f85eba75d8e66c`

```dockerfile
```

-	Layers:
	-	`sha256:052ecf79d8179ed602f4df5a85299720c81ebaab4c01973ea83c30cc4b8b655f`  
		Last Modified: Mon, 12 Aug 2024 17:26:05 GMT  
		Size: 39.0 MB (38964498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99ce8bca182db4e4c6e543540f55fc4ac999622058c0c37d7d0320a4185ddf8`  
		Last Modified: Mon, 12 Aug 2024 17:26:04 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json
