<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:02a9d544b416470c352571738063c2c6cb25d74dc4d1c12170ecf841c609c57c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:9feebd33a647b802f2dc049d9d33c08c7f5c410fd92fc18cdd23cf70f937a450
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.2 MB (564211797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b14bbcf4224058c50fbd5c4d26b5815226b478cb335482b33ba36c960b37526`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:24:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 May 2024 06:24:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 May 2024 06:24:09 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 06:28:11 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 May 2024 06:28:18 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:28:19 GMT
RUN npm install -g rtlcss
# Tue, 14 May 2024 06:28:19 GMT
ENV ODOO_VERSION=15.0
# Tue, 14 May 2024 06:28:19 GMT
ARG ODOO_RELEASE=20240513
# Tue, 14 May 2024 06:28:20 GMT
ARG ODOO_SHA=4404e4d34277a7d77918d1dcea67bc0fc98ba9fe
# Tue, 14 May 2024 06:29:31 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=4404e4d34277a7d77918d1dcea67bc0fc98ba9fe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 May 2024 06:29:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 May 2024 06:29:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 May 2024 06:29:36 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=4404e4d34277a7d77918d1dcea67bc0fc98ba9fe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 May 2024 06:29:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 May 2024 06:29:36 GMT
EXPOSE 8069 8071 8072
# Tue, 14 May 2024 06:29:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 May 2024 06:29:36 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 May 2024 06:29:36 GMT
USER odoo
# Tue, 14 May 2024 06:29:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 May 2024 06:29:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea40ad4a45f4b6dd315642bcec70191945b71cd2af71c7a6efb5254cc49b5010`  
		Last Modified: Tue, 14 May 2024 06:31:04 GMT  
		Size: 220.3 MB (220293966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fa8ded4cc4001dba966a84834cf85d169712b7d70fbf24e172808da07e63b6`  
		Last Modified: Tue, 14 May 2024 06:30:41 GMT  
		Size: 2.6 MB (2627617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9b453d4158c92ef2aca30b32dd3b29ffd490df134dc97fc51461db177c3490`  
		Last Modified: Tue, 14 May 2024 06:30:40 GMT  
		Size: 457.8 KB (457841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69495ea3e4b8f2077ca20cc22f88e7d501cb6bb4545d306c25a242af94ecea7`  
		Last Modified: Tue, 14 May 2024 06:31:13 GMT  
		Size: 309.4 MB (309395978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d0043e8ba852265877811d6f016c524344a0f2a0d5c1e62455b14b0cc6288`  
		Last Modified: Tue, 14 May 2024 06:30:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e62284a514dfb19b716085e0e93aaebb62320d6b8cd7c8bb3fb06f425043f8`  
		Last Modified: Tue, 14 May 2024 06:30:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078ef13c9a910619df003f581e4e646859fb737c6168c39b557fdb602bdf10c8`  
		Last Modified: Tue, 14 May 2024 06:30:38 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dab3d48725542308437b6c2c24ea5053d196955a579947e91c3e28fa998c1e`  
		Last Modified: Tue, 14 May 2024 06:30:38 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:02a9d544b416470c352571738063c2c6cb25d74dc4d1c12170ecf841c609c57c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:9feebd33a647b802f2dc049d9d33c08c7f5c410fd92fc18cdd23cf70f937a450
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.2 MB (564211797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b14bbcf4224058c50fbd5c4d26b5815226b478cb335482b33ba36c960b37526`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:24:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 May 2024 06:24:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 May 2024 06:24:09 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 06:28:11 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 May 2024 06:28:18 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:28:19 GMT
RUN npm install -g rtlcss
# Tue, 14 May 2024 06:28:19 GMT
ENV ODOO_VERSION=15.0
# Tue, 14 May 2024 06:28:19 GMT
ARG ODOO_RELEASE=20240513
# Tue, 14 May 2024 06:28:20 GMT
ARG ODOO_SHA=4404e4d34277a7d77918d1dcea67bc0fc98ba9fe
# Tue, 14 May 2024 06:29:31 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=4404e4d34277a7d77918d1dcea67bc0fc98ba9fe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 May 2024 06:29:35 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 May 2024 06:29:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 May 2024 06:29:36 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=4404e4d34277a7d77918d1dcea67bc0fc98ba9fe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 May 2024 06:29:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 May 2024 06:29:36 GMT
EXPOSE 8069 8071 8072
# Tue, 14 May 2024 06:29:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 May 2024 06:29:36 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 May 2024 06:29:36 GMT
USER odoo
# Tue, 14 May 2024 06:29:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 May 2024 06:29:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea40ad4a45f4b6dd315642bcec70191945b71cd2af71c7a6efb5254cc49b5010`  
		Last Modified: Tue, 14 May 2024 06:31:04 GMT  
		Size: 220.3 MB (220293966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6fa8ded4cc4001dba966a84834cf85d169712b7d70fbf24e172808da07e63b6`  
		Last Modified: Tue, 14 May 2024 06:30:41 GMT  
		Size: 2.6 MB (2627617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9b453d4158c92ef2aca30b32dd3b29ffd490df134dc97fc51461db177c3490`  
		Last Modified: Tue, 14 May 2024 06:30:40 GMT  
		Size: 457.8 KB (457841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69495ea3e4b8f2077ca20cc22f88e7d501cb6bb4545d306c25a242af94ecea7`  
		Last Modified: Tue, 14 May 2024 06:31:13 GMT  
		Size: 309.4 MB (309395978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d0043e8ba852265877811d6f016c524344a0f2a0d5c1e62455b14b0cc6288`  
		Last Modified: Tue, 14 May 2024 06:30:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e62284a514dfb19b716085e0e93aaebb62320d6b8cd7c8bb3fb06f425043f8`  
		Last Modified: Tue, 14 May 2024 06:30:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078ef13c9a910619df003f581e4e646859fb737c6168c39b557fdb602bdf10c8`  
		Last Modified: Tue, 14 May 2024 06:30:38 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36dab3d48725542308437b6c2c24ea5053d196955a579947e91c3e28fa998c1e`  
		Last Modified: Tue, 14 May 2024 06:30:38 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:e99671976488967d63bc7a261abf5d4000ab41fc3d8579f8bde9c53039c16583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:10b53c87fb92e6321cc1fde75ab24d18989756ca40ec1c58c67f58c861eb1a97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.4 MB (583411508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16be33f6300cc65aec0840e25c51e7086f15ba785564e3ada981b75d9b855740`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:24:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 May 2024 06:24:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 May 2024 06:24:09 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 06:24:09 GMT
ARG TARGETARCH
# Tue, 14 May 2024 06:25:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 May 2024 06:25:33 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:25:34 GMT
RUN npm install -g rtlcss
# Tue, 14 May 2024 06:25:34 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 May 2024 06:25:35 GMT
ARG ODOO_RELEASE=20240513
# Tue, 14 May 2024 06:25:35 GMT
ARG ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
# Tue, 14 May 2024 06:26:57 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 May 2024 06:27:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 May 2024 06:27:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 May 2024 06:27:03 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 May 2024 06:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 May 2024 06:27:03 GMT
EXPOSE 8069 8071 8072
# Tue, 14 May 2024 06:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 May 2024 06:27:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 May 2024 06:27:03 GMT
USER odoo
# Tue, 14 May 2024 06:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 May 2024 06:27:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dd11cf2c21af8615b61e3dbd1b8723e7f8ff946ab8e659574473e8c56d2747`  
		Last Modified: Tue, 14 May 2024 06:30:17 GMT  
		Size: 219.6 MB (219604316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72edce1bfd24cc7da1c616e8c9befeccf36d1d316df1042dbffb3b7fb3fa56e0`  
		Last Modified: Tue, 14 May 2024 06:29:52 GMT  
		Size: 2.6 MB (2631771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c82449ba0706bbb6228873e57f51101bbe2541f20750b593344a99758d1528c`  
		Last Modified: Tue, 14 May 2024 06:29:52 GMT  
		Size: 457.8 KB (457832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25e6e30a884907e7b7325dfc96cd6f59706622f20c0b24ce557e383171cd420`  
		Last Modified: Tue, 14 May 2024 06:30:30 GMT  
		Size: 329.3 MB (329281195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176135d89b5f9b51fe2d41e5063331898d06b544e88e596ac3f736654dcfc446`  
		Last Modified: Tue, 14 May 2024 06:29:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfa4cac316b033ff9db2061a4f75d7a1986ea69ac1c228beab39418890a303e`  
		Last Modified: Tue, 14 May 2024 06:29:50 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9874e77004623fc146d066461b9148194d94eea721126726faa5518de9f88ada`  
		Last Modified: Tue, 14 May 2024 06:29:50 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5ef2e27ba3ebda784aeb78f2cabe6b39bfc2ac484bf8c400c96ef2108f8538`  
		Last Modified: Tue, 14 May 2024 06:29:50 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b9474d1604d3149d13d92a327f7169441ae2f1e359e2f4f4522343155596fdae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.0 MB (579031851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a553824f3810ff355b0a91433890048a4b66ae3148d9a73301a17d32a18015c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:18:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 May 2024 03:18:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 May 2024 03:18:17 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 03:18:17 GMT
ARG TARGETARCH
# Tue, 14 May 2024 03:19:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 May 2024 03:19:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:19:33 GMT
RUN npm install -g rtlcss
# Tue, 14 May 2024 03:19:33 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 May 2024 03:19:33 GMT
ARG ODOO_RELEASE=20240513
# Tue, 14 May 2024 03:19:33 GMT
ARG ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
# Tue, 14 May 2024 03:20:44 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 May 2024 03:20:53 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 May 2024 03:20:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 May 2024 03:20:53 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 May 2024 03:20:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 May 2024 03:20:53 GMT
EXPOSE 8069 8071 8072
# Tue, 14 May 2024 03:20:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 May 2024 03:20:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 May 2024 03:20:54 GMT
USER odoo
# Tue, 14 May 2024 03:20:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 May 2024 03:20:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9077b05c2503285c816c8d0ec20c262afab1d37d7c1458f869e1c49ce30692e9`  
		Last Modified: Tue, 14 May 2024 03:21:38 GMT  
		Size: 216.9 MB (216903630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1c62643d80953158eddfd212a017bc3bafb94ab42e56d07f343598db7dd618`  
		Last Modified: Tue, 14 May 2024 03:21:21 GMT  
		Size: 2.6 MB (2635958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6d463cb0a2eba98e4f30d77ee71cb72eb187444bfc6ba5b5dc26b6d5dac3fe`  
		Last Modified: Tue, 14 May 2024 03:21:21 GMT  
		Size: 457.8 KB (457820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56eecb388024d60af4daff1460f415f6a67a855ffde39becb0391a1b16936728`  
		Last Modified: Tue, 14 May 2024 03:21:49 GMT  
		Size: 328.9 MB (328945068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592e54f7d6d3f50713c1387da9d92e4628a6dfd306c80d7518c798ca17d403cf`  
		Last Modified: Tue, 14 May 2024 03:21:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f0aedad45bfd438a36977a3a590713fcbdc616731e224eccf68c7e007ee507`  
		Last Modified: Tue, 14 May 2024 03:21:19 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9776684b42d2add03d365aec8587c1e892936fac5da6f221ed1d3a01aa43aad`  
		Last Modified: Tue, 14 May 2024 03:21:19 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef987d4314f42f52089e5730dc9e03ac2ace73017e475d9b9ded7706b7b3532f`  
		Last Modified: Tue, 14 May 2024 03:21:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:b9407e86b8dea7157f9017242d0a3e09e6fdc25bcb92f2a6d01866e11ed87594
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.0 MB (597974423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc0afa67acf173b81f3532cfd75f1c1c7b0b89a596e549e9fe9afbbd8a78dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:49:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 May 2024 06:49:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 May 2024 06:49:03 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 06:49:03 GMT
ARG TARGETARCH
# Tue, 14 May 2024 06:51:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 May 2024 06:51:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:51:28 GMT
RUN npm install -g rtlcss
# Tue, 14 May 2024 06:51:29 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 May 2024 06:51:29 GMT
ARG ODOO_RELEASE=20240513
# Tue, 14 May 2024 06:51:29 GMT
ARG ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
# Tue, 14 May 2024 06:53:08 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 May 2024 06:53:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 May 2024 06:53:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 May 2024 06:53:23 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 May 2024 06:53:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 May 2024 06:53:24 GMT
EXPOSE 8069 8071 8072
# Tue, 14 May 2024 06:53:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 May 2024 06:53:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 May 2024 06:53:25 GMT
USER odoo
# Tue, 14 May 2024 06:53:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 May 2024 06:53:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b658fbb1be9daae6fbbc8fbea40a485580b25fd8a668fa695ba783647d36d0`  
		Last Modified: Tue, 14 May 2024 06:54:07 GMT  
		Size: 228.6 MB (228601038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720f659dc34db98c24504e3e3bde30cf4b11d53631f8cc2be6e798974500c842`  
		Last Modified: Tue, 14 May 2024 06:53:38 GMT  
		Size: 2.9 MB (2876624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67be58a75a3017b540fa0773b755756160f0449479f04c7df510dc37771c5391`  
		Last Modified: Tue, 14 May 2024 06:53:37 GMT  
		Size: 457.9 KB (457884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a018b6491feb5d36215b697bffd95d93fe1f9764cb942221fcab0f9d0bbcc6da`  
		Last Modified: Tue, 14 May 2024 06:54:20 GMT  
		Size: 330.7 MB (330725254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e86b385fe3870c0326c49b7f671cdf8a4cce3d655c4d95f76484f699ed3dd0`  
		Last Modified: Tue, 14 May 2024 06:53:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c5373e94e1c793d981479d07cbbc8890753f1242aac0bd19262d23b71b2acd`  
		Last Modified: Tue, 14 May 2024 06:53:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f48c468d2b6249dc89e6af80e545b054eeb6a4045410a84dd389f69d56d2d9`  
		Last Modified: Tue, 14 May 2024 06:53:35 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cbec06c483a0c7ed0532c0a0431fd1e001a8901367d68b114e2e7835043185`  
		Last Modified: Tue, 14 May 2024 06:53:35 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:e99671976488967d63bc7a261abf5d4000ab41fc3d8579f8bde9c53039c16583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:10b53c87fb92e6321cc1fde75ab24d18989756ca40ec1c58c67f58c861eb1a97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.4 MB (583411508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16be33f6300cc65aec0840e25c51e7086f15ba785564e3ada981b75d9b855740`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:24:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 May 2024 06:24:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 May 2024 06:24:09 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 06:24:09 GMT
ARG TARGETARCH
# Tue, 14 May 2024 06:25:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 May 2024 06:25:33 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:25:34 GMT
RUN npm install -g rtlcss
# Tue, 14 May 2024 06:25:34 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 May 2024 06:25:35 GMT
ARG ODOO_RELEASE=20240513
# Tue, 14 May 2024 06:25:35 GMT
ARG ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
# Tue, 14 May 2024 06:26:57 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 May 2024 06:27:02 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 May 2024 06:27:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 May 2024 06:27:03 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 May 2024 06:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 May 2024 06:27:03 GMT
EXPOSE 8069 8071 8072
# Tue, 14 May 2024 06:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 May 2024 06:27:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 May 2024 06:27:03 GMT
USER odoo
# Tue, 14 May 2024 06:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 May 2024 06:27:04 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dd11cf2c21af8615b61e3dbd1b8723e7f8ff946ab8e659574473e8c56d2747`  
		Last Modified: Tue, 14 May 2024 06:30:17 GMT  
		Size: 219.6 MB (219604316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72edce1bfd24cc7da1c616e8c9befeccf36d1d316df1042dbffb3b7fb3fa56e0`  
		Last Modified: Tue, 14 May 2024 06:29:52 GMT  
		Size: 2.6 MB (2631771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c82449ba0706bbb6228873e57f51101bbe2541f20750b593344a99758d1528c`  
		Last Modified: Tue, 14 May 2024 06:29:52 GMT  
		Size: 457.8 KB (457832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25e6e30a884907e7b7325dfc96cd6f59706622f20c0b24ce557e383171cd420`  
		Last Modified: Tue, 14 May 2024 06:30:30 GMT  
		Size: 329.3 MB (329281195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176135d89b5f9b51fe2d41e5063331898d06b544e88e596ac3f736654dcfc446`  
		Last Modified: Tue, 14 May 2024 06:29:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfa4cac316b033ff9db2061a4f75d7a1986ea69ac1c228beab39418890a303e`  
		Last Modified: Tue, 14 May 2024 06:29:50 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9874e77004623fc146d066461b9148194d94eea721126726faa5518de9f88ada`  
		Last Modified: Tue, 14 May 2024 06:29:50 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5ef2e27ba3ebda784aeb78f2cabe6b39bfc2ac484bf8c400c96ef2108f8538`  
		Last Modified: Tue, 14 May 2024 06:29:50 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b9474d1604d3149d13d92a327f7169441ae2f1e359e2f4f4522343155596fdae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.0 MB (579031851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a553824f3810ff355b0a91433890048a4b66ae3148d9a73301a17d32a18015c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:18:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 May 2024 03:18:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 May 2024 03:18:17 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 03:18:17 GMT
ARG TARGETARCH
# Tue, 14 May 2024 03:19:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 May 2024 03:19:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:19:33 GMT
RUN npm install -g rtlcss
# Tue, 14 May 2024 03:19:33 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 May 2024 03:19:33 GMT
ARG ODOO_RELEASE=20240513
# Tue, 14 May 2024 03:19:33 GMT
ARG ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
# Tue, 14 May 2024 03:20:44 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 May 2024 03:20:53 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 May 2024 03:20:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 May 2024 03:20:53 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 May 2024 03:20:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 May 2024 03:20:53 GMT
EXPOSE 8069 8071 8072
# Tue, 14 May 2024 03:20:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 May 2024 03:20:53 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 May 2024 03:20:54 GMT
USER odoo
# Tue, 14 May 2024 03:20:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 May 2024 03:20:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9077b05c2503285c816c8d0ec20c262afab1d37d7c1458f869e1c49ce30692e9`  
		Last Modified: Tue, 14 May 2024 03:21:38 GMT  
		Size: 216.9 MB (216903630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1c62643d80953158eddfd212a017bc3bafb94ab42e56d07f343598db7dd618`  
		Last Modified: Tue, 14 May 2024 03:21:21 GMT  
		Size: 2.6 MB (2635958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6d463cb0a2eba98e4f30d77ee71cb72eb187444bfc6ba5b5dc26b6d5dac3fe`  
		Last Modified: Tue, 14 May 2024 03:21:21 GMT  
		Size: 457.8 KB (457820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56eecb388024d60af4daff1460f415f6a67a855ffde39becb0391a1b16936728`  
		Last Modified: Tue, 14 May 2024 03:21:49 GMT  
		Size: 328.9 MB (328945068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592e54f7d6d3f50713c1387da9d92e4628a6dfd306c80d7518c798ca17d403cf`  
		Last Modified: Tue, 14 May 2024 03:21:19 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f0aedad45bfd438a36977a3a590713fcbdc616731e224eccf68c7e007ee507`  
		Last Modified: Tue, 14 May 2024 03:21:19 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9776684b42d2add03d365aec8587c1e892936fac5da6f221ed1d3a01aa43aad`  
		Last Modified: Tue, 14 May 2024 03:21:19 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef987d4314f42f52089e5730dc9e03ac2ace73017e475d9b9ded7706b7b3532f`  
		Last Modified: Tue, 14 May 2024 03:21:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b9407e86b8dea7157f9017242d0a3e09e6fdc25bcb92f2a6d01866e11ed87594
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.0 MB (597974423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bc0afa67acf173b81f3532cfd75f1c1c7b0b89a596e549e9fe9afbbd8a78dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:49:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 14 May 2024 06:49:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 14 May 2024 06:49:03 GMT
ENV LANG=C.UTF-8
# Tue, 14 May 2024 06:49:03 GMT
ARG TARGETARCH
# Tue, 14 May 2024 06:51:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 14 May 2024 06:51:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:51:28 GMT
RUN npm install -g rtlcss
# Tue, 14 May 2024 06:51:29 GMT
ENV ODOO_VERSION=16.0
# Tue, 14 May 2024 06:51:29 GMT
ARG ODOO_RELEASE=20240513
# Tue, 14 May 2024 06:51:29 GMT
ARG ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
# Tue, 14 May 2024 06:53:08 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 14 May 2024 06:53:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Tue, 14 May 2024 06:53:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 14 May 2024 06:53:23 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=a1e0f0f72a7c09367bc0c09c4b75e801d15e11e6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 14 May 2024 06:53:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 14 May 2024 06:53:24 GMT
EXPOSE 8069 8071 8072
# Tue, 14 May 2024 06:53:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 14 May 2024 06:53:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 14 May 2024 06:53:25 GMT
USER odoo
# Tue, 14 May 2024 06:53:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 May 2024 06:53:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b658fbb1be9daae6fbbc8fbea40a485580b25fd8a668fa695ba783647d36d0`  
		Last Modified: Tue, 14 May 2024 06:54:07 GMT  
		Size: 228.6 MB (228601038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720f659dc34db98c24504e3e3bde30cf4b11d53631f8cc2be6e798974500c842`  
		Last Modified: Tue, 14 May 2024 06:53:38 GMT  
		Size: 2.9 MB (2876624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67be58a75a3017b540fa0773b755756160f0449479f04c7df510dc37771c5391`  
		Last Modified: Tue, 14 May 2024 06:53:37 GMT  
		Size: 457.9 KB (457884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a018b6491feb5d36215b697bffd95d93fe1f9764cb942221fcab0f9d0bbcc6da`  
		Last Modified: Tue, 14 May 2024 06:54:20 GMT  
		Size: 330.7 MB (330725254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e86b385fe3870c0326c49b7f671cdf8a4cce3d655c4d95f76484f699ed3dd0`  
		Last Modified: Tue, 14 May 2024 06:53:35 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c5373e94e1c793d981479d07cbbc8890753f1242aac0bd19262d23b71b2acd`  
		Last Modified: Tue, 14 May 2024 06:53:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f48c468d2b6249dc89e6af80e545b054eeb6a4045410a84dd389f69d56d2d9`  
		Last Modified: Tue, 14 May 2024 06:53:35 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cbec06c483a0c7ed0532c0a0431fd1e001a8901367d68b114e2e7835043185`  
		Last Modified: Tue, 14 May 2024 06:53:35 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:bab5b91bba6efa9c3a8d7344869f23017408c9f691dd11640082ddcba8efaeb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:6e5ba0d61b58fc7b96ade28cc5629b5f692856ed384a9108d15c8206e487deb1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602978917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa2814a4c9a50904788e5d5f506b01d8a60522430409949170317fa91aa3f1e`
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
# Thu, 02 May 2024 01:48:45 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 May 2024 01:48:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 May 2024 01:48:45 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 01:48:45 GMT
ARG TARGETARCH
# Thu, 02 May 2024 01:50:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 May 2024 01:51:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:51:11 GMT
RUN npm install -g rtlcss
# Thu, 02 May 2024 01:51:11 GMT
ENV ODOO_VERSION=17.0
# Mon, 13 May 2024 18:28:27 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:28:27 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:30:35 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:30:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:30:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:30:39 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:30:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:30:39 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:30:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:30:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:30:40 GMT
USER odoo
# Mon, 13 May 2024 18:30:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:30:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc6a2729a2817ef06e9dda70829f42a53a97239cae20c2bacedb195d297ba0b`  
		Last Modified: Thu, 02 May 2024 01:54:19 GMT  
		Size: 233.7 MB (233722654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be642aed9f10700697e78c3c790686681140e29aac403b5a36a0bf73d128f74`  
		Last Modified: Thu, 02 May 2024 01:53:52 GMT  
		Size: 2.5 MB (2530493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652e6603812dc2dc31a6600fde661fd0f472c1db60ffdf7f131ca3a241518b9b`  
		Last Modified: Thu, 02 May 2024 01:53:52 GMT  
		Size: 459.5 KB (459460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65861a35542bca13181ce6ae828b535c337ec8897b9c5a9b8240c840d3ec1434`  
		Last Modified: Mon, 13 May 2024 18:34:39 GMT  
		Size: 335.8 MB (335824189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c3c424a2c0119aaae6dc6c0c7c36f6015fd141576e8681dd796fb5ac9dda24`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dc686ff2f80940cdf1f1b51d3a964529d48714241428611384d8e419dcfdfd`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d90839dd1bbc5aac92b108f886a9913e8894a7e727e616896200cb8d66b59b`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b54b8005a8d54a591ee56f9c4191b6d76968ef966bcef57950a803eb8753765`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3c0ca70dd35b3b9cef81b809cd61330031f5d8d83267890045d4cba7633d3b66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597933367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efebd7e8f7746af6b8c3dcad0d5ded350a10d66dd39d85d9cbc29991a9bdef3a`
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
# Thu, 02 May 2024 01:28:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 May 2024 01:28:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 May 2024 01:28:33 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 01:28:33 GMT
ARG TARGETARCH
# Thu, 02 May 2024 01:30:55 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 May 2024 01:31:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:31:11 GMT
RUN npm install -g rtlcss
# Thu, 02 May 2024 01:31:11 GMT
ENV ODOO_VERSION=17.0
# Mon, 13 May 2024 18:41:09 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:41:09 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:43:29 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:43:31 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:43:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:43:32 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:43:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:43:32 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:43:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:43:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:43:32 GMT
USER odoo
# Mon, 13 May 2024 18:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:43:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d5983fdb42d6e446c61ffd23ea73a31d297eb116faab716b0a05982385aef7`  
		Last Modified: Thu, 02 May 2024 01:33:56 GMT  
		Size: 231.1 MB (231130596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf51c84c847e95593779366fe62fbfc47376ab1cbb6b6a2891c096fbce365476`  
		Last Modified: Thu, 02 May 2024 01:33:37 GMT  
		Size: 2.5 MB (2523315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4821493b21fb69aad8b99473d2e8c6fbc2c2ef7b66fe8255b0856b3929182b80`  
		Last Modified: Thu, 02 May 2024 01:33:37 GMT  
		Size: 459.4 KB (459401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ee49d1eabf028301ea2a11a1775c4af9248d3b185413b84b12748d4036ce3`  
		Last Modified: Mon, 13 May 2024 18:46:11 GMT  
		Size: 335.4 MB (335416400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bac3b6f3c326d9f185b80d4cb49521f4802280e7a9467caea5707140f5ab42`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8ed1b1c23e00865a567d859c903725f72f925814e87b4b4478d0e9f219f609`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03076fe297bd9ca2328b3894bf5aa4b030baba681f8ea5b3020ec6813b590b76`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01e5be11ac4fe759e0b1541348ed40421f5cd8e4682b691ad72fa7f9fbd0027`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:e55c6407a34bb127e07f326fc982540c2739056ffac68d5973869a5bf6529214
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.7 MB (619729556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331cab68dcb4e956dec4edc771ec19218d5fb00ea34e159303513a85eb38f468`
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
# Thu, 02 May 2024 02:35:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 May 2024 02:35:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 May 2024 02:35:02 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 02:35:02 GMT
ARG TARGETARCH
# Thu, 02 May 2024 02:39:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 May 2024 02:39:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:39:35 GMT
RUN npm install -g rtlcss
# Thu, 02 May 2024 02:39:35 GMT
ENV ODOO_VERSION=17.0
# Mon, 13 May 2024 18:19:35 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:19:35 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:22:25 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:22:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:22:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:22:40 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:22:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:22:41 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:22:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:22:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:22:42 GMT
USER odoo
# Mon, 13 May 2024 18:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:22:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25675fc6cdcee8d4016b34ff54239a1de0278ba15b6ac0af402ce732889c506`  
		Last Modified: Thu, 02 May 2024 02:44:10 GMT  
		Size: 243.3 MB (243299854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c366bfa6d5ff39e1ec4aa3977efc2d8ae2e82fea7a6c2dd6b4cc84294fcb1146`  
		Last Modified: Thu, 02 May 2024 02:43:38 GMT  
		Size: 2.8 MB (2806021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d273121e099b8f0742274ce6668b942df2b9a2e52972b6c0d594210cbec8bc9d`  
		Last Modified: Thu, 02 May 2024 02:43:38 GMT  
		Size: 459.4 KB (459395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1a470130561a48fae6876b48e9254b884e31dc27190aba1481b59737628f46`  
		Last Modified: Mon, 13 May 2024 18:26:26 GMT  
		Size: 337.6 MB (337573295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda04e11bc01f4929cf74507168fdd8ba877aeac1b0c6ed8a8f294b5d9fed06`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086883b3f68b91457cf2cc2aef14fc4ead0c6f3786a176c8242d78917148c9c9`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5fba5cd3adda80bc4eec30943db60c7205635d565322a472cbb4a7d9def70f`  
		Last Modified: Mon, 13 May 2024 18:25:32 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975520576c156a7b790fa9a782efc2c4a786168fb235f2213f59a93cb8393d0f`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:bab5b91bba6efa9c3a8d7344869f23017408c9f691dd11640082ddcba8efaeb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:6e5ba0d61b58fc7b96ade28cc5629b5f692856ed384a9108d15c8206e487deb1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602978917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa2814a4c9a50904788e5d5f506b01d8a60522430409949170317fa91aa3f1e`
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
# Thu, 02 May 2024 01:48:45 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 May 2024 01:48:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 May 2024 01:48:45 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 01:48:45 GMT
ARG TARGETARCH
# Thu, 02 May 2024 01:50:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 May 2024 01:51:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:51:11 GMT
RUN npm install -g rtlcss
# Thu, 02 May 2024 01:51:11 GMT
ENV ODOO_VERSION=17.0
# Mon, 13 May 2024 18:28:27 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:28:27 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:30:35 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:30:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:30:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:30:39 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:30:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:30:39 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:30:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:30:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:30:40 GMT
USER odoo
# Mon, 13 May 2024 18:30:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:30:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc6a2729a2817ef06e9dda70829f42a53a97239cae20c2bacedb195d297ba0b`  
		Last Modified: Thu, 02 May 2024 01:54:19 GMT  
		Size: 233.7 MB (233722654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be642aed9f10700697e78c3c790686681140e29aac403b5a36a0bf73d128f74`  
		Last Modified: Thu, 02 May 2024 01:53:52 GMT  
		Size: 2.5 MB (2530493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652e6603812dc2dc31a6600fde661fd0f472c1db60ffdf7f131ca3a241518b9b`  
		Last Modified: Thu, 02 May 2024 01:53:52 GMT  
		Size: 459.5 KB (459460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65861a35542bca13181ce6ae828b535c337ec8897b9c5a9b8240c840d3ec1434`  
		Last Modified: Mon, 13 May 2024 18:34:39 GMT  
		Size: 335.8 MB (335824189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c3c424a2c0119aaae6dc6c0c7c36f6015fd141576e8681dd796fb5ac9dda24`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dc686ff2f80940cdf1f1b51d3a964529d48714241428611384d8e419dcfdfd`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d90839dd1bbc5aac92b108f886a9913e8894a7e727e616896200cb8d66b59b`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b54b8005a8d54a591ee56f9c4191b6d76968ef966bcef57950a803eb8753765`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3c0ca70dd35b3b9cef81b809cd61330031f5d8d83267890045d4cba7633d3b66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597933367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efebd7e8f7746af6b8c3dcad0d5ded350a10d66dd39d85d9cbc29991a9bdef3a`
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
# Thu, 02 May 2024 01:28:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 May 2024 01:28:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 May 2024 01:28:33 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 01:28:33 GMT
ARG TARGETARCH
# Thu, 02 May 2024 01:30:55 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 May 2024 01:31:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:31:11 GMT
RUN npm install -g rtlcss
# Thu, 02 May 2024 01:31:11 GMT
ENV ODOO_VERSION=17.0
# Mon, 13 May 2024 18:41:09 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:41:09 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:43:29 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:43:31 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:43:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:43:32 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:43:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:43:32 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:43:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:43:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:43:32 GMT
USER odoo
# Mon, 13 May 2024 18:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:43:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d5983fdb42d6e446c61ffd23ea73a31d297eb116faab716b0a05982385aef7`  
		Last Modified: Thu, 02 May 2024 01:33:56 GMT  
		Size: 231.1 MB (231130596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf51c84c847e95593779366fe62fbfc47376ab1cbb6b6a2891c096fbce365476`  
		Last Modified: Thu, 02 May 2024 01:33:37 GMT  
		Size: 2.5 MB (2523315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4821493b21fb69aad8b99473d2e8c6fbc2c2ef7b66fe8255b0856b3929182b80`  
		Last Modified: Thu, 02 May 2024 01:33:37 GMT  
		Size: 459.4 KB (459401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ee49d1eabf028301ea2a11a1775c4af9248d3b185413b84b12748d4036ce3`  
		Last Modified: Mon, 13 May 2024 18:46:11 GMT  
		Size: 335.4 MB (335416400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bac3b6f3c326d9f185b80d4cb49521f4802280e7a9467caea5707140f5ab42`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8ed1b1c23e00865a567d859c903725f72f925814e87b4b4478d0e9f219f609`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03076fe297bd9ca2328b3894bf5aa4b030baba681f8ea5b3020ec6813b590b76`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01e5be11ac4fe759e0b1541348ed40421f5cd8e4682b691ad72fa7f9fbd0027`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:e55c6407a34bb127e07f326fc982540c2739056ffac68d5973869a5bf6529214
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.7 MB (619729556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331cab68dcb4e956dec4edc771ec19218d5fb00ea34e159303513a85eb38f468`
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
# Thu, 02 May 2024 02:35:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 May 2024 02:35:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 May 2024 02:35:02 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 02:35:02 GMT
ARG TARGETARCH
# Thu, 02 May 2024 02:39:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 May 2024 02:39:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:39:35 GMT
RUN npm install -g rtlcss
# Thu, 02 May 2024 02:39:35 GMT
ENV ODOO_VERSION=17.0
# Mon, 13 May 2024 18:19:35 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:19:35 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:22:25 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:22:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:22:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:22:40 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:22:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:22:41 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:22:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:22:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:22:42 GMT
USER odoo
# Mon, 13 May 2024 18:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:22:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25675fc6cdcee8d4016b34ff54239a1de0278ba15b6ac0af402ce732889c506`  
		Last Modified: Thu, 02 May 2024 02:44:10 GMT  
		Size: 243.3 MB (243299854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c366bfa6d5ff39e1ec4aa3977efc2d8ae2e82fea7a6c2dd6b4cc84294fcb1146`  
		Last Modified: Thu, 02 May 2024 02:43:38 GMT  
		Size: 2.8 MB (2806021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d273121e099b8f0742274ce6668b942df2b9a2e52972b6c0d594210cbec8bc9d`  
		Last Modified: Thu, 02 May 2024 02:43:38 GMT  
		Size: 459.4 KB (459395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1a470130561a48fae6876b48e9254b884e31dc27190aba1481b59737628f46`  
		Last Modified: Mon, 13 May 2024 18:26:26 GMT  
		Size: 337.6 MB (337573295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda04e11bc01f4929cf74507168fdd8ba877aeac1b0c6ed8a8f294b5d9fed06`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086883b3f68b91457cf2cc2aef14fc4ead0c6f3786a176c8242d78917148c9c9`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5fba5cd3adda80bc4eec30943db60c7205635d565322a472cbb4a7d9def70f`  
		Last Modified: Mon, 13 May 2024 18:25:32 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975520576c156a7b790fa9a782efc2c4a786168fb235f2213f59a93cb8393d0f`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:bab5b91bba6efa9c3a8d7344869f23017408c9f691dd11640082ddcba8efaeb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:6e5ba0d61b58fc7b96ade28cc5629b5f692856ed384a9108d15c8206e487deb1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602978917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa2814a4c9a50904788e5d5f506b01d8a60522430409949170317fa91aa3f1e`
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
# Thu, 02 May 2024 01:48:45 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 May 2024 01:48:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 May 2024 01:48:45 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 01:48:45 GMT
ARG TARGETARCH
# Thu, 02 May 2024 01:50:57 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 May 2024 01:51:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:51:11 GMT
RUN npm install -g rtlcss
# Thu, 02 May 2024 01:51:11 GMT
ENV ODOO_VERSION=17.0
# Mon, 13 May 2024 18:28:27 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:28:27 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:30:35 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:30:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:30:38 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:30:39 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:30:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:30:39 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:30:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:30:39 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:30:40 GMT
USER odoo
# Mon, 13 May 2024 18:30:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:30:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc6a2729a2817ef06e9dda70829f42a53a97239cae20c2bacedb195d297ba0b`  
		Last Modified: Thu, 02 May 2024 01:54:19 GMT  
		Size: 233.7 MB (233722654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be642aed9f10700697e78c3c790686681140e29aac403b5a36a0bf73d128f74`  
		Last Modified: Thu, 02 May 2024 01:53:52 GMT  
		Size: 2.5 MB (2530493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652e6603812dc2dc31a6600fde661fd0f472c1db60ffdf7f131ca3a241518b9b`  
		Last Modified: Thu, 02 May 2024 01:53:52 GMT  
		Size: 459.5 KB (459460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65861a35542bca13181ce6ae828b535c337ec8897b9c5a9b8240c840d3ec1434`  
		Last Modified: Mon, 13 May 2024 18:34:39 GMT  
		Size: 335.8 MB (335824189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c3c424a2c0119aaae6dc6c0c7c36f6015fd141576e8681dd796fb5ac9dda24`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02dc686ff2f80940cdf1f1b51d3a964529d48714241428611384d8e419dcfdfd`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d90839dd1bbc5aac92b108f886a9913e8894a7e727e616896200cb8d66b59b`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b54b8005a8d54a591ee56f9c4191b6d76968ef966bcef57950a803eb8753765`  
		Last Modified: Mon, 13 May 2024 18:34:00 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3c0ca70dd35b3b9cef81b809cd61330031f5d8d83267890045d4cba7633d3b66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597933367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efebd7e8f7746af6b8c3dcad0d5ded350a10d66dd39d85d9cbc29991a9bdef3a`
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
# Thu, 02 May 2024 01:28:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 May 2024 01:28:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 May 2024 01:28:33 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 01:28:33 GMT
ARG TARGETARCH
# Thu, 02 May 2024 01:30:55 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 May 2024 01:31:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:31:11 GMT
RUN npm install -g rtlcss
# Thu, 02 May 2024 01:31:11 GMT
ENV ODOO_VERSION=17.0
# Mon, 13 May 2024 18:41:09 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:41:09 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:43:29 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:43:31 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:43:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:43:32 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:43:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:43:32 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:43:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:43:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:43:32 GMT
USER odoo
# Mon, 13 May 2024 18:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:43:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d5983fdb42d6e446c61ffd23ea73a31d297eb116faab716b0a05982385aef7`  
		Last Modified: Thu, 02 May 2024 01:33:56 GMT  
		Size: 231.1 MB (231130596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf51c84c847e95593779366fe62fbfc47376ab1cbb6b6a2891c096fbce365476`  
		Last Modified: Thu, 02 May 2024 01:33:37 GMT  
		Size: 2.5 MB (2523315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4821493b21fb69aad8b99473d2e8c6fbc2c2ef7b66fe8255b0856b3929182b80`  
		Last Modified: Thu, 02 May 2024 01:33:37 GMT  
		Size: 459.4 KB (459401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0ee49d1eabf028301ea2a11a1775c4af9248d3b185413b84b12748d4036ce3`  
		Last Modified: Mon, 13 May 2024 18:46:11 GMT  
		Size: 335.4 MB (335416400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bac3b6f3c326d9f185b80d4cb49521f4802280e7a9467caea5707140f5ab42`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8ed1b1c23e00865a567d859c903725f72f925814e87b4b4478d0e9f219f609`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03076fe297bd9ca2328b3894bf5aa4b030baba681f8ea5b3020ec6813b590b76`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01e5be11ac4fe759e0b1541348ed40421f5cd8e4682b691ad72fa7f9fbd0027`  
		Last Modified: Mon, 13 May 2024 18:45:33 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:e55c6407a34bb127e07f326fc982540c2739056ffac68d5973869a5bf6529214
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.7 MB (619729556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331cab68dcb4e956dec4edc771ec19218d5fb00ea34e159303513a85eb38f468`
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
# Thu, 02 May 2024 02:35:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 May 2024 02:35:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 May 2024 02:35:02 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 02:35:02 GMT
ARG TARGETARCH
# Thu, 02 May 2024 02:39:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 May 2024 02:39:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:39:35 GMT
RUN npm install -g rtlcss
# Thu, 02 May 2024 02:39:35 GMT
ENV ODOO_VERSION=17.0
# Mon, 13 May 2024 18:19:35 GMT
ARG ODOO_RELEASE=20240513
# Mon, 13 May 2024 18:19:35 GMT
ARG ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
# Mon, 13 May 2024 18:22:25 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 13 May 2024 18:22:38 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 13 May 2024 18:22:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 13 May 2024 18:22:40 GMT
# ARGS: ODOO_RELEASE=20240513 ODOO_SHA=5ec8f5007ad564279fd06edfe90cf197711fcfd3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 13 May 2024 18:22:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 13 May 2024 18:22:41 GMT
EXPOSE 8069 8071 8072
# Mon, 13 May 2024 18:22:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 13 May 2024 18:22:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 13 May 2024 18:22:42 GMT
USER odoo
# Mon, 13 May 2024 18:22:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 May 2024 18:22:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25675fc6cdcee8d4016b34ff54239a1de0278ba15b6ac0af402ce732889c506`  
		Last Modified: Thu, 02 May 2024 02:44:10 GMT  
		Size: 243.3 MB (243299854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c366bfa6d5ff39e1ec4aa3977efc2d8ae2e82fea7a6c2dd6b4cc84294fcb1146`  
		Last Modified: Thu, 02 May 2024 02:43:38 GMT  
		Size: 2.8 MB (2806021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d273121e099b8f0742274ce6668b942df2b9a2e52972b6c0d594210cbec8bc9d`  
		Last Modified: Thu, 02 May 2024 02:43:38 GMT  
		Size: 459.4 KB (459395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1a470130561a48fae6876b48e9254b884e31dc27190aba1481b59737628f46`  
		Last Modified: Mon, 13 May 2024 18:26:26 GMT  
		Size: 337.6 MB (337573295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bda04e11bc01f4929cf74507168fdd8ba877aeac1b0c6ed8a8f294b5d9fed06`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086883b3f68b91457cf2cc2aef14fc4ead0c6f3786a176c8242d78917148c9c9`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5fba5cd3adda80bc4eec30943db60c7205635d565322a472cbb4a7d9def70f`  
		Last Modified: Mon, 13 May 2024 18:25:32 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975520576c156a7b790fa9a782efc2c4a786168fb235f2213f59a93cb8393d0f`  
		Last Modified: Mon, 13 May 2024 18:25:31 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
