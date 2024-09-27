<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:15.0-20240924`](#odoo150-20240924)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20240924`](#odoo160-20240924)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20240924`](#odoo170-20240924)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:9843efa8a0c8fba20f81a97fd04339fe0cc49c3162485c3e8bc0447295434ac1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:d28565659af264bfe830dfc95a44ef032e069e75c8a63c3f595323bf6e52b970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.4 MB (564422409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2141d6e26fd0a660e3834bc01cd04dd3caf07421b6f8494c42608f9ceb808f80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Sep 2024 07:24:50 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["bash"]
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=15.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=aff60a8a895d6b5f3cca83ac3832eccf3e40d820
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: ODOO_RELEASE=20240924 ODOO_SHA=aff60a8a895d6b5f3cca83ac3832eccf3e40d820
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: ODOO_RELEASE=20240924 ODOO_SHA=aff60a8a895d6b5f3cca83ac3832eccf3e40d820
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d909df565121bb938f8de2c68ec58b453dbd42b59e582173551c28935da85db7`  
		Last Modified: Fri, 27 Sep 2024 06:09:02 GMT  
		Size: 220.3 MB (220286824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ebfbdc10fc8e658e746669e59f5e3f199c5cfb69095da8c0f4844291b43e4f`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 2.5 MB (2491550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ff680154e92e79dfb4cf1ff4065138b93856471950f79ca75ff1c3b2a4f7ab`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 471.6 KB (471578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29fc5639ff0246d80d08305dc5568723f49e9b328fbce12db4e0d90c192b117`  
		Last Modified: Fri, 27 Sep 2024 06:09:04 GMT  
		Size: 309.7 MB (309741426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da66d955686e33af2975a2cfb7f4df451b8a8e490d5781a5b371042666056b98`  
		Last Modified: Fri, 27 Sep 2024 06:08:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c45db42d9903dbc1658fe92131cf3453c18868e7dee274007e9a994b571159b`  
		Last Modified: Fri, 27 Sep 2024 06:08:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e906b2624dd1953d7c2e3ff750d409099fc57d28997179eeaf98d0b215d1ac23`  
		Last Modified: Fri, 27 Sep 2024 06:08:58 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9c6706b015f0e03aafaa140c52723e2787fa3caca96bcad93894af1f9c90a`  
		Last Modified: Fri, 27 Sep 2024 06:08:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15` - unknown; unknown

```console
$ docker pull odoo@sha256:97f2cbe541cd8585334844e803e915f0a4bf0f1e294dc102f400198b6f4bd9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34714030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8432ae784c6c0cd6f8d290992ee1bd5cc0f441e26d7f5a644fd548a769ba2d`

```dockerfile
```

-	Layers:
	-	`sha256:9262ffa545ad15c92c607e494e42c9f31c1866677676846ee82ef62c54045d16`  
		Last Modified: Fri, 27 Sep 2024 06:08:57 GMT  
		Size: 34.7 MB (34689399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:767324ffe333a9fd91744f6a0b466c5a015e7c2d9a40942a4123f4595cafcfe5`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0`

```console
$ docker pull odoo@sha256:9843efa8a0c8fba20f81a97fd04339fe0cc49c3162485c3e8bc0447295434ac1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:d28565659af264bfe830dfc95a44ef032e069e75c8a63c3f595323bf6e52b970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.4 MB (564422409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2141d6e26fd0a660e3834bc01cd04dd3caf07421b6f8494c42608f9ceb808f80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Sep 2024 07:24:50 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["bash"]
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=15.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=aff60a8a895d6b5f3cca83ac3832eccf3e40d820
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: ODOO_RELEASE=20240924 ODOO_SHA=aff60a8a895d6b5f3cca83ac3832eccf3e40d820
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: ODOO_RELEASE=20240924 ODOO_SHA=aff60a8a895d6b5f3cca83ac3832eccf3e40d820
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d909df565121bb938f8de2c68ec58b453dbd42b59e582173551c28935da85db7`  
		Last Modified: Fri, 27 Sep 2024 06:09:02 GMT  
		Size: 220.3 MB (220286824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ebfbdc10fc8e658e746669e59f5e3f199c5cfb69095da8c0f4844291b43e4f`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 2.5 MB (2491550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ff680154e92e79dfb4cf1ff4065138b93856471950f79ca75ff1c3b2a4f7ab`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 471.6 KB (471578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29fc5639ff0246d80d08305dc5568723f49e9b328fbce12db4e0d90c192b117`  
		Last Modified: Fri, 27 Sep 2024 06:09:04 GMT  
		Size: 309.7 MB (309741426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da66d955686e33af2975a2cfb7f4df451b8a8e490d5781a5b371042666056b98`  
		Last Modified: Fri, 27 Sep 2024 06:08:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c45db42d9903dbc1658fe92131cf3453c18868e7dee274007e9a994b571159b`  
		Last Modified: Fri, 27 Sep 2024 06:08:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e906b2624dd1953d7c2e3ff750d409099fc57d28997179eeaf98d0b215d1ac23`  
		Last Modified: Fri, 27 Sep 2024 06:08:58 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9c6706b015f0e03aafaa140c52723e2787fa3caca96bcad93894af1f9c90a`  
		Last Modified: Fri, 27 Sep 2024 06:08:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0` - unknown; unknown

```console
$ docker pull odoo@sha256:97f2cbe541cd8585334844e803e915f0a4bf0f1e294dc102f400198b6f4bd9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34714030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8432ae784c6c0cd6f8d290992ee1bd5cc0f441e26d7f5a644fd548a769ba2d`

```dockerfile
```

-	Layers:
	-	`sha256:9262ffa545ad15c92c607e494e42c9f31c1866677676846ee82ef62c54045d16`  
		Last Modified: Fri, 27 Sep 2024 06:08:57 GMT  
		Size: 34.7 MB (34689399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:767324ffe333a9fd91744f6a0b466c5a015e7c2d9a40942a4123f4595cafcfe5`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0-20240924`

```console
$ docker pull odoo@sha256:9843efa8a0c8fba20f81a97fd04339fe0cc49c3162485c3e8bc0447295434ac1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0-20240924` - linux; amd64

```console
$ docker pull odoo@sha256:d28565659af264bfe830dfc95a44ef032e069e75c8a63c3f595323bf6e52b970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.4 MB (564422409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2141d6e26fd0a660e3834bc01cd04dd3caf07421b6f8494c42608f9ceb808f80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Sep 2024 07:24:50 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["bash"]
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=15.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=aff60a8a895d6b5f3cca83ac3832eccf3e40d820
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: ODOO_RELEASE=20240924 ODOO_SHA=aff60a8a895d6b5f3cca83ac3832eccf3e40d820
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: ODOO_RELEASE=20240924 ODOO_SHA=aff60a8a895d6b5f3cca83ac3832eccf3e40d820
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d909df565121bb938f8de2c68ec58b453dbd42b59e582173551c28935da85db7`  
		Last Modified: Fri, 27 Sep 2024 06:09:02 GMT  
		Size: 220.3 MB (220286824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ebfbdc10fc8e658e746669e59f5e3f199c5cfb69095da8c0f4844291b43e4f`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 2.5 MB (2491550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ff680154e92e79dfb4cf1ff4065138b93856471950f79ca75ff1c3b2a4f7ab`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 471.6 KB (471578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29fc5639ff0246d80d08305dc5568723f49e9b328fbce12db4e0d90c192b117`  
		Last Modified: Fri, 27 Sep 2024 06:09:04 GMT  
		Size: 309.7 MB (309741426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da66d955686e33af2975a2cfb7f4df451b8a8e490d5781a5b371042666056b98`  
		Last Modified: Fri, 27 Sep 2024 06:08:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c45db42d9903dbc1658fe92131cf3453c18868e7dee274007e9a994b571159b`  
		Last Modified: Fri, 27 Sep 2024 06:08:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e906b2624dd1953d7c2e3ff750d409099fc57d28997179eeaf98d0b215d1ac23`  
		Last Modified: Fri, 27 Sep 2024 06:08:58 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c9c6706b015f0e03aafaa140c52723e2787fa3caca96bcad93894af1f9c90a`  
		Last Modified: Fri, 27 Sep 2024 06:08:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0-20240924` - unknown; unknown

```console
$ docker pull odoo@sha256:97f2cbe541cd8585334844e803e915f0a4bf0f1e294dc102f400198b6f4bd9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34714030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8432ae784c6c0cd6f8d290992ee1bd5cc0f441e26d7f5a644fd548a769ba2d`

```dockerfile
```

-	Layers:
	-	`sha256:9262ffa545ad15c92c607e494e42c9f31c1866677676846ee82ef62c54045d16`  
		Last Modified: Fri, 27 Sep 2024 06:08:57 GMT  
		Size: 34.7 MB (34689399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:767324ffe333a9fd91744f6a0b466c5a015e7c2d9a40942a4123f4595cafcfe5`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16`

```console
$ docker pull odoo@sha256:f73f0d61864e86bf8e5a9955596ca2168e4b5b67da5123c0d73140332ecd9418
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:ec8f2ec436c941449fbadbb6d320c05517b6cc8e6ac79cb15921e5d2c96aff64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.3 MB (584316927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34de737b4733d932bcb13020106a94b9be214cbc76b86311ec7af0314907637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Sep 2024 07:24:50 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["bash"]
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=amd64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=16.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc311a188a110853a1c28ed9fe7cdfce883bbd804eaa795051973ba19c23032`  
		Last Modified: Fri, 27 Sep 2024 06:08:59 GMT  
		Size: 219.6 MB (219600536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06baa5167c77f9f8e1a63f8231991707b92935126bedcef178a275772c565718`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 2.5 MB (2493909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de46d00e898b1a899677f145ba6d226ba959a9b07790947fc44900d308265a4`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 471.6 KB (471588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e789b723d1404076de3a42a2a3d02cd73ec965fcadc09fb8aa20e431d8d49b`  
		Last Modified: Fri, 27 Sep 2024 06:08:59 GMT  
		Size: 330.3 MB (330319865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7dcdf9e3a97bac3e73d934d38031dccbe46465e7646fa9f6cb4bec687f0057`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96732414493e3854e26ad9456e3240915e9ed8cb5dbab52f3cab7dcffc1de94d`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb031cbed222898cc511a5a2d0f5dff58a61d6ba4dfee75a6395ee0cc731852`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e6aa6197c7fb563ee698d20bd0a0670688800105d9d631df80101919c1effa`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:c253423ad85e611bcf7cd42f71e8582e7c94d30b85470b9f8d3fc59d31f84490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38800713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a718e4095540165aca3bf57ca5155fb9a4b3167b1fcc83e44e22d83d2dc7a2b5`

```dockerfile
```

-	Layers:
	-	`sha256:070c09125f086826c0cec2484eca858f5c7627e9205e298ff23e1c9fe37a6bf9`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 38.8 MB (38774171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2acfd67d3035309f2c2a23be799cfa1b91bcae67589d2ea8018313bb7086ee14`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:88a7566f3823b3d80e531390894a5fb4a61e67db961ce97a7310ff0acb316be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.9 MB (579917553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157a99aa0c19f2f1728d52631e73825e53e32b7a5a1367fcacd5e8ba8e8c4d08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Sep 2024 07:24:50 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["bash"]
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=arm64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=16.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc07ca1fd04bb239b717843d66e1cf57936003e59f5361f86160bdb82f150bcb`  
		Last Modified: Fri, 27 Sep 2024 15:50:03 GMT  
		Size: 216.9 MB (216900167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1a5805bf35bd3ecb845dca89c9d70ed3acd5507df8c477ae451c60d4072b82`  
		Last Modified: Fri, 27 Sep 2024 15:49:58 GMT  
		Size: 2.5 MB (2504067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab746598447a5a6dbac6e237c968bf2df9c848f25e9a64fbb74690d1bc68638`  
		Last Modified: Fri, 27 Sep 2024 15:49:58 GMT  
		Size: 471.7 KB (471678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f76f502bc3600b930e4596406512e58296651732abe332596cdc0d16679b8ff`  
		Last Modified: Fri, 27 Sep 2024 15:50:07 GMT  
		Size: 330.0 MB (329964054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376932cce06bbd99ca65383d25b39fb6ad7b13a64b1db808283b4996ae47c1c8`  
		Last Modified: Fri, 27 Sep 2024 15:49:59 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe31936f49d06118e6ae804ad34a1cb51cf16080d7da863f74b5b274df125c2`  
		Last Modified: Fri, 27 Sep 2024 15:49:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbc55721ebfc409330f34f092bf1cda80f803d3a33cef4b809b541d116c36ca`  
		Last Modified: Fri, 27 Sep 2024 15:50:00 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7cbf8de8c11bdecdc0072fd6755aa2abc6994ba2ce503fbbe7e42f7281e870`  
		Last Modified: Fri, 27 Sep 2024 15:50:00 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:0fad97c970d4e6bc3b2aaee2d74293a62cc2ddbf9b69f4e19cf293d961f6717a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38807482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2cf6f0d9ba85be29d8b3f6d7c4722f2f51bf6d12fefe4e944ea989535138d4`

```dockerfile
```

-	Layers:
	-	`sha256:3d850a1e5e465406159cca9c9df0bc5ed725860f196a80aff1d1b07b8c4abd15`  
		Last Modified: Fri, 27 Sep 2024 15:49:59 GMT  
		Size: 38.8 MB (38780643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b3b531dd33aaa503006d14320dcf6779b6b4dbb1cb0f80a593886a8d13ac63`  
		Last Modified: Fri, 27 Sep 2024 15:49:58 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:b2545ca8619955b4285f8f135cdb968406f1588e0c552218f09a6eb86ed29c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.7 MB (598727871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d25e8ee1c9829ad5a6afa2f5f009d05f797cbad3e021efc57b804b6c1a6376`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:18 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Wed, 04 Sep 2024 22:26:20 GMT
CMD ["bash"]
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=16.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264aada665692908c4b8983b6bd2091af357eff0993979937a76dd9f51763515`  
		Last Modified: Thu, 12 Sep 2024 19:13:34 GMT  
		Size: 228.6 MB (228590078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84873cb30f32fd9394fcb668bd9c9b11a80f9b18a085897cc396be0d1084f51`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 2.6 MB (2634243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98862cf91747046250cd694f3318708d65474d47ce91022946523da8edd7bf41`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 471.6 KB (471557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c37be0ea3f9f6be6981c24d9dfc3cc7dc92f8cc8f42beeef18f8e197ca1a32`  
		Last Modified: Tue, 24 Sep 2024 23:54:05 GMT  
		Size: 331.7 MB (331730280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2aa6717f29cab46566dc7249be5d7d041e61930c6ef787a89e965c1c2c562e`  
		Last Modified: Tue, 24 Sep 2024 23:53:51 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48581e59dd7a1b8ae9bf1c00774bc41e63a19357cd6d53647435becc313353bf`  
		Last Modified: Tue, 24 Sep 2024 23:53:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600a46d5f2a7549c874c3946d9db6da20f73a599f2db6185406aaa2afa9b55d5`  
		Last Modified: Tue, 24 Sep 2024 23:53:51 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0eca1d3ca786535f2589feeaa37f2d9b7713d66de46efa08955706c9e848e2`  
		Last Modified: Tue, 24 Sep 2024 23:53:52 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:c4a172968a2262cf94a811dbf3415374e3955c9e679c317af19e2cad8d00edc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38807222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093977a86472c4b831013b0507bcdba36eaa726fd1e42a7a2f117418eb3dcce3`

```dockerfile
```

-	Layers:
	-	`sha256:9e1716cff012f522fffca67e09d94967716cb5e9caab34e8c8c9b096dd026d9a`  
		Last Modified: Tue, 24 Sep 2024 23:53:52 GMT  
		Size: 38.8 MB (38780630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5344a341ade9cfc02c8eb30a2912fdf7e5bc2b8442a8f723a01a585e81cd643f`  
		Last Modified: Tue, 24 Sep 2024 23:53:51 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:f73f0d61864e86bf8e5a9955596ca2168e4b5b67da5123c0d73140332ecd9418
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:ec8f2ec436c941449fbadbb6d320c05517b6cc8e6ac79cb15921e5d2c96aff64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.3 MB (584316927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34de737b4733d932bcb13020106a94b9be214cbc76b86311ec7af0314907637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Sep 2024 07:24:50 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["bash"]
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=amd64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=16.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc311a188a110853a1c28ed9fe7cdfce883bbd804eaa795051973ba19c23032`  
		Last Modified: Fri, 27 Sep 2024 06:08:59 GMT  
		Size: 219.6 MB (219600536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06baa5167c77f9f8e1a63f8231991707b92935126bedcef178a275772c565718`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 2.5 MB (2493909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de46d00e898b1a899677f145ba6d226ba959a9b07790947fc44900d308265a4`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 471.6 KB (471588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e789b723d1404076de3a42a2a3d02cd73ec965fcadc09fb8aa20e431d8d49b`  
		Last Modified: Fri, 27 Sep 2024 06:08:59 GMT  
		Size: 330.3 MB (330319865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7dcdf9e3a97bac3e73d934d38031dccbe46465e7646fa9f6cb4bec687f0057`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96732414493e3854e26ad9456e3240915e9ed8cb5dbab52f3cab7dcffc1de94d`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb031cbed222898cc511a5a2d0f5dff58a61d6ba4dfee75a6395ee0cc731852`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e6aa6197c7fb563ee698d20bd0a0670688800105d9d631df80101919c1effa`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c253423ad85e611bcf7cd42f71e8582e7c94d30b85470b9f8d3fc59d31f84490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38800713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a718e4095540165aca3bf57ca5155fb9a4b3167b1fcc83e44e22d83d2dc7a2b5`

```dockerfile
```

-	Layers:
	-	`sha256:070c09125f086826c0cec2484eca858f5c7627e9205e298ff23e1c9fe37a6bf9`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 38.8 MB (38774171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2acfd67d3035309f2c2a23be799cfa1b91bcae67589d2ea8018313bb7086ee14`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:88a7566f3823b3d80e531390894a5fb4a61e67db961ce97a7310ff0acb316be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.9 MB (579917553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157a99aa0c19f2f1728d52631e73825e53e32b7a5a1367fcacd5e8ba8e8c4d08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Sep 2024 07:24:50 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["bash"]
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=arm64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=16.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc07ca1fd04bb239b717843d66e1cf57936003e59f5361f86160bdb82f150bcb`  
		Last Modified: Fri, 27 Sep 2024 15:50:03 GMT  
		Size: 216.9 MB (216900167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1a5805bf35bd3ecb845dca89c9d70ed3acd5507df8c477ae451c60d4072b82`  
		Last Modified: Fri, 27 Sep 2024 15:49:58 GMT  
		Size: 2.5 MB (2504067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab746598447a5a6dbac6e237c968bf2df9c848f25e9a64fbb74690d1bc68638`  
		Last Modified: Fri, 27 Sep 2024 15:49:58 GMT  
		Size: 471.7 KB (471678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f76f502bc3600b930e4596406512e58296651732abe332596cdc0d16679b8ff`  
		Last Modified: Fri, 27 Sep 2024 15:50:07 GMT  
		Size: 330.0 MB (329964054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376932cce06bbd99ca65383d25b39fb6ad7b13a64b1db808283b4996ae47c1c8`  
		Last Modified: Fri, 27 Sep 2024 15:49:59 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe31936f49d06118e6ae804ad34a1cb51cf16080d7da863f74b5b274df125c2`  
		Last Modified: Fri, 27 Sep 2024 15:49:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbc55721ebfc409330f34f092bf1cda80f803d3a33cef4b809b541d116c36ca`  
		Last Modified: Fri, 27 Sep 2024 15:50:00 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7cbf8de8c11bdecdc0072fd6755aa2abc6994ba2ce503fbbe7e42f7281e870`  
		Last Modified: Fri, 27 Sep 2024 15:50:00 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0fad97c970d4e6bc3b2aaee2d74293a62cc2ddbf9b69f4e19cf293d961f6717a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38807482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2cf6f0d9ba85be29d8b3f6d7c4722f2f51bf6d12fefe4e944ea989535138d4`

```dockerfile
```

-	Layers:
	-	`sha256:3d850a1e5e465406159cca9c9df0bc5ed725860f196a80aff1d1b07b8c4abd15`  
		Last Modified: Fri, 27 Sep 2024 15:49:59 GMT  
		Size: 38.8 MB (38780643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b3b531dd33aaa503006d14320dcf6779b6b4dbb1cb0f80a593886a8d13ac63`  
		Last Modified: Fri, 27 Sep 2024 15:49:58 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b2545ca8619955b4285f8f135cdb968406f1588e0c552218f09a6eb86ed29c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.7 MB (598727871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d25e8ee1c9829ad5a6afa2f5f009d05f797cbad3e021efc57b804b6c1a6376`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:18 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Wed, 04 Sep 2024 22:26:20 GMT
CMD ["bash"]
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=16.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264aada665692908c4b8983b6bd2091af357eff0993979937a76dd9f51763515`  
		Last Modified: Thu, 12 Sep 2024 19:13:34 GMT  
		Size: 228.6 MB (228590078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84873cb30f32fd9394fcb668bd9c9b11a80f9b18a085897cc396be0d1084f51`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 2.6 MB (2634243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98862cf91747046250cd694f3318708d65474d47ce91022946523da8edd7bf41`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 471.6 KB (471557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c37be0ea3f9f6be6981c24d9dfc3cc7dc92f8cc8f42beeef18f8e197ca1a32`  
		Last Modified: Tue, 24 Sep 2024 23:54:05 GMT  
		Size: 331.7 MB (331730280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2aa6717f29cab46566dc7249be5d7d041e61930c6ef787a89e965c1c2c562e`  
		Last Modified: Tue, 24 Sep 2024 23:53:51 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48581e59dd7a1b8ae9bf1c00774bc41e63a19357cd6d53647435becc313353bf`  
		Last Modified: Tue, 24 Sep 2024 23:53:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600a46d5f2a7549c874c3946d9db6da20f73a599f2db6185406aaa2afa9b55d5`  
		Last Modified: Tue, 24 Sep 2024 23:53:51 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0eca1d3ca786535f2589feeaa37f2d9b7713d66de46efa08955706c9e848e2`  
		Last Modified: Tue, 24 Sep 2024 23:53:52 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c4a172968a2262cf94a811dbf3415374e3955c9e679c317af19e2cad8d00edc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38807222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093977a86472c4b831013b0507bcdba36eaa726fd1e42a7a2f117418eb3dcce3`

```dockerfile
```

-	Layers:
	-	`sha256:9e1716cff012f522fffca67e09d94967716cb5e9caab34e8c8c9b096dd026d9a`  
		Last Modified: Tue, 24 Sep 2024 23:53:52 GMT  
		Size: 38.8 MB (38780630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5344a341ade9cfc02c8eb30a2912fdf7e5bc2b8442a8f723a01a585e81cd643f`  
		Last Modified: Tue, 24 Sep 2024 23:53:51 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20240924`

```console
$ docker pull odoo@sha256:f73f0d61864e86bf8e5a9955596ca2168e4b5b67da5123c0d73140332ecd9418
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0-20240924` - linux; amd64

```console
$ docker pull odoo@sha256:ec8f2ec436c941449fbadbb6d320c05517b6cc8e6ac79cb15921e5d2c96aff64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.3 MB (584316927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34de737b4733d932bcb13020106a94b9be214cbc76b86311ec7af0314907637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Sep 2024 07:24:50 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["bash"]
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=amd64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=16.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc311a188a110853a1c28ed9fe7cdfce883bbd804eaa795051973ba19c23032`  
		Last Modified: Fri, 27 Sep 2024 06:08:59 GMT  
		Size: 219.6 MB (219600536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06baa5167c77f9f8e1a63f8231991707b92935126bedcef178a275772c565718`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 2.5 MB (2493909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de46d00e898b1a899677f145ba6d226ba959a9b07790947fc44900d308265a4`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 471.6 KB (471588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e789b723d1404076de3a42a2a3d02cd73ec965fcadc09fb8aa20e431d8d49b`  
		Last Modified: Fri, 27 Sep 2024 06:08:59 GMT  
		Size: 330.3 MB (330319865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7dcdf9e3a97bac3e73d934d38031dccbe46465e7646fa9f6cb4bec687f0057`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96732414493e3854e26ad9456e3240915e9ed8cb5dbab52f3cab7dcffc1de94d`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb031cbed222898cc511a5a2d0f5dff58a61d6ba4dfee75a6395ee0cc731852`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e6aa6197c7fb563ee698d20bd0a0670688800105d9d631df80101919c1effa`  
		Last Modified: Fri, 27 Sep 2024 06:08:56 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240924` - unknown; unknown

```console
$ docker pull odoo@sha256:c253423ad85e611bcf7cd42f71e8582e7c94d30b85470b9f8d3fc59d31f84490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38800713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a718e4095540165aca3bf57ca5155fb9a4b3167b1fcc83e44e22d83d2dc7a2b5`

```dockerfile
```

-	Layers:
	-	`sha256:070c09125f086826c0cec2484eca858f5c7627e9205e298ff23e1c9fe37a6bf9`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 38.8 MB (38774171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2acfd67d3035309f2c2a23be799cfa1b91bcae67589d2ea8018313bb7086ee14`  
		Last Modified: Fri, 27 Sep 2024 06:08:55 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240924` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:88a7566f3823b3d80e531390894a5fb4a61e67db961ce97a7310ff0acb316be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.9 MB (579917553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157a99aa0c19f2f1728d52631e73825e53e32b7a5a1367fcacd5e8ba8e8c4d08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Sep 2024 07:24:50 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["bash"]
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=arm64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=16.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc07ca1fd04bb239b717843d66e1cf57936003e59f5361f86160bdb82f150bcb`  
		Last Modified: Fri, 27 Sep 2024 15:50:03 GMT  
		Size: 216.9 MB (216900167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1a5805bf35bd3ecb845dca89c9d70ed3acd5507df8c477ae451c60d4072b82`  
		Last Modified: Fri, 27 Sep 2024 15:49:58 GMT  
		Size: 2.5 MB (2504067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab746598447a5a6dbac6e237c968bf2df9c848f25e9a64fbb74690d1bc68638`  
		Last Modified: Fri, 27 Sep 2024 15:49:58 GMT  
		Size: 471.7 KB (471678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f76f502bc3600b930e4596406512e58296651732abe332596cdc0d16679b8ff`  
		Last Modified: Fri, 27 Sep 2024 15:50:07 GMT  
		Size: 330.0 MB (329964054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376932cce06bbd99ca65383d25b39fb6ad7b13a64b1db808283b4996ae47c1c8`  
		Last Modified: Fri, 27 Sep 2024 15:49:59 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe31936f49d06118e6ae804ad34a1cb51cf16080d7da863f74b5b274df125c2`  
		Last Modified: Fri, 27 Sep 2024 15:49:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbc55721ebfc409330f34f092bf1cda80f803d3a33cef4b809b541d116c36ca`  
		Last Modified: Fri, 27 Sep 2024 15:50:00 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7cbf8de8c11bdecdc0072fd6755aa2abc6994ba2ce503fbbe7e42f7281e870`  
		Last Modified: Fri, 27 Sep 2024 15:50:00 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240924` - unknown; unknown

```console
$ docker pull odoo@sha256:0fad97c970d4e6bc3b2aaee2d74293a62cc2ddbf9b69f4e19cf293d961f6717a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38807482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2cf6f0d9ba85be29d8b3f6d7c4722f2f51bf6d12fefe4e944ea989535138d4`

```dockerfile
```

-	Layers:
	-	`sha256:3d850a1e5e465406159cca9c9df0bc5ed725860f196a80aff1d1b07b8c4abd15`  
		Last Modified: Fri, 27 Sep 2024 15:49:59 GMT  
		Size: 38.8 MB (38780643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b3b531dd33aaa503006d14320dcf6779b6b4dbb1cb0f80a593886a8d13ac63`  
		Last Modified: Fri, 27 Sep 2024 15:49:58 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240924` - linux; ppc64le

```console
$ docker pull odoo@sha256:b2545ca8619955b4285f8f135cdb968406f1588e0c552218f09a6eb86ed29c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.7 MB (598727871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d25e8ee1c9829ad5a6afa2f5f009d05f797cbad3e021efc57b804b6c1a6376`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:18 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Wed, 04 Sep 2024 22:26:20 GMT
CMD ["bash"]
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=16.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=1fb02a432e076dd71aca7a7611a07223919356b9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264aada665692908c4b8983b6bd2091af357eff0993979937a76dd9f51763515`  
		Last Modified: Thu, 12 Sep 2024 19:13:34 GMT  
		Size: 228.6 MB (228590078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84873cb30f32fd9394fcb668bd9c9b11a80f9b18a085897cc396be0d1084f51`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 2.6 MB (2634243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98862cf91747046250cd694f3318708d65474d47ce91022946523da8edd7bf41`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 471.6 KB (471557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c37be0ea3f9f6be6981c24d9dfc3cc7dc92f8cc8f42beeef18f8e197ca1a32`  
		Last Modified: Tue, 24 Sep 2024 23:54:05 GMT  
		Size: 331.7 MB (331730280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2aa6717f29cab46566dc7249be5d7d041e61930c6ef787a89e965c1c2c562e`  
		Last Modified: Tue, 24 Sep 2024 23:53:51 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48581e59dd7a1b8ae9bf1c00774bc41e63a19357cd6d53647435becc313353bf`  
		Last Modified: Tue, 24 Sep 2024 23:53:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600a46d5f2a7549c874c3946d9db6da20f73a599f2db6185406aaa2afa9b55d5`  
		Last Modified: Tue, 24 Sep 2024 23:53:51 GMT  
		Size: 592.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0eca1d3ca786535f2589feeaa37f2d9b7713d66de46efa08955706c9e848e2`  
		Last Modified: Tue, 24 Sep 2024 23:53:52 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240924` - unknown; unknown

```console
$ docker pull odoo@sha256:c4a172968a2262cf94a811dbf3415374e3955c9e679c317af19e2cad8d00edc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38807222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093977a86472c4b831013b0507bcdba36eaa726fd1e42a7a2f117418eb3dcce3`

```dockerfile
```

-	Layers:
	-	`sha256:9e1716cff012f522fffca67e09d94967716cb5e9caab34e8c8c9b096dd026d9a`  
		Last Modified: Tue, 24 Sep 2024 23:53:52 GMT  
		Size: 38.8 MB (38780630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5344a341ade9cfc02c8eb30a2912fdf7e5bc2b8442a8f723a01a585e81cd643f`  
		Last Modified: Tue, 24 Sep 2024 23:53:51 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:36fd7197f1e97190dfda0c804c332e07f3c8d718d458ad5f3b2f8491ad157e25
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
$ docker pull odoo@sha256:43bf24487392a69cbba4c78dd04f1e9256fe7ef1cc5fb9265ff88bcab71e1ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597423782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8e70aff2d8f640351cf4382eb68c37d89602eaaf8eac70918e3082dd3caef7`
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
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=amd64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdc2bdd6fe1c81c5e1707b1e1334d800515ad4bc509711fbe1aef16a0c9a831`  
		Last Modified: Tue, 24 Sep 2024 22:58:28 GMT  
		Size: 233.7 MB (233745742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ea0d7231036996ecd44fb0d2afa3be5c2ca836510334a2458436737d03285b`  
		Last Modified: Tue, 24 Sep 2024 22:58:22 GMT  
		Size: 2.3 MB (2315614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488b6736919b02c6166db8481dddd9338c7847c7390c8a4c4be44dce8e3fe245`  
		Last Modified: Tue, 24 Sep 2024 22:58:22 GMT  
		Size: 472.6 KB (472596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df24c0e1387ade27fbdd4115a5a16b0b15c3fd4ae2ef0e4e834d4a4b4523c680`  
		Last Modified: Tue, 24 Sep 2024 22:58:28 GMT  
		Size: 331.4 MB (331351704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19aa6718eccc1d1a631a4ed5d3a6c9cc93307971545e73599369ef37da710462`  
		Last Modified: Tue, 24 Sep 2024 22:58:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419db33196b10de8252def0cbb7948b9bc83ac6d9143da94612b4a91f23a08d8`  
		Last Modified: Tue, 24 Sep 2024 22:58:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e64c26094b509c32334d06e4c866a0f3cd20b9c0f8ca8a7236b1e8084f5046`  
		Last Modified: Tue, 24 Sep 2024 22:58:23 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc729e0bfa2ad2d5a1c2e9a84da058161d9657f0e1fe4653345dedf6a0c5e599`  
		Last Modified: Tue, 24 Sep 2024 22:58:24 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c494bd92bb2498df7190260b0c65622a124c49f942c40f4de9a73f2fe372e9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db0c0ab33d68c338648971b0dfa0f94bd68305a6fde6abae3e8fee3e0d45622`

```dockerfile
```

-	Layers:
	-	`sha256:bb2891f8c40e573243d9bfa92f40dac81903511686f16b7e2eb7f79e9a940703`  
		Last Modified: Tue, 24 Sep 2024 22:58:22 GMT  
		Size: 26.7 KB (26656 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ffdbdca71129cf26b9332d5aab8adcc0dd6a3df53030b3d5e9c671a3baca7eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.2 MB (592228945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3381e386582d9f118364fd5cbb273252151047be52fdec656ef0735c81822ef5`
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
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=arm64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6fadc8f1cdeb7018f3cc730bf5ca5cbd765df35c38756be1faa743e1786be9`  
		Last Modified: Tue, 17 Sep 2024 02:44:10 GMT  
		Size: 231.1 MB (231120471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a152b990945175781adb341944cf665969d147ca436c8a7b53374779e6f6941`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 2.3 MB (2307685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb15fba7b3792bd150e5f11e817299c61abde876d36eedbebdebfe879e3a79`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 472.7 KB (472677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3e0e5ed62ec2c72e1edc53ea6fa430ceb9d16629968ed4b2a987bc0997607e`  
		Last Modified: Tue, 24 Sep 2024 23:00:00 GMT  
		Size: 331.0 MB (330967345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45bd37950bf3e2f394333d1b2f12e199c823b1cf624663fdf3e0008ea64d06`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c072e53319017d46fd0a3ce0eeadde2221f03d781f31f46d43949a5abb9b837`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0c39ddc8cd60fc7767ee5b3ac3bf4ca7c17bd05d3671630ca141c41012388`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa01ac8bff5efbb8bcd137a7acf218e2a92eb61c30e4c2a014a0d95bde21359`  
		Last Modified: Tue, 24 Sep 2024 22:59:49 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:632ab2ea43c64f5ae705ec41fea55529ed3aec7d136f0fa18e5f4d8377707e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39379031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60848d38ddaafbade57c6f27bd4fcc1c58354b8b8dc400bd9b632ee8ec4fe555`

```dockerfile
```

-	Layers:
	-	`sha256:2e77c8d020aa5ee9229eeb54f12a25ce956dc8e76e33cf3be05ed7e2d809157d`  
		Last Modified: Tue, 24 Sep 2024 22:59:50 GMT  
		Size: 39.4 MB (39351855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a5d13345f349814c0163989f4faac5fde231284994f73985c0bd6aff37a68d`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:9e6fb0bc8932806e50cc81a21d4b79571dcc359380e51521f350b0bba558e765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.9 MB (613875614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d909497ffc1cf5db595c2276e3f8ce7d01e898eb46a6e5c7edde35dfae4892b5`
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
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c02d58ebd6534d5afb5a8012d7003f978314b782a10cd19fbc0e6d5d58df3`  
		Last Modified: Tue, 17 Sep 2024 01:53:43 GMT  
		Size: 243.3 MB (243275613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67640bc9b4d0c0923eccbc39ae739c9f734354b3f58be66b9058c61be83d80`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 2.6 MB (2592233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdfb807d76c75fa16e7bed3d97c1200cb7778b2234fd4ebd57a60a93314315`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 472.7 KB (472652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85279eeb6d37f668996f5ff7a095cb58a8da69f7b5342aa3d403225fa5067fe3`  
		Last Modified: Tue, 24 Sep 2024 23:03:36 GMT  
		Size: 333.1 MB (333084429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4acef3f8a5dd88b288877dc0be33fe60b3ba8bb210881b97b86d2992efdee`  
		Last Modified: Tue, 24 Sep 2024 23:03:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0290bf5f6d02b79e508551f6b9bb6150ea742423b4a858163741d02a5866b4`  
		Last Modified: Tue, 24 Sep 2024 23:03:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b377d5653f447bc74bbcc677bda6a7a9f578d9ce2ac9bfcf9c79e418110f0e`  
		Last Modified: Tue, 24 Sep 2024 23:03:28 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9e62e32aa9bbc89a37d970fe9bbdfa4a62e0462a82e622e4721b5950e2e23e`  
		Last Modified: Tue, 24 Sep 2024 23:03:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:ea87118dce6645d5bddc7f8e70b7da03e6aad5e32d3763b95327e4d35758f443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39380574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa640763a7e870cffcb562320ce6d69dab01acc22d43b97f72b6ad9740a2ef7e`

```dockerfile
```

-	Layers:
	-	`sha256:c2054b31c20d789430beef6d8f22d78bb9d67c19143b7e33e0fee1f9e046a0d8`  
		Last Modified: Tue, 24 Sep 2024 23:03:29 GMT  
		Size: 39.4 MB (39353643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dafeacaa96d2c3a28e5a23c07c22e07f2098f7e9f7cc65f6d86b46b99f1975a0`  
		Last Modified: Tue, 24 Sep 2024 23:03:27 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:36fd7197f1e97190dfda0c804c332e07f3c8d718d458ad5f3b2f8491ad157e25
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
$ docker pull odoo@sha256:43bf24487392a69cbba4c78dd04f1e9256fe7ef1cc5fb9265ff88bcab71e1ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597423782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8e70aff2d8f640351cf4382eb68c37d89602eaaf8eac70918e3082dd3caef7`
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
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=amd64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdc2bdd6fe1c81c5e1707b1e1334d800515ad4bc509711fbe1aef16a0c9a831`  
		Last Modified: Tue, 24 Sep 2024 22:58:28 GMT  
		Size: 233.7 MB (233745742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ea0d7231036996ecd44fb0d2afa3be5c2ca836510334a2458436737d03285b`  
		Last Modified: Tue, 24 Sep 2024 22:58:22 GMT  
		Size: 2.3 MB (2315614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488b6736919b02c6166db8481dddd9338c7847c7390c8a4c4be44dce8e3fe245`  
		Last Modified: Tue, 24 Sep 2024 22:58:22 GMT  
		Size: 472.6 KB (472596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df24c0e1387ade27fbdd4115a5a16b0b15c3fd4ae2ef0e4e834d4a4b4523c680`  
		Last Modified: Tue, 24 Sep 2024 22:58:28 GMT  
		Size: 331.4 MB (331351704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19aa6718eccc1d1a631a4ed5d3a6c9cc93307971545e73599369ef37da710462`  
		Last Modified: Tue, 24 Sep 2024 22:58:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419db33196b10de8252def0cbb7948b9bc83ac6d9143da94612b4a91f23a08d8`  
		Last Modified: Tue, 24 Sep 2024 22:58:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e64c26094b509c32334d06e4c866a0f3cd20b9c0f8ca8a7236b1e8084f5046`  
		Last Modified: Tue, 24 Sep 2024 22:58:23 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc729e0bfa2ad2d5a1c2e9a84da058161d9657f0e1fe4653345dedf6a0c5e599`  
		Last Modified: Tue, 24 Sep 2024 22:58:24 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c494bd92bb2498df7190260b0c65622a124c49f942c40f4de9a73f2fe372e9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db0c0ab33d68c338648971b0dfa0f94bd68305a6fde6abae3e8fee3e0d45622`

```dockerfile
```

-	Layers:
	-	`sha256:bb2891f8c40e573243d9bfa92f40dac81903511686f16b7e2eb7f79e9a940703`  
		Last Modified: Tue, 24 Sep 2024 22:58:22 GMT  
		Size: 26.7 KB (26656 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ffdbdca71129cf26b9332d5aab8adcc0dd6a3df53030b3d5e9c671a3baca7eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.2 MB (592228945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3381e386582d9f118364fd5cbb273252151047be52fdec656ef0735c81822ef5`
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
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=arm64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6fadc8f1cdeb7018f3cc730bf5ca5cbd765df35c38756be1faa743e1786be9`  
		Last Modified: Tue, 17 Sep 2024 02:44:10 GMT  
		Size: 231.1 MB (231120471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a152b990945175781adb341944cf665969d147ca436c8a7b53374779e6f6941`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 2.3 MB (2307685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb15fba7b3792bd150e5f11e817299c61abde876d36eedbebdebfe879e3a79`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 472.7 KB (472677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3e0e5ed62ec2c72e1edc53ea6fa430ceb9d16629968ed4b2a987bc0997607e`  
		Last Modified: Tue, 24 Sep 2024 23:00:00 GMT  
		Size: 331.0 MB (330967345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45bd37950bf3e2f394333d1b2f12e199c823b1cf624663fdf3e0008ea64d06`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c072e53319017d46fd0a3ce0eeadde2221f03d781f31f46d43949a5abb9b837`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0c39ddc8cd60fc7767ee5b3ac3bf4ca7c17bd05d3671630ca141c41012388`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa01ac8bff5efbb8bcd137a7acf218e2a92eb61c30e4c2a014a0d95bde21359`  
		Last Modified: Tue, 24 Sep 2024 22:59:49 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:632ab2ea43c64f5ae705ec41fea55529ed3aec7d136f0fa18e5f4d8377707e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39379031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60848d38ddaafbade57c6f27bd4fcc1c58354b8b8dc400bd9b632ee8ec4fe555`

```dockerfile
```

-	Layers:
	-	`sha256:2e77c8d020aa5ee9229eeb54f12a25ce956dc8e76e33cf3be05ed7e2d809157d`  
		Last Modified: Tue, 24 Sep 2024 22:59:50 GMT  
		Size: 39.4 MB (39351855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a5d13345f349814c0163989f4faac5fde231284994f73985c0bd6aff37a68d`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:9e6fb0bc8932806e50cc81a21d4b79571dcc359380e51521f350b0bba558e765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.9 MB (613875614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d909497ffc1cf5db595c2276e3f8ce7d01e898eb46a6e5c7edde35dfae4892b5`
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
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c02d58ebd6534d5afb5a8012d7003f978314b782a10cd19fbc0e6d5d58df3`  
		Last Modified: Tue, 17 Sep 2024 01:53:43 GMT  
		Size: 243.3 MB (243275613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67640bc9b4d0c0923eccbc39ae739c9f734354b3f58be66b9058c61be83d80`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 2.6 MB (2592233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdfb807d76c75fa16e7bed3d97c1200cb7778b2234fd4ebd57a60a93314315`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 472.7 KB (472652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85279eeb6d37f668996f5ff7a095cb58a8da69f7b5342aa3d403225fa5067fe3`  
		Last Modified: Tue, 24 Sep 2024 23:03:36 GMT  
		Size: 333.1 MB (333084429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4acef3f8a5dd88b288877dc0be33fe60b3ba8bb210881b97b86d2992efdee`  
		Last Modified: Tue, 24 Sep 2024 23:03:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0290bf5f6d02b79e508551f6b9bb6150ea742423b4a858163741d02a5866b4`  
		Last Modified: Tue, 24 Sep 2024 23:03:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b377d5653f447bc74bbcc677bda6a7a9f578d9ce2ac9bfcf9c79e418110f0e`  
		Last Modified: Tue, 24 Sep 2024 23:03:28 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9e62e32aa9bbc89a37d970fe9bbdfa4a62e0462a82e622e4721b5950e2e23e`  
		Last Modified: Tue, 24 Sep 2024 23:03:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:ea87118dce6645d5bddc7f8e70b7da03e6aad5e32d3763b95327e4d35758f443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39380574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa640763a7e870cffcb562320ce6d69dab01acc22d43b97f72b6ad9740a2ef7e`

```dockerfile
```

-	Layers:
	-	`sha256:c2054b31c20d789430beef6d8f22d78bb9d67c19143b7e33e0fee1f9e046a0d8`  
		Last Modified: Tue, 24 Sep 2024 23:03:29 GMT  
		Size: 39.4 MB (39353643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dafeacaa96d2c3a28e5a23c07c22e07f2098f7e9f7cc65f6d86b46b99f1975a0`  
		Last Modified: Tue, 24 Sep 2024 23:03:27 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240924`

```console
$ docker pull odoo@sha256:36fd7197f1e97190dfda0c804c332e07f3c8d718d458ad5f3b2f8491ad157e25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20240924` - linux; amd64

```console
$ docker pull odoo@sha256:43bf24487392a69cbba4c78dd04f1e9256fe7ef1cc5fb9265ff88bcab71e1ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597423782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8e70aff2d8f640351cf4382eb68c37d89602eaaf8eac70918e3082dd3caef7`
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
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=amd64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdc2bdd6fe1c81c5e1707b1e1334d800515ad4bc509711fbe1aef16a0c9a831`  
		Last Modified: Tue, 24 Sep 2024 22:58:28 GMT  
		Size: 233.7 MB (233745742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ea0d7231036996ecd44fb0d2afa3be5c2ca836510334a2458436737d03285b`  
		Last Modified: Tue, 24 Sep 2024 22:58:22 GMT  
		Size: 2.3 MB (2315614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488b6736919b02c6166db8481dddd9338c7847c7390c8a4c4be44dce8e3fe245`  
		Last Modified: Tue, 24 Sep 2024 22:58:22 GMT  
		Size: 472.6 KB (472596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df24c0e1387ade27fbdd4115a5a16b0b15c3fd4ae2ef0e4e834d4a4b4523c680`  
		Last Modified: Tue, 24 Sep 2024 22:58:28 GMT  
		Size: 331.4 MB (331351704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19aa6718eccc1d1a631a4ed5d3a6c9cc93307971545e73599369ef37da710462`  
		Last Modified: Tue, 24 Sep 2024 22:58:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419db33196b10de8252def0cbb7948b9bc83ac6d9143da94612b4a91f23a08d8`  
		Last Modified: Tue, 24 Sep 2024 22:58:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e64c26094b509c32334d06e4c866a0f3cd20b9c0f8ca8a7236b1e8084f5046`  
		Last Modified: Tue, 24 Sep 2024 22:58:23 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc729e0bfa2ad2d5a1c2e9a84da058161d9657f0e1fe4653345dedf6a0c5e599`  
		Last Modified: Tue, 24 Sep 2024 22:58:24 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240924` - unknown; unknown

```console
$ docker pull odoo@sha256:c494bd92bb2498df7190260b0c65622a124c49f942c40f4de9a73f2fe372e9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db0c0ab33d68c338648971b0dfa0f94bd68305a6fde6abae3e8fee3e0d45622`

```dockerfile
```

-	Layers:
	-	`sha256:bb2891f8c40e573243d9bfa92f40dac81903511686f16b7e2eb7f79e9a940703`  
		Last Modified: Tue, 24 Sep 2024 22:58:22 GMT  
		Size: 26.7 KB (26656 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240924` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ffdbdca71129cf26b9332d5aab8adcc0dd6a3df53030b3d5e9c671a3baca7eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.2 MB (592228945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3381e386582d9f118364fd5cbb273252151047be52fdec656ef0735c81822ef5`
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
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=arm64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6fadc8f1cdeb7018f3cc730bf5ca5cbd765df35c38756be1faa743e1786be9`  
		Last Modified: Tue, 17 Sep 2024 02:44:10 GMT  
		Size: 231.1 MB (231120471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a152b990945175781adb341944cf665969d147ca436c8a7b53374779e6f6941`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 2.3 MB (2307685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb15fba7b3792bd150e5f11e817299c61abde876d36eedbebdebfe879e3a79`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 472.7 KB (472677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3e0e5ed62ec2c72e1edc53ea6fa430ceb9d16629968ed4b2a987bc0997607e`  
		Last Modified: Tue, 24 Sep 2024 23:00:00 GMT  
		Size: 331.0 MB (330967345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45bd37950bf3e2f394333d1b2f12e199c823b1cf624663fdf3e0008ea64d06`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c072e53319017d46fd0a3ce0eeadde2221f03d781f31f46d43949a5abb9b837`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0c39ddc8cd60fc7767ee5b3ac3bf4ca7c17bd05d3671630ca141c41012388`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa01ac8bff5efbb8bcd137a7acf218e2a92eb61c30e4c2a014a0d95bde21359`  
		Last Modified: Tue, 24 Sep 2024 22:59:49 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240924` - unknown; unknown

```console
$ docker pull odoo@sha256:632ab2ea43c64f5ae705ec41fea55529ed3aec7d136f0fa18e5f4d8377707e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39379031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60848d38ddaafbade57c6f27bd4fcc1c58354b8b8dc400bd9b632ee8ec4fe555`

```dockerfile
```

-	Layers:
	-	`sha256:2e77c8d020aa5ee9229eeb54f12a25ce956dc8e76e33cf3be05ed7e2d809157d`  
		Last Modified: Tue, 24 Sep 2024 22:59:50 GMT  
		Size: 39.4 MB (39351855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a5d13345f349814c0163989f4faac5fde231284994f73985c0bd6aff37a68d`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240924` - linux; ppc64le

```console
$ docker pull odoo@sha256:9e6fb0bc8932806e50cc81a21d4b79571dcc359380e51521f350b0bba558e765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.9 MB (613875614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d909497ffc1cf5db595c2276e3f8ce7d01e898eb46a6e5c7edde35dfae4892b5`
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
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c02d58ebd6534d5afb5a8012d7003f978314b782a10cd19fbc0e6d5d58df3`  
		Last Modified: Tue, 17 Sep 2024 01:53:43 GMT  
		Size: 243.3 MB (243275613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67640bc9b4d0c0923eccbc39ae739c9f734354b3f58be66b9058c61be83d80`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 2.6 MB (2592233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdfb807d76c75fa16e7bed3d97c1200cb7778b2234fd4ebd57a60a93314315`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 472.7 KB (472652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85279eeb6d37f668996f5ff7a095cb58a8da69f7b5342aa3d403225fa5067fe3`  
		Last Modified: Tue, 24 Sep 2024 23:03:36 GMT  
		Size: 333.1 MB (333084429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4acef3f8a5dd88b288877dc0be33fe60b3ba8bb210881b97b86d2992efdee`  
		Last Modified: Tue, 24 Sep 2024 23:03:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0290bf5f6d02b79e508551f6b9bb6150ea742423b4a858163741d02a5866b4`  
		Last Modified: Tue, 24 Sep 2024 23:03:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b377d5653f447bc74bbcc677bda6a7a9f578d9ce2ac9bfcf9c79e418110f0e`  
		Last Modified: Tue, 24 Sep 2024 23:03:28 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9e62e32aa9bbc89a37d970fe9bbdfa4a62e0462a82e622e4721b5950e2e23e`  
		Last Modified: Tue, 24 Sep 2024 23:03:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240924` - unknown; unknown

```console
$ docker pull odoo@sha256:ea87118dce6645d5bddc7f8e70b7da03e6aad5e32d3763b95327e4d35758f443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39380574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa640763a7e870cffcb562320ce6d69dab01acc22d43b97f72b6ad9740a2ef7e`

```dockerfile
```

-	Layers:
	-	`sha256:c2054b31c20d789430beef6d8f22d78bb9d67c19143b7e33e0fee1f9e046a0d8`  
		Last Modified: Tue, 24 Sep 2024 23:03:29 GMT  
		Size: 39.4 MB (39353643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dafeacaa96d2c3a28e5a23c07c22e07f2098f7e9f7cc65f6d86b46b99f1975a0`  
		Last Modified: Tue, 24 Sep 2024 23:03:27 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:36fd7197f1e97190dfda0c804c332e07f3c8d718d458ad5f3b2f8491ad157e25
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
$ docker pull odoo@sha256:43bf24487392a69cbba4c78dd04f1e9256fe7ef1cc5fb9265ff88bcab71e1ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597423782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8e70aff2d8f640351cf4382eb68c37d89602eaaf8eac70918e3082dd3caef7`
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
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=amd64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdc2bdd6fe1c81c5e1707b1e1334d800515ad4bc509711fbe1aef16a0c9a831`  
		Last Modified: Tue, 24 Sep 2024 22:58:28 GMT  
		Size: 233.7 MB (233745742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ea0d7231036996ecd44fb0d2afa3be5c2ca836510334a2458436737d03285b`  
		Last Modified: Tue, 24 Sep 2024 22:58:22 GMT  
		Size: 2.3 MB (2315614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488b6736919b02c6166db8481dddd9338c7847c7390c8a4c4be44dce8e3fe245`  
		Last Modified: Tue, 24 Sep 2024 22:58:22 GMT  
		Size: 472.6 KB (472596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df24c0e1387ade27fbdd4115a5a16b0b15c3fd4ae2ef0e4e834d4a4b4523c680`  
		Last Modified: Tue, 24 Sep 2024 22:58:28 GMT  
		Size: 331.4 MB (331351704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19aa6718eccc1d1a631a4ed5d3a6c9cc93307971545e73599369ef37da710462`  
		Last Modified: Tue, 24 Sep 2024 22:58:23 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419db33196b10de8252def0cbb7948b9bc83ac6d9143da94612b4a91f23a08d8`  
		Last Modified: Tue, 24 Sep 2024 22:58:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e64c26094b509c32334d06e4c866a0f3cd20b9c0f8ca8a7236b1e8084f5046`  
		Last Modified: Tue, 24 Sep 2024 22:58:23 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc729e0bfa2ad2d5a1c2e9a84da058161d9657f0e1fe4653345dedf6a0c5e599`  
		Last Modified: Tue, 24 Sep 2024 22:58:24 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c494bd92bb2498df7190260b0c65622a124c49f942c40f4de9a73f2fe372e9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db0c0ab33d68c338648971b0dfa0f94bd68305a6fde6abae3e8fee3e0d45622`

```dockerfile
```

-	Layers:
	-	`sha256:bb2891f8c40e573243d9bfa92f40dac81903511686f16b7e2eb7f79e9a940703`  
		Last Modified: Tue, 24 Sep 2024 22:58:22 GMT  
		Size: 26.7 KB (26656 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ffdbdca71129cf26b9332d5aab8adcc0dd6a3df53030b3d5e9c671a3baca7eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.2 MB (592228945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3381e386582d9f118364fd5cbb273252151047be52fdec656ef0735c81822ef5`
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
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=arm64
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6fadc8f1cdeb7018f3cc730bf5ca5cbd765df35c38756be1faa743e1786be9`  
		Last Modified: Tue, 17 Sep 2024 02:44:10 GMT  
		Size: 231.1 MB (231120471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a152b990945175781adb341944cf665969d147ca436c8a7b53374779e6f6941`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 2.3 MB (2307685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb15fba7b3792bd150e5f11e817299c61abde876d36eedbebdebfe879e3a79`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 472.7 KB (472677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3e0e5ed62ec2c72e1edc53ea6fa430ceb9d16629968ed4b2a987bc0997607e`  
		Last Modified: Tue, 24 Sep 2024 23:00:00 GMT  
		Size: 331.0 MB (330967345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e45bd37950bf3e2f394333d1b2f12e199c823b1cf624663fdf3e0008ea64d06`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c072e53319017d46fd0a3ce0eeadde2221f03d781f31f46d43949a5abb9b837`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0c39ddc8cd60fc7767ee5b3ac3bf4ca7c17bd05d3671630ca141c41012388`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa01ac8bff5efbb8bcd137a7acf218e2a92eb61c30e4c2a014a0d95bde21359`  
		Last Modified: Tue, 24 Sep 2024 22:59:49 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:632ab2ea43c64f5ae705ec41fea55529ed3aec7d136f0fa18e5f4d8377707e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39379031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60848d38ddaafbade57c6f27bd4fcc1c58354b8b8dc400bd9b632ee8ec4fe555`

```dockerfile
```

-	Layers:
	-	`sha256:2e77c8d020aa5ee9229eeb54f12a25ce956dc8e76e33cf3be05ed7e2d809157d`  
		Last Modified: Tue, 24 Sep 2024 22:59:50 GMT  
		Size: 39.4 MB (39351855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1a5d13345f349814c0163989f4faac5fde231284994f73985c0bd6aff37a68d`  
		Last Modified: Tue, 24 Sep 2024 22:59:48 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:9e6fb0bc8932806e50cc81a21d4b79571dcc359380e51521f350b0bba558e765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.9 MB (613875614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d909497ffc1cf5db595c2276e3f8ce7d01e898eb46a6e5c7edde35dfae4892b5`
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
# Tue, 24 Sep 2024 07:24:50 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Sep 2024 07:24:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Sep 2024 07:24:50 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_RELEASE=20240924
# Tue, 24 Sep 2024 07:24:50 GMT
ARG ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240924 ODOO_SHA=f1b567f442ff645793235cdfaba5be9204ee8b55
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Sep 2024 07:24:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Sep 2024 07:24:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Sep 2024 07:24:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Sep 2024 07:24:50 GMT
USER odoo
# Tue, 24 Sep 2024 07:24:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Sep 2024 07:24:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c02d58ebd6534d5afb5a8012d7003f978314b782a10cd19fbc0e6d5d58df3`  
		Last Modified: Tue, 17 Sep 2024 01:53:43 GMT  
		Size: 243.3 MB (243275613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67640bc9b4d0c0923eccbc39ae739c9f734354b3f58be66b9058c61be83d80`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 2.6 MB (2592233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdfb807d76c75fa16e7bed3d97c1200cb7778b2234fd4ebd57a60a93314315`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 472.7 KB (472652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85279eeb6d37f668996f5ff7a095cb58a8da69f7b5342aa3d403225fa5067fe3`  
		Last Modified: Tue, 24 Sep 2024 23:03:36 GMT  
		Size: 333.1 MB (333084429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4acef3f8a5dd88b288877dc0be33fe60b3ba8bb210881b97b86d2992efdee`  
		Last Modified: Tue, 24 Sep 2024 23:03:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0290bf5f6d02b79e508551f6b9bb6150ea742423b4a858163741d02a5866b4`  
		Last Modified: Tue, 24 Sep 2024 23:03:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b377d5653f447bc74bbcc677bda6a7a9f578d9ce2ac9bfcf9c79e418110f0e`  
		Last Modified: Tue, 24 Sep 2024 23:03:28 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9e62e32aa9bbc89a37d970fe9bbdfa4a62e0462a82e622e4721b5950e2e23e`  
		Last Modified: Tue, 24 Sep 2024 23:03:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:ea87118dce6645d5bddc7f8e70b7da03e6aad5e32d3763b95327e4d35758f443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39380574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa640763a7e870cffcb562320ce6d69dab01acc22d43b97f72b6ad9740a2ef7e`

```dockerfile
```

-	Layers:
	-	`sha256:c2054b31c20d789430beef6d8f22d78bb9d67c19143b7e33e0fee1f9e046a0d8`  
		Last Modified: Tue, 24 Sep 2024 23:03:29 GMT  
		Size: 39.4 MB (39353643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dafeacaa96d2c3a28e5a23c07c22e07f2098f7e9f7cc65f6d86b46b99f1975a0`  
		Last Modified: Tue, 24 Sep 2024 23:03:27 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json
