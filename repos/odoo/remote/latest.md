## `odoo:latest`

```console
$ docker pull odoo@sha256:34806a615878d4045a383b57b8439391aacc361fb30763a9ba51cfbab0f6786a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:8a50954ba7f2324ad43e06afa236cda1b002b8278cb48a89d2392a5e2b7c4b87
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.9 MB (515859704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45bcdd074f917c2fd0bde9713d55f462ee042009139d35c23bb5636298b8a8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:29 GMT
ADD file:b797b4d60ad7954e98ad71574c4fc90ad3da9a5c250112373e92e2af3056e581 in / 
# Tue, 30 Mar 2021 21:49:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 05:28:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 31 Mar 2021 05:28:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 31 Mar 2021 05:28:29 GMT
ENV LANG=C.UTF-8
# Wed, 31 Mar 2021 05:29:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 31 Mar 2021 05:29:44 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 05:29:47 GMT
RUN npm install -g rtlcss
# Wed, 31 Mar 2021 05:29:48 GMT
ENV ODOO_VERSION=14.0
# Wed, 07 Apr 2021 19:51:25 GMT
ARG ODOO_RELEASE=20210407
# Wed, 07 Apr 2021 19:51:25 GMT
ARG ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
# Wed, 07 Apr 2021 19:52:31 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 07 Apr 2021 19:52:35 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 07 Apr 2021 19:52:35 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 07 Apr 2021 19:52:36 GMT
# ARGS: ODOO_RELEASE=20210407 ODOO_SHA=aff621cdd7e1ee2e27769d26356954cc8d143be1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 07 Apr 2021 19:52:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 07 Apr 2021 19:52:36 GMT
EXPOSE 8069 8071 8072
# Wed, 07 Apr 2021 19:52:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 07 Apr 2021 19:52:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 07 Apr 2021 19:52:37 GMT
USER odoo
# Wed, 07 Apr 2021 19:52:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 07 Apr 2021 19:52:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:75646c2fb4101d306585c9b106be1dfa7d82720baabe1c75b64d759ea8adf341`  
		Last Modified: Tue, 30 Mar 2021 21:54:15 GMT  
		Size: 27.1 MB (27139293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891b8c13a6557e87341fe3dae2cacc445b84d3061c83b252ca743c338d64cc83`  
		Last Modified: Wed, 31 Mar 2021 05:37:46 GMT  
		Size: 213.2 MB (213169537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acf2c1161bac7f6d917df1dab741f4f98b3d7d9bb4994d7fd1913385578875e`  
		Last Modified: Wed, 31 Mar 2021 05:37:18 GMT  
		Size: 2.3 MB (2348508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16b52e489bcfae111683bd0dc94749af43d9ea55931a3c2a703c8c3ff3dfb6e`  
		Last Modified: Wed, 31 Mar 2021 05:37:16 GMT  
		Size: 894.0 KB (894018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b049e678c814ae5246118f37ec0988cc42cc96690bccdd6ea9f6cad2f57114c8`  
		Last Modified: Wed, 07 Apr 2021 19:56:11 GMT  
		Size: 272.3 MB (272305917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c78a5820c7d656599da2fef55bc7b006e517667cb059ed9544982532ec17da0`  
		Last Modified: Wed, 07 Apr 2021 19:55:39 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453d50c2bb3dcbef24818b454814d99221d5557698825f25243bbc6e1edb85e3`  
		Last Modified: Wed, 07 Apr 2021 19:55:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04dd632fea738b974175a0a0ad439008139fb06611cdb6a351adcf67343b7476`  
		Last Modified: Wed, 07 Apr 2021 19:55:41 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac361ec738ee19861cf5e8d975c4b68c1efd40d281adbc234de94e94e6b5060`  
		Last Modified: Wed, 07 Apr 2021 19:55:39 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
