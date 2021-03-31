## `odoo:latest`

```console
$ docker pull odoo@sha256:9709bf21e6efe94f3d1967ec760d27479cfaa2b6ef8f68a4a8b68b87b3f654af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:e875c60cdfb0e9fe64deceb15f47af81b8c65540e5da95b7b139594e9230881d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.8 MB (515761252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc7fca734f3957554da9532068db08fe17e5780cafb5cf8c87468c516640f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:08:36 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 27 Mar 2021 06:08:36 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 27 Mar 2021 06:08:36 GMT
ENV LANG=C.UTF-8
# Sat, 27 Mar 2021 06:09:55 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 27 Mar 2021 06:10:09 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:10:15 GMT
RUN npm install -g rtlcss
# Sat, 27 Mar 2021 06:10:15 GMT
ENV ODOO_VERSION=14.0
# Tue, 30 Mar 2021 20:31:09 GMT
ARG ODOO_RELEASE=20210330
# Tue, 30 Mar 2021 20:31:09 GMT
ARG ODOO_SHA=0a0ebf50846a5e5131a6725795c3fc59d511262d
# Tue, 30 Mar 2021 20:32:26 GMT
# ARGS: ODOO_RELEASE=20210330 ODOO_SHA=0a0ebf50846a5e5131a6725795c3fc59d511262d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 30 Mar 2021 20:32:28 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 30 Mar 2021 20:32:28 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 30 Mar 2021 20:32:30 GMT
# ARGS: ODOO_RELEASE=20210330 ODOO_SHA=0a0ebf50846a5e5131a6725795c3fc59d511262d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 30 Mar 2021 20:32:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Mar 2021 20:32:30 GMT
EXPOSE 8069 8071 8072
# Tue, 30 Mar 2021 20:32:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Mar 2021 20:32:31 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 30 Mar 2021 20:32:31 GMT
USER odoo
# Tue, 30 Mar 2021 20:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Mar 2021 20:32:31 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f95e614e07c856f6c1da438d4c95c0a6e5eac30d89fcc3a5734f5135633ed4a`  
		Last Modified: Sat, 27 Mar 2021 06:20:33 GMT  
		Size: 213.2 MB (213156617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08230c79e58cbef992d03708a57cb446a37e38c4aae753a3b55270d96eccf46d`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 2.3 MB (2348523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfde40794ec1a3832504589fefca9859cb38526d3244c425e3dbcefa0cbc7356`  
		Last Modified: Sat, 27 Mar 2021 06:19:45 GMT  
		Size: 910.1 KB (910061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d40543785b0ecbd9954b39352273e6e8f24711215dc28f73fdd23e70bf2692b`  
		Last Modified: Tue, 30 Mar 2021 20:36:14 GMT  
		Size: 272.2 MB (272242624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b07fddd5c4a25abf0e6c28d282e9b84cbafb4347a8cdb189b6e55f7049d542`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c6f7368ed8074690d6c222c3daee393f56e5c7388ef6146c7f76263d08813c`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25729b0270c67c2cafe5a02ed3f0ad4a81c49dadeec47c3dcbe5b7fc112d07a`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a297e06400118a4211607da5f02373a22ec80d118969f8b278f6c070216011`  
		Last Modified: Tue, 30 Mar 2021 20:35:38 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
