## `postgres:16-trixie`

```console
$ docker pull postgres@sha256:593b7a9d81eeb8ae9017c20d8feea985eb03b7de5e468e407e9190c0e04ab3f3
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:16-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:6371bbbc04ce70e76bb63eded63d3107a4e45b53e55e6229c664a3345f9a7ac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160091789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c1acb89ae44b0bc936fdad9c7bcf32a2300ef1dbab9407bb6dd12eaee1c8c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:59:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 04:59:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:59:59 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 04:59:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:00:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 05:00:04 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 05:00:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:00:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 05:00:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:00:08 GMT
ENV PG_MAJOR=16
# Tue, 18 Nov 2025 05:00:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 18 Nov 2025 05:00:08 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Tue, 18 Nov 2025 05:00:19 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 05:00:19 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 05:00:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 05:00:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 05:00:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 05:00:20 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 05:00:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:00:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 05:00:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:00:20 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 05:00:20 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 05:00:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115db6d16b770c0d78217daa599dd2c53319df826dd76b8e5c0f5d5b7448128a`  
		Last Modified: Tue, 18 Nov 2025 05:01:05 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ff652dc2317dd48b9411d8cfcc815960fa241dbf6a900570ce9dd7d545cde2`  
		Last Modified: Tue, 18 Nov 2025 05:01:06 GMT  
		Size: 6.4 MB (6436658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2bcb52083ba266e74a4ff022f72ffd437f599e94e39c0b4e13120b0d7ba61a`  
		Last Modified: Tue, 18 Nov 2025 05:01:05 GMT  
		Size: 1.3 MB (1256603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c4e00df3b46e513e49c148d564f5ffe58720054d30c2c02ea8126434561576`  
		Last Modified: Tue, 18 Nov 2025 05:01:06 GMT  
		Size: 8.2 MB (8203771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fde4663855c283c192591d7a3e0103d3760b881c5292040089a362118e7d96`  
		Last Modified: Tue, 18 Nov 2025 05:01:05 GMT  
		Size: 1.3 MB (1311473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fe86bc7f87487dc5488f9c1cf10b302d2d41c5068ff7eed5a35936a3d77d4d`  
		Last Modified: Tue, 18 Nov 2025 05:01:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e54379c54081e5b2d5fcbc817cf2af1c82db2dd037c79ff7077878c699f4d6`  
		Last Modified: Tue, 18 Nov 2025 05:01:05 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3e79aa53c60794fbe220b88c863c20b73134cb98ee3b7a2985fcc33c660ad4`  
		Last Modified: Tue, 18 Nov 2025 05:01:11 GMT  
		Size: 113.1 MB (113086043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edb059d627d726e71ac78fbae241afbb3c13ef916536784106e8b52c203fd70`  
		Last Modified: Tue, 18 Nov 2025 05:01:05 GMT  
		Size: 10.0 KB (10012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb5da4cc6c32bee09891c59d24f97f6f7d5de5145aa906720cda5aca9896705`  
		Last Modified: Tue, 18 Nov 2025 05:01:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d674417549526cc143892bfd57b3d52db88d2481b9154b7452e8b3c5a88d272`  
		Last Modified: Tue, 18 Nov 2025 05:01:05 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e5c9408eb3d8d16b1e628b840450d329c94df8ffff1cfe189bea49e0e0f1bd`  
		Last Modified: Tue, 18 Nov 2025 05:01:05 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e588012c9445cb8fee1f28e7047d0b4da00b0e0b4279afd369f155bfa2e5b07`  
		Last Modified: Tue, 18 Nov 2025 05:01:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:5b236da42e48f18935ed445e245c63d3155817e54eceb61c182135ad121b23c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b26ee60abfe36034c8022e9896f35bb5284ddfa4f87b54552c01eb53312d4b`

```dockerfile
```

-	Layers:
	-	`sha256:b85d0e6359484521fd0c8250e0163c763bb7502a07471eced3899cb59f11d373`  
		Last Modified: Tue, 18 Nov 2025 06:11:21 GMT  
		Size: 5.7 MB (5708446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6f7ddee4bf8453c112a813268a9270d89866edfc01e0e262daacc50f134451c`  
		Last Modified: Tue, 18 Nov 2025 06:11:23 GMT  
		Size: 53.9 KB (53869 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:11ea422f2816148aecce33b24a650f9088f7ff6018a639e5edbdf06b1ecf5bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154137902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebeaaa463a8868f12ad8f2a570568781cd82bcd565545f3ba5ea7fe508ef2081`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:05:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:05:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:05:43 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:05:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:05:51 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:05:51 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:05:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:05:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:05:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:05:59 GMT
ENV PG_MAJOR=16
# Tue, 18 Nov 2025 03:05:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 18 Nov 2025 03:05:59 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Tue, 18 Nov 2025 03:22:21 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:22:21 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:22:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:22:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:22:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:22:21 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:22:21 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:22:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:22:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:22:22 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:22:22 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:22:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9114657d2bf1ff9fbea075558bfcec7bdba57e3eb25c774f763ec517bae17113`  
		Last Modified: Tue, 18 Nov 2025 03:21:20 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668a2e2f9c3056ff2b84e7aa7d5835f3ba4c23b5d3b2fc3c24413a43ae315391`  
		Last Modified: Tue, 18 Nov 2025 03:22:51 GMT  
		Size: 5.9 MB (5928980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0292203e1324672fd71cf8bd4a88200b25fb053ba2bb5ffebbb914ca5d7d07c6`  
		Last Modified: Tue, 18 Nov 2025 03:22:51 GMT  
		Size: 1.2 MB (1227375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fc8246633d5aaa74bece5928d3cd101f912578c5bba47918740cff00badfcd`  
		Last Modified: Tue, 18 Nov 2025 03:23:02 GMT  
		Size: 8.2 MB (8204176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd280e2cacf378b660cd7b6b3c2f48e834d1fc12d40b59d5ea0698b7d996e26a`  
		Last Modified: Tue, 18 Nov 2025 03:22:52 GMT  
		Size: 1.3 MB (1317174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e313c2c4e7f663e3fdd9213ade331064d3685363c5fa9dda9ed7ed06720a062`  
		Last Modified: Tue, 18 Nov 2025 03:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981d4d3d3c04c03ae287053bed393ec40016093fb401261ac414e2005d57c4f2`  
		Last Modified: Tue, 18 Nov 2025 03:22:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb3c08599db589c4cc2f6e72f19a0d4106c86b2b05586ffce8d0cbe7bdd79f0`  
		Last Modified: Tue, 18 Nov 2025 03:23:00 GMT  
		Size: 109.5 MB (109495296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e1a0fb2c9984effa65bff92443ca0a3d735aa24c76228c231f42f83b462c53`  
		Last Modified: Tue, 18 Nov 2025 03:22:52 GMT  
		Size: 10.0 KB (10007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8d45ae80ccfbbd02c942e4a9a081742b05c9d8b3a33dd8d1bf43879fae0043`  
		Last Modified: Tue, 18 Nov 2025 03:22:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04ac2ff6fded66795f63f0c1246b7a5ba031fa6b6f95ede44ba8c50a38c9510`  
		Last Modified: Tue, 18 Nov 2025 03:22:52 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef67705172fc6bb622c4e679a1c058564c5957d514fafe740c0a8fe631a63a`  
		Last Modified: Tue, 18 Nov 2025 03:22:52 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedafee62ef6acfb94d0cc7c8805df4f1b333824f809cfbf505bdeaaf6538fe5`  
		Last Modified: Tue, 18 Nov 2025 03:22:52 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:6b144d830885e212bd08ad468e66e5d50fcb7e2793d74c15c4bd57b2a12eafa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5779175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ecc947d79aff30309e0d913bdf953623e1e4dd837a160ed441e0e2d8aa9284`

```dockerfile
```

-	Layers:
	-	`sha256:a172f2ed0c86e79a3149d6f918746c298520bc8ab9dcec2e8d3ecf4c8ca01898`  
		Last Modified: Tue, 18 Nov 2025 06:11:27 GMT  
		Size: 5.7 MB (5725084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdcc2800ed2dcdd344aa86e2d5e3771cc4919f80c28d61a33be05dfe04f053f5`  
		Last Modified: Tue, 18 Nov 2025 06:11:28 GMT  
		Size: 54.1 KB (54091 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:475308b89518abbbd996ee30dd70582a5b04263026d0b560d8a007f451936f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149185234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc1ff3d0b10f4eb97485a58b094f42ce919fb78033c3f2865ddc0835df1014c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:27:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:27:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:27:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:27:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:27:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:27:37 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:27:42 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:27:42 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:27:42 GMT
ENV PG_MAJOR=16
# Tue, 18 Nov 2025 03:27:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 18 Nov 2025 03:27:42 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Tue, 18 Nov 2025 03:42:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:42:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:42:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:42:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:42:32 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:42:32 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:42:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:42:32 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:42:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:42:32 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:42:32 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:42:32 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c830ea1cb20a1620db3c38bfa5e06343ef89fdbf8d05db8e7895744bf82be38a`  
		Last Modified: Tue, 18 Nov 2025 03:43:02 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a888dc12dbb4b6f7009806807ab32afdee5bf59f79173ea9bf110132de2932`  
		Last Modified: Tue, 18 Nov 2025 03:43:02 GMT  
		Size: 5.5 MB (5496826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4e76d5fb1ceb51cdd5cc40adb0b570f6057bad7bee267a037b02b190bf7778`  
		Last Modified: Tue, 18 Nov 2025 03:43:02 GMT  
		Size: 1.2 MB (1222267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8406832b408b81458d3459f9ea67cb734f69a7481c6c9363e6f3edbc1356815`  
		Last Modified: Tue, 18 Nov 2025 03:43:02 GMT  
		Size: 8.2 MB (8203936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada201d9f531e0150f52c94bcaeaff385a4093297a75bdab00769c10a3386a22`  
		Last Modified: Tue, 18 Nov 2025 03:43:02 GMT  
		Size: 1.2 MB (1172447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a179367704505bd9a252887b0ab507166165eaf9a2e6630eccde14298123140`  
		Last Modified: Tue, 18 Nov 2025 03:43:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42838853804a59f54d1f1a80f96c1ca3b942da6fc7fb93cbb10a68e50d27301`  
		Last Modified: Tue, 18 Nov 2025 03:43:02 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3def2db51fde300aa1144049c32f2a91911b5c91b52e44c8ba436a70e07bed1c`  
		Last Modified: Tue, 18 Nov 2025 03:43:08 GMT  
		Size: 106.9 MB (106859028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d33ac0c142e77572dab2c530f1d8a678425c9844d154ee7dce4ecbc7ff5b4a`  
		Last Modified: Tue, 18 Nov 2025 03:43:02 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4903564fe8cfba009918fc23babe40ea6a8160a5bff3fb3c9baccbd6e4136c5`  
		Last Modified: Tue, 18 Nov 2025 03:43:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6c3e7cad1eeadf003bc1409745cad2ddeefba7ede80a6a5009c59f3d9c6f8d`  
		Last Modified: Tue, 18 Nov 2025 03:43:03 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ea400392697a3acfcff95c2cf347d7e001741444b9b60f00663b18138e20eb`  
		Last Modified: Tue, 18 Nov 2025 03:43:03 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089216c02a20e2f87198e8921d54a02bf0f56a8fc51257a721cc41acc3cc3c83`  
		Last Modified: Tue, 18 Nov 2025 03:43:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:89033a94db100be2a25d9739f854861c6850a7df155754df04b311fcd8e36e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae41ee3c3bb8b70dee141469e734cf01dbd8db2bcd4605c9eccf2d6931f74592`

```dockerfile
```

-	Layers:
	-	`sha256:e03197f200d09b250b4e7540c5ecafc32ef4beb7c50c87b1b368e9bbe1eec956`  
		Last Modified: Tue, 18 Nov 2025 06:11:32 GMT  
		Size: 5.7 MB (5724389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f0c6d9dd8e7aef3bd8a39f701e2af2012e65e8c995a73db2840d5956f3e601`  
		Last Modified: Tue, 18 Nov 2025 06:11:33 GMT  
		Size: 54.1 KB (54092 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:cd129acb9c0ce1f6ea52c5b9eb0ed0402dd8ab5db6743f87d6b853f6d41ea34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158723977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1985473f7ae970994caab2ea5d0bc7d72ecc3d7dd782a0989112fc2d928ed5d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:02:50 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:02:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:03:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:03:09 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:03:09 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:03:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:03:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:03:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:03:14 GMT
ENV PG_MAJOR=16
# Tue, 18 Nov 2025 03:03:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 18 Nov 2025 03:03:14 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Tue, 18 Nov 2025 03:03:31 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:03:31 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:03:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:03:31 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:03:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:03:31 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:03:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:03:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:03:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:03:31 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:03:31 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:03:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac530c5dbb8a0b468394e6b2631d665d09c435aa18553eef1cadf3ae25cdc700`  
		Last Modified: Tue, 18 Nov 2025 03:04:00 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dc1dffde41266b9b49e34f558e12413fc9b75aefd9bfb755caf434b5dc0a88`  
		Last Modified: Tue, 18 Nov 2025 03:04:01 GMT  
		Size: 6.2 MB (6232042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5bae82822169d1a145bef60a585ad3fd9084df0179c116c231b5de12b35ad3`  
		Last Modified: Tue, 18 Nov 2025 03:04:00 GMT  
		Size: 1.2 MB (1209476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ea3abb40c9cea7e33f53edd41a82037bd1e6fd68a7184987458a76d76c6eab`  
		Last Modified: Tue, 18 Nov 2025 03:04:01 GMT  
		Size: 8.2 MB (8203923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca933282bd110a6823083670b1a5e0c7215c40e29c3d28b13047f299ccb7486`  
		Last Modified: Tue, 18 Nov 2025 03:04:00 GMT  
		Size: 1.2 MB (1220457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea72566aa99e252a3fb520188486c70847cffe79d31a21fa2f25e3ade37ad25f`  
		Last Modified: Tue, 18 Nov 2025 03:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f198b7142ade0fa930b574ad9d95b88ffd1cb8c9e596f49c678a1e4b328f7cc`  
		Last Modified: Tue, 18 Nov 2025 03:04:00 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a0d9b23cb4640546d307aaf6835ea50cb67f12bbca63af278652df9469fca0`  
		Last Modified: Tue, 18 Nov 2025 03:04:13 GMT  
		Size: 111.7 MB (111698698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f9438f5dc4aa54f01f98d9174a728ca04a10acd2336d01b3fa45ce27d114fe`  
		Last Modified: Tue, 18 Nov 2025 03:04:01 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d04407643bc4880ff2936fb08b06043c61cc049542b0d71be62d5a8ff35bec0`  
		Last Modified: Tue, 18 Nov 2025 03:04:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f605ca2336daf233696ea8369341a8c5f978a1972272de2966c61c9af5791562`  
		Last Modified: Tue, 18 Nov 2025 03:04:01 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021d4a50b074af0061a6cc9742ef993c41c8e076ccdc794bb0760925a257a083`  
		Last Modified: Tue, 18 Nov 2025 03:04:00 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abaafaeb462a45179b12a95c55206f3b1d7cc72b911ea9b36518898fc119600`  
		Last Modified: Tue, 18 Nov 2025 03:04:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:b7606d1fd1772d42931d2453b58dc27be962403e485961378d4db47af78a203b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4564d40c9e5faf66c2a20cf38b9f6bc364f14005cdf97c3c192b90e8d96414`

```dockerfile
```

-	Layers:
	-	`sha256:e06cf83bfd4e7a6ebea91c7fee599859d4554813efc116122e32ebc5b280d6b7`  
		Last Modified: Tue, 18 Nov 2025 06:11:38 GMT  
		Size: 5.7 MB (5714792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e57ac5dd4df606344f7a2ff1bd98f044ac41181b92c0326cd00c94c92325da5b`  
		Last Modified: Tue, 18 Nov 2025 06:11:39 GMT  
		Size: 54.1 KB (54138 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; 386

```console
$ docker pull postgres@sha256:956173f583cf64179b3909cafb702df6f2edf31cebaa1cbf04a9be24b5e0482a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.2 MB (169229013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab9dda67fc27f71434a8a5505459139938a31e21060da82062290b2443efaa0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:42:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 02:43:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:43:09 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 02:43:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 02:43:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 02:43:14 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 02:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:43:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 02:43:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 02:43:18 GMT
ENV PG_MAJOR=16
# Tue, 18 Nov 2025 02:43:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 18 Nov 2025 02:43:18 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Tue, 18 Nov 2025 02:53:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 02:53:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 02:53:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 02:53:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 02:53:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 02:53:57 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 02:53:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:53:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 02:53:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:53:57 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 02:53:57 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 02:53:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e960c829aa52f4e1d79c4955050dec2dd62f61eff29b6616e841698f4dd54926`  
		Last Modified: Tue, 18 Nov 2025 02:54:27 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46b90b88a5cf162011a5f30fd3bcb58b708c288734307526f50f32561619a13`  
		Last Modified: Tue, 18 Nov 2025 02:54:27 GMT  
		Size: 6.6 MB (6629602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ace0a556e5c362a368c223acce27e8f748231374a285c856f08912dbb0d359`  
		Last Modified: Tue, 18 Nov 2025 02:54:27 GMT  
		Size: 1.2 MB (1225716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ac6f63f1b61a20957963fffcb23c10f7736c78d6e73b212d4a5412b6b0e14`  
		Last Modified: Tue, 18 Nov 2025 02:54:28 GMT  
		Size: 8.2 MB (8203941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18582b468ab76be5c05eeae83cd90abc2cf9d15bb21610734b6effb5950da7c`  
		Last Modified: Tue, 18 Nov 2025 02:54:27 GMT  
		Size: 1.3 MB (1308176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f870ae2a16f83205108a0529cb6de27d167c2cd1e19516e98ad4fdeced4fb1a`  
		Last Modified: Tue, 18 Nov 2025 02:54:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7a897b443f35d6d2907604ff91578d028e9384fc202ecbf37bbd56852ab4ba`  
		Last Modified: Tue, 18 Nov 2025 02:54:26 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7ce50966ef43579a465ce6fb67e55776957dc28d08845315dd7453a6fc9812`  
		Last Modified: Tue, 18 Nov 2025 02:54:36 GMT  
		Size: 120.5 MB (120547748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b1ba6d8c7db7f7127edff15593440fd3f6401e4260022203b077f221df3700`  
		Last Modified: Tue, 18 Nov 2025 02:54:27 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5fe2641e09ecc839b7db3fcb6d255aa70c55363926a17e099a9fcdfbe679ca`  
		Last Modified: Tue, 18 Nov 2025 02:54:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0caa1f011b262d4305b2e39842f2a6e89cf2ce56b7985dd296162575a6bec4`  
		Last Modified: Tue, 18 Nov 2025 02:54:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6d33f39f9e816a4a44a706e5ebe0aa8c221e7af7a46f65463d62118936ab99`  
		Last Modified: Tue, 18 Nov 2025 02:54:27 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cb5d9fe8f050fc90b9f7ccf39424a76b44fe18cc45ca837ce827867e2b31b6`  
		Last Modified: Tue, 18 Nov 2025 02:54:27 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:8f1695a5ebf3d01463577546412d211f0ab5860ed076527182b7486cc42821cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49a033110d5a748489a96afdea0c933fe470c296cf5ce8ba75ce8f21c9fd2c7`

```dockerfile
```

-	Layers:
	-	`sha256:ce3d042599b843c626d6a2200d5d0787b45f55e2eebdba6fae0a9826d06be765`  
		Last Modified: Tue, 18 Nov 2025 06:11:43 GMT  
		Size: 5.7 MB (5723977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bd3ecbb83a5f1e31b43b62ff6e29d919235b6f352166f9c5033f67b762aa6c5`  
		Last Modified: Tue, 18 Nov 2025 06:11:43 GMT  
		Size: 53.8 KB (53815 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:754448e221f708504de6b658f61a3ff70e696011ba6b7b040506e1334e05ad44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172376364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f91a0f81b81326b1ed7ea9282eac8970473374624fc15c5f3f23dab39f37f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Thu, 13 Nov 2025 21:03:42 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:03:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:04:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:04:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:04:18 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 13 Nov 2025 21:04:18 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:04:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:04:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 21:04:27 GMT
ENV PG_MAJOR=16
# Thu, 13 Nov 2025 21:04:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 13 Nov 2025 21:04:27 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Thu, 13 Nov 2025 21:27:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:27:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:27:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:27:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:27:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:27:19 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:33:37 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:33:37 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:33:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:33:37 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:33:37 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:33:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fc0061372adf3d63a13d2ca7ad0f3e93c559c4946c804f4b6cd8188fe82e18`  
		Last Modified: Thu, 13 Nov 2025 21:06:27 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ea4eea6db9d73280f2865808f223f2945540e75194b34d58d0d2cd5fdd4dc5`  
		Last Modified: Thu, 13 Nov 2025 21:06:28 GMT  
		Size: 7.1 MB (7075854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0055703ee1b9b5dd2d9c1885a2faa38d17a66494ad29256b526f245153a6fc3b`  
		Last Modified: Thu, 13 Nov 2025 21:06:28 GMT  
		Size: 1.2 MB (1214665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e1fc3e056b0187b8b00b4418da5ff6a096b7b79d7699c38c5d901b98afd435`  
		Last Modified: Thu, 13 Nov 2025 21:06:29 GMT  
		Size: 8.2 MB (8203908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa191b7869bd1800b18f744f13025fd248b9169d56129121df2164e220d7fcdc`  
		Last Modified: Thu, 13 Nov 2025 21:06:28 GMT  
		Size: 1.4 MB (1394701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cfd16d3ad528deda1ab9495135db3760b28e8ae530af5fee50698783255c7f`  
		Last Modified: Thu, 13 Nov 2025 21:06:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c324574916baf5af487c21d6adcf241528368e98ec6817195d55bf1c67434b6`  
		Last Modified: Thu, 13 Nov 2025 21:06:28 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231d6148e4eb4e282ab3e9094fb3da8eb320faf504a30e30d234c00b104ebeba`  
		Last Modified: Thu, 13 Nov 2025 21:28:28 GMT  
		Size: 120.9 MB (120867827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a59bb620153ba6d11e2dedbb081202c95fdbd87ad1989cee519a7291df01d5`  
		Last Modified: Thu, 13 Nov 2025 21:28:15 GMT  
		Size: 10.0 KB (10014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ec99b6dfb6cc3bb6e38d5381ddb8a629eb42ecf61c416bedef916028daf0e6`  
		Last Modified: Thu, 13 Nov 2025 21:28:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0712708d7f3c8408648dc7033cbb6815ff5e011f4d1c6ce7719e5b87d40c50b`  
		Last Modified: Thu, 13 Nov 2025 21:28:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2cecfdcee701c0a824bcb36262c49e3436aade179d3e870f0806ba48fe4c34`  
		Last Modified: Fri, 14 Nov 2025 19:34:19 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05719d0c55a4875bca10dfcb20088ddd74ef00db26fd437195c9d28157b0707`  
		Last Modified: Fri, 14 Nov 2025 19:34:19 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:dcdd064f61c20ef832ef204fe91f845f0a55eebd9e2cf9bba92b038bb5a62c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8fdaf673e1870a83fb29442a2ffb09b1d0cb97993838844713c28bc1b7c3ff`

```dockerfile
```

-	Layers:
	-	`sha256:ab687158d720dd8b08f3efb35efceeca575f0bc51fa84ed2bf51fe20bc5eacbd`  
		Last Modified: Fri, 14 Nov 2025 21:13:12 GMT  
		Size: 5.7 MB (5715065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1cc07b151989b8a0f2c49e7fa431943cfdb561f05336d2d68e72db6e010d3f1`  
		Last Modified: Fri, 14 Nov 2025 21:13:13 GMT  
		Size: 53.9 KB (53934 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:2fd10a59494d205b9d2df9b8bac726901ea0b2a947eff41b4ecd2a406f54e6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91558577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2513d4a34b314bf39cf1ba1bf4d20c5becde126fe4c199bef7efa68ab94f79a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 23:37:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Nov 2025 23:38:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:39:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 23:39:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 23:40:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Nov 2025 23:40:04 GMT
ENV LANG=en_US.utf8
# Tue, 04 Nov 2025 23:40:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 22:03:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 22:03:34 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 22:03:34 GMT
ENV PG_MAJOR=16
# Thu, 13 Nov 2025 22:03:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 13 Nov 2025 22:03:34 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Fri, 14 Nov 2025 07:38:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 07:38:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 07:38:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 07:38:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 07:38:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 07:38:41 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 15 Nov 2025 07:40:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 15 Nov 2025 07:40:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 15 Nov 2025 07:40:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 15 Nov 2025 07:40:36 GMT
STOPSIGNAL SIGINT
# Sat, 15 Nov 2025 07:40:36 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 15 Nov 2025 07:40:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37d55c3011ce48efe8b5340c1d17952a31a7ccbd33740e03b4beb1fa13cd08`  
		Last Modified: Wed, 05 Nov 2025 01:45:45 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740b15d328aac9b8cd6aaa0b70eb3464d2f18f8e019f9685fd9492eaacda84c3`  
		Last Modified: Wed, 05 Nov 2025 01:45:48 GMT  
		Size: 6.3 MB (6291276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a53caf52e6aba7e4dff6229654beb9afe47145c315e2b283651efb87c5512ec`  
		Last Modified: Wed, 05 Nov 2025 01:45:45 GMT  
		Size: 1.2 MB (1201883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6648770da4d060ceb20dec8e78d9224a4129eadabec3ee7fc56d287c66d5a1b`  
		Last Modified: Wed, 05 Nov 2025 01:45:46 GMT  
		Size: 8.2 MB (8203570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b7028147a73306c16d8351b86fe10a30cc70681d2316fc2d0c3d694664899d`  
		Last Modified: Wed, 05 Nov 2025 01:45:45 GMT  
		Size: 1.4 MB (1402208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67a541f6f6331fbd6d7ea6d3e646d86231d815486c4b8a6c9afaec8bba773c5`  
		Last Modified: Fri, 14 Nov 2025 00:09:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782d3cf5a012c39ef2f2953f74e44665be00398054f1c73231da9064031cc216`  
		Last Modified: Fri, 14 Nov 2025 00:09:37 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32577549cfab7840e408c75e72fde702292dd8edb8af5cb1afeacc10554de9b3`  
		Last Modified: Fri, 14 Nov 2025 07:41:26 GMT  
		Size: 46.2 MB (46163086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82427006ff65da705fd1f4142b9837ee7d660cd9be827cf4d0092cce19535208`  
		Last Modified: Fri, 14 Nov 2025 07:41:22 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed6362e295a60c02f5a257ade32e235a3a0e23ccbd4ca5081079264c271c84b`  
		Last Modified: Fri, 14 Nov 2025 07:41:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e729966ea1ced6aa244c501fff620a322190f4c2d0907854f09d39d294eff9`  
		Last Modified: Fri, 14 Nov 2025 07:41:22 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948ad9fff54721cd4d0196b024faf9eecfda9387450e1a7ec58dc969beb755be`  
		Last Modified: Sat, 15 Nov 2025 07:42:17 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a70dea47f99e0f5440a4b264d9409149c055eedad0558c1df75b742dd52466`  
		Last Modified: Sat, 15 Nov 2025 07:42:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:16f5e1fd5d9cbf0588baad018e8bb784611ce3edb5efd1bb671d25d2e57b2802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5128660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d7fa1749a2363db7274f8229ac6b9d8e9c0a6b3d6868764c3dec5fd3908b78`

```dockerfile
```

-	Layers:
	-	`sha256:ecb790be8b91d8a42aaaf3f8e3a0ca2f7533c935bed159544151e1747fa7a77f`  
		Last Modified: Sat, 15 Nov 2025 09:08:09 GMT  
		Size: 5.1 MB (5074731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72cd3d5cc687bb08e980949b38da9622aea40f197a2fb5c16a6d348b4a4040cd`  
		Last Modified: Sat, 15 Nov 2025 09:08:10 GMT  
		Size: 53.9 KB (53929 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:4d9efa52c24eb7b42a9099e96a435dd9720a0ba2e6bbf0a59cd819713f02f985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174610813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93abb42704fd0a67c096abb145c2cd40b8ebf09fd7c5f3aea531f78b35aa2e1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:24:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 18 Nov 2025 03:24:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:25:07 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 03:25:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 03:25:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 18 Nov 2025 03:25:12 GMT
ENV LANG=en_US.utf8
# Tue, 18 Nov 2025 03:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:25:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 03:25:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:25:17 GMT
ENV PG_MAJOR=16
# Tue, 18 Nov 2025 03:25:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 18 Nov 2025 03:25:17 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Tue, 18 Nov 2025 03:50:53 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 18 Nov 2025 03:50:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 18 Nov 2025 03:50:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 18 Nov 2025 03:50:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 18 Nov 2025 03:50:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 18 Nov 2025 03:50:53 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 18 Nov 2025 03:50:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 03:50:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 18 Nov 2025 03:50:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 03:50:53 GMT
STOPSIGNAL SIGINT
# Tue, 18 Nov 2025 03:50:53 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 18 Nov 2025 03:50:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1da7a00bc065972ff7a0cc172ae5aeffd57460e2d8201e7ca7f11c9f3d91f81`  
		Last Modified: Tue, 18 Nov 2025 03:38:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6640b0fe0d4888a2c7a19f141461a945d052f3d4237638800abe357409191335`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 6.4 MB (6408826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5934d38de3ba60840502809b113b390285df853744e380bac937d7872e57ea94`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 1.2 MB (1230102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a548d3e72f4a5f82cb7897c75bf9446844f4c0ed467f8c875294c35e3bb31376`  
		Last Modified: Tue, 18 Nov 2025 03:38:30 GMT  
		Size: 8.3 MB (8258828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5896924454e3ca726939ac8bcf6bb15537624f9271e53887928e29f4e4b812e6`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 1.4 MB (1398066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b2d8b2fe721daccd41d2fc57054b8090f304d9d4f5e26f0432cc917aa23ffd`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5b90033baa0840a68a94663b272baee694f3df08e730e0dc5b0c3f76be23d3`  
		Last Modified: Tue, 18 Nov 2025 03:38:28 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce81832bc3e192dc2ab4a4d031383e0586d5d9a46214b90f3e643330e450b6b4`  
		Last Modified: Tue, 18 Nov 2025 03:51:40 GMT  
		Size: 127.5 MB (127459860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ed404d7dd8a3418d191301dd104cfa46bfb7f35cedf22c6a9965d564571391`  
		Last Modified: Tue, 18 Nov 2025 03:51:30 GMT  
		Size: 10.0 KB (10008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f953f40c060d363f0d93fbef9f85f654f037321c9dfe64e6df488e44f8858aee`  
		Last Modified: Tue, 18 Nov 2025 03:51:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d383db3777eadbd770e8289e188c64e4a95b153e98b2498ed7298b020c9737`  
		Last Modified: Tue, 18 Nov 2025 03:51:30 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37269f630de8ea9c31d288064a67d626b88780447a06cd2da39cf6cd2bcbe25e`  
		Last Modified: Tue, 18 Nov 2025 03:51:30 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f22b186308739c6d1889e85e3aabe46f3d060408325cf6529b55c907568242e`  
		Last Modified: Tue, 18 Nov 2025 03:51:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:391c6dc1711ec58faa0a80b1505225fb53da0ca4b8bfeed5662b8eb1a1b174cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a344adf0041866b4355142f7ed85d2e1969d16c90fdb8388a22b8914b238d45`

```dockerfile
```

-	Layers:
	-	`sha256:49069d907f25bc402581dcd3cd5ecffca808f4ea13b2647786c7ba85381da3ad`  
		Last Modified: Tue, 18 Nov 2025 06:11:53 GMT  
		Size: 5.7 MB (5725115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fb4f0d5c15fe36423f1fe9e3e614673630c92b127a544b2c83a79aa9bfc35b7`  
		Last Modified: Tue, 18 Nov 2025 06:11:54 GMT  
		Size: 53.9 KB (53869 bytes)  
		MIME: application/vnd.in-toto+json
