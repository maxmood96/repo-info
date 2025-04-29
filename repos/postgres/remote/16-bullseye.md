## `postgres:16-bullseye`

```console
$ docker pull postgres@sha256:31eed82752caa6f26ba3aaf15a79e5324a17dac3a467065a93acaef13a85e92f
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

### `postgres:16-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:304357aaf19abf6c75136e91d0a6ed2040af0c36fb63579bb8bb84025ce7728f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149395824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07d88c0449e0642f4856b57bbef2c9ea139d80762c080eaee73084cde53532d`
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
ENV PG_MAJOR=16
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=16.8-1.pgdg110+1
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
	-	`sha256:ebeb0346d94212a13cf2112c4523475ae6091eebb4ab7cb9242aae816b476a42`  
		Last Modified: Mon, 28 Apr 2025 21:52:49 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4b5de3926d8b69b8481e414066b151cb32a4d8710798c7300aafc29b297556`  
		Last Modified: Mon, 28 Apr 2025 21:52:49 GMT  
		Size: 4.3 MB (4308139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38fe34639df680d308afe334fe9c404bdaa5f6d3ee42a5c229413d2428a9f47`  
		Last Modified: Mon, 28 Apr 2025 21:52:49 GMT  
		Size: 1.5 MB (1472266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e00e0b4d1ac3930240d1245f0cf72dfec7f9756110d5c00ea9df161d99ba1`  
		Last Modified: Mon, 28 Apr 2025 21:52:50 GMT  
		Size: 8.0 MB (8044594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60c02f6fb896f7700ce6afd8b5592ba8bcf0ef267e4d76482d34b667d7f0db0`  
		Last Modified: Mon, 28 Apr 2025 21:52:50 GMT  
		Size: 1.0 MB (1038374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fed70791e7cb0a14441beb0fd51a540f53801f4a6b6de544447321dd20faa10`  
		Last Modified: Mon, 28 Apr 2025 21:52:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54449f39f52f7010e87cd36b5331a8c723402184446898758c1f9e2a73b3853`  
		Last Modified: Mon, 28 Apr 2025 21:52:50 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd8aca7495488c6c97cd19f1737b2b5f5da9912590090fdfb948baa9fe35aa3`  
		Last Modified: Mon, 28 Apr 2025 21:52:53 GMT  
		Size: 104.3 MB (104257044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd74e074c00677fec292217d8e79b3edabec672c9ed7eeecb14c8ae02dfd86f2`  
		Last Modified: Mon, 28 Apr 2025 21:52:52 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7b6436746e323b163d7d6b90884e477af9d3df2960ca5a94364eabfe949df8`  
		Last Modified: Mon, 28 Apr 2025 21:52:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109da62ba3a3fba4c725b745ddd8c16db10d0fe57d53162a1f0490962f664564`  
		Last Modified: Mon, 28 Apr 2025 21:52:51 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c1a99e4015a9bba0569bfae2eced6853ee1fab8f587fbe2b087b70a5807e34`  
		Last Modified: Mon, 28 Apr 2025 21:52:52 GMT  
		Size: 5.5 KB (5472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991855c0f2d16640b5c17280b0e29f6f043f0e37c1f2f1af5b1b59ac45d42a56`  
		Last Modified: Mon, 28 Apr 2025 21:52:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:0ab7f262ae9b5406814defff51879db6949775921b1242ac5d580460ec8db525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463dcf2bc0a7a1dd55511a34c12a6c557563f875a624dac049f8131e99631056`

```dockerfile
```

-	Layers:
	-	`sha256:71ca4e8e51fb22e750d148b4eda3b97b0778b11d3b07f186ef649ad809f91fb3`  
		Last Modified: Mon, 28 Apr 2025 21:52:49 GMT  
		Size: 6.0 MB (6049151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af16a1d5b56f84b6b378bd7c0d20d8d03966832f55bffd6daf9d6a0f28a4596`  
		Last Modified: Mon, 28 Apr 2025 21:52:49 GMT  
		Size: 53.5 KB (53482 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:59c28f44e8ad8a606f681a2b6cad683f14fb3841e578872d36f3182e9ef56e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137616077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee58a85381e4f632b530ea248d660101b7b40e3addd5a9f1983c1e3eb48b619`
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
ENV PG_MAJOR=16
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=16.8-1.pgdg110+1
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
	-	`sha256:adb4bb4e0c8d4f292bdfba945ee51c4e783636a87162a131763f5baac94342a2`  
		Last Modified: Tue, 29 Apr 2025 01:49:06 GMT  
		Size: 98.1 MB (98058645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb215843e1320de0f07ba8714ffb921e2eadf1ad640b5ce1f7570b761dc1111a`  
		Last Modified: Tue, 29 Apr 2025 01:49:03 GMT  
		Size: 9.9 KB (9924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a594244abe1591e305054548cf462056606fc16f54acc89b149d098145390db2`  
		Last Modified: Tue, 29 Apr 2025 01:49:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b965f988469280719bac4308c344b943f10138f82db2758c38dd39764e213982`  
		Last Modified: Tue, 29 Apr 2025 01:49:03 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de551f7953d24532e9092254ece0a1fcba49d3a3a1b3f294b1e72081e9b7e541`  
		Last Modified: Tue, 29 Apr 2025 01:49:04 GMT  
		Size: 5.5 KB (5471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdbe3e12c44a2d1b15e852df6dac8463712dda1ced166521be9a527d7c6009a`  
		Last Modified: Tue, 29 Apr 2025 01:49:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:577308ca03d004746957223cedab0d6eb3b32e5184693a1e11c4a5e42dffe58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6118278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d804af10b6916721cabacfa6ab5c5e127b2138da07b3ecfd1a1aa967feb110d`

```dockerfile
```

-	Layers:
	-	`sha256:6bbf0c0de463a769af218275b602667edbbcb689d9604a4e77d612545d63c342`  
		Last Modified: Tue, 29 Apr 2025 01:49:02 GMT  
		Size: 6.1 MB (6064608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce14e5400d7f74b7aaaad13122342d782b2b9fc266e2bf8535ff5c8a77f13fd6`  
		Last Modified: Tue, 29 Apr 2025 01:49:02 GMT  
		Size: 53.7 KB (53670 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e098b33713a4e24f180740dee5636504b13220245e92ece8a3ba8c55f1dc5213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146397798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d52893f34c71c1747d6eb2eaa802f280046cbdb010caba151a8f2083c0d2b5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
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
ENV PG_MAJOR=16
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=16.8-1.pgdg110+1
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
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430be6dbf04f131ce669a81b7ec254e6c1afa78bc6a6b4bdef56b88b7cca59be`  
		Last Modified: Tue, 29 Apr 2025 01:08:30 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc012e2ac3cd143798c99a8b0d19c23949f3defbd7a2cef00860da14e0fd5857`  
		Last Modified: Tue, 29 Apr 2025 01:08:31 GMT  
		Size: 4.3 MB (4312815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393efb3fedc0bab07650f589fb317adeff988e7c1a5c9754d3889f9680744207`  
		Last Modified: Tue, 29 Apr 2025 01:08:31 GMT  
		Size: 1.4 MB (1404189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264eceb26e7bad129f6e1ad046be7b1d1d3f8679e574dc8cd1ab3c59e0627256`  
		Last Modified: Tue, 29 Apr 2025 01:08:31 GMT  
		Size: 8.0 MB (8044401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a312d2ff9cd15091b4002f19ef26a812b9d4cae31d64c6861e93426de9a3f8a`  
		Last Modified: Tue, 29 Apr 2025 01:08:32 GMT  
		Size: 1.0 MB (1026596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c458e63551b140446dfc776df323cf95c5da595fe4eab5103808460f721bc927`  
		Last Modified: Tue, 29 Apr 2025 01:08:32 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c423ff53f9e553e0e57a67f62c0886078742f3d007f8f41c0ec4f482f21b6c44`  
		Last Modified: Tue, 29 Apr 2025 01:08:32 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35afe61886f80f8f0e830ce823d8affd9e228385cefd7d30ba6fd10e9d5b7f18`  
		Last Modified: Tue, 29 Apr 2025 01:10:06 GMT  
		Size: 102.8 MB (102844336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3128c7adbf3ad40b76f5e2b1c28ad8fae0611e01085929049924133055bf67`  
		Last Modified: Tue, 29 Apr 2025 01:10:02 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524458ae63d1e713eac8a81cdfb9ba5b3908b3d64d0f007d89865c73614a36a9`  
		Last Modified: Tue, 29 Apr 2025 01:10:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee61f4d8e8081811ed338862df50c28120efbcd0253ae9f2a561eed78f8d833`  
		Last Modified: Tue, 29 Apr 2025 01:10:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ee31e8f7bbfceb2f1d018296be1e40a8d785c85225754b7385a4a11d744df7`  
		Last Modified: Tue, 29 Apr 2025 01:10:03 GMT  
		Size: 5.5 KB (5470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24ae67f03d67ae1e7480ef1aafd638af18983269daa51041ede5428075a3adf`  
		Last Modified: Tue, 29 Apr 2025 01:10:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:57a1d05425f61c1a7a850d281333223276bffba05cb6c98c76559dddeee12b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6109166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a98f3fc6fc1a9053ba2e243d05d762e11d8485ba4b3178bed829630c43dafe7`

```dockerfile
```

-	Layers:
	-	`sha256:7d38005f2ec67472b961d1e7c4212ecc7e167b2115580a1a8fd41b05857aeb42`  
		Last Modified: Tue, 29 Apr 2025 01:10:02 GMT  
		Size: 6.1 MB (6055439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8317ae943ae5f58947408955f08164d83ef2a2632bb099baad54c887a299d439`  
		Last Modified: Tue, 29 Apr 2025 01:10:01 GMT  
		Size: 53.7 KB (53727 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:1159e4add7327e2759227ed6242bf10303754a4fdc9d3d7c2bd226592b8f48d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157593855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54a5dfd6ebf26f9545dbb1897dbddc5637e4065fd7aafb6beba7ad21fc3c6b1`
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
ENV PG_MAJOR=16
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=16.8-1.pgdg110+1
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
	-	`sha256:5fec82cba98bc0f8a10896765fb61cf55050a4340e0ff21a246d3054f897dbb8`  
		Last Modified: Mon, 28 Apr 2025 22:02:47 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db05c6c29930e8c7d31d6a9b9964cdb651e26304bce915bb9d73cade2643c079`  
		Last Modified: Mon, 28 Apr 2025 22:02:47 GMT  
		Size: 4.7 MB (4719714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f0a351dc5ba1751893737702acbbc1404f3ea23df5063300153b86f5ec99b`  
		Last Modified: Mon, 28 Apr 2025 22:02:47 GMT  
		Size: 1.4 MB (1447800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcba7ce9cd4bac6e6e06ac3fa910f7dd4c82e8cbcf4c4b06145a41361027e0e`  
		Last Modified: Mon, 28 Apr 2025 22:02:48 GMT  
		Size: 8.0 MB (8044265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aad8a0047a6735f3ba7f3f31deaa51c453a561fe4f514efde4f87986f892bb1`  
		Last Modified: Mon, 28 Apr 2025 22:02:48 GMT  
		Size: 1.0 MB (1028920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9e1a112da088d8a6d160571e04ca8ac9cb05d150417705174649a5bc70a87d`  
		Last Modified: Mon, 28 Apr 2025 22:02:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94fe0516341bc6352275784009522b62f8abc49835e9c537a1f8012a910f765`  
		Last Modified: Mon, 28 Apr 2025 22:02:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269cc76ae9b31f58ec23a44c42f720a56c04b97916fc8e40ec42acc3985c0229`  
		Last Modified: Mon, 28 Apr 2025 22:02:52 GMT  
		Size: 111.1 MB (111144451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ecf2f3c8f35a874c237837b12627644872a779d76ece3d8e111f8eb68cd828`  
		Last Modified: Mon, 28 Apr 2025 22:02:49 GMT  
		Size: 9.9 KB (9924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a0928f201310c8813868b47b9ff4be15def37bfd1ee5ddc14e34f93c9efd89`  
		Last Modified: Mon, 28 Apr 2025 22:02:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b998de13486aaf4d2f03d3bb23a87f1b3c7c2e854c87ba7bc98f12a83b07a61`  
		Last Modified: Mon, 28 Apr 2025 22:02:49 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ed3b785ff0ac8f359d57dde6e61c614dd15790a3411a16b6f9acd6ca153ecc`  
		Last Modified: Mon, 28 Apr 2025 22:02:50 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e8648019750cf6400d2a580bb68a14f13141fcf2838a11698013ab692ddf0b`  
		Last Modified: Mon, 28 Apr 2025 22:02:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:688af33e9d039850034e6c1e5e627bd9ec726e5948c506ec40cfa1a048b4e72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6115821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad61887f4cf7964bff4bb9f3ec323e9973313f0217f86f875d9003e1832a7f8`

```dockerfile
```

-	Layers:
	-	`sha256:ae18a066b48584932cc3c4ddeb2587173210a3e74d646fdf25dc53d1e0d64d31`  
		Last Modified: Mon, 28 Apr 2025 22:02:47 GMT  
		Size: 6.1 MB (6062383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d0f0350d6dd7d8fdcbfee8bb79fbee62782306294b56e875873e3fa5c0f96b1`  
		Last Modified: Mon, 28 Apr 2025 22:02:47 GMT  
		Size: 53.4 KB (53438 bytes)  
		MIME: application/vnd.in-toto+json
