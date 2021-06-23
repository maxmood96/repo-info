## `postgres:10-buster`

```console
$ docker pull postgres@sha256:68fa9fc579de43a8ae290da14c080cdd294954793ef011ca4a5625c32947ee38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `postgres:10-buster` - linux; amd64

```console
$ docker pull postgres@sha256:8404ff9373cfbe79ff90bd2b1f1d13ad4d7f952f38ffcfaa927eedd83fdedcfd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81507960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c6ca43d63ad1f68c6c471b10e229b128e03576df1d2ccac7862371ee7f438f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:33:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 14:33:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 12 May 2021 14:33:57 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 14:34:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 14:34:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 12 May 2021 14:34:21 GMT
ENV LANG=en_US.utf8
# Wed, 12 May 2021 14:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:34:29 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 14:34:31 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 16 Jun 2021 22:32:10 GMT
ENV PG_MAJOR=10
# Wed, 16 Jun 2021 22:32:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Wed, 16 Jun 2021 22:32:10 GMT
ENV PG_VERSION=10.17-1.pgdg100+1
# Wed, 16 Jun 2021 22:32:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 16 Jun 2021 22:32:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 16 Jun 2021 22:32:27 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 16 Jun 2021 22:32:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 16 Jun 2021 22:32:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 16 Jun 2021 22:32:28 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 16 Jun 2021 22:32:28 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 16 Jun 2021 22:32:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 16 Jun 2021 22:32:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Jun 2021 22:32:30 GMT
STOPSIGNAL SIGINT
# Wed, 16 Jun 2021 22:32:30 GMT
EXPOSE 5432
# Wed, 16 Jun 2021 22:32:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b993d5cc6e9a84a3130f78ebe55f65faa48be24f531c18c8ffaf47e241000`  
		Last Modified: Wed, 12 May 2021 14:40:05 GMT  
		Size: 4.2 MB (4179219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65921886500e967ceb3ecb351d57f7ff716ff2c80968c3ac9433f37aea25c53`  
		Last Modified: Wed, 12 May 2021 14:40:03 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c1a94e4ca8e4e20495b3293c3c3cfc71c6ceb8918a27ea0c34a3f056947198`  
		Last Modified: Wed, 12 May 2021 14:40:04 GMT  
		Size: 1.4 MB (1419400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435dd99ceb686f66e94ad1dc9101faf039bc49863df13f9a2f5f84c0f2e95610`  
		Last Modified: Wed, 12 May 2021 14:40:03 GMT  
		Size: 8.0 MB (7965263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ee8e88c67c9c8fe47ad18c8699316478f3bd56f9f9d64ca6553ad9c1aee769`  
		Last Modified: Wed, 12 May 2021 14:40:01 GMT  
		Size: 391.2 KB (391212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b08674f9421970e07641cbbad748919e87c1e9589250e16adcb24b88e88387`  
		Last Modified: Wed, 12 May 2021 14:40:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d358e850d3e87346cf60611562e51226216d2192b71dc399ef9fab05e28e632`  
		Last Modified: Wed, 12 May 2021 14:40:01 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577d8a0edee21424cbed64d28fb8d7632bb0a3043b7d2bc351c93dabf91b7e51`  
		Last Modified: Wed, 16 Jun 2021 22:39:59 GMT  
		Size: 40.4 MB (40389017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae7cf5d44b165e1276b8042dab40905bb4b77a3e07673d9b9c703cadaf8d7db`  
		Last Modified: Wed, 16 Jun 2021 22:39:49 GMT  
		Size: 8.1 KB (8079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4c92daac10230a57a06aa368c477a915e61440aa7e958710ecbc4f82f0cce`  
		Last Modified: Wed, 16 Jun 2021 22:39:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b404da7d0b773675e8dd2927bcaf624731401f05e03a03f50da74c6eccf294a`  
		Last Modified: Wed, 16 Jun 2021 22:39:49 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab450a70eeaafdde4bf1b8c4f558fd5e8843e55c98ca00061ffd0f35cb90aa4d`  
		Last Modified: Wed, 16 Jun 2021 22:39:49 GMT  
		Size: 4.4 KB (4403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a112b534d02c980111a2cd99810f323d5b97aa49123f71c8bf33f78b8c39b8`  
		Last Modified: Wed, 16 Jun 2021 22:33:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-buster` - linux; arm variant v5

```console
$ docker pull postgres@sha256:0aaeb3b569c47dd24542def3f4ababe0de9c2a4ce91609062d5dd3455aae5a70
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77218267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876dfcee1e16012d8a3c7f315a48392153a29fe05ae2d927f1e6c99b216c6e27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 00:55:35 GMT
ADD file:241925c5ca73c99d58f93bc78d7c5bfb6f8b280201a9b55ade45ba0cc054c31d in / 
# Wed, 12 May 2021 00:55:46 GMT
CMD ["bash"]
# Wed, 16 Jun 2021 01:19:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 16 Jun 2021 01:19:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 16 Jun 2021 01:19:11 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Jun 2021 01:19:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Jun 2021 01:19:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 16 Jun 2021 01:19:44 GMT
ENV LANG=en_US.utf8
# Wed, 16 Jun 2021 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Jun 2021 01:19:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 16 Jun 2021 01:19:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Thu, 17 Jun 2021 00:25:09 GMT
ENV PG_MAJOR=10
# Thu, 17 Jun 2021 00:25:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Thu, 17 Jun 2021 00:25:09 GMT
ENV PG_VERSION=10.17-1.pgdg100+1
# Thu, 17 Jun 2021 00:35:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 17 Jun 2021 00:35:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 17 Jun 2021 00:35:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 17 Jun 2021 00:35:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 17 Jun 2021 00:35:31 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 17 Jun 2021 00:35:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 17 Jun 2021 00:35:32 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Thu, 17 Jun 2021 00:35:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 17 Jun 2021 00:35:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Jun 2021 00:35:33 GMT
STOPSIGNAL SIGINT
# Thu, 17 Jun 2021 00:35:33 GMT
EXPOSE 5432
# Thu, 17 Jun 2021 00:35:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:48885a8e20b16cb3bb9d2c3aafc7f040d8609844f69ca8482c42b4829d01b6da`  
		Last Modified: Wed, 12 May 2021 01:10:24 GMT  
		Size: 24.9 MB (24879601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96839a8af50d5993e4941636ec99d6a2c635203241a6fa300a56f5452b21e5b4`  
		Last Modified: Wed, 16 Jun 2021 02:48:00 GMT  
		Size: 3.8 MB (3848014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3e7181e51db3c7dda10708185c5f121b41710502f785d8a3d123bbacd6b560`  
		Last Modified: Wed, 16 Jun 2021 02:47:57 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b382e008baaadfaf278c37a0213e0bdb956fbe862d61aac7e7a0c924d06db4`  
		Last Modified: Wed, 16 Jun 2021 02:47:58 GMT  
		Size: 1.4 MB (1378636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9440b94fd26c601fa99c152fb74f21476fd3c5cd0b9e65cd1eac0fc7db1ba6be`  
		Last Modified: Wed, 16 Jun 2021 02:48:01 GMT  
		Size: 8.0 MB (7965245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6784db25ccf9b6b5183fc17f0e0a9eb92cea76b4701eeba5795f0047ea24595d`  
		Last Modified: Wed, 16 Jun 2021 02:47:55 GMT  
		Size: 390.4 KB (390426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4b83961ba29245b4b81823e7c5da894a79b4ec31167c2ed51fd7a3ac331461`  
		Last Modified: Wed, 16 Jun 2021 02:47:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4033563612369390bac66d37bb474315242eb932752344137cfe7bcd31cb0f`  
		Last Modified: Wed, 16 Jun 2021 02:47:54 GMT  
		Size: 3.1 KB (3054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b3ab36a3cc1855d4a13940cf9078c269c26cd8e2f95df47a4a125253357d23`  
		Last Modified: Thu, 17 Jun 2021 01:12:48 GMT  
		Size: 38.7 MB (38738411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d6eecd37ea474d1c6778ee251c381b956b50f795a94d38bb8149383201d3f6`  
		Last Modified: Thu, 17 Jun 2021 01:12:36 GMT  
		Size: 8.1 KB (8080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27717fe6edd70232d90f1aebc33f724df0cbd9061011479fe1393e3551fb1ab8`  
		Last Modified: Thu, 17 Jun 2021 01:12:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79bcd8637ee16a70a696e2b4eafb1b2e0e833c3422c8bf7c308e0d650e49f8c`  
		Last Modified: Thu, 17 Jun 2021 01:12:36 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de97baf0b6f0d0473ba23b033634a5d0e4ac6098b8fb3d6c514e441196d2870`  
		Last Modified: Thu, 17 Jun 2021 01:12:36 GMT  
		Size: 4.4 KB (4403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0e753db948e65e611376b1538ada1af0f3df854d5cb90ac253d91cc5c71c3c`  
		Last Modified: Thu, 17 Jun 2021 01:12:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-buster` - linux; arm variant v7

```console
$ docker pull postgres@sha256:7150b46feb9b28fdf99d748495689430e856f4a6b8fb903db10d7251038c75c8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73610680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271e4217c669138eed2912394148f644bdf177708e763e2e3ffc8c351a0d03f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 01:03:14 GMT
ADD file:94bf2394dc26abd9f028c2933057a8673c8562e58ec4a0f51bb9bde0a5e4dee0 in / 
# Wed, 12 May 2021 01:03:32 GMT
CMD ["bash"]
# Wed, 16 Jun 2021 17:05:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 16 Jun 2021 17:05:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 16 Jun 2021 17:05:40 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Jun 2021 17:05:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Jun 2021 17:06:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 16 Jun 2021 17:06:08 GMT
ENV LANG=en_US.utf8
# Wed, 16 Jun 2021 17:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Jun 2021 17:06:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 16 Jun 2021 17:06:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Thu, 17 Jun 2021 00:55:58 GMT
ENV PG_MAJOR=10
# Thu, 17 Jun 2021 00:55:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Thu, 17 Jun 2021 00:55:59 GMT
ENV PG_VERSION=10.17-1.pgdg100+1
# Thu, 17 Jun 2021 01:05:41 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 17 Jun 2021 01:05:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 17 Jun 2021 01:05:43 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 17 Jun 2021 01:05:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 17 Jun 2021 01:05:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 17 Jun 2021 01:05:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 17 Jun 2021 01:05:45 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Thu, 17 Jun 2021 01:05:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 17 Jun 2021 01:05:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Jun 2021 01:05:46 GMT
STOPSIGNAL SIGINT
# Thu, 17 Jun 2021 01:05:46 GMT
EXPOSE 5432
# Thu, 17 Jun 2021 01:05:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3035777cd90a3389593bc49a7b39b6f67f9f2679f4e04cc59515f4d5f83ad818`  
		Last Modified: Wed, 12 May 2021 01:19:13 GMT  
		Size: 22.7 MB (22746266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781e8a2dd521ae1bb1175f3670daa6096d63240257fc5c0d9c4bfd48382bedf2`  
		Last Modified: Wed, 16 Jun 2021 18:31:41 GMT  
		Size: 3.5 MB (3481649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8510c911d73570d80271300d25f2e67cb9fab8ec21fed40102300a039c46d`  
		Last Modified: Wed, 16 Jun 2021 18:31:40 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eed89b15b1003ef4de5c99674647bb3865018f111340d66ae8d6360ea52122`  
		Last Modified: Wed, 16 Jun 2021 18:31:40 GMT  
		Size: 1.4 MB (1370396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33a5b9a4afa27c81212c6bc749fceb2c0e4de0ecf8099f2b730e5014a515b5b`  
		Last Modified: Wed, 16 Jun 2021 18:31:41 GMT  
		Size: 8.0 MB (7965196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb6f6329508c731d2b049306a30e9effc838cbaece8f2ed1513ad9270245bf8`  
		Last Modified: Wed, 16 Jun 2021 18:31:38 GMT  
		Size: 385.1 KB (385077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1286560dd1d1f1cddda5fce28ce22c12ae8872a4ac5fd4d56464c01c2eeaab0c`  
		Last Modified: Wed, 16 Jun 2021 18:31:37 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f44160ef74c47548aeb4345b20c08453ec5765d3956d0b4f6053929fc4a0d6`  
		Last Modified: Wed, 16 Jun 2021 18:31:37 GMT  
		Size: 3.1 KB (3056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8377f55551578785634e9bd31c0f7ec31a96b83abe751bde29c80853f75bd7`  
		Last Modified: Thu, 17 Jun 2021 01:44:08 GMT  
		Size: 37.6 MB (37644155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5108a5dc62229adcd1bc449e255b634e634167535770efa6e30e197d379ca46c`  
		Last Modified: Thu, 17 Jun 2021 01:43:56 GMT  
		Size: 8.1 KB (8076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c78d76a30aac39638c8ed2768503ba8adc85ec8855cd49c86baffa912d9052f`  
		Last Modified: Thu, 17 Jun 2021 01:43:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef71f32e8c9c1d5946616839506b1ca610a26eee2f28e71e5669eb1834e0ecc`  
		Last Modified: Thu, 17 Jun 2021 01:43:56 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1323551b1f70ac2ecb43a93b59640c10fc4d64898d87aac9d482b44824dd8f`  
		Last Modified: Thu, 17 Jun 2021 01:43:56 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8054ecb4fc85d0ef40460c2e8db9c2033097fe69b075825e74cbf28349434fd8`  
		Last Modified: Thu, 17 Jun 2021 01:43:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-buster` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:546205cc4cf5106a51d37b22c0869293a70a605b796d3d18740c3d052c5404fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79903848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcf9b144097b49c8d0f5620f44ddff9b737418ac20a138665cca9dbcebc8bab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Jun 2021 23:49:40 GMT
ADD file:beee00b59da720f68e12e2ba2a8134207c80c777ddb4ceb03c71e3e4c3f51c93 in / 
# Tue, 22 Jun 2021 23:49:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 08:00:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 23 Jun 2021 08:00:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 23 Jun 2021 08:00:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 23 Jun 2021 08:01:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 23 Jun 2021 08:01:10 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 23 Jun 2021 08:01:11 GMT
ENV LANG=en_US.utf8
# Wed, 23 Jun 2021 08:01:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 08:01:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Jun 2021 08:01:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 23 Jun 2021 08:19:18 GMT
ENV PG_MAJOR=10
# Wed, 23 Jun 2021 08:19:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Wed, 23 Jun 2021 08:19:18 GMT
ENV PG_VERSION=10.17-1.pgdg100+1
# Wed, 23 Jun 2021 08:19:34 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 23 Jun 2021 08:19:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 23 Jun 2021 08:19:35 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 23 Jun 2021 08:19:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 23 Jun 2021 08:19:36 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 23 Jun 2021 08:19:37 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 23 Jun 2021 08:19:37 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 23 Jun 2021 08:19:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 23 Jun 2021 08:19:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Jun 2021 08:19:38 GMT
STOPSIGNAL SIGINT
# Wed, 23 Jun 2021 08:19:38 GMT
EXPOSE 5432
# Wed, 23 Jun 2021 08:19:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:448f6bf000e31217a7c202c659b03b7f8ac8d3ae6b03ef7a2f8339be2f00ff4a`  
		Last Modified: Tue, 22 Jun 2021 23:55:25 GMT  
		Size: 25.9 MB (25914993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac3c0fe3ab17bfa4c3c1f905b67e705dd622e5b719250a3707da3275f6427c`  
		Last Modified: Wed, 23 Jun 2021 08:43:51 GMT  
		Size: 4.2 MB (4170280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4262cf38624a63127b9f8a869b2008bbbc19d68f64ea18a57e1a571a2ac4758a`  
		Last Modified: Wed, 23 Jun 2021 08:43:50 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa7b7e739f9235bd376773e956230ce34be4fee1ac7515b4b061e692e5bcbbd`  
		Last Modified: Wed, 23 Jun 2021 08:43:50 GMT  
		Size: 1.4 MB (1354308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b13a00ff8f5091034119a7504c90c399e5a944d7a4046a7d1de913d3af5d07`  
		Last Modified: Wed, 23 Jun 2021 08:43:50 GMT  
		Size: 8.0 MB (7965162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6582bc95f89c2fffbd09f50933c184070070b2f05ec18079f9253705c81aec`  
		Last Modified: Wed, 23 Jun 2021 08:43:48 GMT  
		Size: 389.4 KB (389428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9731edaa8053d4c7628e5bac8a251b7afd2831aea1b9cf30a41521f2684fd9a4`  
		Last Modified: Wed, 23 Jun 2021 08:43:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7234d2c24f1fc9041caf2d2a5c9adc28a2b7132cb90abcee81043b07965f747a`  
		Last Modified: Wed, 23 Jun 2021 08:43:48 GMT  
		Size: 3.1 KB (3056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4158ca14d02ecf4460db5eb8ff13145e2e7c3b068ed8aee4fe8b766901515191`  
		Last Modified: Wed, 23 Jun 2021 08:45:56 GMT  
		Size: 40.1 MB (40091740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73aeae08f349cbdacd10703013c5c2a60c9ab918b3261640e4ffaaacb53f472c`  
		Last Modified: Wed, 23 Jun 2021 08:45:46 GMT  
		Size: 8.1 KB (8076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be0a88d6c1b190f5fb87938123c5a70cc46fe0b5588b84dd7b2afa7819e721`  
		Last Modified: Wed, 23 Jun 2021 08:45:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4616f778de9c39596c386cee1418e4ca80d00a887c08dfd457c1026d546caa09`  
		Last Modified: Wed, 23 Jun 2021 08:45:46 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ab8c47357970011d4f5efb2a4a18a934669f0ecd9b11981f3b1e39a85b1f5`  
		Last Modified: Wed, 23 Jun 2021 08:45:46 GMT  
		Size: 4.4 KB (4401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6018a99031da6147f959651a599002ddaa5b26984ca54a225be925859ff9e4a7`  
		Last Modified: Wed, 23 Jun 2021 08:45:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-buster` - linux; 386

```console
$ docker pull postgres@sha256:61ba59cf16ddf319bc84720d7bd6a558f4b42812e3d3257de1811fee8ea5d12b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82731228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653ad69883164787685ed54f626cb98d40be716b4669df47125c9c43e551eba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 00:39:52 GMT
ADD file:62173a7456d614031a7b20be741983644d9723c734eee663b099ad6b47af7b35 in / 
# Wed, 12 May 2021 00:39:53 GMT
CMD ["bash"]
# Wed, 12 May 2021 17:08:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 17:08:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 12 May 2021 17:08:53 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 17:09:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 17:09:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 12 May 2021 17:09:12 GMT
ENV LANG=en_US.utf8
# Wed, 12 May 2021 17:09:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:09:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 17:09:19 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 16 Jun 2021 23:16:14 GMT
ENV PG_MAJOR=10
# Wed, 16 Jun 2021 23:16:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Wed, 16 Jun 2021 23:16:15 GMT
ENV PG_VERSION=10.17-1.pgdg100+1
# Wed, 16 Jun 2021 23:16:31 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 16 Jun 2021 23:16:33 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 16 Jun 2021 23:16:33 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 16 Jun 2021 23:16:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 16 Jun 2021 23:16:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 16 Jun 2021 23:16:35 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 16 Jun 2021 23:16:35 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 16 Jun 2021 23:16:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 16 Jun 2021 23:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Jun 2021 23:16:36 GMT
STOPSIGNAL SIGINT
# Wed, 16 Jun 2021 23:16:36 GMT
EXPOSE 5432
# Wed, 16 Jun 2021 23:16:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9b548256784c8e079e5953ec08bd26ce8cbaed0d606a5d350b4bcd12710d2192`  
		Last Modified: Wed, 12 May 2021 00:46:39 GMT  
		Size: 27.8 MB (27795074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575d2475eb150e7d16bbcdfa247b6f1a3aa6a73693f94eb289f098327fb89bb9`  
		Last Modified: Wed, 12 May 2021 17:15:20 GMT  
		Size: 4.5 MB (4543045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b434d866cd5570a22a7a52ded13a7856fcb343a6d230820fb0022fa841e62363`  
		Last Modified: Wed, 12 May 2021 17:15:18 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffb0fa0b2256116815de20a50cb376412fa098595414c406aeef9c597ee16bb`  
		Last Modified: Wed, 12 May 2021 17:15:18 GMT  
		Size: 1.4 MB (1389738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a94ef8cc2afab34e9eb1f1310432c84a8e2bbc1dd48ab64ab9644b8e6982b23`  
		Last Modified: Wed, 12 May 2021 17:15:19 GMT  
		Size: 8.0 MB (7965150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35d27ddd9d107742d4a8ea8fac6ae5d63fc2a680336806633d79d50521f060f`  
		Last Modified: Wed, 12 May 2021 17:15:16 GMT  
		Size: 398.4 KB (398431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bbcb1012cb3c455f850f3efd71c7fa5d6afbd02c9185fb86240c0e64691863`  
		Last Modified: Wed, 12 May 2021 17:15:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a2d9f699733f0ae6ccc320aa99942739cc83b870955e475870edd0adf767d6`  
		Last Modified: Wed, 12 May 2021 17:15:15 GMT  
		Size: 3.1 KB (3053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f5303650f8e4aee688d566e8fb9a8a80c3f7c999ab7e33b199f86fba035a00`  
		Last Modified: Wed, 16 Jun 2021 23:26:55 GMT  
		Size: 40.6 MB (40621863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf1b93d312ea2f745f86d3f5f4de45a53d67300b44b4f4e8c35e2b522ca64b`  
		Last Modified: Wed, 16 Jun 2021 23:26:36 GMT  
		Size: 8.1 KB (8075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac11f8a0f10ac3cc0f1764604562e06f02276069e77c5de3446fe694be0bbc3`  
		Last Modified: Wed, 16 Jun 2021 23:26:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30171606204c4f3c1a0c6dafabc665ff145bcd46fc46ff59b440a7a60d930139`  
		Last Modified: Wed, 16 Jun 2021 23:26:36 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1379cc4f8929611077099b6b9408384113d7fa399736eca087f81934c9a838`  
		Last Modified: Wed, 16 Jun 2021 23:26:36 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ba2764f07208ec5bf542af1ed60f834c184e7a685e205b797c8a404bacc09`  
		Last Modified: Wed, 16 Jun 2021 23:26:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-buster` - linux; mips64le

```console
$ docker pull postgres@sha256:df459aeaad7cd180f47c1e30de89e917855e4cc25fd53087bb5f5d6c4ffdf347
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78649320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2be05371871f9117b9132b6e7f4c8ed94a384eddb961c316ba265e9fe64f1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 01:09:45 GMT
ADD file:867397d3fb44b3b936a4ff02bbc3a1b760fb6865b5a85efab82fff224f704241 in / 
# Wed, 12 May 2021 01:09:46 GMT
CMD ["bash"]
# Wed, 12 May 2021 12:50:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 12:50:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 12 May 2021 12:51:00 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 12:51:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 12:51:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 12 May 2021 12:51:45 GMT
ENV LANG=en_US.utf8
# Wed, 12 May 2021 12:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 12:52:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 12:52:02 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Thu, 17 Jun 2021 00:39:24 GMT
ENV PG_MAJOR=10
# Thu, 17 Jun 2021 00:39:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Thu, 17 Jun 2021 00:39:24 GMT
ENV PG_VERSION=10.17-1.pgdg100+1
# Thu, 17 Jun 2021 01:15:42 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 17 Jun 2021 01:15:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 17 Jun 2021 01:15:47 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 17 Jun 2021 01:15:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 17 Jun 2021 01:15:49 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 17 Jun 2021 01:15:49 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 17 Jun 2021 01:15:50 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Thu, 17 Jun 2021 01:15:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 17 Jun 2021 01:15:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Jun 2021 01:15:52 GMT
STOPSIGNAL SIGINT
# Thu, 17 Jun 2021 01:15:52 GMT
EXPOSE 5432
# Thu, 17 Jun 2021 01:15:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:09564b0ac149fb24b77cbc75ce6fa5d9ba61bd7c99d11b42bd8339c3bb28e557`  
		Last Modified: Wed, 12 May 2021 01:16:36 GMT  
		Size: 25.8 MB (25812884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711734087a2d95ecb47d73397f83c426824b6dcd118984a2af0667aae286d9ff`  
		Last Modified: Wed, 12 May 2021 14:34:14 GMT  
		Size: 4.2 MB (4182535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1162cdaa5e1cce6b85f005af9858ef960750e330ac30edbcdfa756ea2f2ab4f`  
		Last Modified: Wed, 12 May 2021 14:34:10 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27359d35deb141040e851c50117b5f2d741a454f4e8971acc2fc59bc1bfc8c8b`  
		Last Modified: Wed, 12 May 2021 14:34:11 GMT  
		Size: 1.3 MB (1307413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cec65f9ce0c1e4ae5275e0b87bd64d62e37f2d0773112ff56d47b174cf9694c`  
		Last Modified: Wed, 12 May 2021 14:34:15 GMT  
		Size: 8.0 MB (7964671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdaf7052f544eedd7eba3e8a88181c405de5aac9ed4be8d4df658ed61735054`  
		Last Modified: Wed, 12 May 2021 14:34:07 GMT  
		Size: 389.3 KB (389307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97a2946cea7e515e4776c3b5c7b66c1253652efc6c4afb79018e776d1e2b17d`  
		Last Modified: Wed, 12 May 2021 14:34:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80373f65da43be81495635f60f8834f07b39d7bbaddbe635aded32c7f6ac39f3`  
		Last Modified: Wed, 12 May 2021 14:34:07 GMT  
		Size: 3.1 KB (3054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6c79b0bf6db7301eb2f58faf1d7695887767ca4abf52ed724b7b16886e5b05`  
		Last Modified: Thu, 17 Jun 2021 01:55:30 GMT  
		Size: 39.0 MB (38974662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0753181e1ff0ec39aaa4159c33e5dfc03a34da0c7e0e1b6259fe4d85d9f8ecf4`  
		Last Modified: Thu, 17 Jun 2021 01:54:59 GMT  
		Size: 8.1 KB (8080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737756bb294e3858e7069040aefe25ab9a4d97995c3a9dc40683a2a777eb0745`  
		Last Modified: Thu, 17 Jun 2021 01:54:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44560a79585bbbcedb16e753eadfa5775a2fab1dcbb07abbc16f063f724c955`  
		Last Modified: Thu, 17 Jun 2021 01:54:59 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87d4272491355d14e80ac72a94e6959b1d559181059308d5239af9da93d54b5`  
		Last Modified: Thu, 17 Jun 2021 01:54:59 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9f559ad6cf975b629462e02f0b9c3578b4397bec72d7e02f90ff04ffb62f06`  
		Last Modified: Thu, 17 Jun 2021 01:54:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-buster` - linux; ppc64le

```console
$ docker pull postgres@sha256:e20991fad64cc2a413ce9631d6204ba7e57a4c259e9ab5cdc58b92b44a19c7e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87585080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318df2f752d733cfb911240acbbebd15fe90b762309358a35e175b75677ed43f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 23 Jun 2021 00:30:38 GMT
ADD file:e599654230c9fe95fe2c591dbe60e8a0a886cd053b6117230fbae47561145731 in / 
# Wed, 23 Jun 2021 00:30:46 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 05:37:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 23 Jun 2021 05:38:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 23 Jun 2021 05:38:29 GMT
ENV GOSU_VERSION=1.12
# Wed, 23 Jun 2021 05:40:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 23 Jun 2021 05:40:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 23 Jun 2021 05:40:45 GMT
ENV LANG=en_US.utf8
# Wed, 23 Jun 2021 05:41:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 05:41:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Jun 2021 05:41:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 23 Jun 2021 06:04:24 GMT
ENV PG_MAJOR=10
# Wed, 23 Jun 2021 06:04:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Wed, 23 Jun 2021 06:04:41 GMT
ENV PG_VERSION=10.17-1.pgdg100+1
# Wed, 23 Jun 2021 06:06:41 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 23 Jun 2021 06:06:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 23 Jun 2021 06:07:07 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 23 Jun 2021 06:07:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 23 Jun 2021 06:07:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 23 Jun 2021 06:07:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 23 Jun 2021 06:07:31 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 23 Jun 2021 06:07:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 23 Jun 2021 06:07:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Jun 2021 06:07:55 GMT
STOPSIGNAL SIGINT
# Wed, 23 Jun 2021 06:08:01 GMT
EXPOSE 5432
# Wed, 23 Jun 2021 06:08:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f9cb1946299ce1824ee44809cd0c8b419528fee2f0f89e86400787a14b666f59`  
		Last Modified: Wed, 23 Jun 2021 00:37:07 GMT  
		Size: 30.6 MB (30553627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e89b134563ab5479f4009d9250e3a6f1a4d8cc0ef5abc7a890ca99ce1126de3`  
		Last Modified: Wed, 23 Jun 2021 06:17:54 GMT  
		Size: 5.0 MB (4967553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e28cc873846f676dbfca4597116b0c7ad15feedd60831dee56eacaad3132400`  
		Last Modified: Wed, 23 Jun 2021 06:17:51 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b74c9fea9bcb8291b53cd9f048e240e4b3b5fee457f4774a06fd462820c981`  
		Last Modified: Wed, 23 Jun 2021 06:17:51 GMT  
		Size: 1.3 MB (1338280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8da47b7b3df3323e707894b5e736c54b0ce2e729194b3ce70b867745ff2976`  
		Last Modified: Wed, 23 Jun 2021 06:17:51 GMT  
		Size: 8.0 MB (7965585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50945a7f61624d8dd91059cb1ccf68a7ec2f569c3cbc470e235ed153e49d8558`  
		Last Modified: Wed, 23 Jun 2021 06:17:49 GMT  
		Size: 397.2 KB (397204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d056b9ba09a6e667d3b87d57bfc2628080f8b3e75a39581ddb938e3e6e202d05`  
		Last Modified: Wed, 23 Jun 2021 06:17:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd485720540812fce78b6cb85c9a12688c4d2a19efd314e6f28dd97e0b1d085`  
		Last Modified: Wed, 23 Jun 2021 06:17:48 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df2a893ba34692bf7b4e8623eacf34060dc2d58151e4df403ccd418950df376`  
		Last Modified: Wed, 23 Jun 2021 06:19:31 GMT  
		Size: 42.3 MB (42344877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5e3ef5cccdb238e0dde83f723b6ba18aa37312bd9faf68bbf770acc63d4f74`  
		Last Modified: Wed, 23 Jun 2021 06:19:19 GMT  
		Size: 8.1 KB (8079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d17e5b24336949d81b7b1fc0221c29f95eafaf0ce6ae6b233f7315817a38fa`  
		Last Modified: Wed, 23 Jun 2021 06:19:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80761caffb99cfcf1fe1f96dd5c3c820b148a5706c057aa096d1f84322dbda8f`  
		Last Modified: Wed, 23 Jun 2021 06:19:19 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9570cb647601b88eb2ad8fd15f4fc3d69d464f1a0ff8bec497944f03fa3791e4`  
		Last Modified: Wed, 23 Jun 2021 06:19:19 GMT  
		Size: 4.4 KB (4401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58563f039d311fb89110f4e58600168ceaa43ebe21d1c4e7819a63c1a6e0041`  
		Last Modified: Wed, 23 Jun 2021 06:19:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-buster` - linux; s390x

```console
$ docker pull postgres@sha256:052b8953bfab4cc4a98297b5102478a2e281b49652d12fe9365a0261f3cd730c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79932036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b28b457d05fbbd80d8e31729a017b231cbe59dd55b6835a6f9c809d2c5a279`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Jun 2021 23:42:28 GMT
ADD file:a53e5772eefa4592eeff989f279dcc870986db7207b419dc3ae61cae85fce41f in / 
# Tue, 22 Jun 2021 23:42:29 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 04:28:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 23 Jun 2021 04:28:56 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 23 Jun 2021 04:28:56 GMT
ENV GOSU_VERSION=1.12
# Wed, 23 Jun 2021 04:29:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 23 Jun 2021 04:29:09 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 23 Jun 2021 04:29:09 GMT
ENV LANG=en_US.utf8
# Wed, 23 Jun 2021 04:29:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 04:29:13 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Jun 2021 04:29:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 23 Jun 2021 04:59:21 GMT
ENV PG_MAJOR=10
# Wed, 23 Jun 2021 04:59:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Wed, 23 Jun 2021 04:59:21 GMT
ENV PG_VERSION=10.17-1.pgdg100+1
# Wed, 23 Jun 2021 05:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 23 Jun 2021 05:06:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 23 Jun 2021 05:06:36 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 23 Jun 2021 05:06:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 23 Jun 2021 05:06:37 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 23 Jun 2021 05:06:37 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 23 Jun 2021 05:06:37 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 23 Jun 2021 05:06:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 23 Jun 2021 05:06:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Jun 2021 05:06:38 GMT
STOPSIGNAL SIGINT
# Wed, 23 Jun 2021 05:06:39 GMT
EXPOSE 5432
# Wed, 23 Jun 2021 05:06:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d08eb187b3111e87e1b138f7b93df64c5470da613a64d0adc804e17e12aed4dc`  
		Last Modified: Tue, 22 Jun 2021 23:45:45 GMT  
		Size: 25.8 MB (25760716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99b60ef2b79478040c8c3ca3299039831a30c7badfbe6d16855ad4941822ceb`  
		Last Modified: Wed, 23 Jun 2021 05:16:05 GMT  
		Size: 4.1 MB (4060053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a4a62f2a254f029e3d8c1f8bec27159c961cb7a2ad692510a249552f14f2ab`  
		Last Modified: Wed, 23 Jun 2021 05:16:04 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88a397c68280243551d2da16aa81d6922ad8819e1b6b26602ba4d654a46f21e`  
		Last Modified: Wed, 23 Jun 2021 05:16:04 GMT  
		Size: 1.4 MB (1406172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2815bc875cb001669a840d5480c0cac7fe3fe152756407fd06a2d960cf0af6`  
		Last Modified: Wed, 23 Jun 2021 05:16:04 GMT  
		Size: 8.0 MB (8019461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7ac18883f0c91daaca48b0c6689e54bbf1ff0e4ed9a158596a004d22aa1868`  
		Last Modified: Wed, 23 Jun 2021 05:16:03 GMT  
		Size: 388.4 KB (388375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0858d55bbb1aac6825ed98915f99daffe6d3428b8d4921103c83516e47be507`  
		Last Modified: Wed, 23 Jun 2021 05:16:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8744748438aab69abf849a567b4e0f46d449f975062b55efc5a1fee9118e38`  
		Last Modified: Wed, 23 Jun 2021 05:16:02 GMT  
		Size: 3.1 KB (3055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7035f9c3374b1dedcd39aeed775df8d3ee7525acfae2e79d1e733c9ae8144c`  
		Last Modified: Wed, 23 Jun 2021 05:17:04 GMT  
		Size: 40.3 MB (40279312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e7d0e77613ffb94310158f2c8e76a19d3f34c799685e5968336d1f1e67fd79`  
		Last Modified: Wed, 23 Jun 2021 05:16:56 GMT  
		Size: 8.1 KB (8081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e33c4f110c4ff998c5dbfb7d590383dbbb3aab39453d3562549556759ca2c3a`  
		Last Modified: Wed, 23 Jun 2021 05:16:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a0231bb99b8d8468d74f440ac6162fc2407f4e4d33239fdaab62576a5b642d`  
		Last Modified: Wed, 23 Jun 2021 05:16:56 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ef503227da21787afe66f7a57f526f6114e45bab50075585cff3f2dc564937`  
		Last Modified: Wed, 23 Jun 2021 05:16:56 GMT  
		Size: 4.4 KB (4403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2927cf0c58f4f038cca856715c38726d392d81f3d5e17a2eb3fbf827717c81a`  
		Last Modified: Wed, 23 Jun 2021 05:16:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
