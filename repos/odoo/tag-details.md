<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:15.0-20240730`](#odoo150-20240730)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20240730`](#odoo160-20240730)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20240730`](#odoo170-20240730)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:240c850b917b1af805272d258fec5f9b28133cb384712a7901dee4ad73194240
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:c546d8bb579b3a5e9a0ef1e775f0e84cd6374321d1051671420b9bd44bfb2b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563937790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b89e9f6ee7507fe367c80c1d361670c7a2fbe66fac2e68137413934d4050b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=15.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=dca04f296736763d040f26c653bc11ae5020ccc6
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: ODOO_RELEASE=20240730 ODOO_SHA=dca04f296736763d040f26c653bc11ae5020ccc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: ODOO_RELEASE=20240730 ODOO_SHA=dca04f296736763d040f26c653bc11ae5020ccc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe01f5e701a011c965fa618067b47db6ed29efda3050fd23171d655425a19def`  
		Last Modified: Tue, 30 Jul 2024 18:57:24 GMT  
		Size: 220.3 MB (220281611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda8967bc6e2e4bc3c20c25579589b193692bfbcd956dbd4e562115cff643560`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 2.4 MB (2387198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cfef7dd992901bf6436ff1d832dce8729b5f0ae0909f5831a7ee40e8c33079`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 463.3 KB (463258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42537583f75ba6e278cda2e7a2a1ad629a9e0678d99c5563548cbedb6262abb2`  
		Last Modified: Tue, 30 Jul 2024 18:57:28 GMT  
		Size: 309.4 MB (309374958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5168384ce28c8fec5bf0ce1e6cd4d233ea44ea3f6b28cb9af015b9fadbb4152b`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817fcba3018d0c5fe3cdccd96b0f4a60042c5d5b7cfeb853220c357a5ce5a39d`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84c62ced73bbe1a69cc6ef51a48dc78bb688e5567e565b2cdbaade9b8b1cb5e`  
		Last Modified: Tue, 30 Jul 2024 18:57:22 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15a16b02774038e0df603bf313180c8128132f0dbedbf89156d36f9ddb11b89`  
		Last Modified: Tue, 30 Jul 2024 18:57:22 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15` - unknown; unknown

```console
$ docker pull odoo@sha256:faa581c115cb2d5ad0927e5e7e901648e95f8aa6d011c67df2d78bbae8a42dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d8c38e2431620882f7a227ad12b7cc93f588630aaba60e6828a7dfa0438490`

```dockerfile
```

-	Layers:
	-	`sha256:3949963452e8050e3b03ce91a247dbfb8b9bc63fc92364c135653cea4b9dea85`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:758b8a66cad8658e68c9e1a50f18f5a9fd13d99c9c20e0e3605324d40d34b940`  
		Last Modified: Tue, 30 Jul 2024 18:57:20 GMT  
		Size: 24.6 KB (24630 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0`

```console
$ docker pull odoo@sha256:240c850b917b1af805272d258fec5f9b28133cb384712a7901dee4ad73194240
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:c546d8bb579b3a5e9a0ef1e775f0e84cd6374321d1051671420b9bd44bfb2b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563937790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b89e9f6ee7507fe367c80c1d361670c7a2fbe66fac2e68137413934d4050b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=15.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=dca04f296736763d040f26c653bc11ae5020ccc6
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: ODOO_RELEASE=20240730 ODOO_SHA=dca04f296736763d040f26c653bc11ae5020ccc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: ODOO_RELEASE=20240730 ODOO_SHA=dca04f296736763d040f26c653bc11ae5020ccc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe01f5e701a011c965fa618067b47db6ed29efda3050fd23171d655425a19def`  
		Last Modified: Tue, 30 Jul 2024 18:57:24 GMT  
		Size: 220.3 MB (220281611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda8967bc6e2e4bc3c20c25579589b193692bfbcd956dbd4e562115cff643560`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 2.4 MB (2387198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cfef7dd992901bf6436ff1d832dce8729b5f0ae0909f5831a7ee40e8c33079`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 463.3 KB (463258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42537583f75ba6e278cda2e7a2a1ad629a9e0678d99c5563548cbedb6262abb2`  
		Last Modified: Tue, 30 Jul 2024 18:57:28 GMT  
		Size: 309.4 MB (309374958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5168384ce28c8fec5bf0ce1e6cd4d233ea44ea3f6b28cb9af015b9fadbb4152b`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817fcba3018d0c5fe3cdccd96b0f4a60042c5d5b7cfeb853220c357a5ce5a39d`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84c62ced73bbe1a69cc6ef51a48dc78bb688e5567e565b2cdbaade9b8b1cb5e`  
		Last Modified: Tue, 30 Jul 2024 18:57:22 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15a16b02774038e0df603bf313180c8128132f0dbedbf89156d36f9ddb11b89`  
		Last Modified: Tue, 30 Jul 2024 18:57:22 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0` - unknown; unknown

```console
$ docker pull odoo@sha256:faa581c115cb2d5ad0927e5e7e901648e95f8aa6d011c67df2d78bbae8a42dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d8c38e2431620882f7a227ad12b7cc93f588630aaba60e6828a7dfa0438490`

```dockerfile
```

-	Layers:
	-	`sha256:3949963452e8050e3b03ce91a247dbfb8b9bc63fc92364c135653cea4b9dea85`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:758b8a66cad8658e68c9e1a50f18f5a9fd13d99c9c20e0e3605324d40d34b940`  
		Last Modified: Tue, 30 Jul 2024 18:57:20 GMT  
		Size: 24.6 KB (24630 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0-20240730`

```console
$ docker pull odoo@sha256:240c850b917b1af805272d258fec5f9b28133cb384712a7901dee4ad73194240
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0-20240730` - linux; amd64

```console
$ docker pull odoo@sha256:c546d8bb579b3a5e9a0ef1e775f0e84cd6374321d1051671420b9bd44bfb2b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.9 MB (563937790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b89e9f6ee7507fe367c80c1d361670c7a2fbe66fac2e68137413934d4050b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=15.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=dca04f296736763d040f26c653bc11ae5020ccc6
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: ODOO_RELEASE=20240730 ODOO_SHA=dca04f296736763d040f26c653bc11ae5020ccc6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: ODOO_RELEASE=20240730 ODOO_SHA=dca04f296736763d040f26c653bc11ae5020ccc6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe01f5e701a011c965fa618067b47db6ed29efda3050fd23171d655425a19def`  
		Last Modified: Tue, 30 Jul 2024 18:57:24 GMT  
		Size: 220.3 MB (220281611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda8967bc6e2e4bc3c20c25579589b193692bfbcd956dbd4e562115cff643560`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 2.4 MB (2387198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cfef7dd992901bf6436ff1d832dce8729b5f0ae0909f5831a7ee40e8c33079`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 463.3 KB (463258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42537583f75ba6e278cda2e7a2a1ad629a9e0678d99c5563548cbedb6262abb2`  
		Last Modified: Tue, 30 Jul 2024 18:57:28 GMT  
		Size: 309.4 MB (309374958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5168384ce28c8fec5bf0ce1e6cd4d233ea44ea3f6b28cb9af015b9fadbb4152b`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817fcba3018d0c5fe3cdccd96b0f4a60042c5d5b7cfeb853220c357a5ce5a39d`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84c62ced73bbe1a69cc6ef51a48dc78bb688e5567e565b2cdbaade9b8b1cb5e`  
		Last Modified: Tue, 30 Jul 2024 18:57:22 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15a16b02774038e0df603bf313180c8128132f0dbedbf89156d36f9ddb11b89`  
		Last Modified: Tue, 30 Jul 2024 18:57:22 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0-20240730` - unknown; unknown

```console
$ docker pull odoo@sha256:faa581c115cb2d5ad0927e5e7e901648e95f8aa6d011c67df2d78bbae8a42dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34708174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d8c38e2431620882f7a227ad12b7cc93f588630aaba60e6828a7dfa0438490`

```dockerfile
```

-	Layers:
	-	`sha256:3949963452e8050e3b03ce91a247dbfb8b9bc63fc92364c135653cea4b9dea85`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 34.7 MB (34683544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:758b8a66cad8658e68c9e1a50f18f5a9fd13d99c9c20e0e3605324d40d34b940`  
		Last Modified: Tue, 30 Jul 2024 18:57:20 GMT  
		Size: 24.6 KB (24630 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16`

```console
$ docker pull odoo@sha256:5a1150a08ca404f3d2b2879f631bd0d9af0bc5b18a96eb09cd1617463bc0a94a
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
$ docker pull odoo@sha256:4fdcda28649de5559d7aa705b928e773f07f180ce578235e4e6de46d9cbaa88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583309497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f14a0250499af41a454d8059909dd1aec5ac0b54b5af1ec20e4716e76f02842`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec0c2700b643e40d62846e0f01429a6226007c8e952e8c3394679c34b69ecf7`  
		Last Modified: Tue, 30 Jul 2024 18:57:39 GMT  
		Size: 219.6 MB (219593126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f713d5395350bc37e7223b4d5f4e6161be258d6359e416c7699e04306dd7671c`  
		Last Modified: Tue, 30 Jul 2024 18:57:36 GMT  
		Size: 2.4 MB (2391057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7a4ada7089be8ff7ad92c84789ff4fead74f2697047c07362492ae09ee743`  
		Last Modified: Tue, 30 Jul 2024 18:57:36 GMT  
		Size: 463.3 KB (463267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3abdf803f110065270b71269497f95a7c1c46c8cbf318be3299b9370eb0a657`  
		Last Modified: Tue, 30 Jul 2024 18:57:40 GMT  
		Size: 329.4 MB (329431284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5168384ce28c8fec5bf0ce1e6cd4d233ea44ea3f6b28cb9af015b9fadbb4152b`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18e8c574e0e0d3e1b7000b125bbdf6be0d208035e507b904828acbc803c147f`  
		Last Modified: Tue, 30 Jul 2024 18:57:37 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afe2c8b6e03676d0172f63b5165fec9e018f0498cf265995b0efcf93c2318b6`  
		Last Modified: Tue, 30 Jul 2024 18:57:37 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c2d7ea496aa7d3e422741a05c8762d655a44e34c6533009425ad40722643e8`  
		Last Modified: Tue, 30 Jul 2024 18:57:38 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:d7fa6866e54afd8197071c2473b0694d46a39fe073265ff41f35f8c27627c098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38753049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49acac14aa2e8117dde98d5e7a5e928efd41d385c1633c29feffe32cd4cc0a48`

```dockerfile
```

-	Layers:
	-	`sha256:b992c8435ad6818079f6b4ed635bc68ad829d2aa4991a73376cb23323b458a5b`  
		Last Modified: Tue, 30 Jul 2024 18:57:36 GMT  
		Size: 38.7 MB (38726508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dffd138942ca39a816ce555d3db3b4cfffdad970b810c3f05fc62da128ef9c9`  
		Last Modified: Tue, 30 Jul 2024 18:57:36 GMT  
		Size: 26.5 KB (26541 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f0298f93fc6376da9c2f252b286cd843e2c0386dc550dd3923b6827356b0575e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.0 MB (578959158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b67ebb7eff0cdb44d7e5e9f31163bb7acaa3624ebb5f312b0b1472aebc69570`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:d6e3e23c0f1d64871f832f3ba10e325896f4d2c652335e189e3635ee468270a5`  
		Last Modified: Tue, 30 Jul 2024 19:08:21 GMT  
		Size: 329.1 MB (329122041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfdf8eb96e6b7cd4d87d617ad5e9ea4c2b93098a75caa8c17af8674fbd05519`  
		Last Modified: Tue, 30 Jul 2024 19:08:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d67368b645fb819f90e121196904cebccb2dad7c5e379a921f4b091b7acf8f`  
		Last Modified: Tue, 30 Jul 2024 19:08:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56ce5e13bac467f73041dbe6b0e080a8c3a1b0d209c7dac3dcc5f334539287a`  
		Last Modified: Tue, 30 Jul 2024 19:08:15 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2165e05d8be024e28a93eabb983981a37e862a91f1cad41fc22eef27b3f1e01e`  
		Last Modified: Tue, 30 Jul 2024 19:08:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:2428aeeef79168ea2953dc7d8e4551b95450907a5a6f692ad57808afb44a52e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38759819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2855e599c60d31494f98e64cdf5a98adbfbd460db71b3363c98837230475e920`

```dockerfile
```

-	Layers:
	-	`sha256:d1b40c108df0679904da271096bd6ecc76075a6c7f6515746453ce0eceb12468`  
		Last Modified: Tue, 30 Jul 2024 19:08:14 GMT  
		Size: 38.7 MB (38732980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68fa5642ab95f356ac9b5aa197a66933e70897a5cf556ed966a5a2d8a371c1fd`  
		Last Modified: Tue, 30 Jul 2024 19:08:13 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:0df71c234b4769a1089a904749bc4d7eb76d638add3fc0383b752ba3531de13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597891157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4bde6ae0bb908fd34b6c18862e1d61efe9d79896878f77b9b4159593831e7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:642ba0979d4c34e66627195cecd5ca3e5b8731507ffc8f370105c763fc8ef2b6`  
		Last Modified: Tue, 30 Jul 2024 19:17:26 GMT  
		Size: 330.9 MB (330895840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebecb40a2fec333679d83cc9bb0f6bdd799826223fb66b4b7c9bc2b25015852a`  
		Last Modified: Tue, 30 Jul 2024 19:17:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a88a8ff0c5f71e31edea1a5be1edbe264676a8bb0a24660c530ffed0f01c28a`  
		Last Modified: Tue, 30 Jul 2024 19:17:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c0997644ed8166f03a701e2e6a6c6b7fc6a51c0cebe81f186264b105cd43be`  
		Last Modified: Tue, 30 Jul 2024 19:17:05 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f79f5a4dd920988892e5017a6ba56b45cd032eab388240b4f0de1243a12ecd`  
		Last Modified: Tue, 30 Jul 2024 19:17:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:45fbb7323b88934b7aa3f1a0af25d11385fbfbcff5f697325818abe8df6a14dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38761232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0464538a1ebba55c7233c3a4892ee72fd5acceaa4897b6abe339f482f9b04c72`

```dockerfile
```

-	Layers:
	-	`sha256:8dc974a1f6f813c8ba02e8fc21e64f520f64f53c36632511ad10b503d766c89d`  
		Last Modified: Tue, 30 Jul 2024 19:17:06 GMT  
		Size: 38.7 MB (38734640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46bbaba687795b603e81c3bbe90f5a1934bc91839bccdc6379b02f998c17a1d5`  
		Last Modified: Tue, 30 Jul 2024 19:17:02 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:5a1150a08ca404f3d2b2879f631bd0d9af0bc5b18a96eb09cd1617463bc0a94a
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
$ docker pull odoo@sha256:4fdcda28649de5559d7aa705b928e773f07f180ce578235e4e6de46d9cbaa88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583309497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f14a0250499af41a454d8059909dd1aec5ac0b54b5af1ec20e4716e76f02842`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec0c2700b643e40d62846e0f01429a6226007c8e952e8c3394679c34b69ecf7`  
		Last Modified: Tue, 30 Jul 2024 18:57:39 GMT  
		Size: 219.6 MB (219593126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f713d5395350bc37e7223b4d5f4e6161be258d6359e416c7699e04306dd7671c`  
		Last Modified: Tue, 30 Jul 2024 18:57:36 GMT  
		Size: 2.4 MB (2391057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7a4ada7089be8ff7ad92c84789ff4fead74f2697047c07362492ae09ee743`  
		Last Modified: Tue, 30 Jul 2024 18:57:36 GMT  
		Size: 463.3 KB (463267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3abdf803f110065270b71269497f95a7c1c46c8cbf318be3299b9370eb0a657`  
		Last Modified: Tue, 30 Jul 2024 18:57:40 GMT  
		Size: 329.4 MB (329431284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5168384ce28c8fec5bf0ce1e6cd4d233ea44ea3f6b28cb9af015b9fadbb4152b`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18e8c574e0e0d3e1b7000b125bbdf6be0d208035e507b904828acbc803c147f`  
		Last Modified: Tue, 30 Jul 2024 18:57:37 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afe2c8b6e03676d0172f63b5165fec9e018f0498cf265995b0efcf93c2318b6`  
		Last Modified: Tue, 30 Jul 2024 18:57:37 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c2d7ea496aa7d3e422741a05c8762d655a44e34c6533009425ad40722643e8`  
		Last Modified: Tue, 30 Jul 2024 18:57:38 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d7fa6866e54afd8197071c2473b0694d46a39fe073265ff41f35f8c27627c098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38753049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49acac14aa2e8117dde98d5e7a5e928efd41d385c1633c29feffe32cd4cc0a48`

```dockerfile
```

-	Layers:
	-	`sha256:b992c8435ad6818079f6b4ed635bc68ad829d2aa4991a73376cb23323b458a5b`  
		Last Modified: Tue, 30 Jul 2024 18:57:36 GMT  
		Size: 38.7 MB (38726508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dffd138942ca39a816ce555d3db3b4cfffdad970b810c3f05fc62da128ef9c9`  
		Last Modified: Tue, 30 Jul 2024 18:57:36 GMT  
		Size: 26.5 KB (26541 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f0298f93fc6376da9c2f252b286cd843e2c0386dc550dd3923b6827356b0575e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.0 MB (578959158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b67ebb7eff0cdb44d7e5e9f31163bb7acaa3624ebb5f312b0b1472aebc69570`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:d6e3e23c0f1d64871f832f3ba10e325896f4d2c652335e189e3635ee468270a5`  
		Last Modified: Tue, 30 Jul 2024 19:08:21 GMT  
		Size: 329.1 MB (329122041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfdf8eb96e6b7cd4d87d617ad5e9ea4c2b93098a75caa8c17af8674fbd05519`  
		Last Modified: Tue, 30 Jul 2024 19:08:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d67368b645fb819f90e121196904cebccb2dad7c5e379a921f4b091b7acf8f`  
		Last Modified: Tue, 30 Jul 2024 19:08:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56ce5e13bac467f73041dbe6b0e080a8c3a1b0d209c7dac3dcc5f334539287a`  
		Last Modified: Tue, 30 Jul 2024 19:08:15 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2165e05d8be024e28a93eabb983981a37e862a91f1cad41fc22eef27b3f1e01e`  
		Last Modified: Tue, 30 Jul 2024 19:08:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2428aeeef79168ea2953dc7d8e4551b95450907a5a6f692ad57808afb44a52e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38759819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2855e599c60d31494f98e64cdf5a98adbfbd460db71b3363c98837230475e920`

```dockerfile
```

-	Layers:
	-	`sha256:d1b40c108df0679904da271096bd6ecc76075a6c7f6515746453ce0eceb12468`  
		Last Modified: Tue, 30 Jul 2024 19:08:14 GMT  
		Size: 38.7 MB (38732980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68fa5642ab95f356ac9b5aa197a66933e70897a5cf556ed966a5a2d8a371c1fd`  
		Last Modified: Tue, 30 Jul 2024 19:08:13 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:0df71c234b4769a1089a904749bc4d7eb76d638add3fc0383b752ba3531de13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597891157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4bde6ae0bb908fd34b6c18862e1d61efe9d79896878f77b9b4159593831e7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:642ba0979d4c34e66627195cecd5ca3e5b8731507ffc8f370105c763fc8ef2b6`  
		Last Modified: Tue, 30 Jul 2024 19:17:26 GMT  
		Size: 330.9 MB (330895840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebecb40a2fec333679d83cc9bb0f6bdd799826223fb66b4b7c9bc2b25015852a`  
		Last Modified: Tue, 30 Jul 2024 19:17:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a88a8ff0c5f71e31edea1a5be1edbe264676a8bb0a24660c530ffed0f01c28a`  
		Last Modified: Tue, 30 Jul 2024 19:17:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c0997644ed8166f03a701e2e6a6c6b7fc6a51c0cebe81f186264b105cd43be`  
		Last Modified: Tue, 30 Jul 2024 19:17:05 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f79f5a4dd920988892e5017a6ba56b45cd032eab388240b4f0de1243a12ecd`  
		Last Modified: Tue, 30 Jul 2024 19:17:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:45fbb7323b88934b7aa3f1a0af25d11385fbfbcff5f697325818abe8df6a14dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38761232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0464538a1ebba55c7233c3a4892ee72fd5acceaa4897b6abe339f482f9b04c72`

```dockerfile
```

-	Layers:
	-	`sha256:8dc974a1f6f813c8ba02e8fc21e64f520f64f53c36632511ad10b503d766c89d`  
		Last Modified: Tue, 30 Jul 2024 19:17:06 GMT  
		Size: 38.7 MB (38734640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46bbaba687795b603e81c3bbe90f5a1934bc91839bccdc6379b02f998c17a1d5`  
		Last Modified: Tue, 30 Jul 2024 19:17:02 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20240730`

```console
$ docker pull odoo@sha256:5a1150a08ca404f3d2b2879f631bd0d9af0bc5b18a96eb09cd1617463bc0a94a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0-20240730` - linux; amd64

```console
$ docker pull odoo@sha256:4fdcda28649de5559d7aa705b928e773f07f180ce578235e4e6de46d9cbaa88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583309497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f14a0250499af41a454d8059909dd1aec5ac0b54b5af1ec20e4716e76f02842`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec0c2700b643e40d62846e0f01429a6226007c8e952e8c3394679c34b69ecf7`  
		Last Modified: Tue, 30 Jul 2024 18:57:39 GMT  
		Size: 219.6 MB (219593126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f713d5395350bc37e7223b4d5f4e6161be258d6359e416c7699e04306dd7671c`  
		Last Modified: Tue, 30 Jul 2024 18:57:36 GMT  
		Size: 2.4 MB (2391057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7a4ada7089be8ff7ad92c84789ff4fead74f2697047c07362492ae09ee743`  
		Last Modified: Tue, 30 Jul 2024 18:57:36 GMT  
		Size: 463.3 KB (463267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3abdf803f110065270b71269497f95a7c1c46c8cbf318be3299b9370eb0a657`  
		Last Modified: Tue, 30 Jul 2024 18:57:40 GMT  
		Size: 329.4 MB (329431284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5168384ce28c8fec5bf0ce1e6cd4d233ea44ea3f6b28cb9af015b9fadbb4152b`  
		Last Modified: Tue, 30 Jul 2024 18:57:21 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18e8c574e0e0d3e1b7000b125bbdf6be0d208035e507b904828acbc803c147f`  
		Last Modified: Tue, 30 Jul 2024 18:57:37 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afe2c8b6e03676d0172f63b5165fec9e018f0498cf265995b0efcf93c2318b6`  
		Last Modified: Tue, 30 Jul 2024 18:57:37 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c2d7ea496aa7d3e422741a05c8762d655a44e34c6533009425ad40722643e8`  
		Last Modified: Tue, 30 Jul 2024 18:57:38 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240730` - unknown; unknown

```console
$ docker pull odoo@sha256:d7fa6866e54afd8197071c2473b0694d46a39fe073265ff41f35f8c27627c098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38753049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49acac14aa2e8117dde98d5e7a5e928efd41d385c1633c29feffe32cd4cc0a48`

```dockerfile
```

-	Layers:
	-	`sha256:b992c8435ad6818079f6b4ed635bc68ad829d2aa4991a73376cb23323b458a5b`  
		Last Modified: Tue, 30 Jul 2024 18:57:36 GMT  
		Size: 38.7 MB (38726508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dffd138942ca39a816ce555d3db3b4cfffdad970b810c3f05fc62da128ef9c9`  
		Last Modified: Tue, 30 Jul 2024 18:57:36 GMT  
		Size: 26.5 KB (26541 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240730` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f0298f93fc6376da9c2f252b286cd843e2c0386dc550dd3923b6827356b0575e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.0 MB (578959158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b67ebb7eff0cdb44d7e5e9f31163bb7acaa3624ebb5f312b0b1472aebc69570`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:d6e3e23c0f1d64871f832f3ba10e325896f4d2c652335e189e3635ee468270a5`  
		Last Modified: Tue, 30 Jul 2024 19:08:21 GMT  
		Size: 329.1 MB (329122041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfdf8eb96e6b7cd4d87d617ad5e9ea4c2b93098a75caa8c17af8674fbd05519`  
		Last Modified: Tue, 30 Jul 2024 19:08:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d67368b645fb819f90e121196904cebccb2dad7c5e379a921f4b091b7acf8f`  
		Last Modified: Tue, 30 Jul 2024 19:08:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56ce5e13bac467f73041dbe6b0e080a8c3a1b0d209c7dac3dcc5f334539287a`  
		Last Modified: Tue, 30 Jul 2024 19:08:15 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2165e05d8be024e28a93eabb983981a37e862a91f1cad41fc22eef27b3f1e01e`  
		Last Modified: Tue, 30 Jul 2024 19:08:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240730` - unknown; unknown

```console
$ docker pull odoo@sha256:2428aeeef79168ea2953dc7d8e4551b95450907a5a6f692ad57808afb44a52e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38759819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2855e599c60d31494f98e64cdf5a98adbfbd460db71b3363c98837230475e920`

```dockerfile
```

-	Layers:
	-	`sha256:d1b40c108df0679904da271096bd6ecc76075a6c7f6515746453ce0eceb12468`  
		Last Modified: Tue, 30 Jul 2024 19:08:14 GMT  
		Size: 38.7 MB (38732980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68fa5642ab95f356ac9b5aa197a66933e70897a5cf556ed966a5a2d8a371c1fd`  
		Last Modified: Tue, 30 Jul 2024 19:08:13 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240730` - linux; ppc64le

```console
$ docker pull odoo@sha256:0df71c234b4769a1089a904749bc4d7eb76d638add3fc0383b752ba3531de13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597891157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4bde6ae0bb908fd34b6c18862e1d61efe9d79896878f77b9b4159593831e7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=C.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=16.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=05d42e6d53eb45df40abf82d3e60c42dead0ec05
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:642ba0979d4c34e66627195cecd5ca3e5b8731507ffc8f370105c763fc8ef2b6`  
		Last Modified: Tue, 30 Jul 2024 19:17:26 GMT  
		Size: 330.9 MB (330895840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebecb40a2fec333679d83cc9bb0f6bdd799826223fb66b4b7c9bc2b25015852a`  
		Last Modified: Tue, 30 Jul 2024 19:17:04 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a88a8ff0c5f71e31edea1a5be1edbe264676a8bb0a24660c530ffed0f01c28a`  
		Last Modified: Tue, 30 Jul 2024 19:17:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c0997644ed8166f03a701e2e6a6c6b7fc6a51c0cebe81f186264b105cd43be`  
		Last Modified: Tue, 30 Jul 2024 19:17:05 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f79f5a4dd920988892e5017a6ba56b45cd032eab388240b4f0de1243a12ecd`  
		Last Modified: Tue, 30 Jul 2024 19:17:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240730` - unknown; unknown

```console
$ docker pull odoo@sha256:45fbb7323b88934b7aa3f1a0af25d11385fbfbcff5f697325818abe8df6a14dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38761232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0464538a1ebba55c7233c3a4892ee72fd5acceaa4897b6abe339f482f9b04c72`

```dockerfile
```

-	Layers:
	-	`sha256:8dc974a1f6f813c8ba02e8fc21e64f520f64f53c36632511ad10b503d766c89d`  
		Last Modified: Tue, 30 Jul 2024 19:17:06 GMT  
		Size: 38.7 MB (38734640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46bbaba687795b603e81c3bbe90f5a1934bc91839bccdc6379b02f998c17a1d5`  
		Last Modified: Tue, 30 Jul 2024 19:17:02 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:3178ddce5bf9e6d731eca2d4ce50ee539f7ed33be1030eb4ac435f0200d002b9
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
$ docker pull odoo@sha256:b1c74621a306e959bf3689df57f10b9989a9188178d93deb38118cd42c987b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.1 MB (595074176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d65dac06b781c222698ff4ae95d0e331ecefc9c15e441d529b3f3db2b206ac`
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
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28e32c95f92e4eff7f1bbc4324656f715b02173e58c4e8c75da3d73051622ea`  
		Last Modified: Tue, 30 Jul 2024 18:58:16 GMT  
		Size: 233.7 MB (233741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d883fb716564ffd9b8e4320f78e19849addc684badddd64e5cd1a8dcb1e366`  
		Last Modified: Tue, 30 Jul 2024 18:58:11 GMT  
		Size: 2.3 MB (2313693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9121c9c1fa951d2dbd6239d37a4478e76015b536b145a2044ea6568e35128f5c`  
		Last Modified: Tue, 30 Jul 2024 18:58:11 GMT  
		Size: 464.4 KB (464375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19d9c109c6ddc292b315bd28fb1f7dc1e033229d5deec304e4c9d6427fc735b`  
		Last Modified: Tue, 30 Jul 2024 18:58:18 GMT  
		Size: 329.0 MB (329018048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc07e5ea345af659a3a488944cda6f49a136846f2ec52344d4ca195282e0e77`  
		Last Modified: Tue, 30 Jul 2024 18:58:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99376f4e8c4ee9956d771daa521361e206b8294b87818baec58df28c86a82294`  
		Last Modified: Tue, 30 Jul 2024 18:58:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324874f6fe6b81f3f8dc83bb7c7dcf1c0d1cbc65572507cc7efefff18b669c4d`  
		Last Modified: Tue, 30 Jul 2024 18:58:13 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59303977753304931170312b2145e7119e22343c913c8f1fc9a3f628ff4ae99`  
		Last Modified: Tue, 30 Jul 2024 18:58:13 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:91053b05d03aab9d743a446bb0832c34d7003dc3512b3f1ca88eeaf4cc8b1820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38945351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448fa029983f0ec31c39adced736e47d02a1b4d56ad66c4752c131a595112660`

```dockerfile
```

-	Layers:
	-	`sha256:b9bf4b53ce425cd163e838a934cb7855de2e58e7c6fb5ebe6ccb2a54bf39d57a`  
		Last Modified: Tue, 30 Jul 2024 18:58:12 GMT  
		Size: 38.9 MB (38918476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b597c8a23f91a036dab5f70e92b93830652fef3f83a39c17e2acf532fe1c2c9`  
		Last Modified: Tue, 30 Jul 2024 18:58:11 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:241ce1efff5c53b72418eb0d728af55c14fdee68f5a2052a8707cf9d87a2edeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.9 MB (589880352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a1515061046a4f9d536be5a8b3374ee1efbcc83c7d3572d9b14e1c80e6e567`
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
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:fdead12f9d64c538db2043034966e7659df8e6076bd0a0183e3375dc6d9fa008`  
		Last Modified: Tue, 30 Jul 2024 19:04:30 GMT  
		Size: 328.6 MB (328630882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6f4b22a3a04ac44d9a6cb2381be9a135a8b5d2ef0a6fb7fed1bc38be675fd2`  
		Last Modified: Tue, 30 Jul 2024 19:04:22 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cf3b62b4870ce9aa1316a8733bccf55086f4021d491b5ae43a8197ef5f8c1a`  
		Last Modified: Tue, 30 Jul 2024 19:04:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416d78b3bda60853bcb56477f26cfe573253f2cad2f8b21d1b78cdf8ebb63d65`  
		Last Modified: Tue, 30 Jul 2024 19:04:24 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce5ffc27a05a903baca991f44a2ebc89b8f4392d6f2ebf0a60479be3c1f3c03`  
		Last Modified: Tue, 30 Jul 2024 19:04:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:9be14fc5c89bc2869ff4811c0e635f13c064e1cab69455851fa7b316d4741caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38952177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19c45003b0681edbb59c14d2a8cd184a2a03475bd606bef1ea15ab5a4e7591a`

```dockerfile
```

-	Layers:
	-	`sha256:f2bea5159b966efdb29b235732e681a8854b3c15b6728753d6333d28617ab6ce`  
		Last Modified: Tue, 30 Jul 2024 19:04:22 GMT  
		Size: 38.9 MB (38925001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:668bdfa61810ff6e3b8c91620c1bf7e39f581977e16eca8651b51ddb25a3819e`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:91596bae158fd34e956869246d6ddd752c3907ebb34b91ce717062c0fb109420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.5 MB (611543442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc38c4ecfdfe15c105a128f787ba8f190104e51ee291a681bd831da6ff8c78c2`
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
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:a972096075db8310fcdf24f4f5076aa1227e577d34224373e31ccb99902d9346`  
		Last Modified: Tue, 30 Jul 2024 19:08:56 GMT  
		Size: 330.7 MB (330746328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e615e282056774e9d08ffb0b0b4e5154a53ed5d59488c367757a53787160eca1`  
		Last Modified: Tue, 30 Jul 2024 19:08:32 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da72434b849df9ea36f1ee0221ea15ed89809ad6d96c83774b22959a0d772635`  
		Last Modified: Tue, 30 Jul 2024 19:08:32 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bf1c6522a09c10575db194d3aeee7754bf38c5554406845eb5f321dcd6d397`  
		Last Modified: Tue, 30 Jul 2024 19:08:33 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00939a7d5f47bd65842b73247761da3836db97b7e1163e3e4504ef772575f397`  
		Last Modified: Tue, 30 Jul 2024 19:08:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:b965ac61d519922c3b857dd99774d4a31688141c6f5a9a8204fbbe8a553e2922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38953720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232194819aa1bee15bcff6a263b6bc573fd3177a3535ea01fde135af59b107a9`

```dockerfile
```

-	Layers:
	-	`sha256:55afa35b56a010a805e5008ee433e1df7910630cd826a8615e829feea4accbeb`  
		Last Modified: Tue, 30 Jul 2024 19:08:32 GMT  
		Size: 38.9 MB (38926789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ba84a640b332eb88eb7e4a504940a0f2632fe3145c290887f9af2662bb9ae7e`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:3178ddce5bf9e6d731eca2d4ce50ee539f7ed33be1030eb4ac435f0200d002b9
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
$ docker pull odoo@sha256:b1c74621a306e959bf3689df57f10b9989a9188178d93deb38118cd42c987b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.1 MB (595074176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d65dac06b781c222698ff4ae95d0e331ecefc9c15e441d529b3f3db2b206ac`
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
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28e32c95f92e4eff7f1bbc4324656f715b02173e58c4e8c75da3d73051622ea`  
		Last Modified: Tue, 30 Jul 2024 18:58:16 GMT  
		Size: 233.7 MB (233741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d883fb716564ffd9b8e4320f78e19849addc684badddd64e5cd1a8dcb1e366`  
		Last Modified: Tue, 30 Jul 2024 18:58:11 GMT  
		Size: 2.3 MB (2313693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9121c9c1fa951d2dbd6239d37a4478e76015b536b145a2044ea6568e35128f5c`  
		Last Modified: Tue, 30 Jul 2024 18:58:11 GMT  
		Size: 464.4 KB (464375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19d9c109c6ddc292b315bd28fb1f7dc1e033229d5deec304e4c9d6427fc735b`  
		Last Modified: Tue, 30 Jul 2024 18:58:18 GMT  
		Size: 329.0 MB (329018048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc07e5ea345af659a3a488944cda6f49a136846f2ec52344d4ca195282e0e77`  
		Last Modified: Tue, 30 Jul 2024 18:58:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99376f4e8c4ee9956d771daa521361e206b8294b87818baec58df28c86a82294`  
		Last Modified: Tue, 30 Jul 2024 18:58:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324874f6fe6b81f3f8dc83bb7c7dcf1c0d1cbc65572507cc7efefff18b669c4d`  
		Last Modified: Tue, 30 Jul 2024 18:58:13 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59303977753304931170312b2145e7119e22343c913c8f1fc9a3f628ff4ae99`  
		Last Modified: Tue, 30 Jul 2024 18:58:13 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:91053b05d03aab9d743a446bb0832c34d7003dc3512b3f1ca88eeaf4cc8b1820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38945351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448fa029983f0ec31c39adced736e47d02a1b4d56ad66c4752c131a595112660`

```dockerfile
```

-	Layers:
	-	`sha256:b9bf4b53ce425cd163e838a934cb7855de2e58e7c6fb5ebe6ccb2a54bf39d57a`  
		Last Modified: Tue, 30 Jul 2024 18:58:12 GMT  
		Size: 38.9 MB (38918476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b597c8a23f91a036dab5f70e92b93830652fef3f83a39c17e2acf532fe1c2c9`  
		Last Modified: Tue, 30 Jul 2024 18:58:11 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:241ce1efff5c53b72418eb0d728af55c14fdee68f5a2052a8707cf9d87a2edeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.9 MB (589880352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a1515061046a4f9d536be5a8b3374ee1efbcc83c7d3572d9b14e1c80e6e567`
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
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:fdead12f9d64c538db2043034966e7659df8e6076bd0a0183e3375dc6d9fa008`  
		Last Modified: Tue, 30 Jul 2024 19:04:30 GMT  
		Size: 328.6 MB (328630882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6f4b22a3a04ac44d9a6cb2381be9a135a8b5d2ef0a6fb7fed1bc38be675fd2`  
		Last Modified: Tue, 30 Jul 2024 19:04:22 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cf3b62b4870ce9aa1316a8733bccf55086f4021d491b5ae43a8197ef5f8c1a`  
		Last Modified: Tue, 30 Jul 2024 19:04:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416d78b3bda60853bcb56477f26cfe573253f2cad2f8b21d1b78cdf8ebb63d65`  
		Last Modified: Tue, 30 Jul 2024 19:04:24 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce5ffc27a05a903baca991f44a2ebc89b8f4392d6f2ebf0a60479be3c1f3c03`  
		Last Modified: Tue, 30 Jul 2024 19:04:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9be14fc5c89bc2869ff4811c0e635f13c064e1cab69455851fa7b316d4741caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38952177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19c45003b0681edbb59c14d2a8cd184a2a03475bd606bef1ea15ab5a4e7591a`

```dockerfile
```

-	Layers:
	-	`sha256:f2bea5159b966efdb29b235732e681a8854b3c15b6728753d6333d28617ab6ce`  
		Last Modified: Tue, 30 Jul 2024 19:04:22 GMT  
		Size: 38.9 MB (38925001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:668bdfa61810ff6e3b8c91620c1bf7e39f581977e16eca8651b51ddb25a3819e`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:91596bae158fd34e956869246d6ddd752c3907ebb34b91ce717062c0fb109420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.5 MB (611543442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc38c4ecfdfe15c105a128f787ba8f190104e51ee291a681bd831da6ff8c78c2`
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
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:a972096075db8310fcdf24f4f5076aa1227e577d34224373e31ccb99902d9346`  
		Last Modified: Tue, 30 Jul 2024 19:08:56 GMT  
		Size: 330.7 MB (330746328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e615e282056774e9d08ffb0b0b4e5154a53ed5d59488c367757a53787160eca1`  
		Last Modified: Tue, 30 Jul 2024 19:08:32 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da72434b849df9ea36f1ee0221ea15ed89809ad6d96c83774b22959a0d772635`  
		Last Modified: Tue, 30 Jul 2024 19:08:32 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bf1c6522a09c10575db194d3aeee7754bf38c5554406845eb5f321dcd6d397`  
		Last Modified: Tue, 30 Jul 2024 19:08:33 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00939a7d5f47bd65842b73247761da3836db97b7e1163e3e4504ef772575f397`  
		Last Modified: Tue, 30 Jul 2024 19:08:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b965ac61d519922c3b857dd99774d4a31688141c6f5a9a8204fbbe8a553e2922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38953720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232194819aa1bee15bcff6a263b6bc573fd3177a3535ea01fde135af59b107a9`

```dockerfile
```

-	Layers:
	-	`sha256:55afa35b56a010a805e5008ee433e1df7910630cd826a8615e829feea4accbeb`  
		Last Modified: Tue, 30 Jul 2024 19:08:32 GMT  
		Size: 38.9 MB (38926789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ba84a640b332eb88eb7e4a504940a0f2632fe3145c290887f9af2662bb9ae7e`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240730`

```console
$ docker pull odoo@sha256:3178ddce5bf9e6d731eca2d4ce50ee539f7ed33be1030eb4ac435f0200d002b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20240730` - linux; amd64

```console
$ docker pull odoo@sha256:b1c74621a306e959bf3689df57f10b9989a9188178d93deb38118cd42c987b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.1 MB (595074176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d65dac06b781c222698ff4ae95d0e331ecefc9c15e441d529b3f3db2b206ac`
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
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28e32c95f92e4eff7f1bbc4324656f715b02173e58c4e8c75da3d73051622ea`  
		Last Modified: Tue, 30 Jul 2024 18:58:16 GMT  
		Size: 233.7 MB (233741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d883fb716564ffd9b8e4320f78e19849addc684badddd64e5cd1a8dcb1e366`  
		Last Modified: Tue, 30 Jul 2024 18:58:11 GMT  
		Size: 2.3 MB (2313693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9121c9c1fa951d2dbd6239d37a4478e76015b536b145a2044ea6568e35128f5c`  
		Last Modified: Tue, 30 Jul 2024 18:58:11 GMT  
		Size: 464.4 KB (464375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19d9c109c6ddc292b315bd28fb1f7dc1e033229d5deec304e4c9d6427fc735b`  
		Last Modified: Tue, 30 Jul 2024 18:58:18 GMT  
		Size: 329.0 MB (329018048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc07e5ea345af659a3a488944cda6f49a136846f2ec52344d4ca195282e0e77`  
		Last Modified: Tue, 30 Jul 2024 18:58:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99376f4e8c4ee9956d771daa521361e206b8294b87818baec58df28c86a82294`  
		Last Modified: Tue, 30 Jul 2024 18:58:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324874f6fe6b81f3f8dc83bb7c7dcf1c0d1cbc65572507cc7efefff18b669c4d`  
		Last Modified: Tue, 30 Jul 2024 18:58:13 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59303977753304931170312b2145e7119e22343c913c8f1fc9a3f628ff4ae99`  
		Last Modified: Tue, 30 Jul 2024 18:58:13 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240730` - unknown; unknown

```console
$ docker pull odoo@sha256:91053b05d03aab9d743a446bb0832c34d7003dc3512b3f1ca88eeaf4cc8b1820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38945351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448fa029983f0ec31c39adced736e47d02a1b4d56ad66c4752c131a595112660`

```dockerfile
```

-	Layers:
	-	`sha256:b9bf4b53ce425cd163e838a934cb7855de2e58e7c6fb5ebe6ccb2a54bf39d57a`  
		Last Modified: Tue, 30 Jul 2024 18:58:12 GMT  
		Size: 38.9 MB (38918476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b597c8a23f91a036dab5f70e92b93830652fef3f83a39c17e2acf532fe1c2c9`  
		Last Modified: Tue, 30 Jul 2024 18:58:11 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240730` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:241ce1efff5c53b72418eb0d728af55c14fdee68f5a2052a8707cf9d87a2edeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.9 MB (589880352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a1515061046a4f9d536be5a8b3374ee1efbcc83c7d3572d9b14e1c80e6e567`
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
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:fdead12f9d64c538db2043034966e7659df8e6076bd0a0183e3375dc6d9fa008`  
		Last Modified: Tue, 30 Jul 2024 19:04:30 GMT  
		Size: 328.6 MB (328630882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6f4b22a3a04ac44d9a6cb2381be9a135a8b5d2ef0a6fb7fed1bc38be675fd2`  
		Last Modified: Tue, 30 Jul 2024 19:04:22 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cf3b62b4870ce9aa1316a8733bccf55086f4021d491b5ae43a8197ef5f8c1a`  
		Last Modified: Tue, 30 Jul 2024 19:04:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416d78b3bda60853bcb56477f26cfe573253f2cad2f8b21d1b78cdf8ebb63d65`  
		Last Modified: Tue, 30 Jul 2024 19:04:24 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce5ffc27a05a903baca991f44a2ebc89b8f4392d6f2ebf0a60479be3c1f3c03`  
		Last Modified: Tue, 30 Jul 2024 19:04:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240730` - unknown; unknown

```console
$ docker pull odoo@sha256:9be14fc5c89bc2869ff4811c0e635f13c064e1cab69455851fa7b316d4741caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38952177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19c45003b0681edbb59c14d2a8cd184a2a03475bd606bef1ea15ab5a4e7591a`

```dockerfile
```

-	Layers:
	-	`sha256:f2bea5159b966efdb29b235732e681a8854b3c15b6728753d6333d28617ab6ce`  
		Last Modified: Tue, 30 Jul 2024 19:04:22 GMT  
		Size: 38.9 MB (38925001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:668bdfa61810ff6e3b8c91620c1bf7e39f581977e16eca8651b51ddb25a3819e`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240730` - linux; ppc64le

```console
$ docker pull odoo@sha256:91596bae158fd34e956869246d6ddd752c3907ebb34b91ce717062c0fb109420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.5 MB (611543442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc38c4ecfdfe15c105a128f787ba8f190104e51ee291a681bd831da6ff8c78c2`
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
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:a972096075db8310fcdf24f4f5076aa1227e577d34224373e31ccb99902d9346`  
		Last Modified: Tue, 30 Jul 2024 19:08:56 GMT  
		Size: 330.7 MB (330746328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e615e282056774e9d08ffb0b0b4e5154a53ed5d59488c367757a53787160eca1`  
		Last Modified: Tue, 30 Jul 2024 19:08:32 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da72434b849df9ea36f1ee0221ea15ed89809ad6d96c83774b22959a0d772635`  
		Last Modified: Tue, 30 Jul 2024 19:08:32 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bf1c6522a09c10575db194d3aeee7754bf38c5554406845eb5f321dcd6d397`  
		Last Modified: Tue, 30 Jul 2024 19:08:33 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00939a7d5f47bd65842b73247761da3836db97b7e1163e3e4504ef772575f397`  
		Last Modified: Tue, 30 Jul 2024 19:08:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240730` - unknown; unknown

```console
$ docker pull odoo@sha256:b965ac61d519922c3b857dd99774d4a31688141c6f5a9a8204fbbe8a553e2922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38953720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232194819aa1bee15bcff6a263b6bc573fd3177a3535ea01fde135af59b107a9`

```dockerfile
```

-	Layers:
	-	`sha256:55afa35b56a010a805e5008ee433e1df7910630cd826a8615e829feea4accbeb`  
		Last Modified: Tue, 30 Jul 2024 19:08:32 GMT  
		Size: 38.9 MB (38926789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ba84a640b332eb88eb7e4a504940a0f2632fe3145c290887f9af2662bb9ae7e`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:3178ddce5bf9e6d731eca2d4ce50ee539f7ed33be1030eb4ac435f0200d002b9
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
$ docker pull odoo@sha256:b1c74621a306e959bf3689df57f10b9989a9188178d93deb38118cd42c987b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.1 MB (595074176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d65dac06b781c222698ff4ae95d0e331ecefc9c15e441d529b3f3db2b206ac`
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
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28e32c95f92e4eff7f1bbc4324656f715b02173e58c4e8c75da3d73051622ea`  
		Last Modified: Tue, 30 Jul 2024 18:58:16 GMT  
		Size: 233.7 MB (233741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d883fb716564ffd9b8e4320f78e19849addc684badddd64e5cd1a8dcb1e366`  
		Last Modified: Tue, 30 Jul 2024 18:58:11 GMT  
		Size: 2.3 MB (2313693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9121c9c1fa951d2dbd6239d37a4478e76015b536b145a2044ea6568e35128f5c`  
		Last Modified: Tue, 30 Jul 2024 18:58:11 GMT  
		Size: 464.4 KB (464375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19d9c109c6ddc292b315bd28fb1f7dc1e033229d5deec304e4c9d6427fc735b`  
		Last Modified: Tue, 30 Jul 2024 18:58:18 GMT  
		Size: 329.0 MB (329018048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc07e5ea345af659a3a488944cda6f49a136846f2ec52344d4ca195282e0e77`  
		Last Modified: Tue, 30 Jul 2024 18:58:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99376f4e8c4ee9956d771daa521361e206b8294b87818baec58df28c86a82294`  
		Last Modified: Tue, 30 Jul 2024 18:58:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324874f6fe6b81f3f8dc83bb7c7dcf1c0d1cbc65572507cc7efefff18b669c4d`  
		Last Modified: Tue, 30 Jul 2024 18:58:13 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59303977753304931170312b2145e7119e22343c913c8f1fc9a3f628ff4ae99`  
		Last Modified: Tue, 30 Jul 2024 18:58:13 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:91053b05d03aab9d743a446bb0832c34d7003dc3512b3f1ca88eeaf4cc8b1820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38945351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448fa029983f0ec31c39adced736e47d02a1b4d56ad66c4752c131a595112660`

```dockerfile
```

-	Layers:
	-	`sha256:b9bf4b53ce425cd163e838a934cb7855de2e58e7c6fb5ebe6ccb2a54bf39d57a`  
		Last Modified: Tue, 30 Jul 2024 18:58:12 GMT  
		Size: 38.9 MB (38918476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b597c8a23f91a036dab5f70e92b93830652fef3f83a39c17e2acf532fe1c2c9`  
		Last Modified: Tue, 30 Jul 2024 18:58:11 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:241ce1efff5c53b72418eb0d728af55c14fdee68f5a2052a8707cf9d87a2edeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.9 MB (589880352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a1515061046a4f9d536be5a8b3374ee1efbcc83c7d3572d9b14e1c80e6e567`
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
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:fdead12f9d64c538db2043034966e7659df8e6076bd0a0183e3375dc6d9fa008`  
		Last Modified: Tue, 30 Jul 2024 19:04:30 GMT  
		Size: 328.6 MB (328630882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6f4b22a3a04ac44d9a6cb2381be9a135a8b5d2ef0a6fb7fed1bc38be675fd2`  
		Last Modified: Tue, 30 Jul 2024 19:04:22 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cf3b62b4870ce9aa1316a8733bccf55086f4021d491b5ae43a8197ef5f8c1a`  
		Last Modified: Tue, 30 Jul 2024 19:04:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416d78b3bda60853bcb56477f26cfe573253f2cad2f8b21d1b78cdf8ebb63d65`  
		Last Modified: Tue, 30 Jul 2024 19:04:24 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce5ffc27a05a903baca991f44a2ebc89b8f4392d6f2ebf0a60479be3c1f3c03`  
		Last Modified: Tue, 30 Jul 2024 19:04:24 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:9be14fc5c89bc2869ff4811c0e635f13c064e1cab69455851fa7b316d4741caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38952177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19c45003b0681edbb59c14d2a8cd184a2a03475bd606bef1ea15ab5a4e7591a`

```dockerfile
```

-	Layers:
	-	`sha256:f2bea5159b966efdb29b235732e681a8854b3c15b6728753d6333d28617ab6ce`  
		Last Modified: Tue, 30 Jul 2024 19:04:22 GMT  
		Size: 38.9 MB (38925001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:668bdfa61810ff6e3b8c91620c1bf7e39f581977e16eca8651b51ddb25a3819e`  
		Last Modified: Tue, 30 Jul 2024 19:04:21 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:91596bae158fd34e956869246d6ddd752c3907ebb34b91ce717062c0fb109420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.5 MB (611543442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc38c4ecfdfe15c105a128f787ba8f190104e51ee291a681bd831da6ff8c78c2`
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
# Tue, 30 Jul 2024 12:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Jul 2024 12:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jul 2024 12:28:55 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_RELEASE=20240730
# Tue, 30 Jul 2024 12:28:55 GMT
ARG ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240730 ODOO_SHA=f798b05ba7975af1f11abfa6ecb5ef9b22cd712c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jul 2024 12:28:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jul 2024 12:28:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jul 2024 12:28:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jul 2024 12:28:55 GMT
USER odoo
# Tue, 30 Jul 2024 12:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jul 2024 12:28:55 GMT
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
	-	`sha256:a972096075db8310fcdf24f4f5076aa1227e577d34224373e31ccb99902d9346`  
		Last Modified: Tue, 30 Jul 2024 19:08:56 GMT  
		Size: 330.7 MB (330746328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e615e282056774e9d08ffb0b0b4e5154a53ed5d59488c367757a53787160eca1`  
		Last Modified: Tue, 30 Jul 2024 19:08:32 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da72434b849df9ea36f1ee0221ea15ed89809ad6d96c83774b22959a0d772635`  
		Last Modified: Tue, 30 Jul 2024 19:08:32 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bf1c6522a09c10575db194d3aeee7754bf38c5554406845eb5f321dcd6d397`  
		Last Modified: Tue, 30 Jul 2024 19:08:33 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00939a7d5f47bd65842b73247761da3836db97b7e1163e3e4504ef772575f397`  
		Last Modified: Tue, 30 Jul 2024 19:08:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:b965ac61d519922c3b857dd99774d4a31688141c6f5a9a8204fbbe8a553e2922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38953720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232194819aa1bee15bcff6a263b6bc573fd3177a3535ea01fde135af59b107a9`

```dockerfile
```

-	Layers:
	-	`sha256:55afa35b56a010a805e5008ee433e1df7910630cd826a8615e829feea4accbeb`  
		Last Modified: Tue, 30 Jul 2024 19:08:32 GMT  
		Size: 38.9 MB (38926789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ba84a640b332eb88eb7e4a504940a0f2632fe3145c290887f9af2662bb9ae7e`  
		Last Modified: Tue, 30 Jul 2024 19:08:31 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json
