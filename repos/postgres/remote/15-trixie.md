## `postgres:15-trixie`

```console
$ docker pull postgres@sha256:1cd9dd548427751dc0fabb24a3bdf96a6dd08c0025a167ecbb5c14bec21ff94c
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
$ docker pull postgres@sha256:1c2eecbdc71b91d80846d3c6264af5e388fc9d353388e2e53903527338f5f1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158094627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d48187cc8a71167b6c8bb2b30230bf3badbaf0010a4426ca8e07af3eae038e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=15
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ed16669c95044564ab12a22761a11afa5390ccef28685dca22c4b645cf0ec8`  
		Last Modified: Mon, 08 Sep 2025 22:38:44 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e58066018376d571c33fb417518467e571bcf2411ba2adf303cf844c8b223f1`  
		Last Modified: Mon, 08 Sep 2025 23:09:44 GMT  
		Size: 6.4 MB (6436574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18445125df5f08dde20c0116e4b45f5b0a289c5cbb607502c253c057130165f`  
		Last Modified: Mon, 08 Sep 2025 22:52:24 GMT  
		Size: 1.3 MB (1255594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a3ca0fb792b4a8f9df6d849e4e3ac3d4bc85f6a874cad91474dd5a0677ab7`  
		Last Modified: Mon, 08 Sep 2025 23:09:44 GMT  
		Size: 8.2 MB (8203640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a0056e8c0596c1bc99293701caea250bcc910199b203351a3475de9b73cfdc`  
		Last Modified: Mon, 08 Sep 2025 22:52:24 GMT  
		Size: 1.3 MB (1311406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4494753109c05555675a4649f82c9b1b2a27573e3c91442bf2c58da2871279`  
		Last Modified: Mon, 08 Sep 2025 22:38:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9286f415f93ad8e267f2514f86d61ba78089f60f6ffb3814b28410375e8f1534`  
		Last Modified: Mon, 08 Sep 2025 22:38:44 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60570350e677e08d3c9fb2438caef37f81b41293ca77adeceee0b0507eeef8c2`  
		Last Modified: Mon, 08 Sep 2025 23:09:48 GMT  
		Size: 111.1 MB (111093206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b33c9cfc245eb13dae8dd0d9eb3b418dd80d85162c10dd23e0218d77d30e30f`  
		Last Modified: Mon, 08 Sep 2025 22:52:26 GMT  
		Size: 9.9 KB (9879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f082d788df98a6990f97b66ad474b40cf4d608c479c1569dc834c765ee24a30b`  
		Last Modified: Mon, 08 Sep 2025 22:38:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ae653469451641c5ae81f1b822d8bc5671fd144c1083673299b6875c9e1103`  
		Last Modified: Mon, 08 Sep 2025 22:52:23 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e69ab42557e3435700db665642881ed67ac4bf6cf425cf12270b098fa4e6f82`  
		Last Modified: Mon, 08 Sep 2025 22:52:24 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35e17a433deb963a2b77bb4af5a665445ff9fde9db97d1ab03899202f837872`  
		Last Modified: Mon, 08 Sep 2025 22:40:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:85256d1641ee95ad9951186b9a72ab6a3b1d3d53527634b39ca3dc1137e89836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6d518ad6930a1a134c09581ec3818d962b57f98af60840b6baf12ad3acb646`

```dockerfile
```

-	Layers:
	-	`sha256:225bd1599bb37550811d04e20f1ccd3e9ae6e98ffd84ef79adeee51fe71e8a0b`  
		Last Modified: Mon, 08 Sep 2025 23:09:49 GMT  
		Size: 5.7 MB (5724461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e930b2a678371c1d8e4b5f4bf2ba634f136fffa3b3a86186addb906dc68215f2`  
		Last Modified: Mon, 08 Sep 2025 23:09:50 GMT  
		Size: 53.9 KB (53907 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:8462a68e190814e6bb17f4edf5d4dbc3a7b4cefe7d0b1751119e219a1e22e91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152158857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b141197bdd187425801c66f604ea36c08d64e1cac4b7f21133f6758bd01485`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=15
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0addd5f441b0f2031662159755b9f5490fdcb2c4bdd9109f9562d135d1005120`  
		Last Modified: Tue, 09 Sep 2025 02:07:24 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3b607c8ae70c53c7320713d7e1bf193b8e6299b33901c309cb617fbeea88cd`  
		Last Modified: Tue, 09 Sep 2025 05:13:42 GMT  
		Size: 5.9 MB (5928911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee557f082ffd75050a78d80ea37f61a957f67dc7dd33e3afb1c3c2c02591b16`  
		Last Modified: Tue, 09 Sep 2025 02:07:24 GMT  
		Size: 1.2 MB (1226495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2110280258c83bbc53cfa00cda0f7484e6fc9c59c39f578d173406c7a8d51f15`  
		Last Modified: Tue, 09 Sep 2025 05:13:46 GMT  
		Size: 8.2 MB (8204068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0184fa3360cf545648b6adc2b5eb888f16126a01501c3c3b8e0e8eb25e39ddd0`  
		Last Modified: Tue, 09 Sep 2025 02:07:24 GMT  
		Size: 1.3 MB (1317120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55f679b80fdcf64230af6225ca5a2339c85fd3bd3f8198586b08120ca8396de`  
		Last Modified: Tue, 09 Sep 2025 02:07:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d58f24fddefcde5f842cfc7852b83a0b1cf8241c156bc3cfb059c44672a1ffb`  
		Last Modified: Tue, 09 Sep 2025 02:07:24 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4782fb3113407540a5477efbb686a2c25c0f1e289bbfc7b6eb30c9cebb4a440f`  
		Last Modified: Tue, 09 Sep 2025 05:13:51 GMT  
		Size: 107.5 MB (107519798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f587877ae0bd8c6b6bbd8df7a0e517524a2a48763e78db1f2c6005f538abaee`  
		Last Modified: Tue, 09 Sep 2025 02:07:24 GMT  
		Size: 9.9 KB (9871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95627c690342cf51fb726587576be0ae2a14e555dd45ff037f02166e9aed7b8f`  
		Last Modified: Tue, 09 Sep 2025 02:07:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f924467b1d1e34f34b54a7c8830c3160f11bed403afea850a510f4a922d9c104`  
		Last Modified: Tue, 09 Sep 2025 02:07:24 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5a5753510a253ae5538235104b4a26803a5601fa99b5bf8fec78395f90096f`  
		Last Modified: Tue, 09 Sep 2025 02:07:24 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99acf74676a0c1c659bfab563f987292fb2585d4bfed86e33033e920ed309cf`  
		Last Modified: Tue, 09 Sep 2025 02:07:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:56e3910b9e99475dc1fb8e486334530410c4f6e63a6e16a095d94474b43c3a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532421f7e57ac7f3d3548b1ae0ff3ab5916b0b11ae6e1d13bf52862929253db6`

```dockerfile
```

-	Layers:
	-	`sha256:6f720738c3d20b920c6dba54f277ca9d8283276055d3cb058b9d8a770ffbe0fd`  
		Last Modified: Tue, 09 Sep 2025 05:10:26 GMT  
		Size: 5.7 MB (5741103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b177e630b2b95fa7a8490133d9a338794f98a2846458d16d3e0d5c92cd0fd12a`  
		Last Modified: Tue, 09 Sep 2025 05:10:27 GMT  
		Size: 54.1 KB (54130 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:682f4fa84a574fef8c4f531561658047f6bc0f01d3af2b360496d0b3ef3b8367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147240757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b45fe65761cbf15264e75b019fdf6d5210c8e0703bc0d1682235f6c70ed82f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=15
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7624ffe80c22a9a25dc1002c21264d0582e5cf62cd0e22e93ffbf15725c4c556`  
		Last Modified: Tue, 09 Sep 2025 04:01:38 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44da1f248d1c65551a51c4966ed17d8cc6a540114653283d60ef7ae362a10e15`  
		Last Modified: Tue, 09 Sep 2025 05:13:24 GMT  
		Size: 5.5 MB (5496742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d401a20398f578089e71467aebe0ded797ee2f6c1958e1f500a16bab2117f8`  
		Last Modified: Tue, 09 Sep 2025 04:01:39 GMT  
		Size: 1.2 MB (1221709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cbc37ad1c26a4a3d04f3de602312ebdccc664d535b8624691be08d0dd3cb98`  
		Last Modified: Tue, 09 Sep 2025 05:13:29 GMT  
		Size: 8.2 MB (8203798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807d08d8ad33d6de7303fd88246b11c39bff0667fb7704e595995173df79e33`  
		Last Modified: Tue, 09 Sep 2025 04:01:38 GMT  
		Size: 1.2 MB (1172391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7b2127387c76b1937a146028e280df004cb75720ca7a26d8b210b9401dca4`  
		Last Modified: Tue, 09 Sep 2025 04:01:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c6cbac769d9dbdef640b2e35269273b5b1c10621e929e09fd0197b936a9d96`  
		Last Modified: Tue, 09 Sep 2025 04:01:37 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d43b7d3949ff410ca43f5e38ffaca539a85a03e69bd2c9726fa14bc011db03`  
		Last Modified: Tue, 09 Sep 2025 05:13:27 GMT  
		Size: 104.9 MB (104917548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15da41c2c2eb59655f1eaa5e210f58c510cb5e817d315dc3c82ac097aacd1980`  
		Last Modified: Tue, 09 Sep 2025 04:01:38 GMT  
		Size: 9.9 KB (9891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad48ab1f100e6442024ce3f034e474bd479a140603a55a1666c405ad49b7f63`  
		Last Modified: Tue, 09 Sep 2025 04:01:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab412f9656aff3c969d4d746c6e5f77ebb024f24cc81ba6f4de72c6248124f07`  
		Last Modified: Tue, 09 Sep 2025 04:01:38 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e630aeedf7d392ec719907b64060f67840cfcdc991db82c5cdd810a653a319`  
		Last Modified: Tue, 09 Sep 2025 04:01:38 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69c6d13fd2ff6e8d156e7d36c84656d523ce23dc67cf4cb8900e4895ef2cfaa`  
		Last Modified: Tue, 09 Sep 2025 04:01:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:92da0f37edaf30b0b5659ac91c409b3a90ecd664d852835e22ac06ed57ef99d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b62ecb460c9dc72de2a779041f6699eea0051d59a93c5b9eea81e3cd2156a5`

```dockerfile
```

-	Layers:
	-	`sha256:8d1cce786cfa10a14bb27873f74e048606f77f1f1c29e24f814da03e70d22dd5`  
		Last Modified: Tue, 09 Sep 2025 05:10:33 GMT  
		Size: 5.7 MB (5740416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:263099721a5a2cbba1fca2893690ab3b4dd56e7aa63b5a4dc758e3672fdd8826`  
		Last Modified: Tue, 09 Sep 2025 05:10:34 GMT  
		Size: 54.1 KB (54128 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b51b7af2d97ef07780db0d5ca2fe057b2f8dcff7330bba0e1dc441289b1798ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156722650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c313505763e7ef5e2797d6db99a3e731820ff760127d97c0e532760fcf786db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=15
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da1c7240a39538d16f0ec3b7c29c293360b5898d3ad94f4ae82efde61927055`  
		Last Modified: Tue, 09 Sep 2025 01:59:55 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7110de33e2822f35fc9ec57d5ac9908a2fa818c6cd73fe3d2de889db478a380`  
		Last Modified: Tue, 09 Sep 2025 03:00:15 GMT  
		Size: 6.2 MB (6231898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a04620f84544d1e5a6279cfcbda7be923e3f3899a7b383753662678576727a9`  
		Last Modified: Tue, 09 Sep 2025 01:59:55 GMT  
		Size: 1.2 MB (1208674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2673eb93ed9e68fdaac30997d6628324c28e529a08225ef722da27868b4baeb1`  
		Last Modified: Tue, 09 Sep 2025 03:00:18 GMT  
		Size: 8.2 MB (8203812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016a80734744c6cc00497c988c0bc4161436de2176a5994b93edd069e4d1eeb4`  
		Last Modified: Tue, 09 Sep 2025 01:59:57 GMT  
		Size: 1.2 MB (1220406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b2004d7dedce4f3d57b54b588bb30b9fe2b78d58a0a386fd630bb412581bee`  
		Last Modified: Tue, 09 Sep 2025 01:59:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347920de26f3aee18b364b76ace24af014817df47227c2f1d87c71d6e51b0e49`  
		Last Modified: Tue, 09 Sep 2025 01:59:55 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61361295790e98d6d9069d3b8e88ea0db4cf9aa522ef3cf2b2fadbc61b34167`  
		Last Modified: Tue, 09 Sep 2025 05:10:28 GMT  
		Size: 109.7 MB (109700522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70ba1e7b6067a88b73a62329208e914a8a55fbc4d48b9b8070a69f8de02ad08`  
		Last Modified: Tue, 09 Sep 2025 01:59:54 GMT  
		Size: 9.9 KB (9877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5027f749dcef8562588d068e5c1fda24eb064caba0a5346c13a1c2c283e53d11`  
		Last Modified: Tue, 09 Sep 2025 01:59:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f048a26e6556afeb5869f6b37217f30cd1f5724c3d278f8b77aae7ed4a18ecc`  
		Last Modified: Tue, 09 Sep 2025 01:59:54 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582b924004c52020a38820548ac16e9292c974ef037cc4bb39d122df3637b8d1`  
		Last Modified: Tue, 09 Sep 2025 01:59:55 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2177ca3c5f7d53bc88331d298d19afd1fc601214c35d70be5b31458ee485062f`  
		Last Modified: Tue, 09 Sep 2025 01:59:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:5015e5a3465341f5472cbe9d9f9b35b91aa3d4782561a4be8cede4104766d073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5784986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50db4f97e67822399b438e8851182db670e222b3c05a112cb485759a39a4ba9e`

```dockerfile
```

-	Layers:
	-	`sha256:1b049299f0aeb5b96308096c79eb8e75cdaa91930f37d6cc6c9f0de19c975d1b`  
		Last Modified: Tue, 09 Sep 2025 05:10:41 GMT  
		Size: 5.7 MB (5730811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3d93be49b069c1cffe5bedce25465a04571b4a51b64382f153e3824fde0b33`  
		Last Modified: Tue, 09 Sep 2025 05:10:42 GMT  
		Size: 54.2 KB (54175 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; 386

```console
$ docker pull postgres@sha256:4d50f711c69eb1580aeccc657dce6a6f445f5a1dbbf314f9607f0c9e8c8875f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167230259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d591541974da040eb4945df51edbb77fb362c9660cca19b93f69a48c99eb4170`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=15
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1f2c097ef38e3c51aa53148ca4055812af722afc8369110c204f267b1b2dae`  
		Last Modified: Mon, 08 Sep 2025 22:51:15 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9e7d37bdf03a07cb3aeeb9ce00d0d474e697708d368219d6772ca6165b3254`  
		Last Modified: Mon, 08 Sep 2025 23:12:16 GMT  
		Size: 6.6 MB (6629448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f6b0b9c41e300ffc5239c030c1ffb4d9f69d57816c94d9ac756c880fc1a554`  
		Last Modified: Mon, 08 Sep 2025 22:51:13 GMT  
		Size: 1.2 MB (1225047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d754060416ba57ed9c1ca50928c80d34dbaa2d89f16933e55e31cb8959dc03`  
		Last Modified: Mon, 08 Sep 2025 23:12:11 GMT  
		Size: 8.2 MB (8203854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a2d56dcfcfdef1d4df90fa69f2387793f92a54edfaf2d59e284aef2372c374`  
		Last Modified: Mon, 08 Sep 2025 22:51:14 GMT  
		Size: 1.3 MB (1308075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3c552b14ac9676b1b889ed79493e93e62587181e21737e3f49f24f7bce8484`  
		Last Modified: Mon, 08 Sep 2025 22:38:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8705054180f5dcdabef6f90c8f99fe3daefb8f72c9d746a0fac785cd91c6c8cd`  
		Last Modified: Mon, 08 Sep 2025 22:51:13 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6a716c50af8df86fa973b7cdd0e0805d5d260fa68ecce6e791de5af4d58526`  
		Last Modified: Mon, 08 Sep 2025 23:12:17 GMT  
		Size: 118.6 MB (118553341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d99063d212d907a77a1db641b8e76aa9ae478a381d31bbbd022e44aa26cc83`  
		Last Modified: Mon, 08 Sep 2025 22:51:13 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd191dbb21b997cada9e9fcfc8a9a271ada9d81a7448bef4476c1ad2149ef8`  
		Last Modified: Mon, 08 Sep 2025 22:51:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4db1b1b4e162b4dc615f0cf6c2278f1941bc822dc73b348887c1677e729ecf7`  
		Last Modified: Mon, 08 Sep 2025 22:51:13 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248da459195c600bfe378ad4f78cd745dd66cbc23ba3e6acb3d20b4554f617e0`  
		Last Modified: Mon, 08 Sep 2025 22:51:16 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f405354f5a18a7c3cf26842bae591d13ae244298d69c09369cfcde12b68093ba`  
		Last Modified: Mon, 08 Sep 2025 22:51:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:1edcf652bd30f580866600ee0db81125b157ea603a574a4d07ac77348988aef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6749a1f0a511cc46b34d7f91129508a1116c8f92944be4337599081dda1ec4`

```dockerfile
```

-	Layers:
	-	`sha256:5cb9cd622cb72b8032e5514c450c39496a9f4633811d2463e9853635a4dd95cb`  
		Last Modified: Mon, 08 Sep 2025 23:10:05 GMT  
		Size: 5.7 MB (5739984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd540b97585dba08cd04a1c8dde8056d36924fcb5920daad83818245cef75f2`  
		Last Modified: Mon, 08 Sep 2025 23:10:06 GMT  
		Size: 53.9 KB (53853 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:99ee945b805648e78fc4855bee312c03ff2d7b058545f589403b669d6d355325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170319504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e23809ff56790830bb478b15b546e0c684c0ed1a26a6667d1e243277bd735f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=15
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba7845244ff99e017c7b54e32ff0d3f3acf24c37b3886eae2a44e7fb7cfa759`  
		Last Modified: Tue, 09 Sep 2025 13:28:58 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7dcbe5e6e6fd11d1b5b66506b26ad6ab3b9fad8b5660e76e362126d8f5fb4a`  
		Last Modified: Tue, 09 Sep 2025 13:29:00 GMT  
		Size: 7.1 MB (7075892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fa585e43a56b643954588453848961368dad5faf67c5b4499db67f75fb4de0`  
		Last Modified: Tue, 09 Sep 2025 13:28:58 GMT  
		Size: 1.2 MB (1214040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd5a1c030da9e3f25c81241a25c9f3d270c60ca04acbabdaaf241e81fc1347a`  
		Last Modified: Tue, 09 Sep 2025 13:28:59 GMT  
		Size: 8.2 MB (8203875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002623c538a89de26e08b8147b413421481de6773f31d898db7880669debf207`  
		Last Modified: Tue, 09 Sep 2025 13:29:00 GMT  
		Size: 1.4 MB (1394737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e5e536608655807a082af5496244583272d5821dbe14738eb156fa0015da55`  
		Last Modified: Tue, 09 Sep 2025 13:28:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d372b25ac0f201e5298c28296f0e12fe69dff7cc0debf23f6142334de82acd13`  
		Last Modified: Tue, 09 Sep 2025 13:28:59 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16901527bfa38bf98c5a5171ce13a5a6fdb68bdc99fc227673751b7dd6055dfb`  
		Last Modified: Tue, 09 Sep 2025 14:07:02 GMT  
		Size: 118.8 MB (118815894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149cf3c7116cc91b2e4a62bc1c1886e8a8a18eb190a97a2b09cb79134f9f0f1f`  
		Last Modified: Tue, 09 Sep 2025 14:06:46 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee33e3d9882638f635fc800fb8f47ef039cd88f0e965210b6f6f52986a4e9d2d`  
		Last Modified: Tue, 09 Sep 2025 14:06:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb99662ab17858180c2aa65633834bb47980e3c8ca130a2661f93654a1377262`  
		Last Modified: Tue, 09 Sep 2025 14:06:46 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b6aae9e9e45c89c22be591673aea007d0ed652747a4676abc59f2eca4de6a5`  
		Last Modified: Tue, 09 Sep 2025 14:06:47 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af75ca794cbe4f38351abbd91055822c3f1eda2b9e248e4e13d3826e556bcfeb`  
		Last Modified: Tue, 09 Sep 2025 14:06:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:22b55dbeb6ece783a382ca591eb053531c33ed663f7cfdf23ad88dc42c443f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5785067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2af04c5095071614b037614f8b6575cfddfa7c3b2ffc123a793f698bf75bde`

```dockerfile
```

-	Layers:
	-	`sha256:0905b129d993bfa8950d40e4b6691eb415552ae208bf47943bb3b7f567e3bcf1`  
		Last Modified: Tue, 09 Sep 2025 17:09:44 GMT  
		Size: 5.7 MB (5731094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:988c8d7161710f69ba7aebec9bca1f0b6c993a34517c976af3b560a0a4142140`  
		Last Modified: Tue, 09 Sep 2025 17:09:45 GMT  
		Size: 54.0 KB (53973 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:3876c2b5f005f01a7b8d427df102ee1cc58e2eb1d902b74582d39ed75ddaee86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90120216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b36fc08641e81ee3c7ac0cfab6fb4a1f2f48b4787dba39d4534a2a1235db79e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=15
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cf1eb1af28d00acf6a6d72a8bf5ae8459e7a53b1529ad9482dc4ae2304f5ab`  
		Last Modified: Wed, 10 Sep 2025 14:41:14 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc6ec488a92bf9ae958129026876cd19b554c9ec9ab962305e46ff6ecff06b8`  
		Last Modified: Wed, 10 Sep 2025 14:41:15 GMT  
		Size: 6.3 MB (6291292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee71238986494d20c9422f9ee8c233c6ec81d45587a613994eb0589e6cb8d83`  
		Last Modified: Wed, 10 Sep 2025 14:42:35 GMT  
		Size: 1.2 MB (1201077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a808d1ef325624a16ed8ad44fc51e7cad7a9fccb57b85bf8fb19ce0f463f6478`  
		Last Modified: Wed, 10 Sep 2025 14:42:39 GMT  
		Size: 8.2 MB (8203594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ee04f561a2cffd224d5b8e8db98278b240b48e78addd098c735d304451f25f`  
		Last Modified: Wed, 10 Sep 2025 14:42:34 GMT  
		Size: 1.4 MB (1402209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14763f37d68532564a1e5841303b138e329cbbfbc892c542dc9aa3758e8dcb2`  
		Last Modified: Wed, 10 Sep 2025 14:42:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54be933a1df45062f9990ab9e3624e79cb7eaec62b3384c3280f018850824268`  
		Last Modified: Wed, 10 Sep 2025 14:42:44 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e33054fd4dbdddd8a6cd2380662e65ce41788f64c8121409d01b02a5369394d`  
		Last Modified: Wed, 10 Sep 2025 21:22:51 GMT  
		Size: 44.7 MB (44729938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea1cf722b626f4fbe71b1ca3efd18c82fbde616228df45acd193c0fcd67a6e8`  
		Last Modified: Wed, 10 Sep 2025 21:22:40 GMT  
		Size: 9.9 KB (9891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89449e18f98657199168199b9cb9c93681f77b77663358379173349f56488d36`  
		Last Modified: Wed, 10 Sep 2025 21:22:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04d4917062818a0e810e7e401dcaba434ece5278a4ad4849cf49ec99f4e1f76`  
		Last Modified: Wed, 10 Sep 2025 21:22:40 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60698559c66a9a9ed792612cb55cdb4ebbd82823a161f9d85ec5b417e84885a1`  
		Last Modified: Wed, 10 Sep 2025 21:22:41 GMT  
		Size: 5.9 KB (5932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd403e223eb79f526eb1bba4713b0ca4a387e5686c73433fee6013041bb0147`  
		Last Modified: Wed, 10 Sep 2025 21:22:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:9ec722d085d8c9322c2a11eca4f0d9ad1fa0b715e169125ef68896283387bcfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5156478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08d39e0a25a2c17cb65d47488492c0a19c1ee5e71b0f4b790e6f99f10652ce9`

```dockerfile
```

-	Layers:
	-	`sha256:cbf6a01732f1fa807828d9cee64d369044a0e72cc6b95b910efb37335594b4ef`  
		Last Modified: Wed, 10 Sep 2025 23:08:15 GMT  
		Size: 5.1 MB (5102511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0fefcbc7ac7f895ac3f9b0c669e1991ebcd0d68303fbba4cc5c9d1c015cb026`  
		Last Modified: Wed, 10 Sep 2025 23:08:16 GMT  
		Size: 54.0 KB (53967 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:e38be22910630dbbf803bd9f8001b8cd1df903f30fc907e014749fa80ef8c6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172665059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5473f38bd7c0396bd8e419fc378f747496aafbd0dc6b377fa1014b080ad0c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV LANG=en_US.utf8
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_MAJOR=15
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Sep 2025 20:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Sep 2025 20:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Sep 2025 20:04:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:04:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Sep 2025 20:04:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Sep 2025 20:04:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63358eaba2f5c4f43a207e4e2e64916b21d7da7390f42873769212aa17a94f88`  
		Last Modified: Tue, 09 Sep 2025 06:40:47 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb21da94510298eca932ca295b52d37d2d85647dbb291af82bb324c561e12d79`  
		Last Modified: Tue, 09 Sep 2025 08:10:06 GMT  
		Size: 6.4 MB (6408665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf292dd8ccce6d62e0320ce051a1776ca62a36dba2fe8058c5d50e6c8d2189af`  
		Last Modified: Tue, 09 Sep 2025 06:40:51 GMT  
		Size: 1.2 MB (1229400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d75ec5efdc77d682613065eef13be3de4b4d2f94d950ae811ae8916854db8c7`  
		Last Modified: Tue, 09 Sep 2025 08:10:06 GMT  
		Size: 8.3 MB (8258773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ad1bfb54ab9948ed3eeebec1f5bd23db1be002e3ddbe7d847e82f931508e13`  
		Last Modified: Tue, 09 Sep 2025 06:40:56 GMT  
		Size: 1.4 MB (1398015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19385b03430b6ff7c06a095146f24799f825d5d4229816cf17af3d4a75fd62d6`  
		Last Modified: Tue, 09 Sep 2025 06:41:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12fee8ba3e8ce490ba6ebe9ddac6fc4478e91fa7ce8fa9a3b6fbb398c3cd663`  
		Last Modified: Tue, 09 Sep 2025 06:41:04 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1128dfe1276095a2ed3c159375024ac2d8aff38b7c0198c3e19d7b9adad465a6`  
		Last Modified: Tue, 09 Sep 2025 08:56:13 GMT  
		Size: 125.5 MB (125516590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f9be57f48738a2d18ba792e989404d464f4723c9a73663fbcc191e4b6a419e`  
		Last Modified: Tue, 09 Sep 2025 08:55:51 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e9c6f12a8ccfb37101c5109a6a0b736aae807a28184bf7bf4482da4be85840`  
		Last Modified: Tue, 09 Sep 2025 08:55:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01cf647d64afd09b5f83aacc079cc79b02671a7feb668f3fe3e2d2de397bbaf`  
		Last Modified: Tue, 09 Sep 2025 08:55:51 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4699acbe83227ca01901799aae58386476f15439667dcd89be5cfcdb263bbe1`  
		Last Modified: Tue, 09 Sep 2025 08:55:51 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a33e8c54ed67b6d5d602a4d07174f5a95cec02dd7d74f47265557bc9b93e63`  
		Last Modified: Tue, 09 Sep 2025 08:55:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:447f30b2c9f1c1a9b9609239306dd13e8a41057b787fa70aae13e96c0fcebeb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b45e6d3d7be2f3558cdecf89c536a09aeee57cceebbdcc1bee254f2dae4f9a`

```dockerfile
```

-	Layers:
	-	`sha256:2c6f1f0c0cb42726d0d23970098d5047720d1001aa329d40b5f1e2f97aabe885`  
		Last Modified: Tue, 09 Sep 2025 11:09:16 GMT  
		Size: 5.7 MB (5741126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49019a212cadea2ba3ac5871696ca815fa962c12c0c31494753f2358ed2a8fa3`  
		Last Modified: Tue, 09 Sep 2025 11:09:17 GMT  
		Size: 53.9 KB (53907 bytes)  
		MIME: application/vnd.in-toto+json
