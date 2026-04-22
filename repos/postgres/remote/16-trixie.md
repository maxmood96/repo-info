## `postgres:16-trixie`

```console
$ docker pull postgres@sha256:760ea41aae126965bedd587d35a23de37447bb13a6ac4444bef6ff73b8b72234
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

### `postgres:16-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:adaa8b0891d74ee64cc97119c96b4826190ada4644a41d69dfb6c2d96a27f7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160133793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188ac51266eb2476c69f7a145ea50290e3b8d81285a3386197704d8ad677ba5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:32:34 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 01:32:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:32:46 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:32:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:32:50 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 01:32:50 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 01:32:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:32:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:32:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:32:54 GMT
ENV PG_MAJOR=16
# Wed, 22 Apr 2026 01:32:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 22 Apr 2026 01:32:54 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Wed, 22 Apr 2026 01:33:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 01:33:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 01:33:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 01:33:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 01:33:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 01:33:06 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 01:33:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:33:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 01:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:33:06 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 01:33:06 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 01:33:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3326b6522e5b1155762867bbb7e9371a216e89ea4b459b37b2e082c26b208716`  
		Last Modified: Wed, 22 Apr 2026 01:33:25 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decd178ddeb0a319184fbcb714cfa578665ce408d02de164e960c6ff9fb8bfce`  
		Last Modified: Wed, 22 Apr 2026 01:33:25 GMT  
		Size: 6.4 MB (6441220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aef946c609a7e01d587e72825059b0cd79c2f9237470cf5a02773a558d0413`  
		Last Modified: Wed, 22 Apr 2026 01:33:25 GMT  
		Size: 1.3 MB (1256742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102496efe6c148e5c17c4ff8938c2c1226753d954f8ce9a297fb5a022c14a276`  
		Last Modified: Wed, 22 Apr 2026 01:33:26 GMT  
		Size: 8.2 MB (8203804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952c21578f5b7a37afcde7105b8eaef91284dbaf8e679ada71f174ad76ea9d7`  
		Last Modified: Wed, 22 Apr 2026 01:33:26 GMT  
		Size: 1.3 MB (1311670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e42eccf4bc06c75ba125748717d21a947f23d04f6f789f7d0aafba45c26b787`  
		Last Modified: Wed, 22 Apr 2026 01:33:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13375e48b679f8eb5e8270e864970b0d00c9a08b383e88c3a60c52078bd5cf3`  
		Last Modified: Wed, 22 Apr 2026 01:33:27 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e80c373fbadbac31f9844fe71984d24f30f2eba0be5cbd36f5a9731171ba8f6`  
		Last Modified: Wed, 22 Apr 2026 01:33:31 GMT  
		Size: 113.1 MB (113119118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3618b5f7b5bce820ca2bc4fdf64da4f33a5fc10cf9925127a543a4ab1d09022b`  
		Last Modified: Wed, 22 Apr 2026 01:33:28 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88738cb34413e68f8c951381ee3576252544d295e25eea9103cc37351dc2168`  
		Last Modified: Wed, 22 Apr 2026 01:33:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebf6f2e52f35df2a2f1158e3425dba816e41c1aa045648f39e72e5654d3446a`  
		Last Modified: Wed, 22 Apr 2026 01:33:28 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65fa596db1bb4065fa46bb5822c4a5b70460f4765fcfde1c0753cc217b26f7b`  
		Last Modified: Wed, 22 Apr 2026 01:33:29 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef33b0ec2318453743ed2bb9ac0e7877b751a919d144c81ac4ec86ab1847aa8`  
		Last Modified: Wed, 22 Apr 2026 01:33:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:df9e8881b93594d0a3606fc1b6159cbbf4b28679ed14480b74db868026865ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f69a09582395368d1b14f616e878839bcd91717883af1e0b811dba07e5d6792`

```dockerfile
```

-	Layers:
	-	`sha256:61438927987fdd8e01ff7d602379fb61bdbcf8720e1aa7b2ae2dddb2b0bcc718`  
		Last Modified: Wed, 22 Apr 2026 01:33:26 GMT  
		Size: 5.7 MB (5708762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72a8a4ef0d8fa7c4359be1b724f967ea7eec7ef27ace477bc5f63d1f21a797f3`  
		Last Modified: Wed, 22 Apr 2026 01:33:25 GMT  
		Size: 53.9 KB (53868 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:6cc9cb0b75d64ae5fc02d53f8769568d18f4d9425db153ae2cb1fb0c23252c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154168062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16d6629140c25129815131ce93f3233dd00208d92252df7d629c4dda615b5a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:45:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 01:45:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:45:44 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:45:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:45:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 01:45:52 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 01:45:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:45:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:45:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:45:59 GMT
ENV PG_MAJOR=16
# Wed, 22 Apr 2026 01:45:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 22 Apr 2026 01:45:59 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Wed, 22 Apr 2026 02:02:21 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 02:02:21 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 02:02:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 02:02:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 02:02:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 02:02:21 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 02:02:21 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:02:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 02:02:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:02:21 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 02:02:21 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 02:02:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd1f9135103a391689cce20ec91723dda41314cd31f33ef2db8d9ca38a7c33`  
		Last Modified: Wed, 22 Apr 2026 02:02:39 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaf98f677e9d47f2190cf048795202ea13bd1bbfa0e5ff1980669edec37be38`  
		Last Modified: Wed, 22 Apr 2026 02:02:40 GMT  
		Size: 5.9 MB (5932469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24394fca9057b676b64e266abaca44a218d8878e9db63d87b7b00a4c4f41588a`  
		Last Modified: Wed, 22 Apr 2026 02:02:39 GMT  
		Size: 1.2 MB (1227485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccd6027453390e334deed6775c7987c1b780485bc07e850c1f71cd59506d79d`  
		Last Modified: Wed, 22 Apr 2026 02:02:40 GMT  
		Size: 8.2 MB (8204226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88166ff26cab3b11a5b26a5e325fcfa2a4079cfa60b27e3e85f5226e76e33ab`  
		Last Modified: Wed, 22 Apr 2026 02:02:41 GMT  
		Size: 1.3 MB (1317358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae182235377d486f16e22fd5203ce45af6cd8667ff2953f897f9dbbdbcb7d7c`  
		Last Modified: Wed, 22 Apr 2026 02:02:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6315cf5ad242f61f3656bd6fed4e52ba926fb3559c7d4361d60a9acc4c9b0521`  
		Last Modified: Wed, 22 Apr 2026 02:02:41 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8c1cef05684613e7c06bf76bb629e1d7e911e08302b66a581fc1ab46b2c011`  
		Last Modified: Wed, 22 Apr 2026 02:02:44 GMT  
		Size: 109.5 MB (109517284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22a3313927107e62ffa5133df45809118fb9f10ae78ea98224712e8ac962502`  
		Last Modified: Wed, 22 Apr 2026 02:02:43 GMT  
		Size: 10.1 KB (10058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f303a49dbaadd3e239ffea31ebcd7eb057a6d70b5e1f5cd932256c4d43a211e`  
		Last Modified: Wed, 22 Apr 2026 02:02:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a940e3a2fc02c8df752036982313f777f4bb91c32cb6b2f33b6e4d893ff40cd`  
		Last Modified: Wed, 22 Apr 2026 02:02:43 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d893fc19dc6eefad090008d6a4ef2d139c537bfd20d9a4423eebfc4f34b736`  
		Last Modified: Wed, 22 Apr 2026 02:02:44 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d535eae08e663a4368900b9bad1240e7c9b251f4e8b0ac44927f90e2bc45c0`  
		Last Modified: Wed, 22 Apr 2026 02:02:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:188f885fa39bff8bb2d36499dd8484a3b6c885c7050936a25f8e74058fb15661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5779491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e35949191e0d7267a16b23943116a2f44f12ba045430706514ae5bf429b866b`

```dockerfile
```

-	Layers:
	-	`sha256:8aeae4011805de9285ff994f09cfaf798d7f5ff226794948928fec3dc9ac8533`  
		Last Modified: Wed, 22 Apr 2026 02:02:40 GMT  
		Size: 5.7 MB (5725400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f86f7179ba9f29ee889080ea95559598d854a72a3318f5ac966bdd51a40a157`  
		Last Modified: Wed, 22 Apr 2026 02:02:39 GMT  
		Size: 54.1 KB (54091 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6316f84907c949e425a0a5bfe359f8aeaa9302e058d8455cdc66f7cca7c56ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149230464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1eaed688748dcac51562ebadb24d23e18c28c0e15a3a95795f19460edf9341`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 01:44:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:24 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:44:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:44:31 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 01:44:31 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 01:44:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:44:36 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:36 GMT
ENV PG_MAJOR=16
# Wed, 22 Apr 2026 01:44:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 22 Apr 2026 01:44:36 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Wed, 22 Apr 2026 02:12:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 02:12:09 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 02:12:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 02:12:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 02:12:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 02:12:09 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 02:12:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:12:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 02:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:12:10 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 02:12:10 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 02:12:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c149329bff290b9cc6c0dccc7407e96f02c1502e0395951300cd62c5cdc3cc1`  
		Last Modified: Wed, 22 Apr 2026 01:56:40 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd9fec10f4b750bf1dafad269d4980b0a3e3628e906dc3c8282cf51c4e8b4af`  
		Last Modified: Wed, 22 Apr 2026 01:56:41 GMT  
		Size: 5.5 MB (5496583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76f1844af9e8b321d0085f0165c7e7fb18cdee5ecfa272c1fbecf9e4bc385ce`  
		Last Modified: Wed, 22 Apr 2026 01:56:41 GMT  
		Size: 1.2 MB (1222347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5c0b61b044b9684ca0b508680121f83f9005663025942718eda52dee01d7f4`  
		Last Modified: Wed, 22 Apr 2026 01:56:41 GMT  
		Size: 8.2 MB (8204063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15d63a8fa60229d9c6def2e75ccaa0b4aa69d78ef633f325b76bac56dd024a`  
		Last Modified: Wed, 22 Apr 2026 01:56:42 GMT  
		Size: 1.2 MB (1172660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7b556d0d6ba58f6b020546c1455e6310c1ed35618220899564958714a52173`  
		Last Modified: Wed, 22 Apr 2026 01:56:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a91fc3c60cb1918c2708a4a8a1646c79d9a64a4a414279ef765cf22cd2a543`  
		Last Modified: Wed, 22 Apr 2026 01:56:42 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581fda3491637f84e2f9936cfae8d0163cc75a83d07a7de55cb7bb7de8f51b17`  
		Last Modified: Wed, 22 Apr 2026 02:12:30 GMT  
		Size: 106.9 MB (106898904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d449470c9f6b2a7251e4ad04a2643e1cba05d9dc6a8647e21febbd4ecc9479`  
		Last Modified: Wed, 22 Apr 2026 02:12:27 GMT  
		Size: 10.1 KB (10071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d118b1fac5c6c4209dbbbe696eb65b09d9cab70df21c3ac36d8b65ab21a6b4c9`  
		Last Modified: Wed, 22 Apr 2026 02:12:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2134f9b48157ef2b16ddce7b243a9954d698f3c93c5a12dbca5f7ee5c92c1e7`  
		Last Modified: Wed, 22 Apr 2026 02:12:27 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc85d290cdcfc7dfac6b3afa44663482cc8fbb676403da5dd93bbae2b99a53b`  
		Last Modified: Wed, 22 Apr 2026 02:12:28 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb042c80e18ec79e69bfb4fd2286a81db0cf549214f27c1590d447af50ed993`  
		Last Modified: Wed, 22 Apr 2026 02:12:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:c3d618f85e3fa99e362ba60d1fbb70446ded0417f6082d810c7f9314f18d829d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01a500e3a8543ca0b6e32a3cd1e8560b6eca098dda92d3a62ca8a728eaba4dd`

```dockerfile
```

-	Layers:
	-	`sha256:0a4ae99e03bf08fae639792b72ddd0d6852625481059df816e007ffa3a6fc090`  
		Last Modified: Wed, 22 Apr 2026 02:12:27 GMT  
		Size: 5.7 MB (5724705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e50bb9e6efb2d4662f09836d66017e14ccbdc2821598e02be61a950d7401bd80`  
		Last Modified: Wed, 22 Apr 2026 02:12:27 GMT  
		Size: 54.1 KB (54092 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:029129ec5db0de3856db70c12c3b17aaada66553fdf4e6a26cbcb81013807e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158758425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6b782c1e7274e95ea96e2c9958b2e38135ae9e22c623c02dca38e5d84197f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:34:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 01:34:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:34:26 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:34:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:34:31 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 01:34:31 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 01:34:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:34:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:34:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:34:35 GMT
ENV PG_MAJOR=16
# Wed, 22 Apr 2026 01:34:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 22 Apr 2026 01:34:35 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Wed, 22 Apr 2026 01:35:36 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 01:35:36 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 01:35:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 01:35:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 01:35:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 01:35:36 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 01:35:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:35:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 01:35:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:35:36 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 01:35:36 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 01:35:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb6fa73b772555658e5e1993276585dc06601c584d727e454c91a761fd27e61`  
		Last Modified: Wed, 22 Apr 2026 01:35:11 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7311f093afed5bf02624d971515b5054d47e8d50afd9eac8c66af4c5c6ddf8`  
		Last Modified: Wed, 22 Apr 2026 01:35:12 GMT  
		Size: 6.2 MB (6234059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa57db8c1eb81f140c3c2b446c653e55d62a95c706c6e6f006ec4ce8a2cf421`  
		Last Modified: Wed, 22 Apr 2026 01:35:11 GMT  
		Size: 1.2 MB (1209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc15a4115afc641c7577ed322d25ef708ba535ac01a3740adcf033ef800815`  
		Last Modified: Wed, 22 Apr 2026 01:35:12 GMT  
		Size: 8.2 MB (8203979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a865485fc3de53ce61845a419fcd036dd112089b65dda457292fe2356aff957`  
		Last Modified: Wed, 22 Apr 2026 01:35:13 GMT  
		Size: 1.2 MB (1220584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a8be731e1afd2a2cf90dd4479aec4dd5523047b2b9b5ba3184cf46b4f97f42`  
		Last Modified: Wed, 22 Apr 2026 01:35:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba112e1932ca6a9a2e6e761aa26184385df31a6eae88add42bcaeaa7f60dd6f3`  
		Last Modified: Wed, 22 Apr 2026 01:35:13 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427f452d9e5f3cdadd60f18bfe7f26ebddf9875cdc05af3c24aafc381dac431a`  
		Last Modified: Wed, 22 Apr 2026 01:35:58 GMT  
		Size: 111.7 MB (111725490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641ff560184bd8bea3f4310c757828dc9b656ce94b55d190d0a5159efc8fdc50`  
		Last Modified: Wed, 22 Apr 2026 01:35:55 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8091727f1bf958aedca8ee0905bfded08e94bd3f73dc24478ce1307c75a9b4`  
		Last Modified: Wed, 22 Apr 2026 01:35:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6e6d548e5292cfc2942c3c68855599de7d0cccb76028103785f39318cc2b4e`  
		Last Modified: Wed, 22 Apr 2026 01:35:55 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016a29650dfe36402908d5398f19c9bb48bebe3f290c44bc13f2de8a2c2e50ce`  
		Last Modified: Wed, 22 Apr 2026 01:35:56 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9deb97b374e3ffebf44c0dd30e6409395d7815087fa6c4ec16e057f5134432`  
		Last Modified: Wed, 22 Apr 2026 01:35:56 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:01df9d7c27d52f3dabbfb88e3a62c59eabfdda9e826fd91515745b91b1e4baef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ed1e74323b6a966ab3363d312a88ecea3d796b1d68844691d3be953f121118`

```dockerfile
```

-	Layers:
	-	`sha256:bc7ad233306a1e3d7767a850d4afcc32c67a786a0153e5daca14c32df11f254a`  
		Last Modified: Wed, 22 Apr 2026 01:35:55 GMT  
		Size: 5.7 MB (5715108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04a703bfb06aba6500eec7e5e7099776be0b517ffe7923c3bbf35b21d9e20e5`  
		Last Modified: Wed, 22 Apr 2026 01:35:55 GMT  
		Size: 54.1 KB (54138 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; 386

```console
$ docker pull postgres@sha256:264d52896057b935fa23b0cf38ef86b3f0525217788837487dd639131c9e3319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169251838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34bf3ac614ef7ac2057b5f14adcbf58325418c30d1ccf61a88e719e92c27810`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:31:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 01:31:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:31:21 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:31:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:31:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 01:31:26 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 01:31:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:31:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:31:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:31:30 GMT
ENV PG_MAJOR=16
# Wed, 22 Apr 2026 01:31:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 22 Apr 2026 01:31:30 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Wed, 22 Apr 2026 01:41:42 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 01:41:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 01:41:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 01:41:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 01:41:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 01:41:43 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 01:41:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:41:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 01:41:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:41:43 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 01:41:43 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 01:41:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9cb86262fa536a25eb9be1fda8b924b97031e3c9340d497cf1c504bc9c11eb`  
		Last Modified: Wed, 22 Apr 2026 01:42:01 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b032f18ec9f612936c15a421c90a3a9a0929303dae46d9d6071590f682cf7b4f`  
		Last Modified: Wed, 22 Apr 2026 01:42:01 GMT  
		Size: 6.6 MB (6631501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af87c3afd3bb3a5cc7bc61fca94760b3620c7fb7bc296e31f687c1d15cc03ac`  
		Last Modified: Wed, 22 Apr 2026 01:42:01 GMT  
		Size: 1.2 MB (1225825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70492373abc8106c726c4be129422d8bfcf678be7efc7dcd7500db043d8d159c`  
		Last Modified: Wed, 22 Apr 2026 01:42:01 GMT  
		Size: 8.2 MB (8203954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3682746a5c90d4be01ceb067b941ae62066ea5f9525bdc2e9fc39b3bab191c75`  
		Last Modified: Wed, 22 Apr 2026 01:42:02 GMT  
		Size: 1.3 MB (1308262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f0d75b840d50e5fd2e3d88a45cd894dc80605b660297ae3c23b180650cf41d`  
		Last Modified: Wed, 22 Apr 2026 01:42:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c269359f81fe64d72b7bbcc8518e7d1ee6b60b5fd8f3e2e3e760687f3a15d5`  
		Last Modified: Wed, 22 Apr 2026 01:42:03 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615cd0f7df3e0f78da68b65f875d22daa3a0029c60accee5db04a91d51721f45`  
		Last Modified: Wed, 22 Apr 2026 01:42:06 GMT  
		Size: 120.6 MB (120564902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c12460d8f73c3a9a69257b1d9df7ee1d571427cb5b96c8ca6d539c0d14e0524`  
		Last Modified: Wed, 22 Apr 2026 01:42:04 GMT  
		Size: 10.1 KB (10066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ee3b472b679b31d11b8f23ac123aa7c0e0fac0bd41d02d20c3496c2558c17f`  
		Last Modified: Wed, 22 Apr 2026 01:42:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21bae96871407f9cef538aee90976f5827ffb9391e97c0cb2b9e7378393561e`  
		Last Modified: Wed, 22 Apr 2026 01:42:04 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2045c81c8c2355159f6c79524ff21bc92995e7299bd1c1007563be7551de1bb9`  
		Last Modified: Wed, 22 Apr 2026 01:42:05 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cca5b119eca09260449bad7381099c17ea05b83e804a4b4a54512c433f4ebd0`  
		Last Modified: Wed, 22 Apr 2026 01:42:05 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:f5a6e4f9cb91224dacc7a9a1cd580dcbe30022cd54269a621017755cd4b935c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12f8422e7e974f7952879ba19958adcdf140634acf8feafd6d5cf727816c68d`

```dockerfile
```

-	Layers:
	-	`sha256:2f2d9e92a4b6ddaa2e8620821905dbb9752c074c314b179777dda542a5f239cd`  
		Last Modified: Wed, 22 Apr 2026 01:42:01 GMT  
		Size: 5.7 MB (5724293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31d5ef6a078a232bc6e9991533d834c7590799e963c531e900cff5038d09e073`  
		Last Modified: Wed, 22 Apr 2026 01:42:01 GMT  
		Size: 53.8 KB (53815 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:7132f9d30d8a13fdad80d4ef65fb00658c15a6fd936bc0589074994cc9b322f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172385261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035197f789be800bcc55d9c9e863eebea02461da7ca4220363aefdf03ef21ea2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:15:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 03:15:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:16:08 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 03:16:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 03:16:18 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 03:16:18 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 03:16:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:16:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 03:16:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 03:16:27 GMT
ENV PG_MAJOR=16
# Wed, 22 Apr 2026 03:16:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 22 Apr 2026 03:16:27 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Wed, 22 Apr 2026 03:21:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 03:21:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 03:21:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 03:21:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 03:21:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 03:21:39 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 03:21:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 03:21:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 03:21:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 03:21:40 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 03:21:40 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 03:21:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80743a62df7240f153b1bedcca29fefdd1d274308b24d5134b11baa81432937`  
		Last Modified: Wed, 22 Apr 2026 03:17:56 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8145cda07b56fd93635828aba1665e5e084386fab3f7fb014b49eedf805168b4`  
		Last Modified: Wed, 22 Apr 2026 03:17:57 GMT  
		Size: 7.1 MB (7076583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245df6877a5a761d48cecbc70f9fed6f8169ba2f345d4e727b142d14cd83c361`  
		Last Modified: Wed, 22 Apr 2026 03:17:57 GMT  
		Size: 1.2 MB (1214797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a371bc2a61c2e2ed66b4367e0adf3dd506cd07180300666fd8d64e62c404d2d2`  
		Last Modified: Wed, 22 Apr 2026 03:17:57 GMT  
		Size: 8.2 MB (8203992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe5c60e494359e893087e2a0d540cd34545d951000872bd41fc3ebb5c66bfdc`  
		Last Modified: Wed, 22 Apr 2026 03:17:58 GMT  
		Size: 1.4 MB (1394910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924d037b7ab4f45b2955a07af6dcac443ec42e5b9cd3eedb54940a679dd80522`  
		Last Modified: Wed, 22 Apr 2026 03:17:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc29684aebcd65777a1e5c4364e15605182783e36e969e580c963a327943768`  
		Last Modified: Wed, 22 Apr 2026 03:17:58 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aba878ba2884e488c3bafdc167019f653e33e5eb8c4dcd27d56121b237c1b25`  
		Last Modified: Wed, 22 Apr 2026 03:22:31 GMT  
		Size: 120.9 MB (120875883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8e87169f69b791d04baca7aa1a341c7e246ad76ff664f743759b05f9ebb165`  
		Last Modified: Wed, 22 Apr 2026 03:22:28 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3163df656a1ff7bb078cc6435698a291fa6432adf51735050a182eaad3c1c1`  
		Last Modified: Wed, 22 Apr 2026 03:22:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6c63f8f272f4ca25a06314e7c91d7608a0ca5a9fe43a168434b53e1babc2a7`  
		Last Modified: Wed, 22 Apr 2026 03:22:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184762189e2581abe43e5361dc1dadb1a0e6684e4870010bacceace88f16ed8b`  
		Last Modified: Wed, 22 Apr 2026 03:22:29 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec87685b2d9816fdba3b72f9304bb21e450503e94945e9ef43c0814eccaf09c`  
		Last Modified: Wed, 22 Apr 2026 03:22:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:38f6443359a64b071883dfedb336beb9c08e0a0c18ee10a0bfd74db90bf17c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30382ec35fc1f8452ae14e9aa499a204de1fdf5d04a46a26ce6d71af696a8342`

```dockerfile
```

-	Layers:
	-	`sha256:1c6e52dcbf71b90a56ba19c7ba452ecad3cb52c4809f843dcdddc5b20b77304c`  
		Last Modified: Wed, 22 Apr 2026 03:22:28 GMT  
		Size: 5.7 MB (5715375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00f0f6a2eb7b9cf394ac3f1aba0cccbdbe1518b0c11c77ad3e9b44f5f95be54`  
		Last Modified: Wed, 22 Apr 2026 03:22:28 GMT  
		Size: 53.9 KB (53934 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:e888e7707abc5d36043dbdd48736c085e1a9233fe0eb03954fe290e57e51445d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94181349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb7f45345582f4e3196054b985a714a0eb835dd1ec59e2f9d4c54d39b4beb2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Wed, 08 Apr 2026 13:11:36 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 08 Apr 2026 13:12:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Apr 2026 13:13:35 GMT
ENV GOSU_VERSION=1.19
# Wed, 08 Apr 2026 13:13:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 08 Apr 2026 13:14:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 08 Apr 2026 13:14:37 GMT
ENV LANG=en_US.utf8
# Wed, 08 Apr 2026 13:15:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Apr 2026 13:15:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 08 Apr 2026 13:15:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 08 Apr 2026 13:15:20 GMT
ENV PG_MAJOR=16
# Wed, 08 Apr 2026 13:15:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 08 Apr 2026 13:15:20 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Wed, 08 Apr 2026 19:31:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 08 Apr 2026 19:31:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 08 Apr 2026 19:31:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 08 Apr 2026 19:31:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 08 Apr 2026 19:31:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 08 Apr 2026 19:31:49 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 08 Apr 2026 19:31:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 19:31:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 08 Apr 2026 19:31:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Apr 2026 19:31:50 GMT
STOPSIGNAL SIGINT
# Wed, 08 Apr 2026 19:31:50 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 08 Apr 2026 19:31:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85bfa05ff512a09b7f609a01a1951309983f6cd14ae713033c5dcc9c873fc49`  
		Last Modified: Wed, 08 Apr 2026 15:19:02 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ce78e70d8afdf646284cbdc94b068f8a8081fb129a0029f115ae8a36696972`  
		Last Modified: Wed, 08 Apr 2026 15:19:05 GMT  
		Size: 6.3 MB (6293392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35ff328cdafdf470384f15cd77ff64f4ebfb5a10075dd24deeb2f36f8f9cb68`  
		Last Modified: Wed, 08 Apr 2026 15:19:04 GMT  
		Size: 3.8 MB (3818106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44831978cf38d5c3d94ad1b9ef73bfde3d9e736221bbd9d6e0917d44ed44e60`  
		Last Modified: Wed, 08 Apr 2026 15:19:05 GMT  
		Size: 8.2 MB (8203839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f0f262393f005f9bb068cbf565bb433c20b7ca233c0abd3f1789960d04db7e`  
		Last Modified: Wed, 08 Apr 2026 15:19:05 GMT  
		Size: 1.4 MB (1402602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9026932a5f253473763ba90eeb29a2735f7b9773fae70937dff8783ed16194`  
		Last Modified: Wed, 08 Apr 2026 15:19:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2c0793812a0132f11e3b387852cd532da4d4e079ee6768f0444792a5147adf`  
		Last Modified: Wed, 08 Apr 2026 15:19:06 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9207ae6d7bd91f96a948fb3ae9fcb93d2eec8bdb62ab6b13354528d62cc42a8c`  
		Last Modified: Wed, 08 Apr 2026 19:34:22 GMT  
		Size: 46.2 MB (46166805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b33723f5a6b3cd467c706cd40576fac6360e008c83ba0702684e58be8b534`  
		Last Modified: Wed, 08 Apr 2026 19:34:14 GMT  
		Size: 10.1 KB (10071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8e697d3401aa4edd31c8b088ccfb0bf2e1eb6b3be16494c3b26de48ea64115`  
		Last Modified: Wed, 08 Apr 2026 19:34:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dbd634c200b470ea9351d56be14ff12e983d2539b97d48fc663f66091b11bf`  
		Last Modified: Wed, 08 Apr 2026 19:34:14 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5af37bc461b3097d19210d617470ad18f10d29fad97fb31cb8db23bcf28cf58`  
		Last Modified: Wed, 08 Apr 2026 19:34:16 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2315884cf213e8f77fb4b1dd11605c6b8385ae1ff366e8427b6c8cd932f6bd2`  
		Last Modified: Wed, 08 Apr 2026 19:34:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ad91b44cf1ae4e3eb2a377189672fca751147be747eefc6fbc2cc004f31bbb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5128969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce82a4eb30c68eb4df0f1fcf2672fe03ed2f777031f4f1c5a56f1ad061098799`

```dockerfile
```

-	Layers:
	-	`sha256:d554f778638209da93fe6525f72ecd44dfbec6aadbf4a5b473ae51a7d1ddc5dc`  
		Last Modified: Wed, 08 Apr 2026 19:34:15 GMT  
		Size: 5.1 MB (5075041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9139e419a10b87c7b77a52c8b43a67cbc47103846c11f42f02a0e4faf71b9759`  
		Last Modified: Wed, 08 Apr 2026 19:34:14 GMT  
		Size: 53.9 KB (53928 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:79472a0454b07619f36b64dc8c9c6969405df8b0d42308bdc708c610af04e0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174652470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ef134cd81741a0f3a3df5fed0d0b406c9996b69198250eb8cbf1984bdbdcee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:56:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 01:56:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:56:18 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:56:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:56:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 01:56:25 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 01:56:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:56:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:56:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:56:30 GMT
ENV PG_MAJOR=16
# Wed, 22 Apr 2026 01:56:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 22 Apr 2026 01:56:30 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Wed, 22 Apr 2026 03:19:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 03:19:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 03:19:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 03:19:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 03:19:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 03:19:05 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 03:19:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 03:19:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 03:19:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 03:19:06 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 03:19:06 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 03:19:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a758270c0dc688cc56735350d6bb0aad4ae82efb4479cfc317ce63e9f72af`  
		Last Modified: Wed, 22 Apr 2026 02:10:28 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9422a43334c15ec40836f215b7f96f83d0d1f19369e8f4335ed6be6819c6e15a`  
		Last Modified: Wed, 22 Apr 2026 02:10:29 GMT  
		Size: 6.4 MB (6407803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76f17d905b829f369d05816ebd10db2cdeb09fd81a772536c5c77638d1815ff`  
		Last Modified: Wed, 22 Apr 2026 02:10:28 GMT  
		Size: 1.2 MB (1230249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913f8eb212fdabb48a81828c8acb21e4b17910238046ba319726fe7915325c4c`  
		Last Modified: Wed, 22 Apr 2026 02:10:29 GMT  
		Size: 8.3 MB (8259010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bfef94606bc82464a3da274d2c06738836d5a047293604e6df223cb9c27501`  
		Last Modified: Wed, 22 Apr 2026 02:10:29 GMT  
		Size: 1.4 MB (1398240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5d56302446835fc334682dde6adf8d10ada2c2ade700fa6555de8ee70ddd3d`  
		Last Modified: Wed, 22 Apr 2026 02:10:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44dfebe7d09ac91b202c51b4fbc533d1db6978ba77010074c91c89116dc8717`  
		Last Modified: Wed, 22 Apr 2026 02:10:30 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5729d62a2050280f49b012d8506bf4e4f2015d580f5ed7b442ccef083f7ac12`  
		Last Modified: Wed, 22 Apr 2026 03:19:42 GMT  
		Size: 127.5 MB (127495799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd1bf97a3fbaba102fb64c877f36995866ea5d83d7c591d8cbe17209a267fb7`  
		Last Modified: Wed, 22 Apr 2026 03:19:39 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4253296cdfbdb69355a363a1672e8666bebf3c71988eb09adca452ace3ab881`  
		Last Modified: Wed, 22 Apr 2026 03:19:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e872d3babf9497e6d105f28950a19d53e725dd99755af11a2f53a72e87294bba`  
		Last Modified: Wed, 22 Apr 2026 03:19:39 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5165184913158a48f01af4572113220f1e5845e71203a9b02082f2f74b89bd`  
		Last Modified: Wed, 22 Apr 2026 03:19:40 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c4dc8d951a6da9a666951e87f5a135a5346fa70817352e6ebdff3119dc12b2`  
		Last Modified: Wed, 22 Apr 2026 03:19:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:248e826c05ba9aa9245e0a7261bbe681d5e8d3b0b8bef30ff5be48d6785dfd8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5779300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cb068409259c4f5b0a58adad21df795bddc74367c502f9a984c01ae3efba7d`

```dockerfile
```

-	Layers:
	-	`sha256:f577af806e18eb8e2d93d48399be8f9fd836677a99ce5af8d3a556e2c6bf3429`  
		Last Modified: Wed, 22 Apr 2026 03:19:39 GMT  
		Size: 5.7 MB (5725431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56346147b6c60a6c3b798d655ad1bb78880991bb4765fec99a1de253eacff629`  
		Last Modified: Wed, 22 Apr 2026 03:19:39 GMT  
		Size: 53.9 KB (53869 bytes)  
		MIME: application/vnd.in-toto+json
