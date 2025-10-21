## `postgres:bookworm`

```console
$ docker pull postgres@sha256:b09ddb966b4d59521a03c4d1c1d3f3af6ab8fe9853be4689ce7dd003bf8b2d1b
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
$ docker pull postgres@sha256:e50487eb111345de4c0cf484f74244dc30ef7514222853b8f27104db3ea87579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157012936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a793016d7e992543305877fbeb30d4130dd67cf11370bba219ebea629b64d7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
ENV PG_VERSION=18.0-1.pgdg12+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb424e7f5824917b57db296a08110d33fcee3d5c6141c175c5fd08e70c0d0423`  
		Last Modified: Tue, 30 Sep 2025 00:07:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3440ed6bcf2ee2c431a84ea771f97bcf4c7d8c3dfd664e52c8bd79b933f40f`  
		Last Modified: Tue, 30 Sep 2025 00:07:11 GMT  
		Size: 4.5 MB (4534006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c08c07169a835b8616d045741873bb412de2bace632afbf2901fb36a3eef230`  
		Last Modified: Tue, 30 Sep 2025 00:07:11 GMT  
		Size: 1.2 MB (1249465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a5dedb0b9b17bcd28ceda5299244fd5e8f8c57c4828595d194fe05f0d0bc88`  
		Last Modified: Tue, 30 Sep 2025 00:07:11 GMT  
		Size: 8.1 MB (8066491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a378c95e020faee083dc6ca9686fdc8f7a5209c7e6991f81c6e227eae7a49d17`  
		Last Modified: Tue, 30 Sep 2025 00:07:11 GMT  
		Size: 1.2 MB (1196361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751039babae5ce5f9b215d5233805277f843b055d2f9c65adbe98e77fbae14be`  
		Last Modified: Tue, 30 Sep 2025 00:07:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d59b97d1dfda21163c6f76aa5603383b45d261ffaee950bd593545f64be4c`  
		Last Modified: Tue, 30 Sep 2025 00:07:11 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065a6411222d2b762477c5864e739403487e93245e6c729cf6f8844da5641ccc`  
		Last Modified: Tue, 30 Sep 2025 00:07:19 GMT  
		Size: 113.7 MB (113708359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179698b8ae848b290ff765f588aef387fada21101f2aae9d47c745b9e77ecb7a`  
		Last Modified: Tue, 30 Sep 2025 00:07:12 GMT  
		Size: 19.1 KB (19081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1694f76ba5bf57baa7e4bc00cea9a935064892408256989b689e57aa51d3d40b`  
		Last Modified: Tue, 30 Sep 2025 00:07:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2433c366ca00110f5130ef57711dfae57a5d2b320aab22879bbe647a87e30490`  
		Last Modified: Tue, 30 Sep 2025 00:07:11 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569e4ffb72393361c09b311b916dadff1cb645f9651c032dda723f24912a63f`  
		Last Modified: Tue, 30 Sep 2025 00:07:12 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af60ce4418c94e40d8fc835b92fa12fa771536115c475435e832bf99e8fb1f7b`  
		Last Modified: Tue, 30 Sep 2025 00:07:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ea57f063a26917cff17706b21c09759406ebb66aefa723a8d085c98f736720f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6211232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90af841f763194b75537522ea64e149bb45108aa4b8b23e38beabf166bc4bf0e`

```dockerfile
```

-	Layers:
	-	`sha256:ee001dd8fc208885552f0434a218b88669d80f5b62c05411ee9666cf5f4747cc`  
		Last Modified: Tue, 30 Sep 2025 02:10:44 GMT  
		Size: 6.2 MB (6156487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cafebacf253f6a89138d5d612902805b927c519b747164faea7c005856608836`  
		Last Modified: Tue, 30 Sep 2025 02:10:45 GMT  
		Size: 54.7 KB (54745 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:b18aa71b784ac76d78beee70c4350a51e1a70111c95c90b413319e0e2e31408b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87144910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a25e944504d23301ef8ad9644f232176a2262b34609f5bd772f15867b747083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
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
ENV PG_VERSION=18.0-1.pgdg12+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:f982c9691d15a93fba0c1226ca85169d870439f0b6119d1ec61ec73d2a7dc8c3`  
		Last Modified: Tue, 21 Oct 2025 00:19:59 GMT  
		Size: 25.8 MB (25757495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d0111b5c1af34045fe7c2ab4bcb26a158e9c91013360a9eb53122b5e461dc4`  
		Last Modified: Tue, 21 Oct 2025 02:10:55 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2526911c4b884cb7bf0ebe374483d33453cab2212cc1235af72cec6e1b5d886d`  
		Last Modified: Tue, 21 Oct 2025 02:10:56 GMT  
		Size: 4.2 MB (4151177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e76a20c857adb015a88ef3792b5223bae64c00f025398b24c7c0573fa81ada8`  
		Last Modified: Tue, 21 Oct 2025 02:10:56 GMT  
		Size: 1.2 MB (1220023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e0507591c2c2e8dab8b22bb7cf3678e37d3cb18cfc1aa6b277aed0a38df038`  
		Last Modified: Tue, 21 Oct 2025 02:10:56 GMT  
		Size: 8.1 MB (8066601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21938f7a029094e89ea75835e1dd1d1cc84c1682878d9eb1bcad3833cd9cc8e1`  
		Last Modified: Tue, 21 Oct 2025 02:10:55 GMT  
		Size: 1.2 MB (1195032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842af33dcaacd94a953c8e4331caad787a1fc3ccd43204c5fe593796e174422f`  
		Last Modified: Tue, 21 Oct 2025 02:10:55 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c7bdaddbad3e61c1ba49c20878ed97d1fe30782a22b4275fefe39298bcf227`  
		Last Modified: Tue, 21 Oct 2025 02:10:55 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7825ce6e4dab9d86eb24b4a2ca669a9a12bbd4e82690817295c573df80214f`  
		Last Modified: Tue, 21 Oct 2025 02:10:58 GMT  
		Size: 46.7 MB (46724651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d64c741fbde011dbd890d7e1c0b665836f3417407d778e83b70acb2e58dd736`  
		Last Modified: Tue, 21 Oct 2025 02:10:55 GMT  
		Size: 19.1 KB (19091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7323ac5b90325c7370f1bc09a0aca7ec766ad355e4b8f4a534f4a0a5ed8e59`  
		Last Modified: Tue, 21 Oct 2025 02:10:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8347418e0a35c6789c573562d616a98c432016d64987eec3cc6ce2c195aa4e`  
		Last Modified: Tue, 21 Oct 2025 02:10:54 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ca3a436a09f211bcbc58a0cce242c96b20e8881d97c2b6de86057f6867f688`  
		Last Modified: Tue, 21 Oct 2025 02:10:54 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c1840b0848504f9d7e456c9a6fcb6c3319e722fa3f5b7f97dc66a67461471c`  
		Last Modified: Tue, 21 Oct 2025 02:10:54 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f29b7d006fdadb1cd9ff7bcda30a364820599a44c12d0b37b47f9d1bf6629bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fde25466eab7d6cf8397a1c53712a23ab4de6414ac28d24fb145baa8d73c58`

```dockerfile
```

-	Layers:
	-	`sha256:dfc3360d24b779bc15468d7ca1fee39ed9d47a2cc156ad1f89ce35be09858054`  
		Last Modified: Tue, 21 Oct 2025 08:13:44 GMT  
		Size: 5.3 MB (5317006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66973f00dab034b069290d2d3074a53860ff65dbbe1c4febccef80450674937`  
		Last Modified: Tue, 21 Oct 2025 08:13:45 GMT  
		Size: 55.0 KB (54954 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:37d74a26d4992ce86896dec435d67ecd88f111e0df0019624d5d36cad79e4884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83273115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2482abac75214253246c0403716ee9a88004b04327c924316c1a92fa3e39c084`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
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
ENV PG_VERSION=18.0-1.pgdg12+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481d88a62eb17699f22d5abaca3e22339e26b06128ade65fb9a60ea17c7b25a5`  
		Last Modified: Tue, 21 Oct 2025 02:15:45 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab12cf4ff355a67cf97a4af65a77a4c510251feade65ac9e30710e5ee40829e9`  
		Last Modified: Tue, 21 Oct 2025 02:15:45 GMT  
		Size: 3.7 MB (3742666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88303c13212607095b8bdfc1edb473899e241b42cf2be955864a66e42aa202e8`  
		Last Modified: Tue, 21 Oct 2025 02:15:45 GMT  
		Size: 1.2 MB (1215964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7f4946dbc84d4e7f38558304c8584b26b67e62f086b2d219ffaccd6c2b3700`  
		Last Modified: Tue, 21 Oct 2025 02:15:46 GMT  
		Size: 8.1 MB (8066464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35df8d7b933564abf5a089b247234bdf7a4445efa6346d7822f4db9520d6f98`  
		Last Modified: Tue, 21 Oct 2025 02:15:45 GMT  
		Size: 1.1 MB (1067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb90ca75aea06a8a362b8f01fe7d734da77f7086bd72c88a30290adf391a20`  
		Last Modified: Tue, 21 Oct 2025 02:15:46 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a082464f45f84f916481d47c8e96a2136e591bdae0e5b03891c8132feea351cd`  
		Last Modified: Tue, 21 Oct 2025 02:15:46 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5a73d33607ab23cbc5317b0b83eaad203d6d349a00f013daa61bdeb95f4170`  
		Last Modified: Tue, 21 Oct 2025 02:15:54 GMT  
		Size: 45.2 MB (45216844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c88afa97006c1623b578ad7ff8bf724fb5f3b7a29dad6928c620f45e461c0cd`  
		Last Modified: Tue, 21 Oct 2025 02:15:47 GMT  
		Size: 19.1 KB (19089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab21d1a489acd1c2c3a090c4cc38c29f4d390e358b5cc093f22e77c0c541bd3`  
		Last Modified: Tue, 21 Oct 2025 02:15:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103535dad05eeb8057542320ae6f307c1cfff7cc0118c8924490f82076a7b9d0`  
		Last Modified: Tue, 21 Oct 2025 02:15:44 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f19694b6f178995ccf6e9d5e42005178f57c5b5597814fd85ea6bd9988c5225`  
		Last Modified: Tue, 21 Oct 2025 02:15:44 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e5289f8193e0946fb885e740d34a08c643feaf7750520dd921f810ad90ae71`  
		Last Modified: Tue, 21 Oct 2025 02:15:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ac069abd2b665f5d5b23cdf132959dd5ad31ff9b79111b64ee15cc142866dc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea0b1bc2bb5b693c756c7ab25d83d2951560d4a8b80443c01603fbe9f911e68`

```dockerfile
```

-	Layers:
	-	`sha256:821460629c996fb0e466f441764f574b89b15cdc432f4f82327365bb7cb53d02`  
		Last Modified: Tue, 21 Oct 2025 08:13:49 GMT  
		Size: 5.3 MB (5316257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1844a1c68d95c627a17e7b294c64428d2acaddca99efed2feaf848d2f9f178`  
		Last Modified: Tue, 21 Oct 2025 08:13:50 GMT  
		Size: 55.0 KB (54954 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:55e2c7043370d80ee05c120de0b7bff306535c42bda9525df8f485cf6ee9b840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155012188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a70eb258cdd7361765be5de224469c61229b242892b9b25617002b00734f79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
ENV PG_VERSION=18.0-1.pgdg12+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a87031e6cf268990c3d2080e52f3fafa50c98a01c0de9d39391db47901fc38`  
		Last Modified: Tue, 30 Sep 2025 00:10:25 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74f9cf5609597015836e9599fb0e4fb81ca8dba374c85284de5c9ddc7e51cf2`  
		Last Modified: Tue, 30 Sep 2025 00:10:26 GMT  
		Size: 4.5 MB (4519837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad621f9363c125bd940c885d2a119a6cab6369c83ff7c11653dac7172abdb2f`  
		Last Modified: Tue, 30 Sep 2025 00:10:25 GMT  
		Size: 1.2 MB (1203276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2365cc782907425f0b24c21d7582b2c8fe32af1846cb22808de401c79ce6a6`  
		Last Modified: Tue, 30 Sep 2025 00:10:26 GMT  
		Size: 8.1 MB (8066549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cac40618779db5b999987270f04a1ec9076381747bb3c61224cc8ecc1dba68f`  
		Last Modified: Tue, 30 Sep 2025 00:10:26 GMT  
		Size: 1.1 MB (1108960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5574674d96289cfcb0c874192d62f5786d944383d89de663234eed75c3055ed9`  
		Last Modified: Tue, 30 Sep 2025 00:10:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf5f330af9ea5fe499dc7a86d535a188503d1e817ca217f369239d6149c12af`  
		Last Modified: Tue, 30 Sep 2025 00:10:26 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8caddaa47cf0037e8ae5a5abea06fc41e5c81a567e5ac741c86d39451215476`  
		Last Modified: Tue, 30 Sep 2025 00:10:37 GMT  
		Size: 112.0 MB (111981496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b37ccd37ca540565a57dec7c4133faa3d1d27314906fe5b0f3f425b196ea2e5`  
		Last Modified: Tue, 30 Sep 2025 00:10:26 GMT  
		Size: 19.1 KB (19088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7c3c885f01a96acd5c4e8fdc2f09eb3a21598d3437d721424178d9324570d9`  
		Last Modified: Tue, 30 Sep 2025 00:10:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3989d9da54a43b686c0c807ad223ffbcd7b30409cc2dfd4a2885338d2a6b7f6`  
		Last Modified: Tue, 30 Sep 2025 00:10:26 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db9a620c4a293874d2d93257ada93d50aa5e4ec7f8aabf0b6932a84550e6fd1`  
		Last Modified: Tue, 30 Sep 2025 00:10:26 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b67bcf5d05ca32382aa13da80d47567b5713bc4732395107f59d75cd506383`  
		Last Modified: Tue, 30 Sep 2025 00:10:27 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7d36a2ad9459a38dc945dcb50da0bef2d59554cb9968be0b9a62fd87122afe5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6217813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee49eebe889b38c01e9362c090be279ae96819ba6574dec201ff276361cbb62a`

```dockerfile
```

-	Layers:
	-	`sha256:5ce0c501a9bb19e556f300769b3ca05d9494be96d8a954fe253331ab4cc37509`  
		Last Modified: Wed, 01 Oct 2025 20:18:06 GMT  
		Size: 6.2 MB (6162812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5da1a8f9ac696875fa202989708f2feaadc26dfac1b6345f32b19bc4d6e42ef`  
		Last Modified: Wed, 01 Oct 2025 20:18:07 GMT  
		Size: 55.0 KB (55001 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; 386

```console
$ docker pull postgres@sha256:3b0e8cd81812446800672a88b4c81053ee2572bad1a3d4239640b2655c143292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93928490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8d277181172bdc84b77629039b1134bfdabd2a06f64777af146d476c7537be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
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
ENV PG_VERSION=18.0-1.pgdg12+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d5e8d56975a711a20921d39fcb90004e3cee833c0898868668e9569e0c7a30`  
		Last Modified: Tue, 30 Sep 2025 00:15:25 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457191f85690212e6b4e429ba1a3d90009fa8c338035c555f82cd25c099cae14`  
		Last Modified: Tue, 30 Sep 2025 00:15:26 GMT  
		Size: 5.0 MB (4965363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45493ea9b28f466e88d84201cd8045d7c3b3378dcf85ab063bc98f8946f330a3`  
		Last Modified: Tue, 30 Sep 2025 00:15:26 GMT  
		Size: 1.2 MB (1218619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecdd2b257f387f623c4e5878076be723cee2b0a5cbbe9ad23dd3ea1dbab896d`  
		Last Modified: Tue, 30 Sep 2025 00:15:27 GMT  
		Size: 8.1 MB (8066524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74195be52fe9349092e8e8e9e641176b02fc7d472d4578b656054cedaa7ef40`  
		Last Modified: Tue, 30 Sep 2025 00:15:26 GMT  
		Size: 1.1 MB (1137414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7697c8bd917720e8ca79315f69bea6b67de2abb5bab11d03a1ad6b9ac5b4fb4`  
		Last Modified: Tue, 30 Sep 2025 00:15:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e24711d7cca43471a92b8f21e6fe03d3eedad431847705f22d0beb409ec118`  
		Last Modified: Tue, 30 Sep 2025 00:15:26 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e670e2c5f37eafb64ce07d1d53438f6496aa3bb2ae4c53f3802ea1dc10855d`  
		Last Modified: Tue, 30 Sep 2025 00:15:29 GMT  
		Size: 49.3 MB (49301022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e7303f1e9e36ace281e8e869cdc5ba13088e563e3546cdf579ecee8f1b5353`  
		Last Modified: Tue, 30 Sep 2025 00:15:26 GMT  
		Size: 19.1 KB (19082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e768c85ad1f86e8f35e2291aba473dde44045995e27e8805879236e586a36f`  
		Last Modified: Tue, 30 Sep 2025 00:15:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d314f7a5b3ba7024a6584d1ae450fa135d3242217de2b73c6c3a54bfe6bd372`  
		Last Modified: Tue, 30 Sep 2025 00:15:27 GMT  
		Size: 178.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6747848cbfc45a2b90d4f5fd85f4389113ff6228c0b8d6c71480e0883c8f68`  
		Last Modified: Tue, 30 Sep 2025 00:15:27 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0542eee536bd904d17121dfec3d7fab53e4fd20c9ceac2f20d275ddb42dfb7d`  
		Last Modified: Tue, 30 Sep 2025 00:15:27 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a7fb9111d08fe789895e15bc4d9abca09385d09739daf4961d50c778cd18d955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5366262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398de080e7ef436a0253937c47b39a748e39db7525297f463953105006c1fd04`

```dockerfile
```

-	Layers:
	-	`sha256:7d261e1331f5d91cd869aca6d153ec9f45fc2075952a2088c08333f66ed1e400`  
		Last Modified: Wed, 01 Oct 2025 17:29:25 GMT  
		Size: 5.3 MB (5311572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e1d00bc57a4ca756566ff66d14428385a8647159218c6dfbbe6671f69f7def`  
		Last Modified: Wed, 01 Oct 2025 17:29:26 GMT  
		Size: 54.7 KB (54690 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:8df33643eed9fb2c5755e502ddcb227b8cd09567eb3579a3bc92520faa93bc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155895823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c9b213a79d4dedeab994932e5590f066ba000a1f13de627bd38fcc094e063a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
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
ENV PG_VERSION=18.0-1.pgdg12+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:73d0a1261a90ced7c792643cb457a2c9f7bbeca1bcb84939b4029c5a1f01f26c`  
		Last Modified: Mon, 29 Sep 2025 23:34:06 GMT  
		Size: 28.5 MB (28513676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d10de371f209c727ac7bb012b4d1ae77293dd115df15e46d99c8906685f7bc`  
		Last Modified: Tue, 30 Sep 2025 07:49:40 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51dc08b8fefc299e23f62291a740a6503e8024a47aec51f1c8188254e5aebc3`  
		Last Modified: Tue, 30 Sep 2025 07:49:40 GMT  
		Size: 4.5 MB (4475423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925e9737c6a53c1079fbe25aeb57d7cc0d67494dd0b106a4ede817d7e356ed9`  
		Last Modified: Tue, 30 Sep 2025 07:49:41 GMT  
		Size: 1.2 MB (1159164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b0b86761fa1b99021362bcff00b5a29604b076cd885305b8255cca752933dc`  
		Last Modified: Tue, 30 Sep 2025 07:49:44 GMT  
		Size: 8.1 MB (8066690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed61a062b9af0ebd72d636f120d6e1c03bc3985a4305e169304de63b52725741`  
		Last Modified: Tue, 30 Sep 2025 07:49:41 GMT  
		Size: 1.2 MB (1182915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e467bb51148e774913eedeeed34d1fd03c9b290a8256fb6d468c0c109a1dc749`  
		Last Modified: Tue, 30 Sep 2025 07:49:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2422393ffddacc15070620014939ddee7917b45ab02de9469126b47eb5169ce`  
		Last Modified: Tue, 30 Sep 2025 07:49:41 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87637fc04da1d1ab15bc203a4e40637dd424bd5186ba0f91dcdb60eef6b37e84`  
		Last Modified: Tue, 30 Sep 2025 07:50:00 GMT  
		Size: 112.5 MB (112468030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ed397d93c84c6b69f927b83ef970a742325baff477e9aa81b2241245476478`  
		Last Modified: Tue, 30 Sep 2025 07:49:35 GMT  
		Size: 19.1 KB (19083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fd8c97deb7a807b20dcd870eece613894bb0230ae41136335f789960f8577c`  
		Last Modified: Tue, 30 Sep 2025 07:49:35 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c29e6dea9f6985d73c08ef1edd87a1907476fd79fa3ec5afe9ff5c0d9aa92b0`  
		Last Modified: Tue, 30 Sep 2025 07:49:36 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fd95dc057da49f99b9d6b86888fd2272b7a52d12bbc1c416eba7c0f0069c03`  
		Last Modified: Tue, 30 Sep 2025 07:49:36 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b3cccded877addb6373c1946333f0126a9d98c9c940af648416f0eefa57138`  
		Last Modified: Tue, 30 Sep 2025 07:49:36 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d3a698a6d1886cc0e7e77a865c54b5599e6576316e565ac6ac72b24e65cbfd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 KB (54620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fba1b5af60cbe2791258e8129cd1f65cddb3f09ea13232d35856af27a40e026`

```dockerfile
```

-	Layers:
	-	`sha256:5a8716242817b7ace8c35245ab7e7c5236697eaf862d25bce1ba4a8976dbd48c`  
		Last Modified: Tue, 30 Sep 2025 17:09:39 GMT  
		Size: 54.6 KB (54620 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:b4b13b77a1a25d1407ec7af87ea074d1a13911aff235063fa6c00835723266ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169915906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd1869985be230a46523b55c63cde8f2bfb4ace3c87a05435b86753460d8c22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
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
ENV PG_VERSION=18.0-1.pgdg12+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b696225b8b1f2c384d658e9bfe9c57053a8668118d549d3b36da48b6963075`  
		Last Modified: Tue, 21 Oct 2025 06:43:27 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a355fa6dc1d1bb059af61333ce6498fc31ae06df0d851330b2f8b540dfeb63e2`  
		Last Modified: Tue, 21 Oct 2025 06:43:28 GMT  
		Size: 5.4 MB (5368479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bd5bba6ec7a0a6fb95ab8cfa7c66966882e07fbe48a05ef522f88873add047`  
		Last Modified: Tue, 21 Oct 2025 06:43:28 GMT  
		Size: 1.2 MB (1208156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae8ac2c42c9f6594b8d8e1e3d130443d58a4aa43fe466ee3d2cdf1ab9826e35`  
		Last Modified: Tue, 21 Oct 2025 06:43:29 GMT  
		Size: 8.1 MB (8066567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9efe0b9f191c41e1b3ed2ec19364d0ea27eb33b7293ee3977c6982e6b2ddf6`  
		Last Modified: Tue, 21 Oct 2025 06:43:28 GMT  
		Size: 1.3 MB (1283638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47fdfb2477182cd6e7d2f31bd55ac647bc86d5926f2af2104859007788ef824`  
		Last Modified: Tue, 21 Oct 2025 06:43:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6517610580277e06311705631cfff65685fe85d637c330e6c783231df1f27885`  
		Last Modified: Tue, 21 Oct 2025 06:43:28 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daed1933a059050cb85f9d7118a24ca013fe1823c357ac05285c1c4aa7d02512`  
		Last Modified: Tue, 21 Oct 2025 06:43:34 GMT  
		Size: 121.9 MB (121890357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aac3126498e6e4195233bac3f29910f401c38cf1966a4a0baf0f12f472cccd`  
		Last Modified: Tue, 21 Oct 2025 06:43:28 GMT  
		Size: 19.1 KB (19089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c8b66c39e007109f2d8aeb4b3a73330c494aa0f7ae30e5cadb32973fdaa39a`  
		Last Modified: Tue, 21 Oct 2025 06:43:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e652277028d48f85737369f145b222b68708d50ac61733c2c87ba42d061f7d2c`  
		Last Modified: Tue, 21 Oct 2025 06:43:26 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e0e45458675f9c221b3bc7b8d38f6b9fb778c25362576563bafcff003ce79e`  
		Last Modified: Tue, 21 Oct 2025 06:43:26 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096bdb78ef1c32a36fe40b35d0a545e4ecd1de0aff0808d842cd7c2bbf0c20e3`  
		Last Modified: Tue, 21 Oct 2025 06:43:26 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0a4e7192b65b53b45ddbaf240141387d227c5a69432db30bfd9fa7763b0349d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6218677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e3ce2b76a8c4acaa54dc9eb40af1ef25c7c3bfbf5bc0e74010eab0e91eac67`

```dockerfile
```

-	Layers:
	-	`sha256:729e522a96eec4645445853376da70387084fdea4c022c552b98a954c817bbce`  
		Last Modified: Tue, 21 Oct 2025 08:14:05 GMT  
		Size: 6.2 MB (6163872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83722b74f383cfd31fced02218ecc79b30a3f5b96ffd8abed91078f6f9e278c9`  
		Last Modified: Tue, 21 Oct 2025 08:14:06 GMT  
		Size: 54.8 KB (54805 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:571dc711c422a059907f403839ba4e8672f478198d2fc2de378fdb99c99b7137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166356927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4952d011cf04d17b6a07a5a415da301b10339652486df82b001a7b28c646f6cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:22:35 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
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
ENV PG_VERSION=18.0-1.pgdg12+3
# Thu, 25 Sep 2025 18:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d48d314d4c4ad33b7f3f8a91af0de4fa9191497ad35b65135e22f849c79fa77`  
		Last Modified: Tue, 30 Sep 2025 01:43:08 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cb5cf9730db1f8d0432592e9a0487585578c243c8ff054591077265b20cd4a`  
		Last Modified: Tue, 30 Sep 2025 01:43:09 GMT  
		Size: 4.4 MB (4391259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e57ed66ef6a49004560c81c56ba2b027f0ad72448adfc8b3f5af5a1ee44bb6`  
		Last Modified: Tue, 30 Sep 2025 01:43:08 GMT  
		Size: 1.2 MB (1222771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eec6d347aebf4ee1aa4431a08de8e9841df88ad708ebf73e585f17cc918d063`  
		Last Modified: Tue, 30 Sep 2025 01:43:09 GMT  
		Size: 8.1 MB (8120694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00f9087bc347a60749002ae1cb46d8d3ea80bb9a074463d729761d05078feef`  
		Last Modified: Tue, 30 Sep 2025 01:43:08 GMT  
		Size: 1.1 MB (1097018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b8c872ec929275fa054b1dbf9fb365de67171baa61027cbb54b430a969045`  
		Last Modified: Tue, 30 Sep 2025 01:43:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a521c4a60db5584ce5b77818beb26a1c3f38ac85c51bbc911ab57d2c7af7c763`  
		Last Modified: Tue, 30 Sep 2025 01:43:13 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa708d2b72d586b692c08986753c3b2c86e7b80c0deeaf692dd9eedb13fc9ba1`  
		Last Modified: Tue, 30 Sep 2025 01:43:22 GMT  
		Size: 124.6 MB (124610937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1236d4fc04487f5c485f0e620e27190c1c774243cf98003b54568607ad94a6c5`  
		Last Modified: Tue, 30 Sep 2025 01:43:13 GMT  
		Size: 19.1 KB (19087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8aa2172daaa0b70e557cce876879ddf59615b85524dde612bbc5b4c5b25a35`  
		Last Modified: Tue, 30 Sep 2025 01:43:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323ea4834759e7d932adbfb35468a2f6606ed4d9e65a18833fd5a13189d45c4a`  
		Last Modified: Tue, 30 Sep 2025 01:43:15 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc87c55e125390e95dbe631e9409f6a64fe6ce1fe3e4aa6cb55cfa2474867f4`  
		Last Modified: Tue, 30 Sep 2025 01:43:15 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6235805a12258133ba703356c1e458a8007748ee923f2dc8af738aebe71e56`  
		Last Modified: Tue, 30 Sep 2025 01:43:15 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:eda594337787d89a476c38fcbce9285ea8bcfd6fe37a016f995e16b2c77a739c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcfcd755500e1427e5180e6184f769a0d94d180ed642a42f344b15292738f64`

```dockerfile
```

-	Layers:
	-	`sha256:9e8ada189b80b71488468715ccd7db158e5dbe2cba027df0f845b559da61bb11`  
		Last Modified: Wed, 01 Oct 2025 20:18:24 GMT  
		Size: 6.2 MB (6171145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682ec14fe84c44394808f27c5a5a651471d00a78ff6487563a8237fe723a5db8`  
		Last Modified: Wed, 01 Oct 2025 20:18:25 GMT  
		Size: 54.7 KB (54745 bytes)  
		MIME: application/vnd.in-toto+json
