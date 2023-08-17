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
$ docker pull odoo@sha256:09b3fe59b733219bd5aa958444839ec01fb06113cabd7d4441424b5366fd8921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14` - linux; amd64

```console
$ docker pull odoo@sha256:b35b62524f1856dba715db51b201d0ffb67c59818d5c1c30c36493f641bb03fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.1 MB (533061268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4183c4ac89df63c101eaf50519bf16f10add073182038b476be6a72090eaafcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:31 GMT
ADD file:d4315fd7ceb67a5501410e4392ad3fd73642d6e2490f3626ce20a29321fa3682 in / 
# Wed, 16 Aug 2023 01:00:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:21:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:21:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:21:48 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:23:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:23:15 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:23:17 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:23:17 GMT
ENV ODOO_VERSION=14.0
# Thu, 17 Aug 2023 10:16:21 GMT
ARG ODOO_RELEASE=20230816
# Thu, 17 Aug 2023 10:16:22 GMT
ARG ODOO_SHA=765652a730a334b94432b241c54823bd523ff7f4
# Thu, 17 Aug 2023 10:17:36 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=765652a730a334b94432b241c54823bd523ff7f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 17 Aug 2023 10:17:39 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 17 Aug 2023 10:17:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 17 Aug 2023 10:17:40 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=765652a730a334b94432b241c54823bd523ff7f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 17 Aug 2023 10:17:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 17 Aug 2023 10:17:40 GMT
EXPOSE 8069 8071 8072
# Thu, 17 Aug 2023 10:17:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 17 Aug 2023 10:17:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 17 Aug 2023 10:17:40 GMT
USER odoo
# Thu, 17 Aug 2023 10:17:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Aug 2023 10:17:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ddade83992f922bd9baa0e67dd5f7e8f518b6ed19c67e2ea076c92a8b38416c0`  
		Last Modified: Wed, 16 Aug 2023 01:05:53 GMT  
		Size: 27.2 MB (27187428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f94b5ed49a5ec953e83f40169b949808c407c931aa7085a46846902af681137`  
		Last Modified: Wed, 16 Aug 2023 10:27:04 GMT  
		Size: 213.2 MB (213180563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc841b610acfd62afebf8a7dee73883ec3020b5a503100b4b133df781a3bd04d`  
		Last Modified: Wed, 16 Aug 2023 10:26:44 GMT  
		Size: 13.5 MB (13522678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497179ab34d276ead4cb01db777028bf342b2339f9089021ec71d1791a5da458`  
		Last Modified: Wed, 16 Aug 2023 10:26:42 GMT  
		Size: 458.9 KB (458875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e005392ed364569164b46fceeba3187503f04125662df95cf30d1ab17b4d25`  
		Last Modified: Thu, 17 Aug 2023 10:19:55 GMT  
		Size: 278.7 MB (278709258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6b12399580fad3f59932e35cc2698391ed0b2f237d616bb95418df17c6b424`  
		Last Modified: Thu, 17 Aug 2023 10:19:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dd63b53a2ee452a5e92f1225a96cddc37966876867ab6c310501207669afa7`  
		Last Modified: Thu, 17 Aug 2023 10:19:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0126a56c1433b129ee83b97dd1cb11167641c054607f3079bdbf7fae0ba74d4`  
		Last Modified: Thu, 17 Aug 2023 10:19:25 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d421a3438580432179e2081808b881aaffbdd7fde5a38b7905b4fc8d26f6b69`  
		Last Modified: Thu, 17 Aug 2023 10:19:25 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:14.0`

```console
$ docker pull odoo@sha256:09b3fe59b733219bd5aa958444839ec01fb06113cabd7d4441424b5366fd8921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:14.0` - linux; amd64

```console
$ docker pull odoo@sha256:b35b62524f1856dba715db51b201d0ffb67c59818d5c1c30c36493f641bb03fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.1 MB (533061268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4183c4ac89df63c101eaf50519bf16f10add073182038b476be6a72090eaafcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:31 GMT
ADD file:d4315fd7ceb67a5501410e4392ad3fd73642d6e2490f3626ce20a29321fa3682 in / 
# Wed, 16 Aug 2023 01:00:32 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:21:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:21:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:21:48 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:23:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:23:15 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:23:17 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:23:17 GMT
ENV ODOO_VERSION=14.0
# Thu, 17 Aug 2023 10:16:21 GMT
ARG ODOO_RELEASE=20230816
# Thu, 17 Aug 2023 10:16:22 GMT
ARG ODOO_SHA=765652a730a334b94432b241c54823bd523ff7f4
# Thu, 17 Aug 2023 10:17:36 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=765652a730a334b94432b241c54823bd523ff7f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 17 Aug 2023 10:17:39 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 17 Aug 2023 10:17:39 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 17 Aug 2023 10:17:40 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=765652a730a334b94432b241c54823bd523ff7f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 17 Aug 2023 10:17:40 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 17 Aug 2023 10:17:40 GMT
EXPOSE 8069 8071 8072
# Thu, 17 Aug 2023 10:17:40 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 17 Aug 2023 10:17:40 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 17 Aug 2023 10:17:40 GMT
USER odoo
# Thu, 17 Aug 2023 10:17:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Aug 2023 10:17:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ddade83992f922bd9baa0e67dd5f7e8f518b6ed19c67e2ea076c92a8b38416c0`  
		Last Modified: Wed, 16 Aug 2023 01:05:53 GMT  
		Size: 27.2 MB (27187428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f94b5ed49a5ec953e83f40169b949808c407c931aa7085a46846902af681137`  
		Last Modified: Wed, 16 Aug 2023 10:27:04 GMT  
		Size: 213.2 MB (213180563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc841b610acfd62afebf8a7dee73883ec3020b5a503100b4b133df781a3bd04d`  
		Last Modified: Wed, 16 Aug 2023 10:26:44 GMT  
		Size: 13.5 MB (13522678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497179ab34d276ead4cb01db777028bf342b2339f9089021ec71d1791a5da458`  
		Last Modified: Wed, 16 Aug 2023 10:26:42 GMT  
		Size: 458.9 KB (458875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e005392ed364569164b46fceeba3187503f04125662df95cf30d1ab17b4d25`  
		Last Modified: Thu, 17 Aug 2023 10:19:55 GMT  
		Size: 278.7 MB (278709258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6b12399580fad3f59932e35cc2698391ed0b2f237d616bb95418df17c6b424`  
		Last Modified: Thu, 17 Aug 2023 10:19:26 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dd63b53a2ee452a5e92f1225a96cddc37966876867ab6c310501207669afa7`  
		Last Modified: Thu, 17 Aug 2023 10:19:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0126a56c1433b129ee83b97dd1cb11167641c054607f3079bdbf7fae0ba74d4`  
		Last Modified: Thu, 17 Aug 2023 10:19:25 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d421a3438580432179e2081808b881aaffbdd7fde5a38b7905b4fc8d26f6b69`  
		Last Modified: Thu, 17 Aug 2023 10:19:25 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15`

```console
$ docker pull odoo@sha256:12185829981f21f976b671a6743ee7d78dc4a7f4ddd2b2c7db3641977c5224e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:7e46db04852b617c88e7a6495320a214e815d8786846aa0121073e22ed47b769
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562096490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329e8367c40a2df343a4ea1767b96e3d5ce2aeb1897fc56c4c300657b8f42f53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:16:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:16:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:16:30 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:20:15 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:20:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:20:23 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:20:24 GMT
ENV ODOO_VERSION=15.0
# Thu, 17 Aug 2023 10:14:58 GMT
ARG ODOO_RELEASE=20230816
# Thu, 17 Aug 2023 10:14:58 GMT
ARG ODOO_SHA=fd9d9025030be5e07ed90e3f471151e17a7ac9e0
# Thu, 17 Aug 2023 10:16:12 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=fd9d9025030be5e07ed90e3f471151e17a7ac9e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 17 Aug 2023 10:16:16 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 17 Aug 2023 10:16:16 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 17 Aug 2023 10:16:16 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=fd9d9025030be5e07ed90e3f471151e17a7ac9e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 17 Aug 2023 10:16:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 17 Aug 2023 10:16:16 GMT
EXPOSE 8069 8071 8072
# Thu, 17 Aug 2023 10:16:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 17 Aug 2023 10:16:17 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 17 Aug 2023 10:16:17 GMT
USER odoo
# Thu, 17 Aug 2023 10:16:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Aug 2023 10:16:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18e6ccd242f394f129dfb1542a55693c092efc01323daf560f2cea9f7c93f9d`  
		Last Modified: Wed, 16 Aug 2023 10:26:21 GMT  
		Size: 220.3 MB (220302753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8225239de85406993faad4ed5848d1f01aadf58ffcb88de9ba6cbee36f6eff`  
		Last Modified: Wed, 16 Aug 2023 10:25:57 GMT  
		Size: 2.6 MB (2576533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf486b5a74cf8335fb645fe6c165ce01e7422386abffef6f5874c9353e969af6`  
		Last Modified: Wed, 16 Aug 2023 10:25:57 GMT  
		Size: 454.4 KB (454433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ec421c57b25b989c904640cdaef97d7dc4a13c76489d1cdfa62cf15f4c4fb6`  
		Last Modified: Thu, 17 Aug 2023 10:19:16 GMT  
		Size: 307.3 MB (307342630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37096971d2a1aaa9c55c562dfac4062159781ba80e88da1c44f114a4f16ec4a2`  
		Last Modified: Thu, 17 Aug 2023 10:18:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6298d63f01934915ee955356a47026a035bd34b10580dd1206cbaf0cb625f8c`  
		Last Modified: Thu, 17 Aug 2023 10:18:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ce37df3736f581d1ac13c6a6882ea1717b496e8467cd877ae4d1eb79fdd2cc`  
		Last Modified: Thu, 17 Aug 2023 10:18:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff110c6ee883801e2d82bf742b38f742f9da129bb650d39c4560ed3bdf71e50`  
		Last Modified: Thu, 17 Aug 2023 10:18:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:15.0`

```console
$ docker pull odoo@sha256:12185829981f21f976b671a6743ee7d78dc4a7f4ddd2b2c7db3641977c5224e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:7e46db04852b617c88e7a6495320a214e815d8786846aa0121073e22ed47b769
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.1 MB (562096490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329e8367c40a2df343a4ea1767b96e3d5ce2aeb1897fc56c4c300657b8f42f53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:16:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:16:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:16:30 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:20:15 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:20:22 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:20:23 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:20:24 GMT
ENV ODOO_VERSION=15.0
# Thu, 17 Aug 2023 10:14:58 GMT
ARG ODOO_RELEASE=20230816
# Thu, 17 Aug 2023 10:14:58 GMT
ARG ODOO_SHA=fd9d9025030be5e07ed90e3f471151e17a7ac9e0
# Thu, 17 Aug 2023 10:16:12 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=fd9d9025030be5e07ed90e3f471151e17a7ac9e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 17 Aug 2023 10:16:16 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 17 Aug 2023 10:16:16 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 17 Aug 2023 10:16:16 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=fd9d9025030be5e07ed90e3f471151e17a7ac9e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 17 Aug 2023 10:16:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 17 Aug 2023 10:16:16 GMT
EXPOSE 8069 8071 8072
# Thu, 17 Aug 2023 10:16:17 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 17 Aug 2023 10:16:17 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 17 Aug 2023 10:16:17 GMT
USER odoo
# Thu, 17 Aug 2023 10:16:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Aug 2023 10:16:17 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18e6ccd242f394f129dfb1542a55693c092efc01323daf560f2cea9f7c93f9d`  
		Last Modified: Wed, 16 Aug 2023 10:26:21 GMT  
		Size: 220.3 MB (220302753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8225239de85406993faad4ed5848d1f01aadf58ffcb88de9ba6cbee36f6eff`  
		Last Modified: Wed, 16 Aug 2023 10:25:57 GMT  
		Size: 2.6 MB (2576533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf486b5a74cf8335fb645fe6c165ce01e7422386abffef6f5874c9353e969af6`  
		Last Modified: Wed, 16 Aug 2023 10:25:57 GMT  
		Size: 454.4 KB (454433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ec421c57b25b989c904640cdaef97d7dc4a13c76489d1cdfa62cf15f4c4fb6`  
		Last Modified: Thu, 17 Aug 2023 10:19:16 GMT  
		Size: 307.3 MB (307342630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37096971d2a1aaa9c55c562dfac4062159781ba80e88da1c44f114a4f16ec4a2`  
		Last Modified: Thu, 17 Aug 2023 10:18:42 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6298d63f01934915ee955356a47026a035bd34b10580dd1206cbaf0cb625f8c`  
		Last Modified: Thu, 17 Aug 2023 10:18:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ce37df3736f581d1ac13c6a6882ea1717b496e8467cd877ae4d1eb79fdd2cc`  
		Last Modified: Thu, 17 Aug 2023 10:18:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff110c6ee883801e2d82bf742b38f742f9da129bb650d39c4560ed3bdf71e50`  
		Last Modified: Thu, 17 Aug 2023 10:18:42 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16`

```console
$ docker pull odoo@sha256:c6a5e6ecf65cc06c16fedbd8fb30e57b707866c2d3a66adf619d0e5eb8d86ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:aea26ad5d9ddde024bc65fab0c9e126f9f34b5fdcd8ada9a6fa6fff14a4442a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.1 MB (576060265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee332cbe8830d6f2c16a64b99155eca16a84aa314a48e41be89fb2837ad2fa12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:16:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:16:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:16:30 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:17:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:17:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:17:44 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:17:44 GMT
ENV ODOO_VERSION=16.0
# Thu, 17 Aug 2023 10:13:19 GMT
ARG ODOO_RELEASE=20230816
# Thu, 17 Aug 2023 10:13:19 GMT
ARG ODOO_SHA=fc84b0d3fc0cb5506378c91f19681248c6fdb36e
# Thu, 17 Aug 2023 10:14:40 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=fc84b0d3fc0cb5506378c91f19681248c6fdb36e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 17 Aug 2023 10:14:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 17 Aug 2023 10:14:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 17 Aug 2023 10:14:45 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=fc84b0d3fc0cb5506378c91f19681248c6fdb36e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 17 Aug 2023 10:14:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 17 Aug 2023 10:14:46 GMT
EXPOSE 8069 8071 8072
# Thu, 17 Aug 2023 10:14:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 17 Aug 2023 10:14:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 17 Aug 2023 10:14:46 GMT
USER odoo
# Thu, 17 Aug 2023 10:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Aug 2023 10:14:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38faf7b926f64bb75adbf63bb8f9cf962e9fe7240f1b77f975713e522fb38f2f`  
		Last Modified: Wed, 16 Aug 2023 10:25:32 GMT  
		Size: 221.0 MB (220992472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f422a2822ff3c0ddcb0feae90917ad16bfadc792ed6120bb85ec478c192fc14`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 2.6 MB (2579930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e455fdc49a2fa9b84da301d6cacd3ac952037699a291e871cd86ab33ff34b4`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 454.4 KB (454421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87358e6bb36d571ca2c6850f6decdc49db89367b35f6e3803f404ab964dc5d47`  
		Last Modified: Thu, 17 Aug 2023 10:18:29 GMT  
		Size: 320.6 MB (320613299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b320b6cc330fdab724e8646c5256dcad07738d771d3b56b55856a86a9dc3fc`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b592bed196fd23afb7c13e423f00e608b135fa62c651fa75a793bb9ad089f603`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610cd8914d942fe24e705f6e38960750af9b1bfb350668d2103274d90288072c`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e3366e705964c9dba1f589914490d3083790c68344747495afe3654362cec9`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:16.0`

```console
$ docker pull odoo@sha256:c6a5e6ecf65cc06c16fedbd8fb30e57b707866c2d3a66adf619d0e5eb8d86ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:aea26ad5d9ddde024bc65fab0c9e126f9f34b5fdcd8ada9a6fa6fff14a4442a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.1 MB (576060265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee332cbe8830d6f2c16a64b99155eca16a84aa314a48e41be89fb2837ad2fa12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:16:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:16:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:16:30 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:17:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:17:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:17:44 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:17:44 GMT
ENV ODOO_VERSION=16.0
# Thu, 17 Aug 2023 10:13:19 GMT
ARG ODOO_RELEASE=20230816
# Thu, 17 Aug 2023 10:13:19 GMT
ARG ODOO_SHA=fc84b0d3fc0cb5506378c91f19681248c6fdb36e
# Thu, 17 Aug 2023 10:14:40 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=fc84b0d3fc0cb5506378c91f19681248c6fdb36e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 17 Aug 2023 10:14:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 17 Aug 2023 10:14:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 17 Aug 2023 10:14:45 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=fc84b0d3fc0cb5506378c91f19681248c6fdb36e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 17 Aug 2023 10:14:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 17 Aug 2023 10:14:46 GMT
EXPOSE 8069 8071 8072
# Thu, 17 Aug 2023 10:14:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 17 Aug 2023 10:14:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 17 Aug 2023 10:14:46 GMT
USER odoo
# Thu, 17 Aug 2023 10:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Aug 2023 10:14:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38faf7b926f64bb75adbf63bb8f9cf962e9fe7240f1b77f975713e522fb38f2f`  
		Last Modified: Wed, 16 Aug 2023 10:25:32 GMT  
		Size: 221.0 MB (220992472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f422a2822ff3c0ddcb0feae90917ad16bfadc792ed6120bb85ec478c192fc14`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 2.6 MB (2579930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e455fdc49a2fa9b84da301d6cacd3ac952037699a291e871cd86ab33ff34b4`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 454.4 KB (454421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87358e6bb36d571ca2c6850f6decdc49db89367b35f6e3803f404ab964dc5d47`  
		Last Modified: Thu, 17 Aug 2023 10:18:29 GMT  
		Size: 320.6 MB (320613299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b320b6cc330fdab724e8646c5256dcad07738d771d3b56b55856a86a9dc3fc`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b592bed196fd23afb7c13e423f00e608b135fa62c651fa75a793bb9ad089f603`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610cd8914d942fe24e705f6e38960750af9b1bfb350668d2103274d90288072c`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e3366e705964c9dba1f589914490d3083790c68344747495afe3654362cec9`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:c6a5e6ecf65cc06c16fedbd8fb30e57b707866c2d3a66adf619d0e5eb8d86ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:aea26ad5d9ddde024bc65fab0c9e126f9f34b5fdcd8ada9a6fa6fff14a4442a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.1 MB (576060265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee332cbe8830d6f2c16a64b99155eca16a84aa314a48e41be89fb2837ad2fa12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:16:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:16:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:16:30 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:17:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:17:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:17:44 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:17:44 GMT
ENV ODOO_VERSION=16.0
# Thu, 17 Aug 2023 10:13:19 GMT
ARG ODOO_RELEASE=20230816
# Thu, 17 Aug 2023 10:13:19 GMT
ARG ODOO_SHA=fc84b0d3fc0cb5506378c91f19681248c6fdb36e
# Thu, 17 Aug 2023 10:14:40 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=fc84b0d3fc0cb5506378c91f19681248c6fdb36e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 17 Aug 2023 10:14:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 17 Aug 2023 10:14:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 17 Aug 2023 10:14:45 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=fc84b0d3fc0cb5506378c91f19681248c6fdb36e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 17 Aug 2023 10:14:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 17 Aug 2023 10:14:46 GMT
EXPOSE 8069 8071 8072
# Thu, 17 Aug 2023 10:14:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 17 Aug 2023 10:14:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 17 Aug 2023 10:14:46 GMT
USER odoo
# Thu, 17 Aug 2023 10:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Aug 2023 10:14:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38faf7b926f64bb75adbf63bb8f9cf962e9fe7240f1b77f975713e522fb38f2f`  
		Last Modified: Wed, 16 Aug 2023 10:25:32 GMT  
		Size: 221.0 MB (220992472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f422a2822ff3c0ddcb0feae90917ad16bfadc792ed6120bb85ec478c192fc14`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 2.6 MB (2579930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e455fdc49a2fa9b84da301d6cacd3ac952037699a291e871cd86ab33ff34b4`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 454.4 KB (454421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87358e6bb36d571ca2c6850f6decdc49db89367b35f6e3803f404ab964dc5d47`  
		Last Modified: Thu, 17 Aug 2023 10:18:29 GMT  
		Size: 320.6 MB (320613299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b320b6cc330fdab724e8646c5256dcad07738d771d3b56b55856a86a9dc3fc`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b592bed196fd23afb7c13e423f00e608b135fa62c651fa75a793bb9ad089f603`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610cd8914d942fe24e705f6e38960750af9b1bfb350668d2103274d90288072c`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e3366e705964c9dba1f589914490d3083790c68344747495afe3654362cec9`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
