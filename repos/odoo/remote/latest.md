## `odoo:latest`

```console
$ docker pull odoo@sha256:36c362a62d23c338c22175181bc9220ee4d19f3aa6cb79e1eb2285f36a593a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:e52530e2968653f0e4e94eb966d4001ae44e30285ad2003f74afd4ce7bf20808
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.1 MB (511099229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbf465b413ce56cd1087ff4962e911d9686865078e959d03e3b2d757cd04f62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 17:27:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Feb 2021 17:27:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Feb 2021 17:27:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 17:29:04 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Feb 2021 17:29:13 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 17:29:17 GMT
RUN npm install -g rtlcss
# Tue, 09 Feb 2021 17:29:17 GMT
ENV ODOO_VERSION=14.0
# Wed, 10 Feb 2021 19:25:22 GMT
ARG ODOO_RELEASE=20210210
# Wed, 10 Feb 2021 19:25:22 GMT
ARG ODOO_SHA=1b428768c8106106f046f337096c1a9cd49e780d
# Wed, 10 Feb 2021 19:26:29 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=1b428768c8106106f046f337096c1a9cd49e780d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 10 Feb 2021 19:26:31 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 10 Feb 2021 19:26:31 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 10 Feb 2021 19:26:32 GMT
# ARGS: ODOO_RELEASE=20210210 ODOO_SHA=1b428768c8106106f046f337096c1a9cd49e780d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 10 Feb 2021 19:26:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 10 Feb 2021 19:26:32 GMT
EXPOSE 8069 8071 8072
# Wed, 10 Feb 2021 19:26:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 10 Feb 2021 19:26:33 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 10 Feb 2021 19:26:33 GMT
USER odoo
# Wed, 10 Feb 2021 19:26:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 19:26:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f01c0c02d487d167e4440bbc1f9f7d18aef702f607a4f4d53ed03fa8d789738`  
		Last Modified: Tue, 09 Feb 2021 17:39:00 GMT  
		Size: 213.2 MB (213152252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e328a5fa7db6c9ddcf2128f44c9e8e1644ea40f1e250a7427dd00dc2b19700`  
		Last Modified: Tue, 09 Feb 2021 17:37:49 GMT  
		Size: 2.3 MB (2346601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241913ecf51f6d0a8e68d705ef3d58c1745fbbbca4089277a75bd244831b5247`  
		Last Modified: Tue, 09 Feb 2021 17:37:51 GMT  
		Size: 908.6 KB (908573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002b4381da9ba123f495a5b44f705f0035ef5da695db16ba56ac3c83bdf1a430`  
		Last Modified: Wed, 10 Feb 2021 19:30:12 GMT  
		Size: 267.6 MB (267594264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc830ea2367662177974a1e451ca283013ea6ce2e0ab3cf281427c990ae60b7e`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a469ed8af951afee485d0bb2585aeb1c25e349e0ec83645f113cba3fb8f97762`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505caa5c2264d0ff68c93c505e5c5d26f0f2909860f5c6e8642976f2643f1cd9`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 594.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ace15cb84631cedfe88d96f84ead474f5d9e99ba2f467b2f90ea176d8c49900`  
		Last Modified: Wed, 10 Feb 2021 19:29:35 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
