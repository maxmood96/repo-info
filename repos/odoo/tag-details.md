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
$ docker pull odoo@sha256:29ce6a70b8a955fefba9d900d115c62bd074c43eb8b2fca69ec5e3cf5519a9d6
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
$ docker pull odoo@sha256:2b60a06614fca98c9f8a1848a20e06a46b9e85a028981b6aaebefff78de678ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.7 MB (578675482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07501d5280bc94c1bd2519ae343ac59525fd9b65a2e823f8249e1f7d5fac52d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=16.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e2aa30cc0cf08e8fdc3e41695741978aea7cab831e534fa5a23ef604e37617`  
		Last Modified: Tue, 04 Jun 2024 09:02:01 GMT  
		Size: 216.9 MB (216900172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4504004d65ab2e8a19c5a18750ca9f960b5d8c5a83c221acfb683dabac25bda`  
		Last Modified: Tue, 04 Jun 2024 09:01:57 GMT  
		Size: 2.4 MB (2393316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a8a1e844ee8c7ba47b2d5686de7244fb471696bf3a8c4706f7e3e8c7772bf4`  
		Last Modified: Tue, 04 Jun 2024 09:01:57 GMT  
		Size: 457.8 KB (457805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c7a22517818178fe8f146f95c60bb3274e26272bd2fa216341202727a0e297`  
		Last Modified: Tue, 04 Jun 2024 09:02:04 GMT  
		Size: 328.8 MB (328834845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276f75d84cb4d640fd788e0338dc8fdc0880f09ff114feb865ef91b291b06b0b`  
		Last Modified: Tue, 04 Jun 2024 09:01:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae73b1cfd3a6e6ff1d7d4b150f7ae3653cd0ae65895ced5dac5ccdb40a2a4ab4`  
		Last Modified: Tue, 04 Jun 2024 09:01:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42f36cf75aff7103815987878fdc4fa9ae086d3ad6e3db0bf0acd22aa26f12a`  
		Last Modified: Tue, 04 Jun 2024 09:01:59 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991b8b664e17b3aa4b672d5e969558b44c3da2d4b5dc9fb8dd413811c9893a4`  
		Last Modified: Tue, 04 Jun 2024 09:02:00 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:b91d2f33d08c04d4480aea3c05be0592ff95d303e0cba4fc263686a186f51218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38576640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa2af3b73b105ec600df3c215475cc43baed2f7d4b49602ed231bd78efd81c6`

```dockerfile
```

-	Layers:
	-	`sha256:8d9cff7059feb5fdab34ae89a2947a5d9d95cc3ae8d19c3e961042ceab2f1646`  
		Last Modified: Tue, 04 Jun 2024 09:01:58 GMT  
		Size: 38.5 MB (38549850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecf3a06f4d74bcde1e2d4b2894f6575c3b552d9b5eb566aa1a5db82ea3efe881`  
		Last Modified: Tue, 04 Jun 2024 09:01:56 GMT  
		Size: 26.8 KB (26790 bytes)  
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
$ docker pull odoo@sha256:29ce6a70b8a955fefba9d900d115c62bd074c43eb8b2fca69ec5e3cf5519a9d6
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
$ docker pull odoo@sha256:2b60a06614fca98c9f8a1848a20e06a46b9e85a028981b6aaebefff78de678ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.7 MB (578675482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07501d5280bc94c1bd2519ae343ac59525fd9b65a2e823f8249e1f7d5fac52d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=16.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e2aa30cc0cf08e8fdc3e41695741978aea7cab831e534fa5a23ef604e37617`  
		Last Modified: Tue, 04 Jun 2024 09:02:01 GMT  
		Size: 216.9 MB (216900172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4504004d65ab2e8a19c5a18750ca9f960b5d8c5a83c221acfb683dabac25bda`  
		Last Modified: Tue, 04 Jun 2024 09:01:57 GMT  
		Size: 2.4 MB (2393316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a8a1e844ee8c7ba47b2d5686de7244fb471696bf3a8c4706f7e3e8c7772bf4`  
		Last Modified: Tue, 04 Jun 2024 09:01:57 GMT  
		Size: 457.8 KB (457805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c7a22517818178fe8f146f95c60bb3274e26272bd2fa216341202727a0e297`  
		Last Modified: Tue, 04 Jun 2024 09:02:04 GMT  
		Size: 328.8 MB (328834845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276f75d84cb4d640fd788e0338dc8fdc0880f09ff114feb865ef91b291b06b0b`  
		Last Modified: Tue, 04 Jun 2024 09:01:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae73b1cfd3a6e6ff1d7d4b150f7ae3653cd0ae65895ced5dac5ccdb40a2a4ab4`  
		Last Modified: Tue, 04 Jun 2024 09:01:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42f36cf75aff7103815987878fdc4fa9ae086d3ad6e3db0bf0acd22aa26f12a`  
		Last Modified: Tue, 04 Jun 2024 09:01:59 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991b8b664e17b3aa4b672d5e969558b44c3da2d4b5dc9fb8dd413811c9893a4`  
		Last Modified: Tue, 04 Jun 2024 09:02:00 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b91d2f33d08c04d4480aea3c05be0592ff95d303e0cba4fc263686a186f51218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38576640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa2af3b73b105ec600df3c215475cc43baed2f7d4b49602ed231bd78efd81c6`

```dockerfile
```

-	Layers:
	-	`sha256:8d9cff7059feb5fdab34ae89a2947a5d9d95cc3ae8d19c3e961042ceab2f1646`  
		Last Modified: Tue, 04 Jun 2024 09:01:58 GMT  
		Size: 38.5 MB (38549850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecf3a06f4d74bcde1e2d4b2894f6575c3b552d9b5eb566aa1a5db82ea3efe881`  
		Last Modified: Tue, 04 Jun 2024 09:01:56 GMT  
		Size: 26.8 KB (26790 bytes)  
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
$ docker pull odoo@sha256:29ce6a70b8a955fefba9d900d115c62bd074c43eb8b2fca69ec5e3cf5519a9d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
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

### `odoo:16.0-20240603` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2b60a06614fca98c9f8a1848a20e06a46b9e85a028981b6aaebefff78de678ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.7 MB (578675482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07501d5280bc94c1bd2519ae343ac59525fd9b65a2e823f8249e1f7d5fac52d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=16.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=65abfbaad1715b42c627987cefceb1d63a9bf501
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e2aa30cc0cf08e8fdc3e41695741978aea7cab831e534fa5a23ef604e37617`  
		Last Modified: Tue, 04 Jun 2024 09:02:01 GMT  
		Size: 216.9 MB (216900172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4504004d65ab2e8a19c5a18750ca9f960b5d8c5a83c221acfb683dabac25bda`  
		Last Modified: Tue, 04 Jun 2024 09:01:57 GMT  
		Size: 2.4 MB (2393316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a8a1e844ee8c7ba47b2d5686de7244fb471696bf3a8c4706f7e3e8c7772bf4`  
		Last Modified: Tue, 04 Jun 2024 09:01:57 GMT  
		Size: 457.8 KB (457805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c7a22517818178fe8f146f95c60bb3274e26272bd2fa216341202727a0e297`  
		Last Modified: Tue, 04 Jun 2024 09:02:04 GMT  
		Size: 328.8 MB (328834845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276f75d84cb4d640fd788e0338dc8fdc0880f09ff114feb865ef91b291b06b0b`  
		Last Modified: Tue, 04 Jun 2024 09:01:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae73b1cfd3a6e6ff1d7d4b150f7ae3653cd0ae65895ced5dac5ccdb40a2a4ab4`  
		Last Modified: Tue, 04 Jun 2024 09:01:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42f36cf75aff7103815987878fdc4fa9ae086d3ad6e3db0bf0acd22aa26f12a`  
		Last Modified: Tue, 04 Jun 2024 09:01:59 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991b8b664e17b3aa4b672d5e969558b44c3da2d4b5dc9fb8dd413811c9893a4`  
		Last Modified: Tue, 04 Jun 2024 09:02:00 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240603` - unknown; unknown

```console
$ docker pull odoo@sha256:b91d2f33d08c04d4480aea3c05be0592ff95d303e0cba4fc263686a186f51218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.6 MB (38576640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa2af3b73b105ec600df3c215475cc43baed2f7d4b49602ed231bd78efd81c6`

```dockerfile
```

-	Layers:
	-	`sha256:8d9cff7059feb5fdab34ae89a2947a5d9d95cc3ae8d19c3e961042ceab2f1646`  
		Last Modified: Tue, 04 Jun 2024 09:01:58 GMT  
		Size: 38.5 MB (38549850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecf3a06f4d74bcde1e2d4b2894f6575c3b552d9b5eb566aa1a5db82ea3efe881`  
		Last Modified: Tue, 04 Jun 2024 09:01:56 GMT  
		Size: 26.8 KB (26790 bytes)  
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
$ docker pull odoo@sha256:734e0253475816d0869dbaea8f69a920eb6ea16b763204aefadddcee7b169ceb
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
$ docker pull odoo@sha256:af14dc15bc06e0561a8cf98b7648ff87408a6a11ef0f71e8b1284e22f19a41f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.2 MB (602174649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b8db6db108352002d9cebd5435588849bbad817639423ea7bbbb4191ab9695`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 08:31:02 GMT
ARG RELEASE
# Mon, 03 Jun 2024 08:31:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 08:31:02 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 08:31:02 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0060d99b7538c3f2c55229d50cb8ec3084b139dde4914573844673d29b618f`  
		Last Modified: Wed, 05 Jun 2024 02:24:14 GMT  
		Size: 233.7 MB (233726192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6892e9fb77ee105b2306d3ea7718857c542c050b71f829054aaf6ce4554819`  
		Last Modified: Wed, 05 Jun 2024 02:24:10 GMT  
		Size: 2.3 MB (2313358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07f4a59748861fabfd02c0e0d4ee0a79e65e7ad8f130cf6a0d4425ddb9d193d`  
		Last Modified: Wed, 05 Jun 2024 02:24:10 GMT  
		Size: 458.9 KB (458898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9a920a46218438472b05ed6537a422dd3641d7627fcc31c214c3eb12bfa986`  
		Last Modified: Wed, 05 Jun 2024 02:24:15 GMT  
		Size: 336.1 MB (336140004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c990b9fe60d5cb5a8a7ad877326bf2772ce8673f3cfb0522e606b541d290d4`  
		Last Modified: Wed, 05 Jun 2024 02:24:11 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cfe9af6c91e6aeeecbc8569fa9160be9a57e072c6273dfa593b7d255f22c53`  
		Last Modified: Wed, 05 Jun 2024 02:24:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29edf81ca22eab4482ef2ee2aaf9b89287dfaae5180835e8eaf641048e34e8ac`  
		Last Modified: Wed, 05 Jun 2024 02:24:12 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40069cc7e264d95247e7cf2e9d15448a4cd0f3859e10b8619d69414a8b5082dd`  
		Last Modified: Wed, 05 Jun 2024 02:24:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:9f58caa1c9a6e0c30b9b8a946e9b6977d499c4fb1dd939a616f13d9a9a45cdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39332831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca2715e9aa05135ff2607288db463938c47b69555cea0ea32c09477111c2388`

```dockerfile
```

-	Layers:
	-	`sha256:18193b82e6704555ea3e5d8d7f2f3965e045153ce992676b88cc7ffe8f82f0a5`  
		Last Modified: Wed, 05 Jun 2024 02:24:11 GMT  
		Size: 39.3 MB (39306006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c84b916d07e57bd4120be9a8a61290962c6283b652821c322bde0c7cb687f35`  
		Last Modified: Wed, 05 Jun 2024 02:24:10 GMT  
		Size: 26.8 KB (26825 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:783d9a83e7f84cf99cdfac6b0afa79f5299ba320ac7ce2d5a3164124d006c2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.0 MB (596993042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ba352cf72acd07cee55ba0c7ee4441c42cd6062d07a187e926004f3d686c66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 08:31:02 GMT
ARG RELEASE
# Mon, 03 Jun 2024 08:31:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 08:31:02 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 08:31:02 GMT
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
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=17.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47c85e7c880a0b6a0829c41cdd1087784692d8fdbe4814d2a5ea6d83b6f3b5b`  
		Last Modified: Wed, 05 Jun 2024 16:47:36 GMT  
		Size: 231.1 MB (231129490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841be736c8c6adb83390654e12c5e97a2001d96c8d6a80f06b45ae6232d2244e`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 2.3 MB (2307615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109bd45dc8c7ace62c95b96ba7639f50653e7d4c4403ee4cd76b84b03a6a098c`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 458.8 KB (458815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b48313c4dd97d4376313cbaab07a69ff0a8e6a6c134815c06ff60b5921c34a1`  
		Last Modified: Wed, 05 Jun 2024 16:47:42 GMT  
		Size: 335.7 MB (335732898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c5c6fba9ac6d27c750fe1a46fa872acf561b743b9e13ee4c7f5d0863b2ec94`  
		Last Modified: Wed, 05 Jun 2024 16:47:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada0509a1752dcbaefd33deba938d6b4cbb17e2614fc009b5195977eac68855`  
		Last Modified: Wed, 05 Jun 2024 16:47:32 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bc2ec3d090642c91be763a0e3ca75fdf0ade676c95022f03ec5cd5de7ca7c0`  
		Last Modified: Wed, 05 Jun 2024 16:47:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a72e5a12b01212343fd317269857a2d973095055d832de83804cfcafd4eac`  
		Last Modified: Wed, 05 Jun 2024 16:47:33 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:15eb3e0ea5b6f6f73be641476983aa7f94637db62058d3821b88a73f2cdc6a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39339658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f415ec6beb876e5162fb969205c49991f876b7ea6ac3ef90edd709e51e812e58`

```dockerfile
```

-	Layers:
	-	`sha256:c4a79fa78efc4fa5dabd17bd3007dbbd925ab7dc6b91ddfb1675492efc8f995b`  
		Last Modified: Wed, 05 Jun 2024 16:47:32 GMT  
		Size: 39.3 MB (39312531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a67463925ae57cc6457c794582a350a7d1c211ba84898d184f80232de22031`  
		Last Modified: Wed, 05 Jun 2024 16:47:30 GMT  
		Size: 27.1 KB (27127 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:e7d3c1bc20e6961ea2493b2ea3229571da1e18fda26db2c543ce89b4f9e30db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618665749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa8ee8f37f82a2ad51afc915ae6c70d21e171028eee59a4f028017d7e3de397`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 08:31:02 GMT
ARG RELEASE
# Mon, 03 Jun 2024 08:31:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 08:31:02 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 08:31:02 GMT
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
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956fde24697c2bc63ebe0420d94352a09737c296dbd2b36955ee2062e9c0c770`  
		Last Modified: Wed, 05 Jun 2024 14:46:18 GMT  
		Size: 243.3 MB (243268694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ece47ec5864af7e8863954a92dd9f2fc7c049d58deae4e2b4860da85c7ffc64`  
		Last Modified: Wed, 05 Jun 2024 14:46:10 GMT  
		Size: 2.6 MB (2590044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490d2e7a7a95f94f8af2670a352815aca65e795ab1b0f1c0de54ac5c7d0c32a`  
		Last Modified: Wed, 05 Jun 2024 14:46:09 GMT  
		Size: 458.9 KB (458905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f148a04d71dc94ce4a032551f114e9a92de7fda2926f11ef016efe478c6753a9`  
		Last Modified: Wed, 05 Jun 2024 14:46:18 GMT  
		Size: 337.9 MB (337884969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3139750d141005a5ddcf58d0e9235560290d27942b55482993b7b94b07a6461b`  
		Last Modified: Wed, 05 Jun 2024 14:46:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a784f439ade721f837952054404d607017d097da3666ba7b85c7f60c34fd721`  
		Last Modified: Wed, 05 Jun 2024 14:46:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f76b89b926cec393497e3167e2fab33437d0f499b5b763182a233e49884cc1e`  
		Last Modified: Wed, 05 Jun 2024 14:46:12 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab1973a91417f87239d06d968bcb851aa4a5adb0c92bb65405b880b07271fbb`  
		Last Modified: Wed, 05 Jun 2024 14:46:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:7f788b2bd8f469e71e53d0faedf8e5cb70695b5a4d249710d42cf1d4f08413c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39341201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da133d14c762cb785c74fefd91131a67c1ef92deef9442ee8063e281b81d9f4`

```dockerfile
```

-	Layers:
	-	`sha256:0dc4b120a74cab98f422d7219e01d9959701de442e1ec4a4a5c042d94de0b16d`  
		Last Modified: Wed, 05 Jun 2024 14:46:11 GMT  
		Size: 39.3 MB (39314319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:665b1577c728ab0564d2b9b32d08ce38637b655ba96840a886765f93809d7d61`  
		Last Modified: Wed, 05 Jun 2024 14:46:09 GMT  
		Size: 26.9 KB (26882 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:734e0253475816d0869dbaea8f69a920eb6ea16b763204aefadddcee7b169ceb
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
$ docker pull odoo@sha256:af14dc15bc06e0561a8cf98b7648ff87408a6a11ef0f71e8b1284e22f19a41f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.2 MB (602174649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b8db6db108352002d9cebd5435588849bbad817639423ea7bbbb4191ab9695`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 08:31:02 GMT
ARG RELEASE
# Mon, 03 Jun 2024 08:31:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 08:31:02 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 08:31:02 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0060d99b7538c3f2c55229d50cb8ec3084b139dde4914573844673d29b618f`  
		Last Modified: Wed, 05 Jun 2024 02:24:14 GMT  
		Size: 233.7 MB (233726192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6892e9fb77ee105b2306d3ea7718857c542c050b71f829054aaf6ce4554819`  
		Last Modified: Wed, 05 Jun 2024 02:24:10 GMT  
		Size: 2.3 MB (2313358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07f4a59748861fabfd02c0e0d4ee0a79e65e7ad8f130cf6a0d4425ddb9d193d`  
		Last Modified: Wed, 05 Jun 2024 02:24:10 GMT  
		Size: 458.9 KB (458898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9a920a46218438472b05ed6537a422dd3641d7627fcc31c214c3eb12bfa986`  
		Last Modified: Wed, 05 Jun 2024 02:24:15 GMT  
		Size: 336.1 MB (336140004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c990b9fe60d5cb5a8a7ad877326bf2772ce8673f3cfb0522e606b541d290d4`  
		Last Modified: Wed, 05 Jun 2024 02:24:11 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cfe9af6c91e6aeeecbc8569fa9160be9a57e072c6273dfa593b7d255f22c53`  
		Last Modified: Wed, 05 Jun 2024 02:24:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29edf81ca22eab4482ef2ee2aaf9b89287dfaae5180835e8eaf641048e34e8ac`  
		Last Modified: Wed, 05 Jun 2024 02:24:12 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40069cc7e264d95247e7cf2e9d15448a4cd0f3859e10b8619d69414a8b5082dd`  
		Last Modified: Wed, 05 Jun 2024 02:24:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9f58caa1c9a6e0c30b9b8a946e9b6977d499c4fb1dd939a616f13d9a9a45cdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39332831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca2715e9aa05135ff2607288db463938c47b69555cea0ea32c09477111c2388`

```dockerfile
```

-	Layers:
	-	`sha256:18193b82e6704555ea3e5d8d7f2f3965e045153ce992676b88cc7ffe8f82f0a5`  
		Last Modified: Wed, 05 Jun 2024 02:24:11 GMT  
		Size: 39.3 MB (39306006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c84b916d07e57bd4120be9a8a61290962c6283b652821c322bde0c7cb687f35`  
		Last Modified: Wed, 05 Jun 2024 02:24:10 GMT  
		Size: 26.8 KB (26825 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:783d9a83e7f84cf99cdfac6b0afa79f5299ba320ac7ce2d5a3164124d006c2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.0 MB (596993042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ba352cf72acd07cee55ba0c7ee4441c42cd6062d07a187e926004f3d686c66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 08:31:02 GMT
ARG RELEASE
# Mon, 03 Jun 2024 08:31:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 08:31:02 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 08:31:02 GMT
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
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=17.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47c85e7c880a0b6a0829c41cdd1087784692d8fdbe4814d2a5ea6d83b6f3b5b`  
		Last Modified: Wed, 05 Jun 2024 16:47:36 GMT  
		Size: 231.1 MB (231129490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841be736c8c6adb83390654e12c5e97a2001d96c8d6a80f06b45ae6232d2244e`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 2.3 MB (2307615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109bd45dc8c7ace62c95b96ba7639f50653e7d4c4403ee4cd76b84b03a6a098c`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 458.8 KB (458815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b48313c4dd97d4376313cbaab07a69ff0a8e6a6c134815c06ff60b5921c34a1`  
		Last Modified: Wed, 05 Jun 2024 16:47:42 GMT  
		Size: 335.7 MB (335732898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c5c6fba9ac6d27c750fe1a46fa872acf561b743b9e13ee4c7f5d0863b2ec94`  
		Last Modified: Wed, 05 Jun 2024 16:47:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada0509a1752dcbaefd33deba938d6b4cbb17e2614fc009b5195977eac68855`  
		Last Modified: Wed, 05 Jun 2024 16:47:32 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bc2ec3d090642c91be763a0e3ca75fdf0ade676c95022f03ec5cd5de7ca7c0`  
		Last Modified: Wed, 05 Jun 2024 16:47:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a72e5a12b01212343fd317269857a2d973095055d832de83804cfcafd4eac`  
		Last Modified: Wed, 05 Jun 2024 16:47:33 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:15eb3e0ea5b6f6f73be641476983aa7f94637db62058d3821b88a73f2cdc6a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39339658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f415ec6beb876e5162fb969205c49991f876b7ea6ac3ef90edd709e51e812e58`

```dockerfile
```

-	Layers:
	-	`sha256:c4a79fa78efc4fa5dabd17bd3007dbbd925ab7dc6b91ddfb1675492efc8f995b`  
		Last Modified: Wed, 05 Jun 2024 16:47:32 GMT  
		Size: 39.3 MB (39312531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a67463925ae57cc6457c794582a350a7d1c211ba84898d184f80232de22031`  
		Last Modified: Wed, 05 Jun 2024 16:47:30 GMT  
		Size: 27.1 KB (27127 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:e7d3c1bc20e6961ea2493b2ea3229571da1e18fda26db2c543ce89b4f9e30db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618665749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa8ee8f37f82a2ad51afc915ae6c70d21e171028eee59a4f028017d7e3de397`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 08:31:02 GMT
ARG RELEASE
# Mon, 03 Jun 2024 08:31:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 08:31:02 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 08:31:02 GMT
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
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956fde24697c2bc63ebe0420d94352a09737c296dbd2b36955ee2062e9c0c770`  
		Last Modified: Wed, 05 Jun 2024 14:46:18 GMT  
		Size: 243.3 MB (243268694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ece47ec5864af7e8863954a92dd9f2fc7c049d58deae4e2b4860da85c7ffc64`  
		Last Modified: Wed, 05 Jun 2024 14:46:10 GMT  
		Size: 2.6 MB (2590044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490d2e7a7a95f94f8af2670a352815aca65e795ab1b0f1c0de54ac5c7d0c32a`  
		Last Modified: Wed, 05 Jun 2024 14:46:09 GMT  
		Size: 458.9 KB (458905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f148a04d71dc94ce4a032551f114e9a92de7fda2926f11ef016efe478c6753a9`  
		Last Modified: Wed, 05 Jun 2024 14:46:18 GMT  
		Size: 337.9 MB (337884969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3139750d141005a5ddcf58d0e9235560290d27942b55482993b7b94b07a6461b`  
		Last Modified: Wed, 05 Jun 2024 14:46:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a784f439ade721f837952054404d607017d097da3666ba7b85c7f60c34fd721`  
		Last Modified: Wed, 05 Jun 2024 14:46:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f76b89b926cec393497e3167e2fab33437d0f499b5b763182a233e49884cc1e`  
		Last Modified: Wed, 05 Jun 2024 14:46:12 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab1973a91417f87239d06d968bcb851aa4a5adb0c92bb65405b880b07271fbb`  
		Last Modified: Wed, 05 Jun 2024 14:46:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7f788b2bd8f469e71e53d0faedf8e5cb70695b5a4d249710d42cf1d4f08413c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39341201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da133d14c762cb785c74fefd91131a67c1ef92deef9442ee8063e281b81d9f4`

```dockerfile
```

-	Layers:
	-	`sha256:0dc4b120a74cab98f422d7219e01d9959701de442e1ec4a4a5c042d94de0b16d`  
		Last Modified: Wed, 05 Jun 2024 14:46:11 GMT  
		Size: 39.3 MB (39314319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:665b1577c728ab0564d2b9b32d08ce38637b655ba96840a886765f93809d7d61`  
		Last Modified: Wed, 05 Jun 2024 14:46:09 GMT  
		Size: 26.9 KB (26882 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240603`

```console
$ docker pull odoo@sha256:734e0253475816d0869dbaea8f69a920eb6ea16b763204aefadddcee7b169ceb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20240603` - linux; amd64

```console
$ docker pull odoo@sha256:af14dc15bc06e0561a8cf98b7648ff87408a6a11ef0f71e8b1284e22f19a41f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.2 MB (602174649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b8db6db108352002d9cebd5435588849bbad817639423ea7bbbb4191ab9695`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 08:31:02 GMT
ARG RELEASE
# Mon, 03 Jun 2024 08:31:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 08:31:02 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 08:31:02 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0060d99b7538c3f2c55229d50cb8ec3084b139dde4914573844673d29b618f`  
		Last Modified: Wed, 05 Jun 2024 02:24:14 GMT  
		Size: 233.7 MB (233726192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6892e9fb77ee105b2306d3ea7718857c542c050b71f829054aaf6ce4554819`  
		Last Modified: Wed, 05 Jun 2024 02:24:10 GMT  
		Size: 2.3 MB (2313358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07f4a59748861fabfd02c0e0d4ee0a79e65e7ad8f130cf6a0d4425ddb9d193d`  
		Last Modified: Wed, 05 Jun 2024 02:24:10 GMT  
		Size: 458.9 KB (458898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9a920a46218438472b05ed6537a422dd3641d7627fcc31c214c3eb12bfa986`  
		Last Modified: Wed, 05 Jun 2024 02:24:15 GMT  
		Size: 336.1 MB (336140004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c990b9fe60d5cb5a8a7ad877326bf2772ce8673f3cfb0522e606b541d290d4`  
		Last Modified: Wed, 05 Jun 2024 02:24:11 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cfe9af6c91e6aeeecbc8569fa9160be9a57e072c6273dfa593b7d255f22c53`  
		Last Modified: Wed, 05 Jun 2024 02:24:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29edf81ca22eab4482ef2ee2aaf9b89287dfaae5180835e8eaf641048e34e8ac`  
		Last Modified: Wed, 05 Jun 2024 02:24:12 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40069cc7e264d95247e7cf2e9d15448a4cd0f3859e10b8619d69414a8b5082dd`  
		Last Modified: Wed, 05 Jun 2024 02:24:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240603` - unknown; unknown

```console
$ docker pull odoo@sha256:9f58caa1c9a6e0c30b9b8a946e9b6977d499c4fb1dd939a616f13d9a9a45cdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39332831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca2715e9aa05135ff2607288db463938c47b69555cea0ea32c09477111c2388`

```dockerfile
```

-	Layers:
	-	`sha256:18193b82e6704555ea3e5d8d7f2f3965e045153ce992676b88cc7ffe8f82f0a5`  
		Last Modified: Wed, 05 Jun 2024 02:24:11 GMT  
		Size: 39.3 MB (39306006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c84b916d07e57bd4120be9a8a61290962c6283b652821c322bde0c7cb687f35`  
		Last Modified: Wed, 05 Jun 2024 02:24:10 GMT  
		Size: 26.8 KB (26825 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240603` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:783d9a83e7f84cf99cdfac6b0afa79f5299ba320ac7ce2d5a3164124d006c2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.0 MB (596993042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ba352cf72acd07cee55ba0c7ee4441c42cd6062d07a187e926004f3d686c66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 08:31:02 GMT
ARG RELEASE
# Mon, 03 Jun 2024 08:31:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 08:31:02 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 08:31:02 GMT
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
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=17.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47c85e7c880a0b6a0829c41cdd1087784692d8fdbe4814d2a5ea6d83b6f3b5b`  
		Last Modified: Wed, 05 Jun 2024 16:47:36 GMT  
		Size: 231.1 MB (231129490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841be736c8c6adb83390654e12c5e97a2001d96c8d6a80f06b45ae6232d2244e`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 2.3 MB (2307615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109bd45dc8c7ace62c95b96ba7639f50653e7d4c4403ee4cd76b84b03a6a098c`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 458.8 KB (458815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b48313c4dd97d4376313cbaab07a69ff0a8e6a6c134815c06ff60b5921c34a1`  
		Last Modified: Wed, 05 Jun 2024 16:47:42 GMT  
		Size: 335.7 MB (335732898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c5c6fba9ac6d27c750fe1a46fa872acf561b743b9e13ee4c7f5d0863b2ec94`  
		Last Modified: Wed, 05 Jun 2024 16:47:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada0509a1752dcbaefd33deba938d6b4cbb17e2614fc009b5195977eac68855`  
		Last Modified: Wed, 05 Jun 2024 16:47:32 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bc2ec3d090642c91be763a0e3ca75fdf0ade676c95022f03ec5cd5de7ca7c0`  
		Last Modified: Wed, 05 Jun 2024 16:47:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a72e5a12b01212343fd317269857a2d973095055d832de83804cfcafd4eac`  
		Last Modified: Wed, 05 Jun 2024 16:47:33 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240603` - unknown; unknown

```console
$ docker pull odoo@sha256:15eb3e0ea5b6f6f73be641476983aa7f94637db62058d3821b88a73f2cdc6a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39339658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f415ec6beb876e5162fb969205c49991f876b7ea6ac3ef90edd709e51e812e58`

```dockerfile
```

-	Layers:
	-	`sha256:c4a79fa78efc4fa5dabd17bd3007dbbd925ab7dc6b91ddfb1675492efc8f995b`  
		Last Modified: Wed, 05 Jun 2024 16:47:32 GMT  
		Size: 39.3 MB (39312531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a67463925ae57cc6457c794582a350a7d1c211ba84898d184f80232de22031`  
		Last Modified: Wed, 05 Jun 2024 16:47:30 GMT  
		Size: 27.1 KB (27127 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240603` - linux; ppc64le

```console
$ docker pull odoo@sha256:e7d3c1bc20e6961ea2493b2ea3229571da1e18fda26db2c543ce89b4f9e30db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618665749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa8ee8f37f82a2ad51afc915ae6c70d21e171028eee59a4f028017d7e3de397`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 08:31:02 GMT
ARG RELEASE
# Mon, 03 Jun 2024 08:31:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 08:31:02 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 08:31:02 GMT
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
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956fde24697c2bc63ebe0420d94352a09737c296dbd2b36955ee2062e9c0c770`  
		Last Modified: Wed, 05 Jun 2024 14:46:18 GMT  
		Size: 243.3 MB (243268694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ece47ec5864af7e8863954a92dd9f2fc7c049d58deae4e2b4860da85c7ffc64`  
		Last Modified: Wed, 05 Jun 2024 14:46:10 GMT  
		Size: 2.6 MB (2590044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490d2e7a7a95f94f8af2670a352815aca65e795ab1b0f1c0de54ac5c7d0c32a`  
		Last Modified: Wed, 05 Jun 2024 14:46:09 GMT  
		Size: 458.9 KB (458905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f148a04d71dc94ce4a032551f114e9a92de7fda2926f11ef016efe478c6753a9`  
		Last Modified: Wed, 05 Jun 2024 14:46:18 GMT  
		Size: 337.9 MB (337884969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3139750d141005a5ddcf58d0e9235560290d27942b55482993b7b94b07a6461b`  
		Last Modified: Wed, 05 Jun 2024 14:46:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a784f439ade721f837952054404d607017d097da3666ba7b85c7f60c34fd721`  
		Last Modified: Wed, 05 Jun 2024 14:46:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f76b89b926cec393497e3167e2fab33437d0f499b5b763182a233e49884cc1e`  
		Last Modified: Wed, 05 Jun 2024 14:46:12 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab1973a91417f87239d06d968bcb851aa4a5adb0c92bb65405b880b07271fbb`  
		Last Modified: Wed, 05 Jun 2024 14:46:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240603` - unknown; unknown

```console
$ docker pull odoo@sha256:7f788b2bd8f469e71e53d0faedf8e5cb70695b5a4d249710d42cf1d4f08413c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39341201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da133d14c762cb785c74fefd91131a67c1ef92deef9442ee8063e281b81d9f4`

```dockerfile
```

-	Layers:
	-	`sha256:0dc4b120a74cab98f422d7219e01d9959701de442e1ec4a4a5c042d94de0b16d`  
		Last Modified: Wed, 05 Jun 2024 14:46:11 GMT  
		Size: 39.3 MB (39314319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:665b1577c728ab0564d2b9b32d08ce38637b655ba96840a886765f93809d7d61`  
		Last Modified: Wed, 05 Jun 2024 14:46:09 GMT  
		Size: 26.9 KB (26882 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:734e0253475816d0869dbaea8f69a920eb6ea16b763204aefadddcee7b169ceb
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
$ docker pull odoo@sha256:af14dc15bc06e0561a8cf98b7648ff87408a6a11ef0f71e8b1284e22f19a41f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.2 MB (602174649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b8db6db108352002d9cebd5435588849bbad817639423ea7bbbb4191ab9695`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 08:31:02 GMT
ARG RELEASE
# Mon, 03 Jun 2024 08:31:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 08:31:02 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 08:31:02 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0060d99b7538c3f2c55229d50cb8ec3084b139dde4914573844673d29b618f`  
		Last Modified: Wed, 05 Jun 2024 02:24:14 GMT  
		Size: 233.7 MB (233726192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6892e9fb77ee105b2306d3ea7718857c542c050b71f829054aaf6ce4554819`  
		Last Modified: Wed, 05 Jun 2024 02:24:10 GMT  
		Size: 2.3 MB (2313358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07f4a59748861fabfd02c0e0d4ee0a79e65e7ad8f130cf6a0d4425ddb9d193d`  
		Last Modified: Wed, 05 Jun 2024 02:24:10 GMT  
		Size: 458.9 KB (458898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9a920a46218438472b05ed6537a422dd3641d7627fcc31c214c3eb12bfa986`  
		Last Modified: Wed, 05 Jun 2024 02:24:15 GMT  
		Size: 336.1 MB (336140004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c990b9fe60d5cb5a8a7ad877326bf2772ce8673f3cfb0522e606b541d290d4`  
		Last Modified: Wed, 05 Jun 2024 02:24:11 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cfe9af6c91e6aeeecbc8569fa9160be9a57e072c6273dfa593b7d255f22c53`  
		Last Modified: Wed, 05 Jun 2024 02:24:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29edf81ca22eab4482ef2ee2aaf9b89287dfaae5180835e8eaf641048e34e8ac`  
		Last Modified: Wed, 05 Jun 2024 02:24:12 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40069cc7e264d95247e7cf2e9d15448a4cd0f3859e10b8619d69414a8b5082dd`  
		Last Modified: Wed, 05 Jun 2024 02:24:12 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:9f58caa1c9a6e0c30b9b8a946e9b6977d499c4fb1dd939a616f13d9a9a45cdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39332831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca2715e9aa05135ff2607288db463938c47b69555cea0ea32c09477111c2388`

```dockerfile
```

-	Layers:
	-	`sha256:18193b82e6704555ea3e5d8d7f2f3965e045153ce992676b88cc7ffe8f82f0a5`  
		Last Modified: Wed, 05 Jun 2024 02:24:11 GMT  
		Size: 39.3 MB (39306006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c84b916d07e57bd4120be9a8a61290962c6283b652821c322bde0c7cb687f35`  
		Last Modified: Wed, 05 Jun 2024 02:24:10 GMT  
		Size: 26.8 KB (26825 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:783d9a83e7f84cf99cdfac6b0afa79f5299ba320ac7ce2d5a3164124d006c2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.0 MB (596993042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ba352cf72acd07cee55ba0c7ee4441c42cd6062d07a187e926004f3d686c66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 08:31:02 GMT
ARG RELEASE
# Mon, 03 Jun 2024 08:31:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 08:31:02 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 08:31:02 GMT
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
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
ENV ODOO_VERSION=17.0
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_RELEASE=20240603
# Mon, 03 Jun 2024 08:31:02 GMT
ARG ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 03 Jun 2024 08:31:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240603 ODOO_SHA=abc6bbaa55dfecd2b6e00463db48ecac412db1fa
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47c85e7c880a0b6a0829c41cdd1087784692d8fdbe4814d2a5ea6d83b6f3b5b`  
		Last Modified: Wed, 05 Jun 2024 16:47:36 GMT  
		Size: 231.1 MB (231129490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841be736c8c6adb83390654e12c5e97a2001d96c8d6a80f06b45ae6232d2244e`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 2.3 MB (2307615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109bd45dc8c7ace62c95b96ba7639f50653e7d4c4403ee4cd76b84b03a6a098c`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 458.8 KB (458815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b48313c4dd97d4376313cbaab07a69ff0a8e6a6c134815c06ff60b5921c34a1`  
		Last Modified: Wed, 05 Jun 2024 16:47:42 GMT  
		Size: 335.7 MB (335732898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c5c6fba9ac6d27c750fe1a46fa872acf561b743b9e13ee4c7f5d0863b2ec94`  
		Last Modified: Wed, 05 Jun 2024 16:47:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ada0509a1752dcbaefd33deba938d6b4cbb17e2614fc009b5195977eac68855`  
		Last Modified: Wed, 05 Jun 2024 16:47:32 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bc2ec3d090642c91be763a0e3ca75fdf0ade676c95022f03ec5cd5de7ca7c0`  
		Last Modified: Wed, 05 Jun 2024 16:47:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a72e5a12b01212343fd317269857a2d973095055d832de83804cfcafd4eac`  
		Last Modified: Wed, 05 Jun 2024 16:47:33 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:15eb3e0ea5b6f6f73be641476983aa7f94637db62058d3821b88a73f2cdc6a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39339658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f415ec6beb876e5162fb969205c49991f876b7ea6ac3ef90edd709e51e812e58`

```dockerfile
```

-	Layers:
	-	`sha256:c4a79fa78efc4fa5dabd17bd3007dbbd925ab7dc6b91ddfb1675492efc8f995b`  
		Last Modified: Wed, 05 Jun 2024 16:47:32 GMT  
		Size: 39.3 MB (39312531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a67463925ae57cc6457c794582a350a7d1c211ba84898d184f80232de22031`  
		Last Modified: Wed, 05 Jun 2024 16:47:30 GMT  
		Size: 27.1 KB (27127 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:e7d3c1bc20e6961ea2493b2ea3229571da1e18fda26db2c543ce89b4f9e30db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618665749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfa8ee8f37f82a2ad51afc915ae6c70d21e171028eee59a4f028017d7e3de397`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 08:31:02 GMT
ARG RELEASE
# Mon, 03 Jun 2024 08:31:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 08:31:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 08:31:02 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 08:31:02 GMT
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
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956fde24697c2bc63ebe0420d94352a09737c296dbd2b36955ee2062e9c0c770`  
		Last Modified: Wed, 05 Jun 2024 14:46:18 GMT  
		Size: 243.3 MB (243268694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ece47ec5864af7e8863954a92dd9f2fc7c049d58deae4e2b4860da85c7ffc64`  
		Last Modified: Wed, 05 Jun 2024 14:46:10 GMT  
		Size: 2.6 MB (2590044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490d2e7a7a95f94f8af2670a352815aca65e795ab1b0f1c0de54ac5c7d0c32a`  
		Last Modified: Wed, 05 Jun 2024 14:46:09 GMT  
		Size: 458.9 KB (458905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f148a04d71dc94ce4a032551f114e9a92de7fda2926f11ef016efe478c6753a9`  
		Last Modified: Wed, 05 Jun 2024 14:46:18 GMT  
		Size: 337.9 MB (337884969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3139750d141005a5ddcf58d0e9235560290d27942b55482993b7b94b07a6461b`  
		Last Modified: Wed, 05 Jun 2024 14:46:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a784f439ade721f837952054404d607017d097da3666ba7b85c7f60c34fd721`  
		Last Modified: Wed, 05 Jun 2024 14:46:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f76b89b926cec393497e3167e2fab33437d0f499b5b763182a233e49884cc1e`  
		Last Modified: Wed, 05 Jun 2024 14:46:12 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab1973a91417f87239d06d968bcb851aa4a5adb0c92bb65405b880b07271fbb`  
		Last Modified: Wed, 05 Jun 2024 14:46:12 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7f788b2bd8f469e71e53d0faedf8e5cb70695b5a4d249710d42cf1d4f08413c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39341201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da133d14c762cb785c74fefd91131a67c1ef92deef9442ee8063e281b81d9f4`

```dockerfile
```

-	Layers:
	-	`sha256:0dc4b120a74cab98f422d7219e01d9959701de442e1ec4a4a5c042d94de0b16d`  
		Last Modified: Wed, 05 Jun 2024 14:46:11 GMT  
		Size: 39.3 MB (39314319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:665b1577c728ab0564d2b9b32d08ce38637b655ba96840a886765f93809d7d61`  
		Last Modified: Wed, 05 Jun 2024 14:46:09 GMT  
		Size: 26.9 KB (26882 bytes)  
		MIME: application/vnd.in-toto+json
