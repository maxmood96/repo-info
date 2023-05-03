## `odoo:latest`

```console
$ docker pull odoo@sha256:2e2ebbac337620116cd4000d7b8833ad1c296618a11b4e6a8f783a05a0f1215c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:d72f131d2719cdc171b7057bb47eefdaab2841dd25c45024c8254ed3d88be700
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.6 MB (569627367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3e3639d93ff78bb635679fb408e88919d0cf8a1f14079823de89b03190a724`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:11:13 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 03 May 2023 22:11:13 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 03 May 2023 22:11:13 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 22:12:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 03 May 2023 22:12:54 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:12:55 GMT
RUN npm install -g rtlcss
# Wed, 03 May 2023 22:12:56 GMT
ENV ODOO_VERSION=16.0
# Wed, 03 May 2023 22:12:56 GMT
ARG ODOO_RELEASE=20230430
# Wed, 03 May 2023 22:12:56 GMT
ARG ODOO_SHA=1d8d64fec19fc1c31e13d9d9cdc4b127ba4e72cd
# Wed, 03 May 2023 22:14:17 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=1d8d64fec19fc1c31e13d9d9cdc4b127ba4e72cd
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 03 May 2023 22:14:22 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 03 May 2023 22:14:22 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 03 May 2023 22:14:23 GMT
# ARGS: ODOO_RELEASE=20230430 ODOO_SHA=1d8d64fec19fc1c31e13d9d9cdc4b127ba4e72cd
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 03 May 2023 22:14:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 03 May 2023 22:14:23 GMT
EXPOSE 8069 8071 8072
# Wed, 03 May 2023 22:14:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 03 May 2023 22:14:23 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 03 May 2023 22:14:23 GMT
USER odoo
# Wed, 03 May 2023 22:14:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 22:14:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ba628d58ec2cec04d9a4bc73b4015a47d7707f4e4d1e9d92a40ce9c8ddcc66`  
		Last Modified: Wed, 03 May 2023 22:19:54 GMT  
		Size: 220.3 MB (220297784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc07b7d1cfb584aa1c510ede6794940b0d1e644d62606e436b92fd194198144`  
		Last Modified: Wed, 03 May 2023 22:19:30 GMT  
		Size: 2.6 MB (2575304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77a58f0a17b42f1032fbe1881c6d8711bdefa34afb5e985297f35f6c5e69b5`  
		Last Modified: Wed, 03 May 2023 22:19:29 GMT  
		Size: 452.2 KB (452241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91fc12cdc1288fd9654ba11e5c61b1d174f70692cc5b02bbf850127d9e20eb0`  
		Last Modified: Wed, 03 May 2023 22:20:04 GMT  
		Size: 314.9 MB (314896070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2619983c05393da18859f1a59ff48254cb22a9dd04d291f1b066d922474745a7`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0c954a649b1db32a3011c78944731a7a7dc70b6fc85c657a12368d69072511`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e602314abc510f6f52e700d6d0b661bb35ae2a30e46d27bdb6205fa8e61c94`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c06d4c57624a3e3b070ae52f19b5273d9361584b8c4266f6238cf29ded33ef`  
		Last Modified: Wed, 03 May 2023 22:19:27 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
