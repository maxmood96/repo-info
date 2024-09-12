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
$ docker pull odoo@sha256:320de8e10ba44deebb499558f77d629f360b2c07a83e2f18de2538aac0e74a85
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
$ docker pull odoo@sha256:3e31a6f0907810ca94fdc17a013bd35826244426f336494104380a7dc5457ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.3 MB (599341915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c2851a558b18a90bb3467e4592c3b4a04a11dd33cc1cb3a0a7fa869560801a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1bd98a16cd3c673442e42f498f34773b48215de497686e6acc81a9294f0223`  
		Last Modified: Thu, 12 Sep 2024 18:58:33 GMT  
		Size: 236.0 MB (236020111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd06af45a76ed21953cdc99630ea6430082536c4d38a87c3806abd7768d892c`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 2.3 MB (2315842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e11a03d0dd12d8602f087f237fafc2de5eccd67c8776afc325372609d7fab3`  
		Last Modified: Thu, 12 Sep 2024 18:58:29 GMT  
		Size: 472.7 KB (472658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316a71c45c59a37cd3e08cd75d04e4b4a61349c7f1fe288badc25f1eb0efc236`  
		Last Modified: Thu, 12 Sep 2024 18:58:34 GMT  
		Size: 331.0 MB (330994838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfaed02607a202b6a5d86efe5cf9383b86ffcb674fead383446c89398b857ee`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c601410b0451ea4989c9c1bd02cdffcfeff35f6c2aa0a495e0a227a43ca43b4d`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dfd04f21d82c0713fec7b5f92cf208a45815c7a847b97970b97b1465d30547`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47be89bacb3a8671657632155a8c29c4750e2d09d0f9e114e80d7a91d44263af`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:23368febc6185c548f3ffb7d069a904931b60795d7e70f487a1cc6321e7980da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39221438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07b6c79c2928600c2db426511dd41bea2544c6be036043ebc7f31a8687a6dd2`

```dockerfile
```

-	Layers:
	-	`sha256:b37a948afbcb743494949c16be302606ccb7561dd1185b1608c6fa45edfe0600`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 39.2 MB (39194563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47343839d9f44ba64f29ae541c7bea27810e0e416e179eb5fce1ea08b675842b`  
		Last Modified: Thu, 12 Sep 2024 18:58:29 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a0ccf2aaaa2a7d6f084c5ee717f460e3e192379a80ca766ea77210604a47b64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.0 MB (594010797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f74e824859d8431a71332102f80a5030e4fe26ce5e7a9efc29391e8913ebec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
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
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec7e5187a062fd4ad8ee4eeb36f6eacf4bdea2e954b894018d62db463b7d9c1`  
		Last Modified: Thu, 12 Sep 2024 19:03:18 GMT  
		Size: 233.3 MB (233262427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3f1b034194bf5fcb4b8db7adb4927c95bc4d15c13fbe8004ae7efdb9187525`  
		Last Modified: Thu, 12 Sep 2024 19:03:13 GMT  
		Size: 2.3 MB (2307954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5263151f33f3f8c573ce7749dd7936c5e8eb9b4f25fc8d1e4bfb932bb6da8d`  
		Last Modified: Thu, 12 Sep 2024 19:03:13 GMT  
		Size: 472.6 KB (472644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a5c8e272339d2ada416e22e16fedc399a7554d6e9d6a6390726fff20fc8263`  
		Last Modified: Thu, 12 Sep 2024 19:03:20 GMT  
		Size: 330.6 MB (330606647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2003abd496c3f4d3d68536561854609d5ae088f65f2a53c24694d1326069e9e`  
		Last Modified: Thu, 12 Sep 2024 19:03:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f19a25b0133965dac6d5502fb0ae2d8fd6d552713c7a47d9be1deb6ddc2b55`  
		Last Modified: Thu, 12 Sep 2024 19:03:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dfa65ea650974cb4118e7d73bc06556c1b9b07d26e9fa371e165a7e9b8c715`  
		Last Modified: Thu, 12 Sep 2024 19:03:15 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe590702e0ef35d1f23a843afe197a55b99f099cee640b70bc3c463090c2f88e`  
		Last Modified: Thu, 12 Sep 2024 19:03:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:f342a52944ea2573857840f0f94c2bf2beef3ee550aaa1b21eee27ff75603bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39228264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b259c0c73c781b4f591ead5adf4b52462d0c9828367e04d6789d414c1430972`

```dockerfile
```

-	Layers:
	-	`sha256:9a17ef8c0dba22a090873ff2bca538bb3de1a577bed63ecddccdb0e96043af6e`  
		Last Modified: Thu, 12 Sep 2024 19:03:14 GMT  
		Size: 39.2 MB (39201088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35baaf1c61b02e32c6351591e8bf27a963f5f54048d9b7f9c52efda8698d4803`  
		Last Modified: Thu, 12 Sep 2024 19:03:12 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:4a72c4ccaa385487d132a4076ac7f4cdb23aabf3cf50d19f29cd0d4ef817b4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616168802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123a3645a2187a819020ec785ae778b49554f3dc162b7f7dc64403d1901e7172`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
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
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742703807fc36fed2a4242cea37ea0db0d517ecee5c2bb3b38083f9eeb9547d4`  
		Last Modified: Thu, 12 Sep 2024 19:04:42 GMT  
		Size: 245.9 MB (245900526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31729801a5ce405e76357b4ecc0288ab08f50d7532b6f5dec0c2f5130e456945`  
		Last Modified: Thu, 12 Sep 2024 19:04:25 GMT  
		Size: 2.6 MB (2592523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741ddf3cfee38ddf211aa3a5a0d6ddb9d5b93e38b46d76b9062b2db0ffd2502f`  
		Last Modified: Thu, 12 Sep 2024 19:04:25 GMT  
		Size: 472.8 KB (472763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cfb027a23d4a841895e8637a649bf4c904b71084f1c367310f66a6bd5241fd`  
		Last Modified: Thu, 12 Sep 2024 19:04:48 GMT  
		Size: 332.7 MB (332736373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7249df6a5a9bb2dd3cdf337be4ddd9df4adcb153242572f2adb0abac09618fb`  
		Last Modified: Thu, 12 Sep 2024 19:04:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6ab86f35c08574a071839b4a0951ef737f55c824c0f2569e91808f6e0bceb`  
		Last Modified: Thu, 12 Sep 2024 19:04:26 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a4bc86081e705301d725e6f24ddfb29b69ca4674ffaa66cf6534f893c63d28`  
		Last Modified: Thu, 12 Sep 2024 19:04:27 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ec3ac122fbcb07ab5ba16a84723f363956e55797b47f087823537a1ba19f63`  
		Last Modified: Thu, 12 Sep 2024 19:04:27 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:b4f03dd2d8ae83e3c688cd5d7a029cb3ee551185c04a9de81fdeb001caa88cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39229807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bcfff7920ade9d19a762d0eaed4d136380957c97dcceb7e228a8ca644acebaa`

```dockerfile
```

-	Layers:
	-	`sha256:5cb1b9142f1cbfba369b500c993dca8151955b89a13cfb7ba257b7ebbf89390c`  
		Last Modified: Thu, 12 Sep 2024 19:04:27 GMT  
		Size: 39.2 MB (39202876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06596df18cd14fe7c826e9c9202bcb565140e23d3ca1a63dd014fcb53e6816c`  
		Last Modified: Thu, 12 Sep 2024 19:04:25 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:320de8e10ba44deebb499558f77d629f360b2c07a83e2f18de2538aac0e74a85
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
$ docker pull odoo@sha256:3e31a6f0907810ca94fdc17a013bd35826244426f336494104380a7dc5457ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.3 MB (599341915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c2851a558b18a90bb3467e4592c3b4a04a11dd33cc1cb3a0a7fa869560801a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1bd98a16cd3c673442e42f498f34773b48215de497686e6acc81a9294f0223`  
		Last Modified: Thu, 12 Sep 2024 18:58:33 GMT  
		Size: 236.0 MB (236020111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd06af45a76ed21953cdc99630ea6430082536c4d38a87c3806abd7768d892c`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 2.3 MB (2315842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e11a03d0dd12d8602f087f237fafc2de5eccd67c8776afc325372609d7fab3`  
		Last Modified: Thu, 12 Sep 2024 18:58:29 GMT  
		Size: 472.7 KB (472658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316a71c45c59a37cd3e08cd75d04e4b4a61349c7f1fe288badc25f1eb0efc236`  
		Last Modified: Thu, 12 Sep 2024 18:58:34 GMT  
		Size: 331.0 MB (330994838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfaed02607a202b6a5d86efe5cf9383b86ffcb674fead383446c89398b857ee`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c601410b0451ea4989c9c1bd02cdffcfeff35f6c2aa0a495e0a227a43ca43b4d`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dfd04f21d82c0713fec7b5f92cf208a45815c7a847b97970b97b1465d30547`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47be89bacb3a8671657632155a8c29c4750e2d09d0f9e114e80d7a91d44263af`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:23368febc6185c548f3ffb7d069a904931b60795d7e70f487a1cc6321e7980da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39221438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07b6c79c2928600c2db426511dd41bea2544c6be036043ebc7f31a8687a6dd2`

```dockerfile
```

-	Layers:
	-	`sha256:b37a948afbcb743494949c16be302606ccb7561dd1185b1608c6fa45edfe0600`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 39.2 MB (39194563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47343839d9f44ba64f29ae541c7bea27810e0e416e179eb5fce1ea08b675842b`  
		Last Modified: Thu, 12 Sep 2024 18:58:29 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a0ccf2aaaa2a7d6f084c5ee717f460e3e192379a80ca766ea77210604a47b64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.0 MB (594010797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f74e824859d8431a71332102f80a5030e4fe26ce5e7a9efc29391e8913ebec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
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
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec7e5187a062fd4ad8ee4eeb36f6eacf4bdea2e954b894018d62db463b7d9c1`  
		Last Modified: Thu, 12 Sep 2024 19:03:18 GMT  
		Size: 233.3 MB (233262427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3f1b034194bf5fcb4b8db7adb4927c95bc4d15c13fbe8004ae7efdb9187525`  
		Last Modified: Thu, 12 Sep 2024 19:03:13 GMT  
		Size: 2.3 MB (2307954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5263151f33f3f8c573ce7749dd7936c5e8eb9b4f25fc8d1e4bfb932bb6da8d`  
		Last Modified: Thu, 12 Sep 2024 19:03:13 GMT  
		Size: 472.6 KB (472644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a5c8e272339d2ada416e22e16fedc399a7554d6e9d6a6390726fff20fc8263`  
		Last Modified: Thu, 12 Sep 2024 19:03:20 GMT  
		Size: 330.6 MB (330606647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2003abd496c3f4d3d68536561854609d5ae088f65f2a53c24694d1326069e9e`  
		Last Modified: Thu, 12 Sep 2024 19:03:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f19a25b0133965dac6d5502fb0ae2d8fd6d552713c7a47d9be1deb6ddc2b55`  
		Last Modified: Thu, 12 Sep 2024 19:03:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dfa65ea650974cb4118e7d73bc06556c1b9b07d26e9fa371e165a7e9b8c715`  
		Last Modified: Thu, 12 Sep 2024 19:03:15 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe590702e0ef35d1f23a843afe197a55b99f099cee640b70bc3c463090c2f88e`  
		Last Modified: Thu, 12 Sep 2024 19:03:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f342a52944ea2573857840f0f94c2bf2beef3ee550aaa1b21eee27ff75603bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39228264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b259c0c73c781b4f591ead5adf4b52462d0c9828367e04d6789d414c1430972`

```dockerfile
```

-	Layers:
	-	`sha256:9a17ef8c0dba22a090873ff2bca538bb3de1a577bed63ecddccdb0e96043af6e`  
		Last Modified: Thu, 12 Sep 2024 19:03:14 GMT  
		Size: 39.2 MB (39201088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35baaf1c61b02e32c6351591e8bf27a963f5f54048d9b7f9c52efda8698d4803`  
		Last Modified: Thu, 12 Sep 2024 19:03:12 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:4a72c4ccaa385487d132a4076ac7f4cdb23aabf3cf50d19f29cd0d4ef817b4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616168802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123a3645a2187a819020ec785ae778b49554f3dc162b7f7dc64403d1901e7172`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
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
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742703807fc36fed2a4242cea37ea0db0d517ecee5c2bb3b38083f9eeb9547d4`  
		Last Modified: Thu, 12 Sep 2024 19:04:42 GMT  
		Size: 245.9 MB (245900526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31729801a5ce405e76357b4ecc0288ab08f50d7532b6f5dec0c2f5130e456945`  
		Last Modified: Thu, 12 Sep 2024 19:04:25 GMT  
		Size: 2.6 MB (2592523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741ddf3cfee38ddf211aa3a5a0d6ddb9d5b93e38b46d76b9062b2db0ffd2502f`  
		Last Modified: Thu, 12 Sep 2024 19:04:25 GMT  
		Size: 472.8 KB (472763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cfb027a23d4a841895e8637a649bf4c904b71084f1c367310f66a6bd5241fd`  
		Last Modified: Thu, 12 Sep 2024 19:04:48 GMT  
		Size: 332.7 MB (332736373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7249df6a5a9bb2dd3cdf337be4ddd9df4adcb153242572f2adb0abac09618fb`  
		Last Modified: Thu, 12 Sep 2024 19:04:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6ab86f35c08574a071839b4a0951ef737f55c824c0f2569e91808f6e0bceb`  
		Last Modified: Thu, 12 Sep 2024 19:04:26 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a4bc86081e705301d725e6f24ddfb29b69ca4674ffaa66cf6534f893c63d28`  
		Last Modified: Thu, 12 Sep 2024 19:04:27 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ec3ac122fbcb07ab5ba16a84723f363956e55797b47f087823537a1ba19f63`  
		Last Modified: Thu, 12 Sep 2024 19:04:27 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b4f03dd2d8ae83e3c688cd5d7a029cb3ee551185c04a9de81fdeb001caa88cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39229807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bcfff7920ade9d19a762d0eaed4d136380957c97dcceb7e228a8ca644acebaa`

```dockerfile
```

-	Layers:
	-	`sha256:5cb1b9142f1cbfba369b500c993dca8151955b89a13cfb7ba257b7ebbf89390c`  
		Last Modified: Thu, 12 Sep 2024 19:04:27 GMT  
		Size: 39.2 MB (39202876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06596df18cd14fe7c826e9c9202bcb565140e23d3ca1a63dd014fcb53e6816c`  
		Last Modified: Thu, 12 Sep 2024 19:04:25 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20240912`

```console
$ docker pull odoo@sha256:320de8e10ba44deebb499558f77d629f360b2c07a83e2f18de2538aac0e74a85
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
$ docker pull odoo@sha256:3e31a6f0907810ca94fdc17a013bd35826244426f336494104380a7dc5457ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.3 MB (599341915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c2851a558b18a90bb3467e4592c3b4a04a11dd33cc1cb3a0a7fa869560801a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1bd98a16cd3c673442e42f498f34773b48215de497686e6acc81a9294f0223`  
		Last Modified: Thu, 12 Sep 2024 18:58:33 GMT  
		Size: 236.0 MB (236020111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd06af45a76ed21953cdc99630ea6430082536c4d38a87c3806abd7768d892c`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 2.3 MB (2315842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e11a03d0dd12d8602f087f237fafc2de5eccd67c8776afc325372609d7fab3`  
		Last Modified: Thu, 12 Sep 2024 18:58:29 GMT  
		Size: 472.7 KB (472658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316a71c45c59a37cd3e08cd75d04e4b4a61349c7f1fe288badc25f1eb0efc236`  
		Last Modified: Thu, 12 Sep 2024 18:58:34 GMT  
		Size: 331.0 MB (330994838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfaed02607a202b6a5d86efe5cf9383b86ffcb674fead383446c89398b857ee`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c601410b0451ea4989c9c1bd02cdffcfeff35f6c2aa0a495e0a227a43ca43b4d`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dfd04f21d82c0713fec7b5f92cf208a45815c7a847b97970b97b1465d30547`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47be89bacb3a8671657632155a8c29c4750e2d09d0f9e114e80d7a91d44263af`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240912` - unknown; unknown

```console
$ docker pull odoo@sha256:23368febc6185c548f3ffb7d069a904931b60795d7e70f487a1cc6321e7980da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39221438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07b6c79c2928600c2db426511dd41bea2544c6be036043ebc7f31a8687a6dd2`

```dockerfile
```

-	Layers:
	-	`sha256:b37a948afbcb743494949c16be302606ccb7561dd1185b1608c6fa45edfe0600`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 39.2 MB (39194563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47343839d9f44ba64f29ae541c7bea27810e0e416e179eb5fce1ea08b675842b`  
		Last Modified: Thu, 12 Sep 2024 18:58:29 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240912` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a0ccf2aaaa2a7d6f084c5ee717f460e3e192379a80ca766ea77210604a47b64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.0 MB (594010797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f74e824859d8431a71332102f80a5030e4fe26ce5e7a9efc29391e8913ebec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
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
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec7e5187a062fd4ad8ee4eeb36f6eacf4bdea2e954b894018d62db463b7d9c1`  
		Last Modified: Thu, 12 Sep 2024 19:03:18 GMT  
		Size: 233.3 MB (233262427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3f1b034194bf5fcb4b8db7adb4927c95bc4d15c13fbe8004ae7efdb9187525`  
		Last Modified: Thu, 12 Sep 2024 19:03:13 GMT  
		Size: 2.3 MB (2307954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5263151f33f3f8c573ce7749dd7936c5e8eb9b4f25fc8d1e4bfb932bb6da8d`  
		Last Modified: Thu, 12 Sep 2024 19:03:13 GMT  
		Size: 472.6 KB (472644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a5c8e272339d2ada416e22e16fedc399a7554d6e9d6a6390726fff20fc8263`  
		Last Modified: Thu, 12 Sep 2024 19:03:20 GMT  
		Size: 330.6 MB (330606647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2003abd496c3f4d3d68536561854609d5ae088f65f2a53c24694d1326069e9e`  
		Last Modified: Thu, 12 Sep 2024 19:03:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f19a25b0133965dac6d5502fb0ae2d8fd6d552713c7a47d9be1deb6ddc2b55`  
		Last Modified: Thu, 12 Sep 2024 19:03:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dfa65ea650974cb4118e7d73bc06556c1b9b07d26e9fa371e165a7e9b8c715`  
		Last Modified: Thu, 12 Sep 2024 19:03:15 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe590702e0ef35d1f23a843afe197a55b99f099cee640b70bc3c463090c2f88e`  
		Last Modified: Thu, 12 Sep 2024 19:03:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240912` - unknown; unknown

```console
$ docker pull odoo@sha256:f342a52944ea2573857840f0f94c2bf2beef3ee550aaa1b21eee27ff75603bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39228264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b259c0c73c781b4f591ead5adf4b52462d0c9828367e04d6789d414c1430972`

```dockerfile
```

-	Layers:
	-	`sha256:9a17ef8c0dba22a090873ff2bca538bb3de1a577bed63ecddccdb0e96043af6e`  
		Last Modified: Thu, 12 Sep 2024 19:03:14 GMT  
		Size: 39.2 MB (39201088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35baaf1c61b02e32c6351591e8bf27a963f5f54048d9b7f9c52efda8698d4803`  
		Last Modified: Thu, 12 Sep 2024 19:03:12 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20240912` - linux; ppc64le

```console
$ docker pull odoo@sha256:4a72c4ccaa385487d132a4076ac7f4cdb23aabf3cf50d19f29cd0d4ef817b4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616168802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123a3645a2187a819020ec785ae778b49554f3dc162b7f7dc64403d1901e7172`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
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
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742703807fc36fed2a4242cea37ea0db0d517ecee5c2bb3b38083f9eeb9547d4`  
		Last Modified: Thu, 12 Sep 2024 19:04:42 GMT  
		Size: 245.9 MB (245900526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31729801a5ce405e76357b4ecc0288ab08f50d7532b6f5dec0c2f5130e456945`  
		Last Modified: Thu, 12 Sep 2024 19:04:25 GMT  
		Size: 2.6 MB (2592523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741ddf3cfee38ddf211aa3a5a0d6ddb9d5b93e38b46d76b9062b2db0ffd2502f`  
		Last Modified: Thu, 12 Sep 2024 19:04:25 GMT  
		Size: 472.8 KB (472763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cfb027a23d4a841895e8637a649bf4c904b71084f1c367310f66a6bd5241fd`  
		Last Modified: Thu, 12 Sep 2024 19:04:48 GMT  
		Size: 332.7 MB (332736373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7249df6a5a9bb2dd3cdf337be4ddd9df4adcb153242572f2adb0abac09618fb`  
		Last Modified: Thu, 12 Sep 2024 19:04:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6ab86f35c08574a071839b4a0951ef737f55c824c0f2569e91808f6e0bceb`  
		Last Modified: Thu, 12 Sep 2024 19:04:26 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a4bc86081e705301d725e6f24ddfb29b69ca4674ffaa66cf6534f893c63d28`  
		Last Modified: Thu, 12 Sep 2024 19:04:27 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ec3ac122fbcb07ab5ba16a84723f363956e55797b47f087823537a1ba19f63`  
		Last Modified: Thu, 12 Sep 2024 19:04:27 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20240912` - unknown; unknown

```console
$ docker pull odoo@sha256:b4f03dd2d8ae83e3c688cd5d7a029cb3ee551185c04a9de81fdeb001caa88cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39229807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bcfff7920ade9d19a762d0eaed4d136380957c97dcceb7e228a8ca644acebaa`

```dockerfile
```

-	Layers:
	-	`sha256:5cb1b9142f1cbfba369b500c993dca8151955b89a13cfb7ba257b7ebbf89390c`  
		Last Modified: Thu, 12 Sep 2024 19:04:27 GMT  
		Size: 39.2 MB (39202876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06596df18cd14fe7c826e9c9202bcb565140e23d3ca1a63dd014fcb53e6816c`  
		Last Modified: Thu, 12 Sep 2024 19:04:25 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:320de8e10ba44deebb499558f77d629f360b2c07a83e2f18de2538aac0e74a85
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
$ docker pull odoo@sha256:3e31a6f0907810ca94fdc17a013bd35826244426f336494104380a7dc5457ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.3 MB (599341915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c2851a558b18a90bb3467e4592c3b4a04a11dd33cc1cb3a0a7fa869560801a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:22 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:27:24 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Tue, 13 Aug 2024 09:27:24 GMT
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
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1bd98a16cd3c673442e42f498f34773b48215de497686e6acc81a9294f0223`  
		Last Modified: Thu, 12 Sep 2024 18:58:33 GMT  
		Size: 236.0 MB (236020111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd06af45a76ed21953cdc99630ea6430082536c4d38a87c3806abd7768d892c`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 2.3 MB (2315842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e11a03d0dd12d8602f087f237fafc2de5eccd67c8776afc325372609d7fab3`  
		Last Modified: Thu, 12 Sep 2024 18:58:29 GMT  
		Size: 472.7 KB (472658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316a71c45c59a37cd3e08cd75d04e4b4a61349c7f1fe288badc25f1eb0efc236`  
		Last Modified: Thu, 12 Sep 2024 18:58:34 GMT  
		Size: 331.0 MB (330994838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfaed02607a202b6a5d86efe5cf9383b86ffcb674fead383446c89398b857ee`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c601410b0451ea4989c9c1bd02cdffcfeff35f6c2aa0a495e0a227a43ca43b4d`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dfd04f21d82c0713fec7b5f92cf208a45815c7a847b97970b97b1465d30547`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47be89bacb3a8671657632155a8c29c4750e2d09d0f9e114e80d7a91d44263af`  
		Last Modified: Thu, 12 Sep 2024 18:58:31 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:23368febc6185c548f3ffb7d069a904931b60795d7e70f487a1cc6321e7980da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39221438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07b6c79c2928600c2db426511dd41bea2544c6be036043ebc7f31a8687a6dd2`

```dockerfile
```

-	Layers:
	-	`sha256:b37a948afbcb743494949c16be302606ccb7561dd1185b1608c6fa45edfe0600`  
		Last Modified: Thu, 12 Sep 2024 18:58:30 GMT  
		Size: 39.2 MB (39194563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47343839d9f44ba64f29ae541c7bea27810e0e416e179eb5fce1ea08b675842b`  
		Last Modified: Thu, 12 Sep 2024 18:58:29 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a0ccf2aaaa2a7d6f084c5ee717f460e3e192379a80ca766ea77210604a47b64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.0 MB (594010797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f74e824859d8431a71332102f80a5030e4fe26ce5e7a9efc29391e8913ebec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
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
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec7e5187a062fd4ad8ee4eeb36f6eacf4bdea2e954b894018d62db463b7d9c1`  
		Last Modified: Thu, 12 Sep 2024 19:03:18 GMT  
		Size: 233.3 MB (233262427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3f1b034194bf5fcb4b8db7adb4927c95bc4d15c13fbe8004ae7efdb9187525`  
		Last Modified: Thu, 12 Sep 2024 19:03:13 GMT  
		Size: 2.3 MB (2307954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5263151f33f3f8c573ce7749dd7936c5e8eb9b4f25fc8d1e4bfb932bb6da8d`  
		Last Modified: Thu, 12 Sep 2024 19:03:13 GMT  
		Size: 472.6 KB (472644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a5c8e272339d2ada416e22e16fedc399a7554d6e9d6a6390726fff20fc8263`  
		Last Modified: Thu, 12 Sep 2024 19:03:20 GMT  
		Size: 330.6 MB (330606647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2003abd496c3f4d3d68536561854609d5ae088f65f2a53c24694d1326069e9e`  
		Last Modified: Thu, 12 Sep 2024 19:03:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f19a25b0133965dac6d5502fb0ae2d8fd6d552713c7a47d9be1deb6ddc2b55`  
		Last Modified: Thu, 12 Sep 2024 19:03:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dfa65ea650974cb4118e7d73bc06556c1b9b07d26e9fa371e165a7e9b8c715`  
		Last Modified: Thu, 12 Sep 2024 19:03:15 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe590702e0ef35d1f23a843afe197a55b99f099cee640b70bc3c463090c2f88e`  
		Last Modified: Thu, 12 Sep 2024 19:03:15 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f342a52944ea2573857840f0f94c2bf2beef3ee550aaa1b21eee27ff75603bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39228264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b259c0c73c781b4f591ead5adf4b52462d0c9828367e04d6789d414c1430972`

```dockerfile
```

-	Layers:
	-	`sha256:9a17ef8c0dba22a090873ff2bca538bb3de1a577bed63ecddccdb0e96043af6e`  
		Last Modified: Thu, 12 Sep 2024 19:03:14 GMT  
		Size: 39.2 MB (39201088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35baaf1c61b02e32c6351591e8bf27a963f5f54048d9b7f9c52efda8698d4803`  
		Last Modified: Thu, 12 Sep 2024 19:03:12 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:4a72c4ccaa385487d132a4076ac7f4cdb23aabf3cf50d19f29cd0d4ef817b4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.2 MB (616168802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123a3645a2187a819020ec785ae778b49554f3dc162b7f7dc64403d1901e7172`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:11 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:15 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Tue, 13 Aug 2024 09:28:15 GMT
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
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742703807fc36fed2a4242cea37ea0db0d517ecee5c2bb3b38083f9eeb9547d4`  
		Last Modified: Thu, 12 Sep 2024 19:04:42 GMT  
		Size: 245.9 MB (245900526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31729801a5ce405e76357b4ecc0288ab08f50d7532b6f5dec0c2f5130e456945`  
		Last Modified: Thu, 12 Sep 2024 19:04:25 GMT  
		Size: 2.6 MB (2592523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741ddf3cfee38ddf211aa3a5a0d6ddb9d5b93e38b46d76b9062b2db0ffd2502f`  
		Last Modified: Thu, 12 Sep 2024 19:04:25 GMT  
		Size: 472.8 KB (472763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cfb027a23d4a841895e8637a649bf4c904b71084f1c367310f66a6bd5241fd`  
		Last Modified: Thu, 12 Sep 2024 19:04:48 GMT  
		Size: 332.7 MB (332736373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7249df6a5a9bb2dd3cdf337be4ddd9df4adcb153242572f2adb0abac09618fb`  
		Last Modified: Thu, 12 Sep 2024 19:04:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df6ab86f35c08574a071839b4a0951ef737f55c824c0f2569e91808f6e0bceb`  
		Last Modified: Thu, 12 Sep 2024 19:04:26 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a4bc86081e705301d725e6f24ddfb29b69ca4674ffaa66cf6534f893c63d28`  
		Last Modified: Thu, 12 Sep 2024 19:04:27 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ec3ac122fbcb07ab5ba16a84723f363956e55797b47f087823537a1ba19f63`  
		Last Modified: Thu, 12 Sep 2024 19:04:27 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:b4f03dd2d8ae83e3c688cd5d7a029cb3ee551185c04a9de81fdeb001caa88cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39229807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bcfff7920ade9d19a762d0eaed4d136380957c97dcceb7e228a8ca644acebaa`

```dockerfile
```

-	Layers:
	-	`sha256:5cb1b9142f1cbfba369b500c993dca8151955b89a13cfb7ba257b7ebbf89390c`  
		Last Modified: Thu, 12 Sep 2024 19:04:27 GMT  
		Size: 39.2 MB (39202876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06596df18cd14fe7c826e9c9202bcb565140e23d3ca1a63dd014fcb53e6816c`  
		Last Modified: Thu, 12 Sep 2024 19:04:25 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json
