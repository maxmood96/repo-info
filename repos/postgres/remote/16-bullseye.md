## `postgres:16-bullseye`

```console
$ docker pull postgres@sha256:b1999f536918cc1286db87b84822abc6c74ae7e5cc5fc00b00816c953de5207d
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

### `postgres:16-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:2565c2b1392858568fdebedde25218c9e259c87c9f559b0d74005451fdebfc9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149407585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ff387d00bb9abe14fa64884fceb053593302a6f78cf4c066815a91768a4b31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 May 2025 17:29:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=16
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=16.9-1.pgdg110+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d71a2394dd18668cc9a66fd9f4cbda2c37fa9be6692559b615b477f1cd887d`  
		Last Modified: Wed, 21 May 2025 23:19:44 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5100f78397796e4095b43862c37a017c87f5c318a5ad8ef2b273a9d6822d223a`  
		Last Modified: Wed, 21 May 2025 23:19:44 GMT  
		Size: 4.3 MB (4308177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a201b3249ad4ea6b3c4e251c8353edcd373a498aa874eeb9d2006d6ee1e494a3`  
		Last Modified: Wed, 21 May 2025 23:19:44 GMT  
		Size: 1.5 MB (1473570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976d0e431bf9cca082419b939cb246558c7704f6e6789fa8e08adcb6c8183d80`  
		Last Modified: Wed, 21 May 2025 23:19:44 GMT  
		Size: 8.0 MB (8045821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc21b0e6721e5999cd1993c860c7663d3972c6fbada92c3a7776d2da6b4568ac`  
		Last Modified: Wed, 21 May 2025 23:19:45 GMT  
		Size: 1.0 MB (1038338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc0b67e892e9d4ca5ac55b7fe63f88e5d2c62fd45f1e794f076c9fc1836c6c6`  
		Last Modified: Wed, 21 May 2025 23:19:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa3986bdd1350a94a3b465907f45213c16f16d787bdf00c76a45e032d0c8cf3`  
		Last Modified: Wed, 21 May 2025 23:19:45 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285a681326102eb837d973ea4448580d9cf0520f9574c706310ac9fcec75ac0c`  
		Last Modified: Wed, 21 May 2025 23:19:47 GMT  
		Size: 104.3 MB (104264926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8904fcf74ef2e2568bcf5e33901acd6b3d6897ad9c1758a9e0297ec839645fe4`  
		Last Modified: Wed, 21 May 2025 23:19:46 GMT  
		Size: 9.9 KB (9917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bf2f29c459b41510a89302a2e464dd1a6794c93907df1ecd62184ab741f5b7`  
		Last Modified: Wed, 21 May 2025 23:19:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aad0993d3953d0b345c92edb1d1ba5bbf6c05300746af22e18d72fdb9895f0e`  
		Last Modified: Wed, 21 May 2025 23:19:46 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6cde86603854ccce4a4893c45b2f9d7c5544ce4db0668958509440ed966685`  
		Last Modified: Wed, 21 May 2025 23:19:46 GMT  
		Size: 5.5 KB (5471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787a9cfb8957b13d6feb2761abcb91edce84067d6dbb1b05836729af25832792`  
		Last Modified: Wed, 21 May 2025 23:19:47 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:dd4e7dec0115cca958ea71c3793d3b47cfd3602aa3479967b3e633d4681ce37e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6131639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f403b2cab4986075c36d01a9ee61bc29b5d85ebf68d910a5a9a6dc8357417102`

```dockerfile
```

-	Layers:
	-	`sha256:8908e76e12bea05830d756937a74ab43f8bff009f788fa170b2c5292b45b6a62`  
		Last Modified: Wed, 21 May 2025 23:19:44 GMT  
		Size: 6.1 MB (6078177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fcf98b81d522da8126aa5c22931cb0296963a1e7eaf4be7160b2bf2df54ddec`  
		Last Modified: Wed, 21 May 2025 23:19:44 GMT  
		Size: 53.5 KB (53462 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:c1294602a63e7427edb51d3d45ba889138a39943547b13c24d82db43212167f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141443891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf2e948251ce55ce97fd01a65aa39234c188504847acefb6d42a426c8eb7a81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=16
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=16.9-1.pgdg110+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef24263d8904408d4abf0483982a747bf8153de0d52cbb43862ace352b898c4`  
		Last Modified: Tue, 29 Apr 2025 01:18:46 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be0264bb06c2bcee8451dc94c6f8355978ef236eb1a11e672dd512df9c7e7b9`  
		Last Modified: Tue, 29 Apr 2025 01:18:47 GMT  
		Size: 3.6 MB (3601746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a9051786ef8ca1e9ce4ec47810682bb5f8c26e9d78eb7e1f873f82d85c3f16`  
		Last Modified: Tue, 29 Apr 2025 01:18:46 GMT  
		Size: 1.4 MB (1439251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604c2a9e01f796a5afd8b46c903da93b951474ab34284f961ab4c3e793b7df3c`  
		Last Modified: Tue, 29 Apr 2025 01:18:47 GMT  
		Size: 8.0 MB (8044545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7035eab34ad95006258ce8e6a6d625b8c11281827a56ddc22c8384df5f25bc27`  
		Last Modified: Tue, 29 Apr 2025 01:18:48 GMT  
		Size: 908.6 KB (908650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab74d412aa207d36e88063c7272cd4c92f0e39a1c3df9afd5c17b2c29490b1b5`  
		Last Modified: Tue, 29 Apr 2025 01:18:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb07ab6f9f4f5ffcc3eb65dc7f2c635f65140e5fed60a158d072087f7a348c79`  
		Last Modified: Tue, 29 Apr 2025 01:18:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32744daedf8421028101a24f3a6fe94927aaf4aa3526073c582210825b6f8131`  
		Last Modified: Thu, 08 May 2025 20:25:10 GMT  
		Size: 101.9 MB (101886456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dd6289cbe1de9232ad68c6db04c6a85ffb3890db56c0648799c5d33be2844c`  
		Last Modified: Thu, 08 May 2025 20:25:07 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8135584de795e1d195d609559320ce07dd6d4bd96f2ea942754fc447c5ebe403`  
		Last Modified: Thu, 08 May 2025 20:25:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f24917f9272aa99d46915a1a401090b7a1d19dcb453768f05696ecb36e6e37d`  
		Last Modified: Thu, 08 May 2025 20:25:07 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce66518115a97ec5e9263f7ab60203fe87c286bbf071ba5d7bbe024a34143145`  
		Last Modified: Thu, 08 May 2025 20:25:08 GMT  
		Size: 5.5 KB (5475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3edc4cf10f5e8e054953573e44a4aa8d2acd29f0f4f4c090118cc4be0c2bc16`  
		Last Modified: Thu, 08 May 2025 20:25:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:422bba377c457a04d6ee1756495bcbd517cffa04ea5fc9cbfd35e35ce39990ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6119536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5916f7d45acd1f43dfbcba504d43e62421e135f1e12d18fb556f0a7acece68ae`

```dockerfile
```

-	Layers:
	-	`sha256:a6396edb6617cc4a23f5780f0cd675e3b83e1aa5d16ae7c1fa5d6128d844bd91`  
		Last Modified: Thu, 08 May 2025 20:25:07 GMT  
		Size: 6.1 MB (6065880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e22e1dea4d02987a966de8514c19fdce4f03cc9c37eecca643ccb752bb5e3372`  
		Last Modified: Thu, 08 May 2025 20:25:06 GMT  
		Size: 53.7 KB (53656 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:aa0071348cd6dc05439c560a528375a7e794d4aa7ef523e316e989cc054d2b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146430848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac57eeeb63f9baa42f510d45c1b66ce834fb9073cd72ea9fc0a4fbf99ea8ef8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 May 2025 17:29:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=16
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=16.9-1.pgdg110+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32236ba1b821f7c23d25fdf75521f88c96d3223ff4d2910edd70bd6adab8c233`  
		Last Modified: Thu, 22 May 2025 02:08:46 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0d3b9230c80850de668fac2e5bd9a62e220978ee0fc44a5884f3bd6f86f489`  
		Last Modified: Thu, 22 May 2025 02:08:47 GMT  
		Size: 4.3 MB (4312803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defd546e9378a792a8305e5024aab05e8b5bf2e0d6d7bd768f72c42fe731a75d`  
		Last Modified: Thu, 22 May 2025 02:08:46 GMT  
		Size: 1.4 MB (1405889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb1b788a19b9e3bca37df18caa5a08422119f78322397fb5bbced6505d845a2`  
		Last Modified: Thu, 22 May 2025 02:08:47 GMT  
		Size: 8.0 MB (8045785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef0ec8ddfab83b5e0deb2e20fd330b90628b37ee9ace4ef9d685519eb8d637f`  
		Last Modified: Thu, 22 May 2025 02:08:48 GMT  
		Size: 1.0 MB (1026595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1137dc2ab794992162498823a64a9165a7a2c92fe8f04754a932bae9919e8be`  
		Last Modified: Thu, 22 May 2025 02:08:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a6988ceff54ce62d68edc1d1a0a5056cd10320ba65103b42820fb1f0388ad6`  
		Last Modified: Thu, 22 May 2025 02:08:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e182ed4d4ba58e9ed9b5ec155f4bc3103803cfcfbcb5f8185772147a7cbb789b`  
		Last Modified: Thu, 22 May 2025 02:10:27 GMT  
		Size: 102.9 MB (102872711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0317b9f91b00fb2ec668b329f8018fa25e8c43a4a79cf4bacc1bb17f10f3c48d`  
		Last Modified: Thu, 22 May 2025 02:10:20 GMT  
		Size: 9.9 KB (9910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329908c406c576bd225c182396851cb353f7cfaad0c1243720778ea3104342a1`  
		Last Modified: Thu, 22 May 2025 02:10:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7255d30c9a1dd81bdb2b7c018ce1078104ecb275712e35736413b99b2cafab7`  
		Last Modified: Thu, 22 May 2025 02:10:20 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb1a44121490f271aa434a068298ae05cc60b281277c029423c3f58cd0b3425`  
		Last Modified: Thu, 22 May 2025 02:10:21 GMT  
		Size: 5.5 KB (5470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2876bb3cdefafc8bda8aff895f988198e7b514b643e279d567b9e851ab448d0e`  
		Last Modified: Thu, 22 May 2025 02:10:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:8da918eb16f61833d5096fbc55c9c5b2b6beafe0029fa77b73144ae6cb974f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6138172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc62d3d1edfd1833e7ed86127a8e7c2254be76bf45c6f57ae0f8c6f2eca3099f`

```dockerfile
```

-	Layers:
	-	`sha256:581bc17071b4e1143eb0b979b939abcaa803e7d4425c834f1ff697155a95e57b`  
		Last Modified: Thu, 22 May 2025 02:10:21 GMT  
		Size: 6.1 MB (6084465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:781b80ee568a68b08acb389af2957cbf23e43afc280a1f7478b30bcf0a62e79b`  
		Last Modified: Thu, 22 May 2025 02:10:20 GMT  
		Size: 53.7 KB (53707 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:cd793e1916e6756f6610156cafc475e8a17d85c485812dd48df5aa6b4f44e653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162118851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509ab46ed9eefab6d7bea3a269102c2357171f40a3f5b492fd1bb3a792544614`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=16
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=16.9-1.pgdg110+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b8e7965452a87aaf6879747c5ee09f2a65a63db79c6eafc5f4e97fd36dbd6b`  
		Last Modified: Thu, 08 May 2025 19:26:49 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e9f1db341c89d9697f59713078643b0b053acbfea54505c9c786d3940f8625`  
		Last Modified: Thu, 08 May 2025 19:26:49 GMT  
		Size: 4.7 MB (4719645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fec5af2e464bd82b91e9327b83bda470c587bbb8f2e94e4a0b4cb702816214d`  
		Last Modified: Thu, 08 May 2025 19:26:49 GMT  
		Size: 1.4 MB (1447753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056faa6fadf9b615ae4061c04eaed056561397dd2cbd206cc00f5684659188de`  
		Last Modified: Thu, 08 May 2025 19:26:50 GMT  
		Size: 8.0 MB (8044290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ba64e8a5ef7507f2fbc6edaaa259a7528f71fffaed9faf491702768149a0dd`  
		Last Modified: Thu, 08 May 2025 19:26:50 GMT  
		Size: 1.0 MB (1028916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dde8246f9160b7be1e2f69f8d5471dd47d676eeb3c7777d3fe4f27f244facea`  
		Last Modified: Thu, 08 May 2025 19:26:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3490d248c83b1bfa00798d02b827087ddd77f4d0b33b6bafb5342a65b6c12dde`  
		Last Modified: Thu, 08 May 2025 19:26:50 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e677c2251f7feda680afc10a73396d4cfe2e898e3d79b4da9692148add265a6a`  
		Last Modified: Thu, 08 May 2025 19:26:54 GMT  
		Size: 115.7 MB (115669545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82f67ca368b4183263391d3e5de359aa6f913f1d179a0cfc31fa4430ec62a2b`  
		Last Modified: Thu, 08 May 2025 19:26:51 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c24ca6ee5022f2d008a742dbaf9265ed5b4d94de6d317822aa6df1dbc3559a3`  
		Last Modified: Thu, 08 May 2025 19:26:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d0322bafafeaa4107e5e3cb284b5404da8e59619bea8196f0274ef57190f9e`  
		Last Modified: Thu, 08 May 2025 19:26:52 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f34ceeb0d76cff9691c874b0d2f6054c77ea29b1026c73abb304f2b79cb5254`  
		Last Modified: Thu, 08 May 2025 19:26:52 GMT  
		Size: 5.5 KB (5475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c679b45a7dc234e894ab0d94173fc3b4311377f26c32ef75368ca19f300e7e`  
		Last Modified: Thu, 08 May 2025 19:26:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:353d3f89a9fcc901f2d5e15d2578d86379afd928f4473fe0ef78590a8e5e6ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6116958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97666ce96c677b509381cd51d15948df923032ac2040aebfb2ab896a7618928a`

```dockerfile
```

-	Layers:
	-	`sha256:1d0bf17b71bafd3c4840a9687a9bb6b16707ad2a909323fdf1ea8efd738a58c4`  
		Last Modified: Thu, 08 May 2025 19:26:49 GMT  
		Size: 6.1 MB (6063540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d068dc01ad7165e7c80372c05e3ee452ec5279a3cf25600b131a71c92adbd4`  
		Last Modified: Thu, 08 May 2025 19:26:49 GMT  
		Size: 53.4 KB (53418 bytes)  
		MIME: application/vnd.in-toto+json
