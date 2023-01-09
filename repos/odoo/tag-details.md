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
$ docker pull odoo@sha256:9dc8b466a55b0b18926f1e65e5501a13030fc2a00cbd3277bebe6d70def0e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:504e8f34fb85a71b83e589fb71cf64ccd9d48ef1b1d20aaafb82a9b42065e905
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531525368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0f5bb5023bd8013289502da9ca9971eee9a6baa61a98ae78c444d4149914ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:04:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 12:04:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 12:04:03 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:05:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:05:40 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:05:43 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:05:43 GMT
ENV ODOO_VERSION=14.0
# Mon, 09 Jan 2023 17:28:26 GMT
ARG ODOO_RELEASE=20230109
# Mon, 09 Jan 2023 17:28:26 GMT
ARG ODOO_SHA=ef9eef9a5e5bbeb455ac7d1c05cc675e74876609
# Mon, 09 Jan 2023 17:29:57 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=ef9eef9a5e5bbeb455ac7d1c05cc675e74876609
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 09 Jan 2023 17:30:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 09 Jan 2023 17:30:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 09 Jan 2023 17:30:02 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=ef9eef9a5e5bbeb455ac7d1c05cc675e74876609
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 09 Jan 2023 17:30:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Jan 2023 17:30:02 GMT
EXPOSE 8069 8071 8072
# Mon, 09 Jan 2023 17:30:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Jan 2023 17:30:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 09 Jan 2023 17:30:03 GMT
USER odoo
# Mon, 09 Jan 2023 17:30:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Jan 2023 17:30:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fd809e7e6338e9ff619aa861a2c83ea5794e2e9f1e27208941b0cb0830d586`  
		Last Modified: Wed, 21 Dec 2022 12:09:24 GMT  
		Size: 213.2 MB (213188652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7447a10d2ac09f77c91f4405dd22b28022ae50b65e4a89bd2b93bc773c1a76f`  
		Last Modified: Wed, 21 Dec 2022 12:09:01 GMT  
		Size: 13.5 MB (13515235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2a982470c9023112777135e16db2722d58d0e80637be6f6512ed77e73a0e45`  
		Last Modified: Wed, 21 Dec 2022 12:08:58 GMT  
		Size: 457.1 KB (457118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a544d327de006924dd60a859a82d9c513ab5f002251804152861d11559cc469`  
		Last Modified: Mon, 09 Jan 2023 17:32:39 GMT  
		Size: 277.2 MB (277221565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3579f37f60d1655e52cf6b98f3cd07ce8b0a9e4368954149a4800f8e73a1cb36`  
		Last Modified: Mon, 09 Jan 2023 17:32:05 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fa3a5e996155834744df896dc803a863f292b43d949fd7ea7eceb3224d723b`  
		Last Modified: Mon, 09 Jan 2023 17:32:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d414295bd9260495dccd4a9d612d0e1edf468888131eac32ba1a30579f6ea`  
		Last Modified: Mon, 09 Jan 2023 17:32:06 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29f8132f384d6215cf2f5a3a36e52796e6acd72aa8447fe8e542374c91fc465`  
		Last Modified: Mon, 09 Jan 2023 17:32:05 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:9dc8b466a55b0b18926f1e65e5501a13030fc2a00cbd3277bebe6d70def0e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:504e8f34fb85a71b83e589fb71cf64ccd9d48ef1b1d20aaafb82a9b42065e905
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531525368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0f5bb5023bd8013289502da9ca9971eee9a6baa61a98ae78c444d4149914ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:04:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 12:04:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 12:04:03 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:05:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:05:40 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:05:43 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:05:43 GMT
ENV ODOO_VERSION=14.0
# Mon, 09 Jan 2023 17:28:26 GMT
ARG ODOO_RELEASE=20230109
# Mon, 09 Jan 2023 17:28:26 GMT
ARG ODOO_SHA=ef9eef9a5e5bbeb455ac7d1c05cc675e74876609
# Mon, 09 Jan 2023 17:29:57 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=ef9eef9a5e5bbeb455ac7d1c05cc675e74876609
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 09 Jan 2023 17:30:01 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 09 Jan 2023 17:30:02 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 09 Jan 2023 17:30:02 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=ef9eef9a5e5bbeb455ac7d1c05cc675e74876609
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 09 Jan 2023 17:30:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Jan 2023 17:30:02 GMT
EXPOSE 8069 8071 8072
# Mon, 09 Jan 2023 17:30:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Jan 2023 17:30:03 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 09 Jan 2023 17:30:03 GMT
USER odoo
# Mon, 09 Jan 2023 17:30:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Jan 2023 17:30:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fd809e7e6338e9ff619aa861a2c83ea5794e2e9f1e27208941b0cb0830d586`  
		Last Modified: Wed, 21 Dec 2022 12:09:24 GMT  
		Size: 213.2 MB (213188652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7447a10d2ac09f77c91f4405dd22b28022ae50b65e4a89bd2b93bc773c1a76f`  
		Last Modified: Wed, 21 Dec 2022 12:09:01 GMT  
		Size: 13.5 MB (13515235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2a982470c9023112777135e16db2722d58d0e80637be6f6512ed77e73a0e45`  
		Last Modified: Wed, 21 Dec 2022 12:08:58 GMT  
		Size: 457.1 KB (457118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a544d327de006924dd60a859a82d9c513ab5f002251804152861d11559cc469`  
		Last Modified: Mon, 09 Jan 2023 17:32:39 GMT  
		Size: 277.2 MB (277221565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3579f37f60d1655e52cf6b98f3cd07ce8b0a9e4368954149a4800f8e73a1cb36`  
		Last Modified: Mon, 09 Jan 2023 17:32:05 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fa3a5e996155834744df896dc803a863f292b43d949fd7ea7eceb3224d723b`  
		Last Modified: Mon, 09 Jan 2023 17:32:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d414295bd9260495dccd4a9d612d0e1edf468888131eac32ba1a30579f6ea`  
		Last Modified: Mon, 09 Jan 2023 17:32:06 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29f8132f384d6215cf2f5a3a36e52796e6acd72aa8447fe8e542374c91fc465`  
		Last Modified: Mon, 09 Jan 2023 17:32:05 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:23b46c23b29e0e5c587a43bd7ea71c5062ec28ea3ea9d6aabd64c19a5165b09d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:314e1420ca7e9be5d96ed3ed6664142d6dab49f18ed9c430da4262f2d9105de7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.7 MB (559717244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab32b8a4c4532b78ceac26d63673bb22f27a767185820e88e615eefb2d17bf87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:59:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 11:59:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 11:59:17 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:00:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:00:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:00:39 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:02:25 GMT
ENV ODOO_VERSION=15.0
# Mon, 09 Jan 2023 17:26:48 GMT
ARG ODOO_RELEASE=20230109
# Mon, 09 Jan 2023 17:26:48 GMT
ARG ODOO_SHA=618e45490616f63dfb68077523c2971cbb6cdda7
# Mon, 09 Jan 2023 17:28:05 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=618e45490616f63dfb68077523c2971cbb6cdda7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 09 Jan 2023 17:28:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 09 Jan 2023 17:28:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 09 Jan 2023 17:28:10 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=618e45490616f63dfb68077523c2971cbb6cdda7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 09 Jan 2023 17:28:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Jan 2023 17:28:10 GMT
EXPOSE 8069 8071 8072
# Mon, 09 Jan 2023 17:28:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Jan 2023 17:28:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 09 Jan 2023 17:28:10 GMT
USER odoo
# Mon, 09 Jan 2023 17:28:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Jan 2023 17:28:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b33e635a777ad2593a9a160436a438c4cf068b815a9d16dc6e4975f5df5b1c`  
		Last Modified: Wed, 21 Dec 2022 12:07:50 GMT  
		Size: 220.3 MB (220298472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c52fa0ca226e1b60d6963a358d003976668bd83f0ec398305fc945994bf0de`  
		Last Modified: Wed, 21 Dec 2022 12:07:24 GMT  
		Size: 2.6 MB (2573903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb896edd9e6352eb0d87d3b7f13ed806d0cef48cb80e239f4867f41c8a2b79dc`  
		Last Modified: Wed, 21 Dec 2022 12:07:23 GMT  
		Size: 452.6 KB (452551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f935093692d4512a7817a8c4893d23ee6e48716d65cbf0ebb634e48a2fe97049`  
		Last Modified: Mon, 09 Jan 2023 17:31:55 GMT  
		Size: 305.0 MB (304992910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e858fa5cf23c317ae1d890903b405954e2daf6287a517561078a46dcc5a1f908`  
		Last Modified: Mon, 09 Jan 2023 17:31:19 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb96c5015867306298274f9b698e5f55c0a177d1efd362466617c9aa0259045`  
		Last Modified: Mon, 09 Jan 2023 17:31:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ba9fc44b401219598b7abc1c490744cf267d9beb385006d63ebecd8bdf7e3f`  
		Last Modified: Mon, 09 Jan 2023 17:31:19 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9225dbc9d8ec07ea0ca1ce48ab7ea88d92da7b0d47849536827872ed739f9e5d`  
		Last Modified: Mon, 09 Jan 2023 17:31:19 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:23b46c23b29e0e5c587a43bd7ea71c5062ec28ea3ea9d6aabd64c19a5165b09d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:314e1420ca7e9be5d96ed3ed6664142d6dab49f18ed9c430da4262f2d9105de7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.7 MB (559717244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab32b8a4c4532b78ceac26d63673bb22f27a767185820e88e615eefb2d17bf87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:59:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 11:59:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 11:59:17 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:00:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:00:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:00:39 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:02:25 GMT
ENV ODOO_VERSION=15.0
# Mon, 09 Jan 2023 17:26:48 GMT
ARG ODOO_RELEASE=20230109
# Mon, 09 Jan 2023 17:26:48 GMT
ARG ODOO_SHA=618e45490616f63dfb68077523c2971cbb6cdda7
# Mon, 09 Jan 2023 17:28:05 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=618e45490616f63dfb68077523c2971cbb6cdda7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 09 Jan 2023 17:28:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 09 Jan 2023 17:28:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 09 Jan 2023 17:28:10 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=618e45490616f63dfb68077523c2971cbb6cdda7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 09 Jan 2023 17:28:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Jan 2023 17:28:10 GMT
EXPOSE 8069 8071 8072
# Mon, 09 Jan 2023 17:28:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Jan 2023 17:28:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 09 Jan 2023 17:28:10 GMT
USER odoo
# Mon, 09 Jan 2023 17:28:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Jan 2023 17:28:11 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b33e635a777ad2593a9a160436a438c4cf068b815a9d16dc6e4975f5df5b1c`  
		Last Modified: Wed, 21 Dec 2022 12:07:50 GMT  
		Size: 220.3 MB (220298472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c52fa0ca226e1b60d6963a358d003976668bd83f0ec398305fc945994bf0de`  
		Last Modified: Wed, 21 Dec 2022 12:07:24 GMT  
		Size: 2.6 MB (2573903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb896edd9e6352eb0d87d3b7f13ed806d0cef48cb80e239f4867f41c8a2b79dc`  
		Last Modified: Wed, 21 Dec 2022 12:07:23 GMT  
		Size: 452.6 KB (452551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f935093692d4512a7817a8c4893d23ee6e48716d65cbf0ebb634e48a2fe97049`  
		Last Modified: Mon, 09 Jan 2023 17:31:55 GMT  
		Size: 305.0 MB (304992910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e858fa5cf23c317ae1d890903b405954e2daf6287a517561078a46dcc5a1f908`  
		Last Modified: Mon, 09 Jan 2023 17:31:19 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb96c5015867306298274f9b698e5f55c0a177d1efd362466617c9aa0259045`  
		Last Modified: Mon, 09 Jan 2023 17:31:19 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ba9fc44b401219598b7abc1c490744cf267d9beb385006d63ebecd8bdf7e3f`  
		Last Modified: Mon, 09 Jan 2023 17:31:19 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9225dbc9d8ec07ea0ca1ce48ab7ea88d92da7b0d47849536827872ed739f9e5d`  
		Last Modified: Mon, 09 Jan 2023 17:31:19 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:7b04b8be419b6b940827e6c3276d549f4c0883b06e32c4ff6750c25547080a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:611f1ae42f1d55e689343ad37869a86d0da8c2c3d71ed4c00a0bd1624518f442
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.2 MB (566181831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae486913bed23ecf80b51b6d8250226ad044e3dae2b2ff7d672b2fe0a2549c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:59:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 11:59:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 11:59:17 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:00:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:00:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:00:39 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:00:39 GMT
ENV ODOO_VERSION=16.0
# Mon, 09 Jan 2023 17:25:10 GMT
ARG ODOO_RELEASE=20230109
# Mon, 09 Jan 2023 17:25:10 GMT
ARG ODOO_SHA=884bf72c7318835b9ac56be2594032cbba7b8c7b
# Mon, 09 Jan 2023 17:26:37 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=884bf72c7318835b9ac56be2594032cbba7b8c7b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 09 Jan 2023 17:26:41 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 09 Jan 2023 17:26:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 09 Jan 2023 17:26:42 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=884bf72c7318835b9ac56be2594032cbba7b8c7b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 09 Jan 2023 17:26:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Jan 2023 17:26:42 GMT
EXPOSE 8069 8071 8072
# Mon, 09 Jan 2023 17:26:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Jan 2023 17:26:43 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 09 Jan 2023 17:26:43 GMT
USER odoo
# Mon, 09 Jan 2023 17:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Jan 2023 17:26:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b33e635a777ad2593a9a160436a438c4cf068b815a9d16dc6e4975f5df5b1c`  
		Last Modified: Wed, 21 Dec 2022 12:07:50 GMT  
		Size: 220.3 MB (220298472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c52fa0ca226e1b60d6963a358d003976668bd83f0ec398305fc945994bf0de`  
		Last Modified: Wed, 21 Dec 2022 12:07:24 GMT  
		Size: 2.6 MB (2573903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb896edd9e6352eb0d87d3b7f13ed806d0cef48cb80e239f4867f41c8a2b79dc`  
		Last Modified: Wed, 21 Dec 2022 12:07:23 GMT  
		Size: 452.6 KB (452551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ae9ab0a9e82fab6d9612eed16e35fee33fe399ea5a0c859fadcca782a7466b`  
		Last Modified: Mon, 09 Jan 2023 17:31:07 GMT  
		Size: 311.5 MB (311457494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f056f24da2085eea170fb40195e03edac39471525e5b080eb6547567fca665`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bde8ac0d976140e8a7052cc8258540b112cc1a96292c4f9e80fd8c4889c4de`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957fbc26e7fecb9392893753baf9540b573cd8d95041a2bac31860b2a06828dc`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adecbd9431af755491ccabb0fd9d6aa3347846e6fe9df27511aad0ba3a1cd6e4`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:7b04b8be419b6b940827e6c3276d549f4c0883b06e32c4ff6750c25547080a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:611f1ae42f1d55e689343ad37869a86d0da8c2c3d71ed4c00a0bd1624518f442
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.2 MB (566181831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae486913bed23ecf80b51b6d8250226ad044e3dae2b2ff7d672b2fe0a2549c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:59:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 11:59:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 11:59:17 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:00:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:00:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:00:39 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:00:39 GMT
ENV ODOO_VERSION=16.0
# Mon, 09 Jan 2023 17:25:10 GMT
ARG ODOO_RELEASE=20230109
# Mon, 09 Jan 2023 17:25:10 GMT
ARG ODOO_SHA=884bf72c7318835b9ac56be2594032cbba7b8c7b
# Mon, 09 Jan 2023 17:26:37 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=884bf72c7318835b9ac56be2594032cbba7b8c7b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 09 Jan 2023 17:26:41 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 09 Jan 2023 17:26:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 09 Jan 2023 17:26:42 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=884bf72c7318835b9ac56be2594032cbba7b8c7b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 09 Jan 2023 17:26:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Jan 2023 17:26:42 GMT
EXPOSE 8069 8071 8072
# Mon, 09 Jan 2023 17:26:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Jan 2023 17:26:43 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 09 Jan 2023 17:26:43 GMT
USER odoo
# Mon, 09 Jan 2023 17:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Jan 2023 17:26:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b33e635a777ad2593a9a160436a438c4cf068b815a9d16dc6e4975f5df5b1c`  
		Last Modified: Wed, 21 Dec 2022 12:07:50 GMT  
		Size: 220.3 MB (220298472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c52fa0ca226e1b60d6963a358d003976668bd83f0ec398305fc945994bf0de`  
		Last Modified: Wed, 21 Dec 2022 12:07:24 GMT  
		Size: 2.6 MB (2573903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb896edd9e6352eb0d87d3b7f13ed806d0cef48cb80e239f4867f41c8a2b79dc`  
		Last Modified: Wed, 21 Dec 2022 12:07:23 GMT  
		Size: 452.6 KB (452551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ae9ab0a9e82fab6d9612eed16e35fee33fe399ea5a0c859fadcca782a7466b`  
		Last Modified: Mon, 09 Jan 2023 17:31:07 GMT  
		Size: 311.5 MB (311457494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f056f24da2085eea170fb40195e03edac39471525e5b080eb6547567fca665`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bde8ac0d976140e8a7052cc8258540b112cc1a96292c4f9e80fd8c4889c4de`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957fbc26e7fecb9392893753baf9540b573cd8d95041a2bac31860b2a06828dc`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adecbd9431af755491ccabb0fd9d6aa3347846e6fe9df27511aad0ba3a1cd6e4`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:7b04b8be419b6b940827e6c3276d549f4c0883b06e32c4ff6750c25547080a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:611f1ae42f1d55e689343ad37869a86d0da8c2c3d71ed4c00a0bd1624518f442
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.2 MB (566181831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae486913bed23ecf80b51b6d8250226ad044e3dae2b2ff7d672b2fe0a2549c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:59:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 11:59:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 11:59:17 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:00:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:00:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:00:39 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:00:39 GMT
ENV ODOO_VERSION=16.0
# Mon, 09 Jan 2023 17:25:10 GMT
ARG ODOO_RELEASE=20230109
# Mon, 09 Jan 2023 17:25:10 GMT
ARG ODOO_SHA=884bf72c7318835b9ac56be2594032cbba7b8c7b
# Mon, 09 Jan 2023 17:26:37 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=884bf72c7318835b9ac56be2594032cbba7b8c7b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 09 Jan 2023 17:26:41 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 09 Jan 2023 17:26:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 09 Jan 2023 17:26:42 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=884bf72c7318835b9ac56be2594032cbba7b8c7b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 09 Jan 2023 17:26:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Jan 2023 17:26:42 GMT
EXPOSE 8069 8071 8072
# Mon, 09 Jan 2023 17:26:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Jan 2023 17:26:43 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 09 Jan 2023 17:26:43 GMT
USER odoo
# Mon, 09 Jan 2023 17:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Jan 2023 17:26:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b33e635a777ad2593a9a160436a438c4cf068b815a9d16dc6e4975f5df5b1c`  
		Last Modified: Wed, 21 Dec 2022 12:07:50 GMT  
		Size: 220.3 MB (220298472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c52fa0ca226e1b60d6963a358d003976668bd83f0ec398305fc945994bf0de`  
		Last Modified: Wed, 21 Dec 2022 12:07:24 GMT  
		Size: 2.6 MB (2573903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb896edd9e6352eb0d87d3b7f13ed806d0cef48cb80e239f4867f41c8a2b79dc`  
		Last Modified: Wed, 21 Dec 2022 12:07:23 GMT  
		Size: 452.6 KB (452551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ae9ab0a9e82fab6d9612eed16e35fee33fe399ea5a0c859fadcca782a7466b`  
		Last Modified: Mon, 09 Jan 2023 17:31:07 GMT  
		Size: 311.5 MB (311457494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f056f24da2085eea170fb40195e03edac39471525e5b080eb6547567fca665`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bde8ac0d976140e8a7052cc8258540b112cc1a96292c4f9e80fd8c4889c4de`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957fbc26e7fecb9392893753baf9540b573cd8d95041a2bac31860b2a06828dc`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adecbd9431af755491ccabb0fd9d6aa3347846e6fe9df27511aad0ba3a1cd6e4`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
