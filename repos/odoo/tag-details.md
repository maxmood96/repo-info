<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250218`](#odoo160-20250218)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250218`](#odoo170-20250218)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250218`](#odoo180-20250218)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:be3d10a8c2c2e2d758d1ae5fa6862be95a29fd85c26750753d16bd6c1656610b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:a7528e39b58c7d447d997a2a04d8f10e769acae7900eea9f2db2b5be0f655b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.2 MB (584236762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49b0b8aeb4beabba4b814055fcf5f0d7b35d32758f70dbc8bd85f8b83f86ad9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=amd64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=16.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba69b5e1801d19c828d839d90f95c46fa492ef8da663dfbc469a6f51b7a1f86`  
		Last Modified: Tue, 18 Feb 2025 22:29:47 GMT  
		Size: 219.6 MB (219627811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8feded6f36b114dae0844894e55199f90bdc6bedb4314e108d2c4705fd9e18b1`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 2.6 MB (2624925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932bda97339913e7b8221673c983eb0f3076c226979dfe055b0b6a91e2129a1e`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 485.4 KB (485382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc0b2a45b3bcfd58d7938c2fbd9cccdf372bd7b48571b89da7a522294d716a`  
		Last Modified: Tue, 18 Feb 2025 22:29:48 GMT  
		Size: 331.2 MB (331243624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff126b44781c380134caae5bc811884b36f29fa4b1cfc692e99d428f58e6ae2`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43104cd286b2caa00dc9bce8fa135853a682e56cf86bcf0c6ded6387e24cd471`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7324a222cd87f9984442beca25bd024156b320b7d2f241fb8c4d88bb0ae689`  
		Last Modified: Tue, 18 Feb 2025 22:29:45 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad1603e578869c6f56f970900a8b21ca4ad0d3e72120328fa44c532c99c8e0f`  
		Last Modified: Tue, 18 Feb 2025 22:29:45 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:97cef03bb306191acbb2337abf0524b3b1260cfd18fca9de48804e4ef1fa9a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38876960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b84758f0fdc3d7c8b2e0193f9a873eacce8cf357eb6af5c763faed6501baa22`

```dockerfile
```

-	Layers:
	-	`sha256:66dd1d1a7847b960b48ce081a71146ba7dcd00bc0429c5902ec12f5371c8b1a3`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 38.9 MB (38850242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb9fbd372d48cbd4f02682e25ba48999d96109f70000e70593be26a103fc5964`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e59b91ff9a4c8c31bf057b3765775ee0ad55b60ea41b77378de65a6e92df05da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.6 MB (579628882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c1ce42b244b7a0e6a8ab2d4af92bb0fc062220e3f6df98b35dd5a5a21cda45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=arm64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=16.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdff4be9ddc2ce9c0973f24556b70e5def80b93b12dde61c1dc183b17f401de`  
		Last Modified: Mon, 10 Feb 2025 19:59:08 GMT  
		Size: 216.9 MB (216922101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec6fc362eeeaba34f96d497d74afe7ab7fffac2131628c585688aa2d07a663`  
		Last Modified: Mon, 10 Feb 2025 19:59:03 GMT  
		Size: 2.6 MB (2583894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fe5dc7a8dce9250c384cb8e94b1ca2c03d4d916985761a4acc90f52b20f640`  
		Last Modified: Mon, 10 Feb 2025 19:59:03 GMT  
		Size: 485.0 KB (484976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c4cecc551d5bbd33325a4d18a3c646ab91a40ba0d66cd3d0fef29bea8d53fd`  
		Last Modified: Tue, 18 Feb 2025 22:38:08 GMT  
		Size: 330.9 MB (330890670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31ddf17426e4e0929444a63c2ffd2d5fee31547fa1715a5a14eb15281d0d3c1`  
		Last Modified: Tue, 18 Feb 2025 22:38:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04472d046fc9eb29d41f2024f84cae0cf577f8f55042173ff6fbc8b46b8f2459`  
		Last Modified: Tue, 18 Feb 2025 22:38:01 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166e6f8cc7d262971ec267719ea36e80c7874bdb8bac0a72f3c14c4115da5718`  
		Last Modified: Tue, 18 Feb 2025 22:38:01 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7905fc5d7504bd9e5b908f93947dbac57c45f4e9ae3a3042a86e6fd6929df8d2`  
		Last Modified: Tue, 18 Feb 2025 22:38:02 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:59fe35004bfd9bfd8d0f0c9fc03aa591612d9850ad4ed6d90b75f66fd3c6da53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38893808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef6f895233384299cfdb8805b2d8f39638cd8c842d60471117d4e2951fad0a2`

```dockerfile
```

-	Layers:
	-	`sha256:168673cadc8ebccf82801d430b0ab6fd138fd9d3343295c508c63631914f00b6`  
		Last Modified: Tue, 18 Feb 2025 22:38:02 GMT  
		Size: 38.9 MB (38866938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b5eb57431eacc5979951481c5e18338e3481aee43ad953eabdc08fd4a5913d`  
		Last Modified: Tue, 18 Feb 2025 22:38:00 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:be3d10a8c2c2e2d758d1ae5fa6862be95a29fd85c26750753d16bd6c1656610b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:a7528e39b58c7d447d997a2a04d8f10e769acae7900eea9f2db2b5be0f655b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.2 MB (584236762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49b0b8aeb4beabba4b814055fcf5f0d7b35d32758f70dbc8bd85f8b83f86ad9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=amd64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=16.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba69b5e1801d19c828d839d90f95c46fa492ef8da663dfbc469a6f51b7a1f86`  
		Last Modified: Tue, 18 Feb 2025 22:29:47 GMT  
		Size: 219.6 MB (219627811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8feded6f36b114dae0844894e55199f90bdc6bedb4314e108d2c4705fd9e18b1`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 2.6 MB (2624925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932bda97339913e7b8221673c983eb0f3076c226979dfe055b0b6a91e2129a1e`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 485.4 KB (485382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc0b2a45b3bcfd58d7938c2fbd9cccdf372bd7b48571b89da7a522294d716a`  
		Last Modified: Tue, 18 Feb 2025 22:29:48 GMT  
		Size: 331.2 MB (331243624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff126b44781c380134caae5bc811884b36f29fa4b1cfc692e99d428f58e6ae2`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43104cd286b2caa00dc9bce8fa135853a682e56cf86bcf0c6ded6387e24cd471`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7324a222cd87f9984442beca25bd024156b320b7d2f241fb8c4d88bb0ae689`  
		Last Modified: Tue, 18 Feb 2025 22:29:45 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad1603e578869c6f56f970900a8b21ca4ad0d3e72120328fa44c532c99c8e0f`  
		Last Modified: Tue, 18 Feb 2025 22:29:45 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:97cef03bb306191acbb2337abf0524b3b1260cfd18fca9de48804e4ef1fa9a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38876960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b84758f0fdc3d7c8b2e0193f9a873eacce8cf357eb6af5c763faed6501baa22`

```dockerfile
```

-	Layers:
	-	`sha256:66dd1d1a7847b960b48ce081a71146ba7dcd00bc0429c5902ec12f5371c8b1a3`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 38.9 MB (38850242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb9fbd372d48cbd4f02682e25ba48999d96109f70000e70593be26a103fc5964`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e59b91ff9a4c8c31bf057b3765775ee0ad55b60ea41b77378de65a6e92df05da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.6 MB (579628882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c1ce42b244b7a0e6a8ab2d4af92bb0fc062220e3f6df98b35dd5a5a21cda45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=arm64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=16.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdff4be9ddc2ce9c0973f24556b70e5def80b93b12dde61c1dc183b17f401de`  
		Last Modified: Mon, 10 Feb 2025 19:59:08 GMT  
		Size: 216.9 MB (216922101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec6fc362eeeaba34f96d497d74afe7ab7fffac2131628c585688aa2d07a663`  
		Last Modified: Mon, 10 Feb 2025 19:59:03 GMT  
		Size: 2.6 MB (2583894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fe5dc7a8dce9250c384cb8e94b1ca2c03d4d916985761a4acc90f52b20f640`  
		Last Modified: Mon, 10 Feb 2025 19:59:03 GMT  
		Size: 485.0 KB (484976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c4cecc551d5bbd33325a4d18a3c646ab91a40ba0d66cd3d0fef29bea8d53fd`  
		Last Modified: Tue, 18 Feb 2025 22:38:08 GMT  
		Size: 330.9 MB (330890670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31ddf17426e4e0929444a63c2ffd2d5fee31547fa1715a5a14eb15281d0d3c1`  
		Last Modified: Tue, 18 Feb 2025 22:38:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04472d046fc9eb29d41f2024f84cae0cf577f8f55042173ff6fbc8b46b8f2459`  
		Last Modified: Tue, 18 Feb 2025 22:38:01 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166e6f8cc7d262971ec267719ea36e80c7874bdb8bac0a72f3c14c4115da5718`  
		Last Modified: Tue, 18 Feb 2025 22:38:01 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7905fc5d7504bd9e5b908f93947dbac57c45f4e9ae3a3042a86e6fd6929df8d2`  
		Last Modified: Tue, 18 Feb 2025 22:38:02 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:59fe35004bfd9bfd8d0f0c9fc03aa591612d9850ad4ed6d90b75f66fd3c6da53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38893808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef6f895233384299cfdb8805b2d8f39638cd8c842d60471117d4e2951fad0a2`

```dockerfile
```

-	Layers:
	-	`sha256:168673cadc8ebccf82801d430b0ab6fd138fd9d3343295c508c63631914f00b6`  
		Last Modified: Tue, 18 Feb 2025 22:38:02 GMT  
		Size: 38.9 MB (38866938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b5eb57431eacc5979951481c5e18338e3481aee43ad953eabdc08fd4a5913d`  
		Last Modified: Tue, 18 Feb 2025 22:38:00 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250218`

```console
$ docker pull odoo@sha256:be3d10a8c2c2e2d758d1ae5fa6862be95a29fd85c26750753d16bd6c1656610b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250218` - linux; amd64

```console
$ docker pull odoo@sha256:a7528e39b58c7d447d997a2a04d8f10e769acae7900eea9f2db2b5be0f655b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.2 MB (584236762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49b0b8aeb4beabba4b814055fcf5f0d7b35d32758f70dbc8bd85f8b83f86ad9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=amd64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=16.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba69b5e1801d19c828d839d90f95c46fa492ef8da663dfbc469a6f51b7a1f86`  
		Last Modified: Tue, 18 Feb 2025 22:29:47 GMT  
		Size: 219.6 MB (219627811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8feded6f36b114dae0844894e55199f90bdc6bedb4314e108d2c4705fd9e18b1`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 2.6 MB (2624925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932bda97339913e7b8221673c983eb0f3076c226979dfe055b0b6a91e2129a1e`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 485.4 KB (485382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cc0b2a45b3bcfd58d7938c2fbd9cccdf372bd7b48571b89da7a522294d716a`  
		Last Modified: Tue, 18 Feb 2025 22:29:48 GMT  
		Size: 331.2 MB (331243624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff126b44781c380134caae5bc811884b36f29fa4b1cfc692e99d428f58e6ae2`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43104cd286b2caa00dc9bce8fa135853a682e56cf86bcf0c6ded6387e24cd471`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7324a222cd87f9984442beca25bd024156b320b7d2f241fb8c4d88bb0ae689`  
		Last Modified: Tue, 18 Feb 2025 22:29:45 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad1603e578869c6f56f970900a8b21ca4ad0d3e72120328fa44c532c99c8e0f`  
		Last Modified: Tue, 18 Feb 2025 22:29:45 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250218` - unknown; unknown

```console
$ docker pull odoo@sha256:97cef03bb306191acbb2337abf0524b3b1260cfd18fca9de48804e4ef1fa9a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38876960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b84758f0fdc3d7c8b2e0193f9a873eacce8cf357eb6af5c763faed6501baa22`

```dockerfile
```

-	Layers:
	-	`sha256:66dd1d1a7847b960b48ce081a71146ba7dcd00bc0429c5902ec12f5371c8b1a3`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 38.9 MB (38850242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb9fbd372d48cbd4f02682e25ba48999d96109f70000e70593be26a103fc5964`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250218` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e59b91ff9a4c8c31bf057b3765775ee0ad55b60ea41b77378de65a6e92df05da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.6 MB (579628882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c1ce42b244b7a0e6a8ab2d4af92bb0fc062220e3f6df98b35dd5a5a21cda45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=arm64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=16.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=b95e7c08cfdb8d0d25a2016cc5ef295e283da96b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdff4be9ddc2ce9c0973f24556b70e5def80b93b12dde61c1dc183b17f401de`  
		Last Modified: Mon, 10 Feb 2025 19:59:08 GMT  
		Size: 216.9 MB (216922101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ec6fc362eeeaba34f96d497d74afe7ab7fffac2131628c585688aa2d07a663`  
		Last Modified: Mon, 10 Feb 2025 19:59:03 GMT  
		Size: 2.6 MB (2583894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fe5dc7a8dce9250c384cb8e94b1ca2c03d4d916985761a4acc90f52b20f640`  
		Last Modified: Mon, 10 Feb 2025 19:59:03 GMT  
		Size: 485.0 KB (484976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c4cecc551d5bbd33325a4d18a3c646ab91a40ba0d66cd3d0fef29bea8d53fd`  
		Last Modified: Tue, 18 Feb 2025 22:38:08 GMT  
		Size: 330.9 MB (330890670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31ddf17426e4e0929444a63c2ffd2d5fee31547fa1715a5a14eb15281d0d3c1`  
		Last Modified: Tue, 18 Feb 2025 22:38:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04472d046fc9eb29d41f2024f84cae0cf577f8f55042173ff6fbc8b46b8f2459`  
		Last Modified: Tue, 18 Feb 2025 22:38:01 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166e6f8cc7d262971ec267719ea36e80c7874bdb8bac0a72f3c14c4115da5718`  
		Last Modified: Tue, 18 Feb 2025 22:38:01 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7905fc5d7504bd9e5b908f93947dbac57c45f4e9ae3a3042a86e6fd6929df8d2`  
		Last Modified: Tue, 18 Feb 2025 22:38:02 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250218` - unknown; unknown

```console
$ docker pull odoo@sha256:59fe35004bfd9bfd8d0f0c9fc03aa591612d9850ad4ed6d90b75f66fd3c6da53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38893808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef6f895233384299cfdb8805b2d8f39638cd8c842d60471117d4e2951fad0a2`

```dockerfile
```

-	Layers:
	-	`sha256:168673cadc8ebccf82801d430b0ab6fd138fd9d3343295c508c63631914f00b6`  
		Last Modified: Tue, 18 Feb 2025 22:38:02 GMT  
		Size: 38.9 MB (38866938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b5eb57431eacc5979951481c5e18338e3481aee43ad953eabdc08fd4a5913d`  
		Last Modified: Tue, 18 Feb 2025 22:38:00 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:531fe4fc0fb88597f2a28e4549567b344a4370be64ab12bb583a6c8959d0004b
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
$ docker pull odoo@sha256:5a62d754bf167e64ff9be99f3e5d1f7bcc995b9aae38ea053e0779ca6554e373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599997126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cd86ef2cb674ac5aa7fc70371238f77997875228fdeaaa3642092709bece7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=amd64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a5815a7a3144bf7b67d63738647f820982745ce43110cbfaedd6a98b3ec124`  
		Last Modified: Tue, 18 Feb 2025 22:30:18 GMT  
		Size: 233.8 MB (233767390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0f8ffffb1f6dbc733963a94433f43505409c088c4f35981aa92042ef68d2c5`  
		Last Modified: Tue, 18 Feb 2025 22:30:12 GMT  
		Size: 2.5 MB (2519883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42616622beb867079adf7620909cd0c4a35a7e50f8d75b8e600814806acb07e6`  
		Last Modified: Tue, 18 Feb 2025 22:30:11 GMT  
		Size: 486.3 KB (486322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e969b934456a7b7d19d483a783c4291235b788854a4abfbcc8d9982a830d4026`  
		Last Modified: Tue, 18 Feb 2025 22:30:18 GMT  
		Size: 333.7 MB (333685152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76160176b438d3ff2fca8e906898addde00c41b1c57fb804e55e4f8484dd4166`  
		Last Modified: Tue, 18 Feb 2025 22:30:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae8b7733374ac1353a9118a29744838fa9b83cb18fce35ffec16c09dc2f00ff`  
		Last Modified: Tue, 18 Feb 2025 22:30:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81509b0a9719ae5bf92671c804187a2a9da9f09eb49706937e2231c599495749`  
		Last Modified: Tue, 18 Feb 2025 22:30:14 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed44500ce14c1a6fa79e9f9db4f004faa54df7afdc794fa0486804426f0af6`  
		Last Modified: Tue, 18 Feb 2025 22:30:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:05055abc9d3c0265b1642999449f497c74553c5cb34e6fc49a5c1eceaf3e4254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39741143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bacc03a37f1898e5fe9a9fd0e36e5e1d2f57b357667d24f7d0c915fd6c0de528`

```dockerfile
```

-	Layers:
	-	`sha256:ab8510e106676ab892b0bce396b67f1c22ea0ff741251d8e89f75506bc7e4a28`  
		Last Modified: Tue, 18 Feb 2025 22:30:12 GMT  
		Size: 39.7 MB (39714308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f6bfb5d660eb3d801b1cb4af26696ab77b56989322ec64a6b04d3755971feb`  
		Last Modified: Tue, 18 Feb 2025 22:30:11 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c2ada45d2eb9c94047670744b9a667d5a79dc9a9230537de81edb141ffa36023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.8 MB (594788521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f2f48fb83321185e9b91f1892f6d946180fe8fbcbc439f61265eb2022caa09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=arm64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cd174319b3d49c009bb49f3781216969dfe5c7ac9bd0424821c5aba3c12c68`  
		Last Modified: Mon, 10 Feb 2025 19:55:23 GMT  
		Size: 231.2 MB (231161373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac50e3a0dfc9c3070305e2bc94d63f87bcb756c74e69f2821d9afa07c8b5a9`  
		Last Modified: Mon, 10 Feb 2025 19:55:17 GMT  
		Size: 2.5 MB (2485957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2861d19b53d55b76e3e17c50520c494841f59ad3653dc49bf4c1576074de3aa3`  
		Last Modified: Mon, 10 Feb 2025 19:55:17 GMT  
		Size: 486.0 KB (485957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33792066c1f4acdb18902138ea88ba5a4ee8fcffe7b9e45d10c2519db6268d95`  
		Last Modified: Tue, 18 Feb 2025 22:35:16 GMT  
		Size: 333.3 MB (333294615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9134179692325f446dd1daf85ee5499b0e1aab0fb1b09a4406dec78b42944dd`  
		Last Modified: Tue, 18 Feb 2025 22:35:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3866a2174bb9d3665a7cc38428463005249a8b4c4b9d72482a800ba2a1722a`  
		Last Modified: Tue, 18 Feb 2025 22:35:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587268541844c2fd7f88d8529dbc6457e4fcdf3d9d9a83786017f3c209a8a0f8`  
		Last Modified: Tue, 18 Feb 2025 22:35:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb07e15974d6c8687571897086ba8920cb4f0330b5ebf563c3a906588c860173`  
		Last Modified: Tue, 18 Feb 2025 22:35:09 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c1b1c3a1ea3f90b7d7e4155ce378e582d33477a62a6da83eaa498e5233da0e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39759280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2e957c4675fe63ddec3398de79c2d9e9609c223e9116553c6d56f52b2c0ee4`

```dockerfile
```

-	Layers:
	-	`sha256:b4e704616e090c0e9b3faa287cc09076c3902441e272127811daa367d5470524`  
		Last Modified: Tue, 18 Feb 2025 22:35:09 GMT  
		Size: 39.7 MB (39732294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a590757b94a47ff5501983cd798c658cf57ebe6ce277de794a273ac09c04bd`  
		Last Modified: Tue, 18 Feb 2025 22:35:08 GMT  
		Size: 27.0 KB (26986 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:17e172b2e493a9ebb494ebdf9e7b6b652ccc7c34ece70bfc17f2375cc35cc90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.4 MB (616449801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8309e47b1201ec16c4bcbf83dd7c0e2f4dfd753df3ebec4349079eab94e261af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=ppc64le
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98be366a421bba9a2f2eb85712d06dd803611984eece2cffdeea7c9f4baa2f2d`  
		Last Modified: Mon, 10 Feb 2025 19:44:54 GMT  
		Size: 243.3 MB (243286771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ea167816e99f042c18eaece41b176b2d95c32a2ef59146837650dc36cbb54b`  
		Last Modified: Mon, 10 Feb 2025 19:44:29 GMT  
		Size: 2.8 MB (2798267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b96a634db7dbb5e96d74e32260d7d4351a29e086452ffbefc92a1e99abac5a3`  
		Last Modified: Mon, 10 Feb 2025 19:44:29 GMT  
		Size: 486.0 KB (485991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c98c69cf2f4fd2266d9380501ff61559c9e20fe941dfcfd4f0b0b6b3b02ae3`  
		Last Modified: Tue, 18 Feb 2025 22:41:33 GMT  
		Size: 335.4 MB (335428402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0a9cded402d4140e292ea59d26792658ebb05a651a8d5d37f59d367ac4b755`  
		Last Modified: Tue, 18 Feb 2025 22:41:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b40355da666f87f97214c2a20464f2066dbf73b80481a4cf9fbc5488b0abb4c`  
		Last Modified: Tue, 18 Feb 2025 22:41:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1813aa5ee721903db198d9954cd1a57bbb10cdc3e342165ddc9f4688184b230`  
		Last Modified: Tue, 18 Feb 2025 22:41:11 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f8df739e3b1afc8222509fc2dd9b9cc914bc049a1636e1d46edea9121ddb2b`  
		Last Modified: Tue, 18 Feb 2025 22:41:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:4a2791bde63865230c79f0ad07db139137356b153be1e71473e189f87edbba64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39761001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457d0b7c5f23b96d8a473eb0dc5c24ec6933124ac8638f41eb83224198cec86e`

```dockerfile
```

-	Layers:
	-	`sha256:9281149f4a2b50a9868251b0a4b3538de3d7483c1f709bf3d536d8f6c84969b9`  
		Last Modified: Tue, 18 Feb 2025 22:41:13 GMT  
		Size: 39.7 MB (39734110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eabc6d36d3cbf5cb9bc21bf3f5c779276a173153792f47338651f72d2be9d55b`  
		Last Modified: Tue, 18 Feb 2025 22:41:11 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:531fe4fc0fb88597f2a28e4549567b344a4370be64ab12bb583a6c8959d0004b
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
$ docker pull odoo@sha256:5a62d754bf167e64ff9be99f3e5d1f7bcc995b9aae38ea053e0779ca6554e373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599997126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cd86ef2cb674ac5aa7fc70371238f77997875228fdeaaa3642092709bece7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=amd64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a5815a7a3144bf7b67d63738647f820982745ce43110cbfaedd6a98b3ec124`  
		Last Modified: Tue, 18 Feb 2025 22:30:18 GMT  
		Size: 233.8 MB (233767390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0f8ffffb1f6dbc733963a94433f43505409c088c4f35981aa92042ef68d2c5`  
		Last Modified: Tue, 18 Feb 2025 22:30:12 GMT  
		Size: 2.5 MB (2519883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42616622beb867079adf7620909cd0c4a35a7e50f8d75b8e600814806acb07e6`  
		Last Modified: Tue, 18 Feb 2025 22:30:11 GMT  
		Size: 486.3 KB (486322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e969b934456a7b7d19d483a783c4291235b788854a4abfbcc8d9982a830d4026`  
		Last Modified: Tue, 18 Feb 2025 22:30:18 GMT  
		Size: 333.7 MB (333685152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76160176b438d3ff2fca8e906898addde00c41b1c57fb804e55e4f8484dd4166`  
		Last Modified: Tue, 18 Feb 2025 22:30:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae8b7733374ac1353a9118a29744838fa9b83cb18fce35ffec16c09dc2f00ff`  
		Last Modified: Tue, 18 Feb 2025 22:30:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81509b0a9719ae5bf92671c804187a2a9da9f09eb49706937e2231c599495749`  
		Last Modified: Tue, 18 Feb 2025 22:30:14 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed44500ce14c1a6fa79e9f9db4f004faa54df7afdc794fa0486804426f0af6`  
		Last Modified: Tue, 18 Feb 2025 22:30:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:05055abc9d3c0265b1642999449f497c74553c5cb34e6fc49a5c1eceaf3e4254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39741143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bacc03a37f1898e5fe9a9fd0e36e5e1d2f57b357667d24f7d0c915fd6c0de528`

```dockerfile
```

-	Layers:
	-	`sha256:ab8510e106676ab892b0bce396b67f1c22ea0ff741251d8e89f75506bc7e4a28`  
		Last Modified: Tue, 18 Feb 2025 22:30:12 GMT  
		Size: 39.7 MB (39714308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f6bfb5d660eb3d801b1cb4af26696ab77b56989322ec64a6b04d3755971feb`  
		Last Modified: Tue, 18 Feb 2025 22:30:11 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c2ada45d2eb9c94047670744b9a667d5a79dc9a9230537de81edb141ffa36023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.8 MB (594788521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f2f48fb83321185e9b91f1892f6d946180fe8fbcbc439f61265eb2022caa09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=arm64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cd174319b3d49c009bb49f3781216969dfe5c7ac9bd0424821c5aba3c12c68`  
		Last Modified: Mon, 10 Feb 2025 19:55:23 GMT  
		Size: 231.2 MB (231161373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac50e3a0dfc9c3070305e2bc94d63f87bcb756c74e69f2821d9afa07c8b5a9`  
		Last Modified: Mon, 10 Feb 2025 19:55:17 GMT  
		Size: 2.5 MB (2485957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2861d19b53d55b76e3e17c50520c494841f59ad3653dc49bf4c1576074de3aa3`  
		Last Modified: Mon, 10 Feb 2025 19:55:17 GMT  
		Size: 486.0 KB (485957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33792066c1f4acdb18902138ea88ba5a4ee8fcffe7b9e45d10c2519db6268d95`  
		Last Modified: Tue, 18 Feb 2025 22:35:16 GMT  
		Size: 333.3 MB (333294615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9134179692325f446dd1daf85ee5499b0e1aab0fb1b09a4406dec78b42944dd`  
		Last Modified: Tue, 18 Feb 2025 22:35:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3866a2174bb9d3665a7cc38428463005249a8b4c4b9d72482a800ba2a1722a`  
		Last Modified: Tue, 18 Feb 2025 22:35:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587268541844c2fd7f88d8529dbc6457e4fcdf3d9d9a83786017f3c209a8a0f8`  
		Last Modified: Tue, 18 Feb 2025 22:35:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb07e15974d6c8687571897086ba8920cb4f0330b5ebf563c3a906588c860173`  
		Last Modified: Tue, 18 Feb 2025 22:35:09 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c1b1c3a1ea3f90b7d7e4155ce378e582d33477a62a6da83eaa498e5233da0e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39759280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2e957c4675fe63ddec3398de79c2d9e9609c223e9116553c6d56f52b2c0ee4`

```dockerfile
```

-	Layers:
	-	`sha256:b4e704616e090c0e9b3faa287cc09076c3902441e272127811daa367d5470524`  
		Last Modified: Tue, 18 Feb 2025 22:35:09 GMT  
		Size: 39.7 MB (39732294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a590757b94a47ff5501983cd798c658cf57ebe6ce277de794a273ac09c04bd`  
		Last Modified: Tue, 18 Feb 2025 22:35:08 GMT  
		Size: 27.0 KB (26986 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:17e172b2e493a9ebb494ebdf9e7b6b652ccc7c34ece70bfc17f2375cc35cc90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.4 MB (616449801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8309e47b1201ec16c4bcbf83dd7c0e2f4dfd753df3ebec4349079eab94e261af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=ppc64le
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98be366a421bba9a2f2eb85712d06dd803611984eece2cffdeea7c9f4baa2f2d`  
		Last Modified: Mon, 10 Feb 2025 19:44:54 GMT  
		Size: 243.3 MB (243286771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ea167816e99f042c18eaece41b176b2d95c32a2ef59146837650dc36cbb54b`  
		Last Modified: Mon, 10 Feb 2025 19:44:29 GMT  
		Size: 2.8 MB (2798267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b96a634db7dbb5e96d74e32260d7d4351a29e086452ffbefc92a1e99abac5a3`  
		Last Modified: Mon, 10 Feb 2025 19:44:29 GMT  
		Size: 486.0 KB (485991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c98c69cf2f4fd2266d9380501ff61559c9e20fe941dfcfd4f0b0b6b3b02ae3`  
		Last Modified: Tue, 18 Feb 2025 22:41:33 GMT  
		Size: 335.4 MB (335428402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0a9cded402d4140e292ea59d26792658ebb05a651a8d5d37f59d367ac4b755`  
		Last Modified: Tue, 18 Feb 2025 22:41:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b40355da666f87f97214c2a20464f2066dbf73b80481a4cf9fbc5488b0abb4c`  
		Last Modified: Tue, 18 Feb 2025 22:41:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1813aa5ee721903db198d9954cd1a57bbb10cdc3e342165ddc9f4688184b230`  
		Last Modified: Tue, 18 Feb 2025 22:41:11 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f8df739e3b1afc8222509fc2dd9b9cc914bc049a1636e1d46edea9121ddb2b`  
		Last Modified: Tue, 18 Feb 2025 22:41:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4a2791bde63865230c79f0ad07db139137356b153be1e71473e189f87edbba64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39761001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457d0b7c5f23b96d8a473eb0dc5c24ec6933124ac8638f41eb83224198cec86e`

```dockerfile
```

-	Layers:
	-	`sha256:9281149f4a2b50a9868251b0a4b3538de3d7483c1f709bf3d536d8f6c84969b9`  
		Last Modified: Tue, 18 Feb 2025 22:41:13 GMT  
		Size: 39.7 MB (39734110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eabc6d36d3cbf5cb9bc21bf3f5c779276a173153792f47338651f72d2be9d55b`  
		Last Modified: Tue, 18 Feb 2025 22:41:11 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250218`

```console
$ docker pull odoo@sha256:531fe4fc0fb88597f2a28e4549567b344a4370be64ab12bb583a6c8959d0004b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250218` - linux; amd64

```console
$ docker pull odoo@sha256:5a62d754bf167e64ff9be99f3e5d1f7bcc995b9aae38ea053e0779ca6554e373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (599997126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cd86ef2cb674ac5aa7fc70371238f77997875228fdeaaa3642092709bece7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=amd64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a5815a7a3144bf7b67d63738647f820982745ce43110cbfaedd6a98b3ec124`  
		Last Modified: Tue, 18 Feb 2025 22:30:18 GMT  
		Size: 233.8 MB (233767390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0f8ffffb1f6dbc733963a94433f43505409c088c4f35981aa92042ef68d2c5`  
		Last Modified: Tue, 18 Feb 2025 22:30:12 GMT  
		Size: 2.5 MB (2519883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42616622beb867079adf7620909cd0c4a35a7e50f8d75b8e600814806acb07e6`  
		Last Modified: Tue, 18 Feb 2025 22:30:11 GMT  
		Size: 486.3 KB (486322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e969b934456a7b7d19d483a783c4291235b788854a4abfbcc8d9982a830d4026`  
		Last Modified: Tue, 18 Feb 2025 22:30:18 GMT  
		Size: 333.7 MB (333685152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76160176b438d3ff2fca8e906898addde00c41b1c57fb804e55e4f8484dd4166`  
		Last Modified: Tue, 18 Feb 2025 22:30:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae8b7733374ac1353a9118a29744838fa9b83cb18fce35ffec16c09dc2f00ff`  
		Last Modified: Tue, 18 Feb 2025 22:30:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81509b0a9719ae5bf92671c804187a2a9da9f09eb49706937e2231c599495749`  
		Last Modified: Tue, 18 Feb 2025 22:30:14 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed44500ce14c1a6fa79e9f9db4f004faa54df7afdc794fa0486804426f0af6`  
		Last Modified: Tue, 18 Feb 2025 22:30:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250218` - unknown; unknown

```console
$ docker pull odoo@sha256:05055abc9d3c0265b1642999449f497c74553c5cb34e6fc49a5c1eceaf3e4254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39741143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bacc03a37f1898e5fe9a9fd0e36e5e1d2f57b357667d24f7d0c915fd6c0de528`

```dockerfile
```

-	Layers:
	-	`sha256:ab8510e106676ab892b0bce396b67f1c22ea0ff741251d8e89f75506bc7e4a28`  
		Last Modified: Tue, 18 Feb 2025 22:30:12 GMT  
		Size: 39.7 MB (39714308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f6bfb5d660eb3d801b1cb4af26696ab77b56989322ec64a6b04d3755971feb`  
		Last Modified: Tue, 18 Feb 2025 22:30:11 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250218` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c2ada45d2eb9c94047670744b9a667d5a79dc9a9230537de81edb141ffa36023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.8 MB (594788521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f2f48fb83321185e9b91f1892f6d946180fe8fbcbc439f61265eb2022caa09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=arm64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cd174319b3d49c009bb49f3781216969dfe5c7ac9bd0424821c5aba3c12c68`  
		Last Modified: Mon, 10 Feb 2025 19:55:23 GMT  
		Size: 231.2 MB (231161373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac50e3a0dfc9c3070305e2bc94d63f87bcb756c74e69f2821d9afa07c8b5a9`  
		Last Modified: Mon, 10 Feb 2025 19:55:17 GMT  
		Size: 2.5 MB (2485957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2861d19b53d55b76e3e17c50520c494841f59ad3653dc49bf4c1576074de3aa3`  
		Last Modified: Mon, 10 Feb 2025 19:55:17 GMT  
		Size: 486.0 KB (485957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33792066c1f4acdb18902138ea88ba5a4ee8fcffe7b9e45d10c2519db6268d95`  
		Last Modified: Tue, 18 Feb 2025 22:35:16 GMT  
		Size: 333.3 MB (333294615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9134179692325f446dd1daf85ee5499b0e1aab0fb1b09a4406dec78b42944dd`  
		Last Modified: Tue, 18 Feb 2025 22:35:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3866a2174bb9d3665a7cc38428463005249a8b4c4b9d72482a800ba2a1722a`  
		Last Modified: Tue, 18 Feb 2025 22:35:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587268541844c2fd7f88d8529dbc6457e4fcdf3d9d9a83786017f3c209a8a0f8`  
		Last Modified: Tue, 18 Feb 2025 22:35:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb07e15974d6c8687571897086ba8920cb4f0330b5ebf563c3a906588c860173`  
		Last Modified: Tue, 18 Feb 2025 22:35:09 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250218` - unknown; unknown

```console
$ docker pull odoo@sha256:c1b1c3a1ea3f90b7d7e4155ce378e582d33477a62a6da83eaa498e5233da0e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39759280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2e957c4675fe63ddec3398de79c2d9e9609c223e9116553c6d56f52b2c0ee4`

```dockerfile
```

-	Layers:
	-	`sha256:b4e704616e090c0e9b3faa287cc09076c3902441e272127811daa367d5470524`  
		Last Modified: Tue, 18 Feb 2025 22:35:09 GMT  
		Size: 39.7 MB (39732294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a590757b94a47ff5501983cd798c658cf57ebe6ce277de794a273ac09c04bd`  
		Last Modified: Tue, 18 Feb 2025 22:35:08 GMT  
		Size: 27.0 KB (26986 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250218` - linux; ppc64le

```console
$ docker pull odoo@sha256:17e172b2e493a9ebb494ebdf9e7b6b652ccc7c34ece70bfc17f2375cc35cc90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.4 MB (616449801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8309e47b1201ec16c4bcbf83dd7c0e2f4dfd753df3ebec4349079eab94e261af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=ppc64le
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=17.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=89289fe99db80d02fdabeb2fa63164f5c0464c43
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98be366a421bba9a2f2eb85712d06dd803611984eece2cffdeea7c9f4baa2f2d`  
		Last Modified: Mon, 10 Feb 2025 19:44:54 GMT  
		Size: 243.3 MB (243286771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ea167816e99f042c18eaece41b176b2d95c32a2ef59146837650dc36cbb54b`  
		Last Modified: Mon, 10 Feb 2025 19:44:29 GMT  
		Size: 2.8 MB (2798267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b96a634db7dbb5e96d74e32260d7d4351a29e086452ffbefc92a1e99abac5a3`  
		Last Modified: Mon, 10 Feb 2025 19:44:29 GMT  
		Size: 486.0 KB (485991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c98c69cf2f4fd2266d9380501ff61559c9e20fe941dfcfd4f0b0b6b3b02ae3`  
		Last Modified: Tue, 18 Feb 2025 22:41:33 GMT  
		Size: 335.4 MB (335428402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0a9cded402d4140e292ea59d26792658ebb05a651a8d5d37f59d367ac4b755`  
		Last Modified: Tue, 18 Feb 2025 22:41:11 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b40355da666f87f97214c2a20464f2066dbf73b80481a4cf9fbc5488b0abb4c`  
		Last Modified: Tue, 18 Feb 2025 22:41:11 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1813aa5ee721903db198d9954cd1a57bbb10cdc3e342165ddc9f4688184b230`  
		Last Modified: Tue, 18 Feb 2025 22:41:11 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f8df739e3b1afc8222509fc2dd9b9cc914bc049a1636e1d46edea9121ddb2b`  
		Last Modified: Tue, 18 Feb 2025 22:41:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250218` - unknown; unknown

```console
$ docker pull odoo@sha256:4a2791bde63865230c79f0ad07db139137356b153be1e71473e189f87edbba64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39761001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457d0b7c5f23b96d8a473eb0dc5c24ec6933124ac8638f41eb83224198cec86e`

```dockerfile
```

-	Layers:
	-	`sha256:9281149f4a2b50a9868251b0a4b3538de3d7483c1f709bf3d536d8f6c84969b9`  
		Last Modified: Tue, 18 Feb 2025 22:41:13 GMT  
		Size: 39.7 MB (39734110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eabc6d36d3cbf5cb9bc21bf3f5c779276a173153792f47338651f72d2be9d55b`  
		Last Modified: Tue, 18 Feb 2025 22:41:11 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:5ae9cc3b8fabe0082c33d13dbc6447246f82f239531fa284aca13c5df29073f1
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
$ docker pull odoo@sha256:81572f0f17dfe5b36336e107ff310c192d41ef75785a5dbf0893c49c9d13b544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.1 MB (670058434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dc8784c617326a6379c4fcdf36be3828029ef58a05bd2d5d8edf68b80f657b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=amd64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=18.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb504ee8ee6d41eb94a4cd7da0039a9f1a5fd579ca509b22003278269f4b489`  
		Last Modified: Tue, 18 Feb 2025 22:31:13 GMT  
		Size: 254.5 MB (254514296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf33a98a9bb99569e58d122799b525113922c9559abb198b74cdbb8263386e0`  
		Last Modified: Tue, 18 Feb 2025 22:31:08 GMT  
		Size: 16.7 MB (16678119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b38518b3a453b907131ca33f58b46e67d18e1e41cc0044b5f107044bf4f5a`  
		Last Modified: Tue, 18 Feb 2025 22:31:07 GMT  
		Size: 486.1 KB (486075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875b50acdf3a1501f794a2461d4207f77a7c9a5b16cadf21ff279643247f4a02`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 368.6 MB (368623214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6050296f2359e22fd6662b2c4788ad3e36908fb984099b6d96433843d0fa75f0`  
		Last Modified: Tue, 18 Feb 2025 22:31:08 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85180e70fc660f66f813bca28a1fdb775f596cb26b85220c8d7e7d6766478e53`  
		Last Modified: Tue, 18 Feb 2025 22:31:09 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82649552273dfeb1376eecd2b3320319cd5e9a9d96775f4a0bf4d5a729d07a5e`  
		Last Modified: Tue, 18 Feb 2025 22:31:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e72d05e56d93c9fb355080d045ed84204b8395182c93a987fc717471f4656e`  
		Last Modified: Tue, 18 Feb 2025 22:31:10 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:e3aa6a44f3785e4ebb08ff1d3d6423f5e1ebf3dec0ec871fc1b15a2022ecac74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58718313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc930de66c3b5c04aa67865efb8d59d2d050758013b2599e06c6817eab061e5`

```dockerfile
```

-	Layers:
	-	`sha256:55c8f638ca7dcd7fa7a3da5b787b7719d2da79af14a361bfa17cffd0b1270398`  
		Last Modified: Tue, 18 Feb 2025 22:31:09 GMT  
		Size: 58.7 MB (58691177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6564ba4c2a28ca46f87ba3ada45142e59e1e262b28f2101ff42f41e144aea30`  
		Last Modified: Tue, 18 Feb 2025 22:31:07 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a4a75ffaf1ed746005dfa14681e8b4a5e1d51740c9c21061ca4c08dbdd74a028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.3 MB (666349026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e796b2f183057280c1f317797ed6392fdb87f4f3e7b7395b8ddc76349230ee25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=arm64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=18.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4423ae3417994b02e28e725cf3fc1fbb074aba9d094ffeb5dbce79bb54e0f8b`  
		Last Modified: Mon, 10 Feb 2025 19:48:48 GMT  
		Size: 251.9 MB (251943363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1572c494925a5dc1301929c70510c4fddbc44dc821e6c485bf3c660b9332bc39`  
		Last Modified: Mon, 10 Feb 2025 19:48:44 GMT  
		Size: 16.6 MB (16581015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bba4c4196ec9c1a655094047ad1675b7e3cce5bd2735fe164bd0586d2471128`  
		Last Modified: Mon, 10 Feb 2025 19:48:43 GMT  
		Size: 485.7 KB (485723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea2da15dfb1b65f5d16bf113932773d6501130ec57ee26418df6f58d6414130`  
		Last Modified: Tue, 18 Feb 2025 22:31:25 GMT  
		Size: 368.4 MB (368442889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff126b44781c380134caae5bc811884b36f29fa4b1cfc692e99d428f58e6ae2`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15d364fe3877a1319effead720299d7f17b7909a4fb134917ed26c39fa8956b`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf53425a6182560cf31878a94832e9120747c21b9bbf9f5d3696d71821d2573`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee94a7c29e4110e1fab1d1ea992219ec7a96606add7b498de2da5c42de52d1c`  
		Last Modified: Tue, 18 Feb 2025 22:31:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:c1de4ce0bef5a40a4fa940806954a54f330282294471eecce390003a446cac77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58737247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0649741eceaa8a4a5df26513c9887cd8bf9bd099fecf4d1f4a3cd46ca0b83582`

```dockerfile
```

-	Layers:
	-	`sha256:9c0be2f77d0765010d0b48894cb08da7f4e4b7b5921dd86473e5a0c073c48989`  
		Last Modified: Tue, 18 Feb 2025 22:31:20 GMT  
		Size: 58.7 MB (58709947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e979aeebc5def7610beb6169d47ac4ade323c5177583facbdc16e6cf226481`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:ac47ac91c143801e346d688ad5b946688e37972014afb9e04eb27cbd787953c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.4 MB (686426161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd8746f4ace16dbaee6fa2ef9dc49b9e343deb111602f542b8218309eb36023`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=ppc64le
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=18.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8455c54b495abb021f3ea0c5c47e4cc801d26c3f5b4f623f88a5ba88b4181458`  
		Last Modified: Mon, 10 Feb 2025 20:17:37 GMT  
		Size: 265.1 MB (265074206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0aa37e025c7ccd816c72a6cf91884a71817e56a69b066240616f7a2ae1537`  
		Last Modified: Mon, 10 Feb 2025 20:17:28 GMT  
		Size: 17.3 MB (17306456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a84f231b270cb999af35933efb7b7de7e00f97622369b26ac2dc6fec5558d7`  
		Last Modified: Mon, 10 Feb 2025 20:17:27 GMT  
		Size: 485.7 KB (485744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3185ddcb346c58a9c9458eb3aae9cbc151f162d9175e091bc728faf906b38881`  
		Last Modified: Tue, 18 Feb 2025 22:35:17 GMT  
		Size: 369.2 MB (369167487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c38c3550276428ae82c87d9a0198fea0bbe85a08e4dc8752f83b8668b38631a`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecbc3738e9209c1614330b9673d8424c1977410806c471699c2d337b046c8d3`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55c35b7c8f906d668e862bb346e25793451308081aded2bd5357929195ce56e`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9f2842375ea32a28d4b42604178f888325d669617de548fa5f4d055b082fe`  
		Last Modified: Tue, 18 Feb 2025 22:34:50 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:58db09feab7f74139006efc8a7671c951c6b73abe597beedad81beaf6691fe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58738017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e25c6b1790aa11b8513075bf8b1759e4978d214f02077ecbd07a8d1794b5ef`

```dockerfile
```

-	Layers:
	-	`sha256:17bb7f85ac41b157cd10780fbd87a59ec10945dc557243df4f1906f2b71861b0`  
		Last Modified: Tue, 18 Feb 2025 22:34:51 GMT  
		Size: 58.7 MB (58710819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e891c78d247fda1363a6e6408b8b6dda03e28bf8c010dc9f036c8e2d6e27d12`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:5ae9cc3b8fabe0082c33d13dbc6447246f82f239531fa284aca13c5df29073f1
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
$ docker pull odoo@sha256:81572f0f17dfe5b36336e107ff310c192d41ef75785a5dbf0893c49c9d13b544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.1 MB (670058434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dc8784c617326a6379c4fcdf36be3828029ef58a05bd2d5d8edf68b80f657b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=amd64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=18.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb504ee8ee6d41eb94a4cd7da0039a9f1a5fd579ca509b22003278269f4b489`  
		Last Modified: Tue, 18 Feb 2025 22:31:13 GMT  
		Size: 254.5 MB (254514296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf33a98a9bb99569e58d122799b525113922c9559abb198b74cdbb8263386e0`  
		Last Modified: Tue, 18 Feb 2025 22:31:08 GMT  
		Size: 16.7 MB (16678119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b38518b3a453b907131ca33f58b46e67d18e1e41cc0044b5f107044bf4f5a`  
		Last Modified: Tue, 18 Feb 2025 22:31:07 GMT  
		Size: 486.1 KB (486075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875b50acdf3a1501f794a2461d4207f77a7c9a5b16cadf21ff279643247f4a02`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 368.6 MB (368623214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6050296f2359e22fd6662b2c4788ad3e36908fb984099b6d96433843d0fa75f0`  
		Last Modified: Tue, 18 Feb 2025 22:31:08 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85180e70fc660f66f813bca28a1fdb775f596cb26b85220c8d7e7d6766478e53`  
		Last Modified: Tue, 18 Feb 2025 22:31:09 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82649552273dfeb1376eecd2b3320319cd5e9a9d96775f4a0bf4d5a729d07a5e`  
		Last Modified: Tue, 18 Feb 2025 22:31:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e72d05e56d93c9fb355080d045ed84204b8395182c93a987fc717471f4656e`  
		Last Modified: Tue, 18 Feb 2025 22:31:10 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e3aa6a44f3785e4ebb08ff1d3d6423f5e1ebf3dec0ec871fc1b15a2022ecac74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58718313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc930de66c3b5c04aa67865efb8d59d2d050758013b2599e06c6817eab061e5`

```dockerfile
```

-	Layers:
	-	`sha256:55c8f638ca7dcd7fa7a3da5b787b7719d2da79af14a361bfa17cffd0b1270398`  
		Last Modified: Tue, 18 Feb 2025 22:31:09 GMT  
		Size: 58.7 MB (58691177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6564ba4c2a28ca46f87ba3ada45142e59e1e262b28f2101ff42f41e144aea30`  
		Last Modified: Tue, 18 Feb 2025 22:31:07 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a4a75ffaf1ed746005dfa14681e8b4a5e1d51740c9c21061ca4c08dbdd74a028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.3 MB (666349026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e796b2f183057280c1f317797ed6392fdb87f4f3e7b7395b8ddc76349230ee25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=arm64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=18.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4423ae3417994b02e28e725cf3fc1fbb074aba9d094ffeb5dbce79bb54e0f8b`  
		Last Modified: Mon, 10 Feb 2025 19:48:48 GMT  
		Size: 251.9 MB (251943363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1572c494925a5dc1301929c70510c4fddbc44dc821e6c485bf3c660b9332bc39`  
		Last Modified: Mon, 10 Feb 2025 19:48:44 GMT  
		Size: 16.6 MB (16581015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bba4c4196ec9c1a655094047ad1675b7e3cce5bd2735fe164bd0586d2471128`  
		Last Modified: Mon, 10 Feb 2025 19:48:43 GMT  
		Size: 485.7 KB (485723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea2da15dfb1b65f5d16bf113932773d6501130ec57ee26418df6f58d6414130`  
		Last Modified: Tue, 18 Feb 2025 22:31:25 GMT  
		Size: 368.4 MB (368442889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff126b44781c380134caae5bc811884b36f29fa4b1cfc692e99d428f58e6ae2`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15d364fe3877a1319effead720299d7f17b7909a4fb134917ed26c39fa8956b`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf53425a6182560cf31878a94832e9120747c21b9bbf9f5d3696d71821d2573`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee94a7c29e4110e1fab1d1ea992219ec7a96606add7b498de2da5c42de52d1c`  
		Last Modified: Tue, 18 Feb 2025 22:31:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c1de4ce0bef5a40a4fa940806954a54f330282294471eecce390003a446cac77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58737247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0649741eceaa8a4a5df26513c9887cd8bf9bd099fecf4d1f4a3cd46ca0b83582`

```dockerfile
```

-	Layers:
	-	`sha256:9c0be2f77d0765010d0b48894cb08da7f4e4b7b5921dd86473e5a0c073c48989`  
		Last Modified: Tue, 18 Feb 2025 22:31:20 GMT  
		Size: 58.7 MB (58709947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e979aeebc5def7610beb6169d47ac4ade323c5177583facbdc16e6cf226481`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:ac47ac91c143801e346d688ad5b946688e37972014afb9e04eb27cbd787953c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.4 MB (686426161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd8746f4ace16dbaee6fa2ef9dc49b9e343deb111602f542b8218309eb36023`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=ppc64le
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=18.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8455c54b495abb021f3ea0c5c47e4cc801d26c3f5b4f623f88a5ba88b4181458`  
		Last Modified: Mon, 10 Feb 2025 20:17:37 GMT  
		Size: 265.1 MB (265074206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0aa37e025c7ccd816c72a6cf91884a71817e56a69b066240616f7a2ae1537`  
		Last Modified: Mon, 10 Feb 2025 20:17:28 GMT  
		Size: 17.3 MB (17306456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a84f231b270cb999af35933efb7b7de7e00f97622369b26ac2dc6fec5558d7`  
		Last Modified: Mon, 10 Feb 2025 20:17:27 GMT  
		Size: 485.7 KB (485744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3185ddcb346c58a9c9458eb3aae9cbc151f162d9175e091bc728faf906b38881`  
		Last Modified: Tue, 18 Feb 2025 22:35:17 GMT  
		Size: 369.2 MB (369167487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c38c3550276428ae82c87d9a0198fea0bbe85a08e4dc8752f83b8668b38631a`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecbc3738e9209c1614330b9673d8424c1977410806c471699c2d337b046c8d3`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55c35b7c8f906d668e862bb346e25793451308081aded2bd5357929195ce56e`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9f2842375ea32a28d4b42604178f888325d669617de548fa5f4d055b082fe`  
		Last Modified: Tue, 18 Feb 2025 22:34:50 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:58db09feab7f74139006efc8a7671c951c6b73abe597beedad81beaf6691fe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58738017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e25c6b1790aa11b8513075bf8b1759e4978d214f02077ecbd07a8d1794b5ef`

```dockerfile
```

-	Layers:
	-	`sha256:17bb7f85ac41b157cd10780fbd87a59ec10945dc557243df4f1906f2b71861b0`  
		Last Modified: Tue, 18 Feb 2025 22:34:51 GMT  
		Size: 58.7 MB (58710819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e891c78d247fda1363a6e6408b8b6dda03e28bf8c010dc9f036c8e2d6e27d12`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250218`

```console
$ docker pull odoo@sha256:5ae9cc3b8fabe0082c33d13dbc6447246f82f239531fa284aca13c5df29073f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250218` - linux; amd64

```console
$ docker pull odoo@sha256:81572f0f17dfe5b36336e107ff310c192d41ef75785a5dbf0893c49c9d13b544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.1 MB (670058434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dc8784c617326a6379c4fcdf36be3828029ef58a05bd2d5d8edf68b80f657b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=amd64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=18.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb504ee8ee6d41eb94a4cd7da0039a9f1a5fd579ca509b22003278269f4b489`  
		Last Modified: Tue, 18 Feb 2025 22:31:13 GMT  
		Size: 254.5 MB (254514296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf33a98a9bb99569e58d122799b525113922c9559abb198b74cdbb8263386e0`  
		Last Modified: Tue, 18 Feb 2025 22:31:08 GMT  
		Size: 16.7 MB (16678119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b38518b3a453b907131ca33f58b46e67d18e1e41cc0044b5f107044bf4f5a`  
		Last Modified: Tue, 18 Feb 2025 22:31:07 GMT  
		Size: 486.1 KB (486075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875b50acdf3a1501f794a2461d4207f77a7c9a5b16cadf21ff279643247f4a02`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 368.6 MB (368623214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6050296f2359e22fd6662b2c4788ad3e36908fb984099b6d96433843d0fa75f0`  
		Last Modified: Tue, 18 Feb 2025 22:31:08 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85180e70fc660f66f813bca28a1fdb775f596cb26b85220c8d7e7d6766478e53`  
		Last Modified: Tue, 18 Feb 2025 22:31:09 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82649552273dfeb1376eecd2b3320319cd5e9a9d96775f4a0bf4d5a729d07a5e`  
		Last Modified: Tue, 18 Feb 2025 22:31:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e72d05e56d93c9fb355080d045ed84204b8395182c93a987fc717471f4656e`  
		Last Modified: Tue, 18 Feb 2025 22:31:10 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250218` - unknown; unknown

```console
$ docker pull odoo@sha256:e3aa6a44f3785e4ebb08ff1d3d6423f5e1ebf3dec0ec871fc1b15a2022ecac74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58718313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc930de66c3b5c04aa67865efb8d59d2d050758013b2599e06c6817eab061e5`

```dockerfile
```

-	Layers:
	-	`sha256:55c8f638ca7dcd7fa7a3da5b787b7719d2da79af14a361bfa17cffd0b1270398`  
		Last Modified: Tue, 18 Feb 2025 22:31:09 GMT  
		Size: 58.7 MB (58691177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6564ba4c2a28ca46f87ba3ada45142e59e1e262b28f2101ff42f41e144aea30`  
		Last Modified: Tue, 18 Feb 2025 22:31:07 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250218` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a4a75ffaf1ed746005dfa14681e8b4a5e1d51740c9c21061ca4c08dbdd74a028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.3 MB (666349026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e796b2f183057280c1f317797ed6392fdb87f4f3e7b7395b8ddc76349230ee25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=arm64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=18.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4423ae3417994b02e28e725cf3fc1fbb074aba9d094ffeb5dbce79bb54e0f8b`  
		Last Modified: Mon, 10 Feb 2025 19:48:48 GMT  
		Size: 251.9 MB (251943363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1572c494925a5dc1301929c70510c4fddbc44dc821e6c485bf3c660b9332bc39`  
		Last Modified: Mon, 10 Feb 2025 19:48:44 GMT  
		Size: 16.6 MB (16581015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bba4c4196ec9c1a655094047ad1675b7e3cce5bd2735fe164bd0586d2471128`  
		Last Modified: Mon, 10 Feb 2025 19:48:43 GMT  
		Size: 485.7 KB (485723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea2da15dfb1b65f5d16bf113932773d6501130ec57ee26418df6f58d6414130`  
		Last Modified: Tue, 18 Feb 2025 22:31:25 GMT  
		Size: 368.4 MB (368442889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff126b44781c380134caae5bc811884b36f29fa4b1cfc692e99d428f58e6ae2`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15d364fe3877a1319effead720299d7f17b7909a4fb134917ed26c39fa8956b`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf53425a6182560cf31878a94832e9120747c21b9bbf9f5d3696d71821d2573`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee94a7c29e4110e1fab1d1ea992219ec7a96606add7b498de2da5c42de52d1c`  
		Last Modified: Tue, 18 Feb 2025 22:31:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250218` - unknown; unknown

```console
$ docker pull odoo@sha256:c1de4ce0bef5a40a4fa940806954a54f330282294471eecce390003a446cac77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58737247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0649741eceaa8a4a5df26513c9887cd8bf9bd099fecf4d1f4a3cd46ca0b83582`

```dockerfile
```

-	Layers:
	-	`sha256:9c0be2f77d0765010d0b48894cb08da7f4e4b7b5921dd86473e5a0c073c48989`  
		Last Modified: Tue, 18 Feb 2025 22:31:20 GMT  
		Size: 58.7 MB (58709947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e979aeebc5def7610beb6169d47ac4ade323c5177583facbdc16e6cf226481`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250218` - linux; ppc64le

```console
$ docker pull odoo@sha256:ac47ac91c143801e346d688ad5b946688e37972014afb9e04eb27cbd787953c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.4 MB (686426161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd8746f4ace16dbaee6fa2ef9dc49b9e343deb111602f542b8218309eb36023`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=ppc64le
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=18.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8455c54b495abb021f3ea0c5c47e4cc801d26c3f5b4f623f88a5ba88b4181458`  
		Last Modified: Mon, 10 Feb 2025 20:17:37 GMT  
		Size: 265.1 MB (265074206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0aa37e025c7ccd816c72a6cf91884a71817e56a69b066240616f7a2ae1537`  
		Last Modified: Mon, 10 Feb 2025 20:17:28 GMT  
		Size: 17.3 MB (17306456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a84f231b270cb999af35933efb7b7de7e00f97622369b26ac2dc6fec5558d7`  
		Last Modified: Mon, 10 Feb 2025 20:17:27 GMT  
		Size: 485.7 KB (485744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3185ddcb346c58a9c9458eb3aae9cbc151f162d9175e091bc728faf906b38881`  
		Last Modified: Tue, 18 Feb 2025 22:35:17 GMT  
		Size: 369.2 MB (369167487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c38c3550276428ae82c87d9a0198fea0bbe85a08e4dc8752f83b8668b38631a`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecbc3738e9209c1614330b9673d8424c1977410806c471699c2d337b046c8d3`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55c35b7c8f906d668e862bb346e25793451308081aded2bd5357929195ce56e`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9f2842375ea32a28d4b42604178f888325d669617de548fa5f4d055b082fe`  
		Last Modified: Tue, 18 Feb 2025 22:34:50 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250218` - unknown; unknown

```console
$ docker pull odoo@sha256:58db09feab7f74139006efc8a7671c951c6b73abe597beedad81beaf6691fe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58738017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e25c6b1790aa11b8513075bf8b1759e4978d214f02077ecbd07a8d1794b5ef`

```dockerfile
```

-	Layers:
	-	`sha256:17bb7f85ac41b157cd10780fbd87a59ec10945dc557243df4f1906f2b71861b0`  
		Last Modified: Tue, 18 Feb 2025 22:34:51 GMT  
		Size: 58.7 MB (58710819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e891c78d247fda1363a6e6408b8b6dda03e28bf8c010dc9f036c8e2d6e27d12`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:5ae9cc3b8fabe0082c33d13dbc6447246f82f239531fa284aca13c5df29073f1
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
$ docker pull odoo@sha256:81572f0f17dfe5b36336e107ff310c192d41ef75785a5dbf0893c49c9d13b544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.1 MB (670058434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dc8784c617326a6379c4fcdf36be3828029ef58a05bd2d5d8edf68b80f657b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=amd64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=18.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb504ee8ee6d41eb94a4cd7da0039a9f1a5fd579ca509b22003278269f4b489`  
		Last Modified: Tue, 18 Feb 2025 22:31:13 GMT  
		Size: 254.5 MB (254514296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf33a98a9bb99569e58d122799b525113922c9559abb198b74cdbb8263386e0`  
		Last Modified: Tue, 18 Feb 2025 22:31:08 GMT  
		Size: 16.7 MB (16678119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720b38518b3a453b907131ca33f58b46e67d18e1e41cc0044b5f107044bf4f5a`  
		Last Modified: Tue, 18 Feb 2025 22:31:07 GMT  
		Size: 486.1 KB (486075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875b50acdf3a1501f794a2461d4207f77a7c9a5b16cadf21ff279643247f4a02`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 368.6 MB (368623214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6050296f2359e22fd6662b2c4788ad3e36908fb984099b6d96433843d0fa75f0`  
		Last Modified: Tue, 18 Feb 2025 22:31:08 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85180e70fc660f66f813bca28a1fdb775f596cb26b85220c8d7e7d6766478e53`  
		Last Modified: Tue, 18 Feb 2025 22:31:09 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82649552273dfeb1376eecd2b3320319cd5e9a9d96775f4a0bf4d5a729d07a5e`  
		Last Modified: Tue, 18 Feb 2025 22:31:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e72d05e56d93c9fb355080d045ed84204b8395182c93a987fc717471f4656e`  
		Last Modified: Tue, 18 Feb 2025 22:31:10 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:e3aa6a44f3785e4ebb08ff1d3d6423f5e1ebf3dec0ec871fc1b15a2022ecac74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58718313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc930de66c3b5c04aa67865efb8d59d2d050758013b2599e06c6817eab061e5`

```dockerfile
```

-	Layers:
	-	`sha256:55c8f638ca7dcd7fa7a3da5b787b7719d2da79af14a361bfa17cffd0b1270398`  
		Last Modified: Tue, 18 Feb 2025 22:31:09 GMT  
		Size: 58.7 MB (58691177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6564ba4c2a28ca46f87ba3ada45142e59e1e262b28f2101ff42f41e144aea30`  
		Last Modified: Tue, 18 Feb 2025 22:31:07 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a4a75ffaf1ed746005dfa14681e8b4a5e1d51740c9c21061ca4c08dbdd74a028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.3 MB (666349026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e796b2f183057280c1f317797ed6392fdb87f4f3e7b7395b8ddc76349230ee25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=arm64
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=18.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4423ae3417994b02e28e725cf3fc1fbb074aba9d094ffeb5dbce79bb54e0f8b`  
		Last Modified: Mon, 10 Feb 2025 19:48:48 GMT  
		Size: 251.9 MB (251943363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1572c494925a5dc1301929c70510c4fddbc44dc821e6c485bf3c660b9332bc39`  
		Last Modified: Mon, 10 Feb 2025 19:48:44 GMT  
		Size: 16.6 MB (16581015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bba4c4196ec9c1a655094047ad1675b7e3cce5bd2735fe164bd0586d2471128`  
		Last Modified: Mon, 10 Feb 2025 19:48:43 GMT  
		Size: 485.7 KB (485723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea2da15dfb1b65f5d16bf113932773d6501130ec57ee26418df6f58d6414130`  
		Last Modified: Tue, 18 Feb 2025 22:31:25 GMT  
		Size: 368.4 MB (368442889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff126b44781c380134caae5bc811884b36f29fa4b1cfc692e99d428f58e6ae2`  
		Last Modified: Tue, 18 Feb 2025 22:29:44 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15d364fe3877a1319effead720299d7f17b7909a4fb134917ed26c39fa8956b`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf53425a6182560cf31878a94832e9120747c21b9bbf9f5d3696d71821d2573`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee94a7c29e4110e1fab1d1ea992219ec7a96606add7b498de2da5c42de52d1c`  
		Last Modified: Tue, 18 Feb 2025 22:31:19 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c1de4ce0bef5a40a4fa940806954a54f330282294471eecce390003a446cac77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58737247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0649741eceaa8a4a5df26513c9887cd8bf9bd099fecf4d1f4a3cd46ca0b83582`

```dockerfile
```

-	Layers:
	-	`sha256:9c0be2f77d0765010d0b48894cb08da7f4e4b7b5921dd86473e5a0c073c48989`  
		Last Modified: Tue, 18 Feb 2025 22:31:20 GMT  
		Size: 58.7 MB (58709947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e979aeebc5def7610beb6169d47ac4ade323c5177583facbdc16e6cf226481`  
		Last Modified: Tue, 18 Feb 2025 22:31:18 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:ac47ac91c143801e346d688ad5b946688e37972014afb9e04eb27cbd787953c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.4 MB (686426161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd8746f4ace16dbaee6fa2ef9dc49b9e343deb111602f542b8218309eb36023`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Tue, 18 Feb 2025 08:26:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 18 Feb 2025 08:26:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Feb 2025 08:26:12 GMT
ARG TARGETARCH=ppc64le
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_VERSION=18.0
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_RELEASE=20250218
# Tue, 18 Feb 2025 08:26:12 GMT
ARG ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250218 ODOO_SHA=122896192ed221711dd471d27b2bd2f934c2ec07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 18 Feb 2025 08:26:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 18 Feb 2025 08:26:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 18 Feb 2025 08:26:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 18 Feb 2025 08:26:12 GMT
USER odoo
# Tue, 18 Feb 2025 08:26:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Feb 2025 08:26:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8455c54b495abb021f3ea0c5c47e4cc801d26c3f5b4f623f88a5ba88b4181458`  
		Last Modified: Mon, 10 Feb 2025 20:17:37 GMT  
		Size: 265.1 MB (265074206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0aa37e025c7ccd816c72a6cf91884a71817e56a69b066240616f7a2ae1537`  
		Last Modified: Mon, 10 Feb 2025 20:17:28 GMT  
		Size: 17.3 MB (17306456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a84f231b270cb999af35933efb7b7de7e00f97622369b26ac2dc6fec5558d7`  
		Last Modified: Mon, 10 Feb 2025 20:17:27 GMT  
		Size: 485.7 KB (485744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3185ddcb346c58a9c9458eb3aae9cbc151f162d9175e091bc728faf906b38881`  
		Last Modified: Tue, 18 Feb 2025 22:35:17 GMT  
		Size: 369.2 MB (369167487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c38c3550276428ae82c87d9a0198fea0bbe85a08e4dc8752f83b8668b38631a`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecbc3738e9209c1614330b9673d8424c1977410806c471699c2d337b046c8d3`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55c35b7c8f906d668e862bb346e25793451308081aded2bd5357929195ce56e`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9f2842375ea32a28d4b42604178f888325d669617de548fa5f4d055b082fe`  
		Last Modified: Tue, 18 Feb 2025 22:34:50 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:58db09feab7f74139006efc8a7671c951c6b73abe597beedad81beaf6691fe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58738017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e25c6b1790aa11b8513075bf8b1759e4978d214f02077ecbd07a8d1794b5ef`

```dockerfile
```

-	Layers:
	-	`sha256:17bb7f85ac41b157cd10780fbd87a59ec10945dc557243df4f1906f2b71861b0`  
		Last Modified: Tue, 18 Feb 2025 22:34:51 GMT  
		Size: 58.7 MB (58710819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e891c78d247fda1363a6e6408b8b6dda03e28bf8c010dc9f036c8e2d6e27d12`  
		Last Modified: Tue, 18 Feb 2025 22:34:49 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
