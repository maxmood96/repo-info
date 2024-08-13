## `postgres:bookworm`

```console
$ docker pull postgres@sha256:099dbb13112c133b37463fd312d3134aabfd5b3db3846f2f336b2996a9566bec
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
$ docker pull postgres@sha256:07ad6d6385313c68c8acd575ac8cc0d73921cdea430afd3dc228782ee1f5a73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153447168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69092dbdec0ddd9e1860e67be2c040b83cce9ffec785b2f740f34e8eb43178e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg120+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd23fa89c286aaaea69d8d8753d67c8268863040dd05312c0728ba22e74ac73`  
		Last Modified: Tue, 13 Aug 2024 01:21:31 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9110f5284332a02a5bb8d8e24c0dc41a7cd373a6c839e232744412904207dcc1`  
		Last Modified: Tue, 13 Aug 2024 01:21:32 GMT  
		Size: 4.5 MB (4533687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a5b191a941c2b7c7ac4151e87f32f7ef7e5ef1bbc9d621069c382aea1cc2ac`  
		Last Modified: Tue, 13 Aug 2024 01:21:31 GMT  
		Size: 1.4 MB (1446619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0baaf1c42c663179d7d676a48f976f918e0a45c12a29fb28d4ca5243456c30f`  
		Last Modified: Tue, 13 Aug 2024 01:21:32 GMT  
		Size: 8.1 MB (8066212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c42bd6bf4888ce7ab749a4623877882e3bbf1c3bbbee725db31e88d346449e4`  
		Last Modified: Tue, 13 Aug 2024 01:21:32 GMT  
		Size: 1.2 MB (1196040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb55f9f5ebf8c3f1a0619d6b6c87e65d3a64be92a6b342141a17179cb14953ca`  
		Last Modified: Tue, 13 Aug 2024 01:21:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eeec50ef8e162a764cc9cb44ef2c9a17e5294746a8f07d1399126a4302c4ed3`  
		Last Modified: Tue, 13 Aug 2024 01:21:33 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3d1f8aa00217b52c61bac7b931e07f70d36763d74ea4c7d03164c54a68d172`  
		Last Modified: Tue, 13 Aug 2024 01:21:36 GMT  
		Size: 109.1 MB (109058140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199cdf05dfecd314ae9f537bd3e666612c773d7132403ae25131fb9e46f17b11`  
		Last Modified: Tue, 13 Aug 2024 01:21:33 GMT  
		Size: 9.9 KB (9917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438d147df75093e0d197dba6b09b6603e979c122f181ac4058cd1b6c3a6b9ba6`  
		Last Modified: Tue, 13 Aug 2024 01:21:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e706f2e5938c23792df1b56a9b844d01d935c8e115826fa962d79349b43b46`  
		Last Modified: Tue, 13 Aug 2024 01:21:34 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2505d0b604222834009c0f60ae77fb54978228d6944ee00147c551b2dbbc1e1c`  
		Last Modified: Tue, 13 Aug 2024 01:21:35 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133de8acf4aa91a041781bdd71f1a46eb9a2a613762a572348e260233777c99d`  
		Last Modified: Tue, 13 Aug 2024 01:21:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5adf8b0ef7e8911c83abc1101f5acc9a7f4c2dcc300e9318c8eb585cc9ce5a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3177c5306d084cabbba234761641d558adb4453d3372ca34b37c237393608b`

```dockerfile
```

-	Layers:
	-	`sha256:db3b2493d9249feca1fbc060e4db0424b159f335219017ff21db381899fa857d`  
		Last Modified: Tue, 13 Aug 2024 01:21:32 GMT  
		Size: 5.7 MB (5749749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9b1baa4515af0585b26b186a8b8130d4e5faa426f5c13627b5f7be919251ad1`  
		Last Modified: Tue, 13 Aug 2024 01:21:31 GMT  
		Size: 55.0 KB (55040 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:5d28adb0ef133afd7e8ec00523994265a27a88615664d7520b9a2ad19a0ce402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146178566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c14ea3c6cb7071043607eb8df0950a15b1032bcd25fc21480fb777bf4ee6083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:01 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
# Mon, 22 Jul 2024 23:57:01 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg120+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e5f426a0038285fe41e79a1f182ce2b0fc81ae1511ed7b086d11c72960b81d`  
		Last Modified: Thu, 08 Aug 2024 19:17:33 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514b72509b73a0239738641cab477b8ec41b14d4d4408cb36bc46508a83e70c6`  
		Last Modified: Thu, 08 Aug 2024 19:17:33 GMT  
		Size: 4.2 MB (4150875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ba1e65c1d6c89e4cecafa0fd0431610f25fb0391042bbff174575671107215`  
		Last Modified: Thu, 08 Aug 2024 19:17:33 GMT  
		Size: 1.4 MB (1423818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf55ec4029974d792237a9ae53f2426fcc983f4f8cdf4aaca942975daf2404f`  
		Last Modified: Thu, 08 Aug 2024 19:17:34 GMT  
		Size: 8.1 MB (8066322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e922c489574b9892bcf87bde34bfd5fca6f658fb9dc0db029c2e5db2017e07ca`  
		Last Modified: Thu, 08 Aug 2024 19:17:34 GMT  
		Size: 1.2 MB (1194823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340c34ca24c124b5241ac6f06a02304f858bc457ba9855110c323fdc9b047bb9`  
		Last Modified: Thu, 08 Aug 2024 19:17:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb7b24a6ecc9edaa06a0578a468c3040001301f073ee7532f089cb647c7ff4a`  
		Last Modified: Thu, 08 Aug 2024 19:17:34 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff94d493e6fda8940647d4de6b6cf626296cbea6f0d85c987c12e8235f00e732`  
		Last Modified: Thu, 08 Aug 2024 19:54:27 GMT  
		Size: 104.4 MB (104435172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0d94052449aedd72c5d2e2fd8480f83636ef0d15efdb303f829a77a2c1cbfd`  
		Last Modified: Thu, 08 Aug 2024 19:54:24 GMT  
		Size: 9.9 KB (9928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77b4212682f79e7d9ca6415a926366307d3713ac8e6fb2bd9943746c26916d6`  
		Last Modified: Thu, 08 Aug 2024 19:54:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392d9d6058426109936334b066bb9a16cc12634ad6394ed4d36fd889ca262a98`  
		Last Modified: Thu, 08 Aug 2024 19:54:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2f0be22d6c0b9184dab9c9dcfd7734de92e68948ad2b77821ad241b583aa7d`  
		Last Modified: Thu, 08 Aug 2024 19:54:25 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe8b12bfcc66293b5e031df30f62baf4b65df6211c2fa5197a027d840ba0851`  
		Last Modified: Thu, 08 Aug 2024 19:54:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:176415cea573497c3affdc51f0534476b0327113a0bed71adbf6871d7c8f09f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d685b78787ddfd4c8c5ba8d3d14dbf4680b7c26a8ab8d1ab5c894acdf43f9005`

```dockerfile
```

-	Layers:
	-	`sha256:3a2e95984674a92ce892f0d8c1b1067d046f02ae100a394c6137abbeb4f6e6c1`  
		Last Modified: Thu, 08 Aug 2024 19:54:24 GMT  
		Size: 5.8 MB (5767162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87eae2f349fcf13e30f514e1991f5563bc445abc8e7917787e8b2be07a55c8ec`  
		Last Modified: Thu, 08 Aug 2024 19:54:23 GMT  
		Size: 55.3 KB (55268 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6c6cd4ec34a84587531325c860ecf71790bd8f2dd240c8eafedd8c3a54893513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140898923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967065e3f9483f673b9e40a2c09e66c9a07994096b94ed80a4cedee368fa9247`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:06 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Tue, 23 Jul 2024 03:03:07 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg120+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea3a49c46c094a279aa08cdcbcca92896632f8795e70853a45d5ae111fe4c25`  
		Last Modified: Thu, 08 Aug 2024 19:32:43 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1f353aa220336e01ea6ba39c6abd089ae0cf3325886c35e05badecc762d9a4`  
		Last Modified: Thu, 08 Aug 2024 19:32:43 GMT  
		Size: 3.7 MB (3742536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed155b4e2a3e27652b71782a7d15194532e0990016795256e54891839b4a1fd7`  
		Last Modified: Thu, 08 Aug 2024 19:32:43 GMT  
		Size: 1.4 MB (1413616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45b8817d9ff802897edf608126878c31fb8ce996134a107a11ad30521b7f73b`  
		Last Modified: Thu, 08 Aug 2024 19:32:44 GMT  
		Size: 8.1 MB (8066233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ac119a42337f2f78507e4111d492265ccd780996ba9dee5f363ae3e46ad76`  
		Last Modified: Thu, 08 Aug 2024 19:32:44 GMT  
		Size: 1.1 MB (1066964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02147fce0d53719f82c9d578dde335427be99988086002064787080f47134d1b`  
		Last Modified: Thu, 08 Aug 2024 19:32:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f96c8a9129ebff2f03586fed3d6dad8ffd1b236f8341da4416e57ec58bfb80e`  
		Last Modified: Thu, 08 Aug 2024 19:32:45 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b6e62b43beb8b1174f933a15f80b77a1d6b98e469e59eb082d0770dbfd10f5`  
		Last Modified: Thu, 08 Aug 2024 20:14:38 GMT  
		Size: 101.9 MB (101871115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6f73536a46c38e7f361212de6ebabbcc6e7de74629f33e7eda46150c31e46`  
		Last Modified: Thu, 08 Aug 2024 20:14:35 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357ce7167de55adc626d1ac0bc43df9f81de7e7a189acfa902c0935ce0408a6`  
		Last Modified: Thu, 08 Aug 2024 20:14:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f013b4587c84e19f43d8244b14ee4496f1777a75a9853b5873cb06a3d02aa47a`  
		Last Modified: Thu, 08 Aug 2024 20:14:35 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91765bda1012e9f65aa9b6f148bdac570748c1a82940ff368d342653cedda5b3`  
		Last Modified: Thu, 08 Aug 2024 20:14:36 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638cd2582d724454103bedcb36f191bdcc90708ede3153d8ce27c38d825c3c1e`  
		Last Modified: Thu, 08 Aug 2024 20:14:36 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:cb7937af7f299786407f7b92ba54716451f414e96028296029b70a49249b7a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c34b188aca6cff963bc24e0608a9413ee1832fea1ab03cf87964bbbfa8ec75`

```dockerfile
```

-	Layers:
	-	`sha256:86106ddfad761d586f4f5e18bb1d460d9cc883dff0838aea19c2fd9eb9f53a22`  
		Last Modified: Thu, 08 Aug 2024 20:14:35 GMT  
		Size: 5.8 MB (5766831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b9e6d62abf412ee0285c0fed9ee1ae71ba6f2396b5f298dbaeddbe6a95c5e2a`  
		Last Modified: Thu, 08 Aug 2024 20:14:35 GMT  
		Size: 55.3 KB (55269 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:15f0fc26e52885482f6a9d9637db7a0a9075ec8ba0929bc05aa96e3f9f688cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151621841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e30f79909c3acff8b96de70cfadb2b8c4f4f753da355f03d8c1489ecc1d6da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg120+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410e6664cff39734b23ad0ac61f6c074573698f37688dfbf884be4150be6a985`  
		Last Modified: Thu, 08 Aug 2024 19:11:08 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348078e7844fe737124338250d987dce2691340b1b82293506d0ac6e0717e155`  
		Last Modified: Thu, 08 Aug 2024 19:11:09 GMT  
		Size: 4.5 MB (4499149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bb45ed9da018b69df75614db0932ba03367b864070203505ceb564e9cb5be8`  
		Last Modified: Thu, 08 Aug 2024 19:11:08 GMT  
		Size: 1.4 MB (1378722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ce427aba9b67d94cdf0d0e96f086771cd6fa11c0e0263d487b8810cfc45cca`  
		Last Modified: Thu, 08 Aug 2024 19:11:09 GMT  
		Size: 8.1 MB (8066275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0b03073a01c065b9ed22a66d6d225c6654ea2378612df312369b58b1f605ef`  
		Last Modified: Thu, 08 Aug 2024 19:11:10 GMT  
		Size: 1.1 MB (1108692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43ccc6a89238503e14e7e57e11d0e7487920de837fd472733a2c82ded5bc43c`  
		Last Modified: Thu, 08 Aug 2024 19:11:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa01237db67e1c2da1cfc6b5b541ac0376384413225d5337e2eb48be4e0eb994`  
		Last Modified: Thu, 08 Aug 2024 19:11:10 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b92283dde4a8cdb6a8f130303d376b411fc723d22b040d906c4c3976557cae`  
		Last Modified: Thu, 08 Aug 2024 19:20:02 GMT  
		Size: 107.4 MB (107392191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be4a35f7b708f87e1eaada6503b75f097c1374313bce5d85f3cc8ec7dc6c21a`  
		Last Modified: Thu, 08 Aug 2024 19:19:58 GMT  
		Size: 9.9 KB (9915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f69db13ff2310f7b6d2c258334bc85d7232a292eb9013026a993701cd963247`  
		Last Modified: Thu, 08 Aug 2024 19:19:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1960e56810f71bf58db3e9334914f9cf51dcad08b577a051c4614b5a22870cf1`  
		Last Modified: Thu, 08 Aug 2024 19:19:58 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca33794197e6f258657ebcb1cfdf62f3db0a70c9f45a867baaf299036ba31a4`  
		Last Modified: Thu, 08 Aug 2024 19:19:59 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b4e1cfe501a40b335fa29363055264d6f2b2a77baafcbf7b682da2306ca8e1`  
		Last Modified: Thu, 08 Aug 2024 19:19:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:980efdc278d265a95ebae7cefb42108849c02fad2b31003161a42b419aebabe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5811487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90c003cddcfe0d1ac22c7c2f6f8ba47969e90c51e39436563e281c87ecb324a`

```dockerfile
```

-	Layers:
	-	`sha256:c5e28e0c26804fcb1f0a7fa97728bfe4c6016d42cc408f9345ffdacfcf44a4c7`  
		Last Modified: Thu, 08 Aug 2024 19:19:58 GMT  
		Size: 5.8 MB (5756114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ebb416f058932c15f9ebb80753687548b07ccf79ec0ae8f6c0d02c7e48014ef`  
		Last Modified: Thu, 08 Aug 2024 19:19:58 GMT  
		Size: 55.4 KB (55373 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; 386

```console
$ docker pull postgres@sha256:d66ca842fc017d37627e7a1608fefce7758e4fabf60736ccf6c33ec779fbdb59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161576177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b092c3a965d5ad6c02ed3ad2914f6f2aed0f42342c0b82508d94149f69d98b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg120+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998aee6abe4ca98319be98aac25df9671016c72ae3aea39da8ba24f6f437b36`  
		Last Modified: Tue, 13 Aug 2024 01:34:21 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d430e5da8a78ea9c107d5537253832782aaee19b5846bbae2e29b3832ee701`  
		Last Modified: Tue, 13 Aug 2024 01:34:22 GMT  
		Size: 5.0 MB (4965050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302cc3ef8858f6522304e84cb08303f30dca224be38258b5d56b73579187b3f0`  
		Last Modified: Tue, 13 Aug 2024 01:34:22 GMT  
		Size: 1.4 MB (1422120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a6b38d6999f806a30bd2d39a928fe46329e08e7d24bc1811655126c8ad83ed`  
		Last Modified: Tue, 13 Aug 2024 01:34:22 GMT  
		Size: 8.1 MB (8066250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0918c24139b0d5d6ce2b190517a6a0810a8f5fa1b43998df5cf946c5a703b6a8`  
		Last Modified: Tue, 13 Aug 2024 01:34:22 GMT  
		Size: 1.1 MB (1137136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb77c21f535965b136a53580248d753beadfe4bfbc1ad536260dd0d8bedbacb`  
		Last Modified: Tue, 13 Aug 2024 01:34:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248fe1453129071dcd01dfae74018ce2dc5349da7de9ee29f334928a15e0bef9`  
		Last Modified: Tue, 13 Aug 2024 01:34:23 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af94b19dc468620a5eb0a83889c426f40f0c89aaddde83a3a178d323ba6eef2`  
		Last Modified: Tue, 13 Aug 2024 01:34:26 GMT  
		Size: 115.8 MB (115821095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9d2930077e0987c45efcfb410ac28b9a66487fe84b6add7d2bc9b11dd0596f`  
		Last Modified: Tue, 13 Aug 2024 01:34:23 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e166c741cedc9e31cc6740d5d0daeaf748913ce27b105a02f39f6bf13291b11`  
		Last Modified: Tue, 13 Aug 2024 01:34:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a77c3445f19e115b32c0d9e041de20e4e6e1457bbccccd6eb3f6c0942525c5f`  
		Last Modified: Tue, 13 Aug 2024 01:34:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a073e5ead1aa5904340a66b30bca2f3d80c3d2135d7f5e28afa4304940c08eca`  
		Last Modified: Tue, 13 Aug 2024 01:34:24 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6558211dfba5dbf1f13e6d618c939cb5c8916e096fc24b19e3e941dab4e58f`  
		Last Modified: Tue, 13 Aug 2024 01:34:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:39828fa811134f6a1c3526ba036f804c4fb41e2b7f4f144b2b6d63a1c1f3db83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b223de06d81fdba3a22a8d0937c0dde90e70768882fd532949abed23cb5698a`

```dockerfile
```

-	Layers:
	-	`sha256:36daef717f50a93f1711f45b9b51c65e3a55e1b22e03447aeae37b34d0d3fcdf`  
		Last Modified: Tue, 13 Aug 2024 01:34:22 GMT  
		Size: 5.8 MB (5765189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe186ed0ce74e21e2d7b1936d4b2879b387e273d1d4343f1b24884a01353e90`  
		Last Modified: Tue, 13 Aug 2024 01:34:21 GMT  
		Size: 55.0 KB (54979 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:19f1b00300915a8f4024fc16fadcfc52cd702330844bea81f802d020e8629b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148866227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15aaec19509e4e138a669d3390dd4f6c90f9559c1366cf373c72925b58050d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 00:37:51 GMT
ADD file:6b0de87e15c6880fed3a8430d23a511322519e32c50677c24f4597141e3a85ff in / 
# Tue, 23 Jul 2024 00:37:56 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg120+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8de7af9de8596141237ef7c589f08f773ca8ce07671b2bd7e192055d5165f74`  
		Last Modified: Tue, 23 Jul 2024 00:49:06 GMT  
		Size: 29.1 MB (29124926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdffd4752225577c77b92a925d351a821becfbbd7e51cc4325fcf475ff76bcec`  
		Last Modified: Thu, 08 Aug 2024 20:13:04 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60380b141f1742604eaf3fb53014fce9b7cf7e9ec8a22c966cf2e9a603447410`  
		Last Modified: Thu, 08 Aug 2024 20:13:04 GMT  
		Size: 4.5 MB (4475080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35115b566247f21cd64a08ec1588212b4fb343688702c3858738c0b65f5c91f0`  
		Last Modified: Thu, 08 Aug 2024 20:13:04 GMT  
		Size: 1.3 MB (1333788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2c96cdee48b9746d7edc829ec0fabf0f1af08a79cd412232f81c0b005583a3`  
		Last Modified: Thu, 08 Aug 2024 20:13:05 GMT  
		Size: 8.1 MB (8066416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94efb9def9dd824ae3668d009c2e41c6df37604f98679cd776e2488b45e51cb`  
		Last Modified: Thu, 08 Aug 2024 20:13:05 GMT  
		Size: 1.2 MB (1182630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c246bc0a801b03313dbfe9b2b56ec8dfa5edf7a6a181dd342aa6491b1ab63855`  
		Last Modified: Thu, 08 Aug 2024 20:13:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8f3d13fda07638f9b2507ea4956ef99e670d9d5500246836b35280c56879e8`  
		Last Modified: Thu, 08 Aug 2024 20:13:06 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0b756e92a48a6801b08ca171d236f0d395e5d2673ec30b316280a14e73e791`  
		Last Modified: Thu, 08 Aug 2024 22:37:20 GMT  
		Size: 104.7 MB (104663126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519eebbf5272e6efa226325750496555aea2df9d3c8d936c417c0c0d3a7be4fd`  
		Last Modified: Thu, 08 Aug 2024 22:37:10 GMT  
		Size: 9.9 KB (9928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fa69239e553caddb301a2de6b67e5a990e9558ef0a8674faab31659ba3e4a6`  
		Last Modified: Thu, 08 Aug 2024 22:37:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a617fd035c018681b1a029b73003e0caac06c41a15f7c078965445b98b848b3`  
		Last Modified: Thu, 08 Aug 2024 22:37:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3745540debcb2306773d8d48a7c04baaca42d722e0df0cd181b5a9ccfcdb6312`  
		Last Modified: Thu, 08 Aug 2024 22:37:11 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614802d153a5e7402a4231dcbd69e5b51a6c66613dac7f75277cac5f64d9518c`  
		Last Modified: Thu, 08 Aug 2024 22:37:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8a96d9673192d17fd79a945dbc788b38f2f3d0f9372e7933acf84bd6cd645563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 KB (54929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34b267b226b03d146b3802a86e04ad7b889cf48ea93a1f8dd36a72348d0eeba`

```dockerfile
```

-	Layers:
	-	`sha256:4ff04b16d15a2ccfc71d1e948b5b2f257132ca89c522d7a6c6bd2a45e8726422`  
		Last Modified: Thu, 08 Aug 2024 22:37:09 GMT  
		Size: 54.9 KB (54929 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:42e5c5a027444a9d9e5bb7023276d7d630e35ca01d7f52c91d80494f254e556b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165633209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6185d9a748b4a714297f0744e185d227896dca55b6b69d493135717345c9a29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 01:26:56 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Tue, 23 Jul 2024 01:26:58 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg120+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a48330d28cfb607eb211b4ea71a85ec4c1e728bcecf3fd5b2eee9f912057a3`  
		Last Modified: Thu, 08 Aug 2024 19:21:08 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecffe9c0d1a6836b72ee5ab183e354e3514f145680a18edebe65d36210adbd79`  
		Last Modified: Thu, 08 Aug 2024 19:21:09 GMT  
		Size: 5.4 MB (5368169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7420257dfd2b699795c1e793ce3dda8598d0d3630224b296d3f6931bdaf728`  
		Last Modified: Thu, 08 Aug 2024 19:21:09 GMT  
		Size: 1.4 MB (1368619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6503714d1e88f6e30cdee05dc91c0ec51e98c75f2edeeea0fec0fa32efe3a4f4`  
		Last Modified: Thu, 08 Aug 2024 19:21:09 GMT  
		Size: 8.1 MB (8066311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c95d76469d2a7a9a5a44bb76aecc213c6099720dc2587fbcaae5fa13d474c0e`  
		Last Modified: Thu, 08 Aug 2024 19:21:10 GMT  
		Size: 1.3 MB (1283479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8344049f59cc6909a63042d943e904ca40f51dbc1e4f49cc1a6fc50759eaee16`  
		Last Modified: Thu, 08 Aug 2024 19:21:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dfb73436f9b7f5d9525b531073ab135c0b680e67418024859c8046c17ef847`  
		Last Modified: Thu, 08 Aug 2024 19:21:10 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf68b749cf8952ec26470df42af25a50733b78fbcae4cdd76ee73bb5e72bbaf`  
		Last Modified: Thu, 08 Aug 2024 19:32:45 GMT  
		Size: 116.4 MB (116404105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9ac63450b907a8bafa733c1d0728a1b4f5e0a89aa015e95b74121c9d7b3ff9`  
		Last Modified: Thu, 08 Aug 2024 19:32:41 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3db296517b1ffb67e3d6b850a6ddecfbc5ebff7b39c542a976aa46a8d0813e`  
		Last Modified: Thu, 08 Aug 2024 19:32:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95371cc619f0202a268deea84f4e6be68ef32e309d78117572b84d706b292bfc`  
		Last Modified: Thu, 08 Aug 2024 19:32:42 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75507e749c36ad940455dee79bb5ec61382633d5ea0aa57fe1e0415f332d6f0`  
		Last Modified: Thu, 08 Aug 2024 19:32:42 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7976548c591e685b6fdc69be9202a907ba79468eb66be293f9ab261d22a08be`  
		Last Modified: Thu, 08 Aug 2024 19:32:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a69839be3074e79ecb6f1e4c130b431ddaf2d5b19f16c19d24228653456e1cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5812101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c8d60f75468e723bdb182cc949f4a3536488d825225ca8b2aada71957dad6c`

```dockerfile
```

-	Layers:
	-	`sha256:c14a202ebdcc14f73c67e1805b89625453ae73047098d046b2f2b214232429e6`  
		Last Modified: Thu, 08 Aug 2024 19:32:41 GMT  
		Size: 5.8 MB (5756990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbfdec9cda1af0cff4881059f85e76fd6ecacdac429e5b87a558708d9e1661bf`  
		Last Modified: Thu, 08 Aug 2024 19:32:41 GMT  
		Size: 55.1 KB (55111 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:85f5f414412877085dd48b014445f30b784a307546c4d6b5a30083624b12d908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158948073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147f38893aaedeba57da14835b22b8d318731347d6eb01cdb270f26265c71b07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 02:27:49 GMT
ADD file:d8b037f30c0a2aeded43f72fe61531da3a0e449e034255bb0a7b2182e4e3ca8a in / 
# Tue, 23 Jul 2024 02:27:50 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg120+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:48319744c6dacda7d13413becf85a83639982e97ecf615295a1257ccc3082721`  
		Last Modified: Tue, 23 Jul 2024 02:32:44 GMT  
		Size: 27.5 MB (27490099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824094e9ce7d032d4a4582a7b3f11fac5f20a5c725bcbb16f40b3599e190d065`  
		Last Modified: Thu, 08 Aug 2024 19:18:28 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cdc2132f8879868df60ec73b9cd1d0f199ee359bc3fd8d81c1848c24b8bee0`  
		Last Modified: Thu, 08 Aug 2024 19:18:29 GMT  
		Size: 4.4 MB (4391079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4309977ca3884a04a6453181a0aca4832b78e8c0844420f69d50d787767facdb`  
		Last Modified: Thu, 08 Aug 2024 19:18:28 GMT  
		Size: 1.4 MB (1412727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d884733da4f75baa8db7fd03263a99ca4d33766437cfc720d057bd6c3955e6`  
		Last Modified: Thu, 08 Aug 2024 19:18:29 GMT  
		Size: 8.1 MB (8120415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca38af275cc38ca549a0e53a671aa75f592f4b1855a095b3b35f5ca74114fa46`  
		Last Modified: Thu, 08 Aug 2024 19:18:29 GMT  
		Size: 1.1 MB (1096720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f981ef31790da38ecac1df753ec3278778d3d9af61ccf7a4dff27740ed53bac`  
		Last Modified: Thu, 08 Aug 2024 19:18:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75f7a7a2fe09ebf72b27738442148b81f249c915c5b41b889ff4f251865f73a`  
		Last Modified: Thu, 08 Aug 2024 19:18:29 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0382540f643eb32f69f770a26ab68ec3b6422e9e18df83dd947ad5430d6215`  
		Last Modified: Thu, 08 Aug 2024 19:44:58 GMT  
		Size: 116.4 MB (116416783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea87749b3316b97fd12f6068d926a2ec7fe659de7c4a7d687a7e5407662c2030`  
		Last Modified: Thu, 08 Aug 2024 19:44:55 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e543731aea3eb5fa9f8cb792a4a882a152230271e9e9a942c9f9a27f5ad1baf6`  
		Last Modified: Thu, 08 Aug 2024 19:44:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513df9a617e4cc239f4bebce8f3bd998383b9e9d2f04f3c7c1a0d0c75d48da63`  
		Last Modified: Thu, 08 Aug 2024 19:44:55 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c837b98298080d88fc630da1c4ef00032c6f9f7fad0724c7dbe21277b916554`  
		Last Modified: Thu, 08 Aug 2024 19:44:56 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d93367393cc0b686b1b8ff719d14d68d42b636ac82ffc8fd284d864afccfb5`  
		Last Modified: Thu, 08 Aug 2024 19:44:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:669d3d38a07aa9ed07857af5b2a68737733abf09155dc5cff2215f65b9335cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5804183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3856138fb0ceea19da8b67dac6599a1d74cc529510f97b2570a9ad9a67044c`

```dockerfile
```

-	Layers:
	-	`sha256:091ac183da3f62f9c1e20a5bff1b7953faf0459e530087eb0687d1f970871c0d`  
		Last Modified: Thu, 08 Aug 2024 19:44:54 GMT  
		Size: 5.7 MB (5749143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834988af97af2aa447335d08f3ddf6ca3bd750379719f564c515eb6c0047c744`  
		Last Modified: Thu, 08 Aug 2024 19:44:54 GMT  
		Size: 55.0 KB (55040 bytes)  
		MIME: application/vnd.in-toto+json
