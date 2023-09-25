## `odoo:latest`

```console
$ docker pull odoo@sha256:9a622d6bf544aa44eb653227e282b9b090aa527ff4d67f7c49a0717fbda07f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:4c3452274217d93106a440a673914c34ef9392a734b78c3710bf9a53d6d8f76f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.8 MB (576802498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10abb3cd9e9a827db22e802885dc06dfcfc1444b08ed87a6ebd282badf76924c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:05:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 20 Sep 2023 17:05:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 20 Sep 2023 17:05:17 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:06:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 20 Sep 2023 17:06:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:06:34 GMT
RUN npm install -g rtlcss
# Wed, 20 Sep 2023 17:06:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Sep 2023 22:24:56 GMT
ARG ODOO_RELEASE=20230925
# Mon, 25 Sep 2023 22:24:57 GMT
ARG ODOO_SHA=c258ecd198cbd079fe1a271dcba23930820eb12f
# Mon, 25 Sep 2023 22:26:18 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=c258ecd198cbd079fe1a271dcba23930820eb12f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 25 Sep 2023 22:26:23 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 25 Sep 2023 22:26:23 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 25 Sep 2023 22:26:23 GMT
# ARGS: ODOO_RELEASE=20230925 ODOO_SHA=c258ecd198cbd079fe1a271dcba23930820eb12f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 25 Sep 2023 22:26:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Sep 2023 22:26:24 GMT
EXPOSE 8069 8071 8072
# Mon, 25 Sep 2023 22:26:24 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Sep 2023 22:26:24 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 25 Sep 2023 22:26:24 GMT
USER odoo
# Mon, 25 Sep 2023 22:26:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Sep 2023 22:26:24 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11206b2f0b0742a04b2e5aa673cf9bc01605b066d9fb144ce3973545531f57`  
		Last Modified: Wed, 20 Sep 2023 17:14:18 GMT  
		Size: 221.0 MB (220991931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e852d5c710cf3b695ca69683a47c0c02019debf9d920cb9cf770b83b5b466e3`  
		Last Modified: Wed, 20 Sep 2023 17:13:54 GMT  
		Size: 2.6 MB (2627315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2d84b33fdc1c69a8c227d7b0e75f038a4e81d937f06be5b99f42c6ad8c6bc9`  
		Last Modified: Wed, 20 Sep 2023 17:13:53 GMT  
		Size: 455.5 KB (455518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e38f1dbd6155d88625b9f11f5f75df94eb0caa2f4e60cad64d0f28db29e7f2`  
		Last Modified: Mon, 25 Sep 2023 22:30:07 GMT  
		Size: 321.3 MB (321307565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1dcfdbe1f893f30b7617d276b98de89b517719d6d04bc00faa55b15c2dbacf`  
		Last Modified: Mon, 25 Sep 2023 22:29:30 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252d91aa73eb2464c1d4053c046d6010408c5676b65a9efc2c21b96b4ab9f194`  
		Last Modified: Mon, 25 Sep 2023 22:29:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6d7b87a5437483aca0f8715d5a9ee6e1ba000bd59f69145a858673fbaa4339`  
		Last Modified: Mon, 25 Sep 2023 22:29:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55c8f81b83e5f9c9fc83fa02532b653910152495dbf5cb4ba3aa69b6970a9f5`  
		Last Modified: Mon, 25 Sep 2023 22:29:29 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
