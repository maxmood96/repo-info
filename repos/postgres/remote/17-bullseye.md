## `postgres:17-bullseye`

```console
$ docker pull postgres@sha256:a95402e44be43dc84ec16f8c1cde6174ced2c2c36dc0b1e7bf25ac82c827a49d
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

### `postgres:17-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:b681786ac5737091c713488256cf43fa670796600d69c202e7a11158b511e33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150589835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca3d10bab4f22416d644fa7cace0ea9859da2785585afbcc8571896905b6608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg110+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99926d172eae84b85e5fdf0149deb831ef72189f71569d8eb972cfcb79833c79`  
		Last Modified: Mon, 28 Apr 2025 21:52:28 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d7f692fdb5ec4f250f9b8f956a90544fa6f0f89c955c6a0af0c889965ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:52:29 GMT  
		Size: 4.3 MB (4308121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762964253d2d379bb491a22041a17bbe2393198af49e25cfa0f86a37c7338a53`  
		Last Modified: Mon, 28 Apr 2025 21:52:29 GMT  
		Size: 1.5 MB (1472242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c6a7ec5be5339e8dc8a5214508f3c43fc16290455bb3b7a081122835b94435`  
		Last Modified: Mon, 28 Apr 2025 21:52:29 GMT  
		Size: 8.0 MB (8044589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dde96defb0c87cc99d81b5b490a78122678e1ecd24ab6c13bceae489b38bca2`  
		Last Modified: Mon, 28 Apr 2025 21:52:30 GMT  
		Size: 1.0 MB (1038357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4040d8afcb5fbb838eb54a53b046be50aee3e6a2ed887a355891d18babaf40`  
		Last Modified: Mon, 28 Apr 2025 21:52:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfb4e8f8668a2f2b4a13f340c63948c68f33c7ec509dafe09149bbfca83fa10`  
		Last Modified: Mon, 28 Apr 2025 21:52:30 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73aca14b54a7a47d3d28e194f1f03555eca942325828f74f009e1f24e1f599a1`  
		Last Modified: Mon, 28 Apr 2025 21:52:33 GMT  
		Size: 105.5 MB (105450796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9478e36dd66c518e07e8320f5e0cf82ace85bb23919454621faab13d38352e3a`  
		Last Modified: Mon, 28 Apr 2025 21:52:31 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7b38ffd1a5ede9946c05ea037b8afc6571c221771477daf8031f8ccbed6c0b`  
		Last Modified: Mon, 28 Apr 2025 21:52:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ff484aed95c3e9070897a0227934bb4ecd0fb67bd7d762671ac18c4b80c515`  
		Last Modified: Mon, 28 Apr 2025 21:52:32 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3646f8ba5ababd49ef548e9349fe60d26c2763136327eeeca705a9419e1fd13`  
		Last Modified: Mon, 28 Apr 2025 21:52:33 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc06682456bbfc7dc448e60de068b27fd864d74d5521c43a31124274a08ee2fb`  
		Last Modified: Mon, 28 Apr 2025 21:52:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:035d1aa87b37bcb74f583309888b1c9854e1f3e38253cc3db7e047ce0c90546b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6119438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3761affd3252dbef549c27141c878fbeab486ec063094053e543bccb7ff19d3`

```dockerfile
```

-	Layers:
	-	`sha256:c1fed7ab2da47c248f24ce1b1678b6f0146ea87797dac4a6652fb6782e4aad35`  
		Last Modified: Mon, 28 Apr 2025 21:52:29 GMT  
		Size: 6.1 MB (6065645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf95d7b3e81b95d96cde19e4f7f60c573081d26bdb40db3aedd26831e5eef9c`  
		Last Modified: Mon, 28 Apr 2025 21:52:28 GMT  
		Size: 53.8 KB (53793 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:8cb51d7ac3e1f5dfc1cc72886349f2b4834a7ef25fab05a9f38a2f9a2f78ea5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138764259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7296ff0f9af6656e186e50e32df3f3a5e43aa048427fd00987c4d6b254b60b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg110+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef24263d8904408d4abf0483982a747bf8153de0d52cbb43862ace352b898c4`  
		Last Modified: Tue, 29 Apr 2025 01:18:46 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be0264bb06c2bcee8451dc94c6f8355978ef236eb1a11e672dd512df9c7e7b9`  
		Last Modified: Tue, 29 Apr 2025 01:18:47 GMT  
		Size: 3.6 MB (3601746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a9051786ef8ca1e9ce4ec47810682bb5f8c26e9d78eb7e1f873f82d85c3f16`  
		Last Modified: Tue, 29 Apr 2025 01:18:46 GMT  
		Size: 1.4 MB (1439251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604c2a9e01f796a5afd8b46c903da93b951474ab34284f961ab4c3e793b7df3c`  
		Last Modified: Tue, 29 Apr 2025 01:18:47 GMT  
		Size: 8.0 MB (8044545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7035eab34ad95006258ce8e6a6d625b8c11281827a56ddc22c8384df5f25bc27`  
		Last Modified: Tue, 29 Apr 2025 01:18:48 GMT  
		Size: 908.6 KB (908650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab74d412aa207d36e88063c7272cd4c92f0e39a1c3df9afd5c17b2c29490b1b5`  
		Last Modified: Tue, 29 Apr 2025 01:18:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb07ab6f9f4f5ffcc3eb65dc7f2c635f65140e5fed60a158d072087f7a348c79`  
		Last Modified: Tue, 29 Apr 2025 01:18:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bcdba9c8fe696532235f00c14e29ba2372d2406b910a7cd8d28985719ab297`  
		Last Modified: Tue, 29 Apr 2025 01:18:51 GMT  
		Size: 99.2 MB (99206510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c85f43102a40d7c38b0640b25e229b187c7754b572629b2471a792243899d1`  
		Last Modified: Tue, 29 Apr 2025 01:18:49 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8507e801f3c2a146d181a4b38d65a43cdee19ba761916a898c20666a4f8af617`  
		Last Modified: Tue, 29 Apr 2025 01:18:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2695d304a6bef27cf62135be6ecdc85a12ddb28afe93b629363a691328a3dea7`  
		Last Modified: Tue, 29 Apr 2025 01:18:49 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61adbff9138fc1cdc7b70fc7a3e916db5bc6351450eb2efd3ddbfc71feab6316`  
		Last Modified: Tue, 29 Apr 2025 01:18:50 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f2d3f0d02acabee55a97e3b420772518602a0a28b7a0461afb21318586292b`  
		Last Modified: Tue, 29 Apr 2025 01:18:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:5683f9ada2567f68bf92bf47c7107165e4232e2a39d2e7c5a096be5251aa0390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6136827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d9b95b587599fab9403675447d8d369e5ca5148a2a8d942a921d0517116c57`

```dockerfile
```

-	Layers:
	-	`sha256:6743358523cb5c802617d90e67859c85dd978b7f94e8392c27715ea1dfef847b`  
		Last Modified: Tue, 29 Apr 2025 01:18:47 GMT  
		Size: 6.1 MB (6082838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f21d3d602fa8d7bbc337f6eff512436a59c1524742bc2ee70bb57023dbbb5c2a`  
		Last Modified: Tue, 29 Apr 2025 01:18:46 GMT  
		Size: 54.0 KB (53989 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:5215734f56edd0a9f1b2685ef117c5414e0bdabf9f093b7840fa0a8bdf558f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147591214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768d10bb3d3412169983f7a3e3d89aaf69cf10707a1776eae89688d224638e37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg110+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7918240589a5ba7d1c8b459d165ee099299ff7292c7efe37c35245ef9c03f51`  
		Last Modified: Tue, 08 Apr 2025 05:24:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2199ade2816948c911e62ea0c4b3bfb82109f914b16bc7b4fc4bad34e0c3ba86`  
		Last Modified: Tue, 08 Apr 2025 05:24:26 GMT  
		Size: 4.3 MB (4312868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32eced68b9086b2d3a09c6120ff5e43a321a6554ac01ec9c187cef515884e5c`  
		Last Modified: Tue, 08 Apr 2025 05:24:26 GMT  
		Size: 1.4 MB (1404211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac22e9e0911af240f848eca85f950b71436ea96de087af3e9a600d6ee3a9f1d`  
		Last Modified: Tue, 08 Apr 2025 05:24:27 GMT  
		Size: 8.0 MB (8044543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0ba9935e21a6295487171eb2832d2e01c3e5d3ebbac901a93b23f157e98caf`  
		Last Modified: Tue, 08 Apr 2025 05:24:27 GMT  
		Size: 1.0 MB (1026588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bad7a30bdfd7f60560671c6793d3e2442300d01ac6e271785e8767902d2f55`  
		Last Modified: Tue, 08 Apr 2025 05:24:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41837d2b3a931deee49f7341a176013d1eb8f3f42769b07e358e76884101cf31`  
		Last Modified: Tue, 08 Apr 2025 05:24:28 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2560539d684d6b942c17c8b1f5bc0c61c843faa9b3aec5ed43959b9b0cbe6`  
		Last Modified: Tue, 08 Apr 2025 05:24:32 GMT  
		Size: 104.0 MB (104032372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813046815dc8bb5339fa18c4b6492868734e444c47935fc916f6c7ad04c27002`  
		Last Modified: Tue, 08 Apr 2025 05:24:28 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d568531df4f4baffab190f9437dc68084b46e5fddb124e6c47ec5f8044e6d90`  
		Last Modified: Tue, 08 Apr 2025 05:24:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59fc1e7302987f3a0ae0b7a4fd5c0fdecab1c757366de654220bbe6360cafac`  
		Last Modified: Tue, 08 Apr 2025 05:24:29 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b21cb0e8d06d0a36812660301e6117f08e7718ee29c530b81d3e37c7d5bafc9`  
		Last Modified: Tue, 08 Apr 2025 05:24:29 GMT  
		Size: 5.5 KB (5471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5e06c4aab71ea52475ce5137e6cd465d81bee8b353e6f91e3dc66966b56560`  
		Last Modified: Tue, 08 Apr 2025 05:24:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:a3da88ac22ce906338d400ece96692f472559d326a070da5cded4d574cf41f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6126748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19839cf1b2063af3a425181e044b8c0339122be2bc4146901272a1888ae85e32`

```dockerfile
```

-	Layers:
	-	`sha256:1374f201d23980b06c90443b1d5810771b74de5793478490cbae6fec4bfa02f1`  
		Last Modified: Tue, 08 Apr 2025 05:24:27 GMT  
		Size: 6.1 MB (6072698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c391c2d13d6cafbbf5452164372fb4fc576e9a86af203897f7c74a30345d8006`  
		Last Modified: Tue, 08 Apr 2025 05:24:26 GMT  
		Size: 54.0 KB (54050 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:4dc3c977af7d7e36e2d6637de69f2f5614b5c9090588426eff2422cd2e98dbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158838229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c8d10ead047a2b4f5106d39e2b190bd47dd2671078d2f8bfa5d36a5ebf2153`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg110+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae345669c2656bfa3f7e26ad41e8474cdb0ec4f6ce5daa22c2e8f9809ead7ae`  
		Last Modified: Mon, 28 Apr 2025 22:03:57 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df44bd04a1875bfe5ae2771feb4b2d94c6f80eebca6597e1d6031677f88bdbd0`  
		Last Modified: Mon, 28 Apr 2025 22:03:56 GMT  
		Size: 4.7 MB (4719701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2163525bfa9fdf2e675a019098787d632610c31a1b1f932369fd118a7df04b54`  
		Last Modified: Mon, 28 Apr 2025 22:03:56 GMT  
		Size: 1.4 MB (1447782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b4ac6f2dfa14b7c279a7943a5732a6dfc5a95e18276425a6e6a02ca9010a27`  
		Last Modified: Mon, 28 Apr 2025 22:03:56 GMT  
		Size: 8.0 MB (8044477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7260b8b950af44cc5fd8311b7ede3ce70b6f97d25a445508b41d53babfcdbf49`  
		Last Modified: Mon, 28 Apr 2025 22:03:57 GMT  
		Size: 1.0 MB (1028918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c4fc6c71b5af681b77293b328c85d48f18420e1e42777b02a4992c19c7e101`  
		Last Modified: Mon, 28 Apr 2025 22:03:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4333276592b88e83035cd328e4fe84b7defdc8cccbe281f34a69cbf1e4f31a4`  
		Last Modified: Mon, 28 Apr 2025 22:03:58 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0315bcc96442eb64cd4b485be42dd55ddb624085a8648dc3bb24cd06f20a65ff`  
		Last Modified: Mon, 28 Apr 2025 22:04:01 GMT  
		Size: 112.4 MB (112388333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53c7568a9fe3e4ee59b39379f06338f67e0ff77d996f00d63518c2d7ccd50c9`  
		Last Modified: Mon, 28 Apr 2025 22:03:59 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5da01fc9410d751d1421099a2da187f5a4b36581b8e47ce43196e7b42f68ed`  
		Last Modified: Mon, 28 Apr 2025 22:03:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059a5bb7ea0c56f9739e6dc5b6f73dc4c7222b1f41075ede2f7c41f3436f478a`  
		Last Modified: Mon, 28 Apr 2025 22:03:59 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd3feedf3a5cc676d546dfa6caa8187210022ef46caf28efaa36e279922e2e4`  
		Last Modified: Mon, 28 Apr 2025 22:04:00 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc77ee885b2db2779b4d865ea925e7fbcb58ca66571659dcc8ce8739be2d4e01`  
		Last Modified: Mon, 28 Apr 2025 22:04:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:ebd65ad906f4ea559f570e773b68f99b502b9a8ead56f75c829f1146c6b57617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6134344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddccfae0da28db2f1248a02eb5b8bac44959f6e5f7b809341d4bf36b75055ba5`

```dockerfile
```

-	Layers:
	-	`sha256:f950d60933fa0747c829cbc849d3b8ea658bba7dbf84027203bbdd57dd51967d`  
		Last Modified: Mon, 28 Apr 2025 22:03:56 GMT  
		Size: 6.1 MB (6080600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a73506a93f421f746fb38208b53454013d618506596bab7b443c8e976d39b36`  
		Last Modified: Mon, 28 Apr 2025 22:03:56 GMT  
		Size: 53.7 KB (53744 bytes)  
		MIME: application/vnd.in-toto+json
