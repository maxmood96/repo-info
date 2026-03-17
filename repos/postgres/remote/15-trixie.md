## `postgres:15-trixie`

```console
$ docker pull postgres@sha256:47a7cb13d20593b796679217d65c3d405e985a051209a694cd3b295f5e515169
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

### `postgres:15-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:22850452d5a68c00a336883aebf3e51c8967a4286a3517134e6f8d3861257d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (158031432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06aa2e11e5977e6ab2ef540e743459ca474463cb11876117a9f2202b8d0a9512`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:33:29 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:33:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:33:42 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:33:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:33:47 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:33:47 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:33:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:33:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:33:51 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:33:51 GMT
ENV PG_MAJOR=15
# Mon, 16 Mar 2026 22:33:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 16 Mar 2026 22:33:51 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Mon, 16 Mar 2026 22:34:51 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:34:51 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:34:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:34:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 22:34:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 22:34:51 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 22:34:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:34:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:34:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:34:51 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:34:51 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:34:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2467f2f21d99c3bd38700663d79d2130e120dc0e336e300d8818f03c27e74c`  
		Last Modified: Mon, 16 Mar 2026 22:34:28 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ced18622af7809be6eb08f66f0ece3b5e203212dbcf1d02a1d70d458f46c7c`  
		Last Modified: Mon, 16 Mar 2026 22:34:28 GMT  
		Size: 6.4 MB (6441225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af73ff344a10f7cb8311464a4c83bb41d0f297bddba450cfbb54e6c2a8ecc1f7`  
		Last Modified: Mon, 16 Mar 2026 22:34:28 GMT  
		Size: 1.3 MB (1256734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cec992154a6d24a634aa4244340f2d4c6dbc17c61c6dbcc1ce336520524cd2`  
		Last Modified: Mon, 16 Mar 2026 22:34:28 GMT  
		Size: 8.2 MB (8203799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0dcffac314aee19c897dc94f534e42ed26230304579b8d91070dc83b90b64c`  
		Last Modified: Mon, 16 Mar 2026 22:34:29 GMT  
		Size: 1.3 MB (1311646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda354b903ce37407000de778bc230223ace201fef055bcedf95a312d87ff471`  
		Last Modified: Mon, 16 Mar 2026 22:34:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd98f4944fb967f8951cfac9e6ba365da3ab8dfbade10598e054db26e0b1bfb`  
		Last Modified: Mon, 16 Mar 2026 22:34:29 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e04ac2d7d26cd11f3fd7997e7fe68591fd62b891137aa9173452032ba8fabe`  
		Last Modified: Mon, 16 Mar 2026 22:35:12 GMT  
		Size: 111.0 MB (111021907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a2676f0017d4945b7c9b7d420918c7b0e7a5ab0b7b05a94c9b662fe7cef5de`  
		Last Modified: Mon, 16 Mar 2026 22:35:10 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3f9a27af8f768b4379a27572ecbada79175986540c3b06d7194f2a6855c44`  
		Last Modified: Mon, 16 Mar 2026 22:35:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c8c030ed3ba797be6fa0f9c522367f5ab376ba942a29262d7d0ce2fa8f47ca`  
		Last Modified: Mon, 16 Mar 2026 22:35:10 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e686ef69061b178596f4ca134f4ec3db780d37ab4ffe4e9d9bd307f75ecd10`  
		Last Modified: Mon, 16 Mar 2026 22:35:11 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c40507d19cfc6c0bf5f5b7c0a1bff5a18a915927b0c86a3255be27fab2e3a2`  
		Last Modified: Mon, 16 Mar 2026 22:35:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:5e97d30ecc9b63fd2ac7048fa6d00358e4343630e626ebfc4d0e98e0181579f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41028a8930c2e2e792f1ea0d4c733277599f8db4af0ace27998b536b39866f28`

```dockerfile
```

-	Layers:
	-	`sha256:e0f479c780c9496502f07092a99c06f3c1b4de4e9cf58026baefbc3903df10b8`  
		Last Modified: Mon, 16 Mar 2026 22:35:10 GMT  
		Size: 5.6 MB (5642554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe39cf73b6414139a8857d48d8a5c4e2595d646bd78ec74e0db8763a1e3a0711`  
		Last Modified: Mon, 16 Mar 2026 22:35:10 GMT  
		Size: 53.9 KB (53863 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:d692c6ce6202a26e0485350b483852ce1cbeac68d6f605ed975010e4a5e8e336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152074317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ae89a6dfe5c6edf2ded5bc5ba371e66cf5098a1b17dd0796fd50ee55f95df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:48:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:48:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:48:32 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:48:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:48:41 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:48:41 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:48:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:48:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:48:49 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:48:49 GMT
ENV PG_MAJOR=15
# Mon, 16 Mar 2026 22:48:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 16 Mar 2026 22:48:49 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Mon, 16 Mar 2026 23:05:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 23:05:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 23:05:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 23:05:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 23:05:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 23:05:00 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 23:05:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:05:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 23:05:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:05:00 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 23:05:00 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 23:05:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7f956967ae27b2c13ec8260e1c47a3f56babcf9c5adb6faefcc08278bc5e03`  
		Last Modified: Mon, 16 Mar 2026 23:05:19 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1c8e3a395b0d19822a175b68ce6128bb35882719f19d1c3bba1665c425e91d`  
		Last Modified: Mon, 16 Mar 2026 23:05:19 GMT  
		Size: 5.9 MB (5932521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c579e496ec376368156b58dc7d49a35bc57849b37daf1ebbda64224f8a41d78`  
		Last Modified: Mon, 16 Mar 2026 23:05:19 GMT  
		Size: 1.2 MB (1227575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626f549644fd9efd37453e434b5768c97e82fed993507644648fbc59b5bd9f2c`  
		Last Modified: Mon, 16 Mar 2026 23:05:20 GMT  
		Size: 8.2 MB (8204204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b13776621bcad424a54d0f55d1760f429d10f79cb7c474816266b4d479a8432`  
		Last Modified: Mon, 16 Mar 2026 23:05:20 GMT  
		Size: 1.3 MB (1317348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460da4f769338a538e92202feb814bb0f921f6f1fbb8c5c43d67d74c56d45d3b`  
		Last Modified: Mon, 16 Mar 2026 23:05:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d2fa1a412f9ad880865ee033e6bb9fa0fdae8f901af9612de9cfe31f7b78fe`  
		Last Modified: Mon, 16 Mar 2026 23:05:21 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c52cef0f9294413bbcc75a3489d7cff5324b06bc67916e9c2b0ceb5d8f18b7a`  
		Last Modified: Mon, 16 Mar 2026 23:05:24 GMT  
		Size: 107.4 MB (107428395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c792a5a3c38cf488369b958fb0e3b1cf532548cb2e5573b440779c647d1598f`  
		Last Modified: Mon, 16 Mar 2026 23:05:22 GMT  
		Size: 9.9 KB (9879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cd1c26b50afa28c0097cd94434dacfe5eed1f340c1c9a9aa4394a3bcc62caa`  
		Last Modified: Mon, 16 Mar 2026 23:05:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ede978342eecda9f723891f892196cf0c3fc2df6f20da4abe7321535ed3ad8`  
		Last Modified: Mon, 16 Mar 2026 23:05:22 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8986b44dc11e79d28fbceecb07a1cb4d1c3529e4a81805ccb740857df2a8bc43`  
		Last Modified: Mon, 16 Mar 2026 23:05:23 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba04276cd5c2f84b2072646210302f6dedb492a809147a76fd4120d6e11d3a8`  
		Last Modified: Mon, 16 Mar 2026 23:05:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:86e22edf38d604cdfaa68f65b79e7d29aa9bbe8e147ede25ad3433e6ab7bd47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5904acb5721785b7ab6368739311352167bcfa02424a9c4ae4a3bbe57bf66d`

```dockerfile
```

-	Layers:
	-	`sha256:919fe4c6dab5c8bb6b41b14969a53367082e9a88d29875e1ceb87fd281f94405`  
		Last Modified: Mon, 16 Mar 2026 23:05:19 GMT  
		Size: 5.7 MB (5659192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9cbe25cd3818323ee05fc71719c732ed5cc859dfa105f60ff2f960c3fa7a3ee`  
		Last Modified: Mon, 16 Mar 2026 23:05:19 GMT  
		Size: 54.1 KB (54086 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:12fc6b721b9870f06238d9a7dbc3fdaa6bd55a458fa13f54c5e361cfe56337c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147154319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae23ec90a8bf6c0a63a76b38e7f473c6aece8fd0cd69648d364c76947e77153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:03:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 23:03:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:03:38 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:03:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:03:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 23:03:45 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 23:03:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:03:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 23:03:50 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 23:03:50 GMT
ENV PG_MAJOR=15
# Mon, 16 Mar 2026 23:03:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 16 Mar 2026 23:03:50 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Mon, 16 Mar 2026 23:18:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 23:18:01 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 23:18:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 23:18:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 23:18:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 23:18:02 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 23:18:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:18:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 23:18:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:18:02 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 23:18:02 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 23:18:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2cfad8019c83f9d9d6cb75afc41361a25da15c55a83993dee3713a74335f74`  
		Last Modified: Mon, 16 Mar 2026 23:18:19 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7212cfcbdb977175506a5b7aa62c2a91d32cb7a108892d40a274abb14142348f`  
		Last Modified: Mon, 16 Mar 2026 23:18:20 GMT  
		Size: 5.5 MB (5496567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320565718c8fba5f137dbfc6fa96aae706d30912cbb205854eefa9e4598fdc8c`  
		Last Modified: Mon, 16 Mar 2026 23:18:19 GMT  
		Size: 1.2 MB (1222373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49180d0abb303458933863f9c87db1a423dfa54335906c903ec52072751108f`  
		Last Modified: Mon, 16 Mar 2026 23:18:20 GMT  
		Size: 8.2 MB (8203961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62de2fdf08af66638a86db4bfae40f9f048dd8e97b988fc047d3854dfc3492e`  
		Last Modified: Mon, 16 Mar 2026 23:18:21 GMT  
		Size: 1.2 MB (1172596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38903db58dc3ae01616be3ad86ab8b1aff35bd6a21c9752d5872f80bc6f8899a`  
		Last Modified: Mon, 16 Mar 2026 23:18:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f20820970b0c642727dc51000c9a47e423e2795a91b2303fba10b7fe217be0e`  
		Last Modified: Mon, 16 Mar 2026 23:18:21 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a448e173bcd53a20c6cc4b0e1e545c5d50fe0887914e1369ef2a79fddff930`  
		Last Modified: Mon, 16 Mar 2026 23:18:27 GMT  
		Size: 104.8 MB (104828680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26c50dca3ccb691c6d4c5d108999cf483f05c83077232c791b3259c60df734f`  
		Last Modified: Mon, 16 Mar 2026 23:18:22 GMT  
		Size: 9.9 KB (9894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130edae9fe7ec42a70f088ff4d8fa5b8dadc921e2a259cd5005d4cbc6b81e103`  
		Last Modified: Mon, 16 Mar 2026 23:18:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a8a0b93cc3de49f5c5adf00b81dc31160cbce9077c99f84dfb566680de3a22`  
		Last Modified: Mon, 16 Mar 2026 23:18:21 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762f67e8f5ddedf59541144098b8d4fa5c0bd96dba45628f39f8f4c66bc8488c`  
		Last Modified: Mon, 16 Mar 2026 23:18:23 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addb1d688a82d45ca728a21a51e09d0f7204a4b258ea73efaca185f6a1a1f10e`  
		Last Modified: Mon, 16 Mar 2026 23:18:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:7b8f86310736b1f24db33df037af47601e9e8825d6f7745fd5b532d5115ef4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5712583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1038f20432e358566670b0921241b3af055b10c32c2d3d23acb314f3fcee6b7`

```dockerfile
```

-	Layers:
	-	`sha256:40163a19e816c84a5934222e74c0b996ce31b88d0b276fab1c9e541335823371`  
		Last Modified: Mon, 16 Mar 2026 23:18:20 GMT  
		Size: 5.7 MB (5658497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc7701721b4cefca0585943579c7dd6c753049cd92a74001687e8f8adc6110d`  
		Last Modified: Mon, 16 Mar 2026 23:18:19 GMT  
		Size: 54.1 KB (54086 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3c9f8c829468912776a2b0794ee7d3241af197316f9778464c424a4e247ef787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156662020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8476ce799a39839344ad069d50a4623962cb42bd5e14fb94e87fcf4eeff3c4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:36:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:36:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:39 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:36:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:36:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:36:45 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:36:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:36:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:36:49 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:36:49 GMT
ENV PG_MAJOR=15
# Mon, 16 Mar 2026 22:36:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 16 Mar 2026 22:36:49 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Mon, 16 Mar 2026 22:37:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:37:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:37:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:37:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 22:37:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 22:37:05 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 22:37:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:37:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:37:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:37:06 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:37:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:37:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9035978c0819c46c332e6bb9b0f48769ffac261b9be56ebd62ae7a992654210a`  
		Last Modified: Mon, 16 Mar 2026 22:37:24 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0cc485558c226c6c76781cb293aea30fbb7fdc641d4ba5447a1011e8096d82`  
		Last Modified: Mon, 16 Mar 2026 22:37:25 GMT  
		Size: 6.2 MB (6234088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c77fe09b070169dc1458000b3d354cd83081995b52ff047cc1038b0ec8f562a`  
		Last Modified: Mon, 16 Mar 2026 22:37:24 GMT  
		Size: 1.2 MB (1209618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a07c3a6937b36fd9ab53f19b53795cf9b7f3b1c8836185614522deba3ddf3bf`  
		Last Modified: Mon, 16 Mar 2026 22:37:25 GMT  
		Size: 8.2 MB (8204056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aa1e3623ec45c8c22aa9d999d1262b38ca7687c02f9c982767729c847cdd52`  
		Last Modified: Mon, 16 Mar 2026 22:37:25 GMT  
		Size: 1.2 MB (1220654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db70415ab6956ce6e8dea9710df4269a889c263c7421bdb772f7a7efb8f2c29c`  
		Last Modified: Mon, 16 Mar 2026 22:37:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c523241920d0210af44953e5c50b7774168326e57b97a5b5771371bc6b2b486`  
		Last Modified: Mon, 16 Mar 2026 22:37:26 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0ed0e3b0ce392b6694ac548929f0dd4d36958b8250018d243e7b51a66df0d0`  
		Last Modified: Mon, 16 Mar 2026 22:37:29 GMT  
		Size: 109.6 MB (109634563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2434da4e2fe1f26386d4bc39d5f4e474944404388d510bd5e0086e3cac0937`  
		Last Modified: Mon, 16 Mar 2026 22:37:27 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b403ce8476a3811075a7a2d5b27ace1ca4fbd3fbb9ac8c4b87110131fbb5e03`  
		Last Modified: Mon, 16 Mar 2026 22:37:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d543dca95999cae1f7b4ccd325328929821160fa02c04bb7f335b048d391b6e`  
		Last Modified: Mon, 16 Mar 2026 22:37:28 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdbfd2ef67f7f55829e68c91efabf59753b9b282485dc72e4bcc09c993d725a`  
		Last Modified: Mon, 16 Mar 2026 22:37:28 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294466172e3040d3ba438e56be04f544cb2b509fce71c1d175a197cfd247c7c4`  
		Last Modified: Mon, 16 Mar 2026 22:37:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:9048fe91aa3fc044b6d431f78d0bdb1461e7fc791de894d52f8c4db76e9d1ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5703033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9547d0b9e11103f7a185c8dac0f1c144034b4d25665bd7cf2d0fcde574f3234e`

```dockerfile
```

-	Layers:
	-	`sha256:8514c53847337bb67defdda526c4b17019d785fefaf9735afd5cfd96a7d7635a`  
		Last Modified: Mon, 16 Mar 2026 22:37:25 GMT  
		Size: 5.6 MB (5648900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f9d0b39a446a6b880110d7ea8a63724c0d0d65aef51c2143681b518668c3a2c`  
		Last Modified: Mon, 16 Mar 2026 22:37:24 GMT  
		Size: 54.1 KB (54133 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; 386

```console
$ docker pull postgres@sha256:31dc439b93b90546bfc9d0fbb729687fc8f45f79de62bcd46093726e73aa1dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167135901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c5a0a89142485ae1de4e30ed3ae02e585a5e35d8953dbfc197886baa8efe72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:32:49 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:32:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:33:03 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:33:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:33:09 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:33:09 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:33:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:33:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:33:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:33:13 GMT
ENV PG_MAJOR=15
# Mon, 16 Mar 2026 22:33:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 16 Mar 2026 22:33:13 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Mon, 16 Mar 2026 22:43:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:43:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:43:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 22:43:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 22:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 22:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:43:40 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dd34ae929e8e8c17fc0d5328ede745b58003999cf0d2045496aa5d21dbd0d3`  
		Last Modified: Mon, 16 Mar 2026 22:43:58 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58435713d119497f0ee4cac1dbb8e63fccdb659e1cb54b9d27a986ecfe8d233f`  
		Last Modified: Mon, 16 Mar 2026 22:43:58 GMT  
		Size: 6.6 MB (6631496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c1b18c01cb17c116cbbd3ff399793f6cf91ac9d61f2f43cb432c60d3b56f23`  
		Last Modified: Mon, 16 Mar 2026 22:43:58 GMT  
		Size: 1.2 MB (1225799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629734114dcdbb83151b1abe150222a57a911fffaa7a45b43b267d4f385e3441`  
		Last Modified: Mon, 16 Mar 2026 22:43:58 GMT  
		Size: 8.2 MB (8203944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222187a144bfc0f0063fe919495e3220b943bd90e0e898bdc35479586f1ecdfa`  
		Last Modified: Mon, 16 Mar 2026 22:43:59 GMT  
		Size: 1.3 MB (1308253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf55ca9c6a8963f1e5a385b972fbcd6bbe42ea5bc920811cf9a8e96cc37ee66`  
		Last Modified: Mon, 16 Mar 2026 22:43:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20951646a80cac48e34eb68174b16ebf2b047a9fc2b483aba49dd2d74122f83e`  
		Last Modified: Mon, 16 Mar 2026 22:43:59 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64c39149fdc5071e3f93307b671609f21f56d511f918654f59d1ca2e84e3f2e`  
		Last Modified: Mon, 16 Mar 2026 22:44:02 GMT  
		Size: 118.5 MB (118454655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c445a52870baded9813dd34b42569e9e5ae1fb3695762493551004325d6806f1`  
		Last Modified: Mon, 16 Mar 2026 22:44:00 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719fe6af76d6d7607a3eceaf4e28fa9af6b6c677ac31be78f3f8be9089d4709d`  
		Last Modified: Mon, 16 Mar 2026 22:44:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ea917f9bc17ab87a07183eb128c9d32c2fa4547c8bc7f7346112d61892db96`  
		Last Modified: Mon, 16 Mar 2026 22:44:00 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109fa46e72b0fdc7f8c9c9364a4ad86a1e740e2446dcb2ba19965b7ac39adf5a`  
		Last Modified: Mon, 16 Mar 2026 22:44:01 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63664563d333ae43966c3cda40531504c5694e446f3a226ee112456460c049bf`  
		Last Modified: Mon, 16 Mar 2026 22:44:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:79389617c7349843d4f29c6ce54f126b4cba8063f178420944594735fbe0077c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5711894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb588472f1a53b775ad431038505e371de9477c7a370296b17b322bbdd7aef93`

```dockerfile
```

-	Layers:
	-	`sha256:d58b8f3ee02adea747c9ed0ee43e8e64cb219213b4287b63562bd67d8b6fb4ec`  
		Last Modified: Mon, 16 Mar 2026 22:43:58 GMT  
		Size: 5.7 MB (5658085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:382bf5cb81acad1433b9ac0fce4ea93e5879491c7348fd5f141c8de543227d62`  
		Last Modified: Mon, 16 Mar 2026 22:43:58 GMT  
		Size: 53.8 KB (53809 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:df1f5b01c75323962d5985e506544d9ddf807ec79e0896deda25acc0e6a81da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170288108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90d6d0fbe737507c125e171190675566670f8fcbd0f4a82eaf0c1121e2ef705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:56:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 24 Feb 2026 20:56:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:56:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:56:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:56:50 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 24 Feb 2026 20:56:50 GMT
ENV LANG=en_US.utf8
# Tue, 24 Feb 2026 20:56:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:56:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Feb 2026 20:56:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 20:56:59 GMT
ENV PG_MAJOR=15
# Tue, 24 Feb 2026 20:56:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 24 Feb 2026 20:56:59 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Thu, 26 Feb 2026 19:34:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:34:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:34:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:34:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 26 Feb 2026 19:34:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 26 Feb 2026 19:34:06 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 26 Feb 2026 19:34:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:34:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:34:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:34:07 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:34:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:34:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40248b5208b48e0e9ebc31dab2059dabe20332fc4bb1ec45dc8aa5e1fe9c9128`  
		Last Modified: Tue, 24 Feb 2026 20:58:26 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c07d0d1d47bd4056b39ca321d6f1599c262f4e7e7c61fed95bf692a7bf355e7`  
		Last Modified: Tue, 24 Feb 2026 20:58:27 GMT  
		Size: 7.1 MB (7076565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a5f2e35019a76aefee22e397b204520a3f66e4951f57efda4751593a483c29`  
		Last Modified: Tue, 24 Feb 2026 20:58:26 GMT  
		Size: 1.2 MB (1214767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f7a05acca236351baa0b2518676e18567e268cc12c1981ad8b6855176339bb`  
		Last Modified: Tue, 24 Feb 2026 20:58:27 GMT  
		Size: 8.2 MB (8204004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3d66a30c54a599dce72a82fee964c52aa01d586db4c938507314a62bc3af48`  
		Last Modified: Tue, 24 Feb 2026 20:58:27 GMT  
		Size: 1.4 MB (1394901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa754634ead0b3025f44ae8a7a31e0f8b0c32d9914c15de96605223c7d32c45`  
		Last Modified: Tue, 24 Feb 2026 20:58:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c258d92643098feeef8976aec5642f3ca772b343b0556346a5226f72e85b6416`  
		Last Modified: Tue, 24 Feb 2026 20:58:28 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d34f1980b9a1af1cb1f772e3fb84dd3e200f402936bbc8302e94a19d1749f94`  
		Last Modified: Thu, 26 Feb 2026 19:34:55 GMT  
		Size: 118.8 MB (118777024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25aef087c6fe2eb929d7673b8d9b227a45898db4f982841a40622845875fc0e`  
		Last Modified: Thu, 26 Feb 2026 19:34:52 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31480c7c03390760eadd2f3503dba782400d01bf8b77d449743ca74ec30415ca`  
		Last Modified: Thu, 26 Feb 2026 19:34:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f217c0e6289b55216e7997dd33626a81cc71990f68ff9a12c90f9dc7adef9b21`  
		Last Modified: Thu, 26 Feb 2026 19:34:52 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66644b1102ca38d5d5d25476c2ef4aeb6900a037575386fca16027e4ea2bec9a`  
		Last Modified: Thu, 26 Feb 2026 19:34:54 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb7efc27fb5bc452addcd95371d445bd680d602656af9436c6bd16632d8d301`  
		Last Modified: Thu, 26 Feb 2026 19:34:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:9684b20651e360e8059aee53d14feec6ed0351be9db58486eae7532d87d5781f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5703059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b7eea52ecdcd5412d66b73f6b5f7b7f4ca4033562e47bbea17b9ced90aee92`

```dockerfile
```

-	Layers:
	-	`sha256:e6cce4189c3a1177b73d14391942c079c6f2a64025897b559e25d5057d7c7dca`  
		Last Modified: Thu, 26 Feb 2026 19:34:52 GMT  
		Size: 5.6 MB (5649129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d144b4e1c44083c30cfa235d88751a1ff4b7a3412f7018bbe7a46ed35fc20415`  
		Last Modified: Thu, 26 Feb 2026 19:34:52 GMT  
		Size: 53.9 KB (53930 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:542c676f0577618c22053107d932bd05e57cdc4c77361f9cea4f9e4c1393c406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90001966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7361c0a0c60e6eaebeb4eda2a5e49de7a49784536a23d3733f4d037ab8c998`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 10:33:50 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 10:34:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 10:35:45 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 10:35:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 10:36:47 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Feb 2026 10:36:47 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 10:37:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 10:37:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 10:37:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Feb 2026 10:37:30 GMT
ENV PG_MAJOR=15
# Thu, 26 Feb 2026 10:37:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 26 Feb 2026 10:37:30 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Tue, 03 Mar 2026 06:22:58 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Mar 2026 06:22:58 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Mar 2026 06:22:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Mar 2026 06:22:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Mar 2026 06:22:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Mar 2026 06:22:59 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Mar 2026 06:22:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Mar 2026 06:23:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Mar 2026 06:23:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Mar 2026 06:23:00 GMT
STOPSIGNAL SIGINT
# Tue, 03 Mar 2026 06:23:00 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Mar 2026 06:23:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f4de74a642c2b3077707bd1d98d860fa32f2bfe2bc8bec6f008e70352924e8`  
		Last Modified: Thu, 26 Feb 2026 12:47:29 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a8407dad47f53b7bd1ea58319099c5eb75ab9c71c0eaca77278c4ffa19d752`  
		Last Modified: Thu, 26 Feb 2026 12:47:31 GMT  
		Size: 6.3 MB (6293365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66156bf55222d12e2c741e02df3bb126b84a2158817f228188816cf5fdc34b7`  
		Last Modified: Thu, 26 Feb 2026 12:47:30 GMT  
		Size: 1.2 MB (1202062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa18f458f01a6e3a060b40acab343ea7b503f8752ed19cc7d8238801887e74f`  
		Last Modified: Thu, 26 Feb 2026 12:47:32 GMT  
		Size: 8.2 MB (8203602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88856c3799c7a7a18d5a1caec1776767905d6d751c5ca34a43520e664345c9ea`  
		Last Modified: Thu, 26 Feb 2026 12:47:32 GMT  
		Size: 1.4 MB (1402389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9b9b4fafc817b06c3eff32d69f1a43108bca48d49089ec0a13884be0d56a4c`  
		Last Modified: Thu, 26 Feb 2026 12:47:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66199c3c0efda8b281834bafb7b9360c4a8cc288875a8db72f60084aa85bdde4`  
		Last Modified: Thu, 26 Feb 2026 12:47:33 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ed19f3b3a19c3aad02e80cfdc47f608bd3bfd1be69c4e6f4b5248c80883e8`  
		Last Modified: Tue, 03 Mar 2026 06:25:29 GMT  
		Size: 44.6 MB (44603485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ea4c912a30ed466d26895054105284fb692854f26cbf85ba3cc527b6ba95fc`  
		Last Modified: Tue, 03 Mar 2026 06:25:22 GMT  
		Size: 9.9 KB (9893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8755ae69ea7f7a8364c3e66ed5ec99f45b7fa2a42c1c4a3fdb2bdccb5a06a6cc`  
		Last Modified: Tue, 03 Mar 2026 06:25:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388db3554c7d815a9dd425da2df7288f1cc098fd461a1a8a13445ea693fc2bd4`  
		Last Modified: Tue, 03 Mar 2026 06:25:22 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00d29daf8cdd10a02b295e855f5c8f5bfeddf6d5555c529f5313df779354570`  
		Last Modified: Tue, 03 Mar 2026 06:25:24 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff8d76e0d2c10339e2788a2d668358672390264d8bf5461a61daa59655e8770`  
		Last Modified: Tue, 03 Mar 2026 06:25:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:3311212e7925f0f2ce76bbd23a2e49468387d29b8e900beb3d88e91e950257c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5dcae7ff95db83b8bf5a9884666953beab35007455ed2136b61c8913f3d45e`

```dockerfile
```

-	Layers:
	-	`sha256:62015c80f557498f6c0163cf8b2de5f2cfb7424b77cc4757aa1deac71519db0f`  
		Last Modified: Tue, 03 Mar 2026 06:25:23 GMT  
		Size: 5.0 MB (5020562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b763b5d41603febf15c649018d9f77049cd64dea4538de0f8efb1169d3499f2`  
		Last Modified: Tue, 03 Mar 2026 06:25:22 GMT  
		Size: 53.9 KB (53924 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:e30396d0ec2bdc40dd299020605763a755a99736132e133ce420b2c352b8ed36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172574856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3cd2a57344f0700e81313a221fbd3bd0a3ce19abb63d39410ab9b974bbadaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:03:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 23:04:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:04:10 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:04:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:04:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 23:04:16 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 23:04:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:04:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 23:04:21 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 23:04:21 GMT
ENV PG_MAJOR=15
# Mon, 16 Mar 2026 23:04:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 16 Mar 2026 23:04:21 GMT
ENV PG_VERSION=15.17-1.pgdg13+1
# Mon, 16 Mar 2026 23:32:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 23:32:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 23:32:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 23:32:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 16 Mar 2026 23:32:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 16 Mar 2026 23:32:56 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 16 Mar 2026 23:32:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:32:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 23:32:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:32:57 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 23:32:57 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 23:32:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0bedd45617efc9fac0c06527c0d0f407bd931eda950911aedd3c1465b33f07`  
		Last Modified: Mon, 16 Mar 2026 23:19:07 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88034c14cae88b096db0b07fc3c28de80e98a007fd70be84a9e101df401fa66b`  
		Last Modified: Mon, 16 Mar 2026 23:19:07 GMT  
		Size: 6.4 MB (6407809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527d3f83182c3fa177683bdd95e4ea3d2ef9dfda5326661b37033f9e1fd22657`  
		Last Modified: Mon, 16 Mar 2026 23:19:07 GMT  
		Size: 1.2 MB (1230153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c53d2261b6e197c0e30a1201b02d4da8017e7ee4f386f6ddddd1cb591c4824`  
		Last Modified: Mon, 16 Mar 2026 23:19:07 GMT  
		Size: 8.3 MB (8258983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108379b87e375449e4fc0a6820319d08de8830a0c72702e632ac6046be3ee7ea`  
		Last Modified: Mon, 16 Mar 2026 23:19:08 GMT  
		Size: 1.4 MB (1398201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58289d2db003dadd52235e33b0aba6e476ed528de3281e3a3ef5c249ec8fe66`  
		Last Modified: Mon, 16 Mar 2026 23:19:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebc73e057f674fa5f886ea59c73ea78f1120cdc98ecdd1c1e1b7cad612d4516`  
		Last Modified: Mon, 16 Mar 2026 23:19:09 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd3dbd5e4abc2e9928014bac5681ea1583e7d576e51fa772466974b6893dd37`  
		Last Modified: Mon, 16 Mar 2026 23:33:32 GMT  
		Size: 125.4 MB (125423831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0498401952f1ff47257ed700b6a1374041655f67b70bed1d94f1808e21558b`  
		Last Modified: Mon, 16 Mar 2026 23:33:29 GMT  
		Size: 9.9 KB (9880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfe9d1a36c9af276ac1c46e7e3e984807c91340406058d423eb0c1f4cf6bd44`  
		Last Modified: Mon, 16 Mar 2026 23:33:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ed2539bb0f87a43455a8325646b3cd11055bd599a3710a40d66ef53b6621fa`  
		Last Modified: Mon, 16 Mar 2026 23:33:29 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f836a864f4e06f0e31937d49bd7be5381a7027158f8ac2ee55176f03104b3a7f`  
		Last Modified: Mon, 16 Mar 2026 23:33:30 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab2d516641d53a054dd5cae8c07636a4c0bc69b2ae5914a4fbd6601d627d8f7`  
		Last Modified: Mon, 16 Mar 2026 23:33:30 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:4a5019b8f630b641d499abadd72f1b2fa3e3ab7c143bb72ca5db5b5370808fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e19e69e5c3937c483d32ae5295e97cd8f20515b6c8d3c5d9a2605822f837360`

```dockerfile
```

-	Layers:
	-	`sha256:5f15244a9670de47da719edcd25d2289a85c63e69a21e737557931aa0a991218`  
		Last Modified: Mon, 16 Mar 2026 23:33:29 GMT  
		Size: 5.7 MB (5659223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1786173d119fea37f3941b3c33331b76e69f4b272b60361733fb0acacb35e868`  
		Last Modified: Mon, 16 Mar 2026 23:33:29 GMT  
		Size: 53.9 KB (53864 bytes)  
		MIME: application/vnd.in-toto+json
