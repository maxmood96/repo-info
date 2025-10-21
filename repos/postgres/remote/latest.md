## `postgres:latest`

```console
$ docker pull postgres@sha256:78f1aed6e8c0185d3c6963c8343dd018c63e8ba5ebd78c159c7c772a05e75b30
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

### `postgres:latest` - linux; amd64

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

### `postgres:latest` - unknown; unknown

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

### `postgres:latest` - linux; arm variant v5

```console
$ docker pull postgres@sha256:1f9e747c551995d065342b5d60f4ca882dd8c3247fb18461483f5f1fe72647e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91389748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5144bdf7cf26c5c96743a097e783efe24dc7c39557d91b1abcc88c0b73a577f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
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
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62ead22d3483b3ed0bef9f5797fa7da8529ae0300236ec3632485689d08b44b`  
		Last Modified: Tue, 21 Oct 2025 02:57:08 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41df8235295e5eb3f79d78ac94aad30c2202fcacc6e64a3e76ba4073b7676838`  
		Last Modified: Tue, 21 Oct 2025 08:16:38 GMT  
		Size: 5.9 MB (5928916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5d6fae40c8473be63e829b0b98417f36273e379c8e29d304cde07600a9fe2e`  
		Last Modified: Tue, 21 Oct 2025 02:57:15 GMT  
		Size: 1.2 MB (1227370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0909e5057af78f8748e0cbe734ee4400dad8597c02f8f36e5b5c3ac79336e97e`  
		Last Modified: Tue, 21 Oct 2025 08:16:49 GMT  
		Size: 8.2 MB (8203988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22baec81baa5295e52838442647c8c6dd8fc79813a8f0da299390fd4453fba82`  
		Last Modified: Tue, 21 Oct 2025 02:57:09 GMT  
		Size: 1.3 MB (1317070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d245077e4445825b28cb96af6eef7d2b7f1ba24c9b16395815be83bb49e65d`  
		Last Modified: Tue, 21 Oct 2025 02:57:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ef2ec3a399af79e7a3d387ec95ba74a97796d5a6a5f6eec954894801f6c594`  
		Last Modified: Tue, 21 Oct 2025 02:57:08 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3529cb50c3b39d4490f2ef195f2a094c107fc79eff2b1531a56e3dd68f7e850b`  
		Last Modified: Tue, 21 Oct 2025 08:17:10 GMT  
		Size: 46.7 MB (46736090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a622c22b2a8a7a4d9276bd36f7c57bbfb0040dc7c72318324a679d7a194d6b25`  
		Last Modified: Tue, 21 Oct 2025 02:57:08 GMT  
		Size: 19.2 KB (19183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcb44e7736d0a1f959975e06c2d732f810ee047d9dc336c2e4ab77fd5b842e6`  
		Last Modified: Tue, 21 Oct 2025 02:57:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e55c902324ac65669d1ccf4bd57b36e6823c488d4a6f84be9edd5960626016`  
		Last Modified: Tue, 21 Oct 2025 02:12:14 GMT  
		Size: 179.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a213e5c15c2e7558cb0c399904ea1b7b3c741f6a0cf874e714989f5b134ffb1`  
		Last Modified: Tue, 21 Oct 2025 02:12:14 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c90d297bf0612f123a771b93f12b61a58fcc99d786c671f698034262dab1a3`  
		Last Modified: Tue, 21 Oct 2025 02:12:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:15fb2af4af70ed6d5de9c50332e3857d24ffebc2f2050c5bbabed2591064768b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8eaeb14c93977030357243c55b533bf2db8914e2d96a3045942e0e5b20dd82a`

```dockerfile
```

-	Layers:
	-	`sha256:30e21df180d65c23e25c10dbd410099afb3f2c96ee2f605f221fb7c2c295a1f3`  
		Last Modified: Tue, 21 Oct 2025 08:13:23 GMT  
		Size: 5.1 MB (5119622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d5da906cb231d77169753bc873dd2a2ca3b91c7721e028c816d528127d73134`  
		Last Modified: Tue, 21 Oct 2025 08:13:24 GMT  
		Size: 55.8 KB (55842 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm variant v7

```console
$ docker pull postgres@sha256:89f114ddb0a0b4afe5bbe2ad072a9782316b60c9c4a94684b5433b01801c5d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87713930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783273c1310e18db3c28686b09f5fb999b423413f5b531365a8246407cf75141`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
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
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86bfbb3a3d1fd97a6ffc0041d75f23889c427f5dd3d4750fa8bb9f1fcbce5b8`  
		Last Modified: Tue, 21 Oct 2025 02:14:39 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62481779d95373be915f8c5f02bf718ecb8c1f4f11dc3f83b993186a171ec95`  
		Last Modified: Tue, 21 Oct 2025 02:14:39 GMT  
		Size: 5.5 MB (5496778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653e30d6b5669c76684141c9d595c97e97b937c8d4e5fb3c69767704e6aefc6`  
		Last Modified: Tue, 21 Oct 2025 02:14:39 GMT  
		Size: 1.2 MB (1222230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f80eb5d2cf0aa9a651a7b7cfbd417a7225ddc4c9af5eeb08e7ed7831473bca`  
		Last Modified: Tue, 21 Oct 2025 02:14:40 GMT  
		Size: 8.2 MB (8203788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6237841e6c60ddb7c4e1e53e51cac7ae3ee35ed4b8a65688d294708753c083ae`  
		Last Modified: Tue, 21 Oct 2025 02:14:40 GMT  
		Size: 1.2 MB (1172408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f334b3a532f35d6136f24665ee80306298b0c6eb56435033bc3c8a3745d847`  
		Last Modified: Tue, 21 Oct 2025 02:14:40 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355771a8cd8ec43e693cab40077ce79c26ed9f436a85757327daf5cedf0764e0`  
		Last Modified: Tue, 21 Oct 2025 02:14:41 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182cc9eb748087c4b5b95530ee6022d80e7a64094a593c00c8f80c6ac7ba57f4`  
		Last Modified: Tue, 21 Oct 2025 02:14:44 GMT  
		Size: 45.4 MB (45375791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1673be1a44c5898ac952a57b181441eb99b80b03cc6b705980cb7706b427caa0`  
		Last Modified: Tue, 21 Oct 2025 02:14:42 GMT  
		Size: 19.2 KB (19197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93655e3f2df87d3e6b20deae9ef865bca19d6941933a164edd953e16335ce6d`  
		Last Modified: Tue, 21 Oct 2025 02:14:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9127453153a180ee4810b596ccd649f15c5ea27997ba2d55d50b848a2f161099`  
		Last Modified: Tue, 21 Oct 2025 02:14:32 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e8d98d8ded5777ab43140fc968fa323ec35858d47bd271dfccacccddc00007`  
		Last Modified: Tue, 21 Oct 2025 02:14:32 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11e56aaab23235066708bda7ecabc59358785db1e06183fa332f0363c369123`  
		Last Modified: Tue, 21 Oct 2025 02:14:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:3d8cf722201211f37d4e80c60d4cbee5c1299c91c5ece06ce290a46522779c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5174769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94af6adf1ce4c76cd3f0814b0ee00c775550544105facfedeffc47764e697724`

```dockerfile
```

-	Layers:
	-	`sha256:7dbbe9e1ad45b6d97cc3162c2ba06caf4004d0913adcd77317ce95342e59591c`  
		Last Modified: Tue, 21 Oct 2025 08:13:28 GMT  
		Size: 5.1 MB (5118927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfb93ac871dd18b05331fd3ebed58c2d5387601a9c026f21d310e80e687ce2d1`  
		Last Modified: Tue, 21 Oct 2025 08:13:29 GMT  
		Size: 55.8 KB (55842 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm64 variant v8

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

### `postgres:latest` - unknown; unknown

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

### `postgres:latest` - linux; 386

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

### `postgres:latest` - unknown; unknown

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

### `postgres:latest` - linux; ppc64le

```console
$ docker pull postgres@sha256:ee023bad4101fdca61f462707e88bd33a199867bbe7243313606ea92752631ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174607346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56deabcce1b0e2d2fc8d14d3b94ea0b231d892e69a582dd56ccef8c30807f6fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
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
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40a1023b4b39cd8f94f91177dd2ec82c525f22324af0de522a1f09835fe136a`  
		Last Modified: Tue, 21 Oct 2025 06:40:30 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29c4b9f3f865c7765ea212d75d0ebd4fcfaea04bae27c599f87eabe71b22c56`  
		Last Modified: Tue, 21 Oct 2025 06:40:31 GMT  
		Size: 7.1 MB (7075828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9def1058f18b588d5b13bb8b66ff49776a859b6a0212ea973f590d43e53f416`  
		Last Modified: Tue, 21 Oct 2025 06:40:31 GMT  
		Size: 1.2 MB (1214650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced3c4360289dc76e4a0b030541a3a8f8c105a3e21792bc75905b34daa147ac2`  
		Last Modified: Tue, 21 Oct 2025 06:40:32 GMT  
		Size: 8.2 MB (8203891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9007deac861c3b9259c0f6602548253c7142bf9d262e7365bb227d23947fbb81`  
		Last Modified: Tue, 21 Oct 2025 06:40:31 GMT  
		Size: 1.4 MB (1394713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5f5a15780e5c59562d50c53b32948cf7a09139687665b3b5ea053c12c664f0`  
		Last Modified: Tue, 21 Oct 2025 06:40:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37c262893cf7fd23f5295747e9f28c5218ec7fa9a28e960da8b426d116e2c86`  
		Last Modified: Tue, 21 Oct 2025 06:40:31 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cd48e706e031508a482a676c743104f767f047c0f7004652d416a24096f0e3`  
		Last Modified: Tue, 21 Oct 2025 06:40:53 GMT  
		Size: 123.1 MB (123089715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cbff6dd15c62afe49c4516e3a4c07d9dab1a68fc03b35e40be21f55b865c8c`  
		Last Modified: Tue, 21 Oct 2025 06:40:30 GMT  
		Size: 19.2 KB (19189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489baa59ccb5265bcd8ee4c020c82328c5896eb475ae6cac65a3e610b5e0bc38`  
		Last Modified: Tue, 21 Oct 2025 06:40:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15d2ced14b97cb78c6b2fca78731f351c2b533c46363c8653f243b19807e3fa`  
		Last Modified: Tue, 21 Oct 2025 06:40:31 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934f8de64bfcbf00fba47cba1e32aaab10307a4ed3afcba120b27b41d376c4b0`  
		Last Modified: Tue, 21 Oct 2025 06:40:31 GMT  
		Size: 5.9 KB (5924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3d73b7149c47a3eaae4436de28d47999f55201477f3716d3630628cf3cceb4`  
		Last Modified: Tue, 21 Oct 2025 06:40:31 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:2d5c3b992178dd824207c6491012541bd48569d233f2d017b6f8dddac720cbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6018814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477a23c3a1cd3b2d5edfae73acd5c47ff95628e6bda1c489b00ed2aa61181eef`

```dockerfile
```

-	Layers:
	-	`sha256:862fe901ed0b682064f23194853426a0b9f1effe073db38f34314df8ef2d9932`  
		Last Modified: Tue, 21 Oct 2025 08:13:41 GMT  
		Size: 6.0 MB (5963127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:167a43fb88bcf9b0fb661b7fe16faf588a26c33b1595d1ff9df000d9c33ee286`  
		Last Modified: Tue, 21 Oct 2025 08:13:42 GMT  
		Size: 55.7 KB (55687 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; riscv64

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

### `postgres:latest` - unknown; unknown

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

### `postgres:latest` - linux; s390x

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

### `postgres:latest` - unknown; unknown

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
