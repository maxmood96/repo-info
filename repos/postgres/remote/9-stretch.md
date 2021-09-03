## `postgres:9-stretch`

```console
$ docker pull postgres@sha256:a1d23fa4bbb2941bf143fe20b9696f8be2e6d8a13a5063218b1e44d86dc7e2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `postgres:9-stretch` - linux; amd64

```console
$ docker pull postgres@sha256:f4db7d5cb8979fb2698c59f22cbcc9086712a637e8611715cd8010bd8f76a752
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73583337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef432eee5c23eef4d8cba0357f52447068d4064c8dff5cb415f6ac6f15b84a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:46 GMT
ADD file:b8ae56829d548d5bff373622e23d0352bb9d313f09d8fea76dc1892b16c768c8 in / 
# Fri, 03 Sep 2021 01:23:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 12:58:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 12:58:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 03 Sep 2021 12:58:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 03 Sep 2021 12:58:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 03 Sep 2021 12:58:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 03 Sep 2021 12:58:38 GMT
ENV LANG=en_US.utf8
# Fri, 03 Sep 2021 12:58:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 12:58:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 03 Sep 2021 12:58:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Fri, 03 Sep 2021 13:01:24 GMT
ENV PG_MAJOR=9.6
# Fri, 03 Sep 2021 13:01:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/9.6/bin
# Fri, 03 Sep 2021 13:01:24 GMT
ENV PG_VERSION=9.6.23-1.pgdg90+1
# Fri, 03 Sep 2021 13:01:41 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 		"postgresql-contrib-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 03 Sep 2021 13:01:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 03 Sep 2021 13:01:43 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 03 Sep 2021 13:01:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 03 Sep 2021 13:01:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 03 Sep 2021 13:01:45 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 03 Sep 2021 13:01:45 GMT
COPY file:b14ac9ddf7e0a36b021a2f5ce366f60c1befa4d9e96285f4c5a38ce8c3886b3e in /usr/local/bin/ 
# Fri, 03 Sep 2021 13:01:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 03 Sep 2021 13:01:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Sep 2021 13:01:47 GMT
STOPSIGNAL SIGINT
# Fri, 03 Sep 2021 13:01:48 GMT
EXPOSE 5432
# Fri, 03 Sep 2021 13:01:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:442547fc262c2ebd1e2d44ea04cb011b78ec62cc2314c8c71c68ba31ae002cdb`  
		Last Modified: Fri, 03 Sep 2021 01:32:07 GMT  
		Size: 22.5 MB (22527429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f9b0d37d6380825a6301d2ec34983de9d7de26aa097eb5d59abd0690f128c1`  
		Last Modified: Fri, 03 Sep 2021 13:05:36 GMT  
		Size: 4.5 MB (4503304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673a0386621a69d9121dd482d65e3816916fb7585b4b201e550200203235310c`  
		Last Modified: Fri, 03 Sep 2021 13:05:33 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d442b05d6a6418e8a08c0febedebc63702c5511dc1636aa50ea68e9541fb51`  
		Last Modified: Fri, 03 Sep 2021 13:05:34 GMT  
		Size: 1.4 MB (1412280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b9f3eeffa379d0b3d8c61ce5c127a8be1e256808aec04b579d013c4ac12f46`  
		Last Modified: Fri, 03 Sep 2021 13:05:33 GMT  
		Size: 6.2 MB (6185735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b8a068ac5ae050646255027cadc298ee8ecb1c4678caa7fa0b25d2cd720983`  
		Last Modified: Fri, 03 Sep 2021 13:05:31 GMT  
		Size: 385.1 KB (385088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2916937b1163af8ad903ab280faa82dc11e368b8e6bad77b52687f2f59bdd565`  
		Last Modified: Fri, 03 Sep 2021 13:05:31 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddee610c77826d4cdb1f575beb5b150423dec8e3db17ce255b94f76133462504`  
		Last Modified: Fri, 03 Sep 2021 13:05:31 GMT  
		Size: 5.3 KB (5344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9cbe2e8b78b946dda7fad0de8e2eff3d4cd47ff11ee6419ed6046c58fe42e7`  
		Last Modified: Fri, 03 Sep 2021 13:07:39 GMT  
		Size: 38.5 MB (38549486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf59b47e853ad1e6776275b93bbf525bccd7c25e0762e704525db7dc6b28c49`  
		Last Modified: Fri, 03 Sep 2021 13:07:29 GMT  
		Size: 7.9 KB (7864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b66656577df9cb9af9665a605a63adb5953d1f2599fd0b622549302b5e931a`  
		Last Modified: Fri, 03 Sep 2021 13:07:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a786874f0014328c77729e8a71a9191000008e3809e5bd42a7eac5dd74b4c4f8`  
		Last Modified: Fri, 03 Sep 2021 13:07:29 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cc180e8f2db6c4c7310da79d4cf23c964280fc2b194c31f37eee849a867233`  
		Last Modified: Fri, 03 Sep 2021 13:07:29 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2738829e1ed0f05fe97637bd9ef09f99eedd451d22dd59f45d9bc70542844eaa`  
		Last Modified: Fri, 03 Sep 2021 13:07:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-stretch` - linux; arm variant v5

```console
$ docker pull postgres@sha256:90c7a111c12ed84475f0ff9fb92545fc23e19b19b02bb60b909e02e3d680a7fa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70517926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60168cf993b1b7422438b22f4908242cf8bd9ffdbdc5c55bcc123292b7f7a221`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 03 Sep 2021 00:55:51 GMT
ADD file:2ecb9aa1d4a322f0ac93d32a03b6a01ed5fb9f727136a9e6adda019256baa4de in / 
# Fri, 03 Sep 2021 00:55:51 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 10:07:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 10:07:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 03 Sep 2021 10:07:47 GMT
ENV GOSU_VERSION=1.12
# Fri, 03 Sep 2021 10:08:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 03 Sep 2021 10:08:41 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 03 Sep 2021 10:08:41 GMT
ENV LANG=en_US.utf8
# Fri, 03 Sep 2021 10:08:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 10:08:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 03 Sep 2021 10:09:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Fri, 03 Sep 2021 11:49:05 GMT
ENV PG_MAJOR=9.6
# Fri, 03 Sep 2021 11:49:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/9.6/bin
# Fri, 03 Sep 2021 11:49:06 GMT
ENV PG_VERSION=9.6.23-1.pgdg90+1
# Fri, 03 Sep 2021 12:14:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 		"postgresql-contrib-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 03 Sep 2021 12:14:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 03 Sep 2021 12:14:29 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 03 Sep 2021 12:14:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 03 Sep 2021 12:14:31 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 03 Sep 2021 12:14:32 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 03 Sep 2021 12:14:32 GMT
COPY file:b14ac9ddf7e0a36b021a2f5ce366f60c1befa4d9e96285f4c5a38ce8c3886b3e in /usr/local/bin/ 
# Fri, 03 Sep 2021 12:14:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 03 Sep 2021 12:14:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Sep 2021 12:14:35 GMT
STOPSIGNAL SIGINT
# Fri, 03 Sep 2021 12:14:35 GMT
EXPOSE 5432
# Fri, 03 Sep 2021 12:14:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:828d6e40787f20000d8d8818e14bc3a6ac56950cabc44e46b48418c385e2470d`  
		Last Modified: Fri, 03 Sep 2021 01:14:04 GMT  
		Size: 21.2 MB (21204340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297c76a25ec97cb866cd636d911e114125af92a6598bef277aa774199ba3c716`  
		Last Modified: Fri, 03 Sep 2021 12:21:38 GMT  
		Size: 4.2 MB (4238876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896afeb0a788d76e701c3392d42084513eadb0e404ed81b5e5e6a85c53e75ab9`  
		Last Modified: Fri, 03 Sep 2021 12:21:35 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219c0acd0bb2be6b2554baef7f918af997fd16366f92e3c081d4f4110f9daa04`  
		Last Modified: Fri, 03 Sep 2021 12:21:36 GMT  
		Size: 1.4 MB (1371482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3303537561793a987f051d2583335eb9e88a6a7b102f3ed2f338c856f9c4314f`  
		Last Modified: Fri, 03 Sep 2021 12:21:37 GMT  
		Size: 6.2 MB (6185662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73135e6e9a490e86ecd920188e5b61d80659eb46772d8f5f5a465912e5441f6`  
		Last Modified: Fri, 03 Sep 2021 12:21:33 GMT  
		Size: 385.1 KB (385061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5dfb4c51b417e9e8328e02b710cf460f0e2589097ebdb38117596e5747c330`  
		Last Modified: Fri, 03 Sep 2021 12:21:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f2010ec756fa98b4dd707fc1d132449bba99a5651c0bb3a2d86b1c5f71d888`  
		Last Modified: Fri, 03 Sep 2021 12:21:33 GMT  
		Size: 5.3 KB (5341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8270a24010db3b73af8654019275c4e82fff10dfe1701821873330c693270d54`  
		Last Modified: Fri, 03 Sep 2021 12:25:06 GMT  
		Size: 37.1 MB (37112493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fa8f0797194dc4aff246f908d1212c9452013c1365414f6a62779e8abdfb23`  
		Last Modified: Fri, 03 Sep 2021 12:24:38 GMT  
		Size: 7.9 KB (7867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190d6546a0606e482c5574bc99a9368e54bdeb2867bf52c30a74cb520e440451`  
		Last Modified: Fri, 03 Sep 2021 12:24:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7783f4866dd31fe0a73ade7f23630bde8a8eeb0c02057f6a5d9afa8a6bf477f`  
		Last Modified: Fri, 03 Sep 2021 12:24:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08549bab30ba416554ade7cacb1f42e9143e73b915b567b216b018ad34f7bc17`  
		Last Modified: Fri, 03 Sep 2021 12:24:38 GMT  
		Size: 4.4 KB (4409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e11d9f86686539b980a1fc5c07750460bd88db167e095e31f675e80bc842a20`  
		Last Modified: Fri, 03 Sep 2021 12:24:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-stretch` - linux; arm variant v7

```console
$ docker pull postgres@sha256:61e7eabf6ea6b38d946b175db0a3afc1e5d6c1616802ce1414eabd9b6faf6fff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67199103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f014d80a2447d633101764ddf926b3a463e9a62645374074304d2f806c3f2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 17 Aug 2021 02:19:36 GMT
ADD file:1719cfa11cf0f895b82719a2c082abb9f2d9b6dd6efc9e610e9732b97b31f56d in / 
# Tue, 17 Aug 2021 02:19:36 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 18:29:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 18:29:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 17 Aug 2021 18:29:44 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 18:30:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 18:30:30 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 17 Aug 2021 18:30:30 GMT
ENV LANG=en_US.utf8
# Tue, 17 Aug 2021 18:30:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 18:30:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 18:30:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 17 Aug 2021 20:01:38 GMT
ENV PG_MAJOR=9.6
# Tue, 17 Aug 2021 20:01:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/9.6/bin
# Tue, 17 Aug 2021 20:01:39 GMT
ENV PG_VERSION=9.6.23-1.pgdg90+1
# Tue, 17 Aug 2021 20:23:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 		"postgresql-contrib-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 17 Aug 2021 20:23:58 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 17 Aug 2021 20:24:00 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 17 Aug 2021 20:24:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 17 Aug 2021 20:24:02 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 17 Aug 2021 20:24:02 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 17 Aug 2021 20:24:03 GMT
COPY file:b14ac9ddf7e0a36b021a2f5ce366f60c1befa4d9e96285f4c5a38ce8c3886b3e in /usr/local/bin/ 
# Tue, 17 Aug 2021 20:24:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 17 Aug 2021 20:24:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 20:24:05 GMT
STOPSIGNAL SIGINT
# Tue, 17 Aug 2021 20:24:06 GMT
EXPOSE 5432
# Tue, 17 Aug 2021 20:24:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d1f994b3d26e717ce6c4ff9f7b5af7dbc4a4c831977d207f3ab47f213a8287e4`  
		Last Modified: Tue, 17 Aug 2021 02:36:57 GMT  
		Size: 19.3 MB (19316532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908b5e4512318bb4285015da09ef4b4b01e7ca5ece0e76dcfe737c4c959ad27b`  
		Last Modified: Tue, 17 Aug 2021 20:33:19 GMT  
		Size: 3.9 MB (3875039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1eac3f9ca54f30d423083c68c31c3097fae49e782979c57e83b2521df29643`  
		Last Modified: Tue, 17 Aug 2021 20:33:16 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3cb04f36501ea33e5f95ff810116a979296bb678688b4de3af302890f25cc8`  
		Last Modified: Tue, 17 Aug 2021 20:33:17 GMT  
		Size: 1.4 MB (1363885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc8d52e8ae43cf1fffc7b0e6c96de71348b9f76268e4df46f7cdcdf63c76f46`  
		Last Modified: Tue, 17 Aug 2021 20:33:19 GMT  
		Size: 6.2 MB (6185419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bb17b34a136eee32d28590bd44e8d7fc62a63cb90c1fff6b2d1874eae5fb3c`  
		Last Modified: Tue, 17 Aug 2021 20:33:15 GMT  
		Size: 379.2 KB (379194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3200ae1c10d942ed39afce09b289da0f933a19e4c9d6094bdf3d771e12bbe822`  
		Last Modified: Tue, 17 Aug 2021 20:33:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddb2a989cb91aa4a65dfca3fe3a7e800650bb35412ae3940ee90d7c1aa096ff`  
		Last Modified: Tue, 17 Aug 2021 20:33:14 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d191ce88c91c1e7f16ecacdecd94b59a9650ab3ed237cc88595a7d4560def`  
		Last Modified: Tue, 17 Aug 2021 20:36:54 GMT  
		Size: 36.1 MB (36059555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3658d12b38ff73d16e0318498bd7c9ada99d90d75258a2166982d660b738c8e`  
		Last Modified: Tue, 17 Aug 2021 20:36:29 GMT  
		Size: 7.9 KB (7875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ce9385da96ddf1685042f7c5f5960d293c45f6731c0824494761e53e047e6`  
		Last Modified: Tue, 17 Aug 2021 20:36:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fccbe67106c8a7ca4a0a6e3cb0a848ddea351b74f56b51907fe088506f3965`  
		Last Modified: Tue, 17 Aug 2021 20:36:29 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4def4aa80cebb3ae3c755bf487863a5a5c56684b9c733620646e56b01ae7c32a`  
		Last Modified: Tue, 17 Aug 2021 20:36:29 GMT  
		Size: 4.4 KB (4413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2270e34baf0efd5ad4ddd2fd31ed7be767a501b22d2d2429a507335da974119`  
		Last Modified: Tue, 17 Aug 2021 20:36:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-stretch` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:86b4a633b69c3c039ef18d3ca657f01328c94cb0e6f90851a01a7041ec8946c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69798384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234201ab88ac68d8fa1b617cc1f97e80e80fb9cf80d971a96b835311b6410b07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:48 GMT
ADD file:f45934b05bd47c443a0ac02ba0771c25002763d29eb9f8ae723980605ff6f091 in / 
# Fri, 03 Sep 2021 00:42:48 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 07:28:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 07:28:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 03 Sep 2021 07:28:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 03 Sep 2021 07:28:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 03 Sep 2021 07:28:53 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 03 Sep 2021 07:28:53 GMT
ENV LANG=en_US.utf8
# Fri, 03 Sep 2021 07:28:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 07:28:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 03 Sep 2021 07:29:04 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Fri, 03 Sep 2021 07:49:32 GMT
ENV PG_MAJOR=9.6
# Fri, 03 Sep 2021 07:49:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/9.6/bin
# Fri, 03 Sep 2021 07:49:33 GMT
ENV PG_VERSION=9.6.23-1.pgdg90+1
# Fri, 03 Sep 2021 07:58:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 		"postgresql-contrib-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 03 Sep 2021 07:58:45 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 03 Sep 2021 07:58:45 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 03 Sep 2021 07:58:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 03 Sep 2021 07:58:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 03 Sep 2021 07:58:46 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 03 Sep 2021 07:58:46 GMT
COPY file:b14ac9ddf7e0a36b021a2f5ce366f60c1befa4d9e96285f4c5a38ce8c3886b3e in /usr/local/bin/ 
# Fri, 03 Sep 2021 07:58:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 03 Sep 2021 07:58:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Sep 2021 07:58:48 GMT
STOPSIGNAL SIGINT
# Fri, 03 Sep 2021 07:58:48 GMT
EXPOSE 5432
# Fri, 03 Sep 2021 07:58:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bafcab9e99462b57e2818f0017c17049cc46e69473e9d80342344f7116f32e83`  
		Last Modified: Fri, 03 Sep 2021 00:53:26 GMT  
		Size: 20.4 MB (20389506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137a42b6f7f02a8e87c5fa87b42d10288c2f071cf585f4e8768b466dc59556c`  
		Last Modified: Fri, 03 Sep 2021 08:03:18 GMT  
		Size: 4.1 MB (4078558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3351fd3721ce89523f176e641f1a86cb5ea145104c1226362bf37e1d041021b8`  
		Last Modified: Fri, 03 Sep 2021 08:03:17 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad0ff24a0d1d8faddf2d4ce56db139f15ee1d0d734f1874587e47ce9462777c`  
		Last Modified: Fri, 03 Sep 2021 08:03:17 GMT  
		Size: 1.3 MB (1347027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68712ca1484900ba2c9cadd3a620a23d43983bdfa212867e7cb71e4bedb64bef`  
		Last Modified: Fri, 03 Sep 2021 08:03:16 GMT  
		Size: 6.2 MB (6185329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0954b8341d078238d121ef2c4b17698b8fade20b86f92d7bf754fee39800dfdb`  
		Last Modified: Fri, 03 Sep 2021 08:03:15 GMT  
		Size: 377.9 KB (377892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef00c6ae58c2cf71a7ba9a8ea2a663915318296c82f60de6363a7f64df7f4277`  
		Last Modified: Fri, 03 Sep 2021 08:03:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319e0c6bb159c618f49a276f08d1fc230fb4abb5196a3ab3f41077c23ce7ea6f`  
		Last Modified: Fri, 03 Sep 2021 08:03:14 GMT  
		Size: 5.3 KB (5340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb1cab615ca25c11328dd7df4336a8515d52f910b524c5a05dd86e82f0c0edc`  
		Last Modified: Fri, 03 Sep 2021 08:05:10 GMT  
		Size: 37.4 MB (37400049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8450d39aeec565d01a8431e0e93955747d98455b1d66f1e89efec4e3b08612ac`  
		Last Modified: Fri, 03 Sep 2021 08:05:01 GMT  
		Size: 7.9 KB (7864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7614c3b4c4075b99a7fcac7687e484e7237fa4386e07d24f28ae08813260de55`  
		Last Modified: Fri, 03 Sep 2021 08:05:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d10c7f7d849c24cb5e3ae3a1c94d41d51b913871d19b412be09cc739c2da645`  
		Last Modified: Fri, 03 Sep 2021 08:05:01 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ea41f1852e3a59438695951c8e91cc2997eb1a0003f32666b84d314bab47e`  
		Last Modified: Fri, 03 Sep 2021 08:05:01 GMT  
		Size: 4.4 KB (4409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448f9e406236dcc3af5311436bde47824d6c21cff4c69a58feb6e9ab5efb1522`  
		Last Modified: Fri, 03 Sep 2021 08:05:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-stretch` - linux; 386

```console
$ docker pull postgres@sha256:31d58f2965720924991b7130aa5bf45d739802b0abfcbf1e0de212843b106182
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74724255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9a56359820f2bf2bb25be53199eec7d8640cf647b5f516592fdf3e47d3db66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:46 GMT
ADD file:6c8a44184bf1d38b16f52d58ecb80d627ab86fce72a78b094170535fe1f76ad0 in / 
# Fri, 03 Sep 2021 00:42:46 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 16:04:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 16:04:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 03 Sep 2021 16:04:13 GMT
ENV GOSU_VERSION=1.12
# Fri, 03 Sep 2021 16:04:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 03 Sep 2021 16:04:49 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 03 Sep 2021 16:04:50 GMT
ENV LANG=en_US.utf8
# Fri, 03 Sep 2021 16:04:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 16:05:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 03 Sep 2021 16:05:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Fri, 03 Sep 2021 16:07:46 GMT
ENV PG_MAJOR=9.6
# Fri, 03 Sep 2021 16:07:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/9.6/bin
# Fri, 03 Sep 2021 16:07:47 GMT
ENV PG_VERSION=9.6.23-1.pgdg90+1
# Fri, 03 Sep 2021 16:08:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 		"postgresql-contrib-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 03 Sep 2021 16:08:19 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 03 Sep 2021 16:08:21 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 03 Sep 2021 16:08:22 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 03 Sep 2021 16:08:24 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 03 Sep 2021 16:08:24 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 03 Sep 2021 16:08:24 GMT
COPY file:b14ac9ddf7e0a36b021a2f5ce366f60c1befa4d9e96285f4c5a38ce8c3886b3e in /usr/local/bin/ 
# Fri, 03 Sep 2021 16:08:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 03 Sep 2021 16:08:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Sep 2021 16:08:26 GMT
STOPSIGNAL SIGINT
# Fri, 03 Sep 2021 16:08:27 GMT
EXPOSE 5432
# Fri, 03 Sep 2021 16:08:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0b43614231856f083f6dc06bd012a7ac7ff26410a945ea25d4c887e8218a878c`  
		Last Modified: Fri, 03 Sep 2021 00:53:23 GMT  
		Size: 23.2 MB (23156443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abea021c5bc89b9f765dd715203d1385b53a29ccfa57f89bcd984005cf69c726`  
		Last Modified: Fri, 03 Sep 2021 16:14:45 GMT  
		Size: 4.8 MB (4811150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a98f6a5975361064b7aeb87d1b9d605c8de7dbe54b5cd6fc8a79a05b3dfd0f8`  
		Last Modified: Fri, 03 Sep 2021 16:14:42 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838d0a09d7215471a71ef652e21e61fdb937b1ed8bec98d0ab985e8231bad43a`  
		Last Modified: Fri, 03 Sep 2021 16:14:43 GMT  
		Size: 1.4 MB (1382508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ee70d258a0c0b0a9b70578eea4506ef1e0d9c2957b6d53c71d3da95adfde2f`  
		Last Modified: Fri, 03 Sep 2021 16:14:43 GMT  
		Size: 6.2 MB (6185570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fd2706bb58d86695a5979067348a92b7efa5d06c3fa2d270f514e79881239d`  
		Last Modified: Fri, 03 Sep 2021 16:14:40 GMT  
		Size: 393.3 KB (393335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c646f28e6bd0662e1b06bbc1a601e2f95e19182e9645749540f1a8e7092a49`  
		Last Modified: Fri, 03 Sep 2021 16:14:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff53030bfd0020aeb52e4e9f505cb48941c20105c32895230eb4985ebb7c8e8`  
		Last Modified: Fri, 03 Sep 2021 16:14:39 GMT  
		Size: 5.3 KB (5343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1f27adef8c04213c66b6c012170f907b7cd77b7fbd0e0d29aa2aa9edb8d689`  
		Last Modified: Fri, 03 Sep 2021 16:17:36 GMT  
		Size: 38.8 MB (38775236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44253c0528c8e6067ccf5ffe7b3533cfce614dde988a41593a1d0a4c4d3c35a`  
		Last Modified: Fri, 03 Sep 2021 16:17:20 GMT  
		Size: 7.9 KB (7865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e755f648f1172bec7d413708e45e62e0761000a23510d8decf8a8dadc84be`  
		Last Modified: Fri, 03 Sep 2021 16:17:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb940d1b1b68c776780f462325bb1bb985cf4f6918bd3a6251cfb440a306e550`  
		Last Modified: Fri, 03 Sep 2021 16:17:20 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b5e81c55fc68346a7831f2948d8f67f4516c5fd92730872ea2f5d64ad7c6e6`  
		Last Modified: Fri, 03 Sep 2021 16:17:20 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4c0a7fb4ab81bfb293977721f97cf49bbf15fe8fc89483cce4686420691927`  
		Last Modified: Fri, 03 Sep 2021 16:17:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
