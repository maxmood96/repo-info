## `postgres:18-trixie`

```console
$ docker pull postgres@sha256:7e32e9833a6fb1c92c32552794cb6ed569d51b445a54907d35fc112ef39684db
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:18-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:a145910d7079e9fbf73e6df19d5fcca0ce59d747cf7d97ac772bff28c3759c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162293990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbaa243599038521bbda8f6fa286d2a8fc1236509606f22de81d0739b0610ba7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:32:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:32:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:32:35 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:32:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:32:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:32:40 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:32:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:32:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:32:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:32:43 GMT
ENV PG_MAJOR=18
# Fri, 08 May 2026 19:32:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 19:32:43 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Fri, 08 May 2026 19:32:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:32:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:33:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:33:00 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 19:33:00 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 19:33:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:33:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:33:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:33:00 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:33:00 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:33:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e38a999e99de1f8de18e87b2d73942e944596dcbc73f019bc28e5a05b0a0f8e`  
		Last Modified: Fri, 08 May 2026 19:33:19 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0337286b2934dbf3589d8afa5f345c830f421806ab9223fc4c9cfc325466f000`  
		Last Modified: Fri, 08 May 2026 19:33:20 GMT  
		Size: 6.4 MB (6441238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52cb585fd05009159cf299f3c4eab80b38e13422b3c05897da4dab0f86e3d83`  
		Last Modified: Fri, 08 May 2026 19:33:19 GMT  
		Size: 1.3 MB (1256778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631436d0d0b7115351f80a5f06d927cfe66727a8ea56a4ee9d97bd7642ac2a90`  
		Last Modified: Fri, 08 May 2026 19:33:20 GMT  
		Size: 8.2 MB (8203831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c71b11837a28b64776339400d438f370e9f01589d123215bdf2726628179d28`  
		Last Modified: Fri, 08 May 2026 19:33:21 GMT  
		Size: 1.3 MB (1311682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e4e3208450bc219659d21cc66cce5476e1559d082ac5912ac20a067c282fe5`  
		Last Modified: Fri, 08 May 2026 19:33:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9019a56de83a89fc3095abe1e5631fcf516f1733ac6f449924ecc003ff3bc1d`  
		Last Modified: Fri, 08 May 2026 19:33:21 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550df04ae0706dd1ac23484ed086c39b6248c9aa9cd2deb82492247d4dff4b35`  
		Last Modified: Fri, 08 May 2026 19:33:24 GMT  
		Size: 115.3 MB (115270069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9aa5783c64be74d59991bda8e288a1eb8bf0b579b22feb04b355455ec6804c`  
		Last Modified: Fri, 08 May 2026 19:33:22 GMT  
		Size: 19.3 KB (19331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a21d8601fad8153e8b4d607db6e1e8c46de4d2fd1a65a80bc6d5cc7b5ba8dd`  
		Last Modified: Fri, 08 May 2026 19:33:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7572aa056bba16ab15262c78566a9f3410ac12fd5f06029d0de886777d5391fa`  
		Last Modified: Fri, 08 May 2026 19:33:22 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479918537f5986704705eb567e939c621952dda0757daedc6d24590f27b75de7`  
		Last Modified: Fri, 08 May 2026 19:33:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ae297c7801602ef625beb3ec872a3c1500e79289b5e23dee5ee5c131cd0256bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6009247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0a512436fe66afe7aa7aaf41bf806a5672946f0aecb8a93fe8b36dfa03a05a`

```dockerfile
```

-	Layers:
	-	`sha256:934026d9e7a591651f842ed7816a69aa0a6383037a381dd1611ae4f6da51df9b`  
		Last Modified: Fri, 08 May 2026 19:33:20 GMT  
		Size: 6.0 MB (5956789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771ff4140da50066c2b737605ed3cf390c3db0675459e735f8521248dbb4923b`  
		Last Modified: Fri, 08 May 2026 19:33:19 GMT  
		Size: 52.5 KB (52458 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:ca17403708b6eb948a548b0e280e58e7fafe4d0b7934af5ac7ba885daed224c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91468677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b7cad3f1f75b77fed056c53f5a9414865dbeecb4d6d6606fe115b12c37c177`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:38:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 20:38:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:39:04 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 20:39:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 20:39:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 20:39:12 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 20:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:39:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 20:39:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 20:39:20 GMT
ENV PG_MAJOR=18
# Fri, 08 May 2026 20:39:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 20:39:20 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Fri, 08 May 2026 20:52:33 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 20:52:33 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 20:52:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 20:52:33 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 20:52:33 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 20:52:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:52:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 20:52:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:52:33 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 20:52:33 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 20:52:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824d1a31cb1ff21b3c50a696860a8924edca96924bf27f89211d9df74956e1ec`  
		Last Modified: Fri, 08 May 2026 20:52:46 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7a1c7487f98f9ad72288f61d78491c31bace324f1fa449dfea4d5a298d150f`  
		Last Modified: Fri, 08 May 2026 20:52:46 GMT  
		Size: 5.9 MB (5932544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3594982e8e586aed83abeb74c1f93c85c8f771758dae601dada9a9f5ccf1e862`  
		Last Modified: Fri, 08 May 2026 20:52:46 GMT  
		Size: 1.2 MB (1227597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da3fe89175be77b62f3ecb70be0af34ca73d3609787f70200e81e05481ff060`  
		Last Modified: Fri, 08 May 2026 20:52:47 GMT  
		Size: 8.2 MB (8204272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0006f0dd4d1b9b4940a4aa798995804e256b52484b1cb811a9aa2b65cd345f64`  
		Last Modified: Fri, 08 May 2026 20:52:47 GMT  
		Size: 1.3 MB (1317361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca368e963a2a62899fcf9173322fa2c6af8244273ba1fb7ddae7d3bdaf029632`  
		Last Modified: Fri, 08 May 2026 20:52:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c60eadc3fde8d9121f872f87933073e66110f16f52837cf424e8cb2547e1a12`  
		Last Modified: Fri, 08 May 2026 20:52:48 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0a421538eadbb288586a4aad967e81c440103fb415b6401434044bea81d873`  
		Last Modified: Fri, 08 May 2026 20:52:49 GMT  
		Size: 46.8 MB (46808533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1a3b7160f912b42797b6416da1c88b4338bfe9ec4303dbc3888cd24b80aac1`  
		Last Modified: Fri, 08 May 2026 20:52:49 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c62622d530ad8b40f288de0cd3fee8bf7752a495521398119cade71c490bf74`  
		Last Modified: Fri, 08 May 2026 20:52:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf69e2ce2a5f9e3e14f837b3099c44ea207643f3710c5b72605824de3c21e4c`  
		Last Modified: Fri, 08 May 2026 20:52:49 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c9393ed8bb6cf22eb7e919adac6e08a599c73b5c2dfc35d70320e48e399f82`  
		Last Modified: Fri, 08 May 2026 20:52:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:f5d7cb1054dd6e89022c2f7e3fe34f307a63ca1683f936db0e319ffe20f493ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab64e55b18f9edac4faf54b444d9dacee4798c780e4ffcd92ed94e01fb11e4f`

```dockerfile
```

-	Layers:
	-	`sha256:6ba85f3b10b3b390dd32d08f311d58926c467a0a4ef08d9f9270b17a7fda9f45`  
		Last Modified: Fri, 08 May 2026 20:52:46 GMT  
		Size: 5.1 MB (5119932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aaf063ddb701eb2e23fe6d392c41591e1f622c57335cf6a1ea62be131c9dc7c`  
		Last Modified: Fri, 08 May 2026 20:52:46 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:5b741062715279a1be3bfb8b8d212b487b0648dd4a94a2559204aebf8dcd4984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87794444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e98ae04cc7aab3bc0eefff7b41062e755e1c6c3af940012baf873a61be0a48e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:27:21 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:27:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:27:37 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:27:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:27:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:27:43 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:27:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:27:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:27:49 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:27:49 GMT
ENV PG_MAJOR=18
# Fri, 08 May 2026 19:27:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 19:27:49 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Fri, 08 May 2026 19:39:49 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:39:49 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:39:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:39:49 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 19:39:49 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 19:39:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:39:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:39:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:39:49 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:39:49 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:39:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6a4dcf675c6cfd85362f48cdf1aa780b98744d892653aad396dcceb0490c8f`  
		Last Modified: Fri, 08 May 2026 19:40:02 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e9c51b58df328d65b285cc444a73bed8480392fae42b2151798231136d5c08`  
		Last Modified: Fri, 08 May 2026 19:40:02 GMT  
		Size: 5.5 MB (5496587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4beebb05eb291ed8a0c239ba1d4d844bf94cb8b375c2dd6d20a30729c8d6b93`  
		Last Modified: Fri, 08 May 2026 19:40:02 GMT  
		Size: 1.2 MB (1222404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c24bd0df5e2f53047e6aeab087df28c36b4337a534389731f7abb99fde00299`  
		Last Modified: Fri, 08 May 2026 19:40:02 GMT  
		Size: 8.2 MB (8203994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c18ae1fc18108b1f4b4249988e3bff1b73afa13d701d2d6d8ed55477b5ae84`  
		Last Modified: Fri, 08 May 2026 19:40:03 GMT  
		Size: 1.2 MB (1172600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee6cf7717b9f46de5aca886c1acdc672ed8abbf5e7da81d4412a9fb683afb2`  
		Last Modified: Fri, 08 May 2026 19:40:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1710308ed31c68fac528edd7e4ffa395524d2f136c9cce8ac029019a98e0a10a`  
		Last Modified: Fri, 08 May 2026 19:40:04 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1403a85ce80ecf19ada5f4734eeb0addd893d34208a9db04119c9cb97b03a1f`  
		Last Modified: Fri, 08 May 2026 19:40:06 GMT  
		Size: 45.5 MB (45453764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5119a92901ce52cc91bc6b81fb990158b8d3b0ff45609814fb546cf4da84b2`  
		Last Modified: Fri, 08 May 2026 19:40:05 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2213ca54f627eb8469369b2d2030a5e875af63bca27df316576af7a942a529e`  
		Last Modified: Fri, 08 May 2026 19:40:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c8e352a10eb6e85ff7e73ad89888935ed7c4c94f8c4ae2c4920a2dc4b30404`  
		Last Modified: Fri, 08 May 2026 19:40:05 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf37872ee7f91ec172f8e8ee374e2b3abf5fffd18722d0e01f6905336bd98afc`  
		Last Modified: Fri, 08 May 2026 19:40:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:8178578cafd071b3b70b696097bbd3ccabc8b1685b440f788adaba1ebcfc6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7064c6ea640ee3b0f522f574e3c22f4d06d0eb51deac68bd456be23bcea2838e`

```dockerfile
```

-	Layers:
	-	`sha256:a2dcf83b2477591b9e80d8f94a26b0ad2ca9726d0e7c4192fbeff559bd57d79a`  
		Last Modified: Fri, 08 May 2026 19:40:02 GMT  
		Size: 5.1 MB (5119237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4329d30557853abd5989cfd7345b6f0b5e350e7fa23e916a534f7cdc5f66209b`  
		Last Modified: Fri, 08 May 2026 19:40:02 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:0c24d31b13a9801233f136bc80e908bda9577ab7e9c622e572eebc13c186ed4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160909974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e44620f2c3720714a21ef0761baee9326fcb32851ccf1278fa96d895e766e89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:33:34 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:33:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:33:47 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:33:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:33:53 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:33:53 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:33:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:33:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:33:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:33:57 GMT
ENV PG_MAJOR=18
# Fri, 08 May 2026 19:33:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 19:33:57 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Fri, 08 May 2026 19:34:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:34:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:34:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:34:14 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 19:34:14 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 19:34:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:34:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:34:14 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:34:14 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:34:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167deb8fc2d8597ed99165defc41f1cfa615312b725abf68f9e94da1aa39e5b6`  
		Last Modified: Fri, 08 May 2026 19:34:33 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688d7277ee9e712dba6c12734b1aff450842dbd4d38c21f29b43a7f7c200fecd`  
		Last Modified: Fri, 08 May 2026 19:34:33 GMT  
		Size: 6.2 MB (6234111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554910c5fc75c907c20e7678b916980fc03bfadee7779ade4360dffb36caf9a0`  
		Last Modified: Fri, 08 May 2026 19:34:33 GMT  
		Size: 1.2 MB (1209637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a372f7b42fb9036faf75a654a6fccd9f9ea324a7a89b28c9799c97b4acf27b`  
		Last Modified: Fri, 08 May 2026 19:34:33 GMT  
		Size: 8.2 MB (8203952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f17e0bfab44c099cfb941ac46eb4863a3b200290c476b74f7dcb49b98ded23`  
		Last Modified: Fri, 08 May 2026 19:34:34 GMT  
		Size: 1.2 MB (1220601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bf1d5683980c4ab0640df679ccff5311d6782aeb0be61de81b23469c36ac08`  
		Last Modified: Fri, 08 May 2026 19:34:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dadd2767d3bf9ce4724f69d8ccb3ea9c41b7470767f316e1737e3f9eee698e0`  
		Last Modified: Fri, 08 May 2026 19:34:29 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2655c155e52fa5666cbcec141fa1478ebde4b4ecab3938f4b61c034e611d718`  
		Last Modified: Fri, 08 May 2026 19:34:37 GMT  
		Size: 113.9 MB (113867863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c560e07b5e4c726ee32a933a3b5cc825f287f3e29229c47ab6dc2ea47892b76c`  
		Last Modified: Fri, 08 May 2026 19:34:35 GMT  
		Size: 19.3 KB (19327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e52743438dd72f1781350376a64ef46a52b2be15fee48e545c4c7610cb16b8`  
		Last Modified: Fri, 08 May 2026 19:34:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e1506136f21862552089b3da66eee183fcd39370a54f904ef731addce76506`  
		Last Modified: Fri, 08 May 2026 19:34:36 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e62b28af93bc3ee6d1cb06d03a04daba97f5606af44079af1e8e3f3da3fda8`  
		Last Modified: Fri, 08 May 2026 19:34:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:38ced99ed5db55b67b9d4418cdf444533ba3cbf9e6d67528bd15e17479442a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984d7ed1d6b87a9f19c66af83b108d98f99e4949fc3ee3174d30877214f00111`

```dockerfile
```

-	Layers:
	-	`sha256:5b05ef70135ac4bc9c656939a67e9cd1e4b54eec644f92d3bebc66f86287105c`  
		Last Modified: Fri, 08 May 2026 19:34:33 GMT  
		Size: 6.0 MB (5963162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf8dcb553329f8212001154775e49ad1a7de639ddb4d521d089fd1b02d14e13`  
		Last Modified: Fri, 08 May 2026 19:34:33 GMT  
		Size: 52.7 KB (52736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; 386

```console
$ docker pull postgres@sha256:b0648be764db36ab4f78e105764c6919bc2da15b1e98cac8155707e461492a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97570838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99ada11f1d2afdcb7463ddb1ba927b3c38e0ce29aeb744f4f5347a3fcb33ef8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:29:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:29:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:29:48 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:29:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:29:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:29:54 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:29:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:29:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:29:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:29:59 GMT
ENV PG_MAJOR=18
# Fri, 08 May 2026 19:29:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 19:29:59 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Fri, 08 May 2026 19:39:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:39:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:39:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:39:43 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 19:39:43 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 19:39:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:39:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:39:43 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:39:43 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:39:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce6d9daac3d376cdb2024ca14afd93aa6921c6fba54f408d323a8ad2ed2efa3`  
		Last Modified: Fri, 08 May 2026 19:39:56 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8a50a8718bde9cb398ac153e045631d552abc8facc00c3e1e57feb87ca477c`  
		Last Modified: Fri, 08 May 2026 19:39:57 GMT  
		Size: 6.6 MB (6631518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a27297ae58928c9fead0a4f32a764a6f2b8d09ccb9782afeb04046a5a3c5121`  
		Last Modified: Fri, 08 May 2026 19:39:56 GMT  
		Size: 1.2 MB (1225853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f41881c011a402ea7e8fb109774175c0b807a5288d9f30a616b288f90fa5628`  
		Last Modified: Fri, 08 May 2026 19:39:57 GMT  
		Size: 8.2 MB (8204016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb3fb237a4686c59215c5f021d1b8683141145bd3d5d372e9f7a9cd4fb5f484`  
		Last Modified: Fri, 08 May 2026 19:39:57 GMT  
		Size: 1.3 MB (1308263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1d42c18bda7545ad4dcee7ec2c558c2742994db75765f229a74ddb0916f77a`  
		Last Modified: Fri, 08 May 2026 19:39:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd5b015bcd24c8fa04f70fd3677156804c00fc1cc0851c6f37fcbfee66f26b`  
		Last Modified: Fri, 08 May 2026 19:39:58 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab3da0366693fb116d860f27c0d568f05a26784b50fc38aa334249f7cff3ba0`  
		Last Modified: Fri, 08 May 2026 19:40:05 GMT  
		Size: 48.9 MB (48874619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a45a36800b40dd542d0380563689805933f402d504d4b3748d84426be575c50`  
		Last Modified: Fri, 08 May 2026 19:39:59 GMT  
		Size: 19.3 KB (19328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff34c1d7ecc6e77f57c207b997652bef38af63d40c11f818865930b94b33a73`  
		Last Modified: Fri, 08 May 2026 19:39:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2014627c0ae47c3f45c1f5a03e57286fc956fe8a78f186c7c78e12b9fb3423`  
		Last Modified: Fri, 08 May 2026 19:39:59 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4389f3d61da8faee44e44c3727fe5223b577627c97f9db64d82f271204e728c6`  
		Last Modified: Fri, 08 May 2026 19:39:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:3516a569955e7ebea055ddb877c6196eb55a4250aa73812d2414e1574eaf6da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd731f002f53cc8f485b867cfb12146327804f877f5e1c401d31b686a582c5a6`

```dockerfile
```

-	Layers:
	-	`sha256:79029c5d72638cf03f2fa3f9e3f5c056f27d9cb1884119ee4af0d59b023c84a4`  
		Last Modified: Fri, 08 May 2026 19:39:57 GMT  
		Size: 5.1 MB (5115265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed7225095c248deb473cfb133a51bbd21581bf0aae36437815c57bb1528d0cc`  
		Last Modified: Fri, 08 May 2026 19:39:56 GMT  
		Size: 52.4 KB (52390 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:be6967911af4523c43ec48aa5d2991dbf4742286947d066b910f00c7152c4ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174714135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20594413f8aab9cbbbf52bd0e0c0438c2185562008cc178935b400550070cc52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:04:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 22:04:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:04:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 22:04:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 22:05:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 22:05:08 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 22:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:05:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 22:05:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 22:05:17 GMT
ENV PG_MAJOR=18
# Fri, 08 May 2026 22:05:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 22:05:17 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Fri, 08 May 2026 22:05:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 22:05:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 22:05:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 22:05:53 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 22:05:53 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 22:05:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:05:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 22:05:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 22:05:53 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 22:05:53 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 22:05:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2eb5bcf861b5954cbd8aa274be85797f789eaf4f7830d738e4798a1651868f`  
		Last Modified: Fri, 08 May 2026 22:06:33 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c54588ebee8694ff5c5fbf602397f87e358ac7af57d80c8080575f8e637908f`  
		Last Modified: Fri, 08 May 2026 22:06:34 GMT  
		Size: 7.1 MB (7076549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d156dd1c7581b994aceebc6b6f8b3aeae5621031fb3a14bbc7a59ec25d649d`  
		Last Modified: Fri, 08 May 2026 22:06:33 GMT  
		Size: 1.2 MB (1214795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad496728dfe09a0fb255ec139c4280f3dccb2ecef098c1dccdd9169453a997c1`  
		Last Modified: Fri, 08 May 2026 22:06:34 GMT  
		Size: 8.2 MB (8204023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505abe9c519fe082023a9b025f87b79065b404072fad4d9ce899267f09135a69`  
		Last Modified: Fri, 08 May 2026 22:06:34 GMT  
		Size: 1.4 MB (1394915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e1a3bd754a65cf803d92642e60d80a6b17b1c26799da11d9be2ebdb8f9733c`  
		Last Modified: Fri, 08 May 2026 22:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a246767a8a2895b57737fc54d44684a26eb59099490e87fe9df21f18972b685`  
		Last Modified: Fri, 08 May 2026 22:06:35 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489c2b733d4fa6e472a02d70f79301fb847a97fb45198ccdb45f1c59128bd703`  
		Last Modified: Fri, 08 May 2026 22:06:38 GMT  
		Size: 123.2 MB (123195599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550648727dfb630e1653267bd4445aa1711a3130b81fdd4d461f68258f533d9c`  
		Last Modified: Fri, 08 May 2026 22:06:35 GMT  
		Size: 19.3 KB (19330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7071bab0279aa067bdd514b47c3dbcdb02c30f290e8692e558f8a6eab6a5bd54`  
		Last Modified: Fri, 08 May 2026 22:06:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260cf54b33b77affd030ecb60d7127f551b9ecc8feab2dfddaa3b277a9259100`  
		Last Modified: Fri, 08 May 2026 22:06:36 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9ee1b2f9945fb6f1237498cbfde37c1058dd8281b5a85b277e9abb595db035`  
		Last Modified: Fri, 08 May 2026 22:06:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ac6c7a30d4b2200225012b088d784bbd8ac307a5a5e5f69d1d3a07019eb8bec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bf5e9af94a64f063bf6c8e7358968aa2558a4687c0f56af54bba647fe0e034`

```dockerfile
```

-	Layers:
	-	`sha256:388f85ea1cf529158bb60fd8f85ca35f7e950f87fd4abf8323401c4b066e1742`  
		Last Modified: Fri, 08 May 2026 22:06:33 GMT  
		Size: 6.0 MB (5963437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904e57cbb8c392b71d57a4ec903fc38e1f247ad9031ecf8a5ea86a0ded8633de`  
		Last Modified: Fri, 08 May 2026 22:06:33 GMT  
		Size: 52.5 KB (52534 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:fcd965efad6a0da98b1cf67480ef2859ddf1360b33a1029faca3b65ea64b0255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92865399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a94ea2228cc51753ec622eef67a38112d255da91c5e5ef78fa8c5bb17c0d1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sun, 10 May 2026 12:21:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sun, 10 May 2026 12:22:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 May 2026 12:23:42 GMT
ENV GOSU_VERSION=1.19
# Sun, 10 May 2026 12:23:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 10 May 2026 12:24:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sun, 10 May 2026 12:24:43 GMT
ENV LANG=en_US.utf8
# Sun, 10 May 2026 12:25:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 May 2026 12:25:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 May 2026 12:25:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sun, 10 May 2026 12:25:26 GMT
ENV PG_MAJOR=18
# Sun, 10 May 2026 12:25:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Sun, 10 May 2026 12:25:26 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Sun, 10 May 2026 14:27:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sun, 10 May 2026 14:27:33 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sun, 10 May 2026 14:27:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sun, 10 May 2026 14:27:33 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Sun, 10 May 2026 14:27:33 GMT
VOLUME [/var/lib/postgresql]
# Sun, 10 May 2026 14:27:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sun, 10 May 2026 14:27:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sun, 10 May 2026 14:27:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 10 May 2026 14:27:34 GMT
STOPSIGNAL SIGINT
# Sun, 10 May 2026 14:27:34 GMT
EXPOSE map[5432/tcp:{}]
# Sun, 10 May 2026 14:27:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988dc2de045f11813ef1359f5abe174ba62914438fb92d75cab7c65a9647aed2`  
		Last Modified: Sun, 10 May 2026 14:30:04 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bf149e5f1637f24cdc4c472d6e4ca943279612e0d39c8e267125e4ebbe141c`  
		Last Modified: Sun, 10 May 2026 14:30:06 GMT  
		Size: 6.3 MB (6293378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22405ed7ddeb3ddb041a0d46f2314cf33a0b76a8a467e9c2d55a2a69b23735f5`  
		Last Modified: Sun, 10 May 2026 14:30:04 GMT  
		Size: 1.2 MB (1202046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1d93a3e38e95a376c71494a9b760c3874601da3ad347a9397e5584a2fdba3b`  
		Last Modified: Sun, 10 May 2026 14:30:08 GMT  
		Size: 8.2 MB (8203592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b5d68446e4a2a25f4140c2073abfa1f378e16bf8336f3f58606a91b20d9af9`  
		Last Modified: Sun, 10 May 2026 14:30:06 GMT  
		Size: 1.4 MB (1402374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b4166483991e8893bbf63a352298792c54bd94c781e40f75ac232b27f4550f`  
		Last Modified: Sun, 10 May 2026 14:30:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ab377a5216f4b915710db64b9dca4fa85382b9e3963c6a789da9f27fd014d`  
		Last Modified: Sun, 10 May 2026 14:30:07 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83eb6acbbfcc786e3e4db973b7099028753dd423abd1b60f4eded2a3b619abd7`  
		Last Modified: Sun, 10 May 2026 14:30:15 GMT  
		Size: 47.5 MB (47453597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7efeb1808fe8987a714a7ddb263fe593a0b8abfc0cbb9a69b6c0ab3d1e935dc`  
		Last Modified: Sun, 10 May 2026 14:30:08 GMT  
		Size: 19.3 KB (19338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70917c63185240fd75144dc1c67770e02d30c9cd650526528707fd217b5d3928`  
		Last Modified: Sun, 10 May 2026 14:30:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bae5f9c6f54c940c3edbe26aa971b01304e572b12d0094087457112795cb40`  
		Last Modified: Sun, 10 May 2026 14:30:09 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0041d37c373c660954d103b1b1cdeff41b60fb27bbbc277b1bfd16b3c9e049aa`  
		Last Modified: Sun, 10 May 2026 14:30:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:663ac9ad69e66f5cc57270a61b25ccb7edc67d9b3f5f5bd94fbab9759a7fdd10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5162734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6f689ccca1eaaaff2f19db25fdb37cf778fee5abf06551e78984b75579286a`

```dockerfile
```

-	Layers:
	-	`sha256:933f53f93ae5bbc4b4b55d815c9bfc4ad22180da0fc377b4f1a53300b83ad7a9`  
		Last Modified: Sun, 10 May 2026 14:30:06 GMT  
		Size: 5.1 MB (5110205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2e2e4c16f5239a5f8b8f71c43b3da35e3414a6f1bd284fb46523d34fc5a509e`  
		Last Modified: Sun, 10 May 2026 14:30:04 GMT  
		Size: 52.5 KB (52529 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:9a8882158bbff8bc54ea14aa2909247d9d10c87db8ddb4bf72fa7f4954e11941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176925659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d694290d0b306e0767653bb2638758ecf259b4f21a53d68b0705569dd14922`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:07:58 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 20:08:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:08:28 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 20:08:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 20:08:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 20:08:37 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 20:08:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 20:08:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 20:08:47 GMT
ENV PG_MAJOR=18
# Fri, 08 May 2026 20:08:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 08 May 2026 20:08:47 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Fri, 08 May 2026 20:26:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 20:26:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 20:26:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 20:26:08 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 08 May 2026 20:26:08 GMT
VOLUME [/var/lib/postgresql]
# Fri, 08 May 2026 20:26:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:26:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 20:26:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:26:09 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 20:26:09 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 20:26:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324a6d5bc993de76118c34ad358b49e49ec21c76110bd38bf8a9c2a311627727`  
		Last Modified: Fri, 08 May 2026 20:26:45 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96784e671d70834e50d6c40942ae4db432860007f1a1d3ca3a2fb94702158e93`  
		Last Modified: Fri, 08 May 2026 20:26:46 GMT  
		Size: 6.4 MB (6408011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52635f5e39fc81b1081c836e8c897de19e77010241bd6e847f3a050cb4458e1b`  
		Last Modified: Fri, 08 May 2026 20:26:45 GMT  
		Size: 1.2 MB (1230311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32ecff256196f59fabe2e7fd5014efaf226ac93d31f83f1d3bd9e9830813f51`  
		Last Modified: Fri, 08 May 2026 20:26:45 GMT  
		Size: 8.3 MB (8259087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9b036b14f6c076459ab17f58edd2ac18e095da45c4fc41586c00260f74a842`  
		Last Modified: Fri, 08 May 2026 20:26:46 GMT  
		Size: 1.4 MB (1398299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb09830cc71cb54a7a0536f0027bf458b4bcadae9dc56a6e095e5c0ad7601e62`  
		Last Modified: Fri, 08 May 2026 20:26:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddbe193e1088d4792995e6361ab179e35a4b3c8333fec5c7d0c4dfc386907fb`  
		Last Modified: Fri, 08 May 2026 20:26:47 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4eb81e023366f3d97a865a632ff3cf850101172db35781772709b21cd21dd88`  
		Last Modified: Fri, 08 May 2026 20:26:49 GMT  
		Size: 129.8 MB (129759439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c5dda702fe6455ec8e4fb8ff9f3933d700efb61db8d802b2d8921b0fbfd213`  
		Last Modified: Fri, 08 May 2026 20:26:47 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2b07f43e4177fc32cacc551d7e5c1559ed460183322b93a7b2677fd06d05a5`  
		Last Modified: Fri, 08 May 2026 20:26:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31403014792ec9aa5d9468a3d915bb5082b299257af85a341ced0c74cf0ee5e8`  
		Last Modified: Fri, 08 May 2026 20:26:48 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f820d9630d4366967b9289acd39f26f7f10a087d34755244b73d3b1622d756eb`  
		Last Modified: Fri, 08 May 2026 20:26:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:4662fdd4b75bc91ab4933233ad159ad26a1e64594190ca47cd4321e6072f88d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9143f898e86e0aeb6db139f12f125ba3e4ed0db2d7d3abb444977bdf917e21c`

```dockerfile
```

-	Layers:
	-	`sha256:d72d79b7ff5a84426fd9453682ea7748da9c6702c6a0537eaf84c1b4dc502d05`  
		Last Modified: Fri, 08 May 2026 20:26:45 GMT  
		Size: 6.0 MB (5973459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07cf1598f10d23fcc8e32881e2b3dba1ee1a1382fba7c4a7e3e23308c55824b`  
		Last Modified: Fri, 08 May 2026 20:26:45 GMT  
		Size: 52.5 KB (52458 bytes)  
		MIME: application/vnd.in-toto+json
