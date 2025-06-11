<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250606`](#odoo160-20250606)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250606`](#odoo170-20250606)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250606`](#odoo180-20250606)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:5e105fc7e648952c37357b2b211bcd2f35e42acf2a9c3f8b18e83b3b18c6d6f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:d58dd63d413958063dbebd6d9a07d45c6bb626d0d929f63d9d9fc2aa7d322126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.9 MB (584911023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d58259a27ce3703d3d5c91d0641efe3f86d6d066af8dbb596b908f70882ede`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 06 Jun 2025 14:44:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=C.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=amd64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=16.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374407731e109b5436acaf268923a59a2b99f7405e32858c02d81fbdeb97909d`  
		Last Modified: Wed, 11 Jun 2025 01:13:09 GMT  
		Size: 219.6 MB (219626738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e003f23bda056f64e9a0feb2e40cf4f8bf09edba8556232f453e691982bee53`  
		Last Modified: Tue, 10 Jun 2025 23:44:44 GMT  
		Size: 2.6 MB (2627138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fe207828595147a13505d121763dfc365cdfba79458753e8366a5f1496fd30`  
		Last Modified: Tue, 10 Jun 2025 23:44:43 GMT  
		Size: 478.9 KB (478926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3570cb4eb495a94c4631a057bf3785a6007a2e2406e463c38bc9494fcdad752b`  
		Last Modified: Wed, 11 Jun 2025 01:13:23 GMT  
		Size: 331.9 MB (331919729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2de98cb0fe4e4cf5629b4c61be5123f1107e807a959ad052e6a21872860106`  
		Last Modified: Tue, 10 Jun 2025 23:44:44 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675ad2ce58fab711fdb7060dcacd1ae92a19b8fca2a2a32b0f2d50a593c0ba3d`  
		Last Modified: Tue, 10 Jun 2025 23:44:43 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc16b88287f7a3ddb2c86602eeb0cc76d0d79858271c42c9c55295970b30dfc5`  
		Last Modified: Tue, 10 Jun 2025 23:44:44 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350f4aebde134a81f85833de5fd12e459da1a7e463a030eae18c0d803ac0fd54`  
		Last Modified: Tue, 10 Jun 2025 23:44:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:7bf1acf34e8839f900031948f83e44002fa584de8b992b6f51570cd636f5dede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39550612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936d74dba2a4b8016d1ed2d7cc3b6808dd5042d118494be39011a15e4ce443ac`

```dockerfile
```

-	Layers:
	-	`sha256:3a30ce12256ec79a44e8da263001f229a56092ef360cb9797b44da22a240850f`  
		Last Modified: Wed, 11 Jun 2025 01:12:38 GMT  
		Size: 39.5 MB (39523895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c39cfdf16999e46eaf0f1bfea5a296482e6f8353e30766b66ec41fe2ee70afc`  
		Last Modified: Wed, 11 Jun 2025 01:12:39 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:36c60714cfe2c4ba4b2070d1ac0a014541ea7eb81e2e206334edbb6e585a6da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.9 MB (581930240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71e61d7310a77c57d2a4eaf54d2aa66eb7a50a25a03cff424b0dd048ebadfae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=C.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=arm64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=16.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9476b7a4e88461986ad5951a333edbdf8b690af7e7f35cbb8409c9b79e923d`  
		Last Modified: Fri, 06 Jun 2025 20:34:05 GMT  
		Size: 218.5 MB (218476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5c2b5a93487142a7785022fa1593902936985b10d6ece49d971572c11027fb`  
		Last Modified: Fri, 06 Jun 2025 17:33:53 GMT  
		Size: 2.6 MB (2635686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8539cadb1e1b321e36e39c5bfa226a1cb34abc2a544d02e2161c3cefbc2725`  
		Last Modified: Fri, 06 Jun 2025 17:33:53 GMT  
		Size: 478.9 KB (478929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2e98bd438cc1f6d0fec791bab56ab2ce4d8e239b999fa37cabc98251795365`  
		Last Modified: Fri, 06 Jun 2025 20:34:37 GMT  
		Size: 331.6 MB (331590593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6175c8a514f711d6db1691a53c8c83223a63051b4aa6e26217f4edae5f905ad1`  
		Last Modified: Fri, 06 Jun 2025 17:33:51 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1dc975973c66b85736e452beac76d129e8172e7758276e7e8aa5d4b2b3c88b`  
		Last Modified: Fri, 06 Jun 2025 17:33:52 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caf24bc24e182a2586a970273360013b009187aa1f1c493d025b7aece3ad761`  
		Last Modified: Fri, 06 Jun 2025 17:33:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53029613bc98a2793b4a4e853387ee0238438ff5986077d334631658bccbb692`  
		Last Modified: Fri, 06 Jun 2025 17:33:52 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:0d53d74b6f4ca6632ec9f93b82dcb0260c86ec632c0a3d4606068d6373ac1257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38982840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab95e596b4e39b0e227b7240505a26d253d164250662771b6167c0662e33448d`

```dockerfile
```

-	Layers:
	-	`sha256:ca937507c52c1afc993ca7e7f5d50d325251827d076e301feecf16df305bb675`  
		Last Modified: Fri, 06 Jun 2025 19:13:06 GMT  
		Size: 39.0 MB (38955970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46e71a1881d0ff15dbc2e1076c7281690ff0bfc2eeef433f248a086d1001498c`  
		Last Modified: Fri, 06 Jun 2025 19:13:07 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:5e105fc7e648952c37357b2b211bcd2f35e42acf2a9c3f8b18e83b3b18c6d6f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:d58dd63d413958063dbebd6d9a07d45c6bb626d0d929f63d9d9fc2aa7d322126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.9 MB (584911023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d58259a27ce3703d3d5c91d0641efe3f86d6d066af8dbb596b908f70882ede`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 06 Jun 2025 14:44:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=C.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=amd64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=16.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374407731e109b5436acaf268923a59a2b99f7405e32858c02d81fbdeb97909d`  
		Last Modified: Wed, 11 Jun 2025 01:13:09 GMT  
		Size: 219.6 MB (219626738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e003f23bda056f64e9a0feb2e40cf4f8bf09edba8556232f453e691982bee53`  
		Last Modified: Tue, 10 Jun 2025 23:44:44 GMT  
		Size: 2.6 MB (2627138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fe207828595147a13505d121763dfc365cdfba79458753e8366a5f1496fd30`  
		Last Modified: Tue, 10 Jun 2025 23:44:43 GMT  
		Size: 478.9 KB (478926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3570cb4eb495a94c4631a057bf3785a6007a2e2406e463c38bc9494fcdad752b`  
		Last Modified: Wed, 11 Jun 2025 01:13:23 GMT  
		Size: 331.9 MB (331919729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2de98cb0fe4e4cf5629b4c61be5123f1107e807a959ad052e6a21872860106`  
		Last Modified: Tue, 10 Jun 2025 23:44:44 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675ad2ce58fab711fdb7060dcacd1ae92a19b8fca2a2a32b0f2d50a593c0ba3d`  
		Last Modified: Tue, 10 Jun 2025 23:44:43 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc16b88287f7a3ddb2c86602eeb0cc76d0d79858271c42c9c55295970b30dfc5`  
		Last Modified: Tue, 10 Jun 2025 23:44:44 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350f4aebde134a81f85833de5fd12e459da1a7e463a030eae18c0d803ac0fd54`  
		Last Modified: Tue, 10 Jun 2025 23:44:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7bf1acf34e8839f900031948f83e44002fa584de8b992b6f51570cd636f5dede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39550612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936d74dba2a4b8016d1ed2d7cc3b6808dd5042d118494be39011a15e4ce443ac`

```dockerfile
```

-	Layers:
	-	`sha256:3a30ce12256ec79a44e8da263001f229a56092ef360cb9797b44da22a240850f`  
		Last Modified: Wed, 11 Jun 2025 01:12:38 GMT  
		Size: 39.5 MB (39523895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c39cfdf16999e46eaf0f1bfea5a296482e6f8353e30766b66ec41fe2ee70afc`  
		Last Modified: Wed, 11 Jun 2025 01:12:39 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:36c60714cfe2c4ba4b2070d1ac0a014541ea7eb81e2e206334edbb6e585a6da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.9 MB (581930240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71e61d7310a77c57d2a4eaf54d2aa66eb7a50a25a03cff424b0dd048ebadfae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=C.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=arm64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=16.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9476b7a4e88461986ad5951a333edbdf8b690af7e7f35cbb8409c9b79e923d`  
		Last Modified: Fri, 06 Jun 2025 20:34:05 GMT  
		Size: 218.5 MB (218476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5c2b5a93487142a7785022fa1593902936985b10d6ece49d971572c11027fb`  
		Last Modified: Fri, 06 Jun 2025 17:33:53 GMT  
		Size: 2.6 MB (2635686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8539cadb1e1b321e36e39c5bfa226a1cb34abc2a544d02e2161c3cefbc2725`  
		Last Modified: Fri, 06 Jun 2025 17:33:53 GMT  
		Size: 478.9 KB (478929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2e98bd438cc1f6d0fec791bab56ab2ce4d8e239b999fa37cabc98251795365`  
		Last Modified: Fri, 06 Jun 2025 20:34:37 GMT  
		Size: 331.6 MB (331590593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6175c8a514f711d6db1691a53c8c83223a63051b4aa6e26217f4edae5f905ad1`  
		Last Modified: Fri, 06 Jun 2025 17:33:51 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1dc975973c66b85736e452beac76d129e8172e7758276e7e8aa5d4b2b3c88b`  
		Last Modified: Fri, 06 Jun 2025 17:33:52 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caf24bc24e182a2586a970273360013b009187aa1f1c493d025b7aece3ad761`  
		Last Modified: Fri, 06 Jun 2025 17:33:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53029613bc98a2793b4a4e853387ee0238438ff5986077d334631658bccbb692`  
		Last Modified: Fri, 06 Jun 2025 17:33:52 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0d53d74b6f4ca6632ec9f93b82dcb0260c86ec632c0a3d4606068d6373ac1257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38982840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab95e596b4e39b0e227b7240505a26d253d164250662771b6167c0662e33448d`

```dockerfile
```

-	Layers:
	-	`sha256:ca937507c52c1afc993ca7e7f5d50d325251827d076e301feecf16df305bb675`  
		Last Modified: Fri, 06 Jun 2025 19:13:06 GMT  
		Size: 39.0 MB (38955970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46e71a1881d0ff15dbc2e1076c7281690ff0bfc2eeef433f248a086d1001498c`  
		Last Modified: Fri, 06 Jun 2025 19:13:07 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250606`

```console
$ docker pull odoo@sha256:5e105fc7e648952c37357b2b211bcd2f35e42acf2a9c3f8b18e83b3b18c6d6f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250606` - linux; amd64

```console
$ docker pull odoo@sha256:d58dd63d413958063dbebd6d9a07d45c6bb626d0d929f63d9d9fc2aa7d322126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.9 MB (584911023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d58259a27ce3703d3d5c91d0641efe3f86d6d066af8dbb596b908f70882ede`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 06 Jun 2025 14:44:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=C.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=amd64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=16.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374407731e109b5436acaf268923a59a2b99f7405e32858c02d81fbdeb97909d`  
		Last Modified: Wed, 11 Jun 2025 01:13:09 GMT  
		Size: 219.6 MB (219626738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e003f23bda056f64e9a0feb2e40cf4f8bf09edba8556232f453e691982bee53`  
		Last Modified: Tue, 10 Jun 2025 23:44:44 GMT  
		Size: 2.6 MB (2627138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fe207828595147a13505d121763dfc365cdfba79458753e8366a5f1496fd30`  
		Last Modified: Tue, 10 Jun 2025 23:44:43 GMT  
		Size: 478.9 KB (478926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3570cb4eb495a94c4631a057bf3785a6007a2e2406e463c38bc9494fcdad752b`  
		Last Modified: Wed, 11 Jun 2025 01:13:23 GMT  
		Size: 331.9 MB (331919729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2de98cb0fe4e4cf5629b4c61be5123f1107e807a959ad052e6a21872860106`  
		Last Modified: Tue, 10 Jun 2025 23:44:44 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675ad2ce58fab711fdb7060dcacd1ae92a19b8fca2a2a32b0f2d50a593c0ba3d`  
		Last Modified: Tue, 10 Jun 2025 23:44:43 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc16b88287f7a3ddb2c86602eeb0cc76d0d79858271c42c9c55295970b30dfc5`  
		Last Modified: Tue, 10 Jun 2025 23:44:44 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350f4aebde134a81f85833de5fd12e459da1a7e463a030eae18c0d803ac0fd54`  
		Last Modified: Tue, 10 Jun 2025 23:44:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250606` - unknown; unknown

```console
$ docker pull odoo@sha256:7bf1acf34e8839f900031948f83e44002fa584de8b992b6f51570cd636f5dede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39550612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936d74dba2a4b8016d1ed2d7cc3b6808dd5042d118494be39011a15e4ce443ac`

```dockerfile
```

-	Layers:
	-	`sha256:3a30ce12256ec79a44e8da263001f229a56092ef360cb9797b44da22a240850f`  
		Last Modified: Wed, 11 Jun 2025 01:12:38 GMT  
		Size: 39.5 MB (39523895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c39cfdf16999e46eaf0f1bfea5a296482e6f8353e30766b66ec41fe2ee70afc`  
		Last Modified: Wed, 11 Jun 2025 01:12:39 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250606` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:36c60714cfe2c4ba4b2070d1ac0a014541ea7eb81e2e206334edbb6e585a6da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.9 MB (581930240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71e61d7310a77c57d2a4eaf54d2aa66eb7a50a25a03cff424b0dd048ebadfae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=C.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=arm64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=16.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=6c17bfea51c8b371140b947b14e7e44ef65f1b08
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9476b7a4e88461986ad5951a333edbdf8b690af7e7f35cbb8409c9b79e923d`  
		Last Modified: Fri, 06 Jun 2025 20:34:05 GMT  
		Size: 218.5 MB (218476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5c2b5a93487142a7785022fa1593902936985b10d6ece49d971572c11027fb`  
		Last Modified: Fri, 06 Jun 2025 17:33:53 GMT  
		Size: 2.6 MB (2635686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8539cadb1e1b321e36e39c5bfa226a1cb34abc2a544d02e2161c3cefbc2725`  
		Last Modified: Fri, 06 Jun 2025 17:33:53 GMT  
		Size: 478.9 KB (478929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2e98bd438cc1f6d0fec791bab56ab2ce4d8e239b999fa37cabc98251795365`  
		Last Modified: Fri, 06 Jun 2025 20:34:37 GMT  
		Size: 331.6 MB (331590593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6175c8a514f711d6db1691a53c8c83223a63051b4aa6e26217f4edae5f905ad1`  
		Last Modified: Fri, 06 Jun 2025 17:33:51 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1dc975973c66b85736e452beac76d129e8172e7758276e7e8aa5d4b2b3c88b`  
		Last Modified: Fri, 06 Jun 2025 17:33:52 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caf24bc24e182a2586a970273360013b009187aa1f1c493d025b7aece3ad761`  
		Last Modified: Fri, 06 Jun 2025 17:33:52 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53029613bc98a2793b4a4e853387ee0238438ff5986077d334631658bccbb692`  
		Last Modified: Fri, 06 Jun 2025 17:33:52 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250606` - unknown; unknown

```console
$ docker pull odoo@sha256:0d53d74b6f4ca6632ec9f93b82dcb0260c86ec632c0a3d4606068d6373ac1257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38982840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab95e596b4e39b0e227b7240505a26d253d164250662771b6167c0662e33448d`

```dockerfile
```

-	Layers:
	-	`sha256:ca937507c52c1afc993ca7e7f5d50d325251827d076e301feecf16df305bb675`  
		Last Modified: Fri, 06 Jun 2025 19:13:06 GMT  
		Size: 39.0 MB (38955970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46e71a1881d0ff15dbc2e1076c7281690ff0bfc2eeef433f248a086d1001498c`  
		Last Modified: Fri, 06 Jun 2025 19:13:07 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:c6a43962705f8b7fb378db5ac630eea3581b9d8623e680a5b3b7ac4f67575eb0
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
$ docker pull odoo@sha256:7106bc6fb9d367753ac70533b07257d39b72dc528356f421cbe873329eab383d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600960374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5312a98ce76701b62ce5b64749cde0f54e0e7dc552b9ffd8fbb84552ed10b531`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=amd64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=17.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a75dd4757359ee26c2e1d8887ba4fe127242b70c3d8998bc89e282bb5f0a08d`  
		Last Modified: Fri, 06 Jun 2025 19:12:48 GMT  
		Size: 233.8 MB (233779969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b817eb147d3521e6f49dfbffb172a58211bd7c69ebe751e9e52eae43f604145`  
		Last Modified: Fri, 06 Jun 2025 17:32:54 GMT  
		Size: 2.5 MB (2522979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23998548a3b751d893b5419de8d4bd2052bfe1d387489474f7502f57c089cb8`  
		Last Modified: Fri, 06 Jun 2025 17:33:06 GMT  
		Size: 480.0 KB (479967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f73e73fc62b5d30c4840fed4d8fa3c6231f668470c3edd2f72d7244d84947f`  
		Last Modified: Fri, 06 Jun 2025 19:12:53 GMT  
		Size: 334.6 MB (334642018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5668eead2b6d51aacca513503516e7edd7aa8242c098357a4a95cc13f1dd6f49`  
		Last Modified: Fri, 06 Jun 2025 17:33:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583a73e0ed4018ce8a3735864fadfa78916b1d02e5bda577cc39b72884435b8`  
		Last Modified: Fri, 06 Jun 2025 17:33:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c543ef7194c866dfa1a06ed7098e509a8684568a83ee3dbb1083393cd4e5c0ef`  
		Last Modified: Fri, 06 Jun 2025 17:33:17 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6afb85961d5a12ab042e2185d91692d00d3a5fd6085b5da3406e7fe8b630cc9`  
		Last Modified: Fri, 06 Jun 2025 17:33:21 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:0f80527583f55014dfb87838926fcb75756def3101734bd0fafb428930380612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39896338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8056a19cc7f905b6d720df719f1a9ef18f9b3b56cc0c2264bb04a557ac3ca3`

```dockerfile
```

-	Layers:
	-	`sha256:a44e5c447e6e96cd426f0d455599bdf8f624c79fc9e34cd44334061041bb1892`  
		Last Modified: Fri, 06 Jun 2025 19:12:39 GMT  
		Size: 39.9 MB (39869503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f14f165504302f10e00c686cc2d726ffc20e47e6f361dd1598bc55eed09c53df`  
		Last Modified: Fri, 06 Jun 2025 19:12:40 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:15369048234039e992ce0df3ba63112f48fdf9ddd164727f84895adc1b67ae65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 MB (595752821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4ccba74e036a119afc0b55c37ec559788704577ac70e0bdfd36793f742563a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=arm64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=17.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ec0718f997931fbe341cd742f18641bf91f7619d4631a3998bd00b372da275`  
		Last Modified: Tue, 03 Jun 2025 13:56:42 GMT  
		Size: 231.1 MB (231144514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a70dcb9f54bb32e38d0a8e6394083353fe8b3b982315e6887cc3ca87a90c56`  
		Last Modified: Tue, 03 Jun 2025 13:56:28 GMT  
		Size: 2.5 MB (2516242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc17931ec959010bbd9f1fcd517bf0f6ce3fec744f832903684d64fdef50da5`  
		Last Modified: Tue, 03 Jun 2025 13:56:27 GMT  
		Size: 479.9 KB (479945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ed221bdd9a75745f2b1641fca9ca21d024904c0e9fdd666a785d69bf757537`  
		Last Modified: Fri, 06 Jun 2025 19:16:11 GMT  
		Size: 334.3 MB (334254104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5b6bbcef45b83ff4c88abf4528641dc63b199e4ee6ba04f24aa06993fc532b`  
		Last Modified: Fri, 06 Jun 2025 17:30:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6f13d5c61129dbadb5b9722f64321d0572ae4a2039a356d758246d0180bca4`  
		Last Modified: Fri, 06 Jun 2025 17:30:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2d4b94de4017aff1051b01254dc7398b8ed8259fe8b35f6c3c32c9b789fc45`  
		Last Modified: Fri, 06 Jun 2025 17:30:13 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9821d67ad513c67b64a44a56719d65a3b83adc95d351e6a714240fd55be5656a`  
		Last Modified: Fri, 06 Jun 2025 17:30:12 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:b4f923092a8f55988c983e5ecbcff86015976e8fb4f87f5070482ca175e957bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39902997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba73f671b965963171816d20e1bd7d1ac139234dbaa225a71bc384965df11937`

```dockerfile
```

-	Layers:
	-	`sha256:c4b55978a3adb2d4dd3cf7bdc6d594b26babfde46fa88085d7c1d57b91ef7dd8`  
		Last Modified: Fri, 06 Jun 2025 19:13:19 GMT  
		Size: 39.9 MB (39876010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d20fdc84b1932809b167584e9795d1e45ce24cbfe0c6dac3ce8c044d8e2b26`  
		Last Modified: Fri, 06 Jun 2025 19:13:20 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:c2103420b50c47a856f75dca094806d8d4b9bf7c5e971dcc804721571fc70d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.4 MB (617402413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a86edf0f3ac2403328a3bdce0c4183854f1007a0706b8010a3b40e88da20e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:33:39 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:43 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Fri, 30 May 2025 22:33:43 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=ppc64le
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=17.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7226df727826e2ae3e585430603b9896b6efd1bb9ccd5a8c0f458a4fe9c8707`  
		Last Modified: Fri, 06 Jun 2025 20:32:37 GMT  
		Size: 243.3 MB (243258772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f1e9aa712432a5e39ce559cb39ee4eac90c87dd6398e9cd65777b3ec8e0782`  
		Last Modified: Thu, 05 Jun 2025 00:00:11 GMT  
		Size: 2.8 MB (2841449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62a350920074433bd2feba3924cae7668634f2df0cb7b44b7f87325cd59cc6a`  
		Last Modified: Wed, 04 Jun 2025 23:40:12 GMT  
		Size: 480.0 KB (479983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e84465a4e8a30035f31abba7c0ac75facc42afb9e92dfb490f381d86c4c35d`  
		Last Modified: Fri, 06 Jun 2025 20:32:38 GMT  
		Size: 336.4 MB (336379415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecdbfb36f397fdf44d5dfad03c3fa2ec9544c12d74aada47da4e03d102b4382`  
		Last Modified: Fri, 06 Jun 2025 17:36:25 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e97daf110fa9aa8ad295de9ab13682ca0201a2bea453ba45b192168841e57f`  
		Last Modified: Fri, 06 Jun 2025 17:36:26 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf85a360dec40832ca299cd4490ba692c236e879cfc0606bcbb1a626c4d00be`  
		Last Modified: Fri, 06 Jun 2025 17:36:26 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee25605edc31dcd577d63e703a16bc95a6058aea4b243fcb8fac0a766caf61b0`  
		Last Modified: Fri, 06 Jun 2025 17:36:25 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:5eebddcf4e557e7138e74f32a53aa62e69a1ddd448588019c9c55061e5019f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39905001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25533d93975d7a1ed992594a6cb55cf40800ec17ad2a37456e344b7b3aee18f3`

```dockerfile
```

-	Layers:
	-	`sha256:defafb5fcee415e7b119c91f6cfeba7e0cf18b2f786e566cc46b75953dcc1a39`  
		Last Modified: Fri, 06 Jun 2025 19:13:57 GMT  
		Size: 39.9 MB (39878110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62201b9259c97df2ac5188f95b3ff94f6aa54aa72dc83f0126a96305589e9310`  
		Last Modified: Fri, 06 Jun 2025 19:13:58 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:c6a43962705f8b7fb378db5ac630eea3581b9d8623e680a5b3b7ac4f67575eb0
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
$ docker pull odoo@sha256:7106bc6fb9d367753ac70533b07257d39b72dc528356f421cbe873329eab383d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600960374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5312a98ce76701b62ce5b64749cde0f54e0e7dc552b9ffd8fbb84552ed10b531`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=amd64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=17.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a75dd4757359ee26c2e1d8887ba4fe127242b70c3d8998bc89e282bb5f0a08d`  
		Last Modified: Fri, 06 Jun 2025 19:12:48 GMT  
		Size: 233.8 MB (233779969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b817eb147d3521e6f49dfbffb172a58211bd7c69ebe751e9e52eae43f604145`  
		Last Modified: Fri, 06 Jun 2025 17:32:54 GMT  
		Size: 2.5 MB (2522979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23998548a3b751d893b5419de8d4bd2052bfe1d387489474f7502f57c089cb8`  
		Last Modified: Fri, 06 Jun 2025 17:33:06 GMT  
		Size: 480.0 KB (479967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f73e73fc62b5d30c4840fed4d8fa3c6231f668470c3edd2f72d7244d84947f`  
		Last Modified: Fri, 06 Jun 2025 19:12:53 GMT  
		Size: 334.6 MB (334642018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5668eead2b6d51aacca513503516e7edd7aa8242c098357a4a95cc13f1dd6f49`  
		Last Modified: Fri, 06 Jun 2025 17:33:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583a73e0ed4018ce8a3735864fadfa78916b1d02e5bda577cc39b72884435b8`  
		Last Modified: Fri, 06 Jun 2025 17:33:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c543ef7194c866dfa1a06ed7098e509a8684568a83ee3dbb1083393cd4e5c0ef`  
		Last Modified: Fri, 06 Jun 2025 17:33:17 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6afb85961d5a12ab042e2185d91692d00d3a5fd6085b5da3406e7fe8b630cc9`  
		Last Modified: Fri, 06 Jun 2025 17:33:21 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0f80527583f55014dfb87838926fcb75756def3101734bd0fafb428930380612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39896338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8056a19cc7f905b6d720df719f1a9ef18f9b3b56cc0c2264bb04a557ac3ca3`

```dockerfile
```

-	Layers:
	-	`sha256:a44e5c447e6e96cd426f0d455599bdf8f624c79fc9e34cd44334061041bb1892`  
		Last Modified: Fri, 06 Jun 2025 19:12:39 GMT  
		Size: 39.9 MB (39869503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f14f165504302f10e00c686cc2d726ffc20e47e6f361dd1598bc55eed09c53df`  
		Last Modified: Fri, 06 Jun 2025 19:12:40 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:15369048234039e992ce0df3ba63112f48fdf9ddd164727f84895adc1b67ae65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 MB (595752821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4ccba74e036a119afc0b55c37ec559788704577ac70e0bdfd36793f742563a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=arm64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=17.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ec0718f997931fbe341cd742f18641bf91f7619d4631a3998bd00b372da275`  
		Last Modified: Tue, 03 Jun 2025 13:56:42 GMT  
		Size: 231.1 MB (231144514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a70dcb9f54bb32e38d0a8e6394083353fe8b3b982315e6887cc3ca87a90c56`  
		Last Modified: Tue, 03 Jun 2025 13:56:28 GMT  
		Size: 2.5 MB (2516242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc17931ec959010bbd9f1fcd517bf0f6ce3fec744f832903684d64fdef50da5`  
		Last Modified: Tue, 03 Jun 2025 13:56:27 GMT  
		Size: 479.9 KB (479945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ed221bdd9a75745f2b1641fca9ca21d024904c0e9fdd666a785d69bf757537`  
		Last Modified: Fri, 06 Jun 2025 19:16:11 GMT  
		Size: 334.3 MB (334254104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5b6bbcef45b83ff4c88abf4528641dc63b199e4ee6ba04f24aa06993fc532b`  
		Last Modified: Fri, 06 Jun 2025 17:30:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6f13d5c61129dbadb5b9722f64321d0572ae4a2039a356d758246d0180bca4`  
		Last Modified: Fri, 06 Jun 2025 17:30:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2d4b94de4017aff1051b01254dc7398b8ed8259fe8b35f6c3c32c9b789fc45`  
		Last Modified: Fri, 06 Jun 2025 17:30:13 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9821d67ad513c67b64a44a56719d65a3b83adc95d351e6a714240fd55be5656a`  
		Last Modified: Fri, 06 Jun 2025 17:30:12 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b4f923092a8f55988c983e5ecbcff86015976e8fb4f87f5070482ca175e957bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39902997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba73f671b965963171816d20e1bd7d1ac139234dbaa225a71bc384965df11937`

```dockerfile
```

-	Layers:
	-	`sha256:c4b55978a3adb2d4dd3cf7bdc6d594b26babfde46fa88085d7c1d57b91ef7dd8`  
		Last Modified: Fri, 06 Jun 2025 19:13:19 GMT  
		Size: 39.9 MB (39876010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d20fdc84b1932809b167584e9795d1e45ce24cbfe0c6dac3ce8c044d8e2b26`  
		Last Modified: Fri, 06 Jun 2025 19:13:20 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:c2103420b50c47a856f75dca094806d8d4b9bf7c5e971dcc804721571fc70d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.4 MB (617402413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a86edf0f3ac2403328a3bdce0c4183854f1007a0706b8010a3b40e88da20e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:33:39 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:43 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Fri, 30 May 2025 22:33:43 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=ppc64le
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=17.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7226df727826e2ae3e585430603b9896b6efd1bb9ccd5a8c0f458a4fe9c8707`  
		Last Modified: Fri, 06 Jun 2025 20:32:37 GMT  
		Size: 243.3 MB (243258772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f1e9aa712432a5e39ce559cb39ee4eac90c87dd6398e9cd65777b3ec8e0782`  
		Last Modified: Thu, 05 Jun 2025 00:00:11 GMT  
		Size: 2.8 MB (2841449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62a350920074433bd2feba3924cae7668634f2df0cb7b44b7f87325cd59cc6a`  
		Last Modified: Wed, 04 Jun 2025 23:40:12 GMT  
		Size: 480.0 KB (479983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e84465a4e8a30035f31abba7c0ac75facc42afb9e92dfb490f381d86c4c35d`  
		Last Modified: Fri, 06 Jun 2025 20:32:38 GMT  
		Size: 336.4 MB (336379415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecdbfb36f397fdf44d5dfad03c3fa2ec9544c12d74aada47da4e03d102b4382`  
		Last Modified: Fri, 06 Jun 2025 17:36:25 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e97daf110fa9aa8ad295de9ab13682ca0201a2bea453ba45b192168841e57f`  
		Last Modified: Fri, 06 Jun 2025 17:36:26 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf85a360dec40832ca299cd4490ba692c236e879cfc0606bcbb1a626c4d00be`  
		Last Modified: Fri, 06 Jun 2025 17:36:26 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee25605edc31dcd577d63e703a16bc95a6058aea4b243fcb8fac0a766caf61b0`  
		Last Modified: Fri, 06 Jun 2025 17:36:25 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:5eebddcf4e557e7138e74f32a53aa62e69a1ddd448588019c9c55061e5019f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39905001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25533d93975d7a1ed992594a6cb55cf40800ec17ad2a37456e344b7b3aee18f3`

```dockerfile
```

-	Layers:
	-	`sha256:defafb5fcee415e7b119c91f6cfeba7e0cf18b2f786e566cc46b75953dcc1a39`  
		Last Modified: Fri, 06 Jun 2025 19:13:57 GMT  
		Size: 39.9 MB (39878110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62201b9259c97df2ac5188f95b3ff94f6aa54aa72dc83f0126a96305589e9310`  
		Last Modified: Fri, 06 Jun 2025 19:13:58 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250606`

```console
$ docker pull odoo@sha256:c6a43962705f8b7fb378db5ac630eea3581b9d8623e680a5b3b7ac4f67575eb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250606` - linux; amd64

```console
$ docker pull odoo@sha256:7106bc6fb9d367753ac70533b07257d39b72dc528356f421cbe873329eab383d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600960374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5312a98ce76701b62ce5b64749cde0f54e0e7dc552b9ffd8fbb84552ed10b531`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=amd64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=17.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a75dd4757359ee26c2e1d8887ba4fe127242b70c3d8998bc89e282bb5f0a08d`  
		Last Modified: Fri, 06 Jun 2025 19:12:48 GMT  
		Size: 233.8 MB (233779969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b817eb147d3521e6f49dfbffb172a58211bd7c69ebe751e9e52eae43f604145`  
		Last Modified: Fri, 06 Jun 2025 17:32:54 GMT  
		Size: 2.5 MB (2522979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23998548a3b751d893b5419de8d4bd2052bfe1d387489474f7502f57c089cb8`  
		Last Modified: Fri, 06 Jun 2025 17:33:06 GMT  
		Size: 480.0 KB (479967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f73e73fc62b5d30c4840fed4d8fa3c6231f668470c3edd2f72d7244d84947f`  
		Last Modified: Fri, 06 Jun 2025 19:12:53 GMT  
		Size: 334.6 MB (334642018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5668eead2b6d51aacca513503516e7edd7aa8242c098357a4a95cc13f1dd6f49`  
		Last Modified: Fri, 06 Jun 2025 17:33:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583a73e0ed4018ce8a3735864fadfa78916b1d02e5bda577cc39b72884435b8`  
		Last Modified: Fri, 06 Jun 2025 17:33:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c543ef7194c866dfa1a06ed7098e509a8684568a83ee3dbb1083393cd4e5c0ef`  
		Last Modified: Fri, 06 Jun 2025 17:33:17 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6afb85961d5a12ab042e2185d91692d00d3a5fd6085b5da3406e7fe8b630cc9`  
		Last Modified: Fri, 06 Jun 2025 17:33:21 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250606` - unknown; unknown

```console
$ docker pull odoo@sha256:0f80527583f55014dfb87838926fcb75756def3101734bd0fafb428930380612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39896338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8056a19cc7f905b6d720df719f1a9ef18f9b3b56cc0c2264bb04a557ac3ca3`

```dockerfile
```

-	Layers:
	-	`sha256:a44e5c447e6e96cd426f0d455599bdf8f624c79fc9e34cd44334061041bb1892`  
		Last Modified: Fri, 06 Jun 2025 19:12:39 GMT  
		Size: 39.9 MB (39869503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f14f165504302f10e00c686cc2d726ffc20e47e6f361dd1598bc55eed09c53df`  
		Last Modified: Fri, 06 Jun 2025 19:12:40 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250606` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:15369048234039e992ce0df3ba63112f48fdf9ddd164727f84895adc1b67ae65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.8 MB (595752821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4ccba74e036a119afc0b55c37ec559788704577ac70e0bdfd36793f742563a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=arm64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=17.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ec0718f997931fbe341cd742f18641bf91f7619d4631a3998bd00b372da275`  
		Last Modified: Tue, 03 Jun 2025 13:56:42 GMT  
		Size: 231.1 MB (231144514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a70dcb9f54bb32e38d0a8e6394083353fe8b3b982315e6887cc3ca87a90c56`  
		Last Modified: Tue, 03 Jun 2025 13:56:28 GMT  
		Size: 2.5 MB (2516242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc17931ec959010bbd9f1fcd517bf0f6ce3fec744f832903684d64fdef50da5`  
		Last Modified: Tue, 03 Jun 2025 13:56:27 GMT  
		Size: 479.9 KB (479945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ed221bdd9a75745f2b1641fca9ca21d024904c0e9fdd666a785d69bf757537`  
		Last Modified: Fri, 06 Jun 2025 19:16:11 GMT  
		Size: 334.3 MB (334254104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5b6bbcef45b83ff4c88abf4528641dc63b199e4ee6ba04f24aa06993fc532b`  
		Last Modified: Fri, 06 Jun 2025 17:30:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6f13d5c61129dbadb5b9722f64321d0572ae4a2039a356d758246d0180bca4`  
		Last Modified: Fri, 06 Jun 2025 17:30:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2d4b94de4017aff1051b01254dc7398b8ed8259fe8b35f6c3c32c9b789fc45`  
		Last Modified: Fri, 06 Jun 2025 17:30:13 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9821d67ad513c67b64a44a56719d65a3b83adc95d351e6a714240fd55be5656a`  
		Last Modified: Fri, 06 Jun 2025 17:30:12 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250606` - unknown; unknown

```console
$ docker pull odoo@sha256:b4f923092a8f55988c983e5ecbcff86015976e8fb4f87f5070482ca175e957bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39902997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba73f671b965963171816d20e1bd7d1ac139234dbaa225a71bc384965df11937`

```dockerfile
```

-	Layers:
	-	`sha256:c4b55978a3adb2d4dd3cf7bdc6d594b26babfde46fa88085d7c1d57b91ef7dd8`  
		Last Modified: Fri, 06 Jun 2025 19:13:19 GMT  
		Size: 39.9 MB (39876010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d20fdc84b1932809b167584e9795d1e45ce24cbfe0c6dac3ce8c044d8e2b26`  
		Last Modified: Fri, 06 Jun 2025 19:13:20 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250606` - linux; ppc64le

```console
$ docker pull odoo@sha256:c2103420b50c47a856f75dca094806d8d4b9bf7c5e971dcc804721571fc70d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.4 MB (617402413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a86edf0f3ac2403328a3bdce0c4183854f1007a0706b8010a3b40e88da20e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 30 May 2025 22:33:39 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:39 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:43 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Fri, 30 May 2025 22:33:43 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=ppc64le
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=17.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=1898185cb41509fa2eca7ec88dddd37afa356f89
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7226df727826e2ae3e585430603b9896b6efd1bb9ccd5a8c0f458a4fe9c8707`  
		Last Modified: Fri, 06 Jun 2025 20:32:37 GMT  
		Size: 243.3 MB (243258772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f1e9aa712432a5e39ce559cb39ee4eac90c87dd6398e9cd65777b3ec8e0782`  
		Last Modified: Thu, 05 Jun 2025 00:00:11 GMT  
		Size: 2.8 MB (2841449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62a350920074433bd2feba3924cae7668634f2df0cb7b44b7f87325cd59cc6a`  
		Last Modified: Wed, 04 Jun 2025 23:40:12 GMT  
		Size: 480.0 KB (479983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e84465a4e8a30035f31abba7c0ac75facc42afb9e92dfb490f381d86c4c35d`  
		Last Modified: Fri, 06 Jun 2025 20:32:38 GMT  
		Size: 336.4 MB (336379415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecdbfb36f397fdf44d5dfad03c3fa2ec9544c12d74aada47da4e03d102b4382`  
		Last Modified: Fri, 06 Jun 2025 17:36:25 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e97daf110fa9aa8ad295de9ab13682ca0201a2bea453ba45b192168841e57f`  
		Last Modified: Fri, 06 Jun 2025 17:36:26 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf85a360dec40832ca299cd4490ba692c236e879cfc0606bcbb1a626c4d00be`  
		Last Modified: Fri, 06 Jun 2025 17:36:26 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee25605edc31dcd577d63e703a16bc95a6058aea4b243fcb8fac0a766caf61b0`  
		Last Modified: Fri, 06 Jun 2025 17:36:25 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250606` - unknown; unknown

```console
$ docker pull odoo@sha256:5eebddcf4e557e7138e74f32a53aa62e69a1ddd448588019c9c55061e5019f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39905001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25533d93975d7a1ed992594a6cb55cf40800ec17ad2a37456e344b7b3aee18f3`

```dockerfile
```

-	Layers:
	-	`sha256:defafb5fcee415e7b119c91f6cfeba7e0cf18b2f786e566cc46b75953dcc1a39`  
		Last Modified: Fri, 06 Jun 2025 19:13:57 GMT  
		Size: 39.9 MB (39878110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62201b9259c97df2ac5188f95b3ff94f6aa54aa72dc83f0126a96305589e9310`  
		Last Modified: Fri, 06 Jun 2025 19:13:58 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:9ed1354116ba4ffe674a459d65180ce22ccd05bb714fbc8474be5692e8192dd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18` - linux; amd64

```console
$ docker pull odoo@sha256:1b787f53f8615dac47a823100eeee49f7e9df5d3776abbe6bf2f35d7efc86014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.7 MB (671708121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa72d03fe5adc1c3196d05c48f91f2e22f59f63f752a6bba7d964a038f1a25b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=amd64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=18.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d88c54ed93070b52e426687bc4f566ea3629520552cab449ca9aaa9096b5da`  
		Last Modified: Fri, 06 Jun 2025 19:13:24 GMT  
		Size: 254.5 MB (254519024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cfa877a012a36563587636bc84fff944134bc9b13f9988e06373f0f1471b4b`  
		Last Modified: Fri, 06 Jun 2025 17:26:57 GMT  
		Size: 14.3 MB (14275045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220c81613229e6a97ed5a72f7fce510d6426b01e6f241c882e6ebaa5a83e3c0f`  
		Last Modified: Fri, 06 Jun 2025 17:26:57 GMT  
		Size: 479.7 KB (479717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0454584e1bc364dc5bcafe9a3178dc09e6ad3aedbaef72269628c1debd7576f0`  
		Last Modified: Fri, 06 Jun 2025 19:13:32 GMT  
		Size: 372.7 MB (372716558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a35afa233e367c450bcbb71e80ebc0af4ac2a7278609eed658426e9bb69f581`  
		Last Modified: Fri, 06 Jun 2025 17:26:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fdabdbcf811458b0dc91d8977cc81fd9aab01dc01f7ba0957eedf865c24483`  
		Last Modified: Fri, 06 Jun 2025 17:26:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fa914e6c66d9d85b5719c92692be90edb38212ad2ebccf980620beea4add5c`  
		Last Modified: Fri, 06 Jun 2025 17:26:57 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fedf6b4c6972de7e41ef381d028c1de8cb0055eb78829446a02a6ed63db661`  
		Last Modified: Fri, 06 Jun 2025 17:26:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:16bc5f0f2cde93c4303dcd0f46da55f0d1bdda4c57b35ebedd0de644285a949f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59418334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5c4ea92d0161ca3be4d7b6eee40b2abe244df7401388e3fd5ee7025ed46540`

```dockerfile
```

-	Layers:
	-	`sha256:319ea88e724cac196ecff9e6bc61e9d16dc2fa6f02039e25217bc97a360c39ca`  
		Last Modified: Fri, 06 Jun 2025 19:12:59 GMT  
		Size: 59.4 MB (59391198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6facbb3600e4f3d4b4da9bae9f0cb11a46df60e7e4025a92946274fba9580e`  
		Last Modified: Fri, 06 Jun 2025 19:13:01 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b7ae820754cd858baca901dbb417547d4144905dcc7c540d0af34c851703c36f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.1 MB (668096864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d77a8ef0c3be0e563d33ef064b298487f59521e797dc81f746ec4b88efc1cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=arm64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=18.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4315199468ce86f2db99234ac7b624c3ff21f9015cb49bcc83244dc5d1e18b`  
		Last Modified: Tue, 03 Jun 2025 13:32:40 GMT  
		Size: 251.9 MB (251941614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e313ca65afe3e86a5825bb239f3b567abf0e6c64a1af4a1e55865dff947432`  
		Last Modified: Tue, 03 Jun 2025 13:31:32 GMT  
		Size: 14.3 MB (14252778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db30f637b9fad6dd03fa06fe2981c8e0d743f0f24c2b216c7f749532a567008`  
		Last Modified: Tue, 03 Jun 2025 13:31:26 GMT  
		Size: 479.7 KB (479713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6775706cc821df9d664e60d09d4e7f3235f19731c3254d6c6b549aacdf25c1a7`  
		Last Modified: Fri, 06 Jun 2025 19:14:42 GMT  
		Size: 372.6 MB (372568420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43fcb891cd90c74e1c52befb217eb6d2aef3ccf8faef195f6867a56d3f33b83`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0a9ba66273c9998333d6120ad2a3452367b9223b04ec01454a7497fc00dac7`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feeb8bccb61a176403b16993a65a6a6b62029f1943d025b6af47f735879d820`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95b155297d4750e744a3a60619d4afb92f454b489a03b79c7e670bfe872d397`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:6c849da87f47b9a5a592398bbe3716dfd23f3806e06389a8bf4dcf08b3b99ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59425785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7877e3f519c93112191659e56ed8480a2032ed50401960c4f6e5c5c45325ea4b`

```dockerfile
```

-	Layers:
	-	`sha256:9dc87255e4d736a646974adeb92140f682c1686594104eaa552721ab00fac157`  
		Last Modified: Fri, 06 Jun 2025 19:14:28 GMT  
		Size: 59.4 MB (59398485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db17698e08cc822a974d027e6cac3e4d0601150c9e2260e5daa61dca019d0fe5`  
		Last Modified: Fri, 06 Jun 2025 19:14:29 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:9d185e6dc8c1746a022396c03d0003133d944b9b2ba2f347d533cad98fa6f050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.9 MB (687933601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82e52384b41aa1e5d2a9eeea692542177ea608c018398bed34e19250e5b981b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:29:58 GMT
ARG RELEASE
# Thu, 29 May 2025 04:29:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:02 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Thu, 29 May 2025 04:30:02 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=ppc64le
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=18.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a5b95226fecfdc3ba76d3eedd24473ed37062675a8ada707540009b28ef1c3`  
		Last Modified: Tue, 03 Jun 2025 14:34:31 GMT  
		Size: 265.1 MB (265076915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5e13c1a1d9c93366a170b1e6a11b74a42e1df0387d6a43545841af0af93069`  
		Last Modified: Tue, 03 Jun 2025 14:34:10 GMT  
		Size: 14.8 MB (14798210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3651a97c6ca59b6f4b02957ee8ca413a53501e5cfac770618183dea46fa2fa8d`  
		Last Modified: Tue, 03 Jun 2025 14:34:59 GMT  
		Size: 479.8 KB (479803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9a60ea5994ffc057d5a570094e7ded0c81f17bfbd4fdd6e92673ba3b14582`  
		Last Modified: Fri, 06 Jun 2025 20:31:08 GMT  
		Size: 373.3 MB (373251023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540a5953fd75b9c55b3bd0146b344c4b90557bb17e731149179e1e29fa4c9ef4`  
		Last Modified: Fri, 06 Jun 2025 17:51:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dd7aadec0757effd4351988657970427e3bd440fdccfe7bc5e03ad79d0c915`  
		Last Modified: Fri, 06 Jun 2025 17:51:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee4bdc441c22cf9429948a0b0a94cc8a3a1226a37d3df9b549030d37f318c0b`  
		Last Modified: Fri, 06 Jun 2025 17:51:22 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa7172b1978088755e635b5a093953948fedb14d46a62c3972f121aa54631af`  
		Last Modified: Fri, 06 Jun 2025 17:51:25 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:f09e1af0c1cd26327b8e827f775b0d9a6be4ff320155e7b5a0224d24fcbe4971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59426785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b7a8d382d5d16e83a60c28c09bb52eb350f8fffd478edcecdfc8dc79c6a7ee`

```dockerfile
```

-	Layers:
	-	`sha256:47c01571b36f22a7218958047fa308232fd341fff8bd15116493aa39bf09e1ad`  
		Last Modified: Fri, 06 Jun 2025 19:15:37 GMT  
		Size: 59.4 MB (59399587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a58444853ca8db065f1ad4303bad0182d4292f89d5767e4ff5f327ff58f69a`  
		Last Modified: Fri, 06 Jun 2025 19:15:38 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:9ed1354116ba4ffe674a459d65180ce22ccd05bb714fbc8474be5692e8192dd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0` - linux; amd64

```console
$ docker pull odoo@sha256:1b787f53f8615dac47a823100eeee49f7e9df5d3776abbe6bf2f35d7efc86014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.7 MB (671708121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa72d03fe5adc1c3196d05c48f91f2e22f59f63f752a6bba7d964a038f1a25b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=amd64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=18.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d88c54ed93070b52e426687bc4f566ea3629520552cab449ca9aaa9096b5da`  
		Last Modified: Fri, 06 Jun 2025 19:13:24 GMT  
		Size: 254.5 MB (254519024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cfa877a012a36563587636bc84fff944134bc9b13f9988e06373f0f1471b4b`  
		Last Modified: Fri, 06 Jun 2025 17:26:57 GMT  
		Size: 14.3 MB (14275045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220c81613229e6a97ed5a72f7fce510d6426b01e6f241c882e6ebaa5a83e3c0f`  
		Last Modified: Fri, 06 Jun 2025 17:26:57 GMT  
		Size: 479.7 KB (479717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0454584e1bc364dc5bcafe9a3178dc09e6ad3aedbaef72269628c1debd7576f0`  
		Last Modified: Fri, 06 Jun 2025 19:13:32 GMT  
		Size: 372.7 MB (372716558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a35afa233e367c450bcbb71e80ebc0af4ac2a7278609eed658426e9bb69f581`  
		Last Modified: Fri, 06 Jun 2025 17:26:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fdabdbcf811458b0dc91d8977cc81fd9aab01dc01f7ba0957eedf865c24483`  
		Last Modified: Fri, 06 Jun 2025 17:26:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fa914e6c66d9d85b5719c92692be90edb38212ad2ebccf980620beea4add5c`  
		Last Modified: Fri, 06 Jun 2025 17:26:57 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fedf6b4c6972de7e41ef381d028c1de8cb0055eb78829446a02a6ed63db661`  
		Last Modified: Fri, 06 Jun 2025 17:26:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:16bc5f0f2cde93c4303dcd0f46da55f0d1bdda4c57b35ebedd0de644285a949f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59418334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5c4ea92d0161ca3be4d7b6eee40b2abe244df7401388e3fd5ee7025ed46540`

```dockerfile
```

-	Layers:
	-	`sha256:319ea88e724cac196ecff9e6bc61e9d16dc2fa6f02039e25217bc97a360c39ca`  
		Last Modified: Fri, 06 Jun 2025 19:12:59 GMT  
		Size: 59.4 MB (59391198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6facbb3600e4f3d4b4da9bae9f0cb11a46df60e7e4025a92946274fba9580e`  
		Last Modified: Fri, 06 Jun 2025 19:13:01 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b7ae820754cd858baca901dbb417547d4144905dcc7c540d0af34c851703c36f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.1 MB (668096864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d77a8ef0c3be0e563d33ef064b298487f59521e797dc81f746ec4b88efc1cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=arm64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=18.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4315199468ce86f2db99234ac7b624c3ff21f9015cb49bcc83244dc5d1e18b`  
		Last Modified: Tue, 03 Jun 2025 13:32:40 GMT  
		Size: 251.9 MB (251941614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e313ca65afe3e86a5825bb239f3b567abf0e6c64a1af4a1e55865dff947432`  
		Last Modified: Tue, 03 Jun 2025 13:31:32 GMT  
		Size: 14.3 MB (14252778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db30f637b9fad6dd03fa06fe2981c8e0d743f0f24c2b216c7f749532a567008`  
		Last Modified: Tue, 03 Jun 2025 13:31:26 GMT  
		Size: 479.7 KB (479713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6775706cc821df9d664e60d09d4e7f3235f19731c3254d6c6b549aacdf25c1a7`  
		Last Modified: Fri, 06 Jun 2025 19:14:42 GMT  
		Size: 372.6 MB (372568420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43fcb891cd90c74e1c52befb217eb6d2aef3ccf8faef195f6867a56d3f33b83`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0a9ba66273c9998333d6120ad2a3452367b9223b04ec01454a7497fc00dac7`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feeb8bccb61a176403b16993a65a6a6b62029f1943d025b6af47f735879d820`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95b155297d4750e744a3a60619d4afb92f454b489a03b79c7e670bfe872d397`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6c849da87f47b9a5a592398bbe3716dfd23f3806e06389a8bf4dcf08b3b99ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59425785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7877e3f519c93112191659e56ed8480a2032ed50401960c4f6e5c5c45325ea4b`

```dockerfile
```

-	Layers:
	-	`sha256:9dc87255e4d736a646974adeb92140f682c1686594104eaa552721ab00fac157`  
		Last Modified: Fri, 06 Jun 2025 19:14:28 GMT  
		Size: 59.4 MB (59398485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db17698e08cc822a974d027e6cac3e4d0601150c9e2260e5daa61dca019d0fe5`  
		Last Modified: Fri, 06 Jun 2025 19:14:29 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:9d185e6dc8c1746a022396c03d0003133d944b9b2ba2f347d533cad98fa6f050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.9 MB (687933601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82e52384b41aa1e5d2a9eeea692542177ea608c018398bed34e19250e5b981b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:29:58 GMT
ARG RELEASE
# Thu, 29 May 2025 04:29:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:02 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Thu, 29 May 2025 04:30:02 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=ppc64le
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=18.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a5b95226fecfdc3ba76d3eedd24473ed37062675a8ada707540009b28ef1c3`  
		Last Modified: Tue, 03 Jun 2025 14:34:31 GMT  
		Size: 265.1 MB (265076915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5e13c1a1d9c93366a170b1e6a11b74a42e1df0387d6a43545841af0af93069`  
		Last Modified: Tue, 03 Jun 2025 14:34:10 GMT  
		Size: 14.8 MB (14798210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3651a97c6ca59b6f4b02957ee8ca413a53501e5cfac770618183dea46fa2fa8d`  
		Last Modified: Tue, 03 Jun 2025 14:34:59 GMT  
		Size: 479.8 KB (479803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9a60ea5994ffc057d5a570094e7ded0c81f17bfbd4fdd6e92673ba3b14582`  
		Last Modified: Fri, 06 Jun 2025 20:31:08 GMT  
		Size: 373.3 MB (373251023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540a5953fd75b9c55b3bd0146b344c4b90557bb17e731149179e1e29fa4c9ef4`  
		Last Modified: Fri, 06 Jun 2025 17:51:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dd7aadec0757effd4351988657970427e3bd440fdccfe7bc5e03ad79d0c915`  
		Last Modified: Fri, 06 Jun 2025 17:51:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee4bdc441c22cf9429948a0b0a94cc8a3a1226a37d3df9b549030d37f318c0b`  
		Last Modified: Fri, 06 Jun 2025 17:51:22 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa7172b1978088755e635b5a093953948fedb14d46a62c3972f121aa54631af`  
		Last Modified: Fri, 06 Jun 2025 17:51:25 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f09e1af0c1cd26327b8e827f775b0d9a6be4ff320155e7b5a0224d24fcbe4971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59426785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b7a8d382d5d16e83a60c28c09bb52eb350f8fffd478edcecdfc8dc79c6a7ee`

```dockerfile
```

-	Layers:
	-	`sha256:47c01571b36f22a7218958047fa308232fd341fff8bd15116493aa39bf09e1ad`  
		Last Modified: Fri, 06 Jun 2025 19:15:37 GMT  
		Size: 59.4 MB (59399587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a58444853ca8db065f1ad4303bad0182d4292f89d5767e4ff5f327ff58f69a`  
		Last Modified: Fri, 06 Jun 2025 19:15:38 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250606`

```console
$ docker pull odoo@sha256:9ed1354116ba4ffe674a459d65180ce22ccd05bb714fbc8474be5692e8192dd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250606` - linux; amd64

```console
$ docker pull odoo@sha256:1b787f53f8615dac47a823100eeee49f7e9df5d3776abbe6bf2f35d7efc86014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.7 MB (671708121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa72d03fe5adc1c3196d05c48f91f2e22f59f63f752a6bba7d964a038f1a25b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=amd64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=18.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d88c54ed93070b52e426687bc4f566ea3629520552cab449ca9aaa9096b5da`  
		Last Modified: Fri, 06 Jun 2025 19:13:24 GMT  
		Size: 254.5 MB (254519024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cfa877a012a36563587636bc84fff944134bc9b13f9988e06373f0f1471b4b`  
		Last Modified: Fri, 06 Jun 2025 17:26:57 GMT  
		Size: 14.3 MB (14275045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220c81613229e6a97ed5a72f7fce510d6426b01e6f241c882e6ebaa5a83e3c0f`  
		Last Modified: Fri, 06 Jun 2025 17:26:57 GMT  
		Size: 479.7 KB (479717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0454584e1bc364dc5bcafe9a3178dc09e6ad3aedbaef72269628c1debd7576f0`  
		Last Modified: Fri, 06 Jun 2025 19:13:32 GMT  
		Size: 372.7 MB (372716558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a35afa233e367c450bcbb71e80ebc0af4ac2a7278609eed658426e9bb69f581`  
		Last Modified: Fri, 06 Jun 2025 17:26:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fdabdbcf811458b0dc91d8977cc81fd9aab01dc01f7ba0957eedf865c24483`  
		Last Modified: Fri, 06 Jun 2025 17:26:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fa914e6c66d9d85b5719c92692be90edb38212ad2ebccf980620beea4add5c`  
		Last Modified: Fri, 06 Jun 2025 17:26:57 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fedf6b4c6972de7e41ef381d028c1de8cb0055eb78829446a02a6ed63db661`  
		Last Modified: Fri, 06 Jun 2025 17:26:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250606` - unknown; unknown

```console
$ docker pull odoo@sha256:16bc5f0f2cde93c4303dcd0f46da55f0d1bdda4c57b35ebedd0de644285a949f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59418334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5c4ea92d0161ca3be4d7b6eee40b2abe244df7401388e3fd5ee7025ed46540`

```dockerfile
```

-	Layers:
	-	`sha256:319ea88e724cac196ecff9e6bc61e9d16dc2fa6f02039e25217bc97a360c39ca`  
		Last Modified: Fri, 06 Jun 2025 19:12:59 GMT  
		Size: 59.4 MB (59391198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6facbb3600e4f3d4b4da9bae9f0cb11a46df60e7e4025a92946274fba9580e`  
		Last Modified: Fri, 06 Jun 2025 19:13:01 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250606` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b7ae820754cd858baca901dbb417547d4144905dcc7c540d0af34c851703c36f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.1 MB (668096864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d77a8ef0c3be0e563d33ef064b298487f59521e797dc81f746ec4b88efc1cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=arm64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=18.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4315199468ce86f2db99234ac7b624c3ff21f9015cb49bcc83244dc5d1e18b`  
		Last Modified: Tue, 03 Jun 2025 13:32:40 GMT  
		Size: 251.9 MB (251941614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e313ca65afe3e86a5825bb239f3b567abf0e6c64a1af4a1e55865dff947432`  
		Last Modified: Tue, 03 Jun 2025 13:31:32 GMT  
		Size: 14.3 MB (14252778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db30f637b9fad6dd03fa06fe2981c8e0d743f0f24c2b216c7f749532a567008`  
		Last Modified: Tue, 03 Jun 2025 13:31:26 GMT  
		Size: 479.7 KB (479713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6775706cc821df9d664e60d09d4e7f3235f19731c3254d6c6b549aacdf25c1a7`  
		Last Modified: Fri, 06 Jun 2025 19:14:42 GMT  
		Size: 372.6 MB (372568420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43fcb891cd90c74e1c52befb217eb6d2aef3ccf8faef195f6867a56d3f33b83`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0a9ba66273c9998333d6120ad2a3452367b9223b04ec01454a7497fc00dac7`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feeb8bccb61a176403b16993a65a6a6b62029f1943d025b6af47f735879d820`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95b155297d4750e744a3a60619d4afb92f454b489a03b79c7e670bfe872d397`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250606` - unknown; unknown

```console
$ docker pull odoo@sha256:6c849da87f47b9a5a592398bbe3716dfd23f3806e06389a8bf4dcf08b3b99ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59425785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7877e3f519c93112191659e56ed8480a2032ed50401960c4f6e5c5c45325ea4b`

```dockerfile
```

-	Layers:
	-	`sha256:9dc87255e4d736a646974adeb92140f682c1686594104eaa552721ab00fac157`  
		Last Modified: Fri, 06 Jun 2025 19:14:28 GMT  
		Size: 59.4 MB (59398485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db17698e08cc822a974d027e6cac3e4d0601150c9e2260e5daa61dca019d0fe5`  
		Last Modified: Fri, 06 Jun 2025 19:14:29 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250606` - linux; ppc64le

```console
$ docker pull odoo@sha256:9d185e6dc8c1746a022396c03d0003133d944b9b2ba2f347d533cad98fa6f050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.9 MB (687933601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82e52384b41aa1e5d2a9eeea692542177ea608c018398bed34e19250e5b981b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:29:58 GMT
ARG RELEASE
# Thu, 29 May 2025 04:29:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:02 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Thu, 29 May 2025 04:30:02 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=ppc64le
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=18.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a5b95226fecfdc3ba76d3eedd24473ed37062675a8ada707540009b28ef1c3`  
		Last Modified: Tue, 03 Jun 2025 14:34:31 GMT  
		Size: 265.1 MB (265076915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5e13c1a1d9c93366a170b1e6a11b74a42e1df0387d6a43545841af0af93069`  
		Last Modified: Tue, 03 Jun 2025 14:34:10 GMT  
		Size: 14.8 MB (14798210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3651a97c6ca59b6f4b02957ee8ca413a53501e5cfac770618183dea46fa2fa8d`  
		Last Modified: Tue, 03 Jun 2025 14:34:59 GMT  
		Size: 479.8 KB (479803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9a60ea5994ffc057d5a570094e7ded0c81f17bfbd4fdd6e92673ba3b14582`  
		Last Modified: Fri, 06 Jun 2025 20:31:08 GMT  
		Size: 373.3 MB (373251023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540a5953fd75b9c55b3bd0146b344c4b90557bb17e731149179e1e29fa4c9ef4`  
		Last Modified: Fri, 06 Jun 2025 17:51:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dd7aadec0757effd4351988657970427e3bd440fdccfe7bc5e03ad79d0c915`  
		Last Modified: Fri, 06 Jun 2025 17:51:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee4bdc441c22cf9429948a0b0a94cc8a3a1226a37d3df9b549030d37f318c0b`  
		Last Modified: Fri, 06 Jun 2025 17:51:22 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa7172b1978088755e635b5a093953948fedb14d46a62c3972f121aa54631af`  
		Last Modified: Fri, 06 Jun 2025 17:51:25 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250606` - unknown; unknown

```console
$ docker pull odoo@sha256:f09e1af0c1cd26327b8e827f775b0d9a6be4ff320155e7b5a0224d24fcbe4971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59426785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b7a8d382d5d16e83a60c28c09bb52eb350f8fffd478edcecdfc8dc79c6a7ee`

```dockerfile
```

-	Layers:
	-	`sha256:47c01571b36f22a7218958047fa308232fd341fff8bd15116493aa39bf09e1ad`  
		Last Modified: Fri, 06 Jun 2025 19:15:37 GMT  
		Size: 59.4 MB (59399587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a58444853ca8db065f1ad4303bad0182d4292f89d5767e4ff5f327ff58f69a`  
		Last Modified: Fri, 06 Jun 2025 19:15:38 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:9ed1354116ba4ffe674a459d65180ce22ccd05bb714fbc8474be5692e8192dd0
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
$ docker pull odoo@sha256:1b787f53f8615dac47a823100eeee49f7e9df5d3776abbe6bf2f35d7efc86014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.7 MB (671708121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa72d03fe5adc1c3196d05c48f91f2e22f59f63f752a6bba7d964a038f1a25b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=amd64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=18.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d88c54ed93070b52e426687bc4f566ea3629520552cab449ca9aaa9096b5da`  
		Last Modified: Fri, 06 Jun 2025 19:13:24 GMT  
		Size: 254.5 MB (254519024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cfa877a012a36563587636bc84fff944134bc9b13f9988e06373f0f1471b4b`  
		Last Modified: Fri, 06 Jun 2025 17:26:57 GMT  
		Size: 14.3 MB (14275045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220c81613229e6a97ed5a72f7fce510d6426b01e6f241c882e6ebaa5a83e3c0f`  
		Last Modified: Fri, 06 Jun 2025 17:26:57 GMT  
		Size: 479.7 KB (479717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0454584e1bc364dc5bcafe9a3178dc09e6ad3aedbaef72269628c1debd7576f0`  
		Last Modified: Fri, 06 Jun 2025 19:13:32 GMT  
		Size: 372.7 MB (372716558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a35afa233e367c450bcbb71e80ebc0af4ac2a7278609eed658426e9bb69f581`  
		Last Modified: Fri, 06 Jun 2025 17:26:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fdabdbcf811458b0dc91d8977cc81fd9aab01dc01f7ba0957eedf865c24483`  
		Last Modified: Fri, 06 Jun 2025 17:26:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fa914e6c66d9d85b5719c92692be90edb38212ad2ebccf980620beea4add5c`  
		Last Modified: Fri, 06 Jun 2025 17:26:57 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fedf6b4c6972de7e41ef381d028c1de8cb0055eb78829446a02a6ed63db661`  
		Last Modified: Fri, 06 Jun 2025 17:26:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:16bc5f0f2cde93c4303dcd0f46da55f0d1bdda4c57b35ebedd0de644285a949f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59418334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5c4ea92d0161ca3be4d7b6eee40b2abe244df7401388e3fd5ee7025ed46540`

```dockerfile
```

-	Layers:
	-	`sha256:319ea88e724cac196ecff9e6bc61e9d16dc2fa6f02039e25217bc97a360c39ca`  
		Last Modified: Fri, 06 Jun 2025 19:12:59 GMT  
		Size: 59.4 MB (59391198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd6facbb3600e4f3d4b4da9bae9f0cb11a46df60e7e4025a92946274fba9580e`  
		Last Modified: Fri, 06 Jun 2025 19:13:01 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b7ae820754cd858baca901dbb417547d4144905dcc7c540d0af34c851703c36f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.1 MB (668096864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d77a8ef0c3be0e563d33ef064b298487f59521e797dc81f746ec4b88efc1cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:30:33 GMT
ARG RELEASE
# Thu, 29 May 2025 04:30:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:30:33 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:36 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Thu, 29 May 2025 04:30:36 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=arm64
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=18.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4315199468ce86f2db99234ac7b624c3ff21f9015cb49bcc83244dc5d1e18b`  
		Last Modified: Tue, 03 Jun 2025 13:32:40 GMT  
		Size: 251.9 MB (251941614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e313ca65afe3e86a5825bb239f3b567abf0e6c64a1af4a1e55865dff947432`  
		Last Modified: Tue, 03 Jun 2025 13:31:32 GMT  
		Size: 14.3 MB (14252778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db30f637b9fad6dd03fa06fe2981c8e0d743f0f24c2b216c7f749532a567008`  
		Last Modified: Tue, 03 Jun 2025 13:31:26 GMT  
		Size: 479.7 KB (479713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6775706cc821df9d664e60d09d4e7f3235f19731c3254d6c6b549aacdf25c1a7`  
		Last Modified: Fri, 06 Jun 2025 19:14:42 GMT  
		Size: 372.6 MB (372568420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43fcb891cd90c74e1c52befb217eb6d2aef3ccf8faef195f6867a56d3f33b83`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0a9ba66273c9998333d6120ad2a3452367b9223b04ec01454a7497fc00dac7`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feeb8bccb61a176403b16993a65a6a6b62029f1943d025b6af47f735879d820`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95b155297d4750e744a3a60619d4afb92f454b489a03b79c7e670bfe872d397`  
		Last Modified: Fri, 06 Jun 2025 17:26:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:6c849da87f47b9a5a592398bbe3716dfd23f3806e06389a8bf4dcf08b3b99ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59425785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7877e3f519c93112191659e56ed8480a2032ed50401960c4f6e5c5c45325ea4b`

```dockerfile
```

-	Layers:
	-	`sha256:9dc87255e4d736a646974adeb92140f682c1686594104eaa552721ab00fac157`  
		Last Modified: Fri, 06 Jun 2025 19:14:28 GMT  
		Size: 59.4 MB (59398485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db17698e08cc822a974d027e6cac3e4d0601150c9e2260e5daa61dca019d0fe5`  
		Last Modified: Fri, 06 Jun 2025 19:14:29 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:9d185e6dc8c1746a022396c03d0003133d944b9b2ba2f347d533cad98fa6f050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.9 MB (687933601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82e52384b41aa1e5d2a9eeea692542177ea608c018398bed34e19250e5b981b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 29 May 2025 04:29:58 GMT
ARG RELEASE
# Thu, 29 May 2025 04:29:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:29:58 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:30:02 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Thu, 29 May 2025 04:30:02 GMT
CMD ["/bin/bash"]
# Fri, 06 Jun 2025 14:44:58 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 06 Jun 2025 14:44:58 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Jun 2025 14:44:58 GMT
ARG TARGETARCH=ppc64le
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_VERSION=18.0
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_RELEASE=20250606
# Fri, 06 Jun 2025 14:44:58 GMT
ARG ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250606 ODOO_SHA=25d2db3f75cc930fbf35d819d9fb812c93a645ce
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 06 Jun 2025 14:44:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 06 Jun 2025 14:44:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 06 Jun 2025 14:44:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 06 Jun 2025 14:44:58 GMT
USER odoo
# Fri, 06 Jun 2025 14:44:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Jun 2025 14:44:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a5b95226fecfdc3ba76d3eedd24473ed37062675a8ada707540009b28ef1c3`  
		Last Modified: Tue, 03 Jun 2025 14:34:31 GMT  
		Size: 265.1 MB (265076915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5e13c1a1d9c93366a170b1e6a11b74a42e1df0387d6a43545841af0af93069`  
		Last Modified: Tue, 03 Jun 2025 14:34:10 GMT  
		Size: 14.8 MB (14798210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3651a97c6ca59b6f4b02957ee8ca413a53501e5cfac770618183dea46fa2fa8d`  
		Last Modified: Tue, 03 Jun 2025 14:34:59 GMT  
		Size: 479.8 KB (479803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9a60ea5994ffc057d5a570094e7ded0c81f17bfbd4fdd6e92673ba3b14582`  
		Last Modified: Fri, 06 Jun 2025 20:31:08 GMT  
		Size: 373.3 MB (373251023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540a5953fd75b9c55b3bd0146b344c4b90557bb17e731149179e1e29fa4c9ef4`  
		Last Modified: Fri, 06 Jun 2025 17:51:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dd7aadec0757effd4351988657970427e3bd440fdccfe7bc5e03ad79d0c915`  
		Last Modified: Fri, 06 Jun 2025 17:51:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee4bdc441c22cf9429948a0b0a94cc8a3a1226a37d3df9b549030d37f318c0b`  
		Last Modified: Fri, 06 Jun 2025 17:51:22 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa7172b1978088755e635b5a093953948fedb14d46a62c3972f121aa54631af`  
		Last Modified: Fri, 06 Jun 2025 17:51:25 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f09e1af0c1cd26327b8e827f775b0d9a6be4ff320155e7b5a0224d24fcbe4971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59426785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b7a8d382d5d16e83a60c28c09bb52eb350f8fffd478edcecdfc8dc79c6a7ee`

```dockerfile
```

-	Layers:
	-	`sha256:47c01571b36f22a7218958047fa308232fd341fff8bd15116493aa39bf09e1ad`  
		Last Modified: Fri, 06 Jun 2025 19:15:37 GMT  
		Size: 59.4 MB (59399587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a58444853ca8db065f1ad4303bad0182d4292f89d5767e4ff5f327ff58f69a`  
		Last Modified: Fri, 06 Jun 2025 19:15:38 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
