## `odoo:latest`

```console
$ docker pull odoo@sha256:a27c258e2d0b73f8af3460a0d056bea1874679eb733ee1ad48b80312e1f7a77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:14eb922dfd65ba13c5ee6206d35de63b1c37390de420a7f1c75b5839925b0e7d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.6 MB (516571876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a622ba09ca0ec67573cdb892210033c6aa3f7e522d3b9ed543b13c866c8bf77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:12:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 22 Jul 2021 14:12:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 22 Jul 2021 14:12:41 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 14:14:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 22 Jul 2021 14:14:14 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:14:17 GMT
RUN npm install -g rtlcss
# Thu, 22 Jul 2021 14:14:18 GMT
ENV ODOO_VERSION=14.0
# Thu, 22 Jul 2021 14:14:18 GMT
ARG ODOO_RELEASE=20210720
# Thu, 22 Jul 2021 14:14:18 GMT
ARG ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
# Thu, 22 Jul 2021 14:15:29 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 22 Jul 2021 14:15:33 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 22 Jul 2021 14:15:33 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 22 Jul 2021 14:15:34 GMT
# ARGS: ODOO_RELEASE=20210720 ODOO_SHA=897a15c05244de02eceac2a930d169f2010971a6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 22 Jul 2021 14:15:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 22 Jul 2021 14:15:35 GMT
EXPOSE 8069 8071 8072
# Thu, 22 Jul 2021 14:15:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 22 Jul 2021 14:15:35 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 22 Jul 2021 14:15:35 GMT
USER odoo
# Thu, 22 Jul 2021 14:15:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 22 Jul 2021 14:15:36 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5502f02c83eb9a5d2610c8d0caea8b6d8645db289895c5071886b9231f40ac51`  
		Last Modified: Thu, 22 Jul 2021 14:22:40 GMT  
		Size: 213.2 MB (213172386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a9b423102589afe08dee7c8ee26abe30dce0b452950ca9eb03c425cf098c16`  
		Last Modified: Thu, 22 Jul 2021 14:22:17 GMT  
		Size: 2.3 MB (2349817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62bb0f68ae1402800683d9694dc8f338be4ac729f14a2e24d738f4aa12ea7e6`  
		Last Modified: Thu, 22 Jul 2021 14:22:14 GMT  
		Size: 889.3 KB (889257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb65718bd5e3f1c1bb871ad5f4994122924ff3662d74be1bd6a9e0176649b4e`  
		Last Modified: Thu, 22 Jul 2021 14:22:46 GMT  
		Size: 273.0 MB (273012190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df0c12a812f7f3caa325f459babefa4a34dd1a29b907194054b305f39b58d98`  
		Last Modified: Thu, 22 Jul 2021 14:22:11 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1f4840656a5ed310db0ab8e60a5637a9771dd6ef956d5c382b8cfb49334ec3`  
		Last Modified: Thu, 22 Jul 2021 14:22:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e650314c3551743b9acbc4c940b89521b3573e7017020ec65afbba385794a5c`  
		Last Modified: Thu, 22 Jul 2021 14:22:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cfe4eb055bc4a9b2089a0366ba845f02939106030911d8500b4d08e8f234c1`  
		Last Modified: Thu, 22 Jul 2021 14:22:10 GMT  
		Size: 581.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
