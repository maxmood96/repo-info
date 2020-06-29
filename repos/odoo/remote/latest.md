## `odoo:latest`

```console
$ docker pull odoo@sha256:562dcfc9ec1299498ccf0fd6aa03be98ec84b83d9705712ec8edadfcaa90d616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:9d455e32dad6ce70fba5611f94ed25d664584645abf1c3ed588692549142500d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381865700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f54f7d515762b3e26f16e6485ab7610f45c8f013482d0bc14a989d91557922e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 08:20:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 09 Jun 2020 08:20:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 09 Jun 2020 08:20:12 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2020 08:21:21 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Tue, 09 Jun 2020 08:21:31 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:21:35 GMT
RUN npm install -g rtlcss
# Tue, 09 Jun 2020 08:21:35 GMT
ENV ODOO_VERSION=13.0
# Mon, 29 Jun 2020 20:37:58 GMT
ARG ODOO_RELEASE=20200629
# Mon, 29 Jun 2020 20:37:58 GMT
ARG ODOO_SHA=1d86e2728a65ed2c9f6ea9b6b893df878f75599e
# Mon, 29 Jun 2020 20:38:51 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=1d86e2728a65ed2c9f6ea9b6b893df878f75599e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Mon, 29 Jun 2020 20:38:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Mon, 29 Jun 2020 20:38:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Mon, 29 Jun 2020 20:38:53 GMT
# ARGS: ODOO_RELEASE=20200629 ODOO_SHA=1d86e2728a65ed2c9f6ea9b6b893df878f75599e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Mon, 29 Jun 2020 20:38:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 29 Jun 2020 20:38:54 GMT
EXPOSE 8069 8071 8072
# Mon, 29 Jun 2020 20:38:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 29 Jun 2020 20:38:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Mon, 29 Jun 2020 20:38:54 GMT
USER odoo
# Mon, 29 Jun 2020 20:38:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Jun 2020 20:38:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c38fb221c6bbb14c929d8dc9845e790d99ab77c30f35eeda6d0271790132f8f`  
		Last Modified: Tue, 09 Jun 2020 08:29:18 GMT  
		Size: 204.1 MB (204081824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fbb07c19f556a4061c1794e095cb19bde5b5853b7bbda4820e6f15d50e720e`  
		Last Modified: Tue, 09 Jun 2020 08:28:44 GMT  
		Size: 2.3 MB (2335295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f3dc70f3be0a19e54a19846ffa5cd607a2a93c5323ffc80a908f1b4b856ad4`  
		Last Modified: Tue, 09 Jun 2020 08:28:43 GMT  
		Size: 1.1 MB (1095530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0c04441f8ef8d1451f0f65a419e5ca67cae5f0350a50ceabaad40a26968552`  
		Last Modified: Mon, 29 Jun 2020 20:42:10 GMT  
		Size: 147.3 MB (147252384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01ced95b7d280e6c3510b10069e39f2ddf3d1d708429f4dd85563c2c6962216`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc306e3d6e98068e9e30c6f06e3f146eeaa10ad0beeb814a57afbb5024592756`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5f1596c13e989ec960b6e44fdfe7c62f70bc01b672acf366936aee5e4b995a`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8fe6ed13672ea60237445b3cf3d9e6e69176b8042c586ce615c9088bd2281b`  
		Last Modified: Mon, 29 Jun 2020 20:41:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
