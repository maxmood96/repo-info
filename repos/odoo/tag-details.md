<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:15`](#odoo15)
-	[`odoo:15.0`](#odoo150)
-	[`odoo:15.0-20240912`](#odoo150-20240912)
-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20240912`](#odoo160-20240912)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20240912`](#odoo170-20240912)
-	[`odoo:latest`](#odoolatest)

## `odoo:15`

```console
$ docker pull odoo@sha256:de7ffd6df663ce32d11e36c5f00e6ade9b7089cbd64c80ec97a44489fa802c0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15` - linux; amd64

```console
$ docker pull odoo@sha256:6f6ef25e31b80fb0aa6883c575480189eda299217755ca865eeb6ae194466ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564305418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf86932a8f93c327d502d4332caebe66c014460ef6eeec20e771fa775940d45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
CMD ["bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=C.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=15.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=a2a8947448c8c561336f9b2710eeb9e9cbfdec66
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: ODOO_RELEASE=20240912 ODOO_SHA=a2a8947448c8c561336f9b2710eeb9e9cbfdec66
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: ODOO_RELEASE=20240912 ODOO_SHA=a2a8947448c8c561336f9b2710eeb9e9cbfdec66
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6e7b313a3ba91e62bd03020cd21c83c803d8aa42e337466182f77edd69092e`  
		Last Modified: Thu, 12 Sep 2024 18:58:29 GMT  
		Size: 220.3 MB (220283962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d7d30b4cf6449ed7efc619f61734a67cef7e44c5ae2fc1c5ae122f71edfcfa`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 2.4 MB (2387799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f7b16cfd74856b938e3773c3de7e9f4e9ec5f4e21ef816c1b99437147a889c`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 471.6 KB (471559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12530e1d160f390563c824aa8335e6274645f2a55cbb6228b85e752a4d74cb`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 309.7 MB (309730985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c294418a37344b6333b39972f6077f654e326278cbc9bd0cecca05a6a7bd39c3`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4505bad208f46251da340c73671d0977aed3b91b47b58b8eb6ae96ff75133c0`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1e9e466a9412dccd82e146631c96972e46a5153222295603e845ac85bf3e6b`  
		Last Modified: Thu, 12 Sep 2024 18:58:28 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4606973710f953561927e2e98fc26710a4466ce0c3f90a2c024c0bf7ed1f7f`  
		Last Modified: Thu, 12 Sep 2024 18:58:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15` - unknown; unknown

```console
$ docker pull odoo@sha256:de713b61c5ddf07570010fcd6c191457c7d39e79bbe9c9d626ed753bbd214da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34711731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d370e01d4a0d27e9415cf089c8996921b7bed2b851deb1a9a3e76fd2ce6f499`

```dockerfile
```

-	Layers:
	-	`sha256:f6e5d66588f8ed69db87f8dccc9d6971d69c47cdd248450f56f3440bba5371f1`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 34.7 MB (34687100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f451a39351791b722b48d7931b33b52ad5dcc3261740f22e4e1b08fe1515fe6`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0`

```console
$ docker pull odoo@sha256:de7ffd6df663ce32d11e36c5f00e6ade9b7089cbd64c80ec97a44489fa802c0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0` - linux; amd64

```console
$ docker pull odoo@sha256:6f6ef25e31b80fb0aa6883c575480189eda299217755ca865eeb6ae194466ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564305418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf86932a8f93c327d502d4332caebe66c014460ef6eeec20e771fa775940d45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
CMD ["bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=C.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=15.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=a2a8947448c8c561336f9b2710eeb9e9cbfdec66
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: ODOO_RELEASE=20240912 ODOO_SHA=a2a8947448c8c561336f9b2710eeb9e9cbfdec66
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: ODOO_RELEASE=20240912 ODOO_SHA=a2a8947448c8c561336f9b2710eeb9e9cbfdec66
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6e7b313a3ba91e62bd03020cd21c83c803d8aa42e337466182f77edd69092e`  
		Last Modified: Thu, 12 Sep 2024 18:58:29 GMT  
		Size: 220.3 MB (220283962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d7d30b4cf6449ed7efc619f61734a67cef7e44c5ae2fc1c5ae122f71edfcfa`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 2.4 MB (2387799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f7b16cfd74856b938e3773c3de7e9f4e9ec5f4e21ef816c1b99437147a889c`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 471.6 KB (471559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12530e1d160f390563c824aa8335e6274645f2a55cbb6228b85e752a4d74cb`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 309.7 MB (309730985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c294418a37344b6333b39972f6077f654e326278cbc9bd0cecca05a6a7bd39c3`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4505bad208f46251da340c73671d0977aed3b91b47b58b8eb6ae96ff75133c0`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1e9e466a9412dccd82e146631c96972e46a5153222295603e845ac85bf3e6b`  
		Last Modified: Thu, 12 Sep 2024 18:58:28 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4606973710f953561927e2e98fc26710a4466ce0c3f90a2c024c0bf7ed1f7f`  
		Last Modified: Thu, 12 Sep 2024 18:58:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0` - unknown; unknown

```console
$ docker pull odoo@sha256:de713b61c5ddf07570010fcd6c191457c7d39e79bbe9c9d626ed753bbd214da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34711731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d370e01d4a0d27e9415cf089c8996921b7bed2b851deb1a9a3e76fd2ce6f499`

```dockerfile
```

-	Layers:
	-	`sha256:f6e5d66588f8ed69db87f8dccc9d6971d69c47cdd248450f56f3440bba5371f1`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 34.7 MB (34687100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f451a39351791b722b48d7931b33b52ad5dcc3261740f22e4e1b08fe1515fe6`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:15.0-20240912`

```console
$ docker pull odoo@sha256:de7ffd6df663ce32d11e36c5f00e6ade9b7089cbd64c80ec97a44489fa802c0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `odoo:15.0-20240912` - linux; amd64

```console
$ docker pull odoo@sha256:6f6ef25e31b80fb0aa6883c575480189eda299217755ca865eeb6ae194466ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564305418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf86932a8f93c327d502d4332caebe66c014460ef6eeec20e771fa775940d45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
CMD ["bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=C.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-num2words         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.buster_amd64.deb     && echo 'ea8277df4297afc507c61122f3c349af142f31e5 wkhtmltox.deb' | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=15.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=a2a8947448c8c561336f9b2710eeb9e9cbfdec66
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: ODOO_RELEASE=20240912 ODOO_SHA=a2a8947448c8c561336f9b2710eeb9e9cbfdec66
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: ODOO_RELEASE=20240912 ODOO_SHA=a2a8947448c8c561336f9b2710eeb9e9cbfdec66
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6e7b313a3ba91e62bd03020cd21c83c803d8aa42e337466182f77edd69092e`  
		Last Modified: Thu, 12 Sep 2024 18:58:29 GMT  
		Size: 220.3 MB (220283962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d7d30b4cf6449ed7efc619f61734a67cef7e44c5ae2fc1c5ae122f71edfcfa`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 2.4 MB (2387799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f7b16cfd74856b938e3773c3de7e9f4e9ec5f4e21ef816c1b99437147a889c`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 471.6 KB (471559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12530e1d160f390563c824aa8335e6274645f2a55cbb6228b85e752a4d74cb`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 309.7 MB (309730985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c294418a37344b6333b39972f6077f654e326278cbc9bd0cecca05a6a7bd39c3`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4505bad208f46251da340c73671d0977aed3b91b47b58b8eb6ae96ff75133c0`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1e9e466a9412dccd82e146631c96972e46a5153222295603e845ac85bf3e6b`  
		Last Modified: Thu, 12 Sep 2024 18:58:28 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4606973710f953561927e2e98fc26710a4466ce0c3f90a2c024c0bf7ed1f7f`  
		Last Modified: Thu, 12 Sep 2024 18:58:28 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:15.0-20240912` - unknown; unknown

```console
$ docker pull odoo@sha256:de713b61c5ddf07570010fcd6c191457c7d39e79bbe9c9d626ed753bbd214da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34711731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d370e01d4a0d27e9415cf089c8996921b7bed2b851deb1a9a3e76fd2ce6f499`

```dockerfile
```

-	Layers:
	-	`sha256:f6e5d66588f8ed69db87f8dccc9d6971d69c47cdd248450f56f3440bba5371f1`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 34.7 MB (34687100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f451a39351791b722b48d7931b33b52ad5dcc3261740f22e4e1b08fe1515fe6`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 24.6 KB (24631 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16`

```console
$ docker pull odoo@sha256:59cf13b0c60716fc8edacf252d1b6faa9a25998c56326f86e8916435ee3c4211
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:f398f6ea64051f1bdbba69b3722d4e4bfffe7a92f903139a1d79c3fda4180296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.1 MB (584099178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c2e3697b72ae1a7e5ddd9cbd5028cfbd90dd2d5c496b0f604a82bde48d2b02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
CMD ["bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=C.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=amd64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=16.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc08480c5a0516d9575c8a1cd6bbe34244f1400e6e04d80d1f4f32c5a289a758`  
		Last Modified: Thu, 12 Sep 2024 18:58:28 GMT  
		Size: 219.6 MB (219596755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced74ac6867698a6b0e44e4a83e027abe7a2a170871b98917328e6678cdddb98`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 2.4 MB (2391535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2253ac22f737479aff3bfaaa4d3eb695700f1a12e77c6118e8ef13c5a885a94`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 471.6 KB (471599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95335fd0fca5f3870592fff3ebab502b80db4052d5d9a7cba356ecdf935047ff`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 330.2 MB (330208176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51eb70403e4f6bb75c59ac7bc4a7e1c399f1bf987f6793b07457757501adf679`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b7aaaa61d1bad43aa32ccf7133a0a8446545b7cec321e2b75a8ec5e6c3f62c`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2585dedeb91eb2e8545c50cf0816ece276ce00cafca2bb1610e052588f48d`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0a08fcd2f8abee809f7863504badc0da9dbc3847008aea667681c42d959411`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:b0965b6448049e25e61d251386af3addfcbaee260fbe46e6ac862fbdd18b7b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38759250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51c23f784f6611cae6a7cf4166cc3614d1c353a6cb591ec6d62b88cd86885a8`

```dockerfile
```

-	Layers:
	-	`sha256:2f5ec1ffc6af61a4bdd9b73fd2c1160c3a90474dde022709d2b4f5bf7ad54a33`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 38.7 MB (38732709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7ee7e97f25d131e18dce1ab974eb2a19eb47e330a2e00327a11fa2cff977c3`  
		Last Modified: Thu, 12 Sep 2024 18:58:25 GMT  
		Size: 26.5 KB (26541 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ce65491d3c7369041fe81563f7760d83025edb3608e02d65eb0c2b3eaadce72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.7 MB (579716093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc8eeedef03ae17b1d5e5ff297409f2d145aa78e0f578136d54fcf2c9085660`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=C.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=arm64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=16.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9b80c0458b39dc7027bcd9267dcf9929f12d1fedc238c6d6e15f9f7d40ff71`  
		Last Modified: Thu, 12 Sep 2024 19:07:14 GMT  
		Size: 216.9 MB (216904671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbd148e585efaffa155ac66cc23a810a2891ccc6fa25f4cd0cf799205240a2d`  
		Last Modified: Thu, 12 Sep 2024 19:07:09 GMT  
		Size: 2.4 MB (2394072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0c8a757a358446584c7eca2e7086bec59701aa8bcd5cfedb083d165838c50b`  
		Last Modified: Thu, 12 Sep 2024 19:07:08 GMT  
		Size: 471.6 KB (471627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe4798c8502b4c9f4449c27b5c5fdb9bbfc53e4965bf7a6359295526f8edbdf`  
		Last Modified: Thu, 12 Sep 2024 19:07:16 GMT  
		Size: 329.9 MB (329868924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6266ec94d377a6149442360a41bd8cfa6482419f961fcd5134c7a7ed4744f44`  
		Last Modified: Thu, 12 Sep 2024 19:07:10 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5857f53b254f8e817f02ce349f92e3552b3a3689279e391690024d151554503`  
		Last Modified: Thu, 12 Sep 2024 19:07:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39335296e208bc103caed07b31750c8f3a73adc5643ead22d9992ed7b92ed02`  
		Last Modified: Thu, 12 Sep 2024 19:07:11 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b41993cdb5858d46b9aaba74f3195ff52ac62b00b7760d48f4cff54a4f134d`  
		Last Modified: Thu, 12 Sep 2024 19:07:11 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:c4e440ed32f131e139cb8de0eadc3ac1b951bba4538734f7a446b13ee1f0b568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38766019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033b89678954a9f20536bbc737d307df502379d21ff4fba7fd1f0d434f8314b7`

```dockerfile
```

-	Layers:
	-	`sha256:abfdeb00e320350de95c1fdb149d5ea798bc4d0fb1a633d0a258bdd37ade3c05`  
		Last Modified: Thu, 12 Sep 2024 19:07:10 GMT  
		Size: 38.7 MB (38739181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760660a7fce71f8f9db03e7b7acf5314d6bd572100e7f89f13cb9229be802928`  
		Last Modified: Thu, 12 Sep 2024 19:07:08 GMT  
		Size: 26.8 KB (26838 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; ppc64le

```console
$ docker pull odoo@sha256:e3c538fd6949a811dbf69ca87261ad022a3d7637d0aa115790894d89fb19f5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.6 MB (598635279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053d30b80c42ff57d0ac739d764c5bcbda61ee157e1cb59e07ebed3e8cb6c0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:18 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Wed, 04 Sep 2024 22:26:20 GMT
CMD ["bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=C.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=ppc64le
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=16.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264aada665692908c4b8983b6bd2091af357eff0993979937a76dd9f51763515`  
		Last Modified: Thu, 12 Sep 2024 19:13:34 GMT  
		Size: 228.6 MB (228590078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84873cb30f32fd9394fcb668bd9c9b11a80f9b18a085897cc396be0d1084f51`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 2.6 MB (2634243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98862cf91747046250cd694f3318708d65474d47ce91022946523da8edd7bf41`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 471.6 KB (471557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc029b4f723e58478d9506ddf3d4ca6d474c7ac551911ea285106d9fa581d55d`  
		Last Modified: Thu, 12 Sep 2024 19:13:48 GMT  
		Size: 331.6 MB (331637691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bace5122267de241bba6a38314257eadb211b691872afb028ed44c604009bb6`  
		Last Modified: Thu, 12 Sep 2024 19:13:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154b7510156feb936683f2394b9d436238972277af01f987927b0f09300d28bd`  
		Last Modified: Thu, 12 Sep 2024 19:13:29 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00aa6067311be4279fb85a69e20d182c305a52c1156b5290eb4c3be9461d799`  
		Last Modified: Thu, 12 Sep 2024 19:13:29 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c77468f5d738123779f53486e3beb56af3000d00bccb30d1352171331178f68`  
		Last Modified: Thu, 12 Sep 2024 19:13:30 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:71b9e60d77244a3f4bc9074910cd3a2f6b633cc06bd02595cb77a0d2b84a291f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38767379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6777c1223a39f76f5b306f1be2126885c0b833b5e4cc271955cee990459feb50`

```dockerfile
```

-	Layers:
	-	`sha256:0458baa3397cfb18667bac5c8e5e7130889d30eefe5475c81396cd03eddbafb1`  
		Last Modified: Thu, 12 Sep 2024 19:13:29 GMT  
		Size: 38.7 MB (38740787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f4721cc483763bac0a09db09170d39e658af8456f5983f27d5e25f944fc6e84`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:59cf13b0c60716fc8edacf252d1b6faa9a25998c56326f86e8916435ee3c4211
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:f398f6ea64051f1bdbba69b3722d4e4bfffe7a92f903139a1d79c3fda4180296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.1 MB (584099178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c2e3697b72ae1a7e5ddd9cbd5028cfbd90dd2d5c496b0f604a82bde48d2b02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
CMD ["bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=C.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=amd64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=16.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc08480c5a0516d9575c8a1cd6bbe34244f1400e6e04d80d1f4f32c5a289a758`  
		Last Modified: Thu, 12 Sep 2024 18:58:28 GMT  
		Size: 219.6 MB (219596755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced74ac6867698a6b0e44e4a83e027abe7a2a170871b98917328e6678cdddb98`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 2.4 MB (2391535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2253ac22f737479aff3bfaaa4d3eb695700f1a12e77c6118e8ef13c5a885a94`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 471.6 KB (471599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95335fd0fca5f3870592fff3ebab502b80db4052d5d9a7cba356ecdf935047ff`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 330.2 MB (330208176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51eb70403e4f6bb75c59ac7bc4a7e1c399f1bf987f6793b07457757501adf679`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b7aaaa61d1bad43aa32ccf7133a0a8446545b7cec321e2b75a8ec5e6c3f62c`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2585dedeb91eb2e8545c50cf0816ece276ce00cafca2bb1610e052588f48d`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0a08fcd2f8abee809f7863504badc0da9dbc3847008aea667681c42d959411`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b0965b6448049e25e61d251386af3addfcbaee260fbe46e6ac862fbdd18b7b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38759250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51c23f784f6611cae6a7cf4166cc3614d1c353a6cb591ec6d62b88cd86885a8`

```dockerfile
```

-	Layers:
	-	`sha256:2f5ec1ffc6af61a4bdd9b73fd2c1160c3a90474dde022709d2b4f5bf7ad54a33`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 38.7 MB (38732709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7ee7e97f25d131e18dce1ab974eb2a19eb47e330a2e00327a11fa2cff977c3`  
		Last Modified: Thu, 12 Sep 2024 18:58:25 GMT  
		Size: 26.5 KB (26541 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ce65491d3c7369041fe81563f7760d83025edb3608e02d65eb0c2b3eaadce72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.7 MB (579716093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc8eeedef03ae17b1d5e5ff297409f2d145aa78e0f578136d54fcf2c9085660`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=C.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=arm64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=16.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9b80c0458b39dc7027bcd9267dcf9929f12d1fedc238c6d6e15f9f7d40ff71`  
		Last Modified: Thu, 12 Sep 2024 19:07:14 GMT  
		Size: 216.9 MB (216904671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbd148e585efaffa155ac66cc23a810a2891ccc6fa25f4cd0cf799205240a2d`  
		Last Modified: Thu, 12 Sep 2024 19:07:09 GMT  
		Size: 2.4 MB (2394072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0c8a757a358446584c7eca2e7086bec59701aa8bcd5cfedb083d165838c50b`  
		Last Modified: Thu, 12 Sep 2024 19:07:08 GMT  
		Size: 471.6 KB (471627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe4798c8502b4c9f4449c27b5c5fdb9bbfc53e4965bf7a6359295526f8edbdf`  
		Last Modified: Thu, 12 Sep 2024 19:07:16 GMT  
		Size: 329.9 MB (329868924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6266ec94d377a6149442360a41bd8cfa6482419f961fcd5134c7a7ed4744f44`  
		Last Modified: Thu, 12 Sep 2024 19:07:10 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5857f53b254f8e817f02ce349f92e3552b3a3689279e391690024d151554503`  
		Last Modified: Thu, 12 Sep 2024 19:07:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39335296e208bc103caed07b31750c8f3a73adc5643ead22d9992ed7b92ed02`  
		Last Modified: Thu, 12 Sep 2024 19:07:11 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b41993cdb5858d46b9aaba74f3195ff52ac62b00b7760d48f4cff54a4f134d`  
		Last Modified: Thu, 12 Sep 2024 19:07:11 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c4e440ed32f131e139cb8de0eadc3ac1b951bba4538734f7a446b13ee1f0b568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38766019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033b89678954a9f20536bbc737d307df502379d21ff4fba7fd1f0d434f8314b7`

```dockerfile
```

-	Layers:
	-	`sha256:abfdeb00e320350de95c1fdb149d5ea798bc4d0fb1a633d0a258bdd37ade3c05`  
		Last Modified: Thu, 12 Sep 2024 19:07:10 GMT  
		Size: 38.7 MB (38739181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760660a7fce71f8f9db03e7b7acf5314d6bd572100e7f89f13cb9229be802928`  
		Last Modified: Thu, 12 Sep 2024 19:07:08 GMT  
		Size: 26.8 KB (26838 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:e3c538fd6949a811dbf69ca87261ad022a3d7637d0aa115790894d89fb19f5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.6 MB (598635279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053d30b80c42ff57d0ac739d764c5bcbda61ee157e1cb59e07ebed3e8cb6c0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:18 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Wed, 04 Sep 2024 22:26:20 GMT
CMD ["bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=C.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=ppc64le
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=16.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264aada665692908c4b8983b6bd2091af357eff0993979937a76dd9f51763515`  
		Last Modified: Thu, 12 Sep 2024 19:13:34 GMT  
		Size: 228.6 MB (228590078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84873cb30f32fd9394fcb668bd9c9b11a80f9b18a085897cc396be0d1084f51`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 2.6 MB (2634243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98862cf91747046250cd694f3318708d65474d47ce91022946523da8edd7bf41`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 471.6 KB (471557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc029b4f723e58478d9506ddf3d4ca6d474c7ac551911ea285106d9fa581d55d`  
		Last Modified: Thu, 12 Sep 2024 19:13:48 GMT  
		Size: 331.6 MB (331637691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bace5122267de241bba6a38314257eadb211b691872afb028ed44c604009bb6`  
		Last Modified: Thu, 12 Sep 2024 19:13:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154b7510156feb936683f2394b9d436238972277af01f987927b0f09300d28bd`  
		Last Modified: Thu, 12 Sep 2024 19:13:29 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00aa6067311be4279fb85a69e20d182c305a52c1156b5290eb4c3be9461d799`  
		Last Modified: Thu, 12 Sep 2024 19:13:29 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c77468f5d738123779f53486e3beb56af3000d00bccb30d1352171331178f68`  
		Last Modified: Thu, 12 Sep 2024 19:13:30 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:71b9e60d77244a3f4bc9074910cd3a2f6b633cc06bd02595cb77a0d2b84a291f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38767379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6777c1223a39f76f5b306f1be2126885c0b833b5e4cc271955cee990459feb50`

```dockerfile
```

-	Layers:
	-	`sha256:0458baa3397cfb18667bac5c8e5e7130889d30eefe5475c81396cd03eddbafb1`  
		Last Modified: Thu, 12 Sep 2024 19:13:29 GMT  
		Size: 38.7 MB (38740787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f4721cc483763bac0a09db09170d39e658af8456f5983f27d5e25f944fc6e84`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20240912`

```console
$ docker pull odoo@sha256:59cf13b0c60716fc8edacf252d1b6faa9a25998c56326f86e8916435ee3c4211
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:16.0-20240912` - linux; amd64

```console
$ docker pull odoo@sha256:f398f6ea64051f1bdbba69b3722d4e4bfffe7a92f903139a1d79c3fda4180296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.1 MB (584099178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c2e3697b72ae1a7e5ddd9cbd5028cfbd90dd2d5c496b0f604a82bde48d2b02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 22:31:09 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Wed, 04 Sep 2024 22:31:09 GMT
CMD ["bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=C.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=amd64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=16.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc08480c5a0516d9575c8a1cd6bbe34244f1400e6e04d80d1f4f32c5a289a758`  
		Last Modified: Thu, 12 Sep 2024 18:58:28 GMT  
		Size: 219.6 MB (219596755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced74ac6867698a6b0e44e4a83e027abe7a2a170871b98917328e6678cdddb98`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 2.4 MB (2391535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2253ac22f737479aff3bfaaa4d3eb695700f1a12e77c6118e8ef13c5a885a94`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 471.6 KB (471599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95335fd0fca5f3870592fff3ebab502b80db4052d5d9a7cba356ecdf935047ff`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 330.2 MB (330208176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51eb70403e4f6bb75c59ac7bc4a7e1c399f1bf987f6793b07457757501adf679`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b7aaaa61d1bad43aa32ccf7133a0a8446545b7cec321e2b75a8ec5e6c3f62c`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2585dedeb91eb2e8545c50cf0816ece276ce00cafca2bb1610e052588f48d`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0a08fcd2f8abee809f7863504badc0da9dbc3847008aea667681c42d959411`  
		Last Modified: Thu, 12 Sep 2024 18:58:27 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240912` - unknown; unknown

```console
$ docker pull odoo@sha256:b0965b6448049e25e61d251386af3addfcbaee260fbe46e6ac862fbdd18b7b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38759250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51c23f784f6611cae6a7cf4166cc3614d1c353a6cb591ec6d62b88cd86885a8`

```dockerfile
```

-	Layers:
	-	`sha256:2f5ec1ffc6af61a4bdd9b73fd2c1160c3a90474dde022709d2b4f5bf7ad54a33`  
		Last Modified: Thu, 12 Sep 2024 18:58:26 GMT  
		Size: 38.7 MB (38732709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7ee7e97f25d131e18dce1ab974eb2a19eb47e330a2e00327a11fa2cff977c3`  
		Last Modified: Thu, 12 Sep 2024 18:58:25 GMT  
		Size: 26.5 KB (26541 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240912` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ce65491d3c7369041fe81563f7760d83025edb3608e02d65eb0c2b3eaadce72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.7 MB (579716093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc8eeedef03ae17b1d5e5ff297409f2d145aa78e0f578136d54fcf2c9085660`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=C.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=arm64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=16.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9b80c0458b39dc7027bcd9267dcf9929f12d1fedc238c6d6e15f9f7d40ff71`  
		Last Modified: Thu, 12 Sep 2024 19:07:14 GMT  
		Size: 216.9 MB (216904671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbd148e585efaffa155ac66cc23a810a2891ccc6fa25f4cd0cf799205240a2d`  
		Last Modified: Thu, 12 Sep 2024 19:07:09 GMT  
		Size: 2.4 MB (2394072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0c8a757a358446584c7eca2e7086bec59701aa8bcd5cfedb083d165838c50b`  
		Last Modified: Thu, 12 Sep 2024 19:07:08 GMT  
		Size: 471.6 KB (471627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe4798c8502b4c9f4449c27b5c5fdb9bbfc53e4965bf7a6359295526f8edbdf`  
		Last Modified: Thu, 12 Sep 2024 19:07:16 GMT  
		Size: 329.9 MB (329868924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6266ec94d377a6149442360a41bd8cfa6482419f961fcd5134c7a7ed4744f44`  
		Last Modified: Thu, 12 Sep 2024 19:07:10 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5857f53b254f8e817f02ce349f92e3552b3a3689279e391690024d151554503`  
		Last Modified: Thu, 12 Sep 2024 19:07:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39335296e208bc103caed07b31750c8f3a73adc5643ead22d9992ed7b92ed02`  
		Last Modified: Thu, 12 Sep 2024 19:07:11 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b41993cdb5858d46b9aaba74f3195ff52ac62b00b7760d48f4cff54a4f134d`  
		Last Modified: Thu, 12 Sep 2024 19:07:11 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240912` - unknown; unknown

```console
$ docker pull odoo@sha256:c4e440ed32f131e139cb8de0eadc3ac1b951bba4538734f7a446b13ee1f0b568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38766019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033b89678954a9f20536bbc737d307df502379d21ff4fba7fd1f0d434f8314b7`

```dockerfile
```

-	Layers:
	-	`sha256:abfdeb00e320350de95c1fdb149d5ea798bc4d0fb1a633d0a258bdd37ade3c05`  
		Last Modified: Thu, 12 Sep 2024 19:07:10 GMT  
		Size: 38.7 MB (38739181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:760660a7fce71f8f9db03e7b7acf5314d6bd572100e7f89f13cb9229be802928`  
		Last Modified: Thu, 12 Sep 2024 19:07:08 GMT  
		Size: 26.8 KB (26838 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20240912` - linux; ppc64le

```console
$ docker pull odoo@sha256:e3c538fd6949a811dbf69ca87261ad022a3d7637d0aa115790894d89fb19f5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.6 MB (598635279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053d30b80c42ff57d0ac739d764c5bcbda61ee157e1cb59e07ebed3e8cb6c0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:18 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Wed, 04 Sep 2024 22:26:20 GMT
CMD ["bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=C.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=ppc64le
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=16.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=52fe9258f56d41d29851e2fd6a329effb741dae7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264aada665692908c4b8983b6bd2091af357eff0993979937a76dd9f51763515`  
		Last Modified: Thu, 12 Sep 2024 19:13:34 GMT  
		Size: 228.6 MB (228590078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84873cb30f32fd9394fcb668bd9c9b11a80f9b18a085897cc396be0d1084f51`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 2.6 MB (2634243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98862cf91747046250cd694f3318708d65474d47ce91022946523da8edd7bf41`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 471.6 KB (471557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc029b4f723e58478d9506ddf3d4ca6d474c7ac551911ea285106d9fa581d55d`  
		Last Modified: Thu, 12 Sep 2024 19:13:48 GMT  
		Size: 331.6 MB (331637691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bace5122267de241bba6a38314257eadb211b691872afb028ed44c604009bb6`  
		Last Modified: Thu, 12 Sep 2024 19:13:28 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154b7510156feb936683f2394b9d436238972277af01f987927b0f09300d28bd`  
		Last Modified: Thu, 12 Sep 2024 19:13:29 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00aa6067311be4279fb85a69e20d182c305a52c1156b5290eb4c3be9461d799`  
		Last Modified: Thu, 12 Sep 2024 19:13:29 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c77468f5d738123779f53486e3beb56af3000d00bccb30d1352171331178f68`  
		Last Modified: Thu, 12 Sep 2024 19:13:30 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20240912` - unknown; unknown

```console
$ docker pull odoo@sha256:71b9e60d77244a3f4bc9074910cd3a2f6b633cc06bd02595cb77a0d2b84a291f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38767379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6777c1223a39f76f5b306f1be2126885c0b833b5e4cc271955cee990459feb50`

```dockerfile
```

-	Layers:
	-	`sha256:0458baa3397cfb18667bac5c8e5e7130889d30eefe5475c81396cd03eddbafb1`  
		Last Modified: Thu, 12 Sep 2024 19:13:29 GMT  
		Size: 38.7 MB (38740787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f4721cc483763bac0a09db09170d39e658af8456f5983f27d5e25f944fc6e84`  
		Last Modified: Thu, 12 Sep 2024 19:13:27 GMT  
		Size: 26.6 KB (26592 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:d2fe034098978bba6d603b3a994a7e6d2ffe62219cd1c92bc974110d07d4b1d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:e34f2b32ae3ec542cea75f2b6823c3ef2811d6ea97cb26f3ca922f418ef1c408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597067381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9785ec55b41b38fec60054d5fbd60868ca62b382a1e440744f4e92b3f0dd89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=amd64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb00a467be04581de6d0ae3e8490555ceac416a6127b3dd10bd3aa03798eeb2d`  
		Last Modified: Tue, 17 Sep 2024 01:02:18 GMT  
		Size: 233.7 MB (233745038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de8307da804acac83f2511537bfb9247028ca64da151a7ec00c6c1a50b70ee`  
		Last Modified: Tue, 17 Sep 2024 01:02:13 GMT  
		Size: 2.3 MB (2315512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3cd6168060e79236d0001c446bc2c3de655e8887bd93cef47d38ac48d5b28c`  
		Last Modified: Tue, 17 Sep 2024 01:02:13 GMT  
		Size: 472.7 KB (472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213683c8a6bf0d18279e9d444300475266d1914ca10d4a095da64fa2871dde0`  
		Last Modified: Tue, 17 Sep 2024 01:02:20 GMT  
		Size: 331.0 MB (330996016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e760b719ca046e84ade9e4e77fc86eb5bac1204fd5cc5c675e906c06e4b7005`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d599f08f252a61d26e597082e6ea5102fa0f4535b521c4500ffc9a9d358b171`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139cd9ab1fe0b54ce18cac3bb4e32751a4cf4470d05cbcbdcf2d20f1604459d2`  
		Last Modified: Tue, 17 Sep 2024 01:02:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fa0ac3c34a78f6ba7217e1a3aba2a7b02a7c36357b89829614c7db8cf9fc9c`  
		Last Modified: Tue, 17 Sep 2024 01:02:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:fc6230d1ac6eb769cf751382bb23f9566a3e541981aa6ca18230392e66e3e084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39221438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e16388a4909b364fff0f7d96144f6d3f99588e164f387db9ec6bef408f42f78`

```dockerfile
```

-	Layers:
	-	`sha256:c99444a83c2a122c2ff0d1810f6453cd2947bec02cb7ad44a77c6925a0aed57c`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 39.2 MB (39194563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b072659bf65ec344e306b9bfcb37cc97af525a79ec1f73c9c65c5767b36f6afb`  
		Last Modified: Tue, 17 Sep 2024 01:02:12 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6611f5cd4c4ae8419cdeaf4ec46b8f23c6d326678fd468c6226c0f2ffb475736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 MB (591868851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce022a8be4133de08eafd2688f199b3ac09b10d085140009766a1f31170ed82a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=arm64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6fadc8f1cdeb7018f3cc730bf5ca5cbd765df35c38756be1faa743e1786be9`  
		Last Modified: Tue, 17 Sep 2024 02:44:10 GMT  
		Size: 231.1 MB (231120471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a152b990945175781adb341944cf665969d147ca436c8a7b53374779e6f6941`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 2.3 MB (2307685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb15fba7b3792bd150e5f11e817299c61abde876d36eedbebdebfe879e3a79`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 472.7 KB (472677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3dc0efa25020a1df1f02165d1ae8e54504881e43af46b33f1672199397667f`  
		Last Modified: Tue, 17 Sep 2024 02:44:11 GMT  
		Size: 330.6 MB (330607248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea0c48ec3b5d0f3ed92cee4e1a2efd7d4d49febec8a285fafb4b92979544dd0`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09f863e745cdbee42411248cd07033079da01761ae92a1e759d5391796f92c6`  
		Last Modified: Tue, 17 Sep 2024 02:44:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5e0c8f3a6fedcfba8dfe25297e2dde28433c647113b14ec50fcbd7f85a5c15`  
		Last Modified: Tue, 17 Sep 2024 02:44:06 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138850a8bb293831a1edd82ff2eb6c592b601ac7d1e519a934e96926a30768b`  
		Last Modified: Tue, 17 Sep 2024 02:44:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:7615a5b62b439b9ec7ca9e2e5ff48ebed15028069877699355956ec4cfffe372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39228264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4cf9f1b29ba9250c8bbebe0dfc04ee73b5c53371f60ad97fa92d00b2bdf348`

```dockerfile
```

-	Layers:
	-	`sha256:09ba83716c6a0b901ce631a4b8758c4339f5d1052c5a908f1979b3c7b9fdd7c0`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 39.2 MB (39201088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7972446f364fc62b55b326ba9c2d373cb39a93fb680e442bf576262bc1e2297e`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:787a8f72b46c6ab612133cd9b25832228997e307e0f7bcae00219b0563745402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.5 MB (613535529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1547286e09cca0c7ea3a41737f0be3f4fb8234f00926f442292b7a5294108707`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=ppc64le
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c02d58ebd6534d5afb5a8012d7003f978314b782a10cd19fbc0e6d5d58df3`  
		Last Modified: Tue, 17 Sep 2024 01:53:43 GMT  
		Size: 243.3 MB (243275613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67640bc9b4d0c0923eccbc39ae739c9f734354b3f58be66b9058c61be83d80`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 2.6 MB (2592233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdfb807d76c75fa16e7bed3d97c1200cb7778b2234fd4ebd57a60a93314315`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 472.7 KB (472652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c78e067de9022a0bd3d724ab7c3a3841af530da68cc046aa7dbc8b32781ada`  
		Last Modified: Tue, 17 Sep 2024 01:53:48 GMT  
		Size: 332.7 MB (332744345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2e863f289fa232c95ab4f1890b04ad695b45f7456d5b4caa5498f249936cc`  
		Last Modified: Tue, 17 Sep 2024 01:53:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab68b8d104879dbc336262260ea6eac356cd4ce0bc2b45a64939c8fdabfd437`  
		Last Modified: Tue, 17 Sep 2024 01:53:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd70b5e06a052e749e914910688b2b6d55d0005dd98dd55dde9073d11e1032b4`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5474009adf7ff1d592384e6e28fdffb03005ee888de7cd8ad193c3cfb7d0220f`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:78eab57ab6e792662a1f31603420132c8cc0adeb52776ff624ac7e9708d4fa97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39229807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b1efa18db0e2ba31828df77f5c6e1ac990131e251a409b8c385c241cbf5f5f`

```dockerfile
```

-	Layers:
	-	`sha256:4586ae5019aa9a909fc1bcadc06216ce30cb52e67a9f717a6ae9f5a3158edad0`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 39.2 MB (39202876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2f144d57bfe690352aba9618874ebbbd3d303c702426731c39660532912e88`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:d2fe034098978bba6d603b3a994a7e6d2ffe62219cd1c92bc974110d07d4b1d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:e34f2b32ae3ec542cea75f2b6823c3ef2811d6ea97cb26f3ca922f418ef1c408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597067381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9785ec55b41b38fec60054d5fbd60868ca62b382a1e440744f4e92b3f0dd89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=amd64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb00a467be04581de6d0ae3e8490555ceac416a6127b3dd10bd3aa03798eeb2d`  
		Last Modified: Tue, 17 Sep 2024 01:02:18 GMT  
		Size: 233.7 MB (233745038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de8307da804acac83f2511537bfb9247028ca64da151a7ec00c6c1a50b70ee`  
		Last Modified: Tue, 17 Sep 2024 01:02:13 GMT  
		Size: 2.3 MB (2315512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3cd6168060e79236d0001c446bc2c3de655e8887bd93cef47d38ac48d5b28c`  
		Last Modified: Tue, 17 Sep 2024 01:02:13 GMT  
		Size: 472.7 KB (472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213683c8a6bf0d18279e9d444300475266d1914ca10d4a095da64fa2871dde0`  
		Last Modified: Tue, 17 Sep 2024 01:02:20 GMT  
		Size: 331.0 MB (330996016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e760b719ca046e84ade9e4e77fc86eb5bac1204fd5cc5c675e906c06e4b7005`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d599f08f252a61d26e597082e6ea5102fa0f4535b521c4500ffc9a9d358b171`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139cd9ab1fe0b54ce18cac3bb4e32751a4cf4470d05cbcbdcf2d20f1604459d2`  
		Last Modified: Tue, 17 Sep 2024 01:02:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fa0ac3c34a78f6ba7217e1a3aba2a7b02a7c36357b89829614c7db8cf9fc9c`  
		Last Modified: Tue, 17 Sep 2024 01:02:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:fc6230d1ac6eb769cf751382bb23f9566a3e541981aa6ca18230392e66e3e084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39221438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e16388a4909b364fff0f7d96144f6d3f99588e164f387db9ec6bef408f42f78`

```dockerfile
```

-	Layers:
	-	`sha256:c99444a83c2a122c2ff0d1810f6453cd2947bec02cb7ad44a77c6925a0aed57c`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 39.2 MB (39194563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b072659bf65ec344e306b9bfcb37cc97af525a79ec1f73c9c65c5767b36f6afb`  
		Last Modified: Tue, 17 Sep 2024 01:02:12 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6611f5cd4c4ae8419cdeaf4ec46b8f23c6d326678fd468c6226c0f2ffb475736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 MB (591868851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce022a8be4133de08eafd2688f199b3ac09b10d085140009766a1f31170ed82a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=arm64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6fadc8f1cdeb7018f3cc730bf5ca5cbd765df35c38756be1faa743e1786be9`  
		Last Modified: Tue, 17 Sep 2024 02:44:10 GMT  
		Size: 231.1 MB (231120471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a152b990945175781adb341944cf665969d147ca436c8a7b53374779e6f6941`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 2.3 MB (2307685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb15fba7b3792bd150e5f11e817299c61abde876d36eedbebdebfe879e3a79`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 472.7 KB (472677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3dc0efa25020a1df1f02165d1ae8e54504881e43af46b33f1672199397667f`  
		Last Modified: Tue, 17 Sep 2024 02:44:11 GMT  
		Size: 330.6 MB (330607248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea0c48ec3b5d0f3ed92cee4e1a2efd7d4d49febec8a285fafb4b92979544dd0`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09f863e745cdbee42411248cd07033079da01761ae92a1e759d5391796f92c6`  
		Last Modified: Tue, 17 Sep 2024 02:44:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5e0c8f3a6fedcfba8dfe25297e2dde28433c647113b14ec50fcbd7f85a5c15`  
		Last Modified: Tue, 17 Sep 2024 02:44:06 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138850a8bb293831a1edd82ff2eb6c592b601ac7d1e519a934e96926a30768b`  
		Last Modified: Tue, 17 Sep 2024 02:44:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7615a5b62b439b9ec7ca9e2e5ff48ebed15028069877699355956ec4cfffe372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39228264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4cf9f1b29ba9250c8bbebe0dfc04ee73b5c53371f60ad97fa92d00b2bdf348`

```dockerfile
```

-	Layers:
	-	`sha256:09ba83716c6a0b901ce631a4b8758c4339f5d1052c5a908f1979b3c7b9fdd7c0`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 39.2 MB (39201088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7972446f364fc62b55b326ba9c2d373cb39a93fb680e442bf576262bc1e2297e`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:787a8f72b46c6ab612133cd9b25832228997e307e0f7bcae00219b0563745402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.5 MB (613535529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1547286e09cca0c7ea3a41737f0be3f4fb8234f00926f442292b7a5294108707`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=ppc64le
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c02d58ebd6534d5afb5a8012d7003f978314b782a10cd19fbc0e6d5d58df3`  
		Last Modified: Tue, 17 Sep 2024 01:53:43 GMT  
		Size: 243.3 MB (243275613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67640bc9b4d0c0923eccbc39ae739c9f734354b3f58be66b9058c61be83d80`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 2.6 MB (2592233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdfb807d76c75fa16e7bed3d97c1200cb7778b2234fd4ebd57a60a93314315`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 472.7 KB (472652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c78e067de9022a0bd3d724ab7c3a3841af530da68cc046aa7dbc8b32781ada`  
		Last Modified: Tue, 17 Sep 2024 01:53:48 GMT  
		Size: 332.7 MB (332744345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2e863f289fa232c95ab4f1890b04ad695b45f7456d5b4caa5498f249936cc`  
		Last Modified: Tue, 17 Sep 2024 01:53:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab68b8d104879dbc336262260ea6eac356cd4ce0bc2b45a64939c8fdabfd437`  
		Last Modified: Tue, 17 Sep 2024 01:53:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd70b5e06a052e749e914910688b2b6d55d0005dd98dd55dde9073d11e1032b4`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5474009adf7ff1d592384e6e28fdffb03005ee888de7cd8ad193c3cfb7d0220f`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:78eab57ab6e792662a1f31603420132c8cc0adeb52776ff624ac7e9708d4fa97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39229807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b1efa18db0e2ba31828df77f5c6e1ac990131e251a409b8c385c241cbf5f5f`

```dockerfile
```

-	Layers:
	-	`sha256:4586ae5019aa9a909fc1bcadc06216ce30cb52e67a9f717a6ae9f5a3158edad0`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 39.2 MB (39202876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2f144d57bfe690352aba9618874ebbbd3d303c702426731c39660532912e88`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240912`

```console
$ docker pull odoo@sha256:d2fe034098978bba6d603b3a994a7e6d2ffe62219cd1c92bc974110d07d4b1d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20240912` - linux; amd64

```console
$ docker pull odoo@sha256:e34f2b32ae3ec542cea75f2b6823c3ef2811d6ea97cb26f3ca922f418ef1c408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597067381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9785ec55b41b38fec60054d5fbd60868ca62b382a1e440744f4e92b3f0dd89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=amd64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb00a467be04581de6d0ae3e8490555ceac416a6127b3dd10bd3aa03798eeb2d`  
		Last Modified: Tue, 17 Sep 2024 01:02:18 GMT  
		Size: 233.7 MB (233745038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de8307da804acac83f2511537bfb9247028ca64da151a7ec00c6c1a50b70ee`  
		Last Modified: Tue, 17 Sep 2024 01:02:13 GMT  
		Size: 2.3 MB (2315512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3cd6168060e79236d0001c446bc2c3de655e8887bd93cef47d38ac48d5b28c`  
		Last Modified: Tue, 17 Sep 2024 01:02:13 GMT  
		Size: 472.7 KB (472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213683c8a6bf0d18279e9d444300475266d1914ca10d4a095da64fa2871dde0`  
		Last Modified: Tue, 17 Sep 2024 01:02:20 GMT  
		Size: 331.0 MB (330996016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e760b719ca046e84ade9e4e77fc86eb5bac1204fd5cc5c675e906c06e4b7005`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d599f08f252a61d26e597082e6ea5102fa0f4535b521c4500ffc9a9d358b171`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139cd9ab1fe0b54ce18cac3bb4e32751a4cf4470d05cbcbdcf2d20f1604459d2`  
		Last Modified: Tue, 17 Sep 2024 01:02:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fa0ac3c34a78f6ba7217e1a3aba2a7b02a7c36357b89829614c7db8cf9fc9c`  
		Last Modified: Tue, 17 Sep 2024 01:02:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240912` - unknown; unknown

```console
$ docker pull odoo@sha256:fc6230d1ac6eb769cf751382bb23f9566a3e541981aa6ca18230392e66e3e084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39221438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e16388a4909b364fff0f7d96144f6d3f99588e164f387db9ec6bef408f42f78`

```dockerfile
```

-	Layers:
	-	`sha256:c99444a83c2a122c2ff0d1810f6453cd2947bec02cb7ad44a77c6925a0aed57c`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 39.2 MB (39194563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b072659bf65ec344e306b9bfcb37cc97af525a79ec1f73c9c65c5767b36f6afb`  
		Last Modified: Tue, 17 Sep 2024 01:02:12 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240912` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6611f5cd4c4ae8419cdeaf4ec46b8f23c6d326678fd468c6226c0f2ffb475736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 MB (591868851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce022a8be4133de08eafd2688f199b3ac09b10d085140009766a1f31170ed82a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=arm64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6fadc8f1cdeb7018f3cc730bf5ca5cbd765df35c38756be1faa743e1786be9`  
		Last Modified: Tue, 17 Sep 2024 02:44:10 GMT  
		Size: 231.1 MB (231120471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a152b990945175781adb341944cf665969d147ca436c8a7b53374779e6f6941`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 2.3 MB (2307685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb15fba7b3792bd150e5f11e817299c61abde876d36eedbebdebfe879e3a79`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 472.7 KB (472677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3dc0efa25020a1df1f02165d1ae8e54504881e43af46b33f1672199397667f`  
		Last Modified: Tue, 17 Sep 2024 02:44:11 GMT  
		Size: 330.6 MB (330607248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea0c48ec3b5d0f3ed92cee4e1a2efd7d4d49febec8a285fafb4b92979544dd0`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09f863e745cdbee42411248cd07033079da01761ae92a1e759d5391796f92c6`  
		Last Modified: Tue, 17 Sep 2024 02:44:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5e0c8f3a6fedcfba8dfe25297e2dde28433c647113b14ec50fcbd7f85a5c15`  
		Last Modified: Tue, 17 Sep 2024 02:44:06 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138850a8bb293831a1edd82ff2eb6c592b601ac7d1e519a934e96926a30768b`  
		Last Modified: Tue, 17 Sep 2024 02:44:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240912` - unknown; unknown

```console
$ docker pull odoo@sha256:7615a5b62b439b9ec7ca9e2e5ff48ebed15028069877699355956ec4cfffe372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39228264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4cf9f1b29ba9250c8bbebe0dfc04ee73b5c53371f60ad97fa92d00b2bdf348`

```dockerfile
```

-	Layers:
	-	`sha256:09ba83716c6a0b901ce631a4b8758c4339f5d1052c5a908f1979b3c7b9fdd7c0`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 39.2 MB (39201088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7972446f364fc62b55b326ba9c2d373cb39a93fb680e442bf576262bc1e2297e`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240912` - linux; ppc64le

```console
$ docker pull odoo@sha256:787a8f72b46c6ab612133cd9b25832228997e307e0f7bcae00219b0563745402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.5 MB (613535529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1547286e09cca0c7ea3a41737f0be3f4fb8234f00926f442292b7a5294108707`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=ppc64le
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c02d58ebd6534d5afb5a8012d7003f978314b782a10cd19fbc0e6d5d58df3`  
		Last Modified: Tue, 17 Sep 2024 01:53:43 GMT  
		Size: 243.3 MB (243275613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67640bc9b4d0c0923eccbc39ae739c9f734354b3f58be66b9058c61be83d80`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 2.6 MB (2592233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdfb807d76c75fa16e7bed3d97c1200cb7778b2234fd4ebd57a60a93314315`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 472.7 KB (472652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c78e067de9022a0bd3d724ab7c3a3841af530da68cc046aa7dbc8b32781ada`  
		Last Modified: Tue, 17 Sep 2024 01:53:48 GMT  
		Size: 332.7 MB (332744345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2e863f289fa232c95ab4f1890b04ad695b45f7456d5b4caa5498f249936cc`  
		Last Modified: Tue, 17 Sep 2024 01:53:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab68b8d104879dbc336262260ea6eac356cd4ce0bc2b45a64939c8fdabfd437`  
		Last Modified: Tue, 17 Sep 2024 01:53:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd70b5e06a052e749e914910688b2b6d55d0005dd98dd55dde9073d11e1032b4`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5474009adf7ff1d592384e6e28fdffb03005ee888de7cd8ad193c3cfb7d0220f`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240912` - unknown; unknown

```console
$ docker pull odoo@sha256:78eab57ab6e792662a1f31603420132c8cc0adeb52776ff624ac7e9708d4fa97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39229807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b1efa18db0e2ba31828df77f5c6e1ac990131e251a409b8c385c241cbf5f5f`

```dockerfile
```

-	Layers:
	-	`sha256:4586ae5019aa9a909fc1bcadc06216ce30cb52e67a9f717a6ae9f5a3158edad0`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 39.2 MB (39202876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2f144d57bfe690352aba9618874ebbbd3d303c702426731c39660532912e88`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:d2fe034098978bba6d603b3a994a7e6d2ffe62219cd1c92bc974110d07d4b1d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:e34f2b32ae3ec542cea75f2b6823c3ef2811d6ea97cb26f3ca922f418ef1c408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597067381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9785ec55b41b38fec60054d5fbd60868ca62b382a1e440744f4e92b3f0dd89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=amd64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb00a467be04581de6d0ae3e8490555ceac416a6127b3dd10bd3aa03798eeb2d`  
		Last Modified: Tue, 17 Sep 2024 01:02:18 GMT  
		Size: 233.7 MB (233745038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de8307da804acac83f2511537bfb9247028ca64da151a7ec00c6c1a50b70ee`  
		Last Modified: Tue, 17 Sep 2024 01:02:13 GMT  
		Size: 2.3 MB (2315512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3cd6168060e79236d0001c446bc2c3de655e8887bd93cef47d38ac48d5b28c`  
		Last Modified: Tue, 17 Sep 2024 01:02:13 GMT  
		Size: 472.7 KB (472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213683c8a6bf0d18279e9d444300475266d1914ca10d4a095da64fa2871dde0`  
		Last Modified: Tue, 17 Sep 2024 01:02:20 GMT  
		Size: 331.0 MB (330996016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e760b719ca046e84ade9e4e77fc86eb5bac1204fd5cc5c675e906c06e4b7005`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d599f08f252a61d26e597082e6ea5102fa0f4535b521c4500ffc9a9d358b171`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139cd9ab1fe0b54ce18cac3bb4e32751a4cf4470d05cbcbdcf2d20f1604459d2`  
		Last Modified: Tue, 17 Sep 2024 01:02:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fa0ac3c34a78f6ba7217e1a3aba2a7b02a7c36357b89829614c7db8cf9fc9c`  
		Last Modified: Tue, 17 Sep 2024 01:02:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:fc6230d1ac6eb769cf751382bb23f9566a3e541981aa6ca18230392e66e3e084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39221438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e16388a4909b364fff0f7d96144f6d3f99588e164f387db9ec6bef408f42f78`

```dockerfile
```

-	Layers:
	-	`sha256:c99444a83c2a122c2ff0d1810f6453cd2947bec02cb7ad44a77c6925a0aed57c`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 39.2 MB (39194563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b072659bf65ec344e306b9bfcb37cc97af525a79ec1f73c9c65c5767b36f6afb`  
		Last Modified: Tue, 17 Sep 2024 01:02:12 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6611f5cd4c4ae8419cdeaf4ec46b8f23c6d326678fd468c6226c0f2ffb475736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 MB (591868851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce022a8be4133de08eafd2688f199b3ac09b10d085140009766a1f31170ed82a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=arm64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6fadc8f1cdeb7018f3cc730bf5ca5cbd765df35c38756be1faa743e1786be9`  
		Last Modified: Tue, 17 Sep 2024 02:44:10 GMT  
		Size: 231.1 MB (231120471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a152b990945175781adb341944cf665969d147ca436c8a7b53374779e6f6941`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 2.3 MB (2307685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb15fba7b3792bd150e5f11e817299c61abde876d36eedbebdebfe879e3a79`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 472.7 KB (472677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3dc0efa25020a1df1f02165d1ae8e54504881e43af46b33f1672199397667f`  
		Last Modified: Tue, 17 Sep 2024 02:44:11 GMT  
		Size: 330.6 MB (330607248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea0c48ec3b5d0f3ed92cee4e1a2efd7d4d49febec8a285fafb4b92979544dd0`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09f863e745cdbee42411248cd07033079da01761ae92a1e759d5391796f92c6`  
		Last Modified: Tue, 17 Sep 2024 02:44:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5e0c8f3a6fedcfba8dfe25297e2dde28433c647113b14ec50fcbd7f85a5c15`  
		Last Modified: Tue, 17 Sep 2024 02:44:06 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138850a8bb293831a1edd82ff2eb6c592b601ac7d1e519a934e96926a30768b`  
		Last Modified: Tue, 17 Sep 2024 02:44:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7615a5b62b439b9ec7ca9e2e5ff48ebed15028069877699355956ec4cfffe372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39228264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4cf9f1b29ba9250c8bbebe0dfc04ee73b5c53371f60ad97fa92d00b2bdf348`

```dockerfile
```

-	Layers:
	-	`sha256:09ba83716c6a0b901ce631a4b8758c4339f5d1052c5a908f1979b3c7b9fdd7c0`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 39.2 MB (39201088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7972446f364fc62b55b326ba9c2d373cb39a93fb680e442bf576262bc1e2297e`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:787a8f72b46c6ab612133cd9b25832228997e307e0f7bcae00219b0563745402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.5 MB (613535529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1547286e09cca0c7ea3a41737f0be3f4fb8234f00926f442292b7a5294108707`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=ppc64le
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c02d58ebd6534d5afb5a8012d7003f978314b782a10cd19fbc0e6d5d58df3`  
		Last Modified: Tue, 17 Sep 2024 01:53:43 GMT  
		Size: 243.3 MB (243275613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67640bc9b4d0c0923eccbc39ae739c9f734354b3f58be66b9058c61be83d80`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 2.6 MB (2592233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdfb807d76c75fa16e7bed3d97c1200cb7778b2234fd4ebd57a60a93314315`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 472.7 KB (472652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c78e067de9022a0bd3d724ab7c3a3841af530da68cc046aa7dbc8b32781ada`  
		Last Modified: Tue, 17 Sep 2024 01:53:48 GMT  
		Size: 332.7 MB (332744345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2e863f289fa232c95ab4f1890b04ad695b45f7456d5b4caa5498f249936cc`  
		Last Modified: Tue, 17 Sep 2024 01:53:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab68b8d104879dbc336262260ea6eac356cd4ce0bc2b45a64939c8fdabfd437`  
		Last Modified: Tue, 17 Sep 2024 01:53:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd70b5e06a052e749e914910688b2b6d55d0005dd98dd55dde9073d11e1032b4`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5474009adf7ff1d592384e6e28fdffb03005ee888de7cd8ad193c3cfb7d0220f`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:78eab57ab6e792662a1f31603420132c8cc0adeb52776ff624ac7e9708d4fa97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39229807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b1efa18db0e2ba31828df77f5c6e1ac990131e251a409b8c385c241cbf5f5f`

```dockerfile
```

-	Layers:
	-	`sha256:4586ae5019aa9a909fc1bcadc06216ce30cb52e67a9f717a6ae9f5a3158edad0`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 39.2 MB (39202876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2f144d57bfe690352aba9618874ebbbd3d303c702426731c39660532912e88`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json
