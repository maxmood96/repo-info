## `postgres:13-bullseye`

```console
$ docker pull postgres@sha256:0907b69d663e2ef6599991fed4a5790de984ec932b2c38f7a88fe8b0abb23ba4
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

### `postgres:13-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:9bc6fc979570a5fb26bf41fb99aac2fa12b327f0608c77898568dba6380f5a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140529699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a77ff4f21b0f589f99531bc2b572545d88d1aeeb4cb303a69907671680e454`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16-1.pgdg110+1
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b5af0c9e0da03f1b7d52510e23eda8230d71bd4aec7344b933b12ff6aa326e`  
		Last Modified: Thu, 05 Sep 2024 00:08:46 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6523834d9106b24d3c7785a3be71b6ef4565b615348c0d197daec6585ed3cb`  
		Last Modified: Thu, 05 Sep 2024 00:08:47 GMT  
		Size: 4.3 MB (4308193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2493d68e0acb83221dac4dbfa59319d944f01b1ddb5442f02e3144b641a54a56`  
		Last Modified: Thu, 05 Sep 2024 00:08:46 GMT  
		Size: 1.5 MB (1472219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a9e5cba4033ade4d0b9601313a1c243f0ecd7846bd36c2b0efd0749ff01f31`  
		Last Modified: Thu, 05 Sep 2024 00:08:47 GMT  
		Size: 8.0 MB (8044401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f28f3731ebb278e6ea933657091ad645ae839be49bbe390a9ce0d4c558f0b`  
		Last Modified: Thu, 05 Sep 2024 00:08:47 GMT  
		Size: 1.0 MB (1038356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b3eea1709addf289aeae925ebe02abf7d83624f7760cf95e29047d1c17c578`  
		Last Modified: Thu, 05 Sep 2024 00:08:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce6f658de00e7b7de608ec45dd4f3af8577db4553cb7194525784d601945699`  
		Last Modified: Thu, 05 Sep 2024 00:08:48 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb7905c2deababc749caa32d5959846ba1af3e389231148acf540a966314d8d`  
		Last Modified: Thu, 05 Sep 2024 00:08:50 GMT  
		Size: 94.2 MB (94217664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8507c9d653d542fd9ec1a1beb5331159ce0018d464dc2f65fdf6770df1cdf2`  
		Last Modified: Thu, 05 Sep 2024 00:08:48 GMT  
		Size: 9.4 KB (9356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b717404999d2d01ece6e7e3b251d020c026652932da020876b97c0aed05ccf`  
		Last Modified: Thu, 05 Sep 2024 00:08:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632476dd7885b467b4c67f9918d9c92d04669dc4cc242c54c0397a5c4b797fa9`  
		Last Modified: Thu, 05 Sep 2024 00:08:48 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55c97db8819a734ff961a131ccbf7db6373c7380a17f72839317ffc5fa1328f`  
		Last Modified: Thu, 05 Sep 2024 00:08:49 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12ed9a86f4d924b008f25e49a765208705baa16a541bb9ec814ee82ed7a36dd`  
		Last Modified: Thu, 05 Sep 2024 00:08:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:90968fec1d159caf2905660abc9db6c4c3481a87ef444ded471f8e21951b335d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5896470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7c1aa8559c09cc795c2f65418e1dc442dd24a87fb0d1101a398fe995d75e95`

```dockerfile
```

-	Layers:
	-	`sha256:ae7a1f4b22cee417a80a363058bc8f3eeb5c4991f1bb1855340c4bcf986c9764`  
		Last Modified: Thu, 05 Sep 2024 00:08:47 GMT  
		Size: 5.8 MB (5842240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f017e80ee526e2da5d4bf3f5862b6683ab7e16aaadfff1438233593f1e7337f4`  
		Last Modified: Thu, 05 Sep 2024 00:08:46 GMT  
		Size: 54.2 KB (54230 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:e6c94668bf4dbc3e6640f1e5ce400901e6bc952342069a60e8cc0c7b1d9f5edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133340924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44f92e09ed36703817fbcab5b9689ae32f09d6fcb487738094152f226d12ef3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD file:b6f3f19f4bd2bf78068380b3cd10d72519ced99a2b5abe830b4729df341dcfdf in / 
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16-1.pgdg110+1
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
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
	-	`sha256:193e13140162db326d59400800678bb96376c87c295bd3ec937c621c3fca30a3`  
		Last Modified: Thu, 05 Sep 2024 08:08:38 GMT  
		Size: 89.9 MB (89875746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727ab3fdc500e5edbdd7a82ade5d1ce7746938f7960cbd14e9719bba47ea0808`  
		Last Modified: Thu, 05 Sep 2024 08:08:35 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9329db3fb0d5b9ed211d54926f8c7964a2e3ff5af78aec348ee6b9a2617447`  
		Last Modified: Thu, 05 Sep 2024 08:08:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a853830de09f7fba006667d53590c91a7ed3c58ac924a5650abf3f028598ef85`  
		Last Modified: Thu, 05 Sep 2024 08:08:35 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25fab84b2511377bc1a25c84eaf1e37aa3ad0ad55c56fd97f55f5911d4f06ff`  
		Last Modified: Thu, 05 Sep 2024 08:08:36 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b8274b87cb214937453f1f29461aedaae4196bcd1cf2864981e681472e38a5`  
		Last Modified: Thu, 05 Sep 2024 08:08:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:493fa3453233f6aaec32736b5a87adc7028e992e8ab5fc9c77ebf0518e9b007f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5907454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ff59cd58caa3e6c3481d6142f3b6fea6643692cce384274d8d60e67c35e146`

```dockerfile
```

-	Layers:
	-	`sha256:989eb7aba9a7642cd5f9e298ea32c3b9b90c57f79f8c5c7f594d91dc1dc75415`  
		Last Modified: Thu, 05 Sep 2024 08:08:35 GMT  
		Size: 5.9 MB (5853027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946da8569d6b562f847804dcff452a03de25d5e32753cce00eab9d7dd2e302ab`  
		Last Modified: Thu, 05 Sep 2024 08:08:35 GMT  
		Size: 54.4 KB (54427 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:053f519f039b164f5c5ddec004d725fdff2462e998270f4f9ca4767833c92af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128511535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f94d66b237ff1e6c3164c340bea77f6df3218bfba8108b36f294a417f91f385`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD file:c451ece1244c14bce110ffbe6906867ce12f8e88234988b0edba91009a9dbbf8 in / 
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16-1.pgdg110+1
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
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
	-	`sha256:b75f5d1a5efe65d2eda01949698116c954a5d54f7361effe0c208ab1be25d711`  
		Last Modified: Thu, 05 Sep 2024 09:08:15 GMT  
		Size: 87.9 MB (87907923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1438035eb3273936c1b9d0806014f627a118a5723e8637d5df72d3df444af18`  
		Last Modified: Thu, 05 Sep 2024 09:08:10 GMT  
		Size: 9.4 KB (9356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5790ca46fb6b4969d3ad4a5a97a1c277793a4a98a03d37d28f459b460d55772b`  
		Last Modified: Thu, 05 Sep 2024 09:08:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee1658d0d4aaae5c202fe0f56974667c378c8c289dfd34d57b19063abfcf7a2`  
		Last Modified: Thu, 05 Sep 2024 09:08:10 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0b9a7d909a8ed9cde13e6094cd16392c46bb16c1460426efeff909137f442c`  
		Last Modified: Thu, 05 Sep 2024 09:08:11 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38d3db9fd9c184c3f91def615ac54ebf4e989919fbeef74ba9809289e9d8948`  
		Last Modified: Thu, 05 Sep 2024 09:08:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:5eabea6c73de57f585bfab983d9a543767d35cf0d2a003dff59e57b9b70b9098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5907074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654039c7ac1b5c37733ca5dfe598c41baa37986a2f2616d21a5a0f2eda7361e7`

```dockerfile
```

-	Layers:
	-	`sha256:f4722f9b9674431ae8f2fdfb4ecab1363f91bc3e893eecf5dccf0d22d15465dc`  
		Last Modified: Thu, 05 Sep 2024 09:08:10 GMT  
		Size: 5.9 MB (5852656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23b6853ac34db2f293b6985f6b2b91edf1d10ce0372d111ff0cef6513783d087`  
		Last Modified: Thu, 05 Sep 2024 09:08:10 GMT  
		Size: 54.4 KB (54418 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b6b556c7907d529dba10bed067a93e219ba8c5e7ab2c75b28b9e3a28287b6fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136937098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c3f122e23bdd198c1283bfde1f631c14eaed78114bffc437043366637a8b27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16-1.pgdg110+1
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2b01cc9b32ef6de1409283ddcbd829b65619e9afccb9d845e9af6bd1be7682`  
		Last Modified: Thu, 05 Sep 2024 16:08:52 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d485dfa76d8a734e194bcb59e9ee5bb65a041a82c13828a230a1c91683a7fd`  
		Last Modified: Thu, 05 Sep 2024 16:08:53 GMT  
		Size: 4.3 MB (4312704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6040b61bcd643bc0d338f3e6058c46a5dac0014fdebdac5b925cc65ff559e5c4`  
		Last Modified: Thu, 05 Sep 2024 16:08:52 GMT  
		Size: 1.4 MB (1404108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656cf2221a1bacb5afca55670af2b9e25a3b9b85529b9f075f5d02924d81ab97`  
		Last Modified: Thu, 05 Sep 2024 16:08:53 GMT  
		Size: 8.0 MB (8044220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da18785bd70d991fdca6bd8d565be084603c5fd8faf6cdae863b104c12afabf`  
		Last Modified: Thu, 05 Sep 2024 16:08:53 GMT  
		Size: 1.0 MB (1026577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd478cc402fa0416b0b01d600dab85704795d3397553868789ae087c6378448`  
		Last Modified: Thu, 05 Sep 2024 16:08:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0278feac55966f4a0f947226fd7a64d6ac31b04b711b476f70d347a8b65fa9ac`  
		Last Modified: Thu, 05 Sep 2024 16:08:54 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14ae58ab60e8d4f0dc9e06bf44bd28cf786b152ce5a22d14e3d9690adb1ba6f`  
		Last Modified: Thu, 05 Sep 2024 16:14:13 GMT  
		Size: 92.1 MB (92054924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aabe82eb0511b106e940bb32e7269cc4dd70b0d7680758a3dd60cb61e66e471`  
		Last Modified: Thu, 05 Sep 2024 16:14:10 GMT  
		Size: 9.4 KB (9357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b66141449171786d70ab72cef0d80672fd5051e9541a3c9f1309399460c74d`  
		Last Modified: Thu, 05 Sep 2024 16:14:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1cfee93a13549dfa11764f869f2cecc18586018b5632231da896d5e4c23826`  
		Last Modified: Thu, 05 Sep 2024 16:14:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edb2f379742e842bc7027623da9ae4c75a72d2642d0cefdeb86c4e037262748`  
		Last Modified: Thu, 05 Sep 2024 16:14:11 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0142de9536f5e87342f7bb59b5c66131448246d1bb915b8b22d23dfc7e3e80d`  
		Last Modified: Thu, 05 Sep 2024 16:14:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:a905d85635ca6a18133151178c64cfc80f243eafdc1d79bb2ff7bee25aa89a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5903045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbe750f22c056715366e9cac6fb54309f67e6f357bc5389c3024a91cbecaba8`

```dockerfile
```

-	Layers:
	-	`sha256:fda74269d1f88ec3e0bd501109dbce97f5aa9dcdb61dfa60bfb3942d80afa76d`  
		Last Modified: Thu, 05 Sep 2024 16:14:10 GMT  
		Size: 5.8 MB (5848530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11f430e0555f474f5f6497d0661c7d91b6f3a7600f7644fc461822b7b86938c7`  
		Last Modified: Thu, 05 Sep 2024 16:14:10 GMT  
		Size: 54.5 KB (54515 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:70fb2700e131c4c6f308ebeb732e1963da13e696afb306513660dffa17547d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143113582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a672b4a12934ff878f11b548ea94c0007f06d45fe75b1b7eb49e2b672d66f7a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16-1.pgdg110+1
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abfe95bfbae3215305360c1cfa78c6c35eda81226af85c5b9844ba64309b55a`  
		Last Modified: Thu, 05 Sep 2024 00:19:51 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023ba8c30a7e06a40bc902be32738e30bd9673eae95b6b2387d544d516815408`  
		Last Modified: Thu, 05 Sep 2024 00:19:52 GMT  
		Size: 4.7 MB (4719561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a7bf0c1cba47bd947b71b6929f99d4c461e36fb9a170f46ee4cff07d7337a5`  
		Last Modified: Thu, 05 Sep 2024 00:19:52 GMT  
		Size: 1.4 MB (1447746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49029a7629be21e48a0d2d168472db545874e8ca195b1c9e52dc552ff5e0857c`  
		Last Modified: Thu, 05 Sep 2024 00:19:52 GMT  
		Size: 8.0 MB (8044348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa8ad7051b7de9e26192d610011f6c9d9291929fcec891b3e70c5b82f894bc5`  
		Last Modified: Thu, 05 Sep 2024 00:19:52 GMT  
		Size: 1.0 MB (1028896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e334986206a66238aed2abf4fcfe65aac68c98a825de55a0f076206d4f6026ed`  
		Last Modified: Thu, 05 Sep 2024 00:19:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b392f8f8d497dc79753529314a3d275029ab6a2706bde026d6f24dbe132348`  
		Last Modified: Thu, 05 Sep 2024 00:19:52 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621e6a6131a32bed66303aa65af334e4f52887052133eea8506e427a21ad6fe3`  
		Last Modified: Thu, 05 Sep 2024 00:19:55 GMT  
		Size: 95.4 MB (95439522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e061196c2d48ff99e6b7c021c6a9f57b1d3ad2df395f8a535461b14159d1e0`  
		Last Modified: Thu, 05 Sep 2024 00:19:53 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bef37c1ad0d150786fe2c6ab289d4d9114d126ad25563d8e1733b7832593af`  
		Last Modified: Thu, 05 Sep 2024 00:19:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7ac69e4126ca62ef8ef72a749f4aa2b76caf5581eeea51b2f5af5ad9d2cab6`  
		Last Modified: Thu, 05 Sep 2024 00:19:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6082e299c4df503979dd7771df8edbf88deb16a02b9cf4b7adac5c9db36416e`  
		Last Modified: Thu, 05 Sep 2024 00:19:54 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a44522398cac6288b3b22de02dfa126b228ede263a7a8dae39742552f850b6`  
		Last Modified: Thu, 05 Sep 2024 00:19:54 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:ee1027902ffa749fc3cffae54cd0251f0768da06206cebe852d01f88012350fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b03486c0fea07fce543bf2ed73cac79d69aa7f0b11aaf5f76283b5aba4d8b2b`

```dockerfile
```

-	Layers:
	-	`sha256:e44cd6ea9413ad0db4e310225c94fe7ddb7305a60825bb2c7298a816b85a1f7d`  
		Last Modified: Thu, 05 Sep 2024 00:19:52 GMT  
		Size: 5.9 MB (5850347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b703e443e4d49d8e57c77544a497c2bbbdf4ac336503dbf81f28646897b18e`  
		Last Modified: Thu, 05 Sep 2024 00:19:51 GMT  
		Size: 54.2 KB (54189 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:510e0adb88b41e4f651833977d8d26eee892278438299670c45a57496af4bc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134824896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abd54c5e36d5a45f0e5c54b72207322f2d1666579e6a008f52b59d76f179fa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD file:d4b92daa2701c7af077c4c89b2b1f5a97cfc6389c09e049b3bdaa36454653bbd in / 
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16-1.pgdg110+1
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:15b8bd5d9ec350cbe23bbccddd5284b3cc9139e037500a63a02025354518d5c8`  
		Last Modified: Tue, 13 Aug 2024 00:23:52 GMT  
		Size: 29.6 MB (29646095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8756e4bf324c450320a08e19331208ae564f36a011174c89af8cb49a53f60c21`  
		Last Modified: Wed, 14 Aug 2024 06:08:12 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80efd2830b090c4732a7cdc9cc81ab571e02a44d3d1437948c71657571e9925a`  
		Last Modified: Wed, 14 Aug 2024 06:08:12 GMT  
		Size: 4.3 MB (4308324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc775a138ac985753fc78bfa32a171a019ed026a41738516b80442dcb0bf0b18`  
		Last Modified: Wed, 14 Aug 2024 06:08:12 GMT  
		Size: 1.4 MB (1359373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd6a47bae0895d43a00e4068c39d18d5630c457b64a3370f0f96284bb42423d`  
		Last Modified: Wed, 14 Aug 2024 06:08:13 GMT  
		Size: 8.0 MB (8044717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30aae077fa3abd7258a46d4e7c2e634a6f65e59687ca05718c7c1736b0a65ce9`  
		Last Modified: Wed, 14 Aug 2024 06:08:13 GMT  
		Size: 1.1 MB (1090275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb13c1ba77f878e041e12823e8b6dc6ea9d93bd7ecab70a97d379b65f470109`  
		Last Modified: Wed, 14 Aug 2024 06:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a98d98bab3c64f344d2e50547954cbd619d9e47596137358497a0ae3457d01`  
		Last Modified: Wed, 14 Aug 2024 06:08:13 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab049fd242bafce8f6501b0e4812533ee2789b55c47b6008100de127b724d5a`  
		Last Modified: Wed, 14 Aug 2024 14:56:04 GMT  
		Size: 90.4 MB (90355908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd9b12f4cd83303ae8c93135f2c3f32674871fedcc078193edde86e0c8d1b87`  
		Last Modified: Wed, 14 Aug 2024 14:55:55 GMT  
		Size: 9.4 KB (9356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84320b9a7f9cda1e31532e82b79f74b98c19130e39964dad6fe5d85f58987494`  
		Last Modified: Wed, 14 Aug 2024 14:55:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc64365051ef3a781ec6dbf5b7ca71c5835a04f0021a811cbc7ce816ff3308`  
		Last Modified: Wed, 14 Aug 2024 14:55:55 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5646375a78d72241db007a1f28d02ef28016d474b80a4f21f321f6eba9b454`  
		Last Modified: Wed, 14 Aug 2024 14:55:56 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff08c8e8c35de6120de777c8b82f0a05ec7b443a0dd2a79cf5c5192d2292e30`  
		Last Modified: Wed, 14 Aug 2024 14:55:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d50329baecfeed89ffd06b5ba6ff14b1a1aa5caa71ce4943429f8403a76f4b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 KB (54083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08efaeb86d217a8bb0917cb35ef659e525b1bd70f21eb9f48ff5654517886c0c`

```dockerfile
```

-	Layers:
	-	`sha256:002569f23d21c13d9bcb876cae8ebca62b6b782dc5d7075b924c925ee99a3a6a`  
		Last Modified: Wed, 14 Aug 2024 14:55:55 GMT  
		Size: 54.1 KB (54083 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:2ffe428f37d5806724770f09949425238211db92fd96008fd4c5898240858748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151346617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29985d971884bdceb061ccd7fa6418c4f4e9f2e3435f260420fc6cfb93d48ba4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16-1.pgdg110+1
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
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
	-	`sha256:1afeea6138b7115d8af3df907f151bfe707cc0db7ccf06a6b404ed63a02007ad`  
		Last Modified: Thu, 05 Sep 2024 03:24:21 GMT  
		Size: 100.3 MB (100253674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b34132c520fa08ae3b79c6fe5d652eb2202ee8ac0179236d0ef0f9d05be4efd`  
		Last Modified: Thu, 05 Sep 2024 03:24:18 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5700a6e6ec067abaebef619656fc880d428ab0c750175ff83295d0cef862538d`  
		Last Modified: Thu, 05 Sep 2024 03:24:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dca852d0ef21bdb6df82de6b4fe6f365245bafb40893ec638c60ac539297409`  
		Last Modified: Thu, 05 Sep 2024 03:24:18 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f6e2b7fa25037c02be2fff3e60eeeb1de35150551106dc7f9d479a04588343`  
		Last Modified: Thu, 05 Sep 2024 03:24:19 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d11eedafff4e80f0239b407f6df9eec00d150ab4e510c5592983c0512e23754`  
		Last Modified: Thu, 05 Sep 2024 03:24:19 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:0797acf4ce061ace35b888e570c518e5cfd7d970eadfe09ca25e1f3e6a6c4ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5903656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38ce12ec664f95fd78e469e89ae3483d36c538224acbe2f44cc8c938e887e0a`

```dockerfile
```

-	Layers:
	-	`sha256:5e4b50a9e5af024e45dba83848d376491953d3e087c7986eb46eed012f9fefab`  
		Last Modified: Thu, 05 Sep 2024 03:24:18 GMT  
		Size: 5.8 MB (5849372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94dd23f4a83d006f3640d68a45f3b85e1cd438de011309c0a1be87b075fe7073`  
		Last Modified: Thu, 05 Sep 2024 03:24:18 GMT  
		Size: 54.3 KB (54284 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:995d2f4638545d97bf3017e44d42534ade85a0a3716a7d4c1ef5c30ed07ef57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144842877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ffc8b60192c982c94f5ef2aa764744681394306c0442dac429c865d2012c8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Thu, 08 Aug 2024 16:37:43 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_MAJOR=13
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PG_VERSION=13.16-1.pgdg110+1
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:37:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:37:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:37:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:37:43 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:37:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:37:43 GMT
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
	-	`sha256:38d03d8ec8f6f30f4fd102169363cb1ac9f57c0cae624eb75281f62bd3d9a4d8`  
		Last Modified: Thu, 05 Sep 2024 05:14:52 GMT  
		Size: 100.4 MB (100406806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9719b84e21b94a63e43877a613058e87adefaa69aeadecc9ac2438a9f6bbf6`  
		Last Modified: Thu, 05 Sep 2024 05:14:51 GMT  
		Size: 9.4 KB (9357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ca6c80affa35cdc0939bac9e36ff2a3339a1ce7a7ab2acf60a2024df5d6dd4`  
		Last Modified: Thu, 05 Sep 2024 05:14:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66254432c5055ffcddb5d7be06a877a20ba3f6e52d11bedbc8b20d09f884714c`  
		Last Modified: Thu, 05 Sep 2024 05:14:51 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59520d02ab37bdbd95f6f8bbb85246d6ebb8f5fad4a56b9989f0ff5d8863e74`  
		Last Modified: Thu, 05 Sep 2024 05:14:51 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d2e96486129457789a16748ab181748acfb7eb1ae50970272df7193699d6d7`  
		Last Modified: Thu, 05 Sep 2024 05:14:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:4c3f5e6d7492c33337f1add3d149f11508deeec96197f88ec7552d2921e63e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5895453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46acf7ecb4e27f1c2cf518f2fe9a0c7c28df11d6b6a293b16677753f3ba04a22`

```dockerfile
```

-	Layers:
	-	`sha256:3703db61dff751a5e6c62204af36589b95c261f5fa8ca0886a165c0afb083308`  
		Last Modified: Thu, 05 Sep 2024 05:14:51 GMT  
		Size: 5.8 MB (5841217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1edcff3df8f71adb0ed4c99819df4a20e777787015546fa487cdefb3c848f98`  
		Last Modified: Thu, 05 Sep 2024 05:14:50 GMT  
		Size: 54.2 KB (54236 bytes)  
		MIME: application/vnd.in-toto+json
