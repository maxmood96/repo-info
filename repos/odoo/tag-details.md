<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250520`](#odoo160-20250520)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250520`](#odoo170-20250520)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250520`](#odoo180-20250520)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:04673e7ae74bc28aa65619d6babe4e85b9ec323e705be671f341e7eb4a7697e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:54fbd16ae45706a0166a2cdd39fd1d033b747e072705a7efcbb45cfaeceaff5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.8 MB (584755233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f66e949e56a5c12aa28b9d44686d5c83be6a884f69d3f60ffafe64c748a27a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=amd64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=16.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de43170be5f9e1fb58ea4e80e1f145dc261e51987c0537bb5227a3d7f3359d68`  
		Last Modified: Tue, 03 Jun 2025 13:34:12 GMT  
		Size: 219.6 MB (219626408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f86d65431509314a01a4aeee22962d375bea3eebd5eff2045251507cefd6f7`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 2.6 MB (2627118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfea23f7b4fafcb782b1b0c54d8c54eb35812c165529527d77c2183f1746b207`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 476.8 KB (476848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b3a1fe21488e465b267af080d89abf50ee1cba6bbce636e151392ebf9c0ed6`  
		Last Modified: Tue, 03 Jun 2025 13:34:12 GMT  
		Size: 331.8 MB (331766491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ae4acd472c4a6dcd2f22d39391a01cb908bdd5cb830bc143b4f54922a79e8f`  
		Last Modified: Tue, 03 Jun 2025 13:34:00 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f88c8fd9f45e28d40f34cf7067b3a3cdc11eb5bc6f5adde9b4e089b072174b`  
		Last Modified: Tue, 03 Jun 2025 13:34:02 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0c547c4a0d605a3fdeef8c715e313e0d9e8e38687e43776aebcb80d2ee385b`  
		Last Modified: Tue, 03 Jun 2025 13:34:03 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ad8579c3ceec1f8ea00538626a95009d6ba32c6329a134dc681afec1652617`  
		Last Modified: Tue, 03 Jun 2025 13:34:05 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:e5dfdd06fa7f9427d4f2fe023764d7b516f60b82f6786c79e0cb405045b3a036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38968959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afea06658746162e781f6a97a9cfbea541470f0c8451ae512254ba9f29e69821`

```dockerfile
```

-	Layers:
	-	`sha256:04abaf723a126102cf34da5edf687eecae225e962687afbb2003f7bc630f1059`  
		Last Modified: Wed, 21 May 2025 23:26:29 GMT  
		Size: 38.9 MB (38942241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4a20fa9aa0aca209fa5277c92dcf780e146cc611c4a6e93802a11f1ab34881`  
		Last Modified: Wed, 21 May 2025 23:26:28 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e66171a6ef28619124574a57885f37aae367eab2321ecb77fb7994316d5e1b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.2 MB (580194160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3800da7c720afca3cda2f9f08088fe75cfeb90d6cb95d37686fa321879f27e04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=arm64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=16.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52977ddac9159aa57ed1b97922da245c54addfb41c40368d3485f2ae50490979`  
		Last Modified: Tue, 03 Jun 2025 13:44:49 GMT  
		Size: 216.9 MB (216915095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71d641156272d1b267d3759d2f2d85fb4e8b558651dc445cfdc9ab9f4c739a9`  
		Last Modified: Tue, 03 Jun 2025 13:44:42 GMT  
		Size: 2.6 MB (2635396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac8799b401de8e7b25cf120a334a8abc489a6f4d208cbd4ce67ff5e4bf567c9`  
		Last Modified: Tue, 03 Jun 2025 13:44:38 GMT  
		Size: 476.9 KB (476932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfcc06d468f6ce02c6d87091b84a57b33553e6e5a7301f315b485392f354c89`  
		Last Modified: Tue, 03 Jun 2025 13:44:51 GMT  
		Size: 331.4 MB (331418058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4a8cd4f0cf96ff9e4be6ab5c52f2568c1eeef40c9797400f44bb5b74b41b4d`  
		Last Modified: Tue, 03 Jun 2025 13:44:35 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dccbd14118628ea9c6c815f44879b33d3aca35c2b63b12f879889065779d271`  
		Last Modified: Tue, 03 Jun 2025 13:44:34 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c4ac1852a22e093a19f78a73882e07e7b85691e104a13c2aa7591d69d5bb0b`  
		Last Modified: Tue, 03 Jun 2025 13:44:35 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5603633e43ead8cdfe1166c297333dfe796274ddf207139372d35eef45df62a1`  
		Last Modified: Tue, 03 Jun 2025 13:44:35 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:c9ac07759f24007bf771546f7a869656d69698c445fdbc9c40a18c07040717e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38975577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9b1ec2310b52a71bc439f33447c3462af4b3dbd4289782c4d96623ef8b2837`

```dockerfile
```

-	Layers:
	-	`sha256:001f3fd0fedfc72c41cbc24e46a400b1e9cd6a42c4353311f1791f18bcbcfcf5`  
		Last Modified: Thu, 22 May 2025 03:33:10 GMT  
		Size: 38.9 MB (38948707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:966d09736419909628018d0f890f6a0b532a99753d0208c3cf8e74702c32b441`  
		Last Modified: Thu, 22 May 2025 03:33:09 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:04673e7ae74bc28aa65619d6babe4e85b9ec323e705be671f341e7eb4a7697e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:54fbd16ae45706a0166a2cdd39fd1d033b747e072705a7efcbb45cfaeceaff5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.8 MB (584755233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f66e949e56a5c12aa28b9d44686d5c83be6a884f69d3f60ffafe64c748a27a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=amd64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=16.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de43170be5f9e1fb58ea4e80e1f145dc261e51987c0537bb5227a3d7f3359d68`  
		Last Modified: Tue, 03 Jun 2025 13:34:12 GMT  
		Size: 219.6 MB (219626408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f86d65431509314a01a4aeee22962d375bea3eebd5eff2045251507cefd6f7`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 2.6 MB (2627118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfea23f7b4fafcb782b1b0c54d8c54eb35812c165529527d77c2183f1746b207`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 476.8 KB (476848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b3a1fe21488e465b267af080d89abf50ee1cba6bbce636e151392ebf9c0ed6`  
		Last Modified: Tue, 03 Jun 2025 13:34:12 GMT  
		Size: 331.8 MB (331766491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ae4acd472c4a6dcd2f22d39391a01cb908bdd5cb830bc143b4f54922a79e8f`  
		Last Modified: Tue, 03 Jun 2025 13:34:00 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f88c8fd9f45e28d40f34cf7067b3a3cdc11eb5bc6f5adde9b4e089b072174b`  
		Last Modified: Tue, 03 Jun 2025 13:34:02 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0c547c4a0d605a3fdeef8c715e313e0d9e8e38687e43776aebcb80d2ee385b`  
		Last Modified: Tue, 03 Jun 2025 13:34:03 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ad8579c3ceec1f8ea00538626a95009d6ba32c6329a134dc681afec1652617`  
		Last Modified: Tue, 03 Jun 2025 13:34:05 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e5dfdd06fa7f9427d4f2fe023764d7b516f60b82f6786c79e0cb405045b3a036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38968959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afea06658746162e781f6a97a9cfbea541470f0c8451ae512254ba9f29e69821`

```dockerfile
```

-	Layers:
	-	`sha256:04abaf723a126102cf34da5edf687eecae225e962687afbb2003f7bc630f1059`  
		Last Modified: Wed, 21 May 2025 23:26:29 GMT  
		Size: 38.9 MB (38942241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4a20fa9aa0aca209fa5277c92dcf780e146cc611c4a6e93802a11f1ab34881`  
		Last Modified: Wed, 21 May 2025 23:26:28 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e66171a6ef28619124574a57885f37aae367eab2321ecb77fb7994316d5e1b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.2 MB (580194160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3800da7c720afca3cda2f9f08088fe75cfeb90d6cb95d37686fa321879f27e04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=arm64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=16.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52977ddac9159aa57ed1b97922da245c54addfb41c40368d3485f2ae50490979`  
		Last Modified: Tue, 03 Jun 2025 13:44:49 GMT  
		Size: 216.9 MB (216915095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71d641156272d1b267d3759d2f2d85fb4e8b558651dc445cfdc9ab9f4c739a9`  
		Last Modified: Tue, 03 Jun 2025 13:44:42 GMT  
		Size: 2.6 MB (2635396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac8799b401de8e7b25cf120a334a8abc489a6f4d208cbd4ce67ff5e4bf567c9`  
		Last Modified: Tue, 03 Jun 2025 13:44:38 GMT  
		Size: 476.9 KB (476932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfcc06d468f6ce02c6d87091b84a57b33553e6e5a7301f315b485392f354c89`  
		Last Modified: Tue, 03 Jun 2025 13:44:51 GMT  
		Size: 331.4 MB (331418058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4a8cd4f0cf96ff9e4be6ab5c52f2568c1eeef40c9797400f44bb5b74b41b4d`  
		Last Modified: Tue, 03 Jun 2025 13:44:35 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dccbd14118628ea9c6c815f44879b33d3aca35c2b63b12f879889065779d271`  
		Last Modified: Tue, 03 Jun 2025 13:44:34 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c4ac1852a22e093a19f78a73882e07e7b85691e104a13c2aa7591d69d5bb0b`  
		Last Modified: Tue, 03 Jun 2025 13:44:35 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5603633e43ead8cdfe1166c297333dfe796274ddf207139372d35eef45df62a1`  
		Last Modified: Tue, 03 Jun 2025 13:44:35 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c9ac07759f24007bf771546f7a869656d69698c445fdbc9c40a18c07040717e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38975577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9b1ec2310b52a71bc439f33447c3462af4b3dbd4289782c4d96623ef8b2837`

```dockerfile
```

-	Layers:
	-	`sha256:001f3fd0fedfc72c41cbc24e46a400b1e9cd6a42c4353311f1791f18bcbcfcf5`  
		Last Modified: Thu, 22 May 2025 03:33:10 GMT  
		Size: 38.9 MB (38948707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:966d09736419909628018d0f890f6a0b532a99753d0208c3cf8e74702c32b441`  
		Last Modified: Thu, 22 May 2025 03:33:09 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250520`

```console
$ docker pull odoo@sha256:04673e7ae74bc28aa65619d6babe4e85b9ec323e705be671f341e7eb4a7697e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250520` - linux; amd64

```console
$ docker pull odoo@sha256:54fbd16ae45706a0166a2cdd39fd1d033b747e072705a7efcbb45cfaeceaff5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.8 MB (584755233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f66e949e56a5c12aa28b9d44686d5c83be6a884f69d3f60ffafe64c748a27a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=amd64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=16.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de43170be5f9e1fb58ea4e80e1f145dc261e51987c0537bb5227a3d7f3359d68`  
		Last Modified: Tue, 03 Jun 2025 13:34:12 GMT  
		Size: 219.6 MB (219626408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f86d65431509314a01a4aeee22962d375bea3eebd5eff2045251507cefd6f7`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 2.6 MB (2627118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfea23f7b4fafcb782b1b0c54d8c54eb35812c165529527d77c2183f1746b207`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 476.8 KB (476848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b3a1fe21488e465b267af080d89abf50ee1cba6bbce636e151392ebf9c0ed6`  
		Last Modified: Tue, 03 Jun 2025 13:34:12 GMT  
		Size: 331.8 MB (331766491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ae4acd472c4a6dcd2f22d39391a01cb908bdd5cb830bc143b4f54922a79e8f`  
		Last Modified: Tue, 03 Jun 2025 13:34:00 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f88c8fd9f45e28d40f34cf7067b3a3cdc11eb5bc6f5adde9b4e089b072174b`  
		Last Modified: Tue, 03 Jun 2025 13:34:02 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0c547c4a0d605a3fdeef8c715e313e0d9e8e38687e43776aebcb80d2ee385b`  
		Last Modified: Tue, 03 Jun 2025 13:34:03 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ad8579c3ceec1f8ea00538626a95009d6ba32c6329a134dc681afec1652617`  
		Last Modified: Tue, 03 Jun 2025 13:34:05 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:e5dfdd06fa7f9427d4f2fe023764d7b516f60b82f6786c79e0cb405045b3a036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38968959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afea06658746162e781f6a97a9cfbea541470f0c8451ae512254ba9f29e69821`

```dockerfile
```

-	Layers:
	-	`sha256:04abaf723a126102cf34da5edf687eecae225e962687afbb2003f7bc630f1059`  
		Last Modified: Wed, 21 May 2025 23:26:29 GMT  
		Size: 38.9 MB (38942241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4a20fa9aa0aca209fa5277c92dcf780e146cc611c4a6e93802a11f1ab34881`  
		Last Modified: Wed, 21 May 2025 23:26:28 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250520` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e66171a6ef28619124574a57885f37aae367eab2321ecb77fb7994316d5e1b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.2 MB (580194160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3800da7c720afca3cda2f9f08088fe75cfeb90d6cb95d37686fa321879f27e04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=C.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=arm64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=16.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=7048493a9889f1f9fa244872401f3983360286ad
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52977ddac9159aa57ed1b97922da245c54addfb41c40368d3485f2ae50490979`  
		Last Modified: Tue, 03 Jun 2025 13:44:49 GMT  
		Size: 216.9 MB (216915095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71d641156272d1b267d3759d2f2d85fb4e8b558651dc445cfdc9ab9f4c739a9`  
		Last Modified: Tue, 03 Jun 2025 13:44:42 GMT  
		Size: 2.6 MB (2635396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac8799b401de8e7b25cf120a334a8abc489a6f4d208cbd4ce67ff5e4bf567c9`  
		Last Modified: Tue, 03 Jun 2025 13:44:38 GMT  
		Size: 476.9 KB (476932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfcc06d468f6ce02c6d87091b84a57b33553e6e5a7301f315b485392f354c89`  
		Last Modified: Tue, 03 Jun 2025 13:44:51 GMT  
		Size: 331.4 MB (331418058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4a8cd4f0cf96ff9e4be6ab5c52f2568c1eeef40c9797400f44bb5b74b41b4d`  
		Last Modified: Tue, 03 Jun 2025 13:44:35 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dccbd14118628ea9c6c815f44879b33d3aca35c2b63b12f879889065779d271`  
		Last Modified: Tue, 03 Jun 2025 13:44:34 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c4ac1852a22e093a19f78a73882e07e7b85691e104a13c2aa7591d69d5bb0b`  
		Last Modified: Tue, 03 Jun 2025 13:44:35 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5603633e43ead8cdfe1166c297333dfe796274ddf207139372d35eef45df62a1`  
		Last Modified: Tue, 03 Jun 2025 13:44:35 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:c9ac07759f24007bf771546f7a869656d69698c445fdbc9c40a18c07040717e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38975577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9b1ec2310b52a71bc439f33447c3462af4b3dbd4289782c4d96623ef8b2837`

```dockerfile
```

-	Layers:
	-	`sha256:001f3fd0fedfc72c41cbc24e46a400b1e9cd6a42c4353311f1791f18bcbcfcf5`  
		Last Modified: Thu, 22 May 2025 03:33:10 GMT  
		Size: 38.9 MB (38948707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:966d09736419909628018d0f890f6a0b532a99753d0208c3cf8e74702c32b441`  
		Last Modified: Thu, 22 May 2025 03:33:09 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:6e7231ed0562ebf9e8f304d6d290c8aef94fef24cf18e1f7ba9fb08b65b3a856
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
$ docker pull odoo@sha256:7f16eec318667966e6cf4ac80fbd8f4e44e87715051fc6e26a6c9aac584f31aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.8 MB (600763490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00cf687621f0f79a47502e0e8c772162a6f53ffc26a0dce858f358c35c10d99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=amd64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b360d64f7b0f6db90719586c9d0eeda34e1d99e76c4a1be5b04dcb1bfccd3b`  
		Last Modified: Tue, 03 Jun 2025 13:33:26 GMT  
		Size: 233.8 MB (233779831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addf3d63f49bde2ffbc4c96be748ba26297df9a722052605e4fa7396d3783767`  
		Last Modified: Tue, 03 Jun 2025 13:31:18 GMT  
		Size: 2.5 MB (2523020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614c5df609d203d1d0a292fce5fb956ad76c2da2a6681aef3262bae99d861618`  
		Last Modified: Tue, 03 Jun 2025 13:31:18 GMT  
		Size: 480.0 KB (480009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5d75578b2293de55c053a1fdcaf549326e9ddc1ce34a7839d18c0ebe2d1390`  
		Last Modified: Tue, 03 Jun 2025 13:32:55 GMT  
		Size: 334.4 MB (334445189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8dcdadeab2e06c147cb82f83a7b0611ad6ffbbab7119ca9be2def8e95f53a`  
		Last Modified: Tue, 03 Jun 2025 13:31:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952040656a54abd231fc56dd5e45a6b077c0ecaff0826657552fed44f43a3282`  
		Last Modified: Tue, 03 Jun 2025 13:31:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12563d03ec32a6a9b201ef234d2942cd5d744d876bf1dd92058897c07815f5d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f36d006ddde19cd26b825db77e87037aa0f7fedc5bc3f1d60a77d94b2b06e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:f492826bb9ae8c5ef2f17091142062d98f4aa7a3925b6f94aa3cf0075c9a0712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39886351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28e1c550941aaa82423b726e0f3df991a4b7044fb9f6463ec2eeacfbcbc5f5a`

```dockerfile
```

-	Layers:
	-	`sha256:bff6ca0c9bcc29270d8e3ccc5ddf28179ead05f4c2e6a13e76da31ec0a148d53`  
		Last Modified: Tue, 03 Jun 2025 04:19:58 GMT  
		Size: 39.9 MB (39859516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c543a8e2db326061c02a889da5ab00de907fbe5a2fa28830d31b7ac3d0d7816`  
		Last Modified: Tue, 03 Jun 2025 04:19:56 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:40606e42274af0d5dd8ac16468133bd6057682d73b605a7441aac4b0f6167fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.5 MB (595545545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1278279d168c9fbe8e4d6857bcf5e2aacd9ecddc8cd6d2febf6b5187183f58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=arm64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
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
	-	`sha256:96e8fe068455898645ce1565836abfee8fff95df3b01fadf2f7469312dd837b0`  
		Last Modified: Tue, 03 Jun 2025 13:56:35 GMT  
		Size: 334.0 MB (334046822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238d28b028cbeaf9113575a3ae59c030b7a9626744def67eaa5299623f1e7289`  
		Last Modified: Tue, 03 Jun 2025 13:56:28 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85699271c1b35e07f4b0c2e20955ada508e900400be26aeb01f463684675651`  
		Last Modified: Tue, 03 Jun 2025 13:56:27 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374e6053c768bdb9b664980c6e6ba4d49daa2796db4a52eec151b553f0dc3aca`  
		Last Modified: Tue, 03 Jun 2025 13:56:27 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43a7e976aa0b02901fbefb116972a1a2b836c061e919dfe56e00ebb8f17ec60`  
		Last Modified: Tue, 03 Jun 2025 13:56:27 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:3fd0b1b60230122da9e0e6b7e5fc781e40ed223c434b1b880f4ec19bf0bc4fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39893010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21dc15cb16f76f0b0f87d019a0d1263de500f3de128bf095fd491fe2687f90c5`

```dockerfile
```

-	Layers:
	-	`sha256:42cc64115d291aded4c309da3a8b56724a69222e55bf665deb1871fd1d864c36`  
		Last Modified: Tue, 03 Jun 2025 05:35:16 GMT  
		Size: 39.9 MB (39866023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:109e101297ffbde320a8ddb312e92783f4ea3896f6280c4378eef65538eaec24`  
		Last Modified: Tue, 03 Jun 2025 05:35:14 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:8eb002a6175828023793589f113ffc1ff20bab424c822fea9567f759dcb95ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.2 MB (617185080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26063182ed239442d8d17b4ef889be169686e88c8c8d144aa10fb3ce11353f4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=ppc64le
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7226df727826e2ae3e585430603b9896b6efd1bb9ccd5a8c0f458a4fe9c8707`  
		Last Modified: Tue, 03 Jun 2025 05:23:11 GMT  
		Size: 243.3 MB (243258772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f1e9aa712432a5e39ce559cb39ee4eac90c87dd6398e9cd65777b3ec8e0782`  
		Last Modified: Tue, 03 Jun 2025 05:22:56 GMT  
		Size: 2.8 MB (2841449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62a350920074433bd2feba3924cae7668634f2df0cb7b44b7f87325cd59cc6a`  
		Last Modified: Tue, 03 Jun 2025 05:22:56 GMT  
		Size: 480.0 KB (479983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77343ab0a1b2443e247b9cfeefb2cc7df7e55b9c9c6012b45f2fcea8ca45445f`  
		Last Modified: Tue, 03 Jun 2025 05:23:22 GMT  
		Size: 336.2 MB (336162077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41259a7d44883d1c82e2dde8bdfc50c22f79db8536270caa38bf94c2dff1195b`  
		Last Modified: Tue, 03 Jun 2025 05:22:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c3f380b34a90c2f54f1963714a872d37b7781e9ff80c039d97e79bd984bf6`  
		Last Modified: Tue, 03 Jun 2025 05:22:57 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85afad483828a2c84fa4f4c51b1f1e42b227c488eb553d6333fa94d51ca3a17a`  
		Last Modified: Tue, 03 Jun 2025 05:22:58 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28de784c5ff8ff49be5e975d21f21a00e48fd36e4cdd2c22b27aba711a97aac`  
		Last Modified: Tue, 03 Jun 2025 05:22:59 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:e884402bdda811214f7ffb5e265cee053bc8864ce0196691cf890bdfadcaba35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39895014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c08ff8d48209ee773898e286682455e5385a5c774320a627773b52e86a4164`

```dockerfile
```

-	Layers:
	-	`sha256:f3e6ca8dc377f40aac3d06ee34fc6593a252728f9cf9cd01c2a39d59b69c0a21`  
		Last Modified: Tue, 03 Jun 2025 05:22:58 GMT  
		Size: 39.9 MB (39868123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d92b9802ce43ec9c390d5d186e894e20412f6ac09ff1b3fe75e56d4a8d91e9c1`  
		Last Modified: Tue, 03 Jun 2025 05:22:55 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:6e7231ed0562ebf9e8f304d6d290c8aef94fef24cf18e1f7ba9fb08b65b3a856
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
$ docker pull odoo@sha256:7f16eec318667966e6cf4ac80fbd8f4e44e87715051fc6e26a6c9aac584f31aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.8 MB (600763490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00cf687621f0f79a47502e0e8c772162a6f53ffc26a0dce858f358c35c10d99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=amd64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b360d64f7b0f6db90719586c9d0eeda34e1d99e76c4a1be5b04dcb1bfccd3b`  
		Last Modified: Tue, 03 Jun 2025 13:33:26 GMT  
		Size: 233.8 MB (233779831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addf3d63f49bde2ffbc4c96be748ba26297df9a722052605e4fa7396d3783767`  
		Last Modified: Tue, 03 Jun 2025 13:31:18 GMT  
		Size: 2.5 MB (2523020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614c5df609d203d1d0a292fce5fb956ad76c2da2a6681aef3262bae99d861618`  
		Last Modified: Tue, 03 Jun 2025 13:31:18 GMT  
		Size: 480.0 KB (480009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5d75578b2293de55c053a1fdcaf549326e9ddc1ce34a7839d18c0ebe2d1390`  
		Last Modified: Tue, 03 Jun 2025 13:32:55 GMT  
		Size: 334.4 MB (334445189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8dcdadeab2e06c147cb82f83a7b0611ad6ffbbab7119ca9be2def8e95f53a`  
		Last Modified: Tue, 03 Jun 2025 13:31:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952040656a54abd231fc56dd5e45a6b077c0ecaff0826657552fed44f43a3282`  
		Last Modified: Tue, 03 Jun 2025 13:31:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12563d03ec32a6a9b201ef234d2942cd5d744d876bf1dd92058897c07815f5d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f36d006ddde19cd26b825db77e87037aa0f7fedc5bc3f1d60a77d94b2b06e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f492826bb9ae8c5ef2f17091142062d98f4aa7a3925b6f94aa3cf0075c9a0712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39886351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28e1c550941aaa82423b726e0f3df991a4b7044fb9f6463ec2eeacfbcbc5f5a`

```dockerfile
```

-	Layers:
	-	`sha256:bff6ca0c9bcc29270d8e3ccc5ddf28179ead05f4c2e6a13e76da31ec0a148d53`  
		Last Modified: Tue, 03 Jun 2025 04:19:58 GMT  
		Size: 39.9 MB (39859516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c543a8e2db326061c02a889da5ab00de907fbe5a2fa28830d31b7ac3d0d7816`  
		Last Modified: Tue, 03 Jun 2025 04:19:56 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:40606e42274af0d5dd8ac16468133bd6057682d73b605a7441aac4b0f6167fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.5 MB (595545545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1278279d168c9fbe8e4d6857bcf5e2aacd9ecddc8cd6d2febf6b5187183f58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=arm64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
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
	-	`sha256:96e8fe068455898645ce1565836abfee8fff95df3b01fadf2f7469312dd837b0`  
		Last Modified: Tue, 03 Jun 2025 13:56:35 GMT  
		Size: 334.0 MB (334046822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238d28b028cbeaf9113575a3ae59c030b7a9626744def67eaa5299623f1e7289`  
		Last Modified: Tue, 03 Jun 2025 13:56:28 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85699271c1b35e07f4b0c2e20955ada508e900400be26aeb01f463684675651`  
		Last Modified: Tue, 03 Jun 2025 13:56:27 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374e6053c768bdb9b664980c6e6ba4d49daa2796db4a52eec151b553f0dc3aca`  
		Last Modified: Tue, 03 Jun 2025 13:56:27 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43a7e976aa0b02901fbefb116972a1a2b836c061e919dfe56e00ebb8f17ec60`  
		Last Modified: Tue, 03 Jun 2025 13:56:27 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:3fd0b1b60230122da9e0e6b7e5fc781e40ed223c434b1b880f4ec19bf0bc4fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39893010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21dc15cb16f76f0b0f87d019a0d1263de500f3de128bf095fd491fe2687f90c5`

```dockerfile
```

-	Layers:
	-	`sha256:42cc64115d291aded4c309da3a8b56724a69222e55bf665deb1871fd1d864c36`  
		Last Modified: Tue, 03 Jun 2025 05:35:16 GMT  
		Size: 39.9 MB (39866023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:109e101297ffbde320a8ddb312e92783f4ea3896f6280c4378eef65538eaec24`  
		Last Modified: Tue, 03 Jun 2025 05:35:14 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:8eb002a6175828023793589f113ffc1ff20bab424c822fea9567f759dcb95ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.2 MB (617185080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26063182ed239442d8d17b4ef889be169686e88c8c8d144aa10fb3ce11353f4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=ppc64le
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7226df727826e2ae3e585430603b9896b6efd1bb9ccd5a8c0f458a4fe9c8707`  
		Last Modified: Tue, 03 Jun 2025 05:23:11 GMT  
		Size: 243.3 MB (243258772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f1e9aa712432a5e39ce559cb39ee4eac90c87dd6398e9cd65777b3ec8e0782`  
		Last Modified: Tue, 03 Jun 2025 05:22:56 GMT  
		Size: 2.8 MB (2841449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62a350920074433bd2feba3924cae7668634f2df0cb7b44b7f87325cd59cc6a`  
		Last Modified: Tue, 03 Jun 2025 05:22:56 GMT  
		Size: 480.0 KB (479983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77343ab0a1b2443e247b9cfeefb2cc7df7e55b9c9c6012b45f2fcea8ca45445f`  
		Last Modified: Tue, 03 Jun 2025 05:23:22 GMT  
		Size: 336.2 MB (336162077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41259a7d44883d1c82e2dde8bdfc50c22f79db8536270caa38bf94c2dff1195b`  
		Last Modified: Tue, 03 Jun 2025 05:22:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c3f380b34a90c2f54f1963714a872d37b7781e9ff80c039d97e79bd984bf6`  
		Last Modified: Tue, 03 Jun 2025 05:22:57 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85afad483828a2c84fa4f4c51b1f1e42b227c488eb553d6333fa94d51ca3a17a`  
		Last Modified: Tue, 03 Jun 2025 05:22:58 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28de784c5ff8ff49be5e975d21f21a00e48fd36e4cdd2c22b27aba711a97aac`  
		Last Modified: Tue, 03 Jun 2025 05:22:59 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e884402bdda811214f7ffb5e265cee053bc8864ce0196691cf890bdfadcaba35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39895014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c08ff8d48209ee773898e286682455e5385a5c774320a627773b52e86a4164`

```dockerfile
```

-	Layers:
	-	`sha256:f3e6ca8dc377f40aac3d06ee34fc6593a252728f9cf9cd01c2a39d59b69c0a21`  
		Last Modified: Tue, 03 Jun 2025 05:22:58 GMT  
		Size: 39.9 MB (39868123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d92b9802ce43ec9c390d5d186e894e20412f6ac09ff1b3fe75e56d4a8d91e9c1`  
		Last Modified: Tue, 03 Jun 2025 05:22:55 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250520`

```console
$ docker pull odoo@sha256:6e7231ed0562ebf9e8f304d6d290c8aef94fef24cf18e1f7ba9fb08b65b3a856
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250520` - linux; amd64

```console
$ docker pull odoo@sha256:7f16eec318667966e6cf4ac80fbd8f4e44e87715051fc6e26a6c9aac584f31aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.8 MB (600763490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00cf687621f0f79a47502e0e8c772162a6f53ffc26a0dce858f358c35c10d99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=amd64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b360d64f7b0f6db90719586c9d0eeda34e1d99e76c4a1be5b04dcb1bfccd3b`  
		Last Modified: Tue, 03 Jun 2025 13:33:26 GMT  
		Size: 233.8 MB (233779831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addf3d63f49bde2ffbc4c96be748ba26297df9a722052605e4fa7396d3783767`  
		Last Modified: Tue, 03 Jun 2025 13:31:18 GMT  
		Size: 2.5 MB (2523020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614c5df609d203d1d0a292fce5fb956ad76c2da2a6681aef3262bae99d861618`  
		Last Modified: Tue, 03 Jun 2025 13:31:18 GMT  
		Size: 480.0 KB (480009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5d75578b2293de55c053a1fdcaf549326e9ddc1ce34a7839d18c0ebe2d1390`  
		Last Modified: Tue, 03 Jun 2025 13:32:55 GMT  
		Size: 334.4 MB (334445189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8dcdadeab2e06c147cb82f83a7b0611ad6ffbbab7119ca9be2def8e95f53a`  
		Last Modified: Tue, 03 Jun 2025 13:31:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952040656a54abd231fc56dd5e45a6b077c0ecaff0826657552fed44f43a3282`  
		Last Modified: Tue, 03 Jun 2025 13:31:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12563d03ec32a6a9b201ef234d2942cd5d744d876bf1dd92058897c07815f5d0`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f36d006ddde19cd26b825db77e87037aa0f7fedc5bc3f1d60a77d94b2b06e`  
		Last Modified: Tue, 03 Jun 2025 13:31:21 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:f492826bb9ae8c5ef2f17091142062d98f4aa7a3925b6f94aa3cf0075c9a0712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39886351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28e1c550941aaa82423b726e0f3df991a4b7044fb9f6463ec2eeacfbcbc5f5a`

```dockerfile
```

-	Layers:
	-	`sha256:bff6ca0c9bcc29270d8e3ccc5ddf28179ead05f4c2e6a13e76da31ec0a148d53`  
		Last Modified: Tue, 03 Jun 2025 04:19:58 GMT  
		Size: 39.9 MB (39859516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c543a8e2db326061c02a889da5ab00de907fbe5a2fa28830d31b7ac3d0d7816`  
		Last Modified: Tue, 03 Jun 2025 04:19:56 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250520` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:40606e42274af0d5dd8ac16468133bd6057682d73b605a7441aac4b0f6167fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.5 MB (595545545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1278279d168c9fbe8e4d6857bcf5e2aacd9ecddc8cd6d2febf6b5187183f58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=arm64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
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
	-	`sha256:96e8fe068455898645ce1565836abfee8fff95df3b01fadf2f7469312dd837b0`  
		Last Modified: Tue, 03 Jun 2025 13:56:35 GMT  
		Size: 334.0 MB (334046822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238d28b028cbeaf9113575a3ae59c030b7a9626744def67eaa5299623f1e7289`  
		Last Modified: Tue, 03 Jun 2025 13:56:28 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85699271c1b35e07f4b0c2e20955ada508e900400be26aeb01f463684675651`  
		Last Modified: Tue, 03 Jun 2025 13:56:27 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374e6053c768bdb9b664980c6e6ba4d49daa2796db4a52eec151b553f0dc3aca`  
		Last Modified: Tue, 03 Jun 2025 13:56:27 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43a7e976aa0b02901fbefb116972a1a2b836c061e919dfe56e00ebb8f17ec60`  
		Last Modified: Tue, 03 Jun 2025 13:56:27 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:3fd0b1b60230122da9e0e6b7e5fc781e40ed223c434b1b880f4ec19bf0bc4fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39893010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21dc15cb16f76f0b0f87d019a0d1263de500f3de128bf095fd491fe2687f90c5`

```dockerfile
```

-	Layers:
	-	`sha256:42cc64115d291aded4c309da3a8b56724a69222e55bf665deb1871fd1d864c36`  
		Last Modified: Tue, 03 Jun 2025 05:35:16 GMT  
		Size: 39.9 MB (39866023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:109e101297ffbde320a8ddb312e92783f4ea3896f6280c4378eef65538eaec24`  
		Last Modified: Tue, 03 Jun 2025 05:35:14 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250520` - linux; ppc64le

```console
$ docker pull odoo@sha256:8eb002a6175828023793589f113ffc1ff20bab424c822fea9567f759dcb95ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.2 MB (617185080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26063182ed239442d8d17b4ef889be169686e88c8c8d144aa10fb3ce11353f4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=ppc64le
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=17.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=4b012e56c605fb2a2d8a0f04c4c09110effbd44c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7226df727826e2ae3e585430603b9896b6efd1bb9ccd5a8c0f458a4fe9c8707`  
		Last Modified: Tue, 03 Jun 2025 05:23:11 GMT  
		Size: 243.3 MB (243258772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f1e9aa712432a5e39ce559cb39ee4eac90c87dd6398e9cd65777b3ec8e0782`  
		Last Modified: Tue, 03 Jun 2025 05:22:56 GMT  
		Size: 2.8 MB (2841449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62a350920074433bd2feba3924cae7668634f2df0cb7b44b7f87325cd59cc6a`  
		Last Modified: Tue, 03 Jun 2025 05:22:56 GMT  
		Size: 480.0 KB (479983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77343ab0a1b2443e247b9cfeefb2cc7df7e55b9c9c6012b45f2fcea8ca45445f`  
		Last Modified: Tue, 03 Jun 2025 05:23:22 GMT  
		Size: 336.2 MB (336162077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41259a7d44883d1c82e2dde8bdfc50c22f79db8536270caa38bf94c2dff1195b`  
		Last Modified: Tue, 03 Jun 2025 05:22:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c3f380b34a90c2f54f1963714a872d37b7781e9ff80c039d97e79bd984bf6`  
		Last Modified: Tue, 03 Jun 2025 05:22:57 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85afad483828a2c84fa4f4c51b1f1e42b227c488eb553d6333fa94d51ca3a17a`  
		Last Modified: Tue, 03 Jun 2025 05:22:58 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28de784c5ff8ff49be5e975d21f21a00e48fd36e4cdd2c22b27aba711a97aac`  
		Last Modified: Tue, 03 Jun 2025 05:22:59 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:e884402bdda811214f7ffb5e265cee053bc8864ce0196691cf890bdfadcaba35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39895014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c08ff8d48209ee773898e286682455e5385a5c774320a627773b52e86a4164`

```dockerfile
```

-	Layers:
	-	`sha256:f3e6ca8dc377f40aac3d06ee34fc6593a252728f9cf9cd01c2a39d59b69c0a21`  
		Last Modified: Tue, 03 Jun 2025 05:22:58 GMT  
		Size: 39.9 MB (39868123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d92b9802ce43ec9c390d5d186e894e20412f6ac09ff1b3fe75e56d4a8d91e9c1`  
		Last Modified: Tue, 03 Jun 2025 05:22:55 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:f8e38505b8548229540c3e150a226c9d9909b24e4f65d280a8bfa7b828712de6
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
$ docker pull odoo@sha256:407b49cdbb36f2698df6ffdf1131623d6245cbe8a045691246332f99f3577e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.2 MB (671248225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4c4835c91be67ca3ba0fa18121ca673f4d63092022560c7d8a768486ed29ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=amd64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b4988ea5b80e51be2c68946861e1642ac7fdb7ce382bc52c955a819810d68b`  
		Last Modified: Tue, 03 Jun 2025 13:32:15 GMT  
		Size: 254.5 MB (254519440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf32a6c4261ca18d8283381ea885ba56188e0a30a261f0a5fd003b875567f3d`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 14.3 MB (14275214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e041984684b3c436afbd0ebe34a379a013d359f8cd1b6cefd803aae09fbc64a8`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 479.7 KB (479718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0477a3b0eaa4b255c767bb32d64e2a039a78849be3ced66eb2ec0c0a917abb34`  
		Last Modified: Tue, 03 Jun 2025 13:32:26 GMT  
		Size: 372.3 MB (372256076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869cc27ca781a40d0c97c4d703757105cd4552bf43f66f6df1e21cc5beaa1c11`  
		Last Modified: Tue, 03 Jun 2025 13:30:52 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d4aa4b31d32c7ad934bbbdfa98511e1f2906ffef1ba97721f6531bb8b698cc`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b654cc91f30aec4d5f1fdb122d13955879c7b0ab50bbde31422de10e0c0f23`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97e7f79729471f37c027670254bc8531fd4e26eeef20a2a5b3a21b3e9524910`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:db265fe125d7dffba9acb32b99288721bed2b03e1a95170fe0661c5612fe42de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59380807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b680242c9c254afba87e565c7b396a7e4fd02fc7f51d0e6079aaa7632e0bfe46`

```dockerfile
```

-	Layers:
	-	`sha256:179485d21ac5c7e2542da2346a21ddec3e18bb816e34594f86cbc600f87d57bb`  
		Last Modified: Tue, 03 Jun 2025 14:33:14 GMT  
		Size: 59.4 MB (59353671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4df4dd0f2833194a74bcf2e5a63681fb66e8e9525a27c19b5ecec3f70634ad9`  
		Last Modified: Tue, 03 Jun 2025 14:32:39 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:022362860372d39c0e52b7c6cb61d2927032fb24c68facfc65685110e350d75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.6 MB (667636966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edac7a4673e7317c2c0cd481a5dac188549a27676c40fae921acbf615804761`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=arm64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
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
	-	`sha256:9d5f6fdd19259bf5d387cb00daca3460a9fb4b8c6a5840027cb0b2d384432b68`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 372.1 MB (372108522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e505fe4c1781ba41009d480fb89876a4e4cc1c92002e9630e10e8a4f57caff7`  
		Last Modified: Tue, 03 Jun 2025 13:31:25 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232f87f9a4d4aea52f75dcb9e1a51466522c6ace60b2e600f9c6a19b6787fce`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9975ca8ffc6b7c540270bb145bc2058a923f10fb0361263bd6a0c9785b4b3d8c`  
		Last Modified: Tue, 03 Jun 2025 13:31:28 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dba5c0279ae3314db8bce605007fbb4c0c4843158bf40f2c565065efe38f7c5`  
		Last Modified: Tue, 03 Jun 2025 13:31:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:d30d9dccc49d537cd8fd5162ac8abb7dd5bbbbbb184c4ce167313a70b263770d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59388258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421c88169750aec73b22e589a3f1e46583bb1e016ce433c8f6a2a8f770382aad`

```dockerfile
```

-	Layers:
	-	`sha256:7e2ba9858eac2530b325489396cca01d3b4b20b622c32a404a5ec3156b798310`  
		Last Modified: Tue, 03 Jun 2025 14:35:21 GMT  
		Size: 59.4 MB (59360958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e05525a728ee954eb17baf77de89ee8a289578eb30e4b67be44d4745de2812f`  
		Last Modified: Tue, 03 Jun 2025 14:35:11 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:c60342338f79f5fb98c1a4610861478eac92f91a4b4705b3780d461bea68edef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.5 MB (687468206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9ee2e0281d0d51167fa2a7b0f82c527dba4e2212f53a2f1e544d651c728614`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=ppc64le
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
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
	-	`sha256:7864b4f2428fe16b03ccbc20db4ee6be5a378b2527595209ee2db5c2bfd4feac`  
		Last Modified: Tue, 03 Jun 2025 14:31:15 GMT  
		Size: 372.8 MB (372785630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266efe06b08b6e799f39b94e718f5bee16cf74d7410279a65552958cc76fc9e7`  
		Last Modified: Tue, 03 Jun 2025 14:35:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fd8b10cad4b4fc2300a39bbdbd5fe09a1b849877723de7e1d1b3a38ddb00e0`  
		Last Modified: Tue, 03 Jun 2025 14:35:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf27c3eb4a5cc49630b0f90674a87d833bac6dcbbac45a3773e2c6c492672e3`  
		Last Modified: Tue, 03 Jun 2025 14:35:06 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c05b2026af69690c22de3ed1af9a63dba36180a39f46ed8f56a5fff9094237`  
		Last Modified: Tue, 03 Jun 2025 14:34:57 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:635e2017d6d208efcfb3af3413da93579f9ea04ba2e663cdb2ee5199a0a97348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59389258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c523b585b957c38780e50e60493b520b4fbe5533b0c2b8a1ba87f6f2a0e989f1`

```dockerfile
```

-	Layers:
	-	`sha256:524b704b57a7ff4d09f654e5bf5998bbedbccbb6485c163781434a7990f56d65`  
		Last Modified: Tue, 03 Jun 2025 14:30:14 GMT  
		Size: 59.4 MB (59362060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:807dfec48598a52becce3ed33d934ec9083832a295e41bb187ce2e4bedd60e0d`  
		Last Modified: Tue, 03 Jun 2025 14:31:47 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:f8e38505b8548229540c3e150a226c9d9909b24e4f65d280a8bfa7b828712de6
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
$ docker pull odoo@sha256:407b49cdbb36f2698df6ffdf1131623d6245cbe8a045691246332f99f3577e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.2 MB (671248225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4c4835c91be67ca3ba0fa18121ca673f4d63092022560c7d8a768486ed29ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=amd64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b4988ea5b80e51be2c68946861e1642ac7fdb7ce382bc52c955a819810d68b`  
		Last Modified: Tue, 03 Jun 2025 13:32:15 GMT  
		Size: 254.5 MB (254519440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf32a6c4261ca18d8283381ea885ba56188e0a30a261f0a5fd003b875567f3d`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 14.3 MB (14275214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e041984684b3c436afbd0ebe34a379a013d359f8cd1b6cefd803aae09fbc64a8`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 479.7 KB (479718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0477a3b0eaa4b255c767bb32d64e2a039a78849be3ced66eb2ec0c0a917abb34`  
		Last Modified: Tue, 03 Jun 2025 13:32:26 GMT  
		Size: 372.3 MB (372256076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869cc27ca781a40d0c97c4d703757105cd4552bf43f66f6df1e21cc5beaa1c11`  
		Last Modified: Tue, 03 Jun 2025 13:30:52 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d4aa4b31d32c7ad934bbbdfa98511e1f2906ffef1ba97721f6531bb8b698cc`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b654cc91f30aec4d5f1fdb122d13955879c7b0ab50bbde31422de10e0c0f23`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97e7f79729471f37c027670254bc8531fd4e26eeef20a2a5b3a21b3e9524910`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:db265fe125d7dffba9acb32b99288721bed2b03e1a95170fe0661c5612fe42de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59380807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b680242c9c254afba87e565c7b396a7e4fd02fc7f51d0e6079aaa7632e0bfe46`

```dockerfile
```

-	Layers:
	-	`sha256:179485d21ac5c7e2542da2346a21ddec3e18bb816e34594f86cbc600f87d57bb`  
		Last Modified: Tue, 03 Jun 2025 14:33:14 GMT  
		Size: 59.4 MB (59353671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4df4dd0f2833194a74bcf2e5a63681fb66e8e9525a27c19b5ecec3f70634ad9`  
		Last Modified: Tue, 03 Jun 2025 14:32:39 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:022362860372d39c0e52b7c6cb61d2927032fb24c68facfc65685110e350d75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.6 MB (667636966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edac7a4673e7317c2c0cd481a5dac188549a27676c40fae921acbf615804761`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=arm64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
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
	-	`sha256:9d5f6fdd19259bf5d387cb00daca3460a9fb4b8c6a5840027cb0b2d384432b68`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 372.1 MB (372108522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e505fe4c1781ba41009d480fb89876a4e4cc1c92002e9630e10e8a4f57caff7`  
		Last Modified: Tue, 03 Jun 2025 13:31:25 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232f87f9a4d4aea52f75dcb9e1a51466522c6ace60b2e600f9c6a19b6787fce`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9975ca8ffc6b7c540270bb145bc2058a923f10fb0361263bd6a0c9785b4b3d8c`  
		Last Modified: Tue, 03 Jun 2025 13:31:28 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dba5c0279ae3314db8bce605007fbb4c0c4843158bf40f2c565065efe38f7c5`  
		Last Modified: Tue, 03 Jun 2025 13:31:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d30d9dccc49d537cd8fd5162ac8abb7dd5bbbbbb184c4ce167313a70b263770d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59388258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421c88169750aec73b22e589a3f1e46583bb1e016ce433c8f6a2a8f770382aad`

```dockerfile
```

-	Layers:
	-	`sha256:7e2ba9858eac2530b325489396cca01d3b4b20b622c32a404a5ec3156b798310`  
		Last Modified: Tue, 03 Jun 2025 14:35:21 GMT  
		Size: 59.4 MB (59360958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e05525a728ee954eb17baf77de89ee8a289578eb30e4b67be44d4745de2812f`  
		Last Modified: Tue, 03 Jun 2025 14:35:11 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:c60342338f79f5fb98c1a4610861478eac92f91a4b4705b3780d461bea68edef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.5 MB (687468206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9ee2e0281d0d51167fa2a7b0f82c527dba4e2212f53a2f1e544d651c728614`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=ppc64le
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
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
	-	`sha256:7864b4f2428fe16b03ccbc20db4ee6be5a378b2527595209ee2db5c2bfd4feac`  
		Last Modified: Tue, 03 Jun 2025 14:31:15 GMT  
		Size: 372.8 MB (372785630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266efe06b08b6e799f39b94e718f5bee16cf74d7410279a65552958cc76fc9e7`  
		Last Modified: Tue, 03 Jun 2025 14:35:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fd8b10cad4b4fc2300a39bbdbd5fe09a1b849877723de7e1d1b3a38ddb00e0`  
		Last Modified: Tue, 03 Jun 2025 14:35:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf27c3eb4a5cc49630b0f90674a87d833bac6dcbbac45a3773e2c6c492672e3`  
		Last Modified: Tue, 03 Jun 2025 14:35:06 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c05b2026af69690c22de3ed1af9a63dba36180a39f46ed8f56a5fff9094237`  
		Last Modified: Tue, 03 Jun 2025 14:34:57 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:635e2017d6d208efcfb3af3413da93579f9ea04ba2e663cdb2ee5199a0a97348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59389258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c523b585b957c38780e50e60493b520b4fbe5533b0c2b8a1ba87f6f2a0e989f1`

```dockerfile
```

-	Layers:
	-	`sha256:524b704b57a7ff4d09f654e5bf5998bbedbccbb6485c163781434a7990f56d65`  
		Last Modified: Tue, 03 Jun 2025 14:30:14 GMT  
		Size: 59.4 MB (59362060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:807dfec48598a52becce3ed33d934ec9083832a295e41bb187ce2e4bedd60e0d`  
		Last Modified: Tue, 03 Jun 2025 14:31:47 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250520`

```console
$ docker pull odoo@sha256:f8e38505b8548229540c3e150a226c9d9909b24e4f65d280a8bfa7b828712de6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250520` - linux; amd64

```console
$ docker pull odoo@sha256:407b49cdbb36f2698df6ffdf1131623d6245cbe8a045691246332f99f3577e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.2 MB (671248225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4c4835c91be67ca3ba0fa18121ca673f4d63092022560c7d8a768486ed29ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=amd64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b4988ea5b80e51be2c68946861e1642ac7fdb7ce382bc52c955a819810d68b`  
		Last Modified: Tue, 03 Jun 2025 13:32:15 GMT  
		Size: 254.5 MB (254519440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf32a6c4261ca18d8283381ea885ba56188e0a30a261f0a5fd003b875567f3d`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 14.3 MB (14275214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e041984684b3c436afbd0ebe34a379a013d359f8cd1b6cefd803aae09fbc64a8`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 479.7 KB (479718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0477a3b0eaa4b255c767bb32d64e2a039a78849be3ced66eb2ec0c0a917abb34`  
		Last Modified: Tue, 03 Jun 2025 13:32:26 GMT  
		Size: 372.3 MB (372256076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869cc27ca781a40d0c97c4d703757105cd4552bf43f66f6df1e21cc5beaa1c11`  
		Last Modified: Tue, 03 Jun 2025 13:30:52 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d4aa4b31d32c7ad934bbbdfa98511e1f2906ffef1ba97721f6531bb8b698cc`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b654cc91f30aec4d5f1fdb122d13955879c7b0ab50bbde31422de10e0c0f23`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97e7f79729471f37c027670254bc8531fd4e26eeef20a2a5b3a21b3e9524910`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:db265fe125d7dffba9acb32b99288721bed2b03e1a95170fe0661c5612fe42de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59380807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b680242c9c254afba87e565c7b396a7e4fd02fc7f51d0e6079aaa7632e0bfe46`

```dockerfile
```

-	Layers:
	-	`sha256:179485d21ac5c7e2542da2346a21ddec3e18bb816e34594f86cbc600f87d57bb`  
		Last Modified: Tue, 03 Jun 2025 14:33:14 GMT  
		Size: 59.4 MB (59353671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4df4dd0f2833194a74bcf2e5a63681fb66e8e9525a27c19b5ecec3f70634ad9`  
		Last Modified: Tue, 03 Jun 2025 14:32:39 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250520` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:022362860372d39c0e52b7c6cb61d2927032fb24c68facfc65685110e350d75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.6 MB (667636966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edac7a4673e7317c2c0cd481a5dac188549a27676c40fae921acbf615804761`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=arm64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
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
	-	`sha256:9d5f6fdd19259bf5d387cb00daca3460a9fb4b8c6a5840027cb0b2d384432b68`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 372.1 MB (372108522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e505fe4c1781ba41009d480fb89876a4e4cc1c92002e9630e10e8a4f57caff7`  
		Last Modified: Tue, 03 Jun 2025 13:31:25 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232f87f9a4d4aea52f75dcb9e1a51466522c6ace60b2e600f9c6a19b6787fce`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9975ca8ffc6b7c540270bb145bc2058a923f10fb0361263bd6a0c9785b4b3d8c`  
		Last Modified: Tue, 03 Jun 2025 13:31:28 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dba5c0279ae3314db8bce605007fbb4c0c4843158bf40f2c565065efe38f7c5`  
		Last Modified: Tue, 03 Jun 2025 13:31:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:d30d9dccc49d537cd8fd5162ac8abb7dd5bbbbbb184c4ce167313a70b263770d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59388258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421c88169750aec73b22e589a3f1e46583bb1e016ce433c8f6a2a8f770382aad`

```dockerfile
```

-	Layers:
	-	`sha256:7e2ba9858eac2530b325489396cca01d3b4b20b622c32a404a5ec3156b798310`  
		Last Modified: Tue, 03 Jun 2025 14:35:21 GMT  
		Size: 59.4 MB (59360958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e05525a728ee954eb17baf77de89ee8a289578eb30e4b67be44d4745de2812f`  
		Last Modified: Tue, 03 Jun 2025 14:35:11 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250520` - linux; ppc64le

```console
$ docker pull odoo@sha256:c60342338f79f5fb98c1a4610861478eac92f91a4b4705b3780d461bea68edef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.5 MB (687468206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9ee2e0281d0d51167fa2a7b0f82c527dba4e2212f53a2f1e544d651c728614`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=ppc64le
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
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
	-	`sha256:7864b4f2428fe16b03ccbc20db4ee6be5a378b2527595209ee2db5c2bfd4feac`  
		Last Modified: Tue, 03 Jun 2025 14:31:15 GMT  
		Size: 372.8 MB (372785630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266efe06b08b6e799f39b94e718f5bee16cf74d7410279a65552958cc76fc9e7`  
		Last Modified: Tue, 03 Jun 2025 14:35:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fd8b10cad4b4fc2300a39bbdbd5fe09a1b849877723de7e1d1b3a38ddb00e0`  
		Last Modified: Tue, 03 Jun 2025 14:35:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf27c3eb4a5cc49630b0f90674a87d833bac6dcbbac45a3773e2c6c492672e3`  
		Last Modified: Tue, 03 Jun 2025 14:35:06 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c05b2026af69690c22de3ed1af9a63dba36180a39f46ed8f56a5fff9094237`  
		Last Modified: Tue, 03 Jun 2025 14:34:57 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:635e2017d6d208efcfb3af3413da93579f9ea04ba2e663cdb2ee5199a0a97348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59389258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c523b585b957c38780e50e60493b520b4fbe5533b0c2b8a1ba87f6f2a0e989f1`

```dockerfile
```

-	Layers:
	-	`sha256:524b704b57a7ff4d09f654e5bf5998bbedbccbb6485c163781434a7990f56d65`  
		Last Modified: Tue, 03 Jun 2025 14:30:14 GMT  
		Size: 59.4 MB (59362060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:807dfec48598a52becce3ed33d934ec9083832a295e41bb187ce2e4bedd60e0d`  
		Last Modified: Tue, 03 Jun 2025 14:31:47 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:f8e38505b8548229540c3e150a226c9d9909b24e4f65d280a8bfa7b828712de6
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
$ docker pull odoo@sha256:407b49cdbb36f2698df6ffdf1131623d6245cbe8a045691246332f99f3577e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.2 MB (671248225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4c4835c91be67ca3ba0fa18121ca673f4d63092022560c7d8a768486ed29ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=amd64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b4988ea5b80e51be2c68946861e1642ac7fdb7ce382bc52c955a819810d68b`  
		Last Modified: Tue, 03 Jun 2025 13:32:15 GMT  
		Size: 254.5 MB (254519440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf32a6c4261ca18d8283381ea885ba56188e0a30a261f0a5fd003b875567f3d`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 14.3 MB (14275214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e041984684b3c436afbd0ebe34a379a013d359f8cd1b6cefd803aae09fbc64a8`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 479.7 KB (479718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0477a3b0eaa4b255c767bb32d64e2a039a78849be3ced66eb2ec0c0a917abb34`  
		Last Modified: Tue, 03 Jun 2025 13:32:26 GMT  
		Size: 372.3 MB (372256076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869cc27ca781a40d0c97c4d703757105cd4552bf43f66f6df1e21cc5beaa1c11`  
		Last Modified: Tue, 03 Jun 2025 13:30:52 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d4aa4b31d32c7ad934bbbdfa98511e1f2906ffef1ba97721f6531bb8b698cc`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b654cc91f30aec4d5f1fdb122d13955879c7b0ab50bbde31422de10e0c0f23`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97e7f79729471f37c027670254bc8531fd4e26eeef20a2a5b3a21b3e9524910`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:db265fe125d7dffba9acb32b99288721bed2b03e1a95170fe0661c5612fe42de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59380807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b680242c9c254afba87e565c7b396a7e4fd02fc7f51d0e6079aaa7632e0bfe46`

```dockerfile
```

-	Layers:
	-	`sha256:179485d21ac5c7e2542da2346a21ddec3e18bb816e34594f86cbc600f87d57bb`  
		Last Modified: Tue, 03 Jun 2025 14:33:14 GMT  
		Size: 59.4 MB (59353671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4df4dd0f2833194a74bcf2e5a63681fb66e8e9525a27c19b5ecec3f70634ad9`  
		Last Modified: Tue, 03 Jun 2025 14:32:39 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:022362860372d39c0e52b7c6cb61d2927032fb24c68facfc65685110e350d75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.6 MB (667636966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edac7a4673e7317c2c0cd481a5dac188549a27676c40fae921acbf615804761`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=arm64
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
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
	-	`sha256:9d5f6fdd19259bf5d387cb00daca3460a9fb4b8c6a5840027cb0b2d384432b68`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 372.1 MB (372108522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e505fe4c1781ba41009d480fb89876a4e4cc1c92002e9630e10e8a4f57caff7`  
		Last Modified: Tue, 03 Jun 2025 13:31:25 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232f87f9a4d4aea52f75dcb9e1a51466522c6ace60b2e600f9c6a19b6787fce`  
		Last Modified: Tue, 03 Jun 2025 13:31:27 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9975ca8ffc6b7c540270bb145bc2058a923f10fb0361263bd6a0c9785b4b3d8c`  
		Last Modified: Tue, 03 Jun 2025 13:31:28 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dba5c0279ae3314db8bce605007fbb4c0c4843158bf40f2c565065efe38f7c5`  
		Last Modified: Tue, 03 Jun 2025 13:31:28 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d30d9dccc49d537cd8fd5162ac8abb7dd5bbbbbb184c4ce167313a70b263770d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59388258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421c88169750aec73b22e589a3f1e46583bb1e016ce433c8f6a2a8f770382aad`

```dockerfile
```

-	Layers:
	-	`sha256:7e2ba9858eac2530b325489396cca01d3b4b20b622c32a404a5ec3156b798310`  
		Last Modified: Tue, 03 Jun 2025 14:35:21 GMT  
		Size: 59.4 MB (59360958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e05525a728ee954eb17baf77de89ee8a289578eb30e4b67be44d4745de2812f`  
		Last Modified: Tue, 03 Jun 2025 14:35:11 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:c60342338f79f5fb98c1a4610861478eac92f91a4b4705b3780d461bea68edef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.5 MB (687468206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9ee2e0281d0d51167fa2a7b0f82c527dba4e2212f53a2f1e544d651c728614`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 20 May 2025 06:38:43 GMT
ARG RELEASE
# Tue, 20 May 2025 06:38:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 20 May 2025 06:38:43 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 20 May 2025 06:38:43 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Tue, 20 May 2025 06:38:43 GMT
CMD ["/bin/bash"]
# Tue, 20 May 2025 06:38:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 20 May 2025 06:38:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 20 May 2025 06:38:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 20 May 2025 06:38:43 GMT
ARG TARGETARCH=ppc64le
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_VERSION=18.0
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_RELEASE=20250520
# Tue, 20 May 2025 06:38:43 GMT
ARG ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 20 May 2025 06:38:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 20 May 2025 06:38:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250520 ODOO_SHA=ce904bed4ffc98863a1ed26e4b6fe27a300262e2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 20 May 2025 06:38:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 20 May 2025 06:38:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 20 May 2025 06:38:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 20 May 2025 06:38:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 20 May 2025 06:38:43 GMT
USER odoo
# Tue, 20 May 2025 06:38:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 20 May 2025 06:38:43 GMT
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
	-	`sha256:7864b4f2428fe16b03ccbc20db4ee6be5a378b2527595209ee2db5c2bfd4feac`  
		Last Modified: Tue, 03 Jun 2025 14:31:15 GMT  
		Size: 372.8 MB (372785630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266efe06b08b6e799f39b94e718f5bee16cf74d7410279a65552958cc76fc9e7`  
		Last Modified: Tue, 03 Jun 2025 14:35:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fd8b10cad4b4fc2300a39bbdbd5fe09a1b849877723de7e1d1b3a38ddb00e0`  
		Last Modified: Tue, 03 Jun 2025 14:35:04 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf27c3eb4a5cc49630b0f90674a87d833bac6dcbbac45a3773e2c6c492672e3`  
		Last Modified: Tue, 03 Jun 2025 14:35:06 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c05b2026af69690c22de3ed1af9a63dba36180a39f46ed8f56a5fff9094237`  
		Last Modified: Tue, 03 Jun 2025 14:34:57 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:635e2017d6d208efcfb3af3413da93579f9ea04ba2e663cdb2ee5199a0a97348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59389258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c523b585b957c38780e50e60493b520b4fbe5533b0c2b8a1ba87f6f2a0e989f1`

```dockerfile
```

-	Layers:
	-	`sha256:524b704b57a7ff4d09f654e5bf5998bbedbccbb6485c163781434a7990f56d65`  
		Last Modified: Tue, 03 Jun 2025 14:30:14 GMT  
		Size: 59.4 MB (59362060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:807dfec48598a52becce3ed33d934ec9083832a295e41bb187ce2e4bedd60e0d`  
		Last Modified: Tue, 03 Jun 2025 14:31:47 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
