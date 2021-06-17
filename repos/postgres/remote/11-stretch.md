## `postgres:11-stretch`

```console
$ docker pull postgres@sha256:5e4435de8f0e0cbfcd52670d64441dab6f7bbb629d1ac9350c3862b12783ef43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `postgres:11-stretch` - linux; amd64

```console
$ docker pull postgres@sha256:deec06c7c7ab8de803d8726033f4ece60a048ae1d9f3819f14d0af65c19a8fdd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106548003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813d7fa865f62ab47c75ce7589c1ada9006dc8c1e891b5195eb2c757dd919876`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 01:23:21 GMT
ADD file:a88164546613d1850e5c5494cccad7124d713187bfabf592a783eb9328de51eb in / 
# Wed, 12 May 2021 01:23:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:36:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 14:36:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 12 May 2021 14:36:11 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 14:36:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 14:36:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 12 May 2021 14:36:29 GMT
ENV LANG=en_US.utf8
# Wed, 12 May 2021 14:36:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:36:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 14:36:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 12 May 2021 14:36:38 GMT
ENV PG_MAJOR=11
# Wed, 16 Jun 2021 22:29:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 16 Jun 2021 22:29:48 GMT
ENV PG_VERSION=11.12-1.pgdg90+1
# Wed, 16 Jun 2021 22:30:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 16 Jun 2021 22:30:10 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 16 Jun 2021 22:30:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 16 Jun 2021 22:30:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 16 Jun 2021 22:30:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 16 Jun 2021 22:30:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 16 Jun 2021 22:30:13 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 16 Jun 2021 22:30:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Jun 2021 22:30:13 GMT
STOPSIGNAL SIGINT
# Wed, 16 Jun 2021 22:30:13 GMT
EXPOSE 5432
# Wed, 16 Jun 2021 22:30:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fa1690ae92289fb310aa27b793a164bf8bbedc7ddd00ca079a31bb8bb315b616`  
		Last Modified: Wed, 12 May 2021 01:30:20 GMT  
		Size: 22.5 MB (22528266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73f6e07b15899df667ce346502d8d5b17d1193f7175e6b766618fb43730f5e2`  
		Last Modified: Wed, 12 May 2021 14:41:14 GMT  
		Size: 4.5 MB (4503314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973a0c44ddbacd1f6c6c6ce492c02046961b2c4b8b627864e1661bd95c120554`  
		Last Modified: Wed, 12 May 2021 14:41:12 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e5342b01d432d09b2c4d0ee7587a0f02b98f89d4c6dccaa80f66015c9ac9ba`  
		Last Modified: Wed, 12 May 2021 14:41:12 GMT  
		Size: 1.4 MB (1412291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578aad0862c9fa757ed2742c6bd2470cdb405ecebebc4c1adbaed7a4ed4fe82f`  
		Last Modified: Wed, 12 May 2021 14:41:12 GMT  
		Size: 6.2 MB (6185597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b157088f7a4589488c98feb1e85f181a38b2df8dd98d12fd1437863e249d01`  
		Last Modified: Wed, 12 May 2021 14:41:10 GMT  
		Size: 385.0 KB (385046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9046f06fc5e0837aca2236f4d14b55c037c80b63c7f20ea6f43b82fbaf9247`  
		Last Modified: Wed, 12 May 2021 14:41:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae19407bdc48f0978fb8b45798887b785418cad03f4a7d7341f899855df662c1`  
		Last Modified: Wed, 12 May 2021 14:41:09 GMT  
		Size: 5.3 KB (5350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f8d73f331e3bc47275ca16bd5c98af18c153f5500e3a1ce80746c24373db07`  
		Last Modified: Wed, 16 Jun 2021 22:39:31 GMT  
		Size: 71.5 MB (71513122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355aec4c48b6f9111dd63620dd810cf422058a58a142a63c55b14242ce3bfffb`  
		Last Modified: Wed, 16 Jun 2021 22:39:21 GMT  
		Size: 8.3 KB (8319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac8c419244c40dba80f4905cd6ede9ff5b9e9a97fa5190705df1ff0fa3f2779`  
		Last Modified: Wed, 16 Jun 2021 22:39:21 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a807af8a30a5f3e15ebca799e6b5e1fc10419a84a20444f39dd9dc7f758011d4`  
		Last Modified: Wed, 16 Jun 2021 22:39:21 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff39cae5e6954658177b7d81f82fe559f5c49c3361c3e3ad6e447e3f5926bca`  
		Last Modified: Wed, 16 Jun 2021 22:39:21 GMT  
		Size: 4.4 KB (4412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-stretch` - linux; arm variant v5

```console
$ docker pull postgres@sha256:a0ee059745b8ba27158f98d6c48f1dcf25e87205f4694b32cb7b40963ef0ea54
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70634731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f4a0f682d0d3bc054a962339dc4f26e0467f401a01ffc1ef650394cb93b20a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 01:01:48 GMT
ADD file:16d8a32cf194273257ffe5ab8604ecd57ac49448b7718598ba444209b96eefe0 in / 
# Wed, 12 May 2021 01:01:50 GMT
CMD ["bash"]
# Wed, 16 Jun 2021 01:58:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 16 Jun 2021 01:58:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 16 Jun 2021 01:58:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Jun 2021 01:59:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Jun 2021 01:59:30 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 16 Jun 2021 01:59:30 GMT
ENV LANG=en_US.utf8
# Wed, 16 Jun 2021 01:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Jun 2021 01:59:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 16 Jun 2021 01:59:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 16 Jun 2021 01:59:44 GMT
ENV PG_MAJOR=11
# Thu, 17 Jun 2021 00:13:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 17 Jun 2021 00:13:53 GMT
ENV PG_VERSION=11.12-1.pgdg90+1
# Thu, 17 Jun 2021 00:24:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 17 Jun 2021 00:24:49 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 17 Jun 2021 00:24:49 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 17 Jun 2021 00:24:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 17 Jun 2021 00:24:50 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 17 Jun 2021 00:24:50 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 17 Jun 2021 00:24:51 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Thu, 17 Jun 2021 00:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Jun 2021 00:24:51 GMT
STOPSIGNAL SIGINT
# Thu, 17 Jun 2021 00:24:51 GMT
EXPOSE 5432
# Thu, 17 Jun 2021 00:24:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:28eac82a41947b150beb3e600cd0173333b788e14f32c944093de53b4beb9372`  
		Last Modified: Wed, 12 May 2021 01:13:18 GMT  
		Size: 21.2 MB (21203944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e12a7d209eaf5296e0aa1dbe83b7856b8f689ad7d7e8fbf9b0def4d6ec6dbe`  
		Last Modified: Wed, 16 Jun 2021 02:49:22 GMT  
		Size: 4.2 MB (4238894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a492df438a7b054e9bdab92ec33798d130acb179bd87f1b60eccc3540e3c7a`  
		Last Modified: Wed, 16 Jun 2021 02:49:20 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b418ab662048b16e3062dee2f232536b71388d800210d8cb63473840ced39dc`  
		Last Modified: Wed, 16 Jun 2021 02:49:21 GMT  
		Size: 1.4 MB (1371467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17833f771774585d00dbdfb312257d9fd5a99ee3164da4702982b6df0ddfe773`  
		Last Modified: Wed, 16 Jun 2021 02:49:21 GMT  
		Size: 6.2 MB (6185509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3833ce3d11563b5a74869cba3efac282ec901c9a297c26f4d08ace1fc05c6300`  
		Last Modified: Wed, 16 Jun 2021 02:49:17 GMT  
		Size: 385.1 KB (385080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e911c678310ae430b4b8da6b0cfaa00eb1559ef0994225b702ea45643d1b782`  
		Last Modified: Wed, 16 Jun 2021 02:49:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84069268cca593cf9bf7eb17bd8fede3ed7da02d02ebe2f86b8cd8a4e724f2e`  
		Last Modified: Wed, 16 Jun 2021 02:49:17 GMT  
		Size: 5.3 KB (5348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d570c55c54c75fe49391f22e39195e85de0010a59923fa793141977b386b088d`  
		Last Modified: Thu, 17 Jun 2021 01:12:13 GMT  
		Size: 37.2 MB (37229477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df71859402a3adefa5cb93e9820a26519b594080213c1f6c2a2aa2146dc65139`  
		Last Modified: Thu, 17 Jun 2021 01:12:04 GMT  
		Size: 8.3 KB (8316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feee9abffbc3966ee4661459b72fae9c465991167231c0b05e5e34299573bb00`  
		Last Modified: Thu, 17 Jun 2021 01:12:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae971c5a4837ea55682559fda4a2efc1be049cd7629bad8613693dd3f884bf93`  
		Last Modified: Thu, 17 Jun 2021 01:12:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e43a7700af72f53762009c0f0dc343ba9c3e36ed47ee2df565be641c871f8b`  
		Last Modified: Thu, 17 Jun 2021 01:12:04 GMT  
		Size: 4.4 KB (4415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-stretch` - linux; arm variant v7

```console
$ docker pull postgres@sha256:90499708350987ad3f50c705840b78ea8649ee1ef1747813bcce9c6606477f68
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67297724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09101c7ef85c9afb1a9b55d635e4c9dc54489874a3475d848ecca95cc5cb9277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 01:13:00 GMT
ADD file:3a0c44e2f78c31814d76ce91706cea345d424f8b49631a1e01dbfe768d244d48 in / 
# Wed, 12 May 2021 01:13:05 GMT
CMD ["bash"]
# Wed, 16 Jun 2021 17:46:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 16 Jun 2021 17:46:09 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 16 Jun 2021 17:46:09 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Jun 2021 17:46:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Jun 2021 17:46:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 16 Jun 2021 17:46:28 GMT
ENV LANG=en_US.utf8
# Wed, 16 Jun 2021 17:46:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Jun 2021 17:46:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 16 Jun 2021 17:46:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 16 Jun 2021 17:46:37 GMT
ENV PG_MAJOR=11
# Thu, 17 Jun 2021 00:43:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 17 Jun 2021 00:43:46 GMT
ENV PG_VERSION=11.12-1.pgdg90+1
# Thu, 17 Jun 2021 00:53:41 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 17 Jun 2021 00:53:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 17 Jun 2021 00:53:43 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 17 Jun 2021 00:53:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 17 Jun 2021 00:53:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 17 Jun 2021 00:53:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 17 Jun 2021 00:53:44 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Thu, 17 Jun 2021 00:53:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Jun 2021 00:53:45 GMT
STOPSIGNAL SIGINT
# Thu, 17 Jun 2021 00:53:45 GMT
EXPOSE 5432
# Thu, 17 Jun 2021 00:53:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ce2b35672977ffba9f48ce0726706cd15d926482c1008f69213433c61ba44966`  
		Last Modified: Wed, 12 May 2021 01:21:44 GMT  
		Size: 19.3 MB (19315154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7564e314889cc660291ca8a4e9f675177e138e581b3d692273caf313ce2129`  
		Last Modified: Wed, 16 Jun 2021 18:33:41 GMT  
		Size: 3.9 MB (3874964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4a4aa5bc9b1965904298cb6bc8e2bea999d0bdfecdc07c1be49fa43596d1bf`  
		Last Modified: Wed, 16 Jun 2021 18:33:40 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237f3cded9e40a7b307ce381944576d4bf86d93717f961d5910c53144bca4215`  
		Last Modified: Wed, 16 Jun 2021 18:33:40 GMT  
		Size: 1.4 MB (1363864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e32e8492180e4a99175b71e31b708e2b9f2bf072525c86e2eab5c33523efd8`  
		Last Modified: Wed, 16 Jun 2021 18:33:39 GMT  
		Size: 6.2 MB (6185591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0755b74062a275fa2176570f30cb494bf14ee2a234886c72732c823cdc1fc1`  
		Last Modified: Wed, 16 Jun 2021 18:33:38 GMT  
		Size: 379.1 KB (379149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e4034c11bba4452f687f02bae7176f3a241bdb7a4927b5d7dc201dc62efa54`  
		Last Modified: Wed, 16 Jun 2021 18:33:37 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011d3b2a97445e80f2be6255292c6b7d9b5daa0e93bb24d89d1260dd0a5e49da`  
		Last Modified: Wed, 16 Jun 2021 18:33:37 GMT  
		Size: 5.3 KB (5346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f778e86c6d90cb81111f5343243a58ec4e9888d1df8177961791f878211a2c48`  
		Last Modified: Thu, 17 Jun 2021 01:43:33 GMT  
		Size: 36.2 MB (36158635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3251e6c43b0ec6488182d50b111865a6112d2ce9181f514353c6781713bb95f`  
		Last Modified: Thu, 17 Jun 2021 01:43:24 GMT  
		Size: 8.3 KB (8325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809680dca1ac75c8a2f3a346d5b3c882a2986c36099a0d393136e8c2e50bc72d`  
		Last Modified: Thu, 17 Jun 2021 01:43:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcc970998fa1352f2cfbc4a0eadc6707a537eb3ace363d2461ca684ab023e4c`  
		Last Modified: Thu, 17 Jun 2021 01:43:24 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecce0bf2587bdd1835c6a8287e29eb6f790d02d71cf3a60e4aae21de740c809`  
		Last Modified: Thu, 17 Jun 2021 01:43:24 GMT  
		Size: 4.4 KB (4411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-stretch` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:23628e13a649e98ca641199912c9d9defdaa8ef83781b6b8f9e7fe86de222bb4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69902758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5432ad31a18106f9deb2da7ed931fac46af927e64ec5344e7bc428191dd04e67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 00:56:51 GMT
ADD file:eb2bf800fab313cdab37eb6f5b5c82b2d95ca00628862c99520f3189748737ec in / 
# Wed, 12 May 2021 00:56:54 GMT
CMD ["bash"]
# Wed, 16 Jun 2021 08:45:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 16 Jun 2021 08:45:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 16 Jun 2021 08:45:11 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Jun 2021 08:45:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Jun 2021 08:45:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 16 Jun 2021 08:45:28 GMT
ENV LANG=en_US.utf8
# Wed, 16 Jun 2021 08:45:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Jun 2021 08:45:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 16 Jun 2021 08:45:36 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 16 Jun 2021 08:45:36 GMT
ENV PG_MAJOR=11
# Wed, 16 Jun 2021 23:12:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 16 Jun 2021 23:12:57 GMT
ENV PG_VERSION=11.12-1.pgdg90+1
# Wed, 16 Jun 2021 23:21:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 16 Jun 2021 23:22:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 16 Jun 2021 23:22:01 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 16 Jun 2021 23:22:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 16 Jun 2021 23:22:02 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 16 Jun 2021 23:22:02 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 16 Jun 2021 23:22:03 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 16 Jun 2021 23:22:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Jun 2021 23:22:03 GMT
STOPSIGNAL SIGINT
# Wed, 16 Jun 2021 23:22:03 GMT
EXPOSE 5432
# Wed, 16 Jun 2021 23:22:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:773a656fe22a8f8eb2899cb7975915653ef0213cc26c0dad998984433b56d5f5`  
		Last Modified: Wed, 12 May 2021 01:04:44 GMT  
		Size: 20.4 MB (20389317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a528a1bac926d6416d1de00f4e4668f04c8b0847aa9f3f5924f4a33167a73c84`  
		Last Modified: Wed, 16 Jun 2021 09:27:45 GMT  
		Size: 4.1 MB (4078639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adc9244caf76e91ceab0ff9523fb9906c8ccbc2e0039c3acfd3169e5c103f98`  
		Last Modified: Wed, 16 Jun 2021 09:27:43 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7694ef9961ff745d363e765969f98a50642d5ebc7376e03bcaddd06078505f1`  
		Last Modified: Wed, 16 Jun 2021 09:27:44 GMT  
		Size: 1.3 MB (1347078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65fa25bf3872661f241b35f76dfa705d387e6036219a075b48b1c6facb1ad88`  
		Last Modified: Wed, 16 Jun 2021 09:27:42 GMT  
		Size: 6.2 MB (6185391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df5195288cd03c7bfab06e3ab1870e780d01434e7549ce12865b84d0cbdf82c`  
		Last Modified: Wed, 16 Jun 2021 09:27:42 GMT  
		Size: 377.9 KB (377891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c093f539807fd2568c4c20fc925b596f86a22b596d4d1269ea12a1f1a6adc83`  
		Last Modified: Wed, 16 Jun 2021 09:27:41 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c422f44f24e81b13de97cc04544987d20ad08a4381ff2ffa24449b1530e89d8`  
		Last Modified: Wed, 16 Jun 2021 09:27:41 GMT  
		Size: 5.3 KB (5346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daee5b0281c469d3f48dec10f30c308c483bfda23820280915caf498540010c6`  
		Last Modified: Wed, 16 Jun 2021 23:49:43 GMT  
		Size: 37.5 MB (37504068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4daeffafd4edae56de3aa7b4bca1e849a4002b4a54e7d7fd8bb800d6dff4c9`  
		Last Modified: Wed, 16 Jun 2021 23:49:36 GMT  
		Size: 8.3 KB (8321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42de306609c64745f59503e7f311015e1d930e7d5f6a19af6e32864f1883d21a`  
		Last Modified: Wed, 16 Jun 2021 23:49:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b264041eeeae83530abf6b9d452e8e618361a98f25172a4cc63fe7394a22134a`  
		Last Modified: Wed, 16 Jun 2021 23:49:36 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ed220f14f2129111c3b28b4b58605bb68f427313779d93f2bc0fc73ef85f01`  
		Last Modified: Wed, 16 Jun 2021 23:49:36 GMT  
		Size: 4.4 KB (4413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-stretch` - linux; 386

```console
$ docker pull postgres@sha256:02875d0f3d9c94200175d2662c4e6446caa83f8eb3f293bf5e676361026d2c18
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109993140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247be2fa16de52beb23e768436d0a777f44d2df730b6ed0c746e89ab45cdc6e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 00:41:59 GMT
ADD file:1e77ef0444477c2378e1fe7ce2e0f741f1d571f4e165a55918634f5c982b2488 in / 
# Wed, 12 May 2021 00:41:59 GMT
CMD ["bash"]
# Wed, 12 May 2021 17:10:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 17:10:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 12 May 2021 17:10:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 17:11:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 17:11:15 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 12 May 2021 17:11:15 GMT
ENV LANG=en_US.utf8
# Wed, 12 May 2021 17:11:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:11:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 17:11:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 12 May 2021 17:11:24 GMT
ENV PG_MAJOR=11
# Wed, 16 Jun 2021 23:13:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 16 Jun 2021 23:13:39 GMT
ENV PG_VERSION=11.12-1.pgdg90+1
# Wed, 16 Jun 2021 23:14:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 16 Jun 2021 23:14:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 16 Jun 2021 23:14:04 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 16 Jun 2021 23:14:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 16 Jun 2021 23:14:05 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 16 Jun 2021 23:14:05 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 16 Jun 2021 23:14:06 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 16 Jun 2021 23:14:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Jun 2021 23:14:06 GMT
STOPSIGNAL SIGINT
# Wed, 16 Jun 2021 23:14:06 GMT
EXPOSE 5432
# Wed, 16 Jun 2021 23:14:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:78aed7426e3ec56c5fe4bd663081f534a0389e8aaca5ef3373711f3172e64e0f`  
		Last Modified: Wed, 12 May 2021 00:49:44 GMT  
		Size: 23.2 MB (23156323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853c431359ccec2ff31de2da6381794536877cf3d03e4be2ab9d1080f946f54b`  
		Last Modified: Wed, 12 May 2021 17:16:31 GMT  
		Size: 4.8 MB (4811188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743e9a43fb2debb7767b2edaf0afd4ab2298262e20aa888d2735d96f356fdea2`  
		Last Modified: Wed, 12 May 2021 17:16:30 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c189b78d439a3ff860d609a839196975fde8029eaca3c8f2e6657441c2c90147`  
		Last Modified: Wed, 12 May 2021 17:16:30 GMT  
		Size: 1.4 MB (1382563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a895994f8457e52840eb2bb002d9e0a602496fb9789decdf2db3ca02285860cc`  
		Last Modified: Wed, 12 May 2021 17:16:30 GMT  
		Size: 6.2 MB (6185556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc8697c1a491fe2f51343de0b37046d8b4f51b417c2b21c72dc6b369325f8cf`  
		Last Modified: Wed, 12 May 2021 17:16:27 GMT  
		Size: 393.3 KB (393341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec0ee523547656671410815e970bf8dec18930642937a41f7ad67001ec871f7`  
		Last Modified: Wed, 12 May 2021 17:16:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fbe480bdfb1b3c702135dfbe21d2465358186fe8da74df02578eddbae919ac`  
		Last Modified: Wed, 12 May 2021 17:16:27 GMT  
		Size: 5.3 KB (5348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16097047a7cc770999bbd24eb72794adfc3073334a5e995581af7d099a45063c`  
		Last Modified: Wed, 16 Jun 2021 23:26:15 GMT  
		Size: 74.0 MB (74043805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77acd0b78ff0647dea24455545e57c943fb80149891841025244e85fc374fa2a`  
		Last Modified: Wed, 16 Jun 2021 23:25:59 GMT  
		Size: 8.3 KB (8324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c682f571d76ff58e836569d9665e7d4077c30417e21cd3647c2601cf2f814e03`  
		Last Modified: Wed, 16 Jun 2021 23:25:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d291b3ba8f02abdbe2d53f1446068740553169da4194b17d15be3ea82d551b3`  
		Last Modified: Wed, 16 Jun 2021 23:25:59 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5352b32400be75f3cb38424979ec44466a83cc4151a3422e1b25357d08ac06f`  
		Last Modified: Wed, 16 Jun 2021 23:25:59 GMT  
		Size: 4.4 KB (4410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
