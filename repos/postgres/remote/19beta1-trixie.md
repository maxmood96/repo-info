## `postgres:19beta1-trixie`

```console
$ docker pull postgres@sha256:8dc46b8d121a9ecdb1324243799066bf24cff3edff2d73537607150d03d84fd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; 386
	-	unknown; unknown

### `postgres:19beta1-trixie` - linux; 386

```console
$ docker pull postgres@sha256:3c40b28459d0b7369e16b374551798852c5a086e1ec113cd544e57d5b22e776d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98190422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71ca6f72b69f7f52bac8991185d599be9807737cf9d310213f373024688cf9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Sat, 06 Jun 2026 00:21:19 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 06 Jun 2026 00:21:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:21:33 GMT
ENV GOSU_VERSION=1.19
# Sat, 06 Jun 2026 00:21:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 06 Jun 2026 00:21:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 06 Jun 2026 00:21:38 GMT
ENV LANG=en_US.utf8
# Sat, 06 Jun 2026 00:21:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Jun 2026 00:21:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 06 Jun 2026 00:21:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 06 Jun 2026 00:21:43 GMT
ENV PG_MAJOR=19
# Sat, 06 Jun 2026 00:21:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/19/bin
# Sat, 06 Jun 2026 00:21:43 GMT
ENV PG_VERSION=19~beta1-1.pgdg13+1
# Sat, 06 Jun 2026 00:30:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 06 Jun 2026 00:30:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 06 Jun 2026 00:30:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 06 Jun 2026 00:30:43 GMT
ENV PGDATA=/var/lib/postgresql/19/docker
# Sat, 06 Jun 2026 00:30:43 GMT
VOLUME [/var/lib/postgresql]
# Sat, 06 Jun 2026 00:30:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:30:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 06 Jun 2026 00:30:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Jun 2026 00:30:43 GMT
STOPSIGNAL SIGINT
# Sat, 06 Jun 2026 00:30:43 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 06 Jun 2026 00:30:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0225f82e2ea3120f738e4ed6236e5ddd1283822aa66cbd247554f1dc55a2ae14`  
		Last Modified: Sat, 06 Jun 2026 00:30:55 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f91751e54447505807d97fc8cb885ee44c3f770bc2c1abfd91d7453dc8cdd4`  
		Last Modified: Sat, 06 Jun 2026 00:30:55 GMT  
		Size: 6.6 MB (6631420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b821d71afabd98a9293fd0e5e7c4fca462336b3afbbe81bdcbc7902601c0e675`  
		Last Modified: Sat, 06 Jun 2026 00:30:55 GMT  
		Size: 1.2 MB (1225844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788c8bed497606f9b9e3042774c52e9aedb442619f5f2b5d23e814f616f8491e`  
		Last Modified: Sat, 06 Jun 2026 00:30:55 GMT  
		Size: 8.2 MB (8204066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915786cded0b9b407510c654a1d39521757bf676e9ad6bc85a85c0e0e5e92bd0`  
		Last Modified: Sat, 06 Jun 2026 00:30:56 GMT  
		Size: 1.3 MB (1308267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fcd58506afabdc16e2892f81b7a8b903b65036393d6acf7b35de1ef8a0801c`  
		Last Modified: Sat, 06 Jun 2026 00:30:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7819efe573f1427e02b6d7f5f29f26e520fd63854dafb3379196f100d745d307`  
		Last Modified: Sat, 06 Jun 2026 00:30:57 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28df6ee32dfa481179a16176cf6c8606a247e5f53e6d4e1800e6fa7771c7a4df`  
		Last Modified: Sat, 06 Jun 2026 00:30:58 GMT  
		Size: 49.5 MB (49493228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc3129af57f4811f5db35cb47076edffc1adeb8b4730d459b696c8990025a82`  
		Last Modified: Sat, 06 Jun 2026 00:30:58 GMT  
		Size: 21.4 KB (21421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ffd43e9d42b10d57cf220e9b7f8aa72ebbfbca078787e080dea5740bf9d5bd`  
		Last Modified: Sat, 06 Jun 2026 00:30:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9b7071e979552a126c2ebd1f9d30f736586a803f5e2464496c889698044c65`  
		Last Modified: Sat, 06 Jun 2026 00:30:58 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513b2f2837a38124912a9be3f8a484a1c9cecc73a6d6d91e368ebc0f68c9d3ac`  
		Last Modified: Sat, 06 Jun 2026 00:30:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:19beta1-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:fbc66e28c3a55897da1f12aeaf9e2353c6c2f3833128caac0689d481eb08baa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5174751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6e5581aba28b2a9138a4a28acf0e8e2835ac7876c498619fdaac93383cffca`

```dockerfile
```

-	Layers:
	-	`sha256:596a647460f01200e3dc272f6e66d3a02dbc809983ded845b9327ccb694566df`  
		Last Modified: Sat, 06 Jun 2026 00:30:55 GMT  
		Size: 5.1 MB (5123514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae4de285aa40ee5db93366311ef439d6aef26e7d6a18a4b73219fb2b06acabd8`  
		Last Modified: Sat, 06 Jun 2026 00:30:55 GMT  
		Size: 51.2 KB (51237 bytes)  
		MIME: application/vnd.in-toto+json
