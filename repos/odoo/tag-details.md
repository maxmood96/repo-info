<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:14`](#odoo14)
-	[`odoo:14.0`](#odoo140)
-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:latest`](#odoolatest)

## `odoo:14`

```console
$ docker pull odoo@sha256:58f224563a7c68827d3ce2719af15d9c16bb96f0fe2f0a752ed0dc864face28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:26b883efc76efb6798151bf61cad76cb1c4dcbf0205a8fcdf6fed0a5a5898d3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.0 MB (532031450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1114290b7d56bfd275a8c38c8b9852dbdfb8ca7d2b837d888dd01d34d736c423`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:50 GMT
ADD file:52316aa7d631242cd16337be337e57187ef07d3965e6284321fbdcd5b4f92b64 in / 
# Thu, 23 Mar 2023 01:30:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:32:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Mar 2023 15:32:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Mar 2023 15:32:47 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 15:34:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Mar 2023 15:34:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:34:31 GMT
RUN npm install -g rtlcss
# Thu, 23 Mar 2023 15:34:31 GMT
ENV ODOO_VERSION=14.0
# Thu, 23 Mar 2023 15:34:31 GMT
ARG ODOO_RELEASE=20230317
# Thu, 23 Mar 2023 15:34:31 GMT
ARG ODOO_SHA=4b677e345f13d6421d78f6a3f3dce4ccf6bd2a99
# Thu, 23 Mar 2023 15:35:45 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=4b677e345f13d6421d78f6a3f3dce4ccf6bd2a99
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Mar 2023 15:35:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Mar 2023 15:35:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Mar 2023 15:35:50 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=4b677e345f13d6421d78f6a3f3dce4ccf6bd2a99
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Mar 2023 15:35:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Mar 2023 15:35:50 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Mar 2023 15:35:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Mar 2023 15:35:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Mar 2023 15:35:50 GMT
USER odoo
# Thu, 23 Mar 2023 15:35:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 15:35:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3689b8de819b48387712c6d4d62d26a52a04c9e88afc68fb9d1dbe48bfa9e21d`  
		Last Modified: Thu, 23 Mar 2023 01:35:01 GMT  
		Size: 27.1 MB (27139869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f61528482665dae135f20097eafcf029dcc696e9337df02d212f93bf2a7da35`  
		Last Modified: Thu, 23 Mar 2023 15:37:57 GMT  
		Size: 213.2 MB (213202815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe18ac80b1ef39f3816a8be03536504a6538e49a75caa291a2bdf1c7c44cb37`  
		Last Modified: Thu, 23 Mar 2023 15:37:36 GMT  
		Size: 13.5 MB (13517778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10e2d42cd68f331b4cc4f81d78f9e461bdeb0cad69e0386459758171aef499`  
		Last Modified: Thu, 23 Mar 2023 15:37:34 GMT  
		Size: 458.3 KB (458270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4df0dd0aa17c703c11b94a8ff0e3e36888d7d799fb14595155225a11fcf364`  
		Last Modified: Thu, 23 Mar 2023 15:38:04 GMT  
		Size: 277.7 MB (277710260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20d35ceb064239208d9cd724414bd733d9e0c847c8f2fb198fa6e2ad90525cf`  
		Last Modified: Thu, 23 Mar 2023 15:37:31 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0f5d9e15ad94da4168a9cc6f2eb64926377a6fa79463d11659c36e15a45a55`  
		Last Modified: Thu, 23 Mar 2023 15:37:31 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51189407846f8bb04e08864c7760a3033cd7c9de86975fedb8761600b3b43f2`  
		Last Modified: Thu, 23 Mar 2023 15:37:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70eac04c2448c367bad6f8d480bf5a86eea9134a705bdf736ecab1d2dd100bde`  
		Last Modified: Thu, 23 Mar 2023 15:37:31 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:58f224563a7c68827d3ce2719af15d9c16bb96f0fe2f0a752ed0dc864face28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:26b883efc76efb6798151bf61cad76cb1c4dcbf0205a8fcdf6fed0a5a5898d3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.0 MB (532031450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1114290b7d56bfd275a8c38c8b9852dbdfb8ca7d2b837d888dd01d34d736c423`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:50 GMT
ADD file:52316aa7d631242cd16337be337e57187ef07d3965e6284321fbdcd5b4f92b64 in / 
# Thu, 23 Mar 2023 01:30:51 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:32:47 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Mar 2023 15:32:47 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Mar 2023 15:32:47 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 15:34:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Mar 2023 15:34:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:34:31 GMT
RUN npm install -g rtlcss
# Thu, 23 Mar 2023 15:34:31 GMT
ENV ODOO_VERSION=14.0
# Thu, 23 Mar 2023 15:34:31 GMT
ARG ODOO_RELEASE=20230317
# Thu, 23 Mar 2023 15:34:31 GMT
ARG ODOO_SHA=4b677e345f13d6421d78f6a3f3dce4ccf6bd2a99
# Thu, 23 Mar 2023 15:35:45 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=4b677e345f13d6421d78f6a3f3dce4ccf6bd2a99
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Mar 2023 15:35:49 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Mar 2023 15:35:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Mar 2023 15:35:50 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=4b677e345f13d6421d78f6a3f3dce4ccf6bd2a99
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Mar 2023 15:35:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Mar 2023 15:35:50 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Mar 2023 15:35:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Mar 2023 15:35:50 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Mar 2023 15:35:50 GMT
USER odoo
# Thu, 23 Mar 2023 15:35:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 15:35:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3689b8de819b48387712c6d4d62d26a52a04c9e88afc68fb9d1dbe48bfa9e21d`  
		Last Modified: Thu, 23 Mar 2023 01:35:01 GMT  
		Size: 27.1 MB (27139869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f61528482665dae135f20097eafcf029dcc696e9337df02d212f93bf2a7da35`  
		Last Modified: Thu, 23 Mar 2023 15:37:57 GMT  
		Size: 213.2 MB (213202815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe18ac80b1ef39f3816a8be03536504a6538e49a75caa291a2bdf1c7c44cb37`  
		Last Modified: Thu, 23 Mar 2023 15:37:36 GMT  
		Size: 13.5 MB (13517778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f10e2d42cd68f331b4cc4f81d78f9e461bdeb0cad69e0386459758171aef499`  
		Last Modified: Thu, 23 Mar 2023 15:37:34 GMT  
		Size: 458.3 KB (458270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4df0dd0aa17c703c11b94a8ff0e3e36888d7d799fb14595155225a11fcf364`  
		Last Modified: Thu, 23 Mar 2023 15:38:04 GMT  
		Size: 277.7 MB (277710260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20d35ceb064239208d9cd724414bd733d9e0c847c8f2fb198fa6e2ad90525cf`  
		Last Modified: Thu, 23 Mar 2023 15:37:31 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0f5d9e15ad94da4168a9cc6f2eb64926377a6fa79463d11659c36e15a45a55`  
		Last Modified: Thu, 23 Mar 2023 15:37:31 GMT  
		Size: 553.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51189407846f8bb04e08864c7760a3033cd7c9de86975fedb8761600b3b43f2`  
		Last Modified: Thu, 23 Mar 2023 15:37:31 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70eac04c2448c367bad6f8d480bf5a86eea9134a705bdf736ecab1d2dd100bde`  
		Last Modified: Thu, 23 Mar 2023 15:37:31 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:23fa8f305b07927248653eaec383cea3b18afe68dce855bb073300923e5d8ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:e8a069687231900d8a241b2837245a64a8eeb53f5c4c3f3efcbb6ecc7db1ea3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.3 MB (560310573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087dbbd2486a6e2306326b7d42f31fdf7e95b0418adc0803b0f2258317096df4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:28:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Mar 2023 15:28:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Mar 2023 15:28:01 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 15:29:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Mar 2023 15:29:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:29:41 GMT
RUN npm install -g rtlcss
# Thu, 23 Mar 2023 15:31:24 GMT
ENV ODOO_VERSION=15.0
# Thu, 23 Mar 2023 15:31:24 GMT
ARG ODOO_RELEASE=20230317
# Thu, 23 Mar 2023 15:31:24 GMT
ARG ODOO_SHA=2ebd7a6c36e415ed18a19148d2a1d8958d140bef
# Thu, 23 Mar 2023 15:32:37 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=2ebd7a6c36e415ed18a19148d2a1d8958d140bef
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Mar 2023 15:32:41 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Mar 2023 15:32:41 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Mar 2023 15:32:41 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=2ebd7a6c36e415ed18a19148d2a1d8958d140bef
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Mar 2023 15:32:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Mar 2023 15:32:42 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Mar 2023 15:32:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Mar 2023 15:32:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Mar 2023 15:32:42 GMT
USER odoo
# Thu, 23 Mar 2023 15:32:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 15:32:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901cea134a7b232935a0e0e3f454f625f49b6bb8b6a0ceaa6e2eb5d9a2cb5541`  
		Last Modified: Thu, 23 Mar 2023 15:36:30 GMT  
		Size: 220.3 MB (220298376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3e9fdc875544ffb1102a5cb8469b7bc326306aff421fb5029bebb88f8c7f1a`  
		Last Modified: Thu, 23 Mar 2023 15:36:05 GMT  
		Size: 2.6 MB (2575178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc62a84f17f296f278e6ee0409b846d9714e16f6f25046de99c215879e92bc7`  
		Last Modified: Thu, 23 Mar 2023 15:36:05 GMT  
		Size: 453.8 KB (453789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabcdfcbbe9b04b0a4391a90770502062c72944f87f62c8cb9a0c89aca721942`  
		Last Modified: Thu, 23 Mar 2023 15:37:23 GMT  
		Size: 305.6 MB (305569367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c02cb096927968428f330ec2a6ac36d2363300ab57d6ffb5e9d47a564e7d5e7`  
		Last Modified: Thu, 23 Mar 2023 15:36:50 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca3f9e8ae0c96d8c4b4a6e1d5767ce8bd296b478090c418da3899443ab59e43`  
		Last Modified: Thu, 23 Mar 2023 15:36:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24530da2aa9d6da6c243c9aee068296b73a8bcbbae3d77f146a0d462bd0f0669`  
		Last Modified: Thu, 23 Mar 2023 15:36:50 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f94d825405922f0e609011162df316ab7a4a15e7998b813d39a1f98710bae9`  
		Last Modified: Thu, 23 Mar 2023 15:36:50 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:23fa8f305b07927248653eaec383cea3b18afe68dce855bb073300923e5d8ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:e8a069687231900d8a241b2837245a64a8eeb53f5c4c3f3efcbb6ecc7db1ea3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.3 MB (560310573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087dbbd2486a6e2306326b7d42f31fdf7e95b0418adc0803b0f2258317096df4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:28:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Mar 2023 15:28:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Mar 2023 15:28:01 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 15:29:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Mar 2023 15:29:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:29:41 GMT
RUN npm install -g rtlcss
# Thu, 23 Mar 2023 15:31:24 GMT
ENV ODOO_VERSION=15.0
# Thu, 23 Mar 2023 15:31:24 GMT
ARG ODOO_RELEASE=20230317
# Thu, 23 Mar 2023 15:31:24 GMT
ARG ODOO_SHA=2ebd7a6c36e415ed18a19148d2a1d8958d140bef
# Thu, 23 Mar 2023 15:32:37 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=2ebd7a6c36e415ed18a19148d2a1d8958d140bef
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Mar 2023 15:32:41 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Mar 2023 15:32:41 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Mar 2023 15:32:41 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=2ebd7a6c36e415ed18a19148d2a1d8958d140bef
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Mar 2023 15:32:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Mar 2023 15:32:42 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Mar 2023 15:32:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Mar 2023 15:32:42 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Mar 2023 15:32:42 GMT
USER odoo
# Thu, 23 Mar 2023 15:32:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 15:32:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901cea134a7b232935a0e0e3f454f625f49b6bb8b6a0ceaa6e2eb5d9a2cb5541`  
		Last Modified: Thu, 23 Mar 2023 15:36:30 GMT  
		Size: 220.3 MB (220298376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3e9fdc875544ffb1102a5cb8469b7bc326306aff421fb5029bebb88f8c7f1a`  
		Last Modified: Thu, 23 Mar 2023 15:36:05 GMT  
		Size: 2.6 MB (2575178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc62a84f17f296f278e6ee0409b846d9714e16f6f25046de99c215879e92bc7`  
		Last Modified: Thu, 23 Mar 2023 15:36:05 GMT  
		Size: 453.8 KB (453789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabcdfcbbe9b04b0a4391a90770502062c72944f87f62c8cb9a0c89aca721942`  
		Last Modified: Thu, 23 Mar 2023 15:37:23 GMT  
		Size: 305.6 MB (305569367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c02cb096927968428f330ec2a6ac36d2363300ab57d6ffb5e9d47a564e7d5e7`  
		Last Modified: Thu, 23 Mar 2023 15:36:50 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca3f9e8ae0c96d8c4b4a6e1d5767ce8bd296b478090c418da3899443ab59e43`  
		Last Modified: Thu, 23 Mar 2023 15:36:50 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24530da2aa9d6da6c243c9aee068296b73a8bcbbae3d77f146a0d462bd0f0669`  
		Last Modified: Thu, 23 Mar 2023 15:36:50 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f94d825405922f0e609011162df316ab7a4a15e7998b813d39a1f98710bae9`  
		Last Modified: Thu, 23 Mar 2023 15:36:50 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:26c9c47701b9837dbbd6968f5fb285d8e5ef0c5056ed57f7b4d27805253983dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:006e79693b044bf0e7ed912da4dd082bcc1724d14f5ab4a14a679b62194b38f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.1 MB (569077969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39383433e0c0a0dffba82fba61154f2de01946245ee29f4474dbcda598d0d766`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:28:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Mar 2023 15:28:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Mar 2023 15:28:01 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 15:29:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Mar 2023 15:29:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:29:41 GMT
RUN npm install -g rtlcss
# Thu, 23 Mar 2023 15:29:41 GMT
ENV ODOO_VERSION=16.0
# Thu, 23 Mar 2023 15:29:41 GMT
ARG ODOO_RELEASE=20230317
# Thu, 23 Mar 2023 15:29:41 GMT
ARG ODOO_SHA=13d351efd1263e2db7788a7c4995935752eab898
# Thu, 23 Mar 2023 15:31:02 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=13d351efd1263e2db7788a7c4995935752eab898
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Mar 2023 15:31:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Mar 2023 15:31:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Mar 2023 15:31:07 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=13d351efd1263e2db7788a7c4995935752eab898
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Mar 2023 15:31:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Mar 2023 15:31:08 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Mar 2023 15:31:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Mar 2023 15:31:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Mar 2023 15:31:08 GMT
USER odoo
# Thu, 23 Mar 2023 15:31:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 15:31:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901cea134a7b232935a0e0e3f454f625f49b6bb8b6a0ceaa6e2eb5d9a2cb5541`  
		Last Modified: Thu, 23 Mar 2023 15:36:30 GMT  
		Size: 220.3 MB (220298376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3e9fdc875544ffb1102a5cb8469b7bc326306aff421fb5029bebb88f8c7f1a`  
		Last Modified: Thu, 23 Mar 2023 15:36:05 GMT  
		Size: 2.6 MB (2575178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc62a84f17f296f278e6ee0409b846d9714e16f6f25046de99c215879e92bc7`  
		Last Modified: Thu, 23 Mar 2023 15:36:05 GMT  
		Size: 453.8 KB (453789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2a4938a5639bad077ea07a159f4c7c6d5540c44dd28031b515118024815eab`  
		Last Modified: Thu, 23 Mar 2023 15:36:39 GMT  
		Size: 314.3 MB (314336762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3484e245d3be7df0aa8ce2c37bc7757852cadad41289a8c2564160820e9669ae`  
		Last Modified: Thu, 23 Mar 2023 15:36:03 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c917edb1e08c277d2dd8f53a690af86aac11fe69eca3fb72d1cd163deafbe926`  
		Last Modified: Thu, 23 Mar 2023 15:36:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5a4adb635b9af1e61681d4cae1d09828809489a8c6d26f0157d3002e88993e`  
		Last Modified: Thu, 23 Mar 2023 15:36:03 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8720c3378ef92ffdda1f139900bdfd62be4a9dd4ddd5b8383b933b523cfa803`  
		Last Modified: Thu, 23 Mar 2023 15:36:03 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:26c9c47701b9837dbbd6968f5fb285d8e5ef0c5056ed57f7b4d27805253983dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:006e79693b044bf0e7ed912da4dd082bcc1724d14f5ab4a14a679b62194b38f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.1 MB (569077969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39383433e0c0a0dffba82fba61154f2de01946245ee29f4474dbcda598d0d766`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:28:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Mar 2023 15:28:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Mar 2023 15:28:01 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 15:29:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Mar 2023 15:29:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:29:41 GMT
RUN npm install -g rtlcss
# Thu, 23 Mar 2023 15:29:41 GMT
ENV ODOO_VERSION=16.0
# Thu, 23 Mar 2023 15:29:41 GMT
ARG ODOO_RELEASE=20230317
# Thu, 23 Mar 2023 15:29:41 GMT
ARG ODOO_SHA=13d351efd1263e2db7788a7c4995935752eab898
# Thu, 23 Mar 2023 15:31:02 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=13d351efd1263e2db7788a7c4995935752eab898
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Mar 2023 15:31:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Mar 2023 15:31:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Mar 2023 15:31:07 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=13d351efd1263e2db7788a7c4995935752eab898
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Mar 2023 15:31:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Mar 2023 15:31:08 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Mar 2023 15:31:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Mar 2023 15:31:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Mar 2023 15:31:08 GMT
USER odoo
# Thu, 23 Mar 2023 15:31:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 15:31:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901cea134a7b232935a0e0e3f454f625f49b6bb8b6a0ceaa6e2eb5d9a2cb5541`  
		Last Modified: Thu, 23 Mar 2023 15:36:30 GMT  
		Size: 220.3 MB (220298376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3e9fdc875544ffb1102a5cb8469b7bc326306aff421fb5029bebb88f8c7f1a`  
		Last Modified: Thu, 23 Mar 2023 15:36:05 GMT  
		Size: 2.6 MB (2575178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc62a84f17f296f278e6ee0409b846d9714e16f6f25046de99c215879e92bc7`  
		Last Modified: Thu, 23 Mar 2023 15:36:05 GMT  
		Size: 453.8 KB (453789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2a4938a5639bad077ea07a159f4c7c6d5540c44dd28031b515118024815eab`  
		Last Modified: Thu, 23 Mar 2023 15:36:39 GMT  
		Size: 314.3 MB (314336762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3484e245d3be7df0aa8ce2c37bc7757852cadad41289a8c2564160820e9669ae`  
		Last Modified: Thu, 23 Mar 2023 15:36:03 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c917edb1e08c277d2dd8f53a690af86aac11fe69eca3fb72d1cd163deafbe926`  
		Last Modified: Thu, 23 Mar 2023 15:36:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5a4adb635b9af1e61681d4cae1d09828809489a8c6d26f0157d3002e88993e`  
		Last Modified: Thu, 23 Mar 2023 15:36:03 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8720c3378ef92ffdda1f139900bdfd62be4a9dd4ddd5b8383b933b523cfa803`  
		Last Modified: Thu, 23 Mar 2023 15:36:03 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:26c9c47701b9837dbbd6968f5fb285d8e5ef0c5056ed57f7b4d27805253983dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:006e79693b044bf0e7ed912da4dd082bcc1724d14f5ab4a14a679b62194b38f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.1 MB (569077969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39383433e0c0a0dffba82fba61154f2de01946245ee29f4474dbcda598d0d766`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 15:28:01 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Mar 2023 15:28:01 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Mar 2023 15:28:01 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 15:29:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Mar 2023 15:29:39 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:29:41 GMT
RUN npm install -g rtlcss
# Thu, 23 Mar 2023 15:29:41 GMT
ENV ODOO_VERSION=16.0
# Thu, 23 Mar 2023 15:29:41 GMT
ARG ODOO_RELEASE=20230317
# Thu, 23 Mar 2023 15:29:41 GMT
ARG ODOO_SHA=13d351efd1263e2db7788a7c4995935752eab898
# Thu, 23 Mar 2023 15:31:02 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=13d351efd1263e2db7788a7c4995935752eab898
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 23 Mar 2023 15:31:07 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 23 Mar 2023 15:31:07 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 23 Mar 2023 15:31:07 GMT
# ARGS: ODOO_RELEASE=20230317 ODOO_SHA=13d351efd1263e2db7788a7c4995935752eab898
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 23 Mar 2023 15:31:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 23 Mar 2023 15:31:08 GMT
EXPOSE 8069 8071 8072
# Thu, 23 Mar 2023 15:31:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 23 Mar 2023 15:31:08 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 23 Mar 2023 15:31:08 GMT
USER odoo
# Thu, 23 Mar 2023 15:31:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 15:31:08 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901cea134a7b232935a0e0e3f454f625f49b6bb8b6a0ceaa6e2eb5d9a2cb5541`  
		Last Modified: Thu, 23 Mar 2023 15:36:30 GMT  
		Size: 220.3 MB (220298376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3e9fdc875544ffb1102a5cb8469b7bc326306aff421fb5029bebb88f8c7f1a`  
		Last Modified: Thu, 23 Mar 2023 15:36:05 GMT  
		Size: 2.6 MB (2575178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc62a84f17f296f278e6ee0409b846d9714e16f6f25046de99c215879e92bc7`  
		Last Modified: Thu, 23 Mar 2023 15:36:05 GMT  
		Size: 453.8 KB (453789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2a4938a5639bad077ea07a159f4c7c6d5540c44dd28031b515118024815eab`  
		Last Modified: Thu, 23 Mar 2023 15:36:39 GMT  
		Size: 314.3 MB (314336762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3484e245d3be7df0aa8ce2c37bc7757852cadad41289a8c2564160820e9669ae`  
		Last Modified: Thu, 23 Mar 2023 15:36:03 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c917edb1e08c277d2dd8f53a690af86aac11fe69eca3fb72d1cd163deafbe926`  
		Last Modified: Thu, 23 Mar 2023 15:36:03 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5a4adb635b9af1e61681d4cae1d09828809489a8c6d26f0157d3002e88993e`  
		Last Modified: Thu, 23 Mar 2023 15:36:03 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8720c3378ef92ffdda1f139900bdfd62be4a9dd4ddd5b8383b933b523cfa803`  
		Last Modified: Thu, 23 Mar 2023 15:36:03 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
