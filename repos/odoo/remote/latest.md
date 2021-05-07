## `odoo:latest`

```console
$ docker pull odoo@sha256:a0b809d3f15aa96aa445e246a4dc2d708930a6eec8f794c0db4fae9d63cd1e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:10b2f69a988e275e9a9a9903546a910e5937957b4fab10c30eb6233e682f0d43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.2 MB (516228493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d50ad77922e35e535b5ff1b7d41171e250bd9e379adc3124c89217038fb7a45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 12:30:53 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 10 Apr 2021 12:30:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 10 Apr 2021 12:30:54 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 12:32:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 10 Apr 2021 12:32:46 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 12:32:51 GMT
RUN npm install -g rtlcss
# Sat, 10 Apr 2021 12:32:51 GMT
ENV ODOO_VERSION=14.0
# Thu, 06 May 2021 21:48:01 GMT
ARG ODOO_RELEASE=20210506
# Thu, 06 May 2021 21:48:01 GMT
ARG ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
# Thu, 06 May 2021 21:49:12 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 06 May 2021 21:49:16 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 06 May 2021 21:49:17 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 06 May 2021 21:49:17 GMT
# ARGS: ODOO_RELEASE=20210506 ODOO_SHA=72d20b873a21d50be6ce363f76b4e78003d93999
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 06 May 2021 21:49:18 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 06 May 2021 21:49:18 GMT
EXPOSE 8069 8071 8072
# Thu, 06 May 2021 21:49:18 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 06 May 2021 21:49:18 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 06 May 2021 21:49:18 GMT
USER odoo
# Thu, 06 May 2021 21:49:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 May 2021 21:49:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df7a8fcf45065b035b83165d399d7900a139dc5e00d9e4d6ce8699785fb5343`  
		Last Modified: Sat, 10 Apr 2021 12:41:41 GMT  
		Size: 213.2 MB (213170428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6128de947157b937143a4ca96babae9ce2e9b71d01a4b53dc0a4e1301bdaa0d4`  
		Last Modified: Sat, 10 Apr 2021 12:41:12 GMT  
		Size: 2.3 MB (2348669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:963607ad2a1b5492ef59daa14209ad6d7e164abe8c9f0636566235cff0d20ade`  
		Last Modified: Sat, 10 Apr 2021 12:41:11 GMT  
		Size: 896.6 KB (896573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773f192a60482e62377afe0585d6ca0537a661b6c573371c7519b3a77d45eb78`  
		Last Modified: Thu, 06 May 2021 21:53:02 GMT  
		Size: 272.7 MB (272671020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4fe1ecd40b0164874a86ecbb4caa7e26a06593c6d96983c1d89137e59092b1`  
		Last Modified: Thu, 06 May 2021 21:52:28 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521cd86a8a315b356742c3d072d10d9b44ecbe24b0da947e7a0838c173ba9b92`  
		Last Modified: Thu, 06 May 2021 21:52:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba2181ef8d5053b9408e6f8a5438c863bab7cadaca34a163b2fb0df804bcb61`  
		Last Modified: Thu, 06 May 2021 21:52:27 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7361b41d2463cd55eeba366f5561088db4895b5250b5303b19dd7e23031c06`  
		Last Modified: Thu, 06 May 2021 21:52:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
