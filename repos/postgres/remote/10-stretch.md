## `postgres:10-stretch`

```console
$ docker pull postgres@sha256:503b66ae4a2a3fc2f306a8ebc25ea2a6d3f3e8e65577cd0e005beeb84b588813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `postgres:10-stretch` - linux; amd64

```console
$ docker pull postgres@sha256:0dedc2709f767bdcea7ba52b5be9fb03e1aeb24cfab2a2d318dff9da11328f50
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73206353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efbd8d35b4b11470d545105b5e039472d59eb5b252b67c52e6339b4fadf1c09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:20:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 12:20:21 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 12 Oct 2021 12:20:21 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Oct 2021 12:20:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Oct 2021 12:20:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 12 Oct 2021 12:20:39 GMT
ENV LANG=en_US.utf8
# Tue, 12 Oct 2021 12:20:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:20:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Oct 2021 12:20:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 12 Oct 2021 12:22:02 GMT
ENV PG_MAJOR=10
# Tue, 12 Oct 2021 12:22:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Tue, 12 Oct 2021 12:22:03 GMT
ENV PG_VERSION=10.18-1.pgdg90+1
# Tue, 12 Oct 2021 12:22:18 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 12 Oct 2021 12:22:19 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 12 Oct 2021 12:22:20 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 12 Oct 2021 12:22:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 12 Oct 2021 12:22:21 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 12 Oct 2021 12:22:21 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 12 Oct 2021 12:22:22 GMT
COPY file:39dd79c055f47ef80495def6993f3e85eb124d02824dc47db35d1043455e54bc in /usr/local/bin/ 
# Tue, 12 Oct 2021 12:22:23 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 12 Oct 2021 12:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 12:22:23 GMT
STOPSIGNAL SIGINT
# Tue, 12 Oct 2021 12:22:23 GMT
EXPOSE 5432
# Tue, 12 Oct 2021 12:22:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f07e2510c1a2b3be68c27a5849f9c878575e9becb97af6e3b473ecb24748fb`  
		Last Modified: Tue, 12 Oct 2021 12:26:33 GMT  
		Size: 4.5 MB (4503769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1db85978c187782e86129ca29fba157feefbd0d176746e1f280389330894c75`  
		Last Modified: Tue, 12 Oct 2021 12:26:31 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca900fc1288f10094641c9ec334e6656a3d6fcb81bdb907221e5010d1157c9a`  
		Last Modified: Tue, 12 Oct 2021 12:26:32 GMT  
		Size: 1.4 MB (1412215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12868e60047376773e127d6c2a4eb339ac0067f9737687a0a05a920c9c994aac`  
		Last Modified: Tue, 12 Oct 2021 12:26:31 GMT  
		Size: 6.2 MB (6185363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba54211abe20531ef48c9538c024d87b53dda3236dbc32b2bed1adfed6b7afd5`  
		Last Modified: Tue, 12 Oct 2021 12:26:30 GMT  
		Size: 385.0 KB (385003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d810661b69cb960f1a5a7ead1082aeecf15aeb1d8be1b71da3d9077a0f2e688`  
		Last Modified: Tue, 12 Oct 2021 12:26:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09140fe561abd752e9e3b3c58e080016cc3992ecb1f2af92f88c74496e601f3c`  
		Last Modified: Tue, 12 Oct 2021 12:26:29 GMT  
		Size: 4.8 KB (4792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea41d4e227b6f95e3b276a67260190d53ca19b6ae1ee375b909d1afa835714c`  
		Last Modified: Tue, 12 Oct 2021 12:27:29 GMT  
		Size: 38.2 MB (38172592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5647f3693daf4344db3294b61ffdb1b058f3f5075a89e76bc0a47022cf318d7f`  
		Last Modified: Tue, 12 Oct 2021 12:27:18 GMT  
		Size: 8.1 KB (8073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a18827d6b4e3735fa1c4e7fd0d6d58eacb6ecbd5b7bcdc8ac6590d0d52ff79`  
		Last Modified: Tue, 12 Oct 2021 12:27:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05725eb8ae120a242fb972a59fbc96c94a56418e0b358b3b39bd92a374dedc66`  
		Last Modified: Tue, 12 Oct 2021 12:27:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934748e9505f018f7a7a5d3c34f341e7c3baaec329bdb50cd6bbf66369a23c6d`  
		Last Modified: Tue, 12 Oct 2021 12:27:18 GMT  
		Size: 4.6 KB (4565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414bbaf40f8f4fe35367475b3d010b270de56fbdcbc992582bb3f92aabd594cc`  
		Last Modified: Tue, 12 Oct 2021 12:27:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-stretch` - linux; arm variant v5

```console
$ docker pull postgres@sha256:137fb5a2b0cac292f881782d37c2c333407db9ba6333f95a35a807191637f4ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70166970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5609e858f05dfab89be7ee7ed72dba020787dacfa22cba790a52510b96790077`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 28 Sep 2021 01:56:40 GMT
ADD file:c0e9a99ba405945353742a7ca9ee5f4807d9626de940828c7e91ea7613fbce6b in / 
# Tue, 28 Sep 2021 01:56:41 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 06:46:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 28 Sep 2021 06:46:02 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 28 Sep 2021 06:46:03 GMT
ENV GOSU_VERSION=1.12
# Tue, 28 Sep 2021 06:46:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 28 Sep 2021 06:46:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 28 Sep 2021 06:46:55 GMT
ENV LANG=en_US.utf8
# Tue, 28 Sep 2021 06:47:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 06:47:08 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Sep 2021 06:47:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 28 Sep 2021 07:36:27 GMT
ENV PG_MAJOR=10
# Tue, 28 Sep 2021 07:36:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Tue, 28 Sep 2021 07:36:28 GMT
ENV PG_VERSION=10.18-1.pgdg90+1
# Tue, 28 Sep 2021 08:02:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 28 Sep 2021 08:02:10 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 28 Sep 2021 08:02:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 28 Sep 2021 08:02:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 28 Sep 2021 08:02:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 28 Sep 2021 08:02:14 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 01 Oct 2021 02:25:21 GMT
COPY file:39dd79c055f47ef80495def6993f3e85eb124d02824dc47db35d1043455e54bc in /usr/local/bin/ 
# Fri, 01 Oct 2021 02:25:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 02:25:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 02:25:23 GMT
STOPSIGNAL SIGINT
# Fri, 01 Oct 2021 02:25:24 GMT
EXPOSE 5432
# Fri, 01 Oct 2021 02:25:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bb8e5fcfd7de8c6ce0f02070264ebe0df51ac6b9717272bead263dd7cca70d0b`  
		Last Modified: Tue, 28 Sep 2021 02:14:29 GMT  
		Size: 21.2 MB (21204242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73644ff9757bcb8fb39d6a3b1f344813adfa61e0a5d9c8cdaa2658d0676d6f6c`  
		Last Modified: Tue, 28 Sep 2021 08:57:47 GMT  
		Size: 4.2 MB (4239296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9581d5c8bb5b918c595eb3b441df16f0486030075effd635f73303bf1e93c9`  
		Last Modified: Tue, 28 Sep 2021 08:57:44 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f69dc224794f632860a105721f6276d38a558bcec13ed570c55a9729c87c4e`  
		Last Modified: Tue, 28 Sep 2021 08:57:45 GMT  
		Size: 1.4 MB (1371454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fd2b370b6cd657f3c85a759ccf13677ef00b7105f3045ba9f10de236ee68ae`  
		Last Modified: Tue, 28 Sep 2021 08:57:47 GMT  
		Size: 6.2 MB (6185662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d625d40558540b118f49566d2c79a33e33b747256c90f5c676fd1a5b8b3db9a`  
		Last Modified: Tue, 28 Sep 2021 08:57:43 GMT  
		Size: 385.1 KB (385051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be0df4e8a7ddf013a43ab3fed0e023abd64860a2f84de78b531eefd31959823`  
		Last Modified: Tue, 28 Sep 2021 08:57:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104d0a12b4a41de11f1ff8d9235398510ca444d8ab81cf1448f27a86d982b020`  
		Last Modified: Tue, 28 Sep 2021 08:57:42 GMT  
		Size: 5.3 KB (5342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5066c69f7a059f47af08450b7d3ecbe9a56d539b63da162112e54723115ebc9`  
		Last Modified: Tue, 28 Sep 2021 08:59:36 GMT  
		Size: 36.8 MB (36760872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d09ad42a9a2cfa25b8730457b51978b81b0e914d8bdf6cdc83e01a2f5ef2cbe`  
		Last Modified: Tue, 28 Sep 2021 08:59:08 GMT  
		Size: 8.1 KB (8084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1987305f0ecb912ff3141e384f412b34fa7926d159aed8ce894cd0a9ca9f8e7e`  
		Last Modified: Tue, 28 Sep 2021 08:59:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6add9c9b25a2e5d53f825777097e89e82499771cdcfd811f0e5a676527186a92`  
		Last Modified: Tue, 28 Sep 2021 08:59:08 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a2f401fd4a4ab5c84f02a9ac23cd4d3b407f663c56c93c00cc3eb9c2486fc3`  
		Last Modified: Fri, 01 Oct 2021 02:32:31 GMT  
		Size: 4.6 KB (4564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b9fa813cbdd6d945823ee6044794568b21921b825e7b08ecf8bd079884fb5d`  
		Last Modified: Fri, 01 Oct 2021 02:32:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-stretch` - linux; arm variant v7

```console
$ docker pull postgres@sha256:0aea6e389bec41659584e93170e161927706bc3c14c7caabc8b800a17710fe0c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66921572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ccd11c620c27419aa66bfddd51782a681278c41377d4e407c3573b77488806`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 30 Sep 2021 18:09:32 GMT
ADD file:a037f8ced10b72f1e0d62328b77376ea1efe206b6116e858b7a641d26fd5b1b0 in / 
# Thu, 30 Sep 2021 18:09:33 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 00:36:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 01 Oct 2021 00:36:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 01 Oct 2021 00:36:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 01 Oct 2021 00:37:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Oct 2021 00:37:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 01 Oct 2021 00:37:37 GMT
ENV LANG=en_US.utf8
# Fri, 01 Oct 2021 00:37:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 00:37:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Oct 2021 00:38:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Fri, 01 Oct 2021 01:23:13 GMT
ENV PG_MAJOR=10
# Fri, 01 Oct 2021 01:23:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Fri, 01 Oct 2021 01:23:14 GMT
ENV PG_VERSION=10.18-1.pgdg90+1
# Fri, 01 Oct 2021 01:45:49 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 01 Oct 2021 01:45:51 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 01 Oct 2021 01:45:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 01 Oct 2021 01:45:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 01 Oct 2021 01:45:55 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 01 Oct 2021 01:45:55 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 01 Oct 2021 01:45:56 GMT
COPY file:39dd79c055f47ef80495def6993f3e85eb124d02824dc47db35d1043455e54bc in /usr/local/bin/ 
# Fri, 01 Oct 2021 01:45:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 01:45:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 01:45:58 GMT
STOPSIGNAL SIGINT
# Fri, 01 Oct 2021 01:45:59 GMT
EXPOSE 5432
# Fri, 01 Oct 2021 01:45:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fce8291cdcf067da304d19441e493cb62fd5be1dcc768569fdeb1e0db374c983`  
		Last Modified: Thu, 30 Sep 2021 18:26:53 GMT  
		Size: 19.3 MB (19316455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfcc324ae93bccefa75e80a7b5c4ca93217b57c4a6a2ba9dfd9fb0f9a1fc2e5`  
		Last Modified: Fri, 01 Oct 2021 02:41:51 GMT  
		Size: 3.9 MB (3875507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf22511a5cca8e02ed87a28c139fc6af8b16d3f33a47f8f79eef26bc8c1a075`  
		Last Modified: Fri, 01 Oct 2021 02:41:49 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd8da2d918e6f6a0ff1329c3416f0d052836e3e75e714ce40570172304efe09`  
		Last Modified: Fri, 01 Oct 2021 02:41:50 GMT  
		Size: 1.4 MB (1363856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a7001638a0251c09805bfc2025f70276a7f50600a2e1a4a15550421c1625cc`  
		Last Modified: Fri, 01 Oct 2021 02:41:52 GMT  
		Size: 6.2 MB (6185629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5bb0a7abd33aadc5de96c22eeb3752a9f25e36136998aa057bccbe09582c4c`  
		Last Modified: Fri, 01 Oct 2021 02:41:48 GMT  
		Size: 379.2 KB (379167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e106a04af6a26617a9107f85fbf96cb64c758dbaeba1caf0d207d1b7e585c3`  
		Last Modified: Fri, 01 Oct 2021 02:41:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e04d88366e52aab927f971db82dcaeae2c0c3612a98abe413f1cfa15649d50`  
		Last Modified: Fri, 01 Oct 2021 02:41:47 GMT  
		Size: 4.8 KB (4792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3c1feb3da77e2feace53f94f49b0a8ed03ceae8ed135ecf55408b3755083fa`  
		Last Modified: Fri, 01 Oct 2021 02:43:57 GMT  
		Size: 35.8 MB (35781115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479eeaeac44bc3fa45baa7d512e3bebd69a8f6fe4a563860b3d6e12f846bcc26`  
		Last Modified: Fri, 01 Oct 2021 02:43:31 GMT  
		Size: 8.1 KB (8079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72de68ddb54dc259426fd1f4f36635f0b895b5b5fcdfdd0630d7c84990040b50`  
		Last Modified: Fri, 01 Oct 2021 02:43:31 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ac90fde3b3fd9152040a53662752df29ea6ba9845e3c195e0be45239139afd`  
		Last Modified: Fri, 01 Oct 2021 02:43:31 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fab05eb9aeb7cc8b88c27024423a6d88363135e3b0d16b88581b3f1d786327b`  
		Last Modified: Fri, 01 Oct 2021 02:43:31 GMT  
		Size: 4.6 KB (4569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b366345f68471aa54642866fbff73bf87e06885a49b1adc2502d89279e47a9`  
		Last Modified: Fri, 01 Oct 2021 02:43:31 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-stretch` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6feb6a44d2629c9615a7d77de4fbde938177a8ba18389609c5241d9037d62c7f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69539646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d37f5bbc5619b73a979e54ae00a7e33ccd5822bab4fc541fd7823909cf7a12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:42:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 12:42:34 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 12 Oct 2021 12:42:34 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Oct 2021 12:42:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Oct 2021 12:42:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 12 Oct 2021 12:42:52 GMT
ENV LANG=en_US.utf8
# Tue, 12 Oct 2021 12:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:42:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Oct 2021 12:43:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 12 Oct 2021 12:53:06 GMT
ENV PG_MAJOR=10
# Tue, 12 Oct 2021 12:53:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Tue, 12 Oct 2021 12:53:07 GMT
ENV PG_VERSION=10.18-1.pgdg90+1
# Tue, 12 Oct 2021 13:02:21 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 12 Oct 2021 13:02:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 12 Oct 2021 13:02:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 12 Oct 2021 13:02:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 12 Oct 2021 13:02:24 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 12 Oct 2021 13:02:24 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 12 Oct 2021 13:02:24 GMT
COPY file:39dd79c055f47ef80495def6993f3e85eb124d02824dc47db35d1043455e54bc in /usr/local/bin/ 
# Tue, 12 Oct 2021 13:02:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 12 Oct 2021 13:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 13:02:25 GMT
STOPSIGNAL SIGINT
# Tue, 12 Oct 2021 13:02:25 GMT
EXPOSE 5432
# Tue, 12 Oct 2021 13:02:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13eb4f4459a7402f1179eca53bcbad6138b63fd8bad6652d00cd47a2481f0c54`  
		Last Modified: Tue, 12 Oct 2021 13:17:08 GMT  
		Size: 4.1 MB (4078942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d945b3664e93a702bdeda7284c0d54035297d7684b7316b5503d0b09506938`  
		Last Modified: Tue, 12 Oct 2021 13:17:06 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f783df8da2e0340cee431274354c0a0a9605959c057cc2e0ae94a16b7baec3d3`  
		Last Modified: Tue, 12 Oct 2021 13:17:07 GMT  
		Size: 1.3 MB (1347010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b44ea2a5edb807c767a1ec9d11c1113bdbdd60a2d5923f53b0195d80b10283`  
		Last Modified: Tue, 12 Oct 2021 13:17:05 GMT  
		Size: 6.2 MB (6185261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607841527993823660aa30a2391978538d0380b2e9ff1d48485710796f3c1eaa`  
		Last Modified: Tue, 12 Oct 2021 13:17:04 GMT  
		Size: 377.9 KB (377856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ffedb40b98205cfd894736fe26452bcefdc40051ce7fe5d22d57dbbf0ee5f0`  
		Last Modified: Tue, 12 Oct 2021 13:17:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5751e84e652165864bdf25d6523e56d05547b49d9b3dd15dae652dfadbefe37`  
		Last Modified: Tue, 12 Oct 2021 13:17:04 GMT  
		Size: 5.3 KB (5343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee5194eb401d60c1a561f95e1af410287a75270b802fcdbb03c11004af57b65`  
		Last Modified: Tue, 12 Oct 2021 13:18:00 GMT  
		Size: 37.1 MB (37140734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5860a871c8fb901a88a7d1686f4ff6b059681dc67d4b0ae0471be7ac27aa62a3`  
		Last Modified: Tue, 12 Oct 2021 13:17:51 GMT  
		Size: 8.1 KB (8076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebc257232c8ee2047a35dda17c346be280f7ca119c97cb4490cf1a54a630d00`  
		Last Modified: Tue, 12 Oct 2021 13:17:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a2d194c05c97bb510a866819d275474b68658403f2c7cb2e05078615ef32ba`  
		Last Modified: Tue, 12 Oct 2021 13:17:52 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b982578ce0cceb30f914088f82580cc8ac81ce82df9cbdbc737e9d031fbf8670`  
		Last Modified: Tue, 12 Oct 2021 13:17:52 GMT  
		Size: 4.6 KB (4568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68a83a235831eba15b764d76730807b15c147464a51c4d18b7dfded2d57ff6a`  
		Last Modified: Tue, 12 Oct 2021 13:17:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-stretch` - linux; 386

```console
$ docker pull postgres@sha256:933072857d6699551a55a13d8f9266cf4d05349b7747e6a8a0b8c7d82c79fc6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74382987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5b3a10062b5db1b54657e73063e94686061e5a00770515ac1364de882bd87c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 28 Sep 2021 01:43:39 GMT
ADD file:701bf587ade8c18fa108e900dd6f545e5c1aeb5fdbdd4fdd3a9b54bf2e38f478 in / 
# Tue, 28 Sep 2021 01:43:39 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 18:15:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 28 Sep 2021 18:15:02 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 28 Sep 2021 18:15:03 GMT
ENV GOSU_VERSION=1.12
# Tue, 28 Sep 2021 18:15:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 28 Sep 2021 18:15:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 28 Sep 2021 18:15:39 GMT
ENV LANG=en_US.utf8
# Tue, 28 Sep 2021 18:15:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 18:15:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Sep 2021 18:15:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 28 Sep 2021 18:28:32 GMT
ENV PG_MAJOR=10
# Tue, 28 Sep 2021 18:28:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Tue, 28 Sep 2021 18:28:33 GMT
ENV PG_VERSION=10.18-1.pgdg90+1
# Tue, 28 Sep 2021 18:28:50 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 28 Sep 2021 18:28:51 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 28 Sep 2021 18:28:52 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 28 Sep 2021 18:28:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 28 Sep 2021 18:28:53 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 28 Sep 2021 18:28:53 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 01 Oct 2021 01:35:30 GMT
COPY file:39dd79c055f47ef80495def6993f3e85eb124d02824dc47db35d1043455e54bc in /usr/local/bin/ 
# Fri, 01 Oct 2021 01:35:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 01 Oct 2021 01:35:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 01:35:33 GMT
STOPSIGNAL SIGINT
# Fri, 01 Oct 2021 01:35:33 GMT
EXPOSE 5432
# Fri, 01 Oct 2021 01:35:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0952a5e9bdc54f828420f1481d98478c53df6eab6bf7b299f150d6b5481457d4`  
		Last Modified: Tue, 28 Sep 2021 01:54:01 GMT  
		Size: 23.2 MB (23156768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea0376f0b79dd78f633c5a22585c304e9b8b79c7ab9101ab330cea428f464f3`  
		Last Modified: Tue, 28 Sep 2021 18:46:34 GMT  
		Size: 4.8 MB (4812042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91313c6f6c972f47c0435473d4ff7f06bbb29b18c6f6ca0499b5cae2c7c995f4`  
		Last Modified: Tue, 28 Sep 2021 18:46:32 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07dbd6527abbac842aeab2772afd3aaab6cceff96507396e0f3e1bf9a09591c9`  
		Last Modified: Tue, 28 Sep 2021 18:46:33 GMT  
		Size: 1.4 MB (1382548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e1b7ddb08fd6ae62c4d30b1bc3ecb4742fa6e4de26a7df8a174aede3781fc4`  
		Last Modified: Tue, 28 Sep 2021 18:46:33 GMT  
		Size: 6.2 MB (6185630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee733b4b9638fecdde14ca2ee69f55ff44fba82c507040c8ca74b43475e41355`  
		Last Modified: Tue, 28 Sep 2021 18:46:31 GMT  
		Size: 393.3 KB (393339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242132f5b3b881b726600bbe465a8224e7ed4cfe3a70142a311b173f062aa22f`  
		Last Modified: Tue, 28 Sep 2021 18:46:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dafeb301e56d39267773ada6fe88b784685e9f5a448f88feb170ed0cf8acb5`  
		Last Modified: Tue, 28 Sep 2021 18:46:30 GMT  
		Size: 5.3 KB (5342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d0ce19c790cf7d87716a784ed2af39448adf3e45df9436cdf70f9336cfad07`  
		Last Modified: Tue, 28 Sep 2021 18:47:45 GMT  
		Size: 38.4 MB (38432277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eb7122cb68cea4d203db23e4e2e0a482bd027b501f761f82d326b4e2a05413`  
		Last Modified: Tue, 28 Sep 2021 18:47:34 GMT  
		Size: 8.1 KB (8075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26c223a8429ff7f148cd009d13ef9a15ceca1206c6fc4737bb18fa3203aff8a`  
		Last Modified: Tue, 28 Sep 2021 18:47:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3993a5ae4e816b6d192769e38b2e1b47d5e5f473bcad54b6892c2218cbed4970`  
		Last Modified: Tue, 28 Sep 2021 18:47:34 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9113d1ed4dc50ff8bd8e81b4fba63f8eba58328fd580e37b6c31e0b78288a5`  
		Last Modified: Fri, 01 Oct 2021 01:42:58 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28274db1c81606cdff2a7507cee30c77bd5aa06d6077a612c6350fc3555b5104`  
		Last Modified: Fri, 01 Oct 2021 01:42:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
