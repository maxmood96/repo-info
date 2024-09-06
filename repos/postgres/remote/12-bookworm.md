## `postgres:12-bookworm`

```console
$ docker pull postgres@sha256:593b8483912c0b2a90da0bdf7ffca077f438c855b6ef07b7e66ce7cd6c3d1bc1
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

### `postgres:12-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:f76758406b7ec6b8fb60cf898c9e47adad816cade96075b84a9aeb3babf8e196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148452983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a67825a2d5e9f8b5f6b1b8d45bb4d910cae3c7018d904bd783335e4b77eb23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15c9e971b89b505d4d7d14ca544e9cd4339f1011a8961d5c3cfd1c41a3ced4`  
		Last Modified: Wed, 04 Sep 2024 23:09:02 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc073baf5aa3abb99691e95853b577851ad1a28efc584d6f76f73c3c3b9d5a9`  
		Last Modified: Wed, 04 Sep 2024 23:09:02 GMT  
		Size: 4.5 MB (4533687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c7ebc7f571bff7f99b24cf9c3369c30ff7b5a85caf1427b631552f5476c55c`  
		Last Modified: Wed, 04 Sep 2024 23:09:02 GMT  
		Size: 1.4 MB (1446663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1788b56169fcac428e90c4a2924cef30321f1f1761d97d95446a9ba03f7d1098`  
		Last Modified: Wed, 04 Sep 2024 23:09:03 GMT  
		Size: 8.1 MB (8066299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3293521dadff479b2ede7eef70d992a101fde6ba6ddae103c08df89c69940bf6`  
		Last Modified: Wed, 04 Sep 2024 23:09:04 GMT  
		Size: 1.2 MB (1196036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36deb9fd4db6acfa45d1893e7b30010922c5c58bdf7182e0b0c4a69a25a86f2d`  
		Last Modified: Wed, 04 Sep 2024 23:09:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfec5e47ecea11ed5303efa9047392850a625d2ec76f42b00aef35b9c29ab7f`  
		Last Modified: Wed, 04 Sep 2024 23:09:03 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efd555e7681920b7451f4a90c9cd088fb63121194958f96deb76a4d83a13b59`  
		Last Modified: Wed, 04 Sep 2024 23:09:05 GMT  
		Size: 104.1 MB (104064477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bff0562b45ce5495948d0a401f7ee2a5bd141ac1ec528a1f201b72fbc2329ae`  
		Last Modified: Wed, 04 Sep 2024 23:09:04 GMT  
		Size: 9.0 KB (9017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce11c838bd1f5dfda845b1150a3d5896f9b7741be8a1611dea80fed68e7a09d`  
		Last Modified: Wed, 04 Sep 2024 23:09:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89319a4f1fde9a8a2feded9c7500510a5107dd1bcca5c7e1fbca6392a7ea90a`  
		Last Modified: Wed, 04 Sep 2024 23:09:05 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5c617ccd877ca1ffd7be92943a51d4330654f64d6d3753bd83c12c6b925223`  
		Last Modified: Wed, 04 Sep 2024 23:09:05 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4cdf1de570284b03b23946fda92cbadfffe8fc653ef15d677dbc633ae2e455`  
		Last Modified: Wed, 04 Sep 2024 23:09:05 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:54642fbd0dd6450e2ac141cd9240ac67bd66ec00d344fd58c2363500ff81b9bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5654732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b963f82e0cf12b83ce8046213bc606372dee776e30257269777f21b8f3b513`

```dockerfile
```

-	Layers:
	-	`sha256:69900ef8c66d91405cbb310392cfb4b64368e5e7dad58068f06181d80ad216cd`  
		Last Modified: Wed, 04 Sep 2024 23:09:03 GMT  
		Size: 5.6 MB (5600291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3ba14b8ea4612905fccb369c2672548f05f198de5c78091644890dd5a64876`  
		Last Modified: Wed, 04 Sep 2024 23:09:02 GMT  
		Size: 54.4 KB (54441 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:91204492a8a360982f76581cae78ae6e42f352e35eb6c5125871a91b456b8d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141166149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26bcd3965a476a37760ba022964c0dbffaae42668a35a83495b2a04652f114f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9ae4c474ed95cd628af882b052c523086cc21ddc0f24ca9b6f8eca4312960b`  
		Last Modified: Thu, 05 Sep 2024 05:48:45 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3023e0032654f8aed6b728bbe7febaffd2807f896f9f134715dc315c905eb3`  
		Last Modified: Thu, 05 Sep 2024 05:48:45 GMT  
		Size: 4.2 MB (4150914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db5800f5b661f501fdde83e66e50910fd6072841f01392ff5fd0a36aff48cf8`  
		Last Modified: Thu, 05 Sep 2024 05:48:45 GMT  
		Size: 1.4 MB (1423884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815cd609b0d2444b8d98a1915bf7cad5e755ec79d47470f84c541d7a31a1fbc6`  
		Last Modified: Thu, 05 Sep 2024 05:48:46 GMT  
		Size: 8.1 MB (8066403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a7cb2e0c74c89d4f114cd0a22f9d61d3e0ab92973ef09055b2bddf249bf984`  
		Last Modified: Thu, 05 Sep 2024 05:48:46 GMT  
		Size: 1.2 MB (1194866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b70053bc41f4c2a8d0d5a7da4aa763d1367f13f8a570840911645523f2a15`  
		Last Modified: Thu, 05 Sep 2024 05:48:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be49688ae1ba33a431c4a7bc035a0f29ffaff6c7c9bc16bd0dea362b144f6c74`  
		Last Modified: Thu, 05 Sep 2024 05:48:46 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76f9434ebd0dac2061640477ac0ab980cf9b9377d5e477a10682e9cca15fd5`  
		Last Modified: Thu, 05 Sep 2024 08:23:06 GMT  
		Size: 99.4 MB (99423318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1d390351fde07a43aadb83f5fdd561452d1aa3a32e0e1ed2e49b417b29c727`  
		Last Modified: Thu, 05 Sep 2024 08:23:03 GMT  
		Size: 9.0 KB (9026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c47d24fa29fa783e60a63fbd50f2d3c75e56ab19ff74f3a1a612b6c33ea20b`  
		Last Modified: Thu, 05 Sep 2024 08:23:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495d4060b19d30a3456ccd722f7eb2951a3c1ff1507b5e54d545d86ae6fe103f`  
		Last Modified: Thu, 05 Sep 2024 08:23:03 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1f257a2eeb0f3f7071a0bb7a3d3459ea7cf21dc6dc70396ab270d2bee671e2`  
		Last Modified: Thu, 05 Sep 2024 08:23:04 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639480f21ffc48d71cee09f0e5870f56e3d7b31d1089e23df67afa055f37e54`  
		Last Modified: Thu, 05 Sep 2024 08:23:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c170e230975615516a208fbe72e093d4731e116ae51b2e7e5f3753bc073f012b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5668326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366429710a38f4c75774fc958265b3256b7d126a127127430f24ec1bc51c4873`

```dockerfile
```

-	Layers:
	-	`sha256:904af46e21ead32c7e272c8abb51029768cf781e0000c10d082627a0a5dc2ede`  
		Last Modified: Thu, 05 Sep 2024 08:23:03 GMT  
		Size: 5.6 MB (5613679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178a534a660b2894c827c9d4bb2e1f46450a155b8aa15e729433497a04831942`  
		Last Modified: Thu, 05 Sep 2024 08:23:03 GMT  
		Size: 54.6 KB (54647 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6066d8c423db4e1e7ca037e7a00643520c39dad1280ebd3fa18716bf96822336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (136009996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465c639bf9f08ae89be87c3694fdc92e999e90e9bd4d934938bf73f79ccd6a44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50662b3d2205bfde48c7c7ee492df609b20867a450a872a8e34fae1467209e84`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bccbd6b6c11095d20b4078ffe578897cefad73d15b33fc0a3eec8093f041eb2`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 3.7 MB (3742532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f537b63140972adb053d00e6965e0d19ac96f9fcf53cc647875e3499d7e072`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 1.4 MB (1413612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818684dea80d219b3b50b12b97fd00572b2325ae91d47de8905c8fb5a0ddd9d4`  
		Last Modified: Thu, 05 Sep 2024 06:53:30 GMT  
		Size: 8.1 MB (8066297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efebd8ca0e3760211b0743352214ceaf97423c6db72d91fe0c68e34edb58328`  
		Last Modified: Thu, 05 Sep 2024 06:53:31 GMT  
		Size: 1.1 MB (1066972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3b1200790e6e3387c0d7caaadab6f6b8ec7d7b34ec10f50f3dea452ba6b39`  
		Last Modified: Thu, 05 Sep 2024 06:53:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01488d49e7609eeb21c76d857556114a92d131aa883ce884d9e9bb1b7f8b9955`  
		Last Modified: Thu, 05 Sep 2024 06:53:31 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e18b8126553ff8270cd6c9fccfc6e0d582c963064518bb420a5d330fc592cfb`  
		Last Modified: Thu, 05 Sep 2024 09:22:18 GMT  
		Size: 97.0 MB (96982972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b6b2b8090753ff49cf3369fd2710787ac23209233a67b775469c300f7dd531`  
		Last Modified: Thu, 05 Sep 2024 09:22:15 GMT  
		Size: 9.0 KB (9026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea96745f876203469e6cfcaf561c8e0e6a25edea59195ae1fc30b13b341d6947`  
		Last Modified: Thu, 05 Sep 2024 09:22:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e78725739b209356ce5faffd1b3c61473d965f4284baa1d03d5eb51ac6af30`  
		Last Modified: Thu, 05 Sep 2024 09:22:15 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2a73fe1635a0c81310182c9b39d6307e7cd72e83a6c2a3bfded05349699cde`  
		Last Modified: Thu, 05 Sep 2024 09:22:16 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896482cf44420a4889dc3c3940fc6a8fb9d05413d67fc839b35f272a8c30cc19`  
		Last Modified: Thu, 05 Sep 2024 09:22:16 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:304a83d8a4e60d58a5975bcc6b4a91f80e538d1c0993c72f9b2dc529e33f4c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da188d494400ec9814760e0ccef4d37d6d1a677d584df2a70f5087d48def0ac7`

```dockerfile
```

-	Layers:
	-	`sha256:b733420c9a736dd4e8ec7f65bbdab07a21ab4d7c7db33414d1b5d56ea69c99f4`  
		Last Modified: Thu, 05 Sep 2024 09:22:16 GMT  
		Size: 5.6 MB (5613348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:367448f92cc933179c378f2065fcec847d452238c1ce0e8278453c637fd343ed`  
		Last Modified: Thu, 05 Sep 2024 09:22:15 GMT  
		Size: 54.6 KB (54648 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:a30086b2224c56181d78b816487f52baffb3a59f2f0e91567931cc360dca75b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146673981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a10e152bceca7078ee5ef708d085868f7159506377f994369e16ed1fddade93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b660189dd276eb885d178c6dfaef70c35e25a3e79e4875706ee64843d5113597`  
		Last Modified: Thu, 05 Sep 2024 16:07:42 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb679f354328bda5f84258d244bea33d7a11c4702b2e394a087a8a26655ec986`  
		Last Modified: Thu, 05 Sep 2024 16:07:43 GMT  
		Size: 4.5 MB (4499176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad02a42a28780a296f5fe31bbc1a1b25cfe25a8a8790ff418d967f1397f3a73e`  
		Last Modified: Thu, 05 Sep 2024 16:07:42 GMT  
		Size: 1.4 MB (1378738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d0f50cfb107989df975c183f12c532d5ad4c4a481ce423726cea7696559966`  
		Last Modified: Thu, 05 Sep 2024 16:07:43 GMT  
		Size: 8.1 MB (8066331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb116a8fa5afd487f740e826706bfe92d368f8a47cb5bed6e8bdf58d2c86265`  
		Last Modified: Thu, 05 Sep 2024 16:07:43 GMT  
		Size: 1.1 MB (1108691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171219159bdab21b1d00d41c425e19019f76fdab1855d461c6a91cbbb0a3b670`  
		Last Modified: Thu, 05 Sep 2024 16:07:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bfe07d8fb479ceaddb6c95fba3286a2d38cf54e67d8c0ad21522c41885326e`  
		Last Modified: Thu, 05 Sep 2024 16:07:44 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0add76cfdfd98f355e07545279115ce08e41043b1d2fd00965d7b97318459883`  
		Last Modified: Thu, 05 Sep 2024 16:15:08 GMT  
		Size: 102.4 MB (102445156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650931bc9a3771962cc77502b9c9ee8cf541c4c2409fbd458d36b0345ba33be2`  
		Last Modified: Thu, 05 Sep 2024 16:15:04 GMT  
		Size: 9.0 KB (9022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da3fb1c12219dd69590389c2f2ba95a277d6ea1936422a9969598b6ad0c8bc`  
		Last Modified: Thu, 05 Sep 2024 16:15:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086d046ca98a84abad759f8069d7af0543e86a982946c447808bdd2e2b971be2`  
		Last Modified: Thu, 05 Sep 2024 16:15:04 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd95123101b9e4d60a278911de861c828ae9bd205869ac9dc782dd6e9176eb49`  
		Last Modified: Thu, 05 Sep 2024 16:15:05 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e97e599debaa1eac77b750f89b32c443da3ad024aec296019ed7b7cf67f82`  
		Last Modified: Thu, 05 Sep 2024 16:15:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f338ec77fa0957272384317628d00c27e698873f6ec524d46442972616376a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5661382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7055f2742eb53e2e11b7ec40db03083760e4775390d77d4bf787e4a645453f1`

```dockerfile
```

-	Layers:
	-	`sha256:54249a789617601969b45cb52a59ec93b1c08b55bb4ab200c388b3f8f8eaa6ef`  
		Last Modified: Thu, 05 Sep 2024 16:15:04 GMT  
		Size: 5.6 MB (5606632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf7e854b0e67d024e58048ca46c6af68960b4f8cd55203aaa9f1bcf0b5f2f94`  
		Last Modified: Thu, 05 Sep 2024 16:15:04 GMT  
		Size: 54.8 KB (54750 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:b5a366b5789aa688ea817e66e3380d99bbe57478bb56c39bac93cfb118026d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156413575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af939f1f4d63ebd62b9867aae117cfd3914b3ed9a204577014c84a6cc021f7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9102e1680f22fb84d3535c7971e66f8bf6d2249e30c751079b9a87c578edb6b7`  
		Last Modified: Thu, 05 Sep 2024 00:20:21 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7eb426c32180a80379ccb88422d5ea5699de4fb2607b86d31459a5eddb001b`  
		Last Modified: Thu, 05 Sep 2024 00:20:21 GMT  
		Size: 5.0 MB (4965091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1233873403bc014757ab5a3d3d8c1122e66dea509421aa79901f4a76b454ec05`  
		Last Modified: Thu, 05 Sep 2024 00:20:21 GMT  
		Size: 1.4 MB (1422115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c509d81f1422dd9ab5257f29223792236e0961e12a2367a41559ad13ffc330e7`  
		Last Modified: Thu, 05 Sep 2024 00:20:21 GMT  
		Size: 8.1 MB (8066307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1dd52d8b45b0b991bd39bf6d654fe9895d2a89a411e80322ec51729f4b804f`  
		Last Modified: Thu, 05 Sep 2024 00:20:22 GMT  
		Size: 1.1 MB (1137135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a1be0eb2f48bc759d5eb62422303ca2a6834dd49421de7b754266c6beab8cf`  
		Last Modified: Thu, 05 Sep 2024 00:20:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30d4bea39b152d4f8297285a4ff9f75b3f4b75b2189be92c524d843fb832464`  
		Last Modified: Thu, 05 Sep 2024 00:20:22 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe7789144e876bf4239d468a5be8459ebd8bce059e19b781c0359e9354b5591`  
		Last Modified: Thu, 05 Sep 2024 00:20:25 GMT  
		Size: 110.7 MB (110659281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57bc575846f7073c7310bf1ff20d2f4d38b63ef653afc314805fdb4cf5cbceb`  
		Last Modified: Thu, 05 Sep 2024 00:20:23 GMT  
		Size: 9.0 KB (9025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6783ae8e33792fa65da96431c0883f61968ac453c9c9d82c1bb67c1e2a208ff`  
		Last Modified: Thu, 05 Sep 2024 00:20:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192078e1ab04946d4405fad0d5b60d18a932fdf727e7d6d36fe63ba487b848e8`  
		Last Modified: Thu, 05 Sep 2024 00:20:23 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87a0e79f4d4d565c75674953fd3df1fdf341215db0ac20bb20cf60cd3c19a75`  
		Last Modified: Thu, 05 Sep 2024 00:20:23 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67129031d8effffe109b8ea5d7a365cb139b501945d75a9aade56fa810964448`  
		Last Modified: Thu, 05 Sep 2024 00:20:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b23557b38e3d518948e0494ba1aa0ae4168fb515716366a4a1153e91ced7a27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5666122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbed2a9866ad0c45b2817c8a2ff7dfd63776481c1548fba008746a7bff225b0e`

```dockerfile
```

-	Layers:
	-	`sha256:2eecb6ddf3971db1a10d0cde92a8a1b0bf626a2241045ddb51508673b9cfe922`  
		Last Modified: Thu, 05 Sep 2024 00:20:21 GMT  
		Size: 5.6 MB (5611732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277721f36c1b719df300fd04f82fac1557a95ec442f4f5cbd34d9972292e3a54`  
		Last Modified: Thu, 05 Sep 2024 00:20:21 GMT  
		Size: 54.4 KB (54390 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:4253fc4de4805984d16256f4bcfe867ab08559a5d110b055be9e1c2520614edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143906731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a70d7a65cc9726398475eed86b9b571753c98e012a56da0407755fd0289ba9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6816d65a3e4f8353643a7b128899349381df213efa9656f19c10a9b5ea808b4`  
		Last Modified: Thu, 05 Sep 2024 16:53:14 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2582c48faeb5f321bdf902ceaf70b33862248078e2e4c9787f83b98bd0c43fd5`  
		Last Modified: Thu, 05 Sep 2024 16:53:15 GMT  
		Size: 4.5 MB (4475058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3e8f22c29b2f27c213f3e56320bf54846e2737e061f819069f7809894322c0`  
		Last Modified: Thu, 05 Sep 2024 16:53:15 GMT  
		Size: 1.3 MB (1333759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04757d844a23c2a19dffb65588017e67356710f54d19ba6625eb9161a56ae52`  
		Last Modified: Thu, 05 Sep 2024 16:53:16 GMT  
		Size: 8.1 MB (8066466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cee2e1b1a6fa76e1bec8663034ad45ecc047698912407ef607416445f02309b`  
		Last Modified: Thu, 05 Sep 2024 16:53:16 GMT  
		Size: 1.2 MB (1182625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220e33cd4eaacd1b9c035697266946423133bd882349a6474f6ca67e49c77c9d`  
		Last Modified: Thu, 05 Sep 2024 16:53:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a7846879e7ce6da899c4a884930489c2259f94036b0d58b324e2e4b5879ddb`  
		Last Modified: Thu, 05 Sep 2024 16:53:17 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327951e1f94d170db9fda390442f2021988461878b82caa0bbf0f7d604d99081`  
		Last Modified: Thu, 05 Sep 2024 21:20:32 GMT  
		Size: 99.7 MB (99704421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7727caaa6f1fb2de9fb6b676832a2ee4c5f088c80a8e1bc2c8c172f5ff537a0c`  
		Last Modified: Thu, 05 Sep 2024 21:20:22 GMT  
		Size: 9.0 KB (9025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe31d37415c66f2b86639db8b8fcf3efbcd627f91f06f56e0211836013c686c`  
		Last Modified: Thu, 05 Sep 2024 21:20:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a849b86702f25e56c6e56b5e305ce1f18545a475cf2626ff7838747d8b9170bc`  
		Last Modified: Thu, 05 Sep 2024 21:20:22 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f917f9b6bec47d1e4e824646372d8b1adf8949a07be8babc3ade092e3e1e1c3e`  
		Last Modified: Thu, 05 Sep 2024 21:20:23 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c666f9ce69c8b921d493b024fc59be681ed273c400e0b9006af1ac2ee5a529`  
		Last Modified: Thu, 05 Sep 2024 21:20:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:745b6bccdfdd2c7a7d9c36dd11786df5ef6f48059ed0ce54c4cd3a8b227609ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 KB (54306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730768436add5c2d5a353d8e841300967fe65a917241495bc72e308a245f0c56`

```dockerfile
```

-	Layers:
	-	`sha256:cb39c51f462ebbff4a4444b917731810ad3764cfce9fda09205069287d286af4`  
		Last Modified: Thu, 05 Sep 2024 21:20:22 GMT  
		Size: 54.3 KB (54306 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:c7f3ff2296a1f1e8965cc92f075f96a37d0a600148d2e020cc6e6c0cb9d93c2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160422317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12cd09909f8b21caa41498973735c074a855c891fb1c6eb30233da7b5047e99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7091a65b3af01393bb237a0dd5e1eb6eb6722714679ff5876b084574dc17706`  
		Last Modified: Thu, 05 Sep 2024 03:09:50 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800ed3f152dd7bf42d96276af7a9d1ce719fd2a3bcef42118e305c36e12221e1`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 5.4 MB (5368161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075f522e2a21fb72d03df834c71e2fbf45a6ec691eeae0decaa36ad2bc0652b0`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 1.4 MB (1368567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dd0b39792e48b0b4936cc2735903bd6daaa6f632a856cfefabf8c621eb16ef`  
		Last Modified: Thu, 05 Sep 2024 03:09:51 GMT  
		Size: 8.1 MB (8066345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8784a13cd11f3237242eb57895bd508e0f5d410cc1017caeced52945e8b97322`  
		Last Modified: Thu, 05 Sep 2024 03:09:52 GMT  
		Size: 1.3 MB (1283474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35aba7bcf3d315f55153104351b2edee8c0103834595bc782d25cbec20f5001b`  
		Last Modified: Thu, 05 Sep 2024 03:09:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f872029cf50f514a97ad2dc9fb914632e626f454e72f4795b87ad68dabc7f3`  
		Last Modified: Thu, 05 Sep 2024 03:09:52 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fc29cc51a46f195a0294620f5a5b36399b8b7e8f925efcfc33df6a710568d9`  
		Last Modified: Thu, 05 Sep 2024 03:25:51 GMT  
		Size: 111.2 MB (111194072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50be7dbdc2a9681647d5cbde2ff034d7a4637203520432a9bbf642e226596e3`  
		Last Modified: Thu, 05 Sep 2024 03:25:47 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e21a301a434566f4be73966fe245b20d581f6f42f7d0eed440bd1cbef78442`  
		Last Modified: Thu, 05 Sep 2024 03:25:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb0c0cd400dd19fab0d8b1df1e198dbc69ded5f06584170f4187f064e2c6ca9`  
		Last Modified: Thu, 05 Sep 2024 03:25:47 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a311fdfc86e31c9de53cf08a42cb4758344c59934c38c3c72dfdfc6893b0a8c`  
		Last Modified: Thu, 05 Sep 2024 03:25:48 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7cf74d96840c24bd1ddc28fe4296a2c6e62b600e8fa57f8cfa703f752d8b25`  
		Last Modified: Thu, 05 Sep 2024 03:25:48 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b49376e7842f57831b9bbc51fac282eabbd7bf2450ed2757d66b9111f1019c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5662021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32df2bf449405ca738fdf87bc94d7c3b01cc2c686938b90e05d1ff13af20179f`

```dockerfile
```

-	Layers:
	-	`sha256:21d3aa8a210988f06bc7e587d6502b8822744926161eea07d511356cf20bacc3`  
		Last Modified: Thu, 05 Sep 2024 03:25:48 GMT  
		Size: 5.6 MB (5607520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46ee04c27aead48091401e0be41baf28ea1775253ea67107d9c09c371a173270`  
		Last Modified: Thu, 05 Sep 2024 03:25:47 GMT  
		Size: 54.5 KB (54501 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:12-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:83e44f328d903e85f52257a59fac81605b044f9bbfd8a490d2bf5bb92673e6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153856747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93a2c41b696807c3a22d4c24df4ba667f1741f5eca5c5b552d9d5fd7ec7ec24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:22:52 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_MAJOR=12
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PG_VERSION=12.20-1.pgdg120+1
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:22:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:22:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:22:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:22:52 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:22:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:22:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a71df81faca4120f677817bbd051e773830b054e72626158c76b4df335fa5f5`  
		Last Modified: Thu, 05 Sep 2024 05:04:02 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697d886823662fa64c552d6ec433809a3b77ca9bb1355ec5cba3160fa530a060`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 4.4 MB (4391038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8a2ee793ee906d11de05d1a1778d1a245ff0121f2521f0fcbd8c5dbc63acbd`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 1.4 MB (1412694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43f4933e2b533e4734d02a6cf60a19522e291bd446eabfa1ecb8031471b1beb`  
		Last Modified: Thu, 05 Sep 2024 05:04:04 GMT  
		Size: 8.1 MB (8120458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29a493f58318811251ef710e6785725733972cd6f778208e7a7663b01cf0128`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 1.1 MB (1096735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd2aad8c7ec9a88dee775539c06b9f365c7fdbec866fd84fe4d372a6dcc4d14`  
		Last Modified: Thu, 05 Sep 2024 05:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0224b48d801dc7fd91c13ef65aac3ab8b4b00134811da28553542be3631fc`  
		Last Modified: Thu, 05 Sep 2024 05:04:04 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ea36459d17376d47ff9f9b2b204d743fdaa1a650b99bb5fe4a657fa10b8e33`  
		Last Modified: Thu, 05 Sep 2024 05:15:57 GMT  
		Size: 111.3 MB (111326162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a69de0e904713dd877e16db78cff51c4f9f06f324d9c34c7bf90e3e2339440`  
		Last Modified: Thu, 05 Sep 2024 05:15:55 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf11a7c4f3d799ef8b67aa2dbae0047e4a7ae2057f0c1799fb3e7b9bbcf5482`  
		Last Modified: Thu, 05 Sep 2024 05:15:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae63863cde4a52304eb9c19e8bb73a0ded3bddc45069c58d2b18fe3be9efae8`  
		Last Modified: Thu, 05 Sep 2024 05:15:55 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3463cc7365aa438348f6cdb014f4410b63daa53907caae078a4e8588c8c46c5`  
		Last Modified: Thu, 05 Sep 2024 05:15:56 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e618b1a5982b7e78b7b50995be19ee241e2191b214984b37cf5f82466288e0a`  
		Last Modified: Thu, 05 Sep 2024 05:15:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:12-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ae771a25b64f98fc5367c552134262b845b84604295c7dd6d781b8a6c047543e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5654126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00909a969db9d7da8d6d08d4b49abaa347f2fab7b1aebf51d56104be64aa9275`

```dockerfile
```

-	Layers:
	-	`sha256:3cd9b04745459dec5b514325d0d4333adecdef37a5944694f61077b53e640404`  
		Last Modified: Thu, 05 Sep 2024 05:15:55 GMT  
		Size: 5.6 MB (5599685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1804ec4b61fd83a047bdea998c1cf60ffbd4c5413835be1ebca723d8c685b07`  
		Last Modified: Thu, 05 Sep 2024 05:15:55 GMT  
		Size: 54.4 KB (54441 bytes)  
		MIME: application/vnd.in-toto+json
