## `postgres:bookworm`

```console
$ docker pull postgres@sha256:864831322bf2520e7d03d899b01b542de6de9ece6fe29c89f19dc5e1d5568ccf
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:843c69368d9b15045d023e68a16afbd0ef6c7285a7029b1403f203fd579ba63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156294527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e86ce23c73bf3bd2b6b6e3d183f24adbc53a137f98b37484601d359e267555f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=17
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074b41e8190fafd9cf3206bc2085756abfc96efae7a3214da5e76d154e021a77`  
		Last Modified: Thu, 08 May 2025 19:14:07 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb26461722d700cfe05d1aef1c9f249f563420cfc91081821cad5b3ad26997bf`  
		Last Modified: Thu, 08 May 2025 19:14:07 GMT  
		Size: 4.5 MB (4533736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddf304e15c06524ab980ae9c38cbd04813124943e30d9f095c49227518681b0`  
		Last Modified: Thu, 08 May 2025 19:14:07 GMT  
		Size: 1.4 MB (1446746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693761670bfc8b5648d2984322f7ad974d55f1d4dbb1c7260fb8b0b5f3650fac`  
		Last Modified: Thu, 08 May 2025 19:14:07 GMT  
		Size: 8.1 MB (8066258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0c607b24959bd55262db4dd31e1fac2e55de5e11c0fd0d2a6e33e2b415d8e5`  
		Last Modified: Thu, 08 May 2025 19:14:08 GMT  
		Size: 1.2 MB (1196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f438059a5a57792f67fdd7544474c66d9858ae6dd473d953415914d9e19dd42d`  
		Last Modified: Thu, 08 May 2025 19:14:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d10e07b30c3db1c48fff1be0c67936b417f32282db2cfa2a384322b11b9866`  
		Last Modified: Thu, 08 May 2025 19:14:08 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877e6448d55bcba824f595ff1d848f9f325ea5d6d39256084249bfc5484611a5`  
		Last Modified: Thu, 08 May 2025 19:14:10 GMT  
		Size: 112.8 MB (112803415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023e132da3ed16913a31022d85cdb97ed0a82c660cd501c75853ac08a7729e1`  
		Last Modified: Thu, 08 May 2025 19:14:09 GMT  
		Size: 10.2 KB (10231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee9d93212496e7d4646660386865510b483a4f4b4424c008fb6d50a9434dd76`  
		Last Modified: Thu, 08 May 2025 19:14:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a308d0de7d3850acdeea0655fb527feca1dbbe6d71b294cecd259516d42b4bca`  
		Last Modified: Thu, 08 May 2025 19:14:09 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ebd47166d0c4a0d16962b98e4b58882817c81a6f958d94536bfd914f85ec6`  
		Last Modified: Thu, 08 May 2025 19:14:09 GMT  
		Size: 5.5 KB (5471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca3b919b7ab2c4a8aeb7ba5de9ebef4eda222ef8ca0ad39b3568186d82e0bb0`  
		Last Modified: Thu, 08 May 2025 19:14:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d095575dada158471e14ef03336f5ee6bd4f56db4e711003b461239c400457e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5873321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4971325e2a79ad7a9ede1dc78d5ccabae41a038ddea22f04f1ab04f47208898b`

```dockerfile
```

-	Layers:
	-	`sha256:9be6b2dedfda486656b722f3de2b9b779334dd301aba508c67a0612addf8c578`  
		Last Modified: Thu, 08 May 2025 19:14:07 GMT  
		Size: 5.8 MB (5818654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d56466bf13663a5cead377d3c4284ba09c75633260e2c99e33231e4b4395f41`  
		Last Modified: Thu, 08 May 2025 19:14:07 GMT  
		Size: 54.7 KB (54667 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:1c9041fafcbccb59d30d94c08380bc839a804e7d668d144285830145b14729bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149377422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd76c528139dbcfc7aadfd6d3f5ea17f1b545f80b5e86fe4658528f1227ad2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=17
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3bc532ff9d2a2a12c6cfc746359843257a240960865aea7ecb10c71e0b93ec78`  
		Last Modified: Mon, 28 Apr 2025 21:07:56 GMT  
		Size: 25.8 MB (25757836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dbd13a5b1ee87638e8ff020b1d2afd3a00a7bc146f2dd322eff851e885678`  
		Last Modified: Tue, 29 Apr 2025 00:11:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddeed145392a589296f4def151c0cba38caa5ada19685adbdb91ba2a6a6b03f`  
		Last Modified: Tue, 29 Apr 2025 00:11:04 GMT  
		Size: 4.2 MB (4151014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df15ff5474dea0b8a303fcd9ca6d5caf5f5ade1fd5c898351501897de7d9f2`  
		Last Modified: Tue, 29 Apr 2025 00:11:04 GMT  
		Size: 1.4 MB (1423985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12dab1affb15219c1bbe269f8dba51a0b04a4393f6cc5b4ddc6b2dbd7e731e3`  
		Last Modified: Tue, 29 Apr 2025 00:11:05 GMT  
		Size: 8.1 MB (8066459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d53a8d7d21b72bc0336ce7f91d99cb2e76a3f5bb8e50f04848caeffcf3871d`  
		Last Modified: Tue, 29 Apr 2025 00:11:05 GMT  
		Size: 1.2 MB (1194889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550a864e050e101f225d9a0cc2bb1b9064f50226333ad9e131522c36a3921ac4`  
		Last Modified: Tue, 29 Apr 2025 00:11:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862b669ee28183d02dee57a101cd1a31845cfd26fe615ab0a0b969ce916dfc59`  
		Last Modified: Tue, 29 Apr 2025 00:11:06 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d8c8a79c7db69d267c98145ec3a97f3a130cc93b11ef7355cf4fab904d0a2c`  
		Last Modified: Thu, 08 May 2025 19:31:48 GMT  
		Size: 108.8 MB (108762629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587662f5661841a431427a8f37775ea8e1c1d549bc85cd16862b6a5405251e50`  
		Last Modified: Thu, 08 May 2025 19:31:45 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba49c69bc7975a8b0c09f4bc07fd887e640211b3c47f8367a5f45cc51d39e1b`  
		Last Modified: Thu, 08 May 2025 19:31:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b89d2202e9c0e335d4d019108bf492a2351216b2ca7bcfe5f294f3de93ea1ba`  
		Last Modified: Thu, 08 May 2025 19:31:45 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daad60ead96fc004efac725be7a22ae86e70c23cb7ccca7def266bba225de458`  
		Last Modified: Thu, 08 May 2025 19:31:46 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d148dd36beb012da2228ca9014aa64a7c2c44d5b4190c22a3f89a0417708df9e`  
		Last Modified: Thu, 08 May 2025 19:31:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:58dc505fd08d8ac8759131d39a751fc57781fc9788e7cd89b671de812eb81e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c984025ab628ec18fdf652fd63cedf425481f5412100f768aca3694053874e`

```dockerfile
```

-	Layers:
	-	`sha256:d60ef9a8aa00d72cdcb0ef6ff7c0c6183a43bc4118334bdc91abf7cc039bfab8`  
		Last Modified: Thu, 08 May 2025 19:31:45 GMT  
		Size: 5.8 MB (5836327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7fb5ba838bdbd808755f15a8ab46022b95bf7a57125cb067249a77ce91eccee`  
		Last Modified: Thu, 08 May 2025 19:31:44 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:57732f4ecd5636f7b36244355e87534c2c5b84bdcfc52bfc365d7494dd8589c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144346945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b069dd468a0fae9c6f5b63d9487f4c51b2632b5c56abfe7f7f7e3cd8329c616`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=17
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdb4fadcfae6c7f639bb005beb451a5d1442c02240a0d69d7265e913295df68`  
		Last Modified: Tue, 29 Apr 2025 01:02:43 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2efccad23750e2931d3ed57d24f2835f3b9ce8744beaa721d9437163c0cf9c`  
		Last Modified: Tue, 29 Apr 2025 01:02:44 GMT  
		Size: 3.7 MB (3742519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f553df79e41f2f793d4828509d5e5323042ad46cd5cd5b31d6d14f8607643`  
		Last Modified: Tue, 29 Apr 2025 01:02:43 GMT  
		Size: 1.4 MB (1413684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad2964e1fa8d5744b87a0ed825b61807320e0a04d4889bb205fa941886b2e0f`  
		Last Modified: Tue, 29 Apr 2025 01:02:44 GMT  
		Size: 8.1 MB (8066255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f726aa2fe47cabbb56851a90a83ab6a9c48b967d6f4ea88827119d6b3120afb5`  
		Last Modified: Tue, 29 Apr 2025 01:02:44 GMT  
		Size: 1.1 MB (1066999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1938ce7122ffddb675c2743693e8ab090236dc16305e5d6d3c52d4d237fc06`  
		Last Modified: Tue, 29 Apr 2025 01:02:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f217542552436de76d587eaa73b78a8a5618772cbc566ca7272527155b615c2`  
		Last Modified: Tue, 29 Apr 2025 01:02:45 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f0128ee310ec9f2a23526c1f7d800cce7dc5737b229ff300a6110aadd13315`  
		Last Modified: Thu, 08 May 2025 19:31:20 GMT  
		Size: 106.1 MB (106098795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c3510929f8f324cf86abd71433d35716dfa49b4e742eb2f392e42a19a793bc`  
		Last Modified: Thu, 08 May 2025 19:31:16 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0d52031df1f6d3abddd6cc4bf3211f2747bc9ff29a6bf3e6393c56a370a575`  
		Last Modified: Thu, 08 May 2025 19:31:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f349256ec94a4752d9994c930377577c2b0dca2df9657c07fc7f3ef2500a420`  
		Last Modified: Thu, 08 May 2025 19:31:16 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edebd86276d4beac3fc494982552fb2f2b3ebfd190fdb5c6c569c0dc8fa837d`  
		Last Modified: Thu, 08 May 2025 19:31:17 GMT  
		Size: 5.5 KB (5471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e243fb38607650b2ad3cbcd6f966d66b28f27999f6c5e8ef7dd8ecea0b3f406`  
		Last Modified: Thu, 08 May 2025 19:31:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:74f7a17bae1ed7ecac96978d1e9d68c40e1059c2b93e6d0f211203cf6d253557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5890800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5224e461fbae9af0700887c3b660f1d62caa7ad5290eca88eff92165b6bc295f`

```dockerfile
```

-	Layers:
	-	`sha256:24dd117addbffd2a16e3473ebae081a7ac6cf0a8bc3a2292595b568daf90d33b`  
		Last Modified: Thu, 08 May 2025 19:31:16 GMT  
		Size: 5.8 MB (5835898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a527aadec78b8e32017bb2f71253b1d46a153adff086846761dafb7cf7505eca`  
		Last Modified: Thu, 08 May 2025 19:31:16 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:0f29d940c2dba2a986362110336edf18517439c256bf1485da28389703dc9440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154146386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b29e82c211e7e20e2c5e5b88bf067619faf08314ccf0d41e6b590d8b3643b88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=17
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec5ceba4f23a571d445a6abc3816fb69a267f6b136fd28092becedee333f635`  
		Last Modified: Thu, 08 May 2025 19:17:24 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057f898184a196899fd5f5b17649957a9e065f8b79892675dedc0d89cd117f11`  
		Last Modified: Thu, 08 May 2025 19:17:25 GMT  
		Size: 4.5 MB (4499181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b955a72f820f4b7a37fe7fb9c6eaeb4ffd9265b8d03922953c3f184502d5ba1b`  
		Last Modified: Thu, 08 May 2025 19:17:25 GMT  
		Size: 1.4 MB (1378755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57660abecc5ce8c29559c3f423b0ad43d3f5b9c6491ef0b571d8b9bce64b3f8c`  
		Last Modified: Thu, 08 May 2025 19:17:26 GMT  
		Size: 8.1 MB (8066315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbfde47bdf50203e707c259fac51a213255093c68e66e17f9f8ea236e31498b`  
		Last Modified: Thu, 08 May 2025 19:17:26 GMT  
		Size: 1.1 MB (1108710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10737efea89a1fe5cc34a0c5bcf378ba3688883b78a471c4d64353f2158d0a4`  
		Last Modified: Thu, 08 May 2025 19:17:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb243f355f93caadba4736280bf2755ab7e7cdd0fbf8fbb4b728a306d0a9a5e2`  
		Last Modified: Thu, 08 May 2025 19:17:26 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0567d9642f4a6dd9fc54c550a67898b83c4dc8e6eb405ffe6c4f442f219609d`  
		Last Modified: Thu, 08 May 2025 19:17:30 GMT  
		Size: 111.0 MB (111006189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853996664957797c7ac3c68edd137098d5bf78fca6fe2b73b5a8317b588f6661`  
		Last Modified: Thu, 08 May 2025 19:17:27 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34b942da5d4b52f136d46808dd0a384b711032dd550ddd34bb221f423e4a71`  
		Last Modified: Thu, 08 May 2025 19:17:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955b88e7e96af1185658445e1bdb83bec9001ae447bfc066db7680e7e02d7cbb`  
		Last Modified: Thu, 08 May 2025 19:17:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba3f58f8af8a3131e2c70964dc67a84d25560b0f526afe1fc1f1b84cfe3f21c`  
		Last Modified: Thu, 08 May 2025 19:17:28 GMT  
		Size: 5.5 KB (5471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f7af1ca0387def1535358facd877bf4ea244453e1ff453ff700193926c2863`  
		Last Modified: Thu, 08 May 2025 19:17:28 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:96b65a26cfc69a4582b179dcf386fff0bcbfc078740b6b22a1ca19ad7b3e7967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5879977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b896927c91637e2db8a46dd474b2d481642f0e6ed5705e30321404c7601990a`

```dockerfile
```

-	Layers:
	-	`sha256:5b34a77696f77c57048ad6a7abc817d4f929a771d2bb222ee9c23485c59417f5`  
		Last Modified: Thu, 08 May 2025 19:17:25 GMT  
		Size: 5.8 MB (5825017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2518a70b6f9751b93c213dc90a38f71c32efe79fbc1cdcf5f0f67b356257f72f`  
		Last Modified: Thu, 08 May 2025 19:17:24 GMT  
		Size: 55.0 KB (54960 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; 386

```console
$ docker pull postgres@sha256:eeb22524f0cc61ad88dcea43049ddb5683d94047594d71c362ff2c340019a4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165212867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bec36957d11370f53ff78fe76c3b562a1a93a612206081ef5cc87cc866706e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=17
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6386601d5dbe1558264483349d0d22f81192242adddc21f05a193594c00f219`  
		Last Modified: Thu, 08 May 2025 19:27:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94b12b661322e758969c7c2c2d74951795c64104aa8a609e98fc92481db88f7`  
		Last Modified: Thu, 08 May 2025 19:27:24 GMT  
		Size: 5.0 MB (4965092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce00077a0a43d51e9f6b8f3834f9a930c5f1e57229e507b3f0cc86334792f9f`  
		Last Modified: Thu, 08 May 2025 19:27:24 GMT  
		Size: 1.4 MB (1422234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc43b68bf39c13615ae413ccbaccc4401c84d840f5c817d5b7c82ffc0d92b95a`  
		Last Modified: Thu, 08 May 2025 19:27:24 GMT  
		Size: 8.1 MB (8066322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aecb1acabca73195a222bcdf767f944b54559d1c0a8eb098a9badcdc0993397`  
		Last Modified: Thu, 08 May 2025 19:27:25 GMT  
		Size: 1.1 MB (1137205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64b304ac1b6f0c6a69f9807d9331b48b8256bf24bf726547250705c21abb08a`  
		Last Modified: Thu, 08 May 2025 19:18:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbee662cbf3b20466ced6fb061444c955680bd84b8e13a2579d62776e9d18ee`  
		Last Modified: Thu, 08 May 2025 19:27:25 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ac3441ace501bd2544a9f744dc5217d931c6d1ee983943619bd08ca635bcb6`  
		Last Modified: Thu, 08 May 2025 19:27:28 GMT  
		Size: 120.4 MB (120390525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604433dae808bd921ba6925b5b54dea88ab3bb1839baad90ca913a1dec29abf0`  
		Last Modified: Thu, 08 May 2025 19:27:25 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c219c197f2646f0d04b81adae2fc0bd4c9f30b24ebe84c2e101050ca8a9b6a`  
		Last Modified: Thu, 08 May 2025 19:27:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b112a088eb85ab277f4632bd4e81f28de73721ee0fd821212e2320b1299538d`  
		Last Modified: Thu, 08 May 2025 19:27:26 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7488b8c652d4ba44ab1081b61797bf11f2629626bb0974988235180373e012`  
		Last Modified: Thu, 08 May 2025 19:27:26 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3071de4db07db1f2a3a81a145c20d60ff29d5eee7a5df2901fbbd4c5d95775d3`  
		Last Modified: Thu, 08 May 2025 19:27:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:53c45727b188989ad7f8ae417372a9fe6a156a981956724e1165c180481412da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2978bfe06902b5049f49de39f9060563d3188d729e5e3ffa7724d68cabe006e`

```dockerfile
```

-	Layers:
	-	`sha256:5be78ae3f072699e2f2785d28c72a6f55f6499e8f35032c3f0b67494d131367a`  
		Last Modified: Thu, 08 May 2025 19:27:24 GMT  
		Size: 5.8 MB (5834339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03324c9583fb9051ec18d8eee526c7d7cb40610e30ed826987b665f6f953fbb0`  
		Last Modified: Thu, 08 May 2025 19:27:24 GMT  
		Size: 54.6 KB (54603 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:002684a50abd6575073cda21e9c9916b4963799758c75b2591ca9fe2915b85b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155163098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd179f46c02618cf17d9019c76aa17ad424b1d6b8879969f8a8c85a5b0d8d2a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=17
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:901060d913f9d0bbb82847b3b60c3a263ed0dac4f75aa29161be6ed89b57082a`  
		Last Modified: Mon, 28 Apr 2025 21:11:19 GMT  
		Size: 28.5 MB (28514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1780050ae792096e0edff3e578099a41e20ce2a23d7434a31a78a13d2b3f501`  
		Last Modified: Tue, 29 Apr 2025 07:45:04 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32022b8dd15ee12863120304ba80701697a0232a841395c6c8d557a11d14223c`  
		Last Modified: Tue, 29 Apr 2025 07:45:05 GMT  
		Size: 4.5 MB (4475158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd295a92609a051f01f5fbadc21ae67c51b1a7e1c423aa13548bb0c3468c722`  
		Last Modified: Tue, 29 Apr 2025 07:45:04 GMT  
		Size: 1.3 MB (1333883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49953f908cacf70551b7bf4187ae9e8b441d92da15103e34ff0b6273a4aaf3ad`  
		Last Modified: Tue, 29 Apr 2025 07:45:05 GMT  
		Size: 8.1 MB (8066514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dad47142b6c9f9cc6e05f01b141c6d270db331bbd00cd1fbd60ae6448fb7cd`  
		Last Modified: Tue, 29 Apr 2025 07:45:05 GMT  
		Size: 1.2 MB (1182704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c74555c4f1f057ae22d7b6c625eda50a7ac21f4a81590748a81cdbb475cfa6`  
		Last Modified: Tue, 29 Apr 2025 07:45:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711e5b1cdae35c1754e7e9e2a5b0567db79bc132e5d66531c8c6c170f8025a1c`  
		Last Modified: Tue, 29 Apr 2025 07:45:06 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719953a60d949f7345f4d1b1c5af27870e8616201367f3c684c11cb89528e91e`  
		Last Modified: Thu, 08 May 2025 20:26:04 GMT  
		Size: 111.6 MB (111570075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff868eb783dc4ef67a610f773c16eae1afdd574f926cb00ffcf3dc77b97a579`  
		Last Modified: Thu, 08 May 2025 20:25:54 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa434164dfc95c793c59fa060fbcf49050a9c0295c465479cb32fe59d679b935`  
		Last Modified: Thu, 08 May 2025 20:25:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967764d79b6a2a4978566ba48a7a7fc27a1d33184435d1cc88bfbc98ccd44bb1`  
		Last Modified: Thu, 08 May 2025 20:25:54 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151900057712afa32b04b8e4946ba58d2aade1ff96ace4a8906259ab762e716e`  
		Last Modified: Thu, 08 May 2025 20:25:55 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02403daba333b03a849fdbee37351f5a05133f1e2fa796090562b9d8c539c6e`  
		Last Modified: Thu, 08 May 2025 20:25:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4d84869526ff42f5d75e4b09889c4e5f8b6e96d91673d4601567f2b3278dd5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 KB (54569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a201b3f59989bcf07b88f37d19b5911ce4bfdd7e458b81ebd2b882dadaa3bac`

```dockerfile
```

-	Layers:
	-	`sha256:dc6b8a3077f00ca08f620ada16ca7bc4437c7910b2055b3cd879b47a57000068`  
		Last Modified: Thu, 08 May 2025 20:25:54 GMT  
		Size: 54.6 KB (54569 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:97eb37128b98b4540622f007389b98cb803ccec513ffbaa74ea77dacf14f4524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169070981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8696ef68def8601594430852de596298a82de52c8e8b8f2959ab793319aea633`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=17
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e15de81941f7c44df819c05a92dc3ec9aabc58baa62bded8abe1faf2916460`  
		Last Modified: Thu, 08 May 2025 19:22:56 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831c9b47c6852f124cf8c14a2f8a90536781879bb40f7108d6be378c04439c52`  
		Last Modified: Thu, 08 May 2025 19:22:57 GMT  
		Size: 5.4 MB (5368200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb6f6a9ebbed3ee6875f5af99d1f6bc1fdeee373801d13c7a50d415bd1f1a48`  
		Last Modified: Thu, 08 May 2025 19:22:56 GMT  
		Size: 1.4 MB (1368742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306e8eca4ddb2df576851f376c80ce1ce94b75b89f6fd608124bb306776e69a5`  
		Last Modified: Thu, 08 May 2025 19:22:57 GMT  
		Size: 8.1 MB (8066383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ca4cb2832001ccf883e85e97e2bcf83c3272a4d94cf409df3556ef8855e058`  
		Last Modified: Thu, 08 May 2025 19:22:58 GMT  
		Size: 1.3 MB (1283565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c373ad9662e17bdbdf2dc7adbe50b25562851f13f39b21f16cacf5cd98352de`  
		Last Modified: Thu, 08 May 2025 19:22:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c75d83d7375487e857f5bf7fd3a5a7bbc0eddf8e5e6d0b905edbc9edca336ef`  
		Last Modified: Thu, 08 May 2025 19:22:58 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e756146586ee09fab8a1fb822ebff3dae4d00d056cb1c8740f75e8955c78788b`  
		Last Modified: Thu, 08 May 2025 19:23:02 GMT  
		Size: 120.9 MB (120895027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d45c812e1eb0181dce61a65cd583c3ada6498cf2ec92f224be07c83081a1a98`  
		Last Modified: Thu, 08 May 2025 19:22:59 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986aab89543c5cbc941602dde0f3916f219c50e9fa20d8f527d7431b0d997bfb`  
		Last Modified: Thu, 08 May 2025 19:22:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08646329dc7038a96cac6ab5c07db01476f8fcaff78a3860a01cfb42d3fa31cf`  
		Last Modified: Thu, 08 May 2025 19:22:59 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdc28e7cc7c79b23fae0230278de5157edb62a9ce112e7d4351987ebe81a25d`  
		Last Modified: Thu, 08 May 2025 19:23:00 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd0ccd1874c8d8dc8291038f1e78689f7aac7973a6b92c1580481cb2c923495`  
		Last Modified: Thu, 08 May 2025 19:23:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d6d36a176e42a8f1ef1959730eb655aa3c2da8b347822481207a74de40241c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5880659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6841d911de15596141497f99065d1b4cd1768d85f0eaa4ac6fa5d45db8a3856`

```dockerfile
```

-	Layers:
	-	`sha256:d564b96fd5b98cddb216d1ff67531399d93abc7f58aff468fae41c58f7d593b3`  
		Last Modified: Thu, 08 May 2025 19:22:57 GMT  
		Size: 5.8 MB (5825915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d101032b0ddd63e32b1021e85e19204d5ebc83853824f2dee8f49b7864588cf4`  
		Last Modified: Thu, 08 May 2025 19:22:56 GMT  
		Size: 54.7 KB (54744 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:62f36e9287db2487dbd90af58d68285652a07119e9b395c0150d1a112d78e489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165585099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5eaa11394e556eaec7f70d38cfec022857d1974b85a7ba090ddbe0fafc6820`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=17
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c248ffe4f21880229522e5ad5c2703976299295d6d894d9490806c0a9a7cf45`  
		Last Modified: Thu, 08 May 2025 19:35:31 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d13e825e9d3e1c8a8132b839b8821c6e5285374a88d601e7a517f251d6c8340`  
		Last Modified: Thu, 08 May 2025 19:35:31 GMT  
		Size: 4.4 MB (4391042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc1e3a56b5833a71fd825838551fb859ecd3993d606c3b62f4d5192775fc04b`  
		Last Modified: Thu, 08 May 2025 19:35:31 GMT  
		Size: 1.4 MB (1412760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a09d1da4e34e97c0c0a8a2337068aff2abbbdac1aa0064fd21bf59b0cb6cb8b`  
		Last Modified: Thu, 08 May 2025 19:35:31 GMT  
		Size: 8.1 MB (8120466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87203bb8ab9f6fd5568bcbd8fc845cfcdca543aab24cb4997ddd11e94d6021c`  
		Last Modified: Thu, 08 May 2025 19:35:32 GMT  
		Size: 1.1 MB (1096776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99bd7b2c30d8fcbd66d1b84412c41c4f63f4aeb1feec906ab0664d8586ad987`  
		Last Modified: Thu, 08 May 2025 19:35:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a07b08d12e1952495315aa4a0d7d5b3aa116f8e46a58d4a7085fca855945183`  
		Last Modified: Thu, 08 May 2025 19:35:32 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7e2f4cf88afd94f9ae020ae7eb6ab557700f27f80b50075301c1826a54ace4`  
		Last Modified: Thu, 08 May 2025 19:35:35 GMT  
		Size: 123.7 MB (123658573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773efe854bf244862c72ed6a09c97a144ca1d0950cca427a4eb9fc4709459d42`  
		Last Modified: Thu, 08 May 2025 19:35:33 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b6616dbeaf21a3fd038fd4e326e4556f1d907da85261ee0d519e364f70fa79`  
		Last Modified: Thu, 08 May 2025 19:35:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88afdc3da8b7f649dda68ee2a2777bfba6587e6256ecb006b7e1a7bd94dd0296`  
		Last Modified: Thu, 08 May 2025 19:35:33 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa421adc133bbcc0731ee120147a020a888fe2b121f51cb27102807cc60e5b6`  
		Last Modified: Thu, 08 May 2025 19:35:34 GMT  
		Size: 5.5 KB (5470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327639aaa7da321b4a9635563d46d194b7b30e2af1f586ab551efd906e02d7cb`  
		Last Modified: Thu, 08 May 2025 19:35:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:17382ba7060063c34c85f278e44f39ed026425dd3b9c81ece205ca0c827d1837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510cdbc930b468218257e83455e366e094f6c931afd3ea0fc3f605b3cd531c1a`

```dockerfile
```

-	Layers:
	-	`sha256:5603a9e27da012d67bba92aa7806dd39bc353aedfbe17346a798fd4f04bfd6ae`  
		Last Modified: Thu, 08 May 2025 19:35:31 GMT  
		Size: 5.8 MB (5834106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baddcd839015866630f052e63c25e10a853d74fe79cd06ec60b88a79f9becea3`  
		Last Modified: Thu, 08 May 2025 19:35:31 GMT  
		Size: 54.7 KB (54665 bytes)  
		MIME: application/vnd.in-toto+json
