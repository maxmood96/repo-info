## `postgres:17beta1-bullseye`

```console
$ docker pull postgres@sha256:90288190bc963864a0e4f929f1bcb63bac20ca499bb1cc950826dd666232aa37
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
$ docker pull postgres@sha256:18471ca34203f0acb54ca84b1e2dbf80a6a8a7e49b98d3d761924f0e90b8f2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133990641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724b58d899fd7cb954747574dafcf7d2282004ebf752ca9752d376162ae65acc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:b23992f77c1f22e7bf9048641d6da1d6ef922d78b4118f6d513e183ae6de7e34 in / 
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
	-	`sha256:4873d96591a32d2d686ff6c86338fc9a63b9d60639482601b5402eb76e56a566`  
		Last Modified: Thu, 13 Jun 2024 01:02:22 GMT  
		Size: 26.6 MB (26594507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2931fa25f098cfb85a9e2ab63b32f42e0a38d948de08037ebaf41564215be3f`  
		Last Modified: Fri, 14 Jun 2024 01:31:38 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af708d144a1736f39af6b983593190d32710b24784ff0d548a5ff97684bfef9c`  
		Last Modified: Fri, 14 Jun 2024 01:31:39 GMT  
		Size: 3.6 MB (3601619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126dbb3b6030510a22eabb64c1c168ac4ff657d79a006f5824746e1c2fd5e340`  
		Last Modified: Fri, 14 Jun 2024 01:31:39 GMT  
		Size: 1.4 MB (1440825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bacc00ecda8352e7b3e2312653e32de97ad93d9ebc13319ae22edea2b44667`  
		Last Modified: Fri, 14 Jun 2024 01:31:39 GMT  
		Size: 8.0 MB (8045802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55803590f5e2c3a873bdebf5238649577ec4b5f0d628ee528df9ac7359fd8ed`  
		Last Modified: Fri, 14 Jun 2024 01:31:40 GMT  
		Size: 908.7 KB (908660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b80780e0a0bbdd60caaeb103723853e5e2db82c08827db79ab4a0cec61215ad`  
		Last Modified: Fri, 14 Jun 2024 01:31:40 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d224aa4d57d0a54614dfc9293cd5826927f9325c08c29f8cc32186695f06631e`  
		Last Modified: Fri, 14 Jun 2024 01:31:40 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdae0721e6a5168e80c129d7ca31f36d203beb3ab452b84880210bd4a3714c43`  
		Last Modified: Fri, 14 Jun 2024 01:31:43 GMT  
		Size: 93.4 MB (93378148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e5944d0cc706fea05697cbd5b5e94c46bfb382a81e25cc053ded3850c0da70`  
		Last Modified: Fri, 14 Jun 2024 01:31:41 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f1a5fbf56334511a8cbf54a4023fd9b38e3dcb7460abbeb8e5235e481b8381`  
		Last Modified: Fri, 14 Jun 2024 01:31:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9a574c5ff4657e46ac07e721dc3492a5b500486479e5caeb66708ccb08a92b`  
		Last Modified: Fri, 14 Jun 2024 01:31:41 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ac4caaf00f79e60a6904bad35ee936043fae4fcb21a8c4dc592fc18ef40511`  
		Last Modified: Fri, 14 Jun 2024 01:31:42 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88eb3a01ede5a5ec322f002e15220f16443bb080b6329ecd8c07fa60187b819d`  
		Last Modified: Fri, 14 Jun 2024 01:31:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2e0da4ee317ce17268c7fcb11e328a0ef93ea7c2a5e6c337ac83335f612337f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6045479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b13a858594f07e88ff56f4e7f7dc2e3e708b3aaedfee58506a17da344f580c5`

```dockerfile
```

-	Layers:
	-	`sha256:412205a5b4975339e79713474a9a67432df8a5683f838e11868859503eb6f74f`  
		Last Modified: Fri, 14 Jun 2024 01:31:39 GMT  
		Size: 6.0 MB (5991659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48232a0054be17ea55dde0df411ea6a9441d792b1f3c49794d5e8cb7b3e0809`  
		Last Modified: Fri, 14 Jun 2024 01:31:38 GMT  
		Size: 53.8 KB (53820 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:970fd9ce8fc8deb85aafdeb3bdd0765b4788f92de36d6dfa25c96a9ed55d22c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142383628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266957802d59edbc048bb7efbbfbf52e9db64c624a0e5cc362eeab25214d1bf3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb28ca68ecfc3c03e505d7540fe02a380ef93dfab58facb8e40674c120c35de4`  
		Last Modified: Fri, 14 Jun 2024 00:42:15 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbd6a6f4ffc2265f4e7190df83c0ebedc51b62f181cc5519e69ecec44873012`  
		Last Modified: Fri, 14 Jun 2024 00:42:15 GMT  
		Size: 4.3 MB (4312765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1c1745601ba7fc2a64b9a3ad7f1a22c9eaa21bb0b557adafa57fb5199eccf0`  
		Last Modified: Fri, 14 Jun 2024 00:42:15 GMT  
		Size: 1.4 MB (1405900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1295861d7380761e55795e2be158e67ddce9cab82d0a361b18ec1b4987da6aa`  
		Last Modified: Fri, 14 Jun 2024 00:42:15 GMT  
		Size: 8.0 MB (8045779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c5f02f0c267ddda7903b8d1c3fd583d4c253988b1bf1372e28704efff61982`  
		Last Modified: Fri, 14 Jun 2024 00:42:16 GMT  
		Size: 1.0 MB (1026604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514b106d79ccc7563e64bcef8d04a100acdafb5f318590284727ecbf6637d1c8`  
		Last Modified: Fri, 14 Jun 2024 00:42:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1ec2b6225396907d9fa7a99e8243c694ee1e58117218df87093b57e0130d43`  
		Last Modified: Fri, 14 Jun 2024 00:42:17 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad1c960cb3d8faaf12f87035ef855da6f743663c62973b72bd91cfeb8aa126a`  
		Last Modified: Fri, 14 Jun 2024 00:42:19 GMT  
		Size: 97.5 MB (97484520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad3c520880d1f8008ef7baefd082a8fc9d8382e6c015a6b726d8666e20c9108`  
		Last Modified: Fri, 14 Jun 2024 00:42:17 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29c6cc7aeff5a1ecfccb2b05078cb4375ca3c2d02b468bf7b4d336800956174`  
		Last Modified: Fri, 14 Jun 2024 00:42:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350258860a5dbbfaecfd4c3b1f028bab174f1c4d300bd542f70a5795865f67ba`  
		Last Modified: Fri, 14 Jun 2024 00:42:18 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013c1bf2402aee09f33dca67cb096d588f5d8d62c5734a0cdb35d0d35f487fba`  
		Last Modified: Fri, 14 Jun 2024 00:42:18 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda130bf4edb9a2b215e3b93358e828f57205d4429d68fb19d72d99bb1af290`  
		Last Modified: Fri, 14 Jun 2024 00:42:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:b0de6e2193e3f8143adc3bc0943643fd44ae77c69e4997805fd9b6c22c75f94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c46451cc607d52187020c4ec9e9db45e2558e87bcd895455da43709d553c641`

```dockerfile
```

-	Layers:
	-	`sha256:d8f5a863e4d7405b9b636b2624ca87a33f5473178b49039a59a4a6570957904a`  
		Last Modified: Fri, 14 Jun 2024 00:42:15 GMT  
		Size: 6.0 MB (5981073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b43deb88b281e78ef5d1747e6f2515ccb17c115a42575d5c87c0cb47294ae3c`  
		Last Modified: Fri, 14 Jun 2024 00:42:15 GMT  
		Size: 53.9 KB (53913 bytes)  
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
$ docker pull postgres@sha256:fa547d1146c8fd9cfffb12082fa83e3423e5119477bb03bf1eb08a3f120e56f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140323911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326372c95115ceeb54cd52f91b3eef5112faa950ba7210292c51679049d34c54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:008c77755df91bc808f2edbc05df1da6419d984abea862dbf73f345500433eb9 in / 
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
	-	`sha256:1b4876387959ae765d8f504e4352c8f85ce0ad5a78eee29be84300f85cfdf0a6`  
		Last Modified: Thu, 13 Jun 2024 01:23:19 GMT  
		Size: 29.7 MB (29651863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fd900b2a4831cab5b1f7cc37454db9ef7773e26c9d69e962517a329864eba8`  
		Last Modified: Fri, 14 Jun 2024 17:34:05 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce93f700666303efc0aff13afeb0cd1c6654d2d9572801b03332433b9c5b969`  
		Last Modified: Fri, 14 Jun 2024 17:34:06 GMT  
		Size: 4.3 MB (4308297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2c9850797a6a9d93cf5a4eb3dcbb9e3a44c138d71f1f56f042ff9151421af6`  
		Last Modified: Fri, 14 Jun 2024 17:34:06 GMT  
		Size: 1.4 MB (1360880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afda38acc11d725297a1ae0b18898e6a1ea52612a81f8d00f892bd88b3ce3b0b`  
		Last Modified: Fri, 14 Jun 2024 17:34:09 GMT  
		Size: 8.0 MB (8046118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e385d90ce8d0d391a189eec4cb6101f676c11a9eea699a2fd67420bbe2a81a`  
		Last Modified: Fri, 14 Jun 2024 17:34:07 GMT  
		Size: 1.1 MB (1090256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced90b1832147c719fcc4e83397006dc5f75cdb7abb17456bbaaed0b46d683a4`  
		Last Modified: Fri, 14 Jun 2024 17:34:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72eeadba7ae21f9006428808020f85525933ab5613405e67b6855d3bbeaa7d97`  
		Last Modified: Fri, 14 Jun 2024 17:34:07 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4b90aab23c2a367b85d8b9970d97a75b07d38157bb06dfc0d53e6533884e37`  
		Last Modified: Fri, 14 Jun 2024 17:34:17 GMT  
		Size: 95.8 MB (95845401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994b2cb16c732191711581245b139f95c8bfde56a4001c07d023706eb2473d4d`  
		Last Modified: Fri, 14 Jun 2024 17:34:08 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8f7a4712581d11f18f58bfaf54705ebacdab501a4c44fd32c757182aefb5a8`  
		Last Modified: Fri, 14 Jun 2024 17:34:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd06a1787e22773ef59347cf4a11767ce5a7b8184e1937748ce3117c01f8b52`  
		Last Modified: Fri, 14 Jun 2024 17:34:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bc981373dde968aa5f7e6bd147189caba1d7de7472f882c239d9bbc3f900ae`  
		Last Modified: Fri, 14 Jun 2024 17:34:09 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5229c56a3d927ecdc2dd6134c0068dfc6d703a18b5754884ae08eacdae5bbb`  
		Last Modified: Fri, 14 Jun 2024 17:34:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:87be9b574dcd3da7c9dbe3e14e71bf36f415f51fb89a51dce8bea9247b81c695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 KB (53483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352cc634b98ad29154eb654f50f7496e2db376cc5ad598694c7da5fe3efbf3dd`

```dockerfile
```

-	Layers:
	-	`sha256:4c80d81267689145af9a15f45ac0c026dd74a1516835389bbcef7f1634986908`  
		Last Modified: Fri, 14 Jun 2024 17:34:05 GMT  
		Size: 53.5 KB (53483 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:99ff935ca668148f7e241cdf774c9c7741cb46fe28513e717dc6e0fa04f09991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157030601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224a21ba07bc8793f049c7ee98a4e4df8dc7f540fd1703ed5ec90ef119f0095f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
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
	-	`sha256:64741f366161eb41a5c86810e08ceabb9f4e4b69ac16c725aa2d48f19486e1be`  
		Last Modified: Thu, 13 Jun 2024 01:22:19 GMT  
		Size: 35.3 MB (35311302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2b27527c85d2cd6dbc22590bb8bdaa83412b625fa9eb9c3136a6ea1d2ab417`  
		Last Modified: Fri, 14 Jun 2024 04:53:08 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d59e63a6c9d9b7d07cc29c879a8ba8b2f01c2c5a7d27b49b1684c9c99dde8f4`  
		Last Modified: Fri, 14 Jun 2024 04:53:08 GMT  
		Size: 5.1 MB (5137838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db27b988c1740fa964246c40f525184c3a4bd5d02e71c1ddb93e7dc766e71de`  
		Last Modified: Fri, 14 Jun 2024 04:53:08 GMT  
		Size: 1.4 MB (1394889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a2e840b112cc0605e96f9254ae319457686607b4f61660d30b406a87ab6ffe`  
		Last Modified: Fri, 14 Jun 2024 04:53:09 GMT  
		Size: 8.0 MB (8045823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701ed289d9fb0fc99d416404e76f755c0b41702540e5c973c28bbb04d95f2e4c`  
		Last Modified: Fri, 14 Jun 2024 04:53:09 GMT  
		Size: 1.2 MB (1197528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d9c03ac9f93f939a8f71c48c62951ffabf9bfcaefc17e328d55dd8c78b4b06`  
		Last Modified: Fri, 14 Jun 2024 04:53:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de3bac2076690319e00d5e3ed8e3e971f68656b2690d2ebc24fefe15d527a70`  
		Last Modified: Fri, 14 Jun 2024 04:53:09 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e754cf75f6ecc583c782416d68613e48e132a8803e5be7eb69d9d284f01ddd4`  
		Last Modified: Fri, 14 Jun 2024 04:53:13 GMT  
		Size: 105.9 MB (105922135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fa4881a20b808179e4a6456e0f8e3ad4b98d5b4f29eb4e4be482235937f95c`  
		Last Modified: Fri, 14 Jun 2024 04:53:10 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc9b3bd936b37dab6d91f7ae7b30854b4efade3b9e420385dedcc1cd8aa2555`  
		Last Modified: Fri, 14 Jun 2024 04:53:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef1f912eb774e7f2a77db2cc0165183c45b6d767abc7411537db0d4a03eeb81`  
		Last Modified: Fri, 14 Jun 2024 04:53:11 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3498a18a104c952c2c8464e30fe1f6c6df00e40182ec8b6d2d2b51873209342`  
		Last Modified: Fri, 14 Jun 2024 04:53:11 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b980ce67fb99540e5654db2ef5d91d0833834e4e0403ff4f1fac9c8042bfa0a`  
		Last Modified: Fri, 14 Jun 2024 04:53:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:045311e11b92b359c9854d158e2902776da5864f3b76495467f16ae90a2d5b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6035609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a45239fa9d7db219502241564bcee23edfc4b71179ef7b5de712a0ab19c3d9`

```dockerfile
```

-	Layers:
	-	`sha256:c50bd4262577cb0edc37ec5b71886c568d10b7d0963a0a72899addad1218c072`  
		Last Modified: Fri, 14 Jun 2024 04:53:08 GMT  
		Size: 6.0 MB (5981921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a6416404f3b88aa860a691ca6807503650225d7e4cdbbdee3867781b456172f`  
		Last Modified: Fri, 14 Jun 2024 04:53:08 GMT  
		Size: 53.7 KB (53688 bytes)  
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
