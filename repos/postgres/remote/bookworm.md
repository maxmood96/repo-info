## `postgres:bookworm`

```console
$ docker pull postgres@sha256:6efd0df010dc3cb40d5e33e3ef84acecc5e73161bd3df06029ee8698e5e12c60
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
$ docker pull postgres@sha256:864779115ab663ff8da5f027bf28aaab83fe377298d537e2886164b4bb1f0595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156293493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb32a7ac3a99e06ee5b81950278662ff78ea518a9fb18866bb8a02a215b78d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=17
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db9b37be7c36d0a67b2a88d496500701f1c7ed2389a5226ca36593c6ffd2fd1`  
		Last Modified: Thu, 22 May 2025 16:52:50 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a82aed48d77b180f52dac43cef566607da8d1eaf3d918a5248fb24d5398486`  
		Last Modified: Thu, 22 May 2025 16:52:52 GMT  
		Size: 4.5 MB (4533787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c852ebdd63e7e75ae5e7720ede1c212eda9ebb1349ff7e5439fdd2471e5be40`  
		Last Modified: Thu, 22 May 2025 16:52:52 GMT  
		Size: 1.4 MB (1446777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28708ff4e046012a0916f7bfc667a3589b4d445fc667b7b22bebf6b34808bb6c`  
		Last Modified: Thu, 22 May 2025 16:52:52 GMT  
		Size: 8.1 MB (8066283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce13d85dabede2a4d2f4a2c54ab4204e5e8f2b198fb4911c5675a74b267e055`  
		Last Modified: Thu, 22 May 2025 16:52:52 GMT  
		Size: 1.2 MB (1196138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1fa28722bb672d096f90a95e8ecf3253513654eb20fbbe4ed140a82e345ad1`  
		Last Modified: Thu, 22 May 2025 16:52:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410cd7ec9a40c90d2bb470c78da3f74cd4e5a6830bc26173ef4f1bfeab83ff52`  
		Last Modified: Thu, 22 May 2025 16:52:52 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475b0e32b8145d3b5a14b626a4d1f31d45048ee7f9dec8fb7333fb856618ce56`  
		Last Modified: Thu, 22 May 2025 16:52:56 GMT  
		Size: 112.8 MB (112804565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7aba16d6a5ee1e1529b515bf0fb83f31311daa2889e17926d38c513f7b26366`  
		Last Modified: Thu, 22 May 2025 16:52:53 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ba8b615fa9edc5a8e4d0234261443fe3a7fec398250992cf1abc05cdf442c6`  
		Last Modified: Thu, 22 May 2025 16:52:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82697a7976dfb48a3d296f9bf4d8c9f88047b58495203b406b777103187ed662`  
		Last Modified: Thu, 22 May 2025 16:52:53 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e11eb1421f32d4bd79d9e501e4546f637412daf9611070348457a53231e59d6`  
		Last Modified: Thu, 22 May 2025 16:52:54 GMT  
		Size: 5.5 KB (5472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb588ce4e678f8da3e3d0a329ceda89e3b53d5ee68aac45277262536f012eb6`  
		Last Modified: Thu, 22 May 2025 16:52:54 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e3d052b9cee406ce76da931a1924f180ad4687dbd5258fbf0a8891aa7e514a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5901084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104106aac6289fe87c88aa745536a7a6e8762e3f8358e36ff4fa33cd425dc74a`

```dockerfile
```

-	Layers:
	-	`sha256:88c94a21b573a5ad8e13a427c780c8e014483dc6d94daad723a07b9ba41c20b7`  
		Last Modified: Thu, 22 May 2025 16:52:52 GMT  
		Size: 5.8 MB (5846541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f111c3c9099fe6a6a9f4fc64d21459d148f5b3237a89f8d17766223cf4ddb00c`  
		Last Modified: Thu, 22 May 2025 16:52:52 GMT  
		Size: 54.5 KB (54543 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:6df23fc09182915578dc73d5f97ed959d125d753116e0c78e0058bb0f3019318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149368636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b7ee6f621a5307566f98567294e99efbc2b5c1a2090e58eab3b5295e6abb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=17
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62d114b6ab0f6245abc5fc53268a3d50ffaed32de00ff91342f543afd0c6d71`  
		Last Modified: Thu, 22 May 2025 17:21:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7c131fcec3d91e9d4ffe06025b742923f6475d89bcfda493a0e3add1b8b7bf`  
		Last Modified: Thu, 22 May 2025 17:21:07 GMT  
		Size: 4.2 MB (4151047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b008c95d3b236b4c39b53e44ebac39f98349ed5799040971df3dd4bb1af9c9`  
		Last Modified: Thu, 22 May 2025 17:21:07 GMT  
		Size: 1.4 MB (1424010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5015d0a089bbb0bcabe77c0ff92f93e3de8d6fc84b603a493104b104b643dc9`  
		Last Modified: Thu, 22 May 2025 17:21:07 GMT  
		Size: 8.1 MB (8066419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c879f0787c314eaee95f2964fb61b12f65ccf25089e46a477f69e6cad94952ee`  
		Last Modified: Thu, 22 May 2025 17:21:07 GMT  
		Size: 1.2 MB (1194910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b45a1f3bc946839e6bd4cbcc3a1085b3f4a5c0d7dd8c215debd0083c9eb88b`  
		Last Modified: Thu, 22 May 2025 17:21:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede282d96d1d58258aeb0085d6b42a94df3fc819bc3ca5d5207a3f09265dfa08`  
		Last Modified: Thu, 22 May 2025 17:21:08 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5b300193d0bf85200b7eec97e4574e6c76676c0283da58b5d4cdbb97c56d87`  
		Last Modified: Thu, 22 May 2025 17:21:11 GMT  
		Size: 108.8 MB (108754736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e880841682e1f0a863121f0ce22a90b9835a37b4b362a3a73154fb1c41bf75a5`  
		Last Modified: Thu, 22 May 2025 17:21:08 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015606cfc803d72f941430512ce594797a527f8df182fc8dfb5f3ad254049695`  
		Last Modified: Thu, 22 May 2025 17:21:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f03c7f84945ad23ecfcf5224a8fe39e473749780711e41e09c36d8f050d53d`  
		Last Modified: Thu, 22 May 2025 17:21:09 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc4004e5a049c889e21d9d4bfcd3a77ebff7b263ec22665db1d2a52f2eec21d`  
		Last Modified: Thu, 22 May 2025 17:21:09 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06f8197ebcc4ea9c5fcb67e92d1f956205ab8afc961ce661c58040806b74613`  
		Last Modified: Thu, 22 May 2025 17:21:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:795853123707d436ef3eed707167119e2e1effd9cb94218bdbbb970019f1e5ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5919475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124c1d1b20bc388a6aaac7a7608d12df642a50488b625877124642a0221e6500`

```dockerfile
```

-	Layers:
	-	`sha256:1a3104114ed7d99e140910d33a63b497411e6f8bb3b5e803f18a47e48a711a5f`  
		Last Modified: Thu, 22 May 2025 17:21:07 GMT  
		Size: 5.9 MB (5864699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e3c1ef336ecbf79c99e008bcbf8f0f6eb892f116b894a25658912a063a2697`  
		Last Modified: Thu, 22 May 2025 17:21:06 GMT  
		Size: 54.8 KB (54776 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:c9703d887d9ea897dd1e1ff1c609b67540931c1ea9d95140114c58e59b897f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144336991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83ce3fab88c97ec01a748a4604f171006d0458b307f43c921c45e33278fa4cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=17
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5e367c41b6be274a9277e95d0e5092ff057faf31509faa631b99e9b4424ba8`  
		Last Modified: Fri, 23 May 2025 05:46:43 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcffd0d6d1eb43b4cef0ccfb9874fe4ed595e2335d72cfad36fe43e7d3762e7c`  
		Last Modified: Fri, 23 May 2025 05:46:43 GMT  
		Size: 3.7 MB (3742558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bdc150075156016172121c6f9e432edd4d2f4da93fa55a77aad454d2c7f500`  
		Last Modified: Fri, 23 May 2025 05:46:43 GMT  
		Size: 1.4 MB (1413720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc73a57c452af6f3bf6f9bdb9f92078f792b67c9c210fa3fe373aad4d11b1f9a`  
		Last Modified: Fri, 23 May 2025 05:46:43 GMT  
		Size: 8.1 MB (8066266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8441757d12f0d744d2de7e3961ecaabed4a58f797971d86ed1d196a0e9d53c`  
		Last Modified: Fri, 23 May 2025 05:46:44 GMT  
		Size: 1.1 MB (1067024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bceb063b3564bc90c57ebf81d08da3e8756b25a1b8ac71a08dd350bb14b99b1`  
		Last Modified: Fri, 23 May 2025 05:46:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73404b3497d6fe561a2cd2d3ac62f70312091540a74b4f2b58778b7f742e4ef`  
		Last Modified: Fri, 23 May 2025 05:46:44 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15332adc571ca988c0f3cff5d8a7b174d3253aa66de849aeebe29af13f26b67`  
		Last Modified: Fri, 23 May 2025 05:46:47 GMT  
		Size: 106.1 MB (106093889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803323e97c518e194a99e26d924107eef2a9e31b9179f32f73b7cd2de8ef413f`  
		Last Modified: Fri, 23 May 2025 05:46:45 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dcc9c69e91c73f090546ae4b3c73c6003e6c466f242f854231f1b7e91b6cee`  
		Last Modified: Fri, 23 May 2025 05:46:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bf173040eb2dd1e743b24cf38e4dfb60cca7316796693f46ac041f7d68f1fc`  
		Last Modified: Fri, 23 May 2025 05:46:45 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa33af76dc4af5420c84f9534696a279c4e2e88fc74544762d4229ce0ba2923`  
		Last Modified: Fri, 23 May 2025 05:46:46 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040f2f9d5760dbe012235ab708fdbd3dd28a88cef5ce279aae335d28bc23764b`  
		Last Modified: Fri, 23 May 2025 05:46:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ebd2ef51059e7d82e806aefe096ff494042eff4f47985bae8a6b846741929920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5918740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7286d2ed8eed6ae73e28e9d8f7f71682831a34aaae94fdce3ac7c0bd659b21ee`

```dockerfile
```

-	Layers:
	-	`sha256:c99755e9dc3da0c70313ce6e90fb3d62df9f897c612fec54434fcdcd81eec339`  
		Last Modified: Fri, 23 May 2025 05:46:43 GMT  
		Size: 5.9 MB (5863962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4ee034138ef7639cafa9771a6915b5375cb2a23c24a6ad67cd88cac922bd046`  
		Last Modified: Fri, 23 May 2025 05:46:43 GMT  
		Size: 54.8 KB (54778 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d8407282030e2800d1959d31199dc6232803c6b8a77b628eccbb334d17f7ad9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154144802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b18d7589355c4cc7cf7cb3d9dd201516c0c7a4d4dfe70a539d7658f4eaf1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=17
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
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
	-	`sha256:23147b95458c10b6f323146e57f58ee48564761431a0b3af2415edce022e7f0f`  
		Last Modified: Thu, 22 May 2025 20:05:18 GMT  
		Size: 111.0 MB (111005882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145a1e4200cb00a03de0cc6b330194f3a3b9004e178df890936423942a0dd4d7`  
		Last Modified: Thu, 22 May 2025 20:05:15 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d93319524947041b37e706405dc33badbb0aa67b3ac5126c37e687728a701a`  
		Last Modified: Thu, 22 May 2025 20:05:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb548e3d4837a51ba2b21459bd864a323921e5b7f2d63617fa735f07c91b3603`  
		Last Modified: Thu, 22 May 2025 20:05:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693d2f517b7395ec35b22f7eb331c7b75e37d3f700d944b10702971b34495c93`  
		Last Modified: Thu, 22 May 2025 20:05:16 GMT  
		Size: 5.5 KB (5470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375094ec64742d51c36830f2e157b7b97bde2a318421d6bb0c65c835a37b7cc5`  
		Last Modified: Thu, 22 May 2025 20:05:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:60b84d66c27c4a07c2eda055f75bc29d596ea0781dae15cd2b567b4da849fd29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5907740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d01f89dd0470b6ef65d217f99ea204064957566bb288bdb7c9145fe3ee2e2c`

```dockerfile
```

-	Layers:
	-	`sha256:aedb567392a9aabce18d5028c4d9609723b24effebdad6d08a60e8968f2b7ca2`  
		Last Modified: Thu, 22 May 2025 20:05:15 GMT  
		Size: 5.9 MB (5852904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d0308b90d6bf65ae878ae3c6d9e35d1f0a14c4c826aef7405649f0c668b70f`  
		Last Modified: Thu, 22 May 2025 20:05:15 GMT  
		Size: 54.8 KB (54836 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; 386

```console
$ docker pull postgres@sha256:e2f42557892eb9156499f5e0b48cd9c59e869ca91f0cb9015948f6904c59cc9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165208486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768811b5b8ea86342b1284f26f31e2fa2fe87555d0ea05bca218f489adf2f33d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=17
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db9b37be7c36d0a67b2a88d496500701f1c7ed2389a5226ca36593c6ffd2fd1`  
		Last Modified: Thu, 22 May 2025 16:52:50 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fc2d5ebff44e871a625ad13bcfaeb749ee6a2bb19382e714b8045514655372`  
		Last Modified: Thu, 22 May 2025 17:06:27 GMT  
		Size: 5.0 MB (4965089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f2e22b34f2124c333443830ce6c88a9e8fd19ae401c2fe5404f7c2a1adb63a`  
		Last Modified: Thu, 22 May 2025 17:06:27 GMT  
		Size: 1.4 MB (1422230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb822f56d9b1483c06981a947a40dc496811e7e8cc7ad76fcfdd1036033069c`  
		Last Modified: Thu, 22 May 2025 17:06:27 GMT  
		Size: 8.1 MB (8066278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f093e16164ecf36860961935375f4e86625333b9cfe959816b30b85b09c895`  
		Last Modified: Thu, 22 May 2025 17:06:27 GMT  
		Size: 1.1 MB (1137216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34799c93bdbcf00dd84fa14a56b2396b4a47514bec80f8a71e4109a2d1f448fc`  
		Last Modified: Thu, 22 May 2025 17:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c69919213dcca5bcf5cf1274c7a961845de08d9df93c8e7c0ef3eab94d23cb3`  
		Last Modified: Thu, 22 May 2025 17:05:38 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d20e911ebf2b1526e1092a562ad53373f67a4316233c29964d1a70df28ddd0`  
		Last Modified: Thu, 22 May 2025 17:06:31 GMT  
		Size: 120.4 MB (120389568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69abd77c5d71d36d73ddf88668111db69baf9551ffcf28ae48be3b46d9ba11e5`  
		Last Modified: Thu, 22 May 2025 17:06:28 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a7d17810331cc3e05441b2f4760cf3fb18cbaea2497d1556d9c5c9dd14fc50`  
		Last Modified: Thu, 22 May 2025 17:06:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d2b01ccf88aa2ae19e696a8f5e8fd9624b176a34cfad6b3d150dc2feafac21`  
		Last Modified: Thu, 22 May 2025 17:06:28 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d11025783bb9567c8563e1cf994d062fa09114c59c4e0c64634ec8234209ce`  
		Last Modified: Thu, 22 May 2025 17:06:29 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0bc161253f23a025af2ef62767ba66ab5146c0711d60e851c6c13f08f15a0c`  
		Last Modified: Thu, 22 May 2025 17:06:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:751731eea4ca2329e09a8bb91d160e29aea7daa27d67127b7c6570799fa83e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5917257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20eced53f5f0db8597b5cd6192a5a6fda687866cb074058efad47388c1c20e20`

```dockerfile
```

-	Layers:
	-	`sha256:cccaf1bb5b76c7b61adb69df7e57fb68172bed4e427a81fca3d87e826f3c5a2f`  
		Last Modified: Thu, 22 May 2025 17:06:27 GMT  
		Size: 5.9 MB (5862778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790b270f1f7f541945687637a92478d4caa2cec1862f4eced2f6b67dc76d20d5`  
		Last Modified: Thu, 22 May 2025 17:06:27 GMT  
		Size: 54.5 KB (54479 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:7e2db96970b40b088e294083580cb5b542a535106dd44f520746af906cff2101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155178729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1571e8d9a4a2c8f934d76e28b111fb0c764d1d1e69bb86272b575b367226abda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=17
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b3bba4720802454008a3814b373e46348369ab53074de47b2a63fc1ede54e3`  
		Last Modified: Fri, 23 May 2025 00:01:05 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f588128e12a3c5557bfebfcf755662572ae0a93f09e6a36240f77340d7cb36`  
		Last Modified: Fri, 23 May 2025 00:01:05 GMT  
		Size: 4.5 MB (4475122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6659f629863412de826e8ca7501c370ae1bc55390b607abe85745c86442e80c5`  
		Last Modified: Fri, 23 May 2025 00:01:05 GMT  
		Size: 1.3 MB (1333877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b50268560830d03de8b845dd179eec793f44bd6f1acacfc244c862277d1e67`  
		Last Modified: Fri, 23 May 2025 00:01:06 GMT  
		Size: 8.1 MB (8066550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0875b09156e66c1bd038d6a3657dd901801b3ca3df0b38a9e430b036eebbcb8`  
		Last Modified: Fri, 23 May 2025 00:01:06 GMT  
		Size: 1.2 MB (1182671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c42fd104633f6c44d40af4a8f59284fadc326286efc0fc99c9575bbe1ee3ce`  
		Last Modified: Fri, 23 May 2025 00:01:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0f952df49c715189ff4560a8606e243143be090bcab84a6a9bdd2b3ef2cff7`  
		Last Modified: Fri, 23 May 2025 00:01:07 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de98afd46de942c20a3bea18aa4cf311c3f4e02b4fe7f732e55955b2bbba084d`  
		Last Modified: Fri, 23 May 2025 00:01:17 GMT  
		Size: 111.6 MB (111588036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe665d86d9ea384d575a0448f447cd21386c7f43bd8ecd28e6bd32b195ad8e93`  
		Last Modified: Fri, 23 May 2025 00:01:08 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22049c1342c32e67e2a6780ac6ab4ff9c4e76bb81379a51b03afc18d9b8ccc6b`  
		Last Modified: Fri, 23 May 2025 00:01:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6688b9b1e895f18566b67dff6ec44eaab4fbcf2141d275ae57c2f424d7b0f5e9`  
		Last Modified: Fri, 23 May 2025 00:01:08 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba3559088b1631b471d53f0329fe49ffaa8ccac4041b89b2d9e4f6783c3e47c`  
		Last Modified: Fri, 23 May 2025 00:01:09 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd3eff0655f297f5f6fbdb769235ad3370dfdbdc0e1484fdadaca10526a3da5`  
		Last Modified: Fri, 23 May 2025 00:01:09 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:97fa29421efa0fc6fc7cbb07be151974b80f4dceacf65fa34357dc9f25ebe9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.4 KB (54445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c86ef6c3d1ef0c5037d00a34dcf714b7768fc7fd22b4183e1af450597b26d4`

```dockerfile
```

-	Layers:
	-	`sha256:9d05f4e8bcc65bd0c90d7b1109379e6ab2d379963ae1e4761afdee7f6523ad10`  
		Last Modified: Fri, 23 May 2025 00:01:05 GMT  
		Size: 54.4 KB (54445 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:184c7cb920bf9d5e0b7d1d178eb236417418a31fbd6c69b79aaf697497157ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169070335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661c6d7ac8ce06f8fd8a5548976d7f9fc0a5a41c85fa72ab78e156c3c201224a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=17
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0be5e9023ac5dd8770972b8cc2f8bf6b3f54a6f24ef4c42ccd3379f5701453`  
		Last Modified: Thu, 22 May 2025 06:58:43 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13f2b0e61d86df3d9dda3a718b074a8a6592871de647e139d627e9756cc9427`  
		Last Modified: Thu, 22 May 2025 06:58:44 GMT  
		Size: 5.4 MB (5368243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409e68602475a6447e3ad1f7f821fa6b262ca0dbd837a106969c0d9f76eb77e0`  
		Last Modified: Thu, 22 May 2025 06:58:44 GMT  
		Size: 1.4 MB (1368746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fc3db6662470e96eba359359d4f27928363cf86caf3960b62aa2cc3098e0fe`  
		Last Modified: Thu, 22 May 2025 06:58:44 GMT  
		Size: 8.1 MB (8066383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9115a328a15e9cbd4f38f65559e00ec18fd815b91c73c70cb444b89745689199`  
		Last Modified: Thu, 22 May 2025 06:58:45 GMT  
		Size: 1.3 MB (1283530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6646fe061b0084825b6a89a9425b906fe61f89ee16fe330046141d9d096d0ec`  
		Last Modified: Thu, 22 May 2025 06:58:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad459b8f4961ae01c0d4633b31cca255551e8c88c2df4dbfbe2180efc0f1c135`  
		Last Modified: Thu, 22 May 2025 06:58:45 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323f4b15db9dbe691c51d083795742e252d975e50989b1d3eea929e19ef6b9e2`  
		Last Modified: Thu, 22 May 2025 17:29:24 GMT  
		Size: 120.9 MB (120895902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dbd77594b33084ea4ee76a8d2fad00c5a5ed86adff70cc35d46e098c0314d4`  
		Last Modified: Thu, 22 May 2025 17:29:21 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c35e81ff18d0f0cae3bf26a0fbcc1f31621172eee84a059ddc51809f20a0f76`  
		Last Modified: Thu, 22 May 2025 17:29:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f961434d36d2144d8615ae53b88bde3e386ddb489d4a35fc6b25a39429027ad`  
		Last Modified: Thu, 22 May 2025 17:29:21 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814dfd2a893198ee5a9a3716e7a2a3d6a46d528699ece845a963027e091a281`  
		Last Modified: Thu, 22 May 2025 17:29:22 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466c4456f1c58e4bfc0cf073db3b18a8db6ae304c3ceaa26fe3addec4f608db6`  
		Last Modified: Thu, 22 May 2025 17:29:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d42b1a357008aeb2f878a64f0bcc76bb5c5e402cbc9113d960c4bcdf94e85895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105550c3ddbada5aba628d034936de5ee3eac0015df0ac446eee82d91ca6f6d9`

```dockerfile
```

-	Layers:
	-	`sha256:9511748478e8f096e34533a2d7d0c8f70b7c46182d87f737ff95347d7f1b6633`  
		Last Modified: Thu, 22 May 2025 17:29:21 GMT  
		Size: 5.9 MB (5853946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a3f55062158d2be54a731c680525f89206212c5ad22937eb12011cf30114ffd`  
		Last Modified: Thu, 22 May 2025 17:29:21 GMT  
		Size: 54.6 KB (54621 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:b27ff762bdf4991a2dbe5e1ac95ccf3cfab59802536120cf2a564e1666a2c0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165583219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f6620a3a86aa2a2a0825bc4af795ebc99260512d152bedeaabafd2988becd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV LANG=en_US.utf8
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_MAJOR=17
# Thu, 22 May 2025 00:48:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 22 May 2025 00:48:07 GMT
ENV PG_VERSION=17.5-1.pgdg120+1
# Thu, 22 May 2025 00:48:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 May 2025 00:48:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 22 May 2025 00:48:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 May 2025 00:48:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 22 May 2025 00:48:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 22 May 2025 00:48:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 00:48:07 GMT
STOPSIGNAL SIGINT
# Thu, 22 May 2025 00:48:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 22 May 2025 00:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2957444059b5f1a79daa28f1dd6e7e5536e324a60183d9673c285866ec1dbd7`  
		Last Modified: Thu, 22 May 2025 17:45:42 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f4c6b0207622f99222fa8dd1cf2104e4275db4e9d1d68de82c2002fdc5c5cd`  
		Last Modified: Thu, 22 May 2025 17:45:42 GMT  
		Size: 4.4 MB (4391071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7369ca142c1a1029c984eac8f3f99d588eebedce4018663ff9941fd613a9f08`  
		Last Modified: Thu, 22 May 2025 17:45:42 GMT  
		Size: 1.4 MB (1412762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2868fe3680365e00bee3adbf2e15927580f5b8a27ff51cc2e5e8473fd62067d2`  
		Last Modified: Thu, 22 May 2025 17:45:43 GMT  
		Size: 8.1 MB (8120435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ffbdab974f00148369acf237aa730b064b9c215fdef16a5db1423c642f4225`  
		Last Modified: Thu, 22 May 2025 17:45:43 GMT  
		Size: 1.1 MB (1096765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83beeccc44047356b4226a6a9ccdae413c15cd7ae8483d8f8d82ad0c1525579`  
		Last Modified: Thu, 22 May 2025 17:45:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96c632e3f718a4c131fc35c76e2feca657623963dc362cd992ef484d5e1dc17`  
		Last Modified: Thu, 22 May 2025 17:45:43 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c874fea40f7b577de7c3723ef62284535ee87555c63a5ac49ab46faf3f796ee2`  
		Last Modified: Thu, 22 May 2025 17:45:46 GMT  
		Size: 123.7 MB (123658761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3a75789f9a06d58d847bb05e438ac7a7057c473fdfaabe7a468537f74a425f`  
		Last Modified: Thu, 22 May 2025 17:45:44 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227e0ec61def7da81f6cb574854f7e69d60428d429deaf851689857aeee63213`  
		Last Modified: Thu, 22 May 2025 17:45:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b78ee17e81609c111e6cb4a903aa924c19b27a005b148fd13bb3f290de5798`  
		Last Modified: Thu, 22 May 2025 17:45:44 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a874dbe51c7fcb2f515985f2a89f7d72991d0d2b893d76074708ce8f494137d`  
		Last Modified: Thu, 22 May 2025 17:45:45 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68ca49651fb09147a75d981a94a496b2187d6d1e7c3d0878b268c877541b0f`  
		Last Modified: Thu, 22 May 2025 17:45:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d981a670b8471d61968ea803300a5f5cad6590ffc474d4d99aa5ba1016076e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5916713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3905daceff3a943acaa241e4f0065ef5775ea220a738fb85a06ef684740d053`

```dockerfile
```

-	Layers:
	-	`sha256:616fdcb34b1904c47fd35eb2601ed1518b2db88035e68cafd3fd064689d84498`  
		Last Modified: Thu, 22 May 2025 17:45:42 GMT  
		Size: 5.9 MB (5862170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2096cd9bffb961cb52f832f99b0b4420366893cfc76f3f38854280a26feab4e`  
		Last Modified: Thu, 22 May 2025 17:45:42 GMT  
		Size: 54.5 KB (54543 bytes)  
		MIME: application/vnd.in-toto+json
