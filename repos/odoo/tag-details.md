<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:15.0-20240904`](#odoo150-20240904)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20240904`](#odoo160-20240904)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20240904`](#odoo170-20240904)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:86e90d164dcb3566106199c5fc8f5ca45c0f37b3da1e914255b90759fa296c66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:661c20d17aa0ace79d11e213b6babbd4ebe64cfe300914bfbabb0f3fd3df2365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564274869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062a1ab3cb8d824e422c60c1a7628e9932cca43ba70372244327ae9989a518ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=C.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=15.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=2ce168169e2b949b155526c0f1f89b1df6c18a26
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: ODOO_RELEASE=20240904 ODOO_SHA=2ce168169e2b949b155526c0f1f89b1df6c18a26
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: ODOO_RELEASE=20240904 ODOO_SHA=2ce168169e2b949b155526c0f1f89b1df6c18a26
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9fdce535bc67eb118f8dbbbf2c044aeb084b655a907619b778a6aec0429881`  
		Last Modified: Wed, 04 Sep 2024 20:59:22 GMT  
		Size: 220.3 MB (220281547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a71889158794e48471d1468526147d397ddc8d362cefdbacbda42cdb5dc9837`  
		Last Modified: Wed, 04 Sep 2024 20:59:14 GMT  
		Size: 2.4 MB (2387815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2144d66ee7c86000407222fabc69765570669a9f2fad49affdb3ac7b9fb5be`  
		Last Modified: Wed, 04 Sep 2024 20:59:14 GMT  
		Size: 471.5 KB (471544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9018b7a4758346dd8e6df86ba434ba8b291bd3808aaa378a6beb2cfcec63e7b0`  
		Last Modified: Wed, 04 Sep 2024 20:59:22 GMT  
		Size: 309.7 MB (309703244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d337b536e7b96b4e036cd6b1f2005836d8bbb0e512f5a3c576c2f51e5ece4cf`  
		Last Modified: Wed, 04 Sep 2024 20:59:15 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072f2c0dbb5a9fb6b00515d06a78baf058d5ac600d72d34057ca7b9c356c9319`  
		Last Modified: Wed, 04 Sep 2024 20:59:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989d35f2bce16286c4c930b28e85067f396ffa232ba36ae36eba448008a9815`  
		Last Modified: Wed, 04 Sep 2024 20:59:16 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444393cfe76cd1590c6c0e3f0d00e193664bd07e7bf0e98205b2e52f4a17e5f8`  
		Last Modified: Wed, 04 Sep 2024 20:59:16 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15` - unknown; unknown

```console
$ docker pull odoo@sha256:8b8173d6c1528e715aa9b946877df1336d8c0c894b9968d45eae1e579c2e46f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34710991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df23eafe8dc1a2b1e132ff70b295f1bc129894a9063fd388cb27d21c69f5c123`

```dockerfile
```

-	Layers:
	-	`sha256:b44cf4d4db908b8251d8449c419908a67a59005d5836613e1cd152afc4a54165`  
		Last Modified: Wed, 04 Sep 2024 20:59:15 GMT  
		Size: 34.7 MB (34686361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17343b81e7651ae1370e01d95a1dd788cfd121b342b84900c436103cce4c4ada`  
		Last Modified: Wed, 04 Sep 2024 20:59:14 GMT  
		Size: 24.6 KB (24630 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0`

```console
$ docker pull odoo@sha256:86e90d164dcb3566106199c5fc8f5ca45c0f37b3da1e914255b90759fa296c66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:661c20d17aa0ace79d11e213b6babbd4ebe64cfe300914bfbabb0f3fd3df2365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564274869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062a1ab3cb8d824e422c60c1a7628e9932cca43ba70372244327ae9989a518ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=C.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=15.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=2ce168169e2b949b155526c0f1f89b1df6c18a26
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: ODOO_RELEASE=20240904 ODOO_SHA=2ce168169e2b949b155526c0f1f89b1df6c18a26
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: ODOO_RELEASE=20240904 ODOO_SHA=2ce168169e2b949b155526c0f1f89b1df6c18a26
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9fdce535bc67eb118f8dbbbf2c044aeb084b655a907619b778a6aec0429881`  
		Last Modified: Wed, 04 Sep 2024 20:59:22 GMT  
		Size: 220.3 MB (220281547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a71889158794e48471d1468526147d397ddc8d362cefdbacbda42cdb5dc9837`  
		Last Modified: Wed, 04 Sep 2024 20:59:14 GMT  
		Size: 2.4 MB (2387815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2144d66ee7c86000407222fabc69765570669a9f2fad49affdb3ac7b9fb5be`  
		Last Modified: Wed, 04 Sep 2024 20:59:14 GMT  
		Size: 471.5 KB (471544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9018b7a4758346dd8e6df86ba434ba8b291bd3808aaa378a6beb2cfcec63e7b0`  
		Last Modified: Wed, 04 Sep 2024 20:59:22 GMT  
		Size: 309.7 MB (309703244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d337b536e7b96b4e036cd6b1f2005836d8bbb0e512f5a3c576c2f51e5ece4cf`  
		Last Modified: Wed, 04 Sep 2024 20:59:15 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072f2c0dbb5a9fb6b00515d06a78baf058d5ac600d72d34057ca7b9c356c9319`  
		Last Modified: Wed, 04 Sep 2024 20:59:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989d35f2bce16286c4c930b28e85067f396ffa232ba36ae36eba448008a9815`  
		Last Modified: Wed, 04 Sep 2024 20:59:16 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444393cfe76cd1590c6c0e3f0d00e193664bd07e7bf0e98205b2e52f4a17e5f8`  
		Last Modified: Wed, 04 Sep 2024 20:59:16 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0` - unknown; unknown

```console
$ docker pull odoo@sha256:8b8173d6c1528e715aa9b946877df1336d8c0c894b9968d45eae1e579c2e46f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34710991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df23eafe8dc1a2b1e132ff70b295f1bc129894a9063fd388cb27d21c69f5c123`

```dockerfile
```

-	Layers:
	-	`sha256:b44cf4d4db908b8251d8449c419908a67a59005d5836613e1cd152afc4a54165`  
		Last Modified: Wed, 04 Sep 2024 20:59:15 GMT  
		Size: 34.7 MB (34686361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17343b81e7651ae1370e01d95a1dd788cfd121b342b84900c436103cce4c4ada`  
		Last Modified: Wed, 04 Sep 2024 20:59:14 GMT  
		Size: 24.6 KB (24630 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0-20240904`

```console
$ docker pull odoo@sha256:86e90d164dcb3566106199c5fc8f5ca45c0f37b3da1e914255b90759fa296c66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0-20240904` - linux; amd64

```console
$ docker pull odoo@sha256:661c20d17aa0ace79d11e213b6babbd4ebe64cfe300914bfbabb0f3fd3df2365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564274869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062a1ab3cb8d824e422c60c1a7628e9932cca43ba70372244327ae9989a518ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=C.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=15.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=2ce168169e2b949b155526c0f1f89b1df6c18a26
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: ODOO_RELEASE=20240904 ODOO_SHA=2ce168169e2b949b155526c0f1f89b1df6c18a26
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: ODOO_RELEASE=20240904 ODOO_SHA=2ce168169e2b949b155526c0f1f89b1df6c18a26
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9fdce535bc67eb118f8dbbbf2c044aeb084b655a907619b778a6aec0429881`  
		Last Modified: Wed, 04 Sep 2024 20:59:22 GMT  
		Size: 220.3 MB (220281547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a71889158794e48471d1468526147d397ddc8d362cefdbacbda42cdb5dc9837`  
		Last Modified: Wed, 04 Sep 2024 20:59:14 GMT  
		Size: 2.4 MB (2387815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2144d66ee7c86000407222fabc69765570669a9f2fad49affdb3ac7b9fb5be`  
		Last Modified: Wed, 04 Sep 2024 20:59:14 GMT  
		Size: 471.5 KB (471544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9018b7a4758346dd8e6df86ba434ba8b291bd3808aaa378a6beb2cfcec63e7b0`  
		Last Modified: Wed, 04 Sep 2024 20:59:22 GMT  
		Size: 309.7 MB (309703244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d337b536e7b96b4e036cd6b1f2005836d8bbb0e512f5a3c576c2f51e5ece4cf`  
		Last Modified: Wed, 04 Sep 2024 20:59:15 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072f2c0dbb5a9fb6b00515d06a78baf058d5ac600d72d34057ca7b9c356c9319`  
		Last Modified: Wed, 04 Sep 2024 20:59:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989d35f2bce16286c4c930b28e85067f396ffa232ba36ae36eba448008a9815`  
		Last Modified: Wed, 04 Sep 2024 20:59:16 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444393cfe76cd1590c6c0e3f0d00e193664bd07e7bf0e98205b2e52f4a17e5f8`  
		Last Modified: Wed, 04 Sep 2024 20:59:16 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0-20240904` - unknown; unknown

```console
$ docker pull odoo@sha256:8b8173d6c1528e715aa9b946877df1336d8c0c894b9968d45eae1e579c2e46f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34710991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df23eafe8dc1a2b1e132ff70b295f1bc129894a9063fd388cb27d21c69f5c123`

```dockerfile
```

-	Layers:
	-	`sha256:b44cf4d4db908b8251d8449c419908a67a59005d5836613e1cd152afc4a54165`  
		Last Modified: Wed, 04 Sep 2024 20:59:15 GMT  
		Size: 34.7 MB (34686361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17343b81e7651ae1370e01d95a1dd788cfd121b342b84900c436103cce4c4ada`  
		Last Modified: Wed, 04 Sep 2024 20:59:14 GMT  
		Size: 24.6 KB (24630 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16`

```console
$ docker pull odoo@sha256:6962d391c0fdd475f00a266c55fbab4934ce4873ba2c33846c65b4b44e3944b9
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
$ docker pull odoo@sha256:1fb477b67590d8706ac48a8213a977a113654e28b69d48ed9966eebe6e336ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.1 MB (584063931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397ffc6a0a1e10e0dac00c775a1fb379d2606c021eb9cc3c81688ca19b77c15a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=C.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=amd64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=16.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c943df1b98560e21bcf19167350260a8b5f65f27290659cf1e28d3e833e6b5`  
		Last Modified: Wed, 04 Sep 2024 20:59:14 GMT  
		Size: 219.6 MB (219595179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ccf99ef02f9d079bf9f05c4926ef6d0b25bded731743b75e64d7d5aae6d3f4`  
		Last Modified: Wed, 04 Sep 2024 20:59:11 GMT  
		Size: 2.4 MB (2391490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc43533ef519aed6e394651f73659bee9dcd10291b7f357fea2a884a3e72ab51`  
		Last Modified: Wed, 04 Sep 2024 20:59:11 GMT  
		Size: 471.5 KB (471488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c03fcfe7692907fbdf326cdaf7bc7c445118dea14263bb461bac57df573084a`  
		Last Modified: Wed, 04 Sep 2024 20:59:16 GMT  
		Size: 330.2 MB (330175052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41d8a814bb33fd91fd6e843dd6d73ce19b9d0b4bb173551307df5a2a3f0d813`  
		Last Modified: Wed, 04 Sep 2024 20:59:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c159c6c2cbb2320efa18860700eda73ad9bfeb15c399d555c705c118267ab2a`  
		Last Modified: Wed, 04 Sep 2024 20:59:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93781abee0dda1e07b73beab9e67f942e4219d12fa2818389c014efd43a87fc`  
		Last Modified: Wed, 04 Sep 2024 20:59:13 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41297fce6eba5ec723987898a77a754d847ca18a5adb5b49bf2df6d4ce9b0fd8`  
		Last Modified: Wed, 04 Sep 2024 20:59:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:75f3e9ca19d3a1ae376bf5ff145f67671b080c70431407338ae1ee5540fec6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38758527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f512a6891038766655666300d1085cfbc56a4bf05b9e49a6a7b5e477f64f18`

```dockerfile
```

-	Layers:
	-	`sha256:c85bf4ee68dca94dda69132f934af16cc4642fab88ffb73ffae5e4e3644bfbee`  
		Last Modified: Wed, 04 Sep 2024 20:59:12 GMT  
		Size: 38.7 MB (38731985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a425ce432dacaa16c0d1195dec1dc5cf68756f499c4f96616fe5c8040feb56e2`  
		Last Modified: Wed, 04 Sep 2024 20:59:11 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f0425fb7e4a817709f027014d6c97df5b0dc70245b7d0bc2f036d30c56e48e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.7 MB (579675699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88622576ddc6e97cddfad97aa7a66ff8a61f2e6c2683d5970f0908625faaab2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:06 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 13 Aug 2024 00:40:06 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=C.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=arm64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=16.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4916f0ae01714a20a0a5ff458b90344ffaaefc6345c7905aa37f82a43593a4`  
		Last Modified: Mon, 19 Aug 2024 18:05:16 GMT  
		Size: 216.9 MB (216902229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffdc4b7cedc1a31fafa7f7d54399d12b095bdebd5ad02fa63495ae04863b893`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 2.4 MB (2394016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b92a7253330c959ed65950618df7f6853cbcd2c9d050c3f4bfd4171fc5755f`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 463.8 KB (463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cd6c547cb1f092bc19cc4943e92061338bd5a1dcd202860fcb2e1aeb448ca5`  
		Last Modified: Wed, 04 Sep 2024 21:03:04 GMT  
		Size: 329.8 MB (329837133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a9e88ca688f0d7e415a1fd1384d9cf3328b6823b32c30dbf17df4cd4a3da1c`  
		Last Modified: Wed, 04 Sep 2024 21:02:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d641128a2c0b14dfb34875a2ae388872867a593b5391b4ac046f9377128e4a`  
		Last Modified: Wed, 04 Sep 2024 21:02:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b087e11637c25d3aeadab2069e6dbf3f58fe078d19ea6aaf85ee3d2d1f2cd2`  
		Last Modified: Wed, 04 Sep 2024 21:02:57 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1218f7fbf4a2a064ef75f4ba3a87feecfb11a2254f433310450852bafc17e477`  
		Last Modified: Wed, 04 Sep 2024 21:02:58 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:156a1eb873a4aba9a81b3afd2bab2e64bc446c241a771f0977c789bd60b00309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38765296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9b579b289a686d35a74ffcbf3afa8084abb0cbca05e1ef0a09edacb31a887d`

```dockerfile
```

-	Layers:
	-	`sha256:4b68d752cdcc4c85a94355ad3aa178d2753e882321a38b484479adb3631fb58f`  
		Last Modified: Wed, 04 Sep 2024 21:02:58 GMT  
		Size: 38.7 MB (38738457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3830e0ef19360f9185e1f0bd18a240fcc4a7b7f4bd1ce745c63ce8b1af867dd`  
		Last Modified: Wed, 04 Sep 2024 21:02:57 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:98a89be6f237ec4929abb9177118449a64955fd86a6316f0333baa039aea970c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.6 MB (598623551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43db5fb151a4c45aa6e65d4de8db25cb93effab85cee83630b08f89fb0fcd453`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:31 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Tue, 13 Aug 2024 00:22:33 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=C.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=ppc64le
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=16.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473977bf1d2bc93688151522365af64276b55d1bd7ed26f1f54dce620240eae5`  
		Last Modified: Mon, 19 Aug 2024 18:11:08 GMT  
		Size: 228.6 MB (228589663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866217a2e7bca4e7ecb960007dfb531409e7b88588617898dd9736a9784b083e`  
		Last Modified: Mon, 19 Aug 2024 18:10:58 GMT  
		Size: 2.6 MB (2634314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1361f8b87aa4ec2df887c300d21f906c8bcdb3c7a7635a5c69e3c002758856c`  
		Last Modified: Mon, 19 Aug 2024 18:10:57 GMT  
		Size: 463.9 KB (463862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb934fa221405b53dfdcf4b7fcd72150aed1d1e24ea53fa697c25aebd4bf05b2`  
		Last Modified: Wed, 04 Sep 2024 21:08:38 GMT  
		Size: 331.6 MB (331628146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91de557457bf0043965ba32c42623c01b40ec138446f452b1f0ff6a0ee36db33`  
		Last Modified: Wed, 04 Sep 2024 21:08:29 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae57f05b3eb1472ec6bbc88621c1f327779ed11611d46c5ec88a3a73c37441b`  
		Last Modified: Wed, 04 Sep 2024 21:08:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681880eece036d2ae59251b72bf408b49401e899703534dc2b7d3d3a03c7db2e`  
		Last Modified: Wed, 04 Sep 2024 21:08:30 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f14b51eb144febc9e0718a647020ec4bb167f8d05a056ee1ea5faf23080ab28`  
		Last Modified: Wed, 04 Sep 2024 21:08:30 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:0b6e08545108970d5e3d44f0719f432b97f3869f2c9b21f603a1f1a8b0476deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38766709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1364bee2ace086d22d70fd31a3f445ca4a68c3b1df8371f3854a6b7618bcc8`

```dockerfile
```

-	Layers:
	-	`sha256:618155a0b090f355daf08d2f7e2c0780b9187e2f4e02a281b576356a4b5cde1a`  
		Last Modified: Wed, 04 Sep 2024 21:08:31 GMT  
		Size: 38.7 MB (38740117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86deac5c39e29c12c93596eb2cce859ab136469f976b9b27db46b48b84660fc`  
		Last Modified: Wed, 04 Sep 2024 21:08:29 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:6962d391c0fdd475f00a266c55fbab4934ce4873ba2c33846c65b4b44e3944b9
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
$ docker pull odoo@sha256:1fb477b67590d8706ac48a8213a977a113654e28b69d48ed9966eebe6e336ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.1 MB (584063931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397ffc6a0a1e10e0dac00c775a1fb379d2606c021eb9cc3c81688ca19b77c15a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=C.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=amd64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=16.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c943df1b98560e21bcf19167350260a8b5f65f27290659cf1e28d3e833e6b5`  
		Last Modified: Wed, 04 Sep 2024 20:59:14 GMT  
		Size: 219.6 MB (219595179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ccf99ef02f9d079bf9f05c4926ef6d0b25bded731743b75e64d7d5aae6d3f4`  
		Last Modified: Wed, 04 Sep 2024 20:59:11 GMT  
		Size: 2.4 MB (2391490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc43533ef519aed6e394651f73659bee9dcd10291b7f357fea2a884a3e72ab51`  
		Last Modified: Wed, 04 Sep 2024 20:59:11 GMT  
		Size: 471.5 KB (471488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c03fcfe7692907fbdf326cdaf7bc7c445118dea14263bb461bac57df573084a`  
		Last Modified: Wed, 04 Sep 2024 20:59:16 GMT  
		Size: 330.2 MB (330175052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41d8a814bb33fd91fd6e843dd6d73ce19b9d0b4bb173551307df5a2a3f0d813`  
		Last Modified: Wed, 04 Sep 2024 20:59:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c159c6c2cbb2320efa18860700eda73ad9bfeb15c399d555c705c118267ab2a`  
		Last Modified: Wed, 04 Sep 2024 20:59:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93781abee0dda1e07b73beab9e67f942e4219d12fa2818389c014efd43a87fc`  
		Last Modified: Wed, 04 Sep 2024 20:59:13 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41297fce6eba5ec723987898a77a754d847ca18a5adb5b49bf2df6d4ce9b0fd8`  
		Last Modified: Wed, 04 Sep 2024 20:59:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:75f3e9ca19d3a1ae376bf5ff145f67671b080c70431407338ae1ee5540fec6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38758527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f512a6891038766655666300d1085cfbc56a4bf05b9e49a6a7b5e477f64f18`

```dockerfile
```

-	Layers:
	-	`sha256:c85bf4ee68dca94dda69132f934af16cc4642fab88ffb73ffae5e4e3644bfbee`  
		Last Modified: Wed, 04 Sep 2024 20:59:12 GMT  
		Size: 38.7 MB (38731985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a425ce432dacaa16c0d1195dec1dc5cf68756f499c4f96616fe5c8040feb56e2`  
		Last Modified: Wed, 04 Sep 2024 20:59:11 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f0425fb7e4a817709f027014d6c97df5b0dc70245b7d0bc2f036d30c56e48e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.7 MB (579675699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88622576ddc6e97cddfad97aa7a66ff8a61f2e6c2683d5970f0908625faaab2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:06 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 13 Aug 2024 00:40:06 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=C.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=arm64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=16.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4916f0ae01714a20a0a5ff458b90344ffaaefc6345c7905aa37f82a43593a4`  
		Last Modified: Mon, 19 Aug 2024 18:05:16 GMT  
		Size: 216.9 MB (216902229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffdc4b7cedc1a31fafa7f7d54399d12b095bdebd5ad02fa63495ae04863b893`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 2.4 MB (2394016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b92a7253330c959ed65950618df7f6853cbcd2c9d050c3f4bfd4171fc5755f`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 463.8 KB (463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cd6c547cb1f092bc19cc4943e92061338bd5a1dcd202860fcb2e1aeb448ca5`  
		Last Modified: Wed, 04 Sep 2024 21:03:04 GMT  
		Size: 329.8 MB (329837133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a9e88ca688f0d7e415a1fd1384d9cf3328b6823b32c30dbf17df4cd4a3da1c`  
		Last Modified: Wed, 04 Sep 2024 21:02:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d641128a2c0b14dfb34875a2ae388872867a593b5391b4ac046f9377128e4a`  
		Last Modified: Wed, 04 Sep 2024 21:02:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b087e11637c25d3aeadab2069e6dbf3f58fe078d19ea6aaf85ee3d2d1f2cd2`  
		Last Modified: Wed, 04 Sep 2024 21:02:57 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1218f7fbf4a2a064ef75f4ba3a87feecfb11a2254f433310450852bafc17e477`  
		Last Modified: Wed, 04 Sep 2024 21:02:58 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:156a1eb873a4aba9a81b3afd2bab2e64bc446c241a771f0977c789bd60b00309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38765296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9b579b289a686d35a74ffcbf3afa8084abb0cbca05e1ef0a09edacb31a887d`

```dockerfile
```

-	Layers:
	-	`sha256:4b68d752cdcc4c85a94355ad3aa178d2753e882321a38b484479adb3631fb58f`  
		Last Modified: Wed, 04 Sep 2024 21:02:58 GMT  
		Size: 38.7 MB (38738457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3830e0ef19360f9185e1f0bd18a240fcc4a7b7f4bd1ce745c63ce8b1af867dd`  
		Last Modified: Wed, 04 Sep 2024 21:02:57 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:98a89be6f237ec4929abb9177118449a64955fd86a6316f0333baa039aea970c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.6 MB (598623551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43db5fb151a4c45aa6e65d4de8db25cb93effab85cee83630b08f89fb0fcd453`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:31 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Tue, 13 Aug 2024 00:22:33 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=C.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=ppc64le
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=16.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473977bf1d2bc93688151522365af64276b55d1bd7ed26f1f54dce620240eae5`  
		Last Modified: Mon, 19 Aug 2024 18:11:08 GMT  
		Size: 228.6 MB (228589663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866217a2e7bca4e7ecb960007dfb531409e7b88588617898dd9736a9784b083e`  
		Last Modified: Mon, 19 Aug 2024 18:10:58 GMT  
		Size: 2.6 MB (2634314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1361f8b87aa4ec2df887c300d21f906c8bcdb3c7a7635a5c69e3c002758856c`  
		Last Modified: Mon, 19 Aug 2024 18:10:57 GMT  
		Size: 463.9 KB (463862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb934fa221405b53dfdcf4b7fcd72150aed1d1e24ea53fa697c25aebd4bf05b2`  
		Last Modified: Wed, 04 Sep 2024 21:08:38 GMT  
		Size: 331.6 MB (331628146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91de557457bf0043965ba32c42623c01b40ec138446f452b1f0ff6a0ee36db33`  
		Last Modified: Wed, 04 Sep 2024 21:08:29 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae57f05b3eb1472ec6bbc88621c1f327779ed11611d46c5ec88a3a73c37441b`  
		Last Modified: Wed, 04 Sep 2024 21:08:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681880eece036d2ae59251b72bf408b49401e899703534dc2b7d3d3a03c7db2e`  
		Last Modified: Wed, 04 Sep 2024 21:08:30 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f14b51eb144febc9e0718a647020ec4bb167f8d05a056ee1ea5faf23080ab28`  
		Last Modified: Wed, 04 Sep 2024 21:08:30 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0b6e08545108970d5e3d44f0719f432b97f3869f2c9b21f603a1f1a8b0476deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38766709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1364bee2ace086d22d70fd31a3f445ca4a68c3b1df8371f3854a6b7618bcc8`

```dockerfile
```

-	Layers:
	-	`sha256:618155a0b090f355daf08d2f7e2c0780b9187e2f4e02a281b576356a4b5cde1a`  
		Last Modified: Wed, 04 Sep 2024 21:08:31 GMT  
		Size: 38.7 MB (38740117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86deac5c39e29c12c93596eb2cce859ab136469f976b9b27db46b48b84660fc`  
		Last Modified: Wed, 04 Sep 2024 21:08:29 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20240904`

```console
$ docker pull odoo@sha256:6962d391c0fdd475f00a266c55fbab4934ce4873ba2c33846c65b4b44e3944b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0-20240904` - linux; amd64

```console
$ docker pull odoo@sha256:1fb477b67590d8706ac48a8213a977a113654e28b69d48ed9966eebe6e336ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.1 MB (584063931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397ffc6a0a1e10e0dac00c775a1fb379d2606c021eb9cc3c81688ca19b77c15a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=C.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=amd64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=16.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c943df1b98560e21bcf19167350260a8b5f65f27290659cf1e28d3e833e6b5`  
		Last Modified: Wed, 04 Sep 2024 20:59:14 GMT  
		Size: 219.6 MB (219595179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ccf99ef02f9d079bf9f05c4926ef6d0b25bded731743b75e64d7d5aae6d3f4`  
		Last Modified: Wed, 04 Sep 2024 20:59:11 GMT  
		Size: 2.4 MB (2391490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc43533ef519aed6e394651f73659bee9dcd10291b7f357fea2a884a3e72ab51`  
		Last Modified: Wed, 04 Sep 2024 20:59:11 GMT  
		Size: 471.5 KB (471488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c03fcfe7692907fbdf326cdaf7bc7c445118dea14263bb461bac57df573084a`  
		Last Modified: Wed, 04 Sep 2024 20:59:16 GMT  
		Size: 330.2 MB (330175052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41d8a814bb33fd91fd6e843dd6d73ce19b9d0b4bb173551307df5a2a3f0d813`  
		Last Modified: Wed, 04 Sep 2024 20:59:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c159c6c2cbb2320efa18860700eda73ad9bfeb15c399d555c705c118267ab2a`  
		Last Modified: Wed, 04 Sep 2024 20:59:12 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93781abee0dda1e07b73beab9e67f942e4219d12fa2818389c014efd43a87fc`  
		Last Modified: Wed, 04 Sep 2024 20:59:13 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41297fce6eba5ec723987898a77a754d847ca18a5adb5b49bf2df6d4ce9b0fd8`  
		Last Modified: Wed, 04 Sep 2024 20:59:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240904` - unknown; unknown

```console
$ docker pull odoo@sha256:75f3e9ca19d3a1ae376bf5ff145f67671b080c70431407338ae1ee5540fec6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38758527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f512a6891038766655666300d1085cfbc56a4bf05b9e49a6a7b5e477f64f18`

```dockerfile
```

-	Layers:
	-	`sha256:c85bf4ee68dca94dda69132f934af16cc4642fab88ffb73ffae5e4e3644bfbee`  
		Last Modified: Wed, 04 Sep 2024 20:59:12 GMT  
		Size: 38.7 MB (38731985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a425ce432dacaa16c0d1195dec1dc5cf68756f499c4f96616fe5c8040feb56e2`  
		Last Modified: Wed, 04 Sep 2024 20:59:11 GMT  
		Size: 26.5 KB (26542 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240904` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f0425fb7e4a817709f027014d6c97df5b0dc70245b7d0bc2f036d30c56e48e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.7 MB (579675699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88622576ddc6e97cddfad97aa7a66ff8a61f2e6c2683d5970f0908625faaab2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:06 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 13 Aug 2024 00:40:06 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=C.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=arm64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=16.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4916f0ae01714a20a0a5ff458b90344ffaaefc6345c7905aa37f82a43593a4`  
		Last Modified: Mon, 19 Aug 2024 18:05:16 GMT  
		Size: 216.9 MB (216902229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffdc4b7cedc1a31fafa7f7d54399d12b095bdebd5ad02fa63495ae04863b893`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 2.4 MB (2394016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b92a7253330c959ed65950618df7f6853cbcd2c9d050c3f4bfd4171fc5755f`  
		Last Modified: Mon, 19 Aug 2024 18:05:12 GMT  
		Size: 463.8 KB (463801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cd6c547cb1f092bc19cc4943e92061338bd5a1dcd202860fcb2e1aeb448ca5`  
		Last Modified: Wed, 04 Sep 2024 21:03:04 GMT  
		Size: 329.8 MB (329837133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a9e88ca688f0d7e415a1fd1384d9cf3328b6823b32c30dbf17df4cd4a3da1c`  
		Last Modified: Wed, 04 Sep 2024 21:02:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d641128a2c0b14dfb34875a2ae388872867a593b5391b4ac046f9377128e4a`  
		Last Modified: Wed, 04 Sep 2024 21:02:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b087e11637c25d3aeadab2069e6dbf3f58fe078d19ea6aaf85ee3d2d1f2cd2`  
		Last Modified: Wed, 04 Sep 2024 21:02:57 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1218f7fbf4a2a064ef75f4ba3a87feecfb11a2254f433310450852bafc17e477`  
		Last Modified: Wed, 04 Sep 2024 21:02:58 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240904` - unknown; unknown

```console
$ docker pull odoo@sha256:156a1eb873a4aba9a81b3afd2bab2e64bc446c241a771f0977c789bd60b00309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38765296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d9b579b289a686d35a74ffcbf3afa8084abb0cbca05e1ef0a09edacb31a887d`

```dockerfile
```

-	Layers:
	-	`sha256:4b68d752cdcc4c85a94355ad3aa178d2753e882321a38b484479adb3631fb58f`  
		Last Modified: Wed, 04 Sep 2024 21:02:58 GMT  
		Size: 38.7 MB (38738457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3830e0ef19360f9185e1f0bd18a240fcc4a7b7f4bd1ce745c63ce8b1af867dd`  
		Last Modified: Wed, 04 Sep 2024 21:02:57 GMT  
		Size: 26.8 KB (26839 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240904` - linux; ppc64le

```console
$ docker pull odoo@sha256:98a89be6f237ec4929abb9177118449a64955fd86a6316f0333baa039aea970c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.6 MB (598623551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43db5fb151a4c45aa6e65d4de8db25cb93effab85cee83630b08f89fb0fcd453`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:31 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Tue, 13 Aug 2024 00:22:33 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=C.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=ppc64le
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=16.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9ff4c6b6b51287a202289ab6038fa506729042aa
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473977bf1d2bc93688151522365af64276b55d1bd7ed26f1f54dce620240eae5`  
		Last Modified: Mon, 19 Aug 2024 18:11:08 GMT  
		Size: 228.6 MB (228589663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866217a2e7bca4e7ecb960007dfb531409e7b88588617898dd9736a9784b083e`  
		Last Modified: Mon, 19 Aug 2024 18:10:58 GMT  
		Size: 2.6 MB (2634314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1361f8b87aa4ec2df887c300d21f906c8bcdb3c7a7635a5c69e3c002758856c`  
		Last Modified: Mon, 19 Aug 2024 18:10:57 GMT  
		Size: 463.9 KB (463862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb934fa221405b53dfdcf4b7fcd72150aed1d1e24ea53fa697c25aebd4bf05b2`  
		Last Modified: Wed, 04 Sep 2024 21:08:38 GMT  
		Size: 331.6 MB (331628146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91de557457bf0043965ba32c42623c01b40ec138446f452b1f0ff6a0ee36db33`  
		Last Modified: Wed, 04 Sep 2024 21:08:29 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae57f05b3eb1472ec6bbc88621c1f327779ed11611d46c5ec88a3a73c37441b`  
		Last Modified: Wed, 04 Sep 2024 21:08:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681880eece036d2ae59251b72bf408b49401e899703534dc2b7d3d3a03c7db2e`  
		Last Modified: Wed, 04 Sep 2024 21:08:30 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f14b51eb144febc9e0718a647020ec4bb167f8d05a056ee1ea5faf23080ab28`  
		Last Modified: Wed, 04 Sep 2024 21:08:30 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240904` - unknown; unknown

```console
$ docker pull odoo@sha256:0b6e08545108970d5e3d44f0719f432b97f3869f2c9b21f603a1f1a8b0476deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38766709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1364bee2ace086d22d70fd31a3f445ca4a68c3b1df8371f3854a6b7618bcc8`

```dockerfile
```

-	Layers:
	-	`sha256:618155a0b090f355daf08d2f7e2c0780b9187e2f4e02a281b576356a4b5cde1a`  
		Last Modified: Wed, 04 Sep 2024 21:08:31 GMT  
		Size: 38.7 MB (38740117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86deac5c39e29c12c93596eb2cce859ab136469f976b9b27db46b48b84660fc`  
		Last Modified: Wed, 04 Sep 2024 21:08:29 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:1faaaea1131accd26aa4250b6d49a93164b01192cb824b4874a5c61fffd68856
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
$ docker pull odoo@sha256:39e714fa71c90e2da40a69c995f825fef07ea9514fd3cdcb68c2e70c03118ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.0 MB (599008711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1fdd45a39697cd62cc6b23a33675db209577f35e71f0e94b1c3dc62cb3b15b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=amd64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=17.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7829e421b21c58e5e528355dbc97c46b13deb6e1d4649107feae23b4b9ca1b`  
		Last Modified: Wed, 04 Sep 2024 21:01:16 GMT  
		Size: 236.0 MB (236022201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a943acc3d6cdef013117963d2fffd9f6fe6e32a4df183cf9bd43246050e85`  
		Last Modified: Wed, 04 Sep 2024 21:01:08 GMT  
		Size: 2.3 MB (2315875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e4151bc93d5bb6bb2dfaae9a6d08d9f953ffd0d8bd6a1a08276b270a939113`  
		Last Modified: Wed, 04 Sep 2024 21:01:08 GMT  
		Size: 472.6 KB (472573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c99f03a0a30b5d5723ea62d524ae0ffb8d2a04bcdcf5974204899601a2b656`  
		Last Modified: Wed, 04 Sep 2024 21:01:15 GMT  
		Size: 330.7 MB (330659595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1e22dc4e0a0e5b415b62ba13e0e8710554e3ab937099dcc6c18c417e791b93`  
		Last Modified: Wed, 04 Sep 2024 21:01:09 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4e911465628ceed81b75bd2b2b345d60d663bf0f54db99f41ad0413340228f`  
		Last Modified: Wed, 04 Sep 2024 21:01:09 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b736703071c38cbdb4545f0b68a35f666a4183700f419dcd3d9e11c5db4409`  
		Last Modified: Wed, 04 Sep 2024 21:01:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d386a22cdd1b08a379259da7b5d9040876f01f1735a63f9e58f89a57cf683dfc`  
		Last Modified: Wed, 04 Sep 2024 21:01:10 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:4489309ee6fabc734d1a5aa3a1b3a3ecd310795f07980ab6eb8f7965d4b9cecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39106829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a231bc5b512e1524a26a6e77e53d6ef4656341f53f9d4c36f2b42c72b675c1f6`

```dockerfile
```

-	Layers:
	-	`sha256:43810190538d2a55665c46f5dce819592c32dc193429b537acd8002c424ddd3f`  
		Last Modified: Wed, 04 Sep 2024 21:01:09 GMT  
		Size: 39.1 MB (39079954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:411380820652d051b8ef6e3f82a46b15285dac492e66af61201ea6b7e635a038`  
		Last Modified: Wed, 04 Sep 2024 21:01:07 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a4be4d3f57ab4b7bb6f9a21edd24f3b254154e1e54cd4affc70fa9507ed43eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.5 MB (591531876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dde0a8dad14feb2daa503b0f3798915250ba8ea1b261c43c87d601b67f7e55f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=arm64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=17.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a581f461c1fc23c9bf3611e1760531153dbb50f01c034b1498d291c26c8520`  
		Last Modified: Sat, 17 Aug 2024 03:34:41 GMT  
		Size: 231.1 MB (231116671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a3dc6c59fbe1745d030ced68224ef58f92023dc33fac4ff765aeebba99ff73`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 2.3 MB (2307689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94117e1eaca32fa3fce3e976dac34e3841e8fa793c3ddc5bf63d01b8342742bb`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 465.0 KB (465019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c87b7e22901613cee50972268352cee537124d3b1aff2c0e6f348fe1a3714b`  
		Last Modified: Wed, 04 Sep 2024 21:00:09 GMT  
		Size: 330.3 MB (330281377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381446fcd95ba28a24af30712aa305a488cc212a179e4ff4450937283c50e182`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0644e79bfd1a710e505a39ad44d1599f6f5667881b1bcd83b6dcaa9850efacfd`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e72aad7fc3edb9e77b143be70f2c107b7fe81f5d3da34b4d7ca6566d072e56`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c126cc25674d3f6eef98ca671f432091122aeb9b4f41159e990674e3a98fc911`  
		Last Modified: Wed, 04 Sep 2024 21:00:02 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:cb652c79a6296f3732274e2ba3feae52a2d88dda4674e6b8248bcaa5cffaf7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39113639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e95fcdce2bfc1cfc45a65b6ce48a4008aad3e2920bcc314808bd2e29571701`

```dockerfile
```

-	Layers:
	-	`sha256:3dac75a9ea97fc3830d4556b80bd776305470a1654aae16a2dd430ca9c6a2469`  
		Last Modified: Wed, 04 Sep 2024 21:00:03 GMT  
		Size: 39.1 MB (39086463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5950d3bf0abec72acd9a11057e1c115d43cec126031b64486928d54cd5f1431`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:2b8ea5dc935e9761c8eb3165cbba317d5542f2241218bdd163a6c533099cec95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 MB (613196980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc3a05127967f0cb801dd09eada9b233710f264dbc25211e3b20305f1748880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=ppc64le
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=17.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649917932e48ae9826c365816bb9ed493a267201a69d663f38dce89f38379d0b`  
		Last Modified: Sat, 17 Aug 2024 02:01:48 GMT  
		Size: 243.3 MB (243276312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4137abe0b20854df48c69fbcd577be8244ecbae68b833dded386e520f586a018`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 2.6 MB (2592374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2fa96facf5686ef0daba4666a3b8cf09d55e1e688fc8357e8fc048129db8f1`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 464.9 KB (464920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57927fec8194e52ff27dbf97e965525f96fd303c8cc2128431315913e96394f`  
		Last Modified: Wed, 04 Sep 2024 21:03:02 GMT  
		Size: 332.4 MB (332396751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aab0338399fe43f049ab3202c269f0cc0a03409cbcf3a73391a41d34448824c`  
		Last Modified: Wed, 04 Sep 2024 21:02:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2296d7d88e32ed72ff6b48466a9623ec321fd5b1dbfe8f1928352826b38ca285`  
		Last Modified: Wed, 04 Sep 2024 21:02:44 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a4f39d77da9fcc01066bd5643ebfd22234b089b8289822fdd7375c06f4e53d`  
		Last Modified: Wed, 04 Sep 2024 21:02:44 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a312cefa74744d6ccf8a31f4b651b1222c1c69608876a0cf2446bcf4db3ddc08`  
		Last Modified: Wed, 04 Sep 2024 21:02:45 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:497ccdfc9af3eae2f565c708fe0166fd67eaa069fe0727f6670dc49378026bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39115182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee7e040473d4f73a7ff545a2ebbd0d6910664fa82e55be8023ea98246a77da7`

```dockerfile
```

-	Layers:
	-	`sha256:0c16ee27ff1cecd4fe6993a22df7c2c555cfd3f4215d6022b5d2d540ee694d6e`  
		Last Modified: Wed, 04 Sep 2024 21:02:45 GMT  
		Size: 39.1 MB (39088251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2c48caeea65e8ea045783ee586c91304faf71f8ae8d2a6e86123810f2d82bc`  
		Last Modified: Wed, 04 Sep 2024 21:02:43 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:1faaaea1131accd26aa4250b6d49a93164b01192cb824b4874a5c61fffd68856
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
$ docker pull odoo@sha256:39e714fa71c90e2da40a69c995f825fef07ea9514fd3cdcb68c2e70c03118ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.0 MB (599008711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1fdd45a39697cd62cc6b23a33675db209577f35e71f0e94b1c3dc62cb3b15b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=amd64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=17.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7829e421b21c58e5e528355dbc97c46b13deb6e1d4649107feae23b4b9ca1b`  
		Last Modified: Wed, 04 Sep 2024 21:01:16 GMT  
		Size: 236.0 MB (236022201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a943acc3d6cdef013117963d2fffd9f6fe6e32a4df183cf9bd43246050e85`  
		Last Modified: Wed, 04 Sep 2024 21:01:08 GMT  
		Size: 2.3 MB (2315875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e4151bc93d5bb6bb2dfaae9a6d08d9f953ffd0d8bd6a1a08276b270a939113`  
		Last Modified: Wed, 04 Sep 2024 21:01:08 GMT  
		Size: 472.6 KB (472573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c99f03a0a30b5d5723ea62d524ae0ffb8d2a04bcdcf5974204899601a2b656`  
		Last Modified: Wed, 04 Sep 2024 21:01:15 GMT  
		Size: 330.7 MB (330659595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1e22dc4e0a0e5b415b62ba13e0e8710554e3ab937099dcc6c18c417e791b93`  
		Last Modified: Wed, 04 Sep 2024 21:01:09 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4e911465628ceed81b75bd2b2b345d60d663bf0f54db99f41ad0413340228f`  
		Last Modified: Wed, 04 Sep 2024 21:01:09 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b736703071c38cbdb4545f0b68a35f666a4183700f419dcd3d9e11c5db4409`  
		Last Modified: Wed, 04 Sep 2024 21:01:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d386a22cdd1b08a379259da7b5d9040876f01f1735a63f9e58f89a57cf683dfc`  
		Last Modified: Wed, 04 Sep 2024 21:01:10 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4489309ee6fabc734d1a5aa3a1b3a3ecd310795f07980ab6eb8f7965d4b9cecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39106829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a231bc5b512e1524a26a6e77e53d6ef4656341f53f9d4c36f2b42c72b675c1f6`

```dockerfile
```

-	Layers:
	-	`sha256:43810190538d2a55665c46f5dce819592c32dc193429b537acd8002c424ddd3f`  
		Last Modified: Wed, 04 Sep 2024 21:01:09 GMT  
		Size: 39.1 MB (39079954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:411380820652d051b8ef6e3f82a46b15285dac492e66af61201ea6b7e635a038`  
		Last Modified: Wed, 04 Sep 2024 21:01:07 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a4be4d3f57ab4b7bb6f9a21edd24f3b254154e1e54cd4affc70fa9507ed43eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.5 MB (591531876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dde0a8dad14feb2daa503b0f3798915250ba8ea1b261c43c87d601b67f7e55f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=arm64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=17.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a581f461c1fc23c9bf3611e1760531153dbb50f01c034b1498d291c26c8520`  
		Last Modified: Sat, 17 Aug 2024 03:34:41 GMT  
		Size: 231.1 MB (231116671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a3dc6c59fbe1745d030ced68224ef58f92023dc33fac4ff765aeebba99ff73`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 2.3 MB (2307689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94117e1eaca32fa3fce3e976dac34e3841e8fa793c3ddc5bf63d01b8342742bb`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 465.0 KB (465019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c87b7e22901613cee50972268352cee537124d3b1aff2c0e6f348fe1a3714b`  
		Last Modified: Wed, 04 Sep 2024 21:00:09 GMT  
		Size: 330.3 MB (330281377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381446fcd95ba28a24af30712aa305a488cc212a179e4ff4450937283c50e182`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0644e79bfd1a710e505a39ad44d1599f6f5667881b1bcd83b6dcaa9850efacfd`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e72aad7fc3edb9e77b143be70f2c107b7fe81f5d3da34b4d7ca6566d072e56`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c126cc25674d3f6eef98ca671f432091122aeb9b4f41159e990674e3a98fc911`  
		Last Modified: Wed, 04 Sep 2024 21:00:02 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cb652c79a6296f3732274e2ba3feae52a2d88dda4674e6b8248bcaa5cffaf7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39113639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e95fcdce2bfc1cfc45a65b6ce48a4008aad3e2920bcc314808bd2e29571701`

```dockerfile
```

-	Layers:
	-	`sha256:3dac75a9ea97fc3830d4556b80bd776305470a1654aae16a2dd430ca9c6a2469`  
		Last Modified: Wed, 04 Sep 2024 21:00:03 GMT  
		Size: 39.1 MB (39086463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5950d3bf0abec72acd9a11057e1c115d43cec126031b64486928d54cd5f1431`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:2b8ea5dc935e9761c8eb3165cbba317d5542f2241218bdd163a6c533099cec95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 MB (613196980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc3a05127967f0cb801dd09eada9b233710f264dbc25211e3b20305f1748880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=ppc64le
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=17.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649917932e48ae9826c365816bb9ed493a267201a69d663f38dce89f38379d0b`  
		Last Modified: Sat, 17 Aug 2024 02:01:48 GMT  
		Size: 243.3 MB (243276312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4137abe0b20854df48c69fbcd577be8244ecbae68b833dded386e520f586a018`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 2.6 MB (2592374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2fa96facf5686ef0daba4666a3b8cf09d55e1e688fc8357e8fc048129db8f1`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 464.9 KB (464920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57927fec8194e52ff27dbf97e965525f96fd303c8cc2128431315913e96394f`  
		Last Modified: Wed, 04 Sep 2024 21:03:02 GMT  
		Size: 332.4 MB (332396751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aab0338399fe43f049ab3202c269f0cc0a03409cbcf3a73391a41d34448824c`  
		Last Modified: Wed, 04 Sep 2024 21:02:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2296d7d88e32ed72ff6b48466a9623ec321fd5b1dbfe8f1928352826b38ca285`  
		Last Modified: Wed, 04 Sep 2024 21:02:44 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a4f39d77da9fcc01066bd5643ebfd22234b089b8289822fdd7375c06f4e53d`  
		Last Modified: Wed, 04 Sep 2024 21:02:44 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a312cefa74744d6ccf8a31f4b651b1222c1c69608876a0cf2446bcf4db3ddc08`  
		Last Modified: Wed, 04 Sep 2024 21:02:45 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:497ccdfc9af3eae2f565c708fe0166fd67eaa069fe0727f6670dc49378026bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39115182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee7e040473d4f73a7ff545a2ebbd0d6910664fa82e55be8023ea98246a77da7`

```dockerfile
```

-	Layers:
	-	`sha256:0c16ee27ff1cecd4fe6993a22df7c2c555cfd3f4215d6022b5d2d540ee694d6e`  
		Last Modified: Wed, 04 Sep 2024 21:02:45 GMT  
		Size: 39.1 MB (39088251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2c48caeea65e8ea045783ee586c91304faf71f8ae8d2a6e86123810f2d82bc`  
		Last Modified: Wed, 04 Sep 2024 21:02:43 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240904`

```console
$ docker pull odoo@sha256:1faaaea1131accd26aa4250b6d49a93164b01192cb824b4874a5c61fffd68856
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20240904` - linux; amd64

```console
$ docker pull odoo@sha256:39e714fa71c90e2da40a69c995f825fef07ea9514fd3cdcb68c2e70c03118ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.0 MB (599008711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1fdd45a39697cd62cc6b23a33675db209577f35e71f0e94b1c3dc62cb3b15b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=amd64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=17.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7829e421b21c58e5e528355dbc97c46b13deb6e1d4649107feae23b4b9ca1b`  
		Last Modified: Wed, 04 Sep 2024 21:01:16 GMT  
		Size: 236.0 MB (236022201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a943acc3d6cdef013117963d2fffd9f6fe6e32a4df183cf9bd43246050e85`  
		Last Modified: Wed, 04 Sep 2024 21:01:08 GMT  
		Size: 2.3 MB (2315875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e4151bc93d5bb6bb2dfaae9a6d08d9f953ffd0d8bd6a1a08276b270a939113`  
		Last Modified: Wed, 04 Sep 2024 21:01:08 GMT  
		Size: 472.6 KB (472573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c99f03a0a30b5d5723ea62d524ae0ffb8d2a04bcdcf5974204899601a2b656`  
		Last Modified: Wed, 04 Sep 2024 21:01:15 GMT  
		Size: 330.7 MB (330659595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1e22dc4e0a0e5b415b62ba13e0e8710554e3ab937099dcc6c18c417e791b93`  
		Last Modified: Wed, 04 Sep 2024 21:01:09 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4e911465628ceed81b75bd2b2b345d60d663bf0f54db99f41ad0413340228f`  
		Last Modified: Wed, 04 Sep 2024 21:01:09 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b736703071c38cbdb4545f0b68a35f666a4183700f419dcd3d9e11c5db4409`  
		Last Modified: Wed, 04 Sep 2024 21:01:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d386a22cdd1b08a379259da7b5d9040876f01f1735a63f9e58f89a57cf683dfc`  
		Last Modified: Wed, 04 Sep 2024 21:01:10 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240904` - unknown; unknown

```console
$ docker pull odoo@sha256:4489309ee6fabc734d1a5aa3a1b3a3ecd310795f07980ab6eb8f7965d4b9cecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39106829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a231bc5b512e1524a26a6e77e53d6ef4656341f53f9d4c36f2b42c72b675c1f6`

```dockerfile
```

-	Layers:
	-	`sha256:43810190538d2a55665c46f5dce819592c32dc193429b537acd8002c424ddd3f`  
		Last Modified: Wed, 04 Sep 2024 21:01:09 GMT  
		Size: 39.1 MB (39079954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:411380820652d051b8ef6e3f82a46b15285dac492e66af61201ea6b7e635a038`  
		Last Modified: Wed, 04 Sep 2024 21:01:07 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240904` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a4be4d3f57ab4b7bb6f9a21edd24f3b254154e1e54cd4affc70fa9507ed43eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.5 MB (591531876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dde0a8dad14feb2daa503b0f3798915250ba8ea1b261c43c87d601b67f7e55f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=arm64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=17.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a581f461c1fc23c9bf3611e1760531153dbb50f01c034b1498d291c26c8520`  
		Last Modified: Sat, 17 Aug 2024 03:34:41 GMT  
		Size: 231.1 MB (231116671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a3dc6c59fbe1745d030ced68224ef58f92023dc33fac4ff765aeebba99ff73`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 2.3 MB (2307689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94117e1eaca32fa3fce3e976dac34e3841e8fa793c3ddc5bf63d01b8342742bb`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 465.0 KB (465019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c87b7e22901613cee50972268352cee537124d3b1aff2c0e6f348fe1a3714b`  
		Last Modified: Wed, 04 Sep 2024 21:00:09 GMT  
		Size: 330.3 MB (330281377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381446fcd95ba28a24af30712aa305a488cc212a179e4ff4450937283c50e182`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0644e79bfd1a710e505a39ad44d1599f6f5667881b1bcd83b6dcaa9850efacfd`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e72aad7fc3edb9e77b143be70f2c107b7fe81f5d3da34b4d7ca6566d072e56`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c126cc25674d3f6eef98ca671f432091122aeb9b4f41159e990674e3a98fc911`  
		Last Modified: Wed, 04 Sep 2024 21:00:02 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240904` - unknown; unknown

```console
$ docker pull odoo@sha256:cb652c79a6296f3732274e2ba3feae52a2d88dda4674e6b8248bcaa5cffaf7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39113639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e95fcdce2bfc1cfc45a65b6ce48a4008aad3e2920bcc314808bd2e29571701`

```dockerfile
```

-	Layers:
	-	`sha256:3dac75a9ea97fc3830d4556b80bd776305470a1654aae16a2dd430ca9c6a2469`  
		Last Modified: Wed, 04 Sep 2024 21:00:03 GMT  
		Size: 39.1 MB (39086463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5950d3bf0abec72acd9a11057e1c115d43cec126031b64486928d54cd5f1431`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240904` - linux; ppc64le

```console
$ docker pull odoo@sha256:2b8ea5dc935e9761c8eb3165cbba317d5542f2241218bdd163a6c533099cec95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 MB (613196980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc3a05127967f0cb801dd09eada9b233710f264dbc25211e3b20305f1748880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=ppc64le
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=17.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649917932e48ae9826c365816bb9ed493a267201a69d663f38dce89f38379d0b`  
		Last Modified: Sat, 17 Aug 2024 02:01:48 GMT  
		Size: 243.3 MB (243276312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4137abe0b20854df48c69fbcd577be8244ecbae68b833dded386e520f586a018`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 2.6 MB (2592374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2fa96facf5686ef0daba4666a3b8cf09d55e1e688fc8357e8fc048129db8f1`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 464.9 KB (464920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57927fec8194e52ff27dbf97e965525f96fd303c8cc2128431315913e96394f`  
		Last Modified: Wed, 04 Sep 2024 21:03:02 GMT  
		Size: 332.4 MB (332396751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aab0338399fe43f049ab3202c269f0cc0a03409cbcf3a73391a41d34448824c`  
		Last Modified: Wed, 04 Sep 2024 21:02:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2296d7d88e32ed72ff6b48466a9623ec321fd5b1dbfe8f1928352826b38ca285`  
		Last Modified: Wed, 04 Sep 2024 21:02:44 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a4f39d77da9fcc01066bd5643ebfd22234b089b8289822fdd7375c06f4e53d`  
		Last Modified: Wed, 04 Sep 2024 21:02:44 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a312cefa74744d6ccf8a31f4b651b1222c1c69608876a0cf2446bcf4db3ddc08`  
		Last Modified: Wed, 04 Sep 2024 21:02:45 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240904` - unknown; unknown

```console
$ docker pull odoo@sha256:497ccdfc9af3eae2f565c708fe0166fd67eaa069fe0727f6670dc49378026bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39115182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee7e040473d4f73a7ff545a2ebbd0d6910664fa82e55be8023ea98246a77da7`

```dockerfile
```

-	Layers:
	-	`sha256:0c16ee27ff1cecd4fe6993a22df7c2c555cfd3f4215d6022b5d2d540ee694d6e`  
		Last Modified: Wed, 04 Sep 2024 21:02:45 GMT  
		Size: 39.1 MB (39088251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2c48caeea65e8ea045783ee586c91304faf71f8ae8d2a6e86123810f2d82bc`  
		Last Modified: Wed, 04 Sep 2024 21:02:43 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:1faaaea1131accd26aa4250b6d49a93164b01192cb824b4874a5c61fffd68856
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
$ docker pull odoo@sha256:39e714fa71c90e2da40a69c995f825fef07ea9514fd3cdcb68c2e70c03118ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.0 MB (599008711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1fdd45a39697cd62cc6b23a33675db209577f35e71f0e94b1c3dc62cb3b15b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
CMD ["/bin/bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=amd64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=17.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7829e421b21c58e5e528355dbc97c46b13deb6e1d4649107feae23b4b9ca1b`  
		Last Modified: Wed, 04 Sep 2024 21:01:16 GMT  
		Size: 236.0 MB (236022201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a943acc3d6cdef013117963d2fffd9f6fe6e32a4df183cf9bd43246050e85`  
		Last Modified: Wed, 04 Sep 2024 21:01:08 GMT  
		Size: 2.3 MB (2315875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e4151bc93d5bb6bb2dfaae9a6d08d9f953ffd0d8bd6a1a08276b270a939113`  
		Last Modified: Wed, 04 Sep 2024 21:01:08 GMT  
		Size: 472.6 KB (472573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c99f03a0a30b5d5723ea62d524ae0ffb8d2a04bcdcf5974204899601a2b656`  
		Last Modified: Wed, 04 Sep 2024 21:01:15 GMT  
		Size: 330.7 MB (330659595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1e22dc4e0a0e5b415b62ba13e0e8710554e3ab937099dcc6c18c417e791b93`  
		Last Modified: Wed, 04 Sep 2024 21:01:09 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4e911465628ceed81b75bd2b2b345d60d663bf0f54db99f41ad0413340228f`  
		Last Modified: Wed, 04 Sep 2024 21:01:09 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b736703071c38cbdb4545f0b68a35f666a4183700f419dcd3d9e11c5db4409`  
		Last Modified: Wed, 04 Sep 2024 21:01:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d386a22cdd1b08a379259da7b5d9040876f01f1735a63f9e58f89a57cf683dfc`  
		Last Modified: Wed, 04 Sep 2024 21:01:10 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:4489309ee6fabc734d1a5aa3a1b3a3ecd310795f07980ab6eb8f7965d4b9cecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39106829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a231bc5b512e1524a26a6e77e53d6ef4656341f53f9d4c36f2b42c72b675c1f6`

```dockerfile
```

-	Layers:
	-	`sha256:43810190538d2a55665c46f5dce819592c32dc193429b537acd8002c424ddd3f`  
		Last Modified: Wed, 04 Sep 2024 21:01:09 GMT  
		Size: 39.1 MB (39079954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:411380820652d051b8ef6e3f82a46b15285dac492e66af61201ea6b7e635a038`  
		Last Modified: Wed, 04 Sep 2024 21:01:07 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a4be4d3f57ab4b7bb6f9a21edd24f3b254154e1e54cd4affc70fa9507ed43eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.5 MB (591531876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dde0a8dad14feb2daa503b0f3798915250ba8ea1b261c43c87d601b67f7e55f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=arm64
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=17.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a581f461c1fc23c9bf3611e1760531153dbb50f01c034b1498d291c26c8520`  
		Last Modified: Sat, 17 Aug 2024 03:34:41 GMT  
		Size: 231.1 MB (231116671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a3dc6c59fbe1745d030ced68224ef58f92023dc33fac4ff765aeebba99ff73`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 2.3 MB (2307689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94117e1eaca32fa3fce3e976dac34e3841e8fa793c3ddc5bf63d01b8342742bb`  
		Last Modified: Sat, 17 Aug 2024 03:34:36 GMT  
		Size: 465.0 KB (465019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c87b7e22901613cee50972268352cee537124d3b1aff2c0e6f348fe1a3714b`  
		Last Modified: Wed, 04 Sep 2024 21:00:09 GMT  
		Size: 330.3 MB (330281377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381446fcd95ba28a24af30712aa305a488cc212a179e4ff4450937283c50e182`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0644e79bfd1a710e505a39ad44d1599f6f5667881b1bcd83b6dcaa9850efacfd`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e72aad7fc3edb9e77b143be70f2c107b7fe81f5d3da34b4d7ca6566d072e56`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c126cc25674d3f6eef98ca671f432091122aeb9b4f41159e990674e3a98fc911`  
		Last Modified: Wed, 04 Sep 2024 21:00:02 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:cb652c79a6296f3732274e2ba3feae52a2d88dda4674e6b8248bcaa5cffaf7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39113639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e95fcdce2bfc1cfc45a65b6ce48a4008aad3e2920bcc314808bd2e29571701`

```dockerfile
```

-	Layers:
	-	`sha256:3dac75a9ea97fc3830d4556b80bd776305470a1654aae16a2dd430ca9c6a2469`  
		Last Modified: Wed, 04 Sep 2024 21:00:03 GMT  
		Size: 39.1 MB (39086463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5950d3bf0abec72acd9a11057e1c115d43cec126031b64486928d54cd5f1431`  
		Last Modified: Wed, 04 Sep 2024 21:00:01 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:2b8ea5dc935e9761c8eb3165cbba317d5542f2241218bdd163a6c533099cec95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.2 MB (613196980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc3a05127967f0cb801dd09eada9b233710f264dbc25211e3b20305f1748880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
CMD ["/bin/bash"]
# Wed, 04 Sep 2024 09:14:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 04 Sep 2024 09:14:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV LANG=en_US.UTF-8
# Wed, 04 Sep 2024 09:14:36 GMT
ARG TARGETARCH=ppc64le
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_VERSION=17.0
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_RELEASE=20240904
# Wed, 04 Sep 2024 09:14:36 GMT
ARG ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240904 ODOO_SHA=9fd807d55facb850ead1ad86dc628e26961dfb20
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 04 Sep 2024 09:14:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 04 Sep 2024 09:14:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 04 Sep 2024 09:14:36 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 04 Sep 2024 09:14:36 GMT
USER odoo
# Wed, 04 Sep 2024 09:14:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 04 Sep 2024 09:14:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649917932e48ae9826c365816bb9ed493a267201a69d663f38dce89f38379d0b`  
		Last Modified: Sat, 17 Aug 2024 02:01:48 GMT  
		Size: 243.3 MB (243276312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4137abe0b20854df48c69fbcd577be8244ecbae68b833dded386e520f586a018`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 2.6 MB (2592374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2fa96facf5686ef0daba4666a3b8cf09d55e1e688fc8357e8fc048129db8f1`  
		Last Modified: Sat, 17 Aug 2024 02:01:42 GMT  
		Size: 464.9 KB (464920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57927fec8194e52ff27dbf97e965525f96fd303c8cc2128431315913e96394f`  
		Last Modified: Wed, 04 Sep 2024 21:03:02 GMT  
		Size: 332.4 MB (332396751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aab0338399fe43f049ab3202c269f0cc0a03409cbcf3a73391a41d34448824c`  
		Last Modified: Wed, 04 Sep 2024 21:02:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2296d7d88e32ed72ff6b48466a9623ec321fd5b1dbfe8f1928352826b38ca285`  
		Last Modified: Wed, 04 Sep 2024 21:02:44 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a4f39d77da9fcc01066bd5643ebfd22234b089b8289822fdd7375c06f4e53d`  
		Last Modified: Wed, 04 Sep 2024 21:02:44 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a312cefa74744d6ccf8a31f4b651b1222c1c69608876a0cf2446bcf4db3ddc08`  
		Last Modified: Wed, 04 Sep 2024 21:02:45 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:497ccdfc9af3eae2f565c708fe0166fd67eaa069fe0727f6670dc49378026bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39115182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee7e040473d4f73a7ff545a2ebbd0d6910664fa82e55be8023ea98246a77da7`

```dockerfile
```

-	Layers:
	-	`sha256:0c16ee27ff1cecd4fe6993a22df7c2c555cfd3f4215d6022b5d2d540ee694d6e`  
		Last Modified: Wed, 04 Sep 2024 21:02:45 GMT  
		Size: 39.1 MB (39088251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2c48caeea65e8ea045783ee586c91304faf71f8ae8d2a6e86123810f2d82bc`  
		Last Modified: Wed, 04 Sep 2024 21:02:43 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json
