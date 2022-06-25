## `postgres:latest`

```console
$ docker pull postgres@sha256:4ba3b78788bb284687376b9c1e0565b245375ddee0fe14cef25e315b6bd88b1a
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
$ docker pull postgres@sha256:d3eecdd28512e721b10d6e270d4ede4cbd57706f0c5bf28ea1dc952eff325650
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137822723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2261d3c6ce0b23bed32e7567a92646b880de73d802550b1275baa0997aa34d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 14:26:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 14:26:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 23 Jun 2022 14:26:14 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 14:26:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 14:26:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 23 Jun 2022 14:26:28 GMT
ENV LANG=en_US.utf8
# Thu, 23 Jun 2022 14:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 14:26:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Jun 2022 14:26:34 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 14:27:08 GMT
ENV PG_MAJOR=14
# Thu, 23 Jun 2022 14:27:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 23 Jun 2022 14:27:08 GMT
ENV PG_VERSION=14.4-1.pgdg110+1
# Thu, 23 Jun 2022 14:27:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 23 Jun 2022 14:27:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 23 Jun 2022 14:27:28 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 23 Jun 2022 14:27:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 23 Jun 2022 14:27:29 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 23 Jun 2022 14:27:29 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 23 Jun 2022 14:27:29 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Thu, 23 Jun 2022 14:27:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 14:27:29 GMT
STOPSIGNAL SIGINT
# Thu, 23 Jun 2022 14:27:29 GMT
EXPOSE 5432
# Thu, 23 Jun 2022 14:27:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53bada42f30af6cb05b321cd1476f8e7618dfcf89614107050a261436b1097c`  
		Last Modified: Thu, 23 Jun 2022 14:31:40 GMT  
		Size: 4.4 MB (4414594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303bde9620f54624dd5ac06c8d299c420b8f422d086bc30b5ad3728419ecf171`  
		Last Modified: Thu, 23 Jun 2022 14:31:38 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c32c0c0a1b9965aeb753d022e0574c5c29890183dbd91a4409659c6b651802e`  
		Last Modified: Thu, 23 Jun 2022 14:31:39 GMT  
		Size: 1.4 MB (1418435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302630a57c0605eca44604de509d0c938ec26c3d5ed27f87c11b643b113873f4`  
		Last Modified: Thu, 23 Jun 2022 14:31:38 GMT  
		Size: 8.0 MB (8045420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfead4dfb390e7fdf514870fbbd258dc62ad3457eda7281a7f0e8d567c7d067`  
		Last Modified: Thu, 23 Jun 2022 14:31:37 GMT  
		Size: 1.3 MB (1261185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d9917b93099eb77b625877b1f755d24af442568a78fc0805c0b09e3d23cda1`  
		Last Modified: Thu, 23 Jun 2022 14:31:36 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb0d8ea11e0d46901df9f6d54845c7aa10fb73ac29b8c22648afa2a308808ac`  
		Last Modified: Thu, 23 Jun 2022 14:31:36 GMT  
		Size: 3.2 KB (3201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb69a02914fd165fabc93b03af3e8b6bcb6de569b42fb71fabdb11b6311d8c46`  
		Last Modified: Thu, 23 Jun 2022 14:32:11 GMT  
		Size: 91.3 MB (91283968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295e6398825d01036116551e1645f429d3355ae0b081e48369ec8f35282d8bd1`  
		Last Modified: Thu, 23 Jun 2022 14:31:59 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadcad7a2f3d95a258c504d2ab52b7aa12f005b07e52449afa3e366356235ba8`  
		Last Modified: Thu, 23 Jun 2022 14:31:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69648da3f43aef0d9e40b6b09d29f1740dd9e18b0fc833e5ae725cdac4b8e50`  
		Last Modified: Thu, 23 Jun 2022 14:31:59 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f430e1124739c194e10da7fbf9eab2efee5fa69e24ad50ca0bde01d628f05ff`  
		Last Modified: Thu, 23 Jun 2022 14:31:58 GMT  
		Size: 4.7 KB (4702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; arm variant v5

```console
$ docker pull postgres@sha256:d52d7ecbfd867efe4d4635d57eca5c262dd251d4e9c84bf5c485c45ff64c1981
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131150183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c72285c414c0c501ac9a18594ccea6cbe0e37d1824e5e26c41340055e5d174`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 23 Jun 2022 00:50:38 GMT
ADD file:839c0e211e2260f5d54f2633e53c817c1f59e2394ba4b12f60e01e46cee61011 in / 
# Thu, 23 Jun 2022 00:50:39 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:30:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 08:30:18 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 23 Jun 2022 08:30:19 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 08:30:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 08:31:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 23 Jun 2022 08:31:04 GMT
ENV LANG=en_US.utf8
# Thu, 23 Jun 2022 08:31:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 08:31:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Jun 2022 08:31:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 09:11:45 GMT
ENV PG_MAJOR=14
# Thu, 23 Jun 2022 09:11:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 23 Jun 2022 09:11:46 GMT
ENV PG_VERSION=14.4-1.pgdg110+1
# Thu, 23 Jun 2022 09:50:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 23 Jun 2022 09:50:31 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 23 Jun 2022 09:50:32 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 23 Jun 2022 09:50:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 23 Jun 2022 09:50:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 23 Jun 2022 09:50:35 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 23 Jun 2022 09:50:35 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Thu, 23 Jun 2022 09:50:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 09:50:36 GMT
STOPSIGNAL SIGINT
# Thu, 23 Jun 2022 09:50:37 GMT
EXPOSE 5432
# Thu, 23 Jun 2022 09:50:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bd2d3b4056bd1b0310082fc5d17c6d03348601456c4b9306d1a333f1cec561f9`  
		Last Modified: Thu, 23 Jun 2022 01:05:39 GMT  
		Size: 28.9 MB (28921550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528a45687a21e84bfd794de80b4b48bed7b5cfee1e713005589cdd227f190f6`  
		Last Modified: Thu, 23 Jun 2022 13:02:42 GMT  
		Size: 4.1 MB (4096605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91dfe8b4a0d84f97547b3cd95a77325f39a56d7e09b5c6cada6a6899719eb86b`  
		Last Modified: Thu, 23 Jun 2022 13:02:39 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b899e4f4c313fe9dd5851822686a2c01bab253137a24c2209e0363720e9a7c64`  
		Last Modified: Thu, 23 Jun 2022 13:02:39 GMT  
		Size: 1.4 MB (1382670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecc13760e9f728491b83588c8efa1bad2e8459c690854d2b9dc4ce04a3d0c3f`  
		Last Modified: Thu, 23 Jun 2022 13:02:44 GMT  
		Size: 8.0 MB (8045435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4888133f250330d22c607a07094c1505f6226990a800434feb9417c27adb209d`  
		Last Modified: Thu, 23 Jun 2022 13:02:38 GMT  
		Size: 1.3 MB (1257360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acb6160cb60f95794d4cb7491038bf35ae77a476da6f205d41690b29a636e84`  
		Last Modified: Thu, 23 Jun 2022 13:02:37 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68e5a67bb9d626a7eb08a175139d61c94dbcaacf4208e54a69d28efc2cabb89`  
		Last Modified: Thu, 23 Jun 2022 13:02:37 GMT  
		Size: 3.2 KB (3201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b32a5625eb04abbaa13d65d05b16127f89c797174c12e27a7a628af003043b`  
		Last Modified: Thu, 23 Jun 2022 13:04:40 GMT  
		Size: 87.4 MB (87426848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7a4b920907c69f362a80a9a4de034f40e8dc3b123125e6a13afba476faa7d6`  
		Last Modified: Thu, 23 Jun 2022 13:03:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc15bc610b8bb8fbc707a62db46649f574608ca722a32bde7cac3229a745a854`  
		Last Modified: Thu, 23 Jun 2022 13:03:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e3ac0ccf8d30dd589e1534cab2cedf2359b2632766f3374576e0527e076c88`  
		Last Modified: Thu, 23 Jun 2022 13:03:43 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96469e38116420e603eacd7c9a0ae47612d3f24e82cf3d85eca120453a931737`  
		Last Modified: Thu, 23 Jun 2022 13:03:43 GMT  
		Size: 4.7 KB (4703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; arm variant v7

```console
$ docker pull postgres@sha256:fe8ee2aa6b450692eab43c107dac480ccb6f5127bb2972eeed0c4c68153e474c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125806586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71944ad3e898ac3140d1f4dd2fbde8bb76ae0afdd5f6bca741f9d5e212764e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 23 Jun 2022 00:59:45 GMT
ADD file:925abfb9fc0e4a7cc0c979b12c9bd2607f5c493d37b05535ca010f81beb060a9 in / 
# Thu, 23 Jun 2022 00:59:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 16:43:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 16:43:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 23 Jun 2022 16:43:44 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 16:44:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 16:44:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 23 Jun 2022 16:44:26 GMT
ENV LANG=en_US.utf8
# Thu, 23 Jun 2022 16:44:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 16:44:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Jun 2022 16:44:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 17:21:21 GMT
ENV PG_MAJOR=14
# Thu, 23 Jun 2022 17:21:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 23 Jun 2022 17:21:22 GMT
ENV PG_VERSION=14.4-1.pgdg110+1
# Thu, 23 Jun 2022 17:55:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 23 Jun 2022 17:55:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 23 Jun 2022 17:55:59 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 23 Jun 2022 17:55:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 23 Jun 2022 17:56:01 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 23 Jun 2022 17:56:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 23 Jun 2022 17:56:02 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Thu, 23 Jun 2022 17:56:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 17:56:03 GMT
STOPSIGNAL SIGINT
# Thu, 23 Jun 2022 17:56:03 GMT
EXPOSE 5432
# Thu, 23 Jun 2022 17:56:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d2fd562560d8062a78064adfbfa204521167c301f00f5ab3c65b9c2a54083dba`  
		Last Modified: Thu, 23 Jun 2022 01:15:22 GMT  
		Size: 26.6 MB (26576105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63319081a6b1a33fd7e630add226ba80013b277dc6015917df7da64337d21aa4`  
		Last Modified: Thu, 23 Jun 2022 20:49:51 GMT  
		Size: 3.7 MB (3717352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced2c4102cda18bca9b6d8d690b110f8793efdac55f6901724ce09df3831eedc`  
		Last Modified: Thu, 23 Jun 2022 20:49:48 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c399ca6f8076180b41a9a2f41ea9dddd933e18cceff70870f953401c16a876a`  
		Last Modified: Thu, 23 Jun 2022 20:49:48 GMT  
		Size: 1.4 MB (1375412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef13cdcefcb9110e976907836b5a4efa3e771c080a898d81ee5307779370a034`  
		Last Modified: Thu, 23 Jun 2022 20:49:51 GMT  
		Size: 8.0 MB (8045369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015dab6ad0f2b3e2a6e4d9a2d55d66f0d95ed7fa84c72bc441d128bd5d9ce002`  
		Last Modified: Thu, 23 Jun 2022 20:49:46 GMT  
		Size: 1.1 MB (1131249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e764dce225c6387cd3c9023818fd785ff89ac9f164124fbe1d43cece89dcb0`  
		Last Modified: Thu, 23 Jun 2022 20:49:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1d70ac02b5e38549b58d2da79c9c491c720fb6db342b7f25213b348826ab9c`  
		Last Modified: Thu, 23 Jun 2022 20:49:53 GMT  
		Size: 3.2 KB (3194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba6abadd74bf3577eafbf7f84d48b1812202001726548c847a6b46928297ebc`  
		Last Modified: Thu, 23 Jun 2022 20:51:46 GMT  
		Size: 84.9 MB (84941406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa9b954142e42f3f870d101200458a737a0eeb2697a671876e1ca45702fa2ce`  
		Last Modified: Thu, 23 Jun 2022 20:50:58 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf9d6e70662610288b9d7da81fe7aeb7535b9527157bdcc08a9e83a13bca333`  
		Last Modified: Thu, 23 Jun 2022 20:50:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39a8523db44528569bae8fb99c6dc57881e349b1093ce14b918d0b000a47745`  
		Last Modified: Thu, 23 Jun 2022 20:50:58 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198649cb96093141e7a8cb61dd85b7cb982d77212f9722d0e9ac39c607694723`  
		Last Modified: Thu, 23 Jun 2022 20:50:58 GMT  
		Size: 4.7 KB (4699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:02d54f4c67fbec15aa73c0b38e7b7a666ba9578fca2ec43bf49ebb26018e0144
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132527248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73bb9903b857fe667edde7fe45df7ccc8e577569bb47fc506bc9b2856df63b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:47:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 08:47:15 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 23 Jun 2022 08:47:16 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 08:47:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 08:47:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 23 Jun 2022 08:47:33 GMT
ENV LANG=en_US.utf8
# Thu, 23 Jun 2022 08:47:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 08:47:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Jun 2022 08:47:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 08:48:26 GMT
ENV PG_MAJOR=14
# Thu, 23 Jun 2022 08:48:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 23 Jun 2022 08:48:27 GMT
ENV PG_VERSION=14.4-1.pgdg110+1
# Thu, 23 Jun 2022 08:48:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 23 Jun 2022 08:48:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 23 Jun 2022 08:48:48 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 23 Jun 2022 08:48:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 23 Jun 2022 08:48:50 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 23 Jun 2022 08:48:51 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 23 Jun 2022 08:48:53 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Thu, 23 Jun 2022 08:48:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 08:48:54 GMT
STOPSIGNAL SIGINT
# Thu, 23 Jun 2022 08:48:55 GMT
EXPOSE 5432
# Thu, 23 Jun 2022 08:48:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3b157c852f2736e12f09046f214fe5f6a0b1652bd860269b3988c92a197026e8`  
		Last Modified: Thu, 23 Jun 2022 00:47:22 GMT  
		Size: 30.1 MB (30065720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d019bcaa13826cb59d653d18da03c778e4115b5f01bc14b348df2b7da19da06`  
		Last Modified: Thu, 23 Jun 2022 09:13:17 GMT  
		Size: 4.2 MB (4209041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c6496d90a8f53ba58fcd3b65b9aa02486e07875bd15d7c961fd40b48f8f715`  
		Last Modified: Thu, 23 Jun 2022 09:13:16 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994bae8aa9406084a7d7b1db15a5048d915fd420f7879fe03ee823f43e07224f`  
		Last Modified: Thu, 23 Jun 2022 09:13:17 GMT  
		Size: 1.3 MB (1346184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255bac0c560b70d77007723570b56c77164a7f1dc1568c0f93a456c4145ab462`  
		Last Modified: Thu, 23 Jun 2022 09:13:16 GMT  
		Size: 8.0 MB (8043612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f605281268d731048a8399f5c9e0082e88518d20d2ba64e0dd8215cd5667f447`  
		Last Modified: Thu, 23 Jun 2022 09:13:15 GMT  
		Size: 1.0 MB (1025848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0037c6d29459637d2c6a94812e6d4e0050cf7475c3a8c8e87d8956e8859e5e3`  
		Last Modified: Thu, 23 Jun 2022 09:13:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064e9138f07b410f97c672ead7ebdf37053caa5b019bafb4005a0ac8d3e30917`  
		Last Modified: Thu, 23 Jun 2022 09:13:14 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32dfc8778babcc62a58c9df8f076ed560494fe8f6ecf0a74d9f51b5cb4ec83b`  
		Last Modified: Thu, 23 Jun 2022 09:13:49 GMT  
		Size: 87.8 MB (87817402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bebc9ac17ba28aae8c277d8cfaec75cec7f90dba4fa26023ec48ea787544219`  
		Last Modified: Thu, 23 Jun 2022 09:13:37 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707562ab5f229ba99ee2ea911c105df1c5d2b6d1e48e5353c38d85df13a02c5d`  
		Last Modified: Thu, 23 Jun 2022 09:13:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5548a4a9c39257160d1f8ae0c8668dcbe1a1fae362b11dee04b681d86c7a95`  
		Last Modified: Thu, 23 Jun 2022 09:13:37 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a09e444c5c080fb28a31dd965e333d7b6834c274960a07dec4b3d30022e5c`  
		Last Modified: Thu, 23 Jun 2022 09:13:37 GMT  
		Size: 4.7 KB (4701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; 386

```console
$ docker pull postgres@sha256:ae41523cb3009a3147763b4db9ca27419b73c25f1cfe6c6fc968de7e74c92f71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139501810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daf4ee8114bacf26f3b29cddfa1f57c76afe8e9901763def3c37950d2db9b45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:33 GMT
ADD file:9d46d3f8fb63833a6dbd8dd796ad541d556046a48342d22e1fd3bffa3fb8e504 in / 
# Thu, 23 Jun 2022 00:39:33 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 10:03:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 10:03:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 23 Jun 2022 10:03:56 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 10:04:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 10:04:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 23 Jun 2022 10:04:11 GMT
ENV LANG=en_US.utf8
# Thu, 23 Jun 2022 10:04:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 10:04:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Jun 2022 10:04:19 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 10:18:38 GMT
ENV PG_MAJOR=14
# Thu, 23 Jun 2022 10:18:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 23 Jun 2022 10:18:40 GMT
ENV PG_VERSION=14.4-1.pgdg110+1
# Thu, 23 Jun 2022 10:31:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 23 Jun 2022 10:31:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 23 Jun 2022 10:31:41 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 23 Jun 2022 10:31:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 23 Jun 2022 10:31:43 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 23 Jun 2022 10:31:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 23 Jun 2022 10:31:46 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Thu, 23 Jun 2022 10:31:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 10:31:47 GMT
STOPSIGNAL SIGINT
# Thu, 23 Jun 2022 10:31:48 GMT
EXPOSE 5432
# Thu, 23 Jun 2022 10:31:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4870b12e407743816673c11cfb39974d80c1569d876287bef61f8c585954822f`  
		Last Modified: Thu, 23 Jun 2022 00:46:40 GMT  
		Size: 32.4 MB (32390198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a815fde110b4f4c5e4780320ba2daeaeabc65198ec76c379fa9151873da9ce`  
		Last Modified: Thu, 23 Jun 2022 11:22:59 GMT  
		Size: 4.6 MB (4606898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09de2f39d0d670d63cd25bbe33f6453594846285564fe7c0f2b607d246a63885`  
		Last Modified: Thu, 23 Jun 2022 11:22:57 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a3d063d529ea34ce96c2e3efc157c3da42e5ad4cdbd1baa487f97eb71229fc`  
		Last Modified: Thu, 23 Jun 2022 11:22:58 GMT  
		Size: 1.4 MB (1385086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e23c1af65c34ab50691c50716b0f441ba60748bee864e64dabf37816defa04`  
		Last Modified: Thu, 23 Jun 2022 11:22:57 GMT  
		Size: 8.0 MB (8043636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea1501def2f9f08add48981469f79176afc475ecc7129015f3eae4f88b9e935`  
		Last Modified: Thu, 23 Jun 2022 11:22:56 GMT  
		Size: 1.0 MB (1027948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8158424953b3f8de3fcae5f292295443937338dd750f21fd60e91789310047a`  
		Last Modified: Thu, 23 Jun 2022 11:22:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6da7dc3bcf2c4a8e538b7d91bbc8cb0771db6deec73fd85d663acc42a520da`  
		Last Modified: Thu, 23 Jun 2022 11:22:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee887a50618c8a4afe01823b2052e86b6f10c3349becc6d9658a0cb048c294a`  
		Last Modified: Thu, 23 Jun 2022 11:23:31 GMT  
		Size: 92.0 MB (92028620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62636afb6a40870943a9cec2dabf036099df248c78f3f57f323dc4752fb1c76`  
		Last Modified: Thu, 23 Jun 2022 11:23:19 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f882758db1892fb58cab61e72b28425739a03c5adfcc1bebc4fda990949d9d88`  
		Last Modified: Thu, 23 Jun 2022 11:23:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48cbda72f288ef6b9b34004269fcd6b45b3475e89c6e3cc3abf1a1099222c64`  
		Last Modified: Thu, 23 Jun 2022 11:23:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dd0568cae25a14a9b349a5e9e4c2691ec5e3d3653d01c1fd1f0a4c80b4b5af`  
		Last Modified: Thu, 23 Jun 2022 11:23:19 GMT  
		Size: 4.7 KB (4698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; mips64le

```console
$ docker pull postgres@sha256:6c8b539db2f229e33c9ac84aecbea11cb6f63c9a71168c0c14c856a487a827c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132284003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a51d62b2417518d2a10de62ef03f7229ea64593d88ad1ffa08a6695d01a5601`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 23 Jun 2022 01:10:25 GMT
ADD file:fd1174cc47ac636f0cab382578a899d69ed489e4dee53ec838955e36066f526a in / 
# Thu, 23 Jun 2022 01:10:29 GMT
CMD ["bash"]
# Fri, 24 Jun 2022 19:08:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Jun 2022 19:09:04 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 24 Jun 2022 19:09:07 GMT
ENV GOSU_VERSION=1.14
# Fri, 24 Jun 2022 19:09:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Jun 2022 19:10:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 24 Jun 2022 19:10:14 GMT
ENV LANG=en_US.utf8
# Fri, 24 Jun 2022 19:10:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Jun 2022 19:10:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Jun 2022 19:10:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 24 Jun 2022 20:14:02 GMT
ENV PG_MAJOR=14
# Fri, 24 Jun 2022 20:14:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Fri, 24 Jun 2022 20:14:07 GMT
ENV PG_VERSION=14.4-1.pgdg110+1
# Fri, 24 Jun 2022 21:14:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 24 Jun 2022 21:14:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 24 Jun 2022 21:14:24 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 24 Jun 2022 21:14:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 24 Jun 2022 21:14:33 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 24 Jun 2022 21:14:37 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 24 Jun 2022 21:14:40 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Fri, 24 Jun 2022 21:14:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 21:14:47 GMT
STOPSIGNAL SIGINT
# Fri, 24 Jun 2022 21:14:51 GMT
EXPOSE 5432
# Fri, 24 Jun 2022 21:14:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d199cb5e183b38c9edcc527cbaaa79bb56da73bd09ed449223842775ef4a244`  
		Last Modified: Thu, 23 Jun 2022 01:20:19 GMT  
		Size: 29.6 MB (29641027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7648df165c72f296de832007d97f5fed3103723bba2ec19e91a081d123ee09e7`  
		Last Modified: Sat, 25 Jun 2022 00:45:36 GMT  
		Size: 4.2 MB (4196313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00f5094daceac1c9ea62422703d283d7ca3356004152b456f74be3d055af0e89`  
		Last Modified: Sat, 25 Jun 2022 00:45:31 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8028c8241c5cfdc7d26f2f98828ac6ca21697fc61939c206f438ea938469343e`  
		Last Modified: Sat, 25 Jun 2022 00:45:32 GMT  
		Size: 1.3 MB (1298125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da59c25c5c741ecf4a7e069b8f2fddd3de1fa0325f2337b9306fa4929a401d2`  
		Last Modified: Sat, 25 Jun 2022 00:45:37 GMT  
		Size: 8.0 MB (8044020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f4695602a43632b8ab413c75f11b6c8f5a4eca6f3a131c8df10a9bbb97e499`  
		Last Modified: Sat, 25 Jun 2022 00:45:29 GMT  
		Size: 1.1 MB (1089523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c9fc5fd743333be08a366a9788cfcaf43f1f7f34d40e268052237a0aa5c48`  
		Last Modified: Sat, 25 Jun 2022 00:45:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa126eaa1168050f95cc77afc8925815476991faf31d837286c0e2e62e63340`  
		Last Modified: Sat, 25 Jun 2022 00:45:28 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ecebc575ab3b8cca74a1e1495cd2fd739c1c74afa57d761d5c548300e78bb5`  
		Last Modified: Sat, 25 Jun 2022 00:47:34 GMT  
		Size: 88.0 MB (87995544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64934d005aa6941ee757a461d1a29e1e0a5773ef7c32175b0cee15013dbe8fe7`  
		Last Modified: Sat, 25 Jun 2022 00:46:38 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121189304da2c10da6dd48b2264c823b1be9ff3fec73a4e8a79f334d4a0576da`  
		Last Modified: Sat, 25 Jun 2022 00:46:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49aff102de9c551f5fb01836e12ed51044549614d40d80980bb76979981028f`  
		Last Modified: Sat, 25 Jun 2022 00:46:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ebe41b909d980919446dc2b1c083e6059ec890b3b93d310bdcd53e944ef8cf`  
		Last Modified: Sat, 25 Jun 2022 00:46:38 GMT  
		Size: 4.7 KB (4701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; ppc64le

```console
$ docker pull postgres@sha256:3bfb1c3afb715562843ee169e2938e724128bc9dfd1ca58718a6ab10c40eee51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146923243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758ac6fe349f1f47b9b507a0d02d88ed318f781df5b1da777a242074408ff267`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 23 Jun 2022 02:02:32 GMT
ADD file:e18c13649ea1f145047652c8e171c4824f9b6b0dbc92127a914c7fca910acf96 in / 
# Thu, 23 Jun 2022 02:02:34 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 17:54:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 17:54:34 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 23 Jun 2022 17:54:36 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 17:55:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 17:55:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 23 Jun 2022 17:55:29 GMT
ENV LANG=en_US.utf8
# Thu, 23 Jun 2022 17:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 17:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Jun 2022 17:55:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 17:58:43 GMT
ENV PG_MAJOR=14
# Thu, 23 Jun 2022 17:58:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 23 Jun 2022 17:58:48 GMT
ENV PG_VERSION=14.4-1.pgdg110+1
# Thu, 23 Jun 2022 17:59:51 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 23 Jun 2022 18:00:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 23 Jun 2022 18:00:16 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 23 Jun 2022 18:00:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 23 Jun 2022 18:00:27 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 23 Jun 2022 18:00:34 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 23 Jun 2022 18:00:35 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Thu, 23 Jun 2022 18:00:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 18:00:43 GMT
STOPSIGNAL SIGINT
# Thu, 23 Jun 2022 18:00:48 GMT
EXPOSE 5432
# Thu, 23 Jun 2022 18:00:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7716f0df7ba06b6f1937cd664805984e25e386a4165f2c6acc65356686e35221`  
		Last Modified: Thu, 23 Jun 2022 02:15:20 GMT  
		Size: 35.3 MB (35286823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020126cd7adc35ddd83605444413437b17db388415b535e0e670d5f67b3c8776`  
		Last Modified: Thu, 23 Jun 2022 18:15:26 GMT  
		Size: 5.2 MB (5222957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c0042078ea251b9c7504ed2587c0d97526de4400c1002381d9bace80beb063`  
		Last Modified: Thu, 23 Jun 2022 18:15:25 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338a832b4ece725ccbb232684fc1ffc9db30723713e5019c96663951c19346e1`  
		Last Modified: Thu, 23 Jun 2022 18:15:25 GMT  
		Size: 1.3 MB (1317569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b01978c049df34ee7f8ee387cf1249d65aa64aea142f3035e0da1c226341bc5`  
		Last Modified: Thu, 23 Jun 2022 18:15:24 GMT  
		Size: 8.0 MB (8045517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d546326ffb4c415f7422b2770cf361b11f292efe885edae9b8438fffa2b7f49`  
		Last Modified: Thu, 23 Jun 2022 18:15:21 GMT  
		Size: 1.4 MB (1420200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e15537e0887b85aa436afa0f4bef0c566dd330c2b8d681bf9b1c07fb208562`  
		Last Modified: Thu, 23 Jun 2022 18:15:21 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010ab4f9e2503ff2ff7bcff2a64696dfdd5d682faac053f4672e36550da10eb9`  
		Last Modified: Thu, 23 Jun 2022 18:15:21 GMT  
		Size: 3.2 KB (3201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508e255be80288ef4351a4d24492b90a8daf65229c46c0d5871039717cc3c684`  
		Last Modified: Thu, 23 Jun 2022 18:16:09 GMT  
		Size: 95.6 MB (95610455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730139582a686c76645f2b89ecf9964871e957f10109402bee9220e9776f0773`  
		Last Modified: Thu, 23 Jun 2022 18:15:52 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16cad75e16079e4d57cb7f3b405757a530ebb200bc378e32433324421ef129b`  
		Last Modified: Thu, 23 Jun 2022 18:15:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2a2a687a7034728f932e6de39c103484a661db17d7a8cc3dae85ddee019548`  
		Last Modified: Thu, 23 Jun 2022 18:15:52 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7cce09f93611c69d641fbd1878f1f556610cb45e8faec3ee1f8a37f6964f89`  
		Last Modified: Thu, 23 Jun 2022 18:15:52 GMT  
		Size: 4.7 KB (4699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:latest` - linux; s390x

```console
$ docker pull postgres@sha256:259d6617c7b33f5e6284cf4a90b0224d6dd918edf7dda5c99d6df4cf705bdd55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85165147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a325fb7ca04e7e135bad989e7d34311f741368b766f077e7eaac71617fa698f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 23 Jun 2022 00:43:10 GMT
ADD file:0b511e3efd87267fb27161eae56c4d08f0fed733697da6ffe6ea96a4cb68e938 in / 
# Thu, 23 Jun 2022 00:43:15 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 08:08:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 08:08:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 23 Jun 2022 08:08:59 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 08:09:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 08:09:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 23 Jun 2022 08:09:28 GMT
ENV LANG=en_US.utf8
# Thu, 23 Jun 2022 08:09:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 08:09:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 23 Jun 2022 08:09:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 08:22:28 GMT
ENV PG_MAJOR=14
# Thu, 23 Jun 2022 08:22:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 23 Jun 2022 08:22:29 GMT
ENV PG_VERSION=14.4-1.pgdg110+1
# Thu, 23 Jun 2022 08:31:33 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 23 Jun 2022 08:31:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 23 Jun 2022 08:31:45 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 23 Jun 2022 08:31:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 23 Jun 2022 08:31:47 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 23 Jun 2022 08:31:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 23 Jun 2022 08:31:49 GMT
COPY file:925d466681c8349f58385c00a8caa567c76b695158aa04bf4ad2ac92604e11c7 in /usr/local/bin/ 
# Thu, 23 Jun 2022 08:31:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 08:31:50 GMT
STOPSIGNAL SIGINT
# Thu, 23 Jun 2022 08:31:51 GMT
EXPOSE 5432
# Thu, 23 Jun 2022 08:31:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c547f465e0c8708ad0c57cf09caa52f4c2b5b295bf10ab1ce71ca17ff81ea36a`  
		Last Modified: Thu, 23 Jun 2022 00:51:59 GMT  
		Size: 29.7 MB (29655262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095780b4f3c40e915ed76f2089ae36b1cecb78fa3c87b5c0c904cbeee8298fe8`  
		Last Modified: Thu, 23 Jun 2022 09:17:41 GMT  
		Size: 4.3 MB (4302483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8a7df919000a6bd661a7ba6cd5438c045e1acc3a0783182de465bb0bdb3e98`  
		Last Modified: Thu, 23 Jun 2022 09:17:41 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a1e57d482182b54639d65add607526ee7afde0ff3d5f00eaa3e0d9d7a893c4`  
		Last Modified: Thu, 23 Jun 2022 09:17:41 GMT  
		Size: 1.4 MB (1381679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaaa6c43b3581001bd0b12339d2fe654d4e7bb10d375cafa1d18596de945a1d`  
		Last Modified: Thu, 23 Jun 2022 09:17:41 GMT  
		Size: 8.1 MB (8099231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d2861463c88cc1e226d3e20ecbe08c3881b4326a427e2049a046351f0ce2f3`  
		Last Modified: Thu, 23 Jun 2022 09:17:39 GMT  
		Size: 1.2 MB (1238070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6c3240a377326867bf202f16784508362cee1b29faa3a9266c46134fcb57cd`  
		Last Modified: Thu, 23 Jun 2022 09:17:39 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d4b5cce3748d8838bda90cc17d89876c5ab51b0fec445dd6b7f484e5d60b3b`  
		Last Modified: Thu, 23 Jun 2022 09:17:39 GMT  
		Size: 3.2 KB (3191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0febd3242d968847724bcdccb28d970bf86acd0802e1abe56516b19c69fb35f9`  
		Last Modified: Thu, 23 Jun 2022 09:18:07 GMT  
		Size: 40.5 MB (40468711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f253f13d299ae175bd9b5b269bafd0ce1b8609a853a6167f2e60fb0b10c020c8`  
		Last Modified: Thu, 23 Jun 2022 09:18:01 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70615c9c1ff00d45df12bb228c6555fe3455bfac0bcb410f05e13450573be2eb`  
		Last Modified: Thu, 23 Jun 2022 09:18:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b046c0b506c1a3252dbec1d85d889a7c8c441266387e0ecc2555e7570f2d85e4`  
		Last Modified: Thu, 23 Jun 2022 09:18:01 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a092a4551fcb7f746b552a62bb12bfb0ea95328268bf0df06942da6fd6be72a`  
		Last Modified: Thu, 23 Jun 2022 09:18:01 GMT  
		Size: 4.7 KB (4703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
