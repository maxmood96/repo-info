## `odoo:latest`

```console
$ docker pull odoo@sha256:bf08efd58d03868f7488cac6e7a4b35bd72950ea3fea57edd6f3c8190fb6c584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:7a3cf9f366c5fbbb05e594f83d70b887096c1d1b96363fea2bb72e95e168a2e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.5 MB (551533241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f16d800a8ab1dcf0c983f4e06ca15da9b9cfef0479830781a326c330fba0f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:59 GMT
ADD file:36919ae6bb25e3269eff949443129a01a8a43fb967fe6563939ebe1e1e9b8228 in / 
# Thu, 17 Mar 2022 04:03:59 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:40:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 18 Mar 2022 08:40:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 18 Mar 2022 08:40:10 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 08:41:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Fri, 18 Mar 2022 08:41:58 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:42:00 GMT
RUN npm install -g rtlcss
# Fri, 18 Mar 2022 08:42:00 GMT
ENV ODOO_VERSION=15.0
# Fri, 25 Mar 2022 19:19:51 GMT
ARG ODOO_RELEASE=20220325
# Fri, 25 Mar 2022 19:19:51 GMT
ARG ODOO_SHA=3d498c38022150b5e3907f2d72346cefe3e16809
# Fri, 25 Mar 2022 19:21:05 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=3d498c38022150b5e3907f2d72346cefe3e16809
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Mar 2022 19:21:09 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Mar 2022 19:21:09 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Mar 2022 19:21:10 GMT
# ARGS: ODOO_RELEASE=20220325 ODOO_SHA=3d498c38022150b5e3907f2d72346cefe3e16809
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Mar 2022 19:21:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Mar 2022 19:21:10 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Mar 2022 19:21:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Mar 2022 19:21:10 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Mar 2022 19:21:10 GMT
USER odoo
# Fri, 25 Mar 2022 19:21:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Mar 2022 19:21:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ae13dd57832654086618a81dbc128846aa092489260c326ee95429b63c3cf213`  
		Last Modified: Thu, 17 Mar 2022 04:10:05 GMT  
		Size: 31.4 MB (31376572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b017bd0f3af794ea97d29bea01710b0112b2dd1193ae49ba1f535e87d7bf27`  
		Last Modified: Fri, 18 Mar 2022 08:50:35 GMT  
		Size: 220.3 MB (220298052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f81dd0cadac34bb3b184c1c920982bd6981304e625e5ad01b9dce5f2bc784d6`  
		Last Modified: Fri, 18 Mar 2022 08:50:04 GMT  
		Size: 2.5 MB (2509910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fc845e3739ad670483a172d5d1497e8da58b94a3d5c68a7f2d7eb5f7baab7c`  
		Last Modified: Fri, 18 Mar 2022 08:50:03 GMT  
		Size: 450.8 KB (450836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e10bbd7e1f2e042a50d54fb4e4990cb2cf911a4646cbdeb680ec4c441c6764f`  
		Last Modified: Fri, 25 Mar 2022 19:25:29 GMT  
		Size: 296.9 MB (296895408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d27d86466ff424c9060bc9c659ee58b9e8c26ea0a4bfd51cbcbedb0c3abe65`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f76a21b5ca0aa40986bb150430365500a9fc271de676721b3f23e51b8a58f2`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e17ff53ea3bb2b9014ffc104a772b7830b08b5746e20575a255ccdc1478184`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5c53c2b940544b2b5dd99beff42022a67f771e964254348845e2d64b754c4e`  
		Last Modified: Fri, 25 Mar 2022 19:24:56 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
