## `postgres:18beta1-bullseye`

```console
$ docker pull postgres@sha256:0739f5c34c677f25ad26a9b0b8c5e676fc0056bb91048412db79f970498cbcb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `postgres:18beta1-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:ccac009b16059d913ba0380472889c6139ebd89e41a243c94d11ded6e7aea7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149416774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641427307f4cbd1483d9c6fe214afa02b21435c38cc4740517dccfe4ff3251f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg110+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96705adc321bfc60e44661f9370271b2a3597dbc6aec3928352192f851126c10`  
		Last Modified: Mon, 09 Jun 2025 23:07:38 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c35db4db5d83245c815b5bfe15ffd8916238a0b7d912094043ca5bab8397d22`  
		Last Modified: Mon, 09 Jun 2025 23:07:40 GMT  
		Size: 4.3 MB (4308147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acce34404e6cd542f47de26c32908eefacdd400e17825eb67910df46560e7b8f`  
		Last Modified: Mon, 09 Jun 2025 23:07:40 GMT  
		Size: 1.5 MB (1473594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761383e7622c12fcb801816d7833907400140e86cf7611582126d3878f90869c`  
		Last Modified: Mon, 09 Jun 2025 23:07:41 GMT  
		Size: 8.0 MB (8045890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b312d66c28be8f5172367d964b08ef307645614e2bb172d197b98d312936cffd`  
		Last Modified: Mon, 09 Jun 2025 23:07:40 GMT  
		Size: 1.0 MB (1038337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a286d7707af618a53e7feb7740c919a5c0a3186d0ca11f6f65e3f11d7800a373`  
		Last Modified: Mon, 09 Jun 2025 23:07:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea59bfab59edb228f0e3c2f646b35a003b8d73f07c65fb9a25cd2cb70bbc67a`  
		Last Modified: Mon, 09 Jun 2025 23:07:40 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945328939e4e4b8ac5fa7c09db4fd5907bf4a38b904174f4abe28a09c75c0898`  
		Last Modified: Mon, 09 Jun 2025 23:07:47 GMT  
		Size: 104.3 MB (104264395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69f5cbb7c44f00a14d3dfb6cfe9ac55c0797203d77ae2ef1e9093e5c9e6317`  
		Last Modified: Mon, 09 Jun 2025 23:07:42 GMT  
		Size: 19.1 KB (19106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c858ffe3e8e260ffc58376bc2f2db14a809b5af63e09ba054ee722782927bfd`  
		Last Modified: Mon, 09 Jun 2025 23:07:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a2188ae3204d1aa3597f491c0db98129fe4326f48819d507b5cf35eeec8f5f`  
		Last Modified: Mon, 09 Jun 2025 23:07:42 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98bee02a156a540f935f85856b16dd8943e143d29ecf7e4b79c9549cbeee22`  
		Last Modified: Mon, 09 Jun 2025 23:07:42 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5957b71e3efa8e915f67a800a22930fc8f3a129b0f450692dbbb8d4d54c859e2`  
		Last Modified: Mon, 09 Jun 2025 23:07:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:04e0e3849731ee91b8d43de9abdbc35421e85de726774733f5555332278e3dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6531576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0758f7383e0bc6c75402abbfe859f1bad3ba34fa7c7f111e2445b17f30e232`

```dockerfile
```

-	Layers:
	-	`sha256:a9c6c231b42e2ed392c36b7ff31864da622494701f3909f12870381588b8949a`  
		Last Modified: Tue, 10 Jun 2025 02:09:43 GMT  
		Size: 6.5 MB (6477410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8c02d7b1779da76e5f2f066072d48f2635fdb25c9d9a6696421f726fb51702`  
		Last Modified: Tue, 10 Jun 2025 02:09:43 GMT  
		Size: 54.2 KB (54166 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:399ce08145da93b5d31fa4d0f48f1b1b74d04ac072e00178edde24582c9e17c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86659709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e096a63e39e604cad4a909c075a27ac66534d489656413acc003c355dc7c2f6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg110+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2091b63a268a34467e23520ae27c312421298f420abd278e760061e42a678899`  
		Last Modified: Tue, 03 Jun 2025 13:50:37 GMT  
		Size: 25.5 MB (25543902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2819feb174cd62d9afe4efa58f14c05d6404e45e9fd646186b5caf9e4ffb95`  
		Last Modified: Tue, 03 Jun 2025 13:44:36 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b854a91797948fa74505443fa76802d4719c60aea4cc87fd15783f71c9acfd55`  
		Last Modified: Tue, 03 Jun 2025 13:44:36 GMT  
		Size: 3.6 MB (3601790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6970d22b731c3a99427af1912f1730e34e40009bc7af854735159a9603ffa3f`  
		Last Modified: Tue, 03 Jun 2025 13:44:36 GMT  
		Size: 1.4 MB (1440887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a3cd249b6bf25ca9bbea16ab2a0959459eff6af0e43e16d8c956d2888065c1`  
		Last Modified: Tue, 03 Jun 2025 13:44:36 GMT  
		Size: 8.0 MB (8045791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d46adcc9f43b0fd86209d8380e586d2c3465d713fe7c68169a9b3899cfd39f0`  
		Last Modified: Tue, 03 Jun 2025 13:44:38 GMT  
		Size: 908.7 KB (908651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aa3404576c56b7e91cee8f6cec2f6cd80e371cbe93a5a27e90528f7ed08518`  
		Last Modified: Tue, 03 Jun 2025 13:44:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd2b53fdac06669f7ad19fd8504e96e7e1429ba317a634f81a63c8d05cc0b2c`  
		Last Modified: Tue, 03 Jun 2025 13:44:40 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497b906dc3ecba55959264695c98ca662c2b50a7f95285b1b85435a46d9ea25e`  
		Last Modified: Mon, 09 Jun 2025 23:30:22 GMT  
		Size: 47.1 MB (47088218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c97b61a611610accac08eeca6ca3d47b993d7644ee4ec2654c935725065b6e7`  
		Last Modified: Mon, 09 Jun 2025 23:30:19 GMT  
		Size: 19.1 KB (19108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee68a632c006ac10690bec59e011042759930d3e3514a7b7be9fda1bc94a6df5`  
		Last Modified: Mon, 09 Jun 2025 23:30:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52560061a59d583a7c286ff35885b918eb5e45c4da729f5668364a1d93eb519c`  
		Last Modified: Mon, 09 Jun 2025 23:30:20 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f7a7d60ddd6b688d391616d2ada84fd28ca946853db7f6abcfa7e1a3ff647d`  
		Last Modified: Mon, 09 Jun 2025 23:30:20 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b073d077539498da0ce1076dfc75dec762f69dba735d4c0b96f362b910eed0b`  
		Last Modified: Mon, 09 Jun 2025 23:30:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:76aabfe62bee526650fa66f59ac736b7b5f840b6e16acbf5d5ce00db1f317994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5685178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0e98486af5e8ca37c233e72c2b621b949b4c64ad3053194609660a9a39332d`

```dockerfile
```

-	Layers:
	-	`sha256:d05e29e4ce9f4dbcca4e5db75834869a46541b18ce93e49c57b792b7e0da1ab6`  
		Last Modified: Tue, 10 Jun 2025 02:09:49 GMT  
		Size: 5.6 MB (5630831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb0bbcfb6c96dab79afed7775f82ba17ea1cde697e37f07bc5ccb7eecd8f4471`  
		Last Modified: Tue, 10 Jun 2025 02:09:50 GMT  
		Size: 54.3 KB (54347 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3710d1f47c3b58c514249ef49bcb5df16e8f569013a3d21ef44e32e45691f6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146422419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c82400e45d033f7557a20b8dabfa4bb1fd414694075ef013499bf721503415`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg110+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade30debac6fbfee61ba0a16cd7cd4a5a2362d0bc00349c425dcae0dbdc27315`  
		Last Modified: Mon, 09 Jun 2025 17:22:47 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b2a1907d3ca81f8fe755299114cc82d225ad26738e3ab6eb8ef3ef4fcb6ade`  
		Last Modified: Mon, 09 Jun 2025 17:22:52 GMT  
		Size: 4.3 MB (4312864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca74376c9de08cab66a966e2fb5d4eee65048765c129b48c8917a07ea47f49a`  
		Last Modified: Mon, 09 Jun 2025 17:23:12 GMT  
		Size: 1.4 MB (1405880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71517e9a8976f9812c6a92b3f26c890109ce95ad52e22925c6351c134dd5e00`  
		Last Modified: Mon, 09 Jun 2025 18:18:05 GMT  
		Size: 8.0 MB (8045811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea5c166f2e4f6a970930938e7e729cc4127254877c529ff44b5f338b8c868e8`  
		Last Modified: Mon, 09 Jun 2025 17:23:19 GMT  
		Size: 1.0 MB (1026592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb977ec5c7a895b3243c2ee24b985aafd1736c73c773d725f88b6f279149a05`  
		Last Modified: Mon, 09 Jun 2025 17:23:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420c61493954d856ffbbade5169251a9c95f0084c9754b65f942342160aa7ba4`  
		Last Modified: Mon, 09 Jun 2025 17:23:29 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab084f025f3a82c7ac676b0679895114028211d9f3170d8b1db28893a5b9b44a`  
		Last Modified: Mon, 09 Jun 2025 23:07:57 GMT  
		Size: 102.9 MB (102854541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a524a3c8fc2036009cd627308f492f01f0d6b43fc4ee9991725a590fe823a0`  
		Last Modified: Mon, 09 Jun 2025 23:11:54 GMT  
		Size: 19.1 KB (19106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5879bd48c1aceb68eaf1ef3fc6d2cdb89de08f58ff6ebbb208850e36f3bbe1`  
		Last Modified: Mon, 09 Jun 2025 23:11:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e6a17c4b798669c61c844076eb5462b0345c3497abaf048486609011dd37b3`  
		Last Modified: Mon, 09 Jun 2025 23:11:59 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de21bca97a05c6d0267f9cb3b214dd004377a4fa42f670cf9a5434350a5ac55b`  
		Last Modified: Mon, 09 Jun 2025 23:12:02 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9144583cf9c134aa64808edb8f3abc206b731497149284156594471b467d38`  
		Last Modified: Mon, 09 Jun 2025 23:12:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:696779c7a796545933e840a3eafeae9cf8327a00ee374187a04cdac19823bf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6538087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880006d775d8b62e2e4d15c8faceda66f6ea8f10c5c93043454399ca9c2ca819`

```dockerfile
```

-	Layers:
	-	`sha256:b22af22cac6c24603c5b129e86f183e284faf61d0194f69e7c5396822a369528`  
		Last Modified: Tue, 10 Jun 2025 02:09:54 GMT  
		Size: 6.5 MB (6483687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16bdbff3e0d0b4664d446a50b41e21e9fd49bf5753b8a788954683c44a7e6025`  
		Last Modified: Tue, 10 Jun 2025 02:09:55 GMT  
		Size: 54.4 KB (54400 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:b67121d9a60051fd8ebfcba0bcbc0a5ed1ea753cc172f69b5347cdbd4c1962f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98034277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246cfe73d7f5b23e4c1b8815c7fc524be464743f7b1d555de843dd4b1f35c8cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg110+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Tue, 03 Jun 2025 13:42:18 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bb0f8c894e3a98da194940cd4da80be8e24d7c4488197242c6513f7d591e3a`  
		Last Modified: Mon, 09 Jun 2025 23:16:26 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfccce295ae179f4abde8429090263e0fafcf99a74be4b18829bf87e0bed1a38`  
		Last Modified: Mon, 09 Jun 2025 23:16:27 GMT  
		Size: 4.7 MB (4719671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0051aea083949ce3d939654bd3f8646e6f9e3f65fb7bae439ad598c02dcaad`  
		Last Modified: Mon, 09 Jun 2025 23:16:34 GMT  
		Size: 1.4 MB (1449317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc05299b4e6702013a3d8af4dea70b35fa835b5fe14c1ce5efa22fe4f02a471c`  
		Last Modified: Mon, 09 Jun 2025 23:16:28 GMT  
		Size: 8.0 MB (8045804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d1f2f699a166c0448a37ef6db01e60b2c3cc1faaaf1cd1f0b005849e9d454e`  
		Last Modified: Mon, 09 Jun 2025 23:16:28 GMT  
		Size: 1.0 MB (1028925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90d66a007be8041e43fe36e1c88ff85d5b257c65a11ed572c2f854cb2e9efdd`  
		Last Modified: Mon, 09 Jun 2025 23:16:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0208f22132eb7a002bce4ba5c18e5102abd0bf5c00e57cb600e707940080ae9`  
		Last Modified: Mon, 09 Jun 2025 23:16:28 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad0ab99bb68c5593ba01c6355bb0e34b6713878b9ce84f5b0db21e1e0357505`  
		Last Modified: Mon, 09 Jun 2025 23:16:32 GMT  
		Size: 51.6 MB (51570883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa1f554700633d2c8f8d11a56c93542e059c4ba5f32f85f93fbfe7610ab6ea5`  
		Last Modified: Mon, 09 Jun 2025 23:16:29 GMT  
		Size: 19.1 KB (19112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe0b8184a88b99c5c568297fbacfa1fbda0be93e2669d2db09609e27fa9a9c1`  
		Last Modified: Mon, 09 Jun 2025 23:16:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4188d7e377c474f432b11c7d2e9da31e1f36aca89ef8c881c7706799058014c5`  
		Last Modified: Mon, 09 Jun 2025 23:16:29 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06b879b1a8af3afbc0bd3f5d26c34a2d95eb95c0c57aeec954c5d951b7b7ec6`  
		Last Modified: Mon, 09 Jun 2025 23:16:29 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6eb333852ddb3f4c67aa739c9619a9b73dfdd7b1f2f029878720aed71d76e4`  
		Last Modified: Mon, 09 Jun 2025 23:16:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:8bf1a44257f54ad856bf605b88764b07df799cb00297918fac716ce067cda1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5679456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16a835ac2c258319bc4b72ad90f9e0ec8263d4eca7591e9e7d3ec31ff3ebb03`

```dockerfile
```

-	Layers:
	-	`sha256:1bd6ac1a3c1b20c19e1bdd80dbce73c4612a1daed60734b16a21e6f5794b1f86`  
		Last Modified: Tue, 10 Jun 2025 02:10:01 GMT  
		Size: 5.6 MB (5625334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:411466e5c3c6cb402c13a5f248278617b6aef0bd431654eb1c77e58550e96112`  
		Last Modified: Tue, 10 Jun 2025 02:10:02 GMT  
		Size: 54.1 KB (54122 bytes)  
		MIME: application/vnd.in-toto+json
