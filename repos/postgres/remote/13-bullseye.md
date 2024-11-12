## `postgres:13-bullseye`

```console
$ docker pull postgres@sha256:4dd782dea15d7932ca93004375da58f3271a5d082920484819ee2f960d664667
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

### `postgres:13-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:fa3208aa7530da442512b549ff76ca385b7b65572dec202ab41bbdb4e1dba1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140555991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f351ff278558ce6115dfa19e9caac15698fd1fda825f301d006fb3ebb06376c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b256a3083eeb0e50ac43c5c14bb5dbe4bec828ec7581a03ba22209361e8eb865`  
		Last Modified: Tue, 12 Nov 2024 02:35:27 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f258af233dffd0e83f67d92ed849f2562d8a8f18b6b1525e5e581cbddca25d8`  
		Last Modified: Tue, 12 Nov 2024 02:35:27 GMT  
		Size: 4.3 MB (4308222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef499346739e571cc507af1406b024f046a5fc7f33d905081ae3294fcadc7d96`  
		Last Modified: Tue, 12 Nov 2024 02:35:27 GMT  
		Size: 1.5 MB (1472228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27817e15ae234f7b320ca06f7c7e65f8a515aeb684c47cc0d4b9d8455490d812`  
		Last Modified: Tue, 12 Nov 2024 02:35:28 GMT  
		Size: 8.0 MB (8044583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464b788f28f13d0a63ad60acd0338356957f11f3b246c4ec099f79610983daaa`  
		Last Modified: Tue, 12 Nov 2024 02:35:28 GMT  
		Size: 1.0 MB (1038377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8423bf6536b5acb9fe2e8ffd61ea5d10db642d699212fcc53d4929833291a3`  
		Last Modified: Tue, 12 Nov 2024 02:35:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddcb1435b8f58745a5b88338da6c127e0c2fbd4b163843b5c54eafba498997d`  
		Last Modified: Tue, 12 Nov 2024 02:35:29 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc9994ae52c0554ba8211bd9d22941dba2019ceaca68ce7c40d899eac22e88a`  
		Last Modified: Tue, 12 Nov 2024 02:35:32 GMT  
		Size: 94.2 MB (94220837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731c844fcc9f60c5662205fd7623f8972dec5c05a6e93da88dda6664ff5555f8`  
		Last Modified: Tue, 12 Nov 2024 02:35:29 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2825d3351794dbf42027b2d56d02476b3af9ecdc32f9dcc87bcb1299be2b4a3f`  
		Last Modified: Tue, 12 Nov 2024 02:35:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94749138b7a87d6ae623704bd7fada6bf0e359dafc212fa8b47ecf3a6afaea04`  
		Last Modified: Tue, 12 Nov 2024 02:35:30 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7571fdfb7cecc96c5c555f037b401b6d7a59ff358d58c69d08fbac4e326aab74`  
		Last Modified: Tue, 12 Nov 2024 02:35:30 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed8c5590570ed525c577ea6de2fc955442e9475fa78f917aa2abc9d98d6820e`  
		Last Modified: Tue, 12 Nov 2024 02:35:30 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:52f7790b95053357ec8b39ad88780fd27ae26bbe906f1abee39dba5a9d3b0d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ff5a7ed87ec7983a1366553166e5492ceefe2e96f30eb8f635a7b53a8ac472`

```dockerfile
```

-	Layers:
	-	`sha256:9e3884b2dd394e86ad9928a728b2bf72f47251794c809ccd63c70ef40cb001b3`  
		Last Modified: Tue, 12 Nov 2024 02:35:27 GMT  
		Size: 5.9 MB (5861164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b21fa5a6624e0c06b592a6be6c0863635f995082a43ef4cc723786d7228241`  
		Last Modified: Tue, 12 Nov 2024 02:35:27 GMT  
		Size: 54.4 KB (54375 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:89489940b88fe734048d21da6c3c6079811c4bd9ef51b498eceecf3d7744fb45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128512057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e881125002cf805a42ba422c66203e36e92fd9dbce5633a11d5a14dd407cc91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD file:1a0a5d58e9eaa765a367c84b6a41097f2f807ca887b02e8a1a36fa504592a5e4 in / 
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
	-	`sha256:25eb86cb375819dcc30b18c185d2922f7f09900a247460cef95d47222230e7dc`  
		Last Modified: Thu, 17 Oct 2024 03:08:12 GMT  
		Size: 26.6 MB (26589555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de32be9c720a52367b74940afdb2d3e32862ccfc2147df092aa04adf6a42f26`  
		Last Modified: Thu, 17 Oct 2024 18:32:55 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ff15a87f66f6a908a6a576490ac34bf482409d26897b5135ebd6948998dd0f`  
		Last Modified: Thu, 17 Oct 2024 18:32:56 GMT  
		Size: 3.6 MB (3601804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffc3f08141a457f9b4c53e40f5589900074e98aac2c94bd540d05315b969199`  
		Last Modified: Thu, 17 Oct 2024 18:32:56 GMT  
		Size: 1.4 MB (1439278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3822cf805c301d7318b7c57c3f006094cff7c26d51121b8fa2b0af8f43468a5`  
		Last Modified: Thu, 17 Oct 2024 18:32:56 GMT  
		Size: 8.0 MB (8044509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36a59a85b06e2bd52d2ec2cb341155d250d3f2be1f9ac26b04df0c11e87acd2`  
		Last Modified: Thu, 17 Oct 2024 18:32:57 GMT  
		Size: 908.7 KB (908668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fbcffbce846085f1aeb1ca37200c908e3fec136a9e13d47da767b24f4c52ef`  
		Last Modified: Thu, 17 Oct 2024 18:32:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d07a02586715b0161df3cbe44f34958fd39fb7cc20fd8d25dd384432c3e9a3b`  
		Last Modified: Thu, 17 Oct 2024 18:32:57 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a506f65371eeb16cf30e9c5b8280baabf59597a9196795783a7b1452d91a287f`  
		Last Modified: Thu, 17 Oct 2024 20:28:52 GMT  
		Size: 87.9 MB (87908063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f68e78edc70167579f84763e93782c3b61301e3cf6c032f3dca00dbdf7291bc`  
		Last Modified: Thu, 17 Oct 2024 20:28:50 GMT  
		Size: 9.4 KB (9353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3193875541aa4e400549d51370729430346df23676bf2f932190a23efcef627`  
		Last Modified: Thu, 17 Oct 2024 20:28:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33fa703ff83999b8479bf8cc1a4f545f452735ba9bd29939955527f36999848`  
		Last Modified: Thu, 17 Oct 2024 20:28:49 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea275c3befb387c3921c9d05cd31abc9bab4acff8ec363bc53dc51718329a08`  
		Last Modified: Thu, 17 Oct 2024 20:28:51 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6f0720700963f109b4b14f2fc0c38288ff39e762282c12155bb479adef153b`  
		Last Modified: Thu, 17 Oct 2024 20:28:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:69cc424485fc7396ab3584f217ec0701f50fe415c68b28ee5e1a0a0a596bc5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5907251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ec96f987c6a087bee4cae13ea109b3ecd2d52a099239918d2d1b1fc681f60`

```dockerfile
```

-	Layers:
	-	`sha256:6284845250ae4cb66c7e64c0bc52ad99a6a67e21284e06793eb01b90745346a8`  
		Last Modified: Thu, 17 Oct 2024 20:28:50 GMT  
		Size: 5.9 MB (5852795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8eb49207e92e9ff505426099f6defa702b11f5b423c7d6788d6191b0eabc582`  
		Last Modified: Thu, 17 Oct 2024 20:28:49 GMT  
		Size: 54.5 KB (54456 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:0bc0ed18fa2a6fff33cbbf25a5a9ab5fc99b090cf7a94e174aadd02a101966b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136967491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99363d05ce749117e4a2463bbc7dfcabdcd1fe3a1ab3703feb5eb851cf8ae87c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625705541eb2c232ec6868052605994a58fd1783ec6af4d33d62324beabdd4ce`  
		Last Modified: Tue, 12 Nov 2024 09:10:50 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86ef8349dcde0e9538a12f2b24d39955b32259d90fd9226e4b09e83a23c6eea`  
		Last Modified: Tue, 12 Nov 2024 09:10:51 GMT  
		Size: 4.3 MB (4312806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408ba174abce076b100b1775066ae161d8f3c617fc9f8c9c5f24d6d9452e4822`  
		Last Modified: Tue, 12 Nov 2024 09:10:51 GMT  
		Size: 1.4 MB (1404090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1823cb8ddc148ec3c8dec960e1f98604509d055e771c71cd86a89084c02d09`  
		Last Modified: Tue, 12 Nov 2024 09:10:51 GMT  
		Size: 8.0 MB (8044346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4ea35053fdfd2a5d6a7dbf5900c78c319262391884c26e2fcc89dddee4be76`  
		Last Modified: Tue, 12 Nov 2024 09:10:52 GMT  
		Size: 1.0 MB (1026586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37385ec28429364a4917c18b2047c5afbbf75d0d2d92d13edaa098af60ce190d`  
		Last Modified: Tue, 12 Nov 2024 09:10:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c022894a4b9e1da9147eceeaa4898b06811b419e7f3efb2aefdf946bb2f7d4`  
		Last Modified: Tue, 12 Nov 2024 09:10:52 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c1b0cf50cd1b759f5c0ad19a38158ad081243d6e97e13bea5562b22f49e4f7`  
		Last Modified: Tue, 12 Nov 2024 09:43:24 GMT  
		Size: 92.1 MB (92067877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bf020e2de2d4100ffa67bc980f60abc754e2d604730f7962df13dc28020976`  
		Last Modified: Tue, 12 Nov 2024 09:43:21 GMT  
		Size: 9.4 KB (9353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a67da29df34358123576889d86db377bbe72d9462e49e3aca8b719ede97a792`  
		Last Modified: Tue, 12 Nov 2024 09:43:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccd1b14654bd964f09cda564dd7703324504a0af56e910ed089aa138331693d`  
		Last Modified: Tue, 12 Nov 2024 09:43:21 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3715a997b0a3f401787cc9b5a9315fafac7a5f07eaf8a98041acbb6caa69167b`  
		Last Modified: Tue, 12 Nov 2024 09:43:22 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9981e722120a1f2da6be0bb2487b8172320e1bb78274fac7894b0d139e9a227`  
		Last Modified: Tue, 12 Nov 2024 09:43:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d1c1b33d1e81b38fd10f41d83090c69d22fad642f9b40175348901b741eaca0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980d1d2a5ce84d1ec30f86c2942cf58fb9370e81a3c80f4f80f72f18dc9b6d50`

```dockerfile
```

-	Layers:
	-	`sha256:b43665443f27282036194e055fb577fd36e228207c96b9afea3519739cd9802d`  
		Last Modified: Tue, 12 Nov 2024 09:43:21 GMT  
		Size: 5.9 MB (5867454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df5c5479b1d42df7aa53a2150cdb73d288c28ee9937d6d4d105c213ccc7de16e`  
		Last Modified: Tue, 12 Nov 2024 09:43:21 GMT  
		Size: 54.6 KB (54618 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:172b673a46e95f9ebd993e39e2dff688922dfca59e7d7a537ffdd552b198cb0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143118865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a76beb8822194c15725c8f2d8c37e22bfdd9f744c85efbfe26ad51644d0c8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:37:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb73d33374c2932380fc60448fc8a8b69fe67fcbf7b1607a3462ddfb3838b09`  
		Last Modified: Tue, 12 Nov 2024 02:46:25 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6711450299347fd9065de672ec2f22f34d1d456112740ac28364caf601e3b90`  
		Last Modified: Tue, 12 Nov 2024 02:46:26 GMT  
		Size: 4.7 MB (4719627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f849435d7ef91206bd4abfab0c4738d2652e02aec872c67af00913f6b743b4d3`  
		Last Modified: Tue, 12 Nov 2024 02:46:26 GMT  
		Size: 1.4 MB (1447805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e04b6fee27dab3bc665e9e16455229578d484daf6313df5d61826b2a071ad4b`  
		Last Modified: Tue, 12 Nov 2024 02:46:26 GMT  
		Size: 8.0 MB (8044463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8301b023fd28efd9fc835904dc7f2a9c3ebc458a7752dc7799197e7cf4d008f`  
		Last Modified: Tue, 12 Nov 2024 02:46:26 GMT  
		Size: 1.0 MB (1028925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bf42def809428ae7e6a8406a6df7d952107fd43e29575c9ba1b3b63321ae87`  
		Last Modified: Tue, 12 Nov 2024 02:46:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506c27cc4c153411a756805dcec2b6bc7ec23d926ca411d3f1a3cf9977e2661e`  
		Last Modified: Tue, 12 Nov 2024 02:46:27 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2080a7efeb3435e4c648c3bb408fe18c5f873d119ad61eb0d21ad7364f678f70`  
		Last Modified: Tue, 12 Nov 2024 02:46:29 GMT  
		Size: 95.4 MB (95434497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe5a52cb07c393ed03ad4eb9659e8e0e144574a8dd66d3f7faa4eb35cf7b821`  
		Last Modified: Tue, 12 Nov 2024 02:46:27 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2947a9552edd71f6b9efa570f359fb030879b833bfe7cde0803efc3f99cd4613`  
		Last Modified: Tue, 12 Nov 2024 02:46:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d82d75e20c7e5174aedad06cff05153269d934fe728c121cbebd6896c5b8156`  
		Last Modified: Tue, 12 Nov 2024 02:46:27 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f180f84f90fd05ad46e624e20cbf05c3b7ea9b90863bfa2006fc7876bb8a070`  
		Last Modified: Tue, 12 Nov 2024 02:46:28 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54aada288c7604f396189e8407230ed7c0420f50f800ea7bff66d52ab2934373`  
		Last Modified: Tue, 12 Nov 2024 02:46:28 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:cc1f4ea839c1fc24da8a12793e24978bef8774131d21a1933fc590044e1a4e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5923815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57430423c2d83bc8d30e9b1fba6349f71b9707a406f6bb854cac1345f7ac509e`

```dockerfile
```

-	Layers:
	-	`sha256:f126982342909a23b13da3e7d4ec5e0784672758e808d22636cd6c71d304e69e`  
		Last Modified: Tue, 12 Nov 2024 02:46:26 GMT  
		Size: 5.9 MB (5869483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3ccc71282004242c5183b48dddafc51a786433cb67a534188ccfe11a976803`  
		Last Modified: Tue, 12 Nov 2024 02:46:25 GMT  
		Size: 54.3 KB (54332 bytes)  
		MIME: application/vnd.in-toto+json
