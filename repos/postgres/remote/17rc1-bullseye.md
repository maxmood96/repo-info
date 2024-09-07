## `postgres:17rc1-bullseye`

```console
$ docker pull postgres@sha256:6348fe05009e211dfe341a093840507affabdd5046b7e7f044531e52a40710eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:17rc1-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:e47a0cbccd77dc612bb3c270ba9b82159eabe8f68e10cfe6d1825b6557e789d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139028880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897d87ed04e48cf86f5636bd13b8569bad18fce5719c42cd98482373a3512163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:48 GMT
ADD file:b6f3f19f4bd2bf78068380b3cd10d72519ced99a2b5abe830b4729df341dcfdf in / 
# Wed, 04 Sep 2024 21:48:48 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17~rc1-1.pgdg110+1
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c8ed7888c72e20491bc1a05ae8b473757ca4d400de33029eab69bacfb9dd933b`  
		Last Modified: Wed, 04 Sep 2024 21:52:15 GMT  
		Size: 28.9 MB (28924911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff08d14835d2a8416c4df6e3dd9e317c595ade6582b069f140f08286cdbad6e`  
		Last Modified: Thu, 05 Sep 2024 06:06:12 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f652cee625fb7c902694dfb64a4dcbd644862142e4dfc68893dd60dd62f5c5`  
		Last Modified: Thu, 05 Sep 2024 06:06:13 GMT  
		Size: 4.0 MB (3991654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d02501ed234a0a5d8e7cbd6a3b78af584bd0c2c5a2559d08ee15ba7e5f06830`  
		Last Modified: Thu, 05 Sep 2024 06:06:13 GMT  
		Size: 1.4 MB (1449215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9160d82cccd2166396d8525cd76bfc39ac2c6a06230e6c5b4fb2a4b6e736dd`  
		Last Modified: Thu, 05 Sep 2024 06:06:13 GMT  
		Size: 8.0 MB (8044317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5cb92b5411bcffbc1c9ab1ecc57e17994310a00f9727277ec63f3e3cca4bf2`  
		Last Modified: Thu, 05 Sep 2024 06:06:13 GMT  
		Size: 1.0 MB (1034881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52386f3c03837e7199651cb1044a0ed933f4fae098f20975ad8db2eb6262efd`  
		Last Modified: Thu, 05 Sep 2024 06:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d037fe4403f7b5c213daecbfb442898d0fca3592426a40bf38cd34bacc6ae7ce`  
		Last Modified: Thu, 05 Sep 2024 06:06:14 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a0576d67507c61ad18f70910c57e3b49bc8a206fb4999670ad81329ee4c100`  
		Last Modified: Fri, 06 Sep 2024 21:33:28 GMT  
		Size: 95.6 MB (95562827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fbc12153a3ebd13bc79afcbef5e739cd581c369e69e6c572541f6d718994f9`  
		Last Modified: Fri, 06 Sep 2024 21:33:25 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b56fcd1ab085d769ff4312632a33992f29db0fb24eecc70a841ed39ccf5555`  
		Last Modified: Fri, 06 Sep 2024 21:33:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3082aa698cd5b296bcd700271c5c061bd2dd5fba5e87e81e0e256323f1cad63a`  
		Last Modified: Fri, 06 Sep 2024 21:33:25 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963ff5f4bf2cb58a1e89bcfa9340e0a1583ed1617d2e8d68ff094cbd9715c517`  
		Last Modified: Fri, 06 Sep 2024 21:33:26 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ba3e7910decf494e0408f6a4834c60e34f4c9ae7a4192ef9e60070036c1bb`  
		Last Modified: Fri, 06 Sep 2024 21:33:26 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:e9ae5478ff0e415c28b282bf69a407c8ce6cecd161c4bc786161d5d43e1f1ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6081000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9944c3312947e5285d17d2b5720d9be3c6a71b159fab845189770d77dbd1955`

```dockerfile
```

-	Layers:
	-	`sha256:280bcf7bad9fb19aacc1e417ec6a908f3b5a72f422472dce7ea9766cdd776743`  
		Last Modified: Fri, 06 Sep 2024 21:33:25 GMT  
		Size: 6.0 MB (6027268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e970099945616b739568f95c73d66f5467bda24b84308b679cdcba6e9ec517bc`  
		Last Modified: Fri, 06 Sep 2024 21:33:25 GMT  
		Size: 53.7 KB (53732 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:d9f7b10853a10fb2bc5536b6429d1a718ff4c6782c6a762eae8cb7bdb8bf99fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134088845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18021bcf86a60eea60c7bd0a3879086b532fb9cb1a994a0bab6b00578643a09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:29 GMT
ADD file:c451ece1244c14bce110ffbe6906867ce12f8e88234988b0edba91009a9dbbf8 in / 
# Wed, 04 Sep 2024 21:58:30 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17~rc1-1.pgdg110+1
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f572303598915f7fb61cc4b47f7207c9ee64d52b9db5fc03ee133ec2dd679347`  
		Last Modified: Wed, 04 Sep 2024 22:02:25 GMT  
		Size: 26.6 MB (26589615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5e9c606d8528311a46a30cb82519938c43b33c4e1f31162ab88efcc0dd0f15`  
		Last Modified: Thu, 05 Sep 2024 07:11:28 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2970a29d8de911f08d48442531c9307bf0ae742938b71d029a754342b919a541`  
		Last Modified: Thu, 05 Sep 2024 07:11:29 GMT  
		Size: 3.6 MB (3601649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b66db6d98ea73837923d726df3338ff4973e9c5bd1b7514f22394af905dd9b4`  
		Last Modified: Thu, 05 Sep 2024 07:11:29 GMT  
		Size: 1.4 MB (1439215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770e958c632b7100f93874e6d8edcf6a0e7bfebd2df344b16f5d3ec2a0f0f714`  
		Last Modified: Thu, 05 Sep 2024 07:11:29 GMT  
		Size: 8.0 MB (8044293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c42f090ffe7dc7637ee220b14061287b2fc4c983da82a663fcd24defc85954`  
		Last Modified: Thu, 05 Sep 2024 07:11:30 GMT  
		Size: 908.6 KB (908647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9846d37a8dad8e0ac73680041abcd9790c9deee18bc1d3cdc6986e340820abf`  
		Last Modified: Thu, 05 Sep 2024 07:11:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b909d375e13dbdd2a339a93e951b8c697bb1f0a9622446bdac7ce891a6eba51`  
		Last Modified: Thu, 05 Sep 2024 07:11:30 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221bc8ee1c7f3bd8c95d57f101510ee37b74458c1074ff5cc2da417ce87f157e`  
		Last Modified: Fri, 06 Sep 2024 21:33:11 GMT  
		Size: 93.5 MB (93484352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38161ba19bb9f6b1b2dd1758764515f87833d6751a0a5e677d0d6fe29db6069`  
		Last Modified: Fri, 06 Sep 2024 21:33:08 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da1c601a01c82e4baceff45516e7774877e6033a4184e85848a7294b56779c0`  
		Last Modified: Fri, 06 Sep 2024 21:33:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90400934de04f25c4f1cc98d6b02e6cc7e338a2c23fbc68e5e8c8816b61f03ec`  
		Last Modified: Fri, 06 Sep 2024 21:33:08 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b58c120f69d1602aefa436da44223c8ec313bd82cc73399bebb0ebfb139c21`  
		Last Modified: Fri, 06 Sep 2024 21:33:09 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31ff541eba8599c94753795174ce1444e4cce5ebd4b5f11c212de58097cd0e0`  
		Last Modified: Fri, 06 Sep 2024 21:33:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:bf75abd3cd65f495e5440a9f411ba380ec0aa2743c443ab33c9bd8b6f2c6460c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6080620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e839d9cff3552ba808be84e9e1a5bb118169ad820523f950b46c131073055571`

```dockerfile
```

-	Layers:
	-	`sha256:c9c952bb75c563336a0bd9aa025cf796fb270e50c6bce3698fce5230a55e4110`  
		Last Modified: Fri, 06 Sep 2024 21:33:08 GMT  
		Size: 6.0 MB (6026897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f909d9b26ff841877eb5bcf451ec0cdb34742ff10c2766458f8fa5c845900d6`  
		Last Modified: Fri, 06 Sep 2024 21:33:08 GMT  
		Size: 53.7 KB (53723 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:5dca99001c18de0a617b5044a6ea34ae3fa076fd1ed16c3aea179569e35b8407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148878019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5346b0a2f65879234c82413b14786b8679bdece61add5e2a2754ea03b5013876`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:56 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Wed, 04 Sep 2024 22:44:56 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17~rc1-1.pgdg110+1
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464e9827b26d04325f8dafd09680dabd2fdb05608483a9b92b550088526d98af`  
		Last Modified: Fri, 06 Sep 2024 21:12:36 GMT  
		Size: 1.7 KB (1672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d17fde7bf177a778281ce987c3605996e445e41ae93b923262d75cb0a7c593`  
		Last Modified: Fri, 06 Sep 2024 21:12:36 GMT  
		Size: 4.7 MB (4719595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199786dc3bbf4414d6a643b11a0b743fd1cded09062701ac3fac26cba4580a33`  
		Last Modified: Fri, 06 Sep 2024 21:12:36 GMT  
		Size: 1.4 MB (1447748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73d4defc1d6e4f221de7b85d026bbd0d0ddc2be3ab9d6ff0d5b43463b4bd4be`  
		Last Modified: Fri, 06 Sep 2024 21:12:36 GMT  
		Size: 8.0 MB (8044135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a24509ff4c938fa7d75af307dc9e647bacc1d5ddbee0f5f90a5fae91082bb0`  
		Last Modified: Fri, 06 Sep 2024 21:12:37 GMT  
		Size: 1.0 MB (1028886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd344967a4a73d33fcbc9679668bbd5c1dcadf04ffa41c12c09a10871050f592`  
		Last Modified: Fri, 06 Sep 2024 21:12:37 GMT  
		Size: 111.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6683b6c0216d2315c0c8bbe43d73c414554106e4792f8c4a249edab1d27044`  
		Last Modified: Fri, 06 Sep 2024 21:12:37 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee97c2743ce6d065d44767a6acb22d351bc9b812acad5e0d2a95c2ab502f5022`  
		Last Modified: Fri, 06 Sep 2024 21:12:40 GMT  
		Size: 101.2 MB (101203279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0f17d837c86f0d0476160ea101a79e1ca3f7f0a22a4f0a0c9a75dce9209934`  
		Last Modified: Fri, 06 Sep 2024 21:12:38 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8529a1ace7f949aa59a615174b676d2df04cdd29b16db79b088082999b69911`  
		Last Modified: Fri, 06 Sep 2024 21:12:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fed4803a30cf42d928942d765514b1ce55e09d7594621870ac1b49b4918329`  
		Last Modified: Fri, 06 Sep 2024 21:12:38 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c99320b1c515dc261c409431ba0697c51b18c9d6a6b2a3a3029b2936279b348`  
		Last Modified: Fri, 06 Sep 2024 21:12:38 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75203d460d21266df72609d05aae74e0c273a31c7cc81cca2f8bdb42b3579d3b`  
		Last Modified: Fri, 06 Sep 2024 21:12:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:aff9166f220be9cbf342a4f7cd5ab5ab62c44ac151399cfb8fd81bccd5e3bf5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016ca5120eae021f4282866a6420f7aff208dc87d37077d4ccd942f14ffc1849`

```dockerfile
```

-	Layers:
	-	`sha256:54fb016eff2817b2ea2c6d677f81f8a66ae8287f4d8d7e91b1fb7a366914096b`  
		Last Modified: Fri, 06 Sep 2024 21:12:36 GMT  
		Size: 6.0 MB (6024601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12c716b309cc81d90681fc8a7e017022223447c8724f12ce7596cd34cabfe1d`  
		Last Modified: Fri, 06 Sep 2024 21:12:36 GMT  
		Size: 53.5 KB (53513 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:a2242bd8075a9ff672c9ec188f10f4c9bc94cb1a454144a17be30fa255d797d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157120062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aaf0e06079315bd36fc0441768266f3eedd9262297f277d13f132aaf6263e62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 04 Sep 2024 22:26:18 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Wed, 04 Sep 2024 22:26:20 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17~rc1-1.pgdg110+1
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb03920874bebaac0313c066da6e1292d051b9bdbd1123d8de0e41a668ccb72e`  
		Last Modified: Thu, 05 Sep 2024 03:12:11 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac3e8856a34a137abae04f17f55e1b3d6a2886709cab091647f4fef7897631a`  
		Last Modified: Thu, 05 Sep 2024 03:12:12 GMT  
		Size: 5.1 MB (5137806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadd44eafb3401af71118033b6cb1bb2e472a4eab258f5ebe20b1b035cbf2d4b`  
		Last Modified: Thu, 05 Sep 2024 03:12:12 GMT  
		Size: 1.4 MB (1393635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae1bc84e0e01888ba16e6babb838cd471e00ecaf928ea1e7beef6406a4b936f`  
		Last Modified: Thu, 05 Sep 2024 03:12:12 GMT  
		Size: 8.0 MB (8044494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db835f9f21dfc6fca2b1aa1d9ed5199d68a03bf4a8742ffe7bc912bee54c791`  
		Last Modified: Thu, 05 Sep 2024 03:12:13 GMT  
		Size: 1.2 MB (1197541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8cb26e1532c0e800af9f9dd22391dda36b40c2d8934633184af9cea8decbe`  
		Last Modified: Thu, 05 Sep 2024 03:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a67336446e997e452360d45b8b18e766a00beff49071b72280c2101482cb427`  
		Last Modified: Thu, 05 Sep 2024 03:12:13 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dbbb2824ee4900f03946580e187f951fafbaaa2246de878719678bc21e00b5`  
		Last Modified: Fri, 06 Sep 2024 21:00:16 GMT  
		Size: 106.0 MB (106026229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1514b86b338024c4c9f6d28fc02f0a1d87490c0d4ee2bd3e3800ddc68680da3b`  
		Last Modified: Fri, 06 Sep 2024 21:00:13 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7a7bff8d11b3f4b273629d818715483edef8a9106cd8e38d3c292af86c2ee0`  
		Last Modified: Fri, 06 Sep 2024 21:00:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9675629767464807dac5b8a92fbae7c23cd9728cdb2a498439ddcf7bfc8c40d6`  
		Last Modified: Fri, 06 Sep 2024 21:00:13 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f99c57e05dfd562314bcb14164c8d5d43e9d6d142d3da6fc3d3a7608ebe328a`  
		Last Modified: Fri, 06 Sep 2024 21:00:14 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe38ef9405f8c98816029b5fab54311c8538f63fbcdd5b35dfe5a6445a08a51`  
		Last Modified: Fri, 06 Sep 2024 21:00:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:e1835b76e4c11e52dea7d666cf78e7d0ffcbf38df5a3a72102faa1996d7cafd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6070606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1539831308d48daaf29a9c388aefa29c44729a925f42cca608e475d270c68cf5`

```dockerfile
```

-	Layers:
	-	`sha256:b7eea125699317d36e9fa73a24fe31564a9346ebc7ee9e4a0b51cdca13e4ba23`  
		Last Modified: Fri, 06 Sep 2024 21:00:13 GMT  
		Size: 6.0 MB (6017016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebcf96c1b8373776178e483f1d18ffb43c1d5b8c4d926b94efa60abb651825c4`  
		Last Modified: Fri, 06 Sep 2024 21:00:12 GMT  
		Size: 53.6 KB (53590 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17rc1-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:7b1a3c0d05bd4425a70481747e4f14e79113069fd1fd2c2122534abc8d555f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150489944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce42e0f4ebbbb4e43e02a3c0966d85e4829859aad60d707a0ac3a5499e0a598`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 04 Sep 2024 21:43:26 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Wed, 04 Sep 2024 21:43:27 GMT
CMD ["bash"]
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV GOSU_VERSION=1.17
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_MAJOR=17
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PG_VERSION=17~rc1-1.pgdg110+1
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 05 Sep 2024 13:44:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 05 Sep 2024 13:44:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 05 Sep 2024 13:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Sep 2024 13:44:37 GMT
STOPSIGNAL SIGINT
# Thu, 05 Sep 2024 13:44:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 05 Sep 2024 13:44:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa74617b6306779ebd9fe52758d2400e81a4c82d80b8c0dd2d87dc02c9187ef`  
		Last Modified: Thu, 05 Sep 2024 05:05:36 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95d1b5d7b1f1d66b6dcf47f49733f151a45df9fc346b7fb40c378aebc629f4a`  
		Last Modified: Thu, 05 Sep 2024 05:05:36 GMT  
		Size: 4.2 MB (4200347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69982ab84b3d7a587c8efaadc9f9082799de1c9183067e379dfb94e9a77af86`  
		Last Modified: Thu, 05 Sep 2024 05:05:36 GMT  
		Size: 1.4 MB (1437973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0ab37ef9cd03d0f26514d5b7d51f3ff5b8c87dd84895233863040b15a688dc`  
		Last Modified: Thu, 05 Sep 2024 05:05:37 GMT  
		Size: 8.1 MB (8098858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29c31483b2b4e9ac50de84964c4b8c92a50c4939ac41224cd8fbde23826d786`  
		Last Modified: Thu, 05 Sep 2024 05:05:37 GMT  
		Size: 1.0 MB (1015252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41e8be03ee08a804c131ea8a9344f92b2d99929f458b23e9745b939edcb267a`  
		Last Modified: Thu, 05 Sep 2024 05:05:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddf8031b775ba82af170e0d5e20c4cf9b27c8e7e983ce8e74a142542dffa1a7`  
		Last Modified: Thu, 05 Sep 2024 05:05:37 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be5353dfb0fddff66e617c6158a82a6736e231dd27701c57b07a735af371f0c`  
		Last Modified: Fri, 06 Sep 2024 20:59:27 GMT  
		Size: 106.1 MB (106052991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e806c0a3b7692c31a3f1a48d9461f6057896a6d1954c2806571322caa90d2a55`  
		Last Modified: Fri, 06 Sep 2024 20:59:25 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52c4c74e8b6d2a5d5e3269335170555dcad79746fd49c0e353e83e6cd0e6e28`  
		Last Modified: Fri, 06 Sep 2024 20:59:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8a73dd1a4d743d71e0c261633e62ff2ae3a0f81a9aab45b7245a1855d0591d`  
		Last Modified: Fri, 06 Sep 2024 20:59:25 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a8d4598b0441048bee3b600b289ad094359f33f8c081910215d8f7d2fe79d8`  
		Last Modified: Fri, 06 Sep 2024 20:59:25 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3423c448c9221b9b2d937cea921443640c0b640bc7786d413df55e280d92afd`  
		Last Modified: Fri, 06 Sep 2024 20:59:26 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17rc1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:4d542e9de1a029a6240104627ab25451779935aea10bd628ee676d60ebeb32fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6062414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862c8a9f80b0fa9fe4fa27bcddb5607dd8a2deb093511f9d192243c72b49055f`

```dockerfile
```

-	Layers:
	-	`sha256:42bfc1486b0544c46ddd604378c3318d4e55b8d99647b6d8420b807282cced86`  
		Last Modified: Fri, 06 Sep 2024 20:59:25 GMT  
		Size: 6.0 MB (6008867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3bdc08826badf4520bad14dfd2dd237a846104492366420e2b6fc226c31c7d3`  
		Last Modified: Fri, 06 Sep 2024 20:59:25 GMT  
		Size: 53.5 KB (53547 bytes)  
		MIME: application/vnd.in-toto+json
