## `postgres:17-bullseye`

```console
$ docker pull postgres@sha256:6b985e8e135120720c8586590e6bcff69209d4b0bb4ff587381ad7948ce54132
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
$ docker pull postgres@sha256:a9bbb66c3b8c2870e9534e21c24bb420ff934ff3d09a8edfecf06376ea3850ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150600974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9257af9c44f6d57ce684416e698c0f21d820b18ea9e6742815f79573bd9a5881`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=17
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=17.5-1.pgdg110+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f929b1ea05bb7c83a0e9a222b36eecdf82fbf022f3ca91afc6fad0dc70b3f74`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96834e4072c81eb9b0dd092f0dc251806a0349ce0f1563ad9b0a3e65cc7a1789`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 4.3 MB (4308097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c83e44a32ad3aa9c48db24a09082726e9eafcc69ffabccc81bb62285bf8e94b`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 1.5 MB (1473558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64696a815e8a601c9c1acacef2338639134d68029221ba411985d681143c1fd`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 8.0 MB (8045833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b2c5c4c47f0138c1e73827dba45927f7c3b46fce9af5e0c2be760a55d63efa`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 1.0 MB (1038317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae6d9183867d9561a77e376d4d9767cb5b7f7e2aa52ce1f2daaf374648ce234`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56c4cb822073dba197586d00ee5753fc8b8daf88b6fe9c40c336eafbe3aeb59`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d588ca9d070738bd8f04ef3446f3e3a76787fd37b60979bf6ce6a02e1d2db6`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 105.5 MB (105458105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507aeca12925ab4bb49d62c676583b5dabc15626dc62f80fb1acea5f5a14680c`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f48d16ffa33137ffa772d1605f48e48c1705f9148fcc140934fb159bd81f73f`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5841dd8fb0528a8a6544410103487c1e63d4d5676e4deac5d4c3dcae7cabe78c`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52183d8b231a3ad0d3adb551498fbc70384b78aa956ce687dd44173b58844835`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 5.5 KB (5471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4c7781b3df69a72a488aebdefc6f57039c41cc283ef6e92f2575e83ab4494c`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:31f8e460a7a7fab841d9038948b4ef613c5435f12ecc8035b59fe636b660b0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6148320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0140105a38e16f4606ae4fd6c7eb52b2dada6120e342fe136755dddf526ea2e7`

```dockerfile
```

-	Layers:
	-	`sha256:ac7b1be878ab12765c1ba9636113772801a8acd74867c3b72f319cadde716866`  
		Last Modified: Fri, 06 Jun 2025 06:49:56 GMT  
		Size: 6.1 MB (6094671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c3f525f6c96ef87f859a05a6f30fcf20ba12bd0492c41d41f6ae32cd1c2c7e`  
		Last Modified: Fri, 06 Jun 2025 06:49:52 GMT  
		Size: 53.6 KB (53649 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:c558db8d63c4e7281b9ccae1f7afc7da675daec3ff6f5f84aaa922d4f9f97552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138778280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e8b11c13a95ee80e8bc3f47447758d2a47271446df02ad8a1145c477d5f172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=17
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=17.5-1.pgdg110+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2091b63a268a34467e23520ae27c312421298f420abd278e760061e42a678899`  
		Last Modified: Tue, 03 Jun 2025 13:50:37 GMT  
		Size: 25.5 MB (25543902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2819feb174cd62d9afe4efa58f14c05d6404e45e9fd646186b5caf9e4ffb95`  
		Last Modified: Tue, 03 Jun 2025 13:44:36 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b854a91797948fa74505443fa76802d4719c60aea4cc87fd15783f71c9acfd55`  
		Last Modified: Tue, 03 Jun 2025 13:44:36 GMT  
		Size: 3.6 MB (3601790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6970d22b731c3a99427af1912f1730e34e40009bc7af854735159a9603ffa3f`  
		Last Modified: Tue, 03 Jun 2025 13:44:36 GMT  
		Size: 1.4 MB (1440887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a3cd249b6bf25ca9bbea16ab2a0959459eff6af0e43e16d8c956d2888065c1`  
		Last Modified: Tue, 03 Jun 2025 13:44:36 GMT  
		Size: 8.0 MB (8045791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d46adcc9f43b0fd86209d8380e586d2c3465d713fe7c68169a9b3899cfd39f0`  
		Last Modified: Tue, 03 Jun 2025 13:44:38 GMT  
		Size: 908.7 KB (908651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aa3404576c56b7e91cee8f6cec2f6cd80e371cbe93a5a27e90528f7ed08518`  
		Last Modified: Tue, 03 Jun 2025 13:44:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd2b53fdac06669f7ad19fd8504e96e7e1429ba317a634f81a63c8d05cc0b2c`  
		Last Modified: Tue, 03 Jun 2025 13:44:40 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb11c4633be7f89ad650188db453aa04222a71bd11c33eac9f99b4cc87cb6f9`  
		Last Modified: Tue, 03 Jun 2025 13:44:49 GMT  
		Size: 99.2 MB (99216135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7cfeb28c5fa1f41308a69d2c81967bde148a0a30599a199ba948eceaff5bd9`  
		Last Modified: Tue, 03 Jun 2025 13:44:42 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e04069820cc5556ff93bb3a4ede4a1d7120d2d9c57e222a808c1962e8f48b7`  
		Last Modified: Tue, 03 Jun 2025 13:44:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526ceab1ff79b4de7b01e53eb0d8771ad96edfc2dfa1f6c58ad1332cd8bd5602`  
		Last Modified: Tue, 03 Jun 2025 13:44:44 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ec4c96c74b498c72e2ba81397ea0dcd82ab5e774de5bf46fa92f2d80b299d5`  
		Last Modified: Tue, 03 Jun 2025 13:44:45 GMT  
		Size: 5.5 KB (5472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6806e919bec2aee82d2159e1a03a31250eaa382b07cb6876502a5ba7b8674bd0`  
		Last Modified: Tue, 03 Jun 2025 13:44:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2e6d664fad57641d66a39161d66ebf79dd9aeb3c4c9840f2170a96cc6d0150e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6165885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04507a73155d392934a92cbbfa94d5a83849ef03df8292d1073dc534fb556493`

```dockerfile
```

-	Layers:
	-	`sha256:5f0d93c203d52fbd8894ae0f109d17c509f642bf1cc576cd3da8a3ae8fb635ee`  
		Last Modified: Fri, 06 Jun 2025 06:54:37 GMT  
		Size: 6.1 MB (6112041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d9ce0f70ea9c3ed3fbf381eb54d316c44165e01a8cc790e922f03303d0be81a`  
		Last Modified: Fri, 06 Jun 2025 06:54:26 GMT  
		Size: 53.8 KB (53844 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d401fa23c471d166e2d220385e9890fba6c2934aa525ef8abd6d3efdacb9cc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147606315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a53534b8b2b9b49be2c09cd30dfebfde1016f6a1783a60bcb971b6b79f61bf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=17
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=17.5-1.pgdg110+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32236ba1b821f7c23d25fdf75521f88c96d3223ff4d2910edd70bd6adab8c233`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0d3b9230c80850de668fac2e5bd9a62e220978ee0fc44a5884f3bd6f86f489`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 4.3 MB (4312803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defd546e9378a792a8305e5024aab05e8b5bf2e0d6d7bd768f72c42fe731a75d`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 1.4 MB (1405889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb1b788a19b9e3bca37df18caa5a08422119f78322397fb5bbced6505d845a2`  
		Last Modified: Tue, 03 Jun 2025 13:35:38 GMT  
		Size: 8.0 MB (8045785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef0ec8ddfab83b5e0deb2e20fd330b90628b37ee9ace4ef9d685519eb8d637f`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 1.0 MB (1026595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1137dc2ab794992162498823a64a9165a7a2c92fe8f04754a932bae9919e8be`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a6988ceff54ce62d68edc1d1a0a5056cd10320ba65103b42820fb1f0388ad6`  
		Last Modified: Tue, 03 Jun 2025 13:30:22 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09db25deacfb5ea14427b117ac111313e1372b7f47abcab852a8e519572c5463`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 104.0 MB (104047850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cee0a5a135391b6381001a415d1b1d98fb1abbadd767bc16fa6262d1f0b7b3`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ed5ee2029d7b7838b8ccb1c597b9a462f42df39836efb3b62a5075a193e6f1`  
		Last Modified: Tue, 03 Jun 2025 13:30:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e02f4630d5a48cc4c75cb8df15580a5c83913201c1d774a5ba91ccfc81dcd72`  
		Last Modified: Tue, 03 Jun 2025 13:30:24 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c92bc2438d99e348640d1f4ed4765d232e079027c90f0ab682a050944fe163`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 5.5 KB (5470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f037a72dad54a8286ad556886bc7fec07ec91ef66a76d8e73ba7a3b951454c`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:b8f7a1d71ccf849decda7c2bf34c4a5661a70a366d2f8b63b707ee190e3ed0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6154877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7262cf9547c3f49e321e740546b6dba19eaef9455ac97b1c7b48e76dd1e3ef`

```dockerfile
```

-	Layers:
	-	`sha256:8b7bcf56f8d893cf7d66efadea1d45a7a96615faf1f769310065f5b377a840f6`  
		Last Modified: Tue, 03 Jun 2025 13:42:57 GMT  
		Size: 6.1 MB (6100971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c314f0d0154d2a8fea02e84c1a9382874789bbd29728b572ecf7d1f32f204dfa`  
		Last Modified: Tue, 03 Jun 2025 13:42:57 GMT  
		Size: 53.9 KB (53906 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:50efa493d96dcd75550bed18aa3fc28a2ab13a51e17a4742691427738465f45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158856998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce0bfe9d13c472866e94933951f1e2d64c7926f9aad84405f7386b76694a5dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=17
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=17.5-1.pgdg110+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:12052fdf3ab2e6e9fdb28b8a21b88f649fc9d652cf2290c0d091eadc22d4fb91`  
		Last Modified: Tue, 03 Jun 2025 13:42:18 GMT  
		Size: 31.2 MB (31189200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ce2178093e91bbe36fa92bd78a2d935f1fbd2ffdae9ce90da095f181182805`  
		Last Modified: Thu, 22 May 2025 17:03:51 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d499b1aff5e6fbb87664315f69bf1da64e1bfa5a208375c0ff9ee32c1a2503f6`  
		Last Modified: Thu, 22 May 2025 17:05:59 GMT  
		Size: 4.7 MB (4719698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d337e7cd0a5527c560a7a65a6486368d4527f868434c1ca8f5cfacfc603aba4`  
		Last Modified: Thu, 22 May 2025 17:05:59 GMT  
		Size: 1.4 MB (1449315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f03a05609aa911841bfa559daeaa8d6ab59d69887a696cd78e3cce6c0b567f0`  
		Last Modified: Thu, 22 May 2025 17:06:00 GMT  
		Size: 8.0 MB (8045907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741a3d0fbd46ba166601af51c20d66039e92b2cac0f05ab10213a10d2199e8f1`  
		Last Modified: Thu, 22 May 2025 17:06:00 GMT  
		Size: 1.0 MB (1028914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64a7e4cc2b3ddf77414f45b3a5c7f8336c6eeebaa5807a7eba4a7ae1dd4b072`  
		Last Modified: Thu, 22 May 2025 17:06:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f345711edca87cc76c4fe7f971736fa8faef235c04952d30aa9fb2b6ecbae06b`  
		Last Modified: Thu, 22 May 2025 17:03:52 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a55ce44455b81707b8d236599d9a5be77461379e2002d583a4b826a0c0a75f7`  
		Last Modified: Thu, 22 May 2025 17:06:04 GMT  
		Size: 112.4 MB (112402840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17118d04a0f69bb2dad36a6fb94ceab1627c7fd58ab2ea03fade8acf8e90ccda`  
		Last Modified: Thu, 22 May 2025 17:06:01 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99e2b6237946e6f7ea9690ab7fbc50572523d6cb9eaf73d04a3e94b5029caa1`  
		Last Modified: Thu, 22 May 2025 17:06:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ec2334fe1371d00f13bf98d0bfd98e9b247d74c9a55e15cc881684669b7275`  
		Last Modified: Thu, 22 May 2025 17:06:02 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470f630e77fd826c300e6b93783b6f60531624b3a324a71873104e61cea24644`  
		Last Modified: Thu, 22 May 2025 17:06:02 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c2abe6fec8a0dc677827dccf5285a17ee10b1eaf691e6f47de277cd6aaac67`  
		Last Modified: Thu, 22 May 2025 17:06:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:e0b3015aa40f89d13311e4089612704a49a81d711dc8e21c545e18e4df9cca32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6163763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb1a7a20ad774ff6f4cb7b287fe21847d75b67a1492bfa813d0505e3a062f7c`

```dockerfile
```

-	Layers:
	-	`sha256:dff3cea7a334b8dfe6f8974602ebf6e7b0a9fcff1741013323a5f1ca174c4d50`  
		Last Modified: Tue, 03 Jun 2025 13:49:18 GMT  
		Size: 6.1 MB (6110163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c381bf2993f131083ac20fcce468be6d00fa7d0eee25ac2675ccef1a9838a9e`  
		Last Modified: Tue, 03 Jun 2025 13:49:17 GMT  
		Size: 53.6 KB (53600 bytes)  
		MIME: application/vnd.in-toto+json
