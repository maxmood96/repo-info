## `postgres:14-bullseye`

```console
$ docker pull postgres@sha256:e730920dee3836956bb8061d38b77a1a335064d029ae93a65da1f8a6eb4b8a53
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

### `postgres:14-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:95b8d0de637c7567f7ecec4d57ccd7832e23c32709ae52962cee0e385bb6734e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145933310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d776f18da183866ef5c9cc8f808f6af8226955491e02a78c8ac5bb045ff6a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:09:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15-1.pgdg110+1
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb54a09793aeb2e1b93b7177aa55b3239ef3a6ba05a41453d262418877c66c36`  
		Last Modified: Tue, 14 Jan 2025 20:33:47 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc9f8a54098ab739bb7e83ba0fca2b3aeea904b3fe91b83aefc52cf7672ab36`  
		Last Modified: Tue, 14 Jan 2025 20:33:47 GMT  
		Size: 4.3 MB (4308200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e61d89637fd573bb6c548fb54a03699c1f0a867447d06e369902ea25d09027`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 1.5 MB (1472208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1167d1b1a06fbc05eccddb77bc1389e59087cacf12f82074c414cd4609d0b69c`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 8.0 MB (8044550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f58f0cef337a636f5891cf484bc75481456304c6332e4acf8d9d1fc75dd2240`  
		Last Modified: Tue, 14 Jan 2025 20:34:21 GMT  
		Size: 1.0 MB (1038338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8baa74dd1c1e754dfbfad32115e063c87e753c973cac42736594919cbd69c2d`  
		Last Modified: Tue, 14 Jan 2025 20:36:48 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ca8dad77110db0305d3b3758b3c03a7d6e21f0c28223e085dbc8ce0b2ae49`  
		Last Modified: Tue, 14 Jan 2025 20:33:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b9521bdae5dec6381b977f6b382a9d7a0b1e0e84c55a6df2ade842132ff752`  
		Last Modified: Tue, 14 Jan 2025 20:33:53 GMT  
		Size: 100.8 MB (100796987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376dca2ec19b2f33b2cf99cac608e1a8cf6349f0aca1be1258b90e37c448495c`  
		Last Modified: Tue, 14 Jan 2025 20:34:21 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e2e553823f591eba92fd5178f262f48c5634310477638d11105f6bffd8a731`  
		Last Modified: Tue, 14 Jan 2025 20:36:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5328887cc46d7cd7496b3ebcbf497dbe70862149f870fcf2bceedd265233bdbf`  
		Last Modified: Tue, 14 Jan 2025 20:33:48 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441c28e92af426e676784bfc0f975c21c0717372e094914bd987eaba23ff1caa`  
		Last Modified: Tue, 14 Jan 2025 20:33:58 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db84b9218628410f66981fedc17d64fa8e59b12b5a0694da1d03d4485e63a6d2`  
		Last Modified: Tue, 14 Jan 2025 20:33:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:36a4915dc4b861d145e4e28077994a4fc78cf245bb037c45b96548bac29d6567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6883e83c1ed967ab2644d50ee3fe9984967585e9d24c9aeefe5f554239d39e`

```dockerfile
```

-	Layers:
	-	`sha256:774d5981ec351c1c30dfbecc21b7575f60739ef6b6644b532dc5c000189c0737`  
		Last Modified: Wed, 15 Jan 2025 05:06:50 GMT  
		Size: 5.9 MB (5902409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:573ca5f4836785d3f3a421c16624160248ba88e966552dd365a1abfe40081fd4`  
		Last Modified: Wed, 15 Jan 2025 04:40:32 GMT  
		Size: 54.0 KB (53993 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:bc00cb98791ceb56376ce065a041cf5609a885da34720b4069525731ba5ec7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134131226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ede49341e9980eafba31a3c0f3b506d090959d3111a9732773c7b4126539408`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:09:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15-1.pgdg110+1
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bafc0b709fff1b657a14551940af81807048c74c63e503c511c438265ec89a`  
		Last Modified: Tue, 14 Jan 2025 22:00:25 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f975e0807809fe76bf2c4859de932ee50e6f49e947f5a1a49aad510b7684de`  
		Last Modified: Tue, 14 Jan 2025 22:00:35 GMT  
		Size: 3.6 MB (3601695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb6df2b8e257a7eda1d3c59549e23c34af700b4f6ac7656286fad61dc52de9c`  
		Last Modified: Tue, 14 Jan 2025 22:00:28 GMT  
		Size: 1.4 MB (1439249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef35b898de2c2ed26801408e41cde59d5ae6ebe8f9354ae4c2eab3de5580b8f3`  
		Last Modified: Tue, 14 Jan 2025 22:00:40 GMT  
		Size: 8.0 MB (8044364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73ef971477037a6fe33388a4295f2f293a338bca50b62cf9510bc34c9977f3c`  
		Last Modified: Tue, 14 Jan 2025 22:00:42 GMT  
		Size: 908.7 KB (908668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a7e95dea3feea2efaa0acb94dd3daae8af06bed3c1673ce2399262422fc4e3`  
		Last Modified: Tue, 14 Jan 2025 22:00:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2983901e72058651f8b788f2a7f436da5ebb614efbd37a8d48ea69113c2cded7`  
		Last Modified: Wed, 15 Jan 2025 01:01:03 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9c8260561a2bf889d0fb5fd441f73bc5b758c8300aca5ba0a2fc7976be0c9e`  
		Last Modified: Wed, 15 Jan 2025 04:40:14 GMT  
		Size: 94.6 MB (94582929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a5f70e25ed45b3614f833c3735ae142d94aa4165957ad7b814c8360e038acb`  
		Last Modified: Wed, 15 Jan 2025 04:40:01 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e9e7ab865504418c4f4fdbb54ac6024c59816b9135ecca87f9390a93069626`  
		Last Modified: Wed, 15 Jan 2025 13:09:35 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855c3c7e94992f2a0c86c233513e67e09027d2a0793c4170fb2980aa94deddcb`  
		Last Modified: Wed, 15 Jan 2025 04:39:55 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c447401fd3ca94ea3abfc35468672e71fdd4c9b72d31a045c15bb090bab2acf7`  
		Last Modified: Wed, 15 Jan 2025 04:39:51 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c777abe80aab2a1842b2b65e5419ea2b561cf3342dfe2254317abc3d5dd335`  
		Last Modified: Wed, 15 Jan 2025 13:09:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:3221b23dfe4118858b88b316e8ab571284ebdb73da5f1809240bfb2aa2beb68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5966457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b20fb1699cc0f92eb9ca3334e8a1627419e844ffd4a7653a90d19f746262c4`

```dockerfile
```

-	Layers:
	-	`sha256:9ee8a757704b6618b30e08f403fddaf4e82090719830c006cb6caf399374667f`  
		Last Modified: Wed, 15 Jan 2025 05:06:57 GMT  
		Size: 5.9 MB (5912276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4010fec211fd01dd02e7bd7dd12bec41bfc041dcd4139401330d41e70b0c734d`  
		Last Modified: Tue, 14 Jan 2025 07:42:16 GMT  
		Size: 54.2 KB (54181 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:4d03f04fbf5050af53e75e8824794f898c90366a3afa8e6b704921c3a91c14b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142974796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0c4dd5f3368532dcc54e1d324e0d21abe8063389409129dec61d22ea3b860a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:09:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15-1.pgdg110+1
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b36d302f8a9da22724b01ad3edb1d16101fab82359501ca8f1feed2fc2cd201`  
		Last Modified: Tue, 14 Jan 2025 20:35:17 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531d7f5be2b7506d5ad4b9aff5db2ac3041e805a533f4f226b0006057cbf1ed0`  
		Last Modified: Tue, 14 Jan 2025 20:35:18 GMT  
		Size: 4.3 MB (4312801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98618b8f6d5579fa5d5505874305171812cc5f23c215fd441412809fada53f9`  
		Last Modified: Tue, 14 Jan 2025 20:43:10 GMT  
		Size: 1.4 MB (1404115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8846735e7d020e5fed1640cd37bcc70daae404ce5c1d5d70cb00643286ff7cd`  
		Last Modified: Tue, 14 Jan 2025 20:35:18 GMT  
		Size: 8.0 MB (8044511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d373474bba828255b5311627514305148190e7243cf38df6346071a766d7adc`  
		Last Modified: Tue, 14 Jan 2025 20:35:18 GMT  
		Size: 1.0 MB (1026607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063c700837a47de565dffe0d6108dfac3680dd70b24434882224f9c82eb1d03b`  
		Last Modified: Tue, 14 Jan 2025 20:43:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204c081de27f53fd775f5cd9393cefa72aa0d51587aabcfec8910197dd81c5c`  
		Last Modified: Tue, 14 Jan 2025 20:43:12 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07517e27efc781b6dd222659ae6655653509998eefe08a0c4c85bc7cad4ea66f`  
		Last Modified: Tue, 14 Jan 2025 20:35:22 GMT  
		Size: 99.4 MB (99421487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff60965940300f3e5058660d47e1749985c63d6ae7b27068216cd7876ddc49f0`  
		Last Modified: Tue, 14 Jan 2025 21:34:43 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cc7e299928b439f2650d7daa4bafdfdaf5399d8f0a693daaa4a9eb5797f68a`  
		Last Modified: Tue, 14 Jan 2025 20:43:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc3d9613234d5dec1bab746068c18c8578f3ab4f32fd574a12ddd60cf6e071e`  
		Last Modified: Tue, 14 Jan 2025 20:43:13 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc75063fdc7ec4652cda8883cf4929abdf4b353ca9764c542423cc77cfbeac64`  
		Last Modified: Tue, 14 Jan 2025 20:35:19 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9159f50f49fce8b4bf7700f02fc14d148310f6b383408cac7d03b3c1be0377bb`  
		Last Modified: Tue, 14 Jan 2025 20:35:19 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:239807b44ae645c0e6a52d97cacc04d69eeb2095ec48efc10543b77c4894670c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c4b1c6be887820c970dd2627cf515568a87f762cd43a1f63c5f3b5b4e89bc2`

```dockerfile
```

-	Layers:
	-	`sha256:ba9cf45f05101c504898cc54ce608b8a94b75b839539356241ceae615a03e127`  
		Last Modified: Wed, 15 Jan 2025 04:38:45 GMT  
		Size: 5.9 MB (5908697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b66d16333aca11ebb6747d5c4973541bf36a5f83f75dcb15afb9ec498c77b860`  
		Last Modified: Wed, 15 Jan 2025 05:07:04 GMT  
		Size: 54.2 KB (54232 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:c561c1fafaeefb93a292e6305ecfc0cfd7f0dcd4cb492f1d75f041c89ec5fa31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154002971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a136a755527e36c30dc7aaee8b2968e29072a9bc66eb5314146ee69d76921e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:09:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_MAJOR=14
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PG_VERSION=14.15-1.pgdg110+1
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:09:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:09:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:09:59 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:09:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:09:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db75dbdc894b493efae588fe2a9b55d3eb5b34adb144be5fd3f7fb8bb38c4be`  
		Last Modified: Wed, 15 Jan 2025 05:07:05 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db6f16dd9bddcf5e122087e07d90efdf8d180aa298924f0280bde5e56b8a886`  
		Last Modified: Wed, 15 Jan 2025 10:01:55 GMT  
		Size: 4.7 MB (4719636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e7822344cf26e0c5d16f57270764aeb82c322025891f0f9c026042bd599531`  
		Last Modified: Wed, 15 Jan 2025 04:38:26 GMT  
		Size: 1.4 MB (1447768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031bfb3876cd246174e296e398210b43b993de3e545f7cecc93bbe4ec907da7d`  
		Last Modified: Wed, 15 Jan 2025 10:01:59 GMT  
		Size: 8.0 MB (8044444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd75944d08af81503d49bc201a64d4bb42ef64501336091339c17610576a88b`  
		Last Modified: Wed, 15 Jan 2025 10:01:55 GMT  
		Size: 1.0 MB (1028890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55ac1679372a71478b679300caf2cb947d47b18c51f63aca7c1c1be046e0a11`  
		Last Modified: Wed, 15 Jan 2025 00:54:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20328012bd1629ac026beb024925a8d2cc4919d3b5ca712ce567b9c8bfd87edb`  
		Last Modified: Wed, 15 Jan 2025 05:07:10 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49490b26ff19cde64f490f7eaca7d745e2f4f8191fcf50ce0c150dc3adbd8cb0`  
		Last Modified: Wed, 15 Jan 2025 04:38:07 GMT  
		Size: 107.6 MB (107562838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8b2eb2da6c882f79edb2aa4b36cff6cffaa53c21ba082fb95b2a019667490c`  
		Last Modified: Wed, 15 Jan 2025 04:37:54 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31097d4013f2014ab6e2d23cb14e7008b0fb3de72349347cf4722fcfe70041b3`  
		Last Modified: Wed, 15 Jan 2025 00:54:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a6c0f4376c9a2f95088bacae322ab90756d420f741a0dae3e6bb471e7944fa`  
		Last Modified: Wed, 15 Jan 2025 10:01:58 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8385b3aacebf605b10113d61ad34eccaa10f6a22824b75e581493e64a47463`  
		Last Modified: Wed, 15 Jan 2025 04:37:47 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7dd6ec2973f84eca8af7d6274b29fe50696871084998bb4342723c83160890`  
		Last Modified: Wed, 15 Jan 2025 10:01:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:f9745237d058d2afeabb8e08050f3b74cf498930ad2f10e992ec77348daf84b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5964000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7947e3a8b794e965dcd739f2656d2a2e503a5a1531aec70b6b5c5a91b1b7c97`

```dockerfile
```

-	Layers:
	-	`sha256:a76baae163c180cbbdb3f3bed6da97b89931850f7c680a26baf6ea12f9dc2af7`  
		Last Modified: Wed, 15 Jan 2025 04:37:37 GMT  
		Size: 5.9 MB (5910051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30004b06a2dcd0b6096302cbebb1df50f01f91ac3ac32e62f84c899ee47c3c15`  
		Last Modified: Wed, 15 Jan 2025 10:02:17 GMT  
		Size: 53.9 KB (53949 bytes)  
		MIME: application/vnd.in-toto+json
