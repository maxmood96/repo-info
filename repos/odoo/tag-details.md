<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:11`](#odoo11)
-	[`odoo:11.0`](#odoo110)
-	[`odoo:12`](#odoo12)
-	[`odoo:12.0`](#odoo120)
-	[`odoo:13`](#odoo13)
-	[`odoo:13.0`](#odoo130)
-	[`odoo:latest`](#odoolatest)

## `odoo:11`

```console
$ docker pull odoo@sha256:7d3a92e53f8f453ef3a53a6f32bd4c17893c5d1d4a214ccf66099446b4a40659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11` - linux; amd64

```console
$ docker pull odoo@sha256:1c8b1f78cd292a0ace0ca88b727a30a3ae55c7268f5dfa856d1df9a41793ef13
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 MB (386251189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5e1e7a589f81c5b07f7d759978b71b80da7e5c06eca79ecbe37aa06d686083`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:49 GMT
ADD file:16a1ddc40c95b14f8d6c79795047776270ee399f36979aaca45978a67bfee134 in / 
# Tue, 04 Aug 2020 15:45:49 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 00:32:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Aug 2020 00:32:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Aug 2020 00:32:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Aug 2020 00:32:39 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 05 Aug 2020 00:34:16 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Aug 2020 00:34:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 00:36:25 GMT
ENV ODOO_VERSION=11.0
# Wed, 26 Aug 2020 21:25:01 GMT
ARG ODOO_RELEASE=20200826
# Wed, 26 Aug 2020 21:25:01 GMT
ARG ODOO_SHA=cf5c3c766ba42861ede4ec9b4027dfc910818a01
# Wed, 26 Aug 2020 21:25:48 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=cf5c3c766ba42861ede4ec9b4027dfc910818a01
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb        && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Aug 2020 21:25:49 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Wed, 26 Aug 2020 21:25:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Aug 2020 21:25:50 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=cf5c3c766ba42861ede4ec9b4027dfc910818a01
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Aug 2020 21:25:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Aug 2020 21:25:50 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Aug 2020 21:25:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Aug 2020 21:25:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Aug 2020 21:25:51 GMT
USER odoo
# Wed, 26 Aug 2020 21:25:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Aug 2020 21:25:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:75cb2ebf3b3cb9c601a22edc7d9a120749da33999b30fba22b6cf2b90ee92823`  
		Last Modified: Tue, 04 Aug 2020 15:52:18 GMT  
		Size: 22.5 MB (22522276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad5c506d50e1dbcc214e3afec29f06e82b7ab2fbfdaa83b7dbe492de47ea5b2`  
		Last Modified: Wed, 05 Aug 2020 00:38:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d430b9279d73c5bcf9ccf812287316870750b3e4e81298ba96b22b66cac9dc7d`  
		Last Modified: Wed, 05 Aug 2020 00:38:36 GMT  
		Size: 219.6 MB (219609743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc34cd5c920e05f814ee9bb94e8cb32c206e1a643d3def70a9a36e63174b3f11`  
		Last Modified: Wed, 05 Aug 2020 00:38:06 GMT  
		Size: 2.3 MB (2336276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4039f6fee20cf77e25792a4f5d6c637054b56df65a94843b4773c61f16ba3b0e`  
		Last Modified: Wed, 26 Aug 2020 21:27:30 GMT  
		Size: 141.8 MB (141780259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f7710afddc28022f9162a47218686f3df107c1193766be63a7d92e7419dcf9`  
		Last Modified: Wed, 26 Aug 2020 21:27:05 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11eff30e7474541373ce053c86116e323c7543a439c30fd6fdfccaeb6f7a97bf`  
		Last Modified: Wed, 26 Aug 2020 21:27:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9815ff8ff1103a55681b2ce199860d1760c6e143fcc1ecc2562b302766e661bb`  
		Last Modified: Wed, 26 Aug 2020 21:27:05 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd73ecf18dac2eda47274e27e9f411ef90e2dbf527427b6fd9209cece005cef0`  
		Last Modified: Wed, 26 Aug 2020 21:27:05 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:11.0`

```console
$ docker pull odoo@sha256:7d3a92e53f8f453ef3a53a6f32bd4c17893c5d1d4a214ccf66099446b4a40659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11.0` - linux; amd64

```console
$ docker pull odoo@sha256:1c8b1f78cd292a0ace0ca88b727a30a3ae55c7268f5dfa856d1df9a41793ef13
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 MB (386251189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5e1e7a589f81c5b07f7d759978b71b80da7e5c06eca79ecbe37aa06d686083`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:49 GMT
ADD file:16a1ddc40c95b14f8d6c79795047776270ee399f36979aaca45978a67bfee134 in / 
# Tue, 04 Aug 2020 15:45:49 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 00:32:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Aug 2020 00:32:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Aug 2020 00:32:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Aug 2020 00:32:39 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 05 Aug 2020 00:34:16 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Aug 2020 00:34:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 00:36:25 GMT
ENV ODOO_VERSION=11.0
# Wed, 26 Aug 2020 21:25:01 GMT
ARG ODOO_RELEASE=20200826
# Wed, 26 Aug 2020 21:25:01 GMT
ARG ODOO_SHA=cf5c3c766ba42861ede4ec9b4027dfc910818a01
# Wed, 26 Aug 2020 21:25:48 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=cf5c3c766ba42861ede4ec9b4027dfc910818a01
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb        && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Aug 2020 21:25:49 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Wed, 26 Aug 2020 21:25:49 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Aug 2020 21:25:50 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=cf5c3c766ba42861ede4ec9b4027dfc910818a01
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Aug 2020 21:25:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Aug 2020 21:25:50 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Aug 2020 21:25:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Aug 2020 21:25:51 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Aug 2020 21:25:51 GMT
USER odoo
# Wed, 26 Aug 2020 21:25:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Aug 2020 21:25:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:75cb2ebf3b3cb9c601a22edc7d9a120749da33999b30fba22b6cf2b90ee92823`  
		Last Modified: Tue, 04 Aug 2020 15:52:18 GMT  
		Size: 22.5 MB (22522276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad5c506d50e1dbcc214e3afec29f06e82b7ab2fbfdaa83b7dbe492de47ea5b2`  
		Last Modified: Wed, 05 Aug 2020 00:38:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d430b9279d73c5bcf9ccf812287316870750b3e4e81298ba96b22b66cac9dc7d`  
		Last Modified: Wed, 05 Aug 2020 00:38:36 GMT  
		Size: 219.6 MB (219609743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc34cd5c920e05f814ee9bb94e8cb32c206e1a643d3def70a9a36e63174b3f11`  
		Last Modified: Wed, 05 Aug 2020 00:38:06 GMT  
		Size: 2.3 MB (2336276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4039f6fee20cf77e25792a4f5d6c637054b56df65a94843b4773c61f16ba3b0e`  
		Last Modified: Wed, 26 Aug 2020 21:27:30 GMT  
		Size: 141.8 MB (141780259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f7710afddc28022f9162a47218686f3df107c1193766be63a7d92e7419dcf9`  
		Last Modified: Wed, 26 Aug 2020 21:27:05 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11eff30e7474541373ce053c86116e323c7543a439c30fd6fdfccaeb6f7a97bf`  
		Last Modified: Wed, 26 Aug 2020 21:27:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9815ff8ff1103a55681b2ce199860d1760c6e143fcc1ecc2562b302766e661bb`  
		Last Modified: Wed, 26 Aug 2020 21:27:05 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd73ecf18dac2eda47274e27e9f411ef90e2dbf527427b6fd9209cece005cef0`  
		Last Modified: Wed, 26 Aug 2020 21:27:05 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12`

```console
$ docker pull odoo@sha256:e2d7dfc343f946749301f9cf1f716bd68f153e3d50624fe99a9d9a5be03cdf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:e9d89eafb3e69e8fa48bf2bb153273072e47c7d7c805f746662037f254e39418
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.4 MB (396409517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449d240d5e853f779e78cc441eb9ac0f23a59f05bfd35553d68ac8839ddb403f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:49 GMT
ADD file:16a1ddc40c95b14f8d6c79795047776270ee399f36979aaca45978a67bfee134 in / 
# Tue, 04 Aug 2020 15:45:49 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 00:32:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Aug 2020 00:32:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Aug 2020 00:32:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Aug 2020 00:32:39 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 05 Aug 2020 00:34:16 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Aug 2020 00:34:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 00:35:10 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 00:35:10 GMT
ENV ODOO_VERSION=12.0
# Wed, 26 Aug 2020 21:24:06 GMT
ARG ODOO_RELEASE=20200826
# Wed, 26 Aug 2020 21:24:06 GMT
ARG ODOO_SHA=3acc73ce5dfbe550d6ad617a4078b0a5d160f9db
# Wed, 26 Aug 2020 21:24:51 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=3acc73ce5dfbe550d6ad617a4078b0a5d160f9db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Aug 2020 21:24:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 26 Aug 2020 21:24:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Aug 2020 21:24:53 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=3acc73ce5dfbe550d6ad617a4078b0a5d160f9db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Aug 2020 21:24:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Aug 2020 21:24:54 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Aug 2020 21:24:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Aug 2020 21:24:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Aug 2020 21:24:54 GMT
USER odoo
# Wed, 26 Aug 2020 21:24:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Aug 2020 21:24:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:75cb2ebf3b3cb9c601a22edc7d9a120749da33999b30fba22b6cf2b90ee92823`  
		Last Modified: Tue, 04 Aug 2020 15:52:18 GMT  
		Size: 22.5 MB (22522276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad5c506d50e1dbcc214e3afec29f06e82b7ab2fbfdaa83b7dbe492de47ea5b2`  
		Last Modified: Wed, 05 Aug 2020 00:38:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d430b9279d73c5bcf9ccf812287316870750b3e4e81298ba96b22b66cac9dc7d`  
		Last Modified: Wed, 05 Aug 2020 00:38:36 GMT  
		Size: 219.6 MB (219609743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc34cd5c920e05f814ee9bb94e8cb32c206e1a643d3def70a9a36e63174b3f11`  
		Last Modified: Wed, 05 Aug 2020 00:38:06 GMT  
		Size: 2.3 MB (2336276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2464addedb0e8016754c0bb4efc785d8712c63bfdb8e1f931c16b7cc7f7387b7`  
		Last Modified: Wed, 05 Aug 2020 00:38:11 GMT  
		Size: 22.2 MB (22241349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e9cca6bf33d84aa07cbcddb373d13b4a62bd87e5cc82b538afbc5b6d17e06e`  
		Last Modified: Wed, 26 Aug 2020 21:27:02 GMT  
		Size: 129.7 MB (129697235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec4bb30ff001f77b9d160dd37fe0b24c6c26c9a69378ef6c13451601979fe28`  
		Last Modified: Wed, 26 Aug 2020 21:26:36 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ab0ec6b654ba1aadf9cee54bb90eba301c1991212c5156fb6b13c9d85e6a0c`  
		Last Modified: Wed, 26 Aug 2020 21:26:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51b21d8a4e19ef0fecf14f843351a458bc2acbec7958ff633bf4c9e2e52cdf5`  
		Last Modified: Wed, 26 Aug 2020 21:26:36 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf11d86d4038215972f3c275300ea88c9eac404636ee905672b2bf02e2fe022`  
		Last Modified: Wed, 26 Aug 2020 21:26:36 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:e2d7dfc343f946749301f9cf1f716bd68f153e3d50624fe99a9d9a5be03cdf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:e9d89eafb3e69e8fa48bf2bb153273072e47c7d7c805f746662037f254e39418
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.4 MB (396409517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449d240d5e853f779e78cc441eb9ac0f23a59f05bfd35553d68ac8839ddb403f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:49 GMT
ADD file:16a1ddc40c95b14f8d6c79795047776270ee399f36979aaca45978a67bfee134 in / 
# Tue, 04 Aug 2020 15:45:49 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 00:32:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Aug 2020 00:32:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Aug 2020 00:32:38 GMT
ENV LANG=C.UTF-8
# Wed, 05 Aug 2020 00:32:39 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Wed, 05 Aug 2020 00:34:16 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Aug 2020 00:34:26 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 00:35:10 GMT
RUN echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install --no-install-recommends -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 00:35:10 GMT
ENV ODOO_VERSION=12.0
# Wed, 26 Aug 2020 21:24:06 GMT
ARG ODOO_RELEASE=20200826
# Wed, 26 Aug 2020 21:24:06 GMT
ARG ODOO_SHA=3acc73ce5dfbe550d6ad617a4078b0a5d160f9db
# Wed, 26 Aug 2020 21:24:51 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=3acc73ce5dfbe550d6ad617a4078b0a5d160f9db
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Aug 2020 21:24:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 26 Aug 2020 21:24:53 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Aug 2020 21:24:53 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=3acc73ce5dfbe550d6ad617a4078b0a5d160f9db
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Aug 2020 21:24:54 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Aug 2020 21:24:54 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Aug 2020 21:24:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Aug 2020 21:24:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Aug 2020 21:24:54 GMT
USER odoo
# Wed, 26 Aug 2020 21:24:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Aug 2020 21:24:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:75cb2ebf3b3cb9c601a22edc7d9a120749da33999b30fba22b6cf2b90ee92823`  
		Last Modified: Tue, 04 Aug 2020 15:52:18 GMT  
		Size: 22.5 MB (22522276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad5c506d50e1dbcc214e3afec29f06e82b7ab2fbfdaa83b7dbe492de47ea5b2`  
		Last Modified: Wed, 05 Aug 2020 00:38:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d430b9279d73c5bcf9ccf812287316870750b3e4e81298ba96b22b66cac9dc7d`  
		Last Modified: Wed, 05 Aug 2020 00:38:36 GMT  
		Size: 219.6 MB (219609743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc34cd5c920e05f814ee9bb94e8cb32c206e1a643d3def70a9a36e63174b3f11`  
		Last Modified: Wed, 05 Aug 2020 00:38:06 GMT  
		Size: 2.3 MB (2336276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2464addedb0e8016754c0bb4efc785d8712c63bfdb8e1f931c16b7cc7f7387b7`  
		Last Modified: Wed, 05 Aug 2020 00:38:11 GMT  
		Size: 22.2 MB (22241349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e9cca6bf33d84aa07cbcddb373d13b4a62bd87e5cc82b538afbc5b6d17e06e`  
		Last Modified: Wed, 26 Aug 2020 21:27:02 GMT  
		Size: 129.7 MB (129697235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec4bb30ff001f77b9d160dd37fe0b24c6c26c9a69378ef6c13451601979fe28`  
		Last Modified: Wed, 26 Aug 2020 21:26:36 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ab0ec6b654ba1aadf9cee54bb90eba301c1991212c5156fb6b13c9d85e6a0c`  
		Last Modified: Wed, 26 Aug 2020 21:26:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51b21d8a4e19ef0fecf14f843351a458bc2acbec7958ff633bf4c9e2e52cdf5`  
		Last Modified: Wed, 26 Aug 2020 21:26:36 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf11d86d4038215972f3c275300ea88c9eac404636ee905672b2bf02e2fe022`  
		Last Modified: Wed, 26 Aug 2020 21:26:36 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:faf6477a54d7cf3ea780789843821e439817bf5c3aa866a07e843ca2b67b6f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:201b3c2d22f596e50be03e9c374b46d100b87fbfc607bb42540341a3fd97160c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.3 MB (382299775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad4d32e0f24c4579c6430ca9f369ca3c660b3308cb1a8ef22254d1b07b0465b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 00:30:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Aug 2020 00:30:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Aug 2020 00:30:22 GMT
ENV LANG=C.UTF-8
# Wed, 05 Aug 2020 00:31:24 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Aug 2020 00:31:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 00:31:36 GMT
RUN npm install -g rtlcss
# Wed, 05 Aug 2020 00:31:36 GMT
ENV ODOO_VERSION=13.0
# Wed, 26 Aug 2020 21:23:01 GMT
ARG ODOO_RELEASE=20200826
# Wed, 26 Aug 2020 21:23:01 GMT
ARG ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
# Wed, 26 Aug 2020 21:23:51 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Aug 2020 21:23:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 26 Aug 2020 21:23:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Aug 2020 21:23:53 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Aug 2020 21:23:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Aug 2020 21:23:53 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Aug 2020 21:23:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Aug 2020 21:23:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Aug 2020 21:23:54 GMT
USER odoo
# Wed, 26 Aug 2020 21:23:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Aug 2020 21:23:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa677b64d95abed08a2d9cb947cd9851cd4dbaea538dfbf571254ad7d5c149fb`  
		Last Modified: Wed, 05 Aug 2020 00:37:57 GMT  
		Size: 204.1 MB (204058599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd4309767ba7ebc1ba1cd04b4b96d90fa8ce3b88c6e27e0a2655d5c1139c19c`  
		Last Modified: Wed, 05 Aug 2020 00:37:26 GMT  
		Size: 2.3 MB (2335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffbc48d26ec0e852866cadfb5a0162007485f8f4c60d28986a74f205ba47bc2`  
		Last Modified: Wed, 05 Aug 2020 00:37:25 GMT  
		Size: 1.1 MB (1096042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b593766a4202737b02190be6fcfe2427b801ac3b98cfe101bd7943aef85f4cb2`  
		Last Modified: Wed, 26 Aug 2020 21:26:31 GMT  
		Size: 147.7 MB (147715296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73120615b086d87fdb19495670eb48838413e919f9320d66f77f1c70084b48b4`  
		Last Modified: Wed, 26 Aug 2020 21:26:02 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e0ceb69235cca3f108af2f440e2942959676222615eeea8c1f1990eeb59094`  
		Last Modified: Wed, 26 Aug 2020 21:26:02 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2def5317f97e95050de3af0aa1f8bf0b06eb0ab6f84a6a07836a514a4834c4f`  
		Last Modified: Wed, 26 Aug 2020 21:26:02 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724924aae197be8f17a923d6d3cdb68a66fdfaa19dae3492b8bd99ec08e0fe96`  
		Last Modified: Wed, 26 Aug 2020 21:26:02 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:faf6477a54d7cf3ea780789843821e439817bf5c3aa866a07e843ca2b67b6f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:201b3c2d22f596e50be03e9c374b46d100b87fbfc607bb42540341a3fd97160c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.3 MB (382299775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad4d32e0f24c4579c6430ca9f369ca3c660b3308cb1a8ef22254d1b07b0465b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 00:30:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Aug 2020 00:30:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Aug 2020 00:30:22 GMT
ENV LANG=C.UTF-8
# Wed, 05 Aug 2020 00:31:24 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Aug 2020 00:31:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 00:31:36 GMT
RUN npm install -g rtlcss
# Wed, 05 Aug 2020 00:31:36 GMT
ENV ODOO_VERSION=13.0
# Wed, 26 Aug 2020 21:23:01 GMT
ARG ODOO_RELEASE=20200826
# Wed, 26 Aug 2020 21:23:01 GMT
ARG ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
# Wed, 26 Aug 2020 21:23:51 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Aug 2020 21:23:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 26 Aug 2020 21:23:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Aug 2020 21:23:53 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Aug 2020 21:23:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Aug 2020 21:23:53 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Aug 2020 21:23:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Aug 2020 21:23:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Aug 2020 21:23:54 GMT
USER odoo
# Wed, 26 Aug 2020 21:23:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Aug 2020 21:23:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa677b64d95abed08a2d9cb947cd9851cd4dbaea538dfbf571254ad7d5c149fb`  
		Last Modified: Wed, 05 Aug 2020 00:37:57 GMT  
		Size: 204.1 MB (204058599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd4309767ba7ebc1ba1cd04b4b96d90fa8ce3b88c6e27e0a2655d5c1139c19c`  
		Last Modified: Wed, 05 Aug 2020 00:37:26 GMT  
		Size: 2.3 MB (2335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffbc48d26ec0e852866cadfb5a0162007485f8f4c60d28986a74f205ba47bc2`  
		Last Modified: Wed, 05 Aug 2020 00:37:25 GMT  
		Size: 1.1 MB (1096042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b593766a4202737b02190be6fcfe2427b801ac3b98cfe101bd7943aef85f4cb2`  
		Last Modified: Wed, 26 Aug 2020 21:26:31 GMT  
		Size: 147.7 MB (147715296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73120615b086d87fdb19495670eb48838413e919f9320d66f77f1c70084b48b4`  
		Last Modified: Wed, 26 Aug 2020 21:26:02 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e0ceb69235cca3f108af2f440e2942959676222615eeea8c1f1990eeb59094`  
		Last Modified: Wed, 26 Aug 2020 21:26:02 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2def5317f97e95050de3af0aa1f8bf0b06eb0ab6f84a6a07836a514a4834c4f`  
		Last Modified: Wed, 26 Aug 2020 21:26:02 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724924aae197be8f17a923d6d3cdb68a66fdfaa19dae3492b8bd99ec08e0fe96`  
		Last Modified: Wed, 26 Aug 2020 21:26:02 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:faf6477a54d7cf3ea780789843821e439817bf5c3aa866a07e843ca2b67b6f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:201b3c2d22f596e50be03e9c374b46d100b87fbfc607bb42540341a3fd97160c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.3 MB (382299775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad4d32e0f24c4579c6430ca9f369ca3c660b3308cb1a8ef22254d1b07b0465b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 00:30:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 05 Aug 2020 00:30:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 05 Aug 2020 00:30:22 GMT
ENV LANG=C.UTF-8
# Wed, 05 Aug 2020 00:31:24 GMT
RUN apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Wed, 05 Aug 2020 00:31:32 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && GNUPGHOME="$(mktemp -d)"         && export GNUPGHOME         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install --no-install-recommends -y postgresql-client         && rm -f /etc/apt/sources.list.d/pgdg.list         && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 00:31:36 GMT
RUN npm install -g rtlcss
# Wed, 05 Aug 2020 00:31:36 GMT
ENV ODOO_VERSION=13.0
# Wed, 26 Aug 2020 21:23:01 GMT
ARG ODOO_RELEASE=20200826
# Wed, 26 Aug 2020 21:23:01 GMT
ARG ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
# Wed, 26 Aug 2020 21:23:51 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && apt-get update         && apt-get -y install --no-install-recommends ./odoo.deb         && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 26 Aug 2020 21:23:52 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Wed, 26 Aug 2020 21:23:52 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 26 Aug 2020 21:23:53 GMT
# ARGS: ODOO_RELEASE=20200826 ODOO_SHA=9fe7d55e64867d177519e99cc45f9ecfeb3746a3
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 26 Aug 2020 21:23:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 26 Aug 2020 21:23:53 GMT
EXPOSE 8069 8071 8072
# Wed, 26 Aug 2020 21:23:54 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 26 Aug 2020 21:23:54 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 26 Aug 2020 21:23:54 GMT
USER odoo
# Wed, 26 Aug 2020 21:23:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Aug 2020 21:23:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa677b64d95abed08a2d9cb947cd9851cd4dbaea538dfbf571254ad7d5c149fb`  
		Last Modified: Wed, 05 Aug 2020 00:37:57 GMT  
		Size: 204.1 MB (204058599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd4309767ba7ebc1ba1cd04b4b96d90fa8ce3b88c6e27e0a2655d5c1139c19c`  
		Last Modified: Wed, 05 Aug 2020 00:37:26 GMT  
		Size: 2.3 MB (2335315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffbc48d26ec0e852866cadfb5a0162007485f8f4c60d28986a74f205ba47bc2`  
		Last Modified: Wed, 05 Aug 2020 00:37:25 GMT  
		Size: 1.1 MB (1096042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b593766a4202737b02190be6fcfe2427b801ac3b98cfe101bd7943aef85f4cb2`  
		Last Modified: Wed, 26 Aug 2020 21:26:31 GMT  
		Size: 147.7 MB (147715296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73120615b086d87fdb19495670eb48838413e919f9320d66f77f1c70084b48b4`  
		Last Modified: Wed, 26 Aug 2020 21:26:02 GMT  
		Size: 670.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e0ceb69235cca3f108af2f440e2942959676222615eeea8c1f1990eeb59094`  
		Last Modified: Wed, 26 Aug 2020 21:26:02 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2def5317f97e95050de3af0aa1f8bf0b06eb0ab6f84a6a07836a514a4834c4f`  
		Last Modified: Wed, 26 Aug 2020 21:26:02 GMT  
		Size: 593.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724924aae197be8f17a923d6d3cdb68a66fdfaa19dae3492b8bd99ec08e0fe96`  
		Last Modified: Wed, 26 Aug 2020 21:26:02 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
