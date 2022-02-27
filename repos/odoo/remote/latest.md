## `odoo:latest`

```console
$ docker pull odoo@sha256:378de7b9cc75e9de2f5c10ada0e0950110a9a31efdd278fc043297abdb5e679d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:a245f41cece0c7118e3016decc569316a928b13d7a13bb0470caf3937e12a460
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548928265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28775e04f869591ceeb617d6f542376dbb072a9b715f7e041d79c862e7f90a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 09:02:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 26 Jan 2022 09:02:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 26 Jan 2022 09:02:43 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jan 2022 09:04:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 26 Jan 2022 09:04:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 09:04:46 GMT
RUN npm install -g rtlcss
# Wed, 26 Jan 2022 09:04:46 GMT
ENV ODOO_VERSION=15.0
# Fri, 25 Feb 2022 19:11:32 GMT
ARG ODOO_RELEASE=20220225
# Fri, 25 Feb 2022 19:11:33 GMT
ARG ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
# Fri, 25 Feb 2022 19:13:30 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Fri, 25 Feb 2022 19:13:34 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Fri, 25 Feb 2022 19:13:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Fri, 25 Feb 2022 19:13:36 GMT
# ARGS: ODOO_RELEASE=20220225 ODOO_SHA=81a0f480b3f9835000cba40e99bf874d9462effe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Fri, 25 Feb 2022 19:13:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 25 Feb 2022 19:13:36 GMT
EXPOSE 8069 8071 8072
# Fri, 25 Feb 2022 19:13:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 25 Feb 2022 19:13:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Fri, 25 Feb 2022 19:13:37 GMT
USER odoo
# Fri, 25 Feb 2022 19:13:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 25 Feb 2022 19:13:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9293b96c918352418f9470373a3ccf1788a2b957d28fcb51b99beab26e73f974`  
		Last Modified: Wed, 26 Jan 2022 09:14:12 GMT  
		Size: 220.3 MB (220291077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfb4ef07b63f082d87ab75156c6ae62bcaf11e1ac37595986d8fd97b5dd5c80`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 2.5 MB (2506147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2f8d17d4fa74bd599ba34671d44d6da384f629a1bda0e322208540e26ae8ee`  
		Last Modified: Wed, 26 Jan 2022 09:13:41 GMT  
		Size: 440.2 KB (440201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe612bff0abd7042b08bb35f553922ce2084684f1ed1be9640f0cb848415380c`  
		Last Modified: Fri, 25 Feb 2022 19:18:20 GMT  
		Size: 294.3 MB (294322114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429bea4d789563cd6537732d4dec566706d4d625084fc5950b43b8e4a2405f29`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0be39161b45aaedb3810d1fea16d48ecdfdef4a9fbf44930d4fccf77a2b236`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86acae5b4ece5d09c16c28c8d53dc73fdc6bbf752ce91f5ebfdf16a3d86f940d`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a6eee278cd3c147cda4d18ee243730ad0c24fed1d398f2348f63ecfc0807b9`  
		Last Modified: Fri, 25 Feb 2022 19:17:43 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
