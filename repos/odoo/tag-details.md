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
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de43170be5f9e1fb58ea4e80e1f145dc261e51987c0537bb5227a3d7f3359d68`  
		Last Modified: Wed, 21 May 2025 23:26:31 GMT  
		Size: 219.6 MB (219626408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f86d65431509314a01a4aeee22962d375bea3eebd5eff2045251507cefd6f7`  
		Last Modified: Wed, 21 May 2025 23:26:29 GMT  
		Size: 2.6 MB (2627118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfea23f7b4fafcb782b1b0c54d8c54eb35812c165529527d77c2183f1746b207`  
		Last Modified: Wed, 21 May 2025 23:26:28 GMT  
		Size: 476.8 KB (476848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b3a1fe21488e465b267af080d89abf50ee1cba6bbce636e151392ebf9c0ed6`  
		Last Modified: Wed, 21 May 2025 23:26:33 GMT  
		Size: 331.8 MB (331766491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ae4acd472c4a6dcd2f22d39391a01cb908bdd5cb830bc143b4f54922a79e8f`  
		Last Modified: Wed, 21 May 2025 23:26:29 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f88c8fd9f45e28d40f34cf7067b3a3cdc11eb5bc6f5adde9b4e089b072174b`  
		Last Modified: Wed, 21 May 2025 23:26:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0c547c4a0d605a3fdeef8c715e313e0d9e8e38687e43776aebcb80d2ee385b`  
		Last Modified: Wed, 21 May 2025 23:26:30 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ad8579c3ceec1f8ea00538626a95009d6ba32c6329a134dc681afec1652617`  
		Last Modified: Wed, 21 May 2025 23:26:30 GMT  
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
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52977ddac9159aa57ed1b97922da245c54addfb41c40368d3485f2ae50490979`  
		Last Modified: Thu, 22 May 2025 03:33:15 GMT  
		Size: 216.9 MB (216915095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71d641156272d1b267d3759d2f2d85fb4e8b558651dc445cfdc9ab9f4c739a9`  
		Last Modified: Thu, 22 May 2025 03:33:09 GMT  
		Size: 2.6 MB (2635396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac8799b401de8e7b25cf120a334a8abc489a6f4d208cbd4ce67ff5e4bf567c9`  
		Last Modified: Thu, 22 May 2025 03:33:09 GMT  
		Size: 476.9 KB (476932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfcc06d468f6ce02c6d87091b84a57b33553e6e5a7301f315b485392f354c89`  
		Last Modified: Thu, 22 May 2025 03:33:20 GMT  
		Size: 331.4 MB (331418058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4a8cd4f0cf96ff9e4be6ab5c52f2568c1eeef40c9797400f44bb5b74b41b4d`  
		Last Modified: Thu, 22 May 2025 03:33:10 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dccbd14118628ea9c6c815f44879b33d3aca35c2b63b12f879889065779d271`  
		Last Modified: Thu, 22 May 2025 03:33:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c4ac1852a22e093a19f78a73882e07e7b85691e104a13c2aa7591d69d5bb0b`  
		Last Modified: Thu, 22 May 2025 03:33:11 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5603633e43ead8cdfe1166c297333dfe796274ddf207139372d35eef45df62a1`  
		Last Modified: Thu, 22 May 2025 03:33:11 GMT  
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
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de43170be5f9e1fb58ea4e80e1f145dc261e51987c0537bb5227a3d7f3359d68`  
		Last Modified: Wed, 21 May 2025 23:26:31 GMT  
		Size: 219.6 MB (219626408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f86d65431509314a01a4aeee22962d375bea3eebd5eff2045251507cefd6f7`  
		Last Modified: Wed, 21 May 2025 23:26:29 GMT  
		Size: 2.6 MB (2627118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfea23f7b4fafcb782b1b0c54d8c54eb35812c165529527d77c2183f1746b207`  
		Last Modified: Wed, 21 May 2025 23:26:28 GMT  
		Size: 476.8 KB (476848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b3a1fe21488e465b267af080d89abf50ee1cba6bbce636e151392ebf9c0ed6`  
		Last Modified: Wed, 21 May 2025 23:26:33 GMT  
		Size: 331.8 MB (331766491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ae4acd472c4a6dcd2f22d39391a01cb908bdd5cb830bc143b4f54922a79e8f`  
		Last Modified: Wed, 21 May 2025 23:26:29 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f88c8fd9f45e28d40f34cf7067b3a3cdc11eb5bc6f5adde9b4e089b072174b`  
		Last Modified: Wed, 21 May 2025 23:26:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0c547c4a0d605a3fdeef8c715e313e0d9e8e38687e43776aebcb80d2ee385b`  
		Last Modified: Wed, 21 May 2025 23:26:30 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ad8579c3ceec1f8ea00538626a95009d6ba32c6329a134dc681afec1652617`  
		Last Modified: Wed, 21 May 2025 23:26:30 GMT  
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
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52977ddac9159aa57ed1b97922da245c54addfb41c40368d3485f2ae50490979`  
		Last Modified: Thu, 22 May 2025 03:33:15 GMT  
		Size: 216.9 MB (216915095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71d641156272d1b267d3759d2f2d85fb4e8b558651dc445cfdc9ab9f4c739a9`  
		Last Modified: Thu, 22 May 2025 03:33:09 GMT  
		Size: 2.6 MB (2635396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac8799b401de8e7b25cf120a334a8abc489a6f4d208cbd4ce67ff5e4bf567c9`  
		Last Modified: Thu, 22 May 2025 03:33:09 GMT  
		Size: 476.9 KB (476932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfcc06d468f6ce02c6d87091b84a57b33553e6e5a7301f315b485392f354c89`  
		Last Modified: Thu, 22 May 2025 03:33:20 GMT  
		Size: 331.4 MB (331418058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4a8cd4f0cf96ff9e4be6ab5c52f2568c1eeef40c9797400f44bb5b74b41b4d`  
		Last Modified: Thu, 22 May 2025 03:33:10 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dccbd14118628ea9c6c815f44879b33d3aca35c2b63b12f879889065779d271`  
		Last Modified: Thu, 22 May 2025 03:33:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c4ac1852a22e093a19f78a73882e07e7b85691e104a13c2aa7591d69d5bb0b`  
		Last Modified: Thu, 22 May 2025 03:33:11 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5603633e43ead8cdfe1166c297333dfe796274ddf207139372d35eef45df62a1`  
		Last Modified: Thu, 22 May 2025 03:33:11 GMT  
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
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de43170be5f9e1fb58ea4e80e1f145dc261e51987c0537bb5227a3d7f3359d68`  
		Last Modified: Wed, 21 May 2025 23:26:31 GMT  
		Size: 219.6 MB (219626408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f86d65431509314a01a4aeee22962d375bea3eebd5eff2045251507cefd6f7`  
		Last Modified: Wed, 21 May 2025 23:26:29 GMT  
		Size: 2.6 MB (2627118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfea23f7b4fafcb782b1b0c54d8c54eb35812c165529527d77c2183f1746b207`  
		Last Modified: Wed, 21 May 2025 23:26:28 GMT  
		Size: 476.8 KB (476848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b3a1fe21488e465b267af080d89abf50ee1cba6bbce636e151392ebf9c0ed6`  
		Last Modified: Wed, 21 May 2025 23:26:33 GMT  
		Size: 331.8 MB (331766491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ae4acd472c4a6dcd2f22d39391a01cb908bdd5cb830bc143b4f54922a79e8f`  
		Last Modified: Wed, 21 May 2025 23:26:29 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f88c8fd9f45e28d40f34cf7067b3a3cdc11eb5bc6f5adde9b4e089b072174b`  
		Last Modified: Wed, 21 May 2025 23:26:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0c547c4a0d605a3fdeef8c715e313e0d9e8e38687e43776aebcb80d2ee385b`  
		Last Modified: Wed, 21 May 2025 23:26:30 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ad8579c3ceec1f8ea00538626a95009d6ba32c6329a134dc681afec1652617`  
		Last Modified: Wed, 21 May 2025 23:26:30 GMT  
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
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52977ddac9159aa57ed1b97922da245c54addfb41c40368d3485f2ae50490979`  
		Last Modified: Thu, 22 May 2025 03:33:15 GMT  
		Size: 216.9 MB (216915095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71d641156272d1b267d3759d2f2d85fb4e8b558651dc445cfdc9ab9f4c739a9`  
		Last Modified: Thu, 22 May 2025 03:33:09 GMT  
		Size: 2.6 MB (2635396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac8799b401de8e7b25cf120a334a8abc489a6f4d208cbd4ce67ff5e4bf567c9`  
		Last Modified: Thu, 22 May 2025 03:33:09 GMT  
		Size: 476.9 KB (476932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfcc06d468f6ce02c6d87091b84a57b33553e6e5a7301f315b485392f354c89`  
		Last Modified: Thu, 22 May 2025 03:33:20 GMT  
		Size: 331.4 MB (331418058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4a8cd4f0cf96ff9e4be6ab5c52f2568c1eeef40c9797400f44bb5b74b41b4d`  
		Last Modified: Thu, 22 May 2025 03:33:10 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dccbd14118628ea9c6c815f44879b33d3aca35c2b63b12f879889065779d271`  
		Last Modified: Thu, 22 May 2025 03:33:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c4ac1852a22e093a19f78a73882e07e7b85691e104a13c2aa7591d69d5bb0b`  
		Last Modified: Thu, 22 May 2025 03:33:11 GMT  
		Size: 589.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5603633e43ead8cdfe1166c297333dfe796274ddf207139372d35eef45df62a1`  
		Last Modified: Thu, 22 May 2025 03:33:11 GMT  
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
$ docker pull odoo@sha256:d90df2730dcd30ec78cb98a05745673c6b44b6a6cd1bbb42587e635b9227bf05
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
$ docker pull odoo@sha256:b4cba31e0dacb4ec6b39f5b566e35878c130eda07a52961d0081d02b76465097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.8 MB (600763219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5200e4944545dc9ccfed451e2e756a1d8162080092cd7f25014b2cd60fa67693`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb513a4b19901f69ef4e52b95a474a53bea9153f86f3888da187dc350e5abf5a`  
		Last Modified: Tue, 20 May 2025 17:25:52 GMT  
		Size: 233.8 MB (233775861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73494d59aad348c008d0f07ccbd22a1f2cb0153711f3f3223d1968a94dcc485f`  
		Last Modified: Tue, 20 May 2025 17:25:46 GMT  
		Size: 2.5 MB (2523144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc208e02d2ee333f590bf8ea3d994ee2be7bfe74263ac1d44787e1d53f09b86e`  
		Last Modified: Tue, 20 May 2025 17:25:46 GMT  
		Size: 477.9 KB (477914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663456ca14fdc12a6320cb43f180934fabd7917804f74e73b6db529857b5b8c0`  
		Last Modified: Tue, 20 May 2025 17:25:55 GMT  
		Size: 334.5 MB (334451247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70f52532529f06f69abf6a2bdd7ef8fc62a3baf18d954fdde4365e405079703`  
		Last Modified: Tue, 20 May 2025 17:25:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a93c771a702e37d62cc8432197f1ddaaa7e7dd6b5568cea3ac8c3a8e3007b37`  
		Last Modified: Tue, 20 May 2025 17:25:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6adc659276acc6244ae8bed2abcc24945946e57ded4bbe0bb52cf3f741261c6`  
		Last Modified: Tue, 20 May 2025 17:25:48 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcddb97494a7d48de1d979035481f42e203ac1d8d4983e6a5dff275e00854e`  
		Last Modified: Tue, 20 May 2025 17:25:49 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:228dfd422295abe1865a48a73b2b8f3bf1add128ee3ac3500b58a0c91085fe9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39886341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c595648243fbce0c13b89e36e938746b141e2a0e44fda1f824506dfe42199b`

```dockerfile
```

-	Layers:
	-	`sha256:cf6bee33ffc09cef71ae398f98b39942563f8b6b8db49647c207a4d66522cbb2`  
		Last Modified: Tue, 20 May 2025 17:25:47 GMT  
		Size: 39.9 MB (39859506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:388097befef02397b43ed3a2492a7189b0cb6bcb4f48935eeab03e443767f970`  
		Last Modified: Tue, 20 May 2025 17:25:46 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:155a8ee0a027226c0c17df95c12a680dfc0d6ebdce80ec1c33f7e16c4682c59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.5 MB (595542878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56af5fe7204f95ed668a202756afeaeece4c5fc82dd82a5c453b8e46941f43e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
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
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bd7108ec52dd78260ad4f80a04efbad121aeeb116b21b9c62b4be07d95faac`  
		Last Modified: Mon, 05 May 2025 18:01:03 GMT  
		Size: 231.1 MB (231147839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81098c35c49b0dbb7a64923e445aa169b5be8372947d45fdcf43f9a26fded010`  
		Last Modified: Mon, 05 May 2025 18:00:57 GMT  
		Size: 2.5 MB (2513154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c8197e625cbc330bb9780b13875799b00dcb7b4c37e7c30d9fb83921330052`  
		Last Modified: Mon, 05 May 2025 18:00:57 GMT  
		Size: 478.8 KB (478808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a0f502f55138db84cbb57330afbf3a06fe7189bce40a2f75f94ee74536635c`  
		Last Modified: Tue, 20 May 2025 17:28:53 GMT  
		Size: 334.0 MB (334046429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f42c231398aa9a496111a6220126d59e38f941c2b111ae40c2acca7b043bcd`  
		Last Modified: Tue, 20 May 2025 17:28:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55fcedd582ea2537a992fa349fa675d3d9fb4f49a3aed3b526f538f323aa7e`  
		Last Modified: Tue, 20 May 2025 17:28:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6023a9aee1a1ca6b663f8b4a18aead25462e14c11fe0fac76d70c0e13f2b259`  
		Last Modified: Tue, 20 May 2025 17:28:45 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd2c4e934e8b0d9dba654a8d64b207ef786e682419bb7966ea201cf6709060a`  
		Last Modified: Tue, 20 May 2025 17:28:47 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:9d4d2b3cf81df2d423ba1677e4fba7b122fdc59dcf9cf61f2b567c5251c55e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39892780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0be3755564e0c159d9a6754a29aac5ab98950bfefd5e8f08e783998b7d4825`

```dockerfile
```

-	Layers:
	-	`sha256:ed7056d5f2759084ced0a601932bfdb246b807330f40c076fb584e56b3507651`  
		Last Modified: Tue, 20 May 2025 17:28:47 GMT  
		Size: 39.9 MB (39865793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39c03223a2b1bfaa042474b5476122ef8794d4de6086e506e053cef3ff709fb6`  
		Last Modified: Tue, 20 May 2025 17:28:45 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:8e6c7cb183b8cdaa0648453de3201f58cfa9cbbd2b0d0b80ef31d9dcb0857646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.2 MB (617185780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ecaec7eb64cd94f8b82c610c69de25aa3c8834c801b3d56aa9dd4595903dba4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
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
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7256933103373699f4c80ac5dca8cf274fbfaf35fe3b97b004dde6379400f230`  
		Last Modified: Mon, 05 May 2025 17:55:06 GMT  
		Size: 243.3 MB (243257313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d6fb2c78472406615a55a954125ead4b4fa0f7dd1f95f3a3e7b8d96aabd9c8`  
		Last Modified: Mon, 05 May 2025 17:54:58 GMT  
		Size: 2.8 MB (2839410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816597fe11dc0154be787d2f241ce0339189981b886d2037475ffd9f8fe0a27c`  
		Last Modified: Mon, 05 May 2025 17:54:57 GMT  
		Size: 478.9 KB (478884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20fcf12d0a0c3be9f83efd3da5c3cb548f4268f84f8e40e1fe67794bd9512b9`  
		Last Modified: Tue, 20 May 2025 17:35:20 GMT  
		Size: 336.2 MB (336164519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5300a9e6ef82f0e8d35416caf6636f252657f3dfb0844fea2d86dad9de3240`  
		Last Modified: Tue, 20 May 2025 17:34:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990f5c9d2c261d5209eacb20489bfe9871c48aa727c62cfbbfdd5b67f4e5fa5c`  
		Last Modified: Tue, 20 May 2025 17:34:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427f7a87a63830ec4eda116e496d4012aa32fa3251158d86a62315515d261106`  
		Last Modified: Tue, 20 May 2025 17:34:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaec67b025e95cfc45e1cd06a03db7ad81f74682264a5b610b9a1bd99c4fcaa`  
		Last Modified: Tue, 20 May 2025 17:34:59 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:022014f27dd0b01a97caf33a44cd7270a96fa968688971bfc480feb5a35f6b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39894784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05595fb54ddde1ee8d4f2eb63e4e552837c69c0b895a1567acb3879f63d54bae`

```dockerfile
```

-	Layers:
	-	`sha256:5acbcc9c301600b8d49bc45530635fba1df441fd9c4f751de442b1ee4b923074`  
		Last Modified: Tue, 20 May 2025 17:35:02 GMT  
		Size: 39.9 MB (39867893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d726010e3e4925897262a05e2ba41dae7f56d8ab5b7f3fbd93f0d8b10dcb5f5`  
		Last Modified: Tue, 20 May 2025 17:34:58 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:d90df2730dcd30ec78cb98a05745673c6b44b6a6cd1bbb42587e635b9227bf05
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
$ docker pull odoo@sha256:b4cba31e0dacb4ec6b39f5b566e35878c130eda07a52961d0081d02b76465097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.8 MB (600763219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5200e4944545dc9ccfed451e2e756a1d8162080092cd7f25014b2cd60fa67693`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb513a4b19901f69ef4e52b95a474a53bea9153f86f3888da187dc350e5abf5a`  
		Last Modified: Tue, 20 May 2025 17:25:52 GMT  
		Size: 233.8 MB (233775861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73494d59aad348c008d0f07ccbd22a1f2cb0153711f3f3223d1968a94dcc485f`  
		Last Modified: Tue, 20 May 2025 17:25:46 GMT  
		Size: 2.5 MB (2523144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc208e02d2ee333f590bf8ea3d994ee2be7bfe74263ac1d44787e1d53f09b86e`  
		Last Modified: Tue, 20 May 2025 17:25:46 GMT  
		Size: 477.9 KB (477914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663456ca14fdc12a6320cb43f180934fabd7917804f74e73b6db529857b5b8c0`  
		Last Modified: Tue, 20 May 2025 17:25:55 GMT  
		Size: 334.5 MB (334451247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70f52532529f06f69abf6a2bdd7ef8fc62a3baf18d954fdde4365e405079703`  
		Last Modified: Tue, 20 May 2025 17:25:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a93c771a702e37d62cc8432197f1ddaaa7e7dd6b5568cea3ac8c3a8e3007b37`  
		Last Modified: Tue, 20 May 2025 17:25:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6adc659276acc6244ae8bed2abcc24945946e57ded4bbe0bb52cf3f741261c6`  
		Last Modified: Tue, 20 May 2025 17:25:48 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcddb97494a7d48de1d979035481f42e203ac1d8d4983e6a5dff275e00854e`  
		Last Modified: Tue, 20 May 2025 17:25:49 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:228dfd422295abe1865a48a73b2b8f3bf1add128ee3ac3500b58a0c91085fe9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39886341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c595648243fbce0c13b89e36e938746b141e2a0e44fda1f824506dfe42199b`

```dockerfile
```

-	Layers:
	-	`sha256:cf6bee33ffc09cef71ae398f98b39942563f8b6b8db49647c207a4d66522cbb2`  
		Last Modified: Tue, 20 May 2025 17:25:47 GMT  
		Size: 39.9 MB (39859506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:388097befef02397b43ed3a2492a7189b0cb6bcb4f48935eeab03e443767f970`  
		Last Modified: Tue, 20 May 2025 17:25:46 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:155a8ee0a027226c0c17df95c12a680dfc0d6ebdce80ec1c33f7e16c4682c59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.5 MB (595542878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56af5fe7204f95ed668a202756afeaeece4c5fc82dd82a5c453b8e46941f43e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
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
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bd7108ec52dd78260ad4f80a04efbad121aeeb116b21b9c62b4be07d95faac`  
		Last Modified: Mon, 05 May 2025 18:01:03 GMT  
		Size: 231.1 MB (231147839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81098c35c49b0dbb7a64923e445aa169b5be8372947d45fdcf43f9a26fded010`  
		Last Modified: Mon, 05 May 2025 18:00:57 GMT  
		Size: 2.5 MB (2513154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c8197e625cbc330bb9780b13875799b00dcb7b4c37e7c30d9fb83921330052`  
		Last Modified: Mon, 05 May 2025 18:00:57 GMT  
		Size: 478.8 KB (478808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a0f502f55138db84cbb57330afbf3a06fe7189bce40a2f75f94ee74536635c`  
		Last Modified: Tue, 20 May 2025 17:28:53 GMT  
		Size: 334.0 MB (334046429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f42c231398aa9a496111a6220126d59e38f941c2b111ae40c2acca7b043bcd`  
		Last Modified: Tue, 20 May 2025 17:28:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55fcedd582ea2537a992fa349fa675d3d9fb4f49a3aed3b526f538f323aa7e`  
		Last Modified: Tue, 20 May 2025 17:28:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6023a9aee1a1ca6b663f8b4a18aead25462e14c11fe0fac76d70c0e13f2b259`  
		Last Modified: Tue, 20 May 2025 17:28:45 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd2c4e934e8b0d9dba654a8d64b207ef786e682419bb7966ea201cf6709060a`  
		Last Modified: Tue, 20 May 2025 17:28:47 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9d4d2b3cf81df2d423ba1677e4fba7b122fdc59dcf9cf61f2b567c5251c55e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39892780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0be3755564e0c159d9a6754a29aac5ab98950bfefd5e8f08e783998b7d4825`

```dockerfile
```

-	Layers:
	-	`sha256:ed7056d5f2759084ced0a601932bfdb246b807330f40c076fb584e56b3507651`  
		Last Modified: Tue, 20 May 2025 17:28:47 GMT  
		Size: 39.9 MB (39865793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39c03223a2b1bfaa042474b5476122ef8794d4de6086e506e053cef3ff709fb6`  
		Last Modified: Tue, 20 May 2025 17:28:45 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:8e6c7cb183b8cdaa0648453de3201f58cfa9cbbd2b0d0b80ef31d9dcb0857646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.2 MB (617185780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ecaec7eb64cd94f8b82c610c69de25aa3c8834c801b3d56aa9dd4595903dba4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
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
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7256933103373699f4c80ac5dca8cf274fbfaf35fe3b97b004dde6379400f230`  
		Last Modified: Mon, 05 May 2025 17:55:06 GMT  
		Size: 243.3 MB (243257313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d6fb2c78472406615a55a954125ead4b4fa0f7dd1f95f3a3e7b8d96aabd9c8`  
		Last Modified: Mon, 05 May 2025 17:54:58 GMT  
		Size: 2.8 MB (2839410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816597fe11dc0154be787d2f241ce0339189981b886d2037475ffd9f8fe0a27c`  
		Last Modified: Mon, 05 May 2025 17:54:57 GMT  
		Size: 478.9 KB (478884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20fcf12d0a0c3be9f83efd3da5c3cb548f4268f84f8e40e1fe67794bd9512b9`  
		Last Modified: Tue, 20 May 2025 17:35:20 GMT  
		Size: 336.2 MB (336164519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5300a9e6ef82f0e8d35416caf6636f252657f3dfb0844fea2d86dad9de3240`  
		Last Modified: Tue, 20 May 2025 17:34:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990f5c9d2c261d5209eacb20489bfe9871c48aa727c62cfbbfdd5b67f4e5fa5c`  
		Last Modified: Tue, 20 May 2025 17:34:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427f7a87a63830ec4eda116e496d4012aa32fa3251158d86a62315515d261106`  
		Last Modified: Tue, 20 May 2025 17:34:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaec67b025e95cfc45e1cd06a03db7ad81f74682264a5b610b9a1bd99c4fcaa`  
		Last Modified: Tue, 20 May 2025 17:34:59 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:022014f27dd0b01a97caf33a44cd7270a96fa968688971bfc480feb5a35f6b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39894784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05595fb54ddde1ee8d4f2eb63e4e552837c69c0b895a1567acb3879f63d54bae`

```dockerfile
```

-	Layers:
	-	`sha256:5acbcc9c301600b8d49bc45530635fba1df441fd9c4f751de442b1ee4b923074`  
		Last Modified: Tue, 20 May 2025 17:35:02 GMT  
		Size: 39.9 MB (39867893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d726010e3e4925897262a05e2ba41dae7f56d8ab5b7f3fbd93f0d8b10dcb5f5`  
		Last Modified: Tue, 20 May 2025 17:34:58 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250520`

```console
$ docker pull odoo@sha256:d90df2730dcd30ec78cb98a05745673c6b44b6a6cd1bbb42587e635b9227bf05
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
$ docker pull odoo@sha256:b4cba31e0dacb4ec6b39f5b566e35878c130eda07a52961d0081d02b76465097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.8 MB (600763219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5200e4944545dc9ccfed451e2e756a1d8162080092cd7f25014b2cd60fa67693`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb513a4b19901f69ef4e52b95a474a53bea9153f86f3888da187dc350e5abf5a`  
		Last Modified: Tue, 20 May 2025 17:25:52 GMT  
		Size: 233.8 MB (233775861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73494d59aad348c008d0f07ccbd22a1f2cb0153711f3f3223d1968a94dcc485f`  
		Last Modified: Tue, 20 May 2025 17:25:46 GMT  
		Size: 2.5 MB (2523144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc208e02d2ee333f590bf8ea3d994ee2be7bfe74263ac1d44787e1d53f09b86e`  
		Last Modified: Tue, 20 May 2025 17:25:46 GMT  
		Size: 477.9 KB (477914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663456ca14fdc12a6320cb43f180934fabd7917804f74e73b6db529857b5b8c0`  
		Last Modified: Tue, 20 May 2025 17:25:55 GMT  
		Size: 334.5 MB (334451247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70f52532529f06f69abf6a2bdd7ef8fc62a3baf18d954fdde4365e405079703`  
		Last Modified: Tue, 20 May 2025 17:25:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a93c771a702e37d62cc8432197f1ddaaa7e7dd6b5568cea3ac8c3a8e3007b37`  
		Last Modified: Tue, 20 May 2025 17:25:48 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6adc659276acc6244ae8bed2abcc24945946e57ded4bbe0bb52cf3f741261c6`  
		Last Modified: Tue, 20 May 2025 17:25:48 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafcddb97494a7d48de1d979035481f42e203ac1d8d4983e6a5dff275e00854e`  
		Last Modified: Tue, 20 May 2025 17:25:49 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:228dfd422295abe1865a48a73b2b8f3bf1add128ee3ac3500b58a0c91085fe9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39886341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c595648243fbce0c13b89e36e938746b141e2a0e44fda1f824506dfe42199b`

```dockerfile
```

-	Layers:
	-	`sha256:cf6bee33ffc09cef71ae398f98b39942563f8b6b8db49647c207a4d66522cbb2`  
		Last Modified: Tue, 20 May 2025 17:25:47 GMT  
		Size: 39.9 MB (39859506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:388097befef02397b43ed3a2492a7189b0cb6bcb4f48935eeab03e443767f970`  
		Last Modified: Tue, 20 May 2025 17:25:46 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250520` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:155a8ee0a027226c0c17df95c12a680dfc0d6ebdce80ec1c33f7e16c4682c59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.5 MB (595542878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56af5fe7204f95ed668a202756afeaeece4c5fc82dd82a5c453b8e46941f43e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
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
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bd7108ec52dd78260ad4f80a04efbad121aeeb116b21b9c62b4be07d95faac`  
		Last Modified: Mon, 05 May 2025 18:01:03 GMT  
		Size: 231.1 MB (231147839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81098c35c49b0dbb7a64923e445aa169b5be8372947d45fdcf43f9a26fded010`  
		Last Modified: Mon, 05 May 2025 18:00:57 GMT  
		Size: 2.5 MB (2513154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c8197e625cbc330bb9780b13875799b00dcb7b4c37e7c30d9fb83921330052`  
		Last Modified: Mon, 05 May 2025 18:00:57 GMT  
		Size: 478.8 KB (478808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a0f502f55138db84cbb57330afbf3a06fe7189bce40a2f75f94ee74536635c`  
		Last Modified: Tue, 20 May 2025 17:28:53 GMT  
		Size: 334.0 MB (334046429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f42c231398aa9a496111a6220126d59e38f941c2b111ae40c2acca7b043bcd`  
		Last Modified: Tue, 20 May 2025 17:28:45 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d55fcedd582ea2537a992fa349fa675d3d9fb4f49a3aed3b526f538f323aa7e`  
		Last Modified: Tue, 20 May 2025 17:28:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6023a9aee1a1ca6b663f8b4a18aead25462e14c11fe0fac76d70c0e13f2b259`  
		Last Modified: Tue, 20 May 2025 17:28:45 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd2c4e934e8b0d9dba654a8d64b207ef786e682419bb7966ea201cf6709060a`  
		Last Modified: Tue, 20 May 2025 17:28:47 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:9d4d2b3cf81df2d423ba1677e4fba7b122fdc59dcf9cf61f2b567c5251c55e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39892780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0be3755564e0c159d9a6754a29aac5ab98950bfefd5e8f08e783998b7d4825`

```dockerfile
```

-	Layers:
	-	`sha256:ed7056d5f2759084ced0a601932bfdb246b807330f40c076fb584e56b3507651`  
		Last Modified: Tue, 20 May 2025 17:28:47 GMT  
		Size: 39.9 MB (39865793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39c03223a2b1bfaa042474b5476122ef8794d4de6086e506e053cef3ff709fb6`  
		Last Modified: Tue, 20 May 2025 17:28:45 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250520` - linux; ppc64le

```console
$ docker pull odoo@sha256:8e6c7cb183b8cdaa0648453de3201f58cfa9cbbd2b0d0b80ef31d9dcb0857646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.2 MB (617185780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ecaec7eb64cd94f8b82c610c69de25aa3c8834c801b3d56aa9dd4595903dba4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
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
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7256933103373699f4c80ac5dca8cf274fbfaf35fe3b97b004dde6379400f230`  
		Last Modified: Mon, 05 May 2025 17:55:06 GMT  
		Size: 243.3 MB (243257313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d6fb2c78472406615a55a954125ead4b4fa0f7dd1f95f3a3e7b8d96aabd9c8`  
		Last Modified: Mon, 05 May 2025 17:54:58 GMT  
		Size: 2.8 MB (2839410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816597fe11dc0154be787d2f241ce0339189981b886d2037475ffd9f8fe0a27c`  
		Last Modified: Mon, 05 May 2025 17:54:57 GMT  
		Size: 478.9 KB (478884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20fcf12d0a0c3be9f83efd3da5c3cb548f4268f84f8e40e1fe67794bd9512b9`  
		Last Modified: Tue, 20 May 2025 17:35:20 GMT  
		Size: 336.2 MB (336164519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5300a9e6ef82f0e8d35416caf6636f252657f3dfb0844fea2d86dad9de3240`  
		Last Modified: Tue, 20 May 2025 17:34:58 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990f5c9d2c261d5209eacb20489bfe9871c48aa727c62cfbbfdd5b67f4e5fa5c`  
		Last Modified: Tue, 20 May 2025 17:34:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427f7a87a63830ec4eda116e496d4012aa32fa3251158d86a62315515d261106`  
		Last Modified: Tue, 20 May 2025 17:34:58 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaec67b025e95cfc45e1cd06a03db7ad81f74682264a5b610b9a1bd99c4fcaa`  
		Last Modified: Tue, 20 May 2025 17:34:59 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:022014f27dd0b01a97caf33a44cd7270a96fa968688971bfc480feb5a35f6b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39894784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05595fb54ddde1ee8d4f2eb63e4e552837c69c0b895a1567acb3879f63d54bae`

```dockerfile
```

-	Layers:
	-	`sha256:5acbcc9c301600b8d49bc45530635fba1df441fd9c4f751de442b1ee4b923074`  
		Last Modified: Tue, 20 May 2025 17:35:02 GMT  
		Size: 39.9 MB (39867893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d726010e3e4925897262a05e2ba41dae7f56d8ab5b7f3fbd93f0d8b10dcb5f5`  
		Last Modified: Tue, 20 May 2025 17:34:58 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:841ecb27d7fb29d0bacc3a569793701fc700e6f1d52a9e007f96cfc213a1ddb8
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
$ docker pull odoo@sha256:3204b08a67c9e680f1e6d6c349cf2c1a8ba982ae907f76313402241bd69f6a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.2 MB (671243826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6ed794cb71fdd3cce36a5d8c1cd32cbf27104f9d1157d4c1e2e31f41fe2a00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e94cd98645efcfa3be6afe44a5c49a07acb727825ec4d81ac00d63e7d54d392`  
		Last Modified: Tue, 20 May 2025 17:26:15 GMT  
		Size: 254.5 MB (254517295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ef960f923ef00940afd0787ef1f9cde23775d67143803e158780b2fbed3c11`  
		Last Modified: Tue, 20 May 2025 17:26:11 GMT  
		Size: 14.3 MB (14274916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f3f32918ae39492de02ba45803ac1538ace26ccdc4eb53695b141bcd6296a`  
		Last Modified: Tue, 20 May 2025 17:26:11 GMT  
		Size: 477.6 KB (477643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dec6eb27a374ea09d2b5e415180a9f0c0ef5f96d536e39fdb64e2fc8e6da03`  
		Last Modified: Tue, 20 May 2025 17:26:16 GMT  
		Size: 372.3 MB (372254006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212bc242a6b41d57269578ea6750b2be78c1723fc75eaf70cddf887298f142fa`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd960cb93a292f5359ad597ff7ccdf154a7bf3fa180716ed5a6dbce5f29a286d`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d96e72f815d011ba5ef72ee4d91726f5debf856d8f69706a01ecf1781d9808`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b2b5afadfaf8516c5315cf5954ad08044d57df10b298812c7fa8e30155972d`  
		Last Modified: Tue, 20 May 2025 17:26:13 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:29f290ac349794ca72dbf62f248880ae99670d7c2938d14215d32be42662019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59380831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8fa6e9a1d12ac5dcfdd641a1e222c68bca61493f4dd064a6fad26040a21e6c`

```dockerfile
```

-	Layers:
	-	`sha256:1441b9f01aa838a5459767ccfa7ab57cc9ea366b5882adc2adcaa7ebf8754b8a`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 59.4 MB (59353695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daaa54207c61bc2a6215a77e6018f6ee22a94cc121cb02dca849430c1d51d929`  
		Last Modified: Tue, 20 May 2025 17:26:11 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:88a09c69a66c4be5ee9dc29be8b146b6412c09f2c7a32f0de8de767ecb34d295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.6 MB (667629866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d286ff0f3a89a5d6b9c8adfecf4bcc75422ef54a73b4f991e18ec88581e07a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
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
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9cea12ad03e430fdf48d3d8940f180d90e8d3ab7751cd37cd03b42984aaf74`  
		Last Modified: Mon, 05 May 2025 17:55:36 GMT  
		Size: 251.9 MB (251942645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa0aced1c160ae538bf0ebec5077a1e8afbcaf5d03efbcbcb962ee3b221dc77`  
		Last Modified: Mon, 05 May 2025 17:55:31 GMT  
		Size: 14.2 MB (14248288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8a45247f2759eee35efbf0f41226f028f4a4c0d102c16f95ecf5a6087605d4`  
		Last Modified: Mon, 05 May 2025 17:55:30 GMT  
		Size: 478.6 KB (478561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceca93b0b29c3064ab238fdb9f103e6a28aa2b81f84b007a6dbca83e5a2d6176`  
		Last Modified: Tue, 20 May 2025 17:25:24 GMT  
		Size: 372.1 MB (372111052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fceeaa6589b979d1ca1668b9e008609a9745d3663a098638573be022c8aa5b`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41753855125de38cd03d382e1a312e8bc74ee7c1191bfcfbcbba96327e7e916`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225a88a94680477b25ef099f4d84d281f58d5feffef7caaf144b015932aaa3e3`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968101ce00f1a089f75cc0ab1bc51894b6555567d679feb10ec4e1bb572d3a1c`  
		Last Modified: Tue, 20 May 2025 17:25:17 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:a070191c5af9e32e6c15847a7ecd9505213e7458cfe5d84f254ba041f671edff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59388062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4a5829afe3b5d96d186f7462368526c68ff7dad78bf4d2f769cb6d555241ae`

```dockerfile
```

-	Layers:
	-	`sha256:6c35f5772f8de5b9ab0c4d6ac960b5e24597c6c2008c8abb75be8f5bdce30bb8`  
		Last Modified: Tue, 20 May 2025 17:25:18 GMT  
		Size: 59.4 MB (59360762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1a0d51055d84cc4e7e5dcce9ab21180f26c7d1a83e15027375f6796b0f1f40`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:773a76d3caae66c54f06109175e212871598ba172a023aedb2c24f48bc9c6008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.5 MB (687478803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7770214846d86f34f5e6f5b34dc308f2bceb2f42b8d2d0e3a4c9bc92ba553be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:57 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:57 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:46:00 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Mon, 28 Apr 2025 09:46:01 GMT
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
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0cfd686d0bf7f2685e08e731f2256951d6fd010571255282341db491622f6`  
		Last Modified: Mon, 05 May 2025 17:46:12 GMT  
		Size: 265.1 MB (265077741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b4970c3558e4f73623c9885fa8a1bddebb7ce9e44d6760e871a869602afee`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 14.8 MB (14797186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5152a85d6330f04722330a9eb18fa24c8dce960b2f2ac3ed34b33e74d5d8439`  
		Last Modified: Mon, 05 May 2025 17:45:55 GMT  
		Size: 478.6 KB (478615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5e4514e756bfface9a851928fea41eb558dff37fab559539f73b1b3471ee6`  
		Last Modified: Tue, 20 May 2025 17:29:15 GMT  
		Size: 372.8 MB (372781985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4cca0d7f1df9c76b7283123d8662b3411463263bd67d3c35d68131d52d014f`  
		Last Modified: Tue, 20 May 2025 17:29:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a3958bb310ce70654885a7d053a8f308f5b7068409b6e221771beaf4541d26`  
		Last Modified: Tue, 20 May 2025 17:29:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e810b558881b3be06fbeeec4b727e2a7344f2e6ccc03e290c3af710b88698c10`  
		Last Modified: Tue, 20 May 2025 17:29:03 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf6278b4511fd58518d30f8249009fbb6305a2125e31cce1085fee6d06fb53`  
		Last Modified: Tue, 20 May 2025 17:29:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:7fedcdfe61492493909dfbb5390fbab8ac3daded9cf81450278d3559af16766e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59389062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98df6d37a90a68138c6ad986b2f2ca646436732190de3cd655b344cb1293c184`

```dockerfile
```

-	Layers:
	-	`sha256:14acec2794a2e268bdf83b7b95d42c43044ca547f97c8269424b6abc26d1de09`  
		Last Modified: Tue, 20 May 2025 17:29:05 GMT  
		Size: 59.4 MB (59361864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b03d995075cfb28dc34da516333a7afd7c6f6e5ffb015a8b4d00c1e6ef1e292`  
		Last Modified: Tue, 20 May 2025 17:29:02 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:841ecb27d7fb29d0bacc3a569793701fc700e6f1d52a9e007f96cfc213a1ddb8
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
$ docker pull odoo@sha256:3204b08a67c9e680f1e6d6c349cf2c1a8ba982ae907f76313402241bd69f6a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.2 MB (671243826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6ed794cb71fdd3cce36a5d8c1cd32cbf27104f9d1157d4c1e2e31f41fe2a00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e94cd98645efcfa3be6afe44a5c49a07acb727825ec4d81ac00d63e7d54d392`  
		Last Modified: Tue, 20 May 2025 17:26:15 GMT  
		Size: 254.5 MB (254517295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ef960f923ef00940afd0787ef1f9cde23775d67143803e158780b2fbed3c11`  
		Last Modified: Tue, 20 May 2025 17:26:11 GMT  
		Size: 14.3 MB (14274916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f3f32918ae39492de02ba45803ac1538ace26ccdc4eb53695b141bcd6296a`  
		Last Modified: Tue, 20 May 2025 17:26:11 GMT  
		Size: 477.6 KB (477643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dec6eb27a374ea09d2b5e415180a9f0c0ef5f96d536e39fdb64e2fc8e6da03`  
		Last Modified: Tue, 20 May 2025 17:26:16 GMT  
		Size: 372.3 MB (372254006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212bc242a6b41d57269578ea6750b2be78c1723fc75eaf70cddf887298f142fa`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd960cb93a292f5359ad597ff7ccdf154a7bf3fa180716ed5a6dbce5f29a286d`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d96e72f815d011ba5ef72ee4d91726f5debf856d8f69706a01ecf1781d9808`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b2b5afadfaf8516c5315cf5954ad08044d57df10b298812c7fa8e30155972d`  
		Last Modified: Tue, 20 May 2025 17:26:13 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:29f290ac349794ca72dbf62f248880ae99670d7c2938d14215d32be42662019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59380831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8fa6e9a1d12ac5dcfdd641a1e222c68bca61493f4dd064a6fad26040a21e6c`

```dockerfile
```

-	Layers:
	-	`sha256:1441b9f01aa838a5459767ccfa7ab57cc9ea366b5882adc2adcaa7ebf8754b8a`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 59.4 MB (59353695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daaa54207c61bc2a6215a77e6018f6ee22a94cc121cb02dca849430c1d51d929`  
		Last Modified: Tue, 20 May 2025 17:26:11 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:88a09c69a66c4be5ee9dc29be8b146b6412c09f2c7a32f0de8de767ecb34d295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.6 MB (667629866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d286ff0f3a89a5d6b9c8adfecf4bcc75422ef54a73b4f991e18ec88581e07a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
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
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9cea12ad03e430fdf48d3d8940f180d90e8d3ab7751cd37cd03b42984aaf74`  
		Last Modified: Mon, 05 May 2025 17:55:36 GMT  
		Size: 251.9 MB (251942645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa0aced1c160ae538bf0ebec5077a1e8afbcaf5d03efbcbcb962ee3b221dc77`  
		Last Modified: Mon, 05 May 2025 17:55:31 GMT  
		Size: 14.2 MB (14248288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8a45247f2759eee35efbf0f41226f028f4a4c0d102c16f95ecf5a6087605d4`  
		Last Modified: Mon, 05 May 2025 17:55:30 GMT  
		Size: 478.6 KB (478561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceca93b0b29c3064ab238fdb9f103e6a28aa2b81f84b007a6dbca83e5a2d6176`  
		Last Modified: Tue, 20 May 2025 17:25:24 GMT  
		Size: 372.1 MB (372111052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fceeaa6589b979d1ca1668b9e008609a9745d3663a098638573be022c8aa5b`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41753855125de38cd03d382e1a312e8bc74ee7c1191bfcfbcbba96327e7e916`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225a88a94680477b25ef099f4d84d281f58d5feffef7caaf144b015932aaa3e3`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968101ce00f1a089f75cc0ab1bc51894b6555567d679feb10ec4e1bb572d3a1c`  
		Last Modified: Tue, 20 May 2025 17:25:17 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a070191c5af9e32e6c15847a7ecd9505213e7458cfe5d84f254ba041f671edff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59388062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4a5829afe3b5d96d186f7462368526c68ff7dad78bf4d2f769cb6d555241ae`

```dockerfile
```

-	Layers:
	-	`sha256:6c35f5772f8de5b9ab0c4d6ac960b5e24597c6c2008c8abb75be8f5bdce30bb8`  
		Last Modified: Tue, 20 May 2025 17:25:18 GMT  
		Size: 59.4 MB (59360762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1a0d51055d84cc4e7e5dcce9ab21180f26c7d1a83e15027375f6796b0f1f40`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:773a76d3caae66c54f06109175e212871598ba172a023aedb2c24f48bc9c6008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.5 MB (687478803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7770214846d86f34f5e6f5b34dc308f2bceb2f42b8d2d0e3a4c9bc92ba553be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:57 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:57 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:46:00 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Mon, 28 Apr 2025 09:46:01 GMT
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
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0cfd686d0bf7f2685e08e731f2256951d6fd010571255282341db491622f6`  
		Last Modified: Mon, 05 May 2025 17:46:12 GMT  
		Size: 265.1 MB (265077741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b4970c3558e4f73623c9885fa8a1bddebb7ce9e44d6760e871a869602afee`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 14.8 MB (14797186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5152a85d6330f04722330a9eb18fa24c8dce960b2f2ac3ed34b33e74d5d8439`  
		Last Modified: Mon, 05 May 2025 17:45:55 GMT  
		Size: 478.6 KB (478615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5e4514e756bfface9a851928fea41eb558dff37fab559539f73b1b3471ee6`  
		Last Modified: Tue, 20 May 2025 17:29:15 GMT  
		Size: 372.8 MB (372781985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4cca0d7f1df9c76b7283123d8662b3411463263bd67d3c35d68131d52d014f`  
		Last Modified: Tue, 20 May 2025 17:29:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a3958bb310ce70654885a7d053a8f308f5b7068409b6e221771beaf4541d26`  
		Last Modified: Tue, 20 May 2025 17:29:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e810b558881b3be06fbeeec4b727e2a7344f2e6ccc03e290c3af710b88698c10`  
		Last Modified: Tue, 20 May 2025 17:29:03 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf6278b4511fd58518d30f8249009fbb6305a2125e31cce1085fee6d06fb53`  
		Last Modified: Tue, 20 May 2025 17:29:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7fedcdfe61492493909dfbb5390fbab8ac3daded9cf81450278d3559af16766e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59389062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98df6d37a90a68138c6ad986b2f2ca646436732190de3cd655b344cb1293c184`

```dockerfile
```

-	Layers:
	-	`sha256:14acec2794a2e268bdf83b7b95d42c43044ca547f97c8269424b6abc26d1de09`  
		Last Modified: Tue, 20 May 2025 17:29:05 GMT  
		Size: 59.4 MB (59361864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b03d995075cfb28dc34da516333a7afd7c6f6e5ffb015a8b4d00c1e6ef1e292`  
		Last Modified: Tue, 20 May 2025 17:29:02 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250520`

```console
$ docker pull odoo@sha256:841ecb27d7fb29d0bacc3a569793701fc700e6f1d52a9e007f96cfc213a1ddb8
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
$ docker pull odoo@sha256:3204b08a67c9e680f1e6d6c349cf2c1a8ba982ae907f76313402241bd69f6a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.2 MB (671243826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6ed794cb71fdd3cce36a5d8c1cd32cbf27104f9d1157d4c1e2e31f41fe2a00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e94cd98645efcfa3be6afe44a5c49a07acb727825ec4d81ac00d63e7d54d392`  
		Last Modified: Tue, 20 May 2025 17:26:15 GMT  
		Size: 254.5 MB (254517295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ef960f923ef00940afd0787ef1f9cde23775d67143803e158780b2fbed3c11`  
		Last Modified: Tue, 20 May 2025 17:26:11 GMT  
		Size: 14.3 MB (14274916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f3f32918ae39492de02ba45803ac1538ace26ccdc4eb53695b141bcd6296a`  
		Last Modified: Tue, 20 May 2025 17:26:11 GMT  
		Size: 477.6 KB (477643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dec6eb27a374ea09d2b5e415180a9f0c0ef5f96d536e39fdb64e2fc8e6da03`  
		Last Modified: Tue, 20 May 2025 17:26:16 GMT  
		Size: 372.3 MB (372254006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212bc242a6b41d57269578ea6750b2be78c1723fc75eaf70cddf887298f142fa`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd960cb93a292f5359ad597ff7ccdf154a7bf3fa180716ed5a6dbce5f29a286d`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d96e72f815d011ba5ef72ee4d91726f5debf856d8f69706a01ecf1781d9808`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b2b5afadfaf8516c5315cf5954ad08044d57df10b298812c7fa8e30155972d`  
		Last Modified: Tue, 20 May 2025 17:26:13 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:29f290ac349794ca72dbf62f248880ae99670d7c2938d14215d32be42662019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59380831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8fa6e9a1d12ac5dcfdd641a1e222c68bca61493f4dd064a6fad26040a21e6c`

```dockerfile
```

-	Layers:
	-	`sha256:1441b9f01aa838a5459767ccfa7ab57cc9ea366b5882adc2adcaa7ebf8754b8a`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 59.4 MB (59353695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daaa54207c61bc2a6215a77e6018f6ee22a94cc121cb02dca849430c1d51d929`  
		Last Modified: Tue, 20 May 2025 17:26:11 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250520` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:88a09c69a66c4be5ee9dc29be8b146b6412c09f2c7a32f0de8de767ecb34d295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.6 MB (667629866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d286ff0f3a89a5d6b9c8adfecf4bcc75422ef54a73b4f991e18ec88581e07a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
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
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9cea12ad03e430fdf48d3d8940f180d90e8d3ab7751cd37cd03b42984aaf74`  
		Last Modified: Mon, 05 May 2025 17:55:36 GMT  
		Size: 251.9 MB (251942645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa0aced1c160ae538bf0ebec5077a1e8afbcaf5d03efbcbcb962ee3b221dc77`  
		Last Modified: Mon, 05 May 2025 17:55:31 GMT  
		Size: 14.2 MB (14248288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8a45247f2759eee35efbf0f41226f028f4a4c0d102c16f95ecf5a6087605d4`  
		Last Modified: Mon, 05 May 2025 17:55:30 GMT  
		Size: 478.6 KB (478561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceca93b0b29c3064ab238fdb9f103e6a28aa2b81f84b007a6dbca83e5a2d6176`  
		Last Modified: Tue, 20 May 2025 17:25:24 GMT  
		Size: 372.1 MB (372111052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fceeaa6589b979d1ca1668b9e008609a9745d3663a098638573be022c8aa5b`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41753855125de38cd03d382e1a312e8bc74ee7c1191bfcfbcbba96327e7e916`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225a88a94680477b25ef099f4d84d281f58d5feffef7caaf144b015932aaa3e3`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968101ce00f1a089f75cc0ab1bc51894b6555567d679feb10ec4e1bb572d3a1c`  
		Last Modified: Tue, 20 May 2025 17:25:17 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:a070191c5af9e32e6c15847a7ecd9505213e7458cfe5d84f254ba041f671edff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59388062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4a5829afe3b5d96d186f7462368526c68ff7dad78bf4d2f769cb6d555241ae`

```dockerfile
```

-	Layers:
	-	`sha256:6c35f5772f8de5b9ab0c4d6ac960b5e24597c6c2008c8abb75be8f5bdce30bb8`  
		Last Modified: Tue, 20 May 2025 17:25:18 GMT  
		Size: 59.4 MB (59360762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1a0d51055d84cc4e7e5dcce9ab21180f26c7d1a83e15027375f6796b0f1f40`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250520` - linux; ppc64le

```console
$ docker pull odoo@sha256:773a76d3caae66c54f06109175e212871598ba172a023aedb2c24f48bc9c6008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.5 MB (687478803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7770214846d86f34f5e6f5b34dc308f2bceb2f42b8d2d0e3a4c9bc92ba553be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:57 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:57 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:46:00 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Mon, 28 Apr 2025 09:46:01 GMT
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
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0cfd686d0bf7f2685e08e731f2256951d6fd010571255282341db491622f6`  
		Last Modified: Mon, 05 May 2025 17:46:12 GMT  
		Size: 265.1 MB (265077741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b4970c3558e4f73623c9885fa8a1bddebb7ce9e44d6760e871a869602afee`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 14.8 MB (14797186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5152a85d6330f04722330a9eb18fa24c8dce960b2f2ac3ed34b33e74d5d8439`  
		Last Modified: Mon, 05 May 2025 17:45:55 GMT  
		Size: 478.6 KB (478615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5e4514e756bfface9a851928fea41eb558dff37fab559539f73b1b3471ee6`  
		Last Modified: Tue, 20 May 2025 17:29:15 GMT  
		Size: 372.8 MB (372781985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4cca0d7f1df9c76b7283123d8662b3411463263bd67d3c35d68131d52d014f`  
		Last Modified: Tue, 20 May 2025 17:29:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a3958bb310ce70654885a7d053a8f308f5b7068409b6e221771beaf4541d26`  
		Last Modified: Tue, 20 May 2025 17:29:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e810b558881b3be06fbeeec4b727e2a7344f2e6ccc03e290c3af710b88698c10`  
		Last Modified: Tue, 20 May 2025 17:29:03 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf6278b4511fd58518d30f8249009fbb6305a2125e31cce1085fee6d06fb53`  
		Last Modified: Tue, 20 May 2025 17:29:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250520` - unknown; unknown

```console
$ docker pull odoo@sha256:7fedcdfe61492493909dfbb5390fbab8ac3daded9cf81450278d3559af16766e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59389062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98df6d37a90a68138c6ad986b2f2ca646436732190de3cd655b344cb1293c184`

```dockerfile
```

-	Layers:
	-	`sha256:14acec2794a2e268bdf83b7b95d42c43044ca547f97c8269424b6abc26d1de09`  
		Last Modified: Tue, 20 May 2025 17:29:05 GMT  
		Size: 59.4 MB (59361864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b03d995075cfb28dc34da516333a7afd7c6f6e5ffb015a8b4d00c1e6ef1e292`  
		Last Modified: Tue, 20 May 2025 17:29:02 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:841ecb27d7fb29d0bacc3a569793701fc700e6f1d52a9e007f96cfc213a1ddb8
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
$ docker pull odoo@sha256:3204b08a67c9e680f1e6d6c349cf2c1a8ba982ae907f76313402241bd69f6a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.2 MB (671243826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6ed794cb71fdd3cce36a5d8c1cd32cbf27104f9d1157d4c1e2e31f41fe2a00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:48 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:48 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:44:50 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 09:44:51 GMT
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e94cd98645efcfa3be6afe44a5c49a07acb727825ec4d81ac00d63e7d54d392`  
		Last Modified: Tue, 20 May 2025 17:26:15 GMT  
		Size: 254.5 MB (254517295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ef960f923ef00940afd0787ef1f9cde23775d67143803e158780b2fbed3c11`  
		Last Modified: Tue, 20 May 2025 17:26:11 GMT  
		Size: 14.3 MB (14274916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3f3f32918ae39492de02ba45803ac1538ace26ccdc4eb53695b141bcd6296a`  
		Last Modified: Tue, 20 May 2025 17:26:11 GMT  
		Size: 477.6 KB (477643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dec6eb27a374ea09d2b5e415180a9f0c0ef5f96d536e39fdb64e2fc8e6da03`  
		Last Modified: Tue, 20 May 2025 17:26:16 GMT  
		Size: 372.3 MB (372254006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212bc242a6b41d57269578ea6750b2be78c1723fc75eaf70cddf887298f142fa`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd960cb93a292f5359ad597ff7ccdf154a7bf3fa180716ed5a6dbce5f29a286d`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d96e72f815d011ba5ef72ee4d91726f5debf856d8f69706a01ecf1781d9808`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b2b5afadfaf8516c5315cf5954ad08044d57df10b298812c7fa8e30155972d`  
		Last Modified: Tue, 20 May 2025 17:26:13 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:29f290ac349794ca72dbf62f248880ae99670d7c2938d14215d32be42662019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59380831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8fa6e9a1d12ac5dcfdd641a1e222c68bca61493f4dd064a6fad26040a21e6c`

```dockerfile
```

-	Layers:
	-	`sha256:1441b9f01aa838a5459767ccfa7ab57cc9ea366b5882adc2adcaa7ebf8754b8a`  
		Last Modified: Tue, 20 May 2025 17:26:12 GMT  
		Size: 59.4 MB (59353695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daaa54207c61bc2a6215a77e6018f6ee22a94cc121cb02dca849430c1d51d929`  
		Last Modified: Tue, 20 May 2025 17:26:11 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:88a09c69a66c4be5ee9dc29be8b146b6412c09f2c7a32f0de8de767ecb34d295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.6 MB (667629866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d286ff0f3a89a5d6b9c8adfecf4bcc75422ef54a73b4f991e18ec88581e07a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:58 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:45:01 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 09:45:01 GMT
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
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9cea12ad03e430fdf48d3d8940f180d90e8d3ab7751cd37cd03b42984aaf74`  
		Last Modified: Mon, 05 May 2025 17:55:36 GMT  
		Size: 251.9 MB (251942645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa0aced1c160ae538bf0ebec5077a1e8afbcaf5d03efbcbcb962ee3b221dc77`  
		Last Modified: Mon, 05 May 2025 17:55:31 GMT  
		Size: 14.2 MB (14248288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8a45247f2759eee35efbf0f41226f028f4a4c0d102c16f95ecf5a6087605d4`  
		Last Modified: Mon, 05 May 2025 17:55:30 GMT  
		Size: 478.6 KB (478561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceca93b0b29c3064ab238fdb9f103e6a28aa2b81f84b007a6dbca83e5a2d6176`  
		Last Modified: Tue, 20 May 2025 17:25:24 GMT  
		Size: 372.1 MB (372111052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fceeaa6589b979d1ca1668b9e008609a9745d3663a098638573be022c8aa5b`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41753855125de38cd03d382e1a312e8bc74ee7c1191bfcfbcbba96327e7e916`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225a88a94680477b25ef099f4d84d281f58d5feffef7caaf144b015932aaa3e3`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968101ce00f1a089f75cc0ab1bc51894b6555567d679feb10ec4e1bb572d3a1c`  
		Last Modified: Tue, 20 May 2025 17:25:17 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:a070191c5af9e32e6c15847a7ecd9505213e7458cfe5d84f254ba041f671edff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59388062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4a5829afe3b5d96d186f7462368526c68ff7dad78bf4d2f769cb6d555241ae`

```dockerfile
```

-	Layers:
	-	`sha256:6c35f5772f8de5b9ab0c4d6ac960b5e24597c6c2008c8abb75be8f5bdce30bb8`  
		Last Modified: Tue, 20 May 2025 17:25:18 GMT  
		Size: 59.4 MB (59360762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1a0d51055d84cc4e7e5dcce9ab21180f26c7d1a83e15027375f6796b0f1f40`  
		Last Modified: Tue, 20 May 2025 17:25:16 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:773a76d3caae66c54f06109175e212871598ba172a023aedb2c24f48bc9c6008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.5 MB (687478803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7770214846d86f34f5e6f5b34dc308f2bceb2f42b8d2d0e3a4c9bc92ba553be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:57 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:57 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 09:46:00 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Mon, 28 Apr 2025 09:46:01 GMT
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
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0cfd686d0bf7f2685e08e731f2256951d6fd010571255282341db491622f6`  
		Last Modified: Mon, 05 May 2025 17:46:12 GMT  
		Size: 265.1 MB (265077741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b4970c3558e4f73623c9885fa8a1bddebb7ce9e44d6760e871a869602afee`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 14.8 MB (14797186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5152a85d6330f04722330a9eb18fa24c8dce960b2f2ac3ed34b33e74d5d8439`  
		Last Modified: Mon, 05 May 2025 17:45:55 GMT  
		Size: 478.6 KB (478615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5e4514e756bfface9a851928fea41eb558dff37fab559539f73b1b3471ee6`  
		Last Modified: Tue, 20 May 2025 17:29:15 GMT  
		Size: 372.8 MB (372781985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4cca0d7f1df9c76b7283123d8662b3411463263bd67d3c35d68131d52d014f`  
		Last Modified: Tue, 20 May 2025 17:29:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a3958bb310ce70654885a7d053a8f308f5b7068409b6e221771beaf4541d26`  
		Last Modified: Tue, 20 May 2025 17:29:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e810b558881b3be06fbeeec4b727e2a7344f2e6ccc03e290c3af710b88698c10`  
		Last Modified: Tue, 20 May 2025 17:29:03 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf6278b4511fd58518d30f8249009fbb6305a2125e31cce1085fee6d06fb53`  
		Last Modified: Tue, 20 May 2025 17:29:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7fedcdfe61492493909dfbb5390fbab8ac3daded9cf81450278d3559af16766e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59389062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98df6d37a90a68138c6ad986b2f2ca646436732190de3cd655b344cb1293c184`

```dockerfile
```

-	Layers:
	-	`sha256:14acec2794a2e268bdf83b7b95d42c43044ca547f97c8269424b6abc26d1de09`  
		Last Modified: Tue, 20 May 2025 17:29:05 GMT  
		Size: 59.4 MB (59361864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b03d995075cfb28dc34da516333a7afd7c6f6e5ffb015a8b4d00c1e6ef1e292`  
		Last Modified: Tue, 20 May 2025 17:29:02 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
