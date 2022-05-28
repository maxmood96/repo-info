## `odoo:latest`

```console
$ docker pull odoo@sha256:2ac35f9beffd680e04256f90531da95418f2720f67e4d253c2500e784078241e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:ae5ea94a0436a54fb6ecb36cbc51ba57633b9608a237c860bdce51d0a0fd8879
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.2 MB (555172445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fc661e09c0757910a0c900ae1c5547e6b81554d2ef11a3a94fd56dffa3ac53`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 28 May 2022 01:20:23 GMT
ADD file:134f25aec8adf83cb940ba073a3409ca85dbb5ae592b704f95193e7d2539a3bc in / 
# Sat, 28 May 2022 01:20:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:59:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Sat, 28 May 2022 11:59:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Sat, 28 May 2022 11:59:12 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 12:00:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Sat, 28 May 2022 12:00:17 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 12:00:19 GMT
RUN npm install -g rtlcss
# Sat, 28 May 2022 12:00:19 GMT
ENV ODOO_VERSION=15.0
# Sat, 28 May 2022 12:00:19 GMT
ARG ODOO_RELEASE=20220520
# Sat, 28 May 2022 12:00:19 GMT
ARG ODOO_SHA=0663b11f4c05c66aadfe74fbd27b14beaa9e0f07
# Sat, 28 May 2022 12:01:33 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=0663b11f4c05c66aadfe74fbd27b14beaa9e0f07
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Sat, 28 May 2022 12:01:37 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Sat, 28 May 2022 12:01:37 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Sat, 28 May 2022 12:01:38 GMT
# ARGS: ODOO_RELEASE=20220520 ODOO_SHA=0663b11f4c05c66aadfe74fbd27b14beaa9e0f07
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Sat, 28 May 2022 12:01:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Sat, 28 May 2022 12:01:38 GMT
EXPOSE 8069 8071 8072
# Sat, 28 May 2022 12:01:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Sat, 28 May 2022 12:01:38 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Sat, 28 May 2022 12:01:38 GMT
USER odoo
# Sat, 28 May 2022 12:01:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 May 2022 12:01:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:42c077c10790d51b6f75c4eb895cbd4da37558f7215b39cbf64c46b288f89bda`  
		Last Modified: Sat, 28 May 2022 01:25:19 GMT  
		Size: 31.4 MB (31379276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e37b27d59935c5c50839381767950da6d3c54f7f411b13929df686c7c2c5cfa`  
		Last Modified: Sat, 28 May 2022 12:08:02 GMT  
		Size: 220.3 MB (220308203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08260db36e74a0f8d1b16ff325980f49c34374c59f07e4005643462652b1e9a0`  
		Last Modified: Sat, 28 May 2022 12:07:36 GMT  
		Size: 2.5 MB (2513560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c77ac3bfba98847aec3a79edd77e2cd7a14ff2ce72e6b8e145c8bc738b2fbcd`  
		Last Modified: Sat, 28 May 2022 12:07:35 GMT  
		Size: 474.1 KB (474093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1180581127f4862a28c59949f32288c499c81906d7016f52a297e2525fa79a`  
		Last Modified: Sat, 28 May 2022 12:08:09 GMT  
		Size: 300.5 MB (300494856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f54ebbf91ac79d05e13d47409d9e9c775c4b7145b6a1a480a64d85eb7fb2c04`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4c788902fed312029bbeed01552b28a4c0c4d9b205ba5095ca43ed2b73a6eb`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004cff4966af458e562bb73e22849b1124a61d4fc8d049bec69f0b357cd3c686`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff000d5cface257df463692de7dfade9590c927751e80f82d6d61dd06865edc1`  
		Last Modified: Sat, 28 May 2022 12:07:33 GMT  
		Size: 580.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
