<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250123`](#odoo160-20250123)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250123`](#odoo170-20250123)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250123`](#odoo180-20250123)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:f3dc7da42bb634874a0fd30959436e8564495bfb69b075ebf5a0de98837fc737
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:8da27f292df6087bf62347ac02ef5796d95e1be043bb376c7f587ef32eb0c87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583887597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b739d27d028c98ba7cfe7ce68222963f6d49d6e94090e2a43ea5e9587681aa3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=amd64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=16.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=442da1ce17c084cdfd091dcecba4bef79c081838
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=442da1ce17c084cdfd091dcecba4bef79c081838
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=442da1ce17c084cdfd091dcecba4bef79c081838
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46acfade9c342514f1eaa6e7e0c4eb26a69301318d586223aa05afa7e7ddbec6`  
		Last Modified: Wed, 15 Jan 2025 20:32:00 GMT  
		Size: 219.6 MB (219629215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a98fdd160e0d8788b288dc1598d924cf75d283f9875f676f6ed9fea61c25ba`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 2.6 MB (2575905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b5abc10b01abacff4018d157669f851195635469d37d14a591e3805f59c208`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 484.9 KB (484917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae8d5b6889e285fdb814134598a326b1af969ecb4e4cce833e3b799b048d181`  
		Last Modified: Wed, 15 Jan 2025 20:32:05 GMT  
		Size: 330.9 MB (330942465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654d3d19fa96b20b2664e80464dce895b03ce6fba2d8e027eda90eb99830ec81`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e42100c458514cd931c17a43a0b469d71d12c80d2b312aa9b0cfdd89914b05`  
		Last Modified: Wed, 15 Jan 2025 20:31:58 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cd3d267843222f52246c0803b5089402225c849b55a0f46fbc4d89816fd6d4`  
		Last Modified: Wed, 15 Jan 2025 20:31:58 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26bba58f012bc950ff58d8989cb0f94c0c15d66c1fcfe851111c31fe18009ee`  
		Last Modified: Wed, 15 Jan 2025 20:31:58 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:1776efa362e7b461e2a592138f01fb13d06fe3b006d5f5e381886f00aa465ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38854379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccaab82c3b49fe64018d151fbfac6d39b12f4f7ebe814bd16e2f0c4d2800f29`

```dockerfile
```

-	Layers:
	-	`sha256:e6c5bf335a31551979074c8b45bca795854b73bfec29488550ec42d9f35a53a1`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 38.8 MB (38827661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a6e7a61d1a957d2538361bb3a856ca145e3f06f66a4b62a0e35109d294d598`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:05a62160cc8a8b171db69e40ab2e2e611d50169f74c9c2e520e0296cf6ee00bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579353165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20512e0580962bace714e24a7c330ea1c7bfe061c3143534c10fb790917fe175`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=arm64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=16.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=442da1ce17c084cdfd091dcecba4bef79c081838
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=442da1ce17c084cdfd091dcecba4bef79c081838
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=442da1ce17c084cdfd091dcecba4bef79c081838
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5d24d3e69c750d459da58fa8db7e255f0e6a8f27b1e06c76cc242cb82ee255`  
		Last Modified: Tue, 14 Jan 2025 07:42:55 GMT  
		Size: 216.9 MB (216921993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe08e0fd5c7f22cb24ce54385a0a3acf88fafb46c2b24d130642e7e3dbb47a95`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 2.6 MB (2583723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bb815672e62f69a2df6317a108d924edbe05d142421e9f9d00819a27ca84b1`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 485.4 KB (485433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26301b45365156d0c0d2d7ed042c4b0283e47bd4c9fd0d03447de51de193e512`  
		Last Modified: Wed, 15 Jan 2025 21:39:38 GMT  
		Size: 330.6 MB (330614675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3347c6e2e1e5c34e31efaaa79c607364f4b5b725885f51d0a3840317b9a44c`  
		Last Modified: Wed, 15 Jan 2025 21:39:29 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013890c90da7729947aa3bc0756d69079e024fe75ea4f3876a6b794576e18de0`  
		Last Modified: Wed, 15 Jan 2025 21:39:29 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79fa70fdc68b82d48182c22bb7bce5d22d13ea6c235a5509393ba2d9723aa7e`  
		Last Modified: Wed, 15 Jan 2025 21:39:29 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37e009995a3b226d33f1c0d3d169b1eefd736bc63eb9b7e3a326d3cd701348`  
		Last Modified: Wed, 15 Jan 2025 21:39:30 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:299a20120379819b4dc626307757b4617767e9136d0025e3757d33850607300d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38861001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316ba8a8777cd4ecb2a0688e0482aa59059283f02f3c423c31e67af0a382ac86`

```dockerfile
```

-	Layers:
	-	`sha256:84dde4cf8b15923b999c3812da7cb84565ac1ff2b53a3104cea7b6b26db685de`  
		Last Modified: Wed, 15 Jan 2025 21:39:30 GMT  
		Size: 38.8 MB (38834131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0ef076fa5afee07dec90157718e14b5cf42d14c054c8f109bf21f688caddaef`  
		Last Modified: Wed, 15 Jan 2025 21:39:29 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:f3dc7da42bb634874a0fd30959436e8564495bfb69b075ebf5a0de98837fc737
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:8da27f292df6087bf62347ac02ef5796d95e1be043bb376c7f587ef32eb0c87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583887597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b739d27d028c98ba7cfe7ce68222963f6d49d6e94090e2a43ea5e9587681aa3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=amd64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=16.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=442da1ce17c084cdfd091dcecba4bef79c081838
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=442da1ce17c084cdfd091dcecba4bef79c081838
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=442da1ce17c084cdfd091dcecba4bef79c081838
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46acfade9c342514f1eaa6e7e0c4eb26a69301318d586223aa05afa7e7ddbec6`  
		Last Modified: Wed, 15 Jan 2025 20:32:00 GMT  
		Size: 219.6 MB (219629215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a98fdd160e0d8788b288dc1598d924cf75d283f9875f676f6ed9fea61c25ba`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 2.6 MB (2575905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b5abc10b01abacff4018d157669f851195635469d37d14a591e3805f59c208`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 484.9 KB (484917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae8d5b6889e285fdb814134598a326b1af969ecb4e4cce833e3b799b048d181`  
		Last Modified: Wed, 15 Jan 2025 20:32:05 GMT  
		Size: 330.9 MB (330942465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654d3d19fa96b20b2664e80464dce895b03ce6fba2d8e027eda90eb99830ec81`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e42100c458514cd931c17a43a0b469d71d12c80d2b312aa9b0cfdd89914b05`  
		Last Modified: Wed, 15 Jan 2025 20:31:58 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cd3d267843222f52246c0803b5089402225c849b55a0f46fbc4d89816fd6d4`  
		Last Modified: Wed, 15 Jan 2025 20:31:58 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26bba58f012bc950ff58d8989cb0f94c0c15d66c1fcfe851111c31fe18009ee`  
		Last Modified: Wed, 15 Jan 2025 20:31:58 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1776efa362e7b461e2a592138f01fb13d06fe3b006d5f5e381886f00aa465ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38854379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccaab82c3b49fe64018d151fbfac6d39b12f4f7ebe814bd16e2f0c4d2800f29`

```dockerfile
```

-	Layers:
	-	`sha256:e6c5bf335a31551979074c8b45bca795854b73bfec29488550ec42d9f35a53a1`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 38.8 MB (38827661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a6e7a61d1a957d2538361bb3a856ca145e3f06f66a4b62a0e35109d294d598`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:05a62160cc8a8b171db69e40ab2e2e611d50169f74c9c2e520e0296cf6ee00bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579353165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20512e0580962bace714e24a7c330ea1c7bfe061c3143534c10fb790917fe175`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=C.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=arm64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=16.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=442da1ce17c084cdfd091dcecba4bef79c081838
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=442da1ce17c084cdfd091dcecba4bef79c081838
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=442da1ce17c084cdfd091dcecba4bef79c081838
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5d24d3e69c750d459da58fa8db7e255f0e6a8f27b1e06c76cc242cb82ee255`  
		Last Modified: Tue, 14 Jan 2025 07:42:55 GMT  
		Size: 216.9 MB (216921993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe08e0fd5c7f22cb24ce54385a0a3acf88fafb46c2b24d130642e7e3dbb47a95`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 2.6 MB (2583723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bb815672e62f69a2df6317a108d924edbe05d142421e9f9d00819a27ca84b1`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 485.4 KB (485433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26301b45365156d0c0d2d7ed042c4b0283e47bd4c9fd0d03447de51de193e512`  
		Last Modified: Wed, 15 Jan 2025 21:39:38 GMT  
		Size: 330.6 MB (330614675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3347c6e2e1e5c34e31efaaa79c607364f4b5b725885f51d0a3840317b9a44c`  
		Last Modified: Wed, 15 Jan 2025 21:39:29 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013890c90da7729947aa3bc0756d69079e024fe75ea4f3876a6b794576e18de0`  
		Last Modified: Wed, 15 Jan 2025 21:39:29 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79fa70fdc68b82d48182c22bb7bce5d22d13ea6c235a5509393ba2d9723aa7e`  
		Last Modified: Wed, 15 Jan 2025 21:39:29 GMT  
		Size: 588.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37e009995a3b226d33f1c0d3d169b1eefd736bc63eb9b7e3a326d3cd701348`  
		Last Modified: Wed, 15 Jan 2025 21:39:30 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:299a20120379819b4dc626307757b4617767e9136d0025e3757d33850607300d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38861001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316ba8a8777cd4ecb2a0688e0482aa59059283f02f3c423c31e67af0a382ac86`

```dockerfile
```

-	Layers:
	-	`sha256:84dde4cf8b15923b999c3812da7cb84565ac1ff2b53a3104cea7b6b26db685de`  
		Last Modified: Wed, 15 Jan 2025 21:39:30 GMT  
		Size: 38.8 MB (38834131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0ef076fa5afee07dec90157718e14b5cf42d14c054c8f109bf21f688caddaef`  
		Last Modified: Wed, 15 Jan 2025 21:39:29 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250123`

**does not exist** (yet?)

## `odoo:17`

```console
$ docker pull odoo@sha256:66bd85dc3bf086a85595091b501432ab5c36a960c60f40827a88cd4ce527fce7
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
$ docker pull odoo@sha256:a7bed4375374680a5771e61978abe9992163da6ed5c443665aca1fa17f4e6c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.3 MB (599284809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396fd69134ec7d20087594ab0a700a00f7aa13f022663a428432a22372a11a31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=amd64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=17.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d371f0f1f22495a0ec6c9a16757139cf1d239d00ad31b0d66473792136817f5c`  
		Last Modified: Wed, 15 Jan 2025 20:32:27 GMT  
		Size: 233.8 MB (233784931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baf814e69e25f86e2c6677a80ec328fb6b7e81e20f7af32acaa61378f5fc036`  
		Last Modified: Wed, 15 Jan 2025 20:32:21 GMT  
		Size: 2.5 MB (2493424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd254519f9fcfd6f898e033c22dfc6934794c697600942238508d74c8cf402c`  
		Last Modified: Wed, 15 Jan 2025 20:32:21 GMT  
		Size: 485.9 KB (485937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41891a33aac831d769bf426a28c070ebf116a4f02a083b34fc1372605ebc5dc2`  
		Last Modified: Wed, 15 Jan 2025 20:32:30 GMT  
		Size: 333.0 MB (332982388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54fc0988a95ab3137c499606463b982202fe991caaa6477b78921776c6f1b2d`  
		Last Modified: Wed, 15 Jan 2025 20:32:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40026252535f340bab88be4da5dcc9c6614427972979a9bddc42ad65fabc023`  
		Last Modified: Wed, 15 Jan 2025 20:32:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe65836bc936a2c3dada0baa65df0805570485d5fc004506e0844e0e41b18c2d`  
		Last Modified: Wed, 15 Jan 2025 20:32:23 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d308e22260de6aa0d3ed6f52557703e3fe02a464de0b94778abc2eb2074412`  
		Last Modified: Wed, 15 Jan 2025 20:32:23 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:a90230f95e922d51d3159696be67a21fb586377709e982f69ed1b81aa148e9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39682455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c033ad21ae0f0c35b99b24bb7468561bf2e5b968d7b6479de653737e72aa2f6`

```dockerfile
```

-	Layers:
	-	`sha256:5c1185075e64f713c4597a35b795d9d3be3e1c62e0c575edaadb2f03473a5c47`  
		Last Modified: Wed, 15 Jan 2025 20:32:22 GMT  
		Size: 39.7 MB (39655620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82a3a838097717bec998d782f3dc632942b08a6f7afb0ab1631b54bc54cd406f`  
		Last Modified: Wed, 15 Jan 2025 20:32:21 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:034de8b3e692d5b0405ee41ebbad16756240a754482c043686a878dd6c3dc103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.1 MB (594064601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1599833f6206cdd5a4f0b491d5d4c3431e5f4b926deeb81dfab70e3c37e7e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=arm64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=17.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec4903ad06f15a77b5bc7d9478e4efe03e19574e069a1c323b755949712d13`  
		Last Modified: Wed, 15 Jan 2025 21:36:40 GMT  
		Size: 231.1 MB (231144470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1c9faabded86415f8b589a233b87683de10e663a1748509bca962962ab2e34`  
		Last Modified: Wed, 15 Jan 2025 21:36:36 GMT  
		Size: 2.5 MB (2485698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f75bb3ce3a1db5400a884b03e52a7205e67189d079b438a548bc9cc03a58f0c`  
		Last Modified: Wed, 15 Jan 2025 21:36:35 GMT  
		Size: 485.9 KB (485940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d891dc6f6b0b1554476268ae1b265e56d049e853c5af27a1801b78c671fed17`  
		Last Modified: Wed, 15 Jan 2025 21:36:45 GMT  
		Size: 332.6 MB (332587725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f8743adbfad73ff4e421f428804f75f1a8d6e91ff10010ea1ba65182876db9`  
		Last Modified: Wed, 15 Jan 2025 21:36:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abab6ca4ee57eaf963be7e0b06b85ac2d401403afc76dedde917456d830d8d96`  
		Last Modified: Wed, 15 Jan 2025 21:36:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481e15d3f8f3d3d2adc9faf8fecf0ef41cab92ef3f3c2e1972f74e8ffeb62707`  
		Last Modified: Wed, 15 Jan 2025 21:36:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5d2a571aef5cf12efb8b1673d5faa1a1f1f5e2af18f2683896a7303df2e8c2`  
		Last Modified: Wed, 15 Jan 2025 21:36:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:4f856c13e2ca52882a298b8f86fed79b18de0900f4b1e7913fae23aa647fc6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39689118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b9e87253988ed2e9508be51d6339206ee45bfe7fe21b71fcbf98e65ae3b94d`

```dockerfile
```

-	Layers:
	-	`sha256:b5a099a7b064a18ea19346ee84b31e67b11e1e94fe1baf8d8be2193e63e2563a`  
		Last Modified: Wed, 15 Jan 2025 21:36:37 GMT  
		Size: 39.7 MB (39662131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41602bd1ac25b91be2c73dd182fad63e6d7390eb1caa9cda5603abaff606dffb`  
		Last Modified: Wed, 15 Jan 2025 21:36:35 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:f8a26a3caf697fe478aaff65cfda76e19338e0be7ce77b8d59589580c3f14598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.8 MB (615751910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a274b45944266892163abb362cae722769532897bec36c2608b2df899c7fd93d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=17.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250115 ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250115 ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e20dd12a5dc90e18349f058ef6faab0e98932d66235accdd4fd4ecf560e9ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:57 GMT  
		Size: 243.3 MB (243302074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36515bda1dae9f508aeb3a52dd6bcac45d347f81ada928cb84ae0eee75d9cf73`  
		Last Modified: Sat, 21 Dec 2024 00:03:39 GMT  
		Size: 2.8 MB (2798263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50956b86a0face373e64d0520f8600ad9870ea660dddb2d3c74cc015a90699c`  
		Last Modified: Wed, 15 Jan 2025 20:39:58 GMT  
		Size: 486.0 KB (485959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1eb2adcb931d67df6d2c556f9162c845faa1e8b03a8d9405fb278782972fcf`  
		Last Modified: Wed, 15 Jan 2025 20:40:11 GMT  
		Size: 334.7 MB (334714934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95458fef825a7b48a9c742a825837b13182e8c2ddb99d5f6ac8dbbe335752b10`  
		Last Modified: Wed, 15 Jan 2025 20:39:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab9e731ac714717c529fda211d55c574963b108a6b90712460733c66e2cf06e`  
		Last Modified: Wed, 15 Jan 2025 20:39:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e699b44de68b9835feaaa23be67ba7727737b577ce31ffe2466ac80ca79a821a`  
		Last Modified: Wed, 15 Jan 2025 20:39:59 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c0c8eccbd4a29610f35b357367dcda058f8a7dbffd8ccd13b7a9f802dbdf39`  
		Last Modified: Wed, 15 Jan 2025 20:39:59 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:a1549ac7f625b4b820f5397aee6b87fee246bebe67a05448435bebc7c4c4ff0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39690837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d313d911f1a087a345e016fb0859df06e9f2f1ac9fd2e7f5e944e171de54ee5b`

```dockerfile
```

-	Layers:
	-	`sha256:4de6a37fc29a9e42277ac8fb9acdff68cd0b17338438f720e9cd733b9867face`  
		Last Modified: Wed, 15 Jan 2025 20:40:00 GMT  
		Size: 39.7 MB (39663947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2a464f6fc2f26942e600fbb899b2b8825d3cb2194308c9e8360b5e01ba03e8`  
		Last Modified: Wed, 15 Jan 2025 20:39:57 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:66bd85dc3bf086a85595091b501432ab5c36a960c60f40827a88cd4ce527fce7
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
$ docker pull odoo@sha256:a7bed4375374680a5771e61978abe9992163da6ed5c443665aca1fa17f4e6c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.3 MB (599284809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396fd69134ec7d20087594ab0a700a00f7aa13f022663a428432a22372a11a31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=amd64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=17.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d371f0f1f22495a0ec6c9a16757139cf1d239d00ad31b0d66473792136817f5c`  
		Last Modified: Wed, 15 Jan 2025 20:32:27 GMT  
		Size: 233.8 MB (233784931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baf814e69e25f86e2c6677a80ec328fb6b7e81e20f7af32acaa61378f5fc036`  
		Last Modified: Wed, 15 Jan 2025 20:32:21 GMT  
		Size: 2.5 MB (2493424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd254519f9fcfd6f898e033c22dfc6934794c697600942238508d74c8cf402c`  
		Last Modified: Wed, 15 Jan 2025 20:32:21 GMT  
		Size: 485.9 KB (485937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41891a33aac831d769bf426a28c070ebf116a4f02a083b34fc1372605ebc5dc2`  
		Last Modified: Wed, 15 Jan 2025 20:32:30 GMT  
		Size: 333.0 MB (332982388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54fc0988a95ab3137c499606463b982202fe991caaa6477b78921776c6f1b2d`  
		Last Modified: Wed, 15 Jan 2025 20:32:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40026252535f340bab88be4da5dcc9c6614427972979a9bddc42ad65fabc023`  
		Last Modified: Wed, 15 Jan 2025 20:32:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe65836bc936a2c3dada0baa65df0805570485d5fc004506e0844e0e41b18c2d`  
		Last Modified: Wed, 15 Jan 2025 20:32:23 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d308e22260de6aa0d3ed6f52557703e3fe02a464de0b94778abc2eb2074412`  
		Last Modified: Wed, 15 Jan 2025 20:32:23 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a90230f95e922d51d3159696be67a21fb586377709e982f69ed1b81aa148e9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39682455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c033ad21ae0f0c35b99b24bb7468561bf2e5b968d7b6479de653737e72aa2f6`

```dockerfile
```

-	Layers:
	-	`sha256:5c1185075e64f713c4597a35b795d9d3be3e1c62e0c575edaadb2f03473a5c47`  
		Last Modified: Wed, 15 Jan 2025 20:32:22 GMT  
		Size: 39.7 MB (39655620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82a3a838097717bec998d782f3dc632942b08a6f7afb0ab1631b54bc54cd406f`  
		Last Modified: Wed, 15 Jan 2025 20:32:21 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:034de8b3e692d5b0405ee41ebbad16756240a754482c043686a878dd6c3dc103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.1 MB (594064601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1599833f6206cdd5a4f0b491d5d4c3431e5f4b926deeb81dfab70e3c37e7e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=arm64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=17.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec4903ad06f15a77b5bc7d9478e4efe03e19574e069a1c323b755949712d13`  
		Last Modified: Wed, 15 Jan 2025 21:36:40 GMT  
		Size: 231.1 MB (231144470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1c9faabded86415f8b589a233b87683de10e663a1748509bca962962ab2e34`  
		Last Modified: Wed, 15 Jan 2025 21:36:36 GMT  
		Size: 2.5 MB (2485698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f75bb3ce3a1db5400a884b03e52a7205e67189d079b438a548bc9cc03a58f0c`  
		Last Modified: Wed, 15 Jan 2025 21:36:35 GMT  
		Size: 485.9 KB (485940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d891dc6f6b0b1554476268ae1b265e56d049e853c5af27a1801b78c671fed17`  
		Last Modified: Wed, 15 Jan 2025 21:36:45 GMT  
		Size: 332.6 MB (332587725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f8743adbfad73ff4e421f428804f75f1a8d6e91ff10010ea1ba65182876db9`  
		Last Modified: Wed, 15 Jan 2025 21:36:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abab6ca4ee57eaf963be7e0b06b85ac2d401403afc76dedde917456d830d8d96`  
		Last Modified: Wed, 15 Jan 2025 21:36:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481e15d3f8f3d3d2adc9faf8fecf0ef41cab92ef3f3c2e1972f74e8ffeb62707`  
		Last Modified: Wed, 15 Jan 2025 21:36:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5d2a571aef5cf12efb8b1673d5faa1a1f1f5e2af18f2683896a7303df2e8c2`  
		Last Modified: Wed, 15 Jan 2025 21:36:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4f856c13e2ca52882a298b8f86fed79b18de0900f4b1e7913fae23aa647fc6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39689118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b9e87253988ed2e9508be51d6339206ee45bfe7fe21b71fcbf98e65ae3b94d`

```dockerfile
```

-	Layers:
	-	`sha256:b5a099a7b064a18ea19346ee84b31e67b11e1e94fe1baf8d8be2193e63e2563a`  
		Last Modified: Wed, 15 Jan 2025 21:36:37 GMT  
		Size: 39.7 MB (39662131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41602bd1ac25b91be2c73dd182fad63e6d7390eb1caa9cda5603abaff606dffb`  
		Last Modified: Wed, 15 Jan 2025 21:36:35 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:f8a26a3caf697fe478aaff65cfda76e19338e0be7ce77b8d59589580c3f14598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.8 MB (615751910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a274b45944266892163abb362cae722769532897bec36c2608b2df899c7fd93d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=17.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250115 ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250115 ODOO_SHA=c149d34b84dae91e0b8fd173c9e2e9bc82a8b60f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e20dd12a5dc90e18349f058ef6faab0e98932d66235accdd4fd4ecf560e9ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:57 GMT  
		Size: 243.3 MB (243302074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36515bda1dae9f508aeb3a52dd6bcac45d347f81ada928cb84ae0eee75d9cf73`  
		Last Modified: Sat, 21 Dec 2024 00:03:39 GMT  
		Size: 2.8 MB (2798263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50956b86a0face373e64d0520f8600ad9870ea660dddb2d3c74cc015a90699c`  
		Last Modified: Wed, 15 Jan 2025 20:39:58 GMT  
		Size: 486.0 KB (485959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1eb2adcb931d67df6d2c556f9162c845faa1e8b03a8d9405fb278782972fcf`  
		Last Modified: Wed, 15 Jan 2025 20:40:11 GMT  
		Size: 334.7 MB (334714934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95458fef825a7b48a9c742a825837b13182e8c2ddb99d5f6ac8dbbe335752b10`  
		Last Modified: Wed, 15 Jan 2025 20:39:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab9e731ac714717c529fda211d55c574963b108a6b90712460733c66e2cf06e`  
		Last Modified: Wed, 15 Jan 2025 20:39:58 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e699b44de68b9835feaaa23be67ba7727737b577ce31ffe2466ac80ca79a821a`  
		Last Modified: Wed, 15 Jan 2025 20:39:59 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c0c8eccbd4a29610f35b357367dcda058f8a7dbffd8ccd13b7a9f802dbdf39`  
		Last Modified: Wed, 15 Jan 2025 20:39:59 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a1549ac7f625b4b820f5397aee6b87fee246bebe67a05448435bebc7c4c4ff0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39690837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d313d911f1a087a345e016fb0859df06e9f2f1ac9fd2e7f5e944e171de54ee5b`

```dockerfile
```

-	Layers:
	-	`sha256:4de6a37fc29a9e42277ac8fb9acdff68cd0b17338438f720e9cd733b9867face`  
		Last Modified: Wed, 15 Jan 2025 20:40:00 GMT  
		Size: 39.7 MB (39663947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2a464f6fc2f26942e600fbb899b2b8825d3cb2194308c9e8360b5e01ba03e8`  
		Last Modified: Wed, 15 Jan 2025 20:39:57 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250123`

**does not exist** (yet?)

## `odoo:18`

```console
$ docker pull odoo@sha256:1011f1f8868a5b289ad8ea58b94760d98bf96280d6cc63504be04ec1f874e3ec
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
$ docker pull odoo@sha256:3bc6d6bf6224bc097a705c4d2905824e105efbd854d0de7a8c008c01576852bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.8 MB (665761275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f799527e2bd6f8d3580c44f985c2eb13fef29a83470c38f846cd86c33d167259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=amd64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d4f3c37ee8c8cd4f16437a8e1efc4c02b17f3879151e2f0c40baf1ccf0b01b`  
		Last Modified: Wed, 15 Jan 2025 20:32:42 GMT  
		Size: 254.5 MB (254515407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1583cd1bd81f938057cdcc9bf8a5b81bdda563d440bab2c1210e6c3f83cc68`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 14.2 MB (14231187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c75d22c8f8037a74816c0da373f35df336f72a785f2b2578e8baf9c26282cf7`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 485.8 KB (485773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f630fa1de8ed9e0b2cf2619eb82c27f34965293378c0bd43e25101b7c88970`  
		Last Modified: Wed, 15 Jan 2025 20:32:45 GMT  
		Size: 366.8 MB (366774502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654d3d19fa96b20b2664e80464dce895b03ce6fba2d8e027eda90eb99830ec81`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7e5f17843f510dfab7af49c284270a17445f472a81c85169a00e5143db0f6c`  
		Last Modified: Wed, 15 Jan 2025 20:32:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6c5b0d5d644c44ec897ba083e23ca6f2a9a1ac72021119ca8ec34c1d73a11e`  
		Last Modified: Wed, 15 Jan 2025 20:32:40 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bad202dba96f5d0c3641e77fc541cbf37cec4384d36835edf3e5df780da08c`  
		Last Modified: Wed, 15 Jan 2025 20:32:40 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:2e58b4d6f3c5accde02163c933b57ce50d33012651333605abab18b8d2d5bb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58396083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd78a039d8f37339b3109cfeb44448a7798eda508f2f31276765662860eb7b7`

```dockerfile
```

-	Layers:
	-	`sha256:73fa6a9bff23ad7edbe125c695020e1648cc56af28aaf8de7220be77f50344c5`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 58.4 MB (58368947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fe9a3b3d4abf003516f872ab11ff8e65c532c01dd4d579096f971cba7f3163`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0307d68b28e2a3eb7ecb77ceecc80f669f28b57c519213db4a1b82d0239f7406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.1 MB (662131977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c2e3fa0f567e8f215630f8e16d580b8a409f03a1c4cf5583ce2b75dd450a15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=arm64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ee3dc37083c88d416c17dbed8e797e8f0c5a483a27bc2bb5f9866637cd604`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 251.9 MB (251942154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf31355664213f01d2ffaa2ff07ceb2a41cacd6b8d61b1aefdf91f894149be`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 14.2 MB (14204373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed3c8a8f456bc9aa89bd20c60375a56af4be0c47c96ca7d2390addbc272e8d`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 485.7 KB (485733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7938239eb18bdd295d3c29951e0573c1aa2af28635b31e53bfb67322ac9a200`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 366.6 MB (366604606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7c4abcb56c1972a7cfbdd6c3407b594a1f690fec4344cd10c447cd083accb`  
		Last Modified: Wed, 15 Jan 2025 21:29:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042caa46e7bc657572be191abae039dff0256880260813b5a708b4eb7e65e7b`  
		Last Modified: Wed, 15 Jan 2025 21:29:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ee760cad61a4e5e37766d8b9b8073aa86f3df86dd17f2f37b24f67bd3e3d1e`  
		Last Modified: Wed, 15 Jan 2025 21:29:43 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b3a26742c4d8e6a3ecf0a8d76a81edb4cbb14c4477998c6799f55eeeff4e93`  
		Last Modified: Wed, 15 Jan 2025 21:29:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:fa0343351b29a4d8e644f817268f8f1c76a379ced41311c4196515d325df8eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58403538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db2c7e81f688f1731c69705bfb32608e67bfa0ce3679d68149de6b6e7389b8e`

```dockerfile
```

-	Layers:
	-	`sha256:41ae930849076446b6152bd549d0ad8ff8d7d1c524626dad8a962d9ad839b243`  
		Last Modified: Wed, 15 Jan 2025 21:29:43 GMT  
		Size: 58.4 MB (58376238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a09d0a28d677a82d2275fd981b7dae617504c4a4b6fc5ab22062cf239121316`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:7ff99cdea0e3f117ffe3867827905e7fdb6a3560e733d6be40b51865f51aafd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.0 MB (682047927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d81400e457420b1992ffb5b16435ef99d33d12b84f202b9723eddafdf48019`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4f22669c2b218e3b4c8798711c74160bdbcc4d4ae6a4e5d8fa984c7c54292`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 485.7 KB (485738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9402f00905f7cce6442ee97fc853e67922ab7c65387edcf9ff7304c1481f41d9`  
		Last Modified: Wed, 15 Jan 2025 20:34:20 GMT  
		Size: 367.3 MB (367305226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11691eb10c5e468c6f4d154c96f27009b0a2d1f57b1f1c063c486b14c1a5ecb`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3a7b4574d244082c36b752b519911f9451c3b453f3011945173174c13dd29a`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998d0347b20a2d6f1c70de4a6f2f7ecf1088a44eedd15805e8b5cae5d7bbf856`  
		Last Modified: Wed, 15 Jan 2025 20:34:10 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687758d5352eac6d316d400790619a39fa332788c5d9b179852188297af69b20`  
		Last Modified: Wed, 15 Jan 2025 20:34:10 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:48021ac6b0b0dacd28e1b66bd6ad2bb4aa7f61a6d60dff4116ef6977bc5b2f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58404307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fc6fa28f9a1ca42ce64f790e488043bef1d092233588036461ece10e7dde2b`

```dockerfile
```

-	Layers:
	-	`sha256:b0374af640497a11f836b4ece487a43e9fb9003533881d77dd2c79ce9b5473af`  
		Last Modified: Wed, 15 Jan 2025 20:34:11 GMT  
		Size: 58.4 MB (58377110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206e9ce76b735ee483ebff8449056fa974873b7fb1f8f7bc68f001a21ddd28ab`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:1011f1f8868a5b289ad8ea58b94760d98bf96280d6cc63504be04ec1f874e3ec
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
$ docker pull odoo@sha256:3bc6d6bf6224bc097a705c4d2905824e105efbd854d0de7a8c008c01576852bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.8 MB (665761275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f799527e2bd6f8d3580c44f985c2eb13fef29a83470c38f846cd86c33d167259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=amd64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d4f3c37ee8c8cd4f16437a8e1efc4c02b17f3879151e2f0c40baf1ccf0b01b`  
		Last Modified: Wed, 15 Jan 2025 20:32:42 GMT  
		Size: 254.5 MB (254515407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1583cd1bd81f938057cdcc9bf8a5b81bdda563d440bab2c1210e6c3f83cc68`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 14.2 MB (14231187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c75d22c8f8037a74816c0da373f35df336f72a785f2b2578e8baf9c26282cf7`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 485.8 KB (485773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f630fa1de8ed9e0b2cf2619eb82c27f34965293378c0bd43e25101b7c88970`  
		Last Modified: Wed, 15 Jan 2025 20:32:45 GMT  
		Size: 366.8 MB (366774502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654d3d19fa96b20b2664e80464dce895b03ce6fba2d8e027eda90eb99830ec81`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7e5f17843f510dfab7af49c284270a17445f472a81c85169a00e5143db0f6c`  
		Last Modified: Wed, 15 Jan 2025 20:32:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6c5b0d5d644c44ec897ba083e23ca6f2a9a1ac72021119ca8ec34c1d73a11e`  
		Last Modified: Wed, 15 Jan 2025 20:32:40 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bad202dba96f5d0c3641e77fc541cbf37cec4384d36835edf3e5df780da08c`  
		Last Modified: Wed, 15 Jan 2025 20:32:40 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2e58b4d6f3c5accde02163c933b57ce50d33012651333605abab18b8d2d5bb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58396083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd78a039d8f37339b3109cfeb44448a7798eda508f2f31276765662860eb7b7`

```dockerfile
```

-	Layers:
	-	`sha256:73fa6a9bff23ad7edbe125c695020e1648cc56af28aaf8de7220be77f50344c5`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 58.4 MB (58368947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fe9a3b3d4abf003516f872ab11ff8e65c532c01dd4d579096f971cba7f3163`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0307d68b28e2a3eb7ecb77ceecc80f669f28b57c519213db4a1b82d0239f7406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.1 MB (662131977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c2e3fa0f567e8f215630f8e16d580b8a409f03a1c4cf5583ce2b75dd450a15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=arm64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ee3dc37083c88d416c17dbed8e797e8f0c5a483a27bc2bb5f9866637cd604`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 251.9 MB (251942154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf31355664213f01d2ffaa2ff07ceb2a41cacd6b8d61b1aefdf91f894149be`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 14.2 MB (14204373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed3c8a8f456bc9aa89bd20c60375a56af4be0c47c96ca7d2390addbc272e8d`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 485.7 KB (485733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7938239eb18bdd295d3c29951e0573c1aa2af28635b31e53bfb67322ac9a200`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 366.6 MB (366604606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7c4abcb56c1972a7cfbdd6c3407b594a1f690fec4344cd10c447cd083accb`  
		Last Modified: Wed, 15 Jan 2025 21:29:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042caa46e7bc657572be191abae039dff0256880260813b5a708b4eb7e65e7b`  
		Last Modified: Wed, 15 Jan 2025 21:29:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ee760cad61a4e5e37766d8b9b8073aa86f3df86dd17f2f37b24f67bd3e3d1e`  
		Last Modified: Wed, 15 Jan 2025 21:29:43 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b3a26742c4d8e6a3ecf0a8d76a81edb4cbb14c4477998c6799f55eeeff4e93`  
		Last Modified: Wed, 15 Jan 2025 21:29:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:fa0343351b29a4d8e644f817268f8f1c76a379ced41311c4196515d325df8eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58403538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db2c7e81f688f1731c69705bfb32608e67bfa0ce3679d68149de6b6e7389b8e`

```dockerfile
```

-	Layers:
	-	`sha256:41ae930849076446b6152bd549d0ad8ff8d7d1c524626dad8a962d9ad839b243`  
		Last Modified: Wed, 15 Jan 2025 21:29:43 GMT  
		Size: 58.4 MB (58376238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a09d0a28d677a82d2275fd981b7dae617504c4a4b6fc5ab22062cf239121316`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:7ff99cdea0e3f117ffe3867827905e7fdb6a3560e733d6be40b51865f51aafd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.0 MB (682047927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d81400e457420b1992ffb5b16435ef99d33d12b84f202b9723eddafdf48019`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4f22669c2b218e3b4c8798711c74160bdbcc4d4ae6a4e5d8fa984c7c54292`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 485.7 KB (485738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9402f00905f7cce6442ee97fc853e67922ab7c65387edcf9ff7304c1481f41d9`  
		Last Modified: Wed, 15 Jan 2025 20:34:20 GMT  
		Size: 367.3 MB (367305226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11691eb10c5e468c6f4d154c96f27009b0a2d1f57b1f1c063c486b14c1a5ecb`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3a7b4574d244082c36b752b519911f9451c3b453f3011945173174c13dd29a`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998d0347b20a2d6f1c70de4a6f2f7ecf1088a44eedd15805e8b5cae5d7bbf856`  
		Last Modified: Wed, 15 Jan 2025 20:34:10 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687758d5352eac6d316d400790619a39fa332788c5d9b179852188297af69b20`  
		Last Modified: Wed, 15 Jan 2025 20:34:10 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:48021ac6b0b0dacd28e1b66bd6ad2bb4aa7f61a6d60dff4116ef6977bc5b2f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58404307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fc6fa28f9a1ca42ce64f790e488043bef1d092233588036461ece10e7dde2b`

```dockerfile
```

-	Layers:
	-	`sha256:b0374af640497a11f836b4ece487a43e9fb9003533881d77dd2c79ce9b5473af`  
		Last Modified: Wed, 15 Jan 2025 20:34:11 GMT  
		Size: 58.4 MB (58377110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206e9ce76b735ee483ebff8449056fa974873b7fb1f8f7bc68f001a21ddd28ab`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250123`

**does not exist** (yet?)

## `odoo:latest`

```console
$ docker pull odoo@sha256:1011f1f8868a5b289ad8ea58b94760d98bf96280d6cc63504be04ec1f874e3ec
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
$ docker pull odoo@sha256:3bc6d6bf6224bc097a705c4d2905824e105efbd854d0de7a8c008c01576852bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.8 MB (665761275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f799527e2bd6f8d3580c44f985c2eb13fef29a83470c38f846cd86c33d167259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=amd64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d4f3c37ee8c8cd4f16437a8e1efc4c02b17f3879151e2f0c40baf1ccf0b01b`  
		Last Modified: Wed, 15 Jan 2025 20:32:42 GMT  
		Size: 254.5 MB (254515407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1583cd1bd81f938057cdcc9bf8a5b81bdda563d440bab2c1210e6c3f83cc68`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 14.2 MB (14231187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c75d22c8f8037a74816c0da373f35df336f72a785f2b2578e8baf9c26282cf7`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 485.8 KB (485773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f630fa1de8ed9e0b2cf2619eb82c27f34965293378c0bd43e25101b7c88970`  
		Last Modified: Wed, 15 Jan 2025 20:32:45 GMT  
		Size: 366.8 MB (366774502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654d3d19fa96b20b2664e80464dce895b03ce6fba2d8e027eda90eb99830ec81`  
		Last Modified: Wed, 15 Jan 2025 20:31:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7e5f17843f510dfab7af49c284270a17445f472a81c85169a00e5143db0f6c`  
		Last Modified: Wed, 15 Jan 2025 20:32:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6c5b0d5d644c44ec897ba083e23ca6f2a9a1ac72021119ca8ec34c1d73a11e`  
		Last Modified: Wed, 15 Jan 2025 20:32:40 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bad202dba96f5d0c3641e77fc541cbf37cec4384d36835edf3e5df780da08c`  
		Last Modified: Wed, 15 Jan 2025 20:32:40 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:2e58b4d6f3c5accde02163c933b57ce50d33012651333605abab18b8d2d5bb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58396083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd78a039d8f37339b3109cfeb44448a7798eda508f2f31276765662860eb7b7`

```dockerfile
```

-	Layers:
	-	`sha256:73fa6a9bff23ad7edbe125c695020e1648cc56af28aaf8de7220be77f50344c5`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 58.4 MB (58368947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fe9a3b3d4abf003516f872ab11ff8e65c532c01dd4d579096f971cba7f3163`  
		Last Modified: Wed, 15 Jan 2025 20:32:39 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0307d68b28e2a3eb7ecb77ceecc80f669f28b57c519213db4a1b82d0239f7406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.1 MB (662131977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c2e3fa0f567e8f215630f8e16d580b8a409f03a1c4cf5583ce2b75dd450a15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=arm64
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ee3dc37083c88d416c17dbed8e797e8f0c5a483a27bc2bb5f9866637cd604`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 251.9 MB (251942154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf31355664213f01d2ffaa2ff07ceb2a41cacd6b8d61b1aefdf91f894149be`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 14.2 MB (14204373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed3c8a8f456bc9aa89bd20c60375a56af4be0c47c96ca7d2390addbc272e8d`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 485.7 KB (485733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7938239eb18bdd295d3c29951e0573c1aa2af28635b31e53bfb67322ac9a200`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 366.6 MB (366604606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7c4abcb56c1972a7cfbdd6c3407b594a1f690fec4344cd10c447cd083accb`  
		Last Modified: Wed, 15 Jan 2025 21:29:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042caa46e7bc657572be191abae039dff0256880260813b5a708b4eb7e65e7b`  
		Last Modified: Wed, 15 Jan 2025 21:29:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ee760cad61a4e5e37766d8b9b8073aa86f3df86dd17f2f37b24f67bd3e3d1e`  
		Last Modified: Wed, 15 Jan 2025 21:29:43 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b3a26742c4d8e6a3ecf0a8d76a81edb4cbb14c4477998c6799f55eeeff4e93`  
		Last Modified: Wed, 15 Jan 2025 21:29:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:fa0343351b29a4d8e644f817268f8f1c76a379ced41311c4196515d325df8eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58403538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db2c7e81f688f1731c69705bfb32608e67bfa0ce3679d68149de6b6e7389b8e`

```dockerfile
```

-	Layers:
	-	`sha256:41ae930849076446b6152bd549d0ad8ff8d7d1c524626dad8a962d9ad839b243`  
		Last Modified: Wed, 15 Jan 2025 21:29:43 GMT  
		Size: 58.4 MB (58376238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a09d0a28d677a82d2275fd981b7dae617504c4a4b6fc5ab22062cf239121316`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:7ff99cdea0e3f117ffe3867827905e7fdb6a3560e733d6be40b51865f51aafd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.0 MB (682047927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d81400e457420b1992ffb5b16435ef99d33d12b84f202b9723eddafdf48019`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 12:28:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Jan 2025 12:28:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Jan 2025 12:28:41 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_VERSION=18.0
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_RELEASE=20250115
# Wed, 15 Jan 2025 12:28:41 GMT
ARG ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250115 ODOO_SHA=81e4f8d693ad8d49e37f2e5f6766b2746320b7cb
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 15 Jan 2025 12:28:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 15 Jan 2025 12:28:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 15 Jan 2025 12:28:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 15 Jan 2025 12:28:41 GMT
USER odoo
# Wed, 15 Jan 2025 12:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 15 Jan 2025 12:28:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4f22669c2b218e3b4c8798711c74160bdbcc4d4ae6a4e5d8fa984c7c54292`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 485.7 KB (485738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9402f00905f7cce6442ee97fc853e67922ab7c65387edcf9ff7304c1481f41d9`  
		Last Modified: Wed, 15 Jan 2025 20:34:20 GMT  
		Size: 367.3 MB (367305226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11691eb10c5e468c6f4d154c96f27009b0a2d1f57b1f1c063c486b14c1a5ecb`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3a7b4574d244082c36b752b519911f9451c3b453f3011945173174c13dd29a`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998d0347b20a2d6f1c70de4a6f2f7ecf1088a44eedd15805e8b5cae5d7bbf856`  
		Last Modified: Wed, 15 Jan 2025 20:34:10 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687758d5352eac6d316d400790619a39fa332788c5d9b179852188297af69b20`  
		Last Modified: Wed, 15 Jan 2025 20:34:10 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:48021ac6b0b0dacd28e1b66bd6ad2bb4aa7f61a6d60dff4116ef6977bc5b2f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58404307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fc6fa28f9a1ca42ce64f790e488043bef1d092233588036461ece10e7dde2b`

```dockerfile
```

-	Layers:
	-	`sha256:b0374af640497a11f836b4ece487a43e9fb9003533881d77dd2c79ce9b5473af`  
		Last Modified: Wed, 15 Jan 2025 20:34:11 GMT  
		Size: 58.4 MB (58377110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206e9ce76b735ee483ebff8449056fa974873b7fb1f8f7bc68f001a21ddd28ab`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json
