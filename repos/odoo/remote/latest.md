## `odoo:latest`

```console
$ docker pull odoo@sha256:529d4665292b56e4a92897d1b587ab2c3d19d5ab047dc38dc4f45a8d058e43e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:4bf021269722b263c09c6b711334c56b0c0db1f6875cb94e2c56e73b726eda85
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 MB (516474691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cf06ebb25be68424b6e213570d9e14be9840630dbeb5fe1e28cf6c2c06c83c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 07:44:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 23 Jun 2021 07:44:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 23 Jun 2021 07:44:57 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 07:46:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 23 Jun 2021 07:46:28 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 07:46:34 GMT
RUN npm install -g rtlcss
# Wed, 23 Jun 2021 07:46:34 GMT
ENV ODOO_VERSION=14.0
# Tue, 13 Jul 2021 18:29:44 GMT
ARG ODOO_RELEASE=20210713
# Tue, 13 Jul 2021 18:29:44 GMT
ARG ODOO_SHA=59408eba9273bf60cb34759b17816553bc583303
# Tue, 13 Jul 2021 18:30:53 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=59408eba9273bf60cb34759b17816553bc583303
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Tue, 13 Jul 2021 18:30:57 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Tue, 13 Jul 2021 18:30:57 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Tue, 13 Jul 2021 18:30:58 GMT
# ARGS: ODOO_RELEASE=20210713 ODOO_SHA=59408eba9273bf60cb34759b17816553bc583303
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Tue, 13 Jul 2021 18:30:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 13 Jul 2021 18:30:58 GMT
EXPOSE 8069 8071 8072
# Tue, 13 Jul 2021 18:30:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 13 Jul 2021 18:30:59 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Tue, 13 Jul 2021 18:30:59 GMT
USER odoo
# Tue, 13 Jul 2021 18:30:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jul 2021 18:30:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80704698691bf3031da85fe60e94cb6d4b0debc3ac2359dd2d707eb4e5681e78`  
		Last Modified: Wed, 23 Jun 2021 07:56:36 GMT  
		Size: 213.2 MB (213171040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebc9af296bc1aa9b42af1b6d402cffc8e0ba56cc15906dbf0e7e73b86f00952`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 2.3 MB (2349730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65481a06fbb9368a1fb401461f0fdeb3a19ce0ef7a7b427d12f614c55ac2527b`  
		Last Modified: Wed, 23 Jun 2021 07:55:49 GMT  
		Size: 885.9 KB (885943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16506a5f3ee5de721e35b0267e025688f246d6ed0927d5ebd8c8b3ea24fc5d67`  
		Last Modified: Tue, 13 Jul 2021 18:34:46 GMT  
		Size: 272.9 MB (272919695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a490d65a662af856dd945bd11dc2c85ac9b9d15d1b06d0bca4fdc47fee1592`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f77f51fd15106ebf823d3cd375775e92a9ead4e8e3f176e13ea1f0bae9f1373`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ac4e98c4c110c6491048b80611467618e18ed7c870e104bd7a82cf81002fc7`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6aabb5a0e9a42b03b43a58eeed96fb3890a0db14cc30478e4cd514f579580e`  
		Last Modified: Tue, 13 Jul 2021 18:34:13 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
