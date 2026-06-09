<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260609`](#odoo170-20260609)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260609`](#odoo180-20260609)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260609`](#odoo190-20260609)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:67f04958d8a71423cc6d3ccb228b998ef7fb36fe214998c47f52aff975120b32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:2431d50aba410562cb907c717e7849fa37da0e25c809250d3d0a00f3db7d5109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611668656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae689a00ec7bae7c4c18da1a52c86cbbb99ab54d8a5cac0fbc780774198e37e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:58:02 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:58:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:58:02 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:58:02 GMT
ARG TARGETARCH=amd64
# Tue, 09 Jun 2026 17:58:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:58:08 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:58:08 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:58:08 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Jun 2026 17:58:08 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:58:08 GMT
ARG ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
# Tue, 09 Jun 2026 17:59:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:59:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:59:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:59:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
USER odoo
# Tue, 09 Jun 2026 17:59:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:59:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74ec776f8c64f150a0b6fa6c4a66b03b0095cab74cabe701d386821c7fad64c`  
		Last Modified: Tue, 09 Jun 2026 18:00:34 GMT  
		Size: 233.8 MB (233835351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4568750a7eb61dc66f8324576303e7e187c8fdbe432dba33f2c29377a6de843`  
		Last Modified: Tue, 09 Jun 2026 18:00:19 GMT  
		Size: 2.6 MB (2611549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1a612d71e484d2d01f77f60a9210f7f11cc198fde8c57daf507a0cf76f6197`  
		Last Modified: Tue, 09 Jun 2026 18:00:18 GMT  
		Size: 483.8 KB (483825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ceb6c70ed350f6b55a9f1a64d8bf9f4315527d9190cf7f6af0a11bed56726c`  
		Last Modified: Tue, 09 Jun 2026 18:00:37 GMT  
		Size: 345.0 MB (344998456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b42a539ff666391a9501b80a852540f728fa8454f6bfa5aaa0bdbc9ae8a8cb`  
		Last Modified: Tue, 09 Jun 2026 18:00:21 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7149ec469fdec73c85f8ecabcdaba750d932410fe73c560cffcb96428101ad`  
		Last Modified: Tue, 09 Jun 2026 18:00:21 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0142c424d9adda9faad9525f1dd87176086a7d2d511d620a4234a1dc387194`  
		Last Modified: Tue, 09 Jun 2026 18:00:23 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75564abc0cc10b4c529469db68ee158ba8f63c356939c7e7db46dd4ac797bb`  
		Last Modified: Tue, 09 Jun 2026 18:00:23 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:12f0057ebbc0874325c26d3bea65bcfc4f072702ba8f0a92bd9768ed591c533d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43101243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f82aea0471ebda7f2cc8e68220666ce1b6da39104f89420bcc25d364c9ddcc2`

```dockerfile
```

-	Layers:
	-	`sha256:5c223e13fb5ba0ad9a165ee06d3050593aeb7b99ad99661d0f7d28849c1b358a`  
		Last Modified: Tue, 09 Jun 2026 18:00:23 GMT  
		Size: 43.1 MB (43074439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2606ccf36f23572458ec2b9381ffd2cbed4feea52637ca7b984980a2c897bfe`  
		Last Modified: Tue, 09 Jun 2026 18:00:18 GMT  
		Size: 26.8 KB (26804 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:61fbfd3acd2c740fad45fbc0e547fbd90e18564963bb52f281120db14d7b7109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606515813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee10daf9a56de531f543234e76f653015f9f938228db2a38539f54a8b144bb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 18:00:07 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 18:00:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 18:00:07 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 18:00:07 GMT
ARG TARGETARCH=arm64
# Tue, 09 Jun 2026 18:00:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 18:00:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 18:00:15 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 18:00:15 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Jun 2026 18:00:15 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 18:00:15 GMT
ARG ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
# Tue, 09 Jun 2026 18:01:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 18:01:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 18:01:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 18:01:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
USER odoo
# Tue, 09 Jun 2026 18:01:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 18:01:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ba583624296ea83cb6ade2e47a97b2d8ea39eb81f2270ef2f6bde66821d3a2`  
		Last Modified: Tue, 09 Jun 2026 18:02:49 GMT  
		Size: 231.2 MB (231202922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9877d6c93cbd8e5542dcf140a53a2ed849c029c1a8580ac1a1fa99fcc1bfccc8`  
		Last Modified: Tue, 09 Jun 2026 18:02:41 GMT  
		Size: 2.6 MB (2606751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f47d6c70b69c3bb077a2fbf0b526a7d84818ea11e02dc70029bed813f6621c`  
		Last Modified: Tue, 09 Jun 2026 18:02:41 GMT  
		Size: 483.8 KB (483836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e65b27fe55c7739b11655340f71220a093c85833cb692e30ba1f1f59e8805a6`  
		Last Modified: Tue, 09 Jun 2026 18:02:52 GMT  
		Size: 344.6 MB (344612892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d21556f7f9499f32dace7030cc3aec4af1e090e766fb59df157df6102efe9e5`  
		Last Modified: Tue, 09 Jun 2026 18:02:43 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791a8aafe6556047774354afae70ba1bd2142aba5615fc986e148f0aa7cbb350`  
		Last Modified: Tue, 09 Jun 2026 18:02:43 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aeee43c236f5d64acf05f6890594ac516bb2406722fa192911ba1150815e62`  
		Last Modified: Tue, 09 Jun 2026 18:02:44 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b58305ace6c57d4c485c51828facafffd65bc3b4a6b3d1e4f9ff60aa47b9f2e`  
		Last Modified: Tue, 09 Jun 2026 18:02:44 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:43ae91478306c0e330621e1e551fe9782d69391e49ab5c7d8421f400eb531212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43107902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886611e2c216d5102121f6b16ae7c9f1f4ffd027055d768a15966efb1e0b930d`

```dockerfile
```

-	Layers:
	-	`sha256:7dd4cedaf2ad042a877e744e8bf53995bb21c1f9717f7f134eb6fdbd2b1c680b`  
		Last Modified: Tue, 09 Jun 2026 18:02:44 GMT  
		Size: 43.1 MB (43080946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dff350ecd492279dff38eade1f08f784c07d3e9c9b660ac2b6b6dd26f6194af`  
		Last Modified: Tue, 09 Jun 2026 18:02:41 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:67f04958d8a71423cc6d3ccb228b998ef7fb36fe214998c47f52aff975120b32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:2431d50aba410562cb907c717e7849fa37da0e25c809250d3d0a00f3db7d5109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611668656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae689a00ec7bae7c4c18da1a52c86cbbb99ab54d8a5cac0fbc780774198e37e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:58:02 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:58:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:58:02 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:58:02 GMT
ARG TARGETARCH=amd64
# Tue, 09 Jun 2026 17:58:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:58:08 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:58:08 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:58:08 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Jun 2026 17:58:08 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:58:08 GMT
ARG ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
# Tue, 09 Jun 2026 17:59:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:59:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:59:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:59:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
USER odoo
# Tue, 09 Jun 2026 17:59:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:59:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74ec776f8c64f150a0b6fa6c4a66b03b0095cab74cabe701d386821c7fad64c`  
		Last Modified: Tue, 09 Jun 2026 18:00:34 GMT  
		Size: 233.8 MB (233835351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4568750a7eb61dc66f8324576303e7e187c8fdbe432dba33f2c29377a6de843`  
		Last Modified: Tue, 09 Jun 2026 18:00:19 GMT  
		Size: 2.6 MB (2611549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1a612d71e484d2d01f77f60a9210f7f11cc198fde8c57daf507a0cf76f6197`  
		Last Modified: Tue, 09 Jun 2026 18:00:18 GMT  
		Size: 483.8 KB (483825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ceb6c70ed350f6b55a9f1a64d8bf9f4315527d9190cf7f6af0a11bed56726c`  
		Last Modified: Tue, 09 Jun 2026 18:00:37 GMT  
		Size: 345.0 MB (344998456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b42a539ff666391a9501b80a852540f728fa8454f6bfa5aaa0bdbc9ae8a8cb`  
		Last Modified: Tue, 09 Jun 2026 18:00:21 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7149ec469fdec73c85f8ecabcdaba750d932410fe73c560cffcb96428101ad`  
		Last Modified: Tue, 09 Jun 2026 18:00:21 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0142c424d9adda9faad9525f1dd87176086a7d2d511d620a4234a1dc387194`  
		Last Modified: Tue, 09 Jun 2026 18:00:23 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75564abc0cc10b4c529469db68ee158ba8f63c356939c7e7db46dd4ac797bb`  
		Last Modified: Tue, 09 Jun 2026 18:00:23 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:12f0057ebbc0874325c26d3bea65bcfc4f072702ba8f0a92bd9768ed591c533d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43101243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f82aea0471ebda7f2cc8e68220666ce1b6da39104f89420bcc25d364c9ddcc2`

```dockerfile
```

-	Layers:
	-	`sha256:5c223e13fb5ba0ad9a165ee06d3050593aeb7b99ad99661d0f7d28849c1b358a`  
		Last Modified: Tue, 09 Jun 2026 18:00:23 GMT  
		Size: 43.1 MB (43074439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2606ccf36f23572458ec2b9381ffd2cbed4feea52637ca7b984980a2c897bfe`  
		Last Modified: Tue, 09 Jun 2026 18:00:18 GMT  
		Size: 26.8 KB (26804 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:61fbfd3acd2c740fad45fbc0e547fbd90e18564963bb52f281120db14d7b7109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606515813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee10daf9a56de531f543234e76f653015f9f938228db2a38539f54a8b144bb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 18:00:07 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 18:00:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 18:00:07 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 18:00:07 GMT
ARG TARGETARCH=arm64
# Tue, 09 Jun 2026 18:00:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 18:00:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 18:00:15 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 18:00:15 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Jun 2026 18:00:15 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 18:00:15 GMT
ARG ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
# Tue, 09 Jun 2026 18:01:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 18:01:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 18:01:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 18:01:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
USER odoo
# Tue, 09 Jun 2026 18:01:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 18:01:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ba583624296ea83cb6ade2e47a97b2d8ea39eb81f2270ef2f6bde66821d3a2`  
		Last Modified: Tue, 09 Jun 2026 18:02:49 GMT  
		Size: 231.2 MB (231202922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9877d6c93cbd8e5542dcf140a53a2ed849c029c1a8580ac1a1fa99fcc1bfccc8`  
		Last Modified: Tue, 09 Jun 2026 18:02:41 GMT  
		Size: 2.6 MB (2606751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f47d6c70b69c3bb077a2fbf0b526a7d84818ea11e02dc70029bed813f6621c`  
		Last Modified: Tue, 09 Jun 2026 18:02:41 GMT  
		Size: 483.8 KB (483836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e65b27fe55c7739b11655340f71220a093c85833cb692e30ba1f1f59e8805a6`  
		Last Modified: Tue, 09 Jun 2026 18:02:52 GMT  
		Size: 344.6 MB (344612892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d21556f7f9499f32dace7030cc3aec4af1e090e766fb59df157df6102efe9e5`  
		Last Modified: Tue, 09 Jun 2026 18:02:43 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791a8aafe6556047774354afae70ba1bd2142aba5615fc986e148f0aa7cbb350`  
		Last Modified: Tue, 09 Jun 2026 18:02:43 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aeee43c236f5d64acf05f6890594ac516bb2406722fa192911ba1150815e62`  
		Last Modified: Tue, 09 Jun 2026 18:02:44 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b58305ace6c57d4c485c51828facafffd65bc3b4a6b3d1e4f9ff60aa47b9f2e`  
		Last Modified: Tue, 09 Jun 2026 18:02:44 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:43ae91478306c0e330621e1e551fe9782d69391e49ab5c7d8421f400eb531212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43107902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886611e2c216d5102121f6b16ae7c9f1f4ffd027055d768a15966efb1e0b930d`

```dockerfile
```

-	Layers:
	-	`sha256:7dd4cedaf2ad042a877e744e8bf53995bb21c1f9717f7f134eb6fdbd2b1c680b`  
		Last Modified: Tue, 09 Jun 2026 18:02:44 GMT  
		Size: 43.1 MB (43080946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dff350ecd492279dff38eade1f08f784c07d3e9c9b660ac2b6b6dd26f6194af`  
		Last Modified: Tue, 09 Jun 2026 18:02:41 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260609`

```console
$ docker pull odoo@sha256:67f04958d8a71423cc6d3ccb228b998ef7fb36fe214998c47f52aff975120b32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260609` - linux; amd64

```console
$ docker pull odoo@sha256:2431d50aba410562cb907c717e7849fa37da0e25c809250d3d0a00f3db7d5109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.7 MB (611668656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae689a00ec7bae7c4c18da1a52c86cbbb99ab54d8a5cac0fbc780774198e37e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:58:02 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:58:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:58:02 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:58:02 GMT
ARG TARGETARCH=amd64
# Tue, 09 Jun 2026 17:58:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:58:08 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:58:08 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:58:08 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Jun 2026 17:58:08 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:58:08 GMT
ARG ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
# Tue, 09 Jun 2026 17:59:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:59:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:59:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:59:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:59:02 GMT
USER odoo
# Tue, 09 Jun 2026 17:59:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:59:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74ec776f8c64f150a0b6fa6c4a66b03b0095cab74cabe701d386821c7fad64c`  
		Last Modified: Tue, 09 Jun 2026 18:00:34 GMT  
		Size: 233.8 MB (233835351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4568750a7eb61dc66f8324576303e7e187c8fdbe432dba33f2c29377a6de843`  
		Last Modified: Tue, 09 Jun 2026 18:00:19 GMT  
		Size: 2.6 MB (2611549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1a612d71e484d2d01f77f60a9210f7f11cc198fde8c57daf507a0cf76f6197`  
		Last Modified: Tue, 09 Jun 2026 18:00:18 GMT  
		Size: 483.8 KB (483825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ceb6c70ed350f6b55a9f1a64d8bf9f4315527d9190cf7f6af0a11bed56726c`  
		Last Modified: Tue, 09 Jun 2026 18:00:37 GMT  
		Size: 345.0 MB (344998456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b42a539ff666391a9501b80a852540f728fa8454f6bfa5aaa0bdbc9ae8a8cb`  
		Last Modified: Tue, 09 Jun 2026 18:00:21 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7149ec469fdec73c85f8ecabcdaba750d932410fe73c560cffcb96428101ad`  
		Last Modified: Tue, 09 Jun 2026 18:00:21 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0142c424d9adda9faad9525f1dd87176086a7d2d511d620a4234a1dc387194`  
		Last Modified: Tue, 09 Jun 2026 18:00:23 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb75564abc0cc10b4c529469db68ee158ba8f63c356939c7e7db46dd4ac797bb`  
		Last Modified: Tue, 09 Jun 2026 18:00:23 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260609` - unknown; unknown

```console
$ docker pull odoo@sha256:12f0057ebbc0874325c26d3bea65bcfc4f072702ba8f0a92bd9768ed591c533d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43101243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f82aea0471ebda7f2cc8e68220666ce1b6da39104f89420bcc25d364c9ddcc2`

```dockerfile
```

-	Layers:
	-	`sha256:5c223e13fb5ba0ad9a165ee06d3050593aeb7b99ad99661d0f7d28849c1b358a`  
		Last Modified: Tue, 09 Jun 2026 18:00:23 GMT  
		Size: 43.1 MB (43074439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2606ccf36f23572458ec2b9381ffd2cbed4feea52637ca7b984980a2c897bfe`  
		Last Modified: Tue, 09 Jun 2026 18:00:18 GMT  
		Size: 26.8 KB (26804 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20260609` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:61fbfd3acd2c740fad45fbc0e547fbd90e18564963bb52f281120db14d7b7109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606515813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee10daf9a56de531f543234e76f653015f9f938228db2a38539f54a8b144bb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 18:00:07 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 18:00:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 18:00:07 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 18:00:07 GMT
ARG TARGETARCH=arm64
# Tue, 09 Jun 2026 18:00:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 18:00:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 18:00:15 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 18:00:15 GMT
ENV ODOO_VERSION=17.0
# Tue, 09 Jun 2026 18:00:15 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 18:00:15 GMT
ARG ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
# Tue, 09 Jun 2026 18:01:18 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=3f1354cc7102f1849cd91d590c76065b1b5a01dc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 18:01:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 18:01:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 18:01:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 18:01:19 GMT
USER odoo
# Tue, 09 Jun 2026 18:01:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 18:01:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ba583624296ea83cb6ade2e47a97b2d8ea39eb81f2270ef2f6bde66821d3a2`  
		Last Modified: Tue, 09 Jun 2026 18:02:49 GMT  
		Size: 231.2 MB (231202922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9877d6c93cbd8e5542dcf140a53a2ed849c029c1a8580ac1a1fa99fcc1bfccc8`  
		Last Modified: Tue, 09 Jun 2026 18:02:41 GMT  
		Size: 2.6 MB (2606751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f47d6c70b69c3bb077a2fbf0b526a7d84818ea11e02dc70029bed813f6621c`  
		Last Modified: Tue, 09 Jun 2026 18:02:41 GMT  
		Size: 483.8 KB (483836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e65b27fe55c7739b11655340f71220a093c85833cb692e30ba1f1f59e8805a6`  
		Last Modified: Tue, 09 Jun 2026 18:02:52 GMT  
		Size: 344.6 MB (344612892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d21556f7f9499f32dace7030cc3aec4af1e090e766fb59df157df6102efe9e5`  
		Last Modified: Tue, 09 Jun 2026 18:02:43 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791a8aafe6556047774354afae70ba1bd2142aba5615fc986e148f0aa7cbb350`  
		Last Modified: Tue, 09 Jun 2026 18:02:43 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70aeee43c236f5d64acf05f6890594ac516bb2406722fa192911ba1150815e62`  
		Last Modified: Tue, 09 Jun 2026 18:02:44 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b58305ace6c57d4c485c51828facafffd65bc3b4a6b3d1e4f9ff60aa47b9f2e`  
		Last Modified: Tue, 09 Jun 2026 18:02:44 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260609` - unknown; unknown

```console
$ docker pull odoo@sha256:43ae91478306c0e330621e1e551fe9782d69391e49ab5c7d8421f400eb531212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43107902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886611e2c216d5102121f6b16ae7c9f1f4ffd027055d768a15966efb1e0b930d`

```dockerfile
```

-	Layers:
	-	`sha256:7dd4cedaf2ad042a877e744e8bf53995bb21c1f9717f7f134eb6fdbd2b1c680b`  
		Last Modified: Tue, 09 Jun 2026 18:02:44 GMT  
		Size: 43.1 MB (43080946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dff350ecd492279dff38eade1f08f784c07d3e9c9b660ac2b6b6dd26f6194af`  
		Last Modified: Tue, 09 Jun 2026 18:02:41 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:f0d5dcafc72cacea66ae0ee8d7950d436d19d084ffade089f51e14c98b823803
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
$ docker pull odoo@sha256:cbe759b2a2291be5de4b25538d31aa5f12a7be040694ac0bb5af244d6f03b4e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.5 MB (687489334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90d2618af9382596dab502aed66db8df548184aaa7c16c98061e6fcb61caf5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:58:46 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:58:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:58:46 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:58:46 GMT
ARG TARGETARCH=amd64
# Tue, 09 Jun 2026 17:58:46 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:58:52 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:58:53 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:58:53 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Jun 2026 17:58:53 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:58:53 GMT
ARG ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
# Tue, 09 Jun 2026 17:59:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:59:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:59:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:59:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
USER odoo
# Tue, 09 Jun 2026 17:59:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:59:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da74a6be825b0749c3ede21b02172eee0ada126f8b97add9fa1a47e9f93b2710`  
		Last Modified: Tue, 09 Jun 2026 18:01:32 GMT  
		Size: 254.7 MB (254678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25943e8bc37baf8f474bbf49859657837a2ed5f0d743c1a3397c9d72aa465b8f`  
		Last Modified: Tue, 09 Jun 2026 18:01:23 GMT  
		Size: 14.4 MB (14370740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b7663c22267e2019ce7a3492c77eb09dd7c25220a26e62ef042e96cfab355c`  
		Last Modified: Tue, 09 Jun 2026 18:01:22 GMT  
		Size: 483.6 KB (483613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16dfdead42f46db400007aca15a790da11425c155d2d9a8fff6b0ade0085deb`  
		Last Modified: Tue, 09 Jun 2026 18:01:35 GMT  
		Size: 388.2 MB (388221357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e322817c1b332e7c297c3573842c0f8fa7f03ee8d164d44572763eb34d068a14`  
		Last Modified: Tue, 09 Jun 2026 18:01:24 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf1e65abdf7ce48a816c91eaefd9bf69a637ee72436ae63483e471a35f8dfb4`  
		Last Modified: Tue, 09 Jun 2026 18:01:25 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6bc4c638d2a7360133e274842d160038c0a5b47bdff0467b8ffc37fab58149`  
		Last Modified: Tue, 09 Jun 2026 18:01:26 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e03c3a7c3f3a200cd64f07b5f0ff01f9e8428056fa1a3c9b0b418135f9668d4`  
		Last Modified: Tue, 09 Jun 2026 18:01:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:c8d0f203cc9cd5b9d3e3a7e03de2f38f3ab7167e9668a05e972f2b8f0fdb225f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62560638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95735248087e0c13c435e1b47a48e5ccb477fbf98ca450a16112266c0bb0e4e3`

```dockerfile
```

-	Layers:
	-	`sha256:5cdaa120842feeb44261f1e93ad62cfdfcb51242ae188eec15b108a840985661`  
		Last Modified: Tue, 09 Jun 2026 18:01:26 GMT  
		Size: 62.5 MB (62533827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bcfc21bfdf4c9655c5fee49a0bca47a126c354310b6c6c6ef1230f85eddf3d9`  
		Last Modified: Tue, 09 Jun 2026 18:01:22 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:cefef1c497534923ce8c092d56d4387d1ad5de2fe888caadcea2c0a2d34a336b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.9 MB (683896475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867a045ba6baf60369475efc1ca622db267b4d8626ac66bda1b1c22bf6ebd6bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 18:00:31 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 18:00:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 18:00:31 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 18:00:31 GMT
ARG TARGETARCH=arm64
# Tue, 09 Jun 2026 18:00:31 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 18:00:38 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 18:00:39 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 18:00:39 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Jun 2026 18:00:39 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 18:00:39 GMT
ARG ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
# Tue, 09 Jun 2026 18:01:38 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 18:01:38 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 18:01:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 18:01:38 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
USER odoo
# Tue, 09 Jun 2026 18:01:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 18:01:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892ebd25c699c1612ec382e908922ab857fd0884f8f0cb69827c7f9a915cfb68`  
		Last Modified: Tue, 09 Jun 2026 18:03:52 GMT  
		Size: 252.1 MB (252126422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5fdde9155efa272ef95f3a4e517f7329ad45dcf561ff11285b5f625387ee7f`  
		Last Modified: Tue, 09 Jun 2026 18:03:42 GMT  
		Size: 14.3 MB (14349085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8eef3b25387c185ab35641f95031684a54b6ea219326e33ec3618147fbea5`  
		Last Modified: Tue, 09 Jun 2026 18:03:41 GMT  
		Size: 483.6 KB (483615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df34eab7bf22f4bed0d6b352b4f8e5805dcfe5cc1a5c2dcb5d282eb6f3006cd`  
		Last Modified: Tue, 09 Jun 2026 18:03:54 GMT  
		Size: 388.1 MB (388058152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f163cef2e7d0f54af0c7fb0f0e7d1eab87fe15d49d141e80c053c5aea278c2`  
		Last Modified: Tue, 09 Jun 2026 18:03:42 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c087bb3c4cf4cec11c54cbf383dcaed731d605ca0b5d1aa0d730dd0c6bb29ed0`  
		Last Modified: Tue, 09 Jun 2026 18:03:44 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fcdfdaf862e9495d2a40a9c5e402a58be319743fc74d8e9163adb80c2197f1`  
		Last Modified: Tue, 09 Jun 2026 18:03:44 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ade0a2fb0f3dc5c52412d98d8c5ec284e1fb46b4a7a7af011dd5a24816d179`  
		Last Modified: Tue, 09 Jun 2026 18:03:45 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:79fc8bdb7330031831baf84f7306efee67011c768aba410f216efb0d2ff8c579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62568065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb164c24334e04bd17048a57684516cf65c42f99f63b75ce53ac3b69685e09bc`

```dockerfile
```

-	Layers:
	-	`sha256:dd55b8e61cfb493995c03f5f1a43c59da4e3d86ed12644a76fea47c60f375f74`  
		Last Modified: Tue, 09 Jun 2026 18:03:44 GMT  
		Size: 62.5 MB (62541102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73483b12b0e9087f3ed7191874f3a914e3963445745b35fb6bdf60f943f93a01`  
		Last Modified: Tue, 09 Jun 2026 18:03:40 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:56d64c92885e5281bad0ce7fdbb14bed8c392607867d66861cd82168251bf669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.6 MB (703563320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15d607640c40a7226674f96dade2c413a96a0885c99d22903ad719ff6b062f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=18.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260609
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
# Tue, 09 Jun 2026 17:57:56 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:57:58 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:57:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:57:59 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:57:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:57:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:57:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:57:59 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:57:59 GMT
USER odoo
# Tue, 09 Jun 2026 17:57:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4af654b931f9420a76bd3dcb3bee9359529003ccfffa85407657f92054a3c6`  
		Last Modified: Tue, 09 Jun 2026 18:02:44 GMT  
		Size: 388.8 MB (388762639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc0cfd47a966d45106b5db727d816bae7217d74e240219cbbeea88b9225843b`  
		Last Modified: Tue, 09 Jun 2026 18:02:33 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb587a5eca49da6c693b87a4c4908107964fc5870929be0a8c0e9c6ff9289d3`  
		Last Modified: Tue, 09 Jun 2026 18:02:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded57417671c9e7d550a8935bdb393efdd907d2423c61c4cd22fea0fa2014d5e`  
		Last Modified: Tue, 09 Jun 2026 18:02:33 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e7055c95e68652a9f5831e2f7540362b0f1c87676dca2860b9b3e500558b3e`  
		Last Modified: Tue, 09 Jun 2026 18:02:34 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:410b04457ff41403bed5d8b68a9f2e702891bed17c78339c8c594ba956b14a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62569069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87683dedeea7dd7ce191e8dce424ecef150a886bc9e92201d372c3a21a7bac6e`

```dockerfile
```

-	Layers:
	-	`sha256:54679ca81c83439552fa81351053b0547f4219e94fafd152b2664854f8e659c9`  
		Last Modified: Tue, 09 Jun 2026 18:02:36 GMT  
		Size: 62.5 MB (62542202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790a23fb89b75f45fe0afac68e8a5e88d8b61588d4b8e96b07985f882d34917e`  
		Last Modified: Tue, 09 Jun 2026 18:02:33 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:f0d5dcafc72cacea66ae0ee8d7950d436d19d084ffade089f51e14c98b823803
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
$ docker pull odoo@sha256:cbe759b2a2291be5de4b25538d31aa5f12a7be040694ac0bb5af244d6f03b4e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.5 MB (687489334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90d2618af9382596dab502aed66db8df548184aaa7c16c98061e6fcb61caf5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:58:46 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:58:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:58:46 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:58:46 GMT
ARG TARGETARCH=amd64
# Tue, 09 Jun 2026 17:58:46 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:58:52 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:58:53 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:58:53 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Jun 2026 17:58:53 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:58:53 GMT
ARG ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
# Tue, 09 Jun 2026 17:59:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:59:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:59:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:59:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
USER odoo
# Tue, 09 Jun 2026 17:59:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:59:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da74a6be825b0749c3ede21b02172eee0ada126f8b97add9fa1a47e9f93b2710`  
		Last Modified: Tue, 09 Jun 2026 18:01:32 GMT  
		Size: 254.7 MB (254678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25943e8bc37baf8f474bbf49859657837a2ed5f0d743c1a3397c9d72aa465b8f`  
		Last Modified: Tue, 09 Jun 2026 18:01:23 GMT  
		Size: 14.4 MB (14370740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b7663c22267e2019ce7a3492c77eb09dd7c25220a26e62ef042e96cfab355c`  
		Last Modified: Tue, 09 Jun 2026 18:01:22 GMT  
		Size: 483.6 KB (483613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16dfdead42f46db400007aca15a790da11425c155d2d9a8fff6b0ade0085deb`  
		Last Modified: Tue, 09 Jun 2026 18:01:35 GMT  
		Size: 388.2 MB (388221357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e322817c1b332e7c297c3573842c0f8fa7f03ee8d164d44572763eb34d068a14`  
		Last Modified: Tue, 09 Jun 2026 18:01:24 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf1e65abdf7ce48a816c91eaefd9bf69a637ee72436ae63483e471a35f8dfb4`  
		Last Modified: Tue, 09 Jun 2026 18:01:25 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6bc4c638d2a7360133e274842d160038c0a5b47bdff0467b8ffc37fab58149`  
		Last Modified: Tue, 09 Jun 2026 18:01:26 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e03c3a7c3f3a200cd64f07b5f0ff01f9e8428056fa1a3c9b0b418135f9668d4`  
		Last Modified: Tue, 09 Jun 2026 18:01:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c8d0f203cc9cd5b9d3e3a7e03de2f38f3ab7167e9668a05e972f2b8f0fdb225f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62560638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95735248087e0c13c435e1b47a48e5ccb477fbf98ca450a16112266c0bb0e4e3`

```dockerfile
```

-	Layers:
	-	`sha256:5cdaa120842feeb44261f1e93ad62cfdfcb51242ae188eec15b108a840985661`  
		Last Modified: Tue, 09 Jun 2026 18:01:26 GMT  
		Size: 62.5 MB (62533827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bcfc21bfdf4c9655c5fee49a0bca47a126c354310b6c6c6ef1230f85eddf3d9`  
		Last Modified: Tue, 09 Jun 2026 18:01:22 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:cefef1c497534923ce8c092d56d4387d1ad5de2fe888caadcea2c0a2d34a336b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.9 MB (683896475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867a045ba6baf60369475efc1ca622db267b4d8626ac66bda1b1c22bf6ebd6bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 18:00:31 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 18:00:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 18:00:31 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 18:00:31 GMT
ARG TARGETARCH=arm64
# Tue, 09 Jun 2026 18:00:31 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 18:00:38 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 18:00:39 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 18:00:39 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Jun 2026 18:00:39 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 18:00:39 GMT
ARG ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
# Tue, 09 Jun 2026 18:01:38 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 18:01:38 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 18:01:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 18:01:38 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
USER odoo
# Tue, 09 Jun 2026 18:01:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 18:01:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892ebd25c699c1612ec382e908922ab857fd0884f8f0cb69827c7f9a915cfb68`  
		Last Modified: Tue, 09 Jun 2026 18:03:52 GMT  
		Size: 252.1 MB (252126422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5fdde9155efa272ef95f3a4e517f7329ad45dcf561ff11285b5f625387ee7f`  
		Last Modified: Tue, 09 Jun 2026 18:03:42 GMT  
		Size: 14.3 MB (14349085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8eef3b25387c185ab35641f95031684a54b6ea219326e33ec3618147fbea5`  
		Last Modified: Tue, 09 Jun 2026 18:03:41 GMT  
		Size: 483.6 KB (483615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df34eab7bf22f4bed0d6b352b4f8e5805dcfe5cc1a5c2dcb5d282eb6f3006cd`  
		Last Modified: Tue, 09 Jun 2026 18:03:54 GMT  
		Size: 388.1 MB (388058152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f163cef2e7d0f54af0c7fb0f0e7d1eab87fe15d49d141e80c053c5aea278c2`  
		Last Modified: Tue, 09 Jun 2026 18:03:42 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c087bb3c4cf4cec11c54cbf383dcaed731d605ca0b5d1aa0d730dd0c6bb29ed0`  
		Last Modified: Tue, 09 Jun 2026 18:03:44 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fcdfdaf862e9495d2a40a9c5e402a58be319743fc74d8e9163adb80c2197f1`  
		Last Modified: Tue, 09 Jun 2026 18:03:44 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ade0a2fb0f3dc5c52412d98d8c5ec284e1fb46b4a7a7af011dd5a24816d179`  
		Last Modified: Tue, 09 Jun 2026 18:03:45 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:79fc8bdb7330031831baf84f7306efee67011c768aba410f216efb0d2ff8c579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62568065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb164c24334e04bd17048a57684516cf65c42f99f63b75ce53ac3b69685e09bc`

```dockerfile
```

-	Layers:
	-	`sha256:dd55b8e61cfb493995c03f5f1a43c59da4e3d86ed12644a76fea47c60f375f74`  
		Last Modified: Tue, 09 Jun 2026 18:03:44 GMT  
		Size: 62.5 MB (62541102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73483b12b0e9087f3ed7191874f3a914e3963445745b35fb6bdf60f943f93a01`  
		Last Modified: Tue, 09 Jun 2026 18:03:40 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:56d64c92885e5281bad0ce7fdbb14bed8c392607867d66861cd82168251bf669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.6 MB (703563320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15d607640c40a7226674f96dade2c413a96a0885c99d22903ad719ff6b062f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=18.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260609
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
# Tue, 09 Jun 2026 17:57:56 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:57:58 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:57:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:57:59 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:57:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:57:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:57:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:57:59 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:57:59 GMT
USER odoo
# Tue, 09 Jun 2026 17:57:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4af654b931f9420a76bd3dcb3bee9359529003ccfffa85407657f92054a3c6`  
		Last Modified: Tue, 09 Jun 2026 18:02:44 GMT  
		Size: 388.8 MB (388762639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc0cfd47a966d45106b5db727d816bae7217d74e240219cbbeea88b9225843b`  
		Last Modified: Tue, 09 Jun 2026 18:02:33 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb587a5eca49da6c693b87a4c4908107964fc5870929be0a8c0e9c6ff9289d3`  
		Last Modified: Tue, 09 Jun 2026 18:02:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded57417671c9e7d550a8935bdb393efdd907d2423c61c4cd22fea0fa2014d5e`  
		Last Modified: Tue, 09 Jun 2026 18:02:33 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e7055c95e68652a9f5831e2f7540362b0f1c87676dca2860b9b3e500558b3e`  
		Last Modified: Tue, 09 Jun 2026 18:02:34 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:410b04457ff41403bed5d8b68a9f2e702891bed17c78339c8c594ba956b14a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62569069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87683dedeea7dd7ce191e8dce424ecef150a886bc9e92201d372c3a21a7bac6e`

```dockerfile
```

-	Layers:
	-	`sha256:54679ca81c83439552fa81351053b0547f4219e94fafd152b2664854f8e659c9`  
		Last Modified: Tue, 09 Jun 2026 18:02:36 GMT  
		Size: 62.5 MB (62542202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790a23fb89b75f45fe0afac68e8a5e88d8b61588d4b8e96b07985f882d34917e`  
		Last Modified: Tue, 09 Jun 2026 18:02:33 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260609`

```console
$ docker pull odoo@sha256:f0d5dcafc72cacea66ae0ee8d7950d436d19d084ffade089f51e14c98b823803
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260609` - linux; amd64

```console
$ docker pull odoo@sha256:cbe759b2a2291be5de4b25538d31aa5f12a7be040694ac0bb5af244d6f03b4e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **687.5 MB (687489334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90d2618af9382596dab502aed66db8df548184aaa7c16c98061e6fcb61caf5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:58:46 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:58:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:58:46 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:58:46 GMT
ARG TARGETARCH=amd64
# Tue, 09 Jun 2026 17:58:46 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:58:52 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:58:53 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:58:53 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Jun 2026 17:58:53 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:58:53 GMT
ARG ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
# Tue, 09 Jun 2026 17:59:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:59:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:59:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:59:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:59:40 GMT
USER odoo
# Tue, 09 Jun 2026 17:59:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:59:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da74a6be825b0749c3ede21b02172eee0ada126f8b97add9fa1a47e9f93b2710`  
		Last Modified: Tue, 09 Jun 2026 18:01:32 GMT  
		Size: 254.7 MB (254678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25943e8bc37baf8f474bbf49859657837a2ed5f0d743c1a3397c9d72aa465b8f`  
		Last Modified: Tue, 09 Jun 2026 18:01:23 GMT  
		Size: 14.4 MB (14370740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b7663c22267e2019ce7a3492c77eb09dd7c25220a26e62ef042e96cfab355c`  
		Last Modified: Tue, 09 Jun 2026 18:01:22 GMT  
		Size: 483.6 KB (483613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16dfdead42f46db400007aca15a790da11425c155d2d9a8fff6b0ade0085deb`  
		Last Modified: Tue, 09 Jun 2026 18:01:35 GMT  
		Size: 388.2 MB (388221357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e322817c1b332e7c297c3573842c0f8fa7f03ee8d164d44572763eb34d068a14`  
		Last Modified: Tue, 09 Jun 2026 18:01:24 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf1e65abdf7ce48a816c91eaefd9bf69a637ee72436ae63483e471a35f8dfb4`  
		Last Modified: Tue, 09 Jun 2026 18:01:25 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6bc4c638d2a7360133e274842d160038c0a5b47bdff0467b8ffc37fab58149`  
		Last Modified: Tue, 09 Jun 2026 18:01:26 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e03c3a7c3f3a200cd64f07b5f0ff01f9e8428056fa1a3c9b0b418135f9668d4`  
		Last Modified: Tue, 09 Jun 2026 18:01:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260609` - unknown; unknown

```console
$ docker pull odoo@sha256:c8d0f203cc9cd5b9d3e3a7e03de2f38f3ab7167e9668a05e972f2b8f0fdb225f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62560638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95735248087e0c13c435e1b47a48e5ccb477fbf98ca450a16112266c0bb0e4e3`

```dockerfile
```

-	Layers:
	-	`sha256:5cdaa120842feeb44261f1e93ad62cfdfcb51242ae188eec15b108a840985661`  
		Last Modified: Tue, 09 Jun 2026 18:01:26 GMT  
		Size: 62.5 MB (62533827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bcfc21bfdf4c9655c5fee49a0bca47a126c354310b6c6c6ef1230f85eddf3d9`  
		Last Modified: Tue, 09 Jun 2026 18:01:22 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260609` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:cefef1c497534923ce8c092d56d4387d1ad5de2fe888caadcea2c0a2d34a336b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.9 MB (683896475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867a045ba6baf60369475efc1ca622db267b4d8626ac66bda1b1c22bf6ebd6bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 18:00:31 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 18:00:31 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 18:00:31 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 18:00:31 GMT
ARG TARGETARCH=arm64
# Tue, 09 Jun 2026 18:00:31 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 18:00:38 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 18:00:39 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 18:00:39 GMT
ENV ODOO_VERSION=18.0
# Tue, 09 Jun 2026 18:00:39 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 18:00:39 GMT
ARG ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
# Tue, 09 Jun 2026 18:01:38 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 18:01:38 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 18:01:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 18:01:38 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 18:01:38 GMT
USER odoo
# Tue, 09 Jun 2026 18:01:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 18:01:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892ebd25c699c1612ec382e908922ab857fd0884f8f0cb69827c7f9a915cfb68`  
		Last Modified: Tue, 09 Jun 2026 18:03:52 GMT  
		Size: 252.1 MB (252126422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5fdde9155efa272ef95f3a4e517f7329ad45dcf561ff11285b5f625387ee7f`  
		Last Modified: Tue, 09 Jun 2026 18:03:42 GMT  
		Size: 14.3 MB (14349085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b8eef3b25387c185ab35641f95031684a54b6ea219326e33ec3618147fbea5`  
		Last Modified: Tue, 09 Jun 2026 18:03:41 GMT  
		Size: 483.6 KB (483615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df34eab7bf22f4bed0d6b352b4f8e5805dcfe5cc1a5c2dcb5d282eb6f3006cd`  
		Last Modified: Tue, 09 Jun 2026 18:03:54 GMT  
		Size: 388.1 MB (388058152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f163cef2e7d0f54af0c7fb0f0e7d1eab87fe15d49d141e80c053c5aea278c2`  
		Last Modified: Tue, 09 Jun 2026 18:03:42 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c087bb3c4cf4cec11c54cbf383dcaed731d605ca0b5d1aa0d730dd0c6bb29ed0`  
		Last Modified: Tue, 09 Jun 2026 18:03:44 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fcdfdaf862e9495d2a40a9c5e402a58be319743fc74d8e9163adb80c2197f1`  
		Last Modified: Tue, 09 Jun 2026 18:03:44 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ade0a2fb0f3dc5c52412d98d8c5ec284e1fb46b4a7a7af011dd5a24816d179`  
		Last Modified: Tue, 09 Jun 2026 18:03:45 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260609` - unknown; unknown

```console
$ docker pull odoo@sha256:79fc8bdb7330031831baf84f7306efee67011c768aba410f216efb0d2ff8c579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62568065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb164c24334e04bd17048a57684516cf65c42f99f63b75ce53ac3b69685e09bc`

```dockerfile
```

-	Layers:
	-	`sha256:dd55b8e61cfb493995c03f5f1a43c59da4e3d86ed12644a76fea47c60f375f74`  
		Last Modified: Tue, 09 Jun 2026 18:03:44 GMT  
		Size: 62.5 MB (62541102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73483b12b0e9087f3ed7191874f3a914e3963445745b35fb6bdf60f943f93a01`  
		Last Modified: Tue, 09 Jun 2026 18:03:40 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260609` - linux; ppc64le

```console
$ docker pull odoo@sha256:56d64c92885e5281bad0ce7fdbb14bed8c392607867d66861cd82168251bf669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.6 MB (703563320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15d607640c40a7226674f96dade2c413a96a0885c99d22903ad719ff6b062f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=18.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260609
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
# Tue, 09 Jun 2026 17:57:56 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:57:58 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:57:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:57:59 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=0c0f770f46958eff5ce016466c89edcb070b3ffe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:57:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:57:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:57:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:57:59 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:57:59 GMT
USER odoo
# Tue, 09 Jun 2026 17:57:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4af654b931f9420a76bd3dcb3bee9359529003ccfffa85407657f92054a3c6`  
		Last Modified: Tue, 09 Jun 2026 18:02:44 GMT  
		Size: 388.8 MB (388762639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc0cfd47a966d45106b5db727d816bae7217d74e240219cbbeea88b9225843b`  
		Last Modified: Tue, 09 Jun 2026 18:02:33 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb587a5eca49da6c693b87a4c4908107964fc5870929be0a8c0e9c6ff9289d3`  
		Last Modified: Tue, 09 Jun 2026 18:02:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded57417671c9e7d550a8935bdb393efdd907d2423c61c4cd22fea0fa2014d5e`  
		Last Modified: Tue, 09 Jun 2026 18:02:33 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e7055c95e68652a9f5831e2f7540362b0f1c87676dca2860b9b3e500558b3e`  
		Last Modified: Tue, 09 Jun 2026 18:02:34 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260609` - unknown; unknown

```console
$ docker pull odoo@sha256:410b04457ff41403bed5d8b68a9f2e702891bed17c78339c8c594ba956b14a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62569069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87683dedeea7dd7ce191e8dce424ecef150a886bc9e92201d372c3a21a7bac6e`

```dockerfile
```

-	Layers:
	-	`sha256:54679ca81c83439552fa81351053b0547f4219e94fafd152b2664854f8e659c9`  
		Last Modified: Tue, 09 Jun 2026 18:02:36 GMT  
		Size: 62.5 MB (62542202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790a23fb89b75f45fe0afac68e8a5e88d8b61588d4b8e96b07985f882d34917e`  
		Last Modified: Tue, 09 Jun 2026 18:02:33 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:3eede45a6be2a1fe4dc2911b7fc5caa8c6d5999e8f56ed8e3135160d6dc115c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19` - linux; amd64

```console
$ docker pull odoo@sha256:17ca74d0757479a99c2401a483cd1a84540bc8be1ba8c344d7da9745c53a6e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.3 MB (706275066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfb46877431666c2ce3209923239c8fd8081bd329e9cc2ecc7fcbef0a3dd4fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:59:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:59:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:59:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:59:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Jun 2026 17:59:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:59:09 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:59:09 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:59:09 GMT
ENV ODOO_VERSION=19.0
# Tue, 09 Jun 2026 17:59:09 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:59:09 GMT
ARG ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
# Tue, 09 Jun 2026 18:00:07 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 18:00:08 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 18:00:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 18:00:08 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
USER odoo
# Tue, 09 Jun 2026 18:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 18:00:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e9e49342a198c2c77b6de2448d6a0a4bb0b8794fd9a6b42fd74b225caef712`  
		Last Modified: Tue, 09 Jun 2026 18:02:22 GMT  
		Size: 254.7 MB (254676097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522cc0cb7f4458ba5b6860c2fcaa04d4bdc0bdcdaa8fadc61f550ac326c8e0fb`  
		Last Modified: Tue, 09 Jun 2026 18:02:14 GMT  
		Size: 14.4 MB (14370794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b697a202e915d6b16063ac31ad06e68cc09b85230d849336308fd19d1fc15b`  
		Last Modified: Tue, 09 Jun 2026 18:02:13 GMT  
		Size: 483.6 KB (483603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e480c1aae10746c1c6dc7afa7c8c825ec22aa7c31a2848378038412bba6e0`  
		Last Modified: Tue, 09 Jun 2026 18:02:25 GMT  
		Size: 407.0 MB (407009021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f25cb03abb341b969e9cc2910dc618cfc93ccf81fd95e453fd17d2120915520`  
		Last Modified: Tue, 09 Jun 2026 18:02:14 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46918ca4f13f721aafb0caf7e87f957299428177232bbae19f1e51cdfe0ae2f`  
		Last Modified: Tue, 09 Jun 2026 18:02:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120f42af961d1d413ab83e1dd42f34c8205444bd3173c363a4b92dcd62f3926b`  
		Last Modified: Tue, 09 Jun 2026 18:02:16 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5e216758713289c5e1420a19207735b6947b8475d6db9da4afb36c4d3e10d8`  
		Last Modified: Tue, 09 Jun 2026 18:02:17 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:5087fdb163c02714d66b8bd39cf24aded4de0db8bf4493b88a7e0258814d611b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70800707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05903e45208ad2a5e73cdbd72ef9aa52533ba2d169f1ec5786b4d19e9db77b45`

```dockerfile
```

-	Layers:
	-	`sha256:bdc6612443e7ac76ffcd219b4ad26bdeedcac27dba0975504834d2e2b8b25dd1`  
		Last Modified: Tue, 09 Jun 2026 18:02:17 GMT  
		Size: 70.8 MB (70773602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d421bd6853b3e6e8c3091ee3d8a28ffccc9751189423603f8630e1a0f850e351`  
		Last Modified: Tue, 09 Jun 2026 18:02:13 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2bc452641550e8ee0707cee890b67ae10a6eff5dd4a9af8413f180b2f0c80991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.7 MB (702700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed27ee59fd9b58685cf14529855592ce8e270e983e6df9e0bb2190efb602c46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:57:29 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:57:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:57:29 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:57:29 GMT
ARG TARGETARCH=arm64
# Tue, 09 Jun 2026 17:57:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:57:38 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:57:38 GMT
ENV ODOO_VERSION=19.0
# Tue, 09 Jun 2026 17:57:38 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:57:38 GMT
ARG ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
# Tue, 09 Jun 2026 17:58:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:58:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:58:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:58:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
USER odoo
# Tue, 09 Jun 2026 17:58:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:58:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7b8dfc0f44855af30a7c3f1abf87864f2fd62b846d0552b89eb2e9dd0eb378`  
		Last Modified: Tue, 09 Jun 2026 18:01:18 GMT  
		Size: 252.1 MB (252126502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e5754573198e5dd4061f098048c208de25abcd3026f0e08bce6330aff649a`  
		Last Modified: Tue, 09 Jun 2026 18:01:09 GMT  
		Size: 14.3 MB (14348186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e85d7565c355c3da04f9e02c290d90eddda3fa6af705771b0e4a4aa28b1fd6e`  
		Last Modified: Tue, 09 Jun 2026 18:01:09 GMT  
		Size: 483.7 KB (483665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d452a7ff7ba3743c74aa753e7a561fd5963e399b7207be1580f8b4003b6cdcc0`  
		Last Modified: Tue, 09 Jun 2026 18:01:21 GMT  
		Size: 406.9 MB (406862967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8ecb5024a7b0e2a758c08c523c157c997bbc678d28d2d4730654b362b6453e`  
		Last Modified: Tue, 09 Jun 2026 18:01:13 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b7ef6546c4e2f4c39d12dc9a05ced79724a123e1ac168f182e3927862a202`  
		Last Modified: Tue, 09 Jun 2026 18:01:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a79a005ab89315dacca9a22c4ac523de650cb15001e1dad142422f89d214ef`  
		Last Modified: Tue, 09 Jun 2026 18:01:14 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b183c7b3996f37f752ccf083c43b636d78fc03a9513da614666ee2e9d2be6be3`  
		Last Modified: Tue, 09 Jun 2026 18:01:17 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:8bbe8853a5d48b14e4a9c5e81e9168eeac19501d5d2874d4d3433fb93af6ee6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70808158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c18c36db8cbe4e79dce40f87698b29453fc4ba61357751c930a627c986b46d`

```dockerfile
```

-	Layers:
	-	`sha256:66534a7fec2147f8059421e60d6d4a760f6460e12a668b7bf16eec9a0e71f18c`  
		Last Modified: Tue, 09 Jun 2026 18:01:12 GMT  
		Size: 70.8 MB (70780889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e9145d435160b9f497d4a00f561d9818c8925e4c2aa1effb2bd6df3b46889d1`  
		Last Modified: Tue, 09 Jun 2026 18:01:08 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:5470e9b9161d524ad1d25443341b719213f29c73b79764a73bcdd8797513d0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.3 MB (722338651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ea28bb43a90dc02284377fb0ed6ce81d70f0c21afecd810701a68e6930a9d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260609
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
# Tue, 09 Jun 2026 17:57:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:57:36 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:57:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:57:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:57:38 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:57:38 GMT
USER odoo
# Tue, 09 Jun 2026 17:57:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34178356017677beb250135311d6774e9608044bfbfdee03dbc42085480d59d2`  
		Last Modified: Tue, 09 Jun 2026 18:03:22 GMT  
		Size: 407.5 MB (407538016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72506d4e3e106f7e71858d8d45429e1c9793c6d87c584558838ec7d3ca6d75`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e0595bff7058f3baf51cafba73d2b41ff93503263e56a78dbd68cd918a4917`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261c92b3aa4bf40ed52719181964fb77c67351e284a7e50a26f90aef996db67c`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c8aa0f168dc1b8ad3de3f5f6ab72cce094a837db8e4d214ac3192509aedf7a`  
		Last Modified: Tue, 09 Jun 2026 18:03:13 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:918b3008a560fce407928b1f427b38f701b2695fc8bb995da820955713565cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70809150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385ab7d41423fef3f7cf7a236a890720f840875df07785a7c21a539ba8355af4`

```dockerfile
```

-	Layers:
	-	`sha256:e13327efb50e4f3dc7269a380f9727e9b1a358346f136ae6347301611dc16f79`  
		Last Modified: Tue, 09 Jun 2026 18:03:16 GMT  
		Size: 70.8 MB (70781983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe3b56a1f09d0004fcbb9245ac1805820e06c1287cd016811bdf832969c1bb2f`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:3eede45a6be2a1fe4dc2911b7fc5caa8c6d5999e8f56ed8e3135160d6dc115c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0` - linux; amd64

```console
$ docker pull odoo@sha256:17ca74d0757479a99c2401a483cd1a84540bc8be1ba8c344d7da9745c53a6e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.3 MB (706275066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfb46877431666c2ce3209923239c8fd8081bd329e9cc2ecc7fcbef0a3dd4fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:59:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:59:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:59:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:59:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Jun 2026 17:59:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:59:09 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:59:09 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:59:09 GMT
ENV ODOO_VERSION=19.0
# Tue, 09 Jun 2026 17:59:09 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:59:09 GMT
ARG ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
# Tue, 09 Jun 2026 18:00:07 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 18:00:08 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 18:00:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 18:00:08 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
USER odoo
# Tue, 09 Jun 2026 18:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 18:00:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e9e49342a198c2c77b6de2448d6a0a4bb0b8794fd9a6b42fd74b225caef712`  
		Last Modified: Tue, 09 Jun 2026 18:02:22 GMT  
		Size: 254.7 MB (254676097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522cc0cb7f4458ba5b6860c2fcaa04d4bdc0bdcdaa8fadc61f550ac326c8e0fb`  
		Last Modified: Tue, 09 Jun 2026 18:02:14 GMT  
		Size: 14.4 MB (14370794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b697a202e915d6b16063ac31ad06e68cc09b85230d849336308fd19d1fc15b`  
		Last Modified: Tue, 09 Jun 2026 18:02:13 GMT  
		Size: 483.6 KB (483603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e480c1aae10746c1c6dc7afa7c8c825ec22aa7c31a2848378038412bba6e0`  
		Last Modified: Tue, 09 Jun 2026 18:02:25 GMT  
		Size: 407.0 MB (407009021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f25cb03abb341b969e9cc2910dc618cfc93ccf81fd95e453fd17d2120915520`  
		Last Modified: Tue, 09 Jun 2026 18:02:14 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46918ca4f13f721aafb0caf7e87f957299428177232bbae19f1e51cdfe0ae2f`  
		Last Modified: Tue, 09 Jun 2026 18:02:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120f42af961d1d413ab83e1dd42f34c8205444bd3173c363a4b92dcd62f3926b`  
		Last Modified: Tue, 09 Jun 2026 18:02:16 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5e216758713289c5e1420a19207735b6947b8475d6db9da4afb36c4d3e10d8`  
		Last Modified: Tue, 09 Jun 2026 18:02:17 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:5087fdb163c02714d66b8bd39cf24aded4de0db8bf4493b88a7e0258814d611b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70800707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05903e45208ad2a5e73cdbd72ef9aa52533ba2d169f1ec5786b4d19e9db77b45`

```dockerfile
```

-	Layers:
	-	`sha256:bdc6612443e7ac76ffcd219b4ad26bdeedcac27dba0975504834d2e2b8b25dd1`  
		Last Modified: Tue, 09 Jun 2026 18:02:17 GMT  
		Size: 70.8 MB (70773602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d421bd6853b3e6e8c3091ee3d8a28ffccc9751189423603f8630e1a0f850e351`  
		Last Modified: Tue, 09 Jun 2026 18:02:13 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2bc452641550e8ee0707cee890b67ae10a6eff5dd4a9af8413f180b2f0c80991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.7 MB (702700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed27ee59fd9b58685cf14529855592ce8e270e983e6df9e0bb2190efb602c46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:57:29 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:57:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:57:29 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:57:29 GMT
ARG TARGETARCH=arm64
# Tue, 09 Jun 2026 17:57:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:57:38 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:57:38 GMT
ENV ODOO_VERSION=19.0
# Tue, 09 Jun 2026 17:57:38 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:57:38 GMT
ARG ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
# Tue, 09 Jun 2026 17:58:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:58:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:58:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:58:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
USER odoo
# Tue, 09 Jun 2026 17:58:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:58:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7b8dfc0f44855af30a7c3f1abf87864f2fd62b846d0552b89eb2e9dd0eb378`  
		Last Modified: Tue, 09 Jun 2026 18:01:18 GMT  
		Size: 252.1 MB (252126502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e5754573198e5dd4061f098048c208de25abcd3026f0e08bce6330aff649a`  
		Last Modified: Tue, 09 Jun 2026 18:01:09 GMT  
		Size: 14.3 MB (14348186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e85d7565c355c3da04f9e02c290d90eddda3fa6af705771b0e4a4aa28b1fd6e`  
		Last Modified: Tue, 09 Jun 2026 18:01:09 GMT  
		Size: 483.7 KB (483665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d452a7ff7ba3743c74aa753e7a561fd5963e399b7207be1580f8b4003b6cdcc0`  
		Last Modified: Tue, 09 Jun 2026 18:01:21 GMT  
		Size: 406.9 MB (406862967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8ecb5024a7b0e2a758c08c523c157c997bbc678d28d2d4730654b362b6453e`  
		Last Modified: Tue, 09 Jun 2026 18:01:13 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b7ef6546c4e2f4c39d12dc9a05ced79724a123e1ac168f182e3927862a202`  
		Last Modified: Tue, 09 Jun 2026 18:01:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a79a005ab89315dacca9a22c4ac523de650cb15001e1dad142422f89d214ef`  
		Last Modified: Tue, 09 Jun 2026 18:01:14 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b183c7b3996f37f752ccf083c43b636d78fc03a9513da614666ee2e9d2be6be3`  
		Last Modified: Tue, 09 Jun 2026 18:01:17 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:8bbe8853a5d48b14e4a9c5e81e9168eeac19501d5d2874d4d3433fb93af6ee6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70808158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c18c36db8cbe4e79dce40f87698b29453fc4ba61357751c930a627c986b46d`

```dockerfile
```

-	Layers:
	-	`sha256:66534a7fec2147f8059421e60d6d4a760f6460e12a668b7bf16eec9a0e71f18c`  
		Last Modified: Tue, 09 Jun 2026 18:01:12 GMT  
		Size: 70.8 MB (70780889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e9145d435160b9f497d4a00f561d9818c8925e4c2aa1effb2bd6df3b46889d1`  
		Last Modified: Tue, 09 Jun 2026 18:01:08 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:5470e9b9161d524ad1d25443341b719213f29c73b79764a73bcdd8797513d0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.3 MB (722338651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ea28bb43a90dc02284377fb0ed6ce81d70f0c21afecd810701a68e6930a9d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260609
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
# Tue, 09 Jun 2026 17:57:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:57:36 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:57:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:57:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:57:38 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:57:38 GMT
USER odoo
# Tue, 09 Jun 2026 17:57:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34178356017677beb250135311d6774e9608044bfbfdee03dbc42085480d59d2`  
		Last Modified: Tue, 09 Jun 2026 18:03:22 GMT  
		Size: 407.5 MB (407538016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72506d4e3e106f7e71858d8d45429e1c9793c6d87c584558838ec7d3ca6d75`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e0595bff7058f3baf51cafba73d2b41ff93503263e56a78dbd68cd918a4917`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261c92b3aa4bf40ed52719181964fb77c67351e284a7e50a26f90aef996db67c`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c8aa0f168dc1b8ad3de3f5f6ab72cce094a837db8e4d214ac3192509aedf7a`  
		Last Modified: Tue, 09 Jun 2026 18:03:13 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:918b3008a560fce407928b1f427b38f701b2695fc8bb995da820955713565cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70809150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385ab7d41423fef3f7cf7a236a890720f840875df07785a7c21a539ba8355af4`

```dockerfile
```

-	Layers:
	-	`sha256:e13327efb50e4f3dc7269a380f9727e9b1a358346f136ae6347301611dc16f79`  
		Last Modified: Tue, 09 Jun 2026 18:03:16 GMT  
		Size: 70.8 MB (70781983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe3b56a1f09d0004fcbb9245ac1805820e06c1287cd016811bdf832969c1bb2f`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260609`

```console
$ docker pull odoo@sha256:3eede45a6be2a1fe4dc2911b7fc5caa8c6d5999e8f56ed8e3135160d6dc115c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20260609` - linux; amd64

```console
$ docker pull odoo@sha256:17ca74d0757479a99c2401a483cd1a84540bc8be1ba8c344d7da9745c53a6e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.3 MB (706275066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfb46877431666c2ce3209923239c8fd8081bd329e9cc2ecc7fcbef0a3dd4fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:59:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:59:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:59:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:59:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Jun 2026 17:59:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:59:09 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:59:09 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:59:09 GMT
ENV ODOO_VERSION=19.0
# Tue, 09 Jun 2026 17:59:09 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:59:09 GMT
ARG ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
# Tue, 09 Jun 2026 18:00:07 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 18:00:08 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 18:00:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 18:00:08 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
USER odoo
# Tue, 09 Jun 2026 18:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 18:00:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e9e49342a198c2c77b6de2448d6a0a4bb0b8794fd9a6b42fd74b225caef712`  
		Last Modified: Tue, 09 Jun 2026 18:02:22 GMT  
		Size: 254.7 MB (254676097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522cc0cb7f4458ba5b6860c2fcaa04d4bdc0bdcdaa8fadc61f550ac326c8e0fb`  
		Last Modified: Tue, 09 Jun 2026 18:02:14 GMT  
		Size: 14.4 MB (14370794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b697a202e915d6b16063ac31ad06e68cc09b85230d849336308fd19d1fc15b`  
		Last Modified: Tue, 09 Jun 2026 18:02:13 GMT  
		Size: 483.6 KB (483603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e480c1aae10746c1c6dc7afa7c8c825ec22aa7c31a2848378038412bba6e0`  
		Last Modified: Tue, 09 Jun 2026 18:02:25 GMT  
		Size: 407.0 MB (407009021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f25cb03abb341b969e9cc2910dc618cfc93ccf81fd95e453fd17d2120915520`  
		Last Modified: Tue, 09 Jun 2026 18:02:14 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46918ca4f13f721aafb0caf7e87f957299428177232bbae19f1e51cdfe0ae2f`  
		Last Modified: Tue, 09 Jun 2026 18:02:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120f42af961d1d413ab83e1dd42f34c8205444bd3173c363a4b92dcd62f3926b`  
		Last Modified: Tue, 09 Jun 2026 18:02:16 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5e216758713289c5e1420a19207735b6947b8475d6db9da4afb36c4d3e10d8`  
		Last Modified: Tue, 09 Jun 2026 18:02:17 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260609` - unknown; unknown

```console
$ docker pull odoo@sha256:5087fdb163c02714d66b8bd39cf24aded4de0db8bf4493b88a7e0258814d611b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70800707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05903e45208ad2a5e73cdbd72ef9aa52533ba2d169f1ec5786b4d19e9db77b45`

```dockerfile
```

-	Layers:
	-	`sha256:bdc6612443e7ac76ffcd219b4ad26bdeedcac27dba0975504834d2e2b8b25dd1`  
		Last Modified: Tue, 09 Jun 2026 18:02:17 GMT  
		Size: 70.8 MB (70773602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d421bd6853b3e6e8c3091ee3d8a28ffccc9751189423603f8630e1a0f850e351`  
		Last Modified: Tue, 09 Jun 2026 18:02:13 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260609` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2bc452641550e8ee0707cee890b67ae10a6eff5dd4a9af8413f180b2f0c80991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.7 MB (702700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed27ee59fd9b58685cf14529855592ce8e270e983e6df9e0bb2190efb602c46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:57:29 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:57:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:57:29 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:57:29 GMT
ARG TARGETARCH=arm64
# Tue, 09 Jun 2026 17:57:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:57:38 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:57:38 GMT
ENV ODOO_VERSION=19.0
# Tue, 09 Jun 2026 17:57:38 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:57:38 GMT
ARG ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
# Tue, 09 Jun 2026 17:58:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:58:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:58:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:58:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
USER odoo
# Tue, 09 Jun 2026 17:58:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:58:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7b8dfc0f44855af30a7c3f1abf87864f2fd62b846d0552b89eb2e9dd0eb378`  
		Last Modified: Tue, 09 Jun 2026 18:01:18 GMT  
		Size: 252.1 MB (252126502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e5754573198e5dd4061f098048c208de25abcd3026f0e08bce6330aff649a`  
		Last Modified: Tue, 09 Jun 2026 18:01:09 GMT  
		Size: 14.3 MB (14348186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e85d7565c355c3da04f9e02c290d90eddda3fa6af705771b0e4a4aa28b1fd6e`  
		Last Modified: Tue, 09 Jun 2026 18:01:09 GMT  
		Size: 483.7 KB (483665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d452a7ff7ba3743c74aa753e7a561fd5963e399b7207be1580f8b4003b6cdcc0`  
		Last Modified: Tue, 09 Jun 2026 18:01:21 GMT  
		Size: 406.9 MB (406862967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8ecb5024a7b0e2a758c08c523c157c997bbc678d28d2d4730654b362b6453e`  
		Last Modified: Tue, 09 Jun 2026 18:01:13 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b7ef6546c4e2f4c39d12dc9a05ced79724a123e1ac168f182e3927862a202`  
		Last Modified: Tue, 09 Jun 2026 18:01:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a79a005ab89315dacca9a22c4ac523de650cb15001e1dad142422f89d214ef`  
		Last Modified: Tue, 09 Jun 2026 18:01:14 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b183c7b3996f37f752ccf083c43b636d78fc03a9513da614666ee2e9d2be6be3`  
		Last Modified: Tue, 09 Jun 2026 18:01:17 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260609` - unknown; unknown

```console
$ docker pull odoo@sha256:8bbe8853a5d48b14e4a9c5e81e9168eeac19501d5d2874d4d3433fb93af6ee6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70808158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c18c36db8cbe4e79dce40f87698b29453fc4ba61357751c930a627c986b46d`

```dockerfile
```

-	Layers:
	-	`sha256:66534a7fec2147f8059421e60d6d4a760f6460e12a668b7bf16eec9a0e71f18c`  
		Last Modified: Tue, 09 Jun 2026 18:01:12 GMT  
		Size: 70.8 MB (70780889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e9145d435160b9f497d4a00f561d9818c8925e4c2aa1effb2bd6df3b46889d1`  
		Last Modified: Tue, 09 Jun 2026 18:01:08 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260609` - linux; ppc64le

```console
$ docker pull odoo@sha256:5470e9b9161d524ad1d25443341b719213f29c73b79764a73bcdd8797513d0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.3 MB (722338651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ea28bb43a90dc02284377fb0ed6ce81d70f0c21afecd810701a68e6930a9d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260609
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
# Tue, 09 Jun 2026 17:57:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:57:36 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:57:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:57:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:57:38 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:57:38 GMT
USER odoo
# Tue, 09 Jun 2026 17:57:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34178356017677beb250135311d6774e9608044bfbfdee03dbc42085480d59d2`  
		Last Modified: Tue, 09 Jun 2026 18:03:22 GMT  
		Size: 407.5 MB (407538016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72506d4e3e106f7e71858d8d45429e1c9793c6d87c584558838ec7d3ca6d75`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e0595bff7058f3baf51cafba73d2b41ff93503263e56a78dbd68cd918a4917`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261c92b3aa4bf40ed52719181964fb77c67351e284a7e50a26f90aef996db67c`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c8aa0f168dc1b8ad3de3f5f6ab72cce094a837db8e4d214ac3192509aedf7a`  
		Last Modified: Tue, 09 Jun 2026 18:03:13 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260609` - unknown; unknown

```console
$ docker pull odoo@sha256:918b3008a560fce407928b1f427b38f701b2695fc8bb995da820955713565cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70809150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385ab7d41423fef3f7cf7a236a890720f840875df07785a7c21a539ba8355af4`

```dockerfile
```

-	Layers:
	-	`sha256:e13327efb50e4f3dc7269a380f9727e9b1a358346f136ae6347301611dc16f79`  
		Last Modified: Tue, 09 Jun 2026 18:03:16 GMT  
		Size: 70.8 MB (70781983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe3b56a1f09d0004fcbb9245ac1805820e06c1287cd016811bdf832969c1bb2f`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:3eede45a6be2a1fe4dc2911b7fc5caa8c6d5999e8f56ed8e3135160d6dc115c7
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
$ docker pull odoo@sha256:17ca74d0757479a99c2401a483cd1a84540bc8be1ba8c344d7da9745c53a6e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.3 MB (706275066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfb46877431666c2ce3209923239c8fd8081bd329e9cc2ecc7fcbef0a3dd4fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:59:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:59:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:59:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:59:03 GMT
ARG TARGETARCH=amd64
# Tue, 09 Jun 2026 17:59:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:59:09 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:59:09 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:59:09 GMT
ENV ODOO_VERSION=19.0
# Tue, 09 Jun 2026 17:59:09 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:59:09 GMT
ARG ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
# Tue, 09 Jun 2026 18:00:07 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 18:00:08 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 18:00:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 18:00:08 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 18:00:08 GMT
USER odoo
# Tue, 09 Jun 2026 18:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 18:00:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e9e49342a198c2c77b6de2448d6a0a4bb0b8794fd9a6b42fd74b225caef712`  
		Last Modified: Tue, 09 Jun 2026 18:02:22 GMT  
		Size: 254.7 MB (254676097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522cc0cb7f4458ba5b6860c2fcaa04d4bdc0bdcdaa8fadc61f550ac326c8e0fb`  
		Last Modified: Tue, 09 Jun 2026 18:02:14 GMT  
		Size: 14.4 MB (14370794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b697a202e915d6b16063ac31ad06e68cc09b85230d849336308fd19d1fc15b`  
		Last Modified: Tue, 09 Jun 2026 18:02:13 GMT  
		Size: 483.6 KB (483603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e480c1aae10746c1c6dc7afa7c8c825ec22aa7c31a2848378038412bba6e0`  
		Last Modified: Tue, 09 Jun 2026 18:02:25 GMT  
		Size: 407.0 MB (407009021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f25cb03abb341b969e9cc2910dc618cfc93ccf81fd95e453fd17d2120915520`  
		Last Modified: Tue, 09 Jun 2026 18:02:14 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46918ca4f13f721aafb0caf7e87f957299428177232bbae19f1e51cdfe0ae2f`  
		Last Modified: Tue, 09 Jun 2026 18:02:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120f42af961d1d413ab83e1dd42f34c8205444bd3173c363a4b92dcd62f3926b`  
		Last Modified: Tue, 09 Jun 2026 18:02:16 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5e216758713289c5e1420a19207735b6947b8475d6db9da4afb36c4d3e10d8`  
		Last Modified: Tue, 09 Jun 2026 18:02:17 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:5087fdb163c02714d66b8bd39cf24aded4de0db8bf4493b88a7e0258814d611b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70800707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05903e45208ad2a5e73cdbd72ef9aa52533ba2d169f1ec5786b4d19e9db77b45`

```dockerfile
```

-	Layers:
	-	`sha256:bdc6612443e7ac76ffcd219b4ad26bdeedcac27dba0975504834d2e2b8b25dd1`  
		Last Modified: Tue, 09 Jun 2026 18:02:17 GMT  
		Size: 70.8 MB (70773602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d421bd6853b3e6e8c3091ee3d8a28ffccc9751189423603f8630e1a0f850e351`  
		Last Modified: Tue, 09 Jun 2026 18:02:13 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2bc452641550e8ee0707cee890b67ae10a6eff5dd4a9af8413f180b2f0c80991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.7 MB (702700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed27ee59fd9b58685cf14529855592ce8e270e983e6df9e0bb2190efb602c46`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 17:57:29 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2026 17:57:29 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2026 17:57:29 GMT
ENV LANG=en_US.UTF-8
# Tue, 09 Jun 2026 17:57:29 GMT
ARG TARGETARCH=arm64
# Tue, 09 Jun 2026 17:57:29 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 17:57:38 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 09 Jun 2026 17:57:38 GMT
ENV ODOO_VERSION=19.0
# Tue, 09 Jun 2026 17:57:38 GMT
ARG ODOO_RELEASE=20260609
# Tue, 09 Jun 2026 17:57:38 GMT
ARG ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
# Tue, 09 Jun 2026 17:58:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:58:40 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:58:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:58:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:58:40 GMT
USER odoo
# Tue, 09 Jun 2026 17:58:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:58:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7b8dfc0f44855af30a7c3f1abf87864f2fd62b846d0552b89eb2e9dd0eb378`  
		Last Modified: Tue, 09 Jun 2026 18:01:18 GMT  
		Size: 252.1 MB (252126502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3e5754573198e5dd4061f098048c208de25abcd3026f0e08bce6330aff649a`  
		Last Modified: Tue, 09 Jun 2026 18:01:09 GMT  
		Size: 14.3 MB (14348186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e85d7565c355c3da04f9e02c290d90eddda3fa6af705771b0e4a4aa28b1fd6e`  
		Last Modified: Tue, 09 Jun 2026 18:01:09 GMT  
		Size: 483.7 KB (483665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d452a7ff7ba3743c74aa753e7a561fd5963e399b7207be1580f8b4003b6cdcc0`  
		Last Modified: Tue, 09 Jun 2026 18:01:21 GMT  
		Size: 406.9 MB (406862967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8ecb5024a7b0e2a758c08c523c157c997bbc678d28d2d4730654b362b6453e`  
		Last Modified: Tue, 09 Jun 2026 18:01:13 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b7ef6546c4e2f4c39d12dc9a05ced79724a123e1ac168f182e3927862a202`  
		Last Modified: Tue, 09 Jun 2026 18:01:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a79a005ab89315dacca9a22c4ac523de650cb15001e1dad142422f89d214ef`  
		Last Modified: Tue, 09 Jun 2026 18:01:14 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b183c7b3996f37f752ccf083c43b636d78fc03a9513da614666ee2e9d2be6be3`  
		Last Modified: Tue, 09 Jun 2026 18:01:17 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:8bbe8853a5d48b14e4a9c5e81e9168eeac19501d5d2874d4d3433fb93af6ee6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70808158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c18c36db8cbe4e79dce40f87698b29453fc4ba61357751c930a627c986b46d`

```dockerfile
```

-	Layers:
	-	`sha256:66534a7fec2147f8059421e60d6d4a760f6460e12a668b7bf16eec9a0e71f18c`  
		Last Modified: Tue, 09 Jun 2026 18:01:12 GMT  
		Size: 70.8 MB (70780889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e9145d435160b9f497d4a00f561d9818c8925e4c2aa1effb2bd6df3b46889d1`  
		Last Modified: Tue, 09 Jun 2026 18:01:08 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:5470e9b9161d524ad1d25443341b719213f29c73b79764a73bcdd8797513d0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.3 MB (722338651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ea28bb43a90dc02284377fb0ed6ce81d70f0c21afecd810701a68e6930a9d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260609
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
# Tue, 09 Jun 2026 17:57:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 09 Jun 2026 17:57:36 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260609 ODOO_SHA=97eb8a50091bc75157c8ea02ecd839179f0dbf5d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 09 Jun 2026 17:57:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 09 Jun 2026 17:57:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 09 Jun 2026 17:57:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 09 Jun 2026 17:57:38 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 09 Jun 2026 17:57:38 GMT
USER odoo
# Tue, 09 Jun 2026 17:57:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jun 2026 17:57:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34178356017677beb250135311d6774e9608044bfbfdee03dbc42085480d59d2`  
		Last Modified: Tue, 09 Jun 2026 18:03:22 GMT  
		Size: 407.5 MB (407538016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72506d4e3e106f7e71858d8d45429e1c9793c6d87c584558838ec7d3ca6d75`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e0595bff7058f3baf51cafba73d2b41ff93503263e56a78dbd68cd918a4917`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 558.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261c92b3aa4bf40ed52719181964fb77c67351e284a7e50a26f90aef996db67c`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c8aa0f168dc1b8ad3de3f5f6ab72cce094a837db8e4d214ac3192509aedf7a`  
		Last Modified: Tue, 09 Jun 2026 18:03:13 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:918b3008a560fce407928b1f427b38f701b2695fc8bb995da820955713565cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70809150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385ab7d41423fef3f7cf7a236a890720f840875df07785a7c21a539ba8355af4`

```dockerfile
```

-	Layers:
	-	`sha256:e13327efb50e4f3dc7269a380f9727e9b1a358346f136ae6347301611dc16f79`  
		Last Modified: Tue, 09 Jun 2026 18:03:16 GMT  
		Size: 70.8 MB (70781983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe3b56a1f09d0004fcbb9245ac1805820e06c1287cd016811bdf832969c1bb2f`  
		Last Modified: Tue, 09 Jun 2026 18:03:12 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json
