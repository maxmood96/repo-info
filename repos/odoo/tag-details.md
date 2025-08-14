<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250807`](#odoo160-20250807)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250807`](#odoo170-20250807)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250807`](#odoo180-20250807)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:0ef27f154012ec8f2ab68e6b6929327fbebd79dd4004bce7059217be256cb07c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:49e452e826fa47a5b6968e8e2d65f145d4a2fe3f4d75938fafe7e2d6dc439ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585303135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb42753dcc9a8d524e49348c00ed58cedb738106a339048b96d58ebb8a7727d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 07 Aug 2025 07:18:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=amd64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=16.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c05c0ed02424b560e88922743703cbcf21288699e94172e2fae8500d9128048`  
		Last Modified: Wed, 13 Aug 2025 00:28:08 GMT  
		Size: 219.6 MB (219625758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3b23e5e0a4f4923c73a33f720c667318afbfc5ecdae8af871bf72de7e1871e`  
		Last Modified: Tue, 12 Aug 2025 21:29:47 GMT  
		Size: 2.6 MB (2627209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d902a8fea5f5fdae018596ee05b61e107c32c77867105af0416aac721622bf`  
		Last Modified: Tue, 12 Aug 2025 21:29:46 GMT  
		Size: 479.4 KB (479378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d2f2040a5a5eecb6919394b7311cc75522f7355057eae5b77b3928be14caf0`  
		Last Modified: Wed, 13 Aug 2025 00:28:53 GMT  
		Size: 332.3 MB (332312240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850a1467a282302c2716bf9ce9216d4a2331fec5bc14059b2d6841d76680da9e`  
		Last Modified: Tue, 12 Aug 2025 21:29:46 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dab97305913a8be9073ff9d280433a3086e6badc53725509931fb3be1d8e5a`  
		Last Modified: Tue, 12 Aug 2025 21:29:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c777ea9368c6dd3d1f8f071398120a47d439aae0a1f92e19158bf5fd4e3fe865`  
		Last Modified: Tue, 12 Aug 2025 21:29:48 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e465758ffe0795dc74e186a0a5bf0dfd296c101676cc757a0262880e7a9aef`  
		Last Modified: Tue, 12 Aug 2025 21:29:47 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:fe056d9b56433f6b6ffb1fb4fd0126cea5973f5a1c03c7a68bd6f09148e2a462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39558663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e195f0e7ae58f06b87a47f2fc34a5d319d70f7509739560cff82cb98eb039dc2`

```dockerfile
```

-	Layers:
	-	`sha256:2c55268aa7ac195301f100dde28e18f4e51546c3abf1335d27b19045d9d1ad0d`  
		Last Modified: Wed, 13 Aug 2025 01:12:21 GMT  
		Size: 39.5 MB (39531948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7830a13dfd9f1098bfae5ad03a882171b81012b3321a2a0b3c14fb3c952f89e`  
		Last Modified: Wed, 13 Aug 2025 01:12:23 GMT  
		Size: 26.7 KB (26715 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:048fef373d9ad357b13940ae31ce4fe9cbc5d3e6e69db041296ce94f86b0a8a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580754817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac40123b352a46e5f74d428f34d99b9504f3bc0017f879a012bdb03f9ab7d18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 07 Aug 2025 07:18:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=arm64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=16.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4e82962c454e3cc1d918a264da7d4ccd7d37ef7335cdd51b44399358b5b5fe`  
		Last Modified: Wed, 13 Aug 2025 09:18:13 GMT  
		Size: 216.9 MB (216918800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91af15ce6cb45bbc927479f91527549c09c129488a5b7c78aec415e21c0d68f6`  
		Last Modified: Wed, 13 Aug 2025 09:07:48 GMT  
		Size: 2.6 MB (2635459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d467a6946846904e0d2f8f0b5f6db1e5526672743fe71294818662b57f930c1`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 479.3 KB (479322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60413ab0887e816b99f04eb7ab325d3489b02fc7cd1280fe9ece9edd7be041d3`  
		Last Modified: Wed, 13 Aug 2025 09:18:13 GMT  
		Size: 332.0 MB (331968314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4566d95c3eb51e0796f90e5f4331cd835f28068d7e35d6ca21192dba6fea028e`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd6bb4c84253f7cf4c890899727552d5749d2b080eead832be748f151f4181b`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54f084eccc5031f02a3399e44cfaca16529d0056af7dff23607944652031444`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125d8265595b069c1035b7854557d284c252815e9398d7d39740087b65e7db4b`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:aecd247a38c4fc9c371a69d1721652d5524f9f7204544d52d8de8f0763a185e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39565284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd79da3db9cda56c26ea9857cf94b228d16a9b3ecafe73e4da7bfabdd26e0e0`

```dockerfile
```

-	Layers:
	-	`sha256:e5d61b11cee04b282c6e97bf96329f66271301eb6a5afd8f20ecbd93145b2316`  
		Last Modified: Wed, 13 Aug 2025 10:12:56 GMT  
		Size: 39.5 MB (39538414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa0e51fa6bd396c9cf76df6986095f0c077b284ec595e167ac6f5e45eb0a4894`  
		Last Modified: Wed, 13 Aug 2025 10:12:57 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:0ef27f154012ec8f2ab68e6b6929327fbebd79dd4004bce7059217be256cb07c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:49e452e826fa47a5b6968e8e2d65f145d4a2fe3f4d75938fafe7e2d6dc439ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585303135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb42753dcc9a8d524e49348c00ed58cedb738106a339048b96d58ebb8a7727d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 07 Aug 2025 07:18:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=amd64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=16.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c05c0ed02424b560e88922743703cbcf21288699e94172e2fae8500d9128048`  
		Last Modified: Wed, 13 Aug 2025 00:28:08 GMT  
		Size: 219.6 MB (219625758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3b23e5e0a4f4923c73a33f720c667318afbfc5ecdae8af871bf72de7e1871e`  
		Last Modified: Tue, 12 Aug 2025 21:29:47 GMT  
		Size: 2.6 MB (2627209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d902a8fea5f5fdae018596ee05b61e107c32c77867105af0416aac721622bf`  
		Last Modified: Tue, 12 Aug 2025 21:29:46 GMT  
		Size: 479.4 KB (479378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d2f2040a5a5eecb6919394b7311cc75522f7355057eae5b77b3928be14caf0`  
		Last Modified: Wed, 13 Aug 2025 00:28:53 GMT  
		Size: 332.3 MB (332312240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850a1467a282302c2716bf9ce9216d4a2331fec5bc14059b2d6841d76680da9e`  
		Last Modified: Tue, 12 Aug 2025 21:29:46 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dab97305913a8be9073ff9d280433a3086e6badc53725509931fb3be1d8e5a`  
		Last Modified: Tue, 12 Aug 2025 21:29:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c777ea9368c6dd3d1f8f071398120a47d439aae0a1f92e19158bf5fd4e3fe865`  
		Last Modified: Tue, 12 Aug 2025 21:29:48 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e465758ffe0795dc74e186a0a5bf0dfd296c101676cc757a0262880e7a9aef`  
		Last Modified: Tue, 12 Aug 2025 21:29:47 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:fe056d9b56433f6b6ffb1fb4fd0126cea5973f5a1c03c7a68bd6f09148e2a462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39558663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e195f0e7ae58f06b87a47f2fc34a5d319d70f7509739560cff82cb98eb039dc2`

```dockerfile
```

-	Layers:
	-	`sha256:2c55268aa7ac195301f100dde28e18f4e51546c3abf1335d27b19045d9d1ad0d`  
		Last Modified: Wed, 13 Aug 2025 01:12:21 GMT  
		Size: 39.5 MB (39531948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7830a13dfd9f1098bfae5ad03a882171b81012b3321a2a0b3c14fb3c952f89e`  
		Last Modified: Wed, 13 Aug 2025 01:12:23 GMT  
		Size: 26.7 KB (26715 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:048fef373d9ad357b13940ae31ce4fe9cbc5d3e6e69db041296ce94f86b0a8a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580754817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac40123b352a46e5f74d428f34d99b9504f3bc0017f879a012bdb03f9ab7d18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 07 Aug 2025 07:18:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=arm64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=16.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4e82962c454e3cc1d918a264da7d4ccd7d37ef7335cdd51b44399358b5b5fe`  
		Last Modified: Wed, 13 Aug 2025 09:18:13 GMT  
		Size: 216.9 MB (216918800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91af15ce6cb45bbc927479f91527549c09c129488a5b7c78aec415e21c0d68f6`  
		Last Modified: Wed, 13 Aug 2025 09:07:48 GMT  
		Size: 2.6 MB (2635459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d467a6946846904e0d2f8f0b5f6db1e5526672743fe71294818662b57f930c1`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 479.3 KB (479322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60413ab0887e816b99f04eb7ab325d3489b02fc7cd1280fe9ece9edd7be041d3`  
		Last Modified: Wed, 13 Aug 2025 09:18:13 GMT  
		Size: 332.0 MB (331968314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4566d95c3eb51e0796f90e5f4331cd835f28068d7e35d6ca21192dba6fea028e`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd6bb4c84253f7cf4c890899727552d5749d2b080eead832be748f151f4181b`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54f084eccc5031f02a3399e44cfaca16529d0056af7dff23607944652031444`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125d8265595b069c1035b7854557d284c252815e9398d7d39740087b65e7db4b`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:aecd247a38c4fc9c371a69d1721652d5524f9f7204544d52d8de8f0763a185e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39565284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd79da3db9cda56c26ea9857cf94b228d16a9b3ecafe73e4da7bfabdd26e0e0`

```dockerfile
```

-	Layers:
	-	`sha256:e5d61b11cee04b282c6e97bf96329f66271301eb6a5afd8f20ecbd93145b2316`  
		Last Modified: Wed, 13 Aug 2025 10:12:56 GMT  
		Size: 39.5 MB (39538414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa0e51fa6bd396c9cf76df6986095f0c077b284ec595e167ac6f5e45eb0a4894`  
		Last Modified: Wed, 13 Aug 2025 10:12:57 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250807`

```console
$ docker pull odoo@sha256:0ef27f154012ec8f2ab68e6b6929327fbebd79dd4004bce7059217be256cb07c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250807` - linux; amd64

```console
$ docker pull odoo@sha256:49e452e826fa47a5b6968e8e2d65f145d4a2fe3f4d75938fafe7e2d6dc439ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.3 MB (585303135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb42753dcc9a8d524e49348c00ed58cedb738106a339048b96d58ebb8a7727d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 07 Aug 2025 07:18:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=amd64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=16.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c05c0ed02424b560e88922743703cbcf21288699e94172e2fae8500d9128048`  
		Last Modified: Wed, 13 Aug 2025 00:28:08 GMT  
		Size: 219.6 MB (219625758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3b23e5e0a4f4923c73a33f720c667318afbfc5ecdae8af871bf72de7e1871e`  
		Last Modified: Tue, 12 Aug 2025 21:29:47 GMT  
		Size: 2.6 MB (2627209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d902a8fea5f5fdae018596ee05b61e107c32c77867105af0416aac721622bf`  
		Last Modified: Tue, 12 Aug 2025 21:29:46 GMT  
		Size: 479.4 KB (479378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d2f2040a5a5eecb6919394b7311cc75522f7355057eae5b77b3928be14caf0`  
		Last Modified: Wed, 13 Aug 2025 00:28:53 GMT  
		Size: 332.3 MB (332312240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850a1467a282302c2716bf9ce9216d4a2331fec5bc14059b2d6841d76680da9e`  
		Last Modified: Tue, 12 Aug 2025 21:29:46 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dab97305913a8be9073ff9d280433a3086e6badc53725509931fb3be1d8e5a`  
		Last Modified: Tue, 12 Aug 2025 21:29:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c777ea9368c6dd3d1f8f071398120a47d439aae0a1f92e19158bf5fd4e3fe865`  
		Last Modified: Tue, 12 Aug 2025 21:29:48 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e465758ffe0795dc74e186a0a5bf0dfd296c101676cc757a0262880e7a9aef`  
		Last Modified: Tue, 12 Aug 2025 21:29:47 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250807` - unknown; unknown

```console
$ docker pull odoo@sha256:fe056d9b56433f6b6ffb1fb4fd0126cea5973f5a1c03c7a68bd6f09148e2a462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39558663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e195f0e7ae58f06b87a47f2fc34a5d319d70f7509739560cff82cb98eb039dc2`

```dockerfile
```

-	Layers:
	-	`sha256:2c55268aa7ac195301f100dde28e18f4e51546c3abf1335d27b19045d9d1ad0d`  
		Last Modified: Wed, 13 Aug 2025 01:12:21 GMT  
		Size: 39.5 MB (39531948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7830a13dfd9f1098bfae5ad03a882171b81012b3321a2a0b3c14fb3c952f89e`  
		Last Modified: Wed, 13 Aug 2025 01:12:23 GMT  
		Size: 26.7 KB (26715 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250807` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:048fef373d9ad357b13940ae31ce4fe9cbc5d3e6e69db041296ce94f86b0a8a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580754817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac40123b352a46e5f74d428f34d99b9504f3bc0017f879a012bdb03f9ab7d18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 07 Aug 2025 07:18:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=C.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=arm64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=16.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=e77cd6f4664a81303035bf56ee0f6f1827a20fee
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4e82962c454e3cc1d918a264da7d4ccd7d37ef7335cdd51b44399358b5b5fe`  
		Last Modified: Wed, 13 Aug 2025 09:18:13 GMT  
		Size: 216.9 MB (216918800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91af15ce6cb45bbc927479f91527549c09c129488a5b7c78aec415e21c0d68f6`  
		Last Modified: Wed, 13 Aug 2025 09:07:48 GMT  
		Size: 2.6 MB (2635459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d467a6946846904e0d2f8f0b5f6db1e5526672743fe71294818662b57f930c1`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 479.3 KB (479322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60413ab0887e816b99f04eb7ab325d3489b02fc7cd1280fe9ece9edd7be041d3`  
		Last Modified: Wed, 13 Aug 2025 09:18:13 GMT  
		Size: 332.0 MB (331968314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4566d95c3eb51e0796f90e5f4331cd835f28068d7e35d6ca21192dba6fea028e`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd6bb4c84253f7cf4c890899727552d5749d2b080eead832be748f151f4181b`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54f084eccc5031f02a3399e44cfaca16529d0056af7dff23607944652031444`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125d8265595b069c1035b7854557d284c252815e9398d7d39740087b65e7db4b`  
		Last Modified: Wed, 13 Aug 2025 09:07:47 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250807` - unknown; unknown

```console
$ docker pull odoo@sha256:aecd247a38c4fc9c371a69d1721652d5524f9f7204544d52d8de8f0763a185e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39565284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd79da3db9cda56c26ea9857cf94b228d16a9b3ecafe73e4da7bfabdd26e0e0`

```dockerfile
```

-	Layers:
	-	`sha256:e5d61b11cee04b282c6e97bf96329f66271301eb6a5afd8f20ecbd93145b2316`  
		Last Modified: Wed, 13 Aug 2025 10:12:56 GMT  
		Size: 39.5 MB (39538414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa0e51fa6bd396c9cf76df6986095f0c077b284ec595e167ac6f5e45eb0a4894`  
		Last Modified: Wed, 13 Aug 2025 10:12:57 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:940c07327d62d00f831f7a98cf05dcd396552adf8c73e43d2d8a6bbdcf15e183
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
$ docker pull odoo@sha256:8fffbe49db153db59d6e2b04965b2d607e66061d6148828e9fb2dcf5f331f53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.8 MB (601791509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b54a375ad61bb5f654d6d6905dc4add3d6c25c21da82f9162e7c7960f8c3b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=amd64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=17.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a642c4eed8f93f91e9b334f783a4f079d8c55c3f772596d26a05ce69c4784ec`  
		Last Modified: Tue, 12 Aug 2025 19:12:37 GMT  
		Size: 233.8 MB (233790834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17634efc9be4636787e671664ae378da7e735d45196c48c5d4ae7551749c1214`  
		Last Modified: Tue, 12 Aug 2025 17:30:10 GMT  
		Size: 2.5 MB (2523056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96843a23a809cc9571e82e3cf72631db4b3861204b8cd73bb0508b0bb971d1ed`  
		Last Modified: Tue, 12 Aug 2025 17:30:12 GMT  
		Size: 480.5 KB (480472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c463ee4230390dce981ebe526254127fc19600495ed9d9c870a103280ae8c0f2`  
		Last Modified: Tue, 12 Aug 2025 19:12:35 GMT  
		Size: 335.5 MB (335457715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f207422b9af943af65c009a7917e874209c05bfb18bce7d979292f9fefac1`  
		Last Modified: Tue, 12 Aug 2025 17:30:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eeb620bca1430ca1e98511a88c10d4fa7802ab7cbb93c4848a9bddcacefc69`  
		Last Modified: Tue, 12 Aug 2025 17:30:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0eb4f52e16cf48e33ba3811d97ba2f7c6952307ac09e05dbc86c3c9755e6ba`  
		Last Modified: Tue, 12 Aug 2025 17:30:13 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a996c305ae6ef0d7ba7445015dca436a813c79323da8276422ee7b66854e4`  
		Last Modified: Tue, 12 Aug 2025 17:30:12 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:4d0fbfc5d178aae3bde41f226b131ce0a29e27c35ab232eff9ae19b32f38add5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40604216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb0e075852c6172f89b7ae511d33d4b4c6327bbdf8c4dc5dc68f6d844e29ee8`

```dockerfile
```

-	Layers:
	-	`sha256:74820c554c29d5214c10886aeb3a08e5cacfc3f5456c1f3f9ff1169ade227e1a`  
		Last Modified: Tue, 12 Aug 2025 19:12:25 GMT  
		Size: 40.6 MB (40577381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcd0baf964989410636494b1ddc87ab90d9e2ebc51a7163bb7fcafa580adab11`  
		Last Modified: Tue, 12 Aug 2025 19:12:26 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:039b25bac32d91caa2ff2cbfc625519c9a25a1a41706f050049f338249171304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.6 MB (596569696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cdae1dbefdb56fb0b3f154720e444e7224839e351e444eae6289d7e2f35e30a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=arm64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=17.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce88273e085fc69344868d25a6ded0d7c2a35a130e9a62ee6ca1b47d36e956e`  
		Last Modified: Tue, 12 Aug 2025 22:14:27 GMT  
		Size: 231.2 MB (231162497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3b2046d4217a5ce0b9be5cb2c6eae5b8af1c71160703bc13823365076ca1c4`  
		Last Modified: Tue, 12 Aug 2025 20:45:51 GMT  
		Size: 2.5 MB (2516790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e75e3cb4ce125c29316f7c6787874fad553b5ff95ba996742bab5b6c2a9f753`  
		Last Modified: Tue, 12 Aug 2025 20:45:50 GMT  
		Size: 480.4 KB (480392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd96c49cf9a0b172e83f4499ef37dbe94f85fe73bac13d4fc3f08082e6d44824`  
		Last Modified: Tue, 12 Aug 2025 22:14:24 GMT  
		Size: 335.0 MB (335048333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1395e4ee60eef1c9276516160a141135c24aef7623055e77fc673aaf63ca7ea9`  
		Last Modified: Tue, 12 Aug 2025 20:45:50 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819237bd520c3436c205b96a2a4df9f8c754a03550b5b736a19788da7d63dbec`  
		Last Modified: Tue, 12 Aug 2025 20:45:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebff89376f351610c5e8bc1b8611f0608f8eebc2f1297cc4a549135ed087aca2`  
		Last Modified: Tue, 12 Aug 2025 20:45:50 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b1426f083e75adc0f75d32a3ac49f4252baed65920e4e162ca7bba312af955`  
		Last Modified: Tue, 12 Aug 2025 20:45:51 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:76e441c607d0a1bef91f378dba1c50491465d3d7c0ad95145ec2079313a7e709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40610874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5458dacce5c83264d71c21212dd32f954cc8bf7721d5f4cd6a919ad9997ee045`

```dockerfile
```

-	Layers:
	-	`sha256:23576acc0d884460b19f8128912e0bc29a6eed01edda4188e32979a2df62d76e`  
		Last Modified: Tue, 12 Aug 2025 22:13:09 GMT  
		Size: 40.6 MB (40583888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c09bd52a2f56ad1b7f21478a835da8a94c3022ecfd801a9004e0ac7f32535a8`  
		Last Modified: Tue, 12 Aug 2025 22:13:10 GMT  
		Size: 27.0 KB (26986 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:a1a056cf15c56b99b0ce557a4a3f8546fcd7561a7ade091a1695b2c86ff01ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.2 MB (618190059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ecbc9b5416588797150de487b1edf757cec96a89eccb6f1bea7c061cda378fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=ppc64le
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=17.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626289f98e141fb35911a2db7b56f0b3c17a927e40fa18d5e75bfe052c0334f1`  
		Last Modified: Tue, 12 Aug 2025 21:58:18 GMT  
		Size: 243.3 MB (243258260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cdf06f3cc41682478576d9ab4e57e6aea676b7a0da14b27a1630b502b0efb7`  
		Last Modified: Tue, 12 Aug 2025 21:59:01 GMT  
		Size: 2.8 MB (2841625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382e4f5f1a6345078ca3cbd61de82e153c765494f47a58a72ff3196627a527ad`  
		Last Modified: Tue, 12 Aug 2025 21:59:01 GMT  
		Size: 480.4 KB (480416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91591a8a8ae8b2ced71d4d9cd42d4c1b7cc1e10e78073783da1b4bd27720a799`  
		Last Modified: Tue, 12 Aug 2025 21:58:21 GMT  
		Size: 337.2 MB (337164178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2039f8d6faaa3ac3c4e518d26c35cf10d078007c291d73a04418993155656c1f`  
		Last Modified: Tue, 12 Aug 2025 21:59:00 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf24035b3b6735db9751221db7d9feb7703e35bfa166659d356a246fc19b69b4`  
		Last Modified: Tue, 12 Aug 2025 21:59:01 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a56ff198f3964c2afcabb4dfd84ee898c115819d6abf5cd4a07e83d3c7d60a`  
		Last Modified: Tue, 12 Aug 2025 22:20:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6142daf3732c08182052152edc1cfa1b10e78c0d97a285f18991504240d3cae`  
		Last Modified: Tue, 12 Aug 2025 22:20:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:b76a91f79952fb18ff66d6c1e4c5b982382910e16446ca7f2422164c6721d13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40612879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f4177b3d6d0416a6c7724f175a7b14331464748c26248d20fe8a6f21af0338`

```dockerfile
```

-	Layers:
	-	`sha256:8c1fda861a67e50265e4a6c03670368dad9c43cab523ab6417727c166bc5eaa9`  
		Last Modified: Wed, 13 Aug 2025 01:14:09 GMT  
		Size: 40.6 MB (40585988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfb9a143b9b1dca8dbe14382575330833f71069d471256c3f157942d6233a11a`  
		Last Modified: Wed, 13 Aug 2025 01:14:11 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:940c07327d62d00f831f7a98cf05dcd396552adf8c73e43d2d8a6bbdcf15e183
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
$ docker pull odoo@sha256:8fffbe49db153db59d6e2b04965b2d607e66061d6148828e9fb2dcf5f331f53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.8 MB (601791509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b54a375ad61bb5f654d6d6905dc4add3d6c25c21da82f9162e7c7960f8c3b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=amd64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=17.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a642c4eed8f93f91e9b334f783a4f079d8c55c3f772596d26a05ce69c4784ec`  
		Last Modified: Tue, 12 Aug 2025 19:12:37 GMT  
		Size: 233.8 MB (233790834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17634efc9be4636787e671664ae378da7e735d45196c48c5d4ae7551749c1214`  
		Last Modified: Tue, 12 Aug 2025 17:30:10 GMT  
		Size: 2.5 MB (2523056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96843a23a809cc9571e82e3cf72631db4b3861204b8cd73bb0508b0bb971d1ed`  
		Last Modified: Tue, 12 Aug 2025 17:30:12 GMT  
		Size: 480.5 KB (480472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c463ee4230390dce981ebe526254127fc19600495ed9d9c870a103280ae8c0f2`  
		Last Modified: Tue, 12 Aug 2025 19:12:35 GMT  
		Size: 335.5 MB (335457715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f207422b9af943af65c009a7917e874209c05bfb18bce7d979292f9fefac1`  
		Last Modified: Tue, 12 Aug 2025 17:30:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eeb620bca1430ca1e98511a88c10d4fa7802ab7cbb93c4848a9bddcacefc69`  
		Last Modified: Tue, 12 Aug 2025 17:30:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0eb4f52e16cf48e33ba3811d97ba2f7c6952307ac09e05dbc86c3c9755e6ba`  
		Last Modified: Tue, 12 Aug 2025 17:30:13 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a996c305ae6ef0d7ba7445015dca436a813c79323da8276422ee7b66854e4`  
		Last Modified: Tue, 12 Aug 2025 17:30:12 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4d0fbfc5d178aae3bde41f226b131ce0a29e27c35ab232eff9ae19b32f38add5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40604216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb0e075852c6172f89b7ae511d33d4b4c6327bbdf8c4dc5dc68f6d844e29ee8`

```dockerfile
```

-	Layers:
	-	`sha256:74820c554c29d5214c10886aeb3a08e5cacfc3f5456c1f3f9ff1169ade227e1a`  
		Last Modified: Tue, 12 Aug 2025 19:12:25 GMT  
		Size: 40.6 MB (40577381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcd0baf964989410636494b1ddc87ab90d9e2ebc51a7163bb7fcafa580adab11`  
		Last Modified: Tue, 12 Aug 2025 19:12:26 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:039b25bac32d91caa2ff2cbfc625519c9a25a1a41706f050049f338249171304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.6 MB (596569696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cdae1dbefdb56fb0b3f154720e444e7224839e351e444eae6289d7e2f35e30a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=arm64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=17.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce88273e085fc69344868d25a6ded0d7c2a35a130e9a62ee6ca1b47d36e956e`  
		Last Modified: Tue, 12 Aug 2025 22:14:27 GMT  
		Size: 231.2 MB (231162497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3b2046d4217a5ce0b9be5cb2c6eae5b8af1c71160703bc13823365076ca1c4`  
		Last Modified: Tue, 12 Aug 2025 20:45:51 GMT  
		Size: 2.5 MB (2516790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e75e3cb4ce125c29316f7c6787874fad553b5ff95ba996742bab5b6c2a9f753`  
		Last Modified: Tue, 12 Aug 2025 20:45:50 GMT  
		Size: 480.4 KB (480392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd96c49cf9a0b172e83f4499ef37dbe94f85fe73bac13d4fc3f08082e6d44824`  
		Last Modified: Tue, 12 Aug 2025 22:14:24 GMT  
		Size: 335.0 MB (335048333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1395e4ee60eef1c9276516160a141135c24aef7623055e77fc673aaf63ca7ea9`  
		Last Modified: Tue, 12 Aug 2025 20:45:50 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819237bd520c3436c205b96a2a4df9f8c754a03550b5b736a19788da7d63dbec`  
		Last Modified: Tue, 12 Aug 2025 20:45:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebff89376f351610c5e8bc1b8611f0608f8eebc2f1297cc4a549135ed087aca2`  
		Last Modified: Tue, 12 Aug 2025 20:45:50 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b1426f083e75adc0f75d32a3ac49f4252baed65920e4e162ca7bba312af955`  
		Last Modified: Tue, 12 Aug 2025 20:45:51 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:76e441c607d0a1bef91f378dba1c50491465d3d7c0ad95145ec2079313a7e709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40610874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5458dacce5c83264d71c21212dd32f954cc8bf7721d5f4cd6a919ad9997ee045`

```dockerfile
```

-	Layers:
	-	`sha256:23576acc0d884460b19f8128912e0bc29a6eed01edda4188e32979a2df62d76e`  
		Last Modified: Tue, 12 Aug 2025 22:13:09 GMT  
		Size: 40.6 MB (40583888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c09bd52a2f56ad1b7f21478a835da8a94c3022ecfd801a9004e0ac7f32535a8`  
		Last Modified: Tue, 12 Aug 2025 22:13:10 GMT  
		Size: 27.0 KB (26986 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:a1a056cf15c56b99b0ce557a4a3f8546fcd7561a7ade091a1695b2c86ff01ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.2 MB (618190059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ecbc9b5416588797150de487b1edf757cec96a89eccb6f1bea7c061cda378fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=ppc64le
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=17.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626289f98e141fb35911a2db7b56f0b3c17a927e40fa18d5e75bfe052c0334f1`  
		Last Modified: Tue, 12 Aug 2025 21:58:18 GMT  
		Size: 243.3 MB (243258260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cdf06f3cc41682478576d9ab4e57e6aea676b7a0da14b27a1630b502b0efb7`  
		Last Modified: Tue, 12 Aug 2025 21:59:01 GMT  
		Size: 2.8 MB (2841625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382e4f5f1a6345078ca3cbd61de82e153c765494f47a58a72ff3196627a527ad`  
		Last Modified: Tue, 12 Aug 2025 21:59:01 GMT  
		Size: 480.4 KB (480416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91591a8a8ae8b2ced71d4d9cd42d4c1b7cc1e10e78073783da1b4bd27720a799`  
		Last Modified: Tue, 12 Aug 2025 21:58:21 GMT  
		Size: 337.2 MB (337164178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2039f8d6faaa3ac3c4e518d26c35cf10d078007c291d73a04418993155656c1f`  
		Last Modified: Tue, 12 Aug 2025 21:59:00 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf24035b3b6735db9751221db7d9feb7703e35bfa166659d356a246fc19b69b4`  
		Last Modified: Tue, 12 Aug 2025 21:59:01 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a56ff198f3964c2afcabb4dfd84ee898c115819d6abf5cd4a07e83d3c7d60a`  
		Last Modified: Tue, 12 Aug 2025 22:20:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6142daf3732c08182052152edc1cfa1b10e78c0d97a285f18991504240d3cae`  
		Last Modified: Tue, 12 Aug 2025 22:20:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b76a91f79952fb18ff66d6c1e4c5b982382910e16446ca7f2422164c6721d13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40612879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f4177b3d6d0416a6c7724f175a7b14331464748c26248d20fe8a6f21af0338`

```dockerfile
```

-	Layers:
	-	`sha256:8c1fda861a67e50265e4a6c03670368dad9c43cab523ab6417727c166bc5eaa9`  
		Last Modified: Wed, 13 Aug 2025 01:14:09 GMT  
		Size: 40.6 MB (40585988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfb9a143b9b1dca8dbe14382575330833f71069d471256c3f157942d6233a11a`  
		Last Modified: Wed, 13 Aug 2025 01:14:11 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250807`

```console
$ docker pull odoo@sha256:940c07327d62d00f831f7a98cf05dcd396552adf8c73e43d2d8a6bbdcf15e183
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250807` - linux; amd64

```console
$ docker pull odoo@sha256:8fffbe49db153db59d6e2b04965b2d607e66061d6148828e9fb2dcf5f331f53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.8 MB (601791509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b54a375ad61bb5f654d6d6905dc4add3d6c25c21da82f9162e7c7960f8c3b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=amd64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=17.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a642c4eed8f93f91e9b334f783a4f079d8c55c3f772596d26a05ce69c4784ec`  
		Last Modified: Tue, 12 Aug 2025 19:12:37 GMT  
		Size: 233.8 MB (233790834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17634efc9be4636787e671664ae378da7e735d45196c48c5d4ae7551749c1214`  
		Last Modified: Tue, 12 Aug 2025 17:30:10 GMT  
		Size: 2.5 MB (2523056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96843a23a809cc9571e82e3cf72631db4b3861204b8cd73bb0508b0bb971d1ed`  
		Last Modified: Tue, 12 Aug 2025 17:30:12 GMT  
		Size: 480.5 KB (480472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c463ee4230390dce981ebe526254127fc19600495ed9d9c870a103280ae8c0f2`  
		Last Modified: Tue, 12 Aug 2025 19:12:35 GMT  
		Size: 335.5 MB (335457715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f207422b9af943af65c009a7917e874209c05bfb18bce7d979292f9fefac1`  
		Last Modified: Tue, 12 Aug 2025 17:30:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4eeb620bca1430ca1e98511a88c10d4fa7802ab7cbb93c4848a9bddcacefc69`  
		Last Modified: Tue, 12 Aug 2025 17:30:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0eb4f52e16cf48e33ba3811d97ba2f7c6952307ac09e05dbc86c3c9755e6ba`  
		Last Modified: Tue, 12 Aug 2025 17:30:13 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a996c305ae6ef0d7ba7445015dca436a813c79323da8276422ee7b66854e4`  
		Last Modified: Tue, 12 Aug 2025 17:30:12 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250807` - unknown; unknown

```console
$ docker pull odoo@sha256:4d0fbfc5d178aae3bde41f226b131ce0a29e27c35ab232eff9ae19b32f38add5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40604216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb0e075852c6172f89b7ae511d33d4b4c6327bbdf8c4dc5dc68f6d844e29ee8`

```dockerfile
```

-	Layers:
	-	`sha256:74820c554c29d5214c10886aeb3a08e5cacfc3f5456c1f3f9ff1169ade227e1a`  
		Last Modified: Tue, 12 Aug 2025 19:12:25 GMT  
		Size: 40.6 MB (40577381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcd0baf964989410636494b1ddc87ab90d9e2ebc51a7163bb7fcafa580adab11`  
		Last Modified: Tue, 12 Aug 2025 19:12:26 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250807` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:039b25bac32d91caa2ff2cbfc625519c9a25a1a41706f050049f338249171304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.6 MB (596569696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cdae1dbefdb56fb0b3f154720e444e7224839e351e444eae6289d7e2f35e30a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=arm64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=17.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce88273e085fc69344868d25a6ded0d7c2a35a130e9a62ee6ca1b47d36e956e`  
		Last Modified: Tue, 12 Aug 2025 22:14:27 GMT  
		Size: 231.2 MB (231162497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3b2046d4217a5ce0b9be5cb2c6eae5b8af1c71160703bc13823365076ca1c4`  
		Last Modified: Tue, 12 Aug 2025 20:45:51 GMT  
		Size: 2.5 MB (2516790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e75e3cb4ce125c29316f7c6787874fad553b5ff95ba996742bab5b6c2a9f753`  
		Last Modified: Tue, 12 Aug 2025 20:45:50 GMT  
		Size: 480.4 KB (480392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd96c49cf9a0b172e83f4499ef37dbe94f85fe73bac13d4fc3f08082e6d44824`  
		Last Modified: Tue, 12 Aug 2025 22:14:24 GMT  
		Size: 335.0 MB (335048333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1395e4ee60eef1c9276516160a141135c24aef7623055e77fc673aaf63ca7ea9`  
		Last Modified: Tue, 12 Aug 2025 20:45:50 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819237bd520c3436c205b96a2a4df9f8c754a03550b5b736a19788da7d63dbec`  
		Last Modified: Tue, 12 Aug 2025 20:45:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebff89376f351610c5e8bc1b8611f0608f8eebc2f1297cc4a549135ed087aca2`  
		Last Modified: Tue, 12 Aug 2025 20:45:50 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b1426f083e75adc0f75d32a3ac49f4252baed65920e4e162ca7bba312af955`  
		Last Modified: Tue, 12 Aug 2025 20:45:51 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250807` - unknown; unknown

```console
$ docker pull odoo@sha256:76e441c607d0a1bef91f378dba1c50491465d3d7c0ad95145ec2079313a7e709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40610874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5458dacce5c83264d71c21212dd32f954cc8bf7721d5f4cd6a919ad9997ee045`

```dockerfile
```

-	Layers:
	-	`sha256:23576acc0d884460b19f8128912e0bc29a6eed01edda4188e32979a2df62d76e`  
		Last Modified: Tue, 12 Aug 2025 22:13:09 GMT  
		Size: 40.6 MB (40583888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c09bd52a2f56ad1b7f21478a835da8a94c3022ecfd801a9004e0ac7f32535a8`  
		Last Modified: Tue, 12 Aug 2025 22:13:10 GMT  
		Size: 27.0 KB (26986 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250807` - linux; ppc64le

```console
$ docker pull odoo@sha256:a1a056cf15c56b99b0ce557a4a3f8546fcd7561a7ade091a1695b2c86ff01ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.2 MB (618190059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ecbc9b5416588797150de487b1edf757cec96a89eccb6f1bea7c061cda378fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=ppc64le
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=17.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=060dbebfa0acc3f69fb3a458c2ce7b732a9624ed
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626289f98e141fb35911a2db7b56f0b3c17a927e40fa18d5e75bfe052c0334f1`  
		Last Modified: Tue, 12 Aug 2025 21:58:18 GMT  
		Size: 243.3 MB (243258260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cdf06f3cc41682478576d9ab4e57e6aea676b7a0da14b27a1630b502b0efb7`  
		Last Modified: Tue, 12 Aug 2025 21:59:01 GMT  
		Size: 2.8 MB (2841625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382e4f5f1a6345078ca3cbd61de82e153c765494f47a58a72ff3196627a527ad`  
		Last Modified: Tue, 12 Aug 2025 21:59:01 GMT  
		Size: 480.4 KB (480416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91591a8a8ae8b2ced71d4d9cd42d4c1b7cc1e10e78073783da1b4bd27720a799`  
		Last Modified: Tue, 12 Aug 2025 21:58:21 GMT  
		Size: 337.2 MB (337164178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2039f8d6faaa3ac3c4e518d26c35cf10d078007c291d73a04418993155656c1f`  
		Last Modified: Tue, 12 Aug 2025 21:59:00 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf24035b3b6735db9751221db7d9feb7703e35bfa166659d356a246fc19b69b4`  
		Last Modified: Tue, 12 Aug 2025 21:59:01 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a56ff198f3964c2afcabb4dfd84ee898c115819d6abf5cd4a07e83d3c7d60a`  
		Last Modified: Tue, 12 Aug 2025 22:20:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6142daf3732c08182052152edc1cfa1b10e78c0d97a285f18991504240d3cae`  
		Last Modified: Tue, 12 Aug 2025 22:20:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250807` - unknown; unknown

```console
$ docker pull odoo@sha256:b76a91f79952fb18ff66d6c1e4c5b982382910e16446ca7f2422164c6721d13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40612879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f4177b3d6d0416a6c7724f175a7b14331464748c26248d20fe8a6f21af0338`

```dockerfile
```

-	Layers:
	-	`sha256:8c1fda861a67e50265e4a6c03670368dad9c43cab523ab6417727c166bc5eaa9`  
		Last Modified: Wed, 13 Aug 2025 01:14:09 GMT  
		Size: 40.6 MB (40585988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfb9a143b9b1dca8dbe14382575330833f71069d471256c3f157942d6233a11a`  
		Last Modified: Wed, 13 Aug 2025 01:14:11 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:bff2d10c97db4d6d826101529b65c61582aff062c834487bb507de982ac2babe
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
$ docker pull odoo@sha256:e3803df4f6f59e9eb3af06ba91ab93a5ab32a273b232098e12743d4d361b566b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.0 MB (674003611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508cd74923ac0568631614ea1ddc5457cd52113e02c33dae291cd31cad39b68d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=amd64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accf4b26ed7e3e5c5b84fbf89bfc86248b4c665c4fb30c6a74e463534c33b58`  
		Last Modified: Tue, 12 Aug 2025 19:12:38 GMT  
		Size: 254.5 MB (254530516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2176b418081e2721380771959bc1b12d3c8728d7fa02c1316cde9a5c6c6247ce`  
		Last Modified: Tue, 12 Aug 2025 17:30:44 GMT  
		Size: 14.3 MB (14278771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ac922f01760b0a9115ba91cba0155732ddf2258b4dd72288b3299164c57020`  
		Last Modified: Tue, 12 Aug 2025 17:30:42 GMT  
		Size: 480.1 KB (480132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c5ba8e0365575c942ddaa4167de5c0a81d3c6c0bf4460c269d0244b1f63851`  
		Last Modified: Tue, 12 Aug 2025 19:12:52 GMT  
		Size: 375.0 MB (374988540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c53c69b31c47987de2cfb037f2f65ee596ff88a00ce9aef19ebb750bf410ec4`  
		Last Modified: Tue, 12 Aug 2025 17:30:42 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493eddf4be7d1512a1ed528cc103177d27fdc3ba10902649218a66c6d1d144be`  
		Last Modified: Tue, 12 Aug 2025 17:30:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a47cc9a432173b06e2d8d8ce26457fd3d96bfed1d2a757273f8c12684db41`  
		Last Modified: Tue, 12 Aug 2025 17:30:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3a1510b3f668365be526d9cdc9257642f900a8619e6cf2468e3fe5f480e57b`  
		Last Modified: Tue, 12 Aug 2025 17:30:43 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:1b425bf9f60c1383e1de1ea8073ff951eb77cdc0e15407fbbe12a693d83d62b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60385898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c27612093385e6379c074bb1356b73312241f804049fa0bdfad689ebc7974b3`

```dockerfile
```

-	Layers:
	-	`sha256:d98aa73edc52453b66ec0f9e145eece3ed5238aae097a7fc868c246599d74049`  
		Last Modified: Tue, 12 Aug 2025 19:12:37 GMT  
		Size: 60.4 MB (60358762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64241b26990c53c81ac1272f9633df61332ef9548c68829afa7403f6a48e292f`  
		Last Modified: Tue, 12 Aug 2025 19:12:39 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:632b7bc2f048d05d463871938c756a1972277870aa008908d9aa300c540e86c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.3 MB (670319862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ad8262d1021aac0cce7be0384c6dee32cfaed21df2b345fe278d0f137ba425`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=arm64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2764d0a9b08cd6785f635910b8b7041adad61b07a594dd5b23b6d2793a602dd2`  
		Last Modified: Tue, 12 Aug 2025 22:09:59 GMT  
		Size: 251.9 MB (251921170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7963f4ce4532e2502d9dfa67c6fb986fa82c85a20326424d1cdcb047eede11e1`  
		Last Modified: Tue, 12 Aug 2025 20:40:42 GMT  
		Size: 14.3 MB (14251480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f57579d763d41f9ae309265ddfebee357b820141f0264b195b5b6185d1dd6c7`  
		Last Modified: Tue, 12 Aug 2025 20:40:40 GMT  
		Size: 480.1 KB (480126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3099773024177c6c3f30215f36699234f4ab6a5e4851ca7d24dd70db4f1996a`  
		Last Modified: Tue, 12 Aug 2025 22:09:56 GMT  
		Size: 374.8 MB (374804270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f7e30f732e5f0e5949a1583a6a1082ae8df65c789119a298664d8ef385a434`  
		Last Modified: Tue, 12 Aug 2025 20:40:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3d0cfc4fbd6a3b9c9380b0523f2a4b17b2533df6af61a76d0682f6bd658807`  
		Last Modified: Tue, 12 Aug 2025 20:40:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a3425b88c5c863415ec3d7c70f3bc5213cf2ea07a7140c5916e2c21041b0ac`  
		Last Modified: Tue, 12 Aug 2025 20:40:38 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeed5d61ff5e56098420386065e25b4f189c29e83b2d094117b34b8cb9db1db`  
		Last Modified: Tue, 12 Aug 2025 20:40:38 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:2709ef27f5e9fe2bec68c310d3ae784f397da1643a077cd8b521a0e8596f3680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60393349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ee25d07ef32f4fe579e359dbde0f1bd60923ea99bd853b476b5d3b16bca9e6`

```dockerfile
```

-	Layers:
	-	`sha256:7c037936d62db2bae70d6024c437de423660698127c61ed2661e96aa690bc384`  
		Last Modified: Tue, 12 Aug 2025 22:13:55 GMT  
		Size: 60.4 MB (60366049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c72c3115490767d39955b1ebfd87b4a2d9549747281c6cb7ea3c4626c5cdcd3`  
		Last Modified: Tue, 12 Aug 2025 22:13:56 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:5e44c86c4f414802eac453bc3a155e9d83eda1e91910add74739e9901a12419a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.2 MB (690211412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dd3b59ae2458d7fe470460d0deefbe1d978d76ba2ae53025229b252b362a59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=ppc64le
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8e1b71885275c9037021a1e76c0de6560cdb71c38eed5464a2419672a55c7`  
		Last Modified: Tue, 12 Aug 2025 23:57:11 GMT  
		Size: 265.1 MB (265079104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4c31c6a80b9102241199be421cee9a2b20c894d2c54e87966647a8a08c57ed`  
		Last Modified: Tue, 12 Aug 2025 21:50:19 GMT  
		Size: 14.8 MB (14799313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70be03624557107effd816b3630b381559527486baefffc70199ca239a131e91`  
		Last Modified: Tue, 12 Aug 2025 21:50:18 GMT  
		Size: 480.2 KB (480159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b361057008ab9435a3cf5d577205e9d3320f115498fceb21c16cada4f59b7b`  
		Last Modified: Tue, 12 Aug 2025 23:57:25 GMT  
		Size: 375.5 MB (375520750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd37cc5f80df8bffca588f9788e6fca89bbca0d41f68525fe2310d2f66ea13e`  
		Last Modified: Tue, 12 Aug 2025 21:50:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468bfea56c41eb82faa1de8fa4fbc1383cb7ed73eaa8399bf7ed02223d24992f`  
		Last Modified: Tue, 12 Aug 2025 21:50:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166c6d4202ce571d1cd3d00b316e0ec4a878866467dca3d685d427088009cdaf`  
		Last Modified: Tue, 12 Aug 2025 21:50:19 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4ba0ad3a2d97611fdc156d3a3311617026e7e4d25e0b1854e126dc1bfda12b`  
		Last Modified: Tue, 12 Aug 2025 21:50:19 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:54cc9a884dba006717cbdb7e754d5a97649aba260603dfd76e21878ec1d4e03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60394349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d401abd63a3a9cfb7ac624ca071b8f64c93499b7bc662aa69b3abf65e82759e`

```dockerfile
```

-	Layers:
	-	`sha256:5244aca5118b3df44c8214965fd5816709cbc308f31d0cda619081430e540e11`  
		Last Modified: Wed, 13 Aug 2025 01:15:15 GMT  
		Size: 60.4 MB (60367151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898d27cb5a60400e6f7dc8af1d212836393510d6716dd345dd159e98e827a3f2`  
		Last Modified: Wed, 13 Aug 2025 01:15:16 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:bff2d10c97db4d6d826101529b65c61582aff062c834487bb507de982ac2babe
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
$ docker pull odoo@sha256:e3803df4f6f59e9eb3af06ba91ab93a5ab32a273b232098e12743d4d361b566b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.0 MB (674003611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508cd74923ac0568631614ea1ddc5457cd52113e02c33dae291cd31cad39b68d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=amd64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accf4b26ed7e3e5c5b84fbf89bfc86248b4c665c4fb30c6a74e463534c33b58`  
		Last Modified: Tue, 12 Aug 2025 19:12:38 GMT  
		Size: 254.5 MB (254530516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2176b418081e2721380771959bc1b12d3c8728d7fa02c1316cde9a5c6c6247ce`  
		Last Modified: Tue, 12 Aug 2025 17:30:44 GMT  
		Size: 14.3 MB (14278771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ac922f01760b0a9115ba91cba0155732ddf2258b4dd72288b3299164c57020`  
		Last Modified: Tue, 12 Aug 2025 17:30:42 GMT  
		Size: 480.1 KB (480132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c5ba8e0365575c942ddaa4167de5c0a81d3c6c0bf4460c269d0244b1f63851`  
		Last Modified: Tue, 12 Aug 2025 19:12:52 GMT  
		Size: 375.0 MB (374988540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c53c69b31c47987de2cfb037f2f65ee596ff88a00ce9aef19ebb750bf410ec4`  
		Last Modified: Tue, 12 Aug 2025 17:30:42 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493eddf4be7d1512a1ed528cc103177d27fdc3ba10902649218a66c6d1d144be`  
		Last Modified: Tue, 12 Aug 2025 17:30:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a47cc9a432173b06e2d8d8ce26457fd3d96bfed1d2a757273f8c12684db41`  
		Last Modified: Tue, 12 Aug 2025 17:30:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3a1510b3f668365be526d9cdc9257642f900a8619e6cf2468e3fe5f480e57b`  
		Last Modified: Tue, 12 Aug 2025 17:30:43 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1b425bf9f60c1383e1de1ea8073ff951eb77cdc0e15407fbbe12a693d83d62b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60385898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c27612093385e6379c074bb1356b73312241f804049fa0bdfad689ebc7974b3`

```dockerfile
```

-	Layers:
	-	`sha256:d98aa73edc52453b66ec0f9e145eece3ed5238aae097a7fc868c246599d74049`  
		Last Modified: Tue, 12 Aug 2025 19:12:37 GMT  
		Size: 60.4 MB (60358762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64241b26990c53c81ac1272f9633df61332ef9548c68829afa7403f6a48e292f`  
		Last Modified: Tue, 12 Aug 2025 19:12:39 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:632b7bc2f048d05d463871938c756a1972277870aa008908d9aa300c540e86c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.3 MB (670319862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ad8262d1021aac0cce7be0384c6dee32cfaed21df2b345fe278d0f137ba425`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=arm64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2764d0a9b08cd6785f635910b8b7041adad61b07a594dd5b23b6d2793a602dd2`  
		Last Modified: Tue, 12 Aug 2025 22:09:59 GMT  
		Size: 251.9 MB (251921170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7963f4ce4532e2502d9dfa67c6fb986fa82c85a20326424d1cdcb047eede11e1`  
		Last Modified: Tue, 12 Aug 2025 20:40:42 GMT  
		Size: 14.3 MB (14251480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f57579d763d41f9ae309265ddfebee357b820141f0264b195b5b6185d1dd6c7`  
		Last Modified: Tue, 12 Aug 2025 20:40:40 GMT  
		Size: 480.1 KB (480126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3099773024177c6c3f30215f36699234f4ab6a5e4851ca7d24dd70db4f1996a`  
		Last Modified: Tue, 12 Aug 2025 22:09:56 GMT  
		Size: 374.8 MB (374804270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f7e30f732e5f0e5949a1583a6a1082ae8df65c789119a298664d8ef385a434`  
		Last Modified: Tue, 12 Aug 2025 20:40:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3d0cfc4fbd6a3b9c9380b0523f2a4b17b2533df6af61a76d0682f6bd658807`  
		Last Modified: Tue, 12 Aug 2025 20:40:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a3425b88c5c863415ec3d7c70f3bc5213cf2ea07a7140c5916e2c21041b0ac`  
		Last Modified: Tue, 12 Aug 2025 20:40:38 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeed5d61ff5e56098420386065e25b4f189c29e83b2d094117b34b8cb9db1db`  
		Last Modified: Tue, 12 Aug 2025 20:40:38 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2709ef27f5e9fe2bec68c310d3ae784f397da1643a077cd8b521a0e8596f3680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60393349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ee25d07ef32f4fe579e359dbde0f1bd60923ea99bd853b476b5d3b16bca9e6`

```dockerfile
```

-	Layers:
	-	`sha256:7c037936d62db2bae70d6024c437de423660698127c61ed2661e96aa690bc384`  
		Last Modified: Tue, 12 Aug 2025 22:13:55 GMT  
		Size: 60.4 MB (60366049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c72c3115490767d39955b1ebfd87b4a2d9549747281c6cb7ea3c4626c5cdcd3`  
		Last Modified: Tue, 12 Aug 2025 22:13:56 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:5e44c86c4f414802eac453bc3a155e9d83eda1e91910add74739e9901a12419a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.2 MB (690211412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dd3b59ae2458d7fe470460d0deefbe1d978d76ba2ae53025229b252b362a59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=ppc64le
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8e1b71885275c9037021a1e76c0de6560cdb71c38eed5464a2419672a55c7`  
		Last Modified: Tue, 12 Aug 2025 23:57:11 GMT  
		Size: 265.1 MB (265079104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4c31c6a80b9102241199be421cee9a2b20c894d2c54e87966647a8a08c57ed`  
		Last Modified: Tue, 12 Aug 2025 21:50:19 GMT  
		Size: 14.8 MB (14799313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70be03624557107effd816b3630b381559527486baefffc70199ca239a131e91`  
		Last Modified: Tue, 12 Aug 2025 21:50:18 GMT  
		Size: 480.2 KB (480159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b361057008ab9435a3cf5d577205e9d3320f115498fceb21c16cada4f59b7b`  
		Last Modified: Tue, 12 Aug 2025 23:57:25 GMT  
		Size: 375.5 MB (375520750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd37cc5f80df8bffca588f9788e6fca89bbca0d41f68525fe2310d2f66ea13e`  
		Last Modified: Tue, 12 Aug 2025 21:50:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468bfea56c41eb82faa1de8fa4fbc1383cb7ed73eaa8399bf7ed02223d24992f`  
		Last Modified: Tue, 12 Aug 2025 21:50:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166c6d4202ce571d1cd3d00b316e0ec4a878866467dca3d685d427088009cdaf`  
		Last Modified: Tue, 12 Aug 2025 21:50:19 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4ba0ad3a2d97611fdc156d3a3311617026e7e4d25e0b1854e126dc1bfda12b`  
		Last Modified: Tue, 12 Aug 2025 21:50:19 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:54cc9a884dba006717cbdb7e754d5a97649aba260603dfd76e21878ec1d4e03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60394349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d401abd63a3a9cfb7ac624ca071b8f64c93499b7bc662aa69b3abf65e82759e`

```dockerfile
```

-	Layers:
	-	`sha256:5244aca5118b3df44c8214965fd5816709cbc308f31d0cda619081430e540e11`  
		Last Modified: Wed, 13 Aug 2025 01:15:15 GMT  
		Size: 60.4 MB (60367151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898d27cb5a60400e6f7dc8af1d212836393510d6716dd345dd159e98e827a3f2`  
		Last Modified: Wed, 13 Aug 2025 01:15:16 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250807`

```console
$ docker pull odoo@sha256:bff2d10c97db4d6d826101529b65c61582aff062c834487bb507de982ac2babe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250807` - linux; amd64

```console
$ docker pull odoo@sha256:e3803df4f6f59e9eb3af06ba91ab93a5ab32a273b232098e12743d4d361b566b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.0 MB (674003611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508cd74923ac0568631614ea1ddc5457cd52113e02c33dae291cd31cad39b68d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=amd64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accf4b26ed7e3e5c5b84fbf89bfc86248b4c665c4fb30c6a74e463534c33b58`  
		Last Modified: Tue, 12 Aug 2025 19:12:38 GMT  
		Size: 254.5 MB (254530516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2176b418081e2721380771959bc1b12d3c8728d7fa02c1316cde9a5c6c6247ce`  
		Last Modified: Tue, 12 Aug 2025 17:30:44 GMT  
		Size: 14.3 MB (14278771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ac922f01760b0a9115ba91cba0155732ddf2258b4dd72288b3299164c57020`  
		Last Modified: Tue, 12 Aug 2025 17:30:42 GMT  
		Size: 480.1 KB (480132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c5ba8e0365575c942ddaa4167de5c0a81d3c6c0bf4460c269d0244b1f63851`  
		Last Modified: Tue, 12 Aug 2025 19:12:52 GMT  
		Size: 375.0 MB (374988540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c53c69b31c47987de2cfb037f2f65ee596ff88a00ce9aef19ebb750bf410ec4`  
		Last Modified: Tue, 12 Aug 2025 17:30:42 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493eddf4be7d1512a1ed528cc103177d27fdc3ba10902649218a66c6d1d144be`  
		Last Modified: Tue, 12 Aug 2025 17:30:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a47cc9a432173b06e2d8d8ce26457fd3d96bfed1d2a757273f8c12684db41`  
		Last Modified: Tue, 12 Aug 2025 17:30:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3a1510b3f668365be526d9cdc9257642f900a8619e6cf2468e3fe5f480e57b`  
		Last Modified: Tue, 12 Aug 2025 17:30:43 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250807` - unknown; unknown

```console
$ docker pull odoo@sha256:1b425bf9f60c1383e1de1ea8073ff951eb77cdc0e15407fbbe12a693d83d62b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60385898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c27612093385e6379c074bb1356b73312241f804049fa0bdfad689ebc7974b3`

```dockerfile
```

-	Layers:
	-	`sha256:d98aa73edc52453b66ec0f9e145eece3ed5238aae097a7fc868c246599d74049`  
		Last Modified: Tue, 12 Aug 2025 19:12:37 GMT  
		Size: 60.4 MB (60358762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64241b26990c53c81ac1272f9633df61332ef9548c68829afa7403f6a48e292f`  
		Last Modified: Tue, 12 Aug 2025 19:12:39 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250807` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:632b7bc2f048d05d463871938c756a1972277870aa008908d9aa300c540e86c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.3 MB (670319862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ad8262d1021aac0cce7be0384c6dee32cfaed21df2b345fe278d0f137ba425`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=arm64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2764d0a9b08cd6785f635910b8b7041adad61b07a594dd5b23b6d2793a602dd2`  
		Last Modified: Tue, 12 Aug 2025 22:09:59 GMT  
		Size: 251.9 MB (251921170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7963f4ce4532e2502d9dfa67c6fb986fa82c85a20326424d1cdcb047eede11e1`  
		Last Modified: Tue, 12 Aug 2025 20:40:42 GMT  
		Size: 14.3 MB (14251480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f57579d763d41f9ae309265ddfebee357b820141f0264b195b5b6185d1dd6c7`  
		Last Modified: Tue, 12 Aug 2025 20:40:40 GMT  
		Size: 480.1 KB (480126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3099773024177c6c3f30215f36699234f4ab6a5e4851ca7d24dd70db4f1996a`  
		Last Modified: Tue, 12 Aug 2025 22:09:56 GMT  
		Size: 374.8 MB (374804270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f7e30f732e5f0e5949a1583a6a1082ae8df65c789119a298664d8ef385a434`  
		Last Modified: Tue, 12 Aug 2025 20:40:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3d0cfc4fbd6a3b9c9380b0523f2a4b17b2533df6af61a76d0682f6bd658807`  
		Last Modified: Tue, 12 Aug 2025 20:40:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a3425b88c5c863415ec3d7c70f3bc5213cf2ea07a7140c5916e2c21041b0ac`  
		Last Modified: Tue, 12 Aug 2025 20:40:38 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeed5d61ff5e56098420386065e25b4f189c29e83b2d094117b34b8cb9db1db`  
		Last Modified: Tue, 12 Aug 2025 20:40:38 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250807` - unknown; unknown

```console
$ docker pull odoo@sha256:2709ef27f5e9fe2bec68c310d3ae784f397da1643a077cd8b521a0e8596f3680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60393349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ee25d07ef32f4fe579e359dbde0f1bd60923ea99bd853b476b5d3b16bca9e6`

```dockerfile
```

-	Layers:
	-	`sha256:7c037936d62db2bae70d6024c437de423660698127c61ed2661e96aa690bc384`  
		Last Modified: Tue, 12 Aug 2025 22:13:55 GMT  
		Size: 60.4 MB (60366049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c72c3115490767d39955b1ebfd87b4a2d9549747281c6cb7ea3c4626c5cdcd3`  
		Last Modified: Tue, 12 Aug 2025 22:13:56 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250807` - linux; ppc64le

```console
$ docker pull odoo@sha256:5e44c86c4f414802eac453bc3a155e9d83eda1e91910add74739e9901a12419a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.2 MB (690211412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dd3b59ae2458d7fe470460d0deefbe1d978d76ba2ae53025229b252b362a59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=ppc64le
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8e1b71885275c9037021a1e76c0de6560cdb71c38eed5464a2419672a55c7`  
		Last Modified: Tue, 12 Aug 2025 23:57:11 GMT  
		Size: 265.1 MB (265079104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4c31c6a80b9102241199be421cee9a2b20c894d2c54e87966647a8a08c57ed`  
		Last Modified: Tue, 12 Aug 2025 21:50:19 GMT  
		Size: 14.8 MB (14799313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70be03624557107effd816b3630b381559527486baefffc70199ca239a131e91`  
		Last Modified: Tue, 12 Aug 2025 21:50:18 GMT  
		Size: 480.2 KB (480159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b361057008ab9435a3cf5d577205e9d3320f115498fceb21c16cada4f59b7b`  
		Last Modified: Tue, 12 Aug 2025 23:57:25 GMT  
		Size: 375.5 MB (375520750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd37cc5f80df8bffca588f9788e6fca89bbca0d41f68525fe2310d2f66ea13e`  
		Last Modified: Tue, 12 Aug 2025 21:50:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468bfea56c41eb82faa1de8fa4fbc1383cb7ed73eaa8399bf7ed02223d24992f`  
		Last Modified: Tue, 12 Aug 2025 21:50:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166c6d4202ce571d1cd3d00b316e0ec4a878866467dca3d685d427088009cdaf`  
		Last Modified: Tue, 12 Aug 2025 21:50:19 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4ba0ad3a2d97611fdc156d3a3311617026e7e4d25e0b1854e126dc1bfda12b`  
		Last Modified: Tue, 12 Aug 2025 21:50:19 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250807` - unknown; unknown

```console
$ docker pull odoo@sha256:54cc9a884dba006717cbdb7e754d5a97649aba260603dfd76e21878ec1d4e03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60394349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d401abd63a3a9cfb7ac624ca071b8f64c93499b7bc662aa69b3abf65e82759e`

```dockerfile
```

-	Layers:
	-	`sha256:5244aca5118b3df44c8214965fd5816709cbc308f31d0cda619081430e540e11`  
		Last Modified: Wed, 13 Aug 2025 01:15:15 GMT  
		Size: 60.4 MB (60367151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898d27cb5a60400e6f7dc8af1d212836393510d6716dd345dd159e98e827a3f2`  
		Last Modified: Wed, 13 Aug 2025 01:15:16 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:bff2d10c97db4d6d826101529b65c61582aff062c834487bb507de982ac2babe
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
$ docker pull odoo@sha256:e3803df4f6f59e9eb3af06ba91ab93a5ab32a273b232098e12743d4d361b566b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.0 MB (674003611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508cd74923ac0568631614ea1ddc5457cd52113e02c33dae291cd31cad39b68d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=amd64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accf4b26ed7e3e5c5b84fbf89bfc86248b4c665c4fb30c6a74e463534c33b58`  
		Last Modified: Tue, 12 Aug 2025 19:12:38 GMT  
		Size: 254.5 MB (254530516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2176b418081e2721380771959bc1b12d3c8728d7fa02c1316cde9a5c6c6247ce`  
		Last Modified: Tue, 12 Aug 2025 17:30:44 GMT  
		Size: 14.3 MB (14278771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ac922f01760b0a9115ba91cba0155732ddf2258b4dd72288b3299164c57020`  
		Last Modified: Tue, 12 Aug 2025 17:30:42 GMT  
		Size: 480.1 KB (480132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c5ba8e0365575c942ddaa4167de5c0a81d3c6c0bf4460c269d0244b1f63851`  
		Last Modified: Tue, 12 Aug 2025 19:12:52 GMT  
		Size: 375.0 MB (374988540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c53c69b31c47987de2cfb037f2f65ee596ff88a00ce9aef19ebb750bf410ec4`  
		Last Modified: Tue, 12 Aug 2025 17:30:42 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493eddf4be7d1512a1ed528cc103177d27fdc3ba10902649218a66c6d1d144be`  
		Last Modified: Tue, 12 Aug 2025 17:30:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a47cc9a432173b06e2d8d8ce26457fd3d96bfed1d2a757273f8c12684db41`  
		Last Modified: Tue, 12 Aug 2025 17:30:42 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3a1510b3f668365be526d9cdc9257642f900a8619e6cf2468e3fe5f480e57b`  
		Last Modified: Tue, 12 Aug 2025 17:30:43 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:1b425bf9f60c1383e1de1ea8073ff951eb77cdc0e15407fbbe12a693d83d62b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60385898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c27612093385e6379c074bb1356b73312241f804049fa0bdfad689ebc7974b3`

```dockerfile
```

-	Layers:
	-	`sha256:d98aa73edc52453b66ec0f9e145eece3ed5238aae097a7fc868c246599d74049`  
		Last Modified: Tue, 12 Aug 2025 19:12:37 GMT  
		Size: 60.4 MB (60358762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64241b26990c53c81ac1272f9633df61332ef9548c68829afa7403f6a48e292f`  
		Last Modified: Tue, 12 Aug 2025 19:12:39 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:632b7bc2f048d05d463871938c756a1972277870aa008908d9aa300c540e86c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.3 MB (670319862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ad8262d1021aac0cce7be0384c6dee32cfaed21df2b345fe278d0f137ba425`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=arm64
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2764d0a9b08cd6785f635910b8b7041adad61b07a594dd5b23b6d2793a602dd2`  
		Last Modified: Tue, 12 Aug 2025 22:09:59 GMT  
		Size: 251.9 MB (251921170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7963f4ce4532e2502d9dfa67c6fb986fa82c85a20326424d1cdcb047eede11e1`  
		Last Modified: Tue, 12 Aug 2025 20:40:42 GMT  
		Size: 14.3 MB (14251480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f57579d763d41f9ae309265ddfebee357b820141f0264b195b5b6185d1dd6c7`  
		Last Modified: Tue, 12 Aug 2025 20:40:40 GMT  
		Size: 480.1 KB (480126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3099773024177c6c3f30215f36699234f4ab6a5e4851ca7d24dd70db4f1996a`  
		Last Modified: Tue, 12 Aug 2025 22:09:56 GMT  
		Size: 374.8 MB (374804270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f7e30f732e5f0e5949a1583a6a1082ae8df65c789119a298664d8ef385a434`  
		Last Modified: Tue, 12 Aug 2025 20:40:40 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3d0cfc4fbd6a3b9c9380b0523f2a4b17b2533df6af61a76d0682f6bd658807`  
		Last Modified: Tue, 12 Aug 2025 20:40:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a3425b88c5c863415ec3d7c70f3bc5213cf2ea07a7140c5916e2c21041b0ac`  
		Last Modified: Tue, 12 Aug 2025 20:40:38 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeed5d61ff5e56098420386065e25b4f189c29e83b2d094117b34b8cb9db1db`  
		Last Modified: Tue, 12 Aug 2025 20:40:38 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:2709ef27f5e9fe2bec68c310d3ae784f397da1643a077cd8b521a0e8596f3680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60393349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ee25d07ef32f4fe579e359dbde0f1bd60923ea99bd853b476b5d3b16bca9e6`

```dockerfile
```

-	Layers:
	-	`sha256:7c037936d62db2bae70d6024c437de423660698127c61ed2661e96aa690bc384`  
		Last Modified: Tue, 12 Aug 2025 22:13:55 GMT  
		Size: 60.4 MB (60366049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c72c3115490767d39955b1ebfd87b4a2d9549747281c6cb7ea3c4626c5cdcd3`  
		Last Modified: Tue, 12 Aug 2025 22:13:56 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:5e44c86c4f414802eac453bc3a155e9d83eda1e91910add74739e9901a12419a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.2 MB (690211412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19dd3b59ae2458d7fe470460d0deefbe1d978d76ba2ae53025229b252b362a59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 07:18:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 07 Aug 2025 07:18:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 07:18:18 GMT
ARG TARGETARCH=ppc64le
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_VERSION=18.0
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_RELEASE=20250807
# Thu, 07 Aug 2025 07:18:18 GMT
ARG ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250807 ODOO_SHA=109d077dd280292aa92daf18777cb772e644f972
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 07 Aug 2025 07:18:18 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 07 Aug 2025 07:18:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 07 Aug 2025 07:18:18 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 07 Aug 2025 07:18:18 GMT
USER odoo
# Thu, 07 Aug 2025 07:18:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 Aug 2025 07:18:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8e1b71885275c9037021a1e76c0de6560cdb71c38eed5464a2419672a55c7`  
		Last Modified: Tue, 12 Aug 2025 23:57:11 GMT  
		Size: 265.1 MB (265079104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4c31c6a80b9102241199be421cee9a2b20c894d2c54e87966647a8a08c57ed`  
		Last Modified: Tue, 12 Aug 2025 21:50:19 GMT  
		Size: 14.8 MB (14799313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70be03624557107effd816b3630b381559527486baefffc70199ca239a131e91`  
		Last Modified: Tue, 12 Aug 2025 21:50:18 GMT  
		Size: 480.2 KB (480159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b361057008ab9435a3cf5d577205e9d3320f115498fceb21c16cada4f59b7b`  
		Last Modified: Tue, 12 Aug 2025 23:57:25 GMT  
		Size: 375.5 MB (375520750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd37cc5f80df8bffca588f9788e6fca89bbca0d41f68525fe2310d2f66ea13e`  
		Last Modified: Tue, 12 Aug 2025 21:50:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468bfea56c41eb82faa1de8fa4fbc1383cb7ed73eaa8399bf7ed02223d24992f`  
		Last Modified: Tue, 12 Aug 2025 21:50:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166c6d4202ce571d1cd3d00b316e0ec4a878866467dca3d685d427088009cdaf`  
		Last Modified: Tue, 12 Aug 2025 21:50:19 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4ba0ad3a2d97611fdc156d3a3311617026e7e4d25e0b1854e126dc1bfda12b`  
		Last Modified: Tue, 12 Aug 2025 21:50:19 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:54cc9a884dba006717cbdb7e754d5a97649aba260603dfd76e21878ec1d4e03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60394349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d401abd63a3a9cfb7ac624ca071b8f64c93499b7bc662aa69b3abf65e82759e`

```dockerfile
```

-	Layers:
	-	`sha256:5244aca5118b3df44c8214965fd5816709cbc308f31d0cda619081430e540e11`  
		Last Modified: Wed, 13 Aug 2025 01:15:15 GMT  
		Size: 60.4 MB (60367151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898d27cb5a60400e6f7dc8af1d212836393510d6716dd345dd159e98e827a3f2`  
		Last Modified: Wed, 13 Aug 2025 01:15:16 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
