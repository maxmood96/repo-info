## `postgres:15-bookworm`

```console
$ docker pull postgres@sha256:d9b1b0ec74e734772a2e76c72d36a51de21f3842a6c872cf356a26a0a6b903d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `postgres:15-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:4ef90ecceb2ec8a4f693a627874ca2563ecd76895a25add69f94d6a8a3f98d38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148939025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0cae92a4f64c1c086a2c621afd21d05f20109f3b3c1457eeb0976875d684fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:20:51 GMT
ADD file:3a8cd4de7f163d93718670f4db1de49045f5e04af3a8aa27d81c0f14647db707 in / 
# Thu, 07 Sep 2023 00:20:51 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 14:22:15 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 14:22:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 14:22:21 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 14:22:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 14:22:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 14:22:36 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 14:22:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 14:22:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 14:22:42 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 14:24:16 GMT
ENV PG_MAJOR=15
# Thu, 07 Sep 2023 14:24:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Fri, 15 Sep 2023 22:30:05 GMT
ENV PG_VERSION=15.4-2.pgdg120+1
# Fri, 15 Sep 2023 22:30:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 22:30:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 22:30:24 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 22:30:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 22:30:25 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 22:30:25 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 22:30:25 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 22:30:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 22:30:25 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 22:30:25 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 22:30:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:360eba32fa65016e0d558c6af176db31a202e9a6071666f9b629cb8ba6ccedf0`  
		Last Modified: Thu, 07 Sep 2023 00:25:22 GMT  
		Size: 29.1 MB (29124494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987678f9780a65e1300c3d532de110c386c1c31426a9d58bf6a89064dc5891e`  
		Last Modified: Thu, 07 Sep 2023 14:29:42 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42299245e9050289da4064333ed9c50baa15c2d2e2553c5c63cd61f1cd58d913`  
		Last Modified: Thu, 07 Sep 2023 14:29:43 GMT  
		Size: 4.6 MB (4618729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcda32ad76a6ffb6b64cdd88d736e02ed9061da715f6e1ace084917f1545a57`  
		Last Modified: Thu, 07 Sep 2023 14:29:42 GMT  
		Size: 1.4 MB (1444748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d81c7506667f1840cfec9f2300f7c8e2fd339b8dc75d994b56510fea75220d`  
		Last Modified: Thu, 07 Sep 2023 14:29:41 GMT  
		Size: 8.1 MB (8065033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7813914a8b7e2fce2df17d99844729d113fe54db71504972e23f275adac38d6`  
		Last Modified: Thu, 07 Sep 2023 14:29:40 GMT  
		Size: 1.4 MB (1405696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876fecb4c432d062ffcc214cbdec029ffe9455f30f3e591f5c9680322f52c963`  
		Last Modified: Thu, 07 Sep 2023 14:29:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8727713246ed1e93b83ea6566473f0e49d331d6bd78d495a25921149423e7f`  
		Last Modified: Thu, 07 Sep 2023 14:29:39 GMT  
		Size: 3.2 KB (3200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6be90f8305f6f639e081d00596cfb372ac390dc6dc6791e0d5079b669fb59f6`  
		Last Modified: Fri, 15 Sep 2023 22:34:23 GMT  
		Size: 104.3 MB (104260868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e88fdcb6fff055f342ed7655e9fc485dc0cae1e0632321e12b41a3528c984f1`  
		Last Modified: Fri, 15 Sep 2023 22:34:10 GMT  
		Size: 9.8 KB (9780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2f4b690495cb32358f81fecafd09a69fef4dfcfa14ab43dece1a1bd6dddb0e`  
		Last Modified: Fri, 15 Sep 2023 22:34:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e102fbfee76e9a002c0c0790b7ef32f963ad0b9b44fc53e07e00109a08557c8`  
		Last Modified: Fri, 15 Sep 2023 22:34:10 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4afb034eaf04b7bb78c691081b2c9a7b7b9d2337cfd61777453cadd9a422ef`  
		Last Modified: Fri, 15 Sep 2023 22:34:10 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:4914d3b7e8198126b0d4d385044ae3bfe5da729d337ed36a87271bc57281c8ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141869897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b72f88c563236ce61c7888900c2687d2e3a0bbedf7f811327c4dcee1cec65c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:48:30 GMT
ADD file:e7b77e5797ddb7e058507462fd5f5aad6864ba08ebc4a6c2743dae81ed0f445d in / 
# Thu, 07 Sep 2023 00:48:31 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:53:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 02:53:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:53:53 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 02:54:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 02:54:15 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 02:54:15 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 02:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:54:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 02:54:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 03:30:01 GMT
ENV PG_MAJOR=15
# Thu, 07 Sep 2023 03:30:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Fri, 15 Sep 2023 23:14:30 GMT
ENV PG_VERSION=15.4-2.pgdg120+1
# Fri, 15 Sep 2023 23:29:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 23:29:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 23:29:19 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 23:29:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 23:29:20 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 23:29:20 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 23:29:20 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 23:29:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 23:29:20 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 23:29:20 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 23:29:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d971e043cc5e8068fe39c736806d279b128c720a08d2e0d41002dcf027787939`  
		Last Modified: Thu, 07 Sep 2023 00:51:35 GMT  
		Size: 27.0 MB (26983530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8b047558c321f3d85dac362acc6b5be2ef1a63e1228dcc312fe0349e7368d`  
		Last Modified: Thu, 07 Sep 2023 05:51:18 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a001ee6f62d264464ebac6fa7957af0eef9f2b372d086b3ceb5ca0716d4a7c`  
		Last Modified: Thu, 07 Sep 2023 05:51:20 GMT  
		Size: 4.2 MB (4236742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088a29538691f49cbe34a2b6ad563f1906160e4d50d03209b0060a3ea384a736`  
		Last Modified: Thu, 07 Sep 2023 05:51:18 GMT  
		Size: 1.4 MB (1422349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5642e454380eb8686c56be7ecce79209c1bbf2b5e9e29d5d0155e611b336f2e2`  
		Last Modified: Thu, 07 Sep 2023 05:51:19 GMT  
		Size: 8.1 MB (8065171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b620324ad132460ef93d433f9180591c03a526c710577816ef1644bec32ddd70`  
		Last Modified: Thu, 07 Sep 2023 05:51:16 GMT  
		Size: 1.4 MB (1404068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4ffcb4a7cd4a043e5b402406876a8cf7b66de35c58e3d7ceb859398ba7d5ee`  
		Last Modified: Thu, 07 Sep 2023 05:51:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef49764891b3f19a655bc08ffff0cc05e87eecd546576c26e55740dcea514f0a`  
		Last Modified: Thu, 07 Sep 2023 05:51:15 GMT  
		Size: 3.2 KB (3201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4087b974af7b9ee23818cddb04daf0985d4f2843b8a43d39759e9fedf6a80efb`  
		Last Modified: Fri, 15 Sep 2023 23:45:49 GMT  
		Size: 99.7 MB (99738566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0514ea5b2bed313f1d5073c8e5c357b945292a4efddf6a4ae08e79694527c1`  
		Last Modified: Fri, 15 Sep 2023 23:45:30 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb76f79f5e47ac776b37cab64a1128d811e273f4bce11c9ae41bcee77567e746`  
		Last Modified: Fri, 15 Sep 2023 23:45:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc5bd61a5933b226d1b5ebf92227d03aad2a476fd9a5ae4180e328f21ca12e9`  
		Last Modified: Fri, 15 Sep 2023 23:45:30 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459f43019f55bec4bd82a83bd2582fb70a8495c2b4ebb1e9e56e537dd4929bf3`  
		Last Modified: Fri, 15 Sep 2023 23:45:30 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:58992c3c031b0df781f62a49722893aa0d38773f3d9fd49b626b0c2518183048
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136738595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fcfb14b6107d368ccce29d7fe7215503bc18c1996493d43d8d4ff323dabe1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:57:48 GMT
ADD file:5775cb975a13a9e48198190564cd469f115a433dabc5c3406c45e1ef0b1ccdf0 in / 
# Thu, 07 Sep 2023 00:57:49 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 04:11:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 04:11:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 04:11:39 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 04:11:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 04:11:55 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 04:11:55 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 04:11:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 04:12:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 04:12:01 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 04:41:52 GMT
ENV PG_MAJOR=15
# Thu, 07 Sep 2023 04:41:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Fri, 15 Sep 2023 22:58:25 GMT
ENV PG_VERSION=15.4-2.pgdg120+1
# Fri, 15 Sep 2023 23:12:34 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 23:12:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 23:12:36 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 23:12:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 23:12:37 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 23:12:37 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 23:12:37 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 23:12:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 23:12:37 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 23:12:37 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 23:12:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a9fec8868f77cdcda1bf847be168c1d104031ca6c8edc961bc7f76e3a4bf54b`  
		Last Modified: Thu, 07 Sep 2023 01:02:31 GMT  
		Size: 24.8 MB (24805221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999d6861171255263f391e61de575844c466d1febd75af8fa5d511fac54e3cfc`  
		Last Modified: Thu, 07 Sep 2023 06:55:41 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53577034808c93e57db36b89db59aa949c0fbc412ce574993eca6d27b888334e`  
		Last Modified: Thu, 07 Sep 2023 06:55:41 GMT  
		Size: 3.8 MB (3839571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf7a366d36d9a45c69a4e4c643b64dd1a52c041349f4725afdb533c28841a2`  
		Last Modified: Thu, 07 Sep 2023 06:55:41 GMT  
		Size: 1.4 MB (1411957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffa833623bff42fe1cb8cbdffb7fadba5270226da7af67adfca20c4602aa02c`  
		Last Modified: Thu, 07 Sep 2023 06:55:41 GMT  
		Size: 8.1 MB (8065045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc754d0b977295419a2f915ff581a2f9bc3b02899e96adebf5124b5eccc19fe7`  
		Last Modified: Thu, 07 Sep 2023 06:55:39 GMT  
		Size: 1.3 MB (1277643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec504dc35e1c85529fedf0ada8ee845054a2b940034afd8184ce27cfecd9f1a`  
		Last Modified: Thu, 07 Sep 2023 06:55:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cccd2df8625a79b96543f30d28afd1ed156b2c0db4639d8a890ab84923a6b0`  
		Last Modified: Thu, 07 Sep 2023 06:55:38 GMT  
		Size: 3.2 KB (3198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9046a28b858f788984b39ba47597a2ed832a36cc290928ba5a835ed461cef3dd`  
		Last Modified: Fri, 15 Sep 2023 23:29:18 GMT  
		Size: 97.3 MB (97319700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d259b07751ba2b4435bbfea25896fbf0b6e6adcdcb1ce1cd23f89995426ae032`  
		Last Modified: Fri, 15 Sep 2023 23:29:04 GMT  
		Size: 9.8 KB (9784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bc3be8d617fc4c3ebe2a99299b98852065bbc7939ae3d0d16a561fbe3d7701`  
		Last Modified: Fri, 15 Sep 2023 23:29:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbe47f3017de183f9e9398dc1001b61c72bfd285f9d8713f2937500c884779a`  
		Last Modified: Fri, 15 Sep 2023 23:29:04 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5d7f40cadf8f1dd033036c03ab6f9300b16924aab9303558e834e7c39ca71f`  
		Last Modified: Fri, 15 Sep 2023 23:29:04 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:0ba700ecc660e3defaf8ef612d8c50ac81ccac61f3cd61c86b71beb2010b2cf1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146885455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281bd8bbb36e0d96efc02e53598907ccc7b7dbd334b4a4ecc19da73642ac929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:39 GMT
ADD file:fb5c8f411c4a1e06c25ac32455221938386907d0b4782fc228ca67de63a7e9de in / 
# Thu, 07 Sep 2023 00:39:39 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 05:48:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 05:49:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 05:49:04 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 05:49:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 05:49:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 05:49:17 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 05:49:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 05:49:21 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 05:49:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 05:50:38 GMT
ENV PG_MAJOR=15
# Thu, 07 Sep 2023 05:50:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Fri, 15 Sep 2023 22:49:39 GMT
ENV PG_VERSION=15.4-2.pgdg120+1
# Fri, 15 Sep 2023 22:49:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 22:49:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 22:49:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 22:49:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 22:49:58 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 22:49:58 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 22:49:58 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 22:49:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 22:49:59 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 22:49:59 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 22:49:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:155eab17d86c47443adc8cebe7fc62c847c03db8cfb1ca53aa6276564fff23ef`  
		Last Modified: Thu, 07 Sep 2023 00:43:02 GMT  
		Size: 29.2 MB (29157149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55722f192d83c20c8f76ea6e4a67442422f4e3b267cf5bb52fab9574a8a823e`  
		Last Modified: Thu, 07 Sep 2023 05:55:26 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ba17ccdd1c8e7039acb98c0b4a8cd5032a8e24401a3a41051b5cee8fff3e10`  
		Last Modified: Thu, 07 Sep 2023 05:55:27 GMT  
		Size: 4.6 MB (4578373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dfde5d5395194e4bd8d2acfa1fbfb6f7fb981552740db93ef72532f54105fe`  
		Last Modified: Thu, 07 Sep 2023 05:55:26 GMT  
		Size: 1.4 MB (1376571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e1089c0d388aca82bdb508c841d9f075b32ef2f15363741feb9ff244dd966b`  
		Last Modified: Thu, 07 Sep 2023 05:55:26 GMT  
		Size: 8.1 MB (8065199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d777fedefbac0ed8c7489beb6415c5d956cdcb3735bf2ebebe57c34cbe311a63`  
		Last Modified: Thu, 07 Sep 2023 05:55:24 GMT  
		Size: 1.3 MB (1317866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0a37cd4f7f3593b3341ef531274d82c2b6d39d815735f96d83e088d21b185d`  
		Last Modified: Thu, 07 Sep 2023 05:55:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d24f0e05805b51cca91a59256efc113f3c1c534404287899152d50e9b03ea7`  
		Last Modified: Thu, 07 Sep 2023 05:55:24 GMT  
		Size: 3.2 KB (3200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d54d3553c19c7820d3572eb0f75567e1ce2e6b84613d00a4a77fd3aeb0888a`  
		Last Modified: Fri, 15 Sep 2023 22:53:19 GMT  
		Size: 102.4 MB (102370837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf42583998b10b39d40f54300ad2dd403f9b727e590e0d213203d3073d2f4d4d`  
		Last Modified: Fri, 15 Sep 2023 22:53:09 GMT  
		Size: 9.8 KB (9780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881e44e9ee52ff5287d20de0a0865efdf09df3fcb685d81608909abeb3958352`  
		Last Modified: Fri, 15 Sep 2023 22:53:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b98ad01362c4c6b00d61f475ec27aac6ab995f995b7be6574fd9d59bd28d72`  
		Last Modified: Fri, 15 Sep 2023 22:53:09 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b1a096613bdc3ee98ed15f9a2f924898ed7ccd85a0a95f1585ef1a688a4ea7`  
		Last Modified: Fri, 15 Sep 2023 22:53:09 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:0e6071110949b378ea1886925ae08a9600c8d4f54b798440689fa277f8356c70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156040290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab9e637c144aa10a2b9f7820f78088e43c007a374ce75941cf56ebfe51433fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:00 GMT
ADD file:0952a54f5474629ed000e89bfd1b8827e49b63270932e45ed8d953a2676ac79c in / 
# Thu, 07 Sep 2023 00:39:00 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:08:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 01:08:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:08:56 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 01:09:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 01:09:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 01:09:17 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 01:09:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:09:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 01:09:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 01:48:53 GMT
ENV PG_MAJOR=15
# Thu, 07 Sep 2023 01:48:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Fri, 15 Sep 2023 23:15:44 GMT
ENV PG_VERSION=15.4-2.pgdg120+1
# Fri, 15 Sep 2023 23:34:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 23:34:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 23:34:55 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 23:34:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 23:34:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 23:34:56 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 23:34:56 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 23:34:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 23:34:56 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 23:34:57 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 23:34:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:30ae0f429560d1effd0839849ab7780512b72d9fbc09a6cec67e03092a85a1d1`  
		Last Modified: Thu, 07 Sep 2023 00:43:48 GMT  
		Size: 30.1 MB (30141753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f46dbec3f5e6f4c75ea8d19dae300dcffbb4aa5d5d46b76033825d46bd8c262`  
		Last Modified: Thu, 07 Sep 2023 04:40:03 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8d71699dabe1c5baf4a11e8c37292bc4f8d1ad9f7800643542f194795389bd`  
		Last Modified: Thu, 07 Sep 2023 04:40:04 GMT  
		Size: 5.0 MB (5039432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40dcb44c9c86789af1867251d6aaa55a0f5626ba1a4d55c7bf0babd8d0ce993a`  
		Last Modified: Thu, 07 Sep 2023 04:40:03 GMT  
		Size: 1.4 MB (1420316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa64f3aa56ca13d5ede15422c423d1e5f8280cf13302284230e2dc05348c81f`  
		Last Modified: Thu, 07 Sep 2023 04:40:04 GMT  
		Size: 8.1 MB (8065077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0143e5ca7ce1c66755ed946ffd59d214d6d446df619144f1a167b2d04f4f77fa`  
		Last Modified: Thu, 07 Sep 2023 04:40:01 GMT  
		Size: 1.3 MB (1346477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e61f6dd5a6b813733d4817d4e1b6dbc03aca80351b3d802637529dbcf5d1a6d`  
		Last Modified: Thu, 07 Sep 2023 04:40:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f517a716c661221e613e926a9a1e5802d4976be5e9465314f7392dda961c4aed`  
		Last Modified: Thu, 07 Sep 2023 04:40:00 GMT  
		Size: 3.2 KB (3200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a6dbc67ad224459bdba6ca481d83722728a16567170e45274e4c7b30652ded`  
		Last Modified: Fri, 15 Sep 2023 23:57:15 GMT  
		Size: 110.0 MB (110007772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999b83b3300165b61f98b8e6770f6eb115a3380359fda879fa73f478fd84b82c`  
		Last Modified: Fri, 15 Sep 2023 23:56:53 GMT  
		Size: 9.8 KB (9788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d6350901a134a19691d058fea06e72df5cdc6554ecc39059181016ff36f57f`  
		Last Modified: Fri, 15 Sep 2023 23:56:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bb2a4680c7bd3274d25eaebbaf0346a40e76992967b1677fd2476651f94998`  
		Last Modified: Fri, 15 Sep 2023 23:56:52 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb095d32300c43e191405c9464651f59b54a84155b8cc49de606d16c88ed7d1`  
		Last Modified: Fri, 15 Sep 2023 23:56:52 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:f990280fe6c5a9fcfc3614e77ec4e1c734b3030b6396cb659295e1068ae16d9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144635105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21381d56a8a135ea8aa20b1017e27e5d8786fc1e08dc4340daae724578eeaf6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 01:09:11 GMT
ADD file:263719948aa8496c0852aa2ef6c6660c25ce35618af5b1c5bc35c901d853bcf8 in / 
# Thu, 07 Sep 2023 01:09:17 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 19:44:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 19:44:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 19:44:58 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 19:45:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 19:45:58 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 19:46:01 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 19:46:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 19:46:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 19:46:31 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 21:58:37 GMT
ENV PG_MAJOR=15
# Thu, 07 Sep 2023 21:58:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Sat, 16 Sep 2023 00:24:39 GMT
ENV PG_VERSION=15.4-2.pgdg120+1
# Sat, 16 Sep 2023 01:28:04 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Sat, 16 Sep 2023 01:28:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Sat, 16 Sep 2023 01:28:16 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 16 Sep 2023 01:28:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 16 Sep 2023 01:28:25 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 16 Sep 2023 01:28:28 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 16 Sep 2023 01:28:31 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Sat, 16 Sep 2023 01:28:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 01:28:38 GMT
STOPSIGNAL SIGINT
# Sat, 16 Sep 2023 01:28:41 GMT
EXPOSE 5432
# Sat, 16 Sep 2023 01:28:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a6519d39af9071c1099bd2a01d04c824d095fb31f439e10814371707227802ae`  
		Last Modified: Thu, 07 Sep 2023 01:20:14 GMT  
		Size: 29.1 MB (29121387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18af474dc84f99261867730073661aba1d2fd9557be2b13b58d9d24d8c73f066`  
		Last Modified: Fri, 08 Sep 2023 07:46:23 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618cd013a798c25885029837623a9d7847c3f015faa81eadab5587c131ca35fd`  
		Last Modified: Fri, 08 Sep 2023 07:46:26 GMT  
		Size: 4.4 MB (4355627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185fcc2cb22a64b3b53aa8d284136774bbdfd422831194549af977436c982c69`  
		Last Modified: Fri, 08 Sep 2023 07:46:24 GMT  
		Size: 1.3 MB (1331491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c9d587d20dea2a5f0ae108d5ca0e269cca19f1a107b3a17a2b0758d1bdbd7f`  
		Last Modified: Fri, 08 Sep 2023 07:46:28 GMT  
		Size: 8.1 MB (8064894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffacf3d23809923d6c0de9ea58fa547184988d38fe6c224e52670a7ccd2c750`  
		Last Modified: Fri, 08 Sep 2023 07:46:21 GMT  
		Size: 1.2 MB (1181558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb738a4bc28ff81d76098f725a2f84a8990d65f0f427abf798f41ff01e7eb4a5`  
		Last Modified: Fri, 08 Sep 2023 07:46:20 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b888b5bb2dc1d7c10d07be463e3f579c948ee61267c232ea1de55cde8a16a40f`  
		Last Modified: Fri, 08 Sep 2023 07:46:19 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff6debb90a2bf85bccaf89b5717fb00687ef3b233458df905c9bbfafdf617b8`  
		Last Modified: Sat, 16 Sep 2023 02:35:13 GMT  
		Size: 100.6 MB (100560887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7de5e44f4505db366cb836b4b80407778944a6948ca429446d3e0a531b98ac`  
		Last Modified: Sat, 16 Sep 2023 02:34:11 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67f63eca11cb90f756e68f8c2301a8e2714a5d65c26f6c4665d167995619901`  
		Last Modified: Sat, 16 Sep 2023 02:34:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64b5b12ca091c8629d7858cebd123f5100d47dadd135517614286b63d2aca7f`  
		Last Modified: Sat, 16 Sep 2023 02:34:11 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7bcc39401a82a1fbbb6ffb9e18a38df184abb3dac5d6d7ef5d44072bf40131`  
		Last Modified: Sat, 16 Sep 2023 02:34:11 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:271b1af180c90e6de3458733c7bd11e67951b9f30a663f4e0134cecdc01a29e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160734743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62623ff01d3faa7a7d93eb00ef2014c9c9d647d4a114ec0c35b3b1b190792b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:17:29 GMT
ADD file:c5cce4a01995fb11fea5067fdf342af046481b4869e8e858a85986686f68ef2a in / 
# Thu, 07 Sep 2023 00:17:32 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 16:25:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 16:25:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 16:25:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 16:25:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 16:26:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 16:26:08 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 16:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 16:26:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 16:26:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 16:29:51 GMT
ENV PG_MAJOR=15
# Thu, 07 Sep 2023 16:29:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Fri, 15 Sep 2023 23:05:58 GMT
ENV PG_VERSION=15.4-2.pgdg120+1
# Fri, 15 Sep 2023 23:07:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 23:07:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 23:07:21 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 23:07:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 23:07:27 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 23:07:28 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 23:07:29 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 23:07:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 23:07:36 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 23:07:37 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 23:07:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1db76043538a495ac265ef61277e1a2137637bebdc1ffa7712108b3efe4a4d33`  
		Last Modified: Thu, 07 Sep 2023 00:23:29 GMT  
		Size: 33.1 MB (33119207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca4407b91945cefaf57592756b201b9bbed2e8dc33baa9972abb512406c06da`  
		Last Modified: Thu, 07 Sep 2023 16:42:09 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e17881de676d15d36eae9d56f24ca1f069cb1abda2d5a5cc896a2f9782d673`  
		Last Modified: Thu, 07 Sep 2023 16:42:10 GMT  
		Size: 5.4 MB (5433636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039c3785da844676d84eda8a89b711923496f248b15dfce8ceca922006528c59`  
		Last Modified: Thu, 07 Sep 2023 16:42:09 GMT  
		Size: 1.4 MB (1367241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c566d192e2b6d880fef53c3ee90831024c62f21caf5d5935c24daf0fc89c1e89`  
		Last Modified: Thu, 07 Sep 2023 16:42:09 GMT  
		Size: 8.1 MB (8065164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e12edd582ad487fdd333d82dd17da5ef809694798fae513d639fb9c5f7dedd3`  
		Last Modified: Thu, 07 Sep 2023 16:42:07 GMT  
		Size: 1.5 MB (1494542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d381305b9544768a35acc06d02a8ade09c3437f15a4b55bfbb9f4d781b89fb9`  
		Last Modified: Thu, 07 Sep 2023 16:42:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b58c5d8694270b75bf48e1e4ab863e482aab47b9deb973e3b855beea679ef9`  
		Last Modified: Thu, 07 Sep 2023 16:42:07 GMT  
		Size: 3.2 KB (3200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb891ffeb60bb034daeb4f2182ac0d63581f4eaf8119cab19542616290e696dc`  
		Last Modified: Fri, 15 Sep 2023 23:14:24 GMT  
		Size: 111.2 MB (111235487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b0c641f69bbe1b6fc0c1feba294067958aa3f87305a1f36fdf8f444dc83dbe`  
		Last Modified: Fri, 15 Sep 2023 23:13:58 GMT  
		Size: 9.8 KB (9785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33a4ef0869d44b8898770986b43e4d8393506f76cef47b472ecfaa1911c3687`  
		Last Modified: Fri, 15 Sep 2023 23:13:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8ebfdbb4d367a8076129f4b8bb76aafaed48f7cf064f3f918df563c2aeae86`  
		Last Modified: Fri, 15 Sep 2023 23:13:58 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8640039558511a0a0e5ea1c47113c56f4fca3828508e3011c706b67e93671a`  
		Last Modified: Fri, 15 Sep 2023 23:13:58 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:c8b13878eb4c0e29cf80a8d42346436c9427a0796e29994748704cade0adf7ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154255446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a946f77824d2dd2da927acdd8e1cbb9b5d31eaf5ff2ee34d9b8804dbce8aab8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:43:39 GMT
ADD file:2a617cce71dc34ce7b62d4b1da4b45cca574c219300ba2be25396630f80bb9cd in / 
# Thu, 07 Sep 2023 00:43:47 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:43:21 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 09:43:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:43:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 09:43:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 09:43:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 09:43:40 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 09:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:43:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 09:43:45 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 09:45:30 GMT
ENV PG_MAJOR=15
# Thu, 07 Sep 2023 09:45:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Fri, 15 Sep 2023 22:31:03 GMT
ENV PG_VERSION=15.4-2.pgdg120+1
# Fri, 15 Sep 2023 22:31:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 22:31:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 22:31:33 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 22:31:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 22:31:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 22:31:34 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 22:31:34 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 22:31:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 22:31:34 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 22:31:34 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 22:31:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:68043338ec5d8515f0dcc40f82eb11d30dd8539a1d30984e4b157df8779f6d53`  
		Last Modified: Thu, 07 Sep 2023 00:49:40 GMT  
		Size: 27.5 MB (27489648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47ff2b4de49c4c26503044f9c80367bcea18c867befe09b99cce4ebc2edd8cf`  
		Last Modified: Thu, 07 Sep 2023 09:54:48 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3709e147d007a9416b5d5c525e0407cb89d479abc59ef6e4190e5654674740be`  
		Last Modified: Thu, 07 Sep 2023 09:54:48 GMT  
		Size: 4.5 MB (4474543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5d2e99909cd167970fb123f11ffaaf2ccd3e2220db859d8682f85175bb264d`  
		Last Modified: Thu, 07 Sep 2023 09:54:47 GMT  
		Size: 1.4 MB (1410596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15e0461a9395a1992567658cfe4a86ba3d72ffe923713c674ef726e86c8d928`  
		Last Modified: Thu, 07 Sep 2023 09:54:47 GMT  
		Size: 8.1 MB (8119622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ed487407e3f8279ef057a42a0f127fd6232bfe32efc6f00719b74d8f6aeab7`  
		Last Modified: Thu, 07 Sep 2023 09:54:46 GMT  
		Size: 1.3 MB (1307758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08560e87a93355c4c4c871dc754a38ec33527ba5c306f9ac90765a421009b2c2`  
		Last Modified: Thu, 07 Sep 2023 09:54:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe713cb98eb252c0f75a308e583accad73d821271550d4d7c20e53aa2697f811`  
		Last Modified: Thu, 07 Sep 2023 09:54:46 GMT  
		Size: 3.2 KB (3193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9569b40537cf0b5bc659074442d3f4ef8a6480c06af607e866e58d54317dbf2d`  
		Last Modified: Fri, 15 Sep 2023 22:37:00 GMT  
		Size: 111.4 MB (111433826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc043da97102896c6021a3f091fb20158577780d728e4402a1be21060cb2717a`  
		Last Modified: Fri, 15 Sep 2023 22:36:46 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f13bfeac9bb2d7453bfad30d1d291c8b12ed8a302449425a4d323624598deb0`  
		Last Modified: Fri, 15 Sep 2023 22:36:46 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a0a62e91dfcdcdc262ac46cd8fb2ecaea69b59fb9bc96382c3f1008ff3d6d`  
		Last Modified: Fri, 15 Sep 2023 22:36:46 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b303285750e87f45fa1e3e62c45bcd2daad75d45ec1add103c56ec38202f84f`  
		Last Modified: Fri, 15 Sep 2023 22:36:46 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
