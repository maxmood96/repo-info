<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250428`](#odoo160-20250428)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250428`](#odoo170-20250428)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250428`](#odoo180-20250428)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:307a634451237368c793c1a3605c233804ab3fa3f91aeeae8b51e8175fe61238
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:ef63955fbac57812d58f70e7573df961282ac7184695bb009513296021c5b80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.7 MB (584674207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53b53b8dcf3efe9e20d07cf02a420a4d6d7a98fba5cfa025b4a9d88a88eeb4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=amd64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=16.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=4dba1e739c24a394f00cb6167fd84f9c9f6819b3
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=4dba1e739c24a394f00cb6167fd84f9c9f6819b3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=4dba1e739c24a394f00cb6167fd84f9c9f6819b3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4929c47639cb8a4083b4b9efe6baa8deccf5fd720aa814bbdf409aed8dba1998`  
		Last Modified: Tue, 15 Apr 2025 16:54:36 GMT  
		Size: 219.6 MB (219626005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb3ded119a7183d31197a3e4353e09964a7e836865b268d1dc075fff0d876ef`  
		Last Modified: Tue, 15 Apr 2025 16:54:33 GMT  
		Size: 2.6 MB (2623352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37974b643a3e1a49566095c5ff9f72bb2646c9544175098362061c3551eca5c2`  
		Last Modified: Tue, 15 Apr 2025 16:54:32 GMT  
		Size: 477.8 KB (477823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4065b05dd405b0a7e5f8aa7f3d22fdfc2d9ad3984aedb3c859e793dba428ba1a`  
		Last Modified: Tue, 15 Apr 2025 16:54:39 GMT  
		Size: 331.7 MB (331687174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c438e93a65d17ebf875d1d68d86a95c2a33227a776fdba590a36299f378972`  
		Last Modified: Tue, 15 Apr 2025 16:54:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372a0b01da44e2d259b7a3066aafdf669667127dd467682e5db53ae118f3c94e`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7f3644624443bfe0428a87a8511b7a3748e312c94e8c6228c0aabd554ac1ad`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a08f2aca8e614d0dea6e0cbee8074ce4ed08a4ecbf5f560fb943474b46f1397`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:f1ea8d557e13e79edf52ce127a652aa1584b29bd627f0efe03d2ccd77e9bc2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38897126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d7a335a4f23636d0d1526c7f7ef52a5bf5117fdc716b63c2972a88f32d5d05`

```dockerfile
```

-	Layers:
	-	`sha256:5e682962c426496859c0296575acd8c4a98c293e182f55850572a10fe7fc3754`  
		Last Modified: Tue, 15 Apr 2025 16:54:33 GMT  
		Size: 38.9 MB (38870409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85533372b13da7990b91702cf52c7e6e82876129b678b10741d952e54090942b`  
		Last Modified: Tue, 15 Apr 2025 16:54:32 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:788e6ed33dd1a1e9d2d07361bfb06a0dd86fc73205d692b7c42981f9e4ca6d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.1 MB (580146402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f6691a2dede05b162b49c716d6239d57431d800d45cf68266755d8071b75f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=arm64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=16.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=4dba1e739c24a394f00cb6167fd84f9c9f6819b3
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=4dba1e739c24a394f00cb6167fd84f9c9f6819b3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=4dba1e739c24a394f00cb6167fd84f9c9f6819b3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1010af4bb7bd2fe309d28e7af442c8463be02241bdde8c7f96ecaca7ed9e9044`  
		Last Modified: Tue, 15 Apr 2025 17:05:56 GMT  
		Size: 216.9 MB (216915028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813d523d53268aac56cddef0b18dfd36fae098c7d05c633f75f904a840e3edbd`  
		Last Modified: Tue, 15 Apr 2025 17:05:51 GMT  
		Size: 2.6 MB (2631517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e9e5ba259cc382a909659688d9f42fada884ea995022ae9373ff3ea11dab03`  
		Last Modified: Tue, 15 Apr 2025 17:05:51 GMT  
		Size: 477.9 KB (477852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2cdf6595afdd7b0ded18e1c2ce5924d382d78ea22c96840b7d088fa8dc57a0`  
		Last Modified: Tue, 15 Apr 2025 17:05:58 GMT  
		Size: 331.4 MB (331370075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea0881566d23e23869b85fba58af15701dc5078afb58c7484ccfced43a7fdcf`  
		Last Modified: Tue, 15 Apr 2025 17:05:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef0e08923bd552b8ddd09fdd9c8db9339092ac221e7462c25b188fd29d48360`  
		Last Modified: Tue, 15 Apr 2025 17:05:52 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69836070997dfa14d33612278e6f4799f22970c6ebe5b383f3d73574af96535`  
		Last Modified: Tue, 15 Apr 2025 17:05:53 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5d9a931ff0d5cbbd5fe638d6548d71d4d82be8e764f29cf71d2bf1866918b8`  
		Last Modified: Tue, 15 Apr 2025 17:05:53 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:53ebe2d3cd932cac34926a4358e78e47c76b557fb177dc19debd5cf69101f2f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38903745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34088c33c50a1ad1cd5dc3c8241e07eb0824e28433dbbd093ae594f22db748c`

```dockerfile
```

-	Layers:
	-	`sha256:f204bd5016ea2e03b2e2ce0b4b9f04051738f3dc668ebe42a62fe68bc06f4e47`  
		Last Modified: Tue, 15 Apr 2025 17:05:52 GMT  
		Size: 38.9 MB (38876875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:147ef7d837a9fcf90f4991669caeb1f9af88846b7ac8d8e3bb1ff30dc1d2551b`  
		Last Modified: Tue, 15 Apr 2025 17:05:51 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:307a634451237368c793c1a3605c233804ab3fa3f91aeeae8b51e8175fe61238
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:ef63955fbac57812d58f70e7573df961282ac7184695bb009513296021c5b80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.7 MB (584674207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53b53b8dcf3efe9e20d07cf02a420a4d6d7a98fba5cfa025b4a9d88a88eeb4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=amd64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=16.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=4dba1e739c24a394f00cb6167fd84f9c9f6819b3
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=4dba1e739c24a394f00cb6167fd84f9c9f6819b3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=4dba1e739c24a394f00cb6167fd84f9c9f6819b3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4929c47639cb8a4083b4b9efe6baa8deccf5fd720aa814bbdf409aed8dba1998`  
		Last Modified: Tue, 15 Apr 2025 16:54:36 GMT  
		Size: 219.6 MB (219626005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb3ded119a7183d31197a3e4353e09964a7e836865b268d1dc075fff0d876ef`  
		Last Modified: Tue, 15 Apr 2025 16:54:33 GMT  
		Size: 2.6 MB (2623352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37974b643a3e1a49566095c5ff9f72bb2646c9544175098362061c3551eca5c2`  
		Last Modified: Tue, 15 Apr 2025 16:54:32 GMT  
		Size: 477.8 KB (477823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4065b05dd405b0a7e5f8aa7f3d22fdfc2d9ad3984aedb3c859e793dba428ba1a`  
		Last Modified: Tue, 15 Apr 2025 16:54:39 GMT  
		Size: 331.7 MB (331687174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c438e93a65d17ebf875d1d68d86a95c2a33227a776fdba590a36299f378972`  
		Last Modified: Tue, 15 Apr 2025 16:54:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372a0b01da44e2d259b7a3066aafdf669667127dd467682e5db53ae118f3c94e`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7f3644624443bfe0428a87a8511b7a3748e312c94e8c6228c0aabd554ac1ad`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a08f2aca8e614d0dea6e0cbee8074ce4ed08a4ecbf5f560fb943474b46f1397`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f1ea8d557e13e79edf52ce127a652aa1584b29bd627f0efe03d2ccd77e9bc2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38897126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d7a335a4f23636d0d1526c7f7ef52a5bf5117fdc716b63c2972a88f32d5d05`

```dockerfile
```

-	Layers:
	-	`sha256:5e682962c426496859c0296575acd8c4a98c293e182f55850572a10fe7fc3754`  
		Last Modified: Tue, 15 Apr 2025 16:54:33 GMT  
		Size: 38.9 MB (38870409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85533372b13da7990b91702cf52c7e6e82876129b678b10741d952e54090942b`  
		Last Modified: Tue, 15 Apr 2025 16:54:32 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:788e6ed33dd1a1e9d2d07361bfb06a0dd86fc73205d692b7c42981f9e4ca6d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.1 MB (580146402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f6691a2dede05b162b49c716d6239d57431d800d45cf68266755d8071b75f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=arm64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=16.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=4dba1e739c24a394f00cb6167fd84f9c9f6819b3
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=4dba1e739c24a394f00cb6167fd84f9c9f6819b3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=4dba1e739c24a394f00cb6167fd84f9c9f6819b3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1010af4bb7bd2fe309d28e7af442c8463be02241bdde8c7f96ecaca7ed9e9044`  
		Last Modified: Tue, 15 Apr 2025 17:05:56 GMT  
		Size: 216.9 MB (216915028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813d523d53268aac56cddef0b18dfd36fae098c7d05c633f75f904a840e3edbd`  
		Last Modified: Tue, 15 Apr 2025 17:05:51 GMT  
		Size: 2.6 MB (2631517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e9e5ba259cc382a909659688d9f42fada884ea995022ae9373ff3ea11dab03`  
		Last Modified: Tue, 15 Apr 2025 17:05:51 GMT  
		Size: 477.9 KB (477852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2cdf6595afdd7b0ded18e1c2ce5924d382d78ea22c96840b7d088fa8dc57a0`  
		Last Modified: Tue, 15 Apr 2025 17:05:58 GMT  
		Size: 331.4 MB (331370075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea0881566d23e23869b85fba58af15701dc5078afb58c7484ccfced43a7fdcf`  
		Last Modified: Tue, 15 Apr 2025 17:05:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef0e08923bd552b8ddd09fdd9c8db9339092ac221e7462c25b188fd29d48360`  
		Last Modified: Tue, 15 Apr 2025 17:05:52 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69836070997dfa14d33612278e6f4799f22970c6ebe5b383f3d73574af96535`  
		Last Modified: Tue, 15 Apr 2025 17:05:53 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5d9a931ff0d5cbbd5fe638d6548d71d4d82be8e764f29cf71d2bf1866918b8`  
		Last Modified: Tue, 15 Apr 2025 17:05:53 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:53ebe2d3cd932cac34926a4358e78e47c76b557fb177dc19debd5cf69101f2f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38903745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34088c33c50a1ad1cd5dc3c8241e07eb0824e28433dbbd093ae594f22db748c`

```dockerfile
```

-	Layers:
	-	`sha256:f204bd5016ea2e03b2e2ce0b4b9f04051738f3dc668ebe42a62fe68bc06f4e47`  
		Last Modified: Tue, 15 Apr 2025 17:05:52 GMT  
		Size: 38.9 MB (38876875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:147ef7d837a9fcf90f4991669caeb1f9af88846b7ac8d8e3bb1ff30dc1d2551b`  
		Last Modified: Tue, 15 Apr 2025 17:05:51 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250428`

**does not exist** (yet?)

## `odoo:17`

```console
$ docker pull odoo@sha256:d85f0dac1e1f43ba2b39b5af51c627832843caa0b5d34e34959dc04caf70d911
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
$ docker pull odoo@sha256:b4e3b7561884a802fc9617099af552cfdac79f7b44ef7a419b7195d0f5893343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.9 MB (602859531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8262cc2b7493c5ce866c1c315aa7d278a770794573d29cecf08f7c527df92c6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=amd64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=17.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00e4511b775dd24b43f97d073aeceae9fa2831378757403993c4adabf19049`  
		Last Modified: Tue, 15 Apr 2025 16:54:37 GMT  
		Size: 236.1 MB (236084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f449f567b1a64de21584a9faa6fcbdaae680feac58b10e71c1ed01f89fd34b18`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 2.5 MB (2520882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be02f75e670edcce8cb27be1bedf8b180f53875231cfbc9cfccc1f96a069fa9`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 478.8 KB (478812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db7dbab60af8b0f0347d756816d2441ea8beb34ad8e8b14c3b5aaad284832ea`  
		Last Modified: Tue, 15 Apr 2025 16:54:41 GMT  
		Size: 334.2 MB (334240486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343768b1755ddd341f650c13f9d2b6cea6235d1e80eb19e5efaffb77298ce3f4`  
		Last Modified: Tue, 15 Apr 2025 16:54:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05e671291fe3b96e5d760bfbaaadd4452ed3907f1f76876c2f85834a98efe0`  
		Last Modified: Tue, 15 Apr 2025 16:54:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c8e5308be0f62317da60fd0f5ecf464095a35a6e636de42159c936e650a5a`  
		Last Modified: Tue, 15 Apr 2025 16:54:35 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0630a9324384f44bb6f290781305464afff365bfddc2384f168df316d244b5`  
		Last Modified: Tue, 15 Apr 2025 16:54:36 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:33047920c7ff7a3de091b6295be9abf0884d4519399ce42cfb5a4d367ad0cb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39797365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8180c797319d330cb0350a45fb886ef9bfb8240446750ab07fb717ff56d1d2e7`

```dockerfile
```

-	Layers:
	-	`sha256:3bc88d213893979f0f7b116ab51749bdcba0095c7a16d53cbfc70335fbf39006`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 39.8 MB (39770530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5344e1748fcfc75b501a8da9240740a41c7777e41374abb685a70d1ab9857275`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6fab32241924b778f4a9f4ff51d3f6a9773caa02485504be3b60e2a3a96e08a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595353584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695290b2a9da7436d876eda9d510c13732a0f90d442e1015c8b1621b0725fc4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:02 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:04 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 07 Apr 2025 07:27:05 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=arm64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=17.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2594a4f5abcadf3468bc3c317f79b7f73ebb06d57ee0f286de0c10b227c587d`  
		Last Modified: Wed, 09 Apr 2025 08:53:35 GMT  
		Size: 231.2 MB (231156805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c970b5a48ed0113b06c96c6d4e719441ef9a04dd3a8500a68929cb7890d9c8e9`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 2.5 MB (2511531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e0366cc408310893605c90e7280f0a52bbab0cf9ff46838abf5e01c241795`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 478.8 KB (478842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92bcccad3c864ff72caf41581eec45c7f1a207aac9cc434fe136a22ef1c0c3`  
		Last Modified: Tue, 15 Apr 2025 17:02:20 GMT  
		Size: 333.8 MB (333849737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac7562a3ec5db12f65671a8fa22eea73aa95f50ce7a875f6b57e4509c0715df`  
		Last Modified: Tue, 15 Apr 2025 17:02:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925df5fff30bcda8f33f7847cb31964e4d64bff6d8a4fa381d01232b8bec3add`  
		Last Modified: Tue, 15 Apr 2025 17:02:13 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3538e4790217568a30990e964778b953a0059b24815c9bab377f8cab1777fc98`  
		Last Modified: Tue, 15 Apr 2025 17:02:13 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab717752cb83ff8a1a50648d4d64b3735f4ec678dbeca518a36deeda96f4f41c`  
		Last Modified: Tue, 15 Apr 2025 17:02:14 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:f7fdd5ecb459f3f3a4b6efe1170cf4e010d199a74a4f9fba485409448c40297e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39804024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f15b08c4dd85ad61272c3af46ef62a9b4aea8dae778953e39000e16270cf3bd`

```dockerfile
```

-	Layers:
	-	`sha256:5cc2bdbfc0cf8b34cd41f541372509e747d394a89d1e7ee4856758a356fa3416`  
		Last Modified: Tue, 15 Apr 2025 17:02:15 GMT  
		Size: 39.8 MB (39777037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df0b1c09d737bcfb944fc6507793109c06b97b2d8aebb2019dc1e3f4e5ff1c7`  
		Last Modified: Tue, 15 Apr 2025 17:02:13 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:c2f60e56da20ed10a236d80119a66b620b6c5ae6a656ceed16b0e370281acf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.0 MB (616991447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f9e8154706a516006b017c99b53900ea2f4a4d08d3c68a69ff7d0d57ebd96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:40 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:44 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 07 Apr 2025 07:25:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=ppc64le
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=17.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250415 ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250415 ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a80722f41cdff77b24851658db2e5345c954314931a4fd7c8e232df68a3b938`  
		Last Modified: Wed, 09 Apr 2025 06:18:02 GMT  
		Size: 243.3 MB (243268755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149b288a3581bcd08012937b5f0df65be85cd32f4fca91d5a5885f579007544`  
		Last Modified: Wed, 09 Apr 2025 06:17:47 GMT  
		Size: 2.8 MB (2838325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9abc5257b5c40fe6ab543b4c7b228a2d235b85f176c0aed824476a2fe8be5`  
		Last Modified: Wed, 09 Apr 2025 06:17:46 GMT  
		Size: 478.8 KB (478821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9fc85f563cd0d89a9cff9604362972f62364e96702dc01173a045751e1ed8a`  
		Last Modified: Tue, 15 Apr 2025 17:05:53 GMT  
		Size: 336.0 MB (335960411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2739f407638bf659a7e8e45958f0547af705dd9f425b38e555b8f729094055`  
		Last Modified: Tue, 15 Apr 2025 17:05:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0208717ddd35efdff951790665889bf9eed33522bd271fcfed5dd745442524ff`  
		Last Modified: Tue, 15 Apr 2025 17:05:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f300943c8c4c55f82899ee41e0df56230d2cefc91382a54148dd904fe8006c24`  
		Last Modified: Tue, 15 Apr 2025 17:05:43 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509ab97472f1d5f29312e32af9e5d3a8e128f17f6280b8c09154876847c4d67`  
		Last Modified: Tue, 15 Apr 2025 17:05:44 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:0d685a903e08d7790bbb28e46057720faea57ecdce54c07fb5c85bb4afea9f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39805728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643a5df1bca276cdf4cffcf20060834ac9edd7a01326f83224fefb4360fcdcb3`

```dockerfile
```

-	Layers:
	-	`sha256:145d74ac123df76fb30b331cd52288963067afd1958c249f820343ca83f69214`  
		Last Modified: Tue, 15 Apr 2025 17:05:45 GMT  
		Size: 39.8 MB (39778837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f36a3fe678346165545b0e4558cc65e3c1d5a65e98af91ac3b0d05f9edfc2643`  
		Last Modified: Tue, 15 Apr 2025 17:05:43 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:d85f0dac1e1f43ba2b39b5af51c627832843caa0b5d34e34959dc04caf70d911
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
$ docker pull odoo@sha256:b4e3b7561884a802fc9617099af552cfdac79f7b44ef7a419b7195d0f5893343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.9 MB (602859531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8262cc2b7493c5ce866c1c315aa7d278a770794573d29cecf08f7c527df92c6b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=amd64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=17.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00e4511b775dd24b43f97d073aeceae9fa2831378757403993c4adabf19049`  
		Last Modified: Tue, 15 Apr 2025 16:54:37 GMT  
		Size: 236.1 MB (236084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f449f567b1a64de21584a9faa6fcbdaae680feac58b10e71c1ed01f89fd34b18`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 2.5 MB (2520882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be02f75e670edcce8cb27be1bedf8b180f53875231cfbc9cfccc1f96a069fa9`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 478.8 KB (478812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db7dbab60af8b0f0347d756816d2441ea8beb34ad8e8b14c3b5aaad284832ea`  
		Last Modified: Tue, 15 Apr 2025 16:54:41 GMT  
		Size: 334.2 MB (334240486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343768b1755ddd341f650c13f9d2b6cea6235d1e80eb19e5efaffb77298ce3f4`  
		Last Modified: Tue, 15 Apr 2025 16:54:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05e671291fe3b96e5d760bfbaaadd4452ed3907f1f76876c2f85834a98efe0`  
		Last Modified: Tue, 15 Apr 2025 16:54:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0c8e5308be0f62317da60fd0f5ecf464095a35a6e636de42159c936e650a5a`  
		Last Modified: Tue, 15 Apr 2025 16:54:35 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0630a9324384f44bb6f290781305464afff365bfddc2384f168df316d244b5`  
		Last Modified: Tue, 15 Apr 2025 16:54:36 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:33047920c7ff7a3de091b6295be9abf0884d4519399ce42cfb5a4d367ad0cb2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39797365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8180c797319d330cb0350a45fb886ef9bfb8240446750ab07fb717ff56d1d2e7`

```dockerfile
```

-	Layers:
	-	`sha256:3bc88d213893979f0f7b116ab51749bdcba0095c7a16d53cbfc70335fbf39006`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 39.8 MB (39770530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5344e1748fcfc75b501a8da9240740a41c7777e41374abb685a70d1ab9857275`  
		Last Modified: Tue, 15 Apr 2025 16:54:34 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6fab32241924b778f4a9f4ff51d3f6a9773caa02485504be3b60e2a3a96e08a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595353584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695290b2a9da7436d876eda9d510c13732a0f90d442e1015c8b1621b0725fc4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:02 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:04 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 07 Apr 2025 07:27:05 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=arm64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=17.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2594a4f5abcadf3468bc3c317f79b7f73ebb06d57ee0f286de0c10b227c587d`  
		Last Modified: Wed, 09 Apr 2025 08:53:35 GMT  
		Size: 231.2 MB (231156805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c970b5a48ed0113b06c96c6d4e719441ef9a04dd3a8500a68929cb7890d9c8e9`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 2.5 MB (2511531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48e0366cc408310893605c90e7280f0a52bbab0cf9ff46838abf5e01c241795`  
		Last Modified: Wed, 09 Apr 2025 08:53:30 GMT  
		Size: 478.8 KB (478842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92bcccad3c864ff72caf41581eec45c7f1a207aac9cc434fe136a22ef1c0c3`  
		Last Modified: Tue, 15 Apr 2025 17:02:20 GMT  
		Size: 333.8 MB (333849737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac7562a3ec5db12f65671a8fa22eea73aa95f50ce7a875f6b57e4509c0715df`  
		Last Modified: Tue, 15 Apr 2025 17:02:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925df5fff30bcda8f33f7847cb31964e4d64bff6d8a4fa381d01232b8bec3add`  
		Last Modified: Tue, 15 Apr 2025 17:02:13 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3538e4790217568a30990e964778b953a0059b24815c9bab377f8cab1777fc98`  
		Last Modified: Tue, 15 Apr 2025 17:02:13 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab717752cb83ff8a1a50648d4d64b3735f4ec678dbeca518a36deeda96f4f41c`  
		Last Modified: Tue, 15 Apr 2025 17:02:14 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f7fdd5ecb459f3f3a4b6efe1170cf4e010d199a74a4f9fba485409448c40297e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39804024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f15b08c4dd85ad61272c3af46ef62a9b4aea8dae778953e39000e16270cf3bd`

```dockerfile
```

-	Layers:
	-	`sha256:5cc2bdbfc0cf8b34cd41f541372509e747d394a89d1e7ee4856758a356fa3416`  
		Last Modified: Tue, 15 Apr 2025 17:02:15 GMT  
		Size: 39.8 MB (39777037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df0b1c09d737bcfb944fc6507793109c06b97b2d8aebb2019dc1e3f4e5ff1c7`  
		Last Modified: Tue, 15 Apr 2025 17:02:13 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:c2f60e56da20ed10a236d80119a66b620b6c5ae6a656ceed16b0e370281acf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.0 MB (616991447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f9e8154706a516006b017c99b53900ea2f4a4d08d3c68a69ff7d0d57ebd96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:40 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:44 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 07 Apr 2025 07:25:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=ppc64le
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=17.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250415 ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250415 ODOO_SHA=c6145d4f40a728b0690ebb118d6331475c159566
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a80722f41cdff77b24851658db2e5345c954314931a4fd7c8e232df68a3b938`  
		Last Modified: Wed, 09 Apr 2025 06:18:02 GMT  
		Size: 243.3 MB (243268755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149b288a3581bcd08012937b5f0df65be85cd32f4fca91d5a5885f579007544`  
		Last Modified: Wed, 09 Apr 2025 06:17:47 GMT  
		Size: 2.8 MB (2838325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9abc5257b5c40fe6ab543b4c7b228a2d235b85f176c0aed824476a2fe8be5`  
		Last Modified: Wed, 09 Apr 2025 06:17:46 GMT  
		Size: 478.8 KB (478821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9fc85f563cd0d89a9cff9604362972f62364e96702dc01173a045751e1ed8a`  
		Last Modified: Tue, 15 Apr 2025 17:05:53 GMT  
		Size: 336.0 MB (335960411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2739f407638bf659a7e8e45958f0547af705dd9f425b38e555b8f729094055`  
		Last Modified: Tue, 15 Apr 2025 17:05:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0208717ddd35efdff951790665889bf9eed33522bd271fcfed5dd745442524ff`  
		Last Modified: Tue, 15 Apr 2025 17:05:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f300943c8c4c55f82899ee41e0df56230d2cefc91382a54148dd904fe8006c24`  
		Last Modified: Tue, 15 Apr 2025 17:05:43 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509ab97472f1d5f29312e32af9e5d3a8e128f17f6280b8c09154876847c4d67`  
		Last Modified: Tue, 15 Apr 2025 17:05:44 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0d685a903e08d7790bbb28e46057720faea57ecdce54c07fb5c85bb4afea9f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39805728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643a5df1bca276cdf4cffcf20060834ac9edd7a01326f83224fefb4360fcdcb3`

```dockerfile
```

-	Layers:
	-	`sha256:145d74ac123df76fb30b331cd52288963067afd1958c249f820343ca83f69214`  
		Last Modified: Tue, 15 Apr 2025 17:05:45 GMT  
		Size: 39.8 MB (39778837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f36a3fe678346165545b0e4558cc65e3c1d5a65e98af91ac3b0d05f9edfc2643`  
		Last Modified: Tue, 15 Apr 2025 17:05:43 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250428`

**does not exist** (yet?)

## `odoo:18`

```console
$ docker pull odoo@sha256:c4ee957e5d5c915b3cd0bd820ccd04607b3f905081450fe4d10f73a7c075d053
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
$ docker pull odoo@sha256:402357ccf5047c11bb68d4929ed961edc4e9b2a0ec100853b990ea02a843da6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 MB (672868266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e27862e2945ab8823f663c6b825b3ca96a063dd9ddd68f12377e4ee22e11f65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=amd64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=18.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d4ee5ab3aa0011d78744362dcece8f0974b85bad79781fdd6a01fb0a3e11f3`  
		Last Modified: Tue, 15 Apr 2025 16:55:15 GMT  
		Size: 254.5 MB (254516693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d98f3c2a15d4d4b6d3989d4f7ac5597f027a1bb5fef2f9d2594899861cf1f0`  
		Last Modified: Tue, 15 Apr 2025 16:55:14 GMT  
		Size: 16.7 MB (16680393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2179c4f8f8efe635f2b6ba667c1dcfdbe93bd84e5a9b1f3becae7fa86f82a706`  
		Last Modified: Tue, 15 Apr 2025 16:55:11 GMT  
		Size: 478.6 KB (478559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfb621b7c01fbe3a1a260334e0e098a6dced0de7324941d54c875639d78b8a9`  
		Last Modified: Tue, 15 Apr 2025 16:55:17 GMT  
		Size: 371.5 MB (371472527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8cf938cfb5473a0c2727ea0807c7bf5007d633cc972fa543435eac01e1daf8`  
		Last Modified: Tue, 15 Apr 2025 16:55:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00b504b70f7a36801c30a77d95dc46ff1a2183a268b614e8e34c818868d3c20`  
		Last Modified: Tue, 15 Apr 2025 16:55:13 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e24694663c798a195e0bc60c0b045d12ef193cee903c96d2a9dd4ea059d899`  
		Last Modified: Tue, 15 Apr 2025 16:55:14 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cf6ec58fce63b80be03d5d483003659f564ebdf068a28dd8c670166f114193`  
		Last Modified: Tue, 15 Apr 2025 16:55:15 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:e5e06fa27c2dbbda81fee6dd880581966d91207a2dfb976926a80d15d1cfacc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59242574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47509d04dc0fdcd86fb3e580686a8bdbb6521b7ef81d5e6dab37bddb84944464`

```dockerfile
```

-	Layers:
	-	`sha256:d1cb8d06c3142968c048436e542661c0c715a4786e5719381d333df7a7617880`  
		Last Modified: Tue, 15 Apr 2025 16:55:12 GMT  
		Size: 59.2 MB (59215438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2b592bdc6dff1214486a3e76feddc4573e3a8e9ab460fdff9f94709960db16`  
		Last Modified: Tue, 15 Apr 2025 16:55:11 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:eaab25ee64bf1f82dc06c3b041a4e7c7a374491a696db36e66694ace7d181d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.8 MB (666838623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cd11069852e1df0ca4b100ed431dd910823fdeb63d0b84cb4eb509282ddcc9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=arm64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=18.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f28a4d01496dc3c8488526531f0cd43e4849300a26c7fbdc7bb922f4cf17e6`  
		Last Modified: Wed, 09 Apr 2025 08:47:46 GMT  
		Size: 251.9 MB (251942372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76167af36288803a2b9d3fe63b5222074b3a43cc5506d8a5c08d977dd8091d5`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 14.2 MB (14248369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e618f2a8900565f418abf47d495f4cb5fe06fad01c8c287981fc193f9563c844`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0786f5ebd97ae80c7ee53223d7a832ebec632e35763f4face06e160c648ac50c`  
		Last Modified: Tue, 15 Apr 2025 16:58:34 GMT  
		Size: 371.3 MB (371319907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e608d1ebac4cda0a3efcc645b6d427a3bcf7e6d6d0b754910a6795ae38838d`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7369ea4c4bc01f06a0f685320401febc7151eefdfb1220b5c355ad312ccb50c`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06819af0622f591d0e09a8a37a327a6547650ac6fc24a782708837d017c03fa9`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5208c8276edbe0dfa10f9c22d3ebaa9cc429f766491d2ee6c1553cfb3829dbb7`  
		Last Modified: Tue, 15 Apr 2025 16:58:27 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:7e9483256482934f3f37362228b16c2cd10d63510f3c144dd28b5c1afac8083d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59250016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21841822065535879d0caa22440de17f73e1c475fcfec6e44c5f0b4c1e85938e`

```dockerfile
```

-	Layers:
	-	`sha256:887d28860681d1db5475e9000d0acddb388645dcab172e012cc82739d918d795`  
		Last Modified: Tue, 15 Apr 2025 16:58:28 GMT  
		Size: 59.2 MB (59222717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9dca536cf1630ff686e3b286b00d1cef945b78e76935f273bc4e064e1d428c`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:c4ae5c38aecccc284a1202cc58b69b7a48dff2715a3df5e7c962294504558fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.7 MB (686708135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394175eff43e420b10480dae496577f495bccecd7e5ae648a14e1bd6dd68a99b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=ppc64le
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=18.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3167c3d5d19553eb6f541f8148ce0fde5f6fdc52f91fe3262e17ab72b2bb7c`  
		Last Modified: Wed, 09 Apr 2025 06:08:46 GMT  
		Size: 265.1 MB (265078243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03255bbd404b7955ffc00de79652692a76726e85ead4098860e24b90ff0c1c`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 14.8 MB (14800172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bae32b327119195160617f8981bd0d463269ec536b920e9a12bb68122da532`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 478.6 KB (478599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05a97ed06e8627565e4e91626c0fbe528714703d50ee993b4094587768ed9b`  
		Last Modified: Tue, 15 Apr 2025 16:59:45 GMT  
		Size: 372.0 MB (372007811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8baafa7ebd79730dc3cb116e7275602a9b3a964d5935579eeca19038b9408b`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee42e6afa025999d10d70d30c48f5ddea4d8523ed09028bd85b8b2311676a2`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7381ee871fd664d625c9f0d3b24bbc88507a1364a8fd7a9f7b32869709f14db4`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef06ffcc6e95febf4f543c62624953a0c3e64fae96de0bd9fd82f5c80f31c42`  
		Last Modified: Tue, 15 Apr 2025 16:59:35 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:1d704842eb6a4249de5910ecc03b2e55627f9d3a8bc7ffbdb092f0cfbc6af9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59250771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59aa84fae3d26819be0ae583dd3f27552996e34c75cf6b5f0dca6f60093b102`

```dockerfile
```

-	Layers:
	-	`sha256:901deb28d47ba3e908cfb0ee29e11cb8bfbd163bb72424f813e11070d3bb2a21`  
		Last Modified: Tue, 15 Apr 2025 16:59:36 GMT  
		Size: 59.2 MB (59223573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:443ac72e492b1877dffb01289de8db477a441f5d88770260d2bdee5cff9e8fc5`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:c4ee957e5d5c915b3cd0bd820ccd04607b3f905081450fe4d10f73a7c075d053
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
$ docker pull odoo@sha256:402357ccf5047c11bb68d4929ed961edc4e9b2a0ec100853b990ea02a843da6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 MB (672868266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e27862e2945ab8823f663c6b825b3ca96a063dd9ddd68f12377e4ee22e11f65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=amd64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=18.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d4ee5ab3aa0011d78744362dcece8f0974b85bad79781fdd6a01fb0a3e11f3`  
		Last Modified: Tue, 15 Apr 2025 16:55:15 GMT  
		Size: 254.5 MB (254516693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d98f3c2a15d4d4b6d3989d4f7ac5597f027a1bb5fef2f9d2594899861cf1f0`  
		Last Modified: Tue, 15 Apr 2025 16:55:14 GMT  
		Size: 16.7 MB (16680393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2179c4f8f8efe635f2b6ba667c1dcfdbe93bd84e5a9b1f3becae7fa86f82a706`  
		Last Modified: Tue, 15 Apr 2025 16:55:11 GMT  
		Size: 478.6 KB (478559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfb621b7c01fbe3a1a260334e0e098a6dced0de7324941d54c875639d78b8a9`  
		Last Modified: Tue, 15 Apr 2025 16:55:17 GMT  
		Size: 371.5 MB (371472527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8cf938cfb5473a0c2727ea0807c7bf5007d633cc972fa543435eac01e1daf8`  
		Last Modified: Tue, 15 Apr 2025 16:55:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00b504b70f7a36801c30a77d95dc46ff1a2183a268b614e8e34c818868d3c20`  
		Last Modified: Tue, 15 Apr 2025 16:55:13 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e24694663c798a195e0bc60c0b045d12ef193cee903c96d2a9dd4ea059d899`  
		Last Modified: Tue, 15 Apr 2025 16:55:14 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cf6ec58fce63b80be03d5d483003659f564ebdf068a28dd8c670166f114193`  
		Last Modified: Tue, 15 Apr 2025 16:55:15 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e5e06fa27c2dbbda81fee6dd880581966d91207a2dfb976926a80d15d1cfacc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59242574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47509d04dc0fdcd86fb3e580686a8bdbb6521b7ef81d5e6dab37bddb84944464`

```dockerfile
```

-	Layers:
	-	`sha256:d1cb8d06c3142968c048436e542661c0c715a4786e5719381d333df7a7617880`  
		Last Modified: Tue, 15 Apr 2025 16:55:12 GMT  
		Size: 59.2 MB (59215438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2b592bdc6dff1214486a3e76feddc4573e3a8e9ab460fdff9f94709960db16`  
		Last Modified: Tue, 15 Apr 2025 16:55:11 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:eaab25ee64bf1f82dc06c3b041a4e7c7a374491a696db36e66694ace7d181d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.8 MB (666838623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cd11069852e1df0ca4b100ed431dd910823fdeb63d0b84cb4eb509282ddcc9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=arm64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=18.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f28a4d01496dc3c8488526531f0cd43e4849300a26c7fbdc7bb922f4cf17e6`  
		Last Modified: Wed, 09 Apr 2025 08:47:46 GMT  
		Size: 251.9 MB (251942372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76167af36288803a2b9d3fe63b5222074b3a43cc5506d8a5c08d977dd8091d5`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 14.2 MB (14248369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e618f2a8900565f418abf47d495f4cb5fe06fad01c8c287981fc193f9563c844`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0786f5ebd97ae80c7ee53223d7a832ebec632e35763f4face06e160c648ac50c`  
		Last Modified: Tue, 15 Apr 2025 16:58:34 GMT  
		Size: 371.3 MB (371319907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e608d1ebac4cda0a3efcc645b6d427a3bcf7e6d6d0b754910a6795ae38838d`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7369ea4c4bc01f06a0f685320401febc7151eefdfb1220b5c355ad312ccb50c`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06819af0622f591d0e09a8a37a327a6547650ac6fc24a782708837d017c03fa9`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5208c8276edbe0dfa10f9c22d3ebaa9cc429f766491d2ee6c1553cfb3829dbb7`  
		Last Modified: Tue, 15 Apr 2025 16:58:27 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7e9483256482934f3f37362228b16c2cd10d63510f3c144dd28b5c1afac8083d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59250016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21841822065535879d0caa22440de17f73e1c475fcfec6e44c5f0b4c1e85938e`

```dockerfile
```

-	Layers:
	-	`sha256:887d28860681d1db5475e9000d0acddb388645dcab172e012cc82739d918d795`  
		Last Modified: Tue, 15 Apr 2025 16:58:28 GMT  
		Size: 59.2 MB (59222717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9dca536cf1630ff686e3b286b00d1cef945b78e76935f273bc4e064e1d428c`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:c4ae5c38aecccc284a1202cc58b69b7a48dff2715a3df5e7c962294504558fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.7 MB (686708135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394175eff43e420b10480dae496577f495bccecd7e5ae648a14e1bd6dd68a99b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=ppc64le
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=18.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3167c3d5d19553eb6f541f8148ce0fde5f6fdc52f91fe3262e17ab72b2bb7c`  
		Last Modified: Wed, 09 Apr 2025 06:08:46 GMT  
		Size: 265.1 MB (265078243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03255bbd404b7955ffc00de79652692a76726e85ead4098860e24b90ff0c1c`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 14.8 MB (14800172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bae32b327119195160617f8981bd0d463269ec536b920e9a12bb68122da532`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 478.6 KB (478599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05a97ed06e8627565e4e91626c0fbe528714703d50ee993b4094587768ed9b`  
		Last Modified: Tue, 15 Apr 2025 16:59:45 GMT  
		Size: 372.0 MB (372007811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8baafa7ebd79730dc3cb116e7275602a9b3a964d5935579eeca19038b9408b`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee42e6afa025999d10d70d30c48f5ddea4d8523ed09028bd85b8b2311676a2`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7381ee871fd664d625c9f0d3b24bbc88507a1364a8fd7a9f7b32869709f14db4`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef06ffcc6e95febf4f543c62624953a0c3e64fae96de0bd9fd82f5c80f31c42`  
		Last Modified: Tue, 15 Apr 2025 16:59:35 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1d704842eb6a4249de5910ecc03b2e55627f9d3a8bc7ffbdb092f0cfbc6af9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59250771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59aa84fae3d26819be0ae583dd3f27552996e34c75cf6b5f0dca6f60093b102`

```dockerfile
```

-	Layers:
	-	`sha256:901deb28d47ba3e908cfb0ee29e11cb8bfbd163bb72424f813e11070d3bb2a21`  
		Last Modified: Tue, 15 Apr 2025 16:59:36 GMT  
		Size: 59.2 MB (59223573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:443ac72e492b1877dffb01289de8db477a441f5d88770260d2bdee5cff9e8fc5`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250428`

**does not exist** (yet?)

## `odoo:latest`

```console
$ docker pull odoo@sha256:c4ee957e5d5c915b3cd0bd820ccd04607b3f905081450fe4d10f73a7c075d053
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
$ docker pull odoo@sha256:402357ccf5047c11bb68d4929ed961edc4e9b2a0ec100853b990ea02a843da6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.9 MB (672868266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e27862e2945ab8823f663c6b825b3ca96a063dd9ddd68f12377e4ee22e11f65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=amd64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=18.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d4ee5ab3aa0011d78744362dcece8f0974b85bad79781fdd6a01fb0a3e11f3`  
		Last Modified: Tue, 15 Apr 2025 16:55:15 GMT  
		Size: 254.5 MB (254516693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d98f3c2a15d4d4b6d3989d4f7ac5597f027a1bb5fef2f9d2594899861cf1f0`  
		Last Modified: Tue, 15 Apr 2025 16:55:14 GMT  
		Size: 16.7 MB (16680393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2179c4f8f8efe635f2b6ba667c1dcfdbe93bd84e5a9b1f3becae7fa86f82a706`  
		Last Modified: Tue, 15 Apr 2025 16:55:11 GMT  
		Size: 478.6 KB (478559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfb621b7c01fbe3a1a260334e0e098a6dced0de7324941d54c875639d78b8a9`  
		Last Modified: Tue, 15 Apr 2025 16:55:17 GMT  
		Size: 371.5 MB (371472527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8cf938cfb5473a0c2727ea0807c7bf5007d633cc972fa543435eac01e1daf8`  
		Last Modified: Tue, 15 Apr 2025 16:55:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00b504b70f7a36801c30a77d95dc46ff1a2183a268b614e8e34c818868d3c20`  
		Last Modified: Tue, 15 Apr 2025 16:55:13 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e24694663c798a195e0bc60c0b045d12ef193cee903c96d2a9dd4ea059d899`  
		Last Modified: Tue, 15 Apr 2025 16:55:14 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cf6ec58fce63b80be03d5d483003659f564ebdf068a28dd8c670166f114193`  
		Last Modified: Tue, 15 Apr 2025 16:55:15 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:e5e06fa27c2dbbda81fee6dd880581966d91207a2dfb976926a80d15d1cfacc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59242574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47509d04dc0fdcd86fb3e580686a8bdbb6521b7ef81d5e6dab37bddb84944464`

```dockerfile
```

-	Layers:
	-	`sha256:d1cb8d06c3142968c048436e542661c0c715a4786e5719381d333df7a7617880`  
		Last Modified: Tue, 15 Apr 2025 16:55:12 GMT  
		Size: 59.2 MB (59215438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2b592bdc6dff1214486a3e76feddc4573e3a8e9ab460fdff9f94709960db16`  
		Last Modified: Tue, 15 Apr 2025 16:55:11 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:eaab25ee64bf1f82dc06c3b041a4e7c7a374491a696db36e66694ace7d181d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.8 MB (666838623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cd11069852e1df0ca4b100ed431dd910823fdeb63d0b84cb4eb509282ddcc9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=arm64
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=18.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f28a4d01496dc3c8488526531f0cd43e4849300a26c7fbdc7bb922f4cf17e6`  
		Last Modified: Wed, 09 Apr 2025 08:47:46 GMT  
		Size: 251.9 MB (251942372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76167af36288803a2b9d3fe63b5222074b3a43cc5506d8a5c08d977dd8091d5`  
		Last Modified: Wed, 09 Apr 2025 08:47:41 GMT  
		Size: 14.2 MB (14248369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e618f2a8900565f418abf47d495f4cb5fe06fad01c8c287981fc193f9563c844`  
		Last Modified: Wed, 09 Apr 2025 08:47:40 GMT  
		Size: 478.6 KB (478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0786f5ebd97ae80c7ee53223d7a832ebec632e35763f4face06e160c648ac50c`  
		Last Modified: Tue, 15 Apr 2025 16:58:34 GMT  
		Size: 371.3 MB (371319907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e608d1ebac4cda0a3efcc645b6d427a3bcf7e6d6d0b754910a6795ae38838d`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7369ea4c4bc01f06a0f685320401febc7151eefdfb1220b5c355ad312ccb50c`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06819af0622f591d0e09a8a37a327a6547650ac6fc24a782708837d017c03fa9`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5208c8276edbe0dfa10f9c22d3ebaa9cc429f766491d2ee6c1553cfb3829dbb7`  
		Last Modified: Tue, 15 Apr 2025 16:58:27 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7e9483256482934f3f37362228b16c2cd10d63510f3c144dd28b5c1afac8083d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59250016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21841822065535879d0caa22440de17f73e1c475fcfec6e44c5f0b4c1e85938e`

```dockerfile
```

-	Layers:
	-	`sha256:887d28860681d1db5475e9000d0acddb388645dcab172e012cc82739d918d795`  
		Last Modified: Tue, 15 Apr 2025 16:58:28 GMT  
		Size: 59.2 MB (59222717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9dca536cf1630ff686e3b286b00d1cef945b78e76935f273bc4e064e1d428c`  
		Last Modified: Tue, 15 Apr 2025 16:58:26 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:c4ae5c38aecccc284a1202cc58b69b7a48dff2715a3df5e7c962294504558fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.7 MB (686708135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394175eff43e420b10480dae496577f495bccecd7e5ae648a14e1bd6dd68a99b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:25:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 15 Apr 2025 14:25:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Apr 2025 14:25:16 GMT
ARG TARGETARCH=ppc64le
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_VERSION=18.0
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_RELEASE=20250415
# Tue, 15 Apr 2025 14:25:16 GMT
ARG ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250415 ODOO_SHA=5011f09e346a00583ad38558edfcf309360fa53c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 15 Apr 2025 14:25:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 15 Apr 2025 14:25:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 15 Apr 2025 14:25:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 15 Apr 2025 14:25:16 GMT
USER odoo
# Tue, 15 Apr 2025 14:25:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 15 Apr 2025 14:25:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3167c3d5d19553eb6f541f8148ce0fde5f6fdc52f91fe3262e17ab72b2bb7c`  
		Last Modified: Wed, 09 Apr 2025 06:08:46 GMT  
		Size: 265.1 MB (265078243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03255bbd404b7955ffc00de79652692a76726e85ead4098860e24b90ff0c1c`  
		Last Modified: Wed, 09 Apr 2025 06:08:29 GMT  
		Size: 14.8 MB (14800172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bae32b327119195160617f8981bd0d463269ec536b920e9a12bb68122da532`  
		Last Modified: Wed, 09 Apr 2025 06:08:28 GMT  
		Size: 478.6 KB (478599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f05a97ed06e8627565e4e91626c0fbe528714703d50ee993b4094587768ed9b`  
		Last Modified: Tue, 15 Apr 2025 16:59:45 GMT  
		Size: 372.0 MB (372007811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8baafa7ebd79730dc3cb116e7275602a9b3a964d5935579eeca19038b9408b`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee42e6afa025999d10d70d30c48f5ddea4d8523ed09028bd85b8b2311676a2`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7381ee871fd664d625c9f0d3b24bbc88507a1364a8fd7a9f7b32869709f14db4`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef06ffcc6e95febf4f543c62624953a0c3e64fae96de0bd9fd82f5c80f31c42`  
		Last Modified: Tue, 15 Apr 2025 16:59:35 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:1d704842eb6a4249de5910ecc03b2e55627f9d3a8bc7ffbdb092f0cfbc6af9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59250771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59aa84fae3d26819be0ae583dd3f27552996e34c75cf6b5f0dca6f60093b102`

```dockerfile
```

-	Layers:
	-	`sha256:901deb28d47ba3e908cfb0ee29e11cb8bfbd163bb72424f813e11070d3bb2a21`  
		Last Modified: Tue, 15 Apr 2025 16:59:36 GMT  
		Size: 59.2 MB (59223573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:443ac72e492b1877dffb01289de8db477a441f5d88770260d2bdee5cff9e8fc5`  
		Last Modified: Tue, 15 Apr 2025 16:59:34 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
