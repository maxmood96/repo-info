## `postgres:bullseye`

```console
$ docker pull postgres@sha256:8b01d4bd7ae45900bdcd620fbae1f48d6c33c9d573907bd4c544b54efe05f14f
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

### `postgres:bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:5e1ac38b42a93aeeab0c141bcadc5c7da84704c92d2095f615bb6944ecb6b735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150370561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af4a8325a624137d29c269c48150037cd38f8d3957bc09d945fd4b6fbf435d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:16:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_MAJOR=17
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_VERSION=17.2-1.pgdg110+1
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:16:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:16:44 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:16:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:16:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade5832a61de100831d0292e97e73e06259666cbfd10e0b7eb02d842f2af813c`  
		Last Modified: Tue, 14 Jan 2025 20:33:41 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba71be4544833c550e0094754ed6de86e7078289e5181a5e5a25ac51d8a6a314`  
		Last Modified: Tue, 14 Jan 2025 02:17:14 GMT  
		Size: 4.3 MB (4308235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29bcfb68598fd1e345204137c6ea47a4f7717c9a1b05b45e79b6e387b4ab551`  
		Last Modified: Tue, 14 Jan 2025 02:17:14 GMT  
		Size: 1.5 MB (1472242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa718e31413d779f1060693a49f9ce5e98fc50e9184cde05952fb9c84337317`  
		Last Modified: Tue, 14 Jan 2025 20:34:07 GMT  
		Size: 8.0 MB (8044525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3add1bd3baf513666874e54e3ec1e3ccd4fff137d454bbccbd76b81a2292bf5`  
		Last Modified: Tue, 14 Jan 2025 20:33:42 GMT  
		Size: 1.0 MB (1038330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c87ca14c59b5e1649923ba5c22138015d1eb59ae66ec103088d39dbc89ee3b`  
		Last Modified: Tue, 14 Jan 2025 20:33:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8622b5a90b1b49d6ac44a295507224001b99eadde01a13aedad68a8f9e4dd9a`  
		Last Modified: Tue, 14 Jan 2025 02:17:15 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14be60487225fd62937de2d3a27f14f64390ec5f04503e3b7d159397ad3d3c39`  
		Last Modified: Tue, 14 Jan 2025 20:33:50 GMT  
		Size: 105.2 MB (105233497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80557b2c4920e5a09048dfe322d7ca39f120fb62e057658de39906632e8d0ae6`  
		Last Modified: Tue, 14 Jan 2025 02:17:15 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95b98044025e9652117989bd80f6f8f3f543f86cf41a8b0fe4dac04a660ae25`  
		Last Modified: Tue, 14 Jan 2025 02:17:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7439aba5692a1bb408adb7814f6c528f3ff282829d77dfe3d5b41065f0ee3be`  
		Last Modified: Tue, 14 Jan 2025 20:33:42 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e277fcec9965b6fa750b6e9de6393c47c5480fcb6f1a21a2ecaaf7c229ffb9`  
		Last Modified: Tue, 14 Jan 2025 02:17:16 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b103ab32fee897b16eb0c7f153808a5791160b093e6e6cf71898a2eace6984b`  
		Last Modified: Tue, 14 Jan 2025 20:33:43 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2497041c70cbfa23b60aa724c5f2f54f93deae39c08fe823a237d0a86845b0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6087813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f41f05e4fdc02d1af774dc1eea0a6f5f8f3a915977a41687d15c29500e16085`

```dockerfile
```

-	Layers:
	-	`sha256:7716da7d2f7a52538889dd018547048d0095b6b9cb9ff8ebfbf36e98f967c960`  
		Last Modified: Tue, 14 Jan 2025 22:24:03 GMT  
		Size: 6.0 MB (6033516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26287bdc57a30ee84bdd212c1e7848befcc7a0d0fb2a68843a30cb48a3211125`  
		Last Modified: Tue, 14 Jan 2025 02:17:14 GMT  
		Size: 54.3 KB (54297 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:d00f6ee65fe25779df6f55b5a63c973b525fa79c36a122a4a509b71c621d57bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138574759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600c7f36aaba549839ac430fe08c4ecc0e6a701a291f4f8aa032cfadb2b151de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:16:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_MAJOR=17
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_VERSION=17.2-1.pgdg110+1
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:16:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:16:44 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:16:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:16:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bafc0b709fff1b657a14551940af81807048c74c63e503c511c438265ec89a`  
		Last Modified: Tue, 14 Jan 2025 22:00:25 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f975e0807809fe76bf2c4859de932ee50e6f49e947f5a1a49aad510b7684de`  
		Last Modified: Tue, 14 Jan 2025 22:00:35 GMT  
		Size: 3.6 MB (3601695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb6df2b8e257a7eda1d3c59549e23c34af700b4f6ac7656286fad61dc52de9c`  
		Last Modified: Tue, 14 Jan 2025 22:00:28 GMT  
		Size: 1.4 MB (1439249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef35b898de2c2ed26801408e41cde59d5ae6ebe8f9354ae4c2eab3de5580b8f3`  
		Last Modified: Tue, 14 Jan 2025 22:00:40 GMT  
		Size: 8.0 MB (8044364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73ef971477037a6fe33388a4295f2f293a338bca50b62cf9510bc34c9977f3c`  
		Last Modified: Tue, 14 Jan 2025 06:11:45 GMT  
		Size: 908.7 KB (908668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a7e95dea3feea2efaa0acb94dd3daae8af06bed3c1673ce2399262422fc4e3`  
		Last Modified: Tue, 14 Jan 2025 22:00:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2983901e72058651f8b788f2a7f436da5ebb614efbd37a8d48ea69113c2cded7`  
		Last Modified: Tue, 14 Jan 2025 06:11:45 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1158a84d6de5f464539a874540d1fddc7bd049d97531d8b6bbccf8108310a97e`  
		Last Modified: Tue, 14 Jan 2025 06:11:48 GMT  
		Size: 99.0 MB (99025753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b466ab3dbf71cd5af89eba49f36fdbf9e4a75ef23159552e5cf87f07ab999824`  
		Last Modified: Tue, 14 Jan 2025 22:22:50 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5468916522c88ca0f514823dde570da6949106b31e3d5a23eb19a2092d99065f`  
		Last Modified: Tue, 14 Jan 2025 06:11:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd628516ea94d01f3f4e3c05b36418956ba232684281e43eb0ce51b1d92705d0`  
		Last Modified: Tue, 14 Jan 2025 22:22:42 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e687986ae2aad2f2aad00ece22de10f881333881612e03b0f9b861ed16cfecc2`  
		Last Modified: Tue, 14 Jan 2025 06:11:47 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59511bfbce0da5b7fcf1db062e5315e685a714e957f5ec3df1f5c4dd33142f3c`  
		Last Modified: Tue, 14 Jan 2025 22:22:34 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:f81ab68edc266881ebe5fb7ba0d0cbaaaf0a4d3b6b58fa4b2bd3aec053ed751d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6105202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8efdcf832571a81dce802007a0e5e599400d6391b47ca69e117005b1bb1a6f`

```dockerfile
```

-	Layers:
	-	`sha256:2b8f943ff71c668e3d2be0fbd5fbff53e99e9d892011d51162bb64b625e9c893`  
		Last Modified: Tue, 14 Jan 2025 06:11:44 GMT  
		Size: 6.1 MB (6050709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827405ca1aa8b13136b4db434482eeab6576f7f8512eac7c100f59f18fd911cd`  
		Last Modified: Tue, 14 Jan 2025 06:11:43 GMT  
		Size: 54.5 KB (54493 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:590b853ac973707c971344abb0ba1a9d1a4cc7571b506e2dd65b148e89a62c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147365994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58c1dcc3f0058b9624e1d66976d3d41ba92e131cbbb96c4d668efa26073c34f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:16:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_MAJOR=17
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_VERSION=17.2-1.pgdg110+1
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:16:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:16:44 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:16:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:16:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 20:33:33 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b36d302f8a9da22724b01ad3edb1d16101fab82359501ca8f1feed2fc2cd201`  
		Last Modified: Tue, 14 Jan 2025 20:35:17 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531d7f5be2b7506d5ad4b9aff5db2ac3041e805a533f4f226b0006057cbf1ed0`  
		Last Modified: Tue, 14 Jan 2025 06:08:07 GMT  
		Size: 4.3 MB (4312801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98618b8f6d5579fa5d5505874305171812cc5f23c215fd441412809fada53f9`  
		Last Modified: Tue, 14 Jan 2025 20:43:10 GMT  
		Size: 1.4 MB (1404115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8846735e7d020e5fed1640cd37bcc70daae404ce5c1d5d70cb00643286ff7cd`  
		Last Modified: Tue, 14 Jan 2025 20:35:18 GMT  
		Size: 8.0 MB (8044511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d373474bba828255b5311627514305148190e7243cf38df6346071a766d7adc`  
		Last Modified: Tue, 14 Jan 2025 20:35:18 GMT  
		Size: 1.0 MB (1026607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063c700837a47de565dffe0d6108dfac3680dd70b24434882224f9c82eb1d03b`  
		Last Modified: Tue, 14 Jan 2025 20:43:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7204c081de27f53fd775f5cd9393cefa72aa0d51587aabcfec8910197dd81c5c`  
		Last Modified: Tue, 14 Jan 2025 20:43:12 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2919df03e18a1ffff1aaa7c4861a03f3ca0a50e977a1e092e7cc63118536fb73`  
		Last Modified: Tue, 14 Jan 2025 06:08:11 GMT  
		Size: 103.8 MB (103811977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a306ce425760275fb6de4005839059455a371cac348e36e5f3151fc84fd6d078`  
		Last Modified: Tue, 14 Jan 2025 06:08:09 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422904fdb998a9b02c31c124f967adcc256d3f21d2db2cc93b5b8edcfd6e272`  
		Last Modified: Tue, 14 Jan 2025 06:08:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d548ae3a932f0382e883c7c575ef59333d582657870557cdff981a8be9e422`  
		Last Modified: Tue, 14 Jan 2025 20:56:09 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abee30ea4ec552a7ed55c135706629f55538934fb056f265200c8328b891b7b`  
		Last Modified: Tue, 14 Jan 2025 06:08:10 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669676e4911eba52d6faaf11324546a8ed147cd0b6bdfa0be6fb373834ab9780`  
		Last Modified: Tue, 14 Jan 2025 20:56:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:12e5604801e002f0e10d925ebf5bdf596bf6d81571be0d5a531559b6c16acc97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6094370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726fa4a9378fee461f2ea8437e4b671439010fa3d6d696691338906854b4edb3`

```dockerfile
```

-	Layers:
	-	`sha256:41403ba9fea8fc29abee3916b02d3183401c5bae3eacec8d8f09d5c4dad296d9`  
		Last Modified: Tue, 14 Jan 2025 06:08:07 GMT  
		Size: 6.0 MB (6039816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4fb8bc2209cdf6632edda2f662ef81c3152aaa6a152efdaf60c95ef9b3564a`  
		Last Modified: Tue, 14 Jan 2025 06:08:07 GMT  
		Size: 54.6 KB (54554 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; 386

```console
$ docker pull postgres@sha256:935518a30b755971e1decff23f0cc216999b44f1501e9bea6a46fb6054799364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158607512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910e38cb727b6cb97912946fb07e8707b1e5a1835bfda3ef120ab8443d051071`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:16:44 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_MAJOR=17
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PG_VERSION=17.2-1.pgdg110+1
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:16:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:16:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:16:44 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:16:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:16:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 20:37:11 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c069f9336ea8ba5ba4b5ae2ca79adb05cf67c503160f8523bb6614c0f722e8`  
		Last Modified: Tue, 14 Jan 2025 02:44:14 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d9ab9751868e541df33c15d32184c228e47cacc5b2f9094e134aa5c2ff4946`  
		Last Modified: Tue, 14 Jan 2025 02:44:14 GMT  
		Size: 4.7 MB (4719727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfa8cb6a6630b9d8fa90c7c2b84782a9499f650c25d90e98c0e4bfbe9bbe079`  
		Last Modified: Tue, 14 Jan 2025 02:44:14 GMT  
		Size: 1.4 MB (1447783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7ce0be4006a2a1ac0eb80faa9833ad2c3ff28e2c4a43db152d98628b357fb`  
		Last Modified: Tue, 14 Jan 2025 02:44:14 GMT  
		Size: 8.0 MB (8044461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace072bcf000c5abd37ba9e8516a874e32b96e3eeee8eb60a9930cad158d787b`  
		Last Modified: Tue, 14 Jan 2025 22:19:58 GMT  
		Size: 1.0 MB (1028908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e44ace939e1774c9e095290204cc8be92475d39b3107b28c3e3c2b992f4f88`  
		Last Modified: Tue, 14 Jan 2025 02:44:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a4e1df331f6f0f301afcd91a4342d4b4846bdf1ddb8917abcb8b5f95a82ee3`  
		Last Modified: Tue, 14 Jan 2025 22:19:51 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cc108dd6df9b85daff30ea5a3a2b32c71b4305f82a039d6b1a2d9e86963694`  
		Last Modified: Tue, 14 Jan 2025 22:19:41 GMT  
		Size: 112.2 MB (112166534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d1ac31ddffa2579aa9d7ca17d7ea2a33cdae17cf796062e6ff786454491275`  
		Last Modified: Tue, 14 Jan 2025 22:19:26 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a7637d6d575e4d24a16ace8d5e98beab4e9f5c5d841668959e2203a2662a31`  
		Last Modified: Tue, 14 Jan 2025 02:44:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d31e3b1a6934b7120cfc1c389a964c1a17c449f62f1e667b81402a5c62820c9`  
		Last Modified: Tue, 14 Jan 2025 02:44:16 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c097e218029e33c654e8cdbbc38f3c99acedc29e9ef40530a330a05f6d60086`  
		Last Modified: Tue, 14 Jan 2025 02:44:16 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79feb10c79daa32d39f8daa57a2bb2211d03341f26468bc00b9b520c9440d5c8`  
		Last Modified: Tue, 14 Jan 2025 02:44:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:9e240fa280cd065b6609cdfcc7e0be281998b1b4c6f1ae330e4f489103a2c35f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83dbf0c0db19281835a88382e581f29c6e0c8377ad7a9a82a3c51373c65ecf5`

```dockerfile
```

-	Layers:
	-	`sha256:eaf6d14f688a812f8da46989f6ee17ee563f5f6ce114dfc780525543c17b702b`  
		Last Modified: Tue, 14 Jan 2025 22:18:59 GMT  
		Size: 6.0 MB (6048471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4349153ae3514b11b349852a5f563cf9fb9172b9e955c40ba008623759d454`  
		Last Modified: Tue, 14 Jan 2025 22:18:53 GMT  
		Size: 54.2 KB (54248 bytes)  
		MIME: application/vnd.in-toto+json
