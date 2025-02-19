## `postgres:17-bookworm`

```console
$ docker pull postgres@sha256:0321e2252ebfeecb8bc1a899755084d29bce872953e1a5a3e25ec0860b739098
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

### `postgres:17-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:e366371d957315076aa46904bbbe3b6a6c2069b5ffdb8fb39d07d25e8f995389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156263153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14b06b9a915a9d6302604c62aeaeac38fae1621197e6daefde4b0a59f8dc4af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV GOSU_VERSION=1.17
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV LANG=en_US.utf8
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_MAJOR=17
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_VERSION=17.3-3.pgdg120+1
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Sun, 16 Feb 2025 19:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 16 Feb 2025 19:03:06 GMT
STOPSIGNAL SIGINT
# Sun, 16 Feb 2025 19:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Sun, 16 Feb 2025 19:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559c5c599163f79ec995d9f59063e1509ba28566dfd31cc692308a65505789b7`  
		Last Modified: Wed, 19 Feb 2025 00:29:08 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4553993e7797ccf223ab029a4899ab10f2a981d707224156097fb052e015f6cc`  
		Last Modified: Wed, 19 Feb 2025 00:29:11 GMT  
		Size: 4.5 MB (4533721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ad38ab49c16e366b1331264ddb83bf69e474411d49f86627db21c2dbc22be8`  
		Last Modified: Wed, 19 Feb 2025 00:29:16 GMT  
		Size: 1.4 MB (1446676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f2363da6dbaf842ab8d172be663f64e95e499992b2815add724224c7f2ea77`  
		Last Modified: Wed, 19 Feb 2025 00:29:20 GMT  
		Size: 8.1 MB (8066266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc773e0cc792cddab6c2401d4e86381b75926b93a208541665f29088addfb37`  
		Last Modified: Wed, 19 Feb 2025 00:29:11 GMT  
		Size: 1.2 MB (1196053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91393204ae5499709bb5ee91480aeb41003edb002af7a3e21cfec9f3b20bab75`  
		Last Modified: Wed, 19 Feb 2025 00:29:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0311d3bf51b30b32ddabb7bac21f10281f57572a1099b9e50b3ad957757c58c`  
		Last Modified: Wed, 19 Feb 2025 00:29:09 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931e444b6b99ef3aa95f8cf8aaf7312ffb10ac5f918484499721b5df3e9139db`  
		Last Modified: Wed, 19 Feb 2025 00:29:20 GMT  
		Size: 112.8 MB (112787582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de06291fc41fe9fe418810456efcb390deaad9a7b302f50f03379963a0cef7e`  
		Last Modified: Wed, 19 Feb 2025 00:29:10 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9512881cf4c2c06f357ef47ab3ed9c5d5e7594a4c0e8860f13965528d43669`  
		Last Modified: Wed, 19 Feb 2025 00:29:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a608baae1e5ca0600856c49c4addd29ff4ddc8fa95e216059a25059d2bfb40d4`  
		Last Modified: Wed, 19 Feb 2025 00:29:09 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91befecb86a303c2142a5ee22bf55bbdafc5e44ee0213d91a706759e029a0c21`  
		Last Modified: Wed, 19 Feb 2025 00:29:08 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da49c2b3211983c57ef7e34dc1f63afcb4e6a25842cde70a313407fea120a74`  
		Last Modified: Wed, 19 Feb 2025 00:29:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:13bb8eace4dec0f9dd735535fc5194038f66b8bdd1944a1505b36bf01ccd5ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5873313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc49c282c79d4f1e89e911444534de267f3fa648a9838809b5431bb49fcbbfe3`

```dockerfile
```

-	Layers:
	-	`sha256:63599b9046fbcda31047faf19f3b349601a097617a7c18149f06990d4d23dd37`  
		Last Modified: Wed, 19 Feb 2025 03:08:53 GMT  
		Size: 5.8 MB (5818627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdea695d28aacc29c2eb1ceafc882698bf3219d833861f50ed4f55d5b97e1dd9`  
		Last Modified: Wed, 19 Feb 2025 03:08:53 GMT  
		Size: 54.7 KB (54686 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:ef22462499bc2b6ff5ccc2b79f48a3bb6a44f8be15b072f9830bf0b16b5b4aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149337860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44599ef05f5d6dcad50d48d837bd53a0c0c21f4541b8c14343dff080bfaa7e29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV GOSU_VERSION=1.17
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV LANG=en_US.utf8
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_MAJOR=17
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_VERSION=17.3-3.pgdg120+1
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Sun, 16 Feb 2025 19:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 16 Feb 2025 19:03:06 GMT
STOPSIGNAL SIGINT
# Sun, 16 Feb 2025 19:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Sun, 16 Feb 2025 19:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742af0a1ef0cb733993ec27fe9feaceb34ba6723afd02433bfb4cd412c081a13`  
		Last Modified: Tue, 04 Feb 2025 18:42:30 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc075b5513d9db4e2edde77ae7cf969395dcfa0560bdacde2bd49c12f0c6e9d`  
		Last Modified: Tue, 04 Feb 2025 09:13:52 GMT  
		Size: 4.2 MB (4150942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b1e8aeb2f8c6a35a98dae5d0f2202283ad606311b0afc193d7298b5c0f88f`  
		Last Modified: Tue, 04 Feb 2025 14:30:17 GMT  
		Size: 1.4 MB (1423868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434240560d86a443bac6c28829234e6f21d0a15cb74a15283876e0456fa1c549`  
		Last Modified: Tue, 04 Feb 2025 09:21:54 GMT  
		Size: 8.1 MB (8066390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541074b6c0b843747b56b494bdf09b14f1586bb51895be90b29da2f5e268ef35`  
		Last Modified: Tue, 04 Feb 2025 10:51:41 GMT  
		Size: 1.2 MB (1194860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c20dc858eab07cef9b3731e38eee94b094574ee1fd00b32d7349ebc62b22b5`  
		Last Modified: Tue, 04 Feb 2025 10:02:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307ec8b3a3d1c80009eee74fde9cf388e300f4a2dd3f47755ed51a7ce17f9be0`  
		Last Modified: Tue, 04 Feb 2025 10:02:46 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75adbf578b668a7ecfb1b2fc3918dd2f969bc7b5bdf0228e09012f299a759ebe`  
		Last Modified: Wed, 19 Feb 2025 00:52:52 GMT  
		Size: 108.7 MB (108744690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff14667b1bdb65ca77badc4e00c3240f484ac9e691044e918bd593b20666e596`  
		Last Modified: Wed, 19 Feb 2025 00:52:27 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a807883c83b501464af08a57f16f1c6c56d78a1211e8d8c08678e99a6f7512e5`  
		Last Modified: Wed, 19 Feb 2025 00:52:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a978670d2b8c3d7c2005446097569b7ecd246778884a220a151d6c8f43bea396`  
		Last Modified: Wed, 19 Feb 2025 00:52:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643476bbe69ac34c0e6e610643407b000bafad59d528ba7a7f8b03ad5c7d8392`  
		Last Modified: Wed, 19 Feb 2025 00:52:27 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ea84369abfc6af4fa009c75564bb8ca2f6314205417fbe9b199c53e61f3fe2`  
		Last Modified: Wed, 19 Feb 2025 00:52:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9c60cf6f1dd96881fb780d1d806ceed40f2965caa12d57e8f8fea398b6b880c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722ac1f365c73e0864e7925c8f822959bb54f375944f7179997c9764d767b941`

```dockerfile
```

-	Layers:
	-	`sha256:1669d00293347d44a309a222ee2b6a8ddba55e0c502cd5f0586d0252ce4d8fbd`  
		Last Modified: Wed, 19 Feb 2025 03:08:56 GMT  
		Size: 5.8 MB (5836300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f62e10cdcc0f2cf89a56dc480b1d3d9b9852c10de9b7f84f6b1caa19cf12089`  
		Last Modified: Wed, 19 Feb 2025 03:08:57 GMT  
		Size: 54.9 KB (54922 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:803e411de25042218b7f9c2db82ba9d888c871fcf107e6beb0935bc1801fa3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144313056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0729856f07355ac288a5b29add45e4f3aeaa0e21ea347acfa2414f6131b58a2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV GOSU_VERSION=1.17
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV LANG=en_US.utf8
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_MAJOR=17
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_VERSION=17.3-3.pgdg120+1
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Sun, 16 Feb 2025 19:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 16 Feb 2025 19:03:06 GMT
STOPSIGNAL SIGINT
# Sun, 16 Feb 2025 19:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Sun, 16 Feb 2025 19:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 05:01:17 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4160ace9f92ccb86a2f055c83f2350ae4f128bf7546d97180475062b0392537c`  
		Last Modified: Tue, 04 Feb 2025 12:03:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b16ca7dd1d34fb02108acef5be0088628ac85a8656103749e342cdee10c5f5`  
		Last Modified: Tue, 04 Feb 2025 10:06:45 GMT  
		Size: 3.7 MB (3742574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da802654af607c599ec3fd003e4267ed7c4458ca46279c31b74cb95c282ce66`  
		Last Modified: Tue, 04 Feb 2025 09:21:07 GMT  
		Size: 1.4 MB (1413611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0bf702446ac76dd0fb0911a2bb11f2483e07ee49e6155aecd89120ff047ed1`  
		Last Modified: Tue, 04 Feb 2025 11:18:25 GMT  
		Size: 8.1 MB (8066264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e719717d5becddbdfc8be96b67452998be56682c1d0930816c27846332fd92d`  
		Last Modified: Tue, 04 Feb 2025 12:16:32 GMT  
		Size: 1.1 MB (1066956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11736829b405c25ec80ca3b6e30d66d5588b0fc6334eb1c3e033c7f0b24bf25`  
		Last Modified: Tue, 04 Feb 2025 12:30:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7338d4e409e568286e0b6f6fc5e701d3e82ed0491a4b6dae12f0b5abe181ee`  
		Last Modified: Tue, 04 Feb 2025 10:06:56 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76eab10cfd81cd8f6f2e505667f3145697edc0caeda74d97e0e2f62bf67386a`  
		Last Modified: Wed, 19 Feb 2025 00:50:03 GMT  
		Size: 106.1 MB (106088554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f1e8bb1ecbd5972b0567d24677c245a62841b550bdc275b6d05ab4c5c7cd10`  
		Last Modified: Wed, 19 Feb 2025 00:49:58 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4d52631c1fcf0d4d77f64ea336c571a4d48c56c2b3e50214ae2f784bb272d9`  
		Last Modified: Wed, 19 Feb 2025 00:49:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228728e860ed745ab68660a25eed9e50bd0fcd47e76b44be5bb7a586f4515b60`  
		Last Modified: Wed, 19 Feb 2025 00:50:01 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897c1f7f23d504f4a25694e8cb70d58fbef47a5f8c673d06c612c730bc3b36db`  
		Last Modified: Wed, 19 Feb 2025 00:50:02 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1a5bf282134c1ec1e13818abacb8fe4ed965ab1aa00a6a1322f938e05f83f8`  
		Last Modified: Wed, 19 Feb 2025 00:50:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e7041e6dbf73db006cf1f221381cd45b442d0425b5fa6cdedc854c375b973a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5890793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b080e9cec50bf04e4f245b7243a7899e028f777ad9d7ed8855d8044a872ebc65`

```dockerfile
```

-	Layers:
	-	`sha256:dcac6610602792b25c826e55f2174ce8a1bf1de05175b5e92db35050b48d6e3b`  
		Last Modified: Wed, 19 Feb 2025 03:08:59 GMT  
		Size: 5.8 MB (5835871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:428589ed41fb0ae6cbe56532ca2901c0ebdc23d2ce7c877153d77c42490d674f`  
		Last Modified: Wed, 19 Feb 2025 03:09:00 GMT  
		Size: 54.9 KB (54922 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d25854a1a9a541873f53087dd4be554219f22074eeabb892505fb9537b482504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154097526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fcc2851c484229deb2ae18b978fdfebae44cb01bd4d767e19e3f397e057e734`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV GOSU_VERSION=1.17
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV LANG=en_US.utf8
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_MAJOR=17
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_VERSION=17.3-3.pgdg120+1
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Sun, 16 Feb 2025 19:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 16 Feb 2025 19:03:06 GMT
STOPSIGNAL SIGINT
# Sun, 16 Feb 2025 19:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Sun, 16 Feb 2025 19:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3573814a3a245bd9fdb362d70549e3fcd553e868459dcf1406964224d1a3a272`  
		Last Modified: Wed, 05 Feb 2025 02:21:00 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfa6399358c4e4d3d3f430502b9c0ef105d0771c6c45891cc135b32fbfdfb74`  
		Last Modified: Wed, 05 Feb 2025 03:07:33 GMT  
		Size: 4.5 MB (4499084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1745f39c82f519598952dd6ce6a52ea7fb9e01b6640374a4032f2113b5e7b8eb`  
		Last Modified: Wed, 05 Feb 2025 02:19:25 GMT  
		Size: 1.4 MB (1378706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bf67ebea6c4bddab49b1eee6630ddf6566937a549adebed7540c53ef08a4a0`  
		Last Modified: Wed, 05 Feb 2025 02:21:06 GMT  
		Size: 8.1 MB (8066314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b54767ab631fc972a1a76e6ac949bd2db2cf49b059ce9b2ffd8a6dd2919b64`  
		Last Modified: Wed, 05 Feb 2025 03:07:37 GMT  
		Size: 1.1 MB (1108700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697baaa59bd764b6e3c460a7fcc1f3febb29c80d33dfc4eae6f4d2185541b98b`  
		Last Modified: Wed, 05 Feb 2025 02:21:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fff65a4d40452b3dfb44a7c16334cc2a06def1b9b6a440506df76258bf2e34`  
		Last Modified: Wed, 05 Feb 2025 02:21:10 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f416e9655d3f00b3863707ef6ff8849fcf46d7aeec7df7734b588d1e933f70b1`  
		Last Modified: Wed, 19 Feb 2025 00:36:52 GMT  
		Size: 111.0 MB (110983290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3654f8a95e774edc4ad408f37ea556e7f71625ca3d63b6fe1fdc48072b10a1`  
		Last Modified: Wed, 19 Feb 2025 00:36:28 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03a0964e5a990fa60ec0373231eab24e9b84465cb0d5b4da676e0e5665e18dc`  
		Last Modified: Wed, 19 Feb 2025 00:36:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9c995badb65e849f16e6c837201edc97df090cfe629c698796bd5f24cca579`  
		Last Modified: Wed, 19 Feb 2025 00:36:31 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e23b8ea54fbeb70d2656f7f702a8601be6159c3cf738f20e7f670cc32e87bd1`  
		Last Modified: Wed, 19 Feb 2025 00:36:31 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62c80cae3a7728810f41ae51e15577566cbced286c907881a92b4c05ba84983`  
		Last Modified: Wed, 19 Feb 2025 00:36:31 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:906c8b2039fa002a7c6047c5932596256f4afde7014e1d02a57b16d45f7c4ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5879969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84515e40f3bca433a4ff96b553581d84bb0c8add847d6794dfa0cd7ab184b66a`

```dockerfile
```

-	Layers:
	-	`sha256:fea3e8b962241907f32138a96d6f1120b74c8629ff027614f9542965a8086cce`  
		Last Modified: Wed, 19 Feb 2025 03:09:03 GMT  
		Size: 5.8 MB (5824990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60f5871a46af93927081f8d3f365c3eb3db7e6fcb4b236904f72771ceac33cd4`  
		Last Modified: Wed, 19 Feb 2025 03:09:03 GMT  
		Size: 55.0 KB (54979 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:430d990606d18a097cbd46dc06c9be036e8c6c506c8f66aeeb8cf484288f236a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165187437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a888f2e66338532d03f3951297a8f465b65bd94e5a858b3a84e0a7a710e3b57a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV GOSU_VERSION=1.17
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV LANG=en_US.utf8
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_MAJOR=17
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_VERSION=17.3-3.pgdg120+1
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Sun, 16 Feb 2025 19:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 16 Feb 2025 19:03:06 GMT
STOPSIGNAL SIGINT
# Sun, 16 Feb 2025 19:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Sun, 16 Feb 2025 19:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c539282102661a4e7e726481590dafa7ef9954e78e49184eac4f52e20aea5d`  
		Last Modified: Wed, 19 Feb 2025 00:42:36 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d53d22694d3acee7b7f5e9404adee6f8b6953b61453218a2a97ba688a430a8`  
		Last Modified: Wed, 19 Feb 2025 00:42:44 GMT  
		Size: 5.0 MB (4965062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b446129f16b27aa345213de4dc97b4b80c27928f6506c006f38ab01ca4b2834`  
		Last Modified: Wed, 19 Feb 2025 00:42:36 GMT  
		Size: 1.4 MB (1422151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfacbf70ba5662b673d4707826a677bad703175b0e99c21fcc299239478d3330`  
		Last Modified: Wed, 19 Feb 2025 00:42:37 GMT  
		Size: 8.1 MB (8066301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e62be32bc7fe2ab62040e33a46aaf9a919d80d39acb77e06f904f194df4307`  
		Last Modified: Wed, 19 Feb 2025 00:42:37 GMT  
		Size: 1.1 MB (1137178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64747506108b82f24b6d6e455ed87e140a55980a58a701eb6891ee7589cbf6c`  
		Last Modified: Wed, 19 Feb 2025 00:42:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69247edff47fae2f85edb3f35cefdf38017c7732298b8056774acdc75cd05418`  
		Last Modified: Wed, 19 Feb 2025 00:42:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803e00f10f569f5dce34d8491b11067b62ecc4eb60543f47da77e8f8d50ded3f`  
		Last Modified: Wed, 19 Feb 2025 00:43:02 GMT  
		Size: 120.4 MB (120388723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da95d30e9ccfba44c059ffecf61601bf17e170548814cc49c5305cf500a4cf2`  
		Last Modified: Wed, 19 Feb 2025 00:42:37 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b369d9f52e4cd3935fe9aec62e6ff05ef2c81ce66867e8e0e94971216ca61c`  
		Last Modified: Wed, 19 Feb 2025 00:42:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acef75be99cfbc4e7e9296225b6f6e6a66bee30b453c19b466d57838af27692`  
		Last Modified: Wed, 19 Feb 2025 00:42:36 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f6bfc18fe70055d1ccb05323ff4d16540a0160ca547af144bbff12e997e948`  
		Last Modified: Wed, 19 Feb 2025 00:42:37 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7109a95701f87625c08c1c9be98588b30a55a2f42ab0237451dd857892c6ae5`  
		Last Modified: Wed, 19 Feb 2025 00:42:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:3dbd1858572de7ed26471193d27383673671ffdc42ae7c38eab060cfb69be8ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806ba0b8aefb705fedf5c5692cb2e584cd6357085709365ca9b303af9fbc2f3b`

```dockerfile
```

-	Layers:
	-	`sha256:8274f5ce39fe8a8730cda49b8285803f6a5ad6a64cbcb7e2724dc69864b8cf2d`  
		Last Modified: Wed, 19 Feb 2025 03:09:07 GMT  
		Size: 5.8 MB (5834312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68fff2152dfebbf23261ce485f4bba20396b236287acee84020b5ee84e63127`  
		Last Modified: Wed, 19 Feb 2025 03:09:07 GMT  
		Size: 54.6 KB (54623 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:9cb2f2488a45164573f520e126c34ddb55c8d330767333e6e5c7df23df22969b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155119554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233476f56c8595ecb02711673248946526689e0b50a9442a0a391c30d9c73b13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV GOSU_VERSION=1.17
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV LANG=en_US.utf8
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_MAJOR=17
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_VERSION=17.3-3.pgdg120+1
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Sun, 16 Feb 2025 19:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 16 Feb 2025 19:03:06 GMT
STOPSIGNAL SIGINT
# Sun, 16 Feb 2025 19:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Sun, 16 Feb 2025 19:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7719e8dd642635cc80cc6a9201e3e12b43c5f81b8b96b4826617eb3a26ef6296`  
		Last Modified: Tue, 04 Feb 2025 20:03:44 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb1203be53afacdadc0f86ebda1b96bdf67fe99f6d6b9312982859db9ddc62a`  
		Last Modified: Tue, 04 Feb 2025 19:03:40 GMT  
		Size: 4.5 MB (4475093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ad73e52814e3b5584157bc395cc6e78a6e29ae72deb1f0b28c57ea4a88b45`  
		Last Modified: Tue, 04 Feb 2025 18:19:06 GMT  
		Size: 1.3 MB (1333770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f690f3824ef93097d65c0de409702fe1686f77be8b24f9fad85c2958516e1aa5`  
		Last Modified: Tue, 04 Feb 2025 19:03:42 GMT  
		Size: 8.1 MB (8066470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bc420e36068670a1196d49557b6cd53eee48327c745a919656afa4d3f2a1a2`  
		Last Modified: Tue, 04 Feb 2025 20:03:50 GMT  
		Size: 1.2 MB (1182594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bff00c1df4e776710c790789bb6291046ed640138fb8637f289fdbd789ac820`  
		Last Modified: Tue, 04 Feb 2025 18:19:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b8bad5a58592332fd97ab300c9375cabad82d5f47ff89fcfba0bd8319bda0e`  
		Last Modified: Tue, 04 Feb 2025 20:04:45 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429e373999ee702b11e5d8bd91eea9ca36db4d258dd029ca9b9cc34b20e76949`  
		Last Modified: Wed, 19 Feb 2025 03:09:51 GMT  
		Size: 111.6 MB (111554481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908aa695758de189235fb720533de21b730e6cb53986f84e26371fd2c0a3c551`  
		Last Modified: Wed, 19 Feb 2025 01:42:01 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e32cfde9ba8baa2bf2255957485977e6b75dafe3cb6f8d4a29d77a8c383a6c6`  
		Last Modified: Wed, 19 Feb 2025 01:42:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d5d584765f2b2efe180bbab8c37e29fbb45f1542639c6b931bccef82b091a3`  
		Last Modified: Wed, 19 Feb 2025 01:42:02 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1133d109076cea4fd504f7166775ab62394c6d116d1be8a383ad872f83825b6`  
		Last Modified: Wed, 19 Feb 2025 01:42:03 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e036c283984af03b8ae8ac9294ae166ee66849a0b181f18152b01441048bad`  
		Last Modified: Wed, 19 Feb 2025 01:42:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:eda5eca9e56370018a2a10312acb7c8c9d75b13445583b3a650a12d3e1491bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 KB (54589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffdfb5409a020b722d45396ce6b56766ac99637f7430792d0a1509b4495f24d`

```dockerfile
```

-	Layers:
	-	`sha256:26c391512eb88173bf20c017808f69a131beebf42169d077430b7658b562306f`  
		Last Modified: Wed, 19 Feb 2025 03:09:10 GMT  
		Size: 54.6 KB (54589 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:b1f7d4e5de34bf129fba257bfdfab79d762e37ff95f6336930505ac20953daf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.0 MB (169039023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b1d98f64a1b9f066fcdcd9c10c669d179d4eafe3ce1ec6b7acacb9299ed6ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV GOSU_VERSION=1.17
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV LANG=en_US.utf8
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_MAJOR=17
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_VERSION=17.3-3.pgdg120+1
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Sun, 16 Feb 2025 19:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 16 Feb 2025 19:03:06 GMT
STOPSIGNAL SIGINT
# Sun, 16 Feb 2025 19:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Sun, 16 Feb 2025 19:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbf715dc59c916c67ca487e709f97dbe5eeb7cae5caac2a42bd73370ac369f2`  
		Last Modified: Fri, 14 Feb 2025 00:10:21 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bd5d0cbe21b3822fe6a1d049d807c51ab70c6c9b8102a4ce98729e7766310a`  
		Last Modified: Fri, 14 Feb 2025 00:10:21 GMT  
		Size: 5.4 MB (5368250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f099fd57534434ea1c4855bcde0da5e3c50c776b8378a491830c26d4859588`  
		Last Modified: Fri, 14 Feb 2025 00:10:21 GMT  
		Size: 1.4 MB (1368700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b61f767fca460546da86f43eab207e9c91299f1b9cbb82e8e8f0a247015cbd`  
		Last Modified: Fri, 14 Feb 2025 00:10:22 GMT  
		Size: 8.1 MB (8066426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a1badedf5ab9eb6a6950176d0f9c4b6d13aac71b48a8bb30e861572c5b3152`  
		Last Modified: Fri, 14 Feb 2025 00:10:21 GMT  
		Size: 1.3 MB (1283559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e12544d44251ca7d34a3c4bfca54895721ac388529eaa3fab78f9f1b0669a04`  
		Last Modified: Fri, 14 Feb 2025 00:10:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3730f4c3688d29b903641f1195074a06319713fb1dc8d85e62cb00f4d69a21`  
		Last Modified: Fri, 14 Feb 2025 00:10:21 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5fc2f86e0e67deaa1bd297c7cfafa0fa385fbfc085ac1693254e7da2f3b50e`  
		Last Modified: Wed, 19 Feb 2025 00:32:03 GMT  
		Size: 120.9 MB (120886747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbcba35f5bcef9dff568181d75bee027edd5f5e8ea17761c950b244f555750`  
		Last Modified: Wed, 19 Feb 2025 00:31:37 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3679ccc2ce1b9e78165970456b68835ff5e622fa247f4c03c49727fc92ab1198`  
		Last Modified: Wed, 19 Feb 2025 00:31:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49725c45295fbcfe0725026725f703db0dc631f1f90ecda9e4ae7db823769088`  
		Last Modified: Wed, 19 Feb 2025 00:31:38 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbc02531b8ec5d8364df18d1db864e17839f684d2b4a3f487f94dc1501fef9b`  
		Last Modified: Wed, 19 Feb 2025 00:31:31 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4a0bf17515295763240260dcbf659cd573acd7aa50fee19208bbe2191c9304`  
		Last Modified: Wed, 19 Feb 2025 00:31:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4c48f23e0bf55e9e57eeda67e5cfa81aa944024a62bad883ded26ef0099b6cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5880653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13cef27f7a32fa6c51b0cdb35b11c2eb65c76dd5abea1e103cadafcb5fef5ec`

```dockerfile
```

-	Layers:
	-	`sha256:a93f0051ea154744f6bd75de9e3007132fd7227a172d7dfe759874e9f4e610c3`  
		Last Modified: Wed, 19 Feb 2025 03:09:11 GMT  
		Size: 5.8 MB (5825888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:173041e4ced271d33dbcb99f6bdf04d21e2e2ab5edc0352eb0a53de7162379da`  
		Last Modified: Wed, 19 Feb 2025 03:09:12 GMT  
		Size: 54.8 KB (54765 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:558e7c636e695580764b25af7a699f204d334805f8a801658f5fd4ac4cff532a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165385848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e68f5a554717cef58dd0850845a1e93b7a52848433c3b30de7764451280445f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV GOSU_VERSION=1.17
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV LANG=en_US.utf8
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_MAJOR=17
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PG_VERSION=17.3-3.pgdg120+1
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sun, 16 Feb 2025 19:03:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Sun, 16 Feb 2025 19:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sun, 16 Feb 2025 19:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 16 Feb 2025 19:03:06 GMT
STOPSIGNAL SIGINT
# Sun, 16 Feb 2025 19:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Sun, 16 Feb 2025 19:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d554aa69becc611618e57d0a1b08418992435e971a46fb711bce4b62f1e1a8`  
		Last Modified: Tue, 04 Feb 2025 09:16:19 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfb0d8a088f529612850247f584a9d256e04cbc01467c1a17a7b04ba25376b8`  
		Last Modified: Tue, 04 Feb 2025 14:02:21 GMT  
		Size: 4.4 MB (4391013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f72b9e5495ea1a46b650fcec5ef849f5fe0381c49cf458a8db80a1c46bceacd`  
		Last Modified: Tue, 04 Feb 2025 09:16:25 GMT  
		Size: 1.4 MB (1412687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3346f3cf585d2aef332f735561c4e09822978e7aeaa76c62df2976af30862f6`  
		Last Modified: Tue, 04 Feb 2025 10:03:12 GMT  
		Size: 8.1 MB (8120462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6adb1ac1ad72022f017cbb1f3c98faeb80575c8c594f54fc6fcb1b887efc06`  
		Last Modified: Tue, 04 Feb 2025 10:53:05 GMT  
		Size: 1.1 MB (1096757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd25cfae7af12635c58a31bc0da453e3fb4be036d59a67092b86e0a7178af2d3`  
		Last Modified: Tue, 04 Feb 2025 11:11:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5f77994cc25c18c297cc567fb352098c8d2c3c3b403de57a3312518b958fcb`  
		Last Modified: Tue, 04 Feb 2025 14:32:18 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80fe49053b8e186a6ad88d1569851c10ef8f05305a9ccd372cb8d817821b28d`  
		Last Modified: Wed, 19 Feb 2025 00:45:22 GMT  
		Size: 123.5 MB (123485741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931afcb3f8ab460f6ca34431be19774b2ff293afa1eb6427e7e35e98fb6b9a25`  
		Last Modified: Wed, 19 Feb 2025 00:44:58 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4167ee19f161ce48b76905da24f839da5793236dc2f81230f86081438dcf0be`  
		Last Modified: Wed, 19 Feb 2025 00:44:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf83e188d082649a89e4c0168288806e5fcd147b67871a72372bf8340c91b65`  
		Last Modified: Wed, 19 Feb 2025 00:44:59 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a075148df2437db8a5dffb59df1f5f2b85c835fe54ff0ce55f761d634ca5a1`  
		Last Modified: Wed, 19 Feb 2025 00:44:53 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aec4f2296040011f93d4806a2b4190ff8388a68744df1627e519a859ff0382`  
		Last Modified: Wed, 19 Feb 2025 00:44:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d6bea2d15f2cc761bca14bebf39de48b6dc7561201946b9e1c5f0aa3c0ff63c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5872596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35992555492b8faa80ce5cfb9cb191d9c55503cda397fe4d7ab565e2dcdc39ff`

```dockerfile
```

-	Layers:
	-	`sha256:1378d3e56fd7f4cba8e005e0b550d4b5f51d3258d875b46a720414421a34e822`  
		Last Modified: Wed, 19 Feb 2025 03:09:15 GMT  
		Size: 5.8 MB (5817910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49943fdba35134b601984cf87cbd6df7ee3051a358a50c703109f7b95f39c97f`  
		Last Modified: Wed, 19 Feb 2025 03:09:15 GMT  
		Size: 54.7 KB (54686 bytes)  
		MIME: application/vnd.in-toto+json
