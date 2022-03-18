## `postgres:11-stretch`

```console
$ docker pull postgres@sha256:67d975b6c5f5be7657ad680f774abd720ac4ae1f90cc89806d38f9fb57864613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `postgres:11-stretch` - linux; amd64

```console
$ docker pull postgres@sha256:6bc5f85898a05b044e6a1b2484ecd64f811f5c1412649cd6a80efb658f73f555
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.5 MB (107452693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1377d9ce15746da91235d2419a59769d64b9b011baea46554b229e5d6a6d22d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 17 Mar 2022 04:06:48 GMT
ADD file:9fc739b295073dd1d9293d2ea8106e21156de790c82a9d19be210c0c63bfb527 in / 
# Thu, 17 Mar 2022 04:06:48 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 13:48:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 13:48:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 17 Mar 2022 13:48:25 GMT
ENV GOSU_VERSION=1.14
# Thu, 17 Mar 2022 13:48:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 17 Mar 2022 13:48:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 17 Mar 2022 13:48:44 GMT
ENV LANG=en_US.utf8
# Thu, 17 Mar 2022 13:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 13:48:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 17 Mar 2022 13:49:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 17 Mar 2022 13:49:18 GMT
ENV PG_MAJOR=11
# Thu, 17 Mar 2022 13:49:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 17 Mar 2022 13:49:18 GMT
ENV PG_VERSION=11.15-1.pgdg90+1
# Thu, 17 Mar 2022 13:49:41 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			apt-get install -y --no-install-recommends clang-6.0; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 17 Mar 2022 13:49:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 17 Mar 2022 13:49:43 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 17 Mar 2022 13:49:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 17 Mar 2022 13:49:43 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 17 Mar 2022 13:49:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 17 Mar 2022 13:49:44 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Thu, 17 Mar 2022 13:49:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 13:49:44 GMT
STOPSIGNAL SIGINT
# Thu, 17 Mar 2022 13:49:44 GMT
EXPOSE 5432
# Thu, 17 Mar 2022 13:49:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5d9da879a61c05a35520eabaa04d22b4867d0cf84a91f4c7b078128e1c820ce5`  
		Last Modified: Thu, 17 Mar 2022 04:14:03 GMT  
		Size: 22.6 MB (22567740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbe7aca3cebb9d1978e0bd772869b1e522ba46f693bc7ec251a70a593613eaa`  
		Last Modified: Thu, 17 Mar 2022 14:04:32 GMT  
		Size: 4.5 MB (4504023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0889c6695e53a6099718534c91281d7f83356ca80bafb8fc03d2b0a13ada173c`  
		Last Modified: Thu, 17 Mar 2022 14:04:31 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4bee59f49a20ace1b8fb7536fb6d3f72288061d76238b9894ca282b4f13580`  
		Last Modified: Thu, 17 Mar 2022 14:04:31 GMT  
		Size: 1.4 MB (1379606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9643bc7544242f73ed2728ced231ce3d24672d017bae484b1b264b6e9e1428`  
		Last Modified: Thu, 17 Mar 2022 14:04:31 GMT  
		Size: 6.2 MB (6185783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a167f44a0e3839acf9f2a01fa3a73a9b3bba938d799d0185ddf835515a3948`  
		Last Modified: Thu, 17 Mar 2022 14:04:29 GMT  
		Size: 1.2 MB (1249893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff13e8e6eba609807cd4f3e1831a388d3ed5746335dfd88c1c56a005053fff9`  
		Last Modified: Thu, 17 Mar 2022 14:04:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6176a95452cf290183403fecc6b2e99c10865b91acca8450098f2877a1f629`  
		Last Modified: Thu, 17 Mar 2022 14:04:28 GMT  
		Size: 5.6 KB (5585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df50906c22a2a75ce39d5ca290710194fc1fa0e41d049e94d30b792b1f4bdaed`  
		Last Modified: Thu, 17 Mar 2022 14:04:37 GMT  
		Size: 71.5 MB (71544743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dd1f1d9c68f8c4a25e0768431e322d35ce6d433667b48c39e7d7b9f227088d`  
		Last Modified: Thu, 17 Mar 2022 14:04:26 GMT  
		Size: 8.3 KB (8323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902e58bf68e99fbe483fde17beea5f80f54bb1c516142a0f3a68008992f02af9`  
		Last Modified: Thu, 17 Mar 2022 14:04:26 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d587eeb739634928645354a3ed0d3741b70576397730616575469c62ba8d15`  
		Last Modified: Thu, 17 Mar 2022 14:04:26 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efe73e0a0bdf3d3edd5bf00a69ee3004f9fafe598b06b200d89dcf56f757dac`  
		Last Modified: Thu, 17 Mar 2022 14:04:27 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-stretch` - linux; arm variant v5

```console
$ docker pull postgres@sha256:adf33aca9a046657b16773db7df54979ea2853219e30379565449a8a951dad43
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71567596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72c913e79e7d72ad1a817a81266875db2d6c081837da4137628b4424fb3f415`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 17 Mar 2022 05:25:17 GMT
ADD file:361613c0ba7e9346788e50c6b777cebaedc3d7d43549a7c05a21d02b7cc91fbe in / 
# Thu, 17 Mar 2022 05:25:18 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 16:30:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 16:30:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 17 Mar 2022 16:30:40 GMT
ENV GOSU_VERSION=1.14
# Thu, 17 Mar 2022 16:31:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 17 Mar 2022 16:31:33 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 17 Mar 2022 16:31:34 GMT
ENV LANG=en_US.utf8
# Thu, 17 Mar 2022 16:31:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 16:31:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 17 Mar 2022 16:32:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 17 Mar 2022 16:32:07 GMT
ENV PG_MAJOR=11
# Thu, 17 Mar 2022 16:32:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 17 Mar 2022 16:32:07 GMT
ENV PG_VERSION=11.15-1.pgdg90+1
# Thu, 17 Mar 2022 16:59:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			apt-get install -y --no-install-recommends clang-6.0; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 17 Mar 2022 16:59:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 17 Mar 2022 16:59:04 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 17 Mar 2022 16:59:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 17 Mar 2022 16:59:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 17 Mar 2022 16:59:06 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 17 Mar 2022 16:59:07 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Thu, 17 Mar 2022 16:59:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 16:59:08 GMT
STOPSIGNAL SIGINT
# Thu, 17 Mar 2022 16:59:08 GMT
EXPOSE 5432
# Thu, 17 Mar 2022 16:59:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d2371effe9f22d47864225c806b5565187fb3f7a418a751f1f8320169de8d566`  
		Last Modified: Thu, 17 Mar 2022 05:42:46 GMT  
		Size: 21.2 MB (21240767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2449b224fa9333fad0e294eca5e517064a2b9250c4ea173b816601f10fdd0b6`  
		Last Modified: Thu, 17 Mar 2022 17:56:30 GMT  
		Size: 4.2 MB (4239527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09063b10a144df04b60f1a075b9a3865a6567bea9b0561b18a61dc56472b54d6`  
		Last Modified: Thu, 17 Mar 2022 17:56:27 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113b5d58da8ab9616e18df4c1be906a5ec6df5899c4ecb4b3dea700b257fd39a`  
		Last Modified: Thu, 17 Mar 2022 17:56:28 GMT  
		Size: 1.3 MB (1344525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a832b0a2ba0d39196830f92313193651f4ce4c5d87cdacaa97dbd9fe542158`  
		Last Modified: Thu, 17 Mar 2022 17:56:30 GMT  
		Size: 6.2 MB (6185731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3152d45ab3913876a3043fafd239beea96dd661e9179e1759acb271e619d91`  
		Last Modified: Thu, 17 Mar 2022 17:56:26 GMT  
		Size: 1.2 MB (1194727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fd4ded7f9b335bf1e38fb77666df40bbb5e7ad13919a1f0bb38b0559d0f647`  
		Last Modified: Thu, 17 Mar 2022 17:56:25 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fb0cb8baa674f9e3a9f66bf79dbd36c3648b52b3ca1e3ed9e797c1dc823874`  
		Last Modified: Thu, 17 Mar 2022 17:56:25 GMT  
		Size: 5.6 KB (5586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f1661d016f7096059229cc52c1255520d7907cd33b9e495c2b05b916764bf3`  
		Last Modified: Thu, 17 Mar 2022 17:56:50 GMT  
		Size: 37.3 MB (37341421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e45ab9fb2ad90a1c76f6ab991ad044f24b29e80656aad44187058e0fae236e5`  
		Last Modified: Thu, 17 Mar 2022 17:56:24 GMT  
		Size: 8.3 KB (8329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be93588a3028fe558f55c9d68a9b18597adc1e045fb6bd43634a4a817730d8e`  
		Last Modified: Thu, 17 Mar 2022 17:56:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc80bb685fbfd67de63d70b441edea8608873df8ff88267664ddcb6eb785db7e`  
		Last Modified: Thu, 17 Mar 2022 17:56:23 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657bd5c85cd3b8f65497ae0562ae91fdc9d930d74a09199b279a2d095d17f2ef`  
		Last Modified: Thu, 17 Mar 2022 17:56:24 GMT  
		Size: 4.7 KB (4705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-stretch` - linux; arm variant v7

```console
$ docker pull postgres@sha256:39a9cfdfbfa9218a8c7ab3efa7323b00b4f8fdee9e73f38b5d1b09c964800912
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68119586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debf634c98a6a6dc713be42f8018fce5de9dc7fa6949cc48f193297eb720774b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 17 Mar 2022 09:36:59 GMT
ADD file:28d5a216145f4b0aa29a7151a22e6e7dab9d430006122bbed8b13f84ae55713e in / 
# Thu, 17 Mar 2022 09:37:00 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 10:07:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 10:07:21 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 18 Mar 2022 10:07:21 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 10:07:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 10:08:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 18 Mar 2022 10:08:06 GMT
ENV LANG=en_US.utf8
# Fri, 18 Mar 2022 10:08:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 10:08:18 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 10:08:33 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 10:08:33 GMT
ENV PG_MAJOR=11
# Fri, 18 Mar 2022 10:08:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Fri, 18 Mar 2022 10:08:34 GMT
ENV PG_VERSION=11.15-1.pgdg90+1
# Fri, 18 Mar 2022 10:32:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			apt-get install -y --no-install-recommends clang-6.0; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 18 Mar 2022 10:32:10 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 18 Mar 2022 10:32:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 18 Mar 2022 10:32:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 18 Mar 2022 10:32:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 18 Mar 2022 10:32:14 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 18 Mar 2022 10:32:15 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Fri, 18 Mar 2022 10:32:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 10:32:16 GMT
STOPSIGNAL SIGINT
# Fri, 18 Mar 2022 10:32:16 GMT
EXPOSE 5432
# Fri, 18 Mar 2022 10:32:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:db6b474f79893f85b457aa5924e44453557a4b8963f5dbf6f78a60f93f73d19d`  
		Last Modified: Thu, 17 Mar 2022 09:53:37 GMT  
		Size: 19.4 MB (19359700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba8744cbc8392d85ecedae091877918dc81688523278005a38a1721d7677453f`  
		Last Modified: Fri, 18 Mar 2022 11:39:01 GMT  
		Size: 3.9 MB (3875785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020d263cd8c5d1673b486272bf93e3965e9d4b39f287dd9c102c4bc42d38f719`  
		Last Modified: Fri, 18 Mar 2022 11:38:58 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e97297dd1c9d3cf3c51b4665109c2e638a11b6cb5baf6c0a7eeb80e21cdf1ca`  
		Last Modified: Fri, 18 Mar 2022 11:38:59 GMT  
		Size: 1.3 MB (1336161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fced99d680a659b2543547aefa5f51493ef545ce6e4c9b9668c53a8ed2452a5`  
		Last Modified: Fri, 18 Mar 2022 11:39:01 GMT  
		Size: 6.2 MB (6185923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1aa013fb40309b63aa11be448d449574344ec2c75b02d709e649f158f0a7999`  
		Last Modified: Fri, 18 Mar 2022 11:38:57 GMT  
		Size: 1.1 MB (1097064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab40da3474c99afbe0b60bba9f549f47b9dcf079737da6f20dba8a97a6f95d1`  
		Last Modified: Fri, 18 Mar 2022 11:38:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d2060c23b05f37b8cd8a2b7cfe626105bd62c5a5488a2223951ba248169ee6`  
		Last Modified: Fri, 18 Mar 2022 11:38:56 GMT  
		Size: 5.6 KB (5582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce6fcc994efdaf20d71e4eb1c75d3b1eeaf281c70608ede70b42b8c6252b79c`  
		Last Modified: Fri, 18 Mar 2022 11:39:18 GMT  
		Size: 36.2 MB (36244049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dafc5c7ea735c0851c6f3948d72fc3867145e63e13d83c8f53a8c55c617bce`  
		Last Modified: Fri, 18 Mar 2022 11:38:54 GMT  
		Size: 8.3 KB (8333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6956e5825f87e97b598a74d342ada9fac0f43b84d5ed91cc26c67ea016fed799`  
		Last Modified: Fri, 18 Mar 2022 11:38:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36db73b1cd665c156d55cb76e5b3fdf81e87d7b58b40eac53a9a98b7215599fc`  
		Last Modified: Fri, 18 Mar 2022 11:38:55 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77282008f63e57591b87a16b9add58b355669c667a9f50ff39b6e7992e88229`  
		Last Modified: Fri, 18 Mar 2022 11:38:54 GMT  
		Size: 4.7 KB (4708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-stretch` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:2d07cb937fcd5f9c0544333ed5f1c513a7ae2b13cb9645c8c4bd621957dbb5a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70451622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c13ccc7fcdc8f50a3e78349232df2feca9daec722e85af134a8b0a73afe9c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 17 Mar 2022 03:24:16 GMT
ADD file:9d9c04bf28d7e6075270ca8a75c01a6d4015bc3eccc4812a82681a7fabf27027 in / 
# Thu, 17 Mar 2022 03:24:17 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:59:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 18:59:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 17 Mar 2022 18:59:15 GMT
ENV GOSU_VERSION=1.14
# Thu, 17 Mar 2022 18:59:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 17 Mar 2022 18:59:34 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 17 Mar 2022 18:59:35 GMT
ENV LANG=en_US.utf8
# Thu, 17 Mar 2022 18:59:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:59:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 17 Mar 2022 19:00:31 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 17 Mar 2022 19:00:32 GMT
ENV PG_MAJOR=11
# Thu, 17 Mar 2022 19:00:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 17 Mar 2022 19:00:34 GMT
ENV PG_VERSION=11.15-1.pgdg90+1
# Thu, 17 Mar 2022 19:09:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			apt-get install -y --no-install-recommends clang-6.0; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 17 Mar 2022 19:09:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 17 Mar 2022 19:09:57 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 17 Mar 2022 19:09:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 17 Mar 2022 19:09:59 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 17 Mar 2022 19:10:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 17 Mar 2022 19:10:02 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Thu, 17 Mar 2022 19:10:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 19:10:03 GMT
STOPSIGNAL SIGINT
# Thu, 17 Mar 2022 19:10:04 GMT
EXPOSE 5432
# Thu, 17 Mar 2022 19:10:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ecb1e7e01fa06e43b3018b38895366ba643cbac6d46bce566be2aa1cf10abf48`  
		Last Modified: Thu, 17 Mar 2022 03:32:58 GMT  
		Size: 20.4 MB (20423817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b507adb4d135dc5cade1091ae2c1d5e0a65d2f7d5975a6ef73bba658fba43`  
		Last Modified: Thu, 17 Mar 2022 19:31:34 GMT  
		Size: 3.9 MB (3891033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0f84e77a479d8de4a473c06b1c096a1ae44e1dceeba23524faeb087a7d3eb6`  
		Last Modified: Thu, 17 Mar 2022 19:31:33 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9611137c0fc9123fb76274364f34b5926d1879fd7af42ac9de5e36dbb5e962a`  
		Last Modified: Thu, 17 Mar 2022 19:31:34 GMT  
		Size: 1.3 MB (1307945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d825cd14160e8780d38a5ffc01d371bc5d43e77947a44de60248de1eb897ef`  
		Last Modified: Thu, 17 Mar 2022 19:31:32 GMT  
		Size: 6.2 MB (6182618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e19dab4d3750006de249bb9fe612c21f5e903acee9c4697794f8862d2ae1e1`  
		Last Modified: Thu, 17 Mar 2022 19:31:31 GMT  
		Size: 1.0 MB (1007497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b75513c9946b7cddb0fff41be4ff556ddb4c2d1032cd62a5a39ddda45d7eb05`  
		Last Modified: Thu, 17 Mar 2022 19:31:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e59a801df16eb75917a145949f981e0618c7bab533cdee4f86b0cf7df5bc835`  
		Last Modified: Thu, 17 Mar 2022 19:31:31 GMT  
		Size: 5.5 KB (5528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d2cc4816aae9478d6e3f06ca46fac87cb0bd91cb8e026bc20329d96e2aca00`  
		Last Modified: Thu, 17 Mar 2022 19:31:35 GMT  
		Size: 37.6 MB (37618082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3889b3c2d38b9258583bb6ccaa4f64190ce80a92b99c70220ed2cebd60f8b3f`  
		Last Modified: Thu, 17 Mar 2022 19:31:29 GMT  
		Size: 8.3 KB (8321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607d2107731364a6a3e86fc9da5621bb3ab3bf4e755e0cc3ec41e0ce1981cb72`  
		Last Modified: Thu, 17 Mar 2022 19:31:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459765d59b9d86b71721d451b19375cc57c0be1b2ed842a8cfc4873da0c382a7`  
		Last Modified: Thu, 17 Mar 2022 19:31:29 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367f787f6a5282992cdd00ec7ed61a4f01f4592ba26f7ce58ae02ffd9f1568ed`  
		Last Modified: Thu, 17 Mar 2022 19:31:29 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-stretch` - linux; 386

```console
$ docker pull postgres@sha256:86c9f85351a8d53a681428a5c2a82954214c797937ed4376ac07e649757ddca6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110875649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce2827186698c9cc1823e7b7f850411d32f4282e48988cba7f0b53ba9a403b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 17 Mar 2022 08:18:48 GMT
ADD file:abf7cf9a26b74977f09b90970656abfd411f0cff78c328ac90ea7b8cc502d164 in / 
# Thu, 17 Mar 2022 08:18:49 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:49:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 18:49:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 17 Mar 2022 18:49:27 GMT
ENV GOSU_VERSION=1.14
# Thu, 17 Mar 2022 18:49:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 17 Mar 2022 18:49:58 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 17 Mar 2022 18:49:59 GMT
ENV LANG=en_US.utf8
# Thu, 17 Mar 2022 18:50:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:50:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 17 Mar 2022 18:50:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 17 Mar 2022 18:50:44 GMT
ENV PG_MAJOR=11
# Thu, 17 Mar 2022 18:50:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Thu, 17 Mar 2022 18:50:44 GMT
ENV PG_VERSION=11.15-1.pgdg90+1
# Thu, 17 Mar 2022 18:51:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						echo 'deb http://deb.debian.org/debian stretch-backports main' >> /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			apt-get install -y --no-install-recommends clang-6.0; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 17 Mar 2022 18:51:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 17 Mar 2022 18:51:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 17 Mar 2022 18:51:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 17 Mar 2022 18:51:16 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 17 Mar 2022 18:51:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 17 Mar 2022 18:51:16 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Thu, 17 Mar 2022 18:51:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 18:51:16 GMT
STOPSIGNAL SIGINT
# Thu, 17 Mar 2022 18:51:16 GMT
EXPOSE 5432
# Thu, 17 Mar 2022 18:51:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0adcdf5d0277dbd78b125a01b32b506f2690141e1c80d0bc171467a2dbcf51fc`  
		Last Modified: Thu, 17 Mar 2022 08:28:53 GMT  
		Size: 23.2 MB (23202853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2176987f4b9c0d08a78fe73b840024f7a974e0c92ba6bd7899eb76e502f40`  
		Last Modified: Thu, 17 Mar 2022 19:24:20 GMT  
		Size: 4.8 MB (4812293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d88782309bcfc834761596bb9201907034f27ba95ae04454d4409f6f9d7d7cc`  
		Last Modified: Thu, 17 Mar 2022 19:24:16 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6c4297317c86fa156921cf87c5e779856159ad9f6d81d952eb5a080eaba25c`  
		Last Modified: Thu, 17 Mar 2022 19:24:17 GMT  
		Size: 1.3 MB (1347447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d356f5d4bd1b8b075531aac0a01b75f86952408c8f44dc93bd27553872391c4a`  
		Last Modified: Thu, 17 Mar 2022 19:24:18 GMT  
		Size: 6.2 MB (6185801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e587b8036d253b12a8053630e6ce978fd083808cd75e2e217308003486041f`  
		Last Modified: Thu, 17 Mar 2022 19:24:15 GMT  
		Size: 1.2 MB (1234552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1e29a94ce7e78a366fba08fe80df800d40fc46a4d12e34f4b6eba338cd8f37`  
		Last Modified: Thu, 17 Mar 2022 19:24:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b877428f0cb78f0b60b8aa46fb469b64ad067303dcf2f486811f943060eb8a`  
		Last Modified: Thu, 17 Mar 2022 19:24:14 GMT  
		Size: 5.6 KB (5586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0790f9868f9db00b2f1598e2c39b5c0cbd1791bfbb50fdfb600b0db621cd5ee6`  
		Last Modified: Thu, 17 Mar 2022 19:24:37 GMT  
		Size: 74.1 MB (74071810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8aca19d7f7cb2d73dc69aa8ff64ccfffd39241e35fdc4ba7d6770573c4297db`  
		Last Modified: Thu, 17 Mar 2022 19:24:12 GMT  
		Size: 8.3 KB (8326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4da62f779ff9df593da90a5053addf9c9b562448ec058e3d1be0cf9a4868487`  
		Last Modified: Thu, 17 Mar 2022 19:24:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4856d8c57692b45b4fe6394728bae448e08f6f5fa5db0d538fce049a89054157`  
		Last Modified: Thu, 17 Mar 2022 19:24:12 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59fbca39e3973163558f252ad99d115a07489167432ff81fbde8176b736e136`  
		Last Modified: Thu, 17 Mar 2022 19:24:11 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
