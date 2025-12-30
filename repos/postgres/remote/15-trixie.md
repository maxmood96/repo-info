## `postgres:15-trixie`

```console
$ docker pull postgres@sha256:9023e10449fd523d8a08922571cf1656c48f33dfa1f5841a33afe6363389b3cd
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
$ docker pull postgres@sha256:576ac5fe7c983bab9241b9db7cbeb652e42b484eed837b65d6bdc47737ec3be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157993997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12bf22fb38aa8c18eb7938731a59b89073dfb8640ec0c91f3d23e393cfc6728`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:38:09 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:38:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:38:21 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:38:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:38:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:38:26 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:38:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:38:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:38:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:38:30 GMT
ENV PG_MAJOR=15
# Mon, 29 Dec 2025 23:38:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 29 Dec 2025 23:38:30 GMT
ENV PG_VERSION=15.15-1.pgdg13+1
# Mon, 29 Dec 2025 23:38:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:38:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:38:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:38:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 29 Dec 2025 23:38:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 29 Dec 2025 23:38:43 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 29 Dec 2025 23:38:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:38:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:38:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:38:44 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:38:44 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:38:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf68bfba782a215ed6785f83baa2fb47948838a5ad6a301b413882974d23ad9`  
		Last Modified: Mon, 29 Dec 2025 23:39:13 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d09bd18eb088978c13fdf5a2f950b0decf761359d131656aa3d7f71847745cf`  
		Last Modified: Mon, 29 Dec 2025 23:39:14 GMT  
		Size: 6.4 MB (6436620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195bac0eec0b8bf7c52b9f458664411d37e222e0ba3de5a5c456dc5f139713ca`  
		Last Modified: Mon, 29 Dec 2025 23:39:13 GMT  
		Size: 1.3 MB (1256603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9511a7a37c191da4aa9fa1125e8a9384787ad12e7edad7bfa94261df9dd844`  
		Last Modified: Mon, 29 Dec 2025 23:39:13 GMT  
		Size: 8.2 MB (8203734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337afc0e3ee1f19da352e865ec6968b760010b7666f1eae24af5bc7b7bfe9e7e`  
		Last Modified: Mon, 29 Dec 2025 23:39:13 GMT  
		Size: 1.3 MB (1311488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef543c8a7a9c72f8b2108779e0e0977e5417d6cb8f3054ffd64038eed8e534c`  
		Last Modified: Mon, 29 Dec 2025 23:39:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc86d799acdf02ccc1f344dcc381c0601aa71c28bf75d9e3a25ed8712a65bdbc`  
		Last Modified: Mon, 29 Dec 2025 23:39:13 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bc2bb369adedb70c32c8e31238d7025f95e3698087d143e3f0b87ebf0ddac9`  
		Last Modified: Mon, 29 Dec 2025 23:39:22 GMT  
		Size: 111.0 MB (110988397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b21acdfee67bd1564cf01e1ae4d38a663213ef96ba2b4bc14571aa687fba409`  
		Last Modified: Mon, 29 Dec 2025 23:39:13 GMT  
		Size: 9.9 KB (9880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2425bc244d6d7643986c2cf8819333793a2560de8db756051c148bdde19cc56c`  
		Last Modified: Mon, 29 Dec 2025 23:39:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c94e34c053e45a6dde16d3d661c85fc959c5fe3020d7229688284991fb19d7e`  
		Last Modified: Mon, 29 Dec 2025 23:39:14 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996cd48d977c9b15c2b3f49b08f2419f544a9b6779c598b8b16574b69a2d702e`  
		Last Modified: Mon, 29 Dec 2025 23:39:14 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0109bec1be4c87b9bc84a3df521d14238a7752d99fa71ba15d20a5a4590b8b5`  
		Last Modified: Mon, 29 Dec 2025 23:39:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:cf23ab32db8857491ac8a1a727323db271108f4b9559b3b6dc66db310b1019c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d65840bc04b24fd53de9ee6090b8c1977d7d6ccd78f44ec143bb457f8c134ed`

```dockerfile
```

-	Layers:
	-	`sha256:f7342a2fb7edd2647801e404e9ed95bd2641f7536835dbc755bb4d9ff3b32a5a`  
		Last Modified: Tue, 30 Dec 2025 03:09:47 GMT  
		Size: 5.6 MB (5642238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a99616e51a769c131150b13458f67ef740a729837e5d2d764a13d34fe1bb5e8`  
		Last Modified: Tue, 30 Dec 2025 03:09:46 GMT  
		Size: 53.9 KB (53864 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:01c5565b6cf46e780ce2d4f247fe95f96f5b1b71dbed0107a37e181f9ae9df6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (152037990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecaff1f5abe6545953ebe0c33a09732b5e0be6812925f80f5efb644659b80c52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:52:15 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:52:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:37 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:52:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:52:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:52:45 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:52:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:52:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:52:54 GMT
ENV PG_MAJOR=15
# Mon, 29 Dec 2025 23:52:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 29 Dec 2025 23:52:54 GMT
ENV PG_VERSION=15.15-1.pgdg13+1
# Tue, 30 Dec 2025 00:23:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:23:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:23:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:23:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 00:23:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 00:23:13 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 00:23:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:23:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:23:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:23:13 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:23:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:23:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e850f62a6257da652b7369522fe607d0d78f4c48c02f42867e3017c68f2e2219`  
		Last Modified: Tue, 30 Dec 2025 00:06:37 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd376745726a267c1ce7f3184998639a1685ea72859dada65433bde5c167ed5`  
		Last Modified: Tue, 30 Dec 2025 00:06:37 GMT  
		Size: 5.9 MB (5929065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe4fef3ee4ab0f232dbcddd6497c28f0153abcd225a56cd3f3a09fe63dafbe1`  
		Last Modified: Tue, 30 Dec 2025 00:06:37 GMT  
		Size: 1.2 MB (1227402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75351a52f89f00ffb50fe56afabbdcc9737fb30781ed8b4eabcbec9a03f9ef5`  
		Last Modified: Tue, 30 Dec 2025 00:06:38 GMT  
		Size: 8.2 MB (8204158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28d05e776b81b11b8ad9a330341a67fe2dad5d5b8f873d2db7d04e9f0a814b0`  
		Last Modified: Tue, 30 Dec 2025 00:06:37 GMT  
		Size: 1.3 MB (1317181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d573d44d4e62c5a82b1c4a75d100364c5a4d5d8bb2c028e346ba8d4b3e05cc4`  
		Last Modified: Tue, 30 Dec 2025 00:06:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8be8b725526b42fe31a04308221dfb1cdd003936427d8cf047bb0e3c5030619`  
		Last Modified: Tue, 30 Dec 2025 00:06:37 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b377a4886554254b3a8960d39fc766811a215f41c66112d5b11b5147bb1f99f2`  
		Last Modified: Tue, 30 Dec 2025 00:23:50 GMT  
		Size: 107.4 MB (107395417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f39f01c0b842f66a1989faf5f36a019e680987b35fab834e872dee3cfae12ed`  
		Last Modified: Tue, 30 Dec 2025 00:23:40 GMT  
		Size: 9.9 KB (9878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2e99068392553b22918f996dd6ec97440d3de3171be6d3fd98cc9e86b48a4d`  
		Last Modified: Tue, 30 Dec 2025 00:23:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc75a8116b4e2304822a940d512be639727d81e0e2f02b480da3b6271ba49ed`  
		Last Modified: Tue, 30 Dec 2025 00:23:39 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8958302bf733e82eec4eb08a1ca093625b9db00dc4af9803532f6d3984f0e5ec`  
		Last Modified: Tue, 30 Dec 2025 00:23:39 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014e03f35ee07085e8656706bd5f7a2082579e901b05cebfcddc366518923f5f`  
		Last Modified: Tue, 30 Dec 2025 00:23:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:a6169bb5432558be37bba9d1296dffcb4f691b95bf3edfa0feebad59d9ff47d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5712963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e8be2339522f908c996b3a999f45908333eba2f9ca6ba990b5252bc37c6ee4`

```dockerfile
```

-	Layers:
	-	`sha256:70ec411127b38ed6ede0463179f7dcf1d4fe67a56209533eeec943c6ea1d6a33`  
		Last Modified: Tue, 30 Dec 2025 03:09:53 GMT  
		Size: 5.7 MB (5658876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a9f72c2bbf99bdeac35a3cc11cf67933fbf5bff071f68468397250a43998714`  
		Last Modified: Tue, 30 Dec 2025 03:09:54 GMT  
		Size: 54.1 KB (54087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:8e79a0f371a8b06a615c70ef0e9a426305833ca44e9bde91ac0cc9d899cf3d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147120773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c89faa1b828958efabad8678336f6e0164e5fedcfc411ce4a9940739923e06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:12:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Dec 2025 00:13:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:13:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 00:13:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 00:13:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 30 Dec 2025 00:13:17 GMT
ENV LANG=en_US.utf8
# Tue, 30 Dec 2025 00:13:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:13:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Dec 2025 00:13:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:13:23 GMT
ENV PG_MAJOR=15
# Tue, 30 Dec 2025 00:13:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 30 Dec 2025 00:13:23 GMT
ENV PG_VERSION=15.15-1.pgdg13+1
# Tue, 30 Dec 2025 00:27:33 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:27:33 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:27:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:27:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 00:27:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 00:27:33 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 00:27:33 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:27:33 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:27:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:27:33 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:27:33 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:27:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4644ca96dfc259afeb6aefa33b8960f9f877d0d78fd86a980e39a61c69a56e0d`  
		Last Modified: Tue, 30 Dec 2025 00:28:01 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de95bf388457e25c615316a00ad0debf028b52448d8dd0479123d5a9f6c260f6`  
		Last Modified: Tue, 30 Dec 2025 00:28:01 GMT  
		Size: 5.5 MB (5496819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63321e03ba3437a97a4af4d2c7c49ad567038ab59b370999a7f08bf0b585ae8b`  
		Last Modified: Tue, 30 Dec 2025 00:28:01 GMT  
		Size: 1.2 MB (1222274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e208debb1e339bcbc4b78f880381f3f23395c21665007a8990ef9d2de9cf923`  
		Last Modified: Tue, 30 Dec 2025 00:28:02 GMT  
		Size: 8.2 MB (8203950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e721b69df4e49537b44c03e0f38e8372f99e6aba22f312780d7fa3e101f26a`  
		Last Modified: Tue, 30 Dec 2025 00:28:02 GMT  
		Size: 1.2 MB (1172486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d9601f68978a0384ef14277946317e74e981909e4c24f723752bac38d79b95`  
		Last Modified: Tue, 30 Dec 2025 00:27:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f2654333f9b7e2125dc2b5a382a52e03f0f27576954dd5e2eeb5ff3e7b3b09`  
		Last Modified: Tue, 30 Dec 2025 00:27:43 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2357185cf0761f078dbddda0f86bbd376b1658bed0f3efbf6cc3eb1a62a670`  
		Last Modified: Tue, 30 Dec 2025 00:28:11 GMT  
		Size: 104.8 MB (104794610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae01cc6bbdb340cd355fe9602d6022f8a1e30e2ef52e6527614a0c3642c0f05a`  
		Last Modified: Tue, 30 Dec 2025 00:28:01 GMT  
		Size: 9.9 KB (9889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edff8dbbe1026c6b9bc32f99d680acb80092e46a040825490a5cda13cc1a333`  
		Last Modified: Tue, 30 Dec 2025 00:28:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5472d3c37bc801915760e6672e56b8c5a61241cd57c862c5ee751280090b50ff`  
		Last Modified: Tue, 30 Dec 2025 00:28:01 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863c9e47007f8403a5c598f22f90175c9871feeeba668cd0c535900050d4e1a6`  
		Last Modified: Tue, 30 Dec 2025 00:28:01 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e5a050eace0e3a39cfb0ad5599318dde4b838148887f7a900a4f18bc09e198`  
		Last Modified: Tue, 30 Dec 2025 00:28:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:a3425a2574527987b52eca708f5c99f67cb684a6a998d317aaa2073a8fbea7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5712268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b023a2cb74d2323023956194a78e4ca8b763e313e6367a42d0550123c88802b6`

```dockerfile
```

-	Layers:
	-	`sha256:2f3733458135544fa5f9db5ce0a7edb51e18e7842986b6f84ff7e69db85f4933`  
		Last Modified: Tue, 30 Dec 2025 03:10:00 GMT  
		Size: 5.7 MB (5658181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53da2a00e3b21153f2208207fe1903e31f1ac11cf847970d324d4abb4ea9a49b`  
		Last Modified: Tue, 30 Dec 2025 03:10:01 GMT  
		Size: 54.1 KB (54087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f92fc477208f31212b628fed4a106d592ccb9338d96dc7ce0e8d4b66414ed875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156639974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6820459072b17efa86f52cf9341f9fc62e1ac6e8f08260dd53a48d52d41fa6e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:41:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:41:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:43 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:41:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:41:49 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:41:49 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:41:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:41:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:41:54 GMT
ENV PG_MAJOR=15
# Mon, 29 Dec 2025 23:41:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 29 Dec 2025 23:41:54 GMT
ENV PG_VERSION=15.15-1.pgdg13+1
# Mon, 29 Dec 2025 23:42:10 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:42:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:42:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:42:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 29 Dec 2025 23:42:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 29 Dec 2025 23:42:11 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 29 Dec 2025 23:42:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:42:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:42:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:42:11 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:42:11 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:42:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084c52268cd11ce19a3ace212b88de45663bbf475335ee0f62ef6b09bfb1b646`  
		Last Modified: Mon, 29 Dec 2025 23:42:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cdcbdc70dc3b913d8c1fbb7e33005722588d6dd2645777c4f5fd150db815cc`  
		Last Modified: Mon, 29 Dec 2025 23:42:41 GMT  
		Size: 6.2 MB (6232056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfa681b6db6390cdaa3b5fd91c0f22a7ef72883885a01e84f1b754966444b5d`  
		Last Modified: Mon, 29 Dec 2025 23:42:40 GMT  
		Size: 1.2 MB (1209469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617dcfc3612f53b631b5d3d79c5799c3bfeae34bb9e43255a82a9baf8f89b917`  
		Last Modified: Mon, 29 Dec 2025 23:42:43 GMT  
		Size: 8.2 MB (8203936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5af95753dae9b28a6596c6b45aa6622e10dbbc2e82bd37dd35febb0a026d481`  
		Last Modified: Mon, 29 Dec 2025 23:42:41 GMT  
		Size: 1.2 MB (1220461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5b59cd57104f0062dc15a4c3d697f022b20783cf58d330f3d4e5bd98376ba7`  
		Last Modified: Mon, 29 Dec 2025 23:42:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d71446181885659a707b66567be64678e7c1033254bfaaaec5f78146d1b125`  
		Last Modified: Mon, 29 Dec 2025 23:42:41 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6233ea4081aae65a9be7c1955d591d1caafa6f5eff0702f1aa4819a4b63db4dc`  
		Last Modified: Mon, 29 Dec 2025 23:42:48 GMT  
		Size: 109.6 MB (109614791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2aaf8ba81b95b6d2f2e257b64942a15ceba34cb0f3d2dda99522b5d62e5bcc`  
		Last Modified: Mon, 29 Dec 2025 23:42:41 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92d63d0be94825bad9ff13459993e0a3b654e528edf2a42c2274a4520214f30`  
		Last Modified: Mon, 29 Dec 2025 23:42:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b0eb009d27bad73606f259589cf91eec3c48994967ae3110fce315dbe77e4e`  
		Last Modified: Mon, 29 Dec 2025 23:42:40 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff12209423a3c476bc0436ad0dc86c4517d8cf28aad66b89778e7793402ac82`  
		Last Modified: Mon, 29 Dec 2025 23:42:40 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf11e64167d40e3d32dc010bae69316438822d312c9eea910b36731ad4ab42b`  
		Last Modified: Mon, 29 Dec 2025 23:42:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:5b404871134889869a981adf445b9968e9ac9a6333c188937af4ce046a0a4d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7962e5931daaf08703db76fa7690fd76d0d465707fe71c1622ede8fe3be7a1e1`

```dockerfile
```

-	Layers:
	-	`sha256:7534f1f14cda273b9b58aeee4ad84911ba41d595d49a2dbf7aea97f625123d77`  
		Last Modified: Tue, 30 Dec 2025 03:10:02 GMT  
		Size: 5.6 MB (5648584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c78e35b1a4869894c0a73b7edb559b0ff8f0b83156f1cdb251d65e8df0d5d2b`  
		Last Modified: Tue, 30 Dec 2025 03:09:55 GMT  
		Size: 54.1 KB (54133 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; 386

```console
$ docker pull postgres@sha256:a4ee90c0d6c0ee22e1b5fc1f507e91cf2869ac02adacee4f50eafc7e5a20832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167107949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d01a27189ac700b9fe7ec5e492eabb91488fba1fa068048a68476f506cfb020`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:34:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:34:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:34:56 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:34:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:35:02 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:35:02 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:35:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:35:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:35:06 GMT
ENV PG_MAJOR=15
# Mon, 29 Dec 2025 23:35:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 29 Dec 2025 23:35:06 GMT
ENV PG_VERSION=15.15-1.pgdg13+1
# Mon, 29 Dec 2025 23:46:49 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:46:49 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:46:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:46:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 29 Dec 2025 23:46:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 29 Dec 2025 23:46:50 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 29 Dec 2025 23:46:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:46:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:46:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:46:50 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:46:50 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:46:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387e2945f5d9380cf9206b62849ec33af96b84004f8fde479fd741bd523a1cdc`  
		Last Modified: Mon, 29 Dec 2025 23:47:22 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4c1efb01771e31b3e437e54e61ccbac2a812148f1e861dc0d439528612896a`  
		Last Modified: Mon, 29 Dec 2025 23:47:22 GMT  
		Size: 6.6 MB (6629537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae6c5bac8e706cb333b9a8cc4d53404d13b5e41405cf604e6a1c6d69512f8c8`  
		Last Modified: Mon, 29 Dec 2025 23:47:22 GMT  
		Size: 1.2 MB (1225693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5891188c83d02375c60b77e768280b8b091b3fb2c1ddebe5199c98688d74aad`  
		Last Modified: Mon, 29 Dec 2025 23:47:22 GMT  
		Size: 8.2 MB (8203976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377a54d59a9db4de67addcaf357d7e06ec13b80f446db587f2902bae40c2d285`  
		Last Modified: Mon, 29 Dec 2025 23:47:22 GMT  
		Size: 1.3 MB (1308189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f53a244e912587e78b7cc194f659bb152637daf61083b6f8a621fedeabaf15`  
		Last Modified: Mon, 29 Dec 2025 23:47:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d5f56945695ddd5fab8f9cffda4637d50d0e713706c7a50ec754e924c1f01d`  
		Last Modified: Mon, 29 Dec 2025 23:47:22 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227dbac6e5891b899c22354404c0571ca4fa3e9c74a7f6c346c97fe5c77ae889`  
		Last Modified: Mon, 29 Dec 2025 23:47:34 GMT  
		Size: 118.4 MB (118426833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff40d1655a55c4f2db198e1511ef396dcfd49fd91a1c12322aee41d39c9ddc37`  
		Last Modified: Mon, 29 Dec 2025 23:47:22 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d462a13208834ae849c51b76252814895c98e71fbad2b6d0fa38646036c314da`  
		Last Modified: Mon, 29 Dec 2025 23:47:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cc30a60efc831637576318b12874100c5110e0ae581543642e99eaf6cc0404`  
		Last Modified: Mon, 29 Dec 2025 23:47:21 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159628866ed3abb87dc6cc2044d26f58a32165d869b34a5451facd64ea02f2fb`  
		Last Modified: Mon, 29 Dec 2025 23:47:21 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e2f1e95f0a44b35d767536dc19d4b516cbfc22419987e56f709c91e82dc279`  
		Last Modified: Mon, 29 Dec 2025 23:47:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:d09adb4984023eca6d13554977cb2f770ad5d17ef5255cb0bacf2e2dfe569ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5711579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22c0ce868e0b7826d8f4bc9d99751641d71cbaa84e30470eb2b38568df40bdc`

```dockerfile
```

-	Layers:
	-	`sha256:6689f61e1ead99ec88b5426e60b7cd7267102463a3e9a332ccc2fd047b481a0d`  
		Last Modified: Tue, 30 Dec 2025 03:10:11 GMT  
		Size: 5.7 MB (5657769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef7998ba1ab2bf39b4877c45a228d0e1535a6ef29364bb71fd950699093ce79`  
		Last Modified: Tue, 30 Dec 2025 03:10:12 GMT  
		Size: 53.8 KB (53810 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:6ba819c02ba8f11e4e339de8b4a2f124d40e23f1cd5d3233a3dee6f4b89fa69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170236394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913f777d223dbb99d17d4704c4178e637284a74b9d5eb80032793fd972b03149`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:58:21 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 09 Dec 2025 01:58:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:58:57 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 01:58:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 01:59:09 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 09 Dec 2025 01:59:09 GMT
ENV LANG=en_US.utf8
# Tue, 09 Dec 2025 01:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:59:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 09 Dec 2025 01:59:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 09 Dec 2025 01:59:18 GMT
ENV PG_MAJOR=15
# Tue, 09 Dec 2025 01:59:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 09 Dec 2025 01:59:18 GMT
ENV PG_VERSION=15.15-1.pgdg13+1
# Tue, 09 Dec 2025 02:03:50 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 09 Dec 2025 02:03:51 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 09 Dec 2025 02:03:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 09 Dec 2025 02:03:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 09 Dec 2025 02:03:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 09 Dec 2025 02:03:52 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 09 Dec 2025 02:03:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 02:03:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 09 Dec 2025 02:03:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 02:03:57 GMT
STOPSIGNAL SIGINT
# Tue, 09 Dec 2025 02:03:57 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 09 Dec 2025 02:03:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e1e14f4d7b041df9ac5fc8de0576537ea278840427d10e9148c696adb70b27`  
		Last Modified: Tue, 09 Dec 2025 02:01:24 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3745b8a53abf95c5c0de5c32dfcb3b3374ddf07ef91fc46c33e5a7e1f1067d0`  
		Last Modified: Tue, 09 Dec 2025 02:01:24 GMT  
		Size: 7.1 MB (7075970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce494898a07197b6881a493ab77d6aff68197d81a66bc208117b16f056aa1f9`  
		Last Modified: Tue, 09 Dec 2025 02:01:25 GMT  
		Size: 1.2 MB (1214722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1cb5cce5854f2b159fd846f364b0dae1a7331a6356d92a487d5c5a537f77b9`  
		Last Modified: Tue, 09 Dec 2025 02:01:24 GMT  
		Size: 8.2 MB (8203970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c04d390fdc287bfc38e367f6ac75664b0147a2e4bff0ec697269892c4c096b4`  
		Last Modified: Tue, 09 Dec 2025 02:01:23 GMT  
		Size: 1.4 MB (1394831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe9c5eb03727d2f38c3eb284ce3f107244d3441c38b3c9186ff8d0f4b13e481`  
		Last Modified: Tue, 09 Dec 2025 02:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec249543bac7d8464c12595e55a8805f97a5535503ed82d2633b4a943e1b120d`  
		Last Modified: Tue, 09 Dec 2025 02:01:23 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ce0fb9a8bf3461ddd64aef4f1f1b83a3b21de93c35ac198fc642c15cd7ee6c`  
		Last Modified: Tue, 09 Dec 2025 02:05:01 GMT  
		Size: 118.7 MB (118729396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700a68795e625d040a7ddee83eb4e12ae1c327bbdf8ea73fd39071debeb28bb5`  
		Last Modified: Tue, 09 Dec 2025 02:04:52 GMT  
		Size: 9.9 KB (9877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d3fa65d60082248cb3a656c8ae0ee9bf0648a5bacc45bb72f943210e13d65c`  
		Last Modified: Tue, 09 Dec 2025 02:04:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef7e9565086b15b2e47b2c5369ed32c784faf6deaf31bba4ba34c2d78034376`  
		Last Modified: Tue, 09 Dec 2025 02:04:52 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62db5884f1ce79c2833c06184b19e97bacb3fe4136b085ad0e46a2dc0b684cc6`  
		Last Modified: Tue, 09 Dec 2025 02:04:52 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1d9a7412615d5c6d618cc9a5ab87b42956923d7ae42b0746251be2048c1abd`  
		Last Modified: Tue, 09 Dec 2025 02:04:52 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:7f0baf973560387e7e0da9da953d990bbb4a14d7101f226fd4e34226b0ea64b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b9d83a6f1228c3cfd0f45ab4639c3bce831ade72c73d164fcc78f93d6f2f91`

```dockerfile
```

-	Layers:
	-	`sha256:7ad9eabf444ab5f45352ddf87be11a2540c8ade91f7e6e0e38b9475e412f35bf`  
		Last Modified: Tue, 09 Dec 2025 03:09:30 GMT  
		Size: 5.6 MB (5648851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbbd5694a8b7abc77575dd9dfde600e047bfe098db9ecd3539e91163fe545f3`  
		Last Modified: Tue, 09 Dec 2025 03:09:31 GMT  
		Size: 53.9 KB (53929 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:3cfea03c231c3ed8ffd6db145a57dedcd55aa1c82f5125eb266360df0d8e43d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89986710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ff0a037fe762aad35610ff35d4c1006ed40520ad59d051560be64a78615a26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 10 Dec 2025 13:55:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 10 Dec 2025 13:56:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Dec 2025 13:56:59 GMT
ENV GOSU_VERSION=1.19
# Wed, 10 Dec 2025 13:56:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 10 Dec 2025 13:57:58 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 10 Dec 2025 13:57:58 GMT
ENV LANG=en_US.utf8
# Wed, 10 Dec 2025 13:58:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Dec 2025 13:58:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 10 Dec 2025 13:58:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 10 Dec 2025 13:58:38 GMT
ENV PG_MAJOR=15
# Wed, 10 Dec 2025 13:58:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 10 Dec 2025 13:58:38 GMT
ENV PG_VERSION=15.15-1.pgdg13+1
# Thu, 11 Dec 2025 02:06:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Dec 2025 02:06:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Dec 2025 02:06:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Dec 2025 02:06:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Dec 2025 02:06:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Dec 2025 02:06:18 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Dec 2025 02:06:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Dec 2025 02:06:19 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Dec 2025 02:06:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Dec 2025 02:06:19 GMT
STOPSIGNAL SIGINT
# Thu, 11 Dec 2025 02:06:19 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Dec 2025 02:06:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7509a6e61e937d2861e580aee3645ccc284662e5ff785c3a9eb5fea93cf517b`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd637312070c560044a9b139cf8983fb8e39b5f60b3c51a2c557980815f7101`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 6.3 MB (6291355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7b1b0d8d9bb5d10b5a2d66ecee216d2f1cae8a593baa99e14a05f9eed3afbb`  
		Last Modified: Wed, 10 Dec 2025 16:03:48 GMT  
		Size: 1.2 MB (1201916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cfccc2a828efdeee76cdfc0241a7a2253c5d5e7ec9c2770454a9f217a9c55a`  
		Last Modified: Wed, 10 Dec 2025 16:03:48 GMT  
		Size: 8.2 MB (8203580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87922f2a83f8c445248a001ee77716a207d176d413c183b77f66b22eb3c3aae`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 1.4 MB (1402222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f877525412689d6256ebb5cd6dd6649d1f971ed1a240aa789cd7554715346e`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4086fc5e0163b1fdce9acbb9093daa90b18ab170c9c52c4e31bea0af44599c`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5543060be4132ddfb8af3d917081b92305a7adce455bfb4a1dce8c2f55b07c86`  
		Last Modified: Thu, 11 Dec 2025 02:09:09 GMT  
		Size: 44.6 MB (44593852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f409ee4a701e94fa36e7f6cc3b60791811a4fa10e9dfda7a904bae1bed6de5`  
		Last Modified: Thu, 11 Dec 2025 02:09:04 GMT  
		Size: 9.9 KB (9889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16dc75b17ca489b056cd6670e761af99e5e1cab63f9f2178d06b7e55909a9852`  
		Last Modified: Thu, 11 Dec 2025 02:09:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d5f073095b32a4268e5cea4b0f4b6a226ac7beb59c1bbcabc9ab0c9d5b728d`  
		Last Modified: Thu, 11 Dec 2025 02:09:04 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1da3c13cb02c594c29fff041b95b7ad0f38420fba4ff131059171b57e4da97`  
		Last Modified: Thu, 11 Dec 2025 02:09:04 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951ec8e2e21bbb0f88a09625d3bb4e31627d4d7cba76a3878b3c60d5f85a10ef`  
		Last Modified: Thu, 11 Dec 2025 02:09:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:e764157d7ca730f037cff75c1d4b945e4057cd58a68d4cd414f4c27c0f6177bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007ab8d19ea7a0d9f774806f9aa628c7fe03f47f1c0b72756d065e014b41cc71`

```dockerfile
```

-	Layers:
	-	`sha256:1b02eed30375ce8e03d94a4b13599e9a6f485fa0d843ab7cc499c3e2b52a3a7f`  
		Last Modified: Thu, 11 Dec 2025 06:08:20 GMT  
		Size: 5.0 MB (5020284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b91e7dda0fc4284bac2527fd69c94126ccefac94afbee50788823fa5f84d748e`  
		Last Modified: Thu, 11 Dec 2025 06:08:28 GMT  
		Size: 53.9 KB (53924 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:8068e065e6f4f19e4ee3799f75ec03bd75ae73ff72feb259b2c67797af1d9ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172541277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a069b42946c7f275fe52010dd24f4094704bf0fb64c3b46b81a410bbed505bbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:04:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Dec 2025 00:04:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:05:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 00:05:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 00:05:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 30 Dec 2025 00:05:05 GMT
ENV LANG=en_US.utf8
# Tue, 30 Dec 2025 00:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:05:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Dec 2025 00:05:09 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:05:09 GMT
ENV PG_MAJOR=15
# Tue, 30 Dec 2025 00:05:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 30 Dec 2025 00:05:09 GMT
ENV PG_VERSION=15.15-1.pgdg13+1
# Tue, 30 Dec 2025 00:29:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:29:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:29:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:29:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 00:29:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 00:29:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 00:29:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:29:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:29:44 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:29:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:29:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3871b04fd556bf546f070d934db142337040c1511e3993155fbfe1b2a7634d`  
		Last Modified: Tue, 30 Dec 2025 00:17:45 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a22bb0424d78630989ba61697f63f36155b542447b51fd8205694c0bfae570`  
		Last Modified: Tue, 30 Dec 2025 00:17:46 GMT  
		Size: 6.4 MB (6408712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48877a21f32883b0a473d58a5d3c2c725aedb82b2063afa607854986510aecc`  
		Last Modified: Tue, 30 Dec 2025 00:17:45 GMT  
		Size: 1.2 MB (1230035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530be41059554fec340cdeb8c6874c135df35f2d394347a3031f0e6999c613c0`  
		Last Modified: Tue, 30 Dec 2025 00:17:46 GMT  
		Size: 8.3 MB (8258850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5995d222c1d70da51ec536a837e683068ac69adc87a709ed1c220518285e3d`  
		Last Modified: Tue, 30 Dec 2025 00:17:45 GMT  
		Size: 1.4 MB (1398084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47abd5cf66b8e0fdb183269061ffc0a0c0e12ba15edb77fca58d406d80c8a87`  
		Last Modified: Tue, 30 Dec 2025 00:17:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfcd45e433d8410ccbe5507dd1b556a0a8e1166f5ad3fbcdf97033490dec9f2`  
		Last Modified: Tue, 30 Dec 2025 00:17:45 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cb7f7d43e7dfc3c2740b0b11fb249319d75ccacfca59c8b6553a4405b8dbbe`  
		Last Modified: Tue, 30 Dec 2025 00:30:47 GMT  
		Size: 125.4 MB (125390555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7925f031dcb704bc86d2c047b63da02204b30a636b2b1b21c5a59fc93597072`  
		Last Modified: Tue, 30 Dec 2025 00:30:22 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c887d2ce9d20f22b4f6c8e669d9780fad1d002ec29a97fc80ab527725c12b6`  
		Last Modified: Tue, 30 Dec 2025 00:30:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb09a1b708d152d89e942e867d57c4447959272c8463d2b0adc2553258b63f0`  
		Last Modified: Tue, 30 Dec 2025 00:30:22 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ee4d3bbd4c4ee95a0362f630d601262bae4b024feed7d0c0b9b4ab383abcef`  
		Last Modified: Tue, 30 Dec 2025 00:30:22 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8aa2392dd8e34bf6d7ced709f3355c9c8bdbf1afb7f2f6bd41c77ef0da3e2e9`  
		Last Modified: Tue, 30 Dec 2025 00:30:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:0054ee12a6112757388934fc777e91c08f9cca7fd134263f732c37e37237bce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5712771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5225267d50e43c9633f1a62e1e4f8ebb6333b29aab9e3a94ee3ae1b3dfa1c6`

```dockerfile
```

-	Layers:
	-	`sha256:1ab7f16a29a4952ce4551c044066ba41b15713c401f1e1562f5175cb899cff3e`  
		Last Modified: Tue, 30 Dec 2025 03:10:46 GMT  
		Size: 5.7 MB (5658907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae015d4a108275aa4945c97e36ba41edc13080639965b70ec15ea67c515dbfd5`  
		Last Modified: Tue, 30 Dec 2025 03:10:47 GMT  
		Size: 53.9 KB (53864 bytes)  
		MIME: application/vnd.in-toto+json
