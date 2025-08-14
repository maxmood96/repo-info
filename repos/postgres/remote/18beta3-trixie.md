## `postgres:18beta3-trixie`

```console
$ docker pull postgres@sha256:54dcac94ae1a67cf151dbd9074e6eaf6eaa1072313232e653d0019b23a5888c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `postgres:18beta3-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:bfe04c13b28435de86184e8af7af685f702b359c8db066010bc27f05e9553621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162419086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089782435d16ac216ff909309c5bdaf0801cd4e1a3e3a8abbc3f129fda1cbbc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg130+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5465e2fc02041d87d4d08ad09ff3db4cf3e62884f1906f2b0256a05ea58c8dc`  
		Last Modified: Thu, 14 Aug 2025 18:20:08 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e6a10f40ef6d9314cd2e9ea4da3ce0a9c9582dbdc8241416ffc91b31a2f885`  
		Last Modified: Thu, 14 Aug 2025 18:20:12 GMT  
		Size: 6.4 MB (6436505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ff5e258f8fd2e2d1ec66e213bccee595fcf0274c83774f7597350da6927758`  
		Last Modified: Thu, 14 Aug 2025 18:20:11 GMT  
		Size: 1.5 MB (1454156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a3021bbca0f9d884878054d882ff115d5cd33a0940fd7085198618e4a81efb`  
		Last Modified: Thu, 14 Aug 2025 18:20:18 GMT  
		Size: 8.2 MB (8203510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d778f3a78df66d0f29025a3313a0ab5f0110437707c3675a96163479b4b8ee04`  
		Last Modified: Thu, 14 Aug 2025 18:20:12 GMT  
		Size: 1.3 MB (1311339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f337ab3e913d3b21c1079d8a347692412985b0cacb992c7b9cdedcd0335e8e70`  
		Last Modified: Thu, 14 Aug 2025 18:20:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5767f5de090d5c6296d2e1950e9855ac1af689c64c521b1f0cb6787e200f522`  
		Last Modified: Thu, 14 Aug 2025 18:20:11 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da154a987ffcaf28850958cd54d9655fa6ffaf8b19c0adacd75ed418f10eee49`  
		Last Modified: Thu, 14 Aug 2025 18:20:25 GMT  
		Size: 115.2 MB (115210255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612e3952f9406e472403720e690e1f3e3b13ae83ff96aaac7ff80402f3a10a87`  
		Last Modified: Thu, 14 Aug 2025 18:20:12 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e65c7349aca678f158f0a6d40d7f83cbce45823027a543ac6c752f69fd4efc`  
		Last Modified: Thu, 14 Aug 2025 18:20:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a081b5283e75931d667ebd09ab1dc7b20eb6704ec3515105622755149e7e5fe0`  
		Last Modified: Thu, 14 Aug 2025 18:20:12 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4834ace7b8442c182815d826cdb94c070f8a2ddca10e3ecf17ac7a2b9aae389`  
		Last Modified: Thu, 14 Aug 2025 18:20:12 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227f03ea0c8cd6989dad00da35bf011bbb262610fc467ee7d948928ce42f4356`  
		Last Modified: Thu, 14 Aug 2025 18:20:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:20ec492bfc621f85966c0432c96a64f9d01de4a253f773c13764598eb6d17ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6091093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251c6eb49d4e5039561538b1b87125055f3d5326a0b4b480624296818c54842b`

```dockerfile
```

-	Layers:
	-	`sha256:fe8947bf1d66502f3f7f597b0b32ce91d69ed8a78c203ceffbd03bab05baeb9c`  
		Last Modified: Thu, 14 Aug 2025 20:18:30 GMT  
		Size: 6.0 MB (6036644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a0481aee180341e8c768fbaeeb4763272c4b03583b2d1c67760d1b47ba7ccfa`  
		Last Modified: Thu, 14 Aug 2025 20:18:31 GMT  
		Size: 54.4 KB (54449 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:9f506af5b757e1ac57897263aa2929bda6364f3ef075a54baa2d7cde0ef3303a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91624175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946526e184658e80d719cea766d48a7dd1bce2e5db80c2f9220f346d1099c5b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg130+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd555c7122721fce9ac50082cb90196ef4c12bad59bb962375f325b09f73e410`  
		Last Modified: Wed, 13 Aug 2025 04:36:28 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a2cc212ba53aec22ad2e2d0c7ad39ec02310cabcef5a77c09f5ad80d0039fb`  
		Last Modified: Wed, 13 Aug 2025 04:36:28 GMT  
		Size: 5.9 MB (5928910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f35d0a16bec41fbde031a2084f103e824e3c968f41f25a59dbc71352c86ed64`  
		Last Modified: Wed, 13 Aug 2025 04:36:28 GMT  
		Size: 1.4 MB (1431838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf83862c0ee44887895b29bf9b7167bccbfb9199fc869a22e9a541569d368cd1`  
		Last Modified: Wed, 13 Aug 2025 04:36:28 GMT  
		Size: 8.2 MB (8203959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ad07e8fb49647542815d02d3f4cea32cc0ab3ce38078cf237f21263e30c7f1`  
		Last Modified: Wed, 13 Aug 2025 04:36:28 GMT  
		Size: 1.3 MB (1317062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d61269617884aec2be9b0aee4748fd6076d2b6d2cc7137cd3ac827d2ce48cc`  
		Last Modified: Wed, 13 Aug 2025 04:36:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9e3325a032bfd78dd7d49fbe2e1dbd72652f8abd15cc5361a05621e0096ec1`  
		Last Modified: Wed, 13 Aug 2025 04:36:28 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aceeabec2e20fb9d5ba479a3bd0a55f0bc534085a9dd66699c78f0bc3e55c8`  
		Last Modified: Thu, 14 Aug 2025 21:35:47 GMT  
		Size: 46.8 MB (46770667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30be2196a1dc1b5a6405ccf402a0fa90f0c9bdf1ba4bb945c885a0d5e7470a3`  
		Last Modified: Thu, 14 Aug 2025 21:35:42 GMT  
		Size: 19.2 KB (19182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2667b975a53c1428c2b41eb8255368ae309a5a51f6d45cafd4b31aaf5b593760`  
		Last Modified: Thu, 14 Aug 2025 21:35:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9a385cd2699764ff604ddab55cec5ed75db8d4356b9810061d168ccbfab361`  
		Last Modified: Thu, 14 Aug 2025 21:35:42 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d078c713d432ee72f27613df72f24901551533b18eecf220d99a696600375e2`  
		Last Modified: Thu, 14 Aug 2025 21:35:42 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f03e3c41551bf83215d285b3b78cf4c32cb6d9634199c7426855ca3f54290c4`  
		Last Modified: Thu, 14 Aug 2025 21:35:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:42b76c87d9a4752d4c6bc49f446088d39e865939f1dd30769a08ac2a1e47464e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815817a2474a9bab782b198abbf997b9ef19a11dd69c0ccd2375918ffcdf82f9`

```dockerfile
```

-	Layers:
	-	`sha256:4be6487f3aeb52a28f8ff0ee20fe8c5b710b18d51bab14605d8d5f83e5fdcb5d`  
		Last Modified: Thu, 14 Aug 2025 23:12:42 GMT  
		Size: 5.2 MB (5199749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3edfada969ac1ef2f80e8766e67627a1c45e55a315d3ba12987b9e084a56429`  
		Last Modified: Thu, 14 Aug 2025 23:12:43 GMT  
		Size: 54.6 KB (54646 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:76f53fee30ad3995972e89995365f6230c206a35b3ecee63b9f9d711913d463d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (87952494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2844652cc5a3ceed1817f7a13959c83542e8d75bb20c95ac5eda49f3ac6385c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg130+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e177436960330c1003ca564bd12601a903395d0b0cbceb49906e76bb133bf9`  
		Last Modified: Wed, 13 Aug 2025 05:36:39 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881281975ed655f87d3850a9c5ffc603c4c28a60acdb55a90978d19ac3895cd4`  
		Last Modified: Wed, 13 Aug 2025 07:37:21 GMT  
		Size: 5.5 MB (5496723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44faa96ea4758b9d6990cb2d217216e0e259882f4e3d258a5f588b4ee3ecde0c`  
		Last Modified: Wed, 13 Aug 2025 05:36:43 GMT  
		Size: 1.4 MB (1421079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30ff06bfe1035684b16f4733453eed17aea6cb49af31f0215ccdb27a2f0df5b`  
		Last Modified: Wed, 13 Aug 2025 07:37:23 GMT  
		Size: 8.2 MB (8203738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc86471180219dce5a3290d91742b99996e732b743b368fb29bf7613c6ea0d02`  
		Last Modified: Wed, 13 Aug 2025 05:36:50 GMT  
		Size: 1.2 MB (1172344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a91e68d4e8d7ceae6ee126ed6a8c666d3fc98f2fcd5e7a4f54c97683917aa23`  
		Last Modified: Wed, 13 Aug 2025 05:36:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142085f25724adf875ea5aff59337bd6ba553b165dff76316376b3e5fa05d93b`  
		Last Modified: Wed, 13 Aug 2025 05:36:57 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4d1fd2e4ca2298c82a3e17d3473024b7df51a35fe98a4553fbffeaf8e72e1a`  
		Last Modified: Thu, 14 Aug 2025 18:33:27 GMT  
		Size: 45.4 MB (45421071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc796478d8004d2003def016fa0429b82e5f92034d83dc11861fe680630818b3`  
		Last Modified: Thu, 14 Aug 2025 18:33:14 GMT  
		Size: 19.2 KB (19204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8857a9f3704d2814ed79228a7b32967cff171917f1abb884649e6152530dd41d`  
		Last Modified: Thu, 14 Aug 2025 18:33:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd177ae1da5986696394c48b9b99d0ea6202ce73c3acd435f42374fa4b94f6b`  
		Last Modified: Thu, 14 Aug 2025 18:33:14 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7342a482446ba8ee6e29769a126b44050bbe52f6e2ead84e21bb42e16750a6d4`  
		Last Modified: Thu, 14 Aug 2025 18:33:14 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786c701965ae8b86bfc86be86f4e8967464533efbe4b7b2359651dd0d39cb3e9`  
		Last Modified: Thu, 14 Aug 2025 18:33:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:db438f1210af01b48d02865ce0b91ac5d96a7b54b221b4fcb4504b240d838328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8f2fdf8cf035f1bbb53b830aa93ac781feab7ef6b3e5694be540cd0f3fccb4`

```dockerfile
```

-	Layers:
	-	`sha256:b4dce3422c453620debac10ade0a6a7570fa6acf1c4aff0ecd8127c31688b11c`  
		Last Modified: Thu, 14 Aug 2025 20:18:36 GMT  
		Size: 5.2 MB (5199062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1849b3e78f0af3903ba384b849546a156be5f91bb3bf9fae2e359f79ce11738b`  
		Last Modified: Thu, 14 Aug 2025 20:18:37 GMT  
		Size: 54.6 KB (54646 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6043f5fbe082556f16ca0da724a9e11c98061caeb6253ed00b8c624d95d4bbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161022276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bafd7264e3f1bdcbd6f7676eb7a2ffea0b49712f2c5cc45756edfdd9610985a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg130+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7098fadfc7263d599e9af91cf79815094f50dc3cc507ade0066d04ad3c726ca`  
		Last Modified: Thu, 14 Aug 2025 18:50:02 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dffe450d7574d241fa48f7ff718c644e3321fd4302af3609a0c8ba64954b09`  
		Last Modified: Thu, 14 Aug 2025 18:50:04 GMT  
		Size: 6.2 MB (6231933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4db2875216f60ed11db0b51dfb0a8c245d707616c1fee2d5be3e7f4f57d7d7`  
		Last Modified: Thu, 14 Aug 2025 18:50:03 GMT  
		Size: 1.4 MB (1386103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc89b2d2c7ebd971d89d938c54a70f717c9fc7a490e68ac21907a55cb0bef1e3`  
		Last Modified: Thu, 14 Aug 2025 18:50:06 GMT  
		Size: 8.2 MB (8203710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94585c28ed89799a31e0ce000be0468632483f98c7bcb0a753b18b3ea98d3244`  
		Last Modified: Thu, 14 Aug 2025 18:50:03 GMT  
		Size: 1.2 MB (1220343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237ff033285bc1aa8935f4969aa89ecab2ebbd9a33046714e4a64a67a8475df9`  
		Last Modified: Thu, 14 Aug 2025 18:50:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd40904509c4302fd6377d5f113d3a63b7856101000b8f3c14e7e5f70d9a8f4`  
		Last Modified: Thu, 14 Aug 2025 18:50:03 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316ea521e2ea2a6ef656dcd9cd4a6cdd6d13dda0116fe9ed4bc7951ff3890ccf`  
		Last Modified: Thu, 14 Aug 2025 18:50:16 GMT  
		Size: 113.8 MB (113814106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51b4b6e4a9ffa07920cdfed2fb114e2fa26f7ed38a8ab26d1886413fbfc3fb8`  
		Last Modified: Thu, 14 Aug 2025 18:50:02 GMT  
		Size: 19.2 KB (19189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80850505d58c05cb555258b830d2e33487294595db09297c61b43396a5aad88`  
		Last Modified: Thu, 14 Aug 2025 18:50:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0543fdfedd19fbb67b8c654618df68e272aa3fe2d920b594f3d1bc425345af`  
		Last Modified: Thu, 14 Aug 2025 18:50:06 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab3a61e34799dc9d29ec25f70e68d66b7fa7a5f287536df91247ae1be647a10`  
		Last Modified: Thu, 14 Aug 2025 18:50:06 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c56c528018a3578254e82c850491d02a171c65951c0ad5d8da34a3371739062`  
		Last Modified: Thu, 14 Aug 2025 18:50:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:a3f934c3a5a5092c2c4375b3659063fdc04e547a9870367e8d0a52fa530d1c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6097667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fad9975670398166952672b749f859e820da4712f8b8fef764ee69e14874c12`

```dockerfile
```

-	Layers:
	-	`sha256:1216d153538871cb7d73647254c6bd232aba50a69af342e13a4a0d524caca7cf`  
		Last Modified: Thu, 14 Aug 2025 20:18:42 GMT  
		Size: 6.0 MB (6042973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c6017e2b5674d2bcf381d751083f2df2cd3aa8202e81436196960541d251f7`  
		Last Modified: Thu, 14 Aug 2025 20:18:44 GMT  
		Size: 54.7 KB (54694 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-trixie` - linux; 386

```console
$ docker pull postgres@sha256:6d4fc6cb0ac0829aa16244d88375ea9e79596f5de41037d12d5c046b4274742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97727222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59cb5446a4379069a32af03b69768a568b37b878646a38d7afdd95229f7bd7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg130+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53455b458e8cc56e0c3a23214495f4d160940933df5154dcb57b04833766473`  
		Last Modified: Thu, 14 Aug 2025 18:30:38 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d7ee8e2e691af2ee85c5fa03869c85b54dd1b9ea19b357c74dfb365f47dbf1`  
		Last Modified: Thu, 14 Aug 2025 18:29:46 GMT  
		Size: 6.6 MB (6629364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae57a149e21384ae9aaf51cb5f1bc830976abfb71cc423c38972ed719c3ef9b`  
		Last Modified: Thu, 14 Aug 2025 18:31:52 GMT  
		Size: 1.4 MB (1429217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0713761aec2737f5456103c01a4ef4f95225c31a4c508759468029c51183c1`  
		Last Modified: Thu, 14 Aug 2025 18:29:46 GMT  
		Size: 8.2 MB (8203687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f6c737a9b0fbbe85ef08ba49af47d3cd09cb24bbb3a3bab64357aa6bc07b0`  
		Last Modified: Thu, 14 Aug 2025 18:33:14 GMT  
		Size: 1.3 MB (1308033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3236b7bd2c2f21f371a221d850422e25b5f88aac5644b356f3162d03e1130092`  
		Last Modified: Thu, 14 Aug 2025 18:33:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c76172a364671c2cc304abd476d9e57d9101d04587c188a2cb713a00f138d7`  
		Last Modified: Thu, 14 Aug 2025 18:33:16 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6eb192ba7b365263e0c795093069fa9b60adb257b3161eb2e2f1fe621eb48`  
		Last Modified: Thu, 14 Aug 2025 18:33:21 GMT  
		Size: 48.8 MB (48837507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885d8b50da0f69942c18a061d57f569ecbed0d33f7ceb2b9d3e8bdc33a574bd4`  
		Last Modified: Thu, 14 Aug 2025 18:33:17 GMT  
		Size: 19.2 KB (19184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9944006ab44c7366f659f29bd9fb9fc5ec612397914ae1a833fbc45b83a227f`  
		Last Modified: Thu, 14 Aug 2025 18:33:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f45af495d7d1b7dd8c29c13f414137311810d7fd14b97146c883eb2f940379`  
		Last Modified: Thu, 14 Aug 2025 18:29:48 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbef2eae11b4e7cc18018f75e427d41c17d69b3535026b10a5ac62b179039579`  
		Last Modified: Thu, 14 Aug 2025 18:29:49 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e236f3c5222a9ed330fad11f902b7fa041f6a07b01a21be87b8d7ca16d6b59`  
		Last Modified: Thu, 14 Aug 2025 18:29:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:fcbba0d965b54a734e4ba4528d723d7540ab7bade916601f36fa7ca2def5b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c07c313bd20d643caa48583f8e4038cdb38999417cdc694499871410aceadf`

```dockerfile
```

-	Layers:
	-	`sha256:9715dac03dc8d7816143d2274ddde5b01d6b3216a47366e49d32196895cb5ba6`  
		Last Modified: Thu, 14 Aug 2025 20:18:50 GMT  
		Size: 5.2 MB (5195122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e030ef5fd9d632c54d9807ba0752f565130b32411b56fe0bfce540204c2665d`  
		Last Modified: Thu, 14 Aug 2025 20:18:51 GMT  
		Size: 54.4 KB (54399 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:af1de42e3b04fc598fa03dc22483979f15aabd69b73c1de2cfe06a5624d1d099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174791652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4091df5d43bdb5f3e7b556f95f09ebf8a34de5520053616af354e0d006c61b7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg130+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c84463a4e245bf480d1082fe107962d670170ad3ce4ceeb441eb1b8c1894de`  
		Last Modified: Wed, 13 Aug 2025 11:18:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab48c672011c47270df0eb9f0fe011c1b11f0f782ddd50fb47509877407eb692`  
		Last Modified: Wed, 13 Aug 2025 11:18:36 GMT  
		Size: 7.1 MB (7075804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584d3214f5520c6f324f729a7d22dc2da1d81fc79af946f19813211f6706f4b7`  
		Last Modified: Wed, 13 Aug 2025 11:18:36 GMT  
		Size: 1.4 MB (1375564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff07dd4e6093aa581bdc2a1d6498f992ffdd0a248c804aa83f4fd205de2e3eed`  
		Last Modified: Wed, 13 Aug 2025 11:18:31 GMT  
		Size: 8.2 MB (8203709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cf24a16b677bfe7b89b4f58449d622a0221b8096fb28ebcb30c3343a51a74f`  
		Last Modified: Wed, 13 Aug 2025 11:18:31 GMT  
		Size: 1.4 MB (1394663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfa5401d8ceef0f3dcc79af5565483fa1c14718a1c6174e89bce76e6bbc7d93`  
		Last Modified: Wed, 13 Aug 2025 11:18:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d071cb6d31991a1b46f9171cb924c00e562156ccffce21e0f904688a6c11a26`  
		Last Modified: Wed, 13 Aug 2025 11:18:31 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc1de4d16dbe99e260926a7cb20b34656dad9728034bf0fad6cd76c2d52b84d`  
		Last Modified: Thu, 14 Aug 2025 18:58:43 GMT  
		Size: 123.1 MB (123117655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7b65036bd030af383da83da238a4e557ba89e5cf4876812844cf6ddab8fc38`  
		Last Modified: Thu, 14 Aug 2025 18:58:32 GMT  
		Size: 19.2 KB (19191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0775b15cdf115db6fbda612d19fd371152103a95fe1cbe14ccb324c34112b847`  
		Last Modified: Thu, 14 Aug 2025 18:58:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b61f9fcdcd3df205af7cd878d73df34d2331782a28d15c71a08d5473855f4f0`  
		Last Modified: Thu, 14 Aug 2025 18:58:32 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2796f73f2d09207dd8e14f8165cb6fb02658f466e2b0f843f31367c532ec5e6d`  
		Last Modified: Thu, 14 Aug 2025 18:58:31 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b303344cfd9e4117c2f29e206caa89cb99727833a48b59dfa028e06376b04e1`  
		Last Modified: Thu, 14 Aug 2025 18:58:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:49356626034cba97a1673eaac505370b9a991cbbbee9fdbf37f01eb5d6779a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6097789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0f86d0e37ee81e28eb300d8bb4b22a1d68f38641d2cd23ea794f263f84a219`

```dockerfile
```

-	Layers:
	-	`sha256:10c5cb237e1f18f6b64070f4beaba84b33681b881c4dfe37eac3f81bb5f0c682`  
		Last Modified: Thu, 14 Aug 2025 20:18:56 GMT  
		Size: 6.0 MB (6043288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a13d90ed45b4bf1514e20b1c2f1319d394ddee4f18c0ad363de676d8649265a6`  
		Last Modified: Thu, 14 Aug 2025 20:18:57 GMT  
		Size: 54.5 KB (54501 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:4b954027c52919d19ad7997ac24dcb0b98128695cecac9665b1096f1e62bdf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177063588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1398c6b83a0dd309f6a5af942b7fd5818f9a79593738c2453421309bda06a5ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg130+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25aeb0c2b2f8a403705aaa83b95622da6bd82510bb53cdca36e1272cbd0ce1f`  
		Last Modified: Wed, 13 Aug 2025 01:43:34 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accebcf53414b9dbc815739458083b2a6f98a6550be094ea88b262aa973a97c1`  
		Last Modified: Wed, 13 Aug 2025 01:43:37 GMT  
		Size: 6.4 MB (6408735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8013a86d3b1526e8549f316b857c57782e17fbeb29e3cc082c40db534c04c72`  
		Last Modified: Wed, 13 Aug 2025 01:43:35 GMT  
		Size: 1.4 MB (1420337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c121b022a27f99e36f3ec7756fc794d10502feedd80ffe25571261315a321ff`  
		Last Modified: Wed, 13 Aug 2025 01:43:36 GMT  
		Size: 8.3 MB (8258719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ea94d1cb2c41e7377a60b32002839fec6b81f9ac5c0562df38de557467c43c`  
		Last Modified: Wed, 13 Aug 2025 01:43:35 GMT  
		Size: 1.4 MB (1397988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b56b31422bd8bace2d32e04b3b5bb8ee7424c4986ab5775be804b7a6c9dea05`  
		Last Modified: Wed, 13 Aug 2025 01:43:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c798199c95340171b328eea53ffec29853d8de362608bce1809335c565563d`  
		Last Modified: Wed, 13 Aug 2025 01:43:35 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef7d69a303ab773d5af02b556df7216b16c4e8a1521635b049bfd8da4cee95d`  
		Last Modified: Thu, 14 Aug 2025 18:56:11 GMT  
		Size: 129.7 MB (129714714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c4a9c46c26376bd678be2a34e9371bc8de7f7dddea74017081f782e912bbcb`  
		Last Modified: Thu, 14 Aug 2025 18:56:42 GMT  
		Size: 19.2 KB (19191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5171474c9782f9ac99261700da851542166d96da85283d2b80dbeb745c9ec1c`  
		Last Modified: Thu, 14 Aug 2025 18:56:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b3c6ec5215b96e03da744737adf2397d47b171ef32a3727eeef2e0cfa2217f`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85559820a99b5542ba089e2abcdf656405e3b50b7c6f3849cdd879d38a2a8ef8`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2109e5044a134fcd605be73bb40fc57a0125ba20c3cc5a84cdd1d55f9f166b`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:eaf242ab0b177577c33d4c1ec57dcf4b7fb6b32ee33a424b960ab88177ceaf90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6107759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3520e64123266dba75894d2c4dd5d58a0ddd297701e7a294b4fd7db161920218`

```dockerfile
```

-	Layers:
	-	`sha256:dcd83579b7579f161b408e6c35d81ce0bd5d974f9fd818dde60f00ce917174b8`  
		Last Modified: Thu, 14 Aug 2025 20:19:03 GMT  
		Size: 6.1 MB (6053310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e55672937cdea5e21b5d0dea5393648dcf831095ff93322167b6ecf5a57d7004`  
		Last Modified: Thu, 14 Aug 2025 20:19:04 GMT  
		Size: 54.4 KB (54449 bytes)  
		MIME: application/vnd.in-toto+json
