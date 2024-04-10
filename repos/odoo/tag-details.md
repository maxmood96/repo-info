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
$ docker pull odoo@sha256:69bfc98b8368b5bd77268850ef7ca42e49ec0113e87942a9fe8dd6d77bf21fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:7687d0f8f38e3d857ea172bc5b9a3ae4b4e8cfd22ae8d5c75619d09256f7753e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564059639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac7c6d796e72db9e7d548b8c949538a6ea4d073476bd68e9a5629f4602e7c11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 10:04:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 10:04:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 10:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 10:08:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 10:08:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:08:17 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 10:08:17 GMT
ENV ODOO_VERSION=15.0
# Fri, 05 Apr 2024 21:06:06 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 21:06:06 GMT
ARG ODOO_SHA=2bb90b9cfad5e331027ffdf9b59d8d40c776ca1c
# Fri, 05 Apr 2024 21:07:17 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=2bb90b9cfad5e331027ffdf9b59d8d40c776ca1c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 21:07:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 21:07:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 21:07:22 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=2bb90b9cfad5e331027ffdf9b59d8d40c776ca1c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 21:07:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 21:07:22 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 21:07:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 21:07:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 21:07:23 GMT
USER odoo
# Fri, 05 Apr 2024 21:07:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 21:07:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f755211239ff95827bdf02a4263220ef29f30514bfb45e9719405f61b7eb1fe`  
		Last Modified: Tue, 12 Mar 2024 10:11:05 GMT  
		Size: 220.3 MB (220291492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e350755bf81273bed12fdf2a9b0164c28be00db54322cbca54eb5c183aa61798`  
		Last Modified: Tue, 12 Mar 2024 10:10:40 GMT  
		Size: 2.6 MB (2625910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1465eacd304d72395092a950bf1096c7504f0a76ef0820999e0bda4a3e4068ea`  
		Last Modified: Tue, 12 Mar 2024 10:10:40 GMT  
		Size: 462.5 KB (462463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90d9dabbe7a6e687411aa99c785eb7fd6181cab179f9d001d849cd1569e86cb`  
		Last Modified: Fri, 05 Apr 2024 21:09:48 GMT  
		Size: 309.3 MB (309254818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3510ec4335894955c87809f88e471079206bf8b53a98bc45cc77cd4f3cadbd9e`  
		Last Modified: Fri, 05 Apr 2024 21:09:14 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea3c2d91a629b12372d8607e6f6047a0fc109685edcaa56fb1aa9818a6034a1`  
		Last Modified: Fri, 05 Apr 2024 21:09:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883881f306b6b8f14374ac6718cb593d62be14ecda40590fec94ae1400c1cb8e`  
		Last Modified: Fri, 05 Apr 2024 21:09:14 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444509bb4476bb98ef65d10cdd4321128b62011d1569650452ec282c86da057f`  
		Last Modified: Fri, 05 Apr 2024 21:09:14 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:69bfc98b8368b5bd77268850ef7ca42e49ec0113e87942a9fe8dd6d77bf21fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:7687d0f8f38e3d857ea172bc5b9a3ae4b4e8cfd22ae8d5c75619d09256f7753e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564059639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac7c6d796e72db9e7d548b8c949538a6ea4d073476bd68e9a5629f4602e7c11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 10:04:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 10:04:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 10:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 10:08:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 10:08:16 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:08:17 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 10:08:17 GMT
ENV ODOO_VERSION=15.0
# Fri, 05 Apr 2024 21:06:06 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 21:06:06 GMT
ARG ODOO_SHA=2bb90b9cfad5e331027ffdf9b59d8d40c776ca1c
# Fri, 05 Apr 2024 21:07:17 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=2bb90b9cfad5e331027ffdf9b59d8d40c776ca1c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 21:07:21 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 21:07:21 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 21:07:22 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=2bb90b9cfad5e331027ffdf9b59d8d40c776ca1c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 21:07:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 21:07:22 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 21:07:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 21:07:22 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 21:07:23 GMT
USER odoo
# Fri, 05 Apr 2024 21:07:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 21:07:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f755211239ff95827bdf02a4263220ef29f30514bfb45e9719405f61b7eb1fe`  
		Last Modified: Tue, 12 Mar 2024 10:11:05 GMT  
		Size: 220.3 MB (220291492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e350755bf81273bed12fdf2a9b0164c28be00db54322cbca54eb5c183aa61798`  
		Last Modified: Tue, 12 Mar 2024 10:10:40 GMT  
		Size: 2.6 MB (2625910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1465eacd304d72395092a950bf1096c7504f0a76ef0820999e0bda4a3e4068ea`  
		Last Modified: Tue, 12 Mar 2024 10:10:40 GMT  
		Size: 462.5 KB (462463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90d9dabbe7a6e687411aa99c785eb7fd6181cab179f9d001d849cd1569e86cb`  
		Last Modified: Fri, 05 Apr 2024 21:09:48 GMT  
		Size: 309.3 MB (309254818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3510ec4335894955c87809f88e471079206bf8b53a98bc45cc77cd4f3cadbd9e`  
		Last Modified: Fri, 05 Apr 2024 21:09:14 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea3c2d91a629b12372d8607e6f6047a0fc109685edcaa56fb1aa9818a6034a1`  
		Last Modified: Fri, 05 Apr 2024 21:09:14 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883881f306b6b8f14374ac6718cb593d62be14ecda40590fec94ae1400c1cb8e`  
		Last Modified: Fri, 05 Apr 2024 21:09:14 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444509bb4476bb98ef65d10cdd4321128b62011d1569650452ec282c86da057f`  
		Last Modified: Fri, 05 Apr 2024 21:09:14 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:e517d486ffea0f94bfb7761d1fe4c9e82d8308c8a99946936a884c2f5b75aa3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:f5f9f0c5f36470750613101dabfa8d1925b2e5a71db2036ebc66c88f94c36d94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.0 MB (583036172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497e0625a3adb64d86ca554c204bc75abfec2753b142eaf41fc4eae33596b733`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 10:04:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 10:04:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 10:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 10:04:23 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 10:05:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 10:05:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:05:44 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 10:05:44 GMT
ENV ODOO_VERSION=16.0
# Fri, 05 Apr 2024 21:04:27 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 21:04:27 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Fri, 05 Apr 2024 21:05:51 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 21:05:54 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 21:05:55 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 21:05:55 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 21:05:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 21:05:55 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 21:05:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 21:05:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 21:05:56 GMT
USER odoo
# Fri, 05 Apr 2024 21:05:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 21:05:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b6792aa9ce6832f860c6e1be9f969760839af537e4898318aa4f6bfb1c028b`  
		Last Modified: Tue, 12 Mar 2024 10:10:15 GMT  
		Size: 219.6 MB (219603015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2315d87d3b1baf540e35d3ecccceacc3315ff5069bf3f9bfa9cfb289aeba9`  
		Last Modified: Tue, 12 Mar 2024 10:09:51 GMT  
		Size: 2.6 MB (2630018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075dda5b3fd48c7f6681e64745ee86cffaf18fee97aeba54f00d6ee06b5ba526`  
		Last Modified: Tue, 12 Mar 2024 10:09:50 GMT  
		Size: 462.5 KB (462467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0253237b85f992f84d06543a3fdaa33bd785073cce602da953a664026523fc`  
		Last Modified: Fri, 05 Apr 2024 21:09:05 GMT  
		Size: 328.9 MB (328915720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1944354a03ff87800dd9ed77da090cb327eb836afa309de7e8e229e0c6fa056f`  
		Last Modified: Fri, 05 Apr 2024 21:08:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141f9bb882f810119549b785e8ff22ec8ae97094159af137de1c989a91e1cd72`  
		Last Modified: Fri, 05 Apr 2024 21:08:27 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5e0b711f8ec83af3664f815865b72fd48fc592de6e89d3aa614773420d2529`  
		Last Modified: Fri, 05 Apr 2024 21:08:27 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d24020db9c292d13a2b6303e8364567c51431a208e5cf796aa0067698ed999`  
		Last Modified: Fri, 05 Apr 2024 21:08:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d25324e54f423555d398be28c22753c7f145dd72872033f85ec2b2c49b6fb70b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.7 MB (578656343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edb1eebdb62b7447cbab778e25400df04ffb2bc3b9acb366d95dae2f3a879d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:50:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 06:50:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 06:50:11 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:50:11 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 06:51:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 06:51:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:51:26 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 06:51:26 GMT
ENV ODOO_VERSION=16.0
# Wed, 10 Apr 2024 06:51:26 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 06:51:26 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Wed, 10 Apr 2024 06:52:49 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 06:52:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 06:52:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 06:52:57 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 06:52:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 06:52:57 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 06:52:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 06:52:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 06:52:57 GMT
USER odoo
# Wed, 10 Apr 2024 06:52:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 06:52:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc553ed1e447dba5d7cd1531a7067a247647cf58771061d9030c71c8b6d14d`  
		Last Modified: Wed, 10 Apr 2024 06:53:31 GMT  
		Size: 216.9 MB (216903831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505728a268c4b89109c2cb3fd49cd9b1dcb63f30c015647bfc1823b0d6774451`  
		Last Modified: Wed, 10 Apr 2024 06:53:14 GMT  
		Size: 2.6 MB (2635212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1bbf349d40bf14f17d8931d7c97e93408ecb08a25175182d63b2592b4c6eac`  
		Last Modified: Wed, 10 Apr 2024 06:53:14 GMT  
		Size: 458.4 KB (458432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34a8e6a4767bc55af7ea7f4c72631e551d41cffa762efc5b73253398390b1d8`  
		Last Modified: Wed, 10 Apr 2024 06:53:42 GMT  
		Size: 328.6 MB (328580095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10420d0695cf8e799078b908497f64f76b477dba223add41e473ff0f111d500`  
		Last Modified: Wed, 10 Apr 2024 06:53:12 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac577dfe3513d6f531784319195b12c9d051aeeb1b1f4a38ae5b3d1166e8e98f`  
		Last Modified: Wed, 10 Apr 2024 06:53:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d695a8a535ed74173ccf570325545b1e22d4819c7f7cf75da76d252b805d00`  
		Last Modified: Wed, 10 Apr 2024 06:53:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a80f87e184f87ed1df1e8ac737ca7988f37e7389d3953e463fcfac6c7eab663`  
		Last Modified: Wed, 10 Apr 2024 06:53:11 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:b000be7d56bb89a61e279293108dc3d25ebc3f1b1ae333649bcdfe39348771e3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.6 MB (597599721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b544ebb4a0072205ed70d0d5459c855d81e85f26e5edf838fb338d1e0687112`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:27:00 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
# Wed, 10 Apr 2024 01:27:02 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:11:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:11:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:11:35 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 12:11:36 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 12:15:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 12:16:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:16:14 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 12:16:15 GMT
ENV ODOO_VERSION=16.0
# Wed, 10 Apr 2024 12:16:16 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 12:16:17 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Wed, 10 Apr 2024 12:18:59 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 12:19:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 12:19:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 12:19:15 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 12:19:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 12:19:17 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 12:19:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 12:19:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 12:19:18 GMT
USER odoo
# Wed, 10 Apr 2024 12:19:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 12:19:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e559728a938c6bae80d026fa29f2c38efa24baa26b769f31f8c84966d4e1df`  
		Last Modified: Wed, 10 Apr 2024 12:20:10 GMT  
		Size: 228.6 MB (228600553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b203ec44cc6f31bfbafaf9862e879fbf8d13940d76cf12c60f413c3d4f7d2413`  
		Last Modified: Wed, 10 Apr 2024 12:19:39 GMT  
		Size: 2.9 MB (2876015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe4e2bda71d3574d3ec461cc470d98dc69f9167871208766805ae0ec7e810f`  
		Last Modified: Wed, 10 Apr 2024 12:19:39 GMT  
		Size: 458.4 KB (458444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44bb59b6134dc895bace6ac001f367ef7df7681d8bb0e8675308b146b5f5fe0`  
		Last Modified: Wed, 10 Apr 2024 12:20:24 GMT  
		Size: 330.4 MB (330358150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9110cd77d7285e0fad9ff5e2b37e63a937f68ecd61c4aa9e602d19637a4e399`  
		Last Modified: Wed, 10 Apr 2024 12:19:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc41657c316f5977709611ffae9798ea44ec41841054cecdfc9956512967de`  
		Last Modified: Wed, 10 Apr 2024 12:19:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aa5a2c270579376228531eac51095da5ab0374e62d177cd7b9d06916b5e113`  
		Last Modified: Wed, 10 Apr 2024 12:19:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c2722d07f6e4f03f8bc5f976b559422fa1f74641856112a4306083f23a3784`  
		Last Modified: Wed, 10 Apr 2024 12:19:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:e517d486ffea0f94bfb7761d1fe4c9e82d8308c8a99946936a884c2f5b75aa3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:f5f9f0c5f36470750613101dabfa8d1925b2e5a71db2036ebc66c88f94c36d94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.0 MB (583036172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497e0625a3adb64d86ca554c204bc75abfec2753b142eaf41fc4eae33596b733`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 10:04:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 12 Mar 2024 10:04:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 12 Mar 2024 10:04:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 10:04:23 GMT
ARG TARGETARCH
# Tue, 12 Mar 2024 10:05:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 12 Mar 2024 10:05:42 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:05:44 GMT
RUN npm install -g rtlcss
# Tue, 12 Mar 2024 10:05:44 GMT
ENV ODOO_VERSION=16.0
# Fri, 05 Apr 2024 21:04:27 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 21:04:27 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Fri, 05 Apr 2024 21:05:51 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 21:05:54 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 21:05:55 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 21:05:55 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 21:05:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 21:05:55 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 21:05:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 21:05:55 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 21:05:56 GMT
USER odoo
# Fri, 05 Apr 2024 21:05:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 21:05:56 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b6792aa9ce6832f860c6e1be9f969760839af537e4898318aa4f6bfb1c028b`  
		Last Modified: Tue, 12 Mar 2024 10:10:15 GMT  
		Size: 219.6 MB (219603015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc2315d87d3b1baf540e35d3ecccceacc3315ff5069bf3f9bfa9cfb289aeba9`  
		Last Modified: Tue, 12 Mar 2024 10:09:51 GMT  
		Size: 2.6 MB (2630018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075dda5b3fd48c7f6681e64745ee86cffaf18fee97aeba54f00d6ee06b5ba526`  
		Last Modified: Tue, 12 Mar 2024 10:09:50 GMT  
		Size: 462.5 KB (462467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0253237b85f992f84d06543a3fdaa33bd785073cce602da953a664026523fc`  
		Last Modified: Fri, 05 Apr 2024 21:09:05 GMT  
		Size: 328.9 MB (328915720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1944354a03ff87800dd9ed77da090cb327eb836afa309de7e8e229e0c6fa056f`  
		Last Modified: Fri, 05 Apr 2024 21:08:27 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141f9bb882f810119549b785e8ff22ec8ae97094159af137de1c989a91e1cd72`  
		Last Modified: Fri, 05 Apr 2024 21:08:27 GMT  
		Size: 552.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5e0b711f8ec83af3664f815865b72fd48fc592de6e89d3aa614773420d2529`  
		Last Modified: Fri, 05 Apr 2024 21:08:27 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d24020db9c292d13a2b6303e8364567c51431a208e5cf796aa0067698ed999`  
		Last Modified: Fri, 05 Apr 2024 21:08:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d25324e54f423555d398be28c22753c7f145dd72872033f85ec2b2c49b6fb70b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.7 MB (578656343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8edb1eebdb62b7447cbab778e25400df04ffb2bc3b9acb366d95dae2f3a879d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:50:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 06:50:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 06:50:11 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:50:11 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 06:51:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 06:51:25 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:51:26 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 06:51:26 GMT
ENV ODOO_VERSION=16.0
# Wed, 10 Apr 2024 06:51:26 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 06:51:26 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Wed, 10 Apr 2024 06:52:49 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 06:52:56 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 06:52:56 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 06:52:57 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 06:52:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 06:52:57 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 06:52:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 06:52:57 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 06:52:57 GMT
USER odoo
# Wed, 10 Apr 2024 06:52:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 06:52:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fc553ed1e447dba5d7cd1531a7067a247647cf58771061d9030c71c8b6d14d`  
		Last Modified: Wed, 10 Apr 2024 06:53:31 GMT  
		Size: 216.9 MB (216903831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505728a268c4b89109c2cb3fd49cd9b1dcb63f30c015647bfc1823b0d6774451`  
		Last Modified: Wed, 10 Apr 2024 06:53:14 GMT  
		Size: 2.6 MB (2635212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc1bbf349d40bf14f17d8931d7c97e93408ecb08a25175182d63b2592b4c6eac`  
		Last Modified: Wed, 10 Apr 2024 06:53:14 GMT  
		Size: 458.4 KB (458432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34a8e6a4767bc55af7ea7f4c72631e551d41cffa762efc5b73253398390b1d8`  
		Last Modified: Wed, 10 Apr 2024 06:53:42 GMT  
		Size: 328.6 MB (328580095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10420d0695cf8e799078b908497f64f76b477dba223add41e473ff0f111d500`  
		Last Modified: Wed, 10 Apr 2024 06:53:12 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac577dfe3513d6f531784319195b12c9d051aeeb1b1f4a38ae5b3d1166e8e98f`  
		Last Modified: Wed, 10 Apr 2024 06:53:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d695a8a535ed74173ccf570325545b1e22d4819c7f7cf75da76d252b805d00`  
		Last Modified: Wed, 10 Apr 2024 06:53:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a80f87e184f87ed1df1e8ac737ca7988f37e7389d3953e463fcfac6c7eab663`  
		Last Modified: Wed, 10 Apr 2024 06:53:11 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b000be7d56bb89a61e279293108dc3d25ebc3f1b1ae333649bcdfe39348771e3
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.6 MB (597599721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b544ebb4a0072205ed70d0d5459c855d81e85f26e5edf838fb338d1e0687112`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Apr 2024 01:27:00 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
# Wed, 10 Apr 2024 01:27:02 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 12:11:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 10 Apr 2024 12:11:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 10 Apr 2024 12:11:35 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 12:11:36 GMT
ARG TARGETARCH
# Wed, 10 Apr 2024 12:15:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 10 Apr 2024 12:16:11 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 12:16:14 GMT
RUN npm install -g rtlcss
# Wed, 10 Apr 2024 12:16:15 GMT
ENV ODOO_VERSION=16.0
# Wed, 10 Apr 2024 12:16:16 GMT
ARG ODOO_RELEASE=20240405
# Wed, 10 Apr 2024 12:16:17 GMT
ARG ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
# Wed, 10 Apr 2024 12:18:59 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Apr 2024 12:19:13 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 10 Apr 2024 12:19:14 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Apr 2024 12:19:15 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=52b55e39027e72c5383746c893503df7db467524
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Apr 2024 12:19:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Apr 2024 12:19:17 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Apr 2024 12:19:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Apr 2024 12:19:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Apr 2024 12:19:18 GMT
USER odoo
# Wed, 10 Apr 2024 12:19:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 12:19:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e559728a938c6bae80d026fa29f2c38efa24baa26b769f31f8c84966d4e1df`  
		Last Modified: Wed, 10 Apr 2024 12:20:10 GMT  
		Size: 228.6 MB (228600553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b203ec44cc6f31bfbafaf9862e879fbf8d13940d76cf12c60f413c3d4f7d2413`  
		Last Modified: Wed, 10 Apr 2024 12:19:39 GMT  
		Size: 2.9 MB (2876015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbe4e2bda71d3574d3ec461cc470d98dc69f9167871208766805ae0ec7e810f`  
		Last Modified: Wed, 10 Apr 2024 12:19:39 GMT  
		Size: 458.4 KB (458444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44bb59b6134dc895bace6ac001f367ef7df7681d8bb0e8675308b146b5f5fe0`  
		Last Modified: Wed, 10 Apr 2024 12:20:24 GMT  
		Size: 330.4 MB (330358150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9110cd77d7285e0fad9ff5e2b37e63a937f68ecd61c4aa9e602d19637a4e399`  
		Last Modified: Wed, 10 Apr 2024 12:19:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdc41657c316f5977709611ffae9798ea44ec41841054cecdfc9956512967de`  
		Last Modified: Wed, 10 Apr 2024 12:19:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43aa5a2c270579376228531eac51095da5ab0374e62d177cd7b9d06916b5e113`  
		Last Modified: Wed, 10 Apr 2024 12:19:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c2722d07f6e4f03f8bc5f976b559422fa1f74641856112a4306083f23a3784`  
		Last Modified: Wed, 10 Apr 2024 12:19:36 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17`

```console
$ docker pull odoo@sha256:d13febe57e6e3761497c27be3d208856d91159578bc10a8547cc350848e20c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:88c13ebdf5d4d1a22980fd13d3e5a29fdbaad9f0c2f96cfecb377a68c6859914
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.7 MB (601736486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a664ffa2315571bfce9f651d3ab2160cb9fff44c797c15cbe4b1594f53542b3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:08:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 03:08:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 03:08:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 03:08:00 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:10:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:10:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:10:22 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:10:23 GMT
ENV ODOO_VERSION=17.0
# Fri, 05 Apr 2024 21:02:03 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 21:02:03 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 21:04:04 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 21:04:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 21:04:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 21:04:09 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 21:04:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 21:04:09 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 21:04:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 21:04:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 21:04:09 GMT
USER odoo
# Fri, 05 Apr 2024 21:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 21:04:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e6c177fc20fa6387e63fd095d01292bafefb3d6e2ff9cb3e6e8b245a08381`  
		Last Modified: Wed, 06 Mar 2024 03:13:23 GMT  
		Size: 233.7 MB (233723335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3cefe2377c5eb4d88fbf2940f0a9dc339567dfe0c5c28fbc4d821dfa2ecb88`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 2.5 MB (2529426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f541a6d153b3dc5b1c957cef96a47ae608073cb3e26838fa2b35b8ce1455d`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 463.5 KB (463535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d03be2acc9355b0f6d9e76cc72d9f69f5ced32e7e2f086bfb9a12a4513d6cf4`  
		Last Modified: Fri, 05 Apr 2024 21:08:17 GMT  
		Size: 334.6 MB (334566422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd64e1300180741927f64f634d3b915c421207c43f61407ad0f6f73af1ec78d0`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cefadd0ddd390bb291024573b6ee8b2f808df571becf6a3d9f38b548f343c8`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b6346e17bf39dc387d1465d85fbc2dbc9014c612a0ee0729a0cb1ecdf208f8`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b8fd5127569c85d394e779e66669757a5493748b54ff27bc4810f0e85959b6`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3436f1f52ed0d937f9f9fd642fd19faf245958421dd33df225e80899e0fd3078
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.7 MB (596700020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63329b547b9d753138a0812b754b7818a9ae406e7f818bd52042da63e6697c6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:54:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 04:54:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 04:54:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 04:54:11 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 04:56:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 04:56:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:56:24 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 04:56:24 GMT
ENV ODOO_VERSION=17.0
# Fri, 05 Apr 2024 19:42:28 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 19:42:28 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 19:44:48 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 19:44:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 19:44:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 19:44:50 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 19:44:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 19:44:50 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 19:44:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 19:44:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 19:44:50 GMT
USER odoo
# Fri, 05 Apr 2024 19:44:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:44:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d9a54b231a5bc1f0a4e20302873f08d395effbeb7c781ed9a3c37af48db7c`  
		Last Modified: Wed, 06 Mar 2024 04:58:49 GMT  
		Size: 231.1 MB (231124838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128cac8b0310aa37c8527357da2df9e5a839ae8ad5078e27613f0d48022f8884`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 2.5 MB (2522173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e922dc5e5f1800b74b668a923fa6fc5ff7f1729d5fd4cec6aa1f172c787096e`  
		Last Modified: Wed, 06 Mar 2024 04:58:29 GMT  
		Size: 463.5 KB (463546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a8dcbe3d3be7a497a7500f37739e8aeb86ea2c42ff1bae253313b0c6004e2a`  
		Last Modified: Fri, 05 Apr 2024 19:47:21 GMT  
		Size: 334.2 MB (334186364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5495fd7423c2f5479b06dcab10def2ad75d471539b0d5e233c46f6e4ea6c6377`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ff6cb284fc6a1f38c5633be835922e13409bf310526c76f7c80a9ba5e9f0f4`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f9b73f88f99e62897eb57e325da70b4ca3d1c6d743c4fb3df902bde36d821b`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac13bb0a340f0f26a2a350b300498403219eef0709d44dc502726f5dd24491ac`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:a6d65d05878e547e0b0ddb8be3b102112fdd9d08f061f8021538f8db8060b9fd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.5 MB (618503012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d337b5fbf0262bba7d88a6d512c3d000da22d70d2cb31e7444ccd0255504b13c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:56:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 02:56:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 02:56:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 02:56:53 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:00:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:01:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:01:25 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:01:26 GMT
ENV ODOO_VERSION=17.0
# Fri, 05 Apr 2024 19:25:12 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 19:25:12 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 19:28:00 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 19:28:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 19:28:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 19:28:13 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 19:28:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 19:28:14 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 19:28:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 19:28:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 19:28:16 GMT
USER odoo
# Fri, 05 Apr 2024 19:28:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:28:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61460e6b4239c04ae02c8b5157a7b6f189f09c73682147f3af518f0dfaa9ef2`  
		Last Modified: Wed, 06 Mar 2024 03:05:32 GMT  
		Size: 243.3 MB (243298759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ae19a2941303126a97448f3501dcc7c1751322804bf811317b9d3391718773`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 2.8 MB (2805258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12901bfadfb439f3d17c6ce880d8353bd0636598d317d2f3e4625f1ce68d290`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 463.6 KB (463555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a1a5d3ad9ee702093094672b17fb5230874af0fb63555cd4f4799cd648c1ee`  
		Last Modified: Fri, 05 Apr 2024 19:31:41 GMT  
		Size: 336.3 MB (336310237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b762bbea18b46227a8d765144ab51fed19ce2fe29c8f26f3e51d8b0dd0429419`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7f4bcfa89f66dc107e007f5c68618c44b747d3b23b08dd42e7ca34f79839a8`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ca0b4f48ffeb04d27fe364dd6fbf50385d133575f6070e03dc631fdea549ab`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379759df926f53ef1a7c24ac561da96972009ee1654efffbb14dfc70d4b78ca`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:17.0`

```console
$ docker pull odoo@sha256:d13febe57e6e3761497c27be3d208856d91159578bc10a8547cc350848e20c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:88c13ebdf5d4d1a22980fd13d3e5a29fdbaad9f0c2f96cfecb377a68c6859914
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.7 MB (601736486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a664ffa2315571bfce9f651d3ab2160cb9fff44c797c15cbe4b1594f53542b3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:08:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 03:08:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 03:08:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 03:08:00 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:10:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:10:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:10:22 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:10:23 GMT
ENV ODOO_VERSION=17.0
# Fri, 05 Apr 2024 21:02:03 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 21:02:03 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 21:04:04 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 21:04:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 21:04:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 21:04:09 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 21:04:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 21:04:09 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 21:04:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 21:04:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 21:04:09 GMT
USER odoo
# Fri, 05 Apr 2024 21:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 21:04:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e6c177fc20fa6387e63fd095d01292bafefb3d6e2ff9cb3e6e8b245a08381`  
		Last Modified: Wed, 06 Mar 2024 03:13:23 GMT  
		Size: 233.7 MB (233723335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3cefe2377c5eb4d88fbf2940f0a9dc339567dfe0c5c28fbc4d821dfa2ecb88`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 2.5 MB (2529426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f541a6d153b3dc5b1c957cef96a47ae608073cb3e26838fa2b35b8ce1455d`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 463.5 KB (463535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d03be2acc9355b0f6d9e76cc72d9f69f5ced32e7e2f086bfb9a12a4513d6cf4`  
		Last Modified: Fri, 05 Apr 2024 21:08:17 GMT  
		Size: 334.6 MB (334566422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd64e1300180741927f64f634d3b915c421207c43f61407ad0f6f73af1ec78d0`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cefadd0ddd390bb291024573b6ee8b2f808df571becf6a3d9f38b548f343c8`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b6346e17bf39dc387d1465d85fbc2dbc9014c612a0ee0729a0cb1ecdf208f8`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b8fd5127569c85d394e779e66669757a5493748b54ff27bc4810f0e85959b6`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3436f1f52ed0d937f9f9fd642fd19faf245958421dd33df225e80899e0fd3078
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.7 MB (596700020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63329b547b9d753138a0812b754b7818a9ae406e7f818bd52042da63e6697c6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:54:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 04:54:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 04:54:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 04:54:11 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 04:56:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 04:56:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:56:24 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 04:56:24 GMT
ENV ODOO_VERSION=17.0
# Fri, 05 Apr 2024 19:42:28 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 19:42:28 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 19:44:48 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 19:44:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 19:44:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 19:44:50 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 19:44:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 19:44:50 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 19:44:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 19:44:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 19:44:50 GMT
USER odoo
# Fri, 05 Apr 2024 19:44:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:44:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d9a54b231a5bc1f0a4e20302873f08d395effbeb7c781ed9a3c37af48db7c`  
		Last Modified: Wed, 06 Mar 2024 04:58:49 GMT  
		Size: 231.1 MB (231124838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128cac8b0310aa37c8527357da2df9e5a839ae8ad5078e27613f0d48022f8884`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 2.5 MB (2522173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e922dc5e5f1800b74b668a923fa6fc5ff7f1729d5fd4cec6aa1f172c787096e`  
		Last Modified: Wed, 06 Mar 2024 04:58:29 GMT  
		Size: 463.5 KB (463546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a8dcbe3d3be7a497a7500f37739e8aeb86ea2c42ff1bae253313b0c6004e2a`  
		Last Modified: Fri, 05 Apr 2024 19:47:21 GMT  
		Size: 334.2 MB (334186364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5495fd7423c2f5479b06dcab10def2ad75d471539b0d5e233c46f6e4ea6c6377`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ff6cb284fc6a1f38c5633be835922e13409bf310526c76f7c80a9ba5e9f0f4`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f9b73f88f99e62897eb57e325da70b4ca3d1c6d743c4fb3df902bde36d821b`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac13bb0a340f0f26a2a350b300498403219eef0709d44dc502726f5dd24491ac`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:a6d65d05878e547e0b0ddb8be3b102112fdd9d08f061f8021538f8db8060b9fd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.5 MB (618503012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d337b5fbf0262bba7d88a6d512c3d000da22d70d2cb31e7444ccd0255504b13c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:56:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 02:56:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 02:56:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 02:56:53 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:00:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:01:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:01:25 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:01:26 GMT
ENV ODOO_VERSION=17.0
# Fri, 05 Apr 2024 19:25:12 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 19:25:12 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 19:28:00 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 19:28:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 19:28:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 19:28:13 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 19:28:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 19:28:14 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 19:28:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 19:28:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 19:28:16 GMT
USER odoo
# Fri, 05 Apr 2024 19:28:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:28:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61460e6b4239c04ae02c8b5157a7b6f189f09c73682147f3af518f0dfaa9ef2`  
		Last Modified: Wed, 06 Mar 2024 03:05:32 GMT  
		Size: 243.3 MB (243298759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ae19a2941303126a97448f3501dcc7c1751322804bf811317b9d3391718773`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 2.8 MB (2805258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12901bfadfb439f3d17c6ce880d8353bd0636598d317d2f3e4625f1ce68d290`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 463.6 KB (463555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a1a5d3ad9ee702093094672b17fb5230874af0fb63555cd4f4799cd648c1ee`  
		Last Modified: Fri, 05 Apr 2024 19:31:41 GMT  
		Size: 336.3 MB (336310237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b762bbea18b46227a8d765144ab51fed19ce2fe29c8f26f3e51d8b0dd0429419`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7f4bcfa89f66dc107e007f5c68618c44b747d3b23b08dd42e7ca34f79839a8`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ca0b4f48ffeb04d27fe364dd6fbf50385d133575f6070e03dc631fdea549ab`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379759df926f53ef1a7c24ac561da96972009ee1654efffbb14dfc70d4b78ca`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:d13febe57e6e3761497c27be3d208856d91159578bc10a8547cc350848e20c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:88c13ebdf5d4d1a22980fd13d3e5a29fdbaad9f0c2f96cfecb377a68c6859914
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.7 MB (601736486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a664ffa2315571bfce9f651d3ab2160cb9fff44c797c15cbe4b1594f53542b3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 03:08:00 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 03:08:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 03:08:00 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 03:08:00 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:10:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:10:21 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:10:22 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:10:23 GMT
ENV ODOO_VERSION=17.0
# Fri, 05 Apr 2024 21:02:03 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 21:02:03 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 21:04:04 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 21:04:08 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 21:04:08 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 21:04:09 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 21:04:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 21:04:09 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 21:04:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 21:04:09 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 21:04:09 GMT
USER odoo
# Fri, 05 Apr 2024 21:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 21:04:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88e6c177fc20fa6387e63fd095d01292bafefb3d6e2ff9cb3e6e8b245a08381`  
		Last Modified: Wed, 06 Mar 2024 03:13:23 GMT  
		Size: 233.7 MB (233723335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3cefe2377c5eb4d88fbf2940f0a9dc339567dfe0c5c28fbc4d821dfa2ecb88`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 2.5 MB (2529426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6f541a6d153b3dc5b1c957cef96a47ae608073cb3e26838fa2b35b8ce1455d`  
		Last Modified: Wed, 06 Mar 2024 03:12:53 GMT  
		Size: 463.5 KB (463535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d03be2acc9355b0f6d9e76cc72d9f69f5ced32e7e2f086bfb9a12a4513d6cf4`  
		Last Modified: Fri, 05 Apr 2024 21:08:17 GMT  
		Size: 334.6 MB (334566422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd64e1300180741927f64f634d3b915c421207c43f61407ad0f6f73af1ec78d0`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cefadd0ddd390bb291024573b6ee8b2f808df571becf6a3d9f38b548f343c8`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b6346e17bf39dc387d1465d85fbc2dbc9014c612a0ee0729a0cb1ecdf208f8`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b8fd5127569c85d394e779e66669757a5493748b54ff27bc4810f0e85959b6`  
		Last Modified: Fri, 05 Apr 2024 21:07:38 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3436f1f52ed0d937f9f9fd642fd19faf245958421dd33df225e80899e0fd3078
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.7 MB (596700020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63329b547b9d753138a0812b754b7818a9ae406e7f818bd52042da63e6697c6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:54:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 04:54:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 04:54:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 04:54:11 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 04:56:10 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 04:56:23 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:56:24 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 04:56:24 GMT
ENV ODOO_VERSION=17.0
# Fri, 05 Apr 2024 19:42:28 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 19:42:28 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 19:44:48 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 19:44:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 19:44:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 19:44:50 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 19:44:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 19:44:50 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 19:44:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 19:44:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 19:44:50 GMT
USER odoo
# Fri, 05 Apr 2024 19:44:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:44:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7d9a54b231a5bc1f0a4e20302873f08d395effbeb7c781ed9a3c37af48db7c`  
		Last Modified: Wed, 06 Mar 2024 04:58:49 GMT  
		Size: 231.1 MB (231124838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128cac8b0310aa37c8527357da2df9e5a839ae8ad5078e27613f0d48022f8884`  
		Last Modified: Wed, 06 Mar 2024 04:58:30 GMT  
		Size: 2.5 MB (2522173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e922dc5e5f1800b74b668a923fa6fc5ff7f1729d5fd4cec6aa1f172c787096e`  
		Last Modified: Wed, 06 Mar 2024 04:58:29 GMT  
		Size: 463.5 KB (463546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a8dcbe3d3be7a497a7500f37739e8aeb86ea2c42ff1bae253313b0c6004e2a`  
		Last Modified: Fri, 05 Apr 2024 19:47:21 GMT  
		Size: 334.2 MB (334186364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5495fd7423c2f5479b06dcab10def2ad75d471539b0d5e233c46f6e4ea6c6377`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ff6cb284fc6a1f38c5633be835922e13409bf310526c76f7c80a9ba5e9f0f4`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f9b73f88f99e62897eb57e325da70b4ca3d1c6d743c4fb3df902bde36d821b`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac13bb0a340f0f26a2a350b300498403219eef0709d44dc502726f5dd24491ac`  
		Last Modified: Fri, 05 Apr 2024 19:46:51 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:a6d65d05878e547e0b0ddb8be3b102112fdd9d08f061f8021538f8db8060b9fd
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.5 MB (618503012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d337b5fbf0262bba7d88a6d512c3d000da22d70d2cb31e7444ccd0255504b13c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 27 Feb 2024 18:28:24 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:28:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:28:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:28:28 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 27 Feb 2024 18:28:28 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 02:56:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 06 Mar 2024 02:56:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 06 Mar 2024 02:56:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 02:56:53 GMT
ARG TARGETARCH
# Wed, 06 Mar 2024 03:00:59 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 06 Mar 2024 03:01:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 03:01:25 GMT
RUN npm install -g rtlcss
# Wed, 06 Mar 2024 03:01:26 GMT
ENV ODOO_VERSION=17.0
# Fri, 05 Apr 2024 19:25:12 GMT
ARG ODOO_RELEASE=20240405
# Fri, 05 Apr 2024 19:25:12 GMT
ARG ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
# Fri, 05 Apr 2024 19:28:00 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 05 Apr 2024 19:28:12 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 05 Apr 2024 19:28:12 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 05 Apr 2024 19:28:13 GMT
# ARGS: ODOO_RELEASE=20240405 ODOO_SHA=da9e09a429982d3b70ec0eef6c282b7a72eda47a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 05 Apr 2024 19:28:14 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 05 Apr 2024 19:28:14 GMT
EXPOSE 8069 8071 8072
# Fri, 05 Apr 2024 19:28:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 05 Apr 2024 19:28:15 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 05 Apr 2024 19:28:16 GMT
USER odoo
# Fri, 05 Apr 2024 19:28:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 05 Apr 2024 19:28:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61460e6b4239c04ae02c8b5157a7b6f189f09c73682147f3af518f0dfaa9ef2`  
		Last Modified: Wed, 06 Mar 2024 03:05:32 GMT  
		Size: 243.3 MB (243298759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ae19a2941303126a97448f3501dcc7c1751322804bf811317b9d3391718773`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 2.8 MB (2805258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12901bfadfb439f3d17c6ce880d8353bd0636598d317d2f3e4625f1ce68d290`  
		Last Modified: Wed, 06 Mar 2024 03:04:59 GMT  
		Size: 463.6 KB (463555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a1a5d3ad9ee702093094672b17fb5230874af0fb63555cd4f4799cd648c1ee`  
		Last Modified: Fri, 05 Apr 2024 19:31:41 GMT  
		Size: 336.3 MB (336310237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b762bbea18b46227a8d765144ab51fed19ce2fe29c8f26f3e51d8b0dd0429419`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7f4bcfa89f66dc107e007f5c68618c44b747d3b23b08dd42e7ca34f79839a8`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ca0b4f48ffeb04d27fe364dd6fbf50385d133575f6070e03dc631fdea549ab`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e379759df926f53ef1a7c24ac561da96972009ee1654efffbb14dfc70d4b78ca`  
		Last Modified: Fri, 05 Apr 2024 19:30:53 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
