## `postgres:13-bullseye`

```console
$ docker pull postgres@sha256:a1bf991d02568003f31699211492bfec4809bb752f34078db152f1536f11d665
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

### `postgres:13-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:6a166acd9b9060021db96756add2aee4b14e1f70148e59307066cbc6ba1ed864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140515289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92cb9392cd2d7e411b50b33898bcf7c7c6406688c078145af1cc9f3c45663868`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:16:46 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Thu, 09 May 2024 18:16:46 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg110+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94850697d474d16119934642abe999edeb3d5200e2438de0efedf87a8ddaa09f`  
		Last Modified: Tue, 23 Jul 2024 07:25:06 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25afba64e76dab1a6804df59103ba7a2b3323bd2cb6c7a1d834ef8a1b8c8a6f9`  
		Last Modified: Tue, 23 Jul 2024 07:25:07 GMT  
		Size: 4.3 MB (4308129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ddfa3246339550627de2bd1fb5cc4e48d6d56331d2bdfe98afa19b638e2648`  
		Last Modified: Tue, 23 Jul 2024 07:25:06 GMT  
		Size: 1.5 MB (1472146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7cce926e241dd09134919e0dcfd5688b7b7b8220a2f8483858fd025887628`  
		Last Modified: Tue, 23 Jul 2024 07:25:07 GMT  
		Size: 8.0 MB (8044467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5811384f33e978171ef55308c47724f97c45b5826e06c7d99124f5a5a536bb`  
		Last Modified: Tue, 23 Jul 2024 07:25:07 GMT  
		Size: 1.0 MB (1038351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c0807230225518b398a09c965e272b006b5e68fcccf4940ff2f6b4d60b1e06`  
		Last Modified: Tue, 23 Jul 2024 07:25:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8d0ae42d2c6618567a749625b5000859c8dddf07ecee87efdb384e0daa7c7`  
		Last Modified: Tue, 23 Jul 2024 07:25:08 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c0234bad226592ead9e33e569715e0a1f0f91568fc41fe825fc05b7aa07df0`  
		Last Modified: Tue, 23 Jul 2024 07:25:09 GMT  
		Size: 94.2 MB (94203679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9787a8f4c7a7c30fd2bbc681773f672c01d0cfa2d925587ed108b1b3892ba3`  
		Last Modified: Tue, 23 Jul 2024 07:25:08 GMT  
		Size: 9.3 KB (9349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da52fc7c63f59f59c1f135defedabdcc6f431eb92477eaa0918d712ef039e0b`  
		Last Modified: Tue, 23 Jul 2024 07:25:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af57035965c57a45dcf864b8a53773b292792d37fb9e9b3837815e5da8b98830`  
		Last Modified: Tue, 23 Jul 2024 07:25:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06285376f6c31e4614d32e1ae81630832c3644d0b075df4f3882135858e0dfe1`  
		Last Modified: Tue, 23 Jul 2024 07:25:09 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ed9bb087ed4f7a3cd716569fbc2adf99f8767f28300166ed079ddb3c6ca2e1`  
		Last Modified: Tue, 23 Jul 2024 07:25:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:15bc94408069b16da82b8d434ab001d093c87576b7937a147329b4d3d20c0eb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5895716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a23070cccee1ac61b107497b44d2be4fcb220d0d3ace873e871bfafa45e27ed`

```dockerfile
```

-	Layers:
	-	`sha256:4bdf11a71ad757c882e3bc6bbb96e05fd2613bb660e85840f4f4688b66f40510`  
		Last Modified: Tue, 23 Jul 2024 07:25:06 GMT  
		Size: 5.8 MB (5841407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff99307de2a84ffd30465b7a4808bad27f6748006cc8cc838e1bd9213fd6038`  
		Last Modified: Tue, 23 Jul 2024 07:25:06 GMT  
		Size: 54.3 KB (54309 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:e76130a4a20e9cab3f474bef9dd8f4b0222b47415048e752caaf46ce173d14d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133331598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d951152d08812a9b40f91816b9767a52cf584234685ef5b9e0866f962ddf7362`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:16:46 GMT
ADD file:56b9d2d0e0360f64ade3cbe073b446e10c8e6bd253b761c16b5f319a8103d181 in / 
# Thu, 09 May 2024 18:16:46 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg110+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5b04226d50f1c00a6c8950192ad70a2038016868ab6ffb162ad447e35e67a3cb`  
		Last Modified: Tue, 23 Jul 2024 00:02:06 GMT  
		Size: 28.9 MB (28930588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5636fe7fb7fba438c7fff4ddcfee0f950769f1572e054a3d895ee33d576339df`  
		Last Modified: Tue, 23 Jul 2024 10:53:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f10f6e1da99de5aa5d3d982890e58c6962a02891f4cce4bb77688d8f33b381d`  
		Last Modified: Tue, 23 Jul 2024 10:53:07 GMT  
		Size: 4.0 MB (3991608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2aa3c40e20f5f3327dffc32b8b1c66f26ef8d4aaf4cd5e576d84da4dba9031`  
		Last Modified: Tue, 23 Jul 2024 10:53:07 GMT  
		Size: 1.4 MB (1449201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05206ec3dc415525ad05c6213ca7c7edff1b0ad3b75090fad05459b03153f947`  
		Last Modified: Tue, 23 Jul 2024 10:53:07 GMT  
		Size: 8.0 MB (8044375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f373a46297041ce97551970eea6995ac0dd2be03aeb3954e26627ea46c4c5e62`  
		Last Modified: Tue, 23 Jul 2024 10:53:08 GMT  
		Size: 1.0 MB (1034855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08b1b6c925b6758a3783d57de9a41b23c931ea43a1eebf60c61ec22b81a6344`  
		Last Modified: Tue, 23 Jul 2024 10:53:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1809b06d89cb509ab3e6d5b275c306715b607a92c7dddd920e4109c96bfb21`  
		Last Modified: Tue, 23 Jul 2024 10:53:08 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba036cdcf460ea41dbc964a34819430f49171ca2b72f93ef8a5fa6ff83bf506`  
		Last Modified: Tue, 23 Jul 2024 12:58:22 GMT  
		Size: 89.9 MB (89860783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e4d29b9e09b3c4eee02b399bc68a4057b5767b015be8003cfb54b70b6f2839`  
		Last Modified: Tue, 23 Jul 2024 12:58:19 GMT  
		Size: 9.4 KB (9353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a2129a282cf9730c68c9b9f8b2f617e7225e877a6137a8df3b81aa0d57860b`  
		Last Modified: Tue, 23 Jul 2024 12:58:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c45b77853760e07486dc545273fde1433e5f74661c24d71fa830b64abe87a7`  
		Last Modified: Tue, 23 Jul 2024 12:58:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd5e7ae9c3cb32a7766f71763eba623e4a640a337251f92fa748bc144c61607`  
		Last Modified: Tue, 23 Jul 2024 12:58:20 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4247beceed6f3c127d035edf944709505294dee8508502457a54011aa91636c`  
		Last Modified: Tue, 23 Jul 2024 12:58:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:7860f7b6db7ceea31f7fa20e692c2baa5abaf05891a82fd450bc1ec00b5fee61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5906700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6bf88d641009211e2346de80d0b6f6614c3e28202779d8919a534d666255c2`

```dockerfile
```

-	Layers:
	-	`sha256:5d7cb1a1800f4b2f7d28285cb08d9ca8a0ded52bc95818bece7e828f6e9df8ea`  
		Last Modified: Tue, 23 Jul 2024 12:58:20 GMT  
		Size: 5.9 MB (5852194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb033ea9c72fd9dac34cb63b8a0b9ff37ebb35346f197f0c6074a2cfb289ca8`  
		Last Modified: Tue, 23 Jul 2024 12:58:19 GMT  
		Size: 54.5 KB (54506 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f810840b8488be10abf241194e40d63ae470a71d2c851bd1cceaaba7cc11fbae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128503000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba722f0a21f6ca14fb618d7e1d5f471da391d6864ee01cba2229c7b248b081d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:16:46 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Thu, 09 May 2024 18:16:46 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg110+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a6ceff8edfa750ec41669897e4e701509ef097630193d533de8ea51ff6be87`  
		Last Modified: Wed, 24 Jul 2024 03:39:29 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e3c70e15085f0d7cfa4a11ebe6ea4bdf616632f9fab54539d0f5670e2dfd28`  
		Last Modified: Wed, 24 Jul 2024 03:39:29 GMT  
		Size: 3.6 MB (3601652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6ce407350240883a0d85a2bb18df5e42164866c334150bb56d9beb535fd416`  
		Last Modified: Wed, 24 Jul 2024 03:39:29 GMT  
		Size: 1.4 MB (1439218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6748cd0342ebbf4e024b27e6894bf07906d06765820f6a2d412c238998b0c0af`  
		Last Modified: Wed, 24 Jul 2024 03:39:30 GMT  
		Size: 8.0 MB (8044461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2792c745a15d6a68fa6a3b6d207da9d1f882df4915155ab5c2c2eea9a11d7f9c`  
		Last Modified: Wed, 24 Jul 2024 03:39:30 GMT  
		Size: 908.7 KB (908656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a8f8e4de235d00231c2c22e12b5c1a449afd64936acae462870e6e167d0fcb`  
		Last Modified: Wed, 24 Jul 2024 03:39:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dd5431cf0e9ae7fc9e2a4b591d5f412ad214f2a3ecc9dd935661ad37631b2c`  
		Last Modified: Wed, 24 Jul 2024 03:39:31 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699e8cc3efdbe420adca9c5b23c87ff07509a318d3a22ff1f6d56cffd4b22231`  
		Last Modified: Wed, 24 Jul 2024 06:01:54 GMT  
		Size: 87.9 MB (87899684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5a0e392c1cc5691269a983fea11d6e1adbc2d553bc7d8e116b8239c8bd5a21`  
		Last Modified: Wed, 24 Jul 2024 06:01:52 GMT  
		Size: 9.4 KB (9360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e5cd6b5b6c32c325c9e3a4c12f84bb5f425435e2a02de7ace2dbee863ae06d`  
		Last Modified: Wed, 24 Jul 2024 06:01:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f769ee99a23004d6b8d02cb5aedfb6096bc711d30af234b0ad03c35e59a48da`  
		Last Modified: Wed, 24 Jul 2024 06:01:52 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c91985922db347f2e71aaba7a0993c01f60d95e6f2a2d7d997974c7d0800031`  
		Last Modified: Wed, 24 Jul 2024 06:01:52 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1024d81a92d25ee399570a4d4b9faba325ada7566335fe00776830135e21cfa9`  
		Last Modified: Wed, 24 Jul 2024 06:01:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:e21861158899ec3fc0799a9a89b071c9448a4c4274192d6aa2ddc9f1989a83be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5906320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9635026d563fdb26e417af2838b88f35e83e81aacd6d0a4d37acd529b7e710c8`

```dockerfile
```

-	Layers:
	-	`sha256:45dc56c56ea668d3c494968f6ae1effed0bb928d134c1d99c62b02cef581f13a`  
		Last Modified: Wed, 24 Jul 2024 06:01:52 GMT  
		Size: 5.9 MB (5851823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a431f5caed2c0623dafa45dc445d45b4d09632f318b3e55584b0cb817fde0a7`  
		Last Modified: Wed, 24 Jul 2024 06:01:51 GMT  
		Size: 54.5 KB (54497 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:57cd1584ae82c2bc130ccc5a42a923e14ca79fcb2536a76067aab4403bfd97c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136919439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc46c1f23769a98eeb0fb36cb8820515d758e8cf8dafca7f6195db7d010c1c7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:16:46 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Thu, 09 May 2024 18:16:46 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg110+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19038ac1efe14f19c7cbe45834b058dd9527627f20b3cd2a131c13434b92051`  
		Last Modified: Wed, 24 Jul 2024 01:17:44 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fed0335853272002eb1b2b202e1c538634d28290ba5cdf05db00ebb18e5f585`  
		Last Modified: Wed, 24 Jul 2024 01:17:45 GMT  
		Size: 4.3 MB (4312724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e4072212783931be3ff566c4dfbd71d8c0b6d9cc088cfdec25e0018208d773`  
		Last Modified: Wed, 24 Jul 2024 01:17:45 GMT  
		Size: 1.4 MB (1404113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edea8b414874235fcd6d9d410603fb395171dcc4109de96a099590d8c9b9b79`  
		Last Modified: Wed, 24 Jul 2024 01:17:45 GMT  
		Size: 8.0 MB (8044287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9108dc601dd847564887d7670935575884d6ba278aab629656b4956574a220`  
		Last Modified: Wed, 24 Jul 2024 01:17:46 GMT  
		Size: 1.0 MB (1026607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bb8f7e4d75b0c7087787c914fa12e12c3a686efa4413f95bf8664038d2e6f9`  
		Last Modified: Wed, 24 Jul 2024 01:17:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f9fc3697a9c79dadadd444099556e8d7555790eb19e553e56a216266c6cf63`  
		Last Modified: Wed, 24 Jul 2024 01:17:46 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da91b0c9a2b6df0f5d33bb0efacf6157f050b4f00deecb25d9dee71dfcb939cf`  
		Last Modified: Wed, 24 Jul 2024 01:48:56 GMT  
		Size: 92.0 MB (92035426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f47c7e1d76c9fb72c199b4076ef2c4ab5cd943d022b5d876dd1f2d865c3b943`  
		Last Modified: Wed, 24 Jul 2024 01:48:53 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5707c2df100b39c9c46e61ae9d98378eadc37c6600bcf178491fb2434c35984e`  
		Last Modified: Wed, 24 Jul 2024 01:48:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36117502975e9177749b9cc743c7bb2fc7361339384ea5dd0a2582d250406b4c`  
		Last Modified: Wed, 24 Jul 2024 01:48:53 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc709b22a77e5728e9d702457eb629df249f483fe1bba92a29672f7432e864b`  
		Last Modified: Wed, 24 Jul 2024 01:48:54 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f6cd577309ceda1e7568a06c05f2e0d5c937f09abcabc33edbaf630d69efca`  
		Last Modified: Wed, 24 Jul 2024 01:48:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:76da84026d613356f3fd6648369c65e3bfa100e0c6cb52942078a6be96e7f5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5902289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c7a7ad03efe5f952c6415c8bf5996314e6090df9668bf061be0c323a5b6fcf`

```dockerfile
```

-	Layers:
	-	`sha256:acd05a19a601b94f8af31c576c8d45330ab143b0e2e6e6953e1230a7f9a10427`  
		Last Modified: Wed, 24 Jul 2024 01:48:54 GMT  
		Size: 5.8 MB (5847697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1315ac245b91d359d6307c3774b5d90e6a6a634c761e37815a51ddafc2d93e`  
		Last Modified: Wed, 24 Jul 2024 01:48:53 GMT  
		Size: 54.6 KB (54592 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:71ad1f6eca0e9647734916dac180e7de9cdda73040e58636fd6c939b70ac6ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143086835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc2b76863e62ee7f6b26f5122650bd3ac59e3396b4278fe05c5cc61975bd2c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:16:46 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
# Thu, 09 May 2024 18:16:46 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg110+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8950000bd8dd16aba99e3dcdf446ea9ae8fcf047cf6bf0fd3e727229356329db`  
		Last Modified: Tue, 23 Jul 2024 06:21:28 GMT  
		Size: 1.7 KB (1673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c70c312d6d7d9d5e5b2fcf331b3d3ad1f9e8ef58cfbef4dfa687e4eeaba1fe`  
		Last Modified: Tue, 23 Jul 2024 06:21:29 GMT  
		Size: 4.7 MB (4719588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d85c791a39f664c4bc58f0064ab31c2a9172b5dcda423acc29b5faf7c0724b`  
		Last Modified: Tue, 23 Jul 2024 06:21:29 GMT  
		Size: 1.4 MB (1447761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c778988774ccdc8bf21ab381969df243d399f29a1ff5734e4e4e934aebe3c1`  
		Last Modified: Tue, 23 Jul 2024 06:21:29 GMT  
		Size: 8.0 MB (8044366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26505ec3383eb5fb87acb6a0143e091c4e7b75d74b47fe65c55e1d6191d3502d`  
		Last Modified: Tue, 23 Jul 2024 06:21:29 GMT  
		Size: 1.0 MB (1028890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b31f3e1e178d9ff3100b36d7c637523434d9758bad04baf9e68706c56e13e`  
		Last Modified: Tue, 23 Jul 2024 06:21:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638d030d2d9f55e8a548e3fd4ec4eddaf4f8bdfa696df7c9088075d4338f9a2d`  
		Last Modified: Tue, 23 Jul 2024 06:21:30 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c765ecf0c15a43adf8a7945e6878953d69436aada58be7e33e3bf9f5845afe`  
		Last Modified: Tue, 23 Jul 2024 06:21:32 GMT  
		Size: 95.4 MB (95412237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0c215f83f6a50149be2d0c129093669fc95bd4138cd0773bca4d1a5f38a62`  
		Last Modified: Tue, 23 Jul 2024 06:21:30 GMT  
		Size: 9.3 KB (9348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443904992a233fe9464bbe2c3983acc0adc770980a6c16bd1d41dfd179e998db`  
		Last Modified: Tue, 23 Jul 2024 06:21:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6a8427bd500ee06ba07031a8167152d76830ae3414c756e8fa806312911be6`  
		Last Modified: Tue, 23 Jul 2024 06:21:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b01cc6eeb5e2a7b3b860ea82b69b7a101e8b53d427268f6b53368997b2bb0f`  
		Last Modified: Tue, 23 Jul 2024 06:21:31 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42b342fb30f51039a3f54ae32c1342408f1688fdb3b8f1775819f8ab20983e1`  
		Last Modified: Tue, 23 Jul 2024 06:21:31 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:05e68684b40eff83afbd4c724f410ac335e67e8a1a729e7026e45bfb3c2ecff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5903782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1057010c370355a9399f3af9637c9c021a7d28c608cf11eac207dd0f82136a22`

```dockerfile
```

-	Layers:
	-	`sha256:0d10f2c1f2a02b27e06589a20bd7f15b31123647d6eb40136928bba6443bd4b2`  
		Last Modified: Tue, 23 Jul 2024 06:21:29 GMT  
		Size: 5.8 MB (5849514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb7f5ca6f94fa82f6e006b00679e878c297f84494f691d9d8e1be7b9391cfe66`  
		Last Modified: Tue, 23 Jul 2024 06:21:29 GMT  
		Size: 54.3 KB (54268 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:710407d5194374e689bb56a10d76ee5fa9037cc57c5c3230475945984e198f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134816894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a21cf71ac6994c1d97338e467556bd1e56c86dbba4641c515177da37d16e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:16:46 GMT
ADD file:791d05eca72cc81080afbb76c7f3f02a74893142203b6aada9e3170404049223 in / 
# Thu, 09 May 2024 18:16:46 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg110+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:59602b870d8ca1e13dffda9de0c5f866f86ff35c1e595ea481bb1b2c48c18b8e`  
		Last Modified: Tue, 02 Jul 2024 01:30:52 GMT  
		Size: 29.6 MB (29639850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e82d37477e5611a05dbd2d1b5b95fd1fc925e36f5a97163d218cc3da2fe380c`  
		Last Modified: Wed, 03 Jul 2024 11:20:15 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a35da21ac3868b9a5da909aedb9c7fca0f566de5d3d22e2ebc0c9f45b7e9842`  
		Last Modified: Wed, 03 Jul 2024 11:20:15 GMT  
		Size: 4.3 MB (4308349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61600c8afaae23a0cca79f401a23cc1ecc13a99618b74296b698e01282c024a8`  
		Last Modified: Wed, 03 Jul 2024 11:20:15 GMT  
		Size: 1.4 MB (1359393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bdf6a84e543068f926a3c15a3a91c6c9b8b9d29f328b0383a51be10384744a`  
		Last Modified: Wed, 03 Jul 2024 11:20:16 GMT  
		Size: 8.0 MB (8044900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a86f132c61e5efaa7825c2043f4a1fe9651d2cd276ca6ab25bbddb00b6cd866`  
		Last Modified: Wed, 03 Jul 2024 11:20:16 GMT  
		Size: 1.1 MB (1090305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8c0b5d5c85fa94f326b8fbc99592016d78d11f3209c7578ee9c5ad4ef2f6df`  
		Last Modified: Wed, 03 Jul 2024 11:20:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91e784d0bf01d660fd75c7d204d9673fb5a51295e7df8522c48533736d303c8`  
		Last Modified: Wed, 03 Jul 2024 11:20:16 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c30d1a740b31ef7ba6db0179ebec010533d07d774c3762a174639105bcae78`  
		Last Modified: Wed, 03 Jul 2024 15:38:16 GMT  
		Size: 90.4 MB (90353880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64e7403bc9146fab2a0af37a61458c8ce534852be28cab6d6d6e52b013faac`  
		Last Modified: Wed, 03 Jul 2024 15:38:08 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17f94f0472ae8512a6994638971fd4033463199ebaf049f07ff3ef0f3011a01`  
		Last Modified: Wed, 03 Jul 2024 15:38:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdaf44f0acab0b303f09ccf41cc2bb46e511d461593b9f574c2e7479bb88a39`  
		Last Modified: Wed, 03 Jul 2024 15:38:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a742bcfa0d209fa091bcd71c7f6ad475ffd4ad08b988291e49a1f1d0a7cf9595`  
		Last Modified: Wed, 03 Jul 2024 15:38:09 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8c51cded774c56db3ba015dff2df505358e8cbbf0859df49209dde1ea9399e`  
		Last Modified: Wed, 03 Jul 2024 15:38:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:ccd51846203d5d1d6976ebf32e234c2cb3e723ca77a900b4f76eceb1b65fc0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 KB (54161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52836590c154caf878ff76a9457ab6948367df53c186115c5a67e9751be9d29a`

```dockerfile
```

-	Layers:
	-	`sha256:b62d51310d81a9202e36c28fb6cb474f0b1776a81594474e6f7e4e8bc61d930b`  
		Last Modified: Wed, 03 Jul 2024 15:38:07 GMT  
		Size: 54.2 KB (54161 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:05dac2e353057336059087110d6fdea36260486fd3994161db3c8ca3c20589d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151337773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93411b09ba2460bdbb1c1633ca6fcfe66611cfedec71b6464d2d549421ac45f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:16:46 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Thu, 09 May 2024 18:16:46 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg110+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a92aeac617d879925b9a88d57f1c8664df54f3425c22018b491d90ecd546c9`  
		Last Modified: Tue, 23 Jul 2024 23:16:23 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6011eaa530ee4bbf244680e54c17d0e3fbbf42306a6aa669be940ad1f8ea311c`  
		Last Modified: Tue, 23 Jul 2024 23:16:24 GMT  
		Size: 5.1 MB (5137826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d96478163bd229bf7e8a8d48c4206a53baea289c564c955adb2f0ddae5da308`  
		Last Modified: Tue, 23 Jul 2024 23:16:24 GMT  
		Size: 1.4 MB (1393639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1deb0412097ea36dfece1de41c99f4c43d276b619fcde3629962ab7fa52377e`  
		Last Modified: Tue, 23 Jul 2024 23:16:24 GMT  
		Size: 8.0 MB (8044537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad760215c33555bd2edfee360447473f37dde1c4d28365229c93857f1f1c8fa8`  
		Last Modified: Tue, 23 Jul 2024 23:16:25 GMT  
		Size: 1.2 MB (1197556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3399a9f34d32e48471c3c520768cd8a61cafd5d7db969e0edfc8916abb59b7a0`  
		Last Modified: Tue, 23 Jul 2024 23:16:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba053f93a2baa0751ced12a029af4e4ca8e2aa1d9577508b34028bcc26d256f1`  
		Last Modified: Tue, 23 Jul 2024 23:16:25 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3961c77a149a1c03dcd6210b5334045b16a62bbd2e734b01a715e9a37e7c221e`  
		Last Modified: Tue, 23 Jul 2024 23:54:42 GMT  
		Size: 100.2 MB (100238814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe82c224756ded71abecfe0b85a3958203b5bf36feb562894d66bce404c89f1`  
		Last Modified: Tue, 23 Jul 2024 23:54:39 GMT  
		Size: 9.4 KB (9353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa05d5e012076786468f0dd700175b0211c64ddc9a90ab8a68479ed3a2886f7`  
		Last Modified: Tue, 23 Jul 2024 23:54:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b784ce44b2dfbcd9afb6698e755ae7d088dc49fefdd3a393e91a966a144118`  
		Last Modified: Tue, 23 Jul 2024 23:54:39 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad838fe93769075837c1d1a3b56eb4a47daa30775b40d0a321f0eecc6230e39`  
		Last Modified: Tue, 23 Jul 2024 23:54:40 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e3795c7af6e47ad4c5ba268f55ba5eeb4bd7467071e98f932b9e73f1f13754`  
		Last Modified: Tue, 23 Jul 2024 23:54:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:8592230608fd2cbdf91893a663a11c36eb7470618cb0da19f6553b68ac6079d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5902902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33151d40365f6d23155481abcca36b682c4b5127003d7eb6738b19fc558c0b3c`

```dockerfile
```

-	Layers:
	-	`sha256:158275c447aad7c2755d21636a4ab03cd23d52df5253199d57d704764f680270`  
		Last Modified: Tue, 23 Jul 2024 23:54:39 GMT  
		Size: 5.8 MB (5848539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4bf92b1665d3328b08f91afa17ab7b8cdc2926b32b03b39b7a1f62e6fd9f1cc`  
		Last Modified: Tue, 23 Jul 2024 23:54:39 GMT  
		Size: 54.4 KB (54363 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:d086aa2c5f51746b679abab34d07c5acccdea79c2b7ed917a81bf564f2eb14e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144840771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fba33c406fa9dcd9dd01cf184cede4ddd9550dad7ceeff0da2880626e9d7eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:16:46 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
# Thu, 09 May 2024 18:16:46 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg110+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:de4a305fc1af45cc7ae97020dfe639e8990f6d00b7e0ef222c4cdd720f0fc373`  
		Last Modified: Tue, 23 Jul 2024 02:33:12 GMT  
		Size: 29.7 MB (29669018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a172539f1709f75df0b591bb0cf689728fb88fd1939ef1966cb706068621afe8`  
		Last Modified: Wed, 24 Jul 2024 02:21:00 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8454328de91698bb71f98979f85addce4732cd3fcef8209931072e6983c7eaa`  
		Last Modified: Wed, 24 Jul 2024 02:21:00 GMT  
		Size: 4.2 MB (4200368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87c2da79a7689187e7ced54dbd567387cfbec7e081caba7841c8f036f48c0a5`  
		Last Modified: Wed, 24 Jul 2024 02:21:00 GMT  
		Size: 1.4 MB (1437992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e0120c75629eb8fca814e4189ea4221115eba8ff72e5ecc548c716e11815f`  
		Last Modified: Wed, 24 Jul 2024 02:21:00 GMT  
		Size: 8.1 MB (8098825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f317afaa53c81db5ed105efff6b0b0a9e1858569500d2e3cf443135f4ab2228f`  
		Last Modified: Wed, 24 Jul 2024 02:21:01 GMT  
		Size: 1.0 MB (1015266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0672758bd603c67a07cf9ffd540e14c74a0e1570e01c72a1889947b933bdcd80`  
		Last Modified: Wed, 24 Jul 2024 02:21:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cda8ea681ff42590b0458067dd85dbfdf10962ce02e77add87bb59e514af888`  
		Last Modified: Wed, 24 Jul 2024 02:21:01 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9b11925b921ade67840ec5d5783294474f7e9a4ff07722cb722e3deab71687`  
		Last Modified: Wed, 24 Jul 2024 03:02:52 GMT  
		Size: 100.4 MB (100399100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3bda844b66d82996be5b2b35910ca1c2a472fbce9458b8448517acad233e54`  
		Last Modified: Wed, 24 Jul 2024 03:02:51 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec5383dbb9f1a1e39aa2650c714d6b0c89ba4c66aa0d8a8210fcd1a18008605`  
		Last Modified: Wed, 24 Jul 2024 03:02:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cc1590c7af6f20b70f4ecd37f92818406192c8c6fa19c088b116b7d64c90c7`  
		Last Modified: Wed, 24 Jul 2024 03:02:51 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dda0ba073ffcfb56b8393d4a7e22d9c07277b19b9b9f5e4d52f1279e5d1c14`  
		Last Modified: Wed, 24 Jul 2024 03:02:51 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e999f352bf99ac1d42aa6db66e1a9a134985ac238f6be3a8a44879943c95700e`  
		Last Modified: Wed, 24 Jul 2024 03:02:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:cf053516c74c97edd62de3fd3673d769c4b93a9e102ab10f6e3969677207c9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5894699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd1eabe9072674010fa44a8e5bac41366de866f62ae74b71d0c1f1a9aca2dc1`

```dockerfile
```

-	Layers:
	-	`sha256:c5f99300952c47de6351fc4a3e3730b41697f8d89b5b40df9b71fb6e14dcb194`  
		Last Modified: Wed, 24 Jul 2024 03:02:51 GMT  
		Size: 5.8 MB (5840384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3790141cbe566fe2df6b1870942fe6d2db6e11054b81cf6c3be42dc5026d2273`  
		Last Modified: Wed, 24 Jul 2024 03:02:50 GMT  
		Size: 54.3 KB (54315 bytes)  
		MIME: application/vnd.in-toto+json
