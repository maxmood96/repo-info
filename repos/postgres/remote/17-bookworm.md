## `postgres:17-bookworm`

```console
$ docker pull postgres@sha256:7c6f7103422e90215a56bc91d2c9bdabb83c491b885d1ec7b1dfabece3d5ce24
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

### `postgres:17-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:ccee7254774ae3932cd496f4fa3a38c7e338746a223de16a67162cb9033a44e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156018217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a131ba16a1756314f9ca8eb43abbd704fbb1707be5ac5905a75563f4cf130c55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212ddcf65ecd88515f3c199a293e4cd56b0f505b65061137abc78e15b17073fc`  
		Last Modified: Tue, 30 Sep 2025 00:08:03 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059d20ce3237b9b4df6341f88dd4a40765a0113fd518281291d873b7f7b2e996`  
		Last Modified: Tue, 30 Sep 2025 00:08:03 GMT  
		Size: 4.5 MB (4534081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e383ba21768db4028c6516ffee560b9be9756b21de8fc69ff5c1e6020d6dfc9`  
		Last Modified: Tue, 30 Sep 2025 00:08:03 GMT  
		Size: 1.2 MB (1249493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35611909a9ff29acfe1bc20558450db7691bf68da35b9d7be88a4f81ed5ecbfe`  
		Last Modified: Tue, 30 Sep 2025 00:08:11 GMT  
		Size: 8.1 MB (8066499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c644dc576cca3c19eb1383aedd46538e58ec396f4e4a4b00eafbda9cac2299a`  
		Last Modified: Tue, 30 Sep 2025 00:08:03 GMT  
		Size: 1.2 MB (1196394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944373a00a694ccd75e08b82325739076c2ecf04d097d0fbe2d2738e176065a5`  
		Last Modified: Tue, 30 Sep 2025 00:08:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e391c85e0431862d69e56d16085be7abecebd5e49e524e1aa3732305a31372`  
		Last Modified: Tue, 30 Sep 2025 00:08:03 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2f2824e8e3ac18374ae72e9b2c0e56df9d40c491057b321b3c2b0579b1e20`  
		Last Modified: Tue, 30 Sep 2025 00:08:32 GMT  
		Size: 112.7 MB (112722363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b291d59feb6c13c4b6f953f2bedf13f4840cae292d709dd2de5ecabf9dbbd7b`  
		Last Modified: Tue, 30 Sep 2025 00:08:03 GMT  
		Size: 10.2 KB (10230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef86185b7558b1443a5c99b395ea121cf1212b90e858bc509e50fb76d21806e`  
		Last Modified: Tue, 30 Sep 2025 00:08:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a17156c87bcea4c7ff86e4d8a8a9b4d13a8f600d94dd2edb7ea2bed6fb8b1f`  
		Last Modified: Tue, 30 Sep 2025 00:08:04 GMT  
		Size: 165.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88532f0e86ff7c00a532ae882d9fffc2c9d60111b9cc66e28b6746b26374e3a`  
		Last Modified: Tue, 30 Sep 2025 00:08:04 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eddb11950c94568a28049099fae77b161b20acf190c165a3d8bf11cc691e06a`  
		Last Modified: Tue, 30 Sep 2025 00:08:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:baa353c77ab03cae0e6cd9a72e4437da707cbc3dbfd3f66ac0741a2356b6f695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86974174d8c18de5dbe7977956edd3d6b6865293a60a6ae0f85b1a1a00661998`

```dockerfile
```

-	Layers:
	-	`sha256:b2afe3cc9fa0ebb5fca2656c8324c1266b35a5437d3820d7e3286bb561f42c41`  
		Last Modified: Tue, 30 Sep 2025 02:10:09 GMT  
		Size: 5.9 MB (5927456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40d04e1d3d902552868d091bcfc298d0baf6ca493042a529bf1c60a4fdbd0610`  
		Last Modified: Tue, 30 Sep 2025 02:10:10 GMT  
		Size: 53.3 KB (53333 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:8f85a9b2d5f4e946a6781a0f85fa26c90ca5a35e9153624b88aa82a9a2427d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149041120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2cef0629a101f3b2e12e0d97c4c020c9835af67bd00a53bf679ffa8ca2c0f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e1e8cf6a98b379fbf689c13a9736cd1289212f7d1817f7bef04f737d92c4359f`  
		Last Modified: Mon, 29 Sep 2025 23:34:08 GMT  
		Size: 25.8 MB (25757437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6de4d0c1a65bab9af7199f7eceadc915f4548d8f1e15f4a4c9870bf6849373`  
		Last Modified: Tue, 30 Sep 2025 00:07:01 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b9d343b79ed3a37b78a19c0dc0a5837f5dedf45802d4b121c7e9210a702aad`  
		Last Modified: Tue, 30 Sep 2025 00:07:02 GMT  
		Size: 4.2 MB (4151189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cf99af8d1c41170fe7992395ce392cf1d31d9fcc9534bf1e79050704c7dcd7`  
		Last Modified: Tue, 30 Sep 2025 00:07:04 GMT  
		Size: 1.2 MB (1220053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421a388c176191bd97226c8e692c884d950b813fd7e94e11ac75407612d2d542`  
		Last Modified: Tue, 30 Sep 2025 00:07:02 GMT  
		Size: 8.1 MB (8066581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b7b0d1e6736b5e25ebe5828cf3ccb0d427c64f74526eb283ca919853b4b43e`  
		Last Modified: Tue, 30 Sep 2025 00:07:01 GMT  
		Size: 1.2 MB (1195034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b8d4e645a4119a64343d639cfde6795ac0f28a5ec0eec81b561e56ce30c26d`  
		Last Modified: Tue, 30 Sep 2025 00:07:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dead5dab4558a9336b88e40250e95701b9d4f36486fdc46126c5676dc84d392`  
		Last Modified: Tue, 30 Sep 2025 00:07:01 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b662efe03822409d75b4373ebd5c9a6dc7d64c8a252a0bbe4a88557f0bce94`  
		Last Modified: Tue, 30 Sep 2025 03:07:37 GMT  
		Size: 108.6 MB (108629760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5452d5aacc49370cbd0600111f9d035243cccc53c33eeb092fe0aef49ef0698`  
		Last Modified: Tue, 30 Sep 2025 00:07:02 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004aba5b61f571eca3d07e837f465b90a48fa0c15b9c7f7701e78255a157ad8e`  
		Last Modified: Tue, 30 Sep 2025 00:07:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1679e49bec13a017c99755cce58ad091f1508be49fbf3f3032e56a72b89e3a7e`  
		Last Modified: Tue, 30 Sep 2025 00:07:02 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b09bc28c4849ac9ed9c5c52463ae960f915ff15626eb93ceb999e6011abb83`  
		Last Modified: Tue, 30 Sep 2025 00:07:02 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a551bbfcf8189c832475827def5f499de3e92051406ae984f6259ff5723d1f58`  
		Last Modified: Tue, 30 Sep 2025 00:07:02 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:228741291f818c2b79bdfdbcceb803fd62375232a271ec0a0e79ddc7c78624de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4864cd88c7e1f82a9a6f6c2521a7820491215971631ac218aebe2a44e327a8`

```dockerfile
```

-	Layers:
	-	`sha256:3572e53cf2d9825489e41aaad5b2628c3d3ae4d109a147051f2f376a3ab61321`  
		Last Modified: Tue, 30 Sep 2025 02:10:15 GMT  
		Size: 5.9 MB (5945771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:066067efbc9bb07e84c643acf4d0a15ae140c3ef557cfc4483e4a9af3c32593f`  
		Last Modified: Tue, 30 Sep 2025 02:10:16 GMT  
		Size: 53.5 KB (53540 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b1b1b31f09877ed0319415125286b487d9b60169226ae62a1804d034f0238a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144046249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7750278d8f9fd9d3fbed43a119449b4801ad5810153b7411298ef95d2f8bf459`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4c0d784fb90dddd991d201014e92ef1ebfe9a20d0f2ea56e2701fb9e8219be91`  
		Last Modified: Mon, 29 Sep 2025 23:34:19 GMT  
		Size: 23.9 MB (23933930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206909334651444dc414e54a3a8ba535095569e9883fe07ba3e99b1794f03044`  
		Last Modified: Tue, 30 Sep 2025 00:45:13 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6950f88e2165456213c415abfe260132b3f95d3aa158cca8a2e9fc62acde75da`  
		Last Modified: Tue, 30 Sep 2025 00:45:15 GMT  
		Size: 3.7 MB (3742707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72404ffbe0c36bea2380eab30d038bfe123e1a2c767e1882343e0efd2dc3c4c`  
		Last Modified: Tue, 30 Sep 2025 00:45:13 GMT  
		Size: 1.2 MB (1216001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfa5673c2d9b8c4f9fd616d979c375dfef427093109e6f93d215b32749dbf01`  
		Last Modified: Tue, 30 Sep 2025 00:45:14 GMT  
		Size: 8.1 MB (8066443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7483c07dfefb8410df9755a99e990305be380af8d9470caa5967d6b2d7e3b0bf`  
		Last Modified: Tue, 30 Sep 2025 00:45:13 GMT  
		Size: 1.1 MB (1067233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e1d67a8538bf648e7faf9b156e492d19555b39ec8ddbc3ab788a8174070313`  
		Last Modified: Tue, 30 Sep 2025 00:45:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c76825a2c0015ebd854f5d4650724f14b9c338908fed6455005238a05921a0e`  
		Last Modified: Tue, 30 Sep 2025 00:45:13 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5789e163af9ef479cc8da890b3f7d87aaecb605e61145ef6769f6691c28e1103`  
		Last Modified: Tue, 30 Sep 2025 00:45:25 GMT  
		Size: 106.0 MB (105998873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692ccf73104c52d0d79ebdeed80b986eb96ebd900aa7c70ad0cf7eac317254d4`  
		Last Modified: Tue, 30 Sep 2025 00:45:13 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edb1c58de6064763138ec9425119456b6b050122c625c9066333cade8087784`  
		Last Modified: Tue, 30 Sep 2025 00:45:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87589e720933a9b68f131cdaccdc3a083119684850b1896abdb42a32ad5d9006`  
		Last Modified: Tue, 30 Sep 2025 00:45:14 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6286c29716f56d44b9bfd1b49b1a2b3b253889506e5b272384fda204050b201f`  
		Last Modified: Tue, 30 Sep 2025 00:45:14 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e18a565ca4b95a84012e2ba66c9ea0a13cbf797a13e474fb20b38f7c9eddf7`  
		Last Modified: Tue, 30 Sep 2025 00:45:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c2470589d43e14dec2f945b8d419c480ae0e9ef5c05e0aebe8b7c0161c35ed56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5548b4c5db337c4d171bba3dc7ca623152c417b8f9463c97f6a0062ea6476c2`

```dockerfile
```

-	Layers:
	-	`sha256:f8b94dcef544bcb2188e95381333aacabba3e64c40cd727db8ff6cb397e00031`  
		Last Modified: Wed, 01 Oct 2025 20:16:21 GMT  
		Size: 5.9 MB (5945026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2f12c68d0ea3a0d26535b73b54245c743672665500df0663e00b3057072dffa`  
		Last Modified: Wed, 01 Oct 2025 20:16:22 GMT  
		Size: 53.5 KB (53540 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:1b3eb9a58d4f74b56fb3788e142f4b1883bec1fcc2d83cc417659c81c5507fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154014684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01ec2aa71d7da6d85e81336da11648c8c93556c2a129896acc3cf0babb64879`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35c856452a418a42ee43d4df8953d3ccf71f2e422842ed41564ca3743f35b9d`  
		Last Modified: Tue, 30 Sep 2025 00:11:20 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49819e59b672f01489d1f76cbaac7f1d5c338a7b605b4f19f2cd044868930bae`  
		Last Modified: Tue, 30 Sep 2025 00:11:20 GMT  
		Size: 4.5 MB (4519848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901ecd07cdb3a04e450f180f2efdfd1eda8ff8a9c8480ea5dd3ffcefd8d782a5`  
		Last Modified: Tue, 30 Sep 2025 00:11:20 GMT  
		Size: 1.2 MB (1203274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010ae71f660ba2df2b529f783fa6a46b291ee46dbf057a1cb4ca830dd6aade46`  
		Last Modified: Tue, 30 Sep 2025 00:11:21 GMT  
		Size: 8.1 MB (8066530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1766978097e02cedd679ff72942c0dcdb73879dedd89a31301cc45fea355ed2`  
		Last Modified: Tue, 30 Sep 2025 00:11:21 GMT  
		Size: 1.1 MB (1108951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcc951fc041e488c9080470d1ee71f94b4149f9badb51b6e8d693e915ab2e9c`  
		Last Modified: Tue, 30 Sep 2025 00:11:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460d7a8671aa52a604225c94730926676806212a0eee20902486286b21788236`  
		Last Modified: Tue, 30 Sep 2025 00:11:21 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69539b74f291637567a85a402f35968a111c12f4b6d67eeb1650266e1a0e8f`  
		Last Modified: Tue, 30 Sep 2025 00:11:28 GMT  
		Size: 111.0 MB (110992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9740feb3695831963a61026f6a4e5ad61ec2f9cca2dd902fde1bcfc9607b21`  
		Last Modified: Tue, 30 Sep 2025 00:11:22 GMT  
		Size: 10.2 KB (10231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271dd60a63dd4ad800a5d3dad67c1c3619825cf440ad8ba3c1f12a9b09e5f7a6`  
		Last Modified: Tue, 30 Sep 2025 00:11:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a81b21986145a8d364e888612d1caaf6678e99c98fb180903abc290b167e294`  
		Last Modified: Tue, 30 Sep 2025 00:11:22 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815716859d1d862a1490e692e015e548f8e7347e29d0b6a407c28831092e24ca`  
		Last Modified: Tue, 30 Sep 2025 00:11:22 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ddab6ec4aee3e2be3bd27be244414c43b53373d22cc00817fd0a495a7ebf3c`  
		Last Modified: Tue, 30 Sep 2025 00:11:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f21b13e8af832f675ecb5d3b0ff323f2c7fafa6934270355fcafd1471daab858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5987345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3107712bda62784f9ba913db367abb7e337c8145ece80c8b44a83112f1ed64ab`

```dockerfile
```

-	Layers:
	-	`sha256:3e8b480d0ea96e7da2913aee52fb0c75192a8d1978a8af56f1b92feb220af6dc`  
		Last Modified: Wed, 01 Oct 2025 20:16:28 GMT  
		Size: 5.9 MB (5933767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba3eb6928520b5a0c641693c7652cb54286ebce1a142c85b6eb7c34bd104642b`  
		Last Modified: Wed, 01 Oct 2025 20:16:30 GMT  
		Size: 53.6 KB (53578 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:097fa41c0f054646ca33c39cdb999e211c6853a2e712eca9e146bf13c6df315e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164865517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c4a2bc3f1bd306794e53f0d8dc79603f1e05f657530329a57aa0dea09b9ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40919815d2d7980783eaa93d257b6625c273b20522182fdaefcf46a8ad0e3d51`  
		Last Modified: Tue, 30 Sep 2025 00:18:04 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209c100366939060b81f511fa7d5c730b61f7c03e2ca1580f2a28f0e7b7afee4`  
		Last Modified: Tue, 30 Sep 2025 00:18:04 GMT  
		Size: 5.0 MB (4965311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a683d951c04e79e16139a8110aebd9b7dc137737fc04ee0ed9f7ae2db04d9a4`  
		Last Modified: Tue, 30 Sep 2025 00:18:04 GMT  
		Size: 1.2 MB (1218584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04649eadba96c4c06f3b000cbd427c2ba3b3bb98868f8a7d1d97d8f2bea3bf34`  
		Last Modified: Tue, 30 Sep 2025 00:18:05 GMT  
		Size: 8.1 MB (8066473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a1a97bd78e775d234b41b7704a7807f32f8f368ca34dd8a32b4d3ae9a4ac6`  
		Last Modified: Tue, 30 Sep 2025 00:18:05 GMT  
		Size: 1.1 MB (1137394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0b5aa63382372d95c1d5389589cb1a805f8d024e8dea4bf4f980867b53f9d0`  
		Last Modified: Tue, 30 Sep 2025 00:18:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76dee5869dfbd6d268e06aec148028df8aa9c53d58a9a07676544358be54f64`  
		Last Modified: Tue, 30 Sep 2025 00:18:04 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afb2e29793d0fb17c63e21a05c9d28253b3a37fb751b84e283dde7a4aa7652c`  
		Last Modified: Tue, 30 Sep 2025 00:18:14 GMT  
		Size: 120.2 MB (120247066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80194e01fe73ece00e9d0e0006d956d138b346338c0e6e8a5345fef8eb275b98`  
		Last Modified: Tue, 30 Sep 2025 00:18:04 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec8f9e759a465236bf904be28c288bace1964c03ecf184b4afa66116334c109`  
		Last Modified: Tue, 30 Sep 2025 00:18:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c6d7477e61ade8f9f2f151071d6593a1108b2f1a8c03f3d4065e1b21e6af14`  
		Last Modified: Tue, 30 Sep 2025 00:18:04 GMT  
		Size: 165.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faae462035edf69e432613831aecdb7d695d5fb869413c7829a6355a2a44cb22`  
		Last Modified: Tue, 30 Sep 2025 00:18:04 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60fff22c994d90bf967683ca0423a159881c283653d511603b27752402db83`  
		Last Modified: Tue, 30 Sep 2025 00:18:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a4149960cb47e068d46c10d8b588d1b5e37541164f2349ed6f980db85520cb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5997203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0e3c0c3f75b92e6e6f58b5a8c80bcdfbfa6c9b2269d65a5e315c2b35df2296`

```dockerfile
```

-	Layers:
	-	`sha256:91a619d81a9cb6d4ab3a612b779c2a84a2cf5a576d32e6e4dd631df85017e5e7`  
		Last Modified: Wed, 01 Oct 2025 18:01:18 GMT  
		Size: 5.9 MB (5943914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11df7ae6a5908080adbbefbab8384311e6bbfe1e37f821e722d17f737b47793c`  
		Last Modified: Wed, 01 Oct 2025 18:01:19 GMT  
		Size: 53.3 KB (53289 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:7afa4844207878ab62fe2c451aab46ec76c23e25105289d58eaea9d197f08928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154877290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030989a3434392fcc52bbc2706a71e8c373e0a5e7fd99d10610a7e1aac929c29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:73d0a1261a90ced7c792643cb457a2c9f7bbeca1bcb84939b4029c5a1f01f26c`  
		Last Modified: Mon, 29 Sep 2025 23:34:06 GMT  
		Size: 28.5 MB (28513676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d10de371f209c727ac7bb012b4d1ae77293dd115df15e46d99c8906685f7bc`  
		Last Modified: Tue, 30 Sep 2025 07:49:40 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51dc08b8fefc299e23f62291a740a6503e8024a47aec51f1c8188254e5aebc3`  
		Last Modified: Tue, 30 Sep 2025 07:49:40 GMT  
		Size: 4.5 MB (4475423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925e9737c6a53c1079fbe25aeb57d7cc0d67494dd0b106a4ede817d7e356ed9`  
		Last Modified: Tue, 30 Sep 2025 07:49:41 GMT  
		Size: 1.2 MB (1159164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b0b86761fa1b99021362bcff00b5a29604b076cd885305b8255cca752933dc`  
		Last Modified: Tue, 30 Sep 2025 07:49:44 GMT  
		Size: 8.1 MB (8066690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed61a062b9af0ebd72d636f120d6e1c03bc3985a4305e169304de63b52725741`  
		Last Modified: Tue, 30 Sep 2025 07:49:41 GMT  
		Size: 1.2 MB (1182915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e467bb51148e774913eedeeed34d1fd03c9b290a8256fb6d468c0c109a1dc749`  
		Last Modified: Tue, 30 Sep 2025 07:49:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2422393ffddacc15070620014939ddee7917b45ab02de9469126b47eb5169ce`  
		Last Modified: Tue, 30 Sep 2025 07:49:41 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448ef6cb1cc80d42b3817fdac42465f77b4f7df769c50459460678cb0d30fc97`  
		Last Modified: Tue, 30 Sep 2025 16:40:03 GMT  
		Size: 111.5 MB (111458356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d567a1b17396759173891ccee4131bc3ffccc7309ef26b672ceba52f2166d199`  
		Last Modified: Tue, 30 Sep 2025 09:54:09 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6702230940f1e9c8978688f2597cef15fbdd99dcd1ec50a900516971cdeed7b`  
		Last Modified: Tue, 30 Sep 2025 09:54:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7027ce3875172dea1f1663d3de37b6e5baad538dc014ba3ea6c99a12bb92279d`  
		Last Modified: Tue, 30 Sep 2025 09:54:10 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e691c32e37fd90611950f80a184f24114dd13d24c7379b7233cbf2e60c2f4e4`  
		Last Modified: Tue, 30 Sep 2025 09:54:10 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0129264fe562cccfc103564cf1e155e942b297058334c0919a21cb245a6affdc`  
		Last Modified: Tue, 30 Sep 2025 09:54:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c75156276263d81daefc2a5f2d95838f148d300bf11b6d1d67c06350ce8d73f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27746c1c11b13cd8aebbcde546ffded545e442d9f85cd8d4ad29612128f5ede8`

```dockerfile
```

-	Layers:
	-	`sha256:95f5c316e675adb4556b568993d780ae5ec5800f0701af5edfa38054ae87f3fc`  
		Last Modified: Tue, 30 Sep 2025 17:09:13 GMT  
		Size: 53.2 KB (53199 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:da8a1fe76010ea67c499f5ad00ff7450f1c287233992fd9413aede50a837739e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168834428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a702262a3fabcbd551d52e7028e418de24df0f5c70bf29f6dd9c34fe0c13853`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b34e22ac0a8b42eb22eafbdd5e9ef44021aa9cd038797e21159ecd39f62ca2`  
		Last Modified: Tue, 30 Sep 2025 01:50:14 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438cc51fcb7698854b75c55e213dd7c754603b5aa15056df39c271e555eef637`  
		Last Modified: Tue, 30 Sep 2025 01:50:15 GMT  
		Size: 5.4 MB (5368501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1098c2fe99169d7503137a4d4eed2222cca76089d19e950df81b799a3382cf0`  
		Last Modified: Tue, 30 Sep 2025 01:50:15 GMT  
		Size: 1.2 MB (1208255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387229d007cf7cee4a9bb80422ffa80ad66bb3a11100a84a65c5784338da6d76`  
		Last Modified: Tue, 30 Sep 2025 01:50:16 GMT  
		Size: 8.1 MB (8066638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053a523ac38cb67fe0c4d13c2b98085a3bee3c6a084a1f0b1d2d524facfdb684`  
		Last Modified: Tue, 30 Sep 2025 01:50:16 GMT  
		Size: 1.3 MB (1283674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d91a3cbde68406e87007653fb55f7978dcab3c9556d371dc32e73144a0d0147`  
		Last Modified: Tue, 30 Sep 2025 01:50:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69849b33835cc7713ae86fdf120d96bdbdb3e3539e44ac31d406089d66048ed`  
		Last Modified: Tue, 30 Sep 2025 01:50:16 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48c68f9a34ea023f1a0adcbb62ae6214fd2469ad78e1c1f1d40b14d5c11f9ac`  
		Last Modified: Tue, 30 Sep 2025 01:52:41 GMT  
		Size: 120.8 MB (120817607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e186b664767d4f47a0b4ea782532251488d1b01a94ff33b997ba9eb9ec50d9`  
		Last Modified: Tue, 30 Sep 2025 01:52:27 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c4abe826b9e1b3ab69ead8033c7decf98e997239d6b90ff1245d39c46268a`  
		Last Modified: Tue, 30 Sep 2025 01:52:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551193a00e4fd6bf76eff1fc3fd279fee0658980136687ab3a9f1ddc8ef1e8f7`  
		Last Modified: Tue, 30 Sep 2025 01:52:27 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfb68d9b2fe4883d4814706582b3ec2479681dc77dbd892e69780c848553640`  
		Last Modified: Tue, 30 Sep 2025 01:52:27 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3814ef5232719ba523cb083159c3a94e5d91f9287be816603e775d426c4d9ec1`  
		Last Modified: Tue, 30 Sep 2025 01:52:27 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0d123cdf019bc4637b9bd507054ac2a55502da726ecdbee62475a8d5dfa5ee7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5988204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3628338714e3a95b70e7d3c6dd3641cbf702da6a0b6f1f4b6169ecc3979bbe`

```dockerfile
```

-	Layers:
	-	`sha256:c62a5d6b33c2970efea79f89a7d64c6ba0ad6850bbc3346205f3ef8d9705a4f0`  
		Last Modified: Wed, 01 Oct 2025 20:16:40 GMT  
		Size: 5.9 MB (5934817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24946bc1e94a7e1812438325adfbfe379c6fb013ae1189e7cd026aea54ee3280`  
		Last Modified: Wed, 01 Oct 2025 20:16:41 GMT  
		Size: 53.4 KB (53387 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:1641bb3cd7706036d7ca6ae6fc626d1970c0ff9ada048111e99ef69472ed2cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165263939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886db85338e5d5bb2aae70832cd5b47064285dfe13daa6fa473cb492410e5ebc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 25 Sep 2025 18:02:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV LANG=en_US.utf8
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_MAJOR=17
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PG_VERSION=17.6-2.pgdg12+1
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 25 Sep 2025 18:02:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 25 Sep 2025 18:02:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 25 Sep 2025 18:02:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Sep 2025 18:02:43 GMT
STOPSIGNAL SIGINT
# Thu, 25 Sep 2025 18:02:43 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 25 Sep 2025 18:02:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d48d314d4c4ad33b7f3f8a91af0de4fa9191497ad35b65135e22f849c79fa77`  
		Last Modified: Tue, 30 Sep 2025 01:43:08 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cb5cf9730db1f8d0432592e9a0487585578c243c8ff054591077265b20cd4a`  
		Last Modified: Tue, 30 Sep 2025 01:43:09 GMT  
		Size: 4.4 MB (4391259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e57ed66ef6a49004560c81c56ba2b027f0ad72448adfc8b3f5af5a1ee44bb6`  
		Last Modified: Tue, 30 Sep 2025 01:43:08 GMT  
		Size: 1.2 MB (1222771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eec6d347aebf4ee1aa4431a08de8e9841df88ad708ebf73e585f17cc918d063`  
		Last Modified: Tue, 30 Sep 2025 01:43:09 GMT  
		Size: 8.1 MB (8120694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00f9087bc347a60749002ae1cb46d8d3ea80bb9a074463d729761d05078feef`  
		Last Modified: Tue, 30 Sep 2025 01:43:08 GMT  
		Size: 1.1 MB (1097018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b8c872ec929275fa054b1dbf9fb365de67171baa61027cbb54b430a969045`  
		Last Modified: Tue, 30 Sep 2025 01:43:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a521c4a60db5584ce5b77818beb26a1c3f38ac85c51bbc911ab57d2c7af7c763`  
		Last Modified: Tue, 30 Sep 2025 01:43:13 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c5014961d3d289cb111db5015608aa99072c816e413f5dbda9bd821c92a40e`  
		Last Modified: Tue, 30 Sep 2025 01:57:15 GMT  
		Size: 123.5 MB (123526815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acdbb64fc779f2c14e5c131dcd7c19d821e544ee7d02a94a7190ac1b1525b0c`  
		Last Modified: Tue, 30 Sep 2025 01:57:05 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a79a806268b9164339944e5930811b732ae909026aaf563ed9a7f1bf3ea68`  
		Last Modified: Tue, 30 Sep 2025 01:57:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661c401a3009294e71f1536bcd629951e8dfcf011778264b2cfd1dc811d0a8fd`  
		Last Modified: Tue, 30 Sep 2025 01:57:05 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e59f671f3136adf7da5a589d05ef26099500cd16f47d99a64ac63d0bda8791`  
		Last Modified: Tue, 30 Sep 2025 01:57:05 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07341c5e9afb80c591f4fa2ce5e7a8b9fe0dc4d5b8a09b954eca9ff30fa6ddf3`  
		Last Modified: Tue, 30 Sep 2025 01:57:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:194c87ae649c0b2f504a43de98d00276cf03d6b59942a5fb5809103263b830da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5993723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68904d7ac4c526de5e845c39d57eb212583728ef84f05a1e869ec174f057f9bb`

```dockerfile
```

-	Layers:
	-	`sha256:9a5b480fcb295c6cc43e92fa1f8133db8f0cdd3854bee368f04597b89721a129`  
		Last Modified: Wed, 01 Oct 2025 20:16:46 GMT  
		Size: 5.9 MB (5940390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8597f978a5cce1075d9edc74ee96d48d7e04c54d4551e0314b2905f3aa6653e`  
		Last Modified: Wed, 01 Oct 2025 20:16:47 GMT  
		Size: 53.3 KB (53333 bytes)  
		MIME: application/vnd.in-toto+json
