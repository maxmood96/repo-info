## `postgres:trixie`

```console
$ docker pull postgres@sha256:073e7c8b84e2197f94c8083634640ab37105effe1bc853ca4d5fbece3219b0e8
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
$ docker pull postgres@sha256:28f01a051c819681a816dca282088111ade7c44f834dd83cfd044f0548d38c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162183797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194f5f2a900a5775ecff2129be107adc7c1ce98b89ac00ca0bed141310b7e6cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_MAJOR=18
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_VERSION=18.0-1.pgdg13+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
VOLUME [/var/lib/postgresql]
# Thu, 25 Sep 2025 18:22:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:22:35 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:22:35 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:22:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1014e14b3351764fa51db5b034650a73d93386730806c87c57ba0654680f6c86`  
		Last Modified: Tue, 30 Sep 2025 00:07:12 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd90ab5059fa59c022fd5fa29e719f12dc88973d112a95ffba0f466e139bc90`  
		Last Modified: Tue, 30 Sep 2025 00:07:13 GMT  
		Size: 6.4 MB (6436596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d70120d9e223a8f13ec2256e330f49337ff72419bc5dad33e1e94fe07d1740`  
		Last Modified: Tue, 30 Sep 2025 00:07:12 GMT  
		Size: 1.3 MB (1256644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6d7b9d8ba80f631e4f3e8e8affe333877ced41f3612a0c27ed82b2f1e3ecd8`  
		Last Modified: Tue, 30 Sep 2025 00:07:14 GMT  
		Size: 8.2 MB (8203659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203b16f56a7d528d3e1b5b704b46379b906781b709755f7e1ed7658573f2a1bc`  
		Last Modified: Tue, 30 Sep 2025 00:07:13 GMT  
		Size: 1.3 MB (1311434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751039babae5ce5f9b215d5233805277f843b055d2f9c65adbe98e77fbae14be`  
		Last Modified: Tue, 30 Sep 2025 00:07:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af7533693a1f7d750d06a08e5f11091dbdfc9f1172568337c4c0e64257727c`  
		Last Modified: Tue, 30 Sep 2025 00:07:10 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a68d6020eab3a1ed5d13fdb052a71d14638730605fd6baf264b337f65c8b033`  
		Last Modified: Tue, 30 Sep 2025 00:07:22 GMT  
		Size: 115.2 MB (115167673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69a7c424b50f8ffb8b67916ddd2bad099679ceeca03c7fa929a25b0308c8162`  
		Last Modified: Tue, 30 Sep 2025 00:07:10 GMT  
		Size: 19.2 KB (19183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed0ac863490139b8e73ce9a49c759616ca7d2f5d2ebed8859c9e3d0ed5c387e`  
		Last Modified: Tue, 30 Sep 2025 00:07:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2433c366ca00110f5130ef57711dfae57a5d2b320aab22879bbe647a87e30490`  
		Last Modified: Tue, 30 Sep 2025 00:07:11 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a585c5f82f15b9e7c14376d469fe8c393676ba6b8e2bd6b6a27807a79671eac3`  
		Last Modified: Tue, 30 Sep 2025 00:07:11 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af60ce4418c94e40d8fc835b92fa12fa771536115c475435e832bf99e8fb1f7b`  
		Last Modified: Tue, 30 Sep 2025 00:07:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:9cab9f583d73b00752761a36c127ade160316bf9de28676fd77ac8a2a0567714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6012034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139ceb83533019abe3c854434712419059019a1002c5f3d078c66e0e3f9821fa`

```dockerfile
```

-	Layers:
	-	`sha256:aa821d5942a2bdf04016993781d8926c98bade097abcdee68ba3e63af0e41bee`  
		Last Modified: Tue, 30 Sep 2025 02:10:33 GMT  
		Size: 6.0 MB (5956425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5c6c44d166e629e45a233a8d01851e838e99d758c59382fbe74d2b48aefc710`  
		Last Modified: Tue, 30 Sep 2025 02:10:34 GMT  
		Size: 55.6 KB (55609 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:0ab5598fe2ae08d502846cf24a01268cf5bda5e4ba392cf3fa50a5a037071af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91389237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa6d372961a87f05a41625d216e8b6f4c19a00aa0274789d4838ac921489fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_MAJOR=18
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_VERSION=18.0-1.pgdg13+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
VOLUME [/var/lib/postgresql]
# Thu, 25 Sep 2025 18:22:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:22:35 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:22:35 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:22:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea9f09faf0325ea24e478a95bdc0fa19d7697e63398208fa381b070aa1f0ed6`  
		Last Modified: Tue, 30 Sep 2025 00:40:04 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6743a74aeaa89f79589bc690ec458cba9eaf5574843dba4f4b3651ca6ef03735`  
		Last Modified: Tue, 30 Sep 2025 00:40:04 GMT  
		Size: 5.9 MB (5928914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87378c8860c51fbd95ad4426d0a5017dc6b6e494542d0dd39dedc362adb99aa1`  
		Last Modified: Tue, 30 Sep 2025 00:40:05 GMT  
		Size: 1.2 MB (1227293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6593771c44e02f8c4e0dc33ac04203c7a44441a662c7075b679f96156c2423`  
		Last Modified: Tue, 30 Sep 2025 00:40:05 GMT  
		Size: 8.2 MB (8204089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75078a603ca814cb1b01268abf7def58b4866ded67d76f74a99e8cda483e4bf`  
		Last Modified: Tue, 30 Sep 2025 00:40:04 GMT  
		Size: 1.3 MB (1317118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd61d2a5c6259b8118021710213d2ea66c56142380072ff506406fa083fdb473`  
		Last Modified: Tue, 30 Sep 2025 00:40:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b34ed475f08070018ad8824d0af72bea6b9271a68e7e67e4b9e323d811dd069`  
		Last Modified: Tue, 30 Sep 2025 00:40:05 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73ad49d1153e752cc1f04450abbf35f705eda0a6177732b8cdcc33d5ad470e8`  
		Last Modified: Tue, 30 Sep 2025 00:40:10 GMT  
		Size: 46.7 MB (46735662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1661ceca7f339bf513f241f8fdb1cf7bc8236a9450877131c1c341c91fc6bfb`  
		Last Modified: Tue, 30 Sep 2025 00:40:05 GMT  
		Size: 19.2 KB (19174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26adea7551773572927ac17ef53403608098b1375127b25736f369bafc0cd995`  
		Last Modified: Tue, 30 Sep 2025 00:40:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d2dca48d1de209c7bb829404bc34ab806026fe443bd7ef6aa5a28754f0b2f`  
		Last Modified: Tue, 30 Sep 2025 00:40:05 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d205f01a51236252acb13503a067655d298fb1242c3f2d4521de4ed7fd5e45c9`  
		Last Modified: Tue, 30 Sep 2025 00:40:05 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c40408fbc4e0544027ad60f9e3ccef4851c9aab7422b2914582a5dd999d69df`  
		Last Modified: Tue, 30 Sep 2025 00:40:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:b0bb62922809b300fcf34fee67bf07ec3d48e2b1a964221f8634fc79a3ab0936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2b4cdb7b9835bcd23d60dca7a0a0e229529794710328a586eed07de26f9254`

```dockerfile
```

-	Layers:
	-	`sha256:a11f686dc0b879f0576e3a4fbca5bded582e3c414511a7a63a505bca58289ae3`  
		Last Modified: Tue, 30 Sep 2025 08:16:11 GMT  
		Size: 5.1 MB (5119568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1890629bc2a31f9f805c23ee0d05065a4240365e51918495c2e2a19b3554e90`  
		Last Modified: Tue, 30 Sep 2025 08:16:12 GMT  
		Size: 55.8 KB (55842 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:617b696c843607e178085b3d52555d88fe11ae071d4c042e5974fb4fecf2f61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87715260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538aece2bf3d4bc216eb93315e31573a81c5f15fd9eac7fae4e2405718385fcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_MAJOR=18
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_VERSION=18.0-1.pgdg13+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
VOLUME [/var/lib/postgresql]
# Thu, 25 Sep 2025 18:22:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:22:35 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:22:35 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:22:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9711f3b6390b8f518d3306f230e9eeb1dfc0e3984495e3d021d29d82dca51a2a`  
		Last Modified: Tue, 30 Sep 2025 00:40:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea607d5533d227465514cd2f76eab1f7e42c518f81d1a6ab6e5fc83bd493729`  
		Last Modified: Tue, 30 Sep 2025 00:40:06 GMT  
		Size: 5.5 MB (5496728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62f8df544efa12070b293d08b8d8cdb0b2f77809592e7d4a09db90dbe0765db`  
		Last Modified: Tue, 30 Sep 2025 00:40:03 GMT  
		Size: 1.2 MB (1222211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18205a33014315e4aec783de6c54e7b442d8a6fae7bd10997fd063be79bece6b`  
		Last Modified: Tue, 30 Sep 2025 00:40:03 GMT  
		Size: 8.2 MB (8203848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4efc0fa666b4cd5c83dc0389b61f9ff1bf33f737c4dcf4af8383cd574ce4e`  
		Last Modified: Tue, 30 Sep 2025 00:40:03 GMT  
		Size: 1.2 MB (1172420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12db5f62ccfe1a4b528c2750fa834183e0751d257fa63679d792490ccb2f4688`  
		Last Modified: Tue, 30 Sep 2025 00:40:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760e8af03e34767fcddad4652e392d08704e3756fdb73bbeea7c94dd38298363`  
		Last Modified: Tue, 30 Sep 2025 00:40:03 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91ddb29f10af65bfa8bcc2188b3d9a17b356fa3ba44f16fca604a31821da259`  
		Last Modified: Tue, 30 Sep 2025 00:40:07 GMT  
		Size: 45.4 MB (45377257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2728cacf0c85ab8c17d770ae1c9dfa96e24a2967f11685efb5c05a19ce5104`  
		Last Modified: Tue, 30 Sep 2025 00:40:04 GMT  
		Size: 19.2 KB (19198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0bba57cf88ee61209ca8c1f74220a13709e6443cce7c63cf9ecbf6f5d5065c`  
		Last Modified: Tue, 30 Sep 2025 00:40:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e39d01f67764d6d9ba0dbe1da5bcbfa780efb61f3f43c139ae33d5d51c48ff`  
		Last Modified: Tue, 30 Sep 2025 00:40:06 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6d7f3a533b58feb7686bea1ed89830b514cb780bbf53821b823ba6a34bd3ce`  
		Last Modified: Tue, 30 Sep 2025 00:40:06 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca13fb7575ef18ab20abfff11e67c3945147e140a0505c9aba1cad5487c560d`  
		Last Modified: Tue, 30 Sep 2025 00:40:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:31122b7e00186c9ed394e7e02a09c5f18d5a92f496a9e9a03429ea7f65a74a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5174715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a4457d2add4c2bf8ce9a2d7c47e0e7f89cf95a8dae34de953302bb1745ad27`

```dockerfile
```

-	Layers:
	-	`sha256:d27713cfa1a2b09f9c1ca86b63214c42d451477d696e3976cd3610b25a5f4352`  
		Last Modified: Wed, 01 Oct 2025 20:17:03 GMT  
		Size: 5.1 MB (5118873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c4f13cd57302087d3e9bd73a7b0755d9995487fe5121e1f4a17dc42d12e53bf`  
		Last Modified: Wed, 01 Oct 2025 20:17:04 GMT  
		Size: 55.8 KB (55842 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:56712d2c76b88a12a1729157ceb318756d5988748254d9fbd22fa80d0dbffa9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160785889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a7e541217c7a1b157f4e0d534eaa715ccca6da24e9778c122873a4cc75d6f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_MAJOR=18
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_VERSION=18.0-1.pgdg13+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
VOLUME [/var/lib/postgresql]
# Thu, 25 Sep 2025 18:22:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:22:35 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:22:35 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:22:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b2a95d18aef1132f3b8d2b5f40b5b0287cec7d371e655fe7489a037a338f52`  
		Last Modified: Tue, 30 Sep 2025 00:10:20 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a4d59e48138611c02311cff05cd760cd33776306aa8224793af20d446352f2`  
		Last Modified: Tue, 30 Sep 2025 00:10:21 GMT  
		Size: 6.2 MB (6231941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c23b052c110eca35bbe61569d26d12a3b397e541a68677073d2c820d795010`  
		Last Modified: Tue, 30 Sep 2025 00:10:21 GMT  
		Size: 1.2 MB (1209414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac2184c9eeb417aca04cdd7cf2d089c4554dab0ad4f3143f17c07f272249fdc`  
		Last Modified: Tue, 30 Sep 2025 00:10:21 GMT  
		Size: 8.2 MB (8203826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629006f53423e775d9feed64cfeaea75849e66f854e6e36e43931d48a8842e46`  
		Last Modified: Tue, 30 Sep 2025 00:10:20 GMT  
		Size: 1.2 MB (1220421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8c601be6b5c19a7d9d97d314abb3027138de495f06d1cabd4564e41210b498`  
		Last Modified: Tue, 30 Sep 2025 00:10:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ca5b2589ca782dff0bd23387e1137f58329ea61ff98852e65d418586180d49`  
		Last Modified: Tue, 30 Sep 2025 00:10:20 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35b58d4239fe5887dcb6b3335f579db0dffecde28b96846f3e9b312e8e8875c`  
		Last Modified: Tue, 30 Sep 2025 00:10:28 GMT  
		Size: 113.7 MB (113749423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80471f789f2716ffb003e65cf9c5d3adae5eed7660b55b8b7656c7fb179dcae2`  
		Last Modified: Tue, 30 Sep 2025 00:10:20 GMT  
		Size: 19.2 KB (19180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02edf08630ef07e166f6f702028c96a54a99208b9f266525f9305d17d84aa415`  
		Last Modified: Tue, 30 Sep 2025 01:02:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d02b11f46d831b6d95c2ca68ac3582bb971bddb6b33fed665fc668948ff083`  
		Last Modified: Tue, 30 Sep 2025 01:02:27 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfc0d48617d9d42f0c3864b56fb834054051301679d723f165abe20c150f9fd`  
		Last Modified: Tue, 30 Sep 2025 01:02:28 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f67b02b6b655e48d2c498e6fc51cb18a91a0cbe1fb5554c6f32303ee1079aa0`  
		Last Modified: Tue, 30 Sep 2025 01:02:28 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ec602853c2c253edcfedb996e262f2d26551c13a1d3f632a3190d4c60809cb6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6018700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4742bbe7f4a6bf21080d49457a70b69c59d241f8cdf3306b1a20018b632ae23`

```dockerfile
```

-	Layers:
	-	`sha256:f44d6f330572197852f1d7661e8639737e63f6d286e953569e2b1e8932cdb603`  
		Last Modified: Wed, 01 Oct 2025 20:17:09 GMT  
		Size: 6.0 MB (5962798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68298a1d40893e0672af6bc8671a37e5ac3747a9937a94416fdb511fc4ecd692`  
		Last Modified: Wed, 01 Oct 2025 20:17:10 GMT  
		Size: 55.9 KB (55902 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; 386

```console
$ docker pull postgres@sha256:cdb16ede83438364ee7e4f30052a1b9c8c3e30df43ccfb6b6028a524adcd6001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97504455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd36fd2cec7fecdcec31d277d3799bbdcc330f3ac0d5f30c4b6d0b5926e35d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_MAJOR=18
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_VERSION=18.0-1.pgdg13+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
VOLUME [/var/lib/postgresql]
# Thu, 25 Sep 2025 18:22:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:22:35 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:22:35 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:22:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c81611869dd0bab02fca5c7fee28c34c14ad6d5ea8b22e44328adca75a8b39`  
		Last Modified: Tue, 30 Sep 2025 00:15:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863e293d51155e92713e68379f1c359a170033cb9d61b6ac659a9634b60816ab`  
		Last Modified: Tue, 30 Sep 2025 00:15:11 GMT  
		Size: 6.6 MB (6629417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c607970b0049724faa955dcb8a28bb39306260bbd57fb863164730c9cb04f9be`  
		Last Modified: Tue, 30 Sep 2025 00:15:11 GMT  
		Size: 1.2 MB (1225611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a140f82116ed087dacec2f4c1738a5ff6aa8b8b30ed70d3ce5186e712f6037`  
		Last Modified: Tue, 30 Sep 2025 00:15:11 GMT  
		Size: 8.2 MB (8203852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d773f368325a5dc35185263c086914545fbab8741f68f03a1dd1662a15e6af2`  
		Last Modified: Tue, 30 Sep 2025 00:15:11 GMT  
		Size: 1.3 MB (1308099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1b0fcfe6071ae06982e108520291da3a870d3367d36598202c2d7efb64a6f0`  
		Last Modified: Tue, 30 Sep 2025 00:15:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c84791fcab63f635889621c6ffa2c5d65c3353138d988eca2f80535ce97698`  
		Last Modified: Tue, 30 Sep 2025 00:15:11 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f05ff9d1a2c266c85a4a115d21a8abbc0535ce90332133ffc0a1310fe39fdc6`  
		Last Modified: Tue, 30 Sep 2025 00:15:14 GMT  
		Size: 48.8 MB (48812925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c78cd55bd0b91344874f8ce54d3f1ed510613a4b52139c54de5ff41c3a1bc8`  
		Last Modified: Tue, 30 Sep 2025 00:15:13 GMT  
		Size: 19.2 KB (19177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef7ba0de4902d284ef3d3fea01b7d21ab856fe7a101fede284618ae2d4a409f`  
		Last Modified: Tue, 30 Sep 2025 00:15:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cf5513b638a84c321bfe40044e4ef25e836bf8fbdc10307db51d4254515045`  
		Last Modified: Tue, 30 Sep 2025 00:15:12 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a79a3d3ba95e71655a67e82995fc20d785221dfc6b10a95cdfa2bec9126150b`  
		Last Modified: Tue, 30 Sep 2025 00:15:12 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80fa5108b089436f7168289554422533441f280eedb4880aa5d70b3191bd971`  
		Last Modified: Tue, 30 Sep 2025 00:15:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ce4c5334dc89e739781cbb615a5a0cfa6b295e646520f1d3c05a50f96b4e10c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c8dc61d5b828c70a51359407a6b1e1b7d7437cd6edc4af5a7b10b2384caee7`

```dockerfile
```

-	Layers:
	-	`sha256:8ca3ad52916401373a03dc47c4424cec1eaf65894da430bb8252663e34295a24`  
		Last Modified: Wed, 01 Oct 2025 17:29:09 GMT  
		Size: 5.1 MB (5114901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:850c7313b8b57e476c1e58e4f3b8e2a92361c57843b1ec212607be69b91cb701`  
		Last Modified: Wed, 01 Oct 2025 17:29:10 GMT  
		Size: 55.5 KB (55539 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:47fcebf62d2223703aa35cf64ec767a165f427f12160893c18fa267a64097729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174607657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fe9030a781171b2ee31b6443f71a17a0aa21b548c6d5e7bc43be863e788221`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_MAJOR=18
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_VERSION=18.0-1.pgdg13+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
VOLUME [/var/lib/postgresql]
# Thu, 25 Sep 2025 18:22:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:22:35 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:22:35 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:22:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08338ed8f1b79726cd0288969f288e0573ba1374bd89f23215daf569d56ba250`  
		Last Modified: Tue, 30 Sep 2025 08:54:35 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1e0bfd686fa1b408c7bc9cab1e4e32e8d908fbcd317b18b3c876fef94677aa`  
		Last Modified: Tue, 30 Sep 2025 08:54:37 GMT  
		Size: 7.1 MB (7075843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1893b2b8288689743d5731a37299ddd83da1d7b4f7ba660346e1657c333628`  
		Last Modified: Tue, 30 Sep 2025 08:54:36 GMT  
		Size: 1.2 MB (1214640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8efaf28657d31f3220ac76bef44d5f0f866954cccaa7e12a638c46205f387f0`  
		Last Modified: Tue, 30 Sep 2025 08:54:36 GMT  
		Size: 8.2 MB (8203838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284b0165dbd0821b3a0f9655b0edf4d53db5e9b2bb77fa3b989f617a7a94a258`  
		Last Modified: Tue, 30 Sep 2025 08:54:36 GMT  
		Size: 1.4 MB (1394687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f0097cdb0ecd3619573a61697b10d89be6aac1cf4c2e0c76f613f7998d587`  
		Last Modified: Tue, 30 Sep 2025 08:54:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261e3ce5322df231d42de54c917b2d7219c0bd232c1fcb82476a1ea183b3a510`  
		Last Modified: Tue, 30 Sep 2025 08:54:37 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fd32a83c1c777e67a3a5f3d0db11174c525f84507e378b37dfa2402274d319`  
		Last Modified: Tue, 30 Sep 2025 08:54:42 GMT  
		Size: 123.1 MB (123090174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff8dfd4f4f049e7082a1b8340779c01a98dc530abe5b888679ca53765a2d191`  
		Last Modified: Tue, 30 Sep 2025 08:54:34 GMT  
		Size: 19.2 KB (19182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acc0bb6f007306f52131dc8f8ff18078b93d6d695fc8151088aa3fa418ec395`  
		Last Modified: Tue, 30 Sep 2025 08:54:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6fd3683c95bae017fe1b010090da0572d15536fd73c17a5cfe2f3116b42ad6`  
		Last Modified: Tue, 30 Sep 2025 08:54:34 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f95db9b0f6d18a557b5649a36b3b025980e74f11b2f1569cea9ebe3d94f35a`  
		Last Modified: Tue, 30 Sep 2025 08:54:34 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3e20a81911bc1997995a850e357274cf1135c8174bbd384d228db774e9a623`  
		Last Modified: Tue, 30 Sep 2025 08:54:34 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:aec30b439e4c54be76c2697ec4cc7acebfc5ad481f56fa226b1b69d09f4286ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6018759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0c18786ffd8af957bae61d7f1b03add1c6b92419fffe8cc81733eb0325326d`

```dockerfile
```

-	Layers:
	-	`sha256:dd77b3519493dcc422a643c3db0fd31e5fdadf1a485a9b9118a71c08b7028eda`  
		Last Modified: Wed, 01 Oct 2025 20:17:18 GMT  
		Size: 6.0 MB (5963073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea46719767798260df3af503637981749427a9cc226ae00f178502b69ff711a`  
		Last Modified: Wed, 01 Oct 2025 20:17:19 GMT  
		Size: 55.7 KB (55686 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:b29889da1235dc2acab6f3e2c0c9f30363be9d3e0ef3a8214da16ef2b04edb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92792014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cd885eefa7895f6fb9d2d4f58c69b798c97e9d67bb59237521a13567a57122`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_MAJOR=18
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_VERSION=18.0-1.pgdg13+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
VOLUME [/var/lib/postgresql]
# Thu, 25 Sep 2025 18:22:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:22:35 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:22:35 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:22:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0301c5c59bebc17ecc500294124ab874204ce31730a3ee6219bf6dca38a15c7`  
		Last Modified: Wed, 01 Oct 2025 00:31:03 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187e6ab47b2cd6059043b34e26caf29a93d6596bd9efaa2145c97eddbed3de4b`  
		Last Modified: Wed, 01 Oct 2025 00:31:05 GMT  
		Size: 6.3 MB (6291255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ff0f2663142e3f11729d4011042015a88618346961ad238d6c4965ca0d173`  
		Last Modified: Wed, 01 Oct 2025 00:31:03 GMT  
		Size: 1.2 MB (1201855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e172862d67506d2bea42d74eb14a779a757710701ae31139aa50345b4fdcffe1`  
		Last Modified: Wed, 01 Oct 2025 00:31:04 GMT  
		Size: 8.2 MB (8203543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da291265f9deabc6c8565e1b700aca1e11ec76d808455b27a8923f6e7a989f`  
		Last Modified: Wed, 01 Oct 2025 00:31:04 GMT  
		Size: 1.4 MB (1402190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ce6f5cd9a4c0cda651a1245dc712f5aa7f7cf8f3cd1f6f19409308029a3bb6`  
		Last Modified: Wed, 01 Oct 2025 00:31:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56934b07a2f469878cf15a23729ac99da93cba163b32cb473a0ca4592720ef88`  
		Last Modified: Wed, 01 Oct 2025 00:31:03 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0800c58da4a906619c188beba9f6a67d41a99253fa26ae4cbc9d7d1f43a871`  
		Last Modified: Wed, 01 Oct 2025 00:31:11 GMT  
		Size: 47.4 MB (47387636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf37eaf3a1a77c3e53bebef0ddfcb87138ad8c3d34268f37d5d4cf3c062d2a4`  
		Last Modified: Wed, 01 Oct 2025 00:31:04 GMT  
		Size: 19.2 KB (19190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf6ffce60e7e522d91c210fbfdab9c2f8e1ec2e76ce1861808a7af1921064ac`  
		Last Modified: Wed, 01 Oct 2025 00:31:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8b1eb79ebb48fca733a7e9ee926c2912d49bb85e7cfe806a53e639aa66e6fe`  
		Last Modified: Wed, 01 Oct 2025 00:31:04 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d080cc1f45784c49ef2b056730710b55873ef8151850e5ff8a92a4b2bd67fff`  
		Last Modified: Wed, 01 Oct 2025 00:31:04 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaa12b5628cea9bac9dedfbfca7211c997116a02a064e43a1c490b77e5c56a8`  
		Last Modified: Wed, 01 Oct 2025 00:31:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:deab2f02eeea34201b25f73dbeafcc78969e40533874d5ad9d6190ea9e01b17d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5165522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d044eb8f27dc67c280c0dc60cda1266bd59ca8fb4511e5cf13d2a09d960ebf3d`

```dockerfile
```

-	Layers:
	-	`sha256:8ea173c0d0ec59cb52a7391e1d99b6c7821d32ce4c0ccc2f594dbb354955baf7`  
		Last Modified: Wed, 01 Oct 2025 05:19:20 GMT  
		Size: 5.1 MB (5109841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff71614732f9ad7141515f714d3f82458179a37c040b0a24a2bfd5d2b6777b5`  
		Last Modified: Wed, 01 Oct 2025 05:19:21 GMT  
		Size: 55.7 KB (55681 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; s390x

```console
$ docker pull postgres@sha256:479f701cd9ea7701460ca3a5cf0ba13820e807f63d5c32b5e860e45c2676b7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176832801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72857fb095500e21098e2e69f021162e9654a6858c06eba98ca9d46c61322084`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_MAJOR=18
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PG_VERSION=18.0-1.pgdg13+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
VOLUME [/var/lib/postgresql]
# Thu, 25 Sep 2025 18:22:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:22:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:22:35 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:22:35 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:22:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053c82e2310313dc0ad3fcc1c087300217954c10197550656ef261ae8c932aa9`  
		Last Modified: Tue, 30 Sep 2025 09:06:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ecef323b728b13a98af7ab543ce3f190fe8188dc8bc46957376ab97f6b4ae5`  
		Last Modified: Wed, 01 Oct 2025 20:07:47 GMT  
		Size: 6.4 MB (6408684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210b5d085b1c93d1248ce46ef2f6c10a2c9c8af15d1e7c0d05a331c6416bb4a5`  
		Last Modified: Tue, 30 Sep 2025 09:06:43 GMT  
		Size: 1.2 MB (1229846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f348bd8fa331234966f5888eb9c88e56c0360f6971afad12f21743a771f1dd`  
		Last Modified: Wed, 01 Oct 2025 20:07:47 GMT  
		Size: 8.3 MB (8258775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b134977a7ddbb94c54b137a96a500e71b31c940917153902fc479315509965`  
		Last Modified: Tue, 30 Sep 2025 09:06:44 GMT  
		Size: 1.4 MB (1398014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907711e040d5f8f23d07c25ce91be8921547f402b9a5b7781728e504e4cdf63e`  
		Last Modified: Tue, 30 Sep 2025 09:06:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb14f3173e96d94c28d3af7afb5f815ee7c7c83cdc0d5fe798b69e0f41ce2e1`  
		Last Modified: Tue, 30 Sep 2025 09:06:42 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6226f29f025b1697ab2b423f5559dfa8dd3debb19fe6710b2765e9a708eebf95`  
		Last Modified: Wed, 01 Oct 2025 20:22:20 GMT  
		Size: 129.7 MB (129670225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0d231951a68f67c4cc1089a3d44f03cc6113581a285e5db8db035eb23cd44e`  
		Last Modified: Tue, 30 Sep 2025 09:06:43 GMT  
		Size: 19.2 KB (19184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837fc775f04952526dd9dc99c91f25da215079a085d9982db9c9ee5fa8470ede`  
		Last Modified: Tue, 30 Sep 2025 09:06:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632f49fb6ad8f30cf36a435ac665e85f53201923c0a93afafda6a913c1f4cb54`  
		Last Modified: Tue, 30 Sep 2025 09:06:42 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b21b2e27b80f3a811fc042bc5011af12704d6648a74a0af360ae0f92f57f25`  
		Last Modified: Tue, 30 Sep 2025 09:06:43 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878a5d53f1bac9cd1d3012b164d98a41ee2a2056ec3ea70ae04ee2267b66f71e`  
		Last Modified: Tue, 30 Sep 2025 09:06:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:7a7f65f6503c8d5fa0ab3c09f03fb97fbc9a376b55008cf62da8f93d2cdba470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6028704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52ad9eb5b35b1b923b628905fc9514d3e6e20473942a48216f21f2693b726fd`

```dockerfile
```

-	Layers:
	-	`sha256:5419298a289713e34afe1a28bdd3790dfa3250bf453446e28119cc40c69ee069`  
		Last Modified: Wed, 01 Oct 2025 20:17:27 GMT  
		Size: 6.0 MB (5973095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b28e0e56acaf376eee45f04df15700b50dbb36ecbe43cabd764d3f7a33028aa0`  
		Last Modified: Wed, 01 Oct 2025 20:17:28 GMT  
		Size: 55.6 KB (55609 bytes)  
		MIME: application/vnd.in-toto+json
