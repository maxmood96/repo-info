<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:15.0-20240603`](#odoo150-20240603)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20240603`](#odoo160-20240603)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20240603`](#odoo170-20240603)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:de406fe997362a242bea2e357965eb98ba2a1e1114135dbbde8256d94a6e6fe4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:e3769adf7e61f1567abf12ed5cc865f86ba3631f2ac59ac546b783a0c03ff6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.8 MB (563791572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f344742227cd68b8ef2c02f161555c5c58fe12474364e34cf50ec3652a72f1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=15.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=1efdbbdfdb0af9defece942b02d5ffc7946f6bfc
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: ODOO_RELEASE=20240603 ODOO_SHA=1efdbbdfdb0af9defece942b02d5ffc7946f6bfc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: ODOO_RELEASE=20240603 ODOO_SHA=1efdbbdfdb0af9defece942b02d5ffc7946f6bfc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee49d9f5960eceb001b923da83dfe32c84a1c33fae9abb4dca2f88578ba87e75`  
		Last Modified: Mon, 03 Jun 2024 19:03:01 GMT  
		Size: 220.3 MB (220281040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae340eae2df79e91d93671c4e5b97c6f6240c4891ab4cf7097fc880c39eee350`  
		Last Modified: Mon, 03 Jun 2024 19:02:58 GMT  
		Size: 2.4 MB (2387301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c971a12245bc5c5d59a93150270e63214ab2048323e825b2ee5076be14cd02ba`  
		Last Modified: Mon, 03 Jun 2024 19:02:58 GMT  
		Size: 457.8 KB (457804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6349a2df2d08a22cc735a89b281a7b0e79d0ec110ecf25349afd0f8f1eb869b5`  
		Last Modified: Mon, 03 Jun 2024 19:03:02 GMT  
		Size: 309.2 MB (309229056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273b5836f8ad6e54eafeb412c7e785dbbacfaf013111571ccab85bcda8d5cc1a`  
		Last Modified: Mon, 03 Jun 2024 19:02:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28bfd7b4df0756c718bf9c1cdf499a8b33b766f8d25b411bf64cb9e2161d6ea`  
		Last Modified: Mon, 03 Jun 2024 19:02:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7ef469b85e325939169729e5a08fd9a73c2075dc447a1c05bd10f5cdca3e0d`  
		Last Modified: Mon, 03 Jun 2024 19:03:00 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edc98fff2e3d111ee24d24cbb423f78c36698988564070bf7c2952ad99e1447`  
		Last Modified: Mon, 03 Jun 2024 19:03:00 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15` - unknown; unknown

```console
$ docker pull odoo@sha256:118a5927f6554382c8a69d263eb073953fd8739d3c7105dbba103794cdf0b359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e73cc4a101f2aa02420a0afa12a27e2a251430192bacacd02e9d2890bb7b15c`

```dockerfile
```

-	Layers:
	-	`sha256:ed15628917e6924e34d7f1ea23e4f2b2c961b4a0d02ee7c48d021ee27b8980bd`  
		Last Modified: Mon, 03 Jun 2024 19:02:58 GMT  
		Size: 34.5 MB (34508694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15540fd4ce27e98ff5c33c4a65027c1a402a793e4eba3025c7cb919200030e13`  
		Last Modified: Mon, 03 Jun 2024 19:02:58 GMT  
		Size: 24.6 KB (24582 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0`

```console
$ docker pull odoo@sha256:de406fe997362a242bea2e357965eb98ba2a1e1114135dbbde8256d94a6e6fe4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:e3769adf7e61f1567abf12ed5cc865f86ba3631f2ac59ac546b783a0c03ff6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.8 MB (563791572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f344742227cd68b8ef2c02f161555c5c58fe12474364e34cf50ec3652a72f1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=15.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=1efdbbdfdb0af9defece942b02d5ffc7946f6bfc
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: ODOO_RELEASE=20240603 ODOO_SHA=1efdbbdfdb0af9defece942b02d5ffc7946f6bfc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: ODOO_RELEASE=20240603 ODOO_SHA=1efdbbdfdb0af9defece942b02d5ffc7946f6bfc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee49d9f5960eceb001b923da83dfe32c84a1c33fae9abb4dca2f88578ba87e75`  
		Last Modified: Mon, 03 Jun 2024 19:03:01 GMT  
		Size: 220.3 MB (220281040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae340eae2df79e91d93671c4e5b97c6f6240c4891ab4cf7097fc880c39eee350`  
		Last Modified: Mon, 03 Jun 2024 19:02:58 GMT  
		Size: 2.4 MB (2387301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c971a12245bc5c5d59a93150270e63214ab2048323e825b2ee5076be14cd02ba`  
		Last Modified: Mon, 03 Jun 2024 19:02:58 GMT  
		Size: 457.8 KB (457804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6349a2df2d08a22cc735a89b281a7b0e79d0ec110ecf25349afd0f8f1eb869b5`  
		Last Modified: Mon, 03 Jun 2024 19:03:02 GMT  
		Size: 309.2 MB (309229056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273b5836f8ad6e54eafeb412c7e785dbbacfaf013111571ccab85bcda8d5cc1a`  
		Last Modified: Mon, 03 Jun 2024 19:02:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28bfd7b4df0756c718bf9c1cdf499a8b33b766f8d25b411bf64cb9e2161d6ea`  
		Last Modified: Mon, 03 Jun 2024 19:02:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7ef469b85e325939169729e5a08fd9a73c2075dc447a1c05bd10f5cdca3e0d`  
		Last Modified: Mon, 03 Jun 2024 19:03:00 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edc98fff2e3d111ee24d24cbb423f78c36698988564070bf7c2952ad99e1447`  
		Last Modified: Mon, 03 Jun 2024 19:03:00 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0` - unknown; unknown

```console
$ docker pull odoo@sha256:118a5927f6554382c8a69d263eb073953fd8739d3c7105dbba103794cdf0b359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e73cc4a101f2aa02420a0afa12a27e2a251430192bacacd02e9d2890bb7b15c`

```dockerfile
```

-	Layers:
	-	`sha256:ed15628917e6924e34d7f1ea23e4f2b2c961b4a0d02ee7c48d021ee27b8980bd`  
		Last Modified: Mon, 03 Jun 2024 19:02:58 GMT  
		Size: 34.5 MB (34508694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15540fd4ce27e98ff5c33c4a65027c1a402a793e4eba3025c7cb919200030e13`  
		Last Modified: Mon, 03 Jun 2024 19:02:58 GMT  
		Size: 24.6 KB (24582 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0-20240603`

```console
$ docker pull odoo@sha256:de406fe997362a242bea2e357965eb98ba2a1e1114135dbbde8256d94a6e6fe4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0-20240603` - linux; amd64

```console
$ docker pull odoo@sha256:e3769adf7e61f1567abf12ed5cc865f86ba3631f2ac59ac546b783a0c03ff6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.8 MB (563791572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f344742227cd68b8ef2c02f161555c5c58fe12474364e34cf50ec3652a72f1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=15.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=1efdbbdfdb0af9defece942b02d5ffc7946f6bfc
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: ODOO_RELEASE=20240603 ODOO_SHA=1efdbbdfdb0af9defece942b02d5ffc7946f6bfc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: ODOO_RELEASE=20240603 ODOO_SHA=1efdbbdfdb0af9defece942b02d5ffc7946f6bfc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee49d9f5960eceb001b923da83dfe32c84a1c33fae9abb4dca2f88578ba87e75`  
		Last Modified: Mon, 03 Jun 2024 19:03:01 GMT  
		Size: 220.3 MB (220281040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae340eae2df79e91d93671c4e5b97c6f6240c4891ab4cf7097fc880c39eee350`  
		Last Modified: Mon, 03 Jun 2024 19:02:58 GMT  
		Size: 2.4 MB (2387301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c971a12245bc5c5d59a93150270e63214ab2048323e825b2ee5076be14cd02ba`  
		Last Modified: Mon, 03 Jun 2024 19:02:58 GMT  
		Size: 457.8 KB (457804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6349a2df2d08a22cc735a89b281a7b0e79d0ec110ecf25349afd0f8f1eb869b5`  
		Last Modified: Mon, 03 Jun 2024 19:03:02 GMT  
		Size: 309.2 MB (309229056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273b5836f8ad6e54eafeb412c7e785dbbacfaf013111571ccab85bcda8d5cc1a`  
		Last Modified: Mon, 03 Jun 2024 19:02:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28bfd7b4df0756c718bf9c1cdf499a8b33b766f8d25b411bf64cb9e2161d6ea`  
		Last Modified: Mon, 03 Jun 2024 19:02:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7ef469b85e325939169729e5a08fd9a73c2075dc447a1c05bd10f5cdca3e0d`  
		Last Modified: Mon, 03 Jun 2024 19:03:00 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edc98fff2e3d111ee24d24cbb423f78c36698988564070bf7c2952ad99e1447`  
		Last Modified: Mon, 03 Jun 2024 19:03:00 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0-20240603` - unknown; unknown

```console
$ docker pull odoo@sha256:118a5927f6554382c8a69d263eb073953fd8739d3c7105dbba103794cdf0b359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e73cc4a101f2aa02420a0afa12a27e2a251430192bacacd02e9d2890bb7b15c`

```dockerfile
```

-	Layers:
	-	`sha256:ed15628917e6924e34d7f1ea23e4f2b2c961b4a0d02ee7c48d021ee27b8980bd`  
		Last Modified: Mon, 03 Jun 2024 19:02:58 GMT  
		Size: 34.5 MB (34508694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15540fd4ce27e98ff5c33c4a65027c1a402a793e4eba3025c7cb919200030e13`  
		Last Modified: Mon, 03 Jun 2024 19:02:58 GMT  
		Size: 24.6 KB (24582 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16`

```console
$ docker pull odoo@sha256:68de7754fcf21d774084722cac677ccd09649b4318d75548d770e7ca947e017e
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
$ docker pull odoo@sha256:8dba97cf238763993f4eff8a57d6342f43523e4c9966778f44e429c44b38c5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.0 MB (583039753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265f3aa231d1cd04dc543e1c02514adaaac9204668434c5bb0790d360c0aebf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=16.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb3a79eecd3738083b21ea3a43297405301bd1ad95ff9f3e74a138bf4d2786c`  
		Last Modified: Mon, 03 Jun 2024 19:03:15 GMT  
		Size: 219.6 MB (219594329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f341518a8e2b1ccff448f557ee5916b0cb2d91b6d7bfe894c22519db3d01ab0`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 2.4 MB (2391067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f4e085ac993692e79dfeead6886f3a3c67c97d10efdcaa85c0746b411d6a9e`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 457.8 KB (457842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce7521a40f6fdca2e4e09bf9ec5b8430126f5a7af3387114cccfabba09ca18f`  
		Last Modified: Mon, 03 Jun 2024 19:03:17 GMT  
		Size: 329.2 MB (329160149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273b5836f8ad6e54eafeb412c7e785dbbacfaf013111571ccab85bcda8d5cc1a`  
		Last Modified: Mon, 03 Jun 2024 19:02:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339ebc60fb917e732360a3c8b8dd0f8753ec1082bdf4135847519fb3a972ccdf`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491a0a49172c9954b34e7bab2caf9af588f368ca51c0b74e17213c624fb92369`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74053f08aeab1fd2d5a16fe9a45261811104914f82547929babba4f05d3d591d`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:9771d7054f66881fb74e2b9aaa38c88c4d7356739debfcd6604ea0de46ec13eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38569871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0eb32cbda225c9ef6a1142654453a189b4d0c84ff0e4cda08d42a516f039d02`

```dockerfile
```

-	Layers:
	-	`sha256:4e3ee79763c20a8fe76dd97744ff5928cc03239ced8bc03ff7c9338663c73082`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 38.5 MB (38543378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b477a3f8e54ad03bd11be49592851d4f3d8fb526e99f0d556ecfb0a1a31940e7`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 26.5 KB (26493 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8a503bf02392da3272a0591df7effdf3a0e0d67d15dc5d1e5c7ec261f964fff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578578727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c8d76533ee1691d06b2480ba49167342fb6c600cac4af3200adabeca535476`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=16.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414f081822e148fbd12e88942138758452276337b5cf8ad49fde3bed38321c60`  
		Last Modified: Thu, 30 May 2024 02:24:03 GMT  
		Size: 216.9 MB (216900476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8080aaf786c4ccd54a7fadc40de3455bf8063851fe27e930efef95cc0aa2619`  
		Last Modified: Thu, 30 May 2024 02:23:58 GMT  
		Size: 2.4 MB (2393326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bde69a325d29e830b01000a32bc7f9c070f5c69486d3ee433941cdb27533394`  
		Last Modified: Thu, 30 May 2024 02:23:58 GMT  
		Size: 457.8 KB (457801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde29033b387b8dd6ed28c7113ca1969cd9cc502f91287d2411bd860390655ac`  
		Last Modified: Thu, 30 May 2024 02:24:05 GMT  
		Size: 328.7 MB (328737782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc009f1a96b30a245fcfd3571f3217745ef4eeee359d020bbf0fe63602a0ed0f`  
		Last Modified: Thu, 30 May 2024 02:23:59 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793b7010766fd70ea5a0b4575ba52da73e922a3ba7ab8aec37f1197310763f46`  
		Last Modified: Thu, 30 May 2024 02:23:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba4e85ba081af75d5b1c1aa270bf41124b1790a463ad35e8b8e0de64f234b5`  
		Last Modified: Thu, 30 May 2024 02:24:00 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eaa9b67deb0ece918299cfa1ac43c086a01c4b4ae1874508fd271f3fb6eaa1`  
		Last Modified: Thu, 30 May 2024 02:24:00 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:84c503de8522f50f20f20021e33e77c5e2b1d3a215fa408ff680c64777b57779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38574689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a316fd2dac07ec5649c7bb2133113f5711df628823a33688ce8ceffbcac7bbf2`

```dockerfile
```

-	Layers:
	-	`sha256:13b083fe0ccd07df3131dece66ba743af5df664a26142a8bff60ea68a90f7aae`  
		Last Modified: Thu, 30 May 2024 02:23:59 GMT  
		Size: 38.5 MB (38548219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f04f9f5dbed164a4a5cd593e0342bd201b491b20082d215ba9b4129dc54f8a30`  
		Last Modified: Thu, 30 May 2024 02:23:57 GMT  
		Size: 26.5 KB (26470 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:b71be58382dff51089c350fd57db4aca7b48d4e54817f7a61ce728cec9bec968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.6 MB (597597754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c781bf5a9b60aafa1b83b5b12d52838816d9a497973806321805c4224f9acd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=16.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477402be4e3f8a663f34ac8b8e2a1e8c5294abd489e284d95bac4c022b04eb16`  
		Last Modified: Tue, 04 Jun 2024 02:14:17 GMT  
		Size: 228.6 MB (228589734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ec4853222654e6fceb4fc51fbc0a42a9d212765267a5df22b7f11424cea224`  
		Last Modified: Tue, 04 Jun 2024 02:14:00 GMT  
		Size: 2.6 MB (2634129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb45c2bf22aec8a5c37fe656cca0e5eeb63433d13ca29e17878b13bd7092546`  
		Last Modified: Tue, 04 Jun 2024 02:13:59 GMT  
		Size: 457.8 KB (457832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce91892bb60fabe36ff1271e018922fef89e7863fde2cf92bd486e99a8c08c0c`  
		Last Modified: Tue, 04 Jun 2024 02:14:32 GMT  
		Size: 330.6 MB (330602464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42795a74c64b2e4094d511f79c0f6cfc0b0b6102263ae7f3c269ff20ee4588f3`  
		Last Modified: Tue, 04 Jun 2024 02:14:00 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2fde2f775db79c623ca2aba8f0aa7c63682975104ebb300f3715149a613f95`  
		Last Modified: Tue, 04 Jun 2024 02:14:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da78d7be0454ab3e9f38099f409bb7246a82f9026a1006a4fcf4bdb5591364`  
		Last Modified: Tue, 04 Jun 2024 02:14:02 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da3374100334a9e84ab9913fea617f749cca11f72e8c87980a1cdeba788b412`  
		Last Modified: Tue, 04 Jun 2024 02:14:02 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:d3dbd7d33b76bcc030ca8acf5c42397741e5f2a69fde9b73ed0d9b32be623ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38578053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541d7ba14195e3d9e289ccdf21867ee7a5f75174010197dc58dc7a42b58e9bff`

```dockerfile
```

-	Layers:
	-	`sha256:8a4499240e1a9cc846e4ee451e093cc673a012881a2fca4202154f17777c022e`  
		Last Modified: Tue, 04 Jun 2024 02:14:06 GMT  
		Size: 38.6 MB (38551510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24a0cf144bdff0e720c391821078d7fd4e7aa394b0cccb05f97ec13a68e6acd7`  
		Last Modified: Tue, 04 Jun 2024 02:14:01 GMT  
		Size: 26.5 KB (26543 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:68de7754fcf21d774084722cac677ccd09649b4318d75548d770e7ca947e017e
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
$ docker pull odoo@sha256:8dba97cf238763993f4eff8a57d6342f43523e4c9966778f44e429c44b38c5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.0 MB (583039753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265f3aa231d1cd04dc543e1c02514adaaac9204668434c5bb0790d360c0aebf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=16.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb3a79eecd3738083b21ea3a43297405301bd1ad95ff9f3e74a138bf4d2786c`  
		Last Modified: Mon, 03 Jun 2024 19:03:15 GMT  
		Size: 219.6 MB (219594329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f341518a8e2b1ccff448f557ee5916b0cb2d91b6d7bfe894c22519db3d01ab0`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 2.4 MB (2391067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f4e085ac993692e79dfeead6886f3a3c67c97d10efdcaa85c0746b411d6a9e`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 457.8 KB (457842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce7521a40f6fdca2e4e09bf9ec5b8430126f5a7af3387114cccfabba09ca18f`  
		Last Modified: Mon, 03 Jun 2024 19:03:17 GMT  
		Size: 329.2 MB (329160149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273b5836f8ad6e54eafeb412c7e785dbbacfaf013111571ccab85bcda8d5cc1a`  
		Last Modified: Mon, 03 Jun 2024 19:02:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339ebc60fb917e732360a3c8b8dd0f8753ec1082bdf4135847519fb3a972ccdf`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491a0a49172c9954b34e7bab2caf9af588f368ca51c0b74e17213c624fb92369`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74053f08aeab1fd2d5a16fe9a45261811104914f82547929babba4f05d3d591d`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9771d7054f66881fb74e2b9aaa38c88c4d7356739debfcd6604ea0de46ec13eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38569871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0eb32cbda225c9ef6a1142654453a189b4d0c84ff0e4cda08d42a516f039d02`

```dockerfile
```

-	Layers:
	-	`sha256:4e3ee79763c20a8fe76dd97744ff5928cc03239ced8bc03ff7c9338663c73082`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 38.5 MB (38543378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b477a3f8e54ad03bd11be49592851d4f3d8fb526e99f0d556ecfb0a1a31940e7`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 26.5 KB (26493 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8a503bf02392da3272a0591df7effdf3a0e0d67d15dc5d1e5c7ec261f964fff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.6 MB (578578727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c8d76533ee1691d06b2480ba49167342fb6c600cac4af3200adabeca535476`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=16.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=bcf783566f132d6391a2e2ee779ce082e904643d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414f081822e148fbd12e88942138758452276337b5cf8ad49fde3bed38321c60`  
		Last Modified: Thu, 30 May 2024 02:24:03 GMT  
		Size: 216.9 MB (216900476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8080aaf786c4ccd54a7fadc40de3455bf8063851fe27e930efef95cc0aa2619`  
		Last Modified: Thu, 30 May 2024 02:23:58 GMT  
		Size: 2.4 MB (2393326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bde69a325d29e830b01000a32bc7f9c070f5c69486d3ee433941cdb27533394`  
		Last Modified: Thu, 30 May 2024 02:23:58 GMT  
		Size: 457.8 KB (457801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde29033b387b8dd6ed28c7113ca1969cd9cc502f91287d2411bd860390655ac`  
		Last Modified: Thu, 30 May 2024 02:24:05 GMT  
		Size: 328.7 MB (328737782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc009f1a96b30a245fcfd3571f3217745ef4eeee359d020bbf0fe63602a0ed0f`  
		Last Modified: Thu, 30 May 2024 02:23:59 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793b7010766fd70ea5a0b4575ba52da73e922a3ba7ab8aec37f1197310763f46`  
		Last Modified: Thu, 30 May 2024 02:23:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba4e85ba081af75d5b1c1aa270bf41124b1790a463ad35e8b8e0de64f234b5`  
		Last Modified: Thu, 30 May 2024 02:24:00 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eaa9b67deb0ece918299cfa1ac43c086a01c4b4ae1874508fd271f3fb6eaa1`  
		Last Modified: Thu, 30 May 2024 02:24:00 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:84c503de8522f50f20f20021e33e77c5e2b1d3a215fa408ff680c64777b57779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38574689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a316fd2dac07ec5649c7bb2133113f5711df628823a33688ce8ceffbcac7bbf2`

```dockerfile
```

-	Layers:
	-	`sha256:13b083fe0ccd07df3131dece66ba743af5df664a26142a8bff60ea68a90f7aae`  
		Last Modified: Thu, 30 May 2024 02:23:59 GMT  
		Size: 38.5 MB (38548219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f04f9f5dbed164a4a5cd593e0342bd201b491b20082d215ba9b4129dc54f8a30`  
		Last Modified: Thu, 30 May 2024 02:23:57 GMT  
		Size: 26.5 KB (26470 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b71be58382dff51089c350fd57db4aca7b48d4e54817f7a61ce728cec9bec968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.6 MB (597597754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c781bf5a9b60aafa1b83b5b12d52838816d9a497973806321805c4224f9acd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=16.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477402be4e3f8a663f34ac8b8e2a1e8c5294abd489e284d95bac4c022b04eb16`  
		Last Modified: Tue, 04 Jun 2024 02:14:17 GMT  
		Size: 228.6 MB (228589734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ec4853222654e6fceb4fc51fbc0a42a9d212765267a5df22b7f11424cea224`  
		Last Modified: Tue, 04 Jun 2024 02:14:00 GMT  
		Size: 2.6 MB (2634129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb45c2bf22aec8a5c37fe656cca0e5eeb63433d13ca29e17878b13bd7092546`  
		Last Modified: Tue, 04 Jun 2024 02:13:59 GMT  
		Size: 457.8 KB (457832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce91892bb60fabe36ff1271e018922fef89e7863fde2cf92bd486e99a8c08c0c`  
		Last Modified: Tue, 04 Jun 2024 02:14:32 GMT  
		Size: 330.6 MB (330602464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42795a74c64b2e4094d511f79c0f6cfc0b0b6102263ae7f3c269ff20ee4588f3`  
		Last Modified: Tue, 04 Jun 2024 02:14:00 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2fde2f775db79c623ca2aba8f0aa7c63682975104ebb300f3715149a613f95`  
		Last Modified: Tue, 04 Jun 2024 02:14:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da78d7be0454ab3e9f38099f409bb7246a82f9026a1006a4fcf4bdb5591364`  
		Last Modified: Tue, 04 Jun 2024 02:14:02 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da3374100334a9e84ab9913fea617f749cca11f72e8c87980a1cdeba788b412`  
		Last Modified: Tue, 04 Jun 2024 02:14:02 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d3dbd7d33b76bcc030ca8acf5c42397741e5f2a69fde9b73ed0d9b32be623ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38578053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541d7ba14195e3d9e289ccdf21867ee7a5f75174010197dc58dc7a42b58e9bff`

```dockerfile
```

-	Layers:
	-	`sha256:8a4499240e1a9cc846e4ee451e093cc673a012881a2fca4202154f17777c022e`  
		Last Modified: Tue, 04 Jun 2024 02:14:06 GMT  
		Size: 38.6 MB (38551510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24a0cf144bdff0e720c391821078d7fd4e7aa394b0cccb05f97ec13a68e6acd7`  
		Last Modified: Tue, 04 Jun 2024 02:14:01 GMT  
		Size: 26.5 KB (26543 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20240603`

```console
$ docker pull odoo@sha256:0b1705187c7eafdd9f973284cd777b3650c949702d51fd3a07180e2b2d8684f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0-20240603` - linux; amd64

```console
$ docker pull odoo@sha256:8dba97cf238763993f4eff8a57d6342f43523e4c9966778f44e429c44b38c5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.0 MB (583039753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265f3aa231d1cd04dc543e1c02514adaaac9204668434c5bb0790d360c0aebf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=16.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb3a79eecd3738083b21ea3a43297405301bd1ad95ff9f3e74a138bf4d2786c`  
		Last Modified: Mon, 03 Jun 2024 19:03:15 GMT  
		Size: 219.6 MB (219594329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f341518a8e2b1ccff448f557ee5916b0cb2d91b6d7bfe894c22519db3d01ab0`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 2.4 MB (2391067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f4e085ac993692e79dfeead6886f3a3c67c97d10efdcaa85c0746b411d6a9e`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 457.8 KB (457842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce7521a40f6fdca2e4e09bf9ec5b8430126f5a7af3387114cccfabba09ca18f`  
		Last Modified: Mon, 03 Jun 2024 19:03:17 GMT  
		Size: 329.2 MB (329160149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273b5836f8ad6e54eafeb412c7e785dbbacfaf013111571ccab85bcda8d5cc1a`  
		Last Modified: Mon, 03 Jun 2024 19:02:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339ebc60fb917e732360a3c8b8dd0f8753ec1082bdf4135847519fb3a972ccdf`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491a0a49172c9954b34e7bab2caf9af588f368ca51c0b74e17213c624fb92369`  
		Last Modified: Mon, 03 Jun 2024 19:03:13 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74053f08aeab1fd2d5a16fe9a45261811104914f82547929babba4f05d3d591d`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240603` - unknown; unknown

```console
$ docker pull odoo@sha256:9771d7054f66881fb74e2b9aaa38c88c4d7356739debfcd6604ea0de46ec13eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38569871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0eb32cbda225c9ef6a1142654453a189b4d0c84ff0e4cda08d42a516f039d02`

```dockerfile
```

-	Layers:
	-	`sha256:4e3ee79763c20a8fe76dd97744ff5928cc03239ced8bc03ff7c9338663c73082`  
		Last Modified: Mon, 03 Jun 2024 19:03:14 GMT  
		Size: 38.5 MB (38543378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b477a3f8e54ad03bd11be49592851d4f3d8fb526e99f0d556ecfb0a1a31940e7`  
		Last Modified: Mon, 03 Jun 2024 19:03:12 GMT  
		Size: 26.5 KB (26493 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240603` - linux; ppc64le

```console
$ docker pull odoo@sha256:b71be58382dff51089c350fd57db4aca7b48d4e54817f7a61ce728cec9bec968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.6 MB (597597754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c781bf5a9b60aafa1b83b5b12d52838816d9a497973806321805c4224f9acd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=C.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=16.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477402be4e3f8a663f34ac8b8e2a1e8c5294abd489e284d95bac4c022b04eb16`  
		Last Modified: Tue, 04 Jun 2024 02:14:17 GMT  
		Size: 228.6 MB (228589734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ec4853222654e6fceb4fc51fbc0a42a9d212765267a5df22b7f11424cea224`  
		Last Modified: Tue, 04 Jun 2024 02:14:00 GMT  
		Size: 2.6 MB (2634129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb45c2bf22aec8a5c37fe656cca0e5eeb63433d13ca29e17878b13bd7092546`  
		Last Modified: Tue, 04 Jun 2024 02:13:59 GMT  
		Size: 457.8 KB (457832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce91892bb60fabe36ff1271e018922fef89e7863fde2cf92bd486e99a8c08c0c`  
		Last Modified: Tue, 04 Jun 2024 02:14:32 GMT  
		Size: 330.6 MB (330602464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42795a74c64b2e4094d511f79c0f6cfc0b0b6102263ae7f3c269ff20ee4588f3`  
		Last Modified: Tue, 04 Jun 2024 02:14:00 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2fde2f775db79c623ca2aba8f0aa7c63682975104ebb300f3715149a613f95`  
		Last Modified: Tue, 04 Jun 2024 02:14:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da78d7be0454ab3e9f38099f409bb7246a82f9026a1006a4fcf4bdb5591364`  
		Last Modified: Tue, 04 Jun 2024 02:14:02 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da3374100334a9e84ab9913fea617f749cca11f72e8c87980a1cdeba788b412`  
		Last Modified: Tue, 04 Jun 2024 02:14:02 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240603` - unknown; unknown

```console
$ docker pull odoo@sha256:d3dbd7d33b76bcc030ca8acf5c42397741e5f2a69fde9b73ed0d9b32be623ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38578053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541d7ba14195e3d9e289ccdf21867ee7a5f75174010197dc58dc7a42b58e9bff`

```dockerfile
```

-	Layers:
	-	`sha256:8a4499240e1a9cc846e4ee451e093cc673a012881a2fca4202154f17777c022e`  
		Last Modified: Tue, 04 Jun 2024 02:14:06 GMT  
		Size: 38.6 MB (38551510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24a0cf144bdff0e720c391821078d7fd4e7aa394b0cccb05f97ec13a68e6acd7`  
		Last Modified: Tue, 04 Jun 2024 02:14:01 GMT  
		Size: 26.5 KB (26543 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:48bad8ffbdc44d5484d9df549003280366b825c62ad6f89606b0f97858eb1adc
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
$ docker pull odoo@sha256:b1835727995e26d5a72cfea80c02ddf945db335c25f4b9b86659b682932c4e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.2 MB (602168305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2086f8679982da30baea29ae0d58225776b05aa4b9e2f0bd682e7848fad86d01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=en_US.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=17.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44eaebb0065b22d1b5d29a1502b577d49f7daf66f8c417e72874985cfc87b1b`  
		Last Modified: Mon, 03 Jun 2024 19:06:10 GMT  
		Size: 233.7 MB (233720506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f91a6c22c481d3db69bf9208e32849c13db426f37a31244b891086430cf1d`  
		Last Modified: Mon, 03 Jun 2024 19:06:04 GMT  
		Size: 2.3 MB (2313314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696eda90bbc8bb2451c254583a438ad2ca97e509cb8200284bd0d34dd0dc9a5e`  
		Last Modified: Mon, 03 Jun 2024 19:06:04 GMT  
		Size: 458.8 KB (458839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9528e3f214f3d5bc4194a8097feff627e6977ef1a615a2093a444faeb21bce0e`  
		Last Modified: Mon, 03 Jun 2024 19:06:15 GMT  
		Size: 336.1 MB (336139255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8e4c5e4411d23314944570fbb3e5be506e887ca90086c32d3383f7d8713b23`  
		Last Modified: Mon, 03 Jun 2024 19:06:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6c5559a2b951b779bfe8b75bf7a0fee396dd4a043be940a96d562bba48db80`  
		Last Modified: Mon, 03 Jun 2024 19:06:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44b0b0009d7b03e2ef405b77f50ab0ad92342f8f7c197fabecca318e94edc84`  
		Last Modified: Mon, 03 Jun 2024 19:06:06 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21b342ff1762301d7121131a730a0f95ac991fd06d1a810b1654eea9bb6b29`  
		Last Modified: Mon, 03 Jun 2024 19:06:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:617b743f0f9f952915fd4481db9e3a0bc730c4cfcca1ae2beec189d64dfcfb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39332830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54d00a03ff3707d2fc7299389bfdc2e92e2af7a5a37a491d0dcd694c7292ce3`

```dockerfile
```

-	Layers:
	-	`sha256:76ccc89cafe3dbdc38f1a0a979234e184433d488ca666d76487b0f791e2f7811`  
		Last Modified: Mon, 03 Jun 2024 19:06:06 GMT  
		Size: 39.3 MB (39306006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ed3bb05a401b587169b42b20edad1f64c83b7f067c7729c6dd5676108148b4`  
		Last Modified: Mon, 03 Jun 2024 19:06:04 GMT  
		Size: 26.8 KB (26824 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a693628cbf707e6b0732304d3598dc95b64b2fc6ff66b20fdae18854af931ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.6 MB (596618598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233581163c27a01b077bdce6e1a6a1edd49a7668961642e8b370c85ccdcaca32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271df60fb2ae7fabd06f5f0fe628403f944bdeba6ceab1507d1d47f8583818c9`  
		Last Modified: Thu, 30 May 2024 02:20:00 GMT  
		Size: 231.1 MB (231129260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d721b04ceea49496f804f547d035ef6e841f1aba7ba13634b871a0a262553ddc`  
		Last Modified: Thu, 30 May 2024 02:19:56 GMT  
		Size: 2.3 MB (2306364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffb0c1ef8ee904225d9eb157f0951f47e738b7919d7427b352e0fcdf644980d`  
		Last Modified: Thu, 30 May 2024 02:19:55 GMT  
		Size: 458.8 KB (458826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f3009fc0ca9a84938ba7632ccbbb79e015de10d56f522f91d5a572b5ecb717`  
		Last Modified: Thu, 30 May 2024 02:20:05 GMT  
		Size: 335.4 MB (335361176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d207689c892df07a8c4c6c6e6dde8ed6edebcac90c38b59eb8d9840f21326c98`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bd5863589606d080b8aec7ee8fafbd4185ba02cc6f0c1de2687f7730b8fb30`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110ad8920a2fc0c2f4a513ea1405bca112e1b9f0187c822961a63f7e70323ef2`  
		Last Modified: Thu, 30 May 2024 02:19:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94e49bae97ebf9195e865e845a98d83141e8998e7ffc54b68328895b45c7a31`  
		Last Modified: Thu, 30 May 2024 02:19:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:984e016c32de2f01b3a50ed71dee5d5283965222a4b1799b9f777133cd87097c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39226161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48795314c03b1ca80e5b7732f9db1df97f2eea32eeb265f19835c5465e33907b`

```dockerfile
```

-	Layers:
	-	`sha256:f376677805c31ca437af69a2de7f17a49d8c7db2fe9465c5ab8ff3784746c19b`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 39.2 MB (39199354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a42aeafd36498d0983a7a9c5b37104a1246819387fe978af4601edc2030027d`  
		Last Modified: Thu, 30 May 2024 02:19:55 GMT  
		Size: 26.8 KB (26807 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:0856f0f465f1b5b833a0c16f6b19477c350dd2deed09cf45a4a702252d7b498a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618662213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e95d0390dfcc84047e153065aef7e99b91fe2fc0c3bd02670a9af4cbffe347`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=en_US.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=17.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b7cf94291ea168ccdc203965a79f54603a4fe2e0738a3acf0f7a8d860e51f32`  
		Last Modified: Sat, 27 Apr 2024 14:45:49 GMT  
		Size: 34.5 MB (34461223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bce02f901cf510611efea394056d49156c523020e7866f490882de224ce1b1a`  
		Last Modified: Mon, 03 Jun 2024 20:25:14 GMT  
		Size: 243.3 MB (243268710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7569fd4e274fa888d627a653da68757f3aaa2d15e3317c784c447dacb0b2679d`  
		Last Modified: Mon, 03 Jun 2024 20:25:08 GMT  
		Size: 2.6 MB (2590185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c9341ba472ae76dc395f908a80ca185dad8148f5986e657cb22a3b4b384087`  
		Last Modified: Mon, 03 Jun 2024 20:25:08 GMT  
		Size: 458.9 KB (458865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90e5365300593d6d11e6affc8a4a6251367c2d2f49f53d0b908b33623180c5f`  
		Last Modified: Mon, 03 Jun 2024 20:25:17 GMT  
		Size: 337.9 MB (337880786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675798c532e30897f37b9c91e259b8d5e8be79056ad0370c79f4e9298b8628b3`  
		Last Modified: Mon, 03 Jun 2024 20:25:09 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf9fdd935295a3f0b7dab9acc7ceaf72813f116e69aa656740d0aba442427b0`  
		Last Modified: Mon, 03 Jun 2024 20:25:09 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441e05cd7712649de3e0e166e53597bc421009e25681e9d8a65c2a95f0365800`  
		Last Modified: Mon, 03 Jun 2024 20:25:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ff6e0501abd44013545fd3ecb373135d92c28eeaa39ebc790bcfdb8215ecb5`  
		Last Modified: Mon, 03 Jun 2024 20:25:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:2fd939615c1fd7a00f5534348b9a35b44ec25fb841a1a44401b6b84b49cd6b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39341201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efd48bf83eec2d5ab288dd29e9ad2a7a10ef06457107e5ac62ba4910d481017`

```dockerfile
```

-	Layers:
	-	`sha256:fc0367739dd3c1d03e14e1e784a7e055d7009cb3f283f9a0bb3b579c6463e9d4`  
		Last Modified: Mon, 03 Jun 2024 20:25:09 GMT  
		Size: 39.3 MB (39314319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5d9f3d8bf81f6ce0c12e1dfbc92854051085d16ec70be00063c47c90ce9882`  
		Last Modified: Mon, 03 Jun 2024 20:25:08 GMT  
		Size: 26.9 KB (26882 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:48bad8ffbdc44d5484d9df549003280366b825c62ad6f89606b0f97858eb1adc
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
$ docker pull odoo@sha256:b1835727995e26d5a72cfea80c02ddf945db335c25f4b9b86659b682932c4e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.2 MB (602168305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2086f8679982da30baea29ae0d58225776b05aa4b9e2f0bd682e7848fad86d01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=en_US.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=17.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44eaebb0065b22d1b5d29a1502b577d49f7daf66f8c417e72874985cfc87b1b`  
		Last Modified: Mon, 03 Jun 2024 19:06:10 GMT  
		Size: 233.7 MB (233720506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f91a6c22c481d3db69bf9208e32849c13db426f37a31244b891086430cf1d`  
		Last Modified: Mon, 03 Jun 2024 19:06:04 GMT  
		Size: 2.3 MB (2313314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696eda90bbc8bb2451c254583a438ad2ca97e509cb8200284bd0d34dd0dc9a5e`  
		Last Modified: Mon, 03 Jun 2024 19:06:04 GMT  
		Size: 458.8 KB (458839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9528e3f214f3d5bc4194a8097feff627e6977ef1a615a2093a444faeb21bce0e`  
		Last Modified: Mon, 03 Jun 2024 19:06:15 GMT  
		Size: 336.1 MB (336139255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8e4c5e4411d23314944570fbb3e5be506e887ca90086c32d3383f7d8713b23`  
		Last Modified: Mon, 03 Jun 2024 19:06:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6c5559a2b951b779bfe8b75bf7a0fee396dd4a043be940a96d562bba48db80`  
		Last Modified: Mon, 03 Jun 2024 19:06:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44b0b0009d7b03e2ef405b77f50ab0ad92342f8f7c197fabecca318e94edc84`  
		Last Modified: Mon, 03 Jun 2024 19:06:06 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21b342ff1762301d7121131a730a0f95ac991fd06d1a810b1654eea9bb6b29`  
		Last Modified: Mon, 03 Jun 2024 19:06:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:617b743f0f9f952915fd4481db9e3a0bc730c4cfcca1ae2beec189d64dfcfb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39332830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54d00a03ff3707d2fc7299389bfdc2e92e2af7a5a37a491d0dcd694c7292ce3`

```dockerfile
```

-	Layers:
	-	`sha256:76ccc89cafe3dbdc38f1a0a979234e184433d488ca666d76487b0f791e2f7811`  
		Last Modified: Mon, 03 Jun 2024 19:06:06 GMT  
		Size: 39.3 MB (39306006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ed3bb05a401b587169b42b20edad1f64c83b7f067c7729c6dd5676108148b4`  
		Last Modified: Mon, 03 Jun 2024 19:06:04 GMT  
		Size: 26.8 KB (26824 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a693628cbf707e6b0732304d3598dc95b64b2fc6ff66b20fdae18854af931ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.6 MB (596618598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233581163c27a01b077bdce6e1a6a1edd49a7668961642e8b370c85ccdcaca32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271df60fb2ae7fabd06f5f0fe628403f944bdeba6ceab1507d1d47f8583818c9`  
		Last Modified: Thu, 30 May 2024 02:20:00 GMT  
		Size: 231.1 MB (231129260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d721b04ceea49496f804f547d035ef6e841f1aba7ba13634b871a0a262553ddc`  
		Last Modified: Thu, 30 May 2024 02:19:56 GMT  
		Size: 2.3 MB (2306364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffb0c1ef8ee904225d9eb157f0951f47e738b7919d7427b352e0fcdf644980d`  
		Last Modified: Thu, 30 May 2024 02:19:55 GMT  
		Size: 458.8 KB (458826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f3009fc0ca9a84938ba7632ccbbb79e015de10d56f522f91d5a572b5ecb717`  
		Last Modified: Thu, 30 May 2024 02:20:05 GMT  
		Size: 335.4 MB (335361176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d207689c892df07a8c4c6c6e6dde8ed6edebcac90c38b59eb8d9840f21326c98`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bd5863589606d080b8aec7ee8fafbd4185ba02cc6f0c1de2687f7730b8fb30`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110ad8920a2fc0c2f4a513ea1405bca112e1b9f0187c822961a63f7e70323ef2`  
		Last Modified: Thu, 30 May 2024 02:19:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94e49bae97ebf9195e865e845a98d83141e8998e7ffc54b68328895b45c7a31`  
		Last Modified: Thu, 30 May 2024 02:19:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:984e016c32de2f01b3a50ed71dee5d5283965222a4b1799b9f777133cd87097c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39226161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48795314c03b1ca80e5b7732f9db1df97f2eea32eeb265f19835c5465e33907b`

```dockerfile
```

-	Layers:
	-	`sha256:f376677805c31ca437af69a2de7f17a49d8c7db2fe9465c5ab8ff3784746c19b`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 39.2 MB (39199354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a42aeafd36498d0983a7a9c5b37104a1246819387fe978af4601edc2030027d`  
		Last Modified: Thu, 30 May 2024 02:19:55 GMT  
		Size: 26.8 KB (26807 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:0856f0f465f1b5b833a0c16f6b19477c350dd2deed09cf45a4a702252d7b498a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618662213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e95d0390dfcc84047e153065aef7e99b91fe2fc0c3bd02670a9af4cbffe347`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=en_US.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=17.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b7cf94291ea168ccdc203965a79f54603a4fe2e0738a3acf0f7a8d860e51f32`  
		Last Modified: Sat, 27 Apr 2024 14:45:49 GMT  
		Size: 34.5 MB (34461223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bce02f901cf510611efea394056d49156c523020e7866f490882de224ce1b1a`  
		Last Modified: Mon, 03 Jun 2024 20:25:14 GMT  
		Size: 243.3 MB (243268710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7569fd4e274fa888d627a653da68757f3aaa2d15e3317c784c447dacb0b2679d`  
		Last Modified: Mon, 03 Jun 2024 20:25:08 GMT  
		Size: 2.6 MB (2590185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c9341ba472ae76dc395f908a80ca185dad8148f5986e657cb22a3b4b384087`  
		Last Modified: Mon, 03 Jun 2024 20:25:08 GMT  
		Size: 458.9 KB (458865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90e5365300593d6d11e6affc8a4a6251367c2d2f49f53d0b908b33623180c5f`  
		Last Modified: Mon, 03 Jun 2024 20:25:17 GMT  
		Size: 337.9 MB (337880786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675798c532e30897f37b9c91e259b8d5e8be79056ad0370c79f4e9298b8628b3`  
		Last Modified: Mon, 03 Jun 2024 20:25:09 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf9fdd935295a3f0b7dab9acc7ceaf72813f116e69aa656740d0aba442427b0`  
		Last Modified: Mon, 03 Jun 2024 20:25:09 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441e05cd7712649de3e0e166e53597bc421009e25681e9d8a65c2a95f0365800`  
		Last Modified: Mon, 03 Jun 2024 20:25:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ff6e0501abd44013545fd3ecb373135d92c28eeaa39ebc790bcfdb8215ecb5`  
		Last Modified: Mon, 03 Jun 2024 20:25:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2fd939615c1fd7a00f5534348b9a35b44ec25fb841a1a44401b6b84b49cd6b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39341201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efd48bf83eec2d5ab288dd29e9ad2a7a10ef06457107e5ac62ba4910d481017`

```dockerfile
```

-	Layers:
	-	`sha256:fc0367739dd3c1d03e14e1e784a7e055d7009cb3f283f9a0bb3b579c6463e9d4`  
		Last Modified: Mon, 03 Jun 2024 20:25:09 GMT  
		Size: 39.3 MB (39314319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5d9f3d8bf81f6ce0c12e1dfbc92854051085d16ec70be00063c47c90ce9882`  
		Last Modified: Mon, 03 Jun 2024 20:25:08 GMT  
		Size: 26.9 KB (26882 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240603`

```console
$ docker pull odoo@sha256:f4d74530cff0d8774e67c8f792ad0ab15705b9ddd56d6efa179e02011aae4ad4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20240603` - linux; amd64

```console
$ docker pull odoo@sha256:b1835727995e26d5a72cfea80c02ddf945db335c25f4b9b86659b682932c4e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.2 MB (602168305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2086f8679982da30baea29ae0d58225776b05aa4b9e2f0bd682e7848fad86d01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=en_US.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=17.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44eaebb0065b22d1b5d29a1502b577d49f7daf66f8c417e72874985cfc87b1b`  
		Last Modified: Mon, 03 Jun 2024 19:06:10 GMT  
		Size: 233.7 MB (233720506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f91a6c22c481d3db69bf9208e32849c13db426f37a31244b891086430cf1d`  
		Last Modified: Mon, 03 Jun 2024 19:06:04 GMT  
		Size: 2.3 MB (2313314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696eda90bbc8bb2451c254583a438ad2ca97e509cb8200284bd0d34dd0dc9a5e`  
		Last Modified: Mon, 03 Jun 2024 19:06:04 GMT  
		Size: 458.8 KB (458839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9528e3f214f3d5bc4194a8097feff627e6977ef1a615a2093a444faeb21bce0e`  
		Last Modified: Mon, 03 Jun 2024 19:06:15 GMT  
		Size: 336.1 MB (336139255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8e4c5e4411d23314944570fbb3e5be506e887ca90086c32d3383f7d8713b23`  
		Last Modified: Mon, 03 Jun 2024 19:06:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6c5559a2b951b779bfe8b75bf7a0fee396dd4a043be940a96d562bba48db80`  
		Last Modified: Mon, 03 Jun 2024 19:06:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44b0b0009d7b03e2ef405b77f50ab0ad92342f8f7c197fabecca318e94edc84`  
		Last Modified: Mon, 03 Jun 2024 19:06:06 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21b342ff1762301d7121131a730a0f95ac991fd06d1a810b1654eea9bb6b29`  
		Last Modified: Mon, 03 Jun 2024 19:06:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240603` - unknown; unknown

```console
$ docker pull odoo@sha256:617b743f0f9f952915fd4481db9e3a0bc730c4cfcca1ae2beec189d64dfcfb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39332830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54d00a03ff3707d2fc7299389bfdc2e92e2af7a5a37a491d0dcd694c7292ce3`

```dockerfile
```

-	Layers:
	-	`sha256:76ccc89cafe3dbdc38f1a0a979234e184433d488ca666d76487b0f791e2f7811`  
		Last Modified: Mon, 03 Jun 2024 19:06:06 GMT  
		Size: 39.3 MB (39306006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ed3bb05a401b587169b42b20edad1f64c83b7f067c7729c6dd5676108148b4`  
		Last Modified: Mon, 03 Jun 2024 19:06:04 GMT  
		Size: 26.8 KB (26824 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240603` - linux; ppc64le

```console
$ docker pull odoo@sha256:0856f0f465f1b5b833a0c16f6b19477c350dd2deed09cf45a4a702252d7b498a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618662213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e95d0390dfcc84047e153065aef7e99b91fe2fc0c3bd02670a9af4cbffe347`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=en_US.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=17.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b7cf94291ea168ccdc203965a79f54603a4fe2e0738a3acf0f7a8d860e51f32`  
		Last Modified: Sat, 27 Apr 2024 14:45:49 GMT  
		Size: 34.5 MB (34461223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bce02f901cf510611efea394056d49156c523020e7866f490882de224ce1b1a`  
		Last Modified: Mon, 03 Jun 2024 20:25:14 GMT  
		Size: 243.3 MB (243268710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7569fd4e274fa888d627a653da68757f3aaa2d15e3317c784c447dacb0b2679d`  
		Last Modified: Mon, 03 Jun 2024 20:25:08 GMT  
		Size: 2.6 MB (2590185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c9341ba472ae76dc395f908a80ca185dad8148f5986e657cb22a3b4b384087`  
		Last Modified: Mon, 03 Jun 2024 20:25:08 GMT  
		Size: 458.9 KB (458865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90e5365300593d6d11e6affc8a4a6251367c2d2f49f53d0b908b33623180c5f`  
		Last Modified: Mon, 03 Jun 2024 20:25:17 GMT  
		Size: 337.9 MB (337880786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675798c532e30897f37b9c91e259b8d5e8be79056ad0370c79f4e9298b8628b3`  
		Last Modified: Mon, 03 Jun 2024 20:25:09 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf9fdd935295a3f0b7dab9acc7ceaf72813f116e69aa656740d0aba442427b0`  
		Last Modified: Mon, 03 Jun 2024 20:25:09 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441e05cd7712649de3e0e166e53597bc421009e25681e9d8a65c2a95f0365800`  
		Last Modified: Mon, 03 Jun 2024 20:25:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ff6e0501abd44013545fd3ecb373135d92c28eeaa39ebc790bcfdb8215ecb5`  
		Last Modified: Mon, 03 Jun 2024 20:25:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240603` - unknown; unknown

```console
$ docker pull odoo@sha256:2fd939615c1fd7a00f5534348b9a35b44ec25fb841a1a44401b6b84b49cd6b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39341201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efd48bf83eec2d5ab288dd29e9ad2a7a10ef06457107e5ac62ba4910d481017`

```dockerfile
```

-	Layers:
	-	`sha256:fc0367739dd3c1d03e14e1e784a7e055d7009cb3f283f9a0bb3b579c6463e9d4`  
		Last Modified: Mon, 03 Jun 2024 20:25:09 GMT  
		Size: 39.3 MB (39314319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5d9f3d8bf81f6ce0c12e1dfbc92854051085d16ec70be00063c47c90ce9882`  
		Last Modified: Mon, 03 Jun 2024 20:25:08 GMT  
		Size: 26.9 KB (26882 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:48bad8ffbdc44d5484d9df549003280366b825c62ad6f89606b0f97858eb1adc
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
$ docker pull odoo@sha256:b1835727995e26d5a72cfea80c02ddf945db335c25f4b9b86659b682932c4e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.2 MB (602168305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2086f8679982da30baea29ae0d58225776b05aa4b9e2f0bd682e7848fad86d01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=en_US.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=17.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44eaebb0065b22d1b5d29a1502b577d49f7daf66f8c417e72874985cfc87b1b`  
		Last Modified: Mon, 03 Jun 2024 19:06:10 GMT  
		Size: 233.7 MB (233720506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f91a6c22c481d3db69bf9208e32849c13db426f37a31244b891086430cf1d`  
		Last Modified: Mon, 03 Jun 2024 19:06:04 GMT  
		Size: 2.3 MB (2313314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696eda90bbc8bb2451c254583a438ad2ca97e509cb8200284bd0d34dd0dc9a5e`  
		Last Modified: Mon, 03 Jun 2024 19:06:04 GMT  
		Size: 458.8 KB (458839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9528e3f214f3d5bc4194a8097feff627e6977ef1a615a2093a444faeb21bce0e`  
		Last Modified: Mon, 03 Jun 2024 19:06:15 GMT  
		Size: 336.1 MB (336139255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8e4c5e4411d23314944570fbb3e5be506e887ca90086c32d3383f7d8713b23`  
		Last Modified: Mon, 03 Jun 2024 19:06:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6c5559a2b951b779bfe8b75bf7a0fee396dd4a043be940a96d562bba48db80`  
		Last Modified: Mon, 03 Jun 2024 19:06:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44b0b0009d7b03e2ef405b77f50ab0ad92342f8f7c197fabecca318e94edc84`  
		Last Modified: Mon, 03 Jun 2024 19:06:06 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21b342ff1762301d7121131a730a0f95ac991fd06d1a810b1654eea9bb6b29`  
		Last Modified: Mon, 03 Jun 2024 19:06:07 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:617b743f0f9f952915fd4481db9e3a0bc730c4cfcca1ae2beec189d64dfcfb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39332830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54d00a03ff3707d2fc7299389bfdc2e92e2af7a5a37a491d0dcd694c7292ce3`

```dockerfile
```

-	Layers:
	-	`sha256:76ccc89cafe3dbdc38f1a0a979234e184433d488ca666d76487b0f791e2f7811`  
		Last Modified: Mon, 03 Jun 2024 19:06:06 GMT  
		Size: 39.3 MB (39306006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ed3bb05a401b587169b42b20edad1f64c83b7f067c7729c6dd5676108148b4`  
		Last Modified: Mon, 03 Jun 2024 19:06:04 GMT  
		Size: 26.8 KB (26824 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a693628cbf707e6b0732304d3598dc95b64b2fc6ff66b20fdae18854af931ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.6 MB (596618598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233581163c27a01b077bdce6e1a6a1edd49a7668961642e8b370c85ccdcaca32`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271df60fb2ae7fabd06f5f0fe628403f944bdeba6ceab1507d1d47f8583818c9`  
		Last Modified: Thu, 30 May 2024 02:20:00 GMT  
		Size: 231.1 MB (231129260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d721b04ceea49496f804f547d035ef6e841f1aba7ba13634b871a0a262553ddc`  
		Last Modified: Thu, 30 May 2024 02:19:56 GMT  
		Size: 2.3 MB (2306364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffb0c1ef8ee904225d9eb157f0951f47e738b7919d7427b352e0fcdf644980d`  
		Last Modified: Thu, 30 May 2024 02:19:55 GMT  
		Size: 458.8 KB (458826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f3009fc0ca9a84938ba7632ccbbb79e015de10d56f522f91d5a572b5ecb717`  
		Last Modified: Thu, 30 May 2024 02:20:05 GMT  
		Size: 335.4 MB (335361176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d207689c892df07a8c4c6c6e6dde8ed6edebcac90c38b59eb8d9840f21326c98`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bd5863589606d080b8aec7ee8fafbd4185ba02cc6f0c1de2687f7730b8fb30`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110ad8920a2fc0c2f4a513ea1405bca112e1b9f0187c822961a63f7e70323ef2`  
		Last Modified: Thu, 30 May 2024 02:19:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94e49bae97ebf9195e865e845a98d83141e8998e7ffc54b68328895b45c7a31`  
		Last Modified: Thu, 30 May 2024 02:19:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:984e016c32de2f01b3a50ed71dee5d5283965222a4b1799b9f777133cd87097c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39226161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48795314c03b1ca80e5b7732f9db1df97f2eea32eeb265f19835c5465e33907b`

```dockerfile
```

-	Layers:
	-	`sha256:f376677805c31ca437af69a2de7f17a49d8c7db2fe9465c5ab8ff3784746c19b`  
		Last Modified: Thu, 30 May 2024 02:19:57 GMT  
		Size: 39.2 MB (39199354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a42aeafd36498d0983a7a9c5b37104a1246819387fe978af4601edc2030027d`  
		Last Modified: Thu, 30 May 2024 02:19:55 GMT  
		Size: 26.8 KB (26807 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:0856f0f465f1b5b833a0c16f6b19477c350dd2deed09cf45a4a702252d7b498a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618662213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e95d0390dfcc84047e153065aef7e99b91fe2fc0c3bd02670a9af4cbffe347`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 08:31:02 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 03 Jun 2024 08:31:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV LANG=en_US.UTF-8
# Mon, 03 Jun 2024 08:31:02 GMT
ARG TARGETARCH
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=17.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 03 Jun 2024 08:31:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 03 Jun 2024 08:31:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
USER odoo
# Mon, 03 Jun 2024 08:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 08:31:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b7cf94291ea168ccdc203965a79f54603a4fe2e0738a3acf0f7a8d860e51f32`  
		Last Modified: Sat, 27 Apr 2024 14:45:49 GMT  
		Size: 34.5 MB (34461223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bce02f901cf510611efea394056d49156c523020e7866f490882de224ce1b1a`  
		Last Modified: Mon, 03 Jun 2024 20:25:14 GMT  
		Size: 243.3 MB (243268710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7569fd4e274fa888d627a653da68757f3aaa2d15e3317c784c447dacb0b2679d`  
		Last Modified: Mon, 03 Jun 2024 20:25:08 GMT  
		Size: 2.6 MB (2590185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c9341ba472ae76dc395f908a80ca185dad8148f5986e657cb22a3b4b384087`  
		Last Modified: Mon, 03 Jun 2024 20:25:08 GMT  
		Size: 458.9 KB (458865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90e5365300593d6d11e6affc8a4a6251367c2d2f49f53d0b908b33623180c5f`  
		Last Modified: Mon, 03 Jun 2024 20:25:17 GMT  
		Size: 337.9 MB (337880786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675798c532e30897f37b9c91e259b8d5e8be79056ad0370c79f4e9298b8628b3`  
		Last Modified: Mon, 03 Jun 2024 20:25:09 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf9fdd935295a3f0b7dab9acc7ceaf72813f116e69aa656740d0aba442427b0`  
		Last Modified: Mon, 03 Jun 2024 20:25:09 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441e05cd7712649de3e0e166e53597bc421009e25681e9d8a65c2a95f0365800`  
		Last Modified: Mon, 03 Jun 2024 20:25:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ff6e0501abd44013545fd3ecb373135d92c28eeaa39ebc790bcfdb8215ecb5`  
		Last Modified: Mon, 03 Jun 2024 20:25:11 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:2fd939615c1fd7a00f5534348b9a35b44ec25fb841a1a44401b6b84b49cd6b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39341201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efd48bf83eec2d5ab288dd29e9ad2a7a10ef06457107e5ac62ba4910d481017`

```dockerfile
```

-	Layers:
	-	`sha256:fc0367739dd3c1d03e14e1e784a7e055d7009cb3f283f9a0bb3b579c6463e9d4`  
		Last Modified: Mon, 03 Jun 2024 20:25:09 GMT  
		Size: 39.3 MB (39314319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5d9f3d8bf81f6ce0c12e1dfbc92854051085d16ec70be00063c47c90ce9882`  
		Last Modified: Mon, 03 Jun 2024 20:25:08 GMT  
		Size: 26.9 KB (26882 bytes)  
		MIME: application/vnd.in-toto+json
