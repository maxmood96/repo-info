## `odoo:latest`

```console
$ docker pull odoo@sha256:7b04b8be419b6b940827e6c3276d549f4c0883b06e32c4ff6750c25547080a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:611f1ae42f1d55e689343ad37869a86d0da8c2c3d71ed4c00a0bd1624518f442
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.2 MB (566181831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae486913bed23ecf80b51b6d8250226ad044e3dae2b2ff7d672b2fe0a2549c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:59:17 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 21 Dec 2022 11:59:17 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 21 Dec 2022 11:59:17 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:00:29 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 21 Dec 2022 12:00:38 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:00:39 GMT
RUN npm install -g rtlcss
# Wed, 21 Dec 2022 12:00:39 GMT
ENV ODOO_VERSION=16.0
# Mon, 09 Jan 2023 17:25:10 GMT
ARG ODOO_RELEASE=20230109
# Mon, 09 Jan 2023 17:25:10 GMT
ARG ODOO_SHA=884bf72c7318835b9ac56be2594032cbba7b8c7b
# Mon, 09 Jan 2023 17:26:37 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=884bf72c7318835b9ac56be2594032cbba7b8c7b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 09 Jan 2023 17:26:41 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Mon, 09 Jan 2023 17:26:42 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 09 Jan 2023 17:26:42 GMT
# ARGS: ODOO_RELEASE=20230109 ODOO_SHA=884bf72c7318835b9ac56be2594032cbba7b8c7b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 09 Jan 2023 17:26:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 09 Jan 2023 17:26:42 GMT
EXPOSE 8069 8071 8072
# Mon, 09 Jan 2023 17:26:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 09 Jan 2023 17:26:43 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 09 Jan 2023 17:26:43 GMT
USER odoo
# Mon, 09 Jan 2023 17:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Jan 2023 17:26:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b33e635a777ad2593a9a160436a438c4cf068b815a9d16dc6e4975f5df5b1c`  
		Last Modified: Wed, 21 Dec 2022 12:07:50 GMT  
		Size: 220.3 MB (220298472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c52fa0ca226e1b60d6963a358d003976668bd83f0ec398305fc945994bf0de`  
		Last Modified: Wed, 21 Dec 2022 12:07:24 GMT  
		Size: 2.6 MB (2573903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb896edd9e6352eb0d87d3b7f13ed806d0cef48cb80e239f4867f41c8a2b79dc`  
		Last Modified: Wed, 21 Dec 2022 12:07:23 GMT  
		Size: 452.6 KB (452551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ae9ab0a9e82fab6d9612eed16e35fee33fe399ea5a0c859fadcca782a7466b`  
		Last Modified: Mon, 09 Jan 2023 17:31:07 GMT  
		Size: 311.5 MB (311457494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f056f24da2085eea170fb40195e03edac39471525e5b080eb6547567fca665`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bde8ac0d976140e8a7052cc8258540b112cc1a96292c4f9e80fd8c4889c4de`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957fbc26e7fecb9392893753baf9540b573cd8d95041a2bac31860b2a06828dc`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adecbd9431af755491ccabb0fd9d6aa3347846e6fe9df27511aad0ba3a1cd6e4`  
		Last Modified: Mon, 09 Jan 2023 17:30:30 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
