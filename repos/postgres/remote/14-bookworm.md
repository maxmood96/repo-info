## `postgres:14-bookworm`

```console
$ docker pull postgres@sha256:5a042a26a7ff1472fcaf84da0a5a73b60bce0d1c85947a1898d73f2cc364c247
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

### `postgres:14-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:74b8170e18a5b66cdd11743eb2dc24e54e75e768aaed61648dddd22ed638a862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152102682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d149b132a60b7b0ff75ed7eb899e994e6aa42827ac50c186db18641b2a276dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 May 2025 17:29:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
ENV PG_MAJOR=14
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=14.18-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c4fba1b430fb6e4f6f74ecb7439e32ef91d23655a7974749f4f1b49392046e`  
		Last Modified: Wed, 21 May 2025 23:19:59 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd81e3305cf461c8825c8bc7d03328c58135b7702322ce3484b13efbeadccc6`  
		Last Modified: Wed, 21 May 2025 23:19:59 GMT  
		Size: 4.5 MB (4533763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44b94fe3053e3116d6a401928631f35b2d6398e9c1d4ee075d01f427fd04b17`  
		Last Modified: Wed, 21 May 2025 23:19:59 GMT  
		Size: 1.4 MB (1446753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49081f9bcb297aa29c3fff941fd547c5d05cbd9551448ad41d375bbe2d24ecb`  
		Last Modified: Wed, 21 May 2025 23:20:00 GMT  
		Size: 8.1 MB (8066253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7292ea52cfbe3a84e9db161e4d831b0fd3783749a75adff4e5039cac3547f657`  
		Last Modified: Wed, 21 May 2025 23:20:00 GMT  
		Size: 1.2 MB (1196120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc02f09f7f0b5d98d40a318af63b889e87838086e113dc3da7436b75b017b2f1`  
		Last Modified: Wed, 21 May 2025 23:20:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2e06e65f947b884ac83a4c30b817200c30ab6ef6b91433c8ef083fe0865d26`  
		Last Modified: Wed, 21 May 2025 23:20:00 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a469d5dbe26dd01efd4ecb41f1eba2eec210cc542e1fda42e8a2b4edb90fd7`  
		Last Modified: Wed, 21 May 2025 23:20:04 GMT  
		Size: 108.6 MB (108614567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc1fb51259641df16bddea3333e0474e1222543be1627b8cd13ff4de64574ce`  
		Last Modified: Wed, 21 May 2025 23:20:01 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9034eb9489cfb82e8ab476dce38bd78a2e7298cdb0950ea82d0ed54a4829441`  
		Last Modified: Wed, 21 May 2025 23:20:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca18026d8432b1fd83b72240df3def70d3505ef2864facf9e2e9369ef9cdef7`  
		Last Modified: Wed, 21 May 2025 23:20:01 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a800f4731b18ed8f5668467451dc0d69d10f09ad25bb9a805c5acefc0e2e1f76`  
		Last Modified: Wed, 21 May 2025 23:20:02 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c95cd6278f18ce7f11178396d2954536fd6a4ce818130523e1d9c3c0f52f391`  
		Last Modified: Wed, 21 May 2025 23:20:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:19384c214960a8e16a2509cf3bad26b40d3ff920887f86bf6d0686f251529eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5767109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c237476c85eb55e9811b9090064ae8e53b29ada1b1693885a591b4d30278ed3`

```dockerfile
```

-	Layers:
	-	`sha256:c6a4a1da39d959ac3c2170462da0dcbd5ed537c44808b0fd908dfb4f5598034c`  
		Last Modified: Wed, 21 May 2025 23:19:59 GMT  
		Size: 5.7 MB (5713042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10ba710bb046515d423e0f0732e934b91f235f9b4e143a7fbe847ea1ae275695`  
		Last Modified: Wed, 21 May 2025 23:19:59 GMT  
		Size: 54.1 KB (54067 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:e63195cebfbb146ed14e9bae24660f568be07c752c3098898890d3eb2767bfa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.1 MB (145127308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a067f8c351da04cfe5d26c8a105f81ca321e4f7497f1f626903096ed9df1750`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
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
ENV PG_MAJOR=14
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=14.18-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:3bc532ff9d2a2a12c6cfc746359843257a240960865aea7ecb10c71e0b93ec78`  
		Last Modified: Mon, 28 Apr 2025 21:07:56 GMT  
		Size: 25.8 MB (25757836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dbd13a5b1ee87638e8ff020b1d2afd3a00a7bc146f2dd322eff851e885678`  
		Last Modified: Tue, 29 Apr 2025 00:11:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddeed145392a589296f4def151c0cba38caa5ada19685adbdb91ba2a6a6b03f`  
		Last Modified: Tue, 29 Apr 2025 00:11:04 GMT  
		Size: 4.2 MB (4151014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df15ff5474dea0b8a303fcd9ca6d5caf5f5ade1fd5c898351501897de7d9f2`  
		Last Modified: Tue, 29 Apr 2025 00:11:04 GMT  
		Size: 1.4 MB (1423985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12dab1affb15219c1bbe269f8dba51a0b04a4393f6cc5b4ddc6b2dbd7e731e3`  
		Last Modified: Tue, 29 Apr 2025 00:11:05 GMT  
		Size: 8.1 MB (8066459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d53a8d7d21b72bc0336ce7f91d99cb2e76a3f5bb8e50f04848caeffcf3871d`  
		Last Modified: Tue, 29 Apr 2025 00:11:05 GMT  
		Size: 1.2 MB (1194889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550a864e050e101f225d9a0cc2bb1b9064f50226333ad9e131522c36a3921ac4`  
		Last Modified: Tue, 29 Apr 2025 00:11:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862b669ee28183d02dee57a101cd1a31845cfd26fe615ab0a0b969ce916dfc59`  
		Last Modified: Tue, 29 Apr 2025 00:11:06 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfdd9227cccab9e38e8b88df1ef593b3c8d9caf3b13f1661ff2712da1626027`  
		Last Modified: Thu, 08 May 2025 20:20:17 GMT  
		Size: 104.5 MB (104513223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c701590b9de8d84b8e0f314344653b281d0c442cda2fb76b4fc55bb4cfd86fa`  
		Last Modified: Thu, 08 May 2025 20:20:13 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb36cb73ea9407a0a8d43c8964d61151e7d63c1ae98d256193acf7cad4d68ad6`  
		Last Modified: Thu, 08 May 2025 20:20:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a914f3546a1d35f451fc1164b7078814501a18373943755b2023b266098a0fe7`  
		Last Modified: Thu, 08 May 2025 20:20:13 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a39a60ae256303009a0f483195b5567d741c36e6374fb9c246d5d9e0aa5c47`  
		Last Modified: Thu, 08 May 2025 20:20:14 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce57fa09791938fc7932fd9946d2e7293c58202570b5b2a542cb0f4f59b3030a`  
		Last Modified: Thu, 08 May 2025 20:20:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4eec86666c2855476d8b4886b20fdd471a8e3165884fe51ead2c53d5156c3ac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e31f9190e2cdadef6e4f9dca9e1c0dbdc8e5e2917e7b3c1dc66a74f5e61ff39`

```dockerfile
```

-	Layers:
	-	`sha256:4e18ce7496107599f786012aca474bced2c84104a781fe783acdad8f22b025de`  
		Last Modified: Thu, 08 May 2025 20:20:13 GMT  
		Size: 5.7 MB (5698592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9497502ff3e557fe41c52e75a93613b50d55607868431f8a2ff2ae672b648cd8`  
		Last Modified: Thu, 08 May 2025 20:20:13 GMT  
		Size: 54.3 KB (54286 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6cc65d6ab8cb8dac0a96a5ebf5e94b33f1c95e083c7834bf88b5ae70510f0715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140179003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ab959eaef26f99f6feac1e0b04347f92b7721cea1246372da37d0dea173f90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
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
ENV PG_MAJOR=14
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=14.18-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdb4fadcfae6c7f639bb005beb451a5d1442c02240a0d69d7265e913295df68`  
		Last Modified: Tue, 29 Apr 2025 01:02:43 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2efccad23750e2931d3ed57d24f2835f3b9ce8744beaa721d9437163c0cf9c`  
		Last Modified: Tue, 29 Apr 2025 01:02:44 GMT  
		Size: 3.7 MB (3742519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f553df79e41f2f793d4828509d5e5323042ad46cd5cd5b31d6d14f8607643`  
		Last Modified: Tue, 29 Apr 2025 01:02:43 GMT  
		Size: 1.4 MB (1413684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad2964e1fa8d5744b87a0ed825b61807320e0a04d4889bb205fa941886b2e0f`  
		Last Modified: Tue, 29 Apr 2025 01:02:44 GMT  
		Size: 8.1 MB (8066255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f726aa2fe47cabbb56851a90a83ab6a9c48b967d6f4ea88827119d6b3120afb5`  
		Last Modified: Tue, 29 Apr 2025 01:02:44 GMT  
		Size: 1.1 MB (1066999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1938ce7122ffddb675c2743693e8ab090236dc16305e5d6d3c52d4d237fc06`  
		Last Modified: Tue, 29 Apr 2025 01:02:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f217542552436de76d587eaa73b78a8a5618772cbc566ca7272527155b615c2`  
		Last Modified: Tue, 29 Apr 2025 01:02:45 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c532e4d2b221b04a2996b10987c248f54923cbe43cdc3acc9a905093b5e517`  
		Last Modified: Thu, 08 May 2025 21:25:34 GMT  
		Size: 101.9 MB (101931561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6637ebdfc98f990d9af8169362fd42da4372e9b7579306c4ed9b908a6f129454`  
		Last Modified: Thu, 08 May 2025 21:25:31 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686a4b4ac9d75472d0901e85f1ae00b2abeed04541f675898430d73d5f05aa34`  
		Last Modified: Thu, 08 May 2025 21:25:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f0da706c3ab5eb36a1c99cb883d42351d8a2d05bfad294fe9fd65a843e0b44`  
		Last Modified: Thu, 08 May 2025 21:25:31 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace22aae806a9b3d74dca9310c73360bbaaa2360ce0c60bcf8c8bf2b51cd9e1c`  
		Last Modified: Thu, 08 May 2025 21:25:32 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38edbcfa8287ef4a582a7b46f8c9bfcd4e3b3a1b3a3f9e9851e5c8673bd07a8`  
		Last Modified: Thu, 08 May 2025 21:25:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:58d6b81bab8133c431d0e36c9be28ea6610bb8dd3f770058c4cb10bd27befd7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5752449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d85ef75b458d5e7964f74f82146e1fdd7a0e1dfeae5879e34219391f1cf277`

```dockerfile
```

-	Layers:
	-	`sha256:24e42ec2b7bb0f4dc3cc7ee76fa733637dcbdf4ad68f0a5feafffd73d185f943`  
		Last Modified: Thu, 08 May 2025 21:25:31 GMT  
		Size: 5.7 MB (5698163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcc45b6772ef51bfe858cbe2a4d1db1ee3ac618e86efa640904d8d54e96aff07`  
		Last Modified: Thu, 08 May 2025 21:25:30 GMT  
		Size: 54.3 KB (54286 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:8049413f9c29c5968583348f642516b20e098dcb1d9a7e079624da203f6cd013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149953844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90756b5bfbb080a1444b1d1223ebdb8bd4e995856fc3d0167ff8f8335202cba6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 May 2025 17:29:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
ENV PG_MAJOR=14
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=14.18-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00668167bf36b74e0f6c11624f118655568ca9ed89e03656282340d6105546a7`  
		Last Modified: Thu, 22 May 2025 02:07:43 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df734c93257bcefb82049d248f9f565b35da93bd5326b97dd5bad718e728dd70`  
		Last Modified: Thu, 22 May 2025 02:07:43 GMT  
		Size: 4.5 MB (4499149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb10b4d18409169ee1f00b605dbb71580eaecc1220921bbd82b2f89a7721a4f`  
		Last Modified: Thu, 22 May 2025 02:07:43 GMT  
		Size: 1.4 MB (1378807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672b4960c737e5a010841b5f0fe15ef4897fd9eec09efda705c7b7b159fd5a5c`  
		Last Modified: Thu, 22 May 2025 02:07:44 GMT  
		Size: 8.1 MB (8066329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40458a09dd0a7d7fa3ef8e32de5e624123521ea5c02a2cb8a0f4ab400c7c3183`  
		Last Modified: Thu, 22 May 2025 02:07:44 GMT  
		Size: 1.1 MB (1108750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510e0bc6d45584b304d9d017080aa4f405a7e53864f13a710399130c7de6c694`  
		Last Modified: Thu, 22 May 2025 02:07:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98943dfcad1174e1ee263a6d3f57528734bc0f826d3ffbdc57f73586ba0766d9`  
		Last Modified: Thu, 22 May 2025 02:07:44 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42d4b8d7ca844fa629672da6181c437a29a64a84ec63a90c00277bd1a37425a`  
		Last Modified: Thu, 22 May 2025 02:12:37 GMT  
		Size: 106.8 MB (106815635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf9e38339f842514a8dcbe531a8d8b619e1fa4a9e743af63b2918436b65237b`  
		Last Modified: Thu, 22 May 2025 02:12:33 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad8219360bd6672a1dc51bef8112209fe21b83c80ead78a53e657d3666849cb`  
		Last Modified: Thu, 22 May 2025 02:12:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6731ee94a857ac32a52ae5d91671044c4f6217a5b9e3d46e388eb3fa5045ea98`  
		Last Modified: Thu, 22 May 2025 02:12:33 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993cbac4e96ab7579c0a3672ac5cc3fe22205086c3b3cde1b15e3f8e6ea3a192`  
		Last Modified: Thu, 22 May 2025 02:12:34 GMT  
		Size: 5.5 KB (5469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3fc482e8866dba22e9f1f9db02b90c1eedbe155c3e5d68b2883e943a250cc0`  
		Last Modified: Thu, 22 May 2025 02:12:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e2e84f7dc8c8f0af96bb6163d95d1ec5f1640aaae8ff754a29fd961bb8a9d7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45f63d310bd90a6f83cfd8b41859aefbb00290da66b08968401a0abd103e96b`

```dockerfile
```

-	Layers:
	-	`sha256:06d32b0c99b88dd2056c5a0a302897ae9c3825fbd3db616089d41e80714d2eb0`  
		Last Modified: Thu, 22 May 2025 02:12:33 GMT  
		Size: 5.7 MB (5719381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f9cedc7a9ce002a23ee33e7fd6faedefc96003dff9a0a2d0651b78f99097656`  
		Last Modified: Thu, 22 May 2025 02:12:33 GMT  
		Size: 54.3 KB (54336 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:a0046bbcffd9065ce828f85c763c99d04376def3f5044873048d4a455f3bd4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160863601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de62db42c056066705a8df8e615cca4b8da1fa2de2381bfda366d637c484e3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
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
ENV PG_MAJOR=14
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=14.18-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e0d44ed3e07d953d40c887d788e8ceac9720e619261275c6f31f0796359a58`  
		Last Modified: Thu, 08 May 2025 19:26:08 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c2e63d5612cecfa58a1fbb7369de2550926b189333277b50943a5a9317bcfd`  
		Last Modified: Thu, 08 May 2025 19:26:08 GMT  
		Size: 5.0 MB (4965129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f302d9ad290f31138dc054e2c2661390f123b29246c95e809065e07fe8204aad`  
		Last Modified: Thu, 08 May 2025 19:26:08 GMT  
		Size: 1.4 MB (1422224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27481124b2c470412397ee9933508a804a2680fccf18cf0dc2e0894f0088941f`  
		Last Modified: Thu, 08 May 2025 19:26:09 GMT  
		Size: 8.1 MB (8066270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e310435f36c99847e7c713c9eae60f6a237ad1915bc3b1fa3741b2447be7eb9`  
		Last Modified: Thu, 08 May 2025 19:26:09 GMT  
		Size: 1.1 MB (1137211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793e8739f0e609149cea9528088ea55ef9e9282d29d8cc8f97a156dcfe7cc679`  
		Last Modified: Thu, 08 May 2025 19:26:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae9ee9c7a24bc5d57315adfb62213c55ede9a747ce7b489dae4b306d996d7a3`  
		Last Modified: Thu, 08 May 2025 19:26:09 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37154f35156b5a8bfa135e3f25ee28bb82dead3cd356bacb9ed6fd6e2387938`  
		Last Modified: Thu, 08 May 2025 19:26:13 GMT  
		Size: 116.0 MB (116041999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cdf5cedaa04b8322d9b2e57adf09c93d47c50417b6a551cccb55b7c9084c4f`  
		Last Modified: Thu, 08 May 2025 19:26:10 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5c150841fa93b30cc94c15c09be373cae731637984b918564979604fdb5e63`  
		Last Modified: Thu, 08 May 2025 19:26:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b103f6b2146367c10576c278576f4c74f420520096bf6a0349542ad509f515b`  
		Last Modified: Thu, 08 May 2025 19:26:10 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca2a9d271fd67795824f31a6beb0306373ff763a91c8c8bed77f12ca8d0c3ca`  
		Last Modified: Thu, 08 May 2025 19:26:11 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce86c6f568059cfa8885428fadc6ceae9c123ca1f8d5bac1aaaa4fdf1dbc966c`  
		Last Modified: Thu, 08 May 2025 19:26:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7cc53ee22150a011cd984aa7e0c69f2cb9219070a0e04c9ee3a469c6cb780d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5750643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d0eb19a1d5aaf353b51e942c1fa25e825544a690aaddcbfe96296e85ccbc03`

```dockerfile
```

-	Layers:
	-	`sha256:ce33e4e5c114ae8d08ef0c46c2ef35539e3bce5c03c0133cf1b6282c0bfd957d`  
		Last Modified: Thu, 08 May 2025 19:26:08 GMT  
		Size: 5.7 MB (5696630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b79233f8b6dc9fa9d403b69c69c892db265bc56085bd8eb20b89cbf0181e92`  
		Last Modified: Thu, 08 May 2025 19:26:08 GMT  
		Size: 54.0 KB (54013 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:082f0a6f9d8782cb1c0de055721a9c7b068cfb616bd62189ce860bfeab398bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150924131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd868633205bfa45b8e5b556f14f7e7abedc5224e571cd8cfef0136a31c6448`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
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
ENV PG_MAJOR=14
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=14.18-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:901060d913f9d0bbb82847b3b60c3a263ed0dac4f75aa29161be6ed89b57082a`  
		Last Modified: Mon, 28 Apr 2025 21:11:19 GMT  
		Size: 28.5 MB (28514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1780050ae792096e0edff3e578099a41e20ce2a23d7434a31a78a13d2b3f501`  
		Last Modified: Tue, 29 Apr 2025 07:45:04 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32022b8dd15ee12863120304ba80701697a0232a841395c6c8d557a11d14223c`  
		Last Modified: Tue, 29 Apr 2025 07:45:05 GMT  
		Size: 4.5 MB (4475158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd295a92609a051f01f5fbadc21ae67c51b1a7e1c423aa13548bb0c3468c722`  
		Last Modified: Tue, 29 Apr 2025 07:45:04 GMT  
		Size: 1.3 MB (1333883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49953f908cacf70551b7bf4187ae9e8b441d92da15103e34ff0b6273a4aaf3ad`  
		Last Modified: Tue, 29 Apr 2025 07:45:05 GMT  
		Size: 8.1 MB (8066514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dad47142b6c9f9cc6e05f01b141c6d270db331bbd00cd1fbd60ae6448fb7cd`  
		Last Modified: Tue, 29 Apr 2025 07:45:05 GMT  
		Size: 1.2 MB (1182704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c74555c4f1f057ae22d7b6c625eda50a7ac21f4a81590748a81cdbb475cfa6`  
		Last Modified: Tue, 29 Apr 2025 07:45:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711e5b1cdae35c1754e7e9e2a5b0567db79bc132e5d66531c8c6c170f8025a1c`  
		Last Modified: Tue, 29 Apr 2025 07:45:06 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdc123d59030d4cda084f0dd5a28c2cce6885b213947f70733faa0f13e16037`  
		Last Modified: Thu, 08 May 2025 23:50:05 GMT  
		Size: 107.3 MB (107331822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e6f5bf7bd7262b098d86b090f985c2c516075c56aa3dda6a350d6c78ad9f61`  
		Last Modified: Thu, 08 May 2025 23:49:55 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6014f50d5fff73b9dda1702306cd62b5e5f5d44de47f621fc0a0f887cd48d0`  
		Last Modified: Thu, 08 May 2025 23:49:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f62c509004c242015a3a4eef37614afaf5d6c4e3c68ca0d9559411385278695`  
		Last Modified: Thu, 08 May 2025 23:49:55 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a3613af8a160101ad2cde9b87be727f9f1611d17a75b056093187413ba8e42`  
		Last Modified: Thu, 08 May 2025 23:49:57 GMT  
		Size: 5.5 KB (5472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f5e7d5094e1542ce1db71f8e7bda5f0aa77ead55ee979dc96b153b50450167`  
		Last Modified: Thu, 08 May 2025 23:49:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a00be324dd9e4e0783b8a5d4c7b0b5ee299e4e921cb54efad240abc52d0655a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 KB (53950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea54eabb2ae07425110419bf84e08c58585624030af816202f83a88552e2e82`

```dockerfile
```

-	Layers:
	-	`sha256:8de127e0bd273ebac95c9d540108cb0e4861e75b0f9111dad597c303bc6aa126`  
		Last Modified: Thu, 08 May 2025 23:49:55 GMT  
		Size: 54.0 KB (53950 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:4a20f91dbc1f69cd1531cb86fe6e3bfe0888e767d7e4396963ddb6b88f758096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164727092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc764acfff2a29b0cac496e1fd2def46ad680c463192b2768eac77aa630de01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
ENV PG_MAJOR=14
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=14.18-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e15de81941f7c44df819c05a92dc3ec9aabc58baa62bded8abe1faf2916460`  
		Last Modified: Thu, 08 May 2025 19:22:56 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831c9b47c6852f124cf8c14a2f8a90536781879bb40f7108d6be378c04439c52`  
		Last Modified: Thu, 08 May 2025 19:22:57 GMT  
		Size: 5.4 MB (5368200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb6f6a9ebbed3ee6875f5af99d1f6bc1fdeee373801d13c7a50d415bd1f1a48`  
		Last Modified: Thu, 08 May 2025 19:22:56 GMT  
		Size: 1.4 MB (1368742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306e8eca4ddb2df576851f376c80ce1ce94b75b89f6fd608124bb306776e69a5`  
		Last Modified: Thu, 08 May 2025 19:22:57 GMT  
		Size: 8.1 MB (8066383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ca4cb2832001ccf883e85e97e2bcf83c3272a4d94cf409df3556ef8855e058`  
		Last Modified: Thu, 08 May 2025 19:22:58 GMT  
		Size: 1.3 MB (1283565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c373ad9662e17bdbdf2dc7adbe50b25562851f13f39b21f16cacf5cd98352de`  
		Last Modified: Thu, 08 May 2025 19:22:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c75d83d7375487e857f5bf7fd3a5a7bbc0eddf8e5e6d0b905edbc9edca336ef`  
		Last Modified: Thu, 08 May 2025 19:22:58 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67ca71302166c18b08d77d39a207e0e9981b458f19cb6e426baaa73c34a50a0`  
		Last Modified: Thu, 08 May 2025 19:50:03 GMT  
		Size: 116.6 MB (116551849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca408c6d6bbcf3c3bc3a35d0b2591bdb825c5ae14100a51762e94ba43a779a`  
		Last Modified: Thu, 08 May 2025 19:49:58 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688bd26b83feec0c28d0818e3b8fc225e056cb4ea46c3ade2d860fad7bfcbe69`  
		Last Modified: Thu, 08 May 2025 19:49:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd566ae8cbc60509413457a7e44bcc1d9e35a1150ad6eaaa1e1490c8ba73168`  
		Last Modified: Thu, 08 May 2025 19:49:59 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b830e7f74f427c0793c5a782a9d1341eba56d55942df1e5f21cc7f9c5652e5b6`  
		Last Modified: Thu, 08 May 2025 19:49:59 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6696d33b42f5530836677f6faa98ebad671ef7eda24cd7073224a7cf71c9a5`  
		Last Modified: Thu, 08 May 2025 19:49:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:528b7d89e6989a7efed53818cf2a77855541096694ebae8271c77c5277f4f03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5746537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecf95a24483b1ad6529ebb8ca78ae2be68fb930bee124e482d3226fb3573c4b`

```dockerfile
```

-	Layers:
	-	`sha256:d6e174ced0d0883aca21ff4d9900221daa4fb6d1c8bf5beb33af9926fb975505`  
		Last Modified: Thu, 08 May 2025 19:49:59 GMT  
		Size: 5.7 MB (5692404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a287ba60f664ccc3315febc67a7f3f594f1deaacc50d2fec75cde51b504894b0`  
		Last Modified: Thu, 08 May 2025 19:49:58 GMT  
		Size: 54.1 KB (54133 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:faaaa39a4cd32f5738e3030bdc87ad49b39a92b04552051b80177d82bf674bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161286391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2f2d20969b2f31ea9736efcd5507d5eb77e3e59ca4c8d0409935f6f43cf429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
ENV PG_MAJOR=14
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=14.18-1.pgdg120+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c248ffe4f21880229522e5ad5c2703976299295d6d894d9490806c0a9a7cf45`  
		Last Modified: Thu, 08 May 2025 19:35:31 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d13e825e9d3e1c8a8132b839b8821c6e5285374a88d601e7a517f251d6c8340`  
		Last Modified: Thu, 08 May 2025 19:35:31 GMT  
		Size: 4.4 MB (4391042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc1e3a56b5833a71fd825838551fb859ecd3993d606c3b62f4d5192775fc04b`  
		Last Modified: Thu, 08 May 2025 19:35:31 GMT  
		Size: 1.4 MB (1412760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a09d1da4e34e97c0c0a8a2337068aff2abbbdac1aa0064fd21bf59b0cb6cb8b`  
		Last Modified: Thu, 08 May 2025 19:35:31 GMT  
		Size: 8.1 MB (8120466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87203bb8ab9f6fd5568bcbd8fc845cfcdca543aab24cb4997ddd11e94d6021c`  
		Last Modified: Thu, 08 May 2025 19:35:32 GMT  
		Size: 1.1 MB (1096776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99bd7b2c30d8fcbd66d1b84412c41c4f63f4aeb1feec906ab0664d8586ad987`  
		Last Modified: Thu, 08 May 2025 19:35:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a07b08d12e1952495315aa4a0d7d5b3aa116f8e46a58d4a7085fca855945183`  
		Last Modified: Thu, 08 May 2025 19:35:32 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad6a77b04d1ed92da9e55a49eba269195709fe6545c61a2b316bd3115dbdc8a`  
		Last Modified: Thu, 08 May 2025 20:42:47 GMT  
		Size: 119.4 MB (119360569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0cbeeb100f6a99f45a10e8c927fb410034ead0a5302326743dabc07dd98ab2`  
		Last Modified: Thu, 08 May 2025 20:42:45 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53320f3eda2ee64042777bbe60648e6eff3880565e3a9fc65e9ffa58cb9e2c0b`  
		Last Modified: Thu, 08 May 2025 20:42:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18b8904db71049f7f553fe847644cc02d9c50d894fd015543af7827d09622ba`  
		Last Modified: Thu, 08 May 2025 20:42:45 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e46aa5673f6f484fad3834efe972026e121c8d4300d14e36b3cca257360b2df`  
		Last Modified: Thu, 08 May 2025 20:42:46 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a3e748506ba70f97055fae0398a69e9db8a5d4d132a389208186fb3340a764`  
		Last Modified: Thu, 08 May 2025 20:42:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b1f6fccd2b8cfafd6a7c50e391a0dff596ba1899a232e09ba00ce56d1f6a597b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5750453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4659b98d2ba0078325bf96c10e69c8fba85402468c1e3aeb85f021eedb9133a5`

```dockerfile
```

-	Layers:
	-	`sha256:fd3daaaa33e22bf6bedb22150dafad45463ef12e4a3fb6f6d5dcdf07d6a6d379`  
		Last Modified: Thu, 08 May 2025 20:42:45 GMT  
		Size: 5.7 MB (5696387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f5173f1e05f46548f0a14d88053478afb564d664a384cc52af84a072059acf5`  
		Last Modified: Thu, 08 May 2025 20:42:45 GMT  
		Size: 54.1 KB (54066 bytes)  
		MIME: application/vnd.in-toto+json
