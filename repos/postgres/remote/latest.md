## `postgres:latest`

```console
$ docker pull postgres@sha256:d28958eeabb54cacf0562886656c8af56cdb379caf6a849c1e69f78ff65d8c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `postgres:latest` - linux; amd64

```console
$ docker pull postgres@sha256:28b6d7ddb558b7117b2be70d03e73b1c132ebc169a108f7f59add3fffbe6d30e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136932609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d191afba1bb1ee80e06afbdca13962b6f3ac9900df5e8d3a4a9f06e8188a8bac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 12:16:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 12:16:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 12 Oct 2021 12:16:10 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Oct 2021 12:16:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Oct 2021 12:16:33 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 12 Oct 2021 12:16:33 GMT
ENV LANG=en_US.utf8
# Tue, 12 Oct 2021 12:16:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 12:16:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Oct 2021 12:16:49 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 12 Oct 2021 12:16:49 GMT
ENV PG_MAJOR=14
# Tue, 12 Oct 2021 12:16:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 12 Oct 2021 12:16:50 GMT
ENV PG_VERSION=14.0-1.pgdg110+1
# Tue, 12 Oct 2021 12:17:10 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 12 Oct 2021 12:17:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 12 Oct 2021 12:17:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 12 Oct 2021 12:17:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 12 Oct 2021 12:17:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 12 Oct 2021 12:17:14 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 12 Oct 2021 12:17:14 GMT
COPY file:39dd79c055f47ef80495def6993f3e85eb124d02824dc47db35d1043455e54bc in /usr/local/bin/ 
# Tue, 12 Oct 2021 12:17:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 12:17:14 GMT
STOPSIGNAL SIGINT
# Tue, 12 Oct 2021 12:17:15 GMT
EXPOSE 5432
# Tue, 12 Oct 2021 12:17:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad0f9d5f5fe21c0fa3ac99c08cf068480bdd2ebc09adce4b81767b0df509bd7`  
		Last Modified: Tue, 12 Oct 2021 12:24:27 GMT  
		Size: 4.4 MB (4414499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff74a7a559cbdfbf9d23234053849d1056dae0e2e7f69671d5bec47661a0d4ef`  
		Last Modified: Tue, 12 Oct 2021 12:24:25 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43dfd845683c4cebbcd3cbdb95bf611fc7a7e88ce3fc709c9675380153a9379`  
		Last Modified: Tue, 12 Oct 2021 12:24:25 GMT  
		Size: 1.5 MB (1450540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e554331369f5844d7ddd374c4536d8e26d0ef0df5d35ff87993f2c8fe6eb74bd`  
		Last Modified: Tue, 12 Oct 2021 12:24:25 GMT  
		Size: 8.0 MB (8045166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25d54a3ac3a7d1bae47256b879f56f92f3f36ef4801e6d5f27300b1449d5035`  
		Last Modified: Tue, 12 Oct 2021 12:24:23 GMT  
		Size: 441.6 KB (441564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc6df00588cd9e292196b96ffb30750e92b07f02165662b35a21a3ae965c291`  
		Last Modified: Tue, 12 Oct 2021 12:24:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4deb2e8648094c506b62bb26ea709e6845b5ab79bef7820be29f959a4ebf8e0`  
		Last Modified: Tue, 12 Oct 2021 12:24:23 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb59c7cc00aa5043ad93fcfb6a226171a3bd316efdb27ae80a197510836cc717`  
		Last Modified: Tue, 12 Oct 2021 12:24:35 GMT  
		Size: 91.2 MB (91204112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c65de4873098fd10a0e66aaab37b7436624c768883652ad842114d765087cc`  
		Last Modified: Tue, 12 Oct 2021 12:24:20 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1525521889be58770d95efa311e7315b6e76ab66bfddb6dae4a48b5401488346`  
		Last Modified: Tue, 12 Oct 2021 12:24:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38df9e245e81f0db13e271b9f222fa7e18afdd8c0dbb0dd41385e8b51929fdd4`  
		Last Modified: Tue, 12 Oct 2021 12:24:20 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380030b85e818f468e04b72b57f533f25d595609b7da12d0b4802304a8187269`  
		Last Modified: Tue, 12 Oct 2021 12:24:20 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; arm variant v5

```console
$ docker pull postgres@sha256:f3f4b4a38d3a55a8d2aafc6e0d7f691961b7599265204ef28390a1017b1cb297
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130234311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905fc13cbc075fe7d1379e61a5d0795f653911182b7c2329a75cd5ee48cf4f97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 28 Sep 2021 01:50:38 GMT
ADD file:da0067258fc1c6a50273e6b3b2673e88fad974a5a1fe4d5eecfeca2df1ff54b3 in / 
# Tue, 28 Sep 2021 01:50:39 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 04:21:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 28 Sep 2021 04:21:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 28 Sep 2021 04:21:52 GMT
ENV GOSU_VERSION=1.12
# Tue, 28 Sep 2021 04:22:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 28 Sep 2021 04:22:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 28 Sep 2021 04:22:39 GMT
ENV LANG=en_US.utf8
# Tue, 28 Sep 2021 04:22:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 04:22:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Sep 2021 04:22:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 28 Sep 2021 04:22:56 GMT
ENV PG_MAJOR=14
# Tue, 28 Sep 2021 04:22:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Fri, 01 Oct 2021 01:10:11 GMT
ENV PG_VERSION=14.0-1.pgdg110+1
# Fri, 01 Oct 2021 01:47:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 01 Oct 2021 01:47:41 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 01 Oct 2021 01:47:43 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 01 Oct 2021 01:47:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 01 Oct 2021 01:47:45 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 01 Oct 2021 01:47:45 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 01 Oct 2021 01:47:46 GMT
COPY file:39dd79c055f47ef80495def6993f3e85eb124d02824dc47db35d1043455e54bc in /usr/local/bin/ 
# Fri, 01 Oct 2021 01:47:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 01:47:47 GMT
STOPSIGNAL SIGINT
# Fri, 01 Oct 2021 01:47:47 GMT
EXPOSE 5432
# Fri, 01 Oct 2021 01:47:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:86f2b8be18fc44e8eb430e2c472979a79cda6eb6fa3add10cc8c5d8764eb90ac`  
		Last Modified: Tue, 28 Sep 2021 02:06:35 GMT  
		Size: 28.9 MB (28910670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d30eb8504c56819605185af701845341d8975e406423278405097f62af2306`  
		Last Modified: Tue, 28 Sep 2021 08:52:54 GMT  
		Size: 4.1 MB (4096354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a243eeeaa2c00737bdd6e98a1fa9a012a7867782cf48628d9ff8924d18b9f18`  
		Last Modified: Tue, 28 Sep 2021 08:52:52 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11403c7ba143852cedde2cb5fc5d9667ab0334c046a7c9ebc8c7850e05fb9c83`  
		Last Modified: Tue, 28 Sep 2021 08:52:52 GMT  
		Size: 1.4 MB (1409777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f8edfacdf52bfedbf204f96cfb85a0e19c8565f7466afdffca94537cd94624`  
		Last Modified: Tue, 28 Sep 2021 08:52:57 GMT  
		Size: 8.0 MB (8045267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823170a97ccf0c83730d7cc699ed2b8cc784fa3a3a434fca8d95389d5a47dee3`  
		Last Modified: Tue, 28 Sep 2021 08:52:50 GMT  
		Size: 439.8 KB (439807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b92b828995d7ff6cb1b2a36baf84eadb6717f6070738cd8e1f2e79abdb34e6`  
		Last Modified: Tue, 28 Sep 2021 08:52:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a0b55cf0d04e78b149e19f243e52ab82558abba6430057c63594f69cc4f8b0`  
		Last Modified: Tue, 28 Sep 2021 08:52:50 GMT  
		Size: 3.1 KB (3054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2916215d1453c885a0d2caf9f63035d5b656a5c704f9974044c09a62779da26`  
		Last Modified: Fri, 01 Oct 2021 02:29:40 GMT  
		Size: 87.3 MB (87313022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6052abaca1fb4ad40f1c713649a01fd586e67279fd0ba84739eba53472fe3f9`  
		Last Modified: Fri, 01 Oct 2021 02:28:45 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7fc9c756086b9f707dfa85647a851f9ac4fefe873a8b247028d04b112a5b3b`  
		Last Modified: Fri, 01 Oct 2021 02:28:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e2f2065dfa0ba7d8721a0116c86a49584a3b38165459f974de5786f4eed071`  
		Last Modified: Fri, 01 Oct 2021 02:28:45 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25bd345bc8ec059596452255e80da8d57584dd34a8fc764c9235dbdc58c6a77`  
		Last Modified: Fri, 01 Oct 2021 02:28:45 GMT  
		Size: 4.6 KB (4560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; arm variant v7

```console
$ docker pull postgres@sha256:054a0dfc211336545a5328a11f907662e7d3df83658435e06c05fc18f5ddf796
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125031338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a58a62e119ec80babe7daed56ba19bdf444c132ec493120e75e90c7e5d9734`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 30 Sep 2021 18:03:01 GMT
ADD file:129e2106788d883a456b145d9aff00c3003ee3480901a30318933b46961d31f3 in / 
# Thu, 30 Sep 2021 18:03:02 GMT
CMD ["bash"]
# Thu, 30 Sep 2021 22:18:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 30 Sep 2021 22:18:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 30 Sep 2021 22:18:46 GMT
ENV GOSU_VERSION=1.12
# Thu, 30 Sep 2021 22:19:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 30 Sep 2021 22:19:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 30 Sep 2021 22:19:26 GMT
ENV LANG=en_US.utf8
# Thu, 30 Sep 2021 22:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 30 Sep 2021 22:19:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 30 Sep 2021 22:19:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Thu, 30 Sep 2021 22:19:41 GMT
ENV PG_MAJOR=14
# Thu, 30 Sep 2021 22:19:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 30 Sep 2021 22:19:41 GMT
ENV PG_VERSION=14.0-1.pgdg110+1
# Thu, 30 Sep 2021 22:54:19 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 30 Sep 2021 22:54:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 30 Sep 2021 22:54:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 30 Sep 2021 22:54:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 30 Sep 2021 22:54:25 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 30 Sep 2021 22:54:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 30 Sep 2021 22:54:26 GMT
COPY file:39dd79c055f47ef80495def6993f3e85eb124d02824dc47db35d1043455e54bc in /usr/local/bin/ 
# Thu, 30 Sep 2021 22:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Sep 2021 22:54:27 GMT
STOPSIGNAL SIGINT
# Thu, 30 Sep 2021 22:54:28 GMT
EXPOSE 5432
# Thu, 30 Sep 2021 22:54:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:aad43ac6bd46b2cab91485c8f1dac6a985df690af3e431e9e0b9fd57ad5ed423`  
		Last Modified: Thu, 30 Sep 2021 18:19:26 GMT  
		Size: 26.6 MB (26571924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580c30d6212fc0c5e892b1da4593e8090bf2ecb6c11bb67204e1d91edba90a39`  
		Last Modified: Fri, 01 Oct 2021 02:35:13 GMT  
		Size: 3.7 MB (3717077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bbf6baf12d4196c3344ddb309f9125e53b1c5519b7c02807638f4d1566cb35`  
		Last Modified: Fri, 01 Oct 2021 02:35:11 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cbe192408c0f71246f8a977f99e7be4f481ea1022978c9913c05b93ea22d27`  
		Last Modified: Fri, 01 Oct 2021 02:35:11 GMT  
		Size: 1.4 MB (1402357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a1f485a8c627ff66806f8ee4e773ddb8386c720e66d121774251b9f910d8a2`  
		Last Modified: Fri, 01 Oct 2021 02:35:15 GMT  
		Size: 8.0 MB (8045260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26fd04001559f62fa19628b46b41fe3f1e6ffb10ca949add4de4e51c5f4a5c3`  
		Last Modified: Fri, 01 Oct 2021 02:35:09 GMT  
		Size: 434.5 KB (434498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec64541f883f087718d008ba9e9ef66a9ba101930a756e7b384fd86ca818eadd`  
		Last Modified: Fri, 01 Oct 2021 02:35:09 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8404f1793575907eab013312ee0f7b699f70be4dd9b53aded7cfe598781f7b83`  
		Last Modified: Fri, 01 Oct 2021 02:35:09 GMT  
		Size: 3.1 KB (3054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85f73cd1d71a6f2b7df3a9638e7822ef799fe6a7ec96993b28a665ff1de54d5`  
		Last Modified: Fri, 01 Oct 2021 02:35:58 GMT  
		Size: 84.8 MB (84840798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b27a5a43bbf53319c6a3fbec3c64f3672e37b23b392c88612e032ac5c6e8b9`  
		Last Modified: Fri, 01 Oct 2021 02:35:07 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb096d3a7d3f515d6affef36d55b6154f555728bf72efcc23e3a66cfd538317`  
		Last Modified: Fri, 01 Oct 2021 02:35:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa04beb8613cd891f22a8bfa23f8376439e135ef20f513704fddd3d7129a3c8`  
		Last Modified: Fri, 01 Oct 2021 02:35:07 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3f57e4aa545ce7fba1911963f38429e901962420f4293dffa67f8368bb0dc9`  
		Last Modified: Fri, 01 Oct 2021 02:35:07 GMT  
		Size: 4.6 KB (4561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e247c43d5966747ed724630d4ab2565098fb23f79688c94aaf250a6470259178
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132083044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef50259a66782b86ccfc3fa5ffb1e1c767e90ea0adb7f08d083ab925368be3c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:43 GMT
ADD file:6472ab63529e688735f77634402740e08fdbd5bfa788c150915027993df7e8ec in / 
# Tue, 28 Sep 2021 01:40:44 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 11:20:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 28 Sep 2021 11:20:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 28 Sep 2021 11:20:47 GMT
ENV GOSU_VERSION=1.12
# Tue, 28 Sep 2021 11:20:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 28 Sep 2021 11:21:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 28 Sep 2021 11:21:03 GMT
ENV LANG=en_US.utf8
# Tue, 28 Sep 2021 11:21:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 11:21:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Sep 2021 11:21:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 28 Sep 2021 11:21:17 GMT
ENV PG_MAJOR=14
# Tue, 28 Sep 2021 11:21:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Fri, 01 Oct 2021 00:18:03 GMT
ENV PG_VERSION=14.0-1.pgdg110+1
# Fri, 01 Oct 2021 00:18:31 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 01 Oct 2021 00:18:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 01 Oct 2021 00:18:33 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 01 Oct 2021 00:18:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 01 Oct 2021 00:18:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 01 Oct 2021 00:18:34 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 01 Oct 2021 00:18:34 GMT
COPY file:39dd79c055f47ef80495def6993f3e85eb124d02824dc47db35d1043455e54bc in /usr/local/bin/ 
# Fri, 01 Oct 2021 00:18:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 00:18:35 GMT
STOPSIGNAL SIGINT
# Fri, 01 Oct 2021 00:18:35 GMT
EXPOSE 5432
# Fri, 01 Oct 2021 00:18:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2f8871a8654eb1158cb626f8dc69992dba7e4bd8796fae6aa7cf967f951f5fe9`  
		Last Modified: Tue, 28 Sep 2021 01:48:25 GMT  
		Size: 30.1 MB (30055408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35bafe1dc851fc9aefa3c150d0df88515dcf3afb315d604f502e1313c697eff`  
		Last Modified: Tue, 28 Sep 2021 11:56:14 GMT  
		Size: 4.4 MB (4415378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8feff4c760546b2e2560db40263f042ce1e57b338319954bca0c1cbcef2707d7`  
		Last Modified: Tue, 28 Sep 2021 11:56:13 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f175da21aafede406ceb81e27cda155f042eaa7c1fea3c05829a1f136e723c`  
		Last Modified: Tue, 28 Sep 2021 11:56:14 GMT  
		Size: 1.4 MB (1386622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b3fad7d77eb59ed5fa57422307a2372ebc1a9f193950f8ff52378be6478a55`  
		Last Modified: Tue, 28 Sep 2021 11:56:13 GMT  
		Size: 8.0 MB (8045158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98de1af01d5a81bb7a1bafee7fc0d2e5b0afc9a30fc01ecd6256383dfa5aa2b2`  
		Last Modified: Tue, 28 Sep 2021 11:56:11 GMT  
		Size: 442.0 KB (441967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285b5ffb3d52a92ee4fbf5f8ce32ee6534d4ef30b4a9d37e4c331ed5ac8838b2`  
		Last Modified: Tue, 28 Sep 2021 11:56:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc74bee4254ef9704b713fcd2daadfd3a426387e3b26f4fa80800c46d9468c4`  
		Last Modified: Tue, 28 Sep 2021 11:56:11 GMT  
		Size: 3.1 KB (3054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f0553587383c55edadd78be147af5bdf08317de2e62ceb04abede4a4b3722b`  
		Last Modified: Fri, 01 Oct 2021 00:27:54 GMT  
		Size: 87.7 MB (87719096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63008bd65bdf67b483ca179fc209f3c64f382c4a8f7d734bae2f12eace55c0a7`  
		Last Modified: Fri, 01 Oct 2021 00:27:40 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b16ef8c572b8a030a4d44446548db413c126f93b0f7c6725cf8c7d7d128736`  
		Last Modified: Fri, 01 Oct 2021 00:27:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bd67bed6bfbfcff2b6d79a204ecb399b24fd1cfa76ff558922bdef69235487`  
		Last Modified: Fri, 01 Oct 2021 00:27:41 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2edd840f24b773891b8e4a2ab156a4c2704c8d6b00b377751740c1715f0a96`  
		Last Modified: Fri, 01 Oct 2021 00:27:41 GMT  
		Size: 4.6 KB (4557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; 386

```console
$ docker pull postgres@sha256:da98eb3d0ac42daede96c9cdf77ac57ef8e3c50614f48fcafe55e691b7d9a590
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139054640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbae312d988b8cc84e74ea1586bdf85bf4b862ada5b86e20e7c43facf475278`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:08 GMT
ADD file:8466bd8df052ea7fa26e49575ac95fd4934ddafdad54a9736ac2bd8e7fc6e735 in / 
# Tue, 28 Sep 2021 01:40:08 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 17:14:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 28 Sep 2021 17:14:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 28 Sep 2021 17:14:35 GMT
ENV GOSU_VERSION=1.12
# Tue, 28 Sep 2021 17:14:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 28 Sep 2021 17:14:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 28 Sep 2021 17:14:54 GMT
ENV LANG=en_US.utf8
# Tue, 28 Sep 2021 17:14:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 17:14:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Sep 2021 17:15:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 28 Sep 2021 17:15:05 GMT
ENV PG_MAJOR=14
# Tue, 28 Sep 2021 17:15:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Fri, 01 Oct 2021 00:57:02 GMT
ENV PG_VERSION=14.0-1.pgdg110+1
# Fri, 01 Oct 2021 01:13:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 01 Oct 2021 01:13:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 01 Oct 2021 01:13:04 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 01 Oct 2021 01:13:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 01 Oct 2021 01:13:05 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 01 Oct 2021 01:13:05 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 01 Oct 2021 01:13:05 GMT
COPY file:39dd79c055f47ef80495def6993f3e85eb124d02824dc47db35d1043455e54bc in /usr/local/bin/ 
# Fri, 01 Oct 2021 01:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Oct 2021 01:13:06 GMT
STOPSIGNAL SIGINT
# Fri, 01 Oct 2021 01:13:06 GMT
EXPOSE 5432
# Fri, 01 Oct 2021 01:13:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e79fce1f6442094a82dc5f6b4d1aa352e04aae39bba821c9021f6da08b1cacaf`  
		Last Modified: Tue, 28 Sep 2021 01:49:07 GMT  
		Size: 32.4 MB (32380160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e1ab074ce3dd0eab68edc193efa5fd98ea3eec7dd073437db711a25cde909a`  
		Last Modified: Tue, 28 Sep 2021 18:43:38 GMT  
		Size: 4.8 MB (4812781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a14356ccb65950a1b3e70fe898d4019f400afb14a7e4687532ae9ebc7b1a32`  
		Last Modified: Tue, 28 Sep 2021 18:43:34 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacd355e554709f268386f1aacbcdc511d5e4a0b536be582f7155e2392f3d120`  
		Last Modified: Tue, 28 Sep 2021 18:43:34 GMT  
		Size: 1.4 MB (1420865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab11af800164f2414b9338520598835ca1fd0b36b7a265157038de15bdbe23`  
		Last Modified: Tue, 28 Sep 2021 18:43:38 GMT  
		Size: 8.0 MB (8045087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324260c4b80910870de54fb8041c61b9b3789fa5df5d1c3699ee6062f16e36ec`  
		Last Modified: Tue, 28 Sep 2021 18:43:32 GMT  
		Size: 447.9 KB (447854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1982aa9ef1665c9c6f25fe4a451bc06b594ff13a3e6339a34eab1d91a5d64bd6`  
		Last Modified: Tue, 28 Sep 2021 18:43:31 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f398ac1d73896e6163ea396677a41c48cba95c0c52b6dfe4039a111dedce906f`  
		Last Modified: Tue, 28 Sep 2021 18:43:31 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a2c8139f5fe19f89e64fa5b809a596dfff7f57f9f512aa89ec5c95576e2600`  
		Last Modified: Fri, 01 Oct 2021 01:39:06 GMT  
		Size: 91.9 MB (91928479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30403c5b27f6928bc724620946cf1a5f7c9cd29bb56c6dd75dafda7267fa7002`  
		Last Modified: Fri, 01 Oct 2021 01:38:47 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb47419286ccfbd7eb43284bdf0b8f6e6ddccfb434254657fc697c60d663eb0`  
		Last Modified: Fri, 01 Oct 2021 01:38:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11fc24868cde945b3495fd22a2be3b0faa64699916718920f916b0b03739a654`  
		Last Modified: Fri, 01 Oct 2021 01:38:47 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12355fafba00c5ba3a36df52b72fa6818d79fbb8d2e60293d99a9c7bf595af7`  
		Last Modified: Fri, 01 Oct 2021 01:38:47 GMT  
		Size: 4.6 KB (4566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; mips64le

```console
$ docker pull postgres@sha256:fa5bcbae7db85113e9e0660a81b104acd746d9ab1c724b372138100b3ca0f917
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131760973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5466d1f22d78a9b9e9751368d92f91b76c44dd32394caaeb6a53f0d7d542d55a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 28 Sep 2021 02:10:40 GMT
ADD file:43593ef3d79c9b74a92e318d44aacb578f6f8d835dd72665e057bbfe73df1a93 in / 
# Tue, 28 Sep 2021 02:10:41 GMT
CMD ["bash"]
# Wed, 06 Oct 2021 01:07:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 06 Oct 2021 01:07:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 06 Oct 2021 01:07:25 GMT
ENV GOSU_VERSION=1.12
# Wed, 06 Oct 2021 01:07:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 06 Oct 2021 01:08:09 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 06 Oct 2021 01:08:10 GMT
ENV LANG=en_US.utf8
# Wed, 06 Oct 2021 01:08:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 01:08:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 06 Oct 2021 01:08:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 06 Oct 2021 01:08:27 GMT
ENV PG_MAJOR=14
# Wed, 06 Oct 2021 01:08:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 06 Oct 2021 01:08:27 GMT
ENV PG_VERSION=14.0-1.pgdg110+1
# Wed, 06 Oct 2021 02:04:19 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 06 Oct 2021 02:04:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 06 Oct 2021 02:04:24 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 06 Oct 2021 02:04:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 06 Oct 2021 02:04:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 06 Oct 2021 02:04:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 06 Oct 2021 02:04:27 GMT
COPY file:39dd79c055f47ef80495def6993f3e85eb124d02824dc47db35d1043455e54bc in /usr/local/bin/ 
# Wed, 06 Oct 2021 02:04:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 02:04:27 GMT
STOPSIGNAL SIGINT
# Wed, 06 Oct 2021 02:04:28 GMT
EXPOSE 5432
# Wed, 06 Oct 2021 02:04:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1f46ea49e27fccc580c8910db39ba7f51ae208a8d24d46a33140afa92ea3d955`  
		Last Modified: Tue, 28 Sep 2021 02:20:45 GMT  
		Size: 29.6 MB (29627871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06363e2276471f2588e3b07792bb620f65e3663f0d5654392e2faa610869e926`  
		Last Modified: Wed, 06 Oct 2021 05:49:33 GMT  
		Size: 4.4 MB (4402808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96daee93ea6f2e4be7d44a99e4512499ffc408a1e6103e8e7cee0402b7a32a50`  
		Last Modified: Wed, 06 Oct 2021 05:49:29 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c859907b98bc1accdae3d2587f19041a649d9cffa92fbb61b37353dd04e042b0`  
		Last Modified: Wed, 06 Oct 2021 05:49:30 GMT  
		Size: 1.3 MB (1339323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bac0ffca8ad59c7d25840cb5a0a52110fbc60217c9c2defdb1970071f9833e`  
		Last Modified: Wed, 06 Oct 2021 05:49:34 GMT  
		Size: 8.0 MB (8043929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdd3ee6acab6c2ce672c80a90f2ed8c923534e14942c9b3db1633cbacda3b09`  
		Last Modified: Wed, 06 Oct 2021 05:49:27 GMT  
		Size: 439.1 KB (439103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e29347902a2953400a73635544f2fef07dbdec1ec25ba7c4e1452db91d8217c`  
		Last Modified: Wed, 06 Oct 2021 05:49:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170ac2499b1b209ef7391e84ab318a9a3928496ffc037db3619d65f980a23696`  
		Last Modified: Wed, 06 Oct 2021 05:49:26 GMT  
		Size: 3.1 KB (3054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadeefab3c9d0ee2cd21afffb0d88f8ff81d3bf8b397bebe86549e12acf49a9a`  
		Last Modified: Wed, 06 Oct 2021 05:50:26 GMT  
		Size: 87.9 MB (87888605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b18ff57fa75c7be8a22ca8ce792ff983a57721fbf453a709ed1bdceb276fc9`  
		Last Modified: Wed, 06 Oct 2021 05:49:24 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510b9e01e40bbc3f62433c3d19cbe895cae822ddaca3def3e97f3ffdea64ba10`  
		Last Modified: Wed, 06 Oct 2021 05:49:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a452fad05ab40f5f3ad57eb84a4b879a4cf1c86e5a9b798093be033dad4ed242`  
		Last Modified: Wed, 06 Oct 2021 05:49:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68a80baeae626afe2d8b808507b6f8aa14bfadd0ca75a9601efbae70f236842`  
		Last Modified: Wed, 06 Oct 2021 05:49:24 GMT  
		Size: 4.6 KB (4561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; ppc64le

```console
$ docker pull postgres@sha256:c95ec2fc5cd577e6d58b7e93c9cd4ba1f93a584ffac266f546b66499153d1f84
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145868736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d12a74bb9ea58eca1b9b053bf13a4e2fe8c786614eb165282acb99127ca729`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 04 Oct 2021 17:55:01 GMT
ADD file:f4b696a766a0d9a808c171a1d5db4f0877b0a784649d63bf461dfcf54b532239 in / 
# Mon, 04 Oct 2021 17:55:06 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 07:54:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 05 Oct 2021 07:54:34 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 05 Oct 2021 07:54:37 GMT
ENV GOSU_VERSION=1.12
# Tue, 05 Oct 2021 07:55:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Oct 2021 07:55:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 05 Oct 2021 07:55:38 GMT
ENV LANG=en_US.utf8
# Tue, 05 Oct 2021 07:55:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Oct 2021 07:55:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Oct 2021 07:56:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 05 Oct 2021 07:56:14 GMT
ENV PG_MAJOR=14
# Tue, 05 Oct 2021 07:56:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 05 Oct 2021 07:56:20 GMT
ENV PG_VERSION=14.0-1.pgdg110+1
# Tue, 05 Oct 2021 07:57:33 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 05 Oct 2021 07:57:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 05 Oct 2021 07:57:51 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 05 Oct 2021 07:57:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 05 Oct 2021 07:58:02 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 05 Oct 2021 07:58:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 05 Oct 2021 07:58:07 GMT
COPY file:39dd79c055f47ef80495def6993f3e85eb124d02824dc47db35d1043455e54bc in /usr/local/bin/ 
# Tue, 05 Oct 2021 07:58:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Oct 2021 07:58:12 GMT
STOPSIGNAL SIGINT
# Tue, 05 Oct 2021 07:58:14 GMT
EXPOSE 5432
# Tue, 05 Oct 2021 07:58:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c3b7af0ed242d09d9fee2dfc48d4553d58ad90c5fb862ab58fb89e2d04c5b922`  
		Last Modified: Mon, 04 Oct 2021 18:07:32 GMT  
		Size: 35.3 MB (35272408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1dfe8576fe80020094eca6a18a1f9824137e677472de220dd08a3a25abd925`  
		Last Modified: Tue, 05 Oct 2021 08:23:43 GMT  
		Size: 5.2 MB (5222842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20320ad4b2721c4785d600224feec4dd2c7872c57c9f2f85fb946648661cefe9`  
		Last Modified: Tue, 05 Oct 2021 08:23:40 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a319d4e6eb9b4b5959c4aeb383e920bdf1af22ea18df0e5f0b4a0075890ffa`  
		Last Modified: Tue, 05 Oct 2021 08:23:39 GMT  
		Size: 1.4 MB (1369874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d150b46cf8a7ef9937ac1b92e672324e678dd53846b61ff7a56b9eb635fa72ac`  
		Last Modified: Tue, 05 Oct 2021 08:23:39 GMT  
		Size: 8.0 MB (8045351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8382f9aa2593f76ac6e748522be16471183ddf642ce38d0d38a51b272e7e32ea`  
		Last Modified: Tue, 05 Oct 2021 08:23:38 GMT  
		Size: 451.5 KB (451490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e20df117a725abc5a24d144190dd6cbd599b4e19a0b5f0e4f90d248333b7ab`  
		Last Modified: Tue, 05 Oct 2021 08:23:37 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e2ab1d4b57fd22540582a33d508d428cedb009060666413073e9585ac98a3d`  
		Last Modified: Tue, 05 Oct 2021 08:23:36 GMT  
		Size: 3.1 KB (3053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d152ace5be9816b7ead5e341bacdc75d6f1f8e644e836a686e12416e83101b3b`  
		Last Modified: Tue, 05 Oct 2021 08:23:50 GMT  
		Size: 95.5 MB (95487341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19e02954cfc57aa2b05dc59199654b22cc3689583e403a9dab16d86b61e4d5e`  
		Last Modified: Tue, 05 Oct 2021 08:23:33 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e4b623db0b9b3118a4984c14760aa70f440e5ea6f26630a800079f12adfdc0`  
		Last Modified: Tue, 05 Oct 2021 08:23:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279af163397c84277588910797f6c0e42a420710bda51fda85d1fffeed557a80`  
		Last Modified: Tue, 05 Oct 2021 08:23:33 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4259b5c8c196c9a5995a0116e92d1fbc16f9d084a251493e98425504f6934833`  
		Last Modified: Tue, 05 Oct 2021 08:23:33 GMT  
		Size: 4.6 KB (4559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; s390x

```console
$ docker pull postgres@sha256:793ebd3bc28ca587e3ad58ad0a23ea7246744b504dc1be4047b7301d5874309d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140813512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc89f274baf7684ec531046d55cfe124c5a797ae7963c0310008576a05764ffc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 12 Oct 2021 00:42:27 GMT
ADD file:6038dd6db57fb05c3d39c02c3379667ccd2989e7667ff773a8020fe6a69a760c in / 
# Tue, 12 Oct 2021 00:42:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 04:42:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 04:42:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 12 Oct 2021 04:42:59 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Oct 2021 04:43:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Oct 2021 04:43:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 12 Oct 2021 04:43:12 GMT
ENV LANG=en_US.utf8
# Tue, 12 Oct 2021 04:43:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 04:43:16 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Oct 2021 04:43:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 12 Oct 2021 04:43:24 GMT
ENV PG_MAJOR=14
# Tue, 12 Oct 2021 04:43:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 12 Oct 2021 04:43:24 GMT
ENV PG_VERSION=14.0-1.pgdg110+1
# Tue, 12 Oct 2021 04:52:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 12 Oct 2021 04:52:51 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 12 Oct 2021 04:52:51 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 12 Oct 2021 04:52:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 12 Oct 2021 04:52:52 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 12 Oct 2021 04:52:52 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 12 Oct 2021 04:52:52 GMT
COPY file:39dd79c055f47ef80495def6993f3e85eb124d02824dc47db35d1043455e54bc in /usr/local/bin/ 
# Tue, 12 Oct 2021 04:52:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 04:52:53 GMT
STOPSIGNAL SIGINT
# Tue, 12 Oct 2021 04:52:53 GMT
EXPOSE 5432
# Tue, 12 Oct 2021 04:52:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ded751c48f72503973be01be2794cc039490f22b039b8ac106e9f17de4980742`  
		Last Modified: Tue, 12 Oct 2021 00:48:05 GMT  
		Size: 29.6 MB (29641215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6a93ff0480588f672b34588196d8b0b3760c35ebf5ca124b6c7d108eee67e2`  
		Last Modified: Tue, 12 Oct 2021 05:31:40 GMT  
		Size: 4.3 MB (4302214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c399cd9323f897614914f42ce31ceff3b554ca1b97ae241a520739e4c445835`  
		Last Modified: Tue, 12 Oct 2021 05:31:38 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559fbc4b29c0170923c34d676d6ee0eec60aa25e3b002335817c5094d5aefab8`  
		Last Modified: Tue, 12 Oct 2021 05:31:38 GMT  
		Size: 1.4 MB (1437301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66acee0cb6da8cf6ea2ec5be275e821cb9e3c7ff11748690bc41489d9fd4ca95`  
		Last Modified: Tue, 12 Oct 2021 05:31:38 GMT  
		Size: 8.1 MB (8099041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6632164197b8c45e2e90e0cf2ce4cc3ae59bf9afb23cda8e7d92922a9956b9f`  
		Last Modified: Tue, 12 Oct 2021 05:31:38 GMT  
		Size: 438.3 KB (438288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085741607fc61219fa4a0eaebb64a12a98c8f2aa40e4ee49c407aa76b648b35b`  
		Last Modified: Tue, 12 Oct 2021 05:31:37 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e542f5ea3f0911ad3cb3c757844641108d934843bdb0a903812670d851daf`  
		Last Modified: Tue, 12 Oct 2021 05:31:37 GMT  
		Size: 3.1 KB (3056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce384069e9b4241397f48627966c7d562ac6777a96053cbaf55e0f2e6cf095`  
		Last Modified: Tue, 12 Oct 2021 05:31:48 GMT  
		Size: 96.9 MB (96876024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79143db2c6889c63acd66964d3ea1a0b57d61338aeb60a709b0035855c347693`  
		Last Modified: Tue, 12 Oct 2021 05:31:36 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666f82252d4115d7b3e941590efb04e8b0d28922c3340d7191047cddaa5b2f89`  
		Last Modified: Tue, 12 Oct 2021 05:31:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc13830db241a61954951eb50de8c694cb2cd79b1527a72df8527c49cd7dcbb`  
		Last Modified: Tue, 12 Oct 2021 05:31:36 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9dc39075fa0e649fbde4afa939246d62d4850558016090c5778471cef14df5a`  
		Last Modified: Tue, 12 Oct 2021 05:31:36 GMT  
		Size: 4.6 KB (4558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
