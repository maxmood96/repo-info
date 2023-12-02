## `postgres:11-bookworm`

```console
$ docker pull postgres@sha256:caf76c09bd20a22215ef3dcf319cec3525cbe8553560a5470a1dbfab17b0555d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:11-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:32189a1bb1aa70a6349fa92f0b9dd077bafec6590ead8fdf4876b19656692961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (147047121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd38faaf4d4293fc31583ac099b6501c6419721f6a66db1ed605232e74806de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 19:02:26 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_MAJOR=11
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PG_VERSION=11.22-1.pgdg120+1
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 19:02:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 19:02:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 19:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 19:02:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 19:02:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 19:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa29d5ddae2e68d0086d91c1bf2bb182b3e9f48248a2c9b45e099939827f6641`  
		Last Modified: Tue, 21 Nov 2023 06:17:49 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acccd9ecaf78093ff51700da5d49ea6dc521d8d7e84bea6c410f5a12286f6aa`  
		Last Modified: Tue, 21 Nov 2023 06:17:49 GMT  
		Size: 4.4 MB (4422703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4026820b7e9666a48e701858638d011e7ac1427faf05041a0aa9563540e61ae`  
		Last Modified: Tue, 21 Nov 2023 06:17:49 GMT  
		Size: 1.4 MB (1448545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce5081f67196b9ad52b7d876b34c81c73d735d2d7633a3b2dcdf00818e7f467`  
		Last Modified: Tue, 21 Nov 2023 06:17:50 GMT  
		Size: 8.1 MB (8067886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1af0f7d4c0d6e80fecac664bc989bcfac6b80d2caed71e367558a64f0b89ab`  
		Last Modified: Tue, 21 Nov 2023 06:17:50 GMT  
		Size: 1.2 MB (1195083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad12215fa6b03a78e717f7e9315e72110a57e97adcb822a07840ef03c9280753`  
		Last Modified: Tue, 21 Nov 2023 06:17:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941c1900c41e9ce78a57a20b35ef6839c1a569f7b9708c4ba56ef8445b76f794`  
		Last Modified: Tue, 21 Nov 2023 06:17:50 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb3f5bba1dc0e3068378bea75270b741ef61417e9dde8c9da00813a0b52816b`  
		Last Modified: Tue, 21 Nov 2023 06:17:54 GMT  
		Size: 102.7 MB (102745168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70078308030193857bbae1e07c878a614b693ac442f5df7e8eb062c4b10c6a1e`  
		Last Modified: Tue, 21 Nov 2023 06:17:51 GMT  
		Size: 8.3 KB (8322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c03ce6d52043ee028c37dfd2d4d427d68dbbfb696d6762fd45007898556b44`  
		Last Modified: Tue, 21 Nov 2023 06:17:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86ada98513322aa30f153bf37259ea22135d51182cd51dd4ba1727d63ee2812`  
		Last Modified: Tue, 21 Nov 2023 06:17:52 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1175b0e755f8a5e52475e3448b8b80e01a4ffc9bb2b07706cebba839fbe141eb`  
		Last Modified: Tue, 21 Nov 2023 06:17:52 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5da0c3d2816077485649d516f654f3717e22b00f9b0d5a0fe46591fb132062b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4878784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d97fb2afc7589b3238369fb8577be9fbfa27f11f98c8c14b4e42bfd85cdb9ef`

```dockerfile
```

-	Layers:
	-	`sha256:31c1fb08a8420de9d1a4923899d3e0f7314bb9d2cf85b05b339795fc7e04dd23`  
		Last Modified: Tue, 21 Nov 2023 06:17:49 GMT  
		Size: 4.8 MB (4828749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3871d61ca308eb579c38358e74e996836a9f4e096d05ad15171e131f51ebc69a`  
		Last Modified: Tue, 21 Nov 2023 06:17:49 GMT  
		Size: 50.0 KB (50035 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:9afd83a701749bb2e7c55ac07bd5ebed4ab5648c8457e1b43bbe4c21fcfbde41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139795518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2407241663a9c1162e58f0c26e7ecd7b90060f5768832bee3cd84bbebcda9b13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 05:00:51 GMT
ADD file:1ae8e5ac45b11d01083680b765e1fcfef9f7938f89d6f424572126fa946d8cdf in / 
# Tue, 21 Nov 2023 05:00:52 GMT
CMD ["bash"]
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV LANG=en_US.utf8
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PG_MAJOR=11
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PG_VERSION=11.22-1.pgdg120+1
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 30 Nov 2023 00:11:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Nov 2023 00:11:07 GMT
STOPSIGNAL SIGINT
# Thu, 30 Nov 2023 00:11:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 30 Nov 2023 00:11:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f476aef5b6e1122850e68c81ef06fc2df17e968961b060483b4d2fb33018aae3`  
		Last Modified: Tue, 21 Nov 2023 05:03:55 GMT  
		Size: 26.9 MB (26922153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c863ca7dc37cc9d54f09d80f7efc95fc0178e7b263ee207d87b3e389318d50b`  
		Last Modified: Tue, 21 Nov 2023 19:33:50 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7dffa6f88c3231ae065b2ac8a5761d4fb2714fc9b620e0ce18c6a4e117c180`  
		Last Modified: Tue, 21 Nov 2023 19:33:51 GMT  
		Size: 4.0 MB (4040458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618ddb4421135e804b37d405cea3e86e469b42c704021086f6ee0061670f7084`  
		Last Modified: Tue, 21 Nov 2023 19:33:51 GMT  
		Size: 1.4 MB (1426029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455859c961c410c425f9371753d5cbd993096afe0f87500c5f1e96e07048815f`  
		Last Modified: Tue, 21 Nov 2023 19:33:51 GMT  
		Size: 8.1 MB (8067930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca058b52570a9e9b7bb7b375680edb208b96c6638aadcef52ed9cfa232f0743`  
		Last Modified: Tue, 21 Nov 2023 19:33:52 GMT  
		Size: 1.2 MB (1193943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38ac683c54e9d588bab738d12f1697b58ada140b9d7b6341cfbfcb39542d9d9`  
		Last Modified: Tue, 21 Nov 2023 19:33:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851553c31be3fb45927fad8181b4d58067a5c9a020f90c5f984c4720cfb297fb`  
		Last Modified: Tue, 21 Nov 2023 19:33:52 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd74ad4491a705c99659b791539c7f33e7ea3db744998a3aa334824fcc3c67f5`  
		Last Modified: Tue, 21 Nov 2023 22:12:02 GMT  
		Size: 98.1 MB (98127175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bc2c9bafa017e13a9fb137ca170a9190e6cf0a191bba45fb6f3bafa53acc1c`  
		Last Modified: Tue, 21 Nov 2023 22:11:58 GMT  
		Size: 8.3 KB (8324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45065954f689b34da93802e57eb61215d4c4771eb94835d341c87dd3ea51bc25`  
		Last Modified: Fri, 01 Dec 2023 22:18:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78923a5682b24748962d78e93f7b817932d2130bfa751e05f2869141de9290f`  
		Last Modified: Fri, 01 Dec 2023 22:18:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307f3f02d6af42c077a1ce695e3f70cf9ab302ac29761ffd92f5ac495a6fe40a`  
		Last Modified: Fri, 01 Dec 2023 22:18:33 GMT  
		Size: 4.8 KB (4780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:08a4fb71e6e250c7bd71844a5ee77603d476169293396e7a00cd5f686484d048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 KB (49837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55fa520b7a87b70540b99e42fdbfda4afceaac4b39d27ad95a94f8708c82c60`

```dockerfile
```

-	Layers:
	-	`sha256:18908c835aa42b60275a4bfff792fd977dbbdbc9aa967c424d4a7ca6b6461eef`  
		Last Modified: Fri, 01 Dec 2023 22:18:33 GMT  
		Size: 49.8 KB (49837 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b70e1ad1036b82b77a62e415d1535992cca631e3949484cdc306121ef54039ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134807813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631e5aea0729982b8c8e6d95d30c64e06f3fdd725c1978d1093fd08711257975`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 03:57:43 GMT
ADD file:b693944382a95fa47622fde77eb98f0cdeafa40261e7334bd355e00f650b6632 in / 
# Tue, 21 Nov 2023 03:57:43 GMT
CMD ["bash"]
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV LANG=en_US.utf8
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PG_MAJOR=11
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PG_VERSION=11.22-1.pgdg120+1
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 30 Nov 2023 00:11:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Nov 2023 00:11:07 GMT
STOPSIGNAL SIGINT
# Thu, 30 Nov 2023 00:11:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 30 Nov 2023 00:11:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b4ce590529bbcf84326048a22fce76fcfcb5c60af5519debd7935a74c1e9126e`  
		Last Modified: Tue, 21 Nov 2023 04:01:50 GMT  
		Size: 24.7 MB (24748925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21f4aebb739ffe9e0940e28d247a8da2f821a7f31a7802ddbeec56c29d382fe`  
		Last Modified: Wed, 22 Nov 2023 01:33:09 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8cff5cb7280b5e856a5c26b4275967808fa3cd8f286358a620731f3890ddf5`  
		Last Modified: Wed, 22 Nov 2023 01:33:09 GMT  
		Size: 3.6 MB (3645045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1afbab58653c806dee1842134bc232fc8cc4443e53a1fe16a5c8e0585e94bce`  
		Last Modified: Wed, 22 Nov 2023 01:33:09 GMT  
		Size: 1.4 MB (1416140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e223d57922c86fb53eee7a89d66e8928409562d66b276b2a7fb121c997054dc0`  
		Last Modified: Wed, 22 Nov 2023 01:33:10 GMT  
		Size: 8.1 MB (8067889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326ab74a3f8493265ec860fd62d15f34dbf491c787bbc030c214ee3e35cbdfc7`  
		Last Modified: Wed, 22 Nov 2023 01:33:10 GMT  
		Size: 1.1 MB (1065924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85273e10b04abf86fdd4cfd58839d0457c8a52b94927a0085fda8527a7eb8eba`  
		Last Modified: Wed, 22 Nov 2023 01:33:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d759abb828279091b19672436eedd188e080b8f24632d0f84c9a990f293319a`  
		Last Modified: Wed, 22 Nov 2023 01:33:10 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b461740655ff398d6dcb88da7d7fb59af5f174c967ca2ba6801c5aa53038cbed`  
		Last Modified: Wed, 22 Nov 2023 04:07:15 GMT  
		Size: 95.8 MB (95846055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91bd7a1e3918f037af6d42096d41d77c79752364ec3ad9ca53912119e98a4e`  
		Last Modified: Wed, 22 Nov 2023 04:07:11 GMT  
		Size: 8.3 KB (8326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3648b7f427daa3a42f858565684335360030fe1562642a844a7d8201683995`  
		Last Modified: Fri, 01 Dec 2023 22:38:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25af871c5ad0355d9f70f2c432850b0fa80247bd9e78c046c91b5b82b96bac16`  
		Last Modified: Fri, 01 Dec 2023 22:38:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63654f25a6925044dfe4d5251d691d9a5d58805575dc42ed93f3449b798eef4`  
		Last Modified: Fri, 01 Dec 2023 22:38:22 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1421017d91c388afe99b7a6592aa7dbc73883452b1a28b95e1155a395f6e50da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3cd5c559ff7889904530750833ccabc52cc712d6d3dd97a6088b9f29a94770`

```dockerfile
```

-	Layers:
	-	`sha256:c621cdd78c22de14de2824bb7e9faf958d55fbddc6dac3c29161cb3b7125b8c1`  
		Last Modified: Fri, 01 Dec 2023 22:38:22 GMT  
		Size: 4.8 MB (4840787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7528ecadd39e4de95c5975d65ea73afcdea463c0f8baab8410355965e12a38d`  
		Last Modified: Fri, 01 Dec 2023 22:38:21 GMT  
		Size: 50.1 KB (50051 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:be4bfc670994840e0822c120873466b3a6783bc7667f89871d5804e0ced799d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145302125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7f0fc3e331f73c3aa6c95772baca9f31da42d2587c4c1ce7522c110a5e141b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV LANG=en_US.utf8
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PG_MAJOR=11
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PG_VERSION=11.22-1.pgdg120+1
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 30 Nov 2023 00:11:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Nov 2023 00:11:07 GMT
STOPSIGNAL SIGINT
# Thu, 30 Nov 2023 00:11:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 30 Nov 2023 00:11:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cceff339129572dbb692e7aa1ed4221a7ffc75cf59151c83b04ff8dc59e069c`  
		Last Modified: Wed, 22 Nov 2023 11:51:51 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205f857684f5cbc32a359894eac031b9e3228e9e600f87a016db9921226bf202`  
		Last Modified: Wed, 22 Nov 2023 11:51:51 GMT  
		Size: 4.4 MB (4383844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba82cb23b34b9baa62d2db06ae15164a9877c18aa858187007c9aecdc11f25`  
		Last Modified: Wed, 22 Nov 2023 11:51:51 GMT  
		Size: 1.4 MB (1380715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bdcf4e4d625179b6cdca8bb63f4f22cd4a04becdd488d4e41a6c7b51bd494b`  
		Last Modified: Wed, 22 Nov 2023 11:51:51 GMT  
		Size: 8.1 MB (8067935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ce7bf87298edf9a9cebc92c39207f310cf48d21dd2388090285ae757661b73`  
		Last Modified: Wed, 22 Nov 2023 11:51:52 GMT  
		Size: 1.1 MB (1107732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53521cca1206cc645107b20f50b6613f0f282e10b9ed7d885ebdbe839004eeb1`  
		Last Modified: Wed, 22 Nov 2023 11:51:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d4091d2a8b6ee3356c1da8b550408ef9e6c726ab9e69d2f82f867407cfa1b2`  
		Last Modified: Wed, 22 Nov 2023 11:51:52 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d60d1c2dd4e94eb321f75df594e2be2ba12202333e9e92e8485147bb5aa015`  
		Last Modified: Wed, 22 Nov 2023 12:21:31 GMT  
		Size: 101.2 MB (101164790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dac95d0a7ee8a60b9c379076119048726fba79a5493796a5c8781f37f123575`  
		Last Modified: Wed, 22 Nov 2023 12:21:28 GMT  
		Size: 8.3 KB (8321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba625eeb6c18da43f086bcc0a5a183f08b5d801e6cff35d90d406c08d65a67c9`  
		Last Modified: Fri, 01 Dec 2023 22:35:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0490def31df5f31e2077695c838abe63943f3e2ad4c7d0acebcc35a4b9f5d9b9`  
		Last Modified: Fri, 01 Dec 2023 22:35:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa39a199395a619b1d4677c7b9e4fe980cd2b8dd30c8355f991341c95f79767`  
		Last Modified: Fri, 01 Dec 2023 22:35:12 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:080a7eb7ba6187f0b38704c8ec60210ef98ca0c67addf6e2e7ba90540cb6a22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4884284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5722cf3f24b65f205b0da99ef2e6774746e24ba05ff60bec017d916a8766ec0`

```dockerfile
```

-	Layers:
	-	`sha256:80ca11bce1f3fd88b0c6396fc0f01db25757fc9e2760c544e869077bf6438e22`  
		Last Modified: Fri, 01 Dec 2023 22:35:12 GMT  
		Size: 4.8 MB (4834405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfb3858c6220138241cb3ebd15ca08cb392c2a27789e733f3b1dea9f4b0c9375`  
		Last Modified: Fri, 01 Dec 2023 22:35:11 GMT  
		Size: 49.9 KB (49879 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:0f337e9e49e853a4eb654ec0ee16a6cab9f4515a24f41eb37849694293a222a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151888720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d160a7ca1cd2ea64b27e0051c1af408b2e13d587bf0b0df3aa2326a2fa9356f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 10 Aug 2023 18:02:22 GMT
ADD file:0c94521fdd9c0a4fdeeb9aad23e68cd053fba0dcd7c3af550aefa79377816e31 in / 
# Thu, 10 Aug 2023 18:02:22 GMT
CMD ["bash"]
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
ENV GOSU_VERSION=1.16
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
ENV LANG=en_US.utf8
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
ENV PG_MAJOR=11
# Thu, 10 Aug 2023 18:02:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 10 Aug 2023 18:02:22 GMT
ENV PG_VERSION=11.21-1.pgdg120+1
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 10 Aug 2023 18:02:22 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 10 Aug 2023 18:02:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 10 Aug 2023 18:02:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Aug 2023 18:02:22 GMT
STOPSIGNAL SIGINT
# Thu, 10 Aug 2023 18:02:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 10 Aug 2023 18:02:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:98bdfce9af831c2a0d0bfcca812d0039cd1666986550f552b4b4c625bd5aa31c`  
		Last Modified: Wed, 01 Nov 2023 00:43:26 GMT  
		Size: 30.2 MB (30164042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9558ee1456705c9615d7bf9c503ae3fdd5e9feafb05984a63937fe44f2882020`  
		Last Modified: Wed, 01 Nov 2023 01:17:46 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634f1bbbcc1566951b5f05beda10c6942d75edbb370d6da1792f88ab5251f3f2`  
		Last Modified: Wed, 01 Nov 2023 01:17:46 GMT  
		Size: 4.8 MB (4844468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3296367646b1479375e970f55175c8a74fb76f06408b44a2444b8bf62e32f7`  
		Last Modified: Wed, 01 Nov 2023 01:17:46 GMT  
		Size: 1.4 MB (1424522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8246c8f037dac021106e169a69786ac9da8a188ea7e4945a1dd7d6aba054f5`  
		Last Modified: Wed, 01 Nov 2023 01:17:47 GMT  
		Size: 8.1 MB (8067913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b0c9ea2d500556dd33a654d00a7ca49d20321a109f745dbdaaf44145f1180e`  
		Last Modified: Wed, 01 Nov 2023 01:17:47 GMT  
		Size: 1.1 MB (1136169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c8520fea571d4a3e4ab6ea2691d34e345d8951c93069f567c9f50ea77b6388`  
		Last Modified: Wed, 01 Nov 2023 01:03:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357ab8271670fdb088e878280ba276cb22ef7a469b10ed3075e62a1466186ad7`  
		Last Modified: Wed, 01 Nov 2023 01:03:25 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3f3e369112a524bf1108403be70c53fcf9c2f8edb0be1f594f343d7546be69`  
		Last Modified: Wed, 01 Nov 2023 01:17:53 GMT  
		Size: 106.2 MB (106233767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0f0dee1523ce477616fc8208ff36719d49dde727fcac00cc81c01fe1eb869f`  
		Last Modified: Wed, 01 Nov 2023 01:17:47 GMT  
		Size: 8.3 KB (8330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9614500eaa762668548f296b0d8de2f13b1affd3e927f96ac2f1221245802623`  
		Last Modified: Wed, 01 Nov 2023 01:17:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbe48076aa39434d5591c5905f31680da98de8380342117ce2eb1f37a307ec2`  
		Last Modified: Wed, 01 Nov 2023 01:17:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45fd9ed1a177a7334cc9190c55b1a68d14fe0978140dbe24dc27f7bb36d95e`  
		Last Modified: Wed, 01 Nov 2023 01:17:48 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:162372cb34cc3defeef916ae280a9e2c585cfd8ab5112e1964238003d7c01989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 KB (49781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345b2e4b1ce55f4ef094844941f57e1b1decddaced3bc8be48151f6243776d84`

```dockerfile
```

-	Layers:
	-	`sha256:81ccb1656562910b484c747e621308530f2b33b0e87f03099fd01fa25ea7ea83`  
		Last Modified: Wed, 01 Nov 2023 01:17:45 GMT  
		Size: 49.8 KB (49781 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:4b93cc31d9363fd56306cbb8c8f0ea4d39009b766fafddb93e33ff78866330fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143130012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d514c50656ec78b3ae8c943137826daeb4e46b6cad1551d6baf351c7213d3553`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 04:09:50 GMT
ADD file:e093749192323dc72b60a8440ddba26c415586f618b5e107fa264ba5eb2ca7ba in / 
# Tue, 21 Nov 2023 04:09:54 GMT
CMD ["bash"]
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV LANG=en_US.utf8
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PG_MAJOR=11
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PG_VERSION=11.22-1.pgdg120+1
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 30 Nov 2023 00:11:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Nov 2023 00:11:07 GMT
STOPSIGNAL SIGINT
# Thu, 30 Nov 2023 00:11:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 30 Nov 2023 00:11:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ebdff2138fee4a3ec27560ab1353dc51c12c2608ff721f5db3d24104872b702a`  
		Last Modified: Tue, 21 Nov 2023 04:20:35 GMT  
		Size: 29.1 MB (29141984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871b96f8117e597e34b3c42046e069e9a9853742b6dc729e7b535c28bfc6779d`  
		Last Modified: Thu, 23 Nov 2023 02:23:22 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7fcc8f2d432d7771d17e625701b453db95c7027f1032834c3a62ab676cf317`  
		Last Modified: Thu, 23 Nov 2023 02:23:23 GMT  
		Size: 4.4 MB (4355757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83300bed39f72a033140a846a97f7266adf45bd0b6d84e37ed437a40d612bb9b`  
		Last Modified: Thu, 23 Nov 2023 02:23:23 GMT  
		Size: 1.3 MB (1335999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7e2fba0bdd77ec3166ca923dd6a279b53177ac4c996eff47553411057f6458`  
		Last Modified: Thu, 23 Nov 2023 02:23:24 GMT  
		Size: 8.1 MB (8068141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce0bdd1562b4671180c14ee1f065b11fddaef70c8b3ed2d93183195153c4a39`  
		Last Modified: Thu, 23 Nov 2023 02:23:24 GMT  
		Size: 1.2 MB (1181570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcca17a3e4955db19e17fbaf970a3515578cc080fa3dc9498e054766268c96ff`  
		Last Modified: Thu, 23 Nov 2023 02:23:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6169d401417f1a1c36c835cfdfc41d14fa36b4866061a4d54a76ae67690f828f`  
		Last Modified: Thu, 23 Nov 2023 02:23:24 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35be4f2be5b53a2d508486348ea46418627824655e1e8278026a0e5d077a4d0`  
		Last Modified: Thu, 23 Nov 2023 13:10:45 GMT  
		Size: 99.0 MB (99028711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940e62f7a2e2b1236d9254258b6b238876d730a5b80e58df30923c6bcae60c11`  
		Last Modified: Thu, 23 Nov 2023 13:10:35 GMT  
		Size: 8.3 KB (8326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2750d97e384c3e35e12e1c78df6415047fafd79bf2aea2de030b7888e3be3fb1`  
		Last Modified: Fri, 01 Dec 2023 22:25:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99770dbd58d65faf241c2312cdca2b479b2020f2d690dfeac7770d8d47a2f855`  
		Last Modified: Fri, 01 Dec 2023 22:25:52 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1991eb7c7a521c3a93461c3aa1278887f797afe4040d9955d58dc16f7565d03`  
		Last Modified: Fri, 01 Dec 2023 22:25:52 GMT  
		Size: 4.8 KB (4793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:63e1944a13b749b8350cf4879976172d9d47e9357d93b5d41a4edf17ef7ea3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 KB (49722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2244ca2a9819fea26fa8cdd41ea92d543b5486232e472043865c22558a22ddd`

```dockerfile
```

-	Layers:
	-	`sha256:1d09feab8d4337e7d5712824181325742008726ca0d079600bc262115180f46b`  
		Last Modified: Fri, 01 Dec 2023 22:25:51 GMT  
		Size: 49.7 KB (49722 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:f2f53f74aabd6c389b1cee3c896fdb98f727dfc21d7b0e230d2fbf0f5042037a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159117765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39835db03c519148f1b82c4114aa37acaeca208ff0503c9b847bcea44e145df0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:14 GMT
ADD file:8b22a531b6611a1e63dfc20e4e2931592e2d821bd4b64c4b2810bb9a36640c02 in / 
# Tue, 21 Nov 2023 04:24:16 GMT
CMD ["bash"]
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV LANG=en_US.utf8
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PG_MAJOR=11
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PG_VERSION=11.22-1.pgdg120+1
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 30 Nov 2023 00:11:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Nov 2023 00:11:07 GMT
STOPSIGNAL SIGINT
# Thu, 30 Nov 2023 00:11:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 30 Nov 2023 00:11:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c570d04e61d8e35a3c8f12179d048d701451f97f9cf2099ea3e3738512dbf062`  
		Last Modified: Tue, 21 Nov 2023 04:28:58 GMT  
		Size: 33.1 MB (33141607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2e1444eb5768a9f1452aad0278ed3b46e23bd0ddcdd4834e4c0c3f04f7a564`  
		Last Modified: Tue, 21 Nov 2023 23:54:59 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa03b72cb005f7e4b1680abe9b55b766463104336988c455382e20b7bd83ffe`  
		Last Modified: Tue, 21 Nov 2023 23:54:59 GMT  
		Size: 5.2 MB (5239246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cb219c2b2f2937086d88d617001b3022093e4bdb6b1b0f88c97f0800c1b221`  
		Last Modified: Tue, 21 Nov 2023 23:54:59 GMT  
		Size: 1.4 MB (1370020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6683bf2a8c7507cae2fa66734a9b0dd44e7a5edfa7c15f56e3aa13d1d24746b`  
		Last Modified: Tue, 21 Nov 2023 23:54:59 GMT  
		Size: 8.1 MB (8067975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fad52c1ffb1abca80e3c384eae4d1ff82626f93d1a47b7b5d6bed759b2ea262`  
		Last Modified: Tue, 21 Nov 2023 23:55:00 GMT  
		Size: 1.3 MB (1282723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32f3822a2b323554f1523ec550320313c2667d02f32f3741e18b559bc1cb1c`  
		Last Modified: Tue, 21 Nov 2023 23:55:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cef556f3a7efce5653c049120b84c12d5783336b1022c9e5039988e03fc155`  
		Last Modified: Tue, 21 Nov 2023 23:55:01 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1abc541b06d11b04ea0921a67c856baf8925b9927eb197ffa7062389937aea`  
		Last Modified: Wed, 22 Nov 2023 00:09:37 GMT  
		Size: 110.0 MB (109998360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54862cf4b128922dc390cb54054cc8c74b467c96b3f05b9d50ee4ac9a1982d8e`  
		Last Modified: Wed, 22 Nov 2023 00:09:34 GMT  
		Size: 8.3 KB (8325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8692d29fe96c6ea78fd84277c60e172232f57dc2bcdad204c6fae34bcc83a4aa`  
		Last Modified: Fri, 01 Dec 2023 22:36:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7b9e4ff14de4233b3d306a94a9ef020920ddae5fb99328cf1ef23a4b50f315`  
		Last Modified: Fri, 01 Dec 2023 22:36:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c4848c6b29e654676a4f7a35b5546496d2aa0490d664354a2fcde0cb4c7c1b`  
		Last Modified: Fri, 01 Dec 2023 22:36:56 GMT  
		Size: 4.8 KB (4782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:fc50b9cfaa4a2aeba30620c2fa5a13e745956b8a70884236043b438903024858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4885885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d1149d7287a8706f437034d31697b3bd635207d6803ed217ce337febc73799`

```dockerfile
```

-	Layers:
	-	`sha256:64a10ba1b87b1ccfedb060f29ad2f8091e385b4d2d96d7d9cceb2f23f49fce0e`  
		Last Modified: Fri, 01 Dec 2023 22:36:56 GMT  
		Size: 4.8 MB (4835966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c197a834aef094b3b5375931366a32d61954b8d93e104444fe52ae60f9ff4a75`  
		Last Modified: Fri, 01 Dec 2023 22:36:55 GMT  
		Size: 49.9 KB (49919 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:11-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:bcfce6c7b1db634d663a187169d6c929967b491f0f602dbdf9915482c6bbf2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152613288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa87de6b4a055eee0d4171c2b8cb596f8e5ba8c04bfd60aa6d9c4fb6022993e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Nov 2023 05:04:35 GMT
ADD file:c33fa9fdde73983850798b6eb1cd062e0398109d1d773e6a937fead7475c8efc in / 
# Tue, 21 Nov 2023 05:04:41 GMT
CMD ["bash"]
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV GOSU_VERSION=1.16
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV LANG=en_US.utf8
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PG_MAJOR=11
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PG_VERSION=11.22-1.pgdg120+1
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 30 Nov 2023 00:11:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 30 Nov 2023 00:11:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 Nov 2023 00:11:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Nov 2023 00:11:07 GMT
STOPSIGNAL SIGINT
# Thu, 30 Nov 2023 00:11:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 30 Nov 2023 00:11:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6daa625e5a040476e253e7acd0befa74254a4865ec836d6334a544d82a21d4be`  
		Last Modified: Tue, 21 Nov 2023 05:10:21 GMT  
		Size: 27.5 MB (27512885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89216ae53f720b4da9522deb1c8896d66a743dbc83d0ab5356ccf6bf6c0ad8e4`  
		Last Modified: Tue, 21 Nov 2023 18:22:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd1123ed4c50e7e0d7ff3fb10d11792421107339b8201d7dea2bde635cf5d86`  
		Last Modified: Tue, 21 Nov 2023 18:22:46 GMT  
		Size: 4.3 MB (4278291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d8142ebc194d7418f51ad332e0a79f3e1a575f2503f46b4f93cb085d5812f4`  
		Last Modified: Tue, 21 Nov 2023 18:22:46 GMT  
		Size: 1.4 MB (1414350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06692ba87c4c56ba5fa93bef232b01a7087875351540daebfdff46dd5c3bc834`  
		Last Modified: Tue, 21 Nov 2023 18:22:46 GMT  
		Size: 8.1 MB (8122208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6068c51b298204ad2608f4a906160c9749c057bc056e26b1ba79715761b391c0`  
		Last Modified: Tue, 21 Nov 2023 18:22:47 GMT  
		Size: 1.1 MB (1095680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b031c4de2d2726bdaa88b1fb2ff2bef864e96adb293b76faaa47facd0235ea`  
		Last Modified: Tue, 21 Nov 2023 18:22:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2508545e1ea1dbe7e27a83463f8337ac42fcfb626c048a9e6364b34354a0a24`  
		Last Modified: Tue, 21 Nov 2023 18:22:47 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5064d7af4d564c8c929eadfd2d53a57e0d6069a62496d08eca5c2fa9bd309955`  
		Last Modified: Tue, 21 Nov 2023 18:59:12 GMT  
		Size: 110.2 MB (110172041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd8ef48256d33c4489949ea9b7e54f503342e8dd55fbf7805e31c4142e3d83d`  
		Last Modified: Tue, 21 Nov 2023 18:59:09 GMT  
		Size: 8.3 KB (8325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2904e04f7814a522b2879523407b53e01db15e2f307304205b145d1c5409278d`  
		Last Modified: Fri, 01 Dec 2023 22:31:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf5cb49ebda1bda8bbd70de0190bb02192cd9f5eba6ce351c00ccca04c7f18c`  
		Last Modified: Fri, 01 Dec 2023 22:31:10 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2567faed4c2a68588f7ae3a2dba8c23b67689f5cdee02f1bd5afb2feb36af9`  
		Last Modified: Fri, 01 Dec 2023 22:31:10 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:11-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b4fcb9d23559159b0b75748c1ad7823720c01a7d8a762e3461e425902ae8f7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4877804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6083690bca1fafcba506a83431c8ed953ba9809079fe3dd6e5a5930f2a5b519e`

```dockerfile
```

-	Layers:
	-	`sha256:87b575f9746188d12fc46d68ed60e2bf6416f3bf95897f28fee52731c692d911`  
		Last Modified: Fri, 01 Dec 2023 22:31:10 GMT  
		Size: 4.8 MB (4827931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08cd7afb5ecda54ed5b89ad282a082f9bf122ef412451218ed47250f31dcd3e6`  
		Last Modified: Fri, 01 Dec 2023 22:31:10 GMT  
		Size: 49.9 KB (49873 bytes)  
		MIME: application/vnd.in-toto+json
