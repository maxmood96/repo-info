## `odoo:latest`

```console
$ docker pull odoo@sha256:c6a5e6ecf65cc06c16fedbd8fb30e57b707866c2d3a66adf619d0e5eb8d86ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:aea26ad5d9ddde024bc65fab0c9e126f9f34b5fdcd8ada9a6fa6fff14a4442a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.1 MB (576060265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee332cbe8830d6f2c16a64b99155eca16a84aa314a48e41be89fb2837ad2fa12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 10:16:30 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 16 Aug 2023 10:16:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 16 Aug 2023 10:16:30 GMT
ENV LANG=C.UTF-8
# Wed, 16 Aug 2023 10:17:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 16 Aug 2023 10:17:43 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:17:44 GMT
RUN npm install -g rtlcss
# Wed, 16 Aug 2023 10:17:44 GMT
ENV ODOO_VERSION=16.0
# Thu, 17 Aug 2023 10:13:19 GMT
ARG ODOO_RELEASE=20230816
# Thu, 17 Aug 2023 10:13:19 GMT
ARG ODOO_SHA=fc84b0d3fc0cb5506378c91f19681248c6fdb36e
# Thu, 17 Aug 2023 10:14:40 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=fc84b0d3fc0cb5506378c91f19681248c6fdb36e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 17 Aug 2023 10:14:45 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Thu, 17 Aug 2023 10:14:45 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 17 Aug 2023 10:14:45 GMT
# ARGS: ODOO_RELEASE=20230816 ODOO_SHA=fc84b0d3fc0cb5506378c91f19681248c6fdb36e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 17 Aug 2023 10:14:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 17 Aug 2023 10:14:46 GMT
EXPOSE 8069 8071 8072
# Thu, 17 Aug 2023 10:14:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 17 Aug 2023 10:14:46 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 17 Aug 2023 10:14:46 GMT
USER odoo
# Thu, 17 Aug 2023 10:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Aug 2023 10:14:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38faf7b926f64bb75adbf63bb8f9cf962e9fe7240f1b77f975713e522fb38f2f`  
		Last Modified: Wed, 16 Aug 2023 10:25:32 GMT  
		Size: 221.0 MB (220992472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f422a2822ff3c0ddcb0feae90917ad16bfadc792ed6120bb85ec478c192fc14`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 2.6 MB (2579930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e455fdc49a2fa9b84da301d6cacd3ac952037699a291e871cd86ab33ff34b4`  
		Last Modified: Wed, 16 Aug 2023 10:25:08 GMT  
		Size: 454.4 KB (454421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87358e6bb36d571ca2c6850f6decdc49db89367b35f6e3803f404ab964dc5d47`  
		Last Modified: Thu, 17 Aug 2023 10:18:29 GMT  
		Size: 320.6 MB (320613299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b320b6cc330fdab724e8646c5256dcad07738d771d3b56b55856a86a9dc3fc`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b592bed196fd23afb7c13e423f00e608b135fa62c651fa75a793bb9ad089f603`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610cd8914d942fe24e705f6e38960750af9b1bfb350668d2103274d90288072c`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e3366e705964c9dba1f589914490d3083790c68344747495afe3654362cec9`  
		Last Modified: Thu, 17 Aug 2023 10:17:54 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
