## `odoo:latest`

```console
$ docker pull odoo@sha256:2c147d75bff49e2b37ffa1e76d9b96d1eebabc9a3895aa6f49a15109c20c299e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:785ae9a91ca0e74edf4301aad19f56cbc6575c3427530671e7c35c16abf8a3ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.5 MB (548496319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e339d3503f7f9e6bba4ff7fabc3fcb03f61105904da0621d7d1cd3d0cfd21d80`
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
# Wed, 26 Jan 2022 09:04:47 GMT
ARG ODOO_RELEASE=20220110
# Wed, 26 Jan 2022 09:04:47 GMT
ARG ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
# Wed, 26 Jan 2022 09:06:06 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Jan 2022 09:06:10 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 26 Jan 2022 09:06:10 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Jan 2022 09:06:11 GMT
# ARGS: ODOO_RELEASE=20220110 ODOO_SHA=7a4c94d79da0b05894effbaff06ca2b7250f0569
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Jan 2022 09:06:11 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Jan 2022 09:06:11 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Jan 2022 09:06:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Jan 2022 09:06:12 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Jan 2022 09:06:12 GMT
USER odoo
# Wed, 26 Jan 2022 09:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Jan 2022 09:06:12 GMT
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
	-	`sha256:e2c1a1010fb85d107e9d673b43a4971e5c5186a6e588ebcb00f94b9db4fe3113`  
		Last Modified: Wed, 26 Jan 2022 09:14:21 GMT  
		Size: 293.9 MB (293890175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0905f2c0188b03b39a5709fd2e15edc5bb4786fd17a63b8cf11e3135a24c1`  
		Last Modified: Wed, 26 Jan 2022 09:13:39 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f61379b5aac40a974ec8fa2a20252d2bdc6bb6e26ff6087149f19eaef624d95`  
		Last Modified: Wed, 26 Jan 2022 09:13:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db405fdc75f98113fe1defb775a5904cfa8dab7b21adb00445b2f022605e6177`  
		Last Modified: Wed, 26 Jan 2022 09:13:38 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bbb38d44f0fb37c54da2fbe03d1c7a9c46c395e843cb06f3a6bf7e7c204e13`  
		Last Modified: Wed, 26 Jan 2022 09:13:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
