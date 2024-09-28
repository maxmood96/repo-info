## `postgres:16-bookworm`

```console
$ docker pull postgres@sha256:17b6fe3a18780358f7f44a02bc21a8ef5f349aa83d8dae96d43cd168a97cf6fa
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

### `postgres:16-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:c558fefcefd412736caa046facd054b4f72f1e45b882600471af213eba46558f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153447315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2490d47edbe06d389faa29630d5d61db10610969a2fcacea017415560855a00a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22e8b34dae94f8e880f128c3c723473be89183caf3d73e23cc20bbbce703e2`  
		Last Modified: Fri, 27 Sep 2024 06:13:15 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c66a4a6b362b448ce2b2a6795bf03f009e2f529d64830ce2f82d787d5959224`  
		Last Modified: Fri, 27 Sep 2024 06:13:16 GMT  
		Size: 4.5 MB (4533671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2bf9ec3ee0e1f352f033dd61bca13e50e99b258176a04ae131a601a2c19452`  
		Last Modified: Fri, 27 Sep 2024 06:13:15 GMT  
		Size: 1.4 MB (1446662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd9cab67597b06537db781c6018bd250214f61e4a281897e508536c04111470`  
		Last Modified: Fri, 27 Sep 2024 06:13:16 GMT  
		Size: 8.1 MB (8066301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae297e90190de077d3fcad8f20dc13948d4caf08332722d778742015956d9c21`  
		Last Modified: Fri, 27 Sep 2024 06:13:16 GMT  
		Size: 1.2 MB (1196078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed09fea7e206a2a9e4f055572c36f865110e111c557c6809f82cccaadd7303c`  
		Last Modified: Fri, 27 Sep 2024 06:13:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347dc7cfffe7b23e43fe3e5572979f39e5517496cc7eedaf6a3a6444c9d05266`  
		Last Modified: Fri, 27 Sep 2024 06:13:17 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfe37b161bf143a2f3714bb4f321762547ca8041d49a953acab25c046539ba0`  
		Last Modified: Fri, 27 Sep 2024 06:13:20 GMT  
		Size: 109.1 MB (109058090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f8e4cc05d19f2cf48bb3d63d2a883a916fc9c71e5be2fc1b8fd28f58615e3`  
		Last Modified: Fri, 27 Sep 2024 06:13:17 GMT  
		Size: 9.9 KB (9915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27d51b7841cc5f7563ff25e8d4e32096fcdfc42de9e19005fc678f7bc47b450`  
		Last Modified: Fri, 27 Sep 2024 06:13:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060b2101ecb8da18bceaa6e2d4d24e8299c3abc350d717848c5e12414435009c`  
		Last Modified: Fri, 27 Sep 2024 06:13:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a098c226604097675220e04b4b4e2cfdce02cd5e56739ec9a8130caa889222`  
		Last Modified: Fri, 27 Sep 2024 06:13:18 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7dbc309f12a27b3f49524506d6af6624caf6fce027c68e520c9f61e3a1de8`  
		Last Modified: Fri, 27 Sep 2024 06:13:18 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:85d3f71ae5c7afa03708b83b72d8f97f8a42c58ec940be28e8a5122061a9fa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5805415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ba25c0f6510afb05432bdba55562034365ccabe03ef72e01b5bff62cde8daf`

```dockerfile
```

-	Layers:
	-	`sha256:bca74741b561870ffcc758e495e91c05802ba006079ba7caf20818153758aa33`  
		Last Modified: Fri, 27 Sep 2024 06:13:16 GMT  
		Size: 5.8 MB (5750983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52213e5a027c8cf20f421d90f8b6911af704f1329f28af9b089bdd48267f8c09`  
		Last Modified: Fri, 27 Sep 2024 06:13:15 GMT  
		Size: 54.4 KB (54432 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:7e0233466a3be1cd07920f99c7f17b3edc9f7405430998d1d353b301aee44568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146180710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853a86b196523db2c73970ba5aa9c227491c8b863aca174cbeed61b81108a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c6ea23909628e95a04f64c06b1b13eebd58d9f30c2461472e0fd1c95625882`  
		Last Modified: Fri, 27 Sep 2024 12:46:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cf5a39ea7a92b60bacf30a2ff06dc0257586469412c3750aa8e7e8d24013b7`  
		Last Modified: Fri, 27 Sep 2024 12:46:03 GMT  
		Size: 4.2 MB (4150914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9652982ab16c0fd7f2b19b22797765e0112bcc85ccfbce9d9c896800817166d`  
		Last Modified: Fri, 27 Sep 2024 12:46:03 GMT  
		Size: 1.4 MB (1423861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cac6f365cdea7c5c033fccf217977852d663b85fca3e0f387964725ed6eab2`  
		Last Modified: Fri, 27 Sep 2024 12:46:04 GMT  
		Size: 8.1 MB (8066414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2890a87d0918b7dc88391359a7e60e89a43b68c263899e83f0c79d285043c3d3`  
		Last Modified: Fri, 27 Sep 2024 12:46:04 GMT  
		Size: 1.2 MB (1194858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebdb5a09ccbe681815ca6e8c740383a60ade1d5ca7ccd3727470bf53d2100da`  
		Last Modified: Fri, 27 Sep 2024 12:46:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6af01088a4c63d9d24095558b1c03e9b5721fa603f3e2a2b5b9c0b1c811d312`  
		Last Modified: Fri, 27 Sep 2024 12:46:04 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3926261d26869e8914d034f1ceaeec8e5efd1c2621c8906cc2a40eb4b1d4cf1`  
		Last Modified: Fri, 27 Sep 2024 13:02:58 GMT  
		Size: 104.4 MB (104437119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa6ef5bb4c80ce3b23f2c34d73949465adc3d1bd95784c3458f0ca5ee086b00`  
		Last Modified: Fri, 27 Sep 2024 13:02:54 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad6ff2536323e383f846dcaa573fe993aca863b8cd275e673ceb4e231b2bdfc`  
		Last Modified: Fri, 27 Sep 2024 13:02:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4869c87c0398d112d918bea22443f09838e272f2e340b2e7d44ecd84989fd755`  
		Last Modified: Fri, 27 Sep 2024 13:02:54 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bfe6de3bcc8a24d68e40d28db9b66a9c17e61bd6e758281277509bb11de998`  
		Last Modified: Fri, 27 Sep 2024 13:02:55 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f767d0a2b8aebceb848070534d42ebac8c4fa08d7274665d7559275d9976b023`  
		Last Modified: Fri, 27 Sep 2024 13:02:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:06ff46898dd5dd9de85d1fa17fb201f82a54aa2d27ef62ecd3c7928ffd932f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5821195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5de5cea0ce80d6d972bad9e62e5d481d165b53f71b81fa3f2ee60c1f38383b9`

```dockerfile
```

-	Layers:
	-	`sha256:7f7828bace89a06fba317ac59d2d0d4f561a4b1ed564e19bcde350a12848659a`  
		Last Modified: Fri, 27 Sep 2024 13:02:54 GMT  
		Size: 5.8 MB (5766551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06ee18cabb2e2d55cc17f39ee0093e31ef075d2c1d2ee415a2184005a87bf5c`  
		Last Modified: Fri, 27 Sep 2024 13:02:54 GMT  
		Size: 54.6 KB (54644 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:9d6e0405b392ae78913edf1e1591533141c0facd1114efb4c289bf8e20b43da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140909844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b0d38f5c5a780ba43229102e2b57ae2d039e33ea521cc6e84dd4426107f149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d39d2d96734dd6c7fab8068ba08f92c7cbc1c98f5894e1c25c2265db8f74a5`  
		Last Modified: Fri, 27 Sep 2024 13:19:22 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a22c508463eb866d2934abcd7fae9234d1932914b2986b18d2d3758cab849b`  
		Last Modified: Fri, 27 Sep 2024 13:19:22 GMT  
		Size: 3.7 MB (3742490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f5dd4f0fd99c6a3012452faaca1c7f98c7ab9c5fb902ab68355721421dfcbf`  
		Last Modified: Fri, 27 Sep 2024 13:19:22 GMT  
		Size: 1.4 MB (1413563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0666a7837552389500ae71853be89df7cc34d20e8d5504a056f763f2855fcf80`  
		Last Modified: Fri, 27 Sep 2024 13:19:23 GMT  
		Size: 8.1 MB (8066267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f162e5e3b3b23a992b39df4c6ca227d40dfd24548618a1b27edaae3f7b2c1cc`  
		Last Modified: Fri, 27 Sep 2024 13:19:23 GMT  
		Size: 1.1 MB (1066954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e04d94c3aff724f37298d31af669139c832234fb26aebfd50d54ebef6be80a`  
		Last Modified: Fri, 27 Sep 2024 13:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d780f92ccafa30779296e018d5d6148e75f89526330fc3bdf6e40d930801edd`  
		Last Modified: Fri, 27 Sep 2024 13:19:23 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b22e2ecec5ce58a7a7996463223d68d92839668f952e91b87fc2562fef67726`  
		Last Modified: Fri, 27 Sep 2024 13:59:21 GMT  
		Size: 101.9 MB (101882178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c978736d97890c15a100023f8fcfa32f13fdce2b76f7c6d27a12cc4db9971592`  
		Last Modified: Fri, 27 Sep 2024 13:59:18 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83db88a24e6fab0765d2a1a5aad379344c0d608f0d0d4b5320d5f7c482976b7d`  
		Last Modified: Fri, 27 Sep 2024 13:59:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e820fa34d509ac44fdb31e1581ffe48e4a5a382064277d850430968c8f405f`  
		Last Modified: Fri, 27 Sep 2024 13:59:18 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0fb66832e9f459a1557ef735881ed1f9ee4a1fad59b8619efd47369c2e27a8`  
		Last Modified: Fri, 27 Sep 2024 13:59:19 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819a6f5e64dd4aa3c9329b5e0e53bbb67c9636f6a2d0bd1ac00b49cef6effc05`  
		Last Modified: Fri, 27 Sep 2024 13:59:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4bdbdbdbe0e0d8d16b28ad66edd26c4b4909aa1bf225d865a30a19801b844396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c2dc0655c237a2a957a78e6c2e81952ce6b3395bdf1dea0799d055582df8e4`

```dockerfile
```

-	Layers:
	-	`sha256:c36862fa45e0c2394f260ca5debb6502931bb517930081182d19311d4dee7c88`  
		Last Modified: Fri, 27 Sep 2024 13:59:18 GMT  
		Size: 5.8 MB (5766220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6387465fdaed242a9cf92d9a75b69826f17a198030c36d081999449ad5618bcc`  
		Last Modified: Fri, 27 Sep 2024 13:59:18 GMT  
		Size: 54.6 KB (54645 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3f00e596c6dd4c04fe6019b84796d46a7b4422273c51de175865950cc429f483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151630715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced3ad69d60ca3aa458ca3f8239e3b5e031720a202a76c9c5dd1edb9ec12a534`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c88e7faf79a34dd0af94058994e066483fb95ac60c57004716687e64f9bed5`  
		Last Modified: Fri, 27 Sep 2024 19:04:17 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86552d6a2e14fbce88d8ffa08a7f7e06dd4c6d7f208b84997c96c0f91053cba5`  
		Last Modified: Fri, 27 Sep 2024 19:04:18 GMT  
		Size: 4.5 MB (4499154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a986120aadb711cc1e9e8fbd5f2f62c7b123e0c329d6c1812be7bc38d03479b2`  
		Last Modified: Fri, 27 Sep 2024 19:04:18 GMT  
		Size: 1.4 MB (1378717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f6f593e3897cc85ba643ed6309995123ad8701a994700d1a796bb9ab0a1200`  
		Last Modified: Fri, 27 Sep 2024 19:04:18 GMT  
		Size: 8.1 MB (8066349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76441873964fa4a8d07dd408edfe47b022e2506a9fdabd6467f71cce1bd6c96a`  
		Last Modified: Fri, 27 Sep 2024 19:04:19 GMT  
		Size: 1.1 MB (1108704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00daffc086af223cc3083937b64cb98e4f5dbaae60aca84f869b695d9be65b4`  
		Last Modified: Fri, 27 Sep 2024 19:04:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e872bee6899bad3fe1acbb7e580e8381aa1f6a99b1e8d7b427011fe3beb076a`  
		Last Modified: Fri, 27 Sep 2024 19:04:19 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d671f95506d48aa25e22851469d766215915b7cb063add07957856feed677a8c`  
		Last Modified: Fri, 27 Sep 2024 19:13:14 GMT  
		Size: 107.4 MB (107401193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99654dcb227c063c91d6fd59700f06884ccd1c2b91702497583771dd470f3694`  
		Last Modified: Fri, 27 Sep 2024 19:13:11 GMT  
		Size: 9.9 KB (9913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efd022483623c7d477e10cbe82be85e2d0a8ee687c2621d55ec1040a837fa31`  
		Last Modified: Fri, 27 Sep 2024 19:13:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f7b5fa95135b954ced99700b344de7a16d7698f50fa995bf4a61084c237086`  
		Last Modified: Fri, 27 Sep 2024 19:13:11 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31e7d9d33c8d40f50f9a75eff244c1ade87296325c63c3c8d6bb893ea3429cf`  
		Last Modified: Fri, 27 Sep 2024 19:13:12 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08e1f72cb6a52f8dd79421f67272387d1f4ab5dc0717994e6d805ef67f32014`  
		Last Modified: Fri, 27 Sep 2024 19:13:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c47cb7f590f146f6e72a8c66a717bcdfaab616e9cbb59bd714b50b4d9760b10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5812064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e770dd3af1655deeba9cd1bac73fc69598c1dd12982e342cde57f82c0539fad`

```dockerfile
```

-	Layers:
	-	`sha256:06a8fefd096703510c4ee3f9e33dacf8e001ae74d3a2a126022e6ea8892e3332`  
		Last Modified: Fri, 27 Sep 2024 19:13:11 GMT  
		Size: 5.8 MB (5757324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a390821958e437393a96ca596d3b612a195684c4bc4676551ac3d6de1ecbc98`  
		Last Modified: Fri, 27 Sep 2024 19:13:11 GMT  
		Size: 54.7 KB (54740 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:1a08c79e9349c3a6e90d11c4719152e2196122787852e53199fe7e497ce77e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161575346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa632e48c9f69e0779da361bbff4f96027cc7de6b6dd4f525624fac038688a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a4642f99845310607b1835b5a378d8815a5de297000feeee1bf8bd63cb388d`  
		Last Modified: Fri, 27 Sep 2024 09:14:04 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adef5644b57b4e29a14c1a4c907faa33b26f53fa6aa4dff0f264dc000d8d9a0a`  
		Last Modified: Fri, 27 Sep 2024 09:14:05 GMT  
		Size: 5.0 MB (4965062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d616a07e2e958f162af7fe0a7c61d2b5963093f5b7d7fce3c749bbc8f177ce0`  
		Last Modified: Fri, 27 Sep 2024 09:14:05 GMT  
		Size: 1.4 MB (1422143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ac4c2c0fe5f1dd3634c18816c9a2080283ae3bf6d3d0d68188ced52675e63b`  
		Last Modified: Fri, 27 Sep 2024 09:14:05 GMT  
		Size: 8.1 MB (8066346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868cee5aa894478f914624dc57c38254400b97260159660506fcb2eb2d4e8363`  
		Last Modified: Fri, 27 Sep 2024 09:14:05 GMT  
		Size: 1.1 MB (1137151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f04d35d919d2b404f596df0717974ff902be2fc387efb29857926a9e0bee972`  
		Last Modified: Fri, 27 Sep 2024 09:14:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4928dafb42a3ac6e66dd4324375fabb7f030cd50a80a10db73e675a2ff77e3a5`  
		Last Modified: Fri, 27 Sep 2024 09:14:06 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb7dd9bfc84de7ff802d623b02b7962260ce62848bf0163329aa8bb1c733c86`  
		Last Modified: Fri, 27 Sep 2024 09:14:11 GMT  
		Size: 115.8 MB (115820187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689d6f72fa5f063bf22c1c1ff0e459c56e5de24e5bfe8b5363b418f0bc1f5664`  
		Last Modified: Fri, 27 Sep 2024 09:14:07 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7928c02bc0eb5e01eed28861b9b892c4b6b591adfa6437ff874e59005e9702`  
		Last Modified: Fri, 27 Sep 2024 09:14:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eec0484c41b90a657bca350aa6c0dd98188125773b937c9666e01fc6fbdef9`  
		Last Modified: Fri, 27 Sep 2024 09:14:07 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829e2c8d1e9e9043339faabd134f2c28868ce31eea10d69afd8047dfb7ae5578`  
		Last Modified: Fri, 27 Sep 2024 09:14:08 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6131631c6e13e45a29e1f1e0a7d5c92e9f847fb4c4739c8fe2991b52542a8d`  
		Last Modified: Fri, 27 Sep 2024 09:14:08 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8f94df9d6e01d9f19ed260b51ad4e540df42710d1781b0a4e446168375351305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5818985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe99bec400d40566957a19e82d68fe834694dceab4af8d8853e93f49ec5156e`

```dockerfile
```

-	Layers:
	-	`sha256:ba2c6683b3ff4ebb253a7ea812b1a427a6e0e8ffa45fa62a163d95c100fbbdf9`  
		Last Modified: Fri, 27 Sep 2024 09:14:05 GMT  
		Size: 5.8 MB (5764604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7891feb41e2de942d66aa3e9713930de90862a10d3713b96ff1af51867c60c9c`  
		Last Modified: Fri, 27 Sep 2024 09:14:04 GMT  
		Size: 54.4 KB (54381 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:6a387efbf3b255d773dd88d04db5f61f6547d4710fac32b2034749ac4f41c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148862838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebb0c045cf5c3c59934db706cc54e9d46ee38a56d469a767693aa5270a2d2ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af314cba9cb12e609d6f5e7e176fd1effba6f3378e51fcc24ee9659d84b3f295`  
		Last Modified: Sat, 28 Sep 2024 05:10:44 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21060f3e92dec884650f41e7e4e842b9df88d05e99485d146ea912652c492750`  
		Last Modified: Sat, 28 Sep 2024 05:10:46 GMT  
		Size: 4.5 MB (4475088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eb518019f221edbdda47fb6b99a27dd048ba63a0c25b471237ee7f9d43a8c4`  
		Last Modified: Sat, 28 Sep 2024 05:10:45 GMT  
		Size: 1.3 MB (1333787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c02e504a5e7f5c5f1111ff9378296b1d069ce86909bf813ef0f94ab896cde83`  
		Last Modified: Sat, 28 Sep 2024 05:10:46 GMT  
		Size: 8.1 MB (8066541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867a2bbc7c3ae5d498f28416ae2860f1f4bf26780b58f517b7ef754a05d11348`  
		Last Modified: Sat, 28 Sep 2024 05:10:46 GMT  
		Size: 1.2 MB (1182634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06717b5d1895893f9dda00250577258ffc2015f94120a03d364ab453fd8e8eb8`  
		Last Modified: Sat, 28 Sep 2024 05:10:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ef5a261d5e09fdd65265fc5d8e3972550396a7bab51431bf87e09c42499e8b`  
		Last Modified: Sat, 28 Sep 2024 05:10:47 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612590b2e4a0fa63da5f19877953cc8695e7f4452d0f79bde6ce9d5af52e2474`  
		Last Modified: Sat, 28 Sep 2024 06:21:41 GMT  
		Size: 104.7 MB (104659675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efb31c3f86223e16b389e844debb7a40a64de0abf9081fb4e224f39253fab72`  
		Last Modified: Sat, 28 Sep 2024 06:21:31 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2a6a30e09caa64af68ef79360b91069fde257871b92894c76be69578e3e9c5`  
		Last Modified: Sat, 28 Sep 2024 06:21:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5637246e7427521d05cda41d00a1dfbf75f4fa262eb9f7804bac4358bba77423`  
		Last Modified: Sat, 28 Sep 2024 06:21:31 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90e190538a60f83c5f8efdd301dd4628b3ba9eb1b4d5df224da28c21ecc48a`  
		Last Modified: Sat, 28 Sep 2024 06:21:32 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1eb62db0cfaf6b26ae597c01c5f5d2ce27e7ceba4570c13854cfe7a6004b072`  
		Last Modified: Sat, 28 Sep 2024 06:21:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1c8364732a6b17e6d544e86dfea24360f5ee5455237572f14ab7c92197bb86ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 KB (54303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb25b7f26f38de6b7d880c8c561dcfb84c94318d8bd84369fd49c5f2af9e6fa`

```dockerfile
```

-	Layers:
	-	`sha256:c3505474faa09196a6c7b3219e0543411918c5622a8266c7b388d5253c023d32`  
		Last Modified: Sat, 28 Sep 2024 06:21:31 GMT  
		Size: 54.3 KB (54303 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:94e19086ea238ca27d9b5395bc0d35ff06497efc629f535fe706a193350b726a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165628871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5903745662f03e0b84d3efc2a43b86d7733dcde27cec557b604a345fd85edb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf54cdb3c51234a200e3a5ea0b998d2697f1733d159674b2d59fd47da9244445`  
		Last Modified: Fri, 27 Sep 2024 22:28:17 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73c826b6f3a053b9527e8192429426da96e225f991578afaac9f17ae3e6b122`  
		Last Modified: Fri, 27 Sep 2024 22:28:17 GMT  
		Size: 5.4 MB (5368147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb16340d27ab05690ec0584c9807deb822e4fc432214b080a1ffe7d1a323fcd`  
		Last Modified: Fri, 27 Sep 2024 22:28:17 GMT  
		Size: 1.4 MB (1368568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71311acb7d188bc0ebb15a1a318aebcc0940c122ea4068301601bebad4193623`  
		Last Modified: Fri, 27 Sep 2024 22:28:18 GMT  
		Size: 8.1 MB (8066361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9f2dbbadd51375c292706713605a90574df14831465849b42dee1b7efec1c9`  
		Last Modified: Fri, 27 Sep 2024 22:28:18 GMT  
		Size: 1.3 MB (1283464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75167300b575090696c4ac208c0f19d409c71a9aba5b6433e69e19a2688b4d29`  
		Last Modified: Fri, 27 Sep 2024 22:28:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f6c4e0fd05ccfc4abe5c654cb666bb38899c21c4ea020fdcac2105b2476a1b`  
		Last Modified: Fri, 27 Sep 2024 22:28:18 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8cefa113660ccb9264c3548b2a31b9b9aa96d793d018eca0b7b6f80827415a`  
		Last Modified: Fri, 27 Sep 2024 22:29:51 GMT  
		Size: 116.4 MB (116399938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642b2abdb4fbe263b72a631ec7dadab2c7276bd7ce2fb52dad4fe598abeecca`  
		Last Modified: Fri, 27 Sep 2024 22:29:47 GMT  
		Size: 9.9 KB (9912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00f7238a23ccac573755bdb7a04c53ad9e448533d7060f55406aa49c5d9390e`  
		Last Modified: Fri, 27 Sep 2024 22:29:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c03ab354777a49bd02d32db638f113034e2761c07b0b0500b17b2d6b7b4971`  
		Last Modified: Fri, 27 Sep 2024 22:29:47 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c9034d902daf248a43010126d51c19ad24bd2fc3be7455df10efbfcf98d43`  
		Last Modified: Fri, 27 Sep 2024 22:29:48 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101da6bd801daaf15e77e4b0ec77bebf1834f9ea979cb2a52f47b108c9dd4fa1`  
		Last Modified: Fri, 27 Sep 2024 22:29:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e92cdaa37df85deff91a64f892e853f0dabcf6a03c71801435ea5fec3576ed23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5812704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0790410f638d4cd220de0b4fd36f2e00f85c56f913ff317947428c4c3c07736b`

```dockerfile
```

-	Layers:
	-	`sha256:c13e84af0df7be7b8a0d718b179108c4a52bcc92a442bd561be32da4f667f7c0`  
		Last Modified: Fri, 27 Sep 2024 22:29:47 GMT  
		Size: 5.8 MB (5758212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54872c26ae31448d6e6f0ee9af09ff015e526c7d0ee5db9115e177940d586617`  
		Last Modified: Fri, 27 Sep 2024 22:29:47 GMT  
		Size: 54.5 KB (54492 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:36798a6e97a850eae87cdc905c5296c1e7752b55538ec13407db5cf0a67d61f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158964658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3778442397521268a54722c88c7b40907f195fb94278d7d2c059de97500d553b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 26 Sep 2024 18:03:00 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV GOSU_VERSION=1.17
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV LANG=en_US.utf8
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_MAJOR=16
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PG_VERSION=16.4-1.pgdg120+2
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Sep 2024 18:03:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Sep 2024 18:03:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Sep 2024 18:03:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Sep 2024 18:03:00 GMT
STOPSIGNAL SIGINT
# Thu, 26 Sep 2024 18:03:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Sep 2024 18:03:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1d520b9a9ee5285c4270cc88cbbb8e5bc257213ae2140ccc073ec841b0f706`  
		Last Modified: Fri, 27 Sep 2024 15:27:34 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c8983de478016b32e2c145a386fac8ee381006eb0b61719536eac3ec333f6a`  
		Last Modified: Fri, 27 Sep 2024 15:27:34 GMT  
		Size: 4.4 MB (4391057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006718e1602ae92f7ab3999ca111386351cd2a5854bc2f0fec2c3f24d107c6b8`  
		Last Modified: Fri, 27 Sep 2024 15:27:34 GMT  
		Size: 1.4 MB (1412683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cb4d66be19cd79ca495d5b66ad9554021cad9a8ed3f2fdd4db17fca094f043`  
		Last Modified: Fri, 27 Sep 2024 15:27:35 GMT  
		Size: 8.1 MB (8120493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57948d4a9af326497a193dfea3caadae37f5a2ce4e2788f989fb3c6373d5d1b`  
		Last Modified: Fri, 27 Sep 2024 15:27:35 GMT  
		Size: 1.1 MB (1096736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f52d75f1b72f3b0d72d67eae3e76667e797da2c8adb610cf1d2edcc241170c0`  
		Last Modified: Fri, 27 Sep 2024 15:27:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02c450ab117a5683efd8ffd8be44cea8c3b424a355ab477785c13980c86466d`  
		Last Modified: Fri, 27 Sep 2024 15:27:35 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b595b2b67bca8ddc6b409ca50f7cbb9e8284b899290c1890c9b302b5a2ddc2bf`  
		Last Modified: Fri, 27 Sep 2024 15:30:53 GMT  
		Size: 116.4 MB (116433426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045fc81a95472b19e3c6c56b1231112af29a76e623f29259e1003d1610687fcc`  
		Last Modified: Fri, 27 Sep 2024 15:30:51 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a2be9669a23a24ba4a849ad650b748448c8b7af986edeacefb65d8da3e0b6d`  
		Last Modified: Fri, 27 Sep 2024 15:30:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01b006c125c7f4ceb3c1b52d5a79c6210dd468667ecb77c2a6278d32c97213f`  
		Last Modified: Fri, 27 Sep 2024 15:30:51 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23666d88dfd86fce014146ef97b7f68f2a58cf79f6b3599504eac5a139ae5d61`  
		Last Modified: Fri, 27 Sep 2024 15:30:52 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82975ee3f1ed2fbc0ae2e19174afbe4816d532b8a218386dbecec9c5cc62cc83`  
		Last Modified: Fri, 27 Sep 2024 15:30:52 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a91c570922799307f20d2d0cc930b683d8a45b3645a1d9882f28c684efee2ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645c63c1ce652c609537e65464ebe81e3774ad5e45d0bf008dbe42cf3a56bef0`

```dockerfile
```

-	Layers:
	-	`sha256:097753699e5797a360259c028d39e16a2a111ce04febd7c78086b4a4b684af8d`  
		Last Modified: Fri, 27 Sep 2024 15:30:51 GMT  
		Size: 5.8 MB (5750377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1ebd2cbdef39cd70809d8f4b1b709bcb8fc1529a9660b0a1924c14a4d421de`  
		Last Modified: Fri, 27 Sep 2024 15:30:51 GMT  
		Size: 54.4 KB (54432 bytes)  
		MIME: application/vnd.in-toto+json
