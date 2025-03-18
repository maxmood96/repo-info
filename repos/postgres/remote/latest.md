## `postgres:latest`

```console
$ docker pull postgres@sha256:58bb12171087c66904a8e9ef17ddfd8e36580ffa3926cb15b4e212abf3f7ef30
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

### `postgres:latest` - linux; amd64

```console
$ docker pull postgres@sha256:feedab244d0d4cd740debc3a533cd641b2fb7d99c3f056de61972093970da724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156265039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e3e031d245f3b1018ac3d56a65130a0b7b6c2a55c16b856445a9fb04ddefaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec99121872b9705f7cf5c0d01769b1582c5ba2ed7a486e75a8706858a8f3bf8`  
		Last Modified: Mon, 17 Mar 2025 23:19:25 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133acbc970dfb4324e8c9658192867ff13da9066590dcdf06d7cac787d80afd4`  
		Last Modified: Mon, 17 Mar 2025 23:19:26 GMT  
		Size: 4.5 MB (4533760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02d97322fc66d8759777ebb492100ae4a8052a34e8753e0bc8878750b224631`  
		Last Modified: Mon, 17 Mar 2025 23:19:26 GMT  
		Size: 1.4 MB (1446696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9643c6baf334f5c5b6f312378aa2a60dd143946429041f16527189f08ae923`  
		Last Modified: Mon, 17 Mar 2025 23:19:26 GMT  
		Size: 8.1 MB (8066271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcedd9434e7a615510918b613a189718cc11fee3257b034b9af0d27b7c1d8fe`  
		Last Modified: Mon, 17 Mar 2025 23:19:27 GMT  
		Size: 1.2 MB (1196082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8982ec96d9c56cb81d780b2b7426845d1f9a3e8f6f616f3bb1d5ab279cf58e`  
		Last Modified: Mon, 17 Mar 2025 23:19:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1824bd6b75d7d438c79f4ee81596d533e6443028bbc5c252088eaa61af3f38ad`  
		Last Modified: Mon, 17 Mar 2025 23:19:27 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbad2bf2d5e63ca8134bcf7a57b0b3640c6eb0cff7d940853bde024b17091538`  
		Last Modified: Mon, 17 Mar 2025 23:19:30 GMT  
		Size: 112.8 MB (112796747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221788d726069b6f14ca774b636552eecb38e2280d53e9e594aba6e1c5ba2df5`  
		Last Modified: Mon, 17 Mar 2025 23:19:28 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f43b682bc0d6d3bc63d0aa96010fdb037b8791bbf0ed872924beabe32d687e`  
		Last Modified: Mon, 17 Mar 2025 23:19:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a2d9e24ab03fc501d3616d22bf09e2f3c1096e7df864aa1d6cb17fde2b7d4c`  
		Last Modified: Mon, 17 Mar 2025 23:19:28 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96cb29b0d136ec56828349bbf5512fb8f9f8977bd2f25643955789d9ff96e97`  
		Last Modified: Mon, 17 Mar 2025 23:19:29 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14097053814583806579566f3a6cf85105159caf0cf2218c42f363716b572401`  
		Last Modified: Mon, 17 Mar 2025 23:19:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:df931ad5c3ec7f61da3173f28b1260c26b66b36a4fe7680e120f4f7cbc9d7719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5873343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10de7e1e4782579a4528dac2947b5372f26db991831a1ebf3732ea527aeaead6`

```dockerfile
```

-	Layers:
	-	`sha256:ae27471804101e23c1644e26c9a82ae49ac179640c63720c1b880a7b5382c310`  
		Last Modified: Mon, 17 Mar 2025 23:19:26 GMT  
		Size: 5.8 MB (5818657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75c83e77f245b6930022cfa9ff7b6177575d3996f5b431e293f949ca19df53d2`  
		Last Modified: Mon, 17 Mar 2025 23:19:25 GMT  
		Size: 54.7 KB (54686 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm variant v5

```console
$ docker pull postgres@sha256:bb3aaf90fe61f113b2cd37142fd4598df59953b70d979c3326fcef65c290f5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149344673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c872108f9e9fd5aece16179824172f0d4baf9f75185ffcf4c648c358ef31aa28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ae6e8a56f74f787b0f7d9aacaa13d7b6ddf781a6f4ad61fce864e911f8d5eb`  
		Last Modified: Tue, 25 Feb 2025 04:07:17 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7e5c1eb3eed5a4a7533ef45712de74bcdf7f12a622e29c36426ce933d0103d`  
		Last Modified: Tue, 25 Feb 2025 04:07:17 GMT  
		Size: 4.2 MB (4150963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a7a98a42d1a7c378de936bdc8454809227da584ea5bef2b083e497eaa5c43`  
		Last Modified: Tue, 25 Feb 2025 04:07:17 GMT  
		Size: 1.4 MB (1423891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67d002c2bf3c5b50f61f0640d5aca352133a5dc309e2762537c449a3aca845f`  
		Last Modified: Tue, 25 Feb 2025 04:07:18 GMT  
		Size: 8.1 MB (8066428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c3bbd93e97b9c314fd0cdcd835f599dcfaf56503d8b1b05d433b17aaf9acdc`  
		Last Modified: Tue, 25 Feb 2025 04:07:18 GMT  
		Size: 1.2 MB (1194896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60a6013dc8012881f58cdc518550e78876486822e65bc24f835046246937f4f`  
		Last Modified: Tue, 25 Feb 2025 04:07:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e491b6f06d34de84c3d46761533989f0ba58103527e7315fd02ca1307d404efd`  
		Last Modified: Tue, 25 Feb 2025 04:07:19 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ca134efb0a8d50472e4fa33b3f54703b5338918cae408c1062c0cc3d020972`  
		Last Modified: Tue, 25 Feb 2025 04:07:22 GMT  
		Size: 108.7 MB (108747241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1919cb0e01e171511e2bcba3d9f91d7a04959ceb4eefe2f2e79e41c9eddac`  
		Last Modified: Tue, 25 Feb 2025 04:07:19 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bc74a53319a20dc3b387c5d082315b19db93e0dd01cca4376cccbbd2e805cf`  
		Last Modified: Tue, 25 Feb 2025 04:07:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14155d8fae331229f2ef187bec36a7b4b0d2ca5f0fd72d5dcfbc0fe449e5eba0`  
		Last Modified: Tue, 25 Feb 2025 04:07:19 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2768532220fa43058da019529186d11e1cd65ace05a5546f0629e74fd77a4ca5`  
		Last Modified: Fri, 28 Feb 2025 23:25:38 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ae408de246225625abc6e771dcdb2f1091d9b6ebe5b0f4c2257676dd2b18e4`  
		Last Modified: Fri, 28 Feb 2025 23:25:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:af7f47af1c2a8f87d59f7b774fcbbc496f6fbfc1fe4c4c7fcb13cdd53736c344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d90a204efaaa3203762d5bb99830fa28c8205f6ba683b58bb6f51bbab3872a6`

```dockerfile
```

-	Layers:
	-	`sha256:d86fe033cd3aa06fb46cea9bd35930a6de3ced8f9e2dc5c33f228a49a5fedad1`  
		Last Modified: Fri, 28 Feb 2025 23:25:38 GMT  
		Size: 5.8 MB (5836318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbfd2225405933361aad31cb3d839b7e575acdeeaac5811abcd844ebf887a22f`  
		Last Modified: Fri, 28 Feb 2025 23:25:37 GMT  
		Size: 54.9 KB (54922 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm variant v7

```console
$ docker pull postgres@sha256:57dbbb122cd0360b0e2bc8705b390382436a4bc9a1f978d92321d25aa5abe9db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144319456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cd654d8539d832a544779d28b63fa1751622e2ba23bd326650e3ff9587e58e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef1a62fea3591817dd52ef79c2559e3f123f349e3cfb5daa531aa5cca19b472`  
		Last Modified: Tue, 25 Feb 2025 04:46:30 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7fcd67935c62da60cf72e0773d008569b0b74d953aaaa47cec7fa02c053e2b`  
		Last Modified: Tue, 25 Feb 2025 04:46:31 GMT  
		Size: 3.7 MB (3742519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c33114712a5394935dc60fd5476e337fceb02111c95d54574d741be93394edc`  
		Last Modified: Tue, 25 Feb 2025 04:46:31 GMT  
		Size: 1.4 MB (1413606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c45fc13a8ea6d2ff0d390feb17e5cecc553b36e92d0af9cec523c5b41f507eb`  
		Last Modified: Tue, 25 Feb 2025 04:46:31 GMT  
		Size: 8.1 MB (8066258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4108b27ebae515afd276a5c91e82f4b9db92464f3b632141345c92ebf2c145f`  
		Last Modified: Tue, 25 Feb 2025 04:46:32 GMT  
		Size: 1.1 MB (1066952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1741afe59bc11a091b636d1e593e15ff354fad80b9671c6764f5f460651d5544`  
		Last Modified: Tue, 25 Feb 2025 04:46:32 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe23fb58710d0e592960dbee784d541353764b757bafb7ff6025d09df4197991`  
		Last Modified: Tue, 25 Feb 2025 04:46:32 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cccec0590d87309ebad1b3e7dd08c3d62029b4866dd7f5aa79e33e3e972598e`  
		Last Modified: Tue, 25 Feb 2025 04:46:36 GMT  
		Size: 106.1 MB (106089771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be265954f125aff1a436ac279ec1452dcee0844a58ae2ea0fb4fc5036e423cb`  
		Last Modified: Tue, 25 Feb 2025 04:46:33 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b38587b9b0a3828fd5a2f54d48da76f0bc48c6dedd2a579d8cc00c12421cf8`  
		Last Modified: Tue, 25 Feb 2025 04:46:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d168fd24f0e603ae961334529817ca936d3c4e1a197b4ef3ca1fa38bf4f88fb5`  
		Last Modified: Tue, 25 Feb 2025 04:46:34 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d2e36948f28f3b3e81126b142df16fad5c59aa2098cf2dc890c3d76abc2937`  
		Last Modified: Fri, 28 Feb 2025 23:24:17 GMT  
		Size: 5.5 KB (5472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200f0dded12a10faee12e6a3e1dd628bfbb933fe2ce2e9c41d4d0c5bfb4ddd1f`  
		Last Modified: Fri, 28 Feb 2025 23:24:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:65b11cbd4ff73d3b54a8cea552be32ee1c372ec2121955f0c7eb6b40a4dda4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5890811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a3aec538ce2d174f6066ca8cbef8b336b96d6c1774cd5f5e933a5185fe720d`

```dockerfile
```

-	Layers:
	-	`sha256:f7748d97e09cdbdd48dde6653d462bb7fbeb98213665d634b7e001428bc42f7d`  
		Last Modified: Fri, 28 Feb 2025 23:24:17 GMT  
		Size: 5.8 MB (5835889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:607b16f05b25c6df3bb6acd8840e9c84089a64ec2ea513b95f2afc1b93d37ce4`  
		Last Modified: Fri, 28 Feb 2025 23:24:17 GMT  
		Size: 54.9 KB (54922 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:100f73067f3a96f6b9b7949c4ae38a8999ba029b10e70853a3a62fb6152cf3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154103570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b50489eee84910b677888d621e0b5ac59a956ce976d158886cb61aa3c482448`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774c54d2d309bc0d9f02c69b29d119216a5a164fbf6cec3480052d097e25f9ea`  
		Last Modified: Tue, 25 Feb 2025 04:57:16 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f36104e57cc5d7fd06391de5bb22aeddbffecb409917d7ecc608c2e3f9c80`  
		Last Modified: Tue, 25 Feb 2025 04:57:17 GMT  
		Size: 4.5 MB (4499142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1655e767f751e08409bb39b05f82292ac7689e09a26a6871442725c24b57d8b0`  
		Last Modified: Tue, 25 Feb 2025 04:57:17 GMT  
		Size: 1.4 MB (1378737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8078a8a245e2f42169dc661d903d811d08a63cf566346516a68aa7477130ae`  
		Last Modified: Tue, 25 Feb 2025 04:57:17 GMT  
		Size: 8.1 MB (8066359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b1b7588421aa8a2178678ef8042b65a9bfc5ade9fea7c685f5a674906db062`  
		Last Modified: Tue, 25 Feb 2025 04:57:18 GMT  
		Size: 1.1 MB (1108728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8417b4134b63cf9697a07dcf7dc6b1801e18389ca122d20a2f66d86fb9d102`  
		Last Modified: Tue, 25 Feb 2025 04:57:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dedce88ca1d4ac15e6d2943f50b93e8fc6b8d5c8902ac60abbdea76b6392e6`  
		Last Modified: Fri, 28 Feb 2025 23:25:32 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551bc275c65f845b384bc7a0fb10652219a511f98d9f01f23485395c2b03f5d1`  
		Last Modified: Fri, 28 Feb 2025 23:25:35 GMT  
		Size: 111.0 MB (110981554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6810bb3d75b9d9d71f1ec5bf9e855922d5f98985a51e17034c367b66a45f97`  
		Last Modified: Fri, 28 Feb 2025 23:25:32 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45b4b1e09b9039162df2851f083036de5f1da48d4f099d5433cd01c3b6730d0`  
		Last Modified: Fri, 28 Feb 2025 23:25:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfbe96df98f3912bcfd860546a5a2a9ded49c28273012afb11995c3da867d9a`  
		Last Modified: Fri, 28 Feb 2025 23:25:33 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434de25e58a434db3f52013add56aa2e7aa6d3551d308d6885c3eaed4bbafdad`  
		Last Modified: Fri, 28 Feb 2025 23:25:33 GMT  
		Size: 5.5 KB (5476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c21e9d8fa8c0a7e419ce04d3585929ccf0db1955c9aa52903c359df462c8d18`  
		Last Modified: Fri, 28 Feb 2025 23:25:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:083675630bca23e3ff43261046378c197647090811befa7d674471af4c728786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5879988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ddc75583c9ad8c2040ee49a1fd999ffa9b3d4ced6bbdd188e1e5806ba4337e`

```dockerfile
```

-	Layers:
	-	`sha256:5f4908df154b0947c10c91b24684e0b88d15e32ea82daee961a5dc548f031259`  
		Last Modified: Fri, 28 Feb 2025 23:25:33 GMT  
		Size: 5.8 MB (5825008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f16f229126a42cb703d137953b40c9575b92e9220bc2b4c5139cb76988710a6`  
		Last Modified: Fri, 28 Feb 2025 23:25:32 GMT  
		Size: 55.0 KB (54980 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; 386

```console
$ docker pull postgres@sha256:8df947e4b872177cbc2d6bae01c46542631982deaf8777849decd495f3fae0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165182241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53dc543fd6768c85696261aa6aa29566fd82d3484385416ab897d84f39dc3bbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83fa51b272e9799473c78d3d795304e4f38e071d315ba22df021948b1bd5566`  
		Last Modified: Tue, 18 Mar 2025 00:39:08 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c11a601a0c363d9d7f592b8c8725d23eab36a44d7f5920fe82619a8d2044b7`  
		Last Modified: Tue, 18 Mar 2025 00:39:08 GMT  
		Size: 5.0 MB (4965066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327e18de29548d9f37d40ada7d7ab67e6c2f40fffe99232dd06fd0b1d3b83b3f`  
		Last Modified: Tue, 18 Mar 2025 00:39:08 GMT  
		Size: 1.4 MB (1422120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e8e5e31a9c5347d15484c6b39de0852906b55a8e51e1ae3736f80056c33a14`  
		Last Modified: Tue, 18 Mar 2025 00:39:08 GMT  
		Size: 8.1 MB (8066267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e8b14ad17c2e553ebb5ee793a0f1af8126eded5a85b7c4538f95327a035c63`  
		Last Modified: Tue, 18 Mar 2025 00:39:09 GMT  
		Size: 1.1 MB (1137187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30597119796eebc8c14fe0eda5c7141fa11acd7e5c84e56ab186ec151febcbb4`  
		Last Modified: Tue, 18 Mar 2025 00:39:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5f05d140330fb5c7470e3afc2a8dda89eb6f1985e43ed63a0e02464b94213d`  
		Last Modified: Tue, 18 Mar 2025 00:39:09 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40203dd3d2b2c9a46534db086c18d68da7688c2f2a7b753c107b89600878272`  
		Last Modified: Tue, 18 Mar 2025 00:39:12 GMT  
		Size: 120.4 MB (120381455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f3e165f6160aa98bdaef9fb0e9d6bf4084e7549bcf67277f222bf4fff038fd`  
		Last Modified: Tue, 18 Mar 2025 00:39:10 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39208ee19143437243d97acb38f0a3d0f9978b684b1d50ad1d4edd12e64ec6a1`  
		Last Modified: Tue, 18 Mar 2025 00:39:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052d0764281469a5fad02372992090994d83369265db57906d5f1c5f7ff19530`  
		Last Modified: Tue, 18 Mar 2025 00:39:10 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe20d4df2f4b75f775bf1d7e1143f79bc355fbccf2c6be0c734d67277dfaea`  
		Last Modified: Tue, 18 Mar 2025 00:39:11 GMT  
		Size: 5.5 KB (5475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08d7b90e7fd3c643d35b5b2719bd2d2ae31be52f0eb405ef90faa0ae7a8484a`  
		Last Modified: Tue, 18 Mar 2025 00:39:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:dd11cbb6a3fdf5f28f42d75585c7ddc6c3d44ea5cfeaae24e643883de9c36a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bc817bde261a2febbe208c37ddb9887003d15635197701751d97e980e1682f`

```dockerfile
```

-	Layers:
	-	`sha256:f4c16a990f20b861145d0a947aa450e42f4f4fbff0966a8d1704e2feda85d442`  
		Last Modified: Tue, 18 Mar 2025 00:39:08 GMT  
		Size: 5.8 MB (5834342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ed72410ca84af200c2828e59ea6b6ffa1ef773db1fb3e903f27a447a9dc2c35`  
		Last Modified: Tue, 18 Mar 2025 00:39:08 GMT  
		Size: 54.6 KB (54623 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; mips64le

```console
$ docker pull postgres@sha256:969bddebf945622bf4f4efb208ee90a1a783f11e19d4a8438992c9a3aa7f037a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155134233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae95855635c3e259795973cbb8216c9a735c46ca4ab54561e06fa13cdd588391`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b7a47f378af392c2d994e47ff5f365139e1ecae15d8d5f92234995297551d6`  
		Last Modified: Tue, 25 Feb 2025 09:53:03 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10229a3a88d3787bd0e7113d1114eb0c919f160ffb6386f03eee4f277112ccb8`  
		Last Modified: Tue, 25 Feb 2025 09:53:04 GMT  
		Size: 4.5 MB (4475116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6729f3ead4b295b74dd33ba806f7ab97ab155c1e99a22ad041ee861bb5880e5c`  
		Last Modified: Tue, 25 Feb 2025 09:53:04 GMT  
		Size: 1.3 MB (1333791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d01fb72125d7d0c4ec5d76599047c4417c6d11cd2ded1f0677f0b2c678a66a1`  
		Last Modified: Tue, 25 Feb 2025 09:53:05 GMT  
		Size: 8.1 MB (8066459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3128187c95e7ff6cbe6ddfba5a07ac591b6b6a8740654e2fd3b6457e3d8a9f29`  
		Last Modified: Tue, 25 Feb 2025 09:53:05 GMT  
		Size: 1.2 MB (1182666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f5a16e1637a0cbabf64edde767edc9e2a9fd6b003dd73863befaa724f4e7df`  
		Last Modified: Tue, 25 Feb 2025 09:53:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a319b3f9bb6db2b0efceb2b096459ef43ee4bd098cc1a186a572b5e57575513`  
		Last Modified: Sat, 01 Mar 2025 00:36:51 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dff5358bfc85f00939ad45942c48c24f8467558ae6e71414f79836c30162d84`  
		Last Modified: Sat, 01 Mar 2025 00:37:02 GMT  
		Size: 111.6 MB (111561880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5e53f70ad9432a44ce789ed20a5ec763fbebe4f8f76071a8fcc6c243e19962`  
		Last Modified: Sat, 01 Mar 2025 00:36:51 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7de395de46863f95e9e167ca808434d38af86d59ecc1375a0aa249fe8f514e1`  
		Last Modified: Sat, 01 Mar 2025 00:36:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342277229903f4d5c4fd9380877d3274a48417d17e3e439af17d459467f50301`  
		Last Modified: Sat, 01 Mar 2025 00:36:52 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f6114ddc416bc8bae46e2c1c958050883d7e8b8a4275111f5a2c3851744d9`  
		Last Modified: Sat, 01 Mar 2025 00:36:52 GMT  
		Size: 5.5 KB (5477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50273361bb70a08d696d6a42b7461eb998c854cce1b7c2b370b5bad43c88f1ed`  
		Last Modified: Sat, 01 Mar 2025 00:36:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:3a64aa27578d0ccb93632eeaee4a58bc6090736e14529aca70cbe437381803e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 KB (54589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a2a1900e4e3885be8242afed2ae9f7af27d81deed543b25e5497791719276d`

```dockerfile
```

-	Layers:
	-	`sha256:f5d7b6074e573adb9ffde139d0c557ed10ee739ef2c3598355be21aab5f6c91c`  
		Last Modified: Sat, 01 Mar 2025 00:36:51 GMT  
		Size: 54.6 KB (54589 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; ppc64le

```console
$ docker pull postgres@sha256:b60247f75b1dd1ce16933d8407743b724685a73cae9bf6294e95b064824b90e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.0 MB (169039657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d752b248bfdb18bcf4238a716c2a8f3ec39f855a020ce344e7b39fa3191c80f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac954bd36cb4d3caebe7e61de9d51f58c1ffaedc4cda3c904297558eab9ce36b`  
		Last Modified: Tue, 25 Feb 2025 03:58:02 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8e2ed2c480eb31e9a5576d38bceb6fa9dd377e634b7ff8b0f5d3cc42e7db6c`  
		Last Modified: Tue, 25 Feb 2025 03:58:03 GMT  
		Size: 5.4 MB (5368256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09570715ce0677b2b7b2e018987af73073b0122db22458a72f57b914a0874d42`  
		Last Modified: Tue, 25 Feb 2025 03:58:03 GMT  
		Size: 1.4 MB (1368690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed6fca48ebab6c7ac4a548551eca931bfac28e13a607ee9e398157384c1638f`  
		Last Modified: Tue, 25 Feb 2025 03:58:03 GMT  
		Size: 8.1 MB (8066406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bba706fadc2087d66a1bca0e5cdd71a9aa301cedcab29ddcd37ea8e2dbb363`  
		Last Modified: Tue, 25 Feb 2025 03:58:04 GMT  
		Size: 1.3 MB (1283536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d62b37b54dd01e35b1f6313a3012f7d1609ad004f64d8241b75a9466274b89b`  
		Last Modified: Tue, 25 Feb 2025 03:58:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfc2180e0627edc5acdad7d7376200cb70b92811ce71ff3c832e1f544695a8a`  
		Last Modified: Tue, 25 Feb 2025 03:58:04 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67a9a2b5b37860e695e86526c45257187f779cd753ae83e6e7f9d831855e7cb`  
		Last Modified: Fri, 28 Feb 2025 23:25:56 GMT  
		Size: 120.9 MB (120879831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6dccae203017aa9b205db276267e436d6ad10e08a9007b2979effe412528b8`  
		Last Modified: Fri, 28 Feb 2025 23:25:52 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab326e890418152eda90fdd1da7f39dbb2f14f5387ca33302b689f99441c1a66`  
		Last Modified: Fri, 28 Feb 2025 23:25:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e57e43f51638e3f5ec2c543066ca51ccfc25f54a312ae6766511fb4fc0aab37`  
		Last Modified: Fri, 28 Feb 2025 23:25:52 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab55f4f197de82c6c81ccff7c8347baac8f3f7cc9408074f8fcced021b22f02`  
		Last Modified: Fri, 28 Feb 2025 23:25:53 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ae408de246225625abc6e771dcdb2f1091d9b6ebe5b0f4c2257676dd2b18e4`  
		Last Modified: Fri, 28 Feb 2025 23:25:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:e8cab8ab9f90a57ebd70ca455cb2c6e7084b9f585f8729d6efa5a1c33c7b7bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5880671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badeea205a219e3bb5d484c4f9f3ed2d376cbe1fa88ba6a3ad16d9e722c9f271`

```dockerfile
```

-	Layers:
	-	`sha256:f4a6b1b4000d4f2402dd1dfa4650b7755f15cba36ed64c210eaf00c55dd19fee`  
		Last Modified: Fri, 28 Feb 2025 23:25:52 GMT  
		Size: 5.8 MB (5825906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc54062f3a5bb571db61bea67b5d4c2e7315d1ab93c15798e548cd6727a513bc`  
		Last Modified: Fri, 28 Feb 2025 23:25:52 GMT  
		Size: 54.8 KB (54765 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; s390x

```console
$ docker pull postgres@sha256:415263a5ee2928c6e1675fc0ce0330fa7fb9510261913dfef71995788b7646ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165402531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5eff40b3fa823057139ddd7bf1e282d22bb8f5857cfc937855ede1f3240ecd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c0aa600752d291a77bfc958eb9eb6772726703221cc4fcf99a44665fc1cfe`  
		Last Modified: Tue, 25 Feb 2025 03:42:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a63e50d66d5cd10e3a8c18df9c8befe4268834fd1eb1869ba5240c6e600beb9`  
		Last Modified: Tue, 25 Feb 2025 03:42:04 GMT  
		Size: 4.4 MB (4390981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b052f44a4679e17525e1bc75b685a791e2b73345c61054f1185f42b857d09e3`  
		Last Modified: Tue, 25 Feb 2025 03:42:04 GMT  
		Size: 1.4 MB (1412657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0c7a8a0744c5aecd4d8342daf0f3ff3cb5f530c3f956f740f475b3d2d3992c`  
		Last Modified: Tue, 25 Feb 2025 03:42:04 GMT  
		Size: 8.1 MB (8120431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed4ea1e6d4feccb2fc26d3befb3c8930e35940c91c70249901ef79b1afdda73`  
		Last Modified: Tue, 25 Feb 2025 03:42:05 GMT  
		Size: 1.1 MB (1096725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6c6185839c1a9d559d3638afcd2598ea4b67f1333615c69a77218deddc2bb6`  
		Last Modified: Tue, 25 Feb 2025 03:42:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bbb1611de92b6ac803ffcd04142e37784bd4e69d4ced471a3208040d73199a`  
		Last Modified: Tue, 25 Feb 2025 03:42:05 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6947acb27ae7b4a867594e16de3ff6f8827994eea81640ef67ffd33717dc94c5`  
		Last Modified: Fri, 28 Feb 2025 23:28:05 GMT  
		Size: 123.5 MB (123496268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f149e3fe3e58e7246d904167a897b2e36cf40a4ba2f843514766ce6a0a41d80a`  
		Last Modified: Fri, 28 Feb 2025 23:28:02 GMT  
		Size: 10.2 KB (10248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e3cf6a5f688918a6359472a251554c1ea2fc56fcb04f0c2f9cc241b516b04e`  
		Last Modified: Fri, 28 Feb 2025 23:28:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d23cc0f104d75d5480a3a2610134b734b25aa2ea732f4af561f8dea8e961859`  
		Last Modified: Fri, 28 Feb 2025 23:28:03 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad13638376863d4df42c820ca704ccf9f57ba429354ec85d498cbfb64b2a382`  
		Last Modified: Fri, 28 Feb 2025 23:28:03 GMT  
		Size: 5.5 KB (5475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e8facebe1968157f2742b37ed2dc48d5b79a8e8e18d571fd878ea3bd88ae02`  
		Last Modified: Fri, 28 Feb 2025 23:28:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:afbe1036f99cd2a43a38af9fd734440c365cb3d6643f6b3af74b1f7b62c4e191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5872615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e8ac91d8245ebe07b36368a536a4b5b870278dc3aafb69ea2a8f1a2ee816f6`

```dockerfile
```

-	Layers:
	-	`sha256:82b53ef97612a81bd63d9c91de5a97e487d93bcc86f4c1c3f44322d7388c5025`  
		Last Modified: Fri, 28 Feb 2025 23:28:03 GMT  
		Size: 5.8 MB (5817928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4881f308c65a441978d9774d5f5186861106b30ae2f22a6a5fc77d2887d3ecb1`  
		Last Modified: Fri, 28 Feb 2025 23:28:02 GMT  
		Size: 54.7 KB (54687 bytes)  
		MIME: application/vnd.in-toto+json
