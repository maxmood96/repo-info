## `postgres:17beta1-bullseye`

```console
$ docker pull postgres@sha256:65ab0e3e31e29013ee4e70fd9dd14e0f34231ed1175349896cb513541479be06
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

### `postgres:17beta1-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:42c284a9389775fed8e49f5f270e9d6d4118b5111a68779199e0a00c9d5cca00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145990378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8a260af06ef1a0c92fabfb2423f43a9fc490cf02f0532ae6738ba7b9317d50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Wed, 29 May 2024 21:09:26 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg110+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54d2a2cf71f009e674fc9f235f9869a68b16945890052d900b4c29688429808`  
		Last Modified: Thu, 13 Jun 2024 18:22:50 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b20d5353a9cf36c15f5efccbea538334c4f9d09dec62657f758d83fdccd697`  
		Last Modified: Thu, 13 Jun 2024 18:22:50 GMT  
		Size: 4.3 MB (4308187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265fdc05f1d4648e0164f548c6086c820f04534e73b97c76c5bc7b740db0e953`  
		Last Modified: Thu, 13 Jun 2024 18:22:50 GMT  
		Size: 1.5 MB (1473544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845f3157eee04b5967b567278221fd219004394e7bd7e667c7f4471e447c10b6`  
		Last Modified: Thu, 13 Jun 2024 18:22:50 GMT  
		Size: 8.0 MB (8045853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07113c728616cf2dc65366ad59fbbd7de8288ef9dee7f2f50838fd23cdb21056`  
		Last Modified: Thu, 13 Jun 2024 18:22:51 GMT  
		Size: 1.0 MB (1038384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fbfd146ecf9d2c201f30f24dd0fafacd77034aa3a865fa08cf6baa9d829268`  
		Last Modified: Thu, 13 Jun 2024 18:22:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd0df1a308841ade780e3b8ae51d6f0a6b981ff72f4fdacd4678a75c70f255b`  
		Last Modified: Thu, 13 Jun 2024 18:22:51 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a065c4d6e491ffa8ed4b619e8e4d593761ba21af566c9aaa4d901b74a4bc7c`  
		Last Modified: Thu, 13 Jun 2024 18:22:52 GMT  
		Size: 99.7 MB (99669290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fe2043e9b298250711a97efeb1a01de16260fc7337f8456788d9d4a3dd915d`  
		Last Modified: Thu, 13 Jun 2024 18:22:52 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba1cb86d8e3572d68452b54a3485a3f78dd3f1d24ddb8eb84b141770a6e66bb`  
		Last Modified: Thu, 13 Jun 2024 18:22:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00785b37e6d6135294cc4598252772e25e21e7bd9794f611b54193e2c6e868b0`  
		Last Modified: Thu, 13 Jun 2024 18:22:52 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28f42b7fb9376ee8135de208a1d97534b3439e4a00d35e9113908ec89733858`  
		Last Modified: Thu, 13 Jun 2024 18:22:52 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a606ff2b695e92c22ec30fd7a2f00dce614fe4a90ff672179db84bd1f69e88`  
		Last Modified: Thu, 13 Jun 2024 18:22:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:df81bbb63b2ce01acf28328de3105e46b3b79206952691b563152c1e090c0cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6028435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9754cfb22b3aad76efd7d9a3b13eaa9849a2d9a42871d62462fb415a2104ba`

```dockerfile
```

-	Layers:
	-	`sha256:b2fbcc6f44356e137ade528c461682872ad398b6e1cc8d5de570fd56b0adcffe`  
		Last Modified: Thu, 13 Jun 2024 18:22:50 GMT  
		Size: 6.0 MB (5974795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a222eba6e809065d14e1de15eea02e129c8824b219b8fad69c2e49eb4d81700`  
		Last Modified: Thu, 13 Jun 2024 18:22:50 GMT  
		Size: 53.6 KB (53640 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:4cbe437829d439ef51d6fb7a1f7d05b1a20f7e97128ad3b4fe8e8fb9c73f54b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138927898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f82b715733fdf0dd4900eeb3eea63548dd162ade6664a24044b976a595b6b40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:78cff0ed53bbaaa1d7680e733d50b8fc9042e257b78718ad822f9ac57a5d1dbb in / 
# Wed, 29 May 2024 21:09:26 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg110+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8a34d14f57d3fcf2d97b9fc0fb4439a2d00afe9411fdc788629eb4074186288`  
		Last Modified: Thu, 13 Jun 2024 00:52:21 GMT  
		Size: 28.9 MB (28936731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91482f2667a2ee602bcd9d22d841f2d1f93424a77a4d9cdbeec791b23ab9a44b`  
		Last Modified: Thu, 13 Jun 2024 20:44:41 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9443af51938bde9947f82821150bf5b7e65c18e451a8f17f5d56fad380f5424c`  
		Last Modified: Thu, 13 Jun 2024 20:44:41 GMT  
		Size: 4.0 MB (3991632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f459cb1eb2ff5cf8f49c1c12823aa250b7dc2a6dd575e0b753bdd54df660d3`  
		Last Modified: Thu, 13 Jun 2024 20:44:41 GMT  
		Size: 1.5 MB (1450639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c64a0172ff1ae12ed668caad303acdecc56642efa735304656265a7776964b1`  
		Last Modified: Thu, 13 Jun 2024 20:44:41 GMT  
		Size: 8.0 MB (8045741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7d510a7ee2896503cadca5ed4a55fe4b8cf6ef1be243df775bc4c91b5e580b`  
		Last Modified: Thu, 13 Jun 2024 20:44:42 GMT  
		Size: 1.0 MB (1034849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88332254e20d49fd6cd4fb1b02c7b586bf8d5fc7048dc9e4a225e7dbfc390d80`  
		Last Modified: Thu, 13 Jun 2024 20:44:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ed0cce26b2b70175dc92d13db4bac90e88d571e509156ecec8b42dd41d8574`  
		Last Modified: Thu, 13 Jun 2024 20:44:42 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c955d84b3c4912485fb5999742661b75b12de1e197d63ead4db11955d27f35f3`  
		Last Modified: Thu, 13 Jun 2024 20:44:45 GMT  
		Size: 95.4 MB (95447228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58908c5153eaa15de87ce9b2a6a64427578ec7e9b9624f926b1f7f2b2183b75`  
		Last Modified: Thu, 13 Jun 2024 20:44:43 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32b075ab068890d4c9ec7c2ac2fe6f95a2f764eee9814c28b23b0d340846855`  
		Last Modified: Thu, 13 Jun 2024 20:44:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c43a5773231f38c46fd48299fe39a3430e05f412dde9848382634ec1a1689c`  
		Last Modified: Thu, 13 Jun 2024 20:44:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b3758f0814cc2c6bad0da496d3873929170ff2b1fb6d7371c7ad0b92659de3`  
		Last Modified: Thu, 13 Jun 2024 20:44:44 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44b9e3458d551c7b3045e94a87278d0c990ae6f730194047135074bfe6e280f`  
		Last Modified: Thu, 13 Jun 2024 20:44:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:f7fcc506feb766e1405d3da9c8ae3c6e7d6b84d697d5a027f1fac02f3eba32b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6045716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a63e5b10d72a35f611884aba1650a72acaf3a747917eacd8c05296c11180fd`

```dockerfile
```

-	Layers:
	-	`sha256:1bad7adeecbe24e9bf16fc22ca970ccae7cb7dd0d5d6c830210ebbac061e6b62`  
		Last Modified: Thu, 13 Jun 2024 20:44:41 GMT  
		Size: 6.0 MB (5991887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:027bec9a549925fdf83ec48cbc78cc8d9f718b4b8ecd67256b36843941d3a780`  
		Last Modified: Thu, 13 Jun 2024 20:44:40 GMT  
		Size: 53.8 KB (53829 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:115ce977ea68bd238b40d231f748c55bc3c005f3243bbd13cec6af30534f80c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133989234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e634883d19dac70994c6b817b45c87b73a6b0112342928250f19fc71cc209412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg110+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a41508a4c90bd170cd5a43afb2489f3abfc2f84ec7c878ed68a79875b07332`  
		Last Modified: Mon, 03 Jun 2024 20:34:46 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbcba39f51046a9f0fff6e32123147275ab3b59f89d77839a6d03f2d833e1990`  
		Last Modified: Mon, 03 Jun 2024 20:34:46 GMT  
		Size: 3.6 MB (3601679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d51a219ade94db6a0980da5625f83efb93330f12025c53599374ebc1b9451df`  
		Last Modified: Mon, 03 Jun 2024 20:34:46 GMT  
		Size: 1.4 MB (1440831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d851ad9209fe7b37127f671da623bba97f26483d68d5f591ca16e8c5ce80fd`  
		Last Modified: Mon, 03 Jun 2024 20:34:46 GMT  
		Size: 8.0 MB (8045816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7b510de9a242d667027ad599fb44a46db93e2d2f2eaa010339c7ba60de54d2`  
		Last Modified: Mon, 03 Jun 2024 20:34:47 GMT  
		Size: 908.7 KB (908667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615e01ffc57b03b7b1616d1b029eeeed995ebc1dbd7edcf2eee909086839ed7a`  
		Last Modified: Mon, 03 Jun 2024 20:34:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fa74912a0e06a92ba2a0e0d0422137c7ecb971158c53ef3b244faf450b29c7`  
		Last Modified: Mon, 03 Jun 2024 20:34:47 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a6feb4deaf235dd27189dbfc8ac0dbe82d0dad9e15fcc064746ce4a1effb57`  
		Last Modified: Mon, 03 Jun 2024 20:34:50 GMT  
		Size: 93.4 MB (93376669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa7da59ff0bb921181fa1ca58a6f8a3d80d66a73c16e9a18180a31184429573`  
		Last Modified: Mon, 03 Jun 2024 20:34:48 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5fab779b974d2e4c21e589afc9485577a0de8e860dc139ca0887ac06c1e18e`  
		Last Modified: Mon, 03 Jun 2024 20:34:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8902cb313e558f0e45b5b8c9bc8c29b4578b4f91f5064867d0afbc80fd95c7c1`  
		Last Modified: Mon, 03 Jun 2024 20:34:48 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96dc7d0ea37b1ae5428e25ce56a99364704fbe337bf1d5848481debda911226`  
		Last Modified: Mon, 03 Jun 2024 20:34:49 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae4a5d1896f4306386f9f92e536d12ce0be6f7556afe594c1eaa9d6563bc75`  
		Last Modified: Mon, 03 Jun 2024 20:34:49 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:be3fb4514ab22def225fe2ca7581e262b20b9416d5f286e53739f739a3295e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6045430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31df91875437310e27f37819fa47e7b2430cff8b80592e0992ad9d9fcfd38a7c`

```dockerfile
```

-	Layers:
	-	`sha256:966774cce52895fcfed2eb4041edb07af943df9bf735c9b0db6465701e31ff35`  
		Last Modified: Mon, 03 Jun 2024 20:34:46 GMT  
		Size: 6.0 MB (5991659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b2de7dc6d476bba82ec02dfc995ab5b0695ecc7aca0c651fc63bc2f04526da`  
		Last Modified: Mon, 03 Jun 2024 20:34:46 GMT  
		Size: 53.8 KB (53771 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d1d68e5fce07e70d9c92b2117666c3f0b0f7342c6e0bd3fc728c08b27d2a33fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142383261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ccf66e7dc994fbacdf36da9d084ae697a9e3cd134741b9718ff84061e01cc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg110+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543e44e79790fb04549a75aa82af49cfcc065a38ceeedd6c53e831cd527a7cfd`  
		Last Modified: Tue, 04 Jun 2024 16:40:28 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca65b4b46fe005a3d657456295d010eec7b4fc90e91144899b1aa984eb3dd03`  
		Last Modified: Tue, 04 Jun 2024 16:40:28 GMT  
		Size: 4.3 MB (4312721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d21702531bcf491f2941a28ba04e77439a410d4cbd106babaaef8a2f172329`  
		Last Modified: Tue, 04 Jun 2024 16:40:28 GMT  
		Size: 1.4 MB (1405870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a703354a89b94ea0f127ed67b525f180bfc86a3b64eb2a0236ecf8deb8b4063`  
		Last Modified: Tue, 04 Jun 2024 16:40:29 GMT  
		Size: 8.0 MB (8045752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c742d98ba82367d43a1da72061a549c5ae4ba27e59f4a4cf571d6900cff4ac`  
		Last Modified: Tue, 04 Jun 2024 16:40:29 GMT  
		Size: 1.0 MB (1026610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc994b0d1e1b85ad538a73d8d35c0b0cc82fdd3d47f9776f0b2cf8f77386db6`  
		Last Modified: Tue, 04 Jun 2024 16:40:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8666dbd3b533e40da7cef6f9424460874d0acc98238f35c5519d53d536e39509`  
		Last Modified: Tue, 04 Jun 2024 16:40:30 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44648c00be879f564aa90b01fb2829b10e040ee70cb0314c1e2ccf0ca68dd414`  
		Last Modified: Tue, 04 Jun 2024 16:40:33 GMT  
		Size: 97.5 MB (97484318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c50e1c934333740f75c59b8e53cad0d39e95b8a6e9d27b29028e75c2202244`  
		Last Modified: Tue, 04 Jun 2024 16:40:30 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cc78bd2c74fd7d61807dcf0137fc7f62486fa787c3f2394e757e504b99fd57`  
		Last Modified: Tue, 04 Jun 2024 16:40:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff88cee81f38f21c6a3c3fc48b8a599cd573323a4c478ed05b5d851ee424ca16`  
		Last Modified: Tue, 04 Jun 2024 16:40:31 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e8fdfcc0954ef835a339d69c950cbc3b0b85f708325917d6da9d719c58b9c3`  
		Last Modified: Tue, 04 Jun 2024 16:40:31 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19112adb7e0c01ecb9a56154536cd829466223f59027d9c48b350bacc6b2503`  
		Last Modified: Tue, 04 Jun 2024 16:40:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:132a53a3073f9d48904706a9e601b923d1dae1656f3911440c5976cc48cc65a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e409ff6b6ed814ff9b475be00d4f71b43c8b26118d6d37eaaec569ecedf97171`

```dockerfile
```

-	Layers:
	-	`sha256:26454e1edf4d350bd8553cf688d1d736262a46fdd2df9f3da6a11125e692d531`  
		Last Modified: Tue, 04 Jun 2024 16:40:28 GMT  
		Size: 6.0 MB (5981073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:122efd8d786d8aff0ce7063f470bd7206776fc00e549469ed362070430d2bca6`  
		Last Modified: Tue, 04 Jun 2024 16:40:28 GMT  
		Size: 53.9 KB (53864 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:4374e78429d5da88a6e9d640d369abdc50bca3ffc9da910619dfeaa9a0ef5436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148775324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184eb138a2c1882b4977222bc5a58671c79e0cfed2aee51e64f227833b4a1caf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:ef80ad838dee1f170442a02f8d0808e624e7c317df766c49aec042c1f3ac4732 in / 
# Wed, 29 May 2024 21:09:26 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg110+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:71e749b27156c50e0706f9267afd1ca9fb38d6272a353964948602fb62336fd8`  
		Last Modified: Thu, 13 Jun 2024 00:44:08 GMT  
		Size: 32.4 MB (32424179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04652b9706f83fd508bcc7b97584f50f7267aad1f237de4e0f5985085b4d5796`  
		Last Modified: Thu, 13 Jun 2024 02:21:54 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c8b4c65a530efb892365cf596f12600691320822f3f4ec9c0caa7b1112dc0c`  
		Last Modified: Thu, 13 Jun 2024 02:21:55 GMT  
		Size: 4.7 MB (4719612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d67022e5f3d2d7cfabac117faf1e0626f1fb2f9351c756fcd776c2d274646`  
		Last Modified: Thu, 13 Jun 2024 02:21:55 GMT  
		Size: 1.4 MB (1449311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e357a415a2b7a5111fe5a1092850178b0e7bb8ead8e2ca22fcff0653ed21ce1`  
		Last Modified: Thu, 13 Jun 2024 02:21:55 GMT  
		Size: 8.0 MB (8045594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984684b56ac708e634b3394532631cbc997680905c36cd44018a26dcaecb3e18`  
		Last Modified: Thu, 13 Jun 2024 02:21:56 GMT  
		Size: 1.0 MB (1028932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d348cfa030a87c00db22d31d2048c63f8a8ae618603e36bf7b40f768472afe8c`  
		Last Modified: Thu, 13 Jun 2024 02:21:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20475dd88c70f7cd0c33d980c5949f87d6b7102bfda69504e6dbc1954412284`  
		Last Modified: Thu, 13 Jun 2024 02:21:56 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd3db23f9eb647d5c08294f998e3927fca54c7e57164c44faa621711931fadf`  
		Last Modified: Thu, 13 Jun 2024 02:21:59 GMT  
		Size: 101.1 MB (101086616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08a8920106646a2ec5bc8ca4ac715276015a56e35ee071c8d1b860863dd1d66`  
		Last Modified: Thu, 13 Jun 2024 02:21:57 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698a2012948df48fc11406f976ae6dfe70519fcb6e356166a45bb63161f9bc18`  
		Last Modified: Thu, 13 Jun 2024 02:21:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b42a0772fb9c0e17ada5da8123fd825020e4bedf0da3868ad61404b02761929`  
		Last Modified: Thu, 13 Jun 2024 02:21:57 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d16873be11054df9f2c85160ec2320468e78ec440c8ccee0b47b09356cf8c30`  
		Last Modified: Thu, 13 Jun 2024 02:21:58 GMT  
		Size: 5.4 KB (5426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc8914e6ef0ebbbc5add10f6f440a992b5186f06d857a38fb0d38c2829bccb2`  
		Last Modified: Thu, 13 Jun 2024 02:21:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:ba7c9b88863bfde33453d0a048c1c467faf9a4eaa783dd66714a71afed92d884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6042830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f8b2257f237b46a9bcf1b58adcb920a4000316e66a47dca57d94d30faf3e5a`

```dockerfile
```

-	Layers:
	-	`sha256:5a25ba4e90ef5aafd366d7dc27bc41c816261b9593176384a44574ceaebcb9e0`  
		Last Modified: Thu, 13 Jun 2024 02:21:55 GMT  
		Size: 6.0 MB (5989220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dc9e401a3bd69061d73c39460a343dee05ae45c8d3d5c36eeff04627f4adc58`  
		Last Modified: Thu, 13 Jun 2024 02:21:54 GMT  
		Size: 53.6 KB (53610 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:7dda828dd845a040f415da86af433d1a25f1fa795228982b429b98336d492712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140322186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4effa525e4748e1c9df8439b1d978d2a88bc4da519cf3daf6b171cbab2ca870`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 14 May 2024 01:12:23 GMT
ADD file:ec3acf4bc32b149c2b67d1b2c5f3a6d1f16fbae266ac16c115e1fca276b970e7 in / 
# Tue, 14 May 2024 01:12:27 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg110+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:38917083d8284ce1ec7533351600bab5d64f8295f3edc5dc651be130fb9a4bd4`  
		Last Modified: Tue, 14 May 2024 01:23:44 GMT  
		Size: 29.7 MB (29651870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904aeea7661c761dd5ab9e4df1c8b0adbe6b0837f6831da8517979c3bca05431`  
		Last Modified: Mon, 03 Jun 2024 22:30:10 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c01d47d7e2e148404f64816ebe87484ac5b7882530ba00d7799778ac2cbdaf3`  
		Last Modified: Mon, 03 Jun 2024 22:30:11 GMT  
		Size: 4.3 MB (4308282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d10d1f95efda91aa9e6946398cb92015553eacd0aab084d2040608be5384cb`  
		Last Modified: Mon, 03 Jun 2024 22:30:11 GMT  
		Size: 1.4 MB (1360863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aa368671acf016b53e02a5e829e1454c08ed903e842f8f2e53a9136c1723af`  
		Last Modified: Mon, 03 Jun 2024 22:30:12 GMT  
		Size: 8.0 MB (8046083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaef9f066f379b73f9b565b7553e622a2039c298ba08d069339aaf7b9f11ca3`  
		Last Modified: Mon, 03 Jun 2024 22:30:12 GMT  
		Size: 1.1 MB (1090251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15a9b7162616adbf9789a807ef33d0f411e5c559b877e97fc4e96f4f2ad0ed0`  
		Last Modified: Mon, 03 Jun 2024 22:30:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569c51a7363a47ead92b67749b1b2060058c13c28f3824c4ad27cff94faa11fd`  
		Last Modified: Mon, 03 Jun 2024 22:30:12 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d60c12d4b620521c73553d542fcf86206c3b134a9ed0bd69c7c644f926e57a`  
		Last Modified: Mon, 03 Jun 2024 22:30:22 GMT  
		Size: 95.8 MB (95843736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a61ea05afe70dda13df4a42741e288575d3e35263dd251c2e20295210b69bd`  
		Last Modified: Mon, 03 Jun 2024 22:30:13 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f482ba4efbd253d4611e7dc47085a43ac1f0c68ae8dcec27027772288148f3`  
		Last Modified: Mon, 03 Jun 2024 22:30:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0643691dee8af2e391d106ab3657fea3c07404611b49ed2398bddd3c7a08ad`  
		Last Modified: Mon, 03 Jun 2024 22:30:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662f505c360773ae55de5f53f52d0cc0a047ad8f26f1d24ac71ac9cf8d280fca`  
		Last Modified: Mon, 03 Jun 2024 22:30:14 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961c41ef6c3ea4a4251133c7895bf78acd5c104f7a7c193f0c7b87060d05e824`  
		Last Modified: Mon, 03 Jun 2024 22:30:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:97134d1eb3813f4a466be42d49195030e2d2cb68518988dcd811ff5b36c10d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 KB (53433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dca44586e97abbfbdb01d46887ae68154eb8f6d3036c2c79c731d20603849f`

```dockerfile
```

-	Layers:
	-	`sha256:9ec561b71d658a828cccdfc14e902e53d8ac013ae6ea304a0639db4b3c76b5fb`  
		Last Modified: Mon, 03 Jun 2024 22:30:10 GMT  
		Size: 53.4 KB (53433 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:a5c4f8e5ffb475bb805f1ded258b3d251a74c77afc83aebe72fe52fa302f5a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157030242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ca02f50dde3d7718b980c5b19d46bf2b19e22030bd174dccf489ae15cb9a8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg110+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3723c65e528c4b0d40e9f13675a6bb2cbc5b94b816621101011567fbe61c47a1`  
		Last Modified: Tue, 04 Jun 2024 00:12:48 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644f89e7f67dec5ee07877fc202e745dc7b709ff6a6e2917e50159296fbf2500`  
		Last Modified: Tue, 04 Jun 2024 00:12:48 GMT  
		Size: 5.1 MB (5137812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e3b99de64917bb3f4a0b6f9d5a7126c072c59108dfcef3b6c256f586878a4e`  
		Last Modified: Tue, 04 Jun 2024 00:12:48 GMT  
		Size: 1.4 MB (1394861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645ad7d0ec9546d8e48e81bb7d88eea13bf9ef615916fab75217b091cd09824`  
		Last Modified: Tue, 04 Jun 2024 00:12:49 GMT  
		Size: 8.0 MB (8045860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d89011d11515b4f7347f10f6b44dd80f9baa9d4e8b421f92560d106fb9d6ba`  
		Last Modified: Tue, 04 Jun 2024 00:12:49 GMT  
		Size: 1.2 MB (1197535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64428183015d0c4883aa8c70d1c37279f81267f18896e263a058f4e1699ce9f`  
		Last Modified: Tue, 04 Jun 2024 00:12:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cd9e37a08d413aac718b4256e1f0119fed5dd74188753996aed50af97d12b2`  
		Last Modified: Tue, 04 Jun 2024 00:12:50 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaacb99d38e2f3f5ddc4ba13c6b797e4b0fddf026fe8a137336b1579804e1963`  
		Last Modified: Tue, 04 Jun 2024 00:12:54 GMT  
		Size: 105.9 MB (105921932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9245e7c301f36f170ef1977cb48cf66336cde9bbff24454259243808dee93bbb`  
		Last Modified: Tue, 04 Jun 2024 00:12:51 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffbbdfc0eaf8cf67b33f331b977f8e8287ff584eda73bdc71f2ae7766f01454`  
		Last Modified: Tue, 04 Jun 2024 00:12:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da80c2c863cd054a83cf00a94f4e27eec337bf1904ccbf5e0c841a5fa76e951`  
		Last Modified: Tue, 04 Jun 2024 00:12:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea4665e4e218be1099c77fc142d70feff2c9d96c0ef703bf8475de7087cfb29`  
		Last Modified: Tue, 04 Jun 2024 00:12:52 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83a8c40bcd2fac50d764a04a2419394d9fd908ca98b136ccfd2dd7aa7c99e8c`  
		Last Modified: Tue, 04 Jun 2024 00:12:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:07cf6ec38ffb15f5be39420ca9d13daf6356f3e152ba5283dc575765c4b73952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906c564ed158d389239d95850bc8ae7d1b103d88b97695815319b824ae71223d`

```dockerfile
```

-	Layers:
	-	`sha256:cdc2f144d0b3be00b12f9eb3809c9d9159ac324347df0881b87323dac30b9579`  
		Last Modified: Tue, 04 Jun 2024 00:12:49 GMT  
		Size: 6.0 MB (5981921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f79994f65d95b35597cbb350ef16ae2e9caf196d8e247909725a2ff2578f9d1`  
		Last Modified: Tue, 04 Jun 2024 00:12:48 GMT  
		Size: 53.6 KB (53639 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:45381f85c98ea9bd469bebe29a9228aeecb12b58ed4c312264f885f50046d6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150381596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ae0d6fdfe2f4e854f0527a9c96a5692b010313281229a827f83c782155034a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:dbc45f2c1dc4ae2fcf0e05b8c9401406afd0f7aa3623659e470bb7d0fb97f9ec in / 
# Wed, 29 May 2024 21:09:26 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg110+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b9966e11fe1c4138e9aa4f0356568463c21e36009b72062413bb596e0e57738f`  
		Last Modified: Thu, 13 Jun 2024 00:48:17 GMT  
		Size: 29.7 MB (29673762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c230adaace3949645878940d610c4ce38c0e447f048b02217e91eb050fec3`  
		Last Modified: Thu, 13 Jun 2024 12:23:54 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bac93d97a40e00dd3390048e4d534c3ab50ffd81ef933870410b6e8dc4ec471`  
		Last Modified: Thu, 13 Jun 2024 12:23:55 GMT  
		Size: 4.2 MB (4200281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0793852fc1f76326929ea80fc34bdd2d26d7ef7d25089b639170768d4e00b42b`  
		Last Modified: Thu, 13 Jun 2024 12:23:57 GMT  
		Size: 1.4 MB (1439447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408bdc779fb25812e76e6855bdc1e12f5b966080f5c04c1d824ceabb23c6cc80`  
		Last Modified: Thu, 13 Jun 2024 12:23:55 GMT  
		Size: 8.1 MB (8099613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419d494d4895e7ea22af6a94b4ed70469bdde216801d7d02da6df9cf27db64a7`  
		Last Modified: Thu, 13 Jun 2024 12:23:55 GMT  
		Size: 1.0 MB (1015255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca5e5eca589d99e7509c8665b60a932cbfd1c44dc4561551a29284bce702b63`  
		Last Modified: Thu, 13 Jun 2024 12:23:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65306f81e991db54de503312aa99f227234fc3f95f0fb208d6b7e9e6175c49f`  
		Last Modified: Thu, 13 Jun 2024 12:23:56 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdb5047da1971b8f6a1dddd184b8b5caf99c13c39f31228f70650e437010a19`  
		Last Modified: Thu, 13 Jun 2024 12:23:58 GMT  
		Size: 105.9 MB (105932148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dde67c9552fc0964e03922dc4b5260e858b231c5b0c8407a38b64ca15c8a757`  
		Last Modified: Thu, 13 Jun 2024 12:23:56 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379f54e512ecd4149aaf4e6d60f70dbd9b20a8e81f056dfdb46f6ca5725839fe`  
		Last Modified: Thu, 13 Jun 2024 12:23:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e042ba3b4e85c567cc30d7e35f29612f1d270057241981ef8a269577912a574`  
		Last Modified: Thu, 13 Jun 2024 12:23:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c79aeda4de88bd30d814db806bb8092cdd5d3b1fc1b240c310c50026ba3e859`  
		Last Modified: Thu, 13 Jun 2024 12:23:57 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fe224ba6d7c06885e727ce9a5cf8f72f733001ba31df3a26892825573c5b9a`  
		Last Modified: Thu, 13 Jun 2024 12:23:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:641a73d8e1ff4f7e618ab9eb9ead53d5fab2892014d57d7134d41c5e16e7f50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6027418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4847a1c889b355f8972e3cb88db7e7245b1700f6ab50cf1b68bb247c142feda`

```dockerfile
```

-	Layers:
	-	`sha256:9dfe45dfbe284c00e3502afb9dca083bfb3bca3c7f49886bb4dc92123b559e05`  
		Last Modified: Thu, 13 Jun 2024 12:23:55 GMT  
		Size: 6.0 MB (5973772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa2daa8ac03405a2dc4a5ec2486a3394ff9730091549a4414e118a9848113a5b`  
		Last Modified: Thu, 13 Jun 2024 12:23:54 GMT  
		Size: 53.6 KB (53646 bytes)  
		MIME: application/vnd.in-toto+json
