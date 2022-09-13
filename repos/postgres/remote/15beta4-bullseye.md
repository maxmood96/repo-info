## `postgres:15beta4-bullseye`

```console
$ docker pull postgres@sha256:51f480bd962757de1d38bd466b9c683b13f058c44f591df8af33b61d3b73b927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; s390x

### `postgres:15beta4-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:171b3262713b106afac03f8e1b0ba94ff928478b5ff3a8f40d29655d892c630f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139826077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aae18b01095cba481a9cc07acd3109de3d4fb1ace462a8d7c10b27b9781a5e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:50 GMT
ADD file:7726efb0e0eb5003dbcf2967ec29364479eec8b41f2569ff189372153115b54b in / 
# Tue, 23 Aug 2022 00:20:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 12:53:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 23 Aug 2022 12:53:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 23 Aug 2022 12:53:30 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 12:53:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 12:53:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 23 Aug 2022 12:53:46 GMT
ENV LANG=en_US.utf8
# Tue, 23 Aug 2022 12:53:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 12:53:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 12:53:51 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 23 Aug 2022 12:53:51 GMT
ENV PG_MAJOR=15
# Tue, 23 Aug 2022 12:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Sep 2022 22:45:27 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Mon, 12 Sep 2022 22:45:49 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Mon, 12 Sep 2022 22:45:50 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Mon, 12 Sep 2022 22:45:51 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 12 Sep 2022 22:45:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Sep 2022 22:45:52 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 12 Sep 2022 22:45:52 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Sep 2022 22:45:52 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Mon, 12 Sep 2022 22:45:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 22:45:52 GMT
STOPSIGNAL SIGINT
# Mon, 12 Sep 2022 22:45:52 GMT
EXPOSE 5432
# Mon, 12 Sep 2022 22:45:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7a6db449b51b92eac5c81cdbd82917785343f1664b2be57b22337b0a40c5b29d`  
		Last Modified: Tue, 23 Aug 2022 00:24:59 GMT  
		Size: 31.4 MB (31381485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f184bc070460801a91ee94a8121f597d61d2fcda0728eba67c35d4bfa789bc`  
		Last Modified: Tue, 23 Aug 2022 12:57:33 GMT  
		Size: 4.4 MB (4414828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606a73c0d34a44356777ffdcdc858c71427825329879a59f1c65356756559a07`  
		Last Modified: Tue, 23 Aug 2022 12:57:32 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39f1600d2b6e26d0ec2a14525c06f9a8f3cbb48e97dfcf372e7efe40f6ada59`  
		Last Modified: Tue, 23 Aug 2022 12:57:32 GMT  
		Size: 1.4 MB (1418437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f42f92b0fea8d74cf3065faabc70e486ce3683c69f133085de28535dab9025`  
		Last Modified: Tue, 23 Aug 2022 12:57:32 GMT  
		Size: 8.0 MB (8045444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b67d2b035449a14ec0ab9b722c7774957ffcfffa1aeb43046b1591cc09f784`  
		Last Modified: Tue, 23 Aug 2022 12:57:30 GMT  
		Size: 1.3 MB (1261166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31107b8480ee255d828effb0d51e19812eb2860b2b88cf51f67e78197105d685`  
		Last Modified: Tue, 23 Aug 2022 12:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26434cf8bfafac28ea2de3c0875a7f09bfa8c814ed419b2faad55a327f56201`  
		Last Modified: Tue, 23 Aug 2022 12:57:30 GMT  
		Size: 3.2 KB (3201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0e9e04c80de4d12d130196649e21b4f93c1d3f9156c3c3e22961f21544f0b1`  
		Last Modified: Mon, 12 Sep 2022 22:50:40 GMT  
		Size: 93.3 MB (93284739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be7180c63a11558b4d609a09d1d983697a1588f7664436180c26c2f556b896c`  
		Last Modified: Mon, 12 Sep 2022 22:50:27 GMT  
		Size: 9.8 KB (9798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686ce1ac0939254b2973cce9c0828b5081108e43ca285870cd7a7eaa7af704e7`  
		Last Modified: Mon, 12 Sep 2022 22:50:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed4dae899d559c9f8aac81e47c6c2b10ee855cab7444df8ccdf43523cc62e3e`  
		Last Modified: Mon, 12 Sep 2022 22:50:27 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf6d1cc3d24d3ca317687c6a5c2347613cdbab16eb4c8e03d516da92b171dad`  
		Last Modified: Mon, 12 Sep 2022 22:50:27 GMT  
		Size: 4.7 KB (4700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta4-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:2bbd9c935fdb8ae50d5d3daa7ff9ee215d440ffc2276557b00c4e59af960362b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138443223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf72d94f8030f80458e361a29b01dbcd905c6fddce9e5b5dd9fe819482b0516`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Aug 2022 01:17:14 GMT
ADD file:83fb076a50e935419eb0db2bd97477d7ed5f16aaac4c8cc35a4a69ac612df327 in / 
# Tue, 23 Aug 2022 01:17:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 10:28:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 23 Aug 2022 10:28:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 23 Aug 2022 10:28:51 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 10:29:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 10:29:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 23 Aug 2022 10:29:11 GMT
ENV LANG=en_US.utf8
# Tue, 23 Aug 2022 10:29:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 10:29:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 10:29:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 23 Aug 2022 10:29:20 GMT
ENV PG_MAJOR=15
# Tue, 23 Aug 2022 10:29:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Sep 2022 22:48:36 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Mon, 12 Sep 2022 23:09:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Mon, 12 Sep 2022 23:09:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Mon, 12 Sep 2022 23:09:49 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 12 Sep 2022 23:09:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Sep 2022 23:09:50 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 12 Sep 2022 23:09:50 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Sep 2022 23:09:50 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Mon, 12 Sep 2022 23:09:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 23:09:50 GMT
STOPSIGNAL SIGINT
# Mon, 12 Sep 2022 23:09:51 GMT
EXPOSE 5432
# Mon, 12 Sep 2022 23:09:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:74eb5afab626122970f8620ac001fcc4a200725acb05519b85aba47a38bf1016`  
		Last Modified: Tue, 23 Aug 2022 01:22:44 GMT  
		Size: 28.9 MB (28917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52aecbb9e51f074914a644e856b81dca28a3198671b7863584888136f6a99aa4`  
		Last Modified: Tue, 23 Aug 2022 11:49:54 GMT  
		Size: 4.1 MB (4096474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44506c04ae4f4d944b20da0f1e83e265af76be7f70c6e3d94be80bd00985d48`  
		Last Modified: Tue, 23 Aug 2022 11:49:52 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc3932cf3d3d58ab39e64f703d9d675dd31ee6a7a79d2922dc8f203eba513a3`  
		Last Modified: Tue, 23 Aug 2022 11:49:52 GMT  
		Size: 1.4 MB (1382635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa1c913864a0709b3be92bd4610120ca5dc65895317ecdf0223b771145772c0`  
		Last Modified: Tue, 23 Aug 2022 11:49:52 GMT  
		Size: 8.0 MB (8045415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8064c12df36655a819e68fd378819ed4d05dafe04bb8fb490d37fc1808938a0`  
		Last Modified: Tue, 23 Aug 2022 11:49:50 GMT  
		Size: 1.3 MB (1257270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c08d76f34a6ab809b059881a4271dee0bc678a27064395d70979183a8bcbb5`  
		Last Modified: Tue, 23 Aug 2022 11:49:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4ae14a54a47a76d72c20c00c3679ba421117e56ba1cd823038def9c64798b4`  
		Last Modified: Tue, 23 Aug 2022 11:49:48 GMT  
		Size: 3.2 KB (3199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbd302d5ff18a1625ca8220197630f1f05062793f38ef6c0be22e3bf35239c3`  
		Last Modified: Mon, 12 Sep 2022 23:11:58 GMT  
		Size: 94.7 MB (94724196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da017048a0e62ac6eac895f4457da9be2023dab9dd06342c475040f4b9a8258`  
		Last Modified: Mon, 12 Sep 2022 23:11:33 GMT  
		Size: 9.8 KB (9804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94468111d8ca1142b2f7481a62811e4be928f009c17f991aa7388c40bec82149`  
		Last Modified: Mon, 12 Sep 2022 23:11:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94c97fdaad8db70aefbbcc045de51ab3fae4858fe7459a613b9da4ed3468e51`  
		Last Modified: Mon, 12 Sep 2022 23:11:33 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7303d586e86372ee206a60b068e9c52ec068508549df12d9de5c5e1442d157ff`  
		Last Modified: Mon, 12 Sep 2022 23:11:33 GMT  
		Size: 4.7 KB (4703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta4-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:506206f0615b2db85e16481215e6a8e57c3210e89ff2c38a6a3a5f933a7bdd9d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132747485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9fb532376d818e9edb731ccdfe745e935b090b8bdf04f4bc1514edb1a46ccc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Aug 2022 01:43:01 GMT
ADD file:4cd1b4287674228db28402a76aa4f241740585448be48b5b15068d275ee9eb84 in / 
# Tue, 23 Aug 2022 01:43:01 GMT
CMD ["bash"]
# Wed, 24 Aug 2022 12:07:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 24 Aug 2022 12:07:38 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 24 Aug 2022 12:07:38 GMT
ENV GOSU_VERSION=1.14
# Wed, 24 Aug 2022 12:07:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 24 Aug 2022 12:07:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 24 Aug 2022 12:07:52 GMT
ENV LANG=en_US.utf8
# Wed, 24 Aug 2022 12:07:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Aug 2022 12:07:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 24 Aug 2022 12:07:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 24 Aug 2022 12:07:57 GMT
ENV PG_MAJOR=15
# Wed, 24 Aug 2022 12:07:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Sep 2022 21:58:06 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Mon, 12 Sep 2022 22:14:36 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Mon, 12 Sep 2022 22:14:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Mon, 12 Sep 2022 22:14:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 12 Sep 2022 22:14:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Sep 2022 22:14:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 12 Sep 2022 22:14:38 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Sep 2022 22:14:38 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Mon, 12 Sep 2022 22:14:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 22:14:39 GMT
STOPSIGNAL SIGINT
# Mon, 12 Sep 2022 22:14:39 GMT
EXPOSE 5432
# Mon, 12 Sep 2022 22:14:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:051ba72559abd0cf65b34b75605580f58636ec3cb994f97de317632a85d82761`  
		Last Modified: Tue, 23 Aug 2022 01:50:05 GMT  
		Size: 26.6 MB (26571732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb8074ebb3b480a1e18555c7115ba4ec7cf13bda955907aa038a62518ba6651`  
		Last Modified: Wed, 24 Aug 2022 13:19:16 GMT  
		Size: 3.7 MB (3717178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f0a2bd27dfd1f00776c2539337d58651f616ef7c81e169ac3398d6d9c45aad`  
		Last Modified: Wed, 24 Aug 2022 13:19:15 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ac77b2a195e4d3fbabb7b78f3a0c5c353e75689e7828c93161c7cad1c1bee0`  
		Last Modified: Wed, 24 Aug 2022 13:19:15 GMT  
		Size: 1.4 MB (1375272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0587534cc7fb1ac3bac1149013b9d3829bdd18592a66b8dc1b742d5b45d2976`  
		Last Modified: Wed, 24 Aug 2022 13:19:14 GMT  
		Size: 8.0 MB (8045344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5a030a2b718eee25b4ea2deedcf8823ecd7af5f7e06c5dcb80baedee72f5cc`  
		Last Modified: Wed, 24 Aug 2022 13:19:12 GMT  
		Size: 1.1 MB (1131161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6cc4a7581b10bc36717bbf2636688fced90c954007320bdde23771506e8f1b`  
		Last Modified: Wed, 24 Aug 2022 13:19:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ea7b7ff3ef0ec74bb6a4d5e9d8d23799dca3901eade772a52ab068735ac525`  
		Last Modified: Wed, 24 Aug 2022 13:19:12 GMT  
		Size: 3.2 KB (3203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7ceb03f9b1b22f9a593e4df70a7153657c95a69458b9b1241e4edff9999195`  
		Last Modified: Mon, 12 Sep 2022 22:24:24 GMT  
		Size: 91.9 MB (91886826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91bf27a3e0335ee84a41f4954eb88538e304d3e8a2fa0ef32ab83cb3463af0e`  
		Last Modified: Mon, 12 Sep 2022 22:24:08 GMT  
		Size: 9.8 KB (9803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7186bb3399f8a2b2dd5d948bcd7ce8139c558b92e2dfe21571e0b09ac6acbfaa`  
		Last Modified: Mon, 12 Sep 2022 22:24:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a4b2bfcbe195bef11ce97818d464ac0f3f8675b1d8592ef57279c3ee419f00`  
		Last Modified: Mon, 12 Sep 2022 22:24:08 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e12bb132dc70a880b711fc427b101652bc97374442a72c5d70ef7e5a06295a`  
		Last Modified: Mon, 12 Sep 2022 22:24:08 GMT  
		Size: 4.7 KB (4700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta4-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:764b3e400f3de423d0e281d2895ada65bfd2f58b302958820f224327a18c9cc0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134488001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66b2d576d235233c49e513ec6e20268f825b45953add1e60603820de522b9b92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 16:47:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 23 Aug 2022 16:47:18 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 23 Aug 2022 16:47:19 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 16:47:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 16:47:34 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 23 Aug 2022 16:47:34 GMT
ENV LANG=en_US.utf8
# Tue, 23 Aug 2022 16:47:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 16:47:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 16:47:41 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 23 Aug 2022 16:47:41 GMT
ENV PG_MAJOR=15
# Tue, 23 Aug 2022 16:47:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Sep 2022 23:25:35 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Mon, 12 Sep 2022 23:25:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Mon, 12 Sep 2022 23:25:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Mon, 12 Sep 2022 23:25:57 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 12 Sep 2022 23:25:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Sep 2022 23:25:59 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 12 Sep 2022 23:26:00 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Sep 2022 23:26:02 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Mon, 12 Sep 2022 23:26:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 23:26:03 GMT
STOPSIGNAL SIGINT
# Mon, 12 Sep 2022 23:26:04 GMT
EXPOSE 5432
# Mon, 12 Sep 2022 23:26:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdf6ae07fecdb4c831db9dba73665ef01dc504538c3cafd5390975884b8c75e`  
		Last Modified: Tue, 23 Aug 2022 16:53:36 GMT  
		Size: 4.2 MB (4209305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39d206d157171c87654dec4d9ca2d67498d1c023318f6dd8da2fc60b96b76c1`  
		Last Modified: Tue, 23 Aug 2022 16:53:35 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d23609ca819cfb485e710ba973926866b84e67b67b7766a05d7bfcbd4553d06`  
		Last Modified: Tue, 23 Aug 2022 16:53:35 GMT  
		Size: 1.3 MB (1346175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283c8a53ad54d1782bfc60760bcf0ba74d46d0e574b8c6b3974405a680ff9841`  
		Last Modified: Tue, 23 Aug 2022 16:53:34 GMT  
		Size: 8.0 MB (8043746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badf8d755b5305a74ac039d0a8eee7d398a8a3f96ee7846b66919128b091d033`  
		Last Modified: Tue, 23 Aug 2022 16:53:33 GMT  
		Size: 1.0 MB (1025856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b35e38850e5b1f584e3f7b3921bbfd858e4e6da87b81c1abe520c0bb449e69`  
		Last Modified: Tue, 23 Aug 2022 16:53:32 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc27ced20187d2a59b16e397ac6fa5b44e569d71197739b81ba841b02e360d4`  
		Last Modified: Tue, 23 Aug 2022 16:53:32 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9acc2dab2a004ec84be811a95e947ed8915893ffef88df095963fa417366e8`  
		Last Modified: Mon, 12 Sep 2022 23:32:14 GMT  
		Size: 89.8 MB (89779419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f60d211325140e8babe62dcd324df32490a4eb98bd2cd19b45aec501a777c8c`  
		Last Modified: Mon, 12 Sep 2022 23:32:01 GMT  
		Size: 9.8 KB (9801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbebf2020c2e5ebaf7532d12ef603a60ccdfa3f6023a1969935be85b47b52dd`  
		Last Modified: Mon, 12 Sep 2022 23:32:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7511e64a092ea3b4f2f9e23c33c439e7014a7bb4ef77c35f0ca48c8c7e6fe39`  
		Last Modified: Mon, 12 Sep 2022 23:32:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a394777408eba2584d68509268e64c6d99c5540d73419cdff0c005e478ae723`  
		Last Modified: Mon, 12 Sep 2022 23:32:01 GMT  
		Size: 4.7 KB (4703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta4-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:f11e2eab65dff1a27f2a2b171eb81f102e44bcb8337071e007d359eec49831d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147454877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fa1427bda271d3e4d51e1e93ea2c48e5e4612898c3d3d56b5e5ce49e02ccb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Aug 2022 01:02:40 GMT
ADD file:5ca62c98116941aaa64ec72afb689a088c46f75a3e83d5b0d4e58d65ec905ccd in / 
# Tue, 23 Aug 2022 01:02:40 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 06:30:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 23 Aug 2022 06:30:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 23 Aug 2022 06:30:56 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 06:31:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 06:31:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 23 Aug 2022 06:31:12 GMT
ENV LANG=en_US.utf8
# Tue, 23 Aug 2022 06:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 06:31:18 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 06:31:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 23 Aug 2022 06:31:21 GMT
ENV PG_MAJOR=15
# Tue, 23 Aug 2022 06:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Sep 2022 22:46:32 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Mon, 12 Sep 2022 23:00:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Mon, 12 Sep 2022 23:00:09 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Mon, 12 Sep 2022 23:00:10 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 12 Sep 2022 23:00:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Sep 2022 23:00:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 12 Sep 2022 23:00:13 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Sep 2022 23:00:15 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Mon, 12 Sep 2022 23:00:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 23:00:16 GMT
STOPSIGNAL SIGINT
# Mon, 12 Sep 2022 23:00:17 GMT
EXPOSE 5432
# Mon, 12 Sep 2022 23:00:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6b3cb4a05a891d9d8a87a2bd7247b16f79832a9d4afbad3ff5068f6fc2ba1560`  
		Last Modified: Tue, 23 Aug 2022 01:08:25 GMT  
		Size: 32.4 MB (32387317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becb9427d62793f7174c7658bf6a42f149b511e602e1a64de75ef4ed03d7a02f`  
		Last Modified: Tue, 23 Aug 2022 07:48:30 GMT  
		Size: 4.6 MB (4607344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163380a1f39a9822e0726fd5924e4f3d127709e25887702aa338ba9eb3491d4e`  
		Last Modified: Tue, 23 Aug 2022 07:48:29 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ee8e41d5b51a96857af5720aac0ab48e2994ffd6876cbb04e1ea7435dd421f`  
		Last Modified: Tue, 23 Aug 2022 07:48:29 GMT  
		Size: 1.4 MB (1385136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc6c94e1f0448b209a2dce566ee6d7e75ae0c45ffbb0e3e71bd2ebb82589796`  
		Last Modified: Tue, 23 Aug 2022 07:48:28 GMT  
		Size: 8.0 MB (8043576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e1460a22fa1e33c2c5da94359ac31b7bf0bb3d01ad6ca2772571494e4b787c`  
		Last Modified: Tue, 23 Aug 2022 07:48:27 GMT  
		Size: 1.0 MB (1027945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869c94cf7ad6c7c9b6c405c1c105a764b195ced65c540e07ece5f69be2c04405`  
		Last Modified: Tue, 23 Aug 2022 07:48:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa77e423ef6a8cc121f24291a4371fd8ed0db0c89bb2fd637cfa5ad0f167116`  
		Last Modified: Tue, 23 Aug 2022 07:48:26 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784baddd8824211daf20b82b3814b2ac747c63be5b201dc26291a01d8e8b1fec`  
		Last Modified: Mon, 12 Sep 2022 23:07:09 GMT  
		Size: 100.0 MB (99983853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3a943ee05d62cad598442dececab6522318a5a112658acd4fd9c4d7dc8c73c`  
		Last Modified: Mon, 12 Sep 2022 23:06:56 GMT  
		Size: 9.8 KB (9801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484769546455166d44fc6f06b728317a16799e1e22ca90f7a8c788f85f7499fd`  
		Last Modified: Mon, 12 Sep 2022 23:06:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73feeba2da7f0aa9987f7cc72d0bd3ec24d2266b8a0b18a5ab3776775b28e4a0`  
		Last Modified: Mon, 12 Sep 2022 23:06:56 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5022b0dace3fe7ca9b2791252ba5d740d8ac5b06a0d6b3f809cafa84b371a74`  
		Last Modified: Mon, 12 Sep 2022 23:06:56 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta4-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:1758adf5e5df49e3bbd44c16d3e262baad10afa5eed4efa5260046b868cb9096
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139712701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600e9f2723789b6aba19168e36760d84ac92d620dcb9aba6a5e14f2cf8dfad97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Aug 2022 00:11:17 GMT
ADD file:37d58e8a76488fed0f1ebafd3ee993569a3c611b3a5d93400485783112b71386 in / 
# Tue, 23 Aug 2022 00:11:22 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:10:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 23 Aug 2022 11:10:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 23 Aug 2022 11:10:13 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 11:10:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 11:11:15 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 23 Aug 2022 11:11:18 GMT
ENV LANG=en_US.utf8
# Tue, 23 Aug 2022 11:11:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:11:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 11:11:48 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 23 Aug 2022 11:11:51 GMT
ENV PG_MAJOR=15
# Tue, 23 Aug 2022 11:11:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Sep 2022 22:07:58 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Mon, 12 Sep 2022 23:09:18 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Mon, 12 Sep 2022 23:09:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Mon, 12 Sep 2022 23:09:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 12 Sep 2022 23:09:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Sep 2022 23:09:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 12 Sep 2022 23:09:42 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Sep 2022 23:09:45 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Mon, 12 Sep 2022 23:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 23:09:51 GMT
STOPSIGNAL SIGINT
# Mon, 12 Sep 2022 23:09:54 GMT
EXPOSE 5432
# Mon, 12 Sep 2022 23:09:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0e8d4fbcc8d2fc93de0170727f6e48b6fc7ec8931443fbda8a8cd154dc6f7d36`  
		Last Modified: Tue, 23 Aug 2022 00:19:35 GMT  
		Size: 29.6 MB (29639012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a601248a592e2cb77b5c5fbe5df7aec2ad1fe31b95cbda4bb4af60efc4036a`  
		Last Modified: Tue, 23 Aug 2022 16:44:53 GMT  
		Size: 4.2 MB (4196214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc21c3fd96498a0618121f229b7b0fc4460d23384212c37565d98ab0b651495b`  
		Last Modified: Tue, 23 Aug 2022 16:44:48 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa20e00a44fc5a13bd46cf6370f87c3374ab4f89fff4108ca154c283275ef57`  
		Last Modified: Tue, 23 Aug 2022 16:44:48 GMT  
		Size: 1.3 MB (1298025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b835238ea78899b2841f8f08bc93d9a70c7f66b392b3c2cdd212a41b97f7a55c`  
		Last Modified: Tue, 23 Aug 2022 16:44:53 GMT  
		Size: 8.0 MB (8044012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f874219aab3bce6d9aecaa587f86af1abb5698d0edf4c55a3594b1474147cf2`  
		Last Modified: Tue, 23 Aug 2022 16:44:46 GMT  
		Size: 1.1 MB (1089496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997f2279f0bd8e61daf0e558372e02c64a8583fddeae89d3653ad7b73305da06`  
		Last Modified: Tue, 23 Aug 2022 16:44:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9242979b94591f43e17eb7a6189c8ca8c01d0d78950bc956940f0cbe3106ce`  
		Last Modified: Tue, 23 Aug 2022 16:44:45 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85405f28aa97d1af09dd574904eb60f196f0a7467ac03e63eb3b55752ac651ab`  
		Last Modified: Mon, 12 Sep 2022 23:11:43 GMT  
		Size: 95.4 MB (95426218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4352ff9e637c791350f839343cd8f9c34ac3b3b498e7387d07df8ef81649092`  
		Last Modified: Mon, 12 Sep 2022 23:10:42 GMT  
		Size: 9.8 KB (9811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087b943ae28d16192f0e546f79813a181632ec11500c16c1c4f8f3a214bcf956`  
		Last Modified: Mon, 12 Sep 2022 23:10:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e03b35db13f9c480eaa04e2cfdd908daea2389438a5b929fa501d73d76736dc`  
		Last Modified: Mon, 12 Sep 2022 23:10:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9c12001b4e7dcb13a7c1aef849b263a672ad1c70956a3da19c8eb3ddba9ae5`  
		Last Modified: Mon, 12 Sep 2022 23:10:42 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta4-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:1aa88cf905d1a28e9f6404d90f61ff4ce3257c23fb71b882f6528782f04cc2d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92135581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96ce45983e7ae0054601a6ddf00726a897b5e0c0b7d85257481e6178e826f62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Aug 2022 00:54:01 GMT
ADD file:7e494cf2e639edf0f0ce27e06887b8488570da37c5fce0a889687622d8cd443e in / 
# Tue, 23 Aug 2022 00:54:03 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 12:09:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 23 Aug 2022 12:09:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 23 Aug 2022 12:09:36 GMT
ENV GOSU_VERSION=1.14
# Tue, 23 Aug 2022 12:09:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 23 Aug 2022 12:09:47 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 23 Aug 2022 12:09:47 GMT
ENV LANG=en_US.utf8
# Tue, 23 Aug 2022 12:09:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 12:09:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 23 Aug 2022 12:09:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 23 Aug 2022 12:09:52 GMT
ENV PG_MAJOR=15
# Tue, 23 Aug 2022 12:09:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 12 Sep 2022 22:51:50 GMT
ENV PG_VERSION=15~beta4-1.pgdg110+1
# Mon, 12 Sep 2022 22:59:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Mon, 12 Sep 2022 22:59:10 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Mon, 12 Sep 2022 22:59:10 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 12 Sep 2022 22:59:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 12 Sep 2022 22:59:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 12 Sep 2022 22:59:11 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 12 Sep 2022 22:59:11 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Mon, 12 Sep 2022 22:59:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 12 Sep 2022 22:59:12 GMT
STOPSIGNAL SIGINT
# Mon, 12 Sep 2022 22:59:12 GMT
EXPOSE 5432
# Mon, 12 Sep 2022 22:59:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1c2e5a5a3305e50395bba8974e6c201849f83c07fb0ad036111055f59157c7ff`  
		Last Modified: Tue, 23 Aug 2022 01:04:36 GMT  
		Size: 29.7 MB (29650094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaae8b3f3177b2e7f1cc1c2bdc2f58e2e757e009afcb4b2f05a8eb4ca15932f`  
		Last Modified: Tue, 23 Aug 2022 12:52:03 GMT  
		Size: 4.3 MB (4302282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb5658447e2cfe1a26d6f27aac5cf8d1f6bc4f22a7555f67e44689a3e4d4308`  
		Last Modified: Tue, 23 Aug 2022 12:52:02 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9595ad34963d694bd3856090b77885ea8a2614f15e453893eb6fb3e15ce02187`  
		Last Modified: Tue, 23 Aug 2022 12:52:02 GMT  
		Size: 1.4 MB (1381590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2887f3dc6cbb5fedc56c945f6768541dab332b2cff0bbe74e8202025238609`  
		Last Modified: Tue, 23 Aug 2022 12:52:02 GMT  
		Size: 8.1 MB (8099117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cd1b5b2e3c167091b0c1006900c9204fe71d8949f3eacf3c2a6b64f85a9d30`  
		Last Modified: Tue, 23 Aug 2022 12:52:01 GMT  
		Size: 1.2 MB (1237911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e57daa6420a8621fc69b4a2e30b3fd238f291b8bfaf2e779044314629c5cf22`  
		Last Modified: Tue, 23 Aug 2022 12:52:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d443c42a103c71b47d721d7013fe9198019c49b1a1358d7b5d129b4daf6ac1`  
		Last Modified: Tue, 23 Aug 2022 12:52:01 GMT  
		Size: 3.2 KB (3194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a021f2fdea8dd370cb1fc9d4fd850bc8e352fc770d414a579761ee4cd8c5f7`  
		Last Modified: Mon, 12 Sep 2022 23:15:19 GMT  
		Size: 47.4 MB (47444605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad032ae17d297c5757d6fe45dd4c5917d968f7923e012a596c3e3d4120b05d5e`  
		Last Modified: Mon, 12 Sep 2022 23:15:13 GMT  
		Size: 9.8 KB (9804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35de39b5364a2c855cde07f061c60839ac13f486ab2ebfac5294e1ddefa2ee94`  
		Last Modified: Mon, 12 Sep 2022 23:15:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0aee2ddb5830983853f0b86262667ac52d7699c7e45c308377f339579436c9`  
		Last Modified: Mon, 12 Sep 2022 23:15:13 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2037dadb7d5948dd4d195f7eb9350d61ba3249e2ae458d47381970f3e518b9cb`  
		Last Modified: Mon, 12 Sep 2022 23:15:13 GMT  
		Size: 4.7 KB (4702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
