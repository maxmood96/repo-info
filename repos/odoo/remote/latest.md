## `odoo:latest`

```console
$ docker pull odoo@sha256:e9d693d1d5bf7667b008694135d8f6e9fa3fec40f8adc948a1af36467d5a4a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:18daa3a80af6205520c700a64cedcab3007e795c8a9de72e5e58f1354193dd10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.0 MB (556016372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7b0883396ecb062e2f92cae8eb93efedd2aab1c4efa543b35ab4ef942ab821`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:42:19 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 23 Jun 2022 04:42:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 23 Jun 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jun 2022 04:43:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 23 Jun 2022 04:43:30 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:43:32 GMT
RUN npm install -g rtlcss
# Thu, 23 Jun 2022 04:43:32 GMT
ENV ODOO_VERSION=15.0
# Fri, 08 Jul 2022 18:39:56 GMT
ARG ODOO_RELEASE=20220708
# Fri, 08 Jul 2022 18:39:56 GMT
ARG ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
# Fri, 08 Jul 2022 18:41:12 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 08 Jul 2022 18:41:17 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 08 Jul 2022 18:41:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 08 Jul 2022 18:41:18 GMT
# ARGS: ODOO_RELEASE=20220708 ODOO_SHA=5e393909c75b3c85ddaaabf587c48197b800e68b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 08 Jul 2022 18:41:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 08 Jul 2022 18:41:18 GMT
EXPOSE 8069 8071 8072
# Fri, 08 Jul 2022 18:41:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 08 Jul 2022 18:41:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 08 Jul 2022 18:41:18 GMT
USER odoo
# Fri, 08 Jul 2022 18:41:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 Jul 2022 18:41:18 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985d8d4799be91199129b639a86c297d32603e21afe9cfc8841d93193da8a300`  
		Last Modified: Thu, 23 Jun 2022 04:51:09 GMT  
		Size: 220.3 MB (220309145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7eb12b3f19b77eb7d077051fb56941bf1917065af5536fbbf03ed8d6892da38`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 2.5 MB (2513193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce450078d93ef4e1ee2bc96f4c29e6fc5b4776fa5ec4d69a370bddf5466f47d`  
		Last Modified: Thu, 23 Jun 2022 04:50:43 GMT  
		Size: 485.4 KB (485399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3910581f15fdcef2185fccd0c2a74311afe8bc687d007096fe46850f943619`  
		Last Modified: Fri, 08 Jul 2022 18:45:06 GMT  
		Size: 301.3 MB (301326761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fc733f9e41f8e7ffab47edf0d95fc50e1d203f85edcfb90ba9c77194eefec8`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0949ead7533e92b06806763af7ba506f58277e31403637dd8239781c1c59a048`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aea26eedacfcb6bc449a6a5aed978cc97bda1c27af44f5047dd8d924f4756c6`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af02f7e0b340396eb88e897214aea454e6a35d79089a16c95e8f531fca44d9ec`  
		Last Modified: Fri, 08 Jul 2022 18:44:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
