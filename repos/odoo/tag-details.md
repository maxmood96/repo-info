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
$ docker pull odoo@sha256:e1cdd834c6a6ce29f746a6f92873461133c4750a34c3cb502967f473c3cd467b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11` - linux; amd64

```console
$ docker pull odoo@sha256:79a83e61bf0534a4bbe001cacf3c6319f7fad03f7ba343f9ed9462d6b420d236
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385941712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0bf6f41ffbeaff1d3ffe7bbc3b61c09663ddabfd73873152815f2867cd2bd27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 22:36:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 16 Apr 2020 22:36:40 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 22:36:41 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 16 Apr 2020 22:38:40 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 16 Apr 2020 22:38:54 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 22:40:43 GMT
ENV ODOO_VERSION=11.0
# Thu, 16 Apr 2020 22:40:44 GMT
ARG ODOO_RELEASE=20200121
# Thu, 16 Apr 2020 22:40:44 GMT
ARG ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
# Thu, 16 Apr 2020 22:41:34 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 16 Apr 2020 22:41:35 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Thu, 16 Apr 2020 22:41:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 16 Apr 2020 22:41:36 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 16 Apr 2020 22:41:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 16 Apr 2020 22:41:37 GMT
EXPOSE 8069 8071
# Thu, 16 Apr 2020 22:41:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 16 Apr 2020 22:41:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 16 Apr 2020 22:41:37 GMT
USER odoo
# Thu, 16 Apr 2020 22:41:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 22:41:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86ad9b5077ce84efe1e6e46944912f3606d20308e03dfe09d07e2797e411b89`  
		Last Modified: Thu, 16 Apr 2020 22:42:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba97ddd28b1013295305adc162d6551ca13302b7c054afcc3cad8facb6409828`  
		Last Modified: Thu, 16 Apr 2020 22:43:42 GMT  
		Size: 219.6 MB (219649945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8f4a6e988b082789a24f62703071c841b8b32dd4cada0184f7f874de359263`  
		Last Modified: Thu, 16 Apr 2020 22:42:49 GMT  
		Size: 2.3 MB (2346254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81884edeba7cd88356dbd1204961fc9d98a55a09d620408fc92b1a739c99fe8`  
		Last Modified: Thu, 16 Apr 2020 22:44:31 GMT  
		Size: 141.4 MB (141429400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9782e7d4ad68510707638ec1cf2d1fe238a2a2132db2f8d2fac723d8fb29aedc`  
		Last Modified: Thu, 16 Apr 2020 22:43:48 GMT  
		Size: 674.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d74a740a14d05e83dc67d41ccd1cd5e6c9b30c694d3bacc75744aec377ca936`  
		Last Modified: Thu, 16 Apr 2020 22:43:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d83e709d55c4501ea7bf5dfa9b1be74ff154857d3b30836a0aaa68bb9fb0c9a`  
		Last Modified: Thu, 16 Apr 2020 22:43:48 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69bd2a9af3415b29789034491859db2fe2cfc28f98f811a1cf886c5c8ded7f9`  
		Last Modified: Thu, 16 Apr 2020 22:43:48 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:11.0`

```console
$ docker pull odoo@sha256:e1cdd834c6a6ce29f746a6f92873461133c4750a34c3cb502967f473c3cd467b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:11.0` - linux; amd64

```console
$ docker pull odoo@sha256:79a83e61bf0534a4bbe001cacf3c6319f7fad03f7ba343f9ed9462d6b420d236
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385941712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0bf6f41ffbeaff1d3ffe7bbc3b61c09663ddabfd73873152815f2867cd2bd27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 22:36:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 16 Apr 2020 22:36:40 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 22:36:41 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 16 Apr 2020 22:38:40 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 16 Apr 2020 22:38:54 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 22:40:43 GMT
ENV ODOO_VERSION=11.0
# Thu, 16 Apr 2020 22:40:44 GMT
ARG ODOO_RELEASE=20200121
# Thu, 16 Apr 2020 22:40:44 GMT
ARG ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
# Thu, 16 Apr 2020 22:41:34 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 16 Apr 2020 22:41:35 GMT
COPY file:cdc612ad49467417b0321c166f94e4f99b071755cb6ade071774e83d3b6ee4cb in / 
# Thu, 16 Apr 2020 22:41:36 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 16 Apr 2020 22:41:36 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=13f30434cb4fb28b11d78fd4e7c616d03362f779
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 16 Apr 2020 22:41:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 16 Apr 2020 22:41:37 GMT
EXPOSE 8069 8071
# Thu, 16 Apr 2020 22:41:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 16 Apr 2020 22:41:37 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 16 Apr 2020 22:41:37 GMT
USER odoo
# Thu, 16 Apr 2020 22:41:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 22:41:38 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86ad9b5077ce84efe1e6e46944912f3606d20308e03dfe09d07e2797e411b89`  
		Last Modified: Thu, 16 Apr 2020 22:42:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba97ddd28b1013295305adc162d6551ca13302b7c054afcc3cad8facb6409828`  
		Last Modified: Thu, 16 Apr 2020 22:43:42 GMT  
		Size: 219.6 MB (219649945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8f4a6e988b082789a24f62703071c841b8b32dd4cada0184f7f874de359263`  
		Last Modified: Thu, 16 Apr 2020 22:42:49 GMT  
		Size: 2.3 MB (2346254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81884edeba7cd88356dbd1204961fc9d98a55a09d620408fc92b1a739c99fe8`  
		Last Modified: Thu, 16 Apr 2020 22:44:31 GMT  
		Size: 141.4 MB (141429400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9782e7d4ad68510707638ec1cf2d1fe238a2a2132db2f8d2fac723d8fb29aedc`  
		Last Modified: Thu, 16 Apr 2020 22:43:48 GMT  
		Size: 674.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d74a740a14d05e83dc67d41ccd1cd5e6c9b30c694d3bacc75744aec377ca936`  
		Last Modified: Thu, 16 Apr 2020 22:43:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d83e709d55c4501ea7bf5dfa9b1be74ff154857d3b30836a0aaa68bb9fb0c9a`  
		Last Modified: Thu, 16 Apr 2020 22:43:48 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69bd2a9af3415b29789034491859db2fe2cfc28f98f811a1cf886c5c8ded7f9`  
		Last Modified: Thu, 16 Apr 2020 22:43:48 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12`

```console
$ docker pull odoo@sha256:078d87626581bee89d8eb409938b2e09972d473c83b276bac27dcad4178a3866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12` - linux; amd64

```console
$ docker pull odoo@sha256:67ca5967ab3e5564dc2b7e647b04abb8156db7ff78491e729b418b3ea295b3fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.9 MB (399890393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e7683e382c9ee613bf6eb6c213450ec966b43aa6a85db4b2d224eec02b5d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 22:36:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 16 Apr 2020 22:36:40 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 22:36:41 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 16 Apr 2020 22:38:40 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 16 Apr 2020 22:38:54 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 22:39:16 GMT
RUN set -x;    echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && export GNUPGHOME="$(mktemp -d)"     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 22:39:16 GMT
ENV ODOO_VERSION=12.0
# Thu, 16 Apr 2020 22:39:16 GMT
ARG ODOO_RELEASE=20200121
# Thu, 16 Apr 2020 22:39:17 GMT
ARG ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
# Thu, 16 Apr 2020 22:40:27 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 16 Apr 2020 22:40:29 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 16 Apr 2020 22:40:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 16 Apr 2020 22:40:31 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 16 Apr 2020 22:40:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 16 Apr 2020 22:40:32 GMT
EXPOSE 8069 8071
# Thu, 16 Apr 2020 22:40:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 16 Apr 2020 22:40:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 16 Apr 2020 22:40:33 GMT
USER odoo
# Thu, 16 Apr 2020 22:40:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 22:40:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86ad9b5077ce84efe1e6e46944912f3606d20308e03dfe09d07e2797e411b89`  
		Last Modified: Thu, 16 Apr 2020 22:42:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba97ddd28b1013295305adc162d6551ca13302b7c054afcc3cad8facb6409828`  
		Last Modified: Thu, 16 Apr 2020 22:43:42 GMT  
		Size: 219.6 MB (219649945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8f4a6e988b082789a24f62703071c841b8b32dd4cada0184f7f874de359263`  
		Last Modified: Thu, 16 Apr 2020 22:42:49 GMT  
		Size: 2.3 MB (2346254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4124b3603634aaf0b53fa466b6df59a8df6ab607ad81cd5309b4f2d54cf26230`  
		Last Modified: Thu, 16 Apr 2020 22:42:57 GMT  
		Size: 26.6 MB (26578314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a216fc083d1ff5c548decb88b3ded861add5c43bf3099c6aa21f2c1eba1da3a5`  
		Last Modified: Thu, 16 Apr 2020 22:43:41 GMT  
		Size: 128.8 MB (128799765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21507bf3597730c72c84bc89dd3aa21ff5c316a9697c88f2c19ef893257c5a4f`  
		Last Modified: Thu, 16 Apr 2020 22:42:48 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb16ff64e0f09a018298e069b77cfdd13e9dfd6dad913b0530a7e2f5849ae39b`  
		Last Modified: Thu, 16 Apr 2020 22:42:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac5fed6c7a581e9ed3eac43521d206a7ee1d3a3ec8702444c277be65235acb8`  
		Last Modified: Thu, 16 Apr 2020 22:42:48 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10d0489619ba04133d8a2d760b664b1b7f1a133579291fc10e371739b7f4d99`  
		Last Modified: Thu, 16 Apr 2020 22:42:48 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:12.0`

```console
$ docker pull odoo@sha256:078d87626581bee89d8eb409938b2e09972d473c83b276bac27dcad4178a3866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:12.0` - linux; amd64

```console
$ docker pull odoo@sha256:67ca5967ab3e5564dc2b7e647b04abb8156db7ff78491e729b418b3ea295b3fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.9 MB (399890393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e7683e382c9ee613bf6eb6c213450ec966b43aa6a85db4b2d224eec02b5d95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 22:36:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 16 Apr 2020 22:36:40 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 22:36:41 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
# Thu, 16 Apr 2020 22:38:40 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl1.0-dev             node-less             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 16 Apr 2020 22:38:54 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 22:39:16 GMT
RUN set -x;    echo "deb http://deb.nodesource.com/node_8.x stretch main" > /etc/apt/sources.list.d/nodesource.list     && export GNUPGHOME="$(mktemp -d)"     && repokey='9FD3B784BC1C6FC31A8A0A1C1655A0AB68576280'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/nodejs.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update     && apt-get install -y nodejs     && npm install -g rtlcss     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 22:39:16 GMT
ENV ODOO_VERSION=12.0
# Thu, 16 Apr 2020 22:39:16 GMT
ARG ODOO_RELEASE=20200121
# Thu, 16 Apr 2020 22:39:17 GMT
ARG ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
# Thu, 16 Apr 2020 22:40:27 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 16 Apr 2020 22:40:29 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 16 Apr 2020 22:40:30 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 16 Apr 2020 22:40:31 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=cb0bcb5d239983468c2e3b3f7cf17f58df820b1c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 16 Apr 2020 22:40:31 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 16 Apr 2020 22:40:32 GMT
EXPOSE 8069 8071
# Thu, 16 Apr 2020 22:40:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 16 Apr 2020 22:40:32 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 16 Apr 2020 22:40:33 GMT
USER odoo
# Thu, 16 Apr 2020 22:40:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 22:40:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86ad9b5077ce84efe1e6e46944912f3606d20308e03dfe09d07e2797e411b89`  
		Last Modified: Thu, 16 Apr 2020 22:42:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba97ddd28b1013295305adc162d6551ca13302b7c054afcc3cad8facb6409828`  
		Last Modified: Thu, 16 Apr 2020 22:43:42 GMT  
		Size: 219.6 MB (219649945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8f4a6e988b082789a24f62703071c841b8b32dd4cada0184f7f874de359263`  
		Last Modified: Thu, 16 Apr 2020 22:42:49 GMT  
		Size: 2.3 MB (2346254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4124b3603634aaf0b53fa466b6df59a8df6ab607ad81cd5309b4f2d54cf26230`  
		Last Modified: Thu, 16 Apr 2020 22:42:57 GMT  
		Size: 26.6 MB (26578314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a216fc083d1ff5c548decb88b3ded861add5c43bf3099c6aa21f2c1eba1da3a5`  
		Last Modified: Thu, 16 Apr 2020 22:43:41 GMT  
		Size: 128.8 MB (128799765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21507bf3597730c72c84bc89dd3aa21ff5c316a9697c88f2c19ef893257c5a4f`  
		Last Modified: Thu, 16 Apr 2020 22:42:48 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb16ff64e0f09a018298e069b77cfdd13e9dfd6dad913b0530a7e2f5849ae39b`  
		Last Modified: Thu, 16 Apr 2020 22:42:48 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac5fed6c7a581e9ed3eac43521d206a7ee1d3a3ec8702444c277be65235acb8`  
		Last Modified: Thu, 16 Apr 2020 22:42:48 GMT  
		Size: 595.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10d0489619ba04133d8a2d760b664b1b7f1a133579291fc10e371739b7f4d99`  
		Last Modified: Thu, 16 Apr 2020 22:42:48 GMT  
		Size: 591.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13`

```console
$ docker pull odoo@sha256:2aa656a0bbc256846021767626f16a86248af27bf1df77abe31b04f4c30b9d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13` - linux; amd64

```console
$ docker pull odoo@sha256:dce86bfbf5d790d4565b138217c7915243a4da57e92a11a8daa5215875ded838
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.4 MB (376406747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728c08742855a3bc22efa0479e1bc0f2350362b9efe60d949f45d9308571dd2f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 22:33:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 16 Apr 2020 22:33:23 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 22:34:56 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 16 Apr 2020 22:35:08 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 22:35:14 GMT
RUN set -x;     npm install -g rtlcss
# Thu, 16 Apr 2020 22:35:14 GMT
ENV ODOO_VERSION=13.0
# Thu, 16 Apr 2020 22:35:15 GMT
ARG ODOO_RELEASE=20200121
# Thu, 16 Apr 2020 22:35:15 GMT
ARG ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
# Thu, 16 Apr 2020 22:36:24 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 16 Apr 2020 22:36:25 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 16 Apr 2020 22:36:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 16 Apr 2020 22:36:26 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 16 Apr 2020 22:36:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 16 Apr 2020 22:36:26 GMT
EXPOSE 8069 8071
# Thu, 16 Apr 2020 22:36:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 16 Apr 2020 22:36:27 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 16 Apr 2020 22:36:27 GMT
USER odoo
# Thu, 16 Apr 2020 22:36:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 22:36:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66325385ddfb471e56d91532ad6c4f6a3d7e063a8fac1fabccd0364a6eb362b7`  
		Last Modified: Thu, 16 Apr 2020 22:42:43 GMT  
		Size: 203.6 MB (203558833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dbdfdea4dd0efbcf5b00db0e1eb38dda90e3488e3384be83a682ad98a93544`  
		Last Modified: Thu, 16 Apr 2020 22:41:53 GMT  
		Size: 2.3 MB (2332477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452732a285fe366bd1c590479def3e69b40c59c7c38fe8365e38b2ade6d96823`  
		Last Modified: Thu, 16 Apr 2020 22:41:53 GMT  
		Size: 1.1 MB (1090307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce037cf8d9123bc2c9122c978df0483a91a0fabdcbe2a09c39456df908bc184e`  
		Last Modified: Thu, 16 Apr 2020 22:42:30 GMT  
		Size: 142.3 MB (142324578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aec3e880957f943a8ca570ffbc1d523a920b1a27a2524fb348706f6d755a2ad`  
		Last Modified: Thu, 16 Apr 2020 22:41:52 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cd1d26a9712969c3748400abae722d9497badfc9fda3116fa222f027918ea6`  
		Last Modified: Thu, 16 Apr 2020 22:41:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84481a476030ad4423b9a3fa8f7738eae9ae9ef86c378706e56c5b92349b6971`  
		Last Modified: Thu, 16 Apr 2020 22:41:52 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76cfd77135a0254ae710bb88e2ee473987f9fed20651c93c189d6be890f4e38`  
		Last Modified: Thu, 16 Apr 2020 22:41:52 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:13.0`

```console
$ docker pull odoo@sha256:2aa656a0bbc256846021767626f16a86248af27bf1df77abe31b04f4c30b9d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:13.0` - linux; amd64

```console
$ docker pull odoo@sha256:dce86bfbf5d790d4565b138217c7915243a4da57e92a11a8daa5215875ded838
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.4 MB (376406747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728c08742855a3bc22efa0479e1bc0f2350362b9efe60d949f45d9308571dd2f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 22:33:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 16 Apr 2020 22:33:23 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 22:34:56 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 16 Apr 2020 22:35:08 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 22:35:14 GMT
RUN set -x;     npm install -g rtlcss
# Thu, 16 Apr 2020 22:35:14 GMT
ENV ODOO_VERSION=13.0
# Thu, 16 Apr 2020 22:35:15 GMT
ARG ODOO_RELEASE=20200121
# Thu, 16 Apr 2020 22:35:15 GMT
ARG ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
# Thu, 16 Apr 2020 22:36:24 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 16 Apr 2020 22:36:25 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 16 Apr 2020 22:36:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 16 Apr 2020 22:36:26 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 16 Apr 2020 22:36:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 16 Apr 2020 22:36:26 GMT
EXPOSE 8069 8071
# Thu, 16 Apr 2020 22:36:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 16 Apr 2020 22:36:27 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 16 Apr 2020 22:36:27 GMT
USER odoo
# Thu, 16 Apr 2020 22:36:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 22:36:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66325385ddfb471e56d91532ad6c4f6a3d7e063a8fac1fabccd0364a6eb362b7`  
		Last Modified: Thu, 16 Apr 2020 22:42:43 GMT  
		Size: 203.6 MB (203558833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dbdfdea4dd0efbcf5b00db0e1eb38dda90e3488e3384be83a682ad98a93544`  
		Last Modified: Thu, 16 Apr 2020 22:41:53 GMT  
		Size: 2.3 MB (2332477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452732a285fe366bd1c590479def3e69b40c59c7c38fe8365e38b2ade6d96823`  
		Last Modified: Thu, 16 Apr 2020 22:41:53 GMT  
		Size: 1.1 MB (1090307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce037cf8d9123bc2c9122c978df0483a91a0fabdcbe2a09c39456df908bc184e`  
		Last Modified: Thu, 16 Apr 2020 22:42:30 GMT  
		Size: 142.3 MB (142324578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aec3e880957f943a8ca570ffbc1d523a920b1a27a2524fb348706f6d755a2ad`  
		Last Modified: Thu, 16 Apr 2020 22:41:52 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cd1d26a9712969c3748400abae722d9497badfc9fda3116fa222f027918ea6`  
		Last Modified: Thu, 16 Apr 2020 22:41:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84481a476030ad4423b9a3fa8f7738eae9ae9ef86c378706e56c5b92349b6971`  
		Last Modified: Thu, 16 Apr 2020 22:41:52 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76cfd77135a0254ae710bb88e2ee473987f9fed20651c93c189d6be890f4e38`  
		Last Modified: Thu, 16 Apr 2020 22:41:52 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `odoo:latest`

```console
$ docker pull odoo@sha256:2aa656a0bbc256846021767626f16a86248af27bf1df77abe31b04f4c30b9d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:dce86bfbf5d790d4565b138217c7915243a4da57e92a11a8daa5215875ded838
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.4 MB (376406747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728c08742855a3bc22efa0479e1bc0f2350362b9efe60d949f45d9308571dd2f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 22:33:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 16 Apr 2020 22:33:23 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 22:34:56 GMT
RUN set -x;         apt-get update         && apt-get install -y --no-install-recommends             ca-certificates             curl             dirmngr             fonts-noto-cjk             gnupg             libssl-dev             node-less             npm             python3-num2words             python3-pip             python3-phonenumbers             python3-pyldap             python3-qrcode             python3-renderpm             python3-setuptools             python3-slugify             python3-vobject             python3-watchdog             python3-xlrd             python3-xlwt             xz-utils         && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.stretch_amd64.deb         && echo '7e35a63f9db14f93ec7feeb0fce76b30c08f2057 wkhtmltox.deb' | sha1sum -c -         && apt-get install -y --no-install-recommends ./wkhtmltox.deb         && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 16 Apr 2020 22:35:08 GMT
RUN set -x;         echo 'deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main' > /etc/apt/sources.list.d/pgdg.list         && export GNUPGHOME="$(mktemp -d)"         && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'         && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"         && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc         && gpgconf --kill all         && rm -rf "$GNUPGHOME"         && apt-get update          && apt-get install -y postgresql-client         && rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 22:35:14 GMT
RUN set -x;     npm install -g rtlcss
# Thu, 16 Apr 2020 22:35:14 GMT
ENV ODOO_VERSION=13.0
# Thu, 16 Apr 2020 22:35:15 GMT
ARG ODOO_RELEASE=20200121
# Thu, 16 Apr 2020 22:35:15 GMT
ARG ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
# Thu, 16 Apr 2020 22:36:24 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN set -x;         curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb         && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -         && dpkg --force-depends -i odoo.deb         && apt-get update         && apt-get -y install -f --no-install-recommends         && rm -rf /var/lib/apt/lists/* odoo.deb
# Thu, 16 Apr 2020 22:36:25 GMT
COPY file:172308c3aaff854a6daab6713c49c8fb84bf96ef2503f0209ef7502dd7574931 in / 
# Thu, 16 Apr 2020 22:36:25 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Thu, 16 Apr 2020 22:36:26 GMT
# ARGS: ODOO_RELEASE=20200121 ODOO_SHA=770d71cfafb9a8f8419b88f8033b964d5742ad57
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Thu, 16 Apr 2020 22:36:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 16 Apr 2020 22:36:26 GMT
EXPOSE 8069 8071
# Thu, 16 Apr 2020 22:36:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 16 Apr 2020 22:36:27 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Thu, 16 Apr 2020 22:36:27 GMT
USER odoo
# Thu, 16 Apr 2020 22:36:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 22:36:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66325385ddfb471e56d91532ad6c4f6a3d7e063a8fac1fabccd0364a6eb362b7`  
		Last Modified: Thu, 16 Apr 2020 22:42:43 GMT  
		Size: 203.6 MB (203558833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dbdfdea4dd0efbcf5b00db0e1eb38dda90e3488e3384be83a682ad98a93544`  
		Last Modified: Thu, 16 Apr 2020 22:41:53 GMT  
		Size: 2.3 MB (2332477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452732a285fe366bd1c590479def3e69b40c59c7c38fe8365e38b2ade6d96823`  
		Last Modified: Thu, 16 Apr 2020 22:41:53 GMT  
		Size: 1.1 MB (1090307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce037cf8d9123bc2c9122c978df0483a91a0fabdcbe2a09c39456df908bc184e`  
		Last Modified: Thu, 16 Apr 2020 22:42:30 GMT  
		Size: 142.3 MB (142324578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aec3e880957f943a8ca570ffbc1d523a920b1a27a2524fb348706f6d755a2ad`  
		Last Modified: Thu, 16 Apr 2020 22:41:52 GMT  
		Size: 673.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cd1d26a9712969c3748400abae722d9497badfc9fda3116fa222f027918ea6`  
		Last Modified: Thu, 16 Apr 2020 22:41:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84481a476030ad4423b9a3fa8f7738eae9ae9ef86c378706e56c5b92349b6971`  
		Last Modified: Thu, 16 Apr 2020 22:41:52 GMT  
		Size: 592.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76cfd77135a0254ae710bb88e2ee473987f9fed20651c93c189d6be890f4e38`  
		Last Modified: Thu, 16 Apr 2020 22:41:52 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
