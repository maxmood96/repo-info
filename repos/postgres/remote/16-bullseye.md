## `postgres:16-bullseye`

```console
$ docker pull postgres@sha256:fd9ad3ea7ad76ce6014a870e4ec221f447194207cb3205ca25c5bd0909cb0a05
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

### `postgres:16-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:e07f542bafb5c272aa2d2fc478b942fb33acb5f0db9e8f33bee15cc2340af951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140902333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8544b0be4341a01f22d13109b783d64e66c00e80edaa196705e103f9c68786f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 20:04:26 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_MAJOR=16
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_VERSION=16.1-1.pgdg110+1
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 20:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 20:04:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 20:04:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbaf8af64e47e50b7aea4e4cd062f2f60ae3b067d5206777246da9a05be52c8`  
		Last Modified: Tue, 21 Nov 2023 06:17:34 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6286d55597f308dc85177b63344ca4566ff163fa4e4e3f44300180bce2d2f5`  
		Last Modified: Tue, 21 Nov 2023 06:17:38 GMT  
		Size: 4.2 MB (4207532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c5d80b4608b42a71ac111c3f981421fbc5b4d2c8c501446ff2fd0f097337e5`  
		Last Modified: Tue, 21 Nov 2023 06:17:38 GMT  
		Size: 1.5 MB (1472439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e7696bb91e97e0f9327994d7addfe81bb3a954d13c725ac7407fe34edbcf5f`  
		Last Modified: Tue, 21 Nov 2023 06:17:38 GMT  
		Size: 8.0 MB (8045284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6928bef9d88b28062337f8a158c9d1ae84e5c7e5a526478262f37147b2b402`  
		Last Modified: Tue, 21 Nov 2023 06:17:38 GMT  
		Size: 1.0 MB (1037449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280a879c7b48550cb7a7566a1d089e859f235b8630367324d75871022b8ae5b6`  
		Last Modified: Tue, 21 Nov 2023 06:17:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef1fd16e4e00771c5d7311198c54877ffd233228f81ddcde5c0368d4601d80c`  
		Last Modified: Tue, 21 Nov 2023 06:17:39 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc94a2d77b8577adfb3d690b41e28cb9deeb6d2e7ff899ffb40a54307215fd4f`  
		Last Modified: Tue, 21 Nov 2023 06:17:42 GMT  
		Size: 94.7 MB (94701858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d96bff01f9bc4a4bc84fee9725363a08d047c66a95b3a71ae55db3dc7b7eb67`  
		Last Modified: Tue, 21 Nov 2023 06:17:39 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e0a6b1ea2c352ea3b19ecd351c0aa05f19cc7d942dde5eeb9341d38b0ba6e8`  
		Last Modified: Tue, 21 Nov 2023 06:17:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb810adeff4a704b7a69d49c6b65d5571b432b4e0a8751db105f127e0bd0099`  
		Last Modified: Tue, 21 Nov 2023 06:17:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61169ef5a86ed53b9a4c5e259debc05da55cda0d4feba26fc4ef3ae8a64aa1a6`  
		Last Modified: Tue, 21 Nov 2023 06:17:40 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:adf5d75008decdc6414b9ab06b8bd44022ec6660c60f57187debd9c98717e32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5107208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ec75c6dfe1be535dabc1dd840932d0cf9bf788301605baa1e35f2e3052a926`

```dockerfile
```

-	Layers:
	-	`sha256:60c38ae79972b53090694c30c1248b28b0b7ae025074ba521e28aab2747e646e`  
		Last Modified: Tue, 21 Nov 2023 06:17:38 GMT  
		Size: 5.1 MB (5056878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dbf7117a74b1e9a030d49e9b92429c8072972cc77b2492ecb366f3710c9c1da`  
		Last Modified: Tue, 21 Nov 2023 06:17:38 GMT  
		Size: 50.3 KB (50330 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:f8ddc33f1252653fd19da8f28e2f6d6c9e5906efea2ec4d1bb6d7e55b103f4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134174862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171f44fe2f1c05b59c92cbfb0aa8e74c60bb7d3f64448027f082deb7d276cf6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 20:04:26 GMT
ADD file:f7d1d017cc4e588f213f4536967b8d58c50b8602fb8a10b786856c35a843f31e in / 
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_MAJOR=16
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_VERSION=16.1-1.pgdg110+1
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 20:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 20:04:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 20:04:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d051266714ac5508b442ebbe5911d353bfacddc64f657eeba14a993cced96358`  
		Last Modified: Tue, 21 Nov 2023 05:04:38 GMT  
		Size: 28.9 MB (28921267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ece1beb92cce2ac06ca58cdf90840eefcd484ca3a322e1ede41adbd2aa5af81`  
		Last Modified: Tue, 21 Nov 2023 20:02:31 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b626f1f20e2d8180138b585029d4c234ef8f68fce1ea4de209c15160a571570`  
		Last Modified: Tue, 21 Nov 2023 20:02:31 GMT  
		Size: 3.9 MB (3889265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848c2a7661551b2883b51208a362b26b127489d0d144f9726925dfcb6c8f296c`  
		Last Modified: Tue, 21 Nov 2023 20:02:31 GMT  
		Size: 1.4 MB (1449946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa10149f3fedf3623013ea4617c0347bf1d5e1018a20c3acb3089fe3f16c201`  
		Last Modified: Tue, 21 Nov 2023 20:02:33 GMT  
		Size: 8.0 MB (8045273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f01ea795e7f5f05e14920788c8357f1db83187f8933ca15bf4b6818312e40b`  
		Last Modified: Tue, 21 Nov 2023 20:02:33 GMT  
		Size: 1.0 MB (1033914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a65ccf4e087845b4aaf62c24b518eb775f6e8ab3080d62030cde1e5890bf51e`  
		Last Modified: Tue, 21 Nov 2023 20:02:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0f312b2560772e07297fec490d54bb2c01a653ed43b44a32d9845e7993b5c7`  
		Last Modified: Tue, 21 Nov 2023 20:02:33 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450d8d97e6d18d3d32494620ee43ea927dc68b30e5175c14a1b55a9c7360b657`  
		Last Modified: Tue, 21 Nov 2023 20:02:37 GMT  
		Size: 90.8 MB (90815249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744a9c29c2e80332696fc478600b773f3b491ee420096326335fb79dfd43ed30`  
		Last Modified: Tue, 21 Nov 2023 20:02:34 GMT  
		Size: 9.9 KB (9928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43e57816c540464d72c85b1b729457396fc8d108dde2f79e3b80edbfaaa165b`  
		Last Modified: Tue, 21 Nov 2023 20:02:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d38f51f2d54e252498e12a2a1ab4197abf9e3921ada20249713f6fc2bd18cf`  
		Last Modified: Tue, 21 Nov 2023 20:02:34 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e9cb614b7500d8c8023f84a7dd4d44ae8ca59fe0d9d5cee1512771fd37f31b`  
		Last Modified: Tue, 21 Nov 2023 20:02:35 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2aa6ee2a52afa3f67a89cf8577bdaaad75f3adf4cf593e442158ea552859b21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 KB (50307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c42ba99b8ca4f718f929e6e3863fcb3b8ae441802cea23da04951784546e40`

```dockerfile
```

-	Layers:
	-	`sha256:7c6224e0879367694f9768ddadac0081d78d65a062fb5de3864ed16b72ae9e53`  
		Last Modified: Tue, 21 Nov 2023 20:02:31 GMT  
		Size: 50.3 KB (50307 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:42eaa8fe412f6334a541511482f746bb41f20225a952b4ffc002abc0b0de86d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128797534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a2d125b6f9b26513f859f0ad752917a33eb753056ab74a6e665e3571551758`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 20:04:26 GMT
ADD file:c4afced274aaa80ab3018b368ed739c1c55e49b41e9637ac44d63e61344fe865 in / 
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_MAJOR=16
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_VERSION=16.1-1.pgdg110+1
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 20:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 20:04:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 20:04:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6dc4ed5513793308b8e30b08e03f97fa54025c3d3f3172c6edccb1dbbc7ff139`  
		Last Modified: Tue, 21 Nov 2023 04:02:35 GMT  
		Size: 26.6 MB (26579014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cc7941b400f3bf57e88ca53cd8f503b865c5758c4a78c8b4c7a8e328530196`  
		Last Modified: Wed, 22 Nov 2023 01:48:04 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4a88703271fa81c161e06205d8313b2f8f0af319f9e0b3ad8c61257ecf43a8`  
		Last Modified: Wed, 22 Nov 2023 01:48:05 GMT  
		Size: 3.5 MB (3509868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a39292d0ae527985471598a74ca795bbde210667b000f267cd16afcf4db4df`  
		Last Modified: Wed, 22 Nov 2023 01:48:05 GMT  
		Size: 1.4 MB (1440036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9409bab78ee01b73d472aa8b928ed37ba03e08bb0b9a13dea577c13c60654b`  
		Last Modified: Wed, 22 Nov 2023 01:48:07 GMT  
		Size: 8.0 MB (8045202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22395ce5acb8645b4427e09aae3b58c5cc849b5d6a5a2a825396e15ac23a11d2`  
		Last Modified: Wed, 22 Nov 2023 01:48:06 GMT  
		Size: 907.8 KB (907774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681b290bd10a5aa1e8c51ba74de59868cb4d847b7e121c7b9363e822124e4772`  
		Last Modified: Wed, 22 Nov 2023 01:48:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dca2bf4cee3e9a783c855ca659a8048dcfcd8982a97eaa0f090e14a1ba182c`  
		Last Modified: Wed, 22 Nov 2023 01:48:06 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09b9c49a62052e3b76d5b8a4ae194131043dc0b39861fa9d0949787dc2106f6`  
		Last Modified: Wed, 22 Nov 2023 01:48:10 GMT  
		Size: 88.3 MB (88295692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943db2cef4ce3f9869e120e2bced2023e3bc00ec1d5753d089dbcb3021e86a36`  
		Last Modified: Wed, 22 Nov 2023 01:48:07 GMT  
		Size: 9.9 KB (9930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6fed8025f0faa28499cda686b26433e410a7449b05a887a8d1dd248fe17711`  
		Last Modified: Wed, 22 Nov 2023 01:48:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95bdbaf989dc40a385e34bb787a52b063d6ebe9837a87597aca16d58c1049f5e`  
		Last Modified: Wed, 22 Nov 2023 01:48:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecd59e99ec503e5d10e70621f88d3d44cf6bcf6356021f073248363b96f6935`  
		Last Modified: Wed, 22 Nov 2023 01:48:08 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:26e0d829301d3f5abb87cde7e20f46d0d9e4153ec7ea61b1dd10785d16ae2c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eeeb31a91f57564b8aa9206f71387f05df2acacde0722483ac8be2bbfd2fea`

```dockerfile
```

-	Layers:
	-	`sha256:66750e92848f097ba05d6be29ac4946b8534ea30dba2e0acbd3316cbcb9008fd`  
		Last Modified: Wed, 22 Nov 2023 01:48:05 GMT  
		Size: 5.1 MB (5072380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35c2a3cebb6af9444cb6eed55559eadac5e44d6fe63aa26cd1ace9dcacc07df2`  
		Last Modified: Wed, 22 Nov 2023 01:48:04 GMT  
		Size: 50.3 KB (50347 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:bfa9d9e9a1b40d646fd20a0f0ee87ecaee5c150d07e0fd9fa7356e093a28eb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135952695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b25837a6866da7e8a5f35c77ee227a69accb5789cd5d172ab93dd11bff7ba1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 20:04:26 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_MAJOR=16
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_VERSION=16.1-1.pgdg110+1
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 20:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 20:04:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 20:04:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d499610b7b67a680fc82a27625cc3960384326345a873ab3729091fde96c2d4`  
		Last Modified: Wed, 22 Nov 2023 11:52:59 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b9d08385de13134ad8df9d9c5a6603d462b4040c8aed8a540ce5c6bbea37e8`  
		Last Modified: Wed, 22 Nov 2023 11:53:00 GMT  
		Size: 4.2 MB (4209368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd9b1488b80fd9988b0d188f94dbfb975e022a376c386cb265ffe5c3b768bdf`  
		Last Modified: Wed, 22 Nov 2023 11:53:00 GMT  
		Size: 1.4 MB (1404352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05093a7fd59075e84a24aa46c2310864ff48fd4dd26e8257c36529acd6f93514`  
		Last Modified: Wed, 22 Nov 2023 11:53:00 GMT  
		Size: 8.0 MB (8045185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6e913704ba9c6cb18a563dc9c85e201f5cf9c09dfe06f2c1532537258b76e9`  
		Last Modified: Wed, 22 Nov 2023 11:53:01 GMT  
		Size: 1.0 MB (1025874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fcd4f567dd99db4cd906a4ef25247ec80783aeacd0b6482f58884caebadfda`  
		Last Modified: Wed, 22 Nov 2023 11:53:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda47adbeb1f61f09d98831d05acf423d1d07ddb6ec1677bfe37ab19c5c07e0d`  
		Last Modified: Wed, 22 Nov 2023 11:53:01 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6bcc06fc9b6c5f1d8b1e71cac3b039b48fd6edb261ae35043be56262ba75ea`  
		Last Modified: Wed, 22 Nov 2023 11:53:04 GMT  
		Size: 91.2 MB (91183846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7094e7c01c6abbea590aa15a6bbae11e7d689287089acc65c3901ff7596ce39a`  
		Last Modified: Wed, 22 Nov 2023 11:53:02 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fc707dc1fb4704ec3e02f6cdfa9e7feb9ee71d342c2cdd3e087a8886127fd7`  
		Last Modified: Wed, 22 Nov 2023 11:53:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1680267eabdcc344649ed97b13ffaf7c3e9b84560352add45ce5cec840210eaa`  
		Last Modified: Wed, 22 Nov 2023 11:53:02 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6947bb3f9997c306744bd6ae4b640b44963516d68907d780c3644105479cd526`  
		Last Modified: Wed, 22 Nov 2023 11:53:06 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:01dd82959d22c7df15e2dfbddc3335bfbf0d83fe8df639fdd6b7c90bdd69d100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5112682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324053197571685679bde02d5237cb07f3a1ffce9d51a817f73663e87425602e`

```dockerfile
```

-	Layers:
	-	`sha256:649524ed42fa0463b1d3684173db97e8d22752b46312ca1a531cb0217f52ed77`  
		Last Modified: Wed, 22 Nov 2023 11:53:00 GMT  
		Size: 5.1 MB (5062511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b5025cb913945e1ace00397d81156545a5ed271aeb3dec95aefda5817ace6f`  
		Last Modified: Wed, 22 Nov 2023 11:52:59 GMT  
		Size: 50.2 KB (50171 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:1698f2bead876fcdb438354c55185dfdecb3a7aa29a6069b1fe95822bf3dcf50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142886337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676cab4c819b6e27db1c5076e4f92a07e80750f77d55af8681d4da6770041c29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 14 Sep 2023 18:21:14 GMT
ADD file:67f223c9c48e525a23fb110e4c105d7128dcac0c10f32c38f98ea84a21d2bd00 in / 
# Thu, 14 Sep 2023 18:21:14 GMT
CMD ["bash"]
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV GOSU_VERSION=1.16
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV LANG=en_US.utf8
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_MAJOR=16
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PG_VERSION=16.0-1.pgdg110+1
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Sep 2023 18:21:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Sep 2023 18:21:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 Sep 2023 18:21:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Sep 2023 18:21:14 GMT
STOPSIGNAL SIGINT
# Thu, 14 Sep 2023 18:21:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Sep 2023 18:21:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bc6810e8fe9346a3caaff984163b789d12b6964a15a2029e384143ca19fef5ad`  
		Last Modified: Wed, 01 Nov 2023 00:44:14 GMT  
		Size: 32.4 MB (32402692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23306281a2cdffb2de89bd9b137734ec646220e349b031c12194f3d77149bdae`  
		Last Modified: Wed, 01 Nov 2023 01:14:59 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7351e0403afe83c86309a164951679e13208aa6cd94a8557b3c2b8d5044bfa9`  
		Last Modified: Wed, 01 Nov 2023 01:15:00 GMT  
		Size: 4.6 MB (4607375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dffd744f9d1cfdd42912ef066f490e2539cc902c151e4e52a821de4b178ecd`  
		Last Modified: Wed, 01 Nov 2023 01:15:00 GMT  
		Size: 1.4 MB (1448282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69526fffd3df9e8a80cdf077a053e45f638617847cbe2d01246ba6c10e23278b`  
		Last Modified: Wed, 01 Nov 2023 01:15:01 GMT  
		Size: 8.0 MB (8045166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdc4086030cd6887fa8874e1007a90c296cb8c0b5e329768fda86fbf19f1f68`  
		Last Modified: Wed, 01 Nov 2023 01:15:01 GMT  
		Size: 1.0 MB (1027952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a197f693be01a0c10ebd64189cfbb41a534e262fe0c834e7255977ae3d9dd4`  
		Last Modified: Wed, 01 Nov 2023 01:15:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02fceffae3e196c62776b62f1da2cdc3ef2dda3b4ea74ad0e6577c81a932944e`  
		Last Modified: Wed, 01 Nov 2023 01:15:02 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede476d15a776bfd3aff3d6a810d5302abb28d1dc0a87530195f495be46873f3`  
		Last Modified: Wed, 01 Nov 2023 01:15:09 GMT  
		Size: 95.3 MB (95334933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12a75d62d18eb5a01185bd78a2b455697be8e95373a994d9d5fc109d197cd4f`  
		Last Modified: Wed, 01 Nov 2023 01:15:03 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcedbf168bcd33aa7128c1607b88c577bd990f84cd03ecaa7370e8f13be6fd8`  
		Last Modified: Wed, 01 Nov 2023 01:15:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c265e15b8dad90d6b1335bb0e3b43764b5c2f3392aee04d004a6253ad0f9152`  
		Last Modified: Wed, 01 Nov 2023 01:15:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f0e2624910175eb26899420a601a9ba9255d7655fe52077af7c72fc7535b02`  
		Last Modified: Wed, 01 Nov 2023 01:15:05 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:a5b3fef662360cce72935289e2c7dc65d0ddad8444939f1c15e1a6d0a9532366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 KB (50071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfe48e9cea51f51a9defe78061da31a60912c5de7d8d7360bf0c261665e918e`

```dockerfile
```

-	Layers:
	-	`sha256:babee0b02804630795680b9a070d8f529393fab90929f762a6c0f5c31c12b200`  
		Last Modified: Wed, 01 Nov 2023 01:14:59 GMT  
		Size: 50.1 KB (50071 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:3557630027da22ea4af95f9bccc93157baad1d7956bb0ff3dc8a132f663df680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135691685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4292b5eb5ec9cd56f21ae953aa55458f8b6ca3c01858880c2ad9d547fc5234`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 20:04:26 GMT
ADD file:09d1c4f0f5b78b81f635498ee58f6ab1843bca8a18549ecc39686f1c60b1951d in / 
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_MAJOR=16
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_VERSION=16.1-1.pgdg110+1
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 20:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 20:04:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 20:04:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a157b7f5d72df9473d33b22278cb42e4e06e22b99ac1864b7b586f36671f15bb`  
		Last Modified: Tue, 21 Nov 2023 04:22:02 GMT  
		Size: 29.6 MB (29636034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785f51b53d1db400472f15ec096a7ee4b64d3c08b994759b18049124438c4010`  
		Last Modified: Thu, 23 Nov 2023 03:33:57 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3778165671f234b7363ec027202183f74d772e1950d82cc3f6278f678dee79d8`  
		Last Modified: Thu, 23 Nov 2023 03:33:57 GMT  
		Size: 4.2 MB (4196358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ffc22c0ea9927329be3519bab2180352190f8f23bd689c2bf7ae7728a4b58d`  
		Last Modified: Thu, 23 Nov 2023 03:33:57 GMT  
		Size: 1.4 MB (1360004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06695751e19c683fa07fd1965155895afddce123ca9e7c3692385a156fed23f`  
		Last Modified: Thu, 23 Nov 2023 03:33:58 GMT  
		Size: 8.0 MB (8045542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edf0bee40de56418f9a87800e244e08967f4a60cb290bafe31b3a6dda9924f1`  
		Last Modified: Thu, 23 Nov 2023 03:33:58 GMT  
		Size: 1.1 MB (1089550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4184426f7fc37d1def27fcf0df1f7857cfc9719ef315d62071070a32836371e`  
		Last Modified: Thu, 23 Nov 2023 03:33:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d171f5a3c657f88f3ab962f218611f594098b65259f3aad13e26350d1d4be229`  
		Last Modified: Thu, 23 Nov 2023 03:33:58 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8484ff9832108685813b895c70da167fc4cff68cc9f35c87394fefdbf88c4f`  
		Last Modified: Thu, 23 Nov 2023 03:34:08 GMT  
		Size: 91.3 MB (91344232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9a8093e7cab1a70cdd642a391027be39a1f4562fb7a4a6200c4bbe1a130cb4`  
		Last Modified: Thu, 23 Nov 2023 03:33:59 GMT  
		Size: 9.9 KB (9932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586418b6a59b624f2414c6c3b8d7a89cfdc2a54acbda85e6b5531c839ead934`  
		Last Modified: Thu, 23 Nov 2023 03:34:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1b761fbc87720be88cb58e49bd540b8e3196ec0c9538e65af242600d3c510b`  
		Last Modified: Thu, 23 Nov 2023 03:33:59 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af24d4b72ac50f3bb29c22113e48a06ae79c33a22f7413b3a5793b9cc57fea87`  
		Last Modified: Thu, 23 Nov 2023 03:34:00 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:96de802e278807663a00321f257cde50398fab47df43f8837f41a42c31144989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 KB (50193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075f6b0c5d53da3f90b68966cc0cda83d07528cf9e1afc49df3191e34f5d8473`

```dockerfile
```

-	Layers:
	-	`sha256:1cc738f485aae225e1e6178f0318c810795611c16dfb25c4b869281b00b60982`  
		Last Modified: Thu, 23 Nov 2023 03:33:57 GMT  
		Size: 50.2 KB (50193 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:34a1f62c8cd9738b8cc9f6a2bca24c74e5f36841003e3a7633257803f0ef2f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150015216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749cebe7a7b68e6057468adee83373b088f4e7efda9aa70912b450ac708dec2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 20:04:26 GMT
ADD file:b0d18f2d04821eb50d1faecc1a64916f5c63dd386ae71a3b2cb1d6c4aac6e1c4 in / 
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_MAJOR=16
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_VERSION=16.1-1.pgdg110+1
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 20:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 20:04:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 20:04:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:60239a74847cd7e9a928353188f3cf096ca8cf648e2b27c765058e169d568fd9`  
		Last Modified: Tue, 21 Nov 2023 04:29:47 GMT  
		Size: 35.3 MB (35293727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16de6da61666e950a5b7b529f3038a00b9f2c676c778ce6877c9554fdd36857c`  
		Last Modified: Tue, 21 Nov 2023 23:56:59 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c98567766a405ce84a0be0e02e7cf9914d6d4691dffc5496c760a347867228`  
		Last Modified: Tue, 21 Nov 2023 23:56:59 GMT  
		Size: 5.0 MB (5015948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c61a8652eea248c5219212393f2a552f9493c1642d9219671579c1ee733f77d`  
		Last Modified: Tue, 21 Nov 2023 23:56:59 GMT  
		Size: 1.4 MB (1394026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdb4e3c161d5532d076597f8745f34a6f37d4c07e3b0e6b813a8739f23e1417`  
		Last Modified: Tue, 21 Nov 2023 23:57:00 GMT  
		Size: 8.0 MB (8045122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02ed0182f1b78eec622706c1ce7e2e3a5db1a8ff2f9e72219ed5427a3cfa888`  
		Last Modified: Tue, 21 Nov 2023 23:57:00 GMT  
		Size: 1.2 MB (1196901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4862e5122b808ebe059b3ed3a9d62dbbcfcfd0a4ee79f3185115cb2be9eb5889`  
		Last Modified: Tue, 21 Nov 2023 23:57:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f110a1ad0cf91d66fa9f7495dcf0d900b6a19805cca2e349d646c9211a38e3d`  
		Last Modified: Tue, 21 Nov 2023 23:57:00 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f374867146d02be17294c7bad081db5e48892db345fe9d60570b930896cbc7`  
		Last Modified: Tue, 21 Nov 2023 23:57:04 GMT  
		Size: 99.0 MB (99049540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8323d47f8509d08fb4c68e2b5203cb1189aa40ca1ee8fef577e87224c715b18d`  
		Last Modified: Tue, 21 Nov 2023 23:57:01 GMT  
		Size: 9.9 KB (9918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d1e8ff99dfcd8c7a1574206b1e4ef1084f70dd1e290093c5b954b2f4c9482d`  
		Last Modified: Tue, 21 Nov 2023 23:57:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26e5574082c14302ebb76ce54fafab3a606cf8e8b8f80828562df9b2b18a1c0`  
		Last Modified: Tue, 21 Nov 2023 23:57:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba72cf118cbcf8c4c82e67dd9ec4bb30d937e8aca374791312bf82377f33308e`  
		Last Modified: Tue, 21 Nov 2023 23:57:02 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:80d8dd2ec3f865a19c71d3b20c567fab6e3a67be3ed47aab3d5b8805cfd2ac87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5114233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7006536b09b65689ba9aba4ca4d5f525b4c3455e4670094f270b35cf45835ae3`

```dockerfile
```

-	Layers:
	-	`sha256:ccbcc3868047998456647ff9b784569e74d392a437829e0977eb3db01a3bd9b3`  
		Last Modified: Tue, 21 Nov 2023 23:56:59 GMT  
		Size: 5.1 MB (5064018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51aedbf8252f804394f76cad7bc3464242ce08f2b6f9f176fdcf1535b16d05b3`  
		Last Modified: Tue, 21 Nov 2023 23:56:59 GMT  
		Size: 50.2 KB (50215 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:14c38a58ee0bda3fdc978d17a93337798bcc661a75fcebb2fd89d2620f5892ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144517020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a902855bccd71e8311d40a2e4ad013e87c796083ea405180284194bda9aabd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 Nov 2023 20:04:26 GMT
ADD file:a545f27075704ce13e33e539170d3f47007424d2cc2bea5aecfd2608a5194151 in / 
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["bash"]
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV GOSU_VERSION=1.16
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV LANG=en_US.utf8
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_MAJOR=16
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PG_VERSION=16.1-1.pgdg110+1
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 Nov 2023 20:04:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 Nov 2023 20:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Nov 2023 20:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Nov 2023 20:04:26 GMT
STOPSIGNAL SIGINT
# Thu, 09 Nov 2023 20:04:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 Nov 2023 20:04:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b114072f1cab66b7376d690985b12816aebab2e4e41fc170e32f111df27951dc`  
		Last Modified: Tue, 21 Nov 2023 05:10:48 GMT  
		Size: 29.7 MB (29656938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c14abe39e5d7af1af3f169efac214a4f5188f9cf0b1eeff4aa56e29edadb83e`  
		Last Modified: Tue, 21 Nov 2023 18:48:13 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda7c74bb621b77965678f0178a83d5ab3be51a08a147477342ecbce0570474b`  
		Last Modified: Tue, 21 Nov 2023 18:48:13 GMT  
		Size: 4.1 MB (4096138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24e48d76c2c7273893bb9fdadd72210e42e08d97d83c1951ece2885024a7ddf`  
		Last Modified: Tue, 21 Nov 2023 18:48:13 GMT  
		Size: 1.4 MB (1438342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907bad315ef26db29b2f1d30476df3623e928037f4f1245879d0acefc7d51fee`  
		Last Modified: Tue, 21 Nov 2023 18:48:14 GMT  
		Size: 8.1 MB (8099088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932751c91c6f7fde288cdfb18a762883255568a6d26c4bab31952f47a2412095`  
		Last Modified: Tue, 21 Nov 2023 18:48:14 GMT  
		Size: 1.0 MB (1014332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51466198f57f994776e57e10129e6e8b2e9e80ceda50f34cfddfd8c226e6a9e1`  
		Last Modified: Tue, 21 Nov 2023 18:48:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f4ed0154dba5579cb0fe28fe0064fd32f637f29598866ce370d1f8641be866`  
		Last Modified: Tue, 21 Nov 2023 18:48:15 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b876296105858756fed4a41c5e7583b43cb5b29e165e3fe9a18feeaa9402f637`  
		Last Modified: Tue, 21 Nov 2023 18:48:17 GMT  
		Size: 100.2 MB (100192232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d7e246b0e86bfdcde3b787d3da308ffad37e76d4b5f9a4aada2623e2334b3d`  
		Last Modified: Tue, 21 Nov 2023 18:48:15 GMT  
		Size: 9.9 KB (9924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24588cf736485dc4a5c5b2089f352eef7d9237728d663884a3fc4c8981f3c38b`  
		Last Modified: Tue, 21 Nov 2023 18:48:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e30507a2fd46b32d1f3b02192087a84b56eae61ed78a9bb6b59f27beb1e7151`  
		Last Modified: Tue, 21 Nov 2023 18:48:16 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51cd50c1894a8856d351bbaf701d08627ed09610c1fdd45eb4b583c258c0657`  
		Last Modified: Tue, 21 Nov 2023 18:48:16 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2bb4db6f7a92ff17238f68d3c3d616094ab471aa85da79b7e21ab7882964dbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0665f0d152b0246001ca90e69e813cc8eceb80b225e0b471425a88e48692014c`

```dockerfile
```

-	Layers:
	-	`sha256:5d209d3c99feecae526e7689ab7e4bb1a20a836cd7cd5380a1fe525c4ab8c65a`  
		Last Modified: Tue, 21 Nov 2023 18:48:13 GMT  
		Size: 5.1 MB (5055857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1cba0b9a1eaf8f3232098ec18c907401c929e7f55c786d8a6192013de2fc467`  
		Last Modified: Tue, 21 Nov 2023 18:48:13 GMT  
		Size: 50.3 KB (50333 bytes)  
		MIME: application/vnd.in-toto+json
