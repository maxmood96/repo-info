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
$ docker pull odoo@sha256:78215285a1eef9ac9756a28befb006142fc73cf1de55cfb18d3d6822a28bb102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:1e202672186ea243f02fb685dcb59dd3f695d8e374418f5b17fd5f418b2ae6d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.8 MB (531773673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82414da7d9435d5c39aafa44613a42a198eb02fd95cc3d812f74a761e885c4fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:22 GMT
ADD file:2254e48bf53907be7a0b1744bc4fcd7805a627672793cf5f86a01ac751a1b24d in / 
# Wed, 01 Mar 2023 04:10:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 18:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Mar 2023 18:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Mar 2023 18:28:55 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 18:30:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 01 Mar 2023 18:30:34 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 18:30:37 GMT
RUN npm install -g rtlcss
# Wed, 01 Mar 2023 18:30:37 GMT
ENV ODOO_VERSION=14.0
# Wed, 01 Mar 2023 18:30:37 GMT
ARG ODOO_RELEASE=20230224
# Wed, 01 Mar 2023 18:30:37 GMT
ARG ODOO_SHA=a59688f0c2c830f243fec130e3c651d93f188658
# Wed, 01 Mar 2023 18:31:51 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=a59688f0c2c830f243fec130e3c651d93f188658
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 01 Mar 2023 18:31:55 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 01 Mar 2023 18:31:55 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 01 Mar 2023 18:31:56 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=a59688f0c2c830f243fec130e3c651d93f188658
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 01 Mar 2023 18:31:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 01 Mar 2023 18:31:56 GMT
EXPOSE 8069 8071 8072
# Wed, 01 Mar 2023 18:31:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 01 Mar 2023 18:31:56 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 01 Mar 2023 18:31:56 GMT
USER odoo
# Wed, 01 Mar 2023 18:31:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Mar 2023 18:31:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8fd419aca81cfd3987d61550e700546537628562693bc01acc9f85468f483706`  
		Last Modified: Wed, 01 Mar 2023 04:15:04 GMT  
		Size: 27.1 MB (27139882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098558a773310761d275e903e5c82ae82e62aeca797d7d0ef00b03572bacee38`  
		Last Modified: Wed, 01 Mar 2023 18:34:10 GMT  
		Size: 213.2 MB (213201748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41b0353de2b48785e5a3ca2e802fc194ffe1afca628efde22ee6692794f2b0f`  
		Last Modified: Wed, 01 Mar 2023 18:33:49 GMT  
		Size: 13.5 MB (13517762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5562db7956eed4ba9670c33d418977feff13172f8d3c302618dc6c4c8201c0`  
		Last Modified: Wed, 01 Mar 2023 18:33:46 GMT  
		Size: 456.4 KB (456438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c063294eab71e0394a317f2d805372af72fbabeebce99cefd1507b32ea575c`  
		Last Modified: Wed, 01 Mar 2023 18:34:17 GMT  
		Size: 277.5 MB (277455380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2382c9da6fe0de330b11a65847f8d1d516e71935f1c3db98faa45e16f7ca52d`  
		Last Modified: Wed, 01 Mar 2023 18:33:44 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e1b80c34356ca83c08bc030486a118ae1c1784f59e48a3f08c731c14747a66`  
		Last Modified: Wed, 01 Mar 2023 18:33:44 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708bf5c21446698f8d3a6a5c090c8ddf5c36b814f9f9b2a0b703b2144d84bcf2`  
		Last Modified: Wed, 01 Mar 2023 18:33:44 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac3b0fd6a30ce9976532d8bfe7d7dcb4cce4dea512cdd3c1a6a6cb8a3c0ad67`  
		Last Modified: Wed, 01 Mar 2023 18:33:44 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:78215285a1eef9ac9756a28befb006142fc73cf1de55cfb18d3d6822a28bb102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:1e202672186ea243f02fb685dcb59dd3f695d8e374418f5b17fd5f418b2ae6d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.8 MB (531773673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82414da7d9435d5c39aafa44613a42a198eb02fd95cc3d812f74a761e885c4fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Mar 2023 04:10:22 GMT
ADD file:2254e48bf53907be7a0b1744bc4fcd7805a627672793cf5f86a01ac751a1b24d in / 
# Wed, 01 Mar 2023 04:10:22 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 18:28:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Mar 2023 18:28:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Mar 2023 18:28:55 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 18:30:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 01 Mar 2023 18:30:34 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 18:30:37 GMT
RUN npm install -g rtlcss
# Wed, 01 Mar 2023 18:30:37 GMT
ENV ODOO_VERSION=14.0
# Wed, 01 Mar 2023 18:30:37 GMT
ARG ODOO_RELEASE=20230224
# Wed, 01 Mar 2023 18:30:37 GMT
ARG ODOO_SHA=a59688f0c2c830f243fec130e3c651d93f188658
# Wed, 01 Mar 2023 18:31:51 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=a59688f0c2c830f243fec130e3c651d93f188658
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 01 Mar 2023 18:31:55 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 01 Mar 2023 18:31:55 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 01 Mar 2023 18:31:56 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=a59688f0c2c830f243fec130e3c651d93f188658
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 01 Mar 2023 18:31:56 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 01 Mar 2023 18:31:56 GMT
EXPOSE 8069 8071 8072
# Wed, 01 Mar 2023 18:31:56 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 01 Mar 2023 18:31:56 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 01 Mar 2023 18:31:56 GMT
USER odoo
# Wed, 01 Mar 2023 18:31:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Mar 2023 18:31:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8fd419aca81cfd3987d61550e700546537628562693bc01acc9f85468f483706`  
		Last Modified: Wed, 01 Mar 2023 04:15:04 GMT  
		Size: 27.1 MB (27139882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098558a773310761d275e903e5c82ae82e62aeca797d7d0ef00b03572bacee38`  
		Last Modified: Wed, 01 Mar 2023 18:34:10 GMT  
		Size: 213.2 MB (213201748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41b0353de2b48785e5a3ca2e802fc194ffe1afca628efde22ee6692794f2b0f`  
		Last Modified: Wed, 01 Mar 2023 18:33:49 GMT  
		Size: 13.5 MB (13517762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5562db7956eed4ba9670c33d418977feff13172f8d3c302618dc6c4c8201c0`  
		Last Modified: Wed, 01 Mar 2023 18:33:46 GMT  
		Size: 456.4 KB (456438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c063294eab71e0394a317f2d805372af72fbabeebce99cefd1507b32ea575c`  
		Last Modified: Wed, 01 Mar 2023 18:34:17 GMT  
		Size: 277.5 MB (277455380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2382c9da6fe0de330b11a65847f8d1d516e71935f1c3db98faa45e16f7ca52d`  
		Last Modified: Wed, 01 Mar 2023 18:33:44 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e1b80c34356ca83c08bc030486a118ae1c1784f59e48a3f08c731c14747a66`  
		Last Modified: Wed, 01 Mar 2023 18:33:44 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:708bf5c21446698f8d3a6a5c090c8ddf5c36b814f9f9b2a0b703b2144d84bcf2`  
		Last Modified: Wed, 01 Mar 2023 18:33:44 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac3b0fd6a30ce9976532d8bfe7d7dcb4cce4dea512cdd3c1a6a6cb8a3c0ad67`  
		Last Modified: Wed, 01 Mar 2023 18:33:44 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:861f94d1e4bf7983a13737c920975e7bd747d89e8bbc6b79ed0f6a6a10d477ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:3455d9627814a147e403ea524f3582ecba8f9919df2ce52d0eb1b89dda00e250
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.2 MB (560164459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3497e8867c1c49bb11141d97659fe8c4fc33c54b25595cbb03043cd6d43813`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 18:24:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Mar 2023 18:24:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Mar 2023 18:24:38 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 18:25:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 01 Mar 2023 18:25:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 18:25:57 GMT
RUN npm install -g rtlcss
# Wed, 01 Mar 2023 18:27:31 GMT
ENV ODOO_VERSION=15.0
# Wed, 01 Mar 2023 18:27:32 GMT
ARG ODOO_RELEASE=20230224
# Wed, 01 Mar 2023 18:27:32 GMT
ARG ODOO_SHA=44613aceddf8e928ca50fc23979b1141fa4bb7d5
# Wed, 01 Mar 2023 18:28:46 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=44613aceddf8e928ca50fc23979b1141fa4bb7d5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 01 Mar 2023 18:28:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 01 Mar 2023 18:28:50 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 01 Mar 2023 18:28:50 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=44613aceddf8e928ca50fc23979b1141fa4bb7d5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 01 Mar 2023 18:28:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 01 Mar 2023 18:28:51 GMT
EXPOSE 8069 8071 8072
# Wed, 01 Mar 2023 18:28:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 01 Mar 2023 18:28:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 01 Mar 2023 18:28:51 GMT
USER odoo
# Wed, 01 Mar 2023 18:28:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Mar 2023 18:28:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0ec9a41360fcaaa5f19bb2439c6b467cf4a33a0b0eaf74839a228bf1723d08`  
		Last Modified: Wed, 01 Mar 2023 18:32:40 GMT  
		Size: 220.3 MB (220298372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cf54990bd6ba63bd5db241053550b76696f1e581799de07562f631fcad34a5`  
		Last Modified: Wed, 01 Mar 2023 18:32:15 GMT  
		Size: 2.6 MB (2575211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0db56a607542f664eb62978c779afe3f2c828db31f16594b723c048ba1b53`  
		Last Modified: Wed, 01 Mar 2023 18:32:15 GMT  
		Size: 452.0 KB (452031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49456b388f9e852bc666c280316ddaa238683fefc7f198d5e59ddaf0dbfb038`  
		Last Modified: Wed, 01 Mar 2023 18:33:35 GMT  
		Size: 305.4 MB (305424980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb2a0289f3f441a80a5b474d7e5274b769dee29c3a05049a2dbd1b4f992691e`  
		Last Modified: Wed, 01 Mar 2023 18:33:02 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9c5651f65103ed470c1a1a4ba0fd0f47400aa960b3788ba47597f5124afab4`  
		Last Modified: Wed, 01 Mar 2023 18:33:02 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a40abae37bb85cd85c7aa5c5dd6f5d96dc4a196d4b5c1478f13130ffd3e1cc`  
		Last Modified: Wed, 01 Mar 2023 18:33:02 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b743c3833ef05ddb52d14a7a7cc4d187b047892b9270a2e46fd47026bc4c58`  
		Last Modified: Wed, 01 Mar 2023 18:33:02 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:861f94d1e4bf7983a13737c920975e7bd747d89e8bbc6b79ed0f6a6a10d477ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:3455d9627814a147e403ea524f3582ecba8f9919df2ce52d0eb1b89dda00e250
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.2 MB (560164459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3497e8867c1c49bb11141d97659fe8c4fc33c54b25595cbb03043cd6d43813`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 18:24:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Mar 2023 18:24:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Mar 2023 18:24:38 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 18:25:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 01 Mar 2023 18:25:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 18:25:57 GMT
RUN npm install -g rtlcss
# Wed, 01 Mar 2023 18:27:31 GMT
ENV ODOO_VERSION=15.0
# Wed, 01 Mar 2023 18:27:32 GMT
ARG ODOO_RELEASE=20230224
# Wed, 01 Mar 2023 18:27:32 GMT
ARG ODOO_SHA=44613aceddf8e928ca50fc23979b1141fa4bb7d5
# Wed, 01 Mar 2023 18:28:46 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=44613aceddf8e928ca50fc23979b1141fa4bb7d5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 01 Mar 2023 18:28:50 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 01 Mar 2023 18:28:50 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 01 Mar 2023 18:28:50 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=44613aceddf8e928ca50fc23979b1141fa4bb7d5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 01 Mar 2023 18:28:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 01 Mar 2023 18:28:51 GMT
EXPOSE 8069 8071 8072
# Wed, 01 Mar 2023 18:28:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 01 Mar 2023 18:28:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 01 Mar 2023 18:28:51 GMT
USER odoo
# Wed, 01 Mar 2023 18:28:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Mar 2023 18:28:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0ec9a41360fcaaa5f19bb2439c6b467cf4a33a0b0eaf74839a228bf1723d08`  
		Last Modified: Wed, 01 Mar 2023 18:32:40 GMT  
		Size: 220.3 MB (220298372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cf54990bd6ba63bd5db241053550b76696f1e581799de07562f631fcad34a5`  
		Last Modified: Wed, 01 Mar 2023 18:32:15 GMT  
		Size: 2.6 MB (2575211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0db56a607542f664eb62978c779afe3f2c828db31f16594b723c048ba1b53`  
		Last Modified: Wed, 01 Mar 2023 18:32:15 GMT  
		Size: 452.0 KB (452031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49456b388f9e852bc666c280316ddaa238683fefc7f198d5e59ddaf0dbfb038`  
		Last Modified: Wed, 01 Mar 2023 18:33:35 GMT  
		Size: 305.4 MB (305424980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb2a0289f3f441a80a5b474d7e5274b769dee29c3a05049a2dbd1b4f992691e`  
		Last Modified: Wed, 01 Mar 2023 18:33:02 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9c5651f65103ed470c1a1a4ba0fd0f47400aa960b3788ba47597f5124afab4`  
		Last Modified: Wed, 01 Mar 2023 18:33:02 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a40abae37bb85cd85c7aa5c5dd6f5d96dc4a196d4b5c1478f13130ffd3e1cc`  
		Last Modified: Wed, 01 Mar 2023 18:33:02 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b743c3833ef05ddb52d14a7a7cc4d187b047892b9270a2e46fd47026bc4c58`  
		Last Modified: Wed, 01 Mar 2023 18:33:02 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:461b1aa5451e5e6123f671ed7a867c448a6e20c247e809bc6fb0f176f59b0b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:dfa42829162d994edb3312f52e8df2d37a1a46b13dd7ae525f8a234c6c81a5c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.6 MB (568643589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b68c11f7889d66b512248e7dddcdf7b21f8baca4bafe0af5cf8c867293ca899`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 18:24:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Mar 2023 18:24:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Mar 2023 18:24:38 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 18:25:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 01 Mar 2023 18:25:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 18:25:57 GMT
RUN npm install -g rtlcss
# Wed, 01 Mar 2023 18:25:57 GMT
ENV ODOO_VERSION=16.0
# Wed, 01 Mar 2023 18:25:57 GMT
ARG ODOO_RELEASE=20230224
# Wed, 01 Mar 2023 18:25:57 GMT
ARG ODOO_SHA=2a4ed4c36b82a05707b6e709182266672a32ace2
# Wed, 01 Mar 2023 18:27:19 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=2a4ed4c36b82a05707b6e709182266672a32ace2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 01 Mar 2023 18:27:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 01 Mar 2023 18:27:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 01 Mar 2023 18:27:24 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=2a4ed4c36b82a05707b6e709182266672a32ace2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 01 Mar 2023 18:27:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 01 Mar 2023 18:27:24 GMT
EXPOSE 8069 8071 8072
# Wed, 01 Mar 2023 18:27:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 01 Mar 2023 18:27:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 01 Mar 2023 18:27:24 GMT
USER odoo
# Wed, 01 Mar 2023 18:27:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Mar 2023 18:27:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0ec9a41360fcaaa5f19bb2439c6b467cf4a33a0b0eaf74839a228bf1723d08`  
		Last Modified: Wed, 01 Mar 2023 18:32:40 GMT  
		Size: 220.3 MB (220298372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cf54990bd6ba63bd5db241053550b76696f1e581799de07562f631fcad34a5`  
		Last Modified: Wed, 01 Mar 2023 18:32:15 GMT  
		Size: 2.6 MB (2575211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0db56a607542f664eb62978c779afe3f2c828db31f16594b723c048ba1b53`  
		Last Modified: Wed, 01 Mar 2023 18:32:15 GMT  
		Size: 452.0 KB (452031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca834915f2be271417a4fc03a5af10aa0ecb2a51ff21588a3915eb7fdb258e75`  
		Last Modified: Wed, 01 Mar 2023 18:32:49 GMT  
		Size: 313.9 MB (313904107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c59126ad844e26577cfd65b9b3a3af48eaa7b25926942c9967bd243818bc4`  
		Last Modified: Wed, 01 Mar 2023 18:32:13 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb79e096fba84ef4010564a1da426ff9429173d3f04fc2d23866425c5ef1086`  
		Last Modified: Wed, 01 Mar 2023 18:32:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04223c20ada0470295447eccd599131a0fa814d82e348334b4f43ec957932296`  
		Last Modified: Wed, 01 Mar 2023 18:32:13 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060f53b96269a4ba58b8ae4ccc88378410215e33665365d4bca270a71bfad4e0`  
		Last Modified: Wed, 01 Mar 2023 18:32:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:461b1aa5451e5e6123f671ed7a867c448a6e20c247e809bc6fb0f176f59b0b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:dfa42829162d994edb3312f52e8df2d37a1a46b13dd7ae525f8a234c6c81a5c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.6 MB (568643589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b68c11f7889d66b512248e7dddcdf7b21f8baca4bafe0af5cf8c867293ca899`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 18:24:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Mar 2023 18:24:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Mar 2023 18:24:38 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 18:25:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 01 Mar 2023 18:25:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 18:25:57 GMT
RUN npm install -g rtlcss
# Wed, 01 Mar 2023 18:25:57 GMT
ENV ODOO_VERSION=16.0
# Wed, 01 Mar 2023 18:25:57 GMT
ARG ODOO_RELEASE=20230224
# Wed, 01 Mar 2023 18:25:57 GMT
ARG ODOO_SHA=2a4ed4c36b82a05707b6e709182266672a32ace2
# Wed, 01 Mar 2023 18:27:19 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=2a4ed4c36b82a05707b6e709182266672a32ace2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 01 Mar 2023 18:27:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 01 Mar 2023 18:27:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 01 Mar 2023 18:27:24 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=2a4ed4c36b82a05707b6e709182266672a32ace2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 01 Mar 2023 18:27:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 01 Mar 2023 18:27:24 GMT
EXPOSE 8069 8071 8072
# Wed, 01 Mar 2023 18:27:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 01 Mar 2023 18:27:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 01 Mar 2023 18:27:24 GMT
USER odoo
# Wed, 01 Mar 2023 18:27:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Mar 2023 18:27:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0ec9a41360fcaaa5f19bb2439c6b467cf4a33a0b0eaf74839a228bf1723d08`  
		Last Modified: Wed, 01 Mar 2023 18:32:40 GMT  
		Size: 220.3 MB (220298372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cf54990bd6ba63bd5db241053550b76696f1e581799de07562f631fcad34a5`  
		Last Modified: Wed, 01 Mar 2023 18:32:15 GMT  
		Size: 2.6 MB (2575211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0db56a607542f664eb62978c779afe3f2c828db31f16594b723c048ba1b53`  
		Last Modified: Wed, 01 Mar 2023 18:32:15 GMT  
		Size: 452.0 KB (452031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca834915f2be271417a4fc03a5af10aa0ecb2a51ff21588a3915eb7fdb258e75`  
		Last Modified: Wed, 01 Mar 2023 18:32:49 GMT  
		Size: 313.9 MB (313904107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c59126ad844e26577cfd65b9b3a3af48eaa7b25926942c9967bd243818bc4`  
		Last Modified: Wed, 01 Mar 2023 18:32:13 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb79e096fba84ef4010564a1da426ff9429173d3f04fc2d23866425c5ef1086`  
		Last Modified: Wed, 01 Mar 2023 18:32:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04223c20ada0470295447eccd599131a0fa814d82e348334b4f43ec957932296`  
		Last Modified: Wed, 01 Mar 2023 18:32:13 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060f53b96269a4ba58b8ae4ccc88378410215e33665365d4bca270a71bfad4e0`  
		Last Modified: Wed, 01 Mar 2023 18:32:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:461b1aa5451e5e6123f671ed7a867c448a6e20c247e809bc6fb0f176f59b0b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:dfa42829162d994edb3312f52e8df2d37a1a46b13dd7ae525f8a234c6c81a5c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **568.6 MB (568643589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b68c11f7889d66b512248e7dddcdf7b21f8baca4bafe0af5cf8c867293ca899`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 18:24:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 01 Mar 2023 18:24:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 01 Mar 2023 18:24:38 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 18:25:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 01 Mar 2023 18:25:55 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 18:25:57 GMT
RUN npm install -g rtlcss
# Wed, 01 Mar 2023 18:25:57 GMT
ENV ODOO_VERSION=16.0
# Wed, 01 Mar 2023 18:25:57 GMT
ARG ODOO_RELEASE=20230224
# Wed, 01 Mar 2023 18:25:57 GMT
ARG ODOO_SHA=2a4ed4c36b82a05707b6e709182266672a32ace2
# Wed, 01 Mar 2023 18:27:19 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=2a4ed4c36b82a05707b6e709182266672a32ace2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 01 Mar 2023 18:27:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 01 Mar 2023 18:27:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 01 Mar 2023 18:27:24 GMT
# ARGS: ODOO_RELEASE=20230224 ODOO_SHA=2a4ed4c36b82a05707b6e709182266672a32ace2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 01 Mar 2023 18:27:24 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 01 Mar 2023 18:27:24 GMT
EXPOSE 8069 8071 8072
# Wed, 01 Mar 2023 18:27:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 01 Mar 2023 18:27:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 01 Mar 2023 18:27:24 GMT
USER odoo
# Wed, 01 Mar 2023 18:27:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Mar 2023 18:27:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0ec9a41360fcaaa5f19bb2439c6b467cf4a33a0b0eaf74839a228bf1723d08`  
		Last Modified: Wed, 01 Mar 2023 18:32:40 GMT  
		Size: 220.3 MB (220298372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cf54990bd6ba63bd5db241053550b76696f1e581799de07562f631fcad34a5`  
		Last Modified: Wed, 01 Mar 2023 18:32:15 GMT  
		Size: 2.6 MB (2575211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d0db56a607542f664eb62978c779afe3f2c828db31f16594b723c048ba1b53`  
		Last Modified: Wed, 01 Mar 2023 18:32:15 GMT  
		Size: 452.0 KB (452031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca834915f2be271417a4fc03a5af10aa0ecb2a51ff21588a3915eb7fdb258e75`  
		Last Modified: Wed, 01 Mar 2023 18:32:49 GMT  
		Size: 313.9 MB (313904107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c59126ad844e26577cfd65b9b3a3af48eaa7b25926942c9967bd243818bc4`  
		Last Modified: Wed, 01 Mar 2023 18:32:13 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb79e096fba84ef4010564a1da426ff9429173d3f04fc2d23866425c5ef1086`  
		Last Modified: Wed, 01 Mar 2023 18:32:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04223c20ada0470295447eccd599131a0fa814d82e348334b4f43ec957932296`  
		Last Modified: Wed, 01 Mar 2023 18:32:13 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060f53b96269a4ba58b8ae4ccc88378410215e33665365d4bca270a71bfad4e0`  
		Last Modified: Wed, 01 Mar 2023 18:32:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
