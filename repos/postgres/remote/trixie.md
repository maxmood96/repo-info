## `postgres:trixie`

```console
$ docker pull postgres@sha256:69e8582b781cb44fa4557b98ed586fe68361e320d9b12f9707494335634f4f3d
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

### `postgres:trixie` - linux; amd64

```console
$ docker pull postgres@sha256:e47309bc9a186ae58078b35a385dc89216d922c0f2f5cbb2bd6390e878dce27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162289123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ea5ef23f82e05dade8d352d51e674e8330f502fce0d1bee4c69550a6863a48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 19:22:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:22:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:22:23 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:22:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:22:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Feb 2026 19:22:28 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:22:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:22:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:22:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Feb 2026 19:22:32 GMT
ENV PG_MAJOR=18
# Thu, 26 Feb 2026 19:22:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 26 Feb 2026 19:22:32 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Thu, 26 Feb 2026 19:22:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:22:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:22:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:22:47 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:22:47 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:22:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:22:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:22:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:22:48 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:22:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:22:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967e70a4ad93c789d2614a38ff63c684372551b38e3cbfcd6fe9539936d34a1b`  
		Last Modified: Thu, 26 Feb 2026 19:23:08 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b030cb6bea0e392ad58ee261fab68a51488eb9582e14026b2fbfbe0ff5d6714`  
		Last Modified: Thu, 26 Feb 2026 19:23:09 GMT  
		Size: 6.4 MB (6441194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f3de31936a2444391fcc13e7475b6738759dc79455eea0e5a27bc814546081`  
		Last Modified: Thu, 26 Feb 2026 19:23:08 GMT  
		Size: 1.3 MB (1256735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358db71ef364a9584f94fb393ed3cd702d44074327b300517058dd4cde379afb`  
		Last Modified: Thu, 26 Feb 2026 19:23:09 GMT  
		Size: 8.2 MB (8203845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3859b312d2537faf483f315ca41b5fe7815c6d8176b4ba68bf52b5bd156a2189`  
		Last Modified: Thu, 26 Feb 2026 19:23:10 GMT  
		Size: 1.3 MB (1311621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a239f8dc77305d869ef6d080351479e5de25f4b3a191afce0ad320407d0bc9`  
		Last Modified: Thu, 26 Feb 2026 19:23:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2113a73362d0b8ebe7fbd6acfe8b6bb7070439967ab7eb46f2cf531cbf52fa`  
		Last Modified: Thu, 26 Feb 2026 19:23:10 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e232269e9149001f7d6fb0cec2a8e4ee231cefa59951b2e1fa9a28fcfd617c53`  
		Last Modified: Thu, 26 Feb 2026 19:23:13 GMT  
		Size: 115.3 MB (115267187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea32e6f70e8bb4da578fdcc5cd381d0fb3493470b3e06df9329c32770e9089b`  
		Last Modified: Thu, 26 Feb 2026 19:23:11 GMT  
		Size: 19.3 KB (19328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4ad6e904edd001eda43540270789d34f738665f74b8d3d1830e8bf167df08f`  
		Last Modified: Thu, 26 Feb 2026 19:23:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7dee01ee448e16ab11f0716ffa1b5516ee65830bab5368c3362d111cdec5b34`  
		Last Modified: Thu, 26 Feb 2026 19:23:11 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0480b5ae6db990e0255123baa59cb1f3cf0447669292474fdba6be0df72bd840`  
		Last Modified: Thu, 26 Feb 2026 19:23:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:8b8f920c3efe71933c9c393890e76c17e828ce7198bfa9dfa4d4f609e49b3db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6009209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d4ca4220ed1b3cb8c1069cb5714458f935a41fc16c9e863e8069efccfdd8f9`

```dockerfile
```

-	Layers:
	-	`sha256:3facd37768c9a453f7fe53885c69595229b185633b77649d9d3dbc5d91523ce3`  
		Last Modified: Thu, 26 Feb 2026 19:23:09 GMT  
		Size: 6.0 MB (5956751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f0f713dfa14c8236e1bfba8db2edb9177d7d6ece1ec99e6cbb559de98b9d7d`  
		Last Modified: Thu, 26 Feb 2026 19:23:08 GMT  
		Size: 52.5 KB (52458 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:224cae6edebf9f964128b1e509bf14066effeaa3902df7824af36e0ca9ddc242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91467190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b016550e347a115f0ce0156061c3cd7ee8f4e9cd6d6b730b7960a3462933b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 19:15:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:16:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:16:13 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:16:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:16:21 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Feb 2026 19:16:21 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:16:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:16:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:16:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Feb 2026 19:16:29 GMT
ENV PG_MAJOR=18
# Thu, 26 Feb 2026 19:16:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 26 Feb 2026 19:16:29 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Thu, 26 Feb 2026 19:29:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:29:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:29:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:29:37 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:29:37 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:29:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:29:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:29:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:29:37 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:29:37 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:29:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f659b68534a399b6c2ec6cad7e375b54c5f1396df8bf0ba0f17bb2abc9e14af`  
		Last Modified: Thu, 26 Feb 2026 19:29:50 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f2339590d8a7345ac971defc97ef20d1a7e2e21af5445151fc2719a98ed5fb`  
		Last Modified: Thu, 26 Feb 2026 19:29:50 GMT  
		Size: 5.9 MB (5932418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d342497ab0886c49e45ae30397b71bcceec4cbdd3c5194b8a0d90f3ff07a8a2d`  
		Last Modified: Thu, 26 Feb 2026 19:29:50 GMT  
		Size: 1.2 MB (1227515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80538fd2c25ae5b4c6604999d9b6b3d90e2c24cd57d7235eeab03e073f71c3c`  
		Last Modified: Thu, 26 Feb 2026 19:29:51 GMT  
		Size: 8.2 MB (8204272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1539e11634098169d4c37a30365fbc976e8b67ec9903f3ccb9045b0957812d`  
		Last Modified: Thu, 26 Feb 2026 19:29:51 GMT  
		Size: 1.3 MB (1317346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f49a617cd6ef8e5a9ce60302957ed655c110de09d5d659352db865c8c4aa15d`  
		Last Modified: Thu, 26 Feb 2026 19:29:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b76a378fa77bca080dc9ab300cf70f63e40e94727728e18d3c298b54bd435a`  
		Last Modified: Thu, 26 Feb 2026 19:29:51 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c7c6a2b53a060f0003f2d189b6c5f495019659f218b6b6ec2d2b3beaa3da9a`  
		Last Modified: Thu, 26 Feb 2026 19:29:53 GMT  
		Size: 46.8 MB (46808118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc400cf154be062d4d52f8dfbb5fe77a73396d8450d51791dd78c313c3fa7f3f`  
		Last Modified: Thu, 26 Feb 2026 19:29:52 GMT  
		Size: 19.3 KB (19324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4f747c44d033bb8c312688096bb5501aab44992f8ce947e0a83acd619a1e96`  
		Last Modified: Thu, 26 Feb 2026 19:29:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab263f669105e22dad9758168f5b04825b69354ba4c615b94055a3d9c548f0d`  
		Last Modified: Thu, 26 Feb 2026 19:29:53 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40a6d3f89604f83364d2a33a8557f0f7598106305f03882e2844f83f3e25c98`  
		Last Modified: Thu, 26 Feb 2026 19:29:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:234c060cd149c2c2e2532ca2388633943e5fbc9de8551256578e327a8277e7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef4699034ccbbd0bc29e2589fef4d8c26f897c94b6b00c632091f2ee3308793`

```dockerfile
```

-	Layers:
	-	`sha256:ff89a629b4cb804b8cd90f4e85f2bda8f170f50f082e31be80155e1aac8a00a4`  
		Last Modified: Thu, 26 Feb 2026 19:29:50 GMT  
		Size: 5.1 MB (5119894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9a9e1f6fcc0f300cdb0eef91afa8d5e936f712c459ea0a952c6a3f7cce8d25`  
		Last Modified: Thu, 26 Feb 2026 19:29:50 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:2d8ac740f626ddcaf2ad76326623a73ad2c8d836b93060aa7a360c3e0aac7896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87791269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63af5f46ed8242d5dc147fc652bf2421f94a80c6e1fb9a826986cfa949a2f93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 19:16:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:16:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:16:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:16:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:16:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Feb 2026 19:16:24 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:16:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:16:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Feb 2026 19:16:30 GMT
ENV PG_MAJOR=18
# Thu, 26 Feb 2026 19:16:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 26 Feb 2026 19:16:30 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Thu, 26 Feb 2026 19:28:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:28:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:28:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:28:30 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:28:30 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:28:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:28:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:28:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:28:30 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:28:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:28:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a23d9fb6699e9423251c04054c68ee34ec1a6378c52412873bacbf82c7ef0ba`  
		Last Modified: Thu, 26 Feb 2026 19:28:43 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372be9f4c601b5b467ff628e4e68aea5ae73cb4246df333e54929cc56383a09b`  
		Last Modified: Thu, 26 Feb 2026 19:28:44 GMT  
		Size: 5.5 MB (5496576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de01a5895372456d52763cd16ba9b1961fd3bb8dac6f5cd8745f94a4829b14d`  
		Last Modified: Thu, 26 Feb 2026 19:28:44 GMT  
		Size: 1.2 MB (1222360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9a26b4b5c0e240c598eb04bf7850e4512991c499c99fb561ed770d9148b36`  
		Last Modified: Thu, 26 Feb 2026 19:28:44 GMT  
		Size: 8.2 MB (8204035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4212f430c2a1d7fba130e11a52094cbf6dc077651477a5a2b584976ff74e3cf6`  
		Last Modified: Thu, 26 Feb 2026 19:28:44 GMT  
		Size: 1.2 MB (1172605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4763bf57b944df9c46ea6b7915a54b574e1865adac154cd25e75e62ce100218`  
		Last Modified: Thu, 26 Feb 2026 19:19:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4653692aa65cabdc94a44d695627a64da37120a971c27336412aa7efd455ca`  
		Last Modified: Thu, 26 Feb 2026 19:28:46 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886b03b0f19ac0c6e7cf171debbfd67067f79f6658613168aba4e3cbc19fe6d1`  
		Last Modified: Thu, 26 Feb 2026 19:28:50 GMT  
		Size: 45.5 MB (45452025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceda216dd6a33bd3472b74510afac6994249e0de8575a053cd686059d2d8d63`  
		Last Modified: Thu, 26 Feb 2026 19:28:46 GMT  
		Size: 19.3 KB (19341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338ed110921435045aa5e8b6e6023f74ce83f6764a00438bf862d34f41667351`  
		Last Modified: Thu, 26 Feb 2026 19:28:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920cae6dd310d82779e6b4af8e5acd750b4c4f146489e3b5c9437fbbc170e6aa`  
		Last Modified: Thu, 26 Feb 2026 19:28:48 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e266ad760bc746a335a572851de362d6d592d892422c74002d56f6b3fb3988`  
		Last Modified: Thu, 26 Feb 2026 19:28:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:2718380aa0e566377f1980db537b5b2e8090c322854795f356d2daa62a58ce0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4623f2d016f3978485c7139e4a8308d9673aa8aea3c1a319fe7ea07786ff47c8`

```dockerfile
```

-	Layers:
	-	`sha256:861934d4b5269515389a6fdbcde739ffb630bda7957f25cab2f50ec870b55baa`  
		Last Modified: Thu, 26 Feb 2026 19:28:43 GMT  
		Size: 5.1 MB (5119199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b161f9d4764a0060170994d49b9fc484b55c33ebb9a0609561fdc3d75271bcfd`  
		Last Modified: Thu, 26 Feb 2026 19:28:43 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:61d20fce33a2fafc227295df2da7cf40ff1fdd9567ffd893b6f1a068efa08684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160905008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56ee5e41a2dd4c36cd8b2b8fcb3f889fdeea88532689691f0080461233ff4b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 19:21:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:21:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:21:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:21:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:21:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Feb 2026 19:21:45 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:21:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:21:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:21:50 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Feb 2026 19:21:50 GMT
ENV PG_MAJOR=18
# Thu, 26 Feb 2026 19:21:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 26 Feb 2026 19:21:50 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Thu, 26 Feb 2026 19:22:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:22:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:22:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:22:07 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:22:07 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:22:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:22:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:22:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:22:07 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:22:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:22:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32907a42ce24e08decf85215562e8949ee69fa3b11615b9b74765354da339743`  
		Last Modified: Thu, 26 Feb 2026 19:22:27 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00600fe93225f91203aac55a357029b22c6d17f6fc5b0c0c3bec63f4beb307e4`  
		Last Modified: Thu, 26 Feb 2026 19:22:27 GMT  
		Size: 6.2 MB (6234051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8f335dbb739aed9a5fc3e1fd5becf7d5dd2276d3bd14c1d61ecaa973040e7d`  
		Last Modified: Thu, 26 Feb 2026 19:22:27 GMT  
		Size: 1.2 MB (1209614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6617baed4df246b18dbddd444e69769e300a91ff94574814b41fb2e7f936ba`  
		Last Modified: Thu, 26 Feb 2026 19:22:28 GMT  
		Size: 8.2 MB (8203983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae13f539d2874bfdc2736b3d00e78012c9d4f80049820ad2b363f5af0900491`  
		Last Modified: Thu, 26 Feb 2026 19:22:28 GMT  
		Size: 1.2 MB (1220585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dca2b464db8a548a3e7e27267b0eebfdcab93cb828ed306d5b260b4722fa310`  
		Last Modified: Thu, 26 Feb 2026 19:22:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678efd827da7a0e036d9a535122ed8bdef483b33e19f518880f073e8f19993e8`  
		Last Modified: Thu, 26 Feb 2026 19:22:29 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4769a7dd3c716fee265ffb9263a043a3157642525236c1690db23c11f4dd6e`  
		Last Modified: Thu, 26 Feb 2026 19:22:32 GMT  
		Size: 113.9 MB (113866763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e712b78f59fd19ca57679c42b83ce510dbb2d906d3dd5d18d8172bce7bf786`  
		Last Modified: Thu, 26 Feb 2026 19:22:30 GMT  
		Size: 19.3 KB (19330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf9a691c71ee27e28a027adb18320c7a3b7f072af820e261617dd1d53b0a322`  
		Last Modified: Thu, 26 Feb 2026 19:22:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b4ac6b41c629685065ea62cf468200035e3917c889a8f7921f0a6d6f3288c4`  
		Last Modified: Thu, 26 Feb 2026 19:22:30 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef786b18402ac1f0b8db86e3c820affd2d46e50f8a2fe67265e052d742b28f0`  
		Last Modified: Thu, 26 Feb 2026 19:22:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:b719134a82867ced67dedecb7ec703c542e71a5d2fed04af390085b39af6a218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a968fe9e10371971dcd41306d970cf17d72b3b02e89be02179ff7e5c566cb6`

```dockerfile
```

-	Layers:
	-	`sha256:f32c3e47bfccf0f5a863edea3c2b7d85d0e01d5ddc6421460350a982c86a3528`  
		Last Modified: Thu, 26 Feb 2026 19:22:27 GMT  
		Size: 6.0 MB (5963124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4768def19ebf7c0946d57c4dad6bf6d174aa162adb40a389ff835564644171`  
		Last Modified: Thu, 26 Feb 2026 19:22:27 GMT  
		Size: 52.7 KB (52736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; 386

```console
$ docker pull postgres@sha256:90ce227aa23b8179494c4956c4d18f22eed50b0d7433e2c0399a2d61cd106a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97567914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa68e9996a9945694fd78f693cb2d38a8cd980b34a0afa60716e9d16105bf057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 19:16:09 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 26 Feb 2026 19:16:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:16:23 GMT
ENV GOSU_VERSION=1.19
# Thu, 26 Feb 2026 19:16:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 26 Feb 2026 19:16:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 26 Feb 2026 19:16:28 GMT
ENV LANG=en_US.utf8
# Thu, 26 Feb 2026 19:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:16:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 26 Feb 2026 19:16:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 26 Feb 2026 19:16:32 GMT
ENV PG_MAJOR=18
# Thu, 26 Feb 2026 19:16:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 26 Feb 2026 19:16:32 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Thu, 26 Feb 2026 19:25:18 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:25:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:25:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:25:18 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:25:18 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:25:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:25:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:25:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:25:18 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:25:18 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:25:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327715e3782cf7088e90a38150e1fc99ca0391644c1e1b70908b5f5e28cefabd`  
		Last Modified: Thu, 26 Feb 2026 19:25:30 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2ca6bf506d8c605c6a40386920a1241bcf947f8e17e7621da923d5bec09d4c`  
		Last Modified: Thu, 26 Feb 2026 19:25:31 GMT  
		Size: 6.6 MB (6631421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15944e67d8885cba2eb08ca21a2b831d5dbc5ddcad804fa0985633f284bc672`  
		Last Modified: Thu, 26 Feb 2026 19:25:31 GMT  
		Size: 1.2 MB (1225834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71acc85d172f9ebc91145a03c0bc2889f03c976d64598f2f397825285be51ae9`  
		Last Modified: Thu, 26 Feb 2026 19:25:31 GMT  
		Size: 8.2 MB (8204011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577e16a287c9055e183a6ac4843b6824c31633312852b92b78d5fe141cc0260b`  
		Last Modified: Thu, 26 Feb 2026 19:25:32 GMT  
		Size: 1.3 MB (1308261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df935d681190c6793e38fc37de8c84dc1dc6b2af5ab073fdf4077cd914a91efa`  
		Last Modified: Thu, 26 Feb 2026 19:19:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c32a6b65bb9a805421344e7bd6b78ca5ee73127c7d7d2c4c6f29e04cd22b61d`  
		Last Modified: Thu, 26 Feb 2026 19:25:32 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56eab8bc412039a35e603ac37c3daf5efbb53ee76f13f16ffce85cda3282def3`  
		Last Modified: Thu, 26 Feb 2026 19:25:33 GMT  
		Size: 48.9 MB (48874559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80351f004f1b4504e2fcba34ec9a242634a173a9ded6f53e86e87390c7a7d755`  
		Last Modified: Thu, 26 Feb 2026 19:25:32 GMT  
		Size: 19.3 KB (19328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec1a9f5d96bc66cdc0b9212c3387b5a275e18615b2f972231e93dec58e9d825`  
		Last Modified: Thu, 26 Feb 2026 19:25:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d437074f6670877d495a0b92feaf266c922870b17c922a8a54d64e1641c837d4`  
		Last Modified: Thu, 26 Feb 2026 19:25:33 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ea10e609b905bff8a355850a5c6e3ead7324660ccd11f608c6cac18f1dc172`  
		Last Modified: Thu, 26 Feb 2026 19:25:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:03708ea2a11d3f6e1928b5ec4380d8ad8a9fd01c3a8e0680db93529240d32459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7151bc59487ab7a526a55401396111b1e8b831f923fd84797b99b96bb3bda7ea`

```dockerfile
```

-	Layers:
	-	`sha256:2bfd14c4df58c95cae84cb7b8b6c79ab6d6b8206bedea3a990a39fb10d95596a`  
		Last Modified: Thu, 26 Feb 2026 19:25:31 GMT  
		Size: 5.1 MB (5115227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:720f3788fc1d3bbda5bc4c64f84a75ae7cc1d7c928496a3b251f3ba0b355a2d7`  
		Last Modified: Thu, 26 Feb 2026 19:25:30 GMT  
		Size: 52.4 KB (52391 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:28571fb4cc9a11f5dbc9256a1faa2eb19758a124896c39ad602ea81eace809c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174715345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbc60b42f11649aab97e2525d823f7909af7b359b03ea34e59b6505a1032aeb`
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
ENV PG_MAJOR=18
# Tue, 24 Feb 2026 20:56:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 24 Feb 2026 20:56:59 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Thu, 26 Feb 2026 19:15:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:15:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:15:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:15:14 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:15:14 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:15:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:15:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:15:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:15:15 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:15:15 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:15:15 GMT
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
	-	`sha256:9259b9858de8f76126ff1c37b8a94f4ddd9584c0c74c9dae1e7912c47469ec87`  
		Last Modified: Thu, 26 Feb 2026 19:15:59 GMT  
		Size: 123.2 MB (123194986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80a3fb6ee242b8c438e25d816568771d91d47fb5e2ffdc3093cf6fd50460140`  
		Last Modified: Thu, 26 Feb 2026 19:15:56 GMT  
		Size: 19.3 KB (19326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62652c502ac4194636e7762d29187cd13dfcb707c6dd34c6103e4926829c905b`  
		Last Modified: Thu, 26 Feb 2026 19:15:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74821b70456ccffbd91e1950c60fb42376f480f77ce95d2f1956093a843f4bb`  
		Last Modified: Thu, 26 Feb 2026 19:15:56 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7262979db00ddb9c7abe16963d4c52a37da33d2cffacc911d0e969e811bf5367`  
		Last Modified: Thu, 26 Feb 2026 19:15:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:7f649ee919e651b2eca5134f82f8cb55450f369aa23f567bb90319a54585ecac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac9adc09cfc2e87eccaa27ebd047b58a060f83e9d194a6c276b3155e2af489b`

```dockerfile
```

-	Layers:
	-	`sha256:b549cf1052a15b9d76b277a4f90e3b9fbd97b9c15d75f1d225bf6a8b5b427cea`  
		Last Modified: Thu, 26 Feb 2026 19:15:56 GMT  
		Size: 6.0 MB (5963399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2189a5b43ecf28a0d58acbdcebcdfd84ba798a633930f599f42441a721e0f5a2`  
		Last Modified: Thu, 26 Feb 2026 19:15:56 GMT  
		Size: 52.5 KB (52534 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:f7097a68136a115e69ef9a6f4938fbf83015f50e8fed7badc8f8223eecc40fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92858902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e88ae771639b5130a5591ef849523a371c55f24adff3de567fd2d2344cea31`
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
ENV PG_MAJOR=18
# Thu, 26 Feb 2026 10:37:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 26 Feb 2026 10:37:30 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Sat, 28 Feb 2026 01:47:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 28 Feb 2026 01:47:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 28 Feb 2026 01:47:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 28 Feb 2026 01:47:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Sat, 28 Feb 2026 01:47:06 GMT
VOLUME [/var/lib/postgresql]
# Sat, 28 Feb 2026 01:47:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 28 Feb 2026 01:47:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 28 Feb 2026 01:47:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Feb 2026 01:47:07 GMT
STOPSIGNAL SIGINT
# Sat, 28 Feb 2026 01:47:07 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 28 Feb 2026 01:47:07 GMT
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
	-	`sha256:576272972e3118dd850b896ad0caa751bc4b846be07c41a4c4d434bc484c9555`  
		Last Modified: Sat, 28 Feb 2026 01:49:42 GMT  
		Size: 47.5 MB (47451144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e264187af5b7c89ed2174347e0d3c052b881164b74f80f6791de2bcb2ccf793a`  
		Last Modified: Sat, 28 Feb 2026 01:49:34 GMT  
		Size: 19.3 KB (19338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff752524325f9858fec16a533e6404ab4db655f1664b8d096c10f3513c38dd20`  
		Last Modified: Sat, 28 Feb 2026 01:49:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeafee2cf7c96751ee5685a1cc5ab33a37d6d8f8c7e5949dd71dec0c8047a41b`  
		Last Modified: Sat, 28 Feb 2026 01:49:34 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26f8244477c2698a0bbd56b3bc021643e0fed3f0acf7511271470cbda2b0060`  
		Last Modified: Sat, 28 Feb 2026 01:49:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:fc284eacfba8a538b0d51e72dcf0e4a68958a72a86e83eb7d1d87b8c59ae6785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5162696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5370435fa29e8a71cdd75b544ec3870ddc353ca1a9a4177ae3b0324e20d8e275`

```dockerfile
```

-	Layers:
	-	`sha256:479243be1e31c0192709e50a840a6d6b0b0429b15439ca5bae9a1571ccaee87d`  
		Last Modified: Sat, 28 Feb 2026 01:49:35 GMT  
		Size: 5.1 MB (5110167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859fcebe2fa552dabbe11ef6b255b15221dfa42f0044f2fdbff20904f76b6dd4`  
		Last Modified: Sat, 28 Feb 2026 01:49:34 GMT  
		Size: 52.5 KB (52529 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; s390x

```console
$ docker pull postgres@sha256:6e1146f77f82cade47580167534d74423ea622d0789cebf702af80f2295f8466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176920998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636aff8b8526f6a1a3c23a22eda41837ec9e2ebb0da308735f6bde19e311687b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:58:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 24 Feb 2026 19:58:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:58:53 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 19:58:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:59:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 24 Feb 2026 19:59:06 GMT
ENV LANG=en_US.utf8
# Tue, 24 Feb 2026 19:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:59:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Feb 2026 19:59:19 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:59:19 GMT
ENV PG_MAJOR=18
# Tue, 24 Feb 2026 19:59:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 24 Feb 2026 19:59:19 GMT
ENV PG_VERSION=18.3-1.pgdg13+1
# Thu, 26 Feb 2026 19:33:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:33:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:33:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:33:23 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:33:23 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:33:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:33:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:33:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:33:24 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:33:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:33:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f89cb3e91c6f05a2aaaec1568bccf0111eb27a1ab74893e027443b68753fe02`  
		Last Modified: Tue, 24 Feb 2026 20:19:13 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a9edf2863b6ea34c01e1f1748cf97e7dd281137dc61ce0756f574075eb20a1`  
		Last Modified: Tue, 24 Feb 2026 20:19:14 GMT  
		Size: 6.4 MB (6408036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e46165db683fe547fefab107b048a75989012f8e59a7e07b3214f6859cda85`  
		Last Modified: Tue, 24 Feb 2026 20:19:13 GMT  
		Size: 1.2 MB (1230336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401960834c8d0f2124e6e9395cd51a41bd7b63a2824b2be6c2dc4ad40d62cec7`  
		Last Modified: Tue, 24 Feb 2026 20:19:14 GMT  
		Size: 8.3 MB (8259108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c1d91545d3cc0591e3d9a14913c132eb264fa903c87d6963052003e35af278`  
		Last Modified: Tue, 24 Feb 2026 20:19:15 GMT  
		Size: 1.4 MB (1398378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e346cb27898b2f1789b656b7135febb4bccaa5fd88dde8b888dad79f0e19e8`  
		Last Modified: Tue, 24 Feb 2026 20:19:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81644e2aa8f1737ea7e351dbd53555d39387732f1a73ed50e6be42548ef0fc01`  
		Last Modified: Tue, 24 Feb 2026 20:19:15 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fcad21216abb35e1278acfc0e6527560b9f0b69433bbc71377f612675119ad`  
		Last Modified: Thu, 26 Feb 2026 19:34:24 GMT  
		Size: 129.8 MB (129757044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65828131baf9187be1665f26d402c84e5c82f3ca3e8f76f5f5c7bc68b6e5d873`  
		Last Modified: Thu, 26 Feb 2026 19:34:18 GMT  
		Size: 19.3 KB (19336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83394c079c53c5356fcc6bf0822e600ed47b8b7373d53ac5173e9088bebb1e21`  
		Last Modified: Thu, 26 Feb 2026 19:34:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290adc71aaf9455b02450ae2b29f8c5fde7e4311ca994d0c4f28a1dab6387f6d`  
		Last Modified: Thu, 26 Feb 2026 19:34:17 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d12cce3ccfef70b536a8ec0f0943914c29d9c5a9dc17b4ba770e122750edc3f`  
		Last Modified: Thu, 26 Feb 2026 19:34:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:2dea6cc8724ea5b01ab98bcefea9f047c6eaf77819295317a7ce3b0c8f231259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd8bdae7fd2cb2f5128561aae431a4f8536cdc6236f550de6c9b967dfca2e0f`

```dockerfile
```

-	Layers:
	-	`sha256:92471f38b2088c65c68ed622429bb94dc38828fc1610ddc7406bb8fb2a5117c3`  
		Last Modified: Thu, 26 Feb 2026 19:34:18 GMT  
		Size: 6.0 MB (5973421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4590e0dba687d4e9ca24c9c167e5311ad2de3925e4b6a8711d3fd50882dc080a`  
		Last Modified: Thu, 26 Feb 2026 19:34:17 GMT  
		Size: 52.5 KB (52457 bytes)  
		MIME: application/vnd.in-toto+json
